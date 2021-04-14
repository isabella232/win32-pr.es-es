---
title: Acerca de los archivos dll de administración de RAS
description: La DLL de administración de RAS exporta las funciones a las que el servidor RAS llama cuando un usuario intenta conectarse o desconectarse.
ms.assetid: c15c6e2d-3bb6-4583-9ac3-19528feb863f
keywords:
- RRAS de administración RAS, DLL de administración de RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb170e8cfa331ab9591aa509772c6f6a743fa49
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104532914"
---
# <a name="about-ras-administration-dlls"></a>Acerca de los archivos dll de administración de RAS

La DLL de administración de RAS exporta las funciones a las que el servidor RAS llama cuando un usuario intenta conectarse o desconectarse. Estos son algunos de los usos posibles de un archivo DLL de administración de RAS:

-   Decida si desea permitir que un usuario se conecte al servidor. El archivo DLL de administración puede proporcionar una comprobación de seguridad además de la autenticación de usuario de RAS estándar.
-   Registra la hora a la que cada usuario se conecta y desconecta del servidor. Esto puede ser útil para fines de facturación o auditoría.
-   Asigne una dirección IP a cada usuario. Esto resulta útil para la seguridad, ya que esta característica se usa para asignar la conexión de un usuario a un equipo específico.

La ubicación del archivo DLL de administración de RAS se especifica en el registro; vea [configuración del registro del archivo dll de administración de Ras](ras-administration-dll-registry-setup.md).

RAS admite varios archivos dll de administración. El registro admite varias ubicaciones de DLL. RAS llama a las funciones de los archivos dll en el orden en que se enumeran en el registro. vea [configuración del registro del archivo dll de administración de Ras](ras-administration-dll-registry-setup.md).

**Windows 2000 Server:** RAS no admite varios archivos dll.

Un archivo DLL de administración de RAS debe implementar y exportar todas las funciones siguientes:

[**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll)

