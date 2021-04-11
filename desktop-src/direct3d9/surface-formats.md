---
description: En Direct3D, todas las imágenes bidimensionales (2D) se representan mediante un intervalo de memoria lineal denominado Surface.
ms.assetid: 33430f01-cd26-45f4-9ce8-ca2c17c7ae6b
title: Formatos de superficie (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78aad64940510a080ba05d0513e7f66d33912a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152433"
---
# <a name="surface-formats-direct3d-9"></a><span data-ttu-id="2ecaa-103">Formatos de superficie (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2ecaa-103">Surface Formats (Direct3D 9)</span></span>

<span data-ttu-id="2ecaa-104">En Direct3D, todas las imágenes bidimensionales (2D) se representan mediante un intervalo de memoria lineal denominado Surface.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-104">In Direct3D, all two-dimensional (2D) images are represented by a linear range of memory called a surface.</span></span> <span data-ttu-id="2ecaa-105">Una superficie puede considerarse como una matriz 2D en la que cada elemento contiene un valor de color que representa una pequeña sección de la imagen, denominada píxel.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-105">A surface can be thought of as a 2D array where each element holds a color value representing a small section of the image, called a pixel.</span></span> <span data-ttu-id="2ecaa-106">El nivel de detalle de una imagen se define tanto en el número de píxeles necesarios para representar la imagen como en el número de bits necesarios para el espectro de colores de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-106">An image's detail level is defined by both the number of pixels needed to represent the image, and the number of bits needed for the image's color spectrum.</span></span> <span data-ttu-id="2ecaa-107">Por ejemplo, una imagen de 800 píxeles de ancho por 600 píxeles de alto con 32 bits de color para cada píxel (escrito como 800x600x32) será más detallada que una imagen de 640 píxeles de ancho por 480 píxeles de alto con 16 bits de color para cada píxel (escrito como 640x480x16).</span><span class="sxs-lookup"><span data-stu-id="2ecaa-107">For example, an image that is 800 pixels wide by 600 pixels high with 32 bits of color for each pixel (written as 800x600x32) will be more detailed than an image that is 640 pixels wide by 480 pixels tall with 16 bits of color for each pixel (written as 640x480x16).</span></span> <span data-ttu-id="2ecaa-108">Del mismo modo, la imagen más detallada requerirá una superficie más grande para almacenar los datos.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-108">Likewise, the more detailed image will require a larger surface to store the data.</span></span> <span data-ttu-id="2ecaa-109">En el caso de una imagen 800x600x32, las dimensiones de la matriz de la superficie serán de 800x600 y cada elemento contendrá un valor de 32 bits para representar su color.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-109">For an 800x600x32 image, the surface's array dimensions will be 800x600, and each element will hold a 32-bit value to represent its color.</span></span>

<span data-ttu-id="2ecaa-110">Todas las superficies tienen un tamaño y almacenan un número específico de bits que representan el color.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-110">All surfaces have a size and store a specific number of bits that represent color.</span></span> <span data-ttu-id="2ecaa-111">Los bits que representan el color se separan en elementos de color individuales: rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-111">The bits that represent color are separated into individual color elements: red, green, and blue.</span></span> <span data-ttu-id="2ecaa-112">En Direct3D, todos los elementos de color se definen mediante el tipo enumerado [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="2ecaa-112">In Direct3D all color elements are defined by the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="2ecaa-113">Un formato de color de Direct3D se divide en el número de bytes reservados para cada color.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-113">A Direct3D color format is broken down into the number of byes reserved for each color.</span></span> <span data-ttu-id="2ecaa-114">Por ejemplo, un formato de color de 16 bits en Direct3D se define como D3DFMT \_ R5G6B5, donde 5 bits están reservados para rojo (R), 6 bits para verde (G) y 5 bits para azul (B).</span><span class="sxs-lookup"><span data-stu-id="2ecaa-114">For example, a 16-bit color format in Direct3D is defined as D3DFMT\_R5G6B5, where 5 bits are reserved for red (R), 6 bits for green (G), and 5 bits for blue (B).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ecaa-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2ecaa-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ecaa-116">Superficies de Direct3D</span><span class="sxs-lookup"><span data-stu-id="2ecaa-116">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> </dl>

 

 



