# C# 14 lernen mit .NET 10

📖 **Das Tutorial lesen: [https://stahe.github.io/de-csharp-oct-2026/](https://stahe.github.io/de-csharp-oct-2026/)**

Dieser Kurs vermittelt die Sprache [C#](https://learn.microsoft.com/fr-fr/dotnet/csharp/) 14 und die Plattform [.NET](https://dotnet.microsoft.com) 10 **anhand praktischer Beispiele**: über zweihundert Programme (fast 300 C#-Dateien), Zeile für Zeile kommentiert, mit den wiedergegebenen Ausführungsergebnissen. Er beginnt mit den Grundlagen der Sprache und behandelt den Datenbankzugriff, die Netzwerkprogrammierung und Webdienste.

Es handelt sich um eine Neufassung des Kurses [Die Sprache C# lernen, Version 3.0, mit dem .NET-3.5-Framework](https://stahe.github.io/de-csharp-mai-2008/) (2008) für C# 14 und .NET 10: dieselbe Gliederung, dieselben Beispiele, derselbe rote Faden, aber mit aktuellem Code. Alle Programme lassen sich mit dem .NET-10-SDK **ohne Fehler oder Warnungen** kompilieren und wurden ausgeführt; die im Kurs gezeigten Ergebnisse stammen aus diesen Läufen.

| C#-3.0-Kurs (2008) | C#-14-Kurs (2026) |
|---|---|
| C# 3.0, .NET-3.5-Framework, nur Windows | C# 14, .NET 10 (LTS), Windows, Linux, macOS |
| Visual C# 2008 Express | VS Code + C# Dev Kit oder Visual Studio 2026, Befehl `dotnet` |
| `.sln`-Projekte und -Lösungen | Einzeldatei-Anwendungen (`dotnet run prog.cs`), `.slnx`-Lösungen |
| grafische Windows-Forms-Oberflächen | Kapitel entfernt (Oberflächen sind heute webbasiert) |
| LINQ „nicht behandelt" | LINQ ausführlich behandelt |
| `ArrayList`, `Hashtable`, `BinaryFormatter` | generische Collections, `System.Text.Json` |
| NUnit 2.4, Spring.NET | MSTest 4, Microsoft.Extensions.DependencyInjection |
| `BackgroundWorker`, Muster `BeginXxx` / `EndXxx` | `Task`, `async` / `await`, Abbruch, `IAsyncEnumerable` |
| SQL Server 2005, ODBC, OLE DB | MySQL 8 (Laragon), MySqlConnector, Entity Framework Core |
| `WebClient`, `WebRequest` | asynchroner `HttpClient`, `TcpClient` / `TcpListener` |
| SOAP-ASMX-Webdienste | REST-/JSON-Webdienste mit ASP.NET Core Minimal API |

## Gliederung des Kurses

| Kapitel | Inhalt |
|---|---|
| Installation | .NET-10-SDK, VS Code / Visual Studio 2026, der Befehl `dotnet`, Einzeldatei-Anwendungen, Projekte, `.slnx`-Lösungen |
| Grundlagen der Sprache | Typen, Literale, Nullable-Typen, Konvertierungen, Arrays, Indizes und Bereiche, Operatoren (`??`, `??=`), `switch`-Ausdrücke und Pattern Matching, Ausnahmen, Aufzählungen, Parameterübergabe, lokale Funktionen, Tupel |
| Klassen, Strukturen, Schnittstellen | Eigenschaften (`init`, `required`, das C#-14-Schlüsselwort `field`), Vererbung, Polymorphie, Operatoren, Indexer, Strukturen, Schnittstellen, Generics, Records, primäre Konstruktoren, C#-14-Erweiterungsmember, Nullable-Referenztypen |
| Häufig verwendete .NET-Klassen | Zeichenketten, Arrays, Collections, **LINQ**, Text- und Binärdateien, JSON, reguläre Ausdrücke (`[GeneratedRegex]`) |
| Schichtenarchitekturen | Schichten [DAO] / [Geschäftslogik] / [UI], **MSTest**-Unit-Tests, **Dependency Injection** |
| Delegates, Lambdas und Ereignisse | `Func`, `Action`, Lambda-Ausdrücke, Closures, Ereignisse, Ausdrucksbäume |
| Ausführungs-Threads | `Thread`, Synchronisierung (C# 13 `Lock`, `Monitor`, `Interlocked` …), nebenläufige Collections, `Parallel` |
| **Asynchrone Programmierung** (neu) | `Task`, `async` / `await`, `WhenAll`, Abbruch, Fortschritt, asynchrone Streams, `Parallel.ForEachAsync`, `Channel<T>` |
| Datenbankzugriff mit ADO.NET | MySQL, `MySqlConnector`, parametrisierte Abfragen und SQL-Injection, Transaktionen, asynchrone Methoden, `DbProviderFactory` |
| **Entity Framework Core** (neu) | Modell, CRUD, LINQ-to-SQL, Beziehungen, Migrationen, optimistische Nebenläufigkeit, rohes SQL, Dependency Injection |
| Webprogrammierung | TCP/IP, IPv6, asynchrone TCP-Clients und -Server, HTTP, `HttpClient`, SMTP |
| Webdienste | REST / JSON mit ASP.NET Core Minimal API, Konsolen-Clients, JavaScript-Webclient |

## Der rote Faden: ein Einkommensteuerrechner in 9 Versionen

Im gesamten Kurs entwickeln wir Version für Version eine Anwendung zur **Berechnung der Einkommensteuer**:

- **Version 1**: ein einziges Programm; **Version 2**: Klassen und Schnittstellen; **Version 3**: Daten aus einer Text- oder JSON-Datei;
- **Versionen 4 und 5**: eine Schichtenarchitektur, getestet mit MSTest und per Dependency Injection eingebunden;
- **Versionen 6 und 7**: Daten in einer MySQL-Datenbank, gelesen mit ADO.NET und anschließend mit Entity Framework Core;
- **Version 8**: ein TCP-Server zur Steuerberechnung und sein Client;
- **Version 9**: ein REST-Webdienst, sein Konsolen-Client und sein Webclient.

## Technologien

C# 14 · .NET 10 · VS Code · Visual Studio 2026 · MSTest 4 · Microsoft.Extensions.DependencyInjection · System.Text.Json · MySQL 8 · MySqlConnector · Entity Framework Core 9 · Pomelo.EntityFrameworkCore.MySql · ASP.NET Core 10 · Laragon

## Voraussetzungen

- Programmiererfahrung in einer beliebigen Sprache.
- Das [.NET-10-SDK](https://dotnet.microsoft.com/download/dotnet/10.0) und ein Code-Editor ([VS Code](https://code.visualstudio.com) mit der Erweiterung C# Dev Kit oder Visual Studio 2026); [Laragon](https://laragon.org) für MySQL (Kapitel zu Datenbanken). Installationsanweisungen finden Sie im Kurs.

## Autor

Dieser Kurs und sein Code wurden von **Claude**, der KI von [Anthropic](https://www.anthropic.com) (Oktober 2026), im Auftrag von Serge Tahé auf Grundlage seines C#-Kurses von 2008 geschrieben.

Prüfer: [Serge Tahé](https://stahe.github.io)
