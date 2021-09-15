---
title: Funciones de API de WebDAV
description: Las siguientes funciones se usan en la API de WebDAV.
ms.assetid: 489cdc17-aca8-4621-bc61-f0f3b9ac22b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1917cd6ebb64470eec6fde9188cc39341142fc8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580692"
---
# <a name="webdav-api-functions"></a>Funciones de API de WebDAV

Las siguientes funciones se usan en la API de WebDAV.



| Función                                                             | Descripción                                                                                                                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DavAddConnection**](/windows/desktop/api/davclnt/nf-davclnt-davaddconnection)                         | Crea una conexión segura a un servidor WebDAV o a un archivo o directorio remoto en un servidor WebDAV.                                                                                                                                   |
| [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback)                                | El cliente webDAV llama a la función de devolución de llamada [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) definida por la aplicación para solicitar al usuario las credenciales.                                                                                           |
| [**DavCancelConnectionsToServer**](/windows/desktop/api/davclnt/nf-davclnt-davcancelconnectionstoserver) | Cierra todas las conexiones a un servidor WebDAV o a un archivo o directorio remoto en un servidor WebDAV.                                                                                                                                        |
| [**DavDeleteConnection**](/windows/desktop/api/davclnt/nf-davclnt-davdeleteconnection)                   | Cierra una conexión que se creó mediante la [**función DavAddConnection.**](/windows/desktop/api/davclnt/nf-davclnt-davaddconnection)                                                                                                                              |
| [**DavFlushFile**](/windows/desktop/api/davclnt/nf-davclnt-davflushfile)                                 | Vacía los datos de la versión local de un archivo remoto en el servidor WebDAV.                                                                                                                                                        |
| [*DavFreeCredCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback_freecred)                        | El cliente webDAV llama a la función de devolución de llamada [*DavFreeCredCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback_freecred) definida por la aplicación para liberar la información de credenciales recuperada por la función de devolución de llamada [*DavAuthCallback.*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) |
| [**DavGetExtendedError**](/windows/desktop/api/davclnt/nf-davclnt-davgetextendederror)                   | Recupera la información de código de error extendida que el servidor WebDAV devolvió para la operación de E/S con error anterior.                                                                                                                  |
| [**DavGetHTTPFromUNCPath**](/windows/desktop/api/davclnt/nf-davclnt-davgethttpfromuncpath)               | Convierte la ruta de acceso UNC especificada en una ruta de acceso HTTP equivalente.                                                                                                                                                                           |
| [**DavGetTheLockOwnerOfTheFile**](/windows/desktop/api/davclnt/nf-davclnt-davgetthelockownerofthefile)   | Devuelve el propietario del bloqueo de archivo para un archivo bloqueado en un servidor WebDAV.                                                                                                                                                             |
| [**DavGetUNCFromHTTPPath**](/windows/desktop/api/davclnt/nf-davclnt-davgetuncfromhttppath)               | Convierte la ruta de acceso HTTP especificada en una ruta unc equivalente.                                                                                                                                                                           |
| [**DavInvalidateCache**](/windows/desktop/api/davclnt/nf-davclnt-davinvalidatecache)                     | Invalida el contenido de la memoria caché local para un archivo remoto en un servidor WebDAV.                                                                                                                                                     |
| [**DavRegisterAuthCallback**](/windows/desktop/api/Davclnt/nf-davclnt-davregisterauthcallback)           | Registra una función de devolución de llamada definida por la aplicación que el cliente de WebDAV puede usar para solicitar al usuario las credenciales.                                                                                                                 |
| [**DavUnregisterAuthCallback**](/windows/desktop/api/Davclnt/nf-davclnt-davunregisterauthcallback)       | Anula el registro de una función de devolución de llamada registrada que el cliente de WebDAV usa para solicitar al usuario las credenciales.                                                                                                                            |



 

 

 




