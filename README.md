# README-AI

<img src="https://img.icons8.com/?size=512&id=55494&format=png" width="100" /><img src="https://img.icons8.com/?size=512&id=kTuxVYRKeKEY&format=png" width="100" />

Auto-generate informative `README.md` files using GPT language model APIs 👾

[![GitHub Workflow Status (with event)](https://img.shields.io/github/actions/workflow/status/eli64s/readme-ai/.github%2Fworkflows%2Frelease-pipeline.yml?logo=GitHub&label=cicd&color=c125ff)](https://github.com/eli64s/readme-ai/actions)
[![Codecov](https://img.shields.io/codecov/c/github/eli64s/readme-ai?logo=codecov&color=c125ff)](https://app.codecov.io/gh/eli64s/readme-ai)
[![PyPI version](https://img.shields.io/pypi/v/readmeai?color=c125ff)](https://badge.fury.io/py/readmeai)
[![PyPI python versions](https://img.shields.io/pypi/pyversions/readmeai.svg?color=c125ff)](https://pypi.python.org/pypi/readmeai/)
![License: MIT](https://img.shields.io/github/license/eli64s/readme-ai?color=c125ff)

---

## 🔗 Quick Links
- [README-AI](#readme-ai)
  - [🔗 Quick Links](#-quick-links)
  - [📍 Overview](#-overview)
  - [🤖 Demo](#-demo)
  - [📦 Features](#-features)
  - [🚀 Quick Start](#-quick-start)
    - [⚙️ Installation](#️-installation)
    - [👩‍💻 Running *README-AI*](#-running-readme-ai)
    - [🧪 Tests](#-tests)
    - [🧩 Configuration](#-configuration)
      - [Command-Line Options](#command-line-options)
      - [Custom Settings](#custom-settings)
  - [🚧 Project Roadmap](#-project-roadmap)
  - [📒 Changelog](#-changelog)
  - [🤝 Contributing](#-contributing)
  - [📄 License](#-license)
  - [👏 Acknowledgments](#-acknowledgments)

---

## 📍 Overview

***Objective***

Developer tool that automatically generates detailed `README.md` files using GPT language model APIs. Simply provide a repository URL or local directory path to your source code, and <em>README-AI</em> handles the documentation for you!

***Motivation***

Streamlines documentation creation and maintenance, enhancing developer productivity. <em>README-AI</em> aims to enable all skill levels, across all domains, to better understand, use, and contribute to open-source projects.<br>

> [!IMPORTANT]
>
> <em>README-AI</em> is currently under development with an opinionated configuration and setup. It is vital to review all text generated by the LLM APIs to ensure it accurately represents your project.

---

## 🤖 Demo

**README-AI standard use**: Standard usage of the <em>readme-ai</em> CLI tool.

[readmeai-cli-demo](https://github.com/eli64s/readme-ai/assets/43382407/89184f7c-1870-44b6-8175-c9c94fadeb6b)

**README-AI offline mode**: You can also run <em>readme-ai</em> without an API key by passing the `--offline` flag to the CLI.

[readmeai-cli-offline-demo](https://github.com/eli64s/readme-ai/assets/43382407/2c9b8456-80b9-4840-8da2-51780ed0c093)

> [!TIP]
>
> Offline mode is useful for quickly generating a boilerplate README without incurring API usage costs. See an example file generated using the `--offline` flag [readme-offline.md](https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-offline.md).

**Streamlit Web App**: Run <em>readme-ai</em> directly in your browser with Streamlit, no installation required!

[readmeai-streamlit-demo](https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-offline.md)

---

## 📦 Features

<br>
<div>
<details>
    <summary style="display: flex; align-items: center;">
        <span style="font-size: 2.0em;"> ❶ Badge Icons</span>
    </summary>
    <table>
        <tr>
            <td>
                <h4><i>Project Slogan and Badges</i></h4>
                <p>
                    ‣ A slogan to highlight your poject is generated by <a href="https://github.com/eli64s/readme-ai/blob/main/readmeai/settings/config.toml#L33">prompting</a> OpenAI's GPT engine.
                    </p>
                <p>
                    ‣ Codebase dependencies and metadata are visualized using <a href="https://shields.io/">Shields.io</a> badges.
                </p>
            </td>
        </tr>
        <tr>
            <td>
                <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/badges.png" alt="badges" />
            </td>
        </tr>
    </table>
    <table>
        <p>
            ‣ Use the CLI option <code>--badges</code> to select the style of badges for your README! <br>
            ‣ 6 options currently supported: <i>flat (default), flat-square, plastic, for-the-badge, social, square</i>. Find a few examples below.
        <tr>
            <td>
                <h4 style="text-align:left;">1. Shieldsio <em>flat</em> badge style</h4>
                <p style="text-align:left;">Command: none as its the default style for <em>readme-ai</em></p>
                <div style="text-align:center;">
                    <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/badges-shieldsio-default.png" alt="badges-shieldsio-default" />
                </div>
            </td>
        </tr>
        <tr>
            <td>
                <h4 style="text-align:left;">2. Shieldsio <em>for-the-badge</em> style</h4>
                <p style="text-align:left;">Command: <code>--badges for-the-badge</code></p>
                <div style="text-align:center;">
                    <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/badges-shieldsio-flat.png" alt="badges-shieldsio-flat" />
                </div>
            </td>
        </tr>
        <tr>
            <td>
                <h4 style="text-align:left;">3. Square <em>iOS style</em> badges</h4>
                <p style="text-align:left;">Command: <code>--badges square</code></p>
                <div style="text-align:center;">
                    <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/badges-square.png" alt="badges-square" />
                </div>
            </td>
        </tr>
    </table>
</details>
</div>
<br>
<div>
    <details>
        <summary style="display: flex; align-items: center;">
            <span style="font-size: 2.0em;"> ❷ Code Documentation</span>
        </summary>
        <table>
            <tr>
                <td colspan="2">
                    <h4><i>Directory Tree and File Summaries</i></h4>
                </td>
            </tr>
            <tr>
                <td colspan="2">
                    <p>‣ Your project's directory structure is visualized using a custom tree function.</p>
                    <p>‣ Each file in the codebase is summarized by OpenAI's <i>GPT</i> model.</p>
                </td>
            </tr>
            <tr>
                <td align="center">
                    <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/repository-tree.png" alt="repository-tree" />
                </td>
                <td align="center">
                    <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/code-summaries.png" alt="code-summaries" />
                </td>
            </tr>
        </table>
    </details>
</div>
<br>
<div>
    <details>
        <summary style="display: flex; align-items: center;">
            <span style="font-size: 2.0em;"> ❸ Features Table</span>
        </summary>
        <table>
            <tr>
                <td>
                    <h4><i>Prompted Text Generation</i></h4>
                    <p>
                        ‣ An overview paragraph and features table are generated using <a href="https://github.com/eli64s/readme-ai/blob/main/readmeai/settings/config.toml#L28">detailed prompts</a>, embedded with project metadata.
                    </p>
                </td>
            </tr>
            <tr>
                <td>
                    <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/feature-table.png" alt="feature-table" />
                </td>
            </tr>
        </table>
    </details>
</div>
<br>
<div>
    <details>
        <summary style="display: flex; align-items: center;">
            <span style="font-size: 2.0em;"> ❹ Dynamic Quick Start Section</span><br>
        </summary>
        <table>
            <tr>
                <td>
                    <h4><i>Installation, Running, and Test</i></h4>
                    <p>
                        ‣ Generates instructions for installing, running, and testing your project. Instructions are created by identifying the codebase's top language and referring to our <a href="https://github.com/eli64s/readme-ai/blob/main/readmeai/settings/language_setup.toml">language_setup.toml</a> configuration file.
                    </p>
                </td>
            </tr>
            <tr>
                <td>
                    <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/usage-instructions.png" alt="usage-instructions" />
                </td>
            </tr>
        </table>
    </details>
</div>
<br>
<div>
    <details>
        <summary style="display: flex; align-items: center;">
            <span style="font-size: 2.0em;"> ❺ Additional README Sections</span><br>
        </summary>
        <table>
            <tr>
                <td>
                    <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/roadmap.png" alt="roadmap" />
                </td>
            </tr>
            <br>
            <tr>
                <td>
                    <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/license.png" alt="license" />
                </td>
            </tr>
        </table>
    </details>
</div>
<br>
<div>
<details>
    <summary style="display: flex; align-items: center;">
        <span style="font-size: 2.0em;">❻ Templates (coming soon)</span><br>
    </summary>
    <table>
        <tr>
            <td>
                <p>‣ Developing CLI option letting users select from a variety of README styles</p>
                <p>‣ Templates for use-cases such as data, machine learning, web development, and more!</p>
            </td>
        </tr>
        <tr>
            <td>
                <h3>AI & ML README Template Concept</h3>
                <ul>
                    <li><strong><a href="#overview">Overview</a></strong>: Summary of the projects' objectives, scope, and expected outcomes.</li>
                    <li><strong><a href="#project-structure">Project Structure</a></strong>: Overview of the organization of the projects and their main components.</li>
                    <li><strong><a href="#data-collection-and-preprocessing">Data Preprocessing</a></strong>: Data sources, collection methods, and types of data</li>
                    <li><strong><a href="#feature-engineering">Feature Engineering</a></strong>: Importance of feature engineering and its impact on model performance.</li>
                    <li><strong><a href="#model-architecture-and-development">Model Architecture and Development</a></strong>: Model selection, dev strategies, and implemented algorithms.</li>
                    <li><strong><a href="#training-and-validation">Training and Validation</a></strong>: Info on model training procedures, hyperparameter tuning, and validation strategies.</li>
                    <li><strong><a href="#testing-and-evaluation">Testing and Evaluation</a></strong>: Model testing results, performance analysis, and comparison with benchmarks.</li>
                    <li><strong><a href="#deployment-and-integration">Deployment and Integration</a></strong>: Integration with other systems, APIs, and user interfaces</li>
                    <li><strong><a href="#usage-and-maintenance">Usage and Maintenance</a></strong>: User guide on how to use the deployed models and interfaces.</li>
                    <li><strong><a href="#results-and-discussion">Results and Discussion</a></strong>: Implications, limitations, and future work.</li>
                    <li><strong><a href="#ethical-considerations">Ethical Considerations</a></strong>: Ethical aspects, data privacy, and fairness in model predictions.</li>
                    <li><strong><a href="#contributing">Contributing</a></strong>: Procedures for submitting contributions, reporting issues, and proposing enhancements.</li>
                    <li><strong><a href="#acknowledgements">Acknowledgements</a></strong>: References to resources, libraries, and frameworks used.</li>
                    <li><strong><a href="#license">License</a></strong>: Explanation of usage rights, restrictions, and attribution requirements.</li>
                </ul>
            </td>
        </tr>
    </table>
</details>
</div>
<br>
<div>
    <details>
        <summary style="display: flex; align-items: center;">
            <span style="font-size: 2.0em;"> ❼ Example README Files</span><br>
        </summary>
        <table>
            <thead>
                <tr>
                    <th></th>
                    <th>Output File</th>
                    <th>Repository</th>
                    <th>Languages</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>1️⃣</td>
                    <td><a href="https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-python.md">readme-python.md</a></td>
                    <td><a href="https://github.com/eli64s/readme-ai">readme-ai</a></td>
                    <td>Python</td>
                </tr>
                <tr>
                    <td>2️⃣</td>
                    <td><a href="https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-typescript.md">readme-typescript.md</a></td>
                    <td><a href="https://github.com/Yuberley/ChatGPT-App-React-Native-TypeScript">chatgpt-app-react-typescript</a></td>
                    <td>TypeScript, React</td>
                </tr>
                <tr>
                    <td>3️⃣</td>
                    <td><a href="https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-javascript.md">readme-javascript.md</a></td>
                    <td><a href="https://github.com/idosal/assistant-chat-gpt-javascript">(repository deleted)</a></td>
                    <td>JavaScript, React</td>
                </tr>
                <tr>
                    <td>4️⃣</td>
                    <td><a href="https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-kotlin.md">readme-kotlin.md</a></td>
                    <td><a href="https://github.com/rumaan/file.io-Android-Client">file.io-android-client</a></td>
                    <td>Kotlin, Java, Android</td>
                </tr>
                <tr>
                    <td>5️⃣</td>
                    <td><a href="https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-rust-c.md">readme-rust-c.md</a></td>
                    <td><a href="https://github.com/DownWithUp/CallMon">rust-c-app</a></td>
                    <td>C, Rust</td>
                </tr>
                <tr>
                    <td>6️⃣</td>
                    <td><a href="https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-go.md">readme-go.md</a></td>
                    <td><a href="https://github.com/olliefr/docker-gs-ping">go-docker-app</a></td>
                    <td>Go</td>
                </tr>
                <tr>
                    <td>7️⃣</td>
                    <td><a href="https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-java.md">readme-java.md</a></td>
                    <td><a href="https://github.com/avjinder/Minimal-Todo">java-minimal-todo</a></td>
                    <td>Java</td>
                </tr>
                <tr>
                    <td>8️⃣</td>
                    <td><a href="https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-fastapi-redis.md">readme-fastapi-redis.md</a></td>
                    <td><a href="https://github.com/FerrariDG/async-ml-inference">async-ml-inference</a></td>
                    <td>Python, FastAPI, Redis</td>
                </tr>
                <tr>
                    <td>9️⃣</td>
                    <td><a href="https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-mlops.md">readme-mlops.md</a></td>
                    <td><a href="https://github.com/GokuMohandas/mlops-course">mlops-course</a></td>
                    <td>Python, Jupyter</td>
                </tr>
                <tr>
                    <td>🔟</td>
                    <td><a href="https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-pyflink.md">readme-pyflink.md</a></td>
                    <td><a href="https://github.com/eli64s/flink-flow">flink-flow</a></td>
                    <td>PyFlink</td>
                </tr>
            </tbody>
        </table>
    </details>
</div>
<br>

<p align="right">
  <a href="#top"><b>Return</b></a>
</p>

---

## 🚀 Quick Start

***Prerequisites***

Ensure that you have the following dependencies installed on your system.

- Python 3.9, 3.10, 3.11, or 3.12
- A package manager or container runtime (pip, docker, conda, etc.)
- OpenAI API ***paid*** account and API key

***Code Repository***

A remote repository URL or local directory path to your project is required to generate a README file. The following repository sources are currently supported.
- GitHub
- GitLab
- Bitbucket
- File System

***OpenAI API***

An OpenAI API account and API key are needed to use *readme-ai*. The following steps outline the process.

<details closed><summary>🔐 OpenAI API Account Setup</summary>

1. Go to the [OpenAI website](https://platform.openai.com/).
2. Click the "Sign up for free" button.
3. Fill out the registration form with your information and agree to the terms of service.
4. Once logged in, click on the "API" tab.
5. Follow the instructions to create a new API key.
6. Copy the API key and keep it in a secure place.

</details>

Additionally, It is essential to understand the potential risks and costs associated with using LLM APIs.

> [!WARNING]
>
> Please review the following information before using *readme-ai*.
>
> 1. **Review Sensitive Information!**: Before running <em>README-AI</em>, ensure all content in your repository is free of sensitive information. <em>README-AI</em> DOES NOT filter out sensitive data from your codebase and generated README file. <em>README-AI</em> DOES NOT alter your codebase in any way, and it is your responsibility to review your codebase before generating a README file, as well as after before publishing it.
>
> 2. **API Usage Costs**: The OpenAI API is not free. Thus, you will be charged for each request made by <em>README-AI</em>. Costs can accumulate rapidly, so it's essential to be aware of your usage. Please monitor your API usage and associated costs by visiting the [OpenAI API Usage Dashboard](https://platform.openai.com/account/usage).
>
> 3. **Paid Account Recommended**: Setting up a paid OpenAI account is highly recommended to avoid potential issues. Without a payment method on file, your API usage will be restricted to base OpenAI's base models. This may result in less accurate README file content and potential errors may occur. For more details, see the [OpenAI Pricing Page](https://openai.com/pricing/).

<p align="right">
  <a href="#top"><b>Return</b></a>
</p>

---

### ⚙️ Installation

Using `pip`
```sh
pip install readmeai
```

Using `docker`
```sh
docker pull zeroxeli/readme-ai:latest
```

Using `conda`
```sh
conda install -c conda-forge readmeai
```

Alternatively, clone the readme-ai repository and build from source.

```sh
git clone https://github.com/eli64s/readme-ai && \
cd readme-ai
```

Then use one of the methods below to install the project's dependencies (Bash, Conda, Pipenv, or Poetry).

Using `bash`
```sh
bash setup/setup.sh
```

Using `pipenv`
```sh
pipenv install && \
pipenv shell
```

Using `poetry`
```sh
poetry install && \
poetry shell
```

---

### 👩‍💻 Running *README-AI*

Before running the application, ensure that you have an OpenAI API key and that it is set as an environment variable.

On `Linux` or `MacOS`
```sh
export OPENAI_API_KEY=YOUR_API_KEY
```

On `Windows`
```sh
set OPENAI_API_KEY=YOUR_API_KEY
```

Use one of the methods below to run the application (Pip, Docker, Conda, Streamlit, etc).

Using `pip`
```sh
readmeai --repository https://github.com/eli64s/readme-ai
```

Using `conda`
```sh
readmeai -r https://github.com/eli64s/readme-ai
```

Using `docker`

```sh
docker run -it \
-e OPENAI_API_KEY=$OPENAI_API_KEY \
-v "$(pwd)":/app zeroxeli/readme-ai:latest \
-r https://github.com/eli64s/readme-ai
```

Using `streamlit`

Try *readme-ai* in your browser using the Streamlit web app. No installation required!

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://readmeai.streamlit.app/)

> [!NOTE]
>
> Hosted on <a href="https://streamlit.io/">Streamlit Community Cloud</a>.
>
> Streamlit App may be unavailable at times as this is a free service.
>
> See the <a href="https://github.com/eli64s/readme-ai-streamlit">readme-ai-streamlit</a> repository for more details.

For the complete list of CLI options and README customization settings, see the [Configuration](#-configuration) section.

Alternatively, you can run the *readme-ai* application directly from the source code.

Using `pipenv`
```sh
pipenv shell && \
python3 -m readmeai.cli.commands -o readme-ai.md -r https://github.com/eli64s/readme-ai
```

Using `poetry`
```sh
poetry shell && \
poetry run python3 -m readmeai.cli.commands -o readme-ai.md -r https://github.com/eli64s/readme-ai
```

---

### 🧪 Tests

Use `pytest` to run the default test suite.
```sh
make test
```

Use `nox` to run the test suite against multiple Python versions `(3.9, 3.10, 3.11, 3.12)`.
```sh
nox -f noxfile.py
```
> [!NOTE]
>
> Nox is an automation toolkit that makes it easier to manage multiple Python testing environments. See the [Nox documentation](https://nox.thea.codes/en/stable/) for more details.

---

### 🧩 Configuration

Run the `readmeai` command in your terminal with the following options to tailor your README file.

#### Command-Line Options

| Flag (Long/Short) | Default | Description | Type | Status |
|-------------------|---------|-------------|------|--------|
| `--align`/`-a` | `center` | Set header text alignment (`left`, `center`). | String | Optional |
| `--api-key`/`-k` | `OPENAI_API_KEY` env var | Your GPT model API key. | String | Optional |
| `--badges`/`-b` | `flat` | Badge style options for your README file. | String | Optional |
| `--emojis`/`-e` | `False` | Add emojis to section header tiles. | Boolean | Optional |
| `--image`/`-i` | `default` | Project logo image displayed in README header. | String | Optional |
| `--model`/`-m` | `gpt-3.5-turbo` | Select GPT model for content generation. | String | Optional |
| `--offline` | `False` | Generate a README without an API key. | Boolean | Optional |
| `--output`/`-o` | `readme-ai.md` | README output file name. | Path/String | Optional |
| `--repository`/`-r` | None | Repository URL or local path. | URL/String | Required |
| `--temperature`/`-t` | `1.0` | LLM API creativity level. | Float | Optional |
| `--template` | None | Choose README template. | String | <em>WIP</em> |
| `--language`/`-l` | `English (en)` | Language for content. | String | <em>WIP</em> |

<sub><em>WIP</em> = work in progress, or feature currently under development.<br>For additional command-line information, run <code>readmeai --help</code> in your terminal for more details about each option.</sub><br><br>

**Badge Icons**

Select your preferred badge icon style for your README file using the `--badges` flag. The following options are currently supported.

| Badge | Preview |
|------------------|----------|
| `flat`           | ![flat](https://img.shields.io/badge/Python-3776AB.svg?&style=flat&logo=Python&logoColor=white) |
| `flat-square`    | ![flat-square](https://img.shields.io/badge/Python-3776AB.svg?&style=flat-square&logo=Python&logoColor=white) |
| `for-the-badge`  | ![for-the-badge](https://img.shields.io/badge/Python-3776AB.svg?&style=for-the-badge&logo=Python&logoColor=white) |
| `plastic`        | ![plastic](https://img.shields.io/badge/Python-3776AB.svg?&style=plastic&logo=Python&logoColor=white) |
| `skills`          | [![Skills](https://skillicons.dev/icons?i=py)](https://skillicons.dev) |
| `skills-light`    | [![Skills-Light](https://skillicons.dev/icons?i=py&theme=light)](https://skillicons.dev) |
| `social`         | ![social](https://img.shields.io/badge/Python-3776AB.svg?&style=social&logo=Python&logoColor=white) |

<br>

**Project Logo**

Select an image to display in your README header section using the `--image` flag. The following options are currently supported.

| Image | Preview |
|----------------|-------|
| `custom`       | Provide a custom image URL. |
| `black`  | <img src="https://img.icons8.com/external-tal-revivo-regular-tal-revivo/96/external-readme-is-a-easy-to-build-a-developer-hub-that-adapts-to-the-user-logo-regular-tal-revivo.png" width="100" height="100" alt="readme-blue"> |
| `blue`      | <img src="https://raw.githubusercontent.com/PKief/vscode-material-icon-theme/ec559a9f6bfd399b82bb44393651661b08aaf7ba/icons/folder-markdown-open.svg" width="100" height="100" alt="default"> |
| `gradient`     | <img src="https://img.icons8.com/nolan/96/markdown.png" width="100" height="100" alt="gradient"> |
| `purple`       | <img src="https://img.icons8.com/external-tal-revivo-duo-tal-revivo/100/external-markdown-a-lightweight-markup-language-with-plain-text-formatting-syntax-logo-duo-tal-revivo.png" width="100" height="100" alt="purple"> |
| `yellow`       | <img src="https://img.icons8.com/pulsar-color/96/markdown.png" width="100" height="100" alt="yellow"> |

#### Custom Settings

To customize the README file generation process in the readme-ai CLI tool, you can modify the project's [configuration file](https://github.com/eli64s/readme-ai/blob/main/readmeai/settings/config.toml). The configuration file is structured using Pydantic models, which are described below in detail.

<details closed><summary>🔠 Pydantic Models</summary>
<br>

`ApiConfig`
- **Description**: Pydantic model for OpenAI API configuration.
- **Attributes**:
  - `endpoint`: The endpoint URL for the OpenAI API.
  - `encoding`: Encoding settings for the API.
  - `model`: The model of the OpenAI language.
  - `rate_limit`: API rate limit.
  - `tokens`: Token limit per request.
  - `tokens_max`: Maximum token limit.
  - `temperature`: Temperature setting for the language model.

`CliConfig`
- **Description**: CLI options for the readme-ai application.
- **Attributes**:
  - `emojis`: Boolean to enable or disable emojis.
  - `offline`: Boolean to enable or disable offline mode.

`GitConfig`
- **Description**: Configuration for Git repository settings.
- **Attributes**:
  - `repository`: Repository URL or local path.
  - `source`: Source of the repository (GitHub, GitLab, etc.).
  - `name`: Optional name for the project.

`MarkdownConfig`
- **Description**: Pydantic model for Markdown code blocks that are used to build and format the README file.
- **Attributes**: Various attributes for markdown formatting like `align`, `image`, `badges`, etc.

`PathsConfig`
- **Description**: Pydantic model for configuration file paths.
- **Attributes**: Paths for various configuration files like `dependency_files`, `ignore_files`, `language_names`, etc.

`PromptsConfig`
- **Description**: Pydantic model for OpenAI prompts.
- **Attributes**: Contains strings for features, overview, slogan, and summaries prompts.

`AppConfig`
- **Description**: Nested Pydantic model for the entire configuration.
- **Sub-Models**: Includes all the above configurations as sub-models.

`AppConfigModel`
- **Description**: Pydantic model for the entire configuration.
- **Attributes**: Contains the `AppConfig` as a sub-model.

`ConfigHelper`
- **Description**: Helper class to load additional configuration files.
- **Functionality**: This class extends the base configuration with additional settings loaded from TOML files.

`Additional Functions`
- **load_config**: Function to load the main configuration from a TOML file.
- **load_config_helper**: Function to load multiple configuration helper TOML files.

</details>

<p align="right">
  <a href="#top"><b>Return</b></a>
</p>

---

## 🚧 Project Roadmap

- [X] Publish project as a Python library via PyPI for easy installation.
  - [*PyPI - readmeai*](https://pypi.org/project/readmeai/)
- [X] Make project available as a Docker image on Docker Hub.
  - [*Docker Hub - readme-ai*](https://hub.docker.com/repository/docker/zeroxeli/readme-ai/general)
- [X] Integrate and deploy app with Streamlit to make tool more widely accessible.
  - [*Streamlit Community Cloud - readmeai*](https://readmeai.streamlit.app/)
- [ ] Refactor our large language model engine to enable more robust README generation.
  - [ ] Explore [LangChain 🦜️🔗](https://python.langchain.com/docs/get_started/introduction) as an alternative to using the OpenAI API directly.
  - [ ] Explore [LlamaIndex 🦙](https://gpt-index.readthedocs.io/en/stable/index.html) framework and Retrieval Augmented Generation (RAG) paradigm.
- [ ] Building template system to create README files for specific use-cases (data, mobile, web, etc.)
- [ ] Add support for generating README files in any language (i.e. CN, ES, FR, JA, KO, RU).
- [ ] Develop GitHub Actions script to automatically update the README file when new code is pushed.



## 📒 Changelog

[Changelog](https://github.com/eli64s/readme-ai/blob/main/CHANGELOG.md)



## 🤝 Contributing

- [Discussions](https://github.com/eli64s/readme-ai/discussions)
- [Open an Issue](https://github.com/eli64s/readme-ai/issues)
- [Contributing Guidelines](https://github.com/eli64s/readme-ai/blob/main/CONTRIBUTING.md)



## 📄 License

[MIT](https://github.com/eli64s/readme-ai/blob/main/LICENSE)



## 👏 Acknowledgments

*Badges*
  - [Shields.io](https://shields.io/)
  - [Aveek-Saha/GitHub-Profile-Badges](https://github.com/Aveek-Saha/GitHub-Profile-Badges)
  - [Ileriayo/Markdown-Badges](https://github.com/Ileriayo/markdown-badges)
  - [tandpfun/skill-icons](https://github.com/tandpfun/skill-icons)


<p align="right">
  <a href="#top"><b>Return</b></a>
</p>

---
