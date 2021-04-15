---
title: IAgentCharacter SetName
description: IAgentCharacter SetName
ms.assetid: 4944f910-60e9-446b-82e9-2794f445789a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec058e338adfa8c998bf26a1223ae71f0c7de3d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714267"
---
# <a name="iagentcharactersetname"></a><span data-ttu-id="831e8-103">IAgentCharacter:: SetName</span><span class="sxs-lookup"><span data-stu-id="831e8-103">IAgentCharacter::SetName</span></span>

<span data-ttu-id="831e8-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="831e8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetName(
   BSTR bszName   // character name
);
```

<span data-ttu-id="831e8-105">Establece el nombre del carácter.</span><span class="sxs-lookup"><span data-stu-id="831e8-105">Sets the name of the character.</span></span>

-   <span data-ttu-id="831e8-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="831e8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="831e8-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span><span class="sxs-lookup"><span data-stu-id="831e8-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="831e8-108">BSTR que establece el nombre del carácter.</span><span class="sxs-lookup"><span data-stu-id="831e8-108">A BSTR that sets the character's name.</span></span> <span data-ttu-id="831e8-109">El nombre predeterminado de un carácter se define cuando se compila con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="831e8-109">A character's default name is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="831e8-110">Puede cambiarlo mediante **IAgentCharacter:: setName**; sin embargo, esto cambia el nombre de carácter de todos los clientes actuales del carácter.</span><span class="sxs-lookup"><span data-stu-id="831e8-110">You can change it using **IAgentCharacter::SetName**; however, this changes the character name for all current clients of the character.</span></span> <span data-ttu-id="831e8-111">Esta propiedad no es persistente (se almacena de forma permanente).</span><span class="sxs-lookup"><span data-stu-id="831e8-111">This property is not persistent (stored permanently).</span></span> <span data-ttu-id="831e8-112">El nombre del carácter vuelve a su nombre predeterminado cada vez que un cliente carga el carácter por primera vez.</span><span class="sxs-lookup"><span data-stu-id="831e8-112">The character's name reverts to its default name whenever the character is first loaded by a client.</span></span>

<span data-ttu-id="831e8-113">El nombre del carácter también puede depender de su identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="831e8-113">The character's name may also depend on its language ID.</span></span> <span data-ttu-id="831e8-114">Los caracteres se pueden compilar con nombres diferentes para distintos idiomas.</span><span class="sxs-lookup"><span data-stu-id="831e8-114">Characters can be compiled with different names for different languages.</span></span>

<span data-ttu-id="831e8-115">El servidor usa la configuración de nombre del carácter en partes de la interfaz del agente de Microsoft, como el título de la ventana comandos de voz cuando el carácter es de entrada-activo y en el menú emergente de la barra de tareas del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="831e8-115">The server uses the character's name setting in parts of the Microsoft Agent's interface, such as the Voice Commands Window title when the character is input-active and in the Microsoft Agent taskbar pop-up menu.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="831e8-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="831e8-116">See Also</span></span>

[<span data-ttu-id="831e8-117">**IAgentCharacter:: GetName**</span><span class="sxs-lookup"><span data-stu-id="831e8-117">**IAgentCharacter::GetName**</span></span>](iagentcharacter--getname.md)


 

 




