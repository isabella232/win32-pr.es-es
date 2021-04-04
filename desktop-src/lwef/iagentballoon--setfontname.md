---
title: IAgentBalloon SetFontName
description: IAgentBalloon SetFontName
ms.assetid: 6babf5f6-2abd-46c2-ade0-899a8e4488bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f983064c5df8cde8322658bbd0c713bbf238ecf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076307"
---
# <a name="iagentballoonsetfontname"></a><span data-ttu-id="cc5e3-103">IAgentBalloon::SetFontName</span><span class="sxs-lookup"><span data-stu-id="cc5e3-103">IAgentBalloon::SetFontName</span></span>

<span data-ttu-id="cc5e3-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cc5e3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font displayed in word balloon
);
                   
```

<span data-ttu-id="cc5e3-105">Establece la fuente que se muestra en el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="cc5e3-105">Sets the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="cc5e3-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="cc5e3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="cc5e3-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span><span class="sxs-lookup"><span data-stu-id="cc5e3-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="cc5e3-108">BSTR que establece la fuente mostrada en el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="cc5e3-108">A BSTR that sets the font displayed in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="cc5e3-109">La fuente predeterminada utilizada en el globo de palabras de un carácter se define en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cc5e3-109">The default font used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="cc5e3-110">Puede cambiarlo con **IAgentBalloon:: SetFontName**.</span><span class="sxs-lookup"><span data-stu-id="cc5e3-110">You can change it with **IAgentBalloon::SetFontName**.</span></span> <span data-ttu-id="cc5e3-111">Sin embargo, el usuario puede invalidar la configuración de fuente para todos los caracteres mediante la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cc5e3-111">However, the user can override the font setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc5e3-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cc5e3-112">See Also</span></span>

[<span data-ttu-id="cc5e3-113">**IAgentBalloon:: GetVisible**</span><span class="sxs-lookup"><span data-stu-id="cc5e3-113">**IAgentBalloon::GetVisible**</span></span>](iagentballoon--getvisible.md)


 

 




