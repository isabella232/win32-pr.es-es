---
title: Copiar fotogramas individuales de una imagen de varios marcos
description: En el ejemplo siguiente se recuperan los marcos individuales de un archivo TIFF de varios marcos.
ms.assetid: dfed0b61-2230-4911-a642-0a6e4beb08d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d6bdb5668bcebb9babcbcb7d07839694750aec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276398"
---
# <a name="copy-individual-frames-from-a-multiple-frame-image"></a>Copiar fotogramas individuales de una imagen de varios marcos

En el ejemplo siguiente se recuperan los marcos individuales de un archivo TIFF de varios marcos. Cuando se creó el archivo TIFF, los fotogramas individuales se agregaron a la dimensión de página (consulte [creación y almacenamiento de una imagen Multiple-Frame](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)). El código muestra cada una de las cuatro páginas y guarda cada página en un archivo de disco PNG independiente.

El código crea un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo TIFF de varios marcos. Para recuperar los marcos individuales (páginas), el código llama al método [**Image:: SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) de ese objeto de **imagen** . El primer argumento que se pasa al método **Image:: SelectActiveFrame** es la dirección de un GUID que especifica la dimensión en la que los fotogramas se agregaron previamente al archivo TIFF de varios marcos. El GUID FrameDimensionPage se define en Gdiplusimaging. h. Otros GUID definidos en ese archivo de encabezado son FrameDimensionTime y FrameDimensionResolution. El segundo argumento que se pasa al método **Image:: SelectActiveFrame** es el índice de base cero de la página deseada.

El código se basa en la función auxiliar GetEncoderClsid, que se muestra en [recuperar el identificador de clase de un codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


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

![Ilustración en la que se muestra una forma geométrica, una fotografía en color, una fotografía monocroma y una forma geométrica diferente](images/multiframe1.png)

 

 



