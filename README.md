# WFL-ASR: Whisper/WavLM for Phoneme Labeling

WFL-ASR is a configurable deep learning model designed for automatic phoneme segmentation using frame-level BIO tagging. It supports both Whisper and WavLM as audio encoders, and is structured for flexible and efficient training on phoneme-aligned datasets.

---

### Phase 1: Initial Setup

1. **Download the project files:** Get the main project files from [**here**](https://github.com/usamireko/WFL-ASR).
2. **Extract the files:** Unzip the downloaded folder to a location of your choice on your computer.
3. **Install dependencies:** Open your terminal.
   - Navigate to the main folder (where `requirements.txt` is located).
   - Run the following command:
     ```
     pip install -r requirements.txt
     ```
     > **Note:** You need to have Python installed on your PC.

---

### Phase 2: Model Installation

1. **Download the model:** Download the **AZTR WFL model** from [**here**](https://github.com/ZzHus272/WFL-ASR-AZTR/releases/tag/AZTR-model).
2. **Deploy the model:** Extract the model files directly into the directory, ensure they are contained within a folder named `aztr`.
3. **Verify Path:** Your directory structure should look like this:

```
aztr/
├── best_model.pt
├── config.yaml
├── langs.txt
└── phonemes.txt
```

---

### Phase 3: Running Inference

1. **Open your terminal:** Open PowerShell or CMD inside the main project folder.
2. **Execute the command:** Run the following command, making sure to replace `"data path"` with the actual path to the folder containing your data.

```bash
python infer.py "data path" --checkpoint "aztr/best_model.pt" --config "aztr/config.yaml" --output "data path" --device cuda --confidence-threshold 0.30
```

---
---

# WFL-ASR: Fonem labeling üçün Whisper/WavLM

**WFL-ASR** kadr səviyyəli **BIO** etiketləmədən istifadə edərək avtomatik fonem segmentasiyası üçün konfiqurasiya edilə bilən dərin öyrənmə modelidir. O, audio enkoderlər kimi həm **Whisper**, həm də **WavLM**-i dəstəkləyir və fonemlərə uyğunlaşdırılmış məlumat dəstlərində çevik və səmərəli təlim üçün strukturlaşdırılıb.

---

### Mərhələ 1: Quraşdırma

1. **Faylları yükləyin:** Əsas layihə fayllarını [**buradan**](https://github.com/usamireko/WFL-ASR) əldə edin.
2. **Faylları arxivdən çıxarın:** Yüklənmiş qovluğu kompüterinizdə istədiyiniz bir yerə köçürün (unzip edin).
3. **Asılılıqları (dependencies) quraşdırın:** Command Prompt və ya terminalı açın.
   - Əsas qovluğa (`requirements.txt` faylının olduğu yerə) keçid edin.
   - Bu komandanı daxil edib işə salın:
     ```
     pip install -r requirements.txt
     ```
     > **Qeyd:** Kompüterinizdə Python quraşdırılmış olmalıdır.

---

### Mərhələ 2: Modelin Quraşdırılması

1. **Modeli yükləyin:** AZTR WFL modelini [**buradan**](https://github.com/ZzHus272/WFL-ASR-AZTR/releases/tag/AZTR-model) yükləyin.
2. **Modeli yerləşdirin:** Model fayllarını birbaşa qovluğa çıxarın və onların `aztr` adlı bir qovluğun içərisində olduğundan əmin olun.
3. **Yolu yoxlayın:** Qovluq strukturunuz bu cür görünməlidir:

```
aztr/
├── best_model.pt
├── config.yaml
├── langs.txt
└── phonemes.txt
```

---

### Mərhələ 3: Modelin İşə Salınması (Inference)

1. **Terminalınızı açın:** Əsas layihə qovluğunun içində PowerShell və ya CMD-ni açın.
2. **Əmri icra edin:** `"data path"` hissəsini məlumatlarınızın olduğu qovluğun faktiki yolu ilə əvəz etdiyinizə əmin olaraq aşağıdakı əmri işə salın:

```bash
python infer.py "data path" --checkpoint "aztr/best_model.pt" --config "aztr/config.yaml" --output "data path" --device cuda --confidence-threshold 0.30
```
