---
title: Interrupción IAgentCharacter
description: Interrupción IAgentCharacter
ms.assetid: ae05d317-e2d9-4d11-a6df-f9b25e43467a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c9f19f716b15a48ec3cdb064aa4c0fdbbd1774
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995118"
---
# <a name="iagentcharacterinterrupt"></a>IAgentCharacter:: Interrupt

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Interrupt(
   long dwReqID,    // request ID to interrupt
   long * pdwReqID  // address of request ID
);
```

Interrumpe la animación especificada (solicitud) de otro carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente. Cuando la función devuelve, *pdwReqID* contiene el identificador de la solicitud.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

IDENTIFICADOR de la solicitud que se va a interrumpir.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador de la solicitud de **interrupción** .

</dd> </dl>

Si carga varios caracteres, puede utilizar este método para sincronizar la animación entre los caracteres. Por ejemplo, si hay otro carácter en una animación de bucle, este método detendrá la animación en bucle e iniciará la siguiente animación en la cola del carácter.

La **interrupción** detiene la animación existente, pero no vacía la cola de animaciones del carácter. Inicia la siguiente animación en la cola del carácter. Para detener y vaciar la cola de un carácter, utilice el método [**Stop**](/windows/desktop/lwef/iagentcharacter--stop) .

No puede usar este método para tener una interrupción de carácter en sí porque el servidor de agente de Microsoft pone en cola el método de **interrupción** en la cola de animaciones del carácter. Por lo tanto, solo puede usar la **interrupción** para detener la animación de otro carácter que haya cargado.

 

 