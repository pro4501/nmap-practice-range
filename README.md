# Nmap Practice Range

A browser-based nmap simulator for practicing port scanning before a lab test. You type real nmap commands into a fake Kali terminal, and the page answers with nmap-style output for a simulated `10.10.10.0/24` network. Everything runs in your browser. No packets are sent anywhere.

## What's inside

- **Practice terminal.** Supports `-sS`, `-sT`, `-sU`, `-sA`, `-sF`, `-sN`, `-sX`, `-sn`, `-Pn`, `-p`, `-p-`, `-F`, `--top-ports`, `-sV`, `-sC`, `-O`, `-A`, `-T0`–`-T5`, `--reason`, `--open`, `-v` and `-oN`/`-oG`/`-oX`/`-oA`. It also has `sudo`, `ping`, `ip a`, `ls`, `cat` and `history`.
- **Root vs. non-root behaviour.** Without `sudo`, raw-packet scans refuse to run and host discovery falls back to TCP connects on ports 80 and 443.
- **Realistic quirks.** Firewalled hosts, a workstation that blocks ping, slow UDP scans, Windows answering FIN/NULL/Xmas probes with RST, TTL-based OS hints, and a service hidden on a high port.
- **25 lab challenges** checked against the live lab, each with a hint and a reveal button.
- **Packet diagrams** of the probes and replies behind each port state.
- **Cheat sheet** of flags, port states and exam tips.
- **25-question theory quiz** with explanations.
- **New lab** button that generates a different network, so the answers change every time.

## Use it

Open `index.html` in any modern browser, or use the GitHub Pages link for this repository. Start with:

```
sudo nmap -sn 10.10.10.0/24
```

Type `help` in the terminal for the full command list.

## Disclaimer

This is a simulation for learning. Only scan real networks you own or have written permission to test.
