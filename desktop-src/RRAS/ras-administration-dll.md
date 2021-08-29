---
title: Acerca de los archivos DLL de administración de RAS
description: El archivo DLL de administración de RAS exporta funciones a las que el servidor RAS llama cada vez que un usuario intenta conectarse o desconectarse.
ms.assetid: c15c6e2d-3bb6-4583-9ac3-19528feb863f
keywords:
- RAS Administration RRAS , RAS administration DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59b6682a3ba16d5d96a0a6eb03cbe877d130b819c5054174388e4fe89764957f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036385"
---
# <a name="about-ras-administration-dlls"></a>Acerca de los archivos DLL de administración de RAS

El archivo DLL de administración de RAS exporta funciones a las que el servidor RAS llama cada vez que un usuario intenta conectarse o desconectarse. Estos son algunos de los usos posibles de un archivo DLL de administración de RAS:

-   Decida si desea permitir que un usuario se conecte al servidor. El archivo DLL de administración puede proporcionar una comprobación de seguridad además de la autenticación de usuario RAS estándar.
-   Registre la hora a la que cada usuario se conecta y se desconecta del servidor. Esto puede ser útil para fines de facturación o auditoría.
-   Asigne una dirección IP a cada usuario. Esto resulta útil para la seguridad, ya que esta característica se usa para asignar la conexión de un usuario a un equipo específico.

La ubicación del archivo DLL de administración de RAS se especifica en el Registro; vea [Instalación del Registro DE DLL de administración de RAS.](ras-administration-dll-registry-setup.md)

RAS admite varios archivos DLL de administración. El registro admite varias ubicaciones dll. RAS llama a las funciones de los archivos DLL en el orden en que se enumeran los archivos DLL en el Registro; vea [Instalación del Registro DE DLL de administración de RAS.](ras-administration-dll-registry-setup.md)

**Windows 2000 Server:** RAS no admite varios archivos DLL.

Un archivo DLL de administración de RAS debe implementar y exportar todas las funciones siguientes:

[**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll)

[**MprAdminLinkLinkLinkupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[**MprAdminTerminateDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll)

Además, el archivo DLL de administración de RAS debe implementar y exportar cualquiera de los dos

[**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) y

[**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)

o

[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) y

[**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

Si no se implementan todas las funciones necesarias, RAS no se inicia.

**Windows 2000 Server:** Un archivo DLL de administración debe implementar [**las funciones MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) y [**MprAdminReleaseIpAddress.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) Si el archivo DLL implementa una de estas funciones, también debe implementar la otra.

RAS llama a [**la función MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) cuando el servicio de enrutamiento y acceso remoto se inicia por primera vez. La **función MprAdminInitializeDll** proporciona una oportunidad para que el archivo DLL de administración realice cualquier inicialización necesaria. De forma similar, RAS llama al [**servicio MprAdminTerminateDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll) cuando se cierra el servicio de enrutamiento y acceso remoto. Esta función permite que el archivo DLL de administración realice cualquier limpieza necesaria antes de salir.

Las [**funciones MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) y [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) permiten que el archivo DLL audite las conexiones de usuario al servidor. Un servidor RAS llama a **la función MprAdminAcceptNewConnection** cada vez que un usuario intenta conectarse. Esta función permite evitar que el usuario se conecte. La **función MprAdminAcceptNewConnection** también podría generar entradas de registro para facturación o auditoría. Cuando el usuario se desconecta, el servidor RAS llama a la función **MprAdminConnectionHangupNotification,** que puede registrar la hora a la que se desconectó el usuario.

Las [**funciones MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) y [**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2) son similares a **MprAdminAcceptNewConnection** y [**MprAdminConnectionHangupNotification.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) Sin embargo, cuando RAS llama a las funciones **MprAdminAcceptNewConnection2** y **MprAdminConnectionHangupNotification2,** RAS pasa un parámetro adicional de tipo [**RAS CONNECTION \_ \_ 2**](/windows/desktop/api/Mprapi/ns-mprapi-ras_connection_2).

RAS admite varios archivos DLL de administración. El usuario de acceso remoto solo puede conectarse si la implementación de la función [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) o [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) en cada uno de los archivos DLL acepta la conexión. En otras palabras, cada archivo DLL debe aceptar la conexión para que el usuario pueda conectarse.

Es posible que una sola conexión RAS use varios vínculos al conectarse a un servidor RAS. Las [**funciones MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink) y [**MprAdminLinkHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification) hacen posible que el archivo DLL de administración administre vínculos individuales en una conexión. RAS llama **a MprAdminAcceptNewLink** cada vez que se establece un nuevo vínculo para una conexión. Dado que todas las conexiones implican al menos un vínculo, RAS siempre llama a **MprAdminAcceptNewLink** una vez inmediatamente después de que [**mprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) o [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) devuelva, siempre que [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) o [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) acepten la conexión. RAS llama **a MprAdminLinkConexiónNotification** cada vez que se cierra un vínculo para una conexión.

Dado que RAS admite varios archivos DLL de administración, el usuario de acceso remoto solo puede conectarse si la implementación de la función [**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink) en cada uno de los archivos DLL acepta la conexión. En otras palabras, cada archivo DLL debe aceptar el vínculo para que se establezca el vínculo.

Una vez que el servidor RAS ha autenticado a un usuario, llama a la función [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) para obtener una dirección IP para el cliente remoto. Esta función proporciona un esquema alternativo para asignar una dirección IP a un usuario de acceso telefónico. Si no se implementa **MprAdminGetIpAddressForUser,** un servidor RAS asocia al usuario remoto con una dirección IP seleccionada de un grupo estático de direcciones IP o una seleccionada por un servidor dhcp (Protocolo de configuración dinámica de host). La **función MprAdminGetIpAddressForUser** permite que el archivo DLL invalide esta dirección IP predeterminada y especifique una dirección IP determinada para cada usuario. La **función MprAdminGetIpAddressForUser** puede establecer una marca que hace que RAS llame a la función [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) cuando el usuario se desconecta. A continuación, el archivo DLL **puede usar MprAdminReleaseIpAddress para** actualizar su asignación de dirección de usuario a IP.

RAS admite varios archivos DLL de administración, pero llama a las funciones [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) y [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) solo en el primer archivo DLL que los implementa y exporta. RAS omite las implementaciones de estas funciones en los otros archivos DLL. RAS comprueba las DLL de estas funciones en el orden en que aparecen en el [registro](ras-administration-dll-registry-setup.md).

RAS serializa las llamadas en el archivo DLL de administración. Una llamada a una de las funciones del archivo DLL para un cliente RAS determinado no adelanta una llamada a esa función para un cliente RAS diferente. RAS no llama a la función para el otro cliente hasta que se completa la llamada inicial. Además, la serialización se extiende a determinados grupos de funciones. Las funciones de dirección IP se serializan como un grupo; Una llamada a [**MprAdminGetIpAddressForUser o**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) bloquea las llamadas en ambas funciones hasta que se devuelve la llamada inicial. [**MprAdminAcceptNewConnection y**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) también se serializan como un grupo.

RAS ejecuta las funciones que asignan direcciones IP en un proceso; las funciones para las notificaciones de conexión y desconexión se ejecutan en otro proceso. Por lo tanto, el archivo DLL no depende de los datos compartidos entre estos dos conjuntos de funciones.

No llame a ninguna de las funciones de [administración de RAS](ras-administration-functions.md) ni a las funciones de administración de usuarios ras desde dentro de una función de llamada. [](ras-user-administration-functions.md) Las llamadas a estas funciones no se devolverán cuando se realizan desde dentro de una función de llamada.

El servidor RAS registra un error en el registro de eventos del sistema si se produce un error cuando intenta cargar un archivo DLL de administración de RAS o al llamar a una de las funciones del archivo DLL. Esto puede ocurrir, por ejemplo, si el archivo DLL especificó un nombre incorrecto para una función exportada o si no indicó el nombre de función en el archivo DEF. La entrada del registro de eventos indica el motivo del error.

**Windows 2000/NT:** No se admiten varios archivos DLL de administración.

 

 




