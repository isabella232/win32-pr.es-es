---
title: Copia de fotogramas individuales de una imagen de varios fotogramas
description: En el ejemplo siguiente se recuperan los fotogramas individuales de un archivo TIFF de varios fotogramas.
ms.assetid: dfed0b61-2230-4911-a642-0a6e4beb08d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8398df806ad56b65114b0cc9a986ea53061183fa4658872b65b7d08ef7e38a9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115105"
---
# <a name="copy-individual-frames-from-a-multiple-frame-image"></a>Copia de fotogramas individuales de una imagen de varios fotogramas

En el ejemplo siguiente se recuperan los fotogramas individuales de un archivo TIFF de varios fotogramas. Cuando se creó el archivo TIFF, los fotogramas individuales se agregaron a la dimensión Page (vea [Creating and Saving a Multiple-Frame Image ).](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md) El código muestra cada una de las cuatro páginas y guarda cada página en un archivo de disco PNG independiente.

El código construye un objeto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo TIFF de varios fotogramas. Para recuperar los fotogramas individuales (páginas), el código llama al método [**Image::SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) de ese **objeto Image.** El primer argumento pasado al método **Image::SelectActiveFrame** es la dirección de un GUID que especifica la dimensión en la que los fotogramas se agregaron previamente al archivo TIFF de varios fotogramas. El GUID FrameDimensionPage se define en Gdiplusimaging.h. Otros GUID definidos en ese archivo de encabezado son FrameDimensionTime y FrameDimensionResolution. El segundo argumento pasado al **método Image::SelectActiveFrame** es el índice de base cero de la página deseada.

El código se basa en la función auxiliar GetEncoderClsid, que se muestra en [Recuperación](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)del identificador de clase para un codificador .


```
GUID   pageGuid = FrameDimensionPage;
CLSID  encoderClsid;
Image  multi(L"Multiframe.tif");

// Get the CLSID of the PNG encoder.
GetEncoderClsid(L"image/png", &encoderClsid);

// Display and save the first page (index 0).
multi.SelectActiveFrame(&pageGuid, 0);
graphics.DrawImage(&multi, 10, 10);
multi.Save(L"Page0.png", &encoderClsid, NULL);

// Display and save the second page.
multi.SelectActiveFrame(&pageGuid, 1);
graphics.DrawImage(&multi, 200, 10);
multi.Save(L"Page1.png", &encoderClsid, NULL);

// Display and save the third page.
multi.SelectActiveFrame(&pageGuid, 2);
graphics.DrawImage(&multi, 10, 150);
multi.Save(L"Page2.png", &encoderClsid, NULL);

// Display and save the fourth page.
multi.SelectActiveFrame(&pageGuid, 3);
graphics.DrawImage(&multi, 200, 150);
multi.Save(L"Page3.png", &encoderClsid, NULL);
```



En la ilustración siguiente se muestran las páginas individuales tal como se muestra en el código anterior.

![ilustración que muestra una forma geométrica, una foto de color, una foto monocromática y una forma geométrica diferente](images/multiframe1.png)

 

 



