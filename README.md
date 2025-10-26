# Transliteration_RNN_LSTM
Develop a model to translate from one language to another character using  RNN LSTM

==================================================================

--- Test Set Results ---
✅ Exact Match Accuracy: 26.50%
📊 Character Error Rate (CER): 23.67%

==================================================================
      Dynamic Model Analysis (for 1-Layer GRU)
==================================================================

--- Model Configuration ---
  - Cell Type: GRU (hardcoded in notebook)
  - Num Layers (n): 1 (hardcoded in notebook)
  - Embedding Dim (e): 256
  - Hidden Dim (h): 512
  - Source Vocab (V_src): 29
  - Target Vocab (V_tgt): 67

--- 1. Practical Parameter Calculation (from Config) ---
  1. Encoder Embedding (V_src * e):           29 * 256 =      7,424
  2. Encoder GRU (n=1):                         1,182,720
  3. Decoder Embedding (V_tgt * e):           67 * 256 =     17,152
  4. Decoder GRU (n=1):                         1,182,720
  5. Decoder Linear (h * V_tgt + V_tgt): (512 * 67) + 67 =     34,371
  --------------------------------------------------
  CALCULATED TOTAL:                         2,424,387

--- Verification ---
  - Actual Model Parameters:             2,424,387
  - Verification:                  ✅ MATCH
==================================================================

--- Transliteration (Hindi) ---

🔤 > ghar
   → घर

🔤 > ajanabee
   → अजनबी

🔤 > jivasham
   → जिवशम

🔤 > quit
