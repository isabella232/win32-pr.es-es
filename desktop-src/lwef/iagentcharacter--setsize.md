---
title: IAgentCharacter setSize
description: IAgentCharacter setSize
ms.assetid: 8324ab84-2b59-4459-b375-700d72b621bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39d5b33afa7ff59516b793f194a0ba186c2e002
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778721"
---
# <a name="iagentcharactersetsize"></a><span data-ttu-id="1ef94-103">IAgentCharacter:: setSize</span><span class="sxs-lookup"><span data-stu-id="1ef94-103">IAgentCharacter::SetSize</span></span>

<span data-ttu-id="1ef94-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1ef94-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSize(
   long * lWidth,  // width of the character frame
   long * lHeight  // height of the character frame
);
```

<span data-ttu-id="1ef94-105">Establece el tamaño del fotograma de animación del carácter.</span><span class="sxs-lookup"><span data-stu-id="1ef94-105">Sets the size of the character's animation frame.</span></span>

-   <span data-ttu-id="1ef94-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1ef94-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1ef94-107"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span><span class="sxs-lookup"><span data-stu-id="1ef94-107"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span></span>
</dt> <dd>

<span data-ttu-id="1ef94-108">Ancho del fotograma de animación del carácter en píxeles.</span><span class="sxs-lookup"><span data-stu-id="1ef94-108">The width of the character's animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="1ef94-109"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span><span class="sxs-lookup"><span data-stu-id="1ef94-109"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span></span>
</dt> <dd>

<span data-ttu-id="1ef94-110">Alto del fotograma de animación del carácter en píxeles.</span><span class="sxs-lookup"><span data-stu-id="1ef94-110">The height of the character's animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="1ef94-111">Al cambiar el tamaño del marco del carácter, se escala el carácter al conjunto de tamaños con este método.</span><span class="sxs-lookup"><span data-stu-id="1ef94-111">Changing the character's frame size scales the character to the size set with this method.</span></span> <span data-ttu-id="1ef94-112">La configuración de esta propiedad se aplica a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="1ef94-112">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="1ef94-113">Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en el marco de la animación rectangular.</span><span class="sxs-lookup"><span data-stu-id="1ef94-113">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ef94-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1ef94-114">See Also</span></span>

[<span data-ttu-id="1ef94-115">**IAgentCharacter:: obtiene**</span><span class="sxs-lookup"><span data-stu-id="1ef94-115">**IAgentCharacter::GetSize**</span></span>](iagentcharacter--getsize.md)


 

 




