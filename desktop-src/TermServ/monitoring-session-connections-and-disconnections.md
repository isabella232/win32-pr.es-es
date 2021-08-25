---
title: Supervisión de conexiones y desconexiones de sesión
description: Para registrar una aplicación con Servicios de Escritorio remoto, almacene el nombre de la aplicación de servidor de canal virtual en el Registro agregando una subclave.
ms.assetid: 8524cb7a-a930-431a-bc5f-b0793781de15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2813399650d535d10864f384afb6b745fb9e50039f2b981df61ceb2e6452a608
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989105"
---
# <a name="monitoring-session-connections-and-disconnections"></a>Supervisión de conexiones y desconexiones de sesión

Para que una aplicación de servicio, como una aplicación de servidor de canal virtual, supervise las conexiones y desconexiones de sesión, debe registrarla con Servicios de Escritorio remoto. Para registrar la aplicación con Servicios de Escritorio remoto, almacene el nombre de la aplicación de servidor de canal virtual en el Registro agregando una subclave en la siguiente ubicación:

**HKEY \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **TerminalServer** \\ **Addins**

La subclave puede tener cualquier nombre. Debe tener un **valor \_ REG SZ,** **Name**, que contenga el nombre simbólico de la aplicación.

``` syntax
Name = AddinName
```

La longitud máxima de la subclave y el valor de **Name** es de 99 caracteres.

La subclave también debe tener **un valor \_ REG DWORD** que indique el tipo de aplicación de servidor.

``` syntax
Type = AddinType
```

*AddinType* debe ser el siguiente valor.



| Value | Significado                               |
|-------|---------------------------------------|
| 3     | Aplicación en modo de usuario, espacio de sesión. |



 

El registro de la aplicación de servicio solo tiene efecto en las sesiones creadas después de realizar el registro.

Para cada aplicación de servicio registrada, Servicios de Escritorio remoto señalará un conjunto de objetos de evento cuando un cliente se conecta o se desconecta de la sesión. Cada complemento de canal virtual debe registrarse y crear los eventos de notificación mediante una llamada [**a CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa). Los nombres de estos objetos de evento cumplen el formato siguiente.

``` syntax
AddinName-Reconnect

AddinName-Disconnect
```

*AddinName es* la cadena especificada en el valor **Nombre** de la subclave del Registro con la que se registra la aplicación de servidor. La creación de estos eventos en una sesión hace que se creen en un directorio de eventos especial por sesión. El directorio de eventos proporciona mayor seguridad al impedir que las aplicaciones de otras sesiones modifiquen el estado de estos eventos.

Para controlar si se reciben eventos RECONNECT y DISCONNECT en el servidor, puede colocar la **marca RemoteControlPersistent** en el Registro bajo la siguiente clave:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **TerminalServer** \\ **Addinname** \\ 

La marca habilita o deshabilita la señalización de los eventos RECONNECT y DISCONNECT cuando se inicia o se detiene una sesión de cliente. La sintaxis del **valor \_ REG DWORD** es la siguiente.

``` syntax
RemoteControlPersistent = flag
```

El valor de *flag* puede ser uno o cero. Cero es el valor predeterminado. Si se establece en uno, no se notificará a la aplicación de servicio si la sesión de cliente se inicia o se detiene. Si se establece en cero, se señala un evento RECONNECT cuando se inicia la sesión de cliente y se señala un evento DISCONNECT cuando se detiene la sesión del cliente.

El formato de nombre de objeto de evento anterior todavía se admite en Windows Server 2008 por compatibilidad con versiones anteriores. Se recomienda usar el formato Windows Server 2008 más reciente porque es más seguro.

El formato de evento anterior es el siguiente.

``` syntax
Global\AddinName-SessionId-Reconnect
 
Global\AddinName-SessionId-Disconnect
```

*AddinName es* la cadena especificada en el valor **Nombre** de la subclave del Registro con la que se registra la aplicación de servidor. *SessionId es* el identificador de sesión de una sesión de cliente.

 

 