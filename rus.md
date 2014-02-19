# Почему стиль кода имеет значение

// TODO: Тавтология

Когда изучал в колледже информатику, у меня преподавал очень трудный
профессор. Его звали доктор Максей, и он вёл более сложные предметы
вроде структур данных и архитектуры компьютеров. Он был чудесным учителем и
обладал талантом доходчиво объяснять сложные понятия. Но вместе с этим он
был очень требователен в оценках. Он не только тщательно проверял код на
предмет работоспособности, но ещё и снимал баллы за оформление кода.

Если вы вдруг пропустили нужные комментарии или даже ошиблись в написании
слова в паре комментариев, он вычитал баллы. Если ваш код был «неопрятным»
(по его стандартам), он вычитал баллы. Его посыл был ясен: качество кода
не только в том, как он запускается, но и в том, как он выглядит. Тогда я
впервые столкнулся со стилем кода.

### А что вообще такое, стиль?

Стиль кода — это то, как ваш код выглядит, вот так просто. И говоря «ваш», я
имею в виду именно вас, того человека, который сейчас читает эту статью.
Стиль кода — вещь очень личная, и у каждого есть свой любимый стиль.
Вы можете прочувствовать свой личный стиль, изучив код, который вы же
и написали когда не придерживались определенного стиля.
У каждого свой собственный стиль, зависящий о того, кто как учился
программированию. Если вы использовали интегрированную среду разработки (IDE)
вроде Visual Studio для обучения, ваш стиль, возможно, совпадает с тем,
который навязан редактором. Если вы учились используя обычный тектовый
редактор, ваш стиль, вероятно, развился из того, что вы считали более
читаемым.

![Руководство по стилю][1]

*Руководства по стилю нужны не только издательским домам. Если вы хотите,
чтобы код было по прежнему легко читать и редактировать даже после нескольких
лет после того, как вы закончили проект, руководство по стилю полезно и
необходимо. (Автор изображения: [Wikidave][2])*

Вы даже можете заменить, что ваш стиль меняется от языка к языку.
Решения, которые вы принимаете в JavaScript, могут не распространяться на ваш
CSS. К примеру, вы можете решить, что в JavaScript строки должны быть в
двойных кавычках, а в CSS следует использовать одинарные. В этом нет ничего
необычного, мы склонны к переключению контекста в то время как переключамся
взад-вперед между языками. Но всё же, это интересное упражнение по
самонаблюдению.

Стиль кода создается из множества маленьких решений в зависимости от языка:

*   Как и когда использовать комментарии.
*   Табы или пробелы для отступов (и сколько пробелов).
*   Подходящие случаи для использования пробелов.
*   Правильное именование переменных и функций.
*   Группировка и организация кода.
*   Паттерны, которые следует использовать.
*   Паттерны, которые не следует использовать.

Этот список ни в коем случае не полон, стиль кода может быть чрезывайно
подробным, таким как [руководство по стилю JavaScript от Google][3], или более
общим, вроде [рекомендации по стилю ядра jQuery][4].

### Это личное

Личный характер стиля кода — это испытание в командной обстановке.
Зачастую, избегая долгих рассуждений, команды откладывают создание руководства
по стилю в долгий ящик под предлогом того, что они не хотят «препятствовать
инновациям и выражениям». Кто-то видит в командных руководствах по стилю
принуждение всех разработчиков быть одинаковыми. Кто-то из разработчиков
возмущается, когда им предлагают руководства по стилю, дескать, они не могут
нормально работать, если кто-то будет говорить им, как писать код.

Ситуация примерно такая же, как если бы несколько музыкантов собирали группу.
Каждый свято уверен, что их способ делать вещи непременно самый лучший (их
«метод» или «процесс»). В группе будут неурядицы пока все будут пытаться
делать по-своему. Невозможно играть хорошую музыку пока все в группе не
согласятся насчет темпа, стиля и того, кто будет задавать ритм. Всякий, кто
слышал хоть раз группу из старшеклассников, знает, это правда. Пока все не
будут на одной волне, ничего путного не выйдет.

Вот почему я настоятельно рекомендую руководства по стилю для команд
разработчиков ПО. Настариваться на одну волну сложно, и руковоство по стилю —
отличное начало. Если все будут писать код, который выглядит одинаково, можно
впоследствии избежать множество проблем.

