---
title: Supervisión de conexiones y desconexiones de sesión
description: Para registrar una aplicación con Servicios de Escritorio remoto, almacene el nombre de la aplicación de servidor de canal virtual en el registro mediante la adición de una subclave.
ms.assetid: 8524cb7a-a930-431a-bc5f-b0793781de15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e819b13594ecec14a2b425560152cadedd4e9122
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077856"
---
# <a name="monitoring-session-connections-and-disconnections"></a>Supervisión de conexiones y desconexiones de sesión

Para una aplicación de servicio, como una aplicación de servidor de canal virtual, para supervisar las conexiones y desconexiones de la sesión, debe registrarla con Servicios de Escritorio remoto. Para registrar la aplicación con Servicios de Escritorio remoto, almacene el nombre de la aplicación de servidor de canal virtual en el registro agregando una subclave en la siguiente ubicación:

**HKEY \_ \_Equipo local** \\ **System** \\ **CurrentControlSet** \\ **control** \\ **TerminalServer** \\ **AddIns**

La subclave puede tener cualquier nombre. Debe tener un valor **reg \_ SZ** , **Name**, que contiene el nombre simbólico de la aplicación.

``` syntax
Name = AddinName
```

La longitud máxima de la subclave y del valor de **Name** es de 99 caracteres.

La subclave también debe tener un valor de **Registro \_ DWORD** que indique el tipo de aplicación de servidor.

``` syntax
Type = AddinType
```

*AddinType* debe ser el siguiente valor.



| Value | Significado                               |
|-------|---------------------------------------|
| 3     | Aplicación de modo de usuario, espacio de sesión. |



 

El registro de la aplicación de servicio solo surte efecto en las sesiones creadas después de realizar el registro.

Para cada aplicación de servicio registrada, Servicios de Escritorio remoto señalará un conjunto de objetos de eventos cuando un cliente se conecta o desconecta de la sesión. Cada complemento de canal virtual debe registrarse y crear los eventos de notificación llamando a [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa). Los nombres de estos objetos de evento se ajustan al formato siguiente.

``` syntax
AddinName-Reconnect

AddinName-Disconnect
```

*AddinName* es la cadena especificada en el valor de **nombre** de la subclave del registro en la que se registra la aplicación de servidor. Al crear estos eventos en una sesión, se crean en un directorio de eventos especial por sesión. El directorio de eventos proporciona seguridad adicional al impedir que las aplicaciones de otras sesiones modifiquen el estado de estos eventos.

Para controlar si se reciben los eventos de reconexión y de desconexión en el servidor, puede colocar la marca **RemoteControlPersistent** en el registro con la siguiente clave:

**HKEY \_ \_Equipo local** \\ **System** \\ **CurrentControlSet** \\ **control** \\ **TerminalServer** \\ **AddIns** \\ *addinname*

La marca habilita o deshabilita la señalización de los eventos de reconexión y desconexión cuando se inicia o se detiene una sesión de cliente. La sintaxis del valor de **reg \_ DWORD** es la siguiente.

``` syntax
RemoteControlPersistent = flag
```

El valor de *Flag* puede ser uno o cero. Cero es el valor predeterminado. Si se establece en uno, no se notificará a la aplicación de servicio si la sesión del cliente se inicia o se detiene. Si se establece en cero, se señalará un evento de reconexión cuando se inicie la sesión del cliente y se señalará un evento de desconexión cuando se detenga la sesión del cliente.

Todavía se admite el formato de nombre de objeto de evento anterior en Windows Server 2008 para mantener la compatibilidad con versiones anteriores. Se recomienda usar el formato más reciente de Windows Server 2008 porque es más seguro.

El formato de evento anterior es el siguiente.

``` syntax
Global\AddinName-SessionId-Reconnect
 
Global\AddinName-SessionId-Disconnect
```

*AddinName* es la cadena especificada en el valor de **nombre** de la subclave del registro en la que se registra la aplicación de servidor. *SessionID* es el identificador de sesión de una sesión de cliente.

 

 