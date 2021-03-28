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
# <a name="copy-individual-frames-from-a-multiple-frame-image"></a><span data-ttu-id="2bd4a-103">Copiar fotogramas individuales de una imagen de varios marcos</span><span class="sxs-lookup"><span data-stu-id="2bd4a-103">Copy individual frames from a multiple-frame image</span></span>

<span data-ttu-id="2bd4a-104">En el ejemplo siguiente se recuperan los marcos individuales de un archivo TIFF de varios marcos.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-104">The following example retrieves the individual frames from a multiple-frame TIFF file.</span></span> <span data-ttu-id="2bd4a-105">Cuando se creó el archivo TIFF, los fotogramas individuales se agregaron a la dimensión de página (consulte [creación y almacenamiento de una imagen Multiple-Frame](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)).</span><span class="sxs-lookup"><span data-stu-id="2bd4a-105">When the TIFF file was created, the individual frames were added to the Page dimension (see [Creating and Saving a Multiple-Frame Image](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)).</span></span> <span data-ttu-id="2bd4a-106">El código muestra cada una de las cuatro páginas y guarda cada página en un archivo de disco PNG independiente.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-106">The code displays each of the four pages and saves each page to a separate PNG disk file.</span></span>

<span data-ttu-id="2bd4a-107">El código crea un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo TIFF de varios marcos.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-107">The code constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the multiple-frame TIFF file.</span></span> <span data-ttu-id="2bd4a-108">Para recuperar los marcos individuales (páginas), el código llama al método [**Image:: SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) de ese objeto de **imagen** .</span><span class="sxs-lookup"><span data-stu-id="2bd4a-108">To retrieve the individual frames (pages), the code calls the [**Image::SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) method of that **Image** object.</span></span> <span data-ttu-id="2bd4a-109">El primer argumento que se pasa al método **Image:: SelectActiveFrame** es la dirección de un GUID que especifica la dimensión en la que los fotogramas se agregaron previamente al archivo TIFF de varios marcos.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-109">The first argument passed to the **Image::SelectActiveFrame** method is the address of a GUID that specifies the dimension in which the frames were previously added to the multiple-frame TIFF file.</span></span> <span data-ttu-id="2bd4a-110">El GUID FrameDimensionPage se define en Gdiplusimaging. h.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-110">The GUID FrameDimensionPage is defined in Gdiplusimaging.h.</span></span> <span data-ttu-id="2bd4a-111">Otros GUID definidos en ese archivo de encabezado son FrameDimensionTime y FrameDimensionResolution.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-111">Other GUIDs defined in that header file are FrameDimensionTime and FrameDimensionResolution.</span></span> <span data-ttu-id="2bd4a-112">El segundo argumento que se pasa al método **Image:: SelectActiveFrame** es el índice de base cero de la página deseada.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-112">The second argument passed to the **Image::SelectActiveFrame** method is the zero-based index of the desired page.</span></span>

<span data-ttu-id="2bd4a-113">El código se basa en la función auxiliar GetEncoderClsid, que se muestra en [recuperar el identificador de clase de un codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="2bd4a-113">The code relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



<span data-ttu-id="2bd4a-114">En la ilustración siguiente se muestran las páginas individuales tal como se muestra en el código anterior.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-114">The following illustration shows the individual pages as displayed by the preceding code.</span></span>

![Ilustración en la que se muestra una forma geométrica, una fotografía en color, una fotografía monocroma y una forma geométrica diferente](images/multiframe1.png)

 

 



