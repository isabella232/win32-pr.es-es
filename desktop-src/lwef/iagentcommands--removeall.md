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
# <a name="iagentcommandsremoveall"></a>IAgentCommands:: RemoveAll

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Remove();
```

Quita todos los [**comandos**](/windows/desktop/lwef/the-command-object) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

Al quitar todos los [**comandos**](/windows/desktop/lwef/the-command-object) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) , también se quitan del menú emergente y de la **ventana comandos de voz** cuando la aplicación es de entrada-activa. **RemoveAll** no quita las entradas de servidor ni de otro cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md)


 

 