---
description: Obtenga información sobre el uso de imágenes, mapas de bits y metarchivos. Windows GDI+ proporciona la clase Image para trabajar con imágenes de trama (mapas de bits) e imágenes vectoriales (metarchivos).
ms.assetid: 57e3bf33-5490-4f4a-addf-356ef8f1aeed
title: Uso de imágenes, mapas de bits y metarchivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d0603c8a428c45feac8cdeb47a46b61dc5e3bd
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395540"
---
# <a name="using-images-bitmaps-and-metafiles"></a><span data-ttu-id="4a330-104">Uso de imágenes, mapas de bits y metarchivos</span><span class="sxs-lookup"><span data-stu-id="4a330-104">Using Images, Bitmaps, and Metafiles</span></span>

<span data-ttu-id="4a330-105">Windows GDI+ proporciona la [**clase Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) para trabajar con imágenes de trama (mapas de bits) e imágenes vectoriales (metarchivos).</span><span class="sxs-lookup"><span data-stu-id="4a330-105">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class for working with raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="4a330-106">La [**clase Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) y la clase [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) heredan de la clase **Image.**</span><span class="sxs-lookup"><span data-stu-id="4a330-106">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class and the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class both inherit from the **Image** class.</span></span> <span data-ttu-id="4a330-107">La **clase Bitmap** amplía las funcionalidades de la clase **Image** al proporcionar métodos adicionales para cargar, guardar y manipular imágenes de trama.</span><span class="sxs-lookup"><span data-stu-id="4a330-107">The **Bitmap** class expands on the capabilities of the **Image** class by providing additional methods for loading, saving, and manipulating raster images.</span></span> <span data-ttu-id="4a330-108">La **clase Metafile** amplía las funcionalidades de la **clase Image** proporcionando métodos adicionales para registrar y examinar imágenes vectoriales.</span><span class="sxs-lookup"><span data-stu-id="4a330-108">The **Metafile** class expands on the capabilities of the **Image** class by providing additional methods for recording and examining vector images.</span></span>

<span data-ttu-id="4a330-109">En los temas siguientes se tratan [**las clases Image,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)y [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) con más detalle:</span><span class="sxs-lookup"><span data-stu-id="4a330-109">The following topics cover the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap), and [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) classes in more detail:</span></span>

-   [<span data-ttu-id="4a330-110">Cargar y mostrar mapas de bits</span><span class="sxs-lookup"><span data-stu-id="4a330-110">Loading and Displaying Bitmaps</span></span>](-gdiplus-loading-and-displaying-bitmaps-use.md)
-   [<span data-ttu-id="4a330-111">Carga y visualización de metarchivos</span><span class="sxs-lookup"><span data-stu-id="4a330-111">Loading and Displaying Metafiles</span></span>](-gdiplus-loading-and-displaying-metafiles-use.md)
-   [<span data-ttu-id="4a330-112">Grabación de metarchivos</span><span class="sxs-lookup"><span data-stu-id="4a330-112">Recording Metafiles</span></span>](-gdiplus-recording-metafiles-use.md)
-   [<span data-ttu-id="4a330-113">Recortar y escalar imágenes</span><span class="sxs-lookup"><span data-stu-id="4a330-113">Cropping and Scaling Images</span></span>](-gdiplus-cropping-and-scaling-images-use.md)
-   [<span data-ttu-id="4a330-114">Rotación, reflexión y sesgo de imágenes</span><span class="sxs-lookup"><span data-stu-id="4a330-114">Rotating, Reflecting, and Skewing Images</span></span>](-gdiplus-rotating-reflecting-and-skewing-images-use.md)
-   [<span data-ttu-id="4a330-115">Uso del modo de interpolación para controlar la calidad de la imagen durante el escalado</span><span class="sxs-lookup"><span data-stu-id="4a330-115">Using Interpolation Mode to Control Image Quality During Scaling</span></span>](-gdiplus-using-interpolation-mode-to-control-image-quality-during-scaling-use.md)
-   [<span data-ttu-id="4a330-116">Creación de imágenes en miniatura</span><span class="sxs-lookup"><span data-stu-id="4a330-116">Creating Thumbnail Images</span></span>](-gdiplus-creating-thumbnail-images-use.md)
-   [<span data-ttu-id="4a330-117">Usar un mapa de bits almacenado en caché para mejorar el rendimiento</span><span class="sxs-lookup"><span data-stu-id="4a330-117">Using a Cached Bitmap to Improve Performance</span></span>](-gdiplus-using-a-cached-bitmap-to-improve-performance-use.md)
-   [<span data-ttu-id="4a330-118">Mejorar el rendimiento evitando el escalado automático</span><span class="sxs-lookup"><span data-stu-id="4a330-118">Improving Performance by Avoiding Automatic Scaling</span></span>](-gdiplus-improving-performance-by-avoiding-automatic-scaling-use.md)
-   [<span data-ttu-id="4a330-119">Leer y escribir metadatos</span><span class="sxs-lookup"><span data-stu-id="4a330-119">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)

 

 



