---
title: IAgentCommands Remove
description: IAgentCommands Remove
ms.assetid: 1f41aa2d-e50b-48a8-87fc-fda4730b035a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5875d1377aecc7e28554bac6aae1ccb2b4f515f730a6ab1b0b3a83cec7573418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477208"
---
# <a name="iagentcommandsremove"></a>IAgentCommands::Remove

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Remove(
   long dwID  // Command ID
);
```

Quita el comando especificado [**de**](/windows/desktop/lwef/the-command-object) una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*
</dt> <dd>

Identificador de un comando [**que se**](/windows/desktop/lwef/the-command-object) quitará de la [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> </dl>

Al quitar un [**comando**](/windows/desktop/lwef/the-command-object) de una colección [**comandos,**](/windows/desktop/lwef/the-commands-collection-object) también se quita del menú emergente y de la ventana Comandos **de** voz cuando la aplicación está activa en la entrada.

## <a name="see-also"></a>Consulte también

[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)


 

 