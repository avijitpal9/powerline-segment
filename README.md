# Powerline custom Segments

Segment for Powerline showing Memory Usage, Python Version, Java Version, Docker Context 
![Screenshot](images/screenshot.png "Screenshot")

## Installation
```
pip install powerlinecust-segments
```

## Usage
### Segment
- Activate the `docker_ctx` segment in `~/.config/powerline/themes/shell/default.json`
```json
{
    "function": "powerlinecust.segments.common.docker_ctx",
    "display": true
}           
```
- Activate the `pyenv` segment in `~/.config/powerline/themes/shell/default.json`
```json
{
    "function": "powerlinecust.segments.common.pyenv",
    "display": true
}
```
- Activate the `jenv` segment in `~/.config/powerline/themes/shell/default.json`
```json
{
    "function": "powerlinecust.segments.common.jenv",
    "display": true
},
```
- Activate the `mem_usage_percent` segment in `~/.config/powerline/themes/shell/default.json`
```json
{
    "function": "powerlinecust.segments.mem_usage.mem_usage_percent",
    "display": true
}
```

### Colorscheme
- Config highlight groups in colorscheme files, e.g. `~/.config/powerline/colorschemes/shell/default.json`:
```json
{
    "groups": {
        "pyenv:version": {
            "bg": "gray3",
            "fg": "green",
            "attrs": []
        },
        "jenv:version": {
            "bg": "black",
            "fg": "red",
            "attrs": [
                "bold"
            ]
        },
        "mem_usage": {
            "bg": "gray3",
            "fg": "green",
            "attrs": []
        },
        "docker_ctx": {
            "bg": "black",
            "fg": "green",
            "attrs": []
        }
    }
}
```

## Dependencies
The only dependency is [psutil](https://github.com/giampaolo/psutil).
