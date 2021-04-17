---
title: IAgentNotifySinkEx DefaultCharacterChange
description: IAgentNotifySinkEx DefaultCharacterChange
ms.assetid: 13acb502-e247-433f-abf3-2d78a2d6a4a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ec212887d17d1aa59d942ece79b3e6928900ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704705"
---
# <a name="iagentnotifysinkexdefaultcharacterchange"></a><span data-ttu-id="8a357-103">IAgentNotifySinkEx::D efaultCharacterChange</span><span class="sxs-lookup"><span data-stu-id="8a357-103">IAgentNotifySinkEx::DefaultCharacterChange</span></span>

<span data-ttu-id="8a357-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8a357-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DefaultCharacterChange(
   BSTR bszGUID  // character identifier
);
```

<span data-ttu-id="8a357-105">Notifica a una aplicación cliente cuando cambia el carácter predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8a357-105">Notifies a client application when the default character changes.</span></span>

-   <span data-ttu-id="8a357-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8a357-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="8a357-107"><span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszGUID*</span><span class="sxs-lookup"><span data-stu-id="8a357-107"><span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszGUID*</span></span>
</dt> <dd>

<span data-ttu-id="8a357-108">Identificador único del carácter.</span><span class="sxs-lookup"><span data-stu-id="8a357-108">The unique identifier for the character.</span></span>

</dd> </dl>

<span data-ttu-id="8a357-109">Cuando el usuario cambia el carácter asignado como carácter predeterminado del usuario, el servidor envía este evento a los clientes que han cargado el carácter predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8a357-109">When the user changes the character assigned as the user's default character, the server sends this event to clients that have loaded the default character.</span></span> <span data-ttu-id="8a357-110">El evento devuelve el identificador único (GUID) del carácter con formato con llaves y guiones, que se define cuando el carácter se crea con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8a357-110">The event returns the character's unique identifier (GUID) formatted with braces and dashes, which is defined when the character is built with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="8a357-111">Cuando aparece el nuevo carácter, se da por supuesto que tiene el mismo tamaño que cualquier instancia ya cargada del carácter o el carácter predeterminado anterior (en ese orden).</span><span class="sxs-lookup"><span data-stu-id="8a357-111">When the new character appears, it assumes the same size as any already loaded instance of the character or the previous default character (in that order).</span></span>

## <a name="see-also"></a><span data-ttu-id="8a357-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8a357-112">See Also</span></span>

[<span data-ttu-id="8a357-113">**IAgent:: Load**</span><span class="sxs-lookup"><span data-stu-id="8a357-113">**IAgent::Load**</span></span>](iagent--load.md)


 

 




