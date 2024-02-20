### Hi there 👋

I am a software developer in the ASP.NET team at Microsoft. I currently work on benchmarking ASP.NET Core and building distributed benchmarking services. I also spend some of this time helping the Orchard Core project by leading the community and contributing to features.

If I am not working or coding, I am probably

sleeping
doing husband and father duties
listening to James Taylor
playing guitar
biking
running
swimming
Open source
When I don't get paid to code, I still code, mainly on these open source projects:

Jint - https://github.com/sebastienros/jint
A JavaScript interpreter for .NET, which allows to run standard scripts in any .NET application. If you need to add some scripting capabilities to your apps, to build a rules engine, or evaluate configurable predicates, you should use it. It's fast and standard compliant.

The first version of this project started at a previous job, where we needed to send email compains, and we wanted to customize these emails using templates. We followed the way Razor was working by translating the template into pure code, but decided that JavaScript would be easier than C# for editors. A few years ago I decided to rewrite it from scratch following the ECMAScript specs. The first week I joined Microsoft I was asked to show a prototype to Scott Guthrie of "jQuery on the server" which I had built with it, that was fun!

YesSQL - https://github.com/sebastienros/yessql
A NoSQL-like document database layer for .NET that works on existing RDBMS like SQL Server, PostgresQL, Sqlite, MySQL. It allows to store documents and define materialized indexes you can query on using SQL directly. Because it's using the database system you want, you can reuse your existing knowledge, and also use custom SQL queries when you need to optimize for performance.

The idea of the project came to me while working on the first version of Orchard CMS, where we would have to split entities in many tables, which was impacting perf a lot. A CMS usually fits a document based approach, with denormalized data. However using brand new NoSQL databases is often an issue in terms of vendor lock-in, or lack of experience on these systems. RavenDB paved the way in .NET, and I thought we could definitely provide similar features using an RDBMS. Now YesSQL is the standard way to store content in Orchard Core.

Fluid - https://github.com/sebastienros/fluid
A Liquid template engine. Liquid is a templating language created by Shopify and used in other places like Jekyll. This can be used to provide a safe way for users to author templates. It also contains an MVC view engines where files like index.liquid will be used automacically for MVC Views.

This project was created for Orchard Core in order to enable users to create safe templates, and faster cold rendering of templates. The issue with Razor for content editors is that it's not safe, as it allows to access anything that C# allows, including reading the whole filesystem, and it is also slower to render a template the first time as it requires compilation. Fluid solves these two issues and now used in other .NET CMSes. Initially I tried to use dotLiquid but was faced with performance issues as it is using regular expressions to parse the templates.

Esprima.NET - https://github.com/sebastienros/esprima-dotnet
Is it a fully compliant ECMAScript parser for .NET. It allows to parse and manipulate JavaScript files, either for executing them, minifying, linting, finding bugs, ... It's use in Jint.

When I started rewriting Jint I followed an advice that Atif Aziz made on the previous version, and made the parser a separate library to Jint. The project is mainly a port of the JavaScript implementation named Esprima created by Ariya Hidayat.

Parlot - https://github.com/sebastienros/parlot
A fast, lightweight and simple to use .NET parser combinator. Parser combinators make it possible to create parsers at runtime, while keeping simplicity by reusing common language constructs. I created Parlot out of interest for this technology and realized it would become even faster than hand-written parsers while still providing ways to customize the languages at runtime.

Shortcodes - https://github.com/sebastienros/shortcodes
A .NET library to parse and evaluate shortcodes. It allows text content editors to inject specialized content blocks using custom arguments, like images, twitter embeds, youtube videos, only with simple blocks like [video 123].

Shortcodes are essential to WordPress, and for the Orchard Core we wanted a similar feature. The parser was written by hand as the syntax is simple and it needs to be efficient.


<!--
**taeul/taeul** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
