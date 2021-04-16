---
title: IAgentBalloon GetFontSize
description: IAgentBalloon GetFontSize
ms.assetid: 4d342ee9-abb4-431b-bd28-f62ab76705ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14b1a921f1f5c9927f58ab9e561569ba3bc98fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269416"
---
# <a name="iagentballoongetfontsize"></a><span data-ttu-id="35550-103">IAgentBalloon::GetFontSize</span><span class="sxs-lookup"><span data-stu-id="35550-103">IAgentBalloon::GetFontSize</span></span>

<span data-ttu-id="35550-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="35550-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in word balloon 
```

<span data-ttu-id="35550-105">Recupera el valor para el tamaño de la fuente que se muestra en un globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="35550-105">Retrieves the value for the size of the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="35550-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="35550-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="35550-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span><span class="sxs-lookup"><span data-stu-id="35550-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="35550-108">Dirección de un valor que recibe el tamaño de la fuente.</span><span class="sxs-lookup"><span data-stu-id="35550-108">The address of a value that receives the size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="35550-109">El tamaño de fuente predeterminado utilizado en un globo de palabras de caracteres se define en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="35550-109">The default font size used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="35550-110">Puede cambiarlo con [**IAgentBalloon:: SetFontSize**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**).</span><span class="sxs-lookup"><span data-stu-id="35550-110">You can change it with [**IAgentBalloon::SetFontSize**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**).</span></span> <span data-ttu-id="35550-111">Sin embargo, el usuario puede invalidar la configuración de tamaño de fuente para todos los caracteres mediante la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="35550-111">However, the user can override the font size settings for all characters using the Microsoft Agent property sheet.</span></span>

 

 




