# InvoiceOCR
The objective for this project was to extract structured text from a PDF file.
To do so, I have first applied proprecessing on the different pages (image conversion, grayscale conversion, noise reduction and binarization).
I have then used the canny edge function, the dilate function and most importantly the findContours function to detect the contours of paragraphs in each page. I have then cropped each zone of text and OCR each zone of the text using pytesseract.

## Classes
The class **Preprocessing_PDF** contains the methods *preprocessing* and *save_preprocessing_images*.
The class **Zonification** contains the methods *zone_identification*, *block_image_text_comparison* and *save_extracted_text*

## Method call

```
preprocessed_pdf_file = Preprocessing_PDF(file_path,file_name)
preprocessed_pdf_file.preprocessing()
preprocessed_pdf_file.save_preprocessing_images()

zonified = Zonification(file_path,file_name)
zonified.zone_identification()
zonified.block_image_text_comparison()
zonified.save_extracted_text()
```
