---
title: IAgentCharacter SetPosition
description: IAgentCharacter SetPosition
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aee48ea26c714c570f7ae11b9b2dbc0fe92ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075502"
---
# <a name="iagentcharactersetposition"></a><span data-ttu-id="71dbd-103">IAgentCharacter:: SetPosition</span><span class="sxs-lookup"><span data-stu-id="71dbd-103">IAgentCharacter::SetPosition</span></span>

<span data-ttu-id="71dbd-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="71dbd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPosition(
   long lLeft,  // screen coordinate of the left edge of character 
   long lTop    // screen coordinate of the top edge of character 
);
```

<span data-ttu-id="71dbd-105">Establece la posición del fotograma de animación del carácter.</span><span class="sxs-lookup"><span data-stu-id="71dbd-105">Sets the position of the character's animation frame.</span></span>

-   <span data-ttu-id="71dbd-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="71dbd-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="71dbd-107"><span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*</span><span class="sxs-lookup"><span data-stu-id="71dbd-107"><span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*</span></span>
</dt> <dd>

<span data-ttu-id="71dbd-108">Coordenada de pantalla del borde izquierdo del marco de la animación de caracteres, en píxeles, con respecto al origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="71dbd-108">Screen coordinate of the character animation frame's left edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="71dbd-109"><span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*</span><span class="sxs-lookup"><span data-stu-id="71dbd-109"><span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*</span></span>
</dt> <dd>

<span data-ttu-id="71dbd-110">Coordenada de pantalla del borde superior del marco de la animación de caracteres, en píxeles, con respecto al origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="71dbd-110">Screen coordinate of the character animation frame's top edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="71dbd-111">La configuración de esta propiedad se aplica a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="71dbd-111">This property's setting applies to all clients of the character.</span></span> <span data-ttu-id="71dbd-112">Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en el marco de la animación rectangular.</span><span class="sxs-lookup"><span data-stu-id="71dbd-112">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

> [!Note]  
> <span data-ttu-id="71dbd-113">A diferencia del método [**moveTo**](https://www.bing.com/search?q=**MoveTo**) , esta función no se pone en cola.</span><span class="sxs-lookup"><span data-stu-id="71dbd-113">Unlike the [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) method, this function is not queued.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="71dbd-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="71dbd-114">See Also</span></span>

[<span data-ttu-id="71dbd-115">**IAgentCharacter:: GetPosition**</span><span class="sxs-lookup"><span data-stu-id="71dbd-115">**IAgentCharacter::GetPosition**</span></span>](iagentcharacter--getposition.md)


 

 




