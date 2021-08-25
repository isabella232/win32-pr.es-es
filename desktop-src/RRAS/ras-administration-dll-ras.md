---
title: DLL de administración de RAS
description: El archivo DLL exporta funciones a las que llama el servidor RAS cada vez que un usuario intenta conectarse o desconectarse.
ms.assetid: 014ab85d-8924-4c7a-89ed-f83e75318ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f6be479d00175750fb4d6ffce73aab4439d2c7df9e6e07f97e9964f267ce82a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909925"
---
# <a name="ras-administration-dll"></a>DLL de administración de RAS

El archivo DLL exporta funciones a las que llama el servidor RAS cada vez que un usuario intenta conectarse o desconectarse. Puede usar el archivo DLL para realizar las siguientes funciones administrativas:

-   Decida si desea permitir que un usuario se conecte al servidor. Esto puede proporcionar una comprobación de seguridad además de la autenticación de usuario RAS estándar.
-   Registre la hora a la que cada usuario se conecta y se desconecta del servidor. Esto puede ser útil para fines de facturación o auditoría.
-   Asigne una dirección IP a cada usuario. Esto puede ser útil por motivos de seguridad para asignar la conexión de un usuario a un equipo específico.

Implemente las siguientes funciones al desarrollar un archivo DLL de administración del servidor RAS.

-   [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
-   [**RasAdminConnectionConexiónAdminupNotification**](rasadminconnectionhangupnotification.md)
-   [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md)
-   [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md)

Un archivo DLL de administración de RAS debe implementar y exportar todas las funciones anteriores. Si alguna de las funciones no está implementada, el servicio de acceso remoto no se iniciará.

Las [**funciones RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md) y [**RasAdminConnectionConnectionConexiónNotification**](rasadminconnectionhangupnotification.md) permiten que el archivo DLL audite las conexiones de usuario al servidor. Un Windows NT/Windows 2000 RAS llama a la función **RasAdminAcceptNewConnection** cada vez que un usuario intenta conectarse. La función puede impedir que el usuario se conecte. También puede usar la función para generar una entrada en un registro para facturación o auditoría. Cuando el usuario se desconecta, el servidor RAS llama a la función **RasAdminConnectionConexiónNotification,** que puede registrar la hora a la que se desconectó el usuario.

Después de que el servidor RAS haya autenticado un llamador, llama a la función [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) para obtener una dirección IP para el cliente remoto. El archivo DLL puede usar esta función para proporcionar un esquema alternativo para asignar una dirección IP a un usuario de acceso telefónico. Si **RasAdminGetIpAddressForUser** no está implementado, un servidor RAS conecta un usuario remoto a una dirección IP seleccionada de un grupo estático de direcciones IP o a una seleccionada por un servidor dhcp (Protocolo de configuración dinámica de host). La **función RasAdminGetIpAddressForUser** permite que el archivo DLL invalide esta dirección IP predeterminada y especifique una dirección IP determinada para cada usuario. La **función RasAdminGetIpAddressForUser** puede establecer una marca que hace que RAS llame a la función [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) cuando el usuario se desconecta. El archivo DLL puede [**usar RasAdminReleaseIpAddress para**](rasadminreleaseipaddress.md) actualizar su asignación de dirección de usuario a IP.

RAS serializa las llamadas en el archivo DLL de administración. Una llamada a una de las funciones del archivo DLL para un cliente RAS determinado nunca se adelantará mediante una llamada a esa función para un cliente RAS diferente. Se garantiza que la llamada inicial se completará antes de que RAS llame a la función para el otro cliente. Además, la serialización se extiende a determinados grupos de funciones. Las funciones de dirección IP se serializan como un grupo; Una llamada a [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) o [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) bloqueará las llamadas en ambos hasta que se complete la llamada inicial. [**RasAdminAcceptNewConnection y**](rasadminacceptnewconnection.md) [**RasAdminConnectionConexiónNotification**](rasadminconnectionhangupnotification.md) también se serializan como un grupo.

RAS ejecuta las funciones para asignar direcciones IP en un proceso y ejecuta las funciones para las notificaciones de conexión y desconexión en otro proceso. Por lo tanto, el archivo DLL no debe depender de los datos compartidos entre los dos conjuntos de funciones.

El servidor RAS registra un error en el registro de eventos del sistema si se produce un error cuando intenta cargar un archivo DLL de administración de RAS o al llamar a una de las funciones del archivo DLL. Esto puede ocurrir, por ejemplo, si el archivo DLL especificó un nombre incorrecto para una función exportada o si no indicó el nombre de la función en el archivo .def. La entrada del registro de eventos indica el motivo del error.

**Windows 2000 Server y versiones posteriores:** Los archivos DLL de administración de RAS que implementan esta interfaz de función ya no funcionan. En su lugar, use la interfaz de función MprAdmin proporcionada con las versiones más recientes de Windows. Para obtener más información, consulte la Referencia [de administración de RAS](remote-access-service-administration-reference.md) en la documentación de Enrutamiento y RAS.

 

 




