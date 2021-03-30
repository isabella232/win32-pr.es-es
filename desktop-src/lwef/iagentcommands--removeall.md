---
title: IAgentCommands RemoveAll
description: IAgentCommands RemoveAll
ms.assetid: fab43363-6325-4566-b7bb-599591f67321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bd374b7c5767c416d2c3bb2281e651ba71acd8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791428"
---
# <a name="iagentcommandsremoveall"></a><span data-ttu-id="0114a-103">IAgentCommands:: RemoveAll</span><span class="sxs-lookup"><span data-stu-id="0114a-103">IAgentCommands::RemoveAll</span></span>

<span data-ttu-id="0114a-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0114a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Remove();
```

<span data-ttu-id="0114a-105">Quita todos los [**comandos**](/windows/desktop/lwef/the-command-object) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="0114a-105">Removes all [**Commands**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="0114a-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0114a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<span data-ttu-id="0114a-107">Al quitar todos los [**comandos**](/windows/desktop/lwef/the-command-object) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) , también se quitan del menú emergente y de la **ventana comandos de voz** cuando la aplicación es de entrada-activa.</span><span class="sxs-lookup"><span data-stu-id="0114a-107">Removing all [**Commands**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection also removes them from the pop-up menu and the **Voice Commands Window** when your application is input-active.</span></span> <span data-ttu-id="0114a-108">**RemoveAll** no quita las entradas de servidor ni de otro cliente.</span><span class="sxs-lookup"><span data-stu-id="0114a-108">**RemoveAll** does not remove server or other client's entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="0114a-109">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0114a-109">See Also</span></span>

<span data-ttu-id="0114a-110">[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md)</span><span class="sxs-lookup"><span data-stu-id="0114a-110">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::Remove**](iagentcommands--remove.md)</span></span>


 

 