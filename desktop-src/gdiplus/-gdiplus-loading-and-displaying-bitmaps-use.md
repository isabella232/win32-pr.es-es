---
description: Para mostrar una imagen de trama (mapa de bits) en la pantalla, necesita un objeto de imagen y un objeto gráfico.
ms.assetid: 8c1a26d9-b640-4f38-8276-10c4464525f2
title: Cargar y mostrar mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: ab2405462db5017215893d50d93dc0b228633cfb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "104987421"
---
# <a name="loading-and-displaying-bitmaps"></a><span data-ttu-id="cb620-103">Cargar y mostrar mapas de bits</span><span class="sxs-lookup"><span data-stu-id="cb620-103">Loading and displaying bitmaps</span></span>

<span data-ttu-id="cb620-104">Consulte también la [aplicación de ejemplo GDI+ del visor WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).</span><span class="sxs-lookup"><span data-stu-id="cb620-104">Also see the [WIC Viewer GDI+ sample app](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).</span></span>

<span data-ttu-id="cb620-105">Para mostrar una imagen de trama (mapa de bits) en la pantalla, necesita un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y un objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="cb620-105">To display a raster image (bitmap) on the screen, you need an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="cb620-106">Pase el nombre de un archivo (o un puntero a un flujo) a un constructor de **imagen** .</span><span class="sxs-lookup"><span data-stu-id="cb620-106">Pass the name of a file (or a pointer to a stream) to an **Image** constructor.</span></span> <span data-ttu-id="cb620-107">Después de crear un objeto de **imagen** , pase la dirección de ese objeto de **imagen** al método **DrawImage** de un objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="cb620-107">After you have created an **Image** object, pass the address of that **Image** object to the **DrawImage** method of a **Graphics** object.</span></span>

<span data-ttu-id="cb620-108">En el ejemplo siguiente se crea un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir de un archivo JPEG y, a continuación, se dibuja la imagen con la esquina superior izquierda en (60, 10):</span><span class="sxs-lookup"><span data-stu-id="cb620-108">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from a JPEG file and then draws the image with its upper-left corner at (60, 10):</span></span>

```cpp
Image image(L"Grapes.jpg");
graphics.DrawImage(&image, 60, 10);
```

<span data-ttu-id="cb620-109">En la ilustración siguiente se muestra la imagen dibujada en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="cb620-109">The following illustration shows the image drawn at the specified location.</span></span>

![<span data-ttu-id="cb620-110">captura de pantalla de una ventana que contiene una imagen, con una llamada para el punto de origen</span><span class="sxs-lookup"><span data-stu-id="cb620-110">screen shot of a window that contains an image, with a callout for the origin point</span></span> ](images/imageposition1.png)

<span data-ttu-id="cb620-111">La clase [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) proporciona métodos básicos para cargar y mostrar imágenes de trama e imágenes vectoriales.</span><span class="sxs-lookup"><span data-stu-id="cb620-111">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides basic methods for loading and displaying raster images and vector images.</span></span> <span data-ttu-id="cb620-112">La clase [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) , que hereda de la clase **Image** , proporciona métodos más especializados para cargar, mostrar y manipular imágenes de tramas.</span><span class="sxs-lookup"><span data-stu-id="cb620-112">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class, which inherits from the **Image** class, provides more specialized methods for loading, displaying, and manipulating raster images.</span></span> <span data-ttu-id="cb620-113">Por ejemplo, puede crear un objeto de **mapa de bits** a partir de un identificador de icono (HICON).</span><span class="sxs-lookup"><span data-stu-id="cb620-113">For example, you can construct a **Bitmap** object from an icon handle (HICON).</span></span>

<span data-ttu-id="cb620-114">En el ejemplo siguiente se obtiene un identificador de un icono y, a continuación, se usa ese identificador para construir un objeto de [**mapa de bits**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) .</span><span class="sxs-lookup"><span data-stu-id="cb620-114">The following example obtains a handle to an icon and then uses that handle to construct a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="cb620-115">El código muestra el icono pasando la dirección del objeto de **mapa de bits** al método **DrawImage** de un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="cb620-115">The code displays the icon by passing the address of the **Bitmap** object to the **DrawImage** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

```cpp
HICON hIcon = LoadIcon(NULL, IDI_APPLICATION);
Bitmap bitmap(hIcon);
graphics.DrawImage(&bitmap, 10, 10);
```

## <a name="see-also"></a><span data-ttu-id="cb620-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb620-116">See also</span></span>

[<span data-ttu-id="cb620-117">Aplicación de ejemplo GDI+ del visor WIC</span><span class="sxs-lookup"><span data-stu-id="cb620-117">WIC Viewer GDI+ sample app</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)
