---
title: Mapas de bits (SDK de Windows Media Player)
description: Mapas de bits
ms.assetid: cd10bc7d-1167-485e-8acf-13c021bc608b
keywords:
- Máscaras móviles de Windows Media Player, mapas de bits
- máscaras, mapas de bits
- referencia para máscaras, mapas de bits
- mapas de bits en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ad690b691c22154bad4db0981e2b5ab760400b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488656"
---
# <a name="bitmaps-windows-media-player-sdk"></a><span data-ttu-id="f1c1d-107">Mapas de bits (SDK de Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="f1c1d-107">Bitmaps (Windows Media Player SDK)</span></span>

<span data-ttu-id="f1c1d-108">Debe usar una o varias imágenes en la máscara y cada imagen debe definirse en el archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="f1c1d-108">You must use one or more images in your skin, and each image must be defined in the skin definition file.</span></span> <span data-ttu-id="f1c1d-109">Si no define una imagen en esta sección, la máscara no podrá utilizarla.</span><span class="sxs-lookup"><span data-stu-id="f1c1d-109">If you do not define an image in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="f1c1d-110">El término "mapa de bits" se usa en toda la referencia en un sentido genérico y hace referencia a las imágenes de mapa de bits con una extensión. bmp, imágenes GIF con una extensión. gif, imágenes JPEG con una extensión. jpg y imágenes PNG con una extensión. png.</span><span class="sxs-lookup"><span data-stu-id="f1c1d-110">The term "bitmap" is used throughout the reference in a generic sense, and refers to bitmap images with a .bmp extension, GIF images with a .gif extension, JPEG images with a .jpg extension, and PNG images with a .png extension.</span></span>

<span data-ttu-id="f1c1d-111">La sección de mapas de bits del archivo de definición de máscara comienza con esta línea:</span><span class="sxs-lookup"><span data-stu-id="f1c1d-111">The Bitmaps section of the skin definition file begins with this line:</span></span>


```C++
[ Bitmaps ]

```



<span data-ttu-id="f1c1d-112">A continuación, debe agregar una o más líneas que contengan información sobre cada una de las imágenes de la máscara.</span><span class="sxs-lookup"><span data-stu-id="f1c1d-112">You then must add one or more lines that contain information about each of the images in your skin.</span></span>

<span data-ttu-id="f1c1d-113">Una línea típica podría ser:</span><span class="sxs-lookup"><span data-stu-id="f1c1d-113">A typical line might be:</span></span>


```C++
    Background  Background.bmp  0,0

```



<span data-ttu-id="f1c1d-114">Puede usar la siguiente plantilla para la sección de mapas de bits del archivo de definición de máscara:</span><span class="sxs-lookup"><span data-stu-id="f1c1d-114">You can use the following template for the Bitmaps section of your skin definition file:</span></span>


```C++
//  <Type>      <Filename>      <X,Y>
//  ------      -----------     -----

```



<span data-ttu-id="f1c1d-115">Debe utilizar el orden siguiente para obtener información de mapa de bits para cada línea de la sección mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="f1c1d-115">You must use the following order for bitmap information for each line in the Bitmap section.</span></span> <span data-ttu-id="f1c1d-116">Cada parte de la línea es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="f1c1d-116">Each part of the line is required.</span></span>

1.  [<span data-ttu-id="f1c1d-117">Tipo de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="f1c1d-117">Bitmap Type</span></span>](bitmap-type.md)
2.  [<span data-ttu-id="f1c1d-118">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="f1c1d-118">File Name</span></span>](file-name.md)
3.  [<span data-ttu-id="f1c1d-119">Unas</span><span class="sxs-lookup"><span data-stu-id="f1c1d-119">Coordinates</span></span>](coordinates.md)

<span data-ttu-id="f1c1d-120">Para obtener un ejemplo de código de mapa de bits, consulte la [sección de mapa de bits de ejemplo](sample-bitmap-section.md).</span><span class="sxs-lookup"><span data-stu-id="f1c1d-120">For an example of bitmap code, see [Sample Bitmap Section](sample-bitmap-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1c1d-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f1c1d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1c1d-122">**Referencia de máscara**</span><span class="sxs-lookup"><span data-stu-id="f1c1d-122">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




