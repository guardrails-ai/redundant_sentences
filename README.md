## Details

| Developed by | Guardrails AI |
| --- | --- |
| Date of development | Feb 15, 2024 |
| Validator type | Chatbots, QA |
| Blog |  |
| License | Apache 2 |
| Input/Output | Output |

## Description

This validator removes redundant sentences from an LLM response, resulting in a response that is more concise.

## Example Usage Guide

### Installation

```bash
$ gudardrails hub install remove-redundant-sentences
```

### Initialization

```python
redundant_sentences_validator = RemoveRedundantSentences(
	threshold=80,
	on_fail="noop"
)

# Create Guard with Validator
guard = Guard.from_string(
    validators=[redundant_sentences_validator, ...],
    num_reasks=2,
)
```

### Invocation

```python
guard(
    "LLM text with possible redundant sentences",
    metadata={"translation_source": "Original text"}
)
```

## API Ref

- `threshold`: The threshold used for matching redundancy.

## Intended use

- Primary intended uses: This is useful while building chatbots / QA bots.
- Out-of-scope use cases:

## Expected deployment metrics

|  | CPU | GPU |
| --- | --- | --- |
| Latency |  | - |
| Memory |  | - |
| Cost |  | - |
| Expected quality |  | - |

## Resources required

- Dependencies: `the_fuzz`
- Foundation model access keys: n/a
- Compute: n/a

## Validator Performance

### Evaluation Dataset

### Model Performance Measures

| Accuracy |  |
| --- | --- |
| F1 Score |  |

### Decision thresholds
