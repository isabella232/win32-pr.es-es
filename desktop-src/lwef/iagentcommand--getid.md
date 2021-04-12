---
title: IAgentCommand GetID
description: IAgentCommand GetID
ms.assetid: 4d8d8be7-7003-4ef3-abba-b5232267c993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1f5887123df19496c0610c53fe59a3f64961cd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420554"
---
# <a name="iagentcommandgetid"></a><span data-ttu-id="84b1a-103">IAgentCommand:: GetID</span><span class="sxs-lookup"><span data-stu-id="84b1a-103">IAgentCommand::GetID</span></span>

<span data-ttu-id="84b1a-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="84b1a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetID(
   long * pdwID  // address of ID for Command
);
```

<span data-ttu-id="84b1a-105">Recupera el identificador de un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="84b1a-105">Retrieves the ID for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="84b1a-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="84b1a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="84b1a-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*</span><span class="sxs-lookup"><span data-stu-id="84b1a-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*</span></span>
</dt> <dd>

<span data-ttu-id="84b1a-108">Dirección de una variable que recibe el identificador de un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="84b1a-108">The address of a variable that receives the ID of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="84b1a-109">Consulte también</span><span class="sxs-lookup"><span data-stu-id="84b1a-109">See Also</span></span>

<span data-ttu-id="84b1a-110">[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md)</span><span class="sxs-lookup"><span data-stu-id="84b1a-110">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::Remove**](iagentcommands--remove.md)</span></span>


 

 