---
description: Windows admite formatos para comprimir mapas de bits que definen sus colores con 8 o 4 bits por píxel. La compresión reduce el almacenamiento en disco y memoria necesario para el mapa de bits.
ms.assetid: 14d14662-910a-4f3f-914e-6ccfc602c822
title: Compresión de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38739f0e33f095b8eff567fc63b57db96b8cdc66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155700"
---
# <a name="bitmap-compression"></a><span data-ttu-id="6d875-104">Compresión de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="6d875-104">Bitmap Compression</span></span>

<span data-ttu-id="6d875-105">Windows admite formatos para comprimir mapas de bits que definen sus colores con 8 o 4 bits por píxel.</span><span class="sxs-lookup"><span data-stu-id="6d875-105">Windows supports formats for compressing bitmaps that define their colors with 8 or 4 bits-per-pixel.</span></span> <span data-ttu-id="6d875-106">La compresión reduce el almacenamiento en disco y memoria necesario para el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="6d875-106">Compression reduces the disk and memory storage required for the bitmap.</span></span>

<span data-ttu-id="6d875-107">Cuando el miembro de **compresión** de la estructura de encabezado de información de mapa de bits es bi \_ RLE8, se usa un formato de codificación de longitud de ejecución (RLE) para comprimir un mapa de bits de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="6d875-107">When the **Compression** member of the bitmap information header structure is BI\_RLE8, a run-length encoding (RLE) format is used to compress an 8-bit bitmap.</span></span> <span data-ttu-id="6d875-108">Este formato se puede comprimir en los modos codificado o absoluto.</span><span class="sxs-lookup"><span data-stu-id="6d875-108">This format can be compressed in encoded or absolute modes.</span></span> <span data-ttu-id="6d875-109">Ambos modos pueden aparecer en cualquier lugar del mismo mapa de bits:</span><span class="sxs-lookup"><span data-stu-id="6d875-109">Both modes can occur anywhere in the same bitmap:</span></span>

-   <span data-ttu-id="6d875-110">El *modo codificado* consta de dos bytes: el primer byte especifica el número de píxeles consecutivos que se van a dibujar utilizando el índice de color contenido en el segundo byte.</span><span class="sxs-lookup"><span data-stu-id="6d875-110">*Encoded mode* consists of two bytes: the first byte specifies the number of consecutive pixels to be drawn using the color index contained in the second byte.</span></span> <span data-ttu-id="6d875-111">Además, el primer byte del par se puede establecer en cero para indicar un carácter de escape que denota el final de una línea, el final de un mapa de bits o un delta, dependiendo del valor del segundo byte.</span><span class="sxs-lookup"><span data-stu-id="6d875-111">In addition, the first byte of the pair can be set to zero to indicate an escape character that denotes the end of a line, the end of a bitmap, or a delta, depending on the value of the second byte.</span></span> <span data-ttu-id="6d875-112">La interpretación del escape depende del valor del segundo byte del par, que puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="6d875-112">The interpretation of the escape depends on the value of the second byte of the pair, which can be one of the following values.</span></span>



| <span data-ttu-id="6d875-113">Value</span><span class="sxs-lookup"><span data-stu-id="6d875-113">Value</span></span> | <span data-ttu-id="6d875-114">Significado</span><span class="sxs-lookup"><span data-stu-id="6d875-114">Meaning</span></span>                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d875-115">0</span><span class="sxs-lookup"><span data-stu-id="6d875-115">0</span></span>     | <span data-ttu-id="6d875-116">Fin de línea.</span><span class="sxs-lookup"><span data-stu-id="6d875-116">End of line.</span></span>                                                                                                                                                |
| <span data-ttu-id="6d875-117">1</span><span class="sxs-lookup"><span data-stu-id="6d875-117">1</span></span>     | <span data-ttu-id="6d875-118">Fin del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="6d875-118">End of bitmap.</span></span>                                                                                                                                              |
| <span data-ttu-id="6d875-119">2</span><span class="sxs-lookup"><span data-stu-id="6d875-119">2</span></span>     | <span data-ttu-id="6d875-120">Paragua.</span><span class="sxs-lookup"><span data-stu-id="6d875-120">Delta.</span></span> <span data-ttu-id="6d875-121">Los 2 bytes que siguen al escape contienen valores sin signo que indican los desplazamientos horizontal y vertical del siguiente píxel desde la posición actual.</span><span class="sxs-lookup"><span data-stu-id="6d875-121">The 2 bytes following the escape contain unsigned values indicating the horizontal and vertical offsets of the next pixel from the current position.</span></span> |



 

-   <span data-ttu-id="6d875-122">En el *modo absoluto*, el primer byte es cero y el segundo byte es un valor en el intervalo 03h a través de FFH.</span><span class="sxs-lookup"><span data-stu-id="6d875-122">In *absolute mode*, the first byte is zero and the second byte is a value in the range 03H through FFH.</span></span> <span data-ttu-id="6d875-123">El segundo byte representa el número de bytes siguientes, cada uno de los cuales contiene el índice de color de un solo píxel.</span><span class="sxs-lookup"><span data-stu-id="6d875-123">The second byte represents the number of bytes that follow, each of which contains the color index of a single pixel.</span></span> <span data-ttu-id="6d875-124">Cuando el segundo byte es dos o menos, el escape tiene el mismo significado que el modo codificado.</span><span class="sxs-lookup"><span data-stu-id="6d875-124">When the second byte is two or less, the escape has the same meaning as encoded mode.</span></span> <span data-ttu-id="6d875-125">En el modo absoluto, cada ejecución debe estar alineada en un límite de palabras.</span><span class="sxs-lookup"><span data-stu-id="6d875-125">In absolute mode, each run must be aligned on a word boundary.</span></span>

