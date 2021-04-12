---
title: Sección de marquesina de ejemplo
description: Sección de marquesina de ejemplo
ms.assetid: 44ed3257-2e1a-4b8d-9d55-a13b0400422d
keywords:
- Aspectos móviles de Windows Media Player, marquesinas
- máscaras, marquesinas
- referencia de las máscaras, marquesinas
- marquesinas en máscaras, sección de marquesina
- archivos de definición de máscara, sección de marquesina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f66588d81b22051a9289a80c8733d5cfe154bed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486963"
---
# <a name="sample-marquee-section"></a><span data-ttu-id="c6964-108">Sección de marquesina de ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6964-108">Sample Marquee Section</span></span>

<span data-ttu-id="c6964-109">Las siguientes líneas muestran una sección de marquesina típica de un archivo de definición de máscara:</span><span class="sxs-lookup"><span data-stu-id="c6964-109">The following lines show a typical Marquee section of a skin definition file:</span></span>


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>

//  ----------   ------       -------      ------------------------

    3,2,234,20   Tahoma,12,N  255,0,0    Title+Author, Title, Author


```



<span data-ttu-id="c6964-110">Esto define un cuadro de presentación de marquesina que muestra el título y el autor si ambos están definidos, el título si solo se define el título o el nombre del autor si solo se define Author.</span><span class="sxs-lookup"><span data-stu-id="c6964-110">This defines a marquee display box that shows the title and author if both are defined, the title if only Title is defined, or the name of the author if only Author is defined.</span></span> <span data-ttu-id="c6964-111">Si no se define ninguno, no se mostrará nada.</span><span class="sxs-lookup"><span data-stu-id="c6964-111">If neither is defined, nothing will be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6964-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6964-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6964-113">**Marquesina**</span><span class="sxs-lookup"><span data-stu-id="c6964-113">**Marquee**</span></span>](marquee.md)
</dt> </dl>

 

 




