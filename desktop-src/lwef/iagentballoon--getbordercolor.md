---
title: IAgentBalloon GetBorderColor
description: IAgentBalloon GetBorderColor
ms.assetid: e6c592c3-0e14-474f-a829-6028f2de5791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f78bf9425cbb12c6a87f3ad64b6c5523dc7bbd8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777581"
---
# <a name="iagentballoongetbordercolor"></a><span data-ttu-id="efab3-103">IAgentBalloon::GetBorderColor</span><span class="sxs-lookup"><span data-stu-id="efab3-103">IAgentBalloon::GetBorderColor</span></span>

<span data-ttu-id="efab3-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="efab3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetBorderColor (
  long * plBorderColor// address of variable for border color displayed
);                    // for word balloon
```

<span data-ttu-id="efab3-105">Recupera el valor del color del borde que se muestra para un globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="efab3-105">Retrieves the value for the border color displayed for a word balloon.</span></span>

-   <span data-ttu-id="efab3-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="efab3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="efab3-107"><span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plBorderColor*</span><span class="sxs-lookup"><span data-stu-id="efab3-107"><span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plBorderColor*</span></span>
</dt> <dd>

<span data-ttu-id="efab3-108">Dirección de una variable que recibe la configuración de color para el borde del globo.</span><span class="sxs-lookup"><span data-stu-id="efab3-108">The address of a variable that receives the color setting for the balloon border.</span></span>

</dd> </dl>

<span data-ttu-id="efab3-109">El color del borde de un globo de palabras de caracteres se define en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="efab3-109">The border color for a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="efab3-110">No se puede cambiar por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="efab3-110">It cannot be changed by an application.</span></span> <span data-ttu-id="efab3-111">Sin embargo, el usuario puede cambiar el color del borde de los globos de palabras para todos los caracteres a través de la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="efab3-111">However, the user can change the border color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="efab3-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="efab3-112">See Also</span></span>

<span data-ttu-id="efab3-113">[**IAgentBalloon:: getBackColor**](iagentballoon--getbackcolor.md), [ **IAgentBalloon:: GetForeColor**](iagentballoon--getforecolor.md)</span><span class="sxs-lookup"><span data-stu-id="efab3-113">[**IAgentBalloon::GetBackColor**](iagentballoon--getbackcolor.md), [**IAgentBalloon::GetForeColor**](iagentballoon--getforecolor.md)</span></span>


 

 




