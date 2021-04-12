---
title: IAgentCharacter GetDescription
description: IAgentCharacter GetDescription
ms.assetid: 729f54ac-1c60-4a7b-b993-5682a6ea2b3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423cd1f5c799cc1f0177f6d3d7922d5d14de1dbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419207"
---
# <a name="iagentcharactergetdescription"></a><span data-ttu-id="f3e11-103">IAgentCharacter:: GetDescription</span><span class="sxs-lookup"><span data-stu-id="f3e11-103">IAgentCharacter::GetDescription</span></span>

<span data-ttu-id="f3e11-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f3e11-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetDescription(
   BSTR * pbszDescription   // address of buffer for character description
); 
```

<span data-ttu-id="f3e11-105">Recupera la descripción del carácter.</span><span class="sxs-lookup"><span data-stu-id="f3e11-105">Retrieves the description of the character.</span></span>

-   <span data-ttu-id="f3e11-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f3e11-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f3e11-107"><span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszDescription*</span><span class="sxs-lookup"><span data-stu-id="f3e11-107"><span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszDescription*</span></span>
</dt> <dd>

<span data-ttu-id="f3e11-108">Dirección de un BSTR que recibe el valor de la descripción del carácter.</span><span class="sxs-lookup"><span data-stu-id="f3e11-108">The address of a BSTR that receives the value of the description for the character.</span></span> <span data-ttu-id="f3e11-109">La descripción de un carácter se define cuando se compila con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f3e11-109">A character's description is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="f3e11-110">La configuración de la descripción es opcional y es posible que no se proporcione para todos los caracteres.</span><span class="sxs-lookup"><span data-stu-id="f3e11-110">The description setting is optional and may not be supplied for all characters.</span></span>

</dd> </dl>

 

 




