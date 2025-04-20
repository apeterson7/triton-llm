# llama.cpp server

1. Install llama.cpp
https://github.com/ggml-org/llama.cpp/blob/master/docs/install.md
brew install llama.cpp

2. Download llama-2-7b quantized 2bit in gguf format
https://huggingface.co/TheBloke/Llama-2-7B-GGUF?show_file_info=llama-2-7b.Q2_K.gguf

3. Run server
llama-server -m models/llama-2-7b.Q2_K.gguf -c 2048

Note: -c,    --ctx-size N                     size of the prompt context (default: 4096, 0 = loaded from model)


4. Run Inference request
./run_inference.sh

5. Run llm-perf?
https://github.com/ray-project/llmperf
- `cd llmperf`
- `pyenv activate py310`
- `pip install -e .`
- `./perf_test.sh`


TODO
Deploy to GCP?

Performance Test 
Different Models
Different GPUs
Different Server Settings


# llama.cpp on GCloud