---
title: IAgentCommands RemoveAll
description: IAgentCommands RemoveAll
ms.assetid: fab43363-6325-4566-b7bb-599591f67321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb855a0eb4cd8a968ec5f03a37aa99fb170158cf75eec9f69a13c392ef94cdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976285"
---
# <a name="iagentcommandsremoveall"></a>IAgentCommands::RemoveAll

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Remove();
```

Quita todos los [**comandos de**](/windows/desktop/lwef/the-command-object) una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

Al quitar todos [**los comandos**](/windows/desktop/lwef/the-command-object) de una colección [**Comandos,**](/windows/desktop/lwef/the-commands-collection-object) también se quitan del menú emergente y de la ventana Comandos **de** voz cuando la aplicación está activa en la entrada. **RemoveAll** no quita las entradas del servidor ni de otros clientes.

## <a name="see-also"></a>Consulte también

[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::Remove**](iagentcommands--remove.md)


 

 