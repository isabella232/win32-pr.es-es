---
title: IAgentBalloon GetForeColor
description: IAgentBalloon GetForeColor
ms.assetid: b06ad924-66b6-42a6-8c97-5bc4c46f6e2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7a251471b0281661b087dbfb9b141c54ff9dc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714243"
---
# <a name="iagentballoongetforecolor"></a><span data-ttu-id="85558-103">IAgentBalloon::GetForeColor</span><span class="sxs-lookup"><span data-stu-id="85558-103">IAgentBalloon::GetForeColor</span></span>

<span data-ttu-id="85558-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="85558-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetForeColor(
   long * plFGColor // address of variable for foreground color displayed
);                  // in word balloon
```

<span data-ttu-id="85558-105">Recupera el valor del color de primer plano mostrado en un globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="85558-105">Retrieves the value for the foreground color displayed in a word balloon.</span></span>

-   <span data-ttu-id="85558-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="85558-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="85558-107"><span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*plFGColor*</span><span class="sxs-lookup"><span data-stu-id="85558-107"><span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*plFGColor*</span></span>
</dt> <dd>

<span data-ttu-id="85558-108">Dirección de una variable que recibe la configuración de color para el globo de primer plano.</span><span class="sxs-lookup"><span data-stu-id="85558-108">The address of a variable that receives the color setting for the balloon foreground.</span></span>

</dd> </dl>

<span data-ttu-id="85558-109">El color de primer plano utilizado en un globo de palabras de caracteres se define en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="85558-109">The foreground color used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="85558-110">No se puede cambiar por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="85558-110">It cannot be changed by an application.</span></span> <span data-ttu-id="85558-111">Sin embargo, el usuario puede invalidar el color de primer plano de los globos de palabras para todos los caracteres a través de la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="85558-111">However, the user can override the foreground color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="85558-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="85558-112">See Also</span></span>

[<span data-ttu-id="85558-113">**IAgentBalloon::GetBackColor**</span><span class="sxs-lookup"><span data-stu-id="85558-113">**IAgentBalloon::GetBackColor**</span></span>](iagentballoon--getbackcolor.md)


 

 




