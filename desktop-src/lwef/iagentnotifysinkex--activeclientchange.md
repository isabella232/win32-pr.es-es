---
title: IAgentNotifySinkEx ActiveClientChange
description: IAgentNotifySinkEx ActiveClientChange
ms.assetid: e953e803-c898-4c07-adc0-8b895b5e8473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96988f80d8a1799bf46f12bd38906e9357453f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704673"
---
# <a name="iagentnotifysinkexactiveclientchange"></a>IAgentNotifySinkEx::ActiveClientChange

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT ActiveClientChange(
...long dwCharID,  // character ID
   long lStatus    // active state flag
);
```

Notifica a una aplicación cliente si su cliente activo ya no es el cliente activo de un carácter.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador del carácter para el que cambió el estado de cliente activo.

</dd> <dt>

<span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*
</dt> <dd>

Cambio de estado activo del cliente, que puede ser una combinación de cualquiera de los siguientes valores:



| Value                                                              | Descripción                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| **const unsigned short** **Activate \_ = 0;**<br/>   | El cliente no es el cliente activo del carácter.                |
| **const unsigned short** **Activate \_ Active = 1;**<br/>      | El cliente es el cliente activo del carácter.                    |
| **const unsigned short** **Active \_ INPUTACTIVE = 2;**<br/> | El cliente es de entrada-activo (cliente activo del carácter superior). |



 

</dd> </dl>

Cuando varias aplicaciones cliente comparten el mismo carácter, el cliente activo del carácter recibe la entrada del mouse (por ejemplo, eventos de clic o arrastre de control del agente de Microsoft). Del mismo modo, cuando se muestran varios caracteres, el cliente activo del carácter superior (también conocido como cliente de entrada-activo) recibe los eventos [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

Cuando el cliente activo de un carácter cambia, este evento devuelve el identificador de ese carácter y **es true** si la aplicación se convierte en el cliente activo del carácter o en **false** si ya no es el cliente activo del carácter.

Una aplicación cliente puede recibir este evento cuando el usuario selecciona la entrada de otra aplicación cliente en el menú emergente del carácter o mediante el comando Voice, la aplicación cliente cambia su estado activo u otra aplicación cliente cierra su conexión con Microsoft Agent. El agente envía este evento solo a las aplicaciones cliente que se ven afectadas directamente: aquellas que se convierten en el cliente activo o dejan de ser el cliente activo.

Puede usar el método [**Activate**](iagentcharacter--activate.md) para establecer si la aplicación es el cliente activo del carácter o para que la aplicación sea el cliente activo de entrada (que también hace que el carácter sea más alto).

## <a name="see-also"></a>Consulte también

[**IAgentCharacter:: Activate**](iagentcharacter--activate.md), [**IAgentCharacterEx:: GetActive**](iagentcharacterex--getactive.md), [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md)


 

 





