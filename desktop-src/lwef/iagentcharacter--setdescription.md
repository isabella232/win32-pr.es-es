---
title: IAgentCharacter SetDescription
description: IAgentCharacter SetDescription
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9815e5c0e01537c7db2b400326f86da37af003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419199"
---
# <a name="iagentcharactersetdescription"></a><span data-ttu-id="c01d8-103">IAgentCharacter:: SetDescription</span><span class="sxs-lookup"><span data-stu-id="c01d8-103">IAgentCharacter::SetDescription</span></span>

<span data-ttu-id="c01d8-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c01d8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetDescription(
   BSTR bszDescription   // character description
); 
```

<span data-ttu-id="c01d8-105">Establece la descripción del carácter.</span><span class="sxs-lookup"><span data-stu-id="c01d8-105">Sets the description of the character.</span></span>

-   <span data-ttu-id="c01d8-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c01d8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c01d8-107"><span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*</span><span class="sxs-lookup"><span data-stu-id="c01d8-107"><span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*</span></span>
</dt> <dd>

<span data-ttu-id="c01d8-108">BSTR que establece la descripción del carácter.</span><span class="sxs-lookup"><span data-stu-id="c01d8-108">A BSTR that sets the description for the character.</span></span> <span data-ttu-id="c01d8-109">La descripción predeterminada de un carácter se define cuando se compila con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c01d8-109">A character's default description is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="c01d8-110">La configuración de la descripción es opcional y es posible que no se proporcione para todos los caracteres.</span><span class="sxs-lookup"><span data-stu-id="c01d8-110">The description setting is optional and may not be supplied for all characters.</span></span> <span data-ttu-id="c01d8-111">Puede cambiar la descripción del carácter mediante **IAgentCharacter:: setDescription**; sin embargo, este valor no es persistente (se almacena de forma permanente).</span><span class="sxs-lookup"><span data-stu-id="c01d8-111">You can change the character's description using **IAgentCharacter::setDescription**; however, this value is not persistent (stored permanently).</span></span> <span data-ttu-id="c01d8-112">La descripción del carácter vuelve a su configuración predeterminada siempre que un cliente carga el carácter por primera vez.</span><span class="sxs-lookup"><span data-stu-id="c01d8-112">The character's description reverts to its default setting whenever the character is first loaded by a client.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="c01d8-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c01d8-113">See Also</span></span>

[<span data-ttu-id="c01d8-114">**IAgentCharacter:: GetDescription**</span><span class="sxs-lookup"><span data-stu-id="c01d8-114">**IAgentCharacter::GetDescription**</span></span>](iagentcharacter--getdescription.md)


 

 




