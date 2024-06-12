<div align="center">
<h1>Document Parsing</h1>
</div>

Parsing documents (PDFs) with various methods to extract meaningful data for RAG and Question answering use cases. Parsing includes `table extraction`, `context-focused` extraction, `content cleaning` such as removal of disclaimers, appendix, etc. without affecting the raw knowledge base of the documents.

## Tables extraction from documents

Various methods are available for extracting tables from documents. Some of the popular methods including `OCR`, `Vision Language Model` models, `table transformers` by **Microsoft**, etc. Their main aim is to retrieve factual tabular data from the documents. 

Apart from this, there are conventional tools such as **PyMuPDF** that do a fair job of extracting tabular data from documents. 

<div align="center">
<table style="width: 100%; table-layout: fixed;">
  <tr>
       <td style="text-align: center; vertical-align: top;"> <!-- comment -->
      <h3><a href="https://github.com/d1pankarmedhi/image-search-engine">Pdf Document</a></h3>
       <img src="https://github.com/d1pankarmedhi/document_parsing/assets/136924835/63e97776-4246-4d43-85b0-768bf50b4145" alt="pdf-document-img" style="width: 400px; height: 400px;">
      <p></p>
    </td>
    <td style="text-align: center; vertical-align: top;">
      <h3><a href="https://github.com/d1pankarmedhi/ViT-vision-transformer">PyMuPDF</a></h3>
      <img src="https://github.com/d1pankarmedhi/document_parsing/assets/136924835/3b242ccd-8001-4a9a-bf56-086cb7344d93" alt="brand-classification" style="width: 400px; height: 400px;">
      <p></p>
    </td>
  </tr>
  </table>
</div>

Please refer to [table_parsing_with_pymupdf](notebooks/table_parsing_with_pymupdf.ipynb) notebook for detailed walk-through.

## Structuring documents with Polars

Documents are hard to parse because of their unstructured nature. The content is distributed throughout the whole piece without proper directive information. 

Search for relevant information to point to a particular section of a document without any prior knowledge is often difficult. 

A proposed way to deal with this is segmenting the whole document into blocks. Blocks of meaningful data can help one identify regions of importance and thus make the extraction and cleaning process easy and efficient.

**Polars** can be used to differentiate the document context into sections/blocks which later can be used to clean the unwanted pieces without wasting any important information from the knowledge base. 

> You can go with pandas instead of polars.

**Document structure with polars**

<div align="center">
<table style="width: 100%; table-layout: fixed;">
  <tr>
       <td style="text-align: center; vertical-align: top;"> <!-- comment -->
       <img src="https://github.com/d1pankarmedhi/document_parsing/assets/136924835/b201d1e9-0733-4d1b-9feb-a67ab1e00b81" alt="structure" style="width: 250px; height: 100px;">
      <p></p>
    </td>
    <td style="text-align: center; vertical-align: top;">
      <img src="https://github.com/d1pankarmedhi/document_parsing/assets/136924835/afd1b4a6-19f6-4a39-a798-6a48b0542cca" alt="structure" style="width: 400px; height: 200px;">
      <p></p>
    </td>

  </tr>
  </table>
</div>


Please refer to [structuing_doucments_with_polars](notebooks/structuring_pdf_with_polars.ipynb) notebook for more details.

