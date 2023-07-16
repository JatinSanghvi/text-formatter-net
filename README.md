# Text Decorator for .NET

<div align="center">
    <picture>
        <source media="(prefers-color-scheme: dark)" srcset="images/logo-dark.png" />
        <source media="(prefers-color-scheme: light)" srcset="images/logo-light.png" />
        <img alt="Text Decorator for .NET logo" src="images/logo-light.png" />
    </picture>
    <p>An elegant way to color and style text in your console applications.</p>
</div>

## NuGet Package

[JatinSanghvi.TextDecorator](https://www.nuget.org/packages/JatinSanghvi.TextDecorator)

## Text Colors

> You will need to activate text decorator once in your application before calling any of its methods, else on certain consoles, the text decorations will not get applied.

```cs
_ = TextDecorator.Activate();

Console.WriteLine("Once in a green forest, a curious fox explored.".BrightRed());
Console.WriteLine("Lost and afraid, he sought a way back.".Green());
```

<picture>
    <source media="(prefers-color-scheme: dark)" srcset="images/1-fg-methods-dark.png" />
    <source media="(prefers-color-scheme: light)" srcset="images/1-fg-methods-light.png" />
    <img alt="Foreground Color Methods" src="images/1-fg-methods-light.png" />
</picture>

The following are the different methods supported for setting the text color along with the corresponding `ConsoleColor` enum members.

| Method Name       | `ConsoleColor` member |
| ----------------- | --------------------- |
| `Black()`         | `Black`               |
| `Red()`           | `DarkRed`             |
| `Green()`         | `DarkGreen`           |
| `Yellow()`        | `DarkYellow`          |
| `Blue()`          | `DarkBlue`            |
| `Magenta()`       | `DarkMagenta`         |
| `Cyan()`          | `DarkCyan`            |
| `White()`         | `Gray`                |
| `Gray()`          | `DarkGray`            |
| `BrightBlack()`   | `DarkGray`            |
| `BrightRed()`     | `Red`                 |
| `BrightGreen()`   | `Green`               |
| `BrightYellow()`  | `Yellow`              |
| `BrightBlue()`    | `Blue`                |
| `BrightMagenta()` | `Magenta`             |
| `BrightCyan()`    | `Cyan`                |
| `BrightWhite()`   | `White`               |

You can also apply text colors by passing one of the `ConsoleColor` enum members to the `Color()` method.

```cs
Console.WriteLine("Encountered friendly creatures who helped.".Color(ConsoleColor.DarkGray));
```

<picture>
    <source media="(prefers-color-scheme: dark)" srcset="images/2-fg-consolecolor-dark.png" />
    <source media="(prefers-color-scheme: light)" srcset="images/2-fg-consolecolor-light.png" />
    <img alt="Foreground ConsoleColor" src="images/2-fg-consolecolor-light.png" />
</picture>

## Text Background Colors

```cs
Console.WriteLine("Time passed; fox learned about the forest.".BgBlue());
Console.WriteLine("Adventures and challenges became life.".BgBrightWhite().Black());
```

<picture>
    <source media="(prefers-color-scheme: dark)" srcset="images/3-bg-methods-dark.png" />
    <source media="(prefers-color-scheme: light)" srcset="images/3-bg-methods-light.png" />
    <img alt="Background Color Methods" src="images/3-bg-methods-light.png" />
</picture>

The following are the different methods supported for setting the text background colors along with the corresponding `ConsoleColor` enum members.

| Method Name         | `ConsoleColor` member |
| ------------------- | --------------------- |
| `BgBlack()`         | `Black`               |
| `BgRed()`           | `DarkRed`             |
| `BgGreen()`         | `DarkGreen`           |
| `BgYellow()`        | `DarkYellow`          |
| `BgBlue()`          | `DarkBlue`            |
| `BgMagenta()`       | `DarkMagenta`         |
| `BgCyan()`          | `DarkCyan`            |
| `BgWhite()`         | `Gray`                |
| `BgGray()`          | `DarkGray`            |
| `BgBrightBlack()`   | `DarkGray`            |
| `BgBrightRed()`     | `Red`                 |
| `BgBrightGreen()`   | `Green`               |
| `BgBrightYellow()`  | `Yellow`              |
| `BgBrightBlue()`    | `Blue`                |
| `BgBrightMagenta()` | `Magenta`             |
| `BgBrightCyan()`    | `Cyan`                |
| `BgBrightWhite()`   | `White`               |

As with the text foreground colors, you can also apply text background colors by passing one of the `ConsoleColor` enum members to the `BgColor()` method.

## Web Colors

You can specify either [HTML color names](https://en.wikipedia.org/wiki/Web_colors#HTML_color_names) such as `HotPink` or [hex triplets](https://en.wikipedia.org/wiki/Web_colors#Hex_triplet) such as `#3b82f6` or `#2c6`, and apply those colors to the text foreground and background.

```cs
Console.WriteLine("An owl, wise and old, became his guide.".Color("HotPink"));
Console.WriteLine("Seasons changed, and fox grew wiser.".Color("#3b82f6"));
Console.WriteLine("Home now felt distant; forest was home.".BgColor("#2c6").Color("#031"));
```

<picture>
    <source media="(prefers-color-scheme: dark)" srcset="images/4-web-colors-dark.png" />
    <source media="(prefers-color-scheme: light)" srcset="images/4-web-colors-light.png" />
    <img alt="Web Colors" src="images/4-web-colors-light.png" />
</picture>

## Text Styles

```cs
Console.WriteLine("With the owl's wisdom, he thrived.".Italic());
Console.WriteLine("The fox embraced nature's harmony.".Underline());
```

<picture>
    <source media="(prefers-color-scheme: dark)" srcset="images/5-styles-dark.png" />
    <source media="(prefers-color-scheme: light)" srcset="images/5-styles-light.png" />
    <img alt="Text Styles" src="images/5-styles-light.png" />
</picture>

There are many text styles supported as listed below.

| Method Name         | Description                        |
| ------------------- | ---------------------------------- |
| `Bold()`            | Increases brightness of foreground |
| `Dim()`             | Reduces brightness of foreground   |
| `Italic()`          | Uses italic font variant           |
| `Underline()`       | Adds underline to text             |
| `Blink()`           | Sets text to blinking              |
| `Inverse()`         | Swaps foreground and background    |
| `Hidden()`          | Sets foreground same as background |
| `Strikethrough()`   | Crosses out text                   |
| `DoubleUnderline()` | Adds double underline to text      |
| `Overline()`        | Adds line over the text            |

## Color and Style Combinations

You can chain the coloring and styling methods in any order as illustrated below to get the best results.

```cs
// String interpolation.
Console.WriteLine("In the {0}, he found {1}.", "green forest".BgGreen(), "belonging".BgBlue());

// String variables.
string action = "danced".Inverse();
Console.WriteLine($"His heart {action} and {action}.".Cyan());

// Composite decoration method.
static string highlight(string text) => text.Bold().Italic().Underline().Blink();

Console.WriteLine($"Forever, the {highlight("curious")} fox {highlight("thrived")}.".Yellow());
```

<picture>
    <source media="(prefers-color-scheme: dark)" srcset="images/6-combinations-dark.gif" />
    <source media="(prefers-color-scheme: light)" srcset="images/6-combinations-light.gif" />
    <img alt="Color and Style Combinations" src="images/6-combinations-light.gif" />
</picture>

## Notes

- The color and style application will be disabled if the `NO_COLOR` environment variable is set. See [https://no-color.org/]() for more information.

- The console colors will vary based on the terminal theme. Use HTML color names or hex triplets to use exact colors.

- If there is any error during initialization, the library does not print any exception message to keep the user experience intact. It prints the input text without colors or styles applied for the rest of the application lifetime. To see the error message, you can pass `true` to the `TextDecorator.Activate` method. This should print exceptions, if any, that prevented the text from being decorated.

- For decorating the non-string values, you will need to first convert them to strings before calling one of the text decoration methods on them. For example, `$"I have {42.ToString().Red()} apples."`. I could have defined the decoration extension methods on the `object` type but that would have flooded the IntelliSense suggestions for each and every variable.

- The strings returned by `TextDecorator` methods should only be used for printing to console. Writing these strings to log files for example, may lead to illegible text and corruption of file content structure.

- Support for Linux and Mac consoles is not yet tested.
