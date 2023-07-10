# llama_hf_optimized

## Requirements

Pytorch >= 2.0.0 to support native flash attention

## Usage

### Before Generation (autoregressive decoding)

```
model.config.use_cache = True
model.config.cache_shape = (
    queries.shape[-1] + response_len,
)
```

### Before Training (forward-backward prop)

```
model.config.use_cache = False
```
