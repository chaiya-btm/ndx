# 🧭 NDX — The Universal Document Index

> **NDX** is the next-generation document format — designed for both **humans and AI**.  
> A universal, intelligent, and interoperable alternative to PDF — built for the age of connected knowledge.

[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](LICENSE)
[![Status](https://img.shields.io/badge/status-in%20development-yellow.svg)](https://github.com/ndx-org/ndx)
[![PDF Compatible](https://img.shields.io/badge/PDF%202.0-compatible-green.svg)](https://www.iso.org/standard/63534.html)

---

## 🌍 Overview

NDX (short for **"Next Document eXchange"**) redefines how digital documents are created, stored, and understood.  

It goes beyond static layouts by embedding **semantic meaning, metadata, and data structure** directly into the file. NDX can be read by humans like a normal document, and by AI systems as structured knowledge.

**In short:**  
> PDF is for printing.  
> NDX is for thinking — and still prints perfectly.

---

## ✨ Key Features

- **🧠 AI-Native Format** – Documents that are readable, indexable, and interpretable by AI and LLMs.  
- **🔗 Structured Data** – Supports embedded JSON, XML, or schema-linked data inside the document.  
- **📄 Human-Friendly Design** – Retains full readability, layout, and typography.  
- **🖨️ Print-Compatible** – Designed to print exactly like PDF — same layout, margins, and precision.  
- **🪄 Drop-in Replacement** – Can be used anywhere a PDF is used today: reports, receipts, invoices, contracts, etc.  
- **⚡ Extensible Framework** – Can be parsed and rendered on web, desktop, or POS/ERP systems.  
- **🔒 Secure and Verifiable** – Supports digital signatures, versioning, and traceable metadata.  
- **🌐 Interoperability First** – Integrates seamlessly with existing systems, APIs, and open standards.  
- **📐 ISO 32000-2 Compatible** – Full bidirectional conversion with PDF 2.0 standard.

---

## 🧩 Tech Stack

| Layer | Technology |
|-------|-------------|
| **Core Engine** | **Rust** — High-performance, memory-safe engine for NDX binary container, layout rendering, and serialization |
| **Format Specification** | JSON + Binary container (NDX Core Spec) |
| **Renderer** | Web (HTML5), Desktop (.NET/Electron), Mobile (Flutter/React Native) |
| **AI Interface** | Schema-based metadata + LLM/RAG integration |
| **Storage Layer** | AWS S3 / IPFS / NDX Cloud |
| **Developer Tools** | NDX SDK (Rust, TypeScript, Python, C#) |
| **Build & Deployment** | Docker, CI/CD (GitHub Actions), WebAssembly (WASM) for lightweight clients |

### 🦀 Why Rust?

Rust powers NDX's core engine because it delivers:

- **Performance** – NDX document rendering is up to **10x faster** than traditional PDF engines
- **Safety** – Memory-safe architecture prevents common vulnerabilities
- **Cross-Platform** – Compiles to native binaries (Windows, macOS, Linux) and WebAssembly
- **Concurrency** – Efficient parallel processing for large document operations
- **Future-Proof** – Modern language with strong ecosystem and active development

---

## 🚀 Vision & Roadmap

### **Phase 1: Foundation (2025)**
- ✅ Define NDX core format specification  
- 🔄 Create converter tools (PDF ⇄ NDX)  
- 🔄 Build NDX Viewer/Renderer for web and desktop  
- 🔄 Release Rust SDK and CLI tools

### **Phase 2: AI Integration (2026)**
- Support embedded knowledge graphs and semantic layers  
- Enable NDX-to-RAG indexing pipelines  
- Introduce NDX metadata APIs  
- Launch vector search integration

### **Phase 3: Ecosystem (2027+)**
- Launch NDX Cloud and developer SDK  
- Integrate NDX with POS/ERP/Document systems  
- Open NDX Marketplace for AI-compatible documents  
- Establish NDX as ISO standard

---

## 🧠 Why NDX?

NDX isn't just a file format.  
It's a **knowledge vessel** — bridging human-readable layout and machine-readable logic.

| Feature | PDF | NDX |
|---------|-----|-----|
| **Print Quality** | ✅ Excellent | ✅ Excellent |
| **Digital Signatures** | ✅ Yes | ✅ Yes (Enhanced) |
| **AI Readable** | ❌ Limited | ✅ Native Support |
| **Semantic Structure** | ⚠️ Tagged PDF only | ✅ Built-in JSON-LD |
| **Vector Search** | ❌ No | ✅ Embedded Index |
| **Streaming** | ❌ Full load required | ✅ Chunk-based |
| **Knowledge Graphs** | ❌ No | ✅ Native RDF |
| **Real-time Collaboration** | ❌ No | 🔄 Coming Soon |

Where PDF froze documents in time, NDX lets them **evolve**, interact, and connect.

---

## 🛠️ Getting Started

### Prerequisites

- Rust 1.75+ (for core development)
- Node.js 18+ (for web tools)
- Python 3.10+ (for SDK/tools)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/ndx-org/ndx.git
   cd ndx
   ```

2. **Build the Rust core**
   ```bash
   cd core
   cargo build --release
   ```

3. **Install dependencies**
   ```bash
   npm install
   ```

4. **Run the demo viewer**
   ```bash
   npm run dev
   ```

5. **Convert your first PDF to NDX**
   ```bash
   ./target/release/ndx convert input.pdf output.ndx
   ```

### Quick Example

```rust
use ndx::Document;

fn main() {
    // Create a new NDX document
    let mut doc = Document::new("My First NDX Document");
    
    // Add a page with content
    doc.add_page()
        .add_text("Hello, NDX!", 50, 770)
        .add_semantic_tag("heading", "Introduction");
    
    // Export to NDX format
    doc.save("output.ndx")?;
    
    // Export to PDF 2.0
    doc.export_pdf("output.pdf")?;
}
```

---

## 📚 Documentation

- **[NDX 2.0 Schema Specification](./docs/ndx-2.0-schema.md)** – Complete technical specification
- **[NDX → PDF 2.0 Conversion Guide](./docs/ndx-to-pdf2.0-conversion-guide.md)** – Export guidelines
- **[PDF 2.0 → NDX Import Guide](./docs/pdf2.0-to-ndx-import-guide.md)** – Import guidelines
- **[API Reference](https://docs.ndx.dev)** – SDK documentation
- **[Examples](./examples/)** – Code samples and use cases

---

## 🤝 Contributing

Contributions are welcome! We're building an open document standard for everyone — developers, designers, AI researchers, and dreamers alike.

### How to Contribute

1. **Fork the repository**
2. **Create your feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Commit your changes**
   ```bash
   git commit -m 'Add some amazing feature'
   ```
4. **Push to the branch**
   ```bash
   git push origin feature/amazing-feature
   ```
5. **Open a Pull Request**

### Development Guidelines

- Follow Rust best practices and `rustfmt` conventions
- Write tests for new features
- Update documentation as needed
- Ensure PDF 2.0 compatibility is maintained
- Run `cargo test` before submitting

See [CONTRIBUTING.md](./CONTRIBUTING.md) for detailed guidelines.

---

## 🧪 Testing

```bash
# Run all tests
cargo test --all

# Run specific test suite
cargo test --package ndx-core

# Run with coverage
cargo tarpaulin --out Html
```

---

## 📐 Compatibility & Standards

NDX is designed to be fully compatible with:

- **ISO 32000-2:2017** (PDF 2.0)
- **JSON-LD 1.1** (Semantic Web)
- **RDF 1.1** (Knowledge Graphs)
- **W3C Web Standards** (HTML5, CSS3)
- **Unicode UTF-8** (International text)

All exported PDFs pass **VeraPDF** validation for PDF 2.0 compliance.

---

## 🎯 Use Cases

### Business & Enterprise
- 📊 **Reports & Analytics** – AI-queryable business reports
- 📑 **Invoices & Receipts** – Machine-readable financial documents
- 📋 **Contracts** – Searchable legal documents with embedded metadata

### Healthcare
- 🏥 **Medical Records** – Structured patient data with privacy controls
- 💊 **Prescriptions** – Machine-readable medication information
- 🧬 **Research Papers** – AI-indexed scientific documents

### Education
- 📚 **Textbooks** – Interactive learning materials
- 📝 **Assignments** – Auto-gradable student submissions
- 🎓 **Certificates** – Verifiable credentials with blockchain integration

### AI & Research
- 🤖 **Training Data** – Structured document datasets for ML
- 🔬 **Knowledge Bases** – Interconnected research documents
- 💡 **RAG Systems** – Native vector search integration

---

## 📜 License

NDX is an open project under the **Apache 2.0 License**.  
See [`LICENSE`](./LICENSE) for more information.

```
Copyright 2025 NDX Project Contributors

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0
```

---

## 🌌 Join the NDX Community

- **🌐 Website:** [ndx.dev](https://ndx.dev) *(coming soon)*
- **💬 Community:** [Telegram @devndx](https://t.me/devndx)
- **💭 Discussions:** [GitHub Discussions](https://github.com/ndx-org/ndx/discussions)
- **🐦 Twitter:** [@ndx_format](https://twitter.com/ndx_format)
- **📧 Email:** hello@ndx.dev

---

## 🙏 Acknowledgments

NDX is built on the shoulders of giants:

- **PDF Standard** – Adobe and ISO for creating the foundation
- **Rust Community** – For building amazing tools and libraries
- **Open Source Contributors** – Everyone who believes in open standards
- **AI Research Community** – For pushing the boundaries of document understanding

---

## 📊 Project Status

| Component | Status | Version |
|-----------|--------|---------|
| Core Engine (Rust) | 🔄 In Development | 0.1.0-alpha |
| NDX Specification | ✅ Draft Complete | 2.0-draft |
| PDF Converter | 🔄 In Progress | 0.1.0-alpha |
| Web Viewer | 📋 Planned | - |
| Desktop App | 📋 Planned | - |
| Cloud Platform | 📋 Planned | - |

---

## 🔮 Future Features

- **Real-time Collaboration** – Google Docs-style editing for NDX
- **Blockchain Integration** – Immutable document verification
- **Multi-modal Support** – Audio, video, and 3D content
- **Smart Templates** – AI-powered document generation
- **Edge Computing** – Render NDX on IoT devices

---

<div align="center">

### 🌟 Star us on GitHub if you believe in the future of intelligent documents!

**NDX: Building the document standard for the intelligent era.**

[⭐ Star](https://github.com/ndx-org/ndx) • [🐛 Report Bug](https://github.com/ndx-org/ndx/issues) • [💡 Request Feature](https://github.com/ndx-org/ndx/issues)

</div>

---

<sub>Made with ❤️ by the NDX community</sub>
