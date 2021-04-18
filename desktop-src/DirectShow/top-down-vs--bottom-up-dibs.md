---
description: Top-Down frente a
ms.assetid: c292f145-f385-4f18-8f98-e414d86860e2
title: Top-Down frente a Bottom-Up DIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e719bea5923aeccc4a0a92b5f73a253e13d2e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667646"
---
# <a name="top-down-vs-bottom-up-dibs"></a><span data-ttu-id="27137-103">Top-Down frente a Bottom-Up DIB</span><span class="sxs-lookup"><span data-stu-id="27137-103">Top-Down vs. Bottom-Up DIBs</span></span>

<span data-ttu-id="27137-104">Si no está familiarizado con la programación de gráficos, puede esperar que un mapa de bits se organice en memoria para que la fila superior de la imagen aparezca al principio del búfer, seguida de la siguiente fila, etc.</span><span class="sxs-lookup"><span data-stu-id="27137-104">If you are new to graphics programming, you might expect that a bitmap would be arranged in memory so that the top row of the image appeared at the start of the buffer, followed by the next row, and so forth.</span></span> <span data-ttu-id="27137-105">Sin embargo, esto no es necesariamente así.</span><span class="sxs-lookup"><span data-stu-id="27137-105">However, this is not necessarily the case.</span></span> <span data-ttu-id="27137-106">En Windows, los mapas de bits independientes del dispositivo (DIB) se pueden colocar en memoria en dos orientaciones diferentes, de arriba abajo y de arriba abajo.</span><span class="sxs-lookup"><span data-stu-id="27137-106">In Windows, device-independent bitmaps (DIBs) can be placed in memory in two different orientations, bottom-up and top-down.</span></span>

<span data-ttu-id="27137-107">En un DIB de abajo arriba, el búfer de la imagen comienza con la fila inferior de píxeles, seguida de la siguiente fila, etc.</span><span class="sxs-lookup"><span data-stu-id="27137-107">In a bottom-up DIB, the image buffer starts with the bottom row of pixels, followed by the next row up, and so forth.</span></span> <span data-ttu-id="27137-108">La fila superior de la imagen es la última fila del búfer.</span><span class="sxs-lookup"><span data-stu-id="27137-108">The top row of the image is the last row in the buffer.</span></span> <span data-ttu-id="27137-109">Por lo tanto, el primer byte de la memoria es el píxel inferior izquierdo de la imagen.</span><span class="sxs-lookup"><span data-stu-id="27137-109">Therefore, the first byte in memory is the bottom-left pixel of the image.</span></span> <span data-ttu-id="27137-110">En GDI, todos los DIB están en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="27137-110">In GDI, all DIBs are bottom-up.</span></span> <span data-ttu-id="27137-111">En el diagrama siguiente se muestra el diseño físico de un DIB de arriba abajo.</span><span class="sxs-lookup"><span data-stu-id="27137-111">The following diagram shows the physical layout of a bottom-up DIB.</span></span>

![DIB de abajo arriba](images/pixel-layout-bottomup.png)

<span data-ttu-id="27137-113">En un DIB de arriba abajo, se invierte el orden de las filas.</span><span class="sxs-lookup"><span data-stu-id="27137-113">In a top-down DIB, the order of the rows is reversed.</span></span> <span data-ttu-id="27137-114">La fila superior de la imagen es la primera fila de la memoria, seguida de la fila siguiente.</span><span class="sxs-lookup"><span data-stu-id="27137-114">The top row of the image is the first row in memory, followed by the next row down.</span></span> <span data-ttu-id="27137-115">La fila inferior de la imagen es la última fila del búfer.</span><span class="sxs-lookup"><span data-stu-id="27137-115">The bottom row of the image is the last row in the buffer.</span></span> <span data-ttu-id="27137-116">Con un DIB de arriba abajo, el primer byte de la memoria es el píxel superior izquierdo de la imagen.</span><span class="sxs-lookup"><span data-stu-id="27137-116">With a top-down DIB, the first byte in memory is the top-left pixel of the image.</span></span> <span data-ttu-id="27137-117">DirectDraw usa DIB de arriba abajo.</span><span class="sxs-lookup"><span data-stu-id="27137-117">DirectDraw uses top-down DIBs.</span></span> <span data-ttu-id="27137-118">En el diagrama siguiente se muestra el diseño físico de un DIB de arriba abajo:</span><span class="sxs-lookup"><span data-stu-id="27137-118">The following diagram shows the physical layout of a top-down DIB:</span></span>

![DIB de arriba abajo](images/pixel-layout-topdown.png)

<span data-ttu-id="27137-120">En el caso de los DIB RGB, la orientación de la imagen se indica mediante el miembro **biheight** de la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="27137-120">For RGB DIBs, the image orientation is indicated by the **biHeight** member of the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="27137-121">Si **biheight** es positivo, la imagen estará en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="27137-121">If **biHeight** is positive, the image is bottom-up.</span></span> <span data-ttu-id="27137-122">Si el valor de **biheight** es negativo, la imagen es de arriba abajo.</span><span class="sxs-lookup"><span data-stu-id="27137-122">If **biHeight** is negative, the image is top-down.</span></span>

<span data-ttu-id="27137-123">Los DIB en formatos YUV siempre son de arriba abajo y se omite el signo del miembro de **bialtura** .</span><span class="sxs-lookup"><span data-stu-id="27137-123">DIBs in YUV formats are always top-down, and the sign of the **biHeight** member is ignored.</span></span> <span data-ttu-id="27137-124">Los descodificadores deben ofrecer formatos YUV con un **bialto** positivo, pero también deben aceptar formatos YUV con una **bialtura** negativa y omitir el signo.</span><span class="sxs-lookup"><span data-stu-id="27137-124">Decoders should offer YUV formats with positive **biHeight**, but they should also accept YUV formats with negative **biHeight** and ignore the sign.</span></span>

<span data-ttu-id="27137-125">Además, cualquier tipo DIB que use un **FourCC** en el miembro de **bicompression** debe expresar su **biheight** como un número positivo, independientemente de cuál sea su orientación, ya que el propio elemento **FourCC** identifica un esquema de compresión cuya orientación de imagen debe entenderse con cualquier filtro compatible.</span><span class="sxs-lookup"><span data-stu-id="27137-125">Also, any DIB type that uses a **FOURCC** in the **biCompression** member, should express its **biHeight** as a positive number no matter what its orientation is, since the **FOURCC** itself identifies a compression scheme whose image orientation should be understood by any compatible filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27137-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="27137-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27137-127">Trabajar con fotogramas de vídeo</span><span class="sxs-lookup"><span data-stu-id="27137-127">Working with Video Frames</span></span>](working-with-video-frames.md)
</dt> </dl>

 

 



