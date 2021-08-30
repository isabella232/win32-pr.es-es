---
title: Conexiones de devolución de llamada
description: RAS admite conexiones en las que el servidor remoto se mantiene y, a continuación, vuelve a llamar al cliente para establecer la conexión.
ms.assetid: 25f0e84d-8900-4efe-b07d-59f25186c976
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b72d10285c6920befe7a508bf69ef1e5d21c19e8632534f94dd8ccb9a0ed1743
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030435"
---
# <a name="callback-connections"></a>Conexiones de devolución de llamada

RAS admite conexiones en las que el servidor remoto se mantiene y, a continuación, vuelve a llamar al cliente para establecer la conexión.

Para cada usuario que pueda conectarse a un servidor RAS, el servidor almacena un atributo de devolución de llamada que controla cómo se realiza la conexión. El atributo predeterminado es Sin devolución de llamada, lo que significa que el usuario puede conectarse al servidor RAS sin una devolución de llamada. Como alternativa, el administrador del servidor RAS puede asignar a un usuario el atributo de devolución de llamada Preset o Set-By-Caller.

Para un usuario al que se le asignó la restricción Preestablecido, el administrador especifica un número de teléfono al que el servidor RAS debe llamar para establecer una conexión. El usuario no puede especificar un número diferente y la conexión no se puede realizar sin una devolución de llamada.

El acceso remoto y el servidor remoto controlan automáticamente una operación de devolución de llamada Connection Manager preestablecida. La aplicación cliente RAS no necesita hacer nada más que proporcionar comentarios al usuario cuando se llama al controlador de notificaciones durante los distintos estados de la operación de devolución de llamada.

Un usuario asignado al privilegio Establecer por llamador puede elegir conectarse con o sin una devolución de llamada. La [**llamada RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) usa el **miembro szCallbackNumber** de la [**estructura RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) para indicar la elección.

El **miembro szCallbackNumber** puede especificar simplemente el número de devolución de llamada; o bien, para establecer la conexión sin una devolución de llamada, **szCallbackNumber** puede apuntar a una cadena vacía, "". En cualquiera de estos casos, el administrador de acceso Connection Manager controla automáticamente la operación de conexión. Al igual que con una operación de devolución de llamada preestablecida, el cliente RAS no necesita realizar ninguna acción que no sea proporcionar comentarios al usuario.

Si la llamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) habilita los estados en pausa [,](paused-states.md) **szCallbackNumber** puede apuntar a una cadena de asterisco, "", para indicar que la operación de conexión debe entrar en un estado en pausa para permitir que el usuario escriba el número de devolución de \* llamada. En este caso, la operación de conexión para un usuario Establecido por llamador entra en un estado en pausa después de que el servidor remoto haya autenticado al usuario. Durante el estado en pausa, el cliente RAS obtiene la entrada del número de devolución de llamada del usuario. A continuación, el cliente reanuda la operación de conexión realizando una segunda llamada **RasDial** en la que **szCallbackNumber** especifica el número proporcionado por el usuario.

> [!Note]  
> Si los estados en pausa no están habilitados, hay un significado diferente cuando **szCallbackNumber** apunta a una cadena de asterisco, " \* ". En este caso, el asterisco indica que el número de devolución de llamada se almacena en el archivo de la libreta de teléfonos especificado por la [**llamada RasDial.**](/windows/desktop/api/Ras/nf-ras-rasdiala)

 

En el caso de una devolución de llamada, la llamada a [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) no se devuelve hasta después de que el servidor haya llamado de nuevo al cliente.

 

 