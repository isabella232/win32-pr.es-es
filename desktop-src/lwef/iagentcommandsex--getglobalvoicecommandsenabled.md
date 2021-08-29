---
title: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
ms.assetid: 9c8fa978-a02b-4dfc-8cf7-e066c5b75122
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28aee044b9b25ff529a8c49943b6fd0bbb4d8175a5f3a9b6d482923170f4bdc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609495"
---
# <a name="iagentcommandsexgetglobalvoicecommandsenabled"></a>IAgentCommandsEx::GetGlobalVoiceCommandsEnabled

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetGlobalVoiceCommandsEnabled(
   long * pbEnabled  // address of the global voice command setting
);
```

Recupera si la gramática de voz de los comandos globales del Agente está habilitada.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Dirección que recibe **True si** la gramática de voz de los comandos globales del Agente está habilitada, **False** si está deshabilitada.

</dd> </dl>

Microsoft Agent agrega automáticamente parámetros de voz (gramática) para abrir y cerrar la ventana Comandos de voz y para mostrar y ocultar el carácter. Cuando este método devuelve **False**, los parámetros de voz de [](caption-property.md) estos comandos, así como los parámetros de voz para el título de los objetos [**Command**](/windows/desktop/lwef/the-command-object) de otros clientes, no se incluyen en la gramática. Esto le permite eliminarlos de la gramática activa actual del cliente. Sin embargo, esta configuración no refleja la inclusión de estos comandos en el menú emergente del carácter.

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx::SetGlobalVoiceCommandsEnabled**](iagentcommandsex--setglobalvoicecommandsenabled.md)


 

 