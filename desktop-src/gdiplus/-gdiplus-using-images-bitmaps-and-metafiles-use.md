---
description: Windows GDI+ proporciona la clase de imagen para trabajar con imágenes de trama (mapas de bits) e imágenes vectoriales (metaarchivos).
ms.assetid: 57e3bf33-5490-4f4a-addf-356ef8f1aeed
title: Usar imágenes, mapas de bits y metaarchivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 445b37caa488fa4b83bcfb7792eb83f6ee1e6e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082490"
---
# <a name="using-images-bitmaps-and-metafiles"></a><span data-ttu-id="68bc6-103">Usar imágenes, mapas de bits y metaarchivos</span><span class="sxs-lookup"><span data-stu-id="68bc6-103">Using Images, Bitmaps, and Metafiles</span></span>

<span data-ttu-id="68bc6-104">Windows GDI+ proporciona la clase de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) para trabajar con imágenes de trama (mapas de bits) e imágenes vectoriales (metaarchivos).</span><span class="sxs-lookup"><span data-stu-id="68bc6-104">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class for working with raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="68bc6-105">La clase [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) y la clase [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) heredan de la clase **Image** .</span><span class="sxs-lookup"><span data-stu-id="68bc6-105">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class and the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class both inherit from the **Image** class.</span></span> <span data-ttu-id="68bc6-106">La clase **Bitmap** amplía las capacidades de la clase **Image** proporcionando métodos adicionales para cargar, guardar y manipular imágenes de tramas.</span><span class="sxs-lookup"><span data-stu-id="68bc6-106">The **Bitmap** class expands on the capabilities of the **Image** class by providing additional methods for loading, saving, and manipulating raster images.</span></span> <span data-ttu-id="68bc6-107">La clase **Metafile** amplía las capacidades de la clase **Image** proporcionando métodos adicionales para grabar y examinar imágenes vectoriales.</span><span class="sxs-lookup"><span data-stu-id="68bc6-107">The **Metafile** class expands on the capabilities of the **Image** class by providing additional methods for recording and examining vector images.</span></span>

<span data-ttu-id="68bc6-108">En los temas siguientes se describen con más detalle las clases [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)y [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) :</span><span class="sxs-lookup"><span data-stu-id="68bc6-108">The following topics cover the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap), and [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) classes in more detail:</span></span>

-   [<span data-ttu-id="68bc6-109">Cargar y mostrar mapas de bits</span><span class="sxs-lookup"><span data-stu-id="68bc6-109">Loading and Displaying Bitmaps</span></span>](-gdiplus-loading-and-displaying-bitmaps-use.md)
-   [<span data-ttu-id="68bc6-110">Cargar y mostrar metaarchivos</span><span class="sxs-lookup"><span data-stu-id="68bc6-110">Loading and Displaying Metafiles</span></span>](-gdiplus-loading-and-displaying-metafiles-use.md)
-   [<span data-ttu-id="68bc6-111">Grabar metaarchivos</span><span class="sxs-lookup"><span data-stu-id="68bc6-111">Recording Metafiles</span></span>](-gdiplus-recording-metafiles-use.md)
-   [<span data-ttu-id="68bc6-112">Recortar y ajustar el tamaño de las imágenes</span><span class="sxs-lookup"><span data-stu-id="68bc6-112">Cropping and Scaling Images</span></span>](-gdiplus-cropping-and-scaling-images-use.md)
-   [<span data-ttu-id="68bc6-113">Girar, reflejar y sesgar imágenes</span><span class="sxs-lookup"><span data-stu-id="68bc6-113">Rotating, Reflecting, and Skewing Images</span></span>](-gdiplus-rotating-reflecting-and-skewing-images-use.md)
-   [<span data-ttu-id="68bc6-114">Usar el modo de interpolación para controlar la calidad de la imagen durante el ajuste de escala</span><span class="sxs-lookup"><span data-stu-id="68bc6-114">Using Interpolation Mode to Control Image Quality During Scaling</span></span>](-gdiplus-using-interpolation-mode-to-control-image-quality-during-scaling-use.md)
-   [<span data-ttu-id="68bc6-115">Crear imágenes en miniatura</span><span class="sxs-lookup"><span data-stu-id="68bc6-115">Creating Thumbnail Images</span></span>](-gdiplus-creating-thumbnail-images-use.md)
-   [<span data-ttu-id="68bc6-116">Uso de un mapa de bits almacenado en caché para mejorar el rendimiento</span><span class="sxs-lookup"><span data-stu-id="68bc6-116">Using a Cached Bitmap to Improve Performance</span></span>](-gdiplus-using-a-cached-bitmap-to-improve-performance-use.md)
-   [<span data-ttu-id="68bc6-117">Mejorar el rendimiento evitando el escalado automático</span><span class="sxs-lookup"><span data-stu-id="68bc6-117">Improving Performance by Avoiding Automatic Scaling</span></span>](-gdiplus-improving-performance-by-avoiding-automatic-scaling-use.md)
-   [<span data-ttu-id="68bc6-118">Leer y escribir metadatos</span><span class="sxs-lookup"><span data-stu-id="68bc6-118">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)

 

 



