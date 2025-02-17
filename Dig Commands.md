# 🌐 Dig Command Cheat Sheet

**dig (Domain Information Groper)** is a powerful DNS lookup utility used to query DNS servers, troubleshoot DNS issues, and obtain detailed domain information.

---

## 📘 Basic Commands

| **Command**               | **Description**                                | **Example**               |
|---------------------------|------------------------------------------------|---------------------------|
| `dig example.com`         | Basic DNS query for A record of a domain.      | `dig google.com`          |
| `dig example.com ANY`      | Retrieves all DNS records for a domain.        | `dig example.com ANY`     |
| `dig example.com +short`   | Displays concise output (just the IP).         | `dig google.com +short`   |
| `dig -x 8.8.8.8`           | Performs a reverse DNS lookup.                 | `dig -x 8.8.8.8`          |

---

## 📜 Querying Specific Record Types

| **Command**               | **Description**                                | **Example**               |
|---------------------------|------------------------------------------------|---------------------------|
| `dig example.com A`       | Queries the IPv4 address of a domain.          | `dig google.com A`        |
| `dig example.com AAAA`    | Queries the IPv6 address of a domain.          | `dig google.com AAAA`     |
| `dig example.com MX`      | Queries Mail Exchange servers.                 | `dig example.com MX`      |
| `dig example.com NS`      | Retrieves Name Server records.                 | `dig example.com NS`      |
| `dig example.com TXT`     | Displays TXT records (e.g., SPF, DKIM).        | `dig example.com TXT`     |
| `dig example.com CNAME`   | Retrieves Canonical Name records.              | `dig www.example.com CNAME`|
| `dig example.com SOA`     | Displays Start of Authority records.           | `dig example.com SOA`     |

---

## 🔄 Query Options and Modifiers

| **Command**                     | **Description**                                | **Example**                     |
|---------------------------------|------------------------------------------------|---------------------------------|
| `dig @8.8.8.8 example.com`      | Queries a specific DNS server.                | `dig @1.1.1.1 google.com`       |
| `dig example.com +noall +answer`| Shows only the answer section.                | `dig example.com +noall +answer`|
| `dig example.com +trace`        | Traces the DNS resolution path.               | `dig example.com +trace`        |
| `dig example.com +multiline`    | Displays records in a more readable format.   | `dig example.com +multiline`    |
| `dig example.com +nocmd`        | Hides the command section in the output.      | `dig example.com +nocmd`        |

---

## ⏱ Timing and Performance

| **Command**               | **Description**                                | **Example**               |
|---------------------------|------------------------------------------------|---------------------------|
| `dig example.com +stats`  | Shows query statistics (e.g., query time).     | `dig google.com +stats`   |
| `dig example.com +time=3` | Sets the query timeout.                        | `dig example.com +time=3` |
| `dig example.com +retry=2`| Sets the number of retries for the query.      | `dig example.com +retry=2`|

---

## 📜 Display and Output Options

| **Command**               | **Description**                                | **Example**               |
|---------------------------|------------------------------------------------|---------------------------|
| `dig example.com +short`  | Displays concise output (e.g., only IP).       | `dig example.com +short`  |
| `dig example.com +noquestion`| Hides the question section.                 | `dig example.com +noquestion`|
| `dig example.com +nocomments`| Hides comment lines in the output.          | `dig example.com +nocomments`|
| `dig example.com +qr`     | Displays the query as it was sent.            | `dig example.com +qr`     |

---

## 🔧 Miscellaneous Commands

| **Command**               | **Description**                                | **Example**               |
|---------------------------|------------------------------------------------|---------------------------|
| `dig -4 example.com`      | Forces IPv4 query.                             | `dig -4 google.com`       |
| `dig -6 example.com`      | Forces IPv6 query.                             | `dig -6 google.com`       |
| `dig +tcp example.com`    | Uses TCP instead of UDP for the query.         | `dig +tcp example.com`    |
| `dig +notcp example.com`  | Disables TCP for the query.                   | `dig +notcp example.com`  |

---

This cheat sheet provides a quick and organized reference for using the `dig` command effectively! 🌐