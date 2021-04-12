---
title: DLL de administración de RAS
description: El archivo DLL exporta las funciones a las que el servidor RAS llama cada vez que un usuario intenta conectarse o desconectarse.
ms.assetid: 014ab85d-8924-4c7a-89ed-f83e75318ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0908032e0916f0937e964408b1551d3f1515dea
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104358520"
---
# <a name="ras-administration-dll"></a>DLL de administración de RAS

El archivo DLL exporta las funciones a las que el servidor RAS llama cada vez que un usuario intenta conectarse o desconectarse. Puede usar el archivo DLL para realizar las siguientes funciones administrativas:

-   Decida si desea permitir que un usuario se conecte al servidor. Esto puede proporcionar una comprobación de seguridad además de la autenticación de usuario de RAS estándar.
-   Registra la hora a la que cada usuario se conecta y desconecta del servidor. Esto puede ser útil para fines de facturación o auditoría.
-   Asigne una dirección IP a cada usuario. Esto puede ser útil por motivos de seguridad para asignar la conexión de un usuario a un equipo específico.

Implemente las siguientes funciones al desarrollar un archivo DLL de administración del servidor RAS.

-   [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
-   [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
-   [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md)
-   [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md)

Un archivo DLL de administración de RAS debe implementar y exportar todas las funciones anteriores. Si alguna de las funciones no está implementada, el servicio de acceso remoto no se iniciará.

Las funciones [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md) y [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md) permiten a la dll auditar las conexiones de usuario al servidor. Un servidor RAS de Windows NT/Windows 2000 llama a la función **RasAdminAcceptNewConnection** cada vez que un usuario intenta conectarse. La función puede impedir que el usuario se conecte. También puede usar la función para generar una entrada en un registro para la facturación o la auditoría. Cuando el usuario se desconecta, el servidor RAS llama a la función **RasAdminConnectionHangupNotification** , que puede registrar la hora a la que el usuario se desconectó.

Una vez que el servidor RAS ha autenticado a un llamador, llama a la función [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) para obtener una dirección IP para el cliente remoto. El archivo DLL puede utilizar esta función para proporcionar un esquema alternativo para asignar una dirección IP a un usuario de acceso telefónico. Si **RasAdminGetIpAddressForUser** no está implementado, un servidor RAS conecta a un usuario remoto con una dirección IP seleccionada desde un grupo estático de direcciones IP, o bien una seleccionada por un servidor de protocolo de configuración dinámica de host (DHCP). La función **RasAdminGetIpAddressForUser** permite que el archivo dll invalide esta dirección IP predeterminada y especifique una dirección IP determinada para cada usuario. La función **RasAdminGetIpAddressForUser** puede establecer una marca que haga que ras llame a la función [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) cuando el usuario se desconecte. El archivo DLL puede utilizar [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) para actualizar su asignación de usuario a dirección IP.

RAS serializa las llamadas en el archivo DLL de administración. Una llamada a una de las funciones del archivo DLL para un cliente RAS determinado nunca se retendrá si se realiza una llamada a esa función para un cliente RAS diferente; se garantiza que la llamada inicial se completará antes de que RAS llame a la función para el otro cliente. Además, la serialización se extiende a determinados grupos de funciones. Las funciones de dirección IP se serializan como un grupo; una llamada a [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) o [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) bloqueará las llamadas en ambos hasta que se complete la llamada inicial. [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md) y [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md) también se serializan como un grupo.

RAS ejecuta las funciones para asignar las direcciones IP en un proceso y ejecuta las funciones para las notificaciones de conexión y desconexión en otro proceso. Por consiguiente, la DLL no debe depender de los datos compartidos entre los dos conjuntos de funciones.

El servidor RAS registra un error en el registro de eventos del sistema si se produce un error al intentar cargar un archivo DLL de administración de RAS o al llamar a una de las funciones del archivo DLL. Esto puede ocurrir, por ejemplo, si el archivo DLL especifica un nombre incorrecto para una función exportada, o si no incluyó el nombre de función en el archivo. def. La entrada del registro de eventos indica el motivo del error.

**Windows 2000 Server y versiones posteriores:** Los archivos dll de administración de RAS que implementan esta interfaz de función ya no funcionan. En su lugar, use la interfaz de la función MprAdmin que se proporciona con las versiones más recientes de Windows. Para obtener más información, consulte la [referencia de administración de Ras](remote-access-service-administration-reference.md) en la documentación de enrutamiento y ras.

 

 




