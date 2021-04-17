---
title: IAgentCharacter se obtiene
description: IAgentCharacter se obtiene
ms.assetid: bc2d6fe4-5945-4a35-b603-409c66f8aa2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e40c219cd0a1dc1d11738149ca7cfd9869fe682e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357792"
---
# <a name="iagentcharactergetsize"></a><span data-ttu-id="32257-103">IAgentCharacter:: obtiene</span><span class="sxs-lookup"><span data-stu-id="32257-103">IAgentCharacter::GetSize</span></span>

<span data-ttu-id="32257-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="32257-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

<span data-ttu-id="32257-105">Recupera el tamaño del fotograma de animación del carácter.</span><span class="sxs-lookup"><span data-stu-id="32257-105">Retrieves the size of the character's animation frame.</span></span>

-   <span data-ttu-id="32257-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="32257-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="32257-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="32257-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="32257-108">Dirección de una variable que recibe el ancho del fotograma de animación de caracteres en píxeles, con respecto al origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="32257-108">Address of a variable that receives the width of the character animation frame in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="32257-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="32257-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="32257-110">Dirección de una variable que recibe el alto del fotograma de animación de caracteres en píxeles, con respecto al origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="32257-110">Address of a variable that receives the height of the character animation frame in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="32257-111">Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en el marco de la animación rectangular.</span><span class="sxs-lookup"><span data-stu-id="32257-111">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="32257-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="32257-112">See Also</span></span>

[<span data-ttu-id="32257-113">**IAgentCharacter:: setSize**</span><span class="sxs-lookup"><span data-stu-id="32257-113">**IAgentCharacter::SetSize**</span></span>](iagentcharacter--setsize.md)


 

 




