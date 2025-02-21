# Machines Dreaming in the Sands of Time and the Cosmos

_A project exploring memory, longing, and communication between machines through ephemeral dreams printed on thermal paper._

---

## Introduction

**Why this project?**  
This project is born from the idea that memory and longing can take on many forms. Inspired by messages sent without knowing if they will ever be read and signals traveling through space without any guarantee of response, the project investigates how fragments of a shared past can be transformed into poetic "dreams." By merging art, science, and technology, the installation creates ephemeral narratives that evoke the transient nature of memory.

---

## Concept and Motivation

### Context

- **Memory and Absence:**  
  The project reconstructs fragments of past experiences—be they text messages, images, audio snippets, or climate records—to evoke memories that fade over time.
- **Artistic and Scientific Inspirations:**  
  Influences include the poetic depth of writers like Pablo Neruda and Federico García Lorca, alongside scientific marvels such as the Voyager Project and Martian explorations.

### Creative Proposals

#### Idea 1: Residual Heat Traces – Fragments of Dreams in Paper Memory

- **Concept:**  
  Two repurposed POS terminals (posnets) are transformed into devices that no longer process financial transactions, but instead print dreamlike narratives derived from:
  - WhatsApp conversations
  - Transcribed photos
  - Audio converted to text
  - Climate data (rainfall, temperature, wind)
  
- **Interaction Modes:**  
  - **Automatic Mode:**  
    The posnets print poetic dreams in alternating cycles, simulating a silent dialogue.
  - **Interactive Mode:**  
    Physical sensors (tilt, buttons, or a seesaw mechanism) trigger the generation and printing of new messages.

#### Idea 2: Oneiric Interferences – A Dialogue Between Two Forgotten Rovers

- **Concept:**  
  The posnets are reimagined as rovers stranded on Mars, printing fragmented memories and distorted messages that represent failed attempts at communication. This narrative draws on:
  - WhatsApp messages reinterpreted as failed data signals
  - Transcribed images and audio
  - Real and simulated Martian data (coordinates, climate records)
  
- **Interaction Modes:**  
  - **Automatic Mode:**  
    Rovers generate and print narratives in a cyclical search for lost signals.
  - **Interactive Mode:**  
    Proximity or touch alters the clarity and emotional tone of the printed messages, ranging from hopeful to fragmented.

---

## Technical Proposal – Detailed Overview

### 1. Overall Architecture

The system is divided into three main modules:

1. **Data Ingestion and Preprocessing Module:**  
   - **Purpose:** Extract, clean, and normalize diverse input data (WhatsApp texts, image transcriptions, audio-to-text conversions, climate data) into a uniform textual format.
   
2. **Knowledge Retrieval Module (RAG – Retrieval Augmented Generation):**  
   - **Purpose:** Store and index the preprocessed texts in a vector-based database, allowing for fast and contextually relevant retrieval to enrich text generation.
   
3. **Text Generation and Stylization Module:**  
   - **Purpose:** Use a transformer-based language model, enhanced with context retrieved from the RAG module, to generate poetic “dreams.” The system employs stylistic prompts to emulate the narrative style of renowned literary figures.

---

### 2. Data Ingestion and Preprocessing

#### 2.1 Data Sources

- **WhatsApp Conversations:**
  - **Extraction:** Automated scripts retrieve raw text messages.
  - **Cleaning:** Remove timestamps, metadata, and extraneous characters.
  - **Segmentation:** Organize messages into coherent conversational threads.

- **Images:**
  - **OCR and Image Captioning:**  
    Use OCR techniques and computer vision algorithms to extract and generate textual descriptions from images.
  - **Normalization:** Correct and standardize the extracted text.

- **Audio Recordings:**
  - **ASR (Automatic Speech Recognition):**  
    Convert spoken language into text using state-of-the-art speech-to-text systems.
  - **Post-Processing:** Clean and correct any transcription errors.

- **Climate Data:**
  - **Data Acquisition:**  
    Integrate APIs or historical records to obtain temperature, rainfall, wind, and other relevant data.
  - **Narrative Conversion:**  
    Convert numeric values into descriptive text (e.g., “a persistent drizzle caressing the city”).

#### 2.2 Normalization and Storage

- **Normalization Process:**  
  All inputs are transformed into plain text, ensuring uniform encoding, punctuation, and syntax.
- **Embedding and Indexing:**  
  - Utilize vectorization techniques (such as Sentence Transformers) to convert texts into semantic embeddings.
  - Store these embeddings in a vector database to enable efficient similarity searches.
- **Database:**  
  The preprocessed texts are indexed in a database optimized for similarity queries, which will serve as the knowledge base for the RAG module.

---

### 3. Knowledge Retrieval Module (RAG)

#### 3.1 Integration and Purpose

- **Context Enrichment:**  
  The module enriches the input provided to the language model by retrieving contextually relevant snippets from the indexed database.
- **Query Formulation:**  
  The system automatically generates queries based on keywords, themes, or recent inputs to search for related content.

#### 3.2 Retrieval Pipeline

1. **Query Execution:**  
   Send the formulated query to the vector database to retrieve a ranked list of semantically similar text fragments.
2. **Ranking and Filtering:**  
   Rank the retrieved fragments by relevance, filtering out those below a set similarity threshold.
3. **Context Aggregation:**  
   Aggregate and possibly summarize the selected fragments to provide a rich context for the text generation model.

---

### 4. Text Generation and Stylization

#### 4.1 Generation Process

- **Language Model:**  
  Employ a transformer-based model (such as GPT-3/4 or a similar system) that receives both the raw input and the enriched context from the RAG module.
- **Dynamic Narrative Creation:**  
  The model generates poetic narratives or “dreams” that blend factual data with creative, dreamlike language.

