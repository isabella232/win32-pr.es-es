---
title: IAgentCommands GetCount
description: IAgentCommands GetCount
ms.assetid: 17140eda-17b0-49c2-8d50-5a38a553191a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ece3e007b644b370ee721cef2d273fa50d43ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420537"
---
# <a name="iagentcommandsgetcount"></a><span data-ttu-id="c2ab4-103">IAgentCommands:: GetCount</span><span class="sxs-lookup"><span data-stu-id="c2ab4-103">IAgentCommands::GetCount</span></span>

<span data-ttu-id="c2ab4-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c2ab4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of count of commands
);                    
```

<span data-ttu-id="c2ab4-105">Recupera el número de objetos de [**comando**](/windows/desktop/lwef/the-command-object) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="c2ab4-105">Retrieves the number of [**Command**](/windows/desktop/lwef/the-command-object) objects in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="c2ab4-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c2ab4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c2ab4-107"><span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*</span><span class="sxs-lookup"><span data-stu-id="c2ab4-107"><span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*</span></span>
</dt> <dd>

<span data-ttu-id="c2ab4-108">Dirección de una variable que recibe el número de [**comandos**](/windows/desktop/lwef/the-command-object) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="c2ab4-108">Address of a variable that receives the number of [**Commands**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

<span data-ttu-id="c2ab4-109">*pdwCount* incluye solo el número de [**comandos**](/windows/desktop/lwef/the-command-object) que se definen en la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="c2ab4-109">*pdwCount* includes only the number of [**Commands**](/windows/desktop/lwef/the-command-object) you define in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="c2ab4-110">No se incluyen las entradas de servidor o de otro cliente.</span><span class="sxs-lookup"><span data-stu-id="c2ab4-110">Server or other client entries are not included.</span></span>

 

 