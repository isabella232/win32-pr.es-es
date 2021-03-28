---
description: La clase Image proporciona métodos básicos para cargar y mostrar imágenes de trama e imágenes vectoriales. La clase Metafile, que hereda de la clase Image, proporciona métodos más especializados para grabar, mostrar y examinar imágenes vectoriales.
ms.assetid: 79b8df1b-6fc5-455b-9d08-57d64bf6bffa
title: Cargar y mostrar metaarchivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5dafe6ef92e80e8487b43a22f50b44c5decd360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082104"
---
# <a name="loading-and-displaying-metafiles"></a><span data-ttu-id="3bbf6-104">Cargar y mostrar metaarchivos</span><span class="sxs-lookup"><span data-stu-id="3bbf6-104">Loading and Displaying Metafiles</span></span>

<span data-ttu-id="3bbf6-105">La clase [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) proporciona métodos básicos para cargar y mostrar imágenes de trama e imágenes vectoriales.</span><span class="sxs-lookup"><span data-stu-id="3bbf6-105">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides basic methods for loading and displaying raster images and vector images.</span></span> <span data-ttu-id="3bbf6-106">La clase [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , que hereda de la clase **Image** , proporciona métodos más especializados para grabar, mostrar y examinar imágenes vectoriales.</span><span class="sxs-lookup"><span data-stu-id="3bbf6-106">The [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class, which inherits from the **Image** class, provides more specialized methods for recording, displaying, and examining vector images.</span></span>

<span data-ttu-id="3bbf6-107">Para mostrar una imagen vectorial (metarchivo) en la pantalla, necesita un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y un objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="3bbf6-107">To display a vector image (metafile) on the screen, you need an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="3bbf6-108">Pase el nombre de un archivo (o un puntero a un flujo) a un constructor de **imagen** .</span><span class="sxs-lookup"><span data-stu-id="3bbf6-108">Pass the name of a file (or a pointer to a stream) to an **Image** constructor.</span></span> <span data-ttu-id="3bbf6-109">Después de crear un objeto de **imagen** , pase la dirección de ese objeto de **imagen** al método **DrawImage** de un objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="3bbf6-109">After you have created an **Image** object, pass the address of that **Image** object to the **DrawImage** method of a **Graphics** object.</span></span>

<span data-ttu-id="3bbf6-110">En el ejemplo siguiente se crea un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir de un archivo EMF (metarchivo mejorado) y, a continuación, se dibuja la imagen con la esquina superior izquierda en (60, 10):</span><span class="sxs-lookup"><span data-stu-id="3bbf6-110">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from an EMF (enhanced metafile) file and then draws the image with its upper-left corner at (60, 10):</span></span>


```
Image image(L"SampleMetafile.emf");
graphics.DrawImage(&image, 60, 10);
```



<span data-ttu-id="3bbf6-111">En la ilustración siguiente se muestra la imagen dibujada en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="3bbf6-111">The following illustration shows the image drawn at the specified location.</span></span>

![captura de pantalla de una ventana que contiene una imagen y especifica el punto de origen](images/imageposition2.png)

 

 