### Communication Is Key

> “Programs are meant to be read by humans and only incidentally for
> computers to execute.”
> — H. Abelson and G. Sussman (in “Structure and Interpretation of Computer
> Programs”)

The most important thing when working on a team is communication. People need
to be able to work together effectively and the only way to do that is by
communicating. As developers, we communicate primarily through code. We
communicate with other parts of the software through code and we communicate
with other developers through code.

While the software your code communicates with doesn’t care how the code
looks, the other developers on your team certainly do. The way code looks adds
to our understanding of it. How many times have you opened up a piece of code
that somebody else wrote, and, before doing anything else, re-indented it the
way that you like? That’s your brain not being able to figure out the code
because of how it looks. When everyone is writing code that looks different,
everyone is constantly trying to visually parse the code before being able to
understand it. When everyone is writing code that looks the same, your brain can
relax a bit as the understanding comes faster.

![BBC GEL][5]
*Not only designers can use style guides to ensure consistent visual design and
informed design decisions. We could use them on the macrolevel as well: for the
little fine details in our code.*

When you start thinking of code as communication with other developers, you
start to realize that you’re not simply writing code, you’re crafting code. Your
code should clearly communicate its purpose to the casual observer. Keep in mind,
your code is destined to be maintained by somebody other than you. You are not
just communicating with other members of your team in the present, you’re also
communicating with members of your team in the future.

I recently received an email from someone who is working on code that I wrote
10 years ago. Apparently, much to my shock and horror, my code is still being
used in the product. He felt compelled to email me to say that he enjoyed
working with my code. I smiled. My future teammate actually did appreciate the
coding style I followed.

### Leave Yourself Clues

> “If you know your enemies and know yourself, you will not be imperiled in a
> hundred battles.”
> — Sun Tzu (in “The Art of War”)

Knowing yourself is important in life as well as coding. However, you’ll
never know yourself well enough to remember exactly what you were thinking when 
you wrote each line of code. Most developers have experienced looking at a very 
old piece of code that they wrote and not having any idea why they wrote it. It’
s not that your memory is bad, it’s just that you make so many of these little 
decisions while writing code that it’s impossible to keep track of them all.

Writing code against a style guide outsources that information into the code
itself. When you decide when and where to use comments, as well as which 
patterns should and shouldn’t be used, you are leaving a breadcrumb trail for 
your future self to find your way back to the meaning of the code. It’s 
incredibly refreshing to open up an old piece of code and have it look like a 
new piece of code. You’re able to acclimate quickly, sidestepping the tedious 
process of relearning what the code does before you can start investigating the 
real issue.

As [Chris Epstein][6] once said during a talk, “be kind to your future self.”

### Make Errors Obvious

One of the biggest reasons to have a coherent style guide is to help make
errors more obvious. Style guides do this by acclimating developers to certain 
patterns. Once you’re acclimated, unfamiliar patterns jump out of the code when 
you look at it. Unfamiliar patterns aren’t always errors, but they definitely 
require a closer look to make sure that nothing is amiss.

For example, consider the JavaScript `switch` statement. It’s a very common
error to mistakenly allow one`case` to fall through into another, such as this
:

    switch(value) {
        case 1:
            doSomething();
    
        case 2:
            doSomethingElse();
            break;
    
        default:
            doDefaultThing();
    }

The first case falls through into the second case so if `value` is 1, then both
`doSomething()` and `doSomethingElse()` are executed. And here’s the question
: is there an error here? It’s possible that the developer forgot to include a
`break` in the first case, but it’s also equally possible that the developer
intended for the first case to fall through to the second case. There’s no way 
to tell just from looking at the code.

Now suppose you have a JavaScript style guide that says something like this:

> “All `switch` statement cases must end with `break`, `throw`, `return`, or a
> comment indicating a fall-through.
> ”

With this style guide, there is definitely a stylistic error, and that means
there could be a logic error. If the first case was supposed to fall through to 
the second case, then it should look like this:

    switch(value) {
        case 1:
            doSomething();
            //falls through
    
        case 2:
            doSomethingElse();
            break;
    
        default:
            doDefaultThing();
    }

