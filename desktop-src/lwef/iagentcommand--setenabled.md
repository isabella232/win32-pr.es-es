---
title: IAgentCommand SetEnabled
description: IAgentCommand SetEnabled
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da164b6603d93496e3381ccc6938a3b6d8f520bcea887cfd11f031cec7d845a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976315"
---
# <a name="iagentcommandsetenabled"></a>IAgentCommand::SetEnabled

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetEnabled(
   long bEnabled  // Enabled setting for Command
);
```

Establece la [**propiedad Enabled**](enabled-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Valor booleano que establece el valor de la [**configuración Habilitado**](enabled-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object). **True** habilita el **comando**; **False** lo deshabilita. No se **puede seleccionar un** comando deshabilitado.

</dd> </dl>

Un [**comando**](/windows/desktop/lwef/the-command-object) debe tener su [**propiedad Enabled**](enabled-property.md) establecida en **True** para poder seleccionarse. También debe tener su propiedad [**Caption**](caption-property.md) establecida y [**su propiedad Visible**](visible-property.md) establecida en **True** para que aparezca en el menú emergente del carácter. Para que el **comando aparezca** en la ventana Comandos **de voz**, debe establecer su [**propiedad**](voice-property.md)Voz.

## <a name="see-also"></a>Consulte también

[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 