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
# <a name="iagentcommandsgetcommand"></a>IAgentCommands::GetCommand

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetCommand(
   long dwCommandID,         // Command ID
   IUnknown ** ppunkCommand  // address of IUnknown interface
);                    
```

Recupera un objeto [**Command**](/windows/desktop/lwef/the-command-object) de la colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

IDENTIFICADOR de un objeto de [**comando**](/windows/desktop/lwef/the-command-object) en la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

Dirección de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) para el objeto de [**comando**](/windows/desktop/lwef/the-command-object) .

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCommand**](iagentcommand.md)


 

 