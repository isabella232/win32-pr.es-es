---
title: IAgentCharacterEx GetGUID
description: IAgentCharacterEx GetGUID
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9e0e14d0931774bf6ab5e1c8599bbebaadd0ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994431"
---
# <a name="iagentcharacterexgetguid"></a><span data-ttu-id="304aa-103">IAgentCharacterEx:: GetGUID</span><span class="sxs-lookup"><span data-stu-id="304aa-103">IAgentCharacterEx::GetGUID</span></span>

<span data-ttu-id="304aa-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="304aa-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetGUID(
   BSTR * pbszGUID  // address of character's ID
);
```

<span data-ttu-id="304aa-105">Recupera el identificador único del carácter.</span><span class="sxs-lookup"><span data-stu-id="304aa-105">Retrieves the unique ID for the character.</span></span>

-   <span data-ttu-id="304aa-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="304aa-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="304aa-107"><span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszGUID*</span><span class="sxs-lookup"><span data-stu-id="304aa-107"><span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszGUID*</span></span>
</dt> <dd>

<span data-ttu-id="304aa-108">Dirección de un BSTR que recibe el identificador del carácter.</span><span class="sxs-lookup"><span data-stu-id="304aa-108">Address of a BSTR that receives the ID for the character.</span></span>

</dd> </dl>

<span data-ttu-id="304aa-109">La propiedad devuelve una representación de cadena del GUID (con formato con llaves y guiones) que el servidor usa para identificar de forma única el carácter.</span><span class="sxs-lookup"><span data-stu-id="304aa-109">The property returns a string representation of the GUID (formatted with braces and dashes) that the server uses to uniquely identify the character.</span></span> <span data-ttu-id="304aa-110">Un identificador de carácter se establece cuando se compila con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="304aa-110">A character identifier is set when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="304aa-111">La propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="304aa-111">The property is read-only.</span></span>

 

 




