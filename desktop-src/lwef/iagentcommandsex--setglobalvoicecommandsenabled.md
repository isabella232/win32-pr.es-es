---
title: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
ms.assetid: f456b1d3-60aa-4b90-90d0-6c695947fa8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87a576a36d3df4b3ddf0ca71f5709a712a3c9e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149234"
---
# <a name="iagentcommandsexsetglobalvoicecommandsenabled"></a>IAgentCommandsEx::SetGlobalVoiceCommandsEnabled

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetGlobalVoiceCommandsEnabled(
 long bEnable  // Enabled setting for Agent's global voice commands
);
```

Establece la propiedad [**habilitada**](enabled-property.md) para la gramática de voz de los comandos globales de Microsoft Agent.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*bEnable*
</dt> <dd>

Valor booleano que establece si está habilitada la gramática de voz de los comandos globales del agente. **True** habilita la gramática de voz; **False** lo deshabilita.

</dd> </dl>

El agente de Microsoft agrega automáticamente parámetros de voz (gramática) para abrir y cerrar la ventana comandos de voz y para mostrar y ocultar el carácter. Cuando se establece en **false**, el agente deshabilita los parámetros de voz para estos comandos, así como los parámetros de voz para el [**título**](caption-property.md) de los objetos de [**comando**](/windows/desktop/lwef/the-command-object) de otros clientes. Esto le permite eliminarlos de la gramática activa actual del cliente. Sin embargo, dado que esto potencialmente bloquea el acceso de voz a otros clientes, restablezca esta propiedad en **true** después de procesar la entrada de voz del usuario.

Deshabilitar la propiedad no afecta al menú emergente del carácter. Los comandos globales agregados por el servidor seguirán apareciendo. No se pueden quitar del menú emergente.

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx::GetGlobalVoiceCommandsEnabled**](iagentcommandsex--getglobalvoicecommandsenabled.md)


 

 