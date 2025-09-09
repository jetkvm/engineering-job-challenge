<div align="center">
    <img alt="  JetKVM logo" src="https://jetkvm.com/logo-blue.png" height="28">

### Engineering Job Challenge

[Discord](https://jetkvm.com/discord) | [Website](https://jetkvm.com) | [Docs](https://jetkvm.com/docs)

</div>
Welcome to the Engineering Job Challenge! 🚀
</br></br>

This is a practical exercise designed to give you a feel for the kind of problems we solve at JetKVM. **Pick one or more challenges, implement your solution in the relevant repos, and send us your patch sets.** Your submission should demonstrate not only that it works, but also clean code, thoughtful design, and a good developer experience.

> [!IMPORTANT]
> Deadline for this job challenge is 23 September, 2025 - 23:59 UTC.

## How to Participate
1. **Clone the repos you need** for the challenge (e.g. kvm, api). Keep private until deadline.
2. **Implement challenges** using the pre-defined challenge branch name

Once you're ready with all the challenges you wanted to implement:
1. **Create a patchset** for each challenge & repo

```bash
git fetch --all --tags
git format-patch \
--base=challenge-base \
challenge-base...<your-challenge-branch> \
-o ~/jetkvm-challenges/<your-challenge-branch>/<repo-name>
```

2. **Package your work**

Zip the whole `~/jetkvm-challenges` directory. It should looks something like:

```
jetkvm-challenges/
  automated-e2e-test-suite/
    kvm/
      0001-add-tests.patch
    api/
      0001-new-endpoint.patch
  h265/
    kvm/
      0001-add-h265-support.patch
```


3. **Email us the challenges**
   - **To:** `jobs [at] jetkvm [dot] com`
   - **Subject:** `JetKVM Engineering Job Challenge`
   - **Body**: Anything you’d like us to know about your solution (e.g. notes, assumptions, trade-offs).
   - **Attachment**: One zip of the `jetkvm-challenges` directory with all the folders & `.patch` files in it.

## Available Challenges

<details open>

<summary>H.265 Support</summary>

Challenge branch name: `h265`

```
- Add H.265 support with a settings option for Auto/H.264/H.265
- Migrate Video Settings from React state to `react-hook-form`
```

</details>

<details>

<summary>Static IPv6</summary>

Challenge branch name: `static-ipv6`

```
- Add static IPv6 support with a toggle to switch from SLAAC
- Migrate Network Settings from React state to `react-hook-form`
```

</details>

<details>

<summary>Device Access Sharing</summary>

Challenge branch name: `access-sharing`

```
- Add support for sharing remote control access via link, with expiration date options
```

</details>

<details>

<summary>Connection Troubleshooting</summary>

Challenge branch name: `connection-troubleshooting`

```
- Improve the end-user experience for connection troubleshooting
    - Browser permissions
    - Operating system settings
    - WebSocket connection
    - WebRTC connection
    - Video encoder issues

Please checkout https://github.com/jetkvm/kvm/issues/84 and https://jetkvm.com/docs/getting-started/troubleshooting#loading-video-stream-issue for more details
```

</details>

<details>

<summary>Automated E2E Test Suite</summary>

Challenge branch name: `automated-e2e-test-suite`

```
- Add Playwright-based tests to catch regressions in input, video, and connection
    - Verify WebSocket, ICE, WebRTC connection states and fake video track presence
- Ensure common setting changes also retain input, video and connection
- Add GitHub Action to run these tests on every PR
```

</details>

<details>

<summary>Multi-Session Support</summary>

Challenge branch name: `multi-session-support`

```
- Allow multiple concurrent connections to the same KVM
- Add control arbitration: define how keyboard/mouse input is handled when multiple sessions are active
```

</details>

## Use of AI Tools

You are welcome to use AI tools while working on this challenge. This reflects how we work day-to-day at JetKVM: AI can speed things up, but it’s not a substitute for thoughtful engineering.
What matters is that you **fully understand the code you submit and could explain it if asked.**

