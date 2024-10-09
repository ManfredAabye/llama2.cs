# Andrej Karpathys llama2.c in einer einzigen Datei aus purem C#.
[llama2.c](https://github.com/karpathy/llama2.c) ist eine sehr einfache Implementierung, um die Inferenz von Modellen mit einer auf [Llama2](https://arxiv.org/pdf/2302.13971.pdf) basierenden Transformer-LLM-Architektur durchzuführen.

Dies ist eine reine C#-Implementierung derselben Funktionalität. Sie ist für Geschwindigkeit optimiert und sehr einfach zu verstehen und anzupassen.

Für OpenSim muss über NuGet "System.Numerics.Tensors" nachinstalliert werden und DotNet auf .net8 gesetzt werden.

## Nutzung

Benötigt .net7 oder höher.

1. Zuerst die Datei stories15M.bin im gleichen Verzeichnis wie die ausführbare Datei ablegen. Du kannst sie [hier](https://huggingface.co/karpathy/tinyllamas/resolve/main/stories15M.bin) herunterladen.
2. Lade den Tokenizer von [hier](https://github.com/karpathy/llama2.c/blob/master/tokenizer.bin) und lege ihn ebenfalls in das gleiche Verzeichnis wie die ausführbare Datei.
```
dotnet build -c Release
```

### Eine zufällige Geschichte generieren
```
.\bin\Release\net7.0\llama2.cs.exe stories15M.bin
```
![WindowsTerminal_LrRTW3joph](https://github.com/trrahul/llama2.cs/assets/7353840/3b469a99-b83a-43f1-b07d-227da7b9ebe0)

### Eine zufällige Geschichte mit einem bestimmten Prompt generieren
```
.\bin\Release\net7.0\llama2.cs.exe stories15M.bin  -i "Vor langer Zeit"
```

### TODO
- [ ] Inferenz mit Llama2-Checkpoints
- [ ] Verwendung von leistungsstarken C#-Typen aus .net8?
- [ ] Trainingsfunktionalität hinzufügen
- [ ] OpenSimulator Implementierung
