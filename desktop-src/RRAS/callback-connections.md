---
title: Conexiones de devolución de llamada
description: RAS admite conexiones en las que el servidor remoto se cuelga y, a continuación, vuelve a llamar al cliente para establecer la conexión.
ms.assetid: 25f0e84d-8900-4efe-b07d-59f25186c976
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9aabe3bf5503f16d7d27e44e02dc19ccb2a6f2e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793516"
---
# <a name="callback-connections"></a>Conexiones de devolución de llamada

RAS admite conexiones en las que el servidor remoto se cuelga y, a continuación, vuelve a llamar al cliente para establecer la conexión.

Para cada usuario que se puede conectar a un servidor RAS, el servidor almacena un atributo de devolución de llamada que controla cómo se realiza la conexión. El atributo predeterminado es sin devolución de llamada, lo que significa que el usuario puede conectarse al servidor RAS sin una devolución de llamada. Como alternativa, el administrador del servidor RAS puede asignar a un usuario el atributo de devolución de llamada preestablecido o establecido por el llamador.

Para un usuario que tenga asignada la restricción preestablecida, el administrador especifica un número de teléfono al que el servidor RAS debe volver a llamar para establecer una conexión. El usuario no puede especificar un número diferente y no se puede establecer la conexión sin una devolución de llamada.

El administrador de conexiones de acceso remoto y el servidor remoto controlan automáticamente una operación de devolución de llamada preestablecida. No es necesario que la aplicación cliente RAS haga nada más que proporcionar comentarios al usuario cuando se llama al controlador de notificación durante los distintos Estados de la operación de devolución de llamada.

Un usuario al que se ha asignado el privilegio Set by Caller puede elegir conectarse con o sin devolución de llamada. La llamada [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) usa el miembro **szCallbackNumber** de la estructura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) para indicar la elección.

El miembro **szCallbackNumber** puede simplemente especificar el número de devolución de llamada; o bien, para establecer la conexión sin una devolución de llamada, **szCallbackNumber** puede apuntar a una cadena vacía, "". En cualquiera de estos casos, el administrador de conexiones de acceso remoto controla la operación de conexión automáticamente. Al igual que con una operación de devolución de llamada preestablecida, el cliente RAS no necesita realizar ninguna acción que no sea para proporcionar comentarios al usuario.

Si la llamada [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) habilita [los Estados en pausa](paused-states.md), **szCallbackNumber** puede apuntar a una cadena de asterisco, " \* ", para indicar que la operación de conexión debe entrar en pausa para permitir que el usuario escriba en el número de devolución de llamada. En este caso, la operación de conexión para un establecido por el usuario que realiza la llamada entra en un estado de pausa después de que el servidor remoto haya autenticado al usuario. Durante el estado de pausa, el cliente RAS obtiene la entrada del número de devolución de llamada del usuario. Después, el cliente reanuda la operación de conexión realizando una segunda llamada **rasdial** en la que **szCallbackNumber** especifica el número proporcionado por el usuario.

> [!Note]  
> Si los Estados pausados no están habilitados, hay un significado diferente cuando **szCallbackNumber** apunta a una cadena de asterisco, " \* ". En este caso, el asterisco indica que el número de devolución de llamada se almacena en el archivo de libreta de teléfonos especificado por la llamada [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) .

 

En el caso de una devolución de llamada, la llamada a [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) no devuelve hasta después de que el servidor haya llamado de nuevo al cliente.

 

 