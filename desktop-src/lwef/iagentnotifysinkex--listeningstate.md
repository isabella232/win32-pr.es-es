---
title: IAgentNotifySinkEx ListeningState
description: IAgentNotifySinkEx ListeningState
ms.assetid: e303b299-0dd0-419a-87a9-1490fe6cf54a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21d3926741f83f66ab6133874ec47783976c0ddb6d3fbd2ee91c6e584813147a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692611"
---
# <a name="iagentnotifysinkexlisteningstate"></a>IAgentNotifySinkEx::ListeningState

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT ListeningState(
   long dwCharacterID,  // character ID
   long bListening,     // listening mode state
   long dwCause         // cause  
);
```

Notifica a una aplicación cliente cuándo cambia el modo de escucha.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*
</dt> <dd>

Carácter para el que ha cambiado el estado de escucha.

</dd> <dt>

<span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*
</dt> <dd>

Estado del modo de escucha. **True** indica que se ha iniciado el modo de escucha; **False**, que ha finalizado el modo de escucha.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

La causa del evento, que puede ser uno de los siguientes valores.



| Valor                                                                             | Descripción                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ PROGRAMDISABLED = 1;**<br/>    | El código del programa ha desactivado el modo de escucha.                                 |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ PROGRAMTIMEDOUT = 2;**<br/>    | Se ha pasado el tiempo de espera del modo de escucha (activado por el código del programa).                          |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ USERTIMEDOUT = 3;**<br/>       | Se ha pasado el tiempo de espera del modo de escucha (activado por la clave de escucha).                     |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ USERRELEASEDKEY = 4;**<br/>    | El modo de escucha se ha desactivado porque el usuario ha liberado la clave de escucha.     |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ USERUTTESEGUROENDED = 5;**<br/> | El modo de escucha se ha desactivado porque el usuario ha terminado de hablar.              |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ CLIENTDEACTIVATED = 6;**<br/>  | El modo de escucha se desactivó porque se desactivó el cliente activo de entrada. |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ DEFAULTCHARCHANGE = 7**<br/>   | El modo de escucha se ha desactivado porque se ha cambiado el carácter predeterminado.       |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ USERDISABLED = 8**<br/>        | El modo de escucha se desactivó porque el usuario deshabilitó la entrada de voz.          |



 

</dd> </dl>

Este evento se envía a todos los clientes cuando el modo de escucha comienza después de que el usuario presiona la tecla Listening o cuando finaliza el tiempo de espera, o cuando el cliente activo de entrada llama al método [**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md) con **True** o **False.**

El evento devuelve valores a los clientes que tienen cargado actualmente este carácter. Todos los demás clientes reciben un carácter nulo (cadena vacía).

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md)


 

 





