---
title: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
ms.assetid: 9c8fa978-a02b-4dfc-8cf7-e066c5b75122
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7275bfe28190e06782cb2564dbf4868dd2c096
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420635"
---
# <a name="iagentcommandsexgetglobalvoicecommandsenabled"></a>IAgentCommandsEx::GetGlobalVoiceCommandsEnabled

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetGlobalVoiceCommandsEnabled(
   long * pbEnabled  // address of the global voice command setting
);
```

Recupera si la gramática de voz para los comandos globales del agente está habilitada.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

La dirección que recibe **true** si la gramática de voz para los comandos globales del agente está habilitada, **false** si está deshabilitada.

</dd> </dl>

El agente de Microsoft agrega automáticamente parámetros de voz (gramática) para abrir y cerrar la ventana comandos de voz y para mostrar y ocultar el carácter. Cuando este método devuelve **false**, los parámetros de voz para estos comandos, así como los parámetros de voz para el [**título**](caption-property.md) de los objetos de [**comando**](/windows/desktop/lwef/the-command-object) de otros clientes, no se incluyen en la gramática. Esto le permite eliminarlos de la gramática activa actual del cliente. Sin embargo, esta configuración no refleja la inclusión de estos comandos en el menú emergente del carácter.

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx::SetGlobalVoiceCommandsEnabled**](iagentcommandsex--setglobalvoicecommandsenabled.md)


 

 