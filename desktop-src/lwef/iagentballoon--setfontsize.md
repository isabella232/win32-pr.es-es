---
title: IAgentBalloon SetFontSize
description: IAgentBalloon SetFontSize
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4984382408739e2d093226d04b1c99582a1a25d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357665"
---
# <a name="iagentballoonsetfontsize"></a><span data-ttu-id="bb553-103">IAgentBalloon::SetFontSize</span><span class="sxs-lookup"><span data-stu-id="bb553-103">IAgentBalloon::SetFontSize</span></span>

<span data-ttu-id="bb553-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bb553-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in word balloon
); 
```

<span data-ttu-id="bb553-105">Establece el tamaño de la fuente que se muestra en el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="bb553-105">Sets the size of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="bb553-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="bb553-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="bb553-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span><span class="sxs-lookup"><span data-stu-id="bb553-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="bb553-108">Tamaño de la fuente.</span><span class="sxs-lookup"><span data-stu-id="bb553-108">The size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="bb553-109">El tamaño de fuente predeterminado utilizado en el globo de palabras de un carácter se define en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bb553-109">The default font size used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="bb553-110">Puede cambiarlo con **IAgentBalloon:: SetFontSize**.</span><span class="sxs-lookup"><span data-stu-id="bb553-110">You can change it with **IAgentBalloon::SetFontSize**.</span></span> <span data-ttu-id="bb553-111">Sin embargo, el usuario puede invalidar la configuración de tamaño de fuente para todos los caracteres mediante la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bb553-111">However, the user can override the font size setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="bb553-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bb553-112">See Also</span></span>

[<span data-ttu-id="bb553-113">**IAgentBalloon::GetFontSize**</span><span class="sxs-lookup"><span data-stu-id="bb553-113">**IAgentBalloon::GetFontSize**</span></span>](iagentballoon--getfontsize.md)


 

 




