# tFPDF
My modified version of tFPDF with support for cropped imaged.

Original by Ian Back : http://www.fpdf.org/en/script/script92.php

## How to use

    <?php
    
    $pdf = new tFPDF();
    $pdf->AddPage();
    
    // Add a Unicode font (uses UTF-8)
    $pdf->AddFont('DejaVu','','DejaVuSansCondensed.ttf',true);
    $pdf->SetFont('DejaVu','',14);
    
    // Add some text
    $pdf->SetTextColor(0, 0, 0);
    $pdf->SetFont('Arial','',14);
    $pdf->Text('Nullam dictum felis eu pede');
    
    //Move down
    $pdf->SetY(20);
    
    // Added cropped image 
    $pdf->ImageCropped('/images/sample.png', 50, 50, 200, 100);
        
    $pdf->Output();
    
    ?>