[**MprAdminLinkHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[**MprAdminTerminateDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll)

Además, el archivo DLL de administración de RAS debe implementar y exportar

[**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) y

[**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)

or

[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) y

[**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

Si no se implementan todas las funciones necesarias, RAS no se inicia.

**Windows 2000 Server:** Un archivo DLL de administración debe implementar las funciones [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) y [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) . Si el archivo DLL implementa una de estas funciones, también debe implementar el otro.

RAS llama a la función [**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) cuando el servicio de enrutamiento y acceso remoto se inicia por primera vez. La función **MprAdminInitializeDll** proporciona una oportunidad para que el archivo dll de administración realice cualquier inicialización necesaria. Del mismo modo, RAS llama al servicio [**MprAdminTerminateDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll) cuando se cierra el servicio de enrutamiento y acceso remoto. Esta función permite que el archivo DLL de administración realice cualquier limpieza necesaria antes de salir.

Las funciones [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) y [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) permiten a la dll auditar las conexiones de usuario al servidor. Un servidor RAS llama a la función **MprAdminAcceptNewConnection** cada vez que un usuario intenta conectarse. Esta función permite impedir que el usuario se conecte. La función **MprAdminAcceptNewConnection** también podría generar entradas de registro para la facturación o la auditoría. Cuando el usuario se desconecta, el servidor RAS llama a la función **MprAdminConnectionHangupNotification** , que puede registrar la hora a la que el usuario se desconectó.

Las funciones [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) y [**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2) son similares a **MprAdminAcceptNewConnection** y [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification). Sin embargo, cuando RAS llama a las funciones **MprAdminAcceptNewConnection2** y **MprAdminConnectionHangupNotification2** , Ras pasa un parámetro adicional del [**tipo \_ conexión RAS \_ 2**](/windows/desktop/api/Mprapi/ns-mprapi-ras_connection_2).

RAS admite varios archivos dll de administración. El usuario de acceso remoto solo puede conectarse si la implementación de la función [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) o [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) en cada uno de los archivos dll acepta la conexión. En otras palabras, cada DLL debe aceptar la conexión para que el usuario pueda conectarse.

Es posible que una sola conexión RAS use varios vínculos al conectarse a un servidor RAS. Las funciones [**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink) y [**MprAdminLinkHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification) permiten que el archivo dll de administración administre los vínculos individuales de una conexión. RAS llama a **MprAdminAcceptNewLink** cada vez que se establece un nuevo vínculo para una conexión. Dado que todas las conexiones incluyen al menos un vínculo, RAS siempre llama a **MprAdminAcceptNewLink** una vez inmediatamente después de que [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) o [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) devuelvan, siempre que [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) o [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) acepten la conexión. RAS llama a **MprAdminLinkHangupNotification** siempre que se cierra un vínculo para una conexión.

Como RAS admite varios archivos dll de administración, el usuario de acceso remoto solo puede conectarse si la implementación de la función [**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink) en cada uno de los archivos dll acepta la conexión. En otras palabras, cada archivo DLL debe aceptar el vínculo para que se establezca el vínculo.

Una vez que el servidor RAS ha autenticado a un usuario, llama a la función [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) para obtener una dirección IP para el cliente remoto. Esta función proporciona un esquema alternativo para asignar una dirección IP a un usuario de acceso telefónico. Si **MprAdminGetIpAddressForUser** no está implementado, un servidor RAS asocia el usuario remoto a una dirección IP que se selecciona de un grupo estático de direcciones IP, o bien uno seleccionado por un servidor de protocolo de configuración dinámica de host (DHCP). La función **MprAdminGetIpAddressForUser** permite que el archivo dll invalide esta dirección IP predeterminada y especifique una dirección IP determinada para cada usuario. La función **MprAdminGetIpAddressForUser** puede establecer una marca que haga que ras llame a la función [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) cuando el usuario se desconecte. Después, el archivo DLL puede utilizar **MprAdminReleaseIpAddress** para actualizar su asignación de usuario a dirección IP.

RAS admite varios archivos dll de administración, pero llama a las funciones [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) y [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) solo en el primer archivo DLL que implementa y exporta. RAS omite las implementaciones de estas funciones en los otros archivos dll. RAS comprueba las DLL para estas funciones en el orden en el que aparecen en el [registro](ras-administration-dll-registry-setup.md).

RAS serializa las llamadas en el archivo DLL de administración. Una llamada a una de las funciones del archivo DLL para un cliente RAS determinado no tiene preferencia sobre una llamada a esa función para un cliente RAS diferente; RAS no llama a la función para el otro cliente hasta que se complete la llamada inicial. Además, la serialización se extiende a determinados grupos de funciones. Las funciones de dirección IP se serializan como un grupo; una llamada a [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) o [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) bloquea las llamadas en ambas funciones hasta que se devuelve la llamada inicial. [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) y [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) también se serializan como un grupo.

RAS ejecuta las funciones que asignan direcciones IP en un proceso. las funciones para las notificaciones de conexión y desconexión se ejecutan en otro proceso. Por consiguiente, el archivo DLL no depende de los datos compartidos entre estos dos conjuntos de funciones.

No llame a ninguna de las funciones de [Administración de Ras](ras-administration-functions.md) ni a [las funciones de administración de usuarios de Ras](ras-user-administration-functions.md) desde una función de llamada. Las llamadas a estas funciones no devolverán cuando se realicen desde una función de llamada.

El servidor RAS registra un error en el registro de eventos del sistema si se produce un error al intentar cargar un archivo DLL de administración de RAS o al llamar a una de las funciones del archivo DLL. Esto puede ocurrir, por ejemplo, si el archivo DLL especifica un nombre incorrecto para una función exportada, o si no incluyó el nombre de función en el archivo DEF. La entrada del registro de eventos indica el motivo del error.

**Windows 2000/NT:** No se admiten varios archivos dll de administración.

 

 




