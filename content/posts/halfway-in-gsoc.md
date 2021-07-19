---
author: "Ankit Hans"
title: "Halfway in Google Summer of Code"
date: "2021-07-10"
description: "How is google summer of code going with aerogears(RedHat)"
tags: ["gsoc", "opensource"]
series: ["Google Summer of Code 2021"]
ShowToc: true
image: "./gsoc-jboss.png"
thumbnail: "./gsoc-jboss.png"
---

## How is GSoC going?

My experience with **Google Summer of Code** and my organisation **Aerogear**(JBoss) has been so great till now, learning new things everyday has really became a part of my life. 

It has been almost 2 months since I got into the program, but it feels like tomorrow! When I started contributing or writing proposal, I was like zero in golang, but comparing then and now, it's different. In this journey I got to know about some great concepts in golang and again many yet to be explored! 

> My favorite part about the Google Summer of Code is you work on projects are are used or will be used in the industry, and this feeling makes you keep going. We have integrated some features and are planning to integrate [Charmil framework](https://github.com/aerogear/charmil) with the [RHOAS](https://github.com/redhat-developer/app-services-cli/) and [Apicurio](https://github.com/Apicurio/apicurio-cli) CLI's.

Need to achieve much bigger targets/goals in coming coding period! Let's hope for the best 🤞

## Again and Refined - What is Charmil?
![charmil-logo](https://cdn.discordapp.com/attachments/852928325197234256/866662720711688192/logo_cropped.png)

I have talked about Charmil ie. my GSoC project, in my previous blog, but this framework keeps on refining each day and there are some info's that needs to be updated. 

> So **Charmil is a Framework for building command line plugins on the top of Cobra golang library**. 

Cobra is standard and very famous in the CLI industry and is being used in many industry projects such as kubernates, rhoas, gh-cli, etc. To make the development process easier we introduced Charmil. 

Charmil solves many problems/issues faced by developers during development of CLI's. The major feature that Charmil brings on the table is the **ability to develop multiple fragmented CLI's, maintained/working in separate repositories, and later embed/combine them in a single Host CLI**.


## Charmil Components in brief

![charmil components](https://cdn.discordapp.com/attachments/852928325197234256/866662699315757076/charmil_pillar.png)

- **Charmil SDK** - For building mutlirepo CLI's
- **Charmil Validator** - Cobra Testing Library
- **Charmil CLI** - Creating starter and managing CLI project
- **Charmil Command Registry** - Install CLI plugins with binary from maintained registry

*For detailed description visit [Charmil](https://github.com/aerogear/charmil)*

## Charmil Validator

This is the charmil library for **testing and controlling many aspects of cobra commands**. Like to test react components we have react-testing-library, similar to that to test cobra commands with some given set of customizable rules, we have charmil validator.

Validator provides a customizable set of config attributes, for example - 
```go
ruleCfg := rules.ValidatorConfig{
	ValidatorRules: rules.ValidatorRules{
		Length: rules.Length{Limits: map[string]rules.Limit{"Use": {Min: 1}}},
		MustExist: rules.MustExist{Fields: map[string]bool{"Args": true}},
		UseMatches: rules.UseMatches{Regexp: `^[^-_+]+$`},
	},
}
```

**Rules provided by validator** -
- LengthRule
- MustExistRule
- UseMatchesRule
- ExampleMatchesRule

It is recommended to use Charmil Validator while writing unit tests for the cobra commands. Validator can check if the commands are **providing proper and latest documentation**, **length and presence of attributes**, **regex matching for command names** etc. It also provides the feature to *skip some command or skip including children for validation*. 

```go
validationErr := rules.ExecuteRules(cmd, &ruleCfg)
if len(validationErr) != 0 {
	t.Errorf("validationErr was not empty, got length: %d; want %d", len(validationErr), 0)
}
for _, errs := range validationErr {
	if errs.Err != nil {
		t.Errorf("%s: cmd %s: %s", errs.Rule, errs.Cmd.CommandPath(), errs.Name)
	}
}
```

Skipping commands for validation is very easy. To skip a single command just provide the CommandPath and to skip the entire chain of commands(including subcommands/children) use a asterik sign immediately after CommandPath
```go
ValidatorOptions: rules.ValidatorOptions{
	SkipCommands: map[string]bool{"mycli actions*": true},
},
```

Hence validator is very customizable and easy to use for developer productivity!
For detailed documentation of charmil validator, visit [Charmil Validator Docs](https://github.com/aerogear/charmil/blob/main/docs/src/validator.md)

Here is a small diagram to show how is validator working under the hood.

![charmil validator](https://cdn.discordapp.com/attachments/852928325197234256/866662866265964544/125803970-d47313c8-0bb9-42e9-81aa-ec4367f21634.png)


## Would like to sync?

- We are keeping all the communications open, so that everyone can sync and is free to contribute. So if you have any feature/bugs suggestions about anything please donot hesitate to open up an [issue](https://github.com/aerogear/charmil/issues/new)
- You can join [Aerogear’s discord server](https://discord.gg/hsDJUPkAWH) to participate in the discussions happening

## GSoC Weekly

I have been maintaining a **Project Tracker** to record the entire process in GSoC and making up of Charmil framework from scratch. Feel free to check it out at https://ankithans.github.io/gsoc21/

## What I have learnt or still learning

Some of these I got from my mentor's feedbacks and others are just my experiences
- **Communicate more and more**, even if you are stuck somewhere for long. Communication is the key here
- **Regularly push code** and ask for reviews
- Focus more on the end users and problems, not just code it first then think. Try to **follow docs first approach**
- Again Communicate more before PR's

> Connect with me here - [LinkedIn](https://www.linkedin.com/in/ankithans/) [Twitter](https://twitter.com/AnkitHans15) [Github](https://github.com/ankithans)
