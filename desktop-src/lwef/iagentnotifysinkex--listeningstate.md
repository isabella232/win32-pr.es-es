---
title: IAgentNotifySinkEx ListeningState
description: IAgentNotifySinkEx ListeningState
ms.assetid: e303b299-0dd0-419a-87a9-1490fe6cf54a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fee8f931030cbd68cd148fc57360d8b0ccf7624
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532212"
---
# <a name="iagentnotifysinkexlisteningstate"></a>IAgentNotifySinkEx::ListeningState

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT ListeningState(
   long dwCharacterID,  // character ID
   long bListening,     // listening mode state
   long dwCause         // cause  
);
```

Notifica a una aplicación cliente cuando cambia el modo de escucha.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*
</dt> <dd>

Carácter para el que ha cambiado el estado de escucha.

</dd> <dt>

<span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*
</dt> <dd>

Estado del modo de escucha. **True** indica que se ha iniciado el modo de escucha; **False**, el modo de escucha ha finalizado.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

La causa del evento, que puede ser uno de los valores siguientes.



| Value                                                                             | Descripción                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| **const unsigned Long** **LSCOMPLETE \_ causa \_ PROGRAMDISABLED = 1;**<br/>    | El modo de escucha estaba desactivado por el código del programa.                                 |
| **const unsigned Long** **LSCOMPLETE \_ causa \_ PROGRAMTIMEDOUT = 2;**<br/>    | Se agotó el tiempo de espera para el modo de escucha (activado por el código del programa).                          |
| **const unsigned Long** **LSCOMPLETE \_ causa \_ USERTIMEDOUT = 3;**<br/>       | Se agotó el tiempo de espera para el modo de escucha (activado por la clave de escucha).                     |
| **const unsigned Long** **LSCOMPLETE \_ causa \_ USERRELEASEDKEY = 4;**<br/>    | El modo de escucha estaba desactivado porque el usuario liberó la clave de escucha.     |
| **const unsigned Long** **LSCOMPLETE \_ causa \_ USERUTTERANCEENDED = 5;**<br/> | El modo de escucha estaba desactivado porque el usuario terminó de hablar.              |
| **const unsigned Long** **LSCOMPLETE \_ causa \_ CLIENTDEACTIVATED = 6;**<br/>  | El modo de escucha estaba desactivado porque se desactivó el cliente activo de entrada. |
| **const unsigned Long** **LSCOMPLETE \_ causa \_ DEFAULTCHARCHANGE = 7**<br/>   | El modo de escucha estaba desactivado porque se cambió el carácter predeterminado.       |
| **const unsigned Long** **LSCOMPLETE \_ causa \_ USERDISABLED = 8**<br/>        | El modo de escucha estaba desactivado porque el usuario deshabilitó la entrada de voz.          |



 

</dd> </dl>

Este evento se envía a todos los clientes cuando el modo de escucha comienza después de que el usuario presione la tecla de escucha o cuando finalice el tiempo de espera, o cuando el cliente de entrada-activo llame al método [**IAgentCharacterEx:: Listen**](iagentcharacterex--listen.md) con **true** o **false**.

El evento devuelve valores a los clientes que actualmente tienen este carácter cargado. El resto de clientes reciben un carácter nulo (cadena vacía).

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx:: Listen**](iagentcharacterex--listen.md)


 

 





