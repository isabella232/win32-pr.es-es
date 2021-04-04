---
title: IAgentCommand SetEnabled
description: IAgentCommand SetEnabled
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8377307d66257f7a9b74ac82512edc6e4ec64034
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077626"
---
# <a name="iagentcommandsetenabled"></a>IAgentCommand:: SetEnabled

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetEnabled(
   long bEnabled  // Enabled setting for Command
);
```

Establece la propiedad [**Enabled**](enabled-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Valor booleano que establece el valor de la configuración [**habilitada**](enabled-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object). **True** habilita el **comando**; **False** lo deshabilita. No se puede seleccionar un **comando** deshabilitado.

</dd> </dl>

Un [**comando**](/windows/desktop/lwef/the-command-object) debe tener la propiedad [**Enabled**](enabled-property.md) establecida en **true** para poder seleccionarse. También debe tener establecida la propiedad [**Caption**](caption-property.md) y su propiedad [**visible**](visible-property.md) establecida en **true** para que aparezca en el menú emergente del carácter. Para que el **comando** aparezca en la **ventana comandos de voz**, debe establecer su propiedad [**Voice**](voice-property.md).

## <a name="see-also"></a>Consulte también

[**IAgentCommand:: GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand:: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 