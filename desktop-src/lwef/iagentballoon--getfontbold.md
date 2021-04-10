---
title: IAgentBalloon GetFontBold
description: IAgentBalloon GetFontBold
ms.assetid: 5a55f771-d68e-4f66-8001-47c141661b06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858f6f42964db1bdd7ae548d308c6f6668b05631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268947"
---
# <a name="iagentballoongetfontbold"></a><span data-ttu-id="1f624-103">IAgentBalloon::GetFontBold</span><span class="sxs-lookup"><span data-stu-id="1f624-103">IAgentBalloon::GetFontBold</span></span>

<span data-ttu-id="1f624-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1f624-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontBold(
   long * pbFontBold  // address of variable for bold setting for
);                    // font displayed in word balloon 
```

<span data-ttu-id="1f624-105">Indica si la fuente utilizada en un globo de palabras está en negrita.</span><span class="sxs-lookup"><span data-stu-id="1f624-105">Indicates whether the font used in a word balloon is bold.</span></span>

-   <span data-ttu-id="1f624-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1f624-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1f624-107"><span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*pbFontBold*</span><span class="sxs-lookup"><span data-stu-id="1f624-107"><span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*pbFontBold*</span></span>
</dt> <dd>

<span data-ttu-id="1f624-108">Dirección de un valor que recibe **true** si la fuente está en negrita y **false** si no está en negrita.</span><span class="sxs-lookup"><span data-stu-id="1f624-108">The address of a value that receives **True** if the font is bold and **False** if not bold.</span></span>

</dd> </dl>

<span data-ttu-id="1f624-109">El estilo de fuente utilizado en un globo de palabras de caracteres se define en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1f624-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="1f624-110">No se puede cambiar por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="1f624-110">It cannot be changed by an application.</span></span> <span data-ttu-id="1f624-111">Sin embargo, el usuario puede invalidar la configuración de fuente para todos los caracteres a través de la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1f624-111">However, the user can override the font settings for all characters through the Microsoft Agent property sheet.</span></span>

 

 




