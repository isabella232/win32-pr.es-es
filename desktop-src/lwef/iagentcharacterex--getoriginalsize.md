---
title: IAgentCharacterEx GetOriginalSize
description: IAgentCharacterEx GetOriginalSize
ms.assetid: a27ae88f-3655-4375-b563-0cc320d012cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e1712587e70d9756e3d37ca9e0f3cbfdb82c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075538"
---
# <a name="iagentcharacterexgetoriginalsize"></a><span data-ttu-id="795b5-103">IAgentCharacterEx::GetOriginalSize</span><span class="sxs-lookup"><span data-stu-id="795b5-103">IAgentCharacterEx::GetOriginalSize</span></span>

<span data-ttu-id="795b5-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="795b5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetOriginalSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

<span data-ttu-id="795b5-105">Recupera el tamaño original del fotograma de animación del carácter.</span><span class="sxs-lookup"><span data-stu-id="795b5-105">Retrieves the original size of the character's animation frame.</span></span>

-   <span data-ttu-id="795b5-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="795b5-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="795b5-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="795b5-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="795b5-108">Dirección de una variable que recibe el ancho original del fotograma de animación de caracteres en píxeles.</span><span class="sxs-lookup"><span data-stu-id="795b5-108">Address of a variable that receives the original width of the character animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="795b5-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="795b5-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="795b5-110">Dirección de una variable que recibe el alto original del fotograma de animación de caracteres en píxeles.</span><span class="sxs-lookup"><span data-stu-id="795b5-110">Address of a variable that receives the original height of the character animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="795b5-111">Esta llamada devuelve el tamaño original del marco de caracteres tal como está integrado en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="795b5-111">This call returns the original size of the character frame as built in the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="795b5-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="795b5-112">See Also</span></span>

[<span data-ttu-id="795b5-113">**IAgentCharacter:: obtiene**</span><span class="sxs-lookup"><span data-stu-id="795b5-113">**IAgentCharacter::GetSize**</span></span>](iagentcharacter--getsize.md)


 

 