If the first case wasn’t supposed to fall through, then it should end with a
statement such as`break`. In either case, the original code is wrong according
to the style guide and that means you need to double check the intended 
functionality. In doing so, you might very well find a bug.

When you have a style guide, code that otherwise seems innocuous immediately
raises a flag because the style isn’t followed. This is one of the most 
overlooked aspects of style guides: by defining what correct code looks like, 
you are more easily able to identify incorrect code and therefore potential bugs
before they happen.

### Devil In The Details

In working with clients to develop their code style guides, I frequently get
asked if the minutia is really that important. A common question is, “aren’t 
these just little details that don’t really matter?” The answer is yes and no. 
Yes, code style doesn’t really matter to the computer that’s running it; no, the
little details matter a lot to the developers who have to maintain the code. 
Think of it this way: a single typo in a book doesn’t disrupt your understanding
or enjoyment of the story. However, if there are a lot of typos, the reading 
experience quickly becomes annoying as you try to decipher the author’s meaning 
despite the words being used.

Coding style is a lot like that. You are defining the equivalent of spelling
and grammar rules for everyone to follow. Your style guide can get quite long 
and detailed, depending on which aspects of the language you want to focus on. 
In my experience, once teams get started on coding style guides, they tend to go
into more and more detail because it helps them organize and understand the code
they already have.

![Order In Your Code][7]
*In art, numbers are usually chaotic and serve a visual purpose. But you need
order in your code.[(Image credit: Alexflx54)][8]*

I’ve never seen a coding style guide with too much detail, but I have seen
them with too little detail. That’s why it’s important for the team to develop a
style guide together. Getting everyone in the same room to discuss what’s really
important to the team will result in a good baseline for the style guide. And 
keep in mind, the style guide should be a living document. It should continue to
grow as the team gets more familiar with each other and the software on which 
they are working.

### Tools To Help

Don’t be afraid of using tools to help enforce coding style. Web developers
have an unprecedented number of tools at their fingertips today, and many of 
them can help ensure that a coding style guide is being followed. These range 
from command line tools that are run as part of the build, to plugins that work 
with text editors. Here are a few tools that can help keep your team on track:

*   [Eclipse Code Formatter][9]  
    The Eclipse IDE has built-in support for code formatting. You can decide
    how specific languages should be formatted and Eclipse can apply the formatting 
    either automatically or on demand.
   
*   [JSHint][10]  
    A JavaScript code quality tool that also checks for stylistic issues.
*   [CSS Lint][11]  
    A CSS code quality tool by [Nicole Sullivan][12] and me that also checks
    for stylistic issues.
   
*   [Checkstyle][13]  
    A tool for checking style guidelines in Java code, which can also be used
    for other languages.
   

These are just a small sampling of the tools that are currently available to
help you work with code style guides. You may find it useful for your team to 
share settings files for various tools so that everyone’s job is made easier. Of
course, building the tools into your continuous integration system is also a 
good idea.

### Conclusion

Coding style guides are an important part of writing code as a professional.
Whether you’re writing JavaScript or CSS or any other language, deciding how 
your code should look is an important part of overall code quality. If you don’t
already have a style guide for your team or project, it’s worth the time to 
start one. There are a bunch of style guides available online to get you started.
Here are just a few:

It’s important that everybody on the team participates in creating the style
guide so there are no misunderstandings. Everyone has to buy in for it to be 
effective, and that starts by letting everyone contribute to its creation.

*(cp)*</article>

 [1]: img/start-image.jpg "Style Guide"
 [2]: http://www.flickr.com/photos/wikidave/7118464049/sizes/c/
 [3]: http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml
 [4]: http://docs.jquery.com/JQuery_Core_Style_Guidelines
 [5]: img/gel2.jpg "BBC GEL"
 [6]: http://chriseppstein.github.com/
 [7]: img/coding.jpg "Order In Your Code"
 [8]: http://www.flickr.com/photos/73807667@N02/8021619893/sizes/c/

 [9]: http://eclipseone.wordpress.com/2009/12/13/automatically-format-and-cleanup-code-every-time-you-save/
 [10]: http://jshint.com
 [11]: http://csslint.net
 [12]: http://stubbornella.org
 [13]: http://checkstyle.sourceforge.net/