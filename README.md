# Assembly AI
Assembly AI is a tool which provides APIs to play around with audio, video and transcriptions. I'll be using some of these APIs in this project.

## Requirements

```console
$ pip install requests
```

### Assembly AI Installation
If you have Homebrew
```console
$ brew tap assemblyai/assemblyai
$ brew install assemblyai
```

If you don't have Homebrew
```console
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/AssemblyAI/assemblyai-cli/main/install.sh)"
```

## Usage

Set API Key as an environment variable
```console
$ export AAI_API_KEY=<YOUR_API_KEY>
```

`NOTE` You can get your API Key after signing in to your Assembly AI account and viewing the Dashboard

If your AssemblyAI API key is stored as an environment variable called `AAI_API_KEY` file, then you can omit the optional `--api_key` argument.

```console
$ python transcribe.py audio_file [--local] [--api_key=<YOUR-API-KEY>"]
```

Example for hosted file:

```console
$ python transcribe.py https://github.com/AssemblyAI-Examples/assemblyai-and-python-in-5-minutes/raw/main/audio.mp3 [--api_key=<YOUR-API-KEY>]
```

Example for local file:

```console
$ python transcribe.py audio.mp3 --local [--api_key=<YOUR-API-KEY>]
```
