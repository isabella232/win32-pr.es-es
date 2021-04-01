---
title: IAgentBalloon GetBackColor
description: IAgentBalloon GetBackColor
ms.assetid: 278ed645-0e6c-4a5d-bd85-3e3b7a1e3333
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cce886c9929892c89b56f162f784dc27a472209
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075920"
---
# <a name="iagentballoongetbackcolor"></a><span data-ttu-id="c8818-103">IAgentBalloon::GetBackColor</span><span class="sxs-lookup"><span data-stu-id="c8818-103">IAgentBalloon::GetBackColor</span></span>

<span data-ttu-id="c8818-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c8818-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetBackColor(
   long * plBGColor  // address of variable for background color displayed
);                   // in word balloon
```

<span data-ttu-id="c8818-105">Recupera el valor para el color de fondo que se muestra en un globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="c8818-105">Retrieves the value for the background color displayed in a word balloon.</span></span>

-   <span data-ttu-id="c8818-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c8818-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c8818-107"><span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*</span><span class="sxs-lookup"><span data-stu-id="c8818-107"><span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*</span></span>
</dt> <dd>

<span data-ttu-id="c8818-108">Dirección de una variable que recibe la configuración de color para el fondo del globo.</span><span class="sxs-lookup"><span data-stu-id="c8818-108">The address of a variable that receives the color setting for the balloon background.</span></span>

</dd> </dl>

<span data-ttu-id="c8818-109">El color de fondo que se usa en un globo de palabras de caracteres se define en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c8818-109">The background color used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="c8818-110">No se puede cambiar por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="c8818-110">It cannot be changed by an application.</span></span> <span data-ttu-id="c8818-111">Sin embargo, el usuario puede cambiar el color de fondo de los globos de palabras para todos los caracteres a través de la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c8818-111">However, the user can change the background color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8818-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c8818-112">See Also</span></span>

[<span data-ttu-id="c8818-113">**IAgentBalloon::GetForeColor**</span><span class="sxs-lookup"><span data-stu-id="c8818-113">**IAgentBalloon::GetForeColor**</span></span>](iagentballoon--getforecolor.md)


 

 




