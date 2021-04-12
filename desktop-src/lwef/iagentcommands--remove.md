---
title: Quitar IAgentCommands
description: Quitar IAgentCommands
ms.assetid: 1f41aa2d-e50b-48a8-87fc-fda4730b035a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0c3321de3d06b5e2ebea873a4bace91482d8c5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104270963"
---
# <a name="iagentcommandsremove"></a><span data-ttu-id="874cb-103">IAgentCommands:: Remove</span><span class="sxs-lookup"><span data-stu-id="874cb-103">IAgentCommands::Remove</span></span>

<span data-ttu-id="874cb-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="874cb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Remove(
   long dwID  // Command ID
);
```

<span data-ttu-id="874cb-105">Quita el [**comando**](/windows/desktop/lwef/the-command-object) especificado de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="874cb-105">Removes the specified [**Command**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="874cb-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="874cb-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="874cb-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span><span class="sxs-lookup"><span data-stu-id="874cb-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span></span>
</dt> <dd>

<span data-ttu-id="874cb-108">IDENTIFICADOR de un [**comando**](/windows/desktop/lwef/the-command-object) que se va a quitar de la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="874cb-108">The ID of a [**Command**](/windows/desktop/lwef/the-command-object) to remove from the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

<span data-ttu-id="874cb-109">Quitar un [**comando**](/windows/desktop/lwef/the-command-object) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) también lo quita del menú emergente y de la **ventana comandos de voz** cuando la aplicación es de entrada-activa.</span><span class="sxs-lookup"><span data-stu-id="874cb-109">Removing a [**Command**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection also removes it from the pop-up menu and the **Voice Commands Window** when your application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="874cb-110">Consulte también</span><span class="sxs-lookup"><span data-stu-id="874cb-110">See Also</span></span>

<span data-ttu-id="874cb-111">[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommands:: RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="874cb-111">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 