---
title: Crear el archivo de región
description: Crear el archivo de región
ms.assetid: e901dfa1-1e06-4136-b877-64be03107f6f
keywords:
- Aspectos móviles de Windows Media Player, archivos de regiones
- máscaras, archivos de regiones
- crear máscaras, archivos de regiones
- Archivos de regiones en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bf3268b101255191bef4b3e4c4880e2bb846414
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356781"
---
# <a name="creating-the-region-file"></a><span data-ttu-id="5598b-107">Crear el archivo de región</span><span class="sxs-lookup"><span data-stu-id="5598b-107">Creating the Region File</span></span>

<span data-ttu-id="5598b-108">Querrá crear un archivo de región que muestre qué áreas responden a los grifos.</span><span class="sxs-lookup"><span data-stu-id="5598b-108">You will want to create a Region file that shows what areas respond to taps.</span></span> <span data-ttu-id="5598b-109">Simplemente puede copiar los niveles base de cada elemento en una nueva capa y colorearlos para que se correspondan con los números de color que utilizará en el archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="5598b-109">You can simply copy the base layers of each element to a new layer, and color them to correspond to the color numbers you will use in the skin definition file.</span></span> <span data-ttu-id="5598b-110">Asegúrese de que las imágenes que crea en esta capa son sólidas y que no se aplica ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="5598b-110">Be sure that the images you create in this layer are solid and that no effects are applied.</span></span> <span data-ttu-id="5598b-111">Probablemente querrá anotar los números de color de cada imagen.</span><span class="sxs-lookup"><span data-stu-id="5598b-111">You will probably want to write down the color numbers for each image.</span></span> <span data-ttu-id="5598b-112">Puede obtener los números de color del selector de colores de Photoshop.</span><span class="sxs-lookup"><span data-stu-id="5598b-112">You can get the color numbers from the Photoshop Color Picker.</span></span> <span data-ttu-id="5598b-113">Desea los números RGB, que son tres números decimales.</span><span class="sxs-lookup"><span data-stu-id="5598b-113">You want the RGB numbers, which are three decimal numbers.</span></span> <span data-ttu-id="5598b-114">Cada número oscila entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="5598b-114">Each number ranges from 0 to 255.</span></span> <span data-ttu-id="5598b-115">Por ejemplo, un rojo sólido sería 255, 0,0.</span><span class="sxs-lookup"><span data-stu-id="5598b-115">For example, a solid red would be 255, 0, 0.</span></span>

> [!Note]  
> <span data-ttu-id="5598b-116">Los archivos de región no se usan en las máscaras móviles de Windows Media Player 10 porque los tipos de botón no se admiten en Windows Media Player 10 Mobile o posterior.</span><span class="sxs-lookup"><span data-stu-id="5598b-116">Region files are not used in Windows Media Player 10 Mobile skins because button types are not supported in Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="5598b-117">La siguiente imagen es el archivo de región.</span><span class="sxs-lookup"><span data-stu-id="5598b-117">The following image is the Region file.</span></span>

![archivo de región](images/ceswmreg.png)

<span data-ttu-id="5598b-119">Solo hay cuatro imágenes en este archivo porque solo los botones PlayPause, detener, siguiente y anterior son botones de tipo de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="5598b-119">There are only four images in this file because only the PlayPause, Stop, Next, and Prev buttons are hit-type buttons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5598b-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5598b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5598b-121">**Crear el arte**</span><span class="sxs-lookup"><span data-stu-id="5598b-121">**Creating the Art**</span></span>](creating-the-art.md)
</dt> </dl>

 

 




