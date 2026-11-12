# Wireshark SOC Labs

Hands-on packet analysis practice for security operations (SOC) work. Each lab is a short write-up of an investigation in Wireshark: the scenario, the filters and features I used, what I found, and why it matters to a defender.

> **Please note:** all captures come from guided practice labs (Networkwalks Academy Wireshark course). The IP addresses, usernames and passwords you see are training data, not real systems or people. This is a learning log, not professional incident-response experience.

## Labs

| Lab | Topic | Main Wireshark skill | Write-up |
|-----|-------|----------------------|----------|
| 3 | Identify the attacker's IP | Reading source/destination addresses | [lab-03](labs/lab-03-identify-attacker-ip.md) |
| 4 and 5 | Follow TCP Stream | Rebuilding a conversation | [lab-04-05](labs/lab-04-05-follow-tcp-stream.md) |
| 6 | HTTP plain text credentials | `http` and POST filters, form data | [lab-06](labs/lab-06-http-plaintext-credentials.md) |
| 7 | Catch the brute force attacker | `ftp.request.command == "PASS"` | [lab-07](labs/lab-07-brute-force-attacker.md) |
| 8 | Catch the call scammer | Telephony, RTP Player | [lab-08](labs/lab-08-call-scammer.md) |
| Extra | TCP retransmissions and resets | `tcp.analysis.*`, `tcp.flags.reset` | [extra](labs/extra-tcp-analysis.md) |

A quick reference of the filters used is in [docs/wireshark-cheatsheet.md](docs/wireshark-cheatsheet.md).

## Skills practised

- Capturing and filtering traffic with Wireshark display filters
- Following TCP streams to read application data
- Spotting clear-text credentials in HTTP and FTP
- Recognising brute-force patterns (many attempts, one source, short intervals)
- Replaying VoIP (RTP) streams
- Reading TCP health signals (retransmissions, resets)
- Writing short, evidence-based investigation notes

## Repository structure

```
README.md
labs/        One write-up per lab
docs/        Filter cheat sheet
images/      Screenshots used in the write-ups
```

## Status

Labs 1, 2, 9 and 10 are not documented yet. I will add them as I complete them.
