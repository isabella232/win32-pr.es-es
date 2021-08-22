---
title: Interrupción de IAgentCharacter
description: Interrupción de IAgentCharacter
ms.assetid: ae05d317-e2d9-4d11-a6df-f9b25e43467a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64ea2529d4da78607d3ad22bf688857c8917e3317df17ae9a5eb99d0b184878e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750910"
---
# <a name="iagentcharacterinterrupt"></a>IAgentCharacter::Interrupt

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Interrupt(
   long dwReqID,    // request ID to interrupt
   long * pdwReqID  // address of request ID
);
```

Interrumpe la animación especificada (solicitud) de otro carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente. Cuando la función devuelve un resultado, *pdwReqID* contiene el identificador de la solicitud.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

Identificador de la solicitud que se interrumpirá.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador **de solicitud** de interrupción.

</dd> </dl>

Si carga varios caracteres, puede usar este método para sincronizar la animación entre caracteres. Por ejemplo, si otro carácter está en una animación de bucle, este método detendrá la animación de bucle e iniciará la animación siguiente en la cola del carácter.

**La** interrupción detiene la animación existente, pero no vacía la cola de animación del carácter. Inicia la siguiente animación en la cola del carácter. Para detener y vaciar la cola de un carácter, use el [**método Stop.**](/windows/desktop/lwef/iagentcharacter--stop)

No puede usar este método para que un carácter se interrumpa a sí mismo porque el servidor del Agente Microsoft pone en cola el método **Interrupt** en la cola de animación del carácter. Por lo tanto, solo puede usar **Interrumpir para** detener la animación de otro carácter que haya cargado.

 

 