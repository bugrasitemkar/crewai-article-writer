# CrewAI Article Writer

A multi-agent system built with CrewAI that automatically researches, writes, and edits blog articles using AI agents working in collaboration.

## Repository Name
`crewai-article-writer`

## Overview

This project demonstrates how to create a team of AI agents that work together to produce high-quality blog articles. The system uses three specialized agents:

- **Content Planner**: Researches and creates comprehensive content outlines
- **Content Writer**: Writes engaging articles based on the planner's research
- **Editor**: Reviews and refines the final content for publication

## Features

- **Multi-Agent Collaboration**: Three AI agents working sequentially to produce articles
- **Customizable Topics**: Generate articles on any topic of your choice
- **SEO-Optimized Content**: Includes keyword research and optimization
- **Markdown Output**: Ready-to-publish formatted content
- **Journalistic Standards**: Balanced viewpoints and fact-checking

## Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/crewai-article-writer.git
cd crewai-article-writer
```

2. Install the required dependencies:
```bash
pip install -r requirements.txt
```

3. Set up your OpenAI API key:
```bash
export OPENAI_API_KEY="your-api-key-here"
```

## Dependencies

```
crewai==0.28.8
crewai_tools==0.1.6
langchain_community==0.0.29
```

## Usage

### Basic Usage

```python
from crewai import Agent, Task, Crew

# Run the article generation crew
result = crew.kickoff(inputs={"topic": "Artificial Intelligence"})
print(result)
```

### Custom Topic Example

```python
# Generate an article on your chosen topic
topic = "Sustainable Energy Solutions"
result = crew.kickoff(inputs={"topic": topic})

# Display as markdown
from IPython.display import Markdown
Markdown(result)
```

## Agent Roles

### Content Planner
- **Role**: Research and planning specialist
- **Goal**: Create comprehensive content plans with SEO keywords
- **Output**: Detailed outline with audience analysis and resources

### Content Writer
- **Role**: Article writing specialist
- **Goal**: Transform plans into engaging, factual articles
- **Output**: Well-structured blog post in markdown format

### Editor
- **Role**: Content quality specialist
- **Goal**: Ensure journalistic standards and brand alignment
- **Output**: Polished, publication-ready article

## Workflow

1. **Planning Phase**: The planner researches the topic and creates a detailed outline
2. **Writing Phase**: The writer creates the article based on the plan
3. **Editing Phase**: The editor reviews and refines the content

## Configuration

The system is configured to use OpenAI's GPT-3.5-turbo by default. You can modify the LLM by updating the environment variables:

```python
os.environ["OPENAI_MODEL_NAME"] = 'gpt-3.5-turbo'
```

## Alternative LLM Support

The system supports various LLM providers:

- **Hugging Face Hub**
- **Mistral API**
- **Cohere**
- **Local models via Ollama**

See the notebook for configuration examples.

## Output Format

The system generates articles in markdown format with:
- Engaging titles and subtitles
- 2-3 paragraphs per section
- SEO-optimized content
- Proper structure (intro, body, conclusion)
- Balanced viewpoints

## Example Output Structure

```markdown
# Article Title

## Introduction
[Engaging introduction paragraphs]

## Key Point 1
[Detailed discussion with supporting information]

## Key Point 2
[Further analysis and insights]

## Conclusion
[Summary and call to action]
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Built with [CrewAI](https://crewai.com/) framework
- Powered by OpenAI's language models
- Inspired by collaborative AI agent workflows

## Support

If you encounter any issues or have questions, please open an issue in the GitHub repository.

---

**Note**: This is an educational project demonstrating multi-agent AI systems. Always review and verify the generated content before publication.
