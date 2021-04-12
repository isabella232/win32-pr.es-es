---
title: IAgentCharacter GetName
description: IAgentCharacter GetName
ms.assetid: 6c013a18-8c56-42a8-8723-31d83b3230cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33679577cfb5179a799ee61207f7ecd9b2be8a21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357794"
---
# <a name="iagentcharactergetname"></a><span data-ttu-id="171e9-103">IAgentCharacter:: GetName</span><span class="sxs-lookup"><span data-stu-id="171e9-103">IAgentCharacter::GetName</span></span>

<span data-ttu-id="171e9-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="171e9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetName(
   BSTR * pbszName   // address of buffer for character name
);
```

<span data-ttu-id="171e9-105">Recupera el nombre del carácter.</span><span class="sxs-lookup"><span data-stu-id="171e9-105">Retrieves the name of the character.</span></span>

-   <span data-ttu-id="171e9-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="171e9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="171e9-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span><span class="sxs-lookup"><span data-stu-id="171e9-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span></span>
</dt> <dd>

<span data-ttu-id="171e9-108">Dirección de un BSTR que recibe el valor del nombre del carácter.</span><span class="sxs-lookup"><span data-stu-id="171e9-108">The address of a BSTR that receives the value of the name for the character.</span></span>

</dd> </dl>

<span data-ttu-id="171e9-109">El nombre predeterminado de un carácter se define cuando se compila con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="171e9-109">A character's default name is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="171e9-110">El nombre de un carácter puede variar en función del identificador de idioma del carácter.</span><span class="sxs-lookup"><span data-stu-id="171e9-110">A character's name may vary based on the character's language ID.</span></span> <span data-ttu-id="171e9-111">Los caracteres se pueden compilar con nombres diferentes para distintos idiomas.</span><span class="sxs-lookup"><span data-stu-id="171e9-111">Characters can be compiled with different names for different languages.</span></span>

<span data-ttu-id="171e9-112">También puede establecer el nombre del carácter mediante **IAgentCharacter: setName**; sin embargo, esto cambia el nombre de todos los clientes actuales del carácter.</span><span class="sxs-lookup"><span data-stu-id="171e9-112">You can also set the character's name using **IAgentCharacter:SetName**; however, this changes the name for all current clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="171e9-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="171e9-113">See Also</span></span>

[<span data-ttu-id="171e9-114">**IAgentCharacter:: SetName**</span><span class="sxs-lookup"><span data-stu-id="171e9-114">**IAgentCharacter::SetName**</span></span>](iagentcharacter--setname.md)


 

 




