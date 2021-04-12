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
# <a name="iagentcommandsremove"></a>IAgentCommands:: Remove

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Remove(
   long dwID  // Command ID
);
```

Quita el [**comando**](/windows/desktop/lwef/the-command-object) especificado de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*
</dt> <dd>

IDENTIFICADOR de un [**comando**](/windows/desktop/lwef/the-command-object) que se va a quitar de la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

Quitar un [**comando**](/windows/desktop/lwef/the-command-object) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) también lo quita del menú emergente y de la **ventana comandos de voz** cuando la aplicación es de entrada-activa.

## <a name="see-also"></a>Consulte también

[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommands:: RemoveAll**](iagentcommands--removeall.md)


 

 