---
description: Trabajar con RGB de 16 bits
ms.assetid: 0a245187-4120-4003-9a8f-6b1e8fa40d38
title: Trabajar con RGB de 16 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6bf4b3217af4d0261d4ab26ca011881762a2a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687721"
---
# <a name="working-with-16-bit-rgb"></a><span data-ttu-id="99caf-103">Trabajar con RGB de 16 bits</span><span class="sxs-lookup"><span data-stu-id="99caf-103">Working with 16-bit RGB</span></span>

<span data-ttu-id="99caf-104">Se definen dos formatos para RGB sin comprimir de 16 bits:</span><span class="sxs-lookup"><span data-stu-id="99caf-104">Two formats are defined for 16-bit uncompressed RGB:</span></span>

-   <span data-ttu-id="99caf-105">MEDIASUBTYPE \_ 555 usa cinco bits cada uno para los componentes rojo, verde y azul de un píxel.</span><span class="sxs-lookup"><span data-stu-id="99caf-105">MEDIASUBTYPE\_555 uses five bits each for the red, green, and blue components in a pixel.</span></span> <span data-ttu-id="99caf-106">Se omite el bit más significativo de la **palabra** .</span><span class="sxs-lookup"><span data-stu-id="99caf-106">The most significant bit in the **WORD** is ignored.</span></span>
-   <span data-ttu-id="99caf-107">MEDIASUBTYPE \_ 565 usa cinco bits para los componentes rojo y azul, y seis bits para el componente verde.</span><span class="sxs-lookup"><span data-stu-id="99caf-107">MEDIASUBTYPE\_565 uses five bits for the red and blue components, and six bits for the green component.</span></span> <span data-ttu-id="99caf-108">Este formato refleja el hecho de que la visión humana es más sensible a las partes verdes del espectro visible.</span><span class="sxs-lookup"><span data-stu-id="99caf-108">This format reflects the fact that human vision is most sensitive to the green portions of the visible spectrum.</span></span>

<span data-ttu-id="99caf-109">**RGB 565**</span><span class="sxs-lookup"><span data-stu-id="99caf-109">**RGB 565**</span></span>

<span data-ttu-id="99caf-110">Para extraer los componentes de color de una imagen de RGB 565, trate cada píxel como un tipo de **palabra** y use las siguientes máscaras de bits:</span><span class="sxs-lookup"><span data-stu-id="99caf-110">To extract the color components from an RGB 565 image, treat each pixel as a **WORD** type and use the following bit masks:</span></span>


```C++
WORD red_mask = 0xF800;
WORD green_mask = 0x7E0;
WORD blue_mask = 0x1F;
```



<span data-ttu-id="99caf-111">Obtenga los componentes de color de un píxel de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="99caf-111">Get the color components from a pixel as follows:</span></span>


```C++
BYTE red_value = (pixel & red_mask) >> 11;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);
```



<span data-ttu-id="99caf-112">Recuerde que los canales rojo y azul son de 5 bits y el canal verde es de 6 bits.</span><span class="sxs-lookup"><span data-stu-id="99caf-112">Remember that the red and blue channels are 5 bits and the green channel is 6 bits.</span></span> <span data-ttu-id="99caf-113">Para convertir estos valores en componentes de 8 bits (para RGB de 24 bits o de 32 bits), debe desplazar a la izquierda el número de bits adecuado:</span><span class="sxs-lookup"><span data-stu-id="99caf-113">To convert these values to 8-bit components (for 24-bit or 32-bit RGB), you must left-shift the appropriate number of bits:</span></span>


```C++
// Expand to 8-bit values.
BYTE red   = red_value << 3;
BYTE green = green_value << 2;
BYTE blue  = blue_value << 3;
```



<span data-ttu-id="99caf-114">Invierta este proceso para crear un píxel RGB 565.</span><span class="sxs-lookup"><span data-stu-id="99caf-114">Reverse this process to create an RGB 565 pixel.</span></span> <span data-ttu-id="99caf-115">Suponiendo que los valores de color se han truncado al número correcto de bits:</span><span class="sxs-lookup"><span data-stu-id="99caf-115">Assuming the color values have been truncated to the correct number of bits:</span></span>


```C++
WORD pixel565 = (red_value << 11) | (green_value << 5) | blue_value;
```



<span data-ttu-id="99caf-116">**RGB 555**</span><span class="sxs-lookup"><span data-stu-id="99caf-116">**RGB 555**</span></span>

<span data-ttu-id="99caf-117">El uso de RGB 555 es esencialmente el mismo que el de RGB 565, salvo que las máscaras de bits y las operaciones de desplazamiento de bits son diferentes.</span><span class="sxs-lookup"><span data-stu-id="99caf-117">Working with RGB 555 is essentially the same as RGB 565, except the bit masks and bit shift operations are different.</span></span> <span data-ttu-id="99caf-118">Para obtener los componentes de color de un píxel RGB 555, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="99caf-118">To get the color components from an RGB 555 pixel, do the following:</span></span>


```C++
WORD red_mask = 0x7C00;
WORD green_mask = 0x3E0;
WORD blue_mask = 0x1F;

BYTE red_value = (pixel & red_mask) >> 10;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);

// Expand to 8-bit values:
BYTE red   = red_value << 3;
BYTE green = green_value << 3;
BYTE blue  = blue_value << 3;
```



<span data-ttu-id="99caf-119">Para empaquetar los valores de color rojo, verde y azul en un píxel RGB 555, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="99caf-119">To pack the red, green, and blue color values into an RGB 555 pixel, do the following:</span></span>


```C++
WORD pixel565 = (red << 10) | (green << 5) | blue;
```



## <a name="related-topics"></a><span data-ttu-id="99caf-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="99caf-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99caf-121">Subtipos de vídeo RGB sin comprimir</span><span class="sxs-lookup"><span data-stu-id="99caf-121">Uncompressed RGB Video Subtypes</span></span>](uncompressed-rgb-video-subtypes.md)
</dt> </dl>

 

 



