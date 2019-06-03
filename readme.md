<p align="center">
<img src="https://github.com/ntpz870817/DNA-storage-YYC/blob/master/logo.png" alt="YYC" title="YYC" width="60%"/>
</p>

---

**YYC** is a ...

## Environment Configuration
The kit is developed by **Python3.5**.

In addition, the packages we are calling now is as follows:

- [x] sys
- [x] os
- [x] random
- [x] math
- [x] struct
- [x] datetime
- [x] numpy
- [x] pickle

## Kit Tree Diagram
```html
├── utils                             // Util module
│    ├── data_handle.py               // Conversion of DNA motifs and binary document
│    ├── log.py                       // Outputting the logs in console
│    ├── model_saver.py               // Save model to file and load model from file
│    ├── monitor.py                   // Getting the progress  situation and the time left
│    ├── motif_friendly.py            // Determining whether motif is friendly to sequencing and synthesis
├── entry.py                          // Main calling function
├── README.md                         // Description document of kit
```

## Method of Application
In the encoding process, we first instantiate the method, and then pass the method and the necessary path into **entry**.

The specific usage is as follows:

```python
import yyc, entry

method = yyc.YYC()

entry.encode(method, input_path="C:\\init.mp4", output_path="C:\\target.dna", model_path="C:\\yyc.pkl")
```

In the decoding process, we first instantiate the method (using path of model file), and then pass the method and the necessary path into **entry**.

The specific usage (using init method) is as follows:

```python
import entry

entry.decode(input_path="C:\\target.dna", output_path="C:\\target.mp4", model_path="C:\\yyc.pkl")
```