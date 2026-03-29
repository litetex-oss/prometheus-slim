# prometheus-slim
A fork of [prometheus](https://github.com/prometheus/prometheus) that removes all plugins and code placed for lobbying

## Why?

While inspecting prometheus that the binary is huge (200MB) and contains a lot of 3rd party vendor code that I will likely never need.

After removing this code the binary was 3-4x smaller.

## What is removed?

* All [plugins](https://github.com/prometheus/prometheus/tree/main/plugins)/"service discovery"
* Propietary code for propietary platforms introduced by "lobbying"
  * Sigv4 aka AWS Signature Version 4
  * AzureAD
  * GoogleIAM

## How?
The updating logic can be found in the [sidecar repo](https://github.com/litetex-oss/prometheus-slim-manager).