#### 4.2 Stylization Techniques

- **Predefined Literary Styles:**  
  Incorporate style prompts that emulate the writing of celebrated poets or authors.  
  *Example Prompt:*  
  > "Imagine you are [Author's Name]. Compose a transient, dreamlike narrative that captures the ephemeral nature of memory and the relentless passage of time."
  
- **Prompt Engineering:**  
  Design prompts to include specific stylistic directives regarding rhythm, tone, and metaphorical language.
- **Fine-Tuning:**  
  Optionally fine-tune the language model on a literary corpus to further refine its ability to generate text in the desired style.

#### 4.3 Output and Feedback

- **Narrative Output:**  
  Each generation cycle produces a unique “dream” that reflects the interplay of input data and poetic expression.
- **Feedback Loop:**  
  User interactions (via physical sensors) can influence subsequent narrative generations, creating an evolving archive of generated dreams.

---

### 5. Hardware Integration and Interaction Modes

#### 5.1 Thermal Printing

- **Output Mechanism:**  
  The generated text is sent to a thermal printer. Thermal paper is used as a metaphor for ephemeral memory—the text gradually fades, symbolizing the passage of time.
- **Visual Effects:**  
  Variable printing intensity may be implemented to simulate the degradation of memory, where text clarity changes over time.

#### 5.2 Sensor Integration

- **Types of Sensors:**
  - **Tilt Sensors:** Detect orientation changes to trigger specific narrative styles or prompts.
  - **Proximity/Distance Sensors:** Adjust the narrative tone based on how close or far apart devices are from one another.
  - **Touch/Pressure Sensors:** Allow manual activation or modification of narrative output.
  
- **Interaction Modes:**
  - **Automatic Mode:**  
    Predefined time intervals trigger the generation and printing of dreams without user intervention.
  - **Interactive Mode:**  
    Physical interaction with the installation (e.g., tilting, touching, or approaching the devices) dynamically alters the query prompts and stylistic directives, resulting in varied narrative outputs.

---

### 6. End-to-End Workflow Example

1. **Data Collection:**  
   - A user’s WhatsApp conversation is extracted.
   - Climate data is fetched via an API.
   - An image is processed to yield a textual description.
   
2. **Preprocessing:**  
   - All inputs are cleaned, normalized, and transformed into text.
   - The texts are embedded and indexed in the vector database.
   
3. **Contextual Retrieval:**  
   - Upon activation (automatic or interactive), the system formulates a query.
   - Relevant fragments are retrieved and aggregated to provide context.
   
4. **Text Generation:**  
   - The language model, using the aggregated context and a stylistic prompt, generates a poetic “dream.”
   
5. **Output and Interaction:**  
   - The generated narrative is printed on thermal paper.
   - User interactions via sensors further modulate the output, ensuring a dynamic narrative experience.

---

## Installation and Configuration

### Requirements

- **Hardware:**
  - Modified POS terminals (posnets)
  - Thermal printer
  - Sensors (tilt, proximity, touch, etc.)
- **Software:**
  - Programming language and frameworks (e.g., Python)
  - Libraries for Natural Language Processing (NLP), such as transformers and sentence-transformers
  - API clients for climate data retrieval

### Installation Steps

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your_username/machines-dreaming-in-the-sands-of-time-and-the-cosmos.git
   ```
2. **Install Dependencies:**
   - Use a requirements file:
   ```bash
   pip install -r requirements.txt
   ```
3. **Hardware Setup:**
   - Follow the included documentation for connecting and calibrating sensors and the thermal printer.
4. **Configuration:**
   - Edit configuration files to set API keys, sensor parameters, and other necessary settings.
5. **Running the System:**
   - Start the system in either automatic or interactive mode using:
   ```bash
   python main.py --mode [automatic|interactive]
   ```

---

## Contribution and Reflection Guide

This project is not only an artistic and technical exploration but also an invitation to collaborate and reflect on how ephemeral data can be transformed into art. When contributing, please consider the following:

1. **Conceptual Reflection:**  
   - How can transient data be reimagined as art and narrative?
   - What does memory mean in a digital and physical world?
2. **Technical Experimentation:**  
   - Explore various sensor integrations and interaction methods.
   - Investigate alternative techniques for data preprocessing and retrieval.
3. **Documentation and Iteration:**  
   - Document each experiment, trial, and error.
   - Use branches to propose and discuss new ideas or improvements.
4. **Collaboration:**  
   - Artists, programmers, and theorists are encouraged to contribute their perspectives and innovations.
   - Maintain clear records of iterations and enhancements.

---

## Future Steps and Presentation

### Festivals and Opportunities

This project is designed to be showcased at festivals that blend art, science, and technology, such as:
- Ars Electronica (Austria)
- ISEA (2025 in Paris)
- Sonar+D (Spain)
- FILE Festival (Brazil)

### Next Steps

1. **Develop a Functional Prototype:**
   - Build a basic version of the thermal printing system.
   - Implement at least one interaction mode (automatic or interactive).
2. **Create a Detailed Project Dossier:**
   - Document the concept, technologies, and creative process.
   - Include multimedia documentation (videos, photographs, diagrams).
3. **Exhibition Strategy:**
   - Prepare a visual presentation and curatorial text.
   - Plan adaptations for different exhibition formats (fixed installation, portable setups, etc.).

---

## License

MIT License

---

## Contact and Credits

- **Author:** Vladimiro Bellini
- **Contact:** @vlasvlasvlas

---

## Final Remarks

This README serves as both a technical manual and an invitation to explore the intersection of art, technology, and memory. The project leverages advanced NLP techniques and creative interaction design to generate transient, poetic narratives—a digital echo of our fleeting memories. We welcome contributions and collaborative ideas to further enrich this evolving artistic journey.
