---
title: Sección de mapa de bits de ejemplo
description: Sección de mapa de bits de ejemplo
ms.assetid: 51b84b34-3cbb-4863-b7dc-e33e80d6ba23
keywords:
- Máscaras móviles de Windows Media Player, mapas de bits
- máscaras, mapas de bits
- referencia para máscaras, mapas de bits
- mapas de bits en máscaras, sección de mapas de bits
- archivos de definición de máscara, sección de mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b05183be7ba56ed5b00a6bfd26ee6162e008cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903686"
---
# <a name="sample-bitmap-section"></a><span data-ttu-id="7b33a-108">Sección de mapa de bits de ejemplo</span><span class="sxs-lookup"><span data-stu-id="7b33a-108">Sample Bitmap Section</span></span>

<span data-ttu-id="7b33a-109">Las siguientes líneas muestran una sección típica de mapas de bits de un archivo de definición de máscara:</span><span class="sxs-lookup"><span data-stu-id="7b33a-109">The following lines show a typical Bitmaps section of a skin definition file:</span></span>


```C++
[ Bitmaps ]

//  <Type>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0
    

```



<span data-ttu-id="7b33a-110">Esto define cinco mapas de bits que se usan para crear una imagen de fondo, imágenes para botones deshabilitados y insertados, una imagen de región para botones de región y una superimagen para trackbars.</span><span class="sxs-lookup"><span data-stu-id="7b33a-110">This defines five bitmaps that are used to create a Background image, images for Disabled and Pushed buttons, a Region image for region buttons, and a Super image for trackbars.</span></span>

> [!Note]  
> <span data-ttu-id="7b33a-111">Los mapas de bits de región y súper están en desuso en las máscaras de Windows Media Player 10 Mobile o posterior.</span><span class="sxs-lookup"><span data-stu-id="7b33a-111">The Region and Super bitmaps are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7b33a-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7b33a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b33a-113">**Mapas de bits**</span><span class="sxs-lookup"><span data-stu-id="7b33a-113">**Bitmaps**</span></span>](bitmaps.md)
</dt> </dl>

 

 




