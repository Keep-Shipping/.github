<p align="center">
  <img src="https://raw.githubusercontent.com/Keep-Shipping/.github/main/assets/banner-keepshipping.png" alt="Keep Shipping. Deploys you can read." width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/STATUS-EARLY%20ACCESS-1950CC?style=for-the-badge&labelColor=11161F" alt="Status: early access">
  <img src="https://img.shields.io/badge/ONE%20FILE-PER%20REPO-EEF0F3?style=for-the-badge&labelColor=11161F" alt="One file per repo">
  <img src="https://img.shields.io/badge/LOCAL-%3D%20CI-EEF0F3?style=for-the-badge&labelColor=11161F" alt="Local equals CI">
</p>

<p align="center">
  <a href="https://keepshipping.run"><b>site</b></a> ·
  <a href="https://keepshipping.run/#early-access">early access</a> ·
  <a href="https://docs.keepshipping.run">docs</a> ·
  <a href="https://keepshipping.run/llms.txt">llms.txt</a>
</p>

---

**Changing a deploy pipeline shouldn't take eleven "fix ci" commits.** Most pipelines are hundreds of
lines of YAML nobody fully understands, Terraform and Docker glued together with shell scripts, and
the only way to test any of it is to push and wait.

**Keep Shipping is one typed, readable workflow file per repo.** It builds your images, plans and
applies your infrastructure, waits for a human where you say so, and deploys.

- **Checked first.** Every step has typed inputs and outputs. Wire a tag where a digest belongs and `keepshipping check` says so before anything runs.
- **Local = CI.** `keepshipping run` on your laptop is the same engine, file and steps as the runner.
- **Built in, not bolted on.** OCI images, Terraform and OpenTofu, approvals, Kubernetes, VMs and serverless are steps, not scripts.

Agents can write, check and run it too; a policy in the same file decides what waits for a person.

## Where it stands

| | What it is | Status |
| :--- | :--- | :--- |
| **Site** | [keepshipping.run](https://keepshipping.run): the idea, the workflow file, an honest comparison | **Live** |
| **Early access** | Invites in small batches. One email when yours is ready | **Open** |
| **`check` and `run`** | The typed workflow engine and CLI | **In development** |
| **Steps** | `oci.*`, `tofu.*` / `terraform.*`, `approval`, `k8s.rollout`, `vm.deploy`, `fn.deploy` | **In development** |
| **Blocks, `decide` (Jev), policy for agents** | Shared versioned steps, typed risk decisions, agent scoping | **Planned** |

The workflow files and CLI output on the site show the design, not measurements.

## Repositories

| Repo | What |
| :--- | :--- |
| [`harness`](https://github.com/Keep-Shipping/harness) | The engine, the `keepshipping` CLI, steps and docs. MIT |
| [`website`](https://github.com/Keep-Shipping/website) | The landing site. Static HTML, one CSS, one JS, Cloudflare Pages |

Questions, or a pipeline you'd like to throw at it: **contact@keepshipping.run**

Keep Shipping is a venture of [Factory Zero](https://factory0.ventures/) (Factory Zero Pte. Ltd.).