<span data-ttu-id="6d875-126">En el ejemplo siguiente se muestran los valores hexadecimales de un mapa de bits comprimido de 8 bits:</span><span class="sxs-lookup"><span data-stu-id="6d875-126">The following example shows the hexadecimal values of an 8-bit compressed bitmap:</span></span>


```C++
[03 04] [05 06] [00 03 45 56 67] [02 78] [00 02 05 01] 
[02 78] [00 00] [09 1E] [00 01] 
```



<span data-ttu-id="6d875-127">El mapa de bits se expande de la manera siguiente (los valores de dos dígitos representan un índice de color para un solo píxel):</span><span class="sxs-lookup"><span data-stu-id="6d875-127">The bitmap expands as follows (two-digit values represent a color index for a single pixel):</span></span>


```C++
04 04 04 
06 06 06 06 06 
45 56 67 
78 78 
move current position 5 right and 1 down 
78 78 
end of line 
1E 1E 1E 1E 1E 1E 1E 1E 1E 
end of RLE bitmap 
```



<span data-ttu-id="6d875-128">Cuando el miembro de **compresión** es bi \_ RLE4, el mapa de bits se comprime con un formato de codificación de longitud de ejecución para un mapa de bits de 4 bits, que también usa los modos codificado y absoluto:</span><span class="sxs-lookup"><span data-stu-id="6d875-128">When the **Compression** member is BI\_RLE4, the bitmap is compressed by using a run-length encoding format for a 4-bit bitmap, which also uses encoded and absolute modes:</span></span>

-   <span data-ttu-id="6d875-129">En el modo codificado, el primer byte del par contiene el número de píxeles que se van a dibujar utilizando los índices de color del segundo byte.</span><span class="sxs-lookup"><span data-stu-id="6d875-129">In encoded mode, the first byte of the pair contains the number of pixels to be drawn using the color indexes in the second byte.</span></span> <span data-ttu-id="6d875-130">El segundo byte contiene dos índices de color, uno en sus 4 bits de orden superior y otro en sus 4 bits de orden inferior.</span><span class="sxs-lookup"><span data-stu-id="6d875-130">The second byte contains two color indexes, one in its high-order 4 bits and one in its low-order 4 bits.</span></span> <span data-ttu-id="6d875-131">El primero de los píxeles se dibuja utilizando el color especificado por los 4 bits de orden superior, el segundo se dibuja con el color de los 4 bits de orden inferior, el tercero se dibuja usando el color de los 4 bits de orden superior, y así sucesivamente, hasta que se dibujen todos los píxeles especificados por el primer byte.</span><span class="sxs-lookup"><span data-stu-id="6d875-131">The first of the pixels is drawn using the color specified by the high-order 4 bits, the second is drawn using the color in the low-order 4 bits, the third is drawn using the color in the high-order 4 bits, and so on, until all the pixels specified by the first byte have been drawn.</span></span>
-   <span data-ttu-id="6d875-132">En el modo absoluto, el primer byte es cero.</span><span class="sxs-lookup"><span data-stu-id="6d875-132">In absolute mode, the first byte is zero.</span></span> <span data-ttu-id="6d875-133">El segundo byte contiene el número de índices de color que siguen.</span><span class="sxs-lookup"><span data-stu-id="6d875-133">The second byte contains the number of color indexes that follow.</span></span> <span data-ttu-id="6d875-134">Los bytes siguientes contienen índices de color en sus 4 bits de orden superior y mínimo, un índice de color para cada píxel.</span><span class="sxs-lookup"><span data-stu-id="6d875-134">Subsequent bytes contain color indexes in their high- and low-order 4 bits, one color index for each pixel.</span></span> <span data-ttu-id="6d875-135">En el modo absoluto, cada ejecución debe estar alineada en un límite de palabras.</span><span class="sxs-lookup"><span data-stu-id="6d875-135">In absolute mode, each run must be aligned on a word boundary.</span></span> <span data-ttu-id="6d875-136">Los escapes de fin de línea, final de mapa de bits y Delta descritos para RLE8 de BI \_ también se aplican a la \_ compresión RLE4 de BI.</span><span class="sxs-lookup"><span data-stu-id="6d875-136">The end-of-line, end-of-bitmap, and delta escapes described for BI\_RLE8 also apply to BI\_RLE4 compression.</span></span>

<span data-ttu-id="6d875-137">En el ejemplo siguiente se muestran los valores hexadecimales de un mapa de bits comprimido de 4 bits:</span><span class="sxs-lookup"><span data-stu-id="6d875-137">The following example shows the hexadecimal values of a 4-bit compressed bitmap:</span></span>


```C++
03 04 05 06 00 06 45 56 67 00 04 78 00 02 05 01 
04 78 00 00 09 1E 00 01 
```



<span data-ttu-id="6d875-138">El mapa de bits se expande de la manera siguiente (los valores de un solo dígito representan un índice de color para un solo píxel):</span><span class="sxs-lookup"><span data-stu-id="6d875-138">The bitmap expands as follows (single-digit values represent a color index for a single pixel):</span></span>


```C++
0 4 0 
0 6 0 6 0 
4 5 5 6 6 7 
7 8 7 8 
move current position 5 right and 1 down 
7 8 7 8 
end of line 
1 E 1 E 1 E 1 E 1 
end of RLE bitmap 
```



 

 



