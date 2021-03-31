---
title: IAgentCommands GetCommand
description: IAgentCommands GetCommand
ms.assetid: 0f4a9152-d5dc-4045-b469-8a03f0369e34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e81043bb8dbe8a6d050f226d09f03b396d0f8f9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077743"
---
# <a name="iagentcommandsgetcommand"></a><span data-ttu-id="fa4af-103">IAgentCommands::GetCommand</span><span class="sxs-lookup"><span data-stu-id="fa4af-103">IAgentCommands::GetCommand</span></span>

<span data-ttu-id="fa4af-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fa4af-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCommand(
   long dwCommandID,         // Command ID
   IUnknown ** ppunkCommand  // address of IUnknown interface
);                    
```

<span data-ttu-id="fa4af-105">Recupera un objeto [**Command**](/windows/desktop/lwef/the-command-object) de la colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="fa4af-105">Retrieves a [**Command**](/windows/desktop/lwef/the-command-object) object from the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="fa4af-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="fa4af-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="fa4af-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span><span class="sxs-lookup"><span data-stu-id="fa4af-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="fa4af-108">IDENTIFICADOR de un objeto de [**comando**](/windows/desktop/lwef/the-command-object) en la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="fa4af-108">The ID of a [**Command**](/windows/desktop/lwef/the-command-object) object in the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="fa4af-109"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span><span class="sxs-lookup"><span data-stu-id="fa4af-109"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span></span>
</dt> <dd>

<span data-ttu-id="fa4af-110">Dirección de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) para el objeto de [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="fa4af-110">The address of the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="fa4af-111">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fa4af-111">See Also</span></span>

[<span data-ttu-id="fa4af-112">**IAgentCommand**</span><span class="sxs-lookup"><span data-stu-id="fa4af-112">**IAgentCommand**</span></span>](iagentcommand.md)


 

 