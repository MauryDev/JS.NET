# JS.NET

## O que é JS.NET?

JS.NET é uma biblioteca C# que executa códigos JavaScript para Windows Forms e Console.

## Quais ferramentas o JS.NET está usando?

- Jint
- MetroFramework
- Esprima.NET

## Jint

O Jint é uma biblioteca para implementação do V8 no C#.

Github: https://github.com/sebastienros/jint

Nuget: https://www.nuget.org/packages/Jint

## Qual é a versão do EcmaScript

O Jint usa a versão 5.

## Esprima.NET

Github: https://github.com/sebastienros/esprima-dotnet

Nuget: https://www.nuget.org/packages/esprima

## MetroFramework

O MetroFramework é usado para adicionar visuais moderno no Windows Forms.

O FormJS usa essa biblioteca no module `Forms`.

Github: https://github.com/thielj/MetroFramework

Nuget: https://www.nuget.org/packages/MetroModernUI/

## Perfomance

Hello World:
| Library | Memory Usage | Max CPU | 
| :-------------: |:-------------:| :-----:|
| FormJS |  |  |
| ConsoleJS | 3MB | 2 |

## Como usar o FormJS?

Para inicializar o FormsJS você precisa chama a função `Start` contendo no parâmetro o código JS.
```cs
internal class MainApp
{
    public static void Main(string[] args)
    {
        FormsJS.Start(@"
            var Forms = require(""Forms"")
            var Drawing = require(""Drawing"")
            var label = Forms.CreateControl(""Label"")
            label.Text = ""Hello World!""
            label.Location = Drawing.Point(""40"",""100"")
            MainForm.Controls.Add(label)
        ")
    }
}
```

## Como usar o ConsoleJS?
Para inicializar o ConsoleJS você precisa chama a função `Start` contendo no parâmetro o código JS.

Exemplo:
```cs
internal class MainApp
{
    public static void Main(string[] args)
    {
        ConsoleJS.Start(@"
            console.log('Hello World!')
        ")
    }
}
```

## Como instalar o FormJS e o ConsoleJS?


[Download](https://github.com/MauryDev/JS.NET/releases)

Os arquivos são:
- FormJS.zip
- ConsoleJS.zip

## Licença

Todos os direitos do JS.NET reservado a Maury Dev.