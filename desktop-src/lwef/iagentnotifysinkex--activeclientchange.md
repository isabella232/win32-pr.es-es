---
title: IAgentNotifySinkEx ActiveClientChange
description: IAgentNotifySinkEx ActiveClientChange
ms.assetid: e953e803-c898-4c07-adc0-8b895b5e8473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50549c4b091a39614fd7ff6b15af0bc1436113dfd2e9b3d31ca86e6995a0e94d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961505"
---
# <a name="iagentnotifysinkexactiveclientchange"></a>IAgentNotifySinkEx::ActiveClientChange

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

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

Identificador del carácter para el que ha cambiado el estado de cliente activo.

</dd> <dt>

<span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*
</dt> <dd>

Cambio de estado activo del cliente, que puede ser una combinación de cualquiera de los valores siguientes:



| Value                                                              | Descripción                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| **const unsigned short** **ACTIVATE \_ NOTACTIVE = 0;**<br/>   | El cliente no es el cliente activo del carácter.                |
| **const unsigned short** **ACTIVATE ACTIVE = \_ 1;**<br/>      | El cliente es el cliente activo del carácter.                    |
| **const unsigned short** **ACTIVATE \_ INPUTACTIVE = 2;**<br/> | El cliente está activo de entrada (cliente activo del carácter superior). |



 

</dd> </dl>

Cuando varias aplicaciones cliente comparten el mismo carácter, el cliente activo del carácter recibe la entrada del mouse (por ejemplo, eventos de clic o arrastre del control de Microsoft Agent). De forma similar, cuando se muestran varios caracteres, el cliente activo del carácter superior (también conocido como cliente activo de entrada) recibe eventos [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

Cuando cambia el cliente activo de un carácter, este evento devuelve el identificador de ese carácter y **True** si la aplicación se ha convertido en el cliente activo del carácter o **False** si ya no es el cliente activo del carácter.

Una aplicación cliente puede recibir este evento cuando el usuario selecciona la entrada de otra aplicación cliente en el menú emergente del carácter o mediante un comando de voz, la aplicación cliente cambia su estado activo u otra aplicación cliente cierra su conexión a Microsoft Agent. El agente envía este evento solo a las aplicaciones cliente que se ven directamente afectadas,aquellas que se convierten en el cliente activo o dejan de ser el cliente activo.

Puede usar el método [**Activate**](iagentcharacter--activate.md) para establecer si la aplicación es el cliente activo del carácter o para convertir la aplicación en el cliente activo de entrada (lo que también hace que el carácter sea el más alto).

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [**IAgentCharacterEx::GetActive**](iagentcharacterex--getactive.md), [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md)


 

 





