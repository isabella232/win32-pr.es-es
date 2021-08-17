---
title: Operación asincrónica
description: En modo asincrónico, una aplicación puede ejecutar cualquier función que incluya un valor de contexto como uno de sus parámetros y pueda seguir ejecutando otros comandos o funciones mientras la aplicación espera a que la función complete su tarea.
ms.assetid: 4b8ade00-deb3-4d9f-9ceb-5ba3296c8c68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e494b79b28b9aaf005fc6b1790d0cf84b07ceade6606f03ce03198426ac33d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562097"
---
# <a name="asynchronous-operation"></a>Operación asincrónica

La cantidad de tiempo que tarda una aplicación en acceder a un recurso de Internet depende de una serie de factores, como la conexión que se usa, el servidor en el que se encuentra el recurso y el número de usuarios que intentan acceder al recurso. En el caso de las aplicaciones que descargan varios recursos o controlan varias tareas (incluidas una o varias descargas), esperar a que se complete cada descarga antes de pasar a la siguiente tarea puede ser muy ineficaz. Para reducir la cantidad de tiempo que una aplicación tiene que esperar, muchas de las funciones de WinINet pueden funcionar de forma asincrónica.

En modo asincrónico, una aplicación puede ejecutar cualquier función que incluya un valor de contexto como uno de sus parámetros y pueda seguir ejecutando otros comandos o funciones mientras la aplicación espera a que la función complete su tarea. Mientras se completa la tarea, se notifica a una función de devolución de llamada de estado proporcionada por la aplicación sobre el progreso de la tarea y cuándo se ha completado. En este momento, la función de devolución de llamada de estado puede llamar a otras funciones o realizar cualquier otra tarea necesaria que dependa de la finalización de la tarea.

No hay afinidad entre subprocesos de devolución de llamada cuando se llama a WinINet de forma asincrónica: una llamada puede comenzar desde un subproceso, pero cualquier otro subproceso puede recibir la devolución de llamada.

-   [Ventajas](#benefits)
-   [Escenarios](#scenarios)
-   [Temas relacionados](#related-topics)

## <a name="benefits"></a>Ventajas

El funcionamiento de forma asincrónica tiene varias ventajas. Por ejemplo:

-   Descargar varios recursos de Internet simultáneamente.

    Puede conectarse a varios recursos de Internet al mismo tiempo y descargarlos a medida que estén disponibles.

-   Aumentar el rendimiento de la aplicación.

    Una aplicación que usa las funciones de WinINet de forma asincrónica no tiene que esperar hasta que se complete la solicitud, por lo que la aplicación puede realizar otras tareas que no dependen de la solicitud, lo que mejora el rendimiento general de la aplicación.

-   Supervise el progreso de la descarga.

    La función de devolución de llamada de estado recibe notificaciones mientras procesa una solicitud. Si es necesario, la aplicación puede usar la información proporcionada por esa función de devolución de llamada de estado para mantener al usuario informado sobre el progreso de la operación o para interrumpir las solicitudes que tardan demasiado tiempo en completarse.

## <a name="scenarios"></a>Escenarios

Supongamos que la aplicación debe descargar los precios del café de los sitios Downfall Coffee & Tea y Fourth Coffee y comparar los precios. El sitio cuarto café normalmente tiene un tiempo de respuesta más lento, por lo que la aplicación debe descargar la información de Downfall Coffee & Té primero.

Se desarrollan dos versiones de la aplicación. Uno funciona de forma sincrónica, descargando primero los precios del sitio downfall Coffee & Tea y, después, los precios del sitio cuarto café. El segundo funciona de forma asincrónica, enviando solicitudes a ambos sitios y descargando los precios cuando estén disponibles.

En la tabla siguiente se muestra lo que ocurriría si el cuarto sitio de café fuera más rápido en un día determinado.



| Evento                                                            | Versión sincrónica                        | Versión asincrónica                                     |
|------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------------|
| Inicio                                                            | Envío de una solicitud a Downfall Coffee & Tea      | Envío de solicitudes a Downfall Coffee & Té y Cuarto Café |
| Solicitud de la versión asincrónica a Cuarto café completado | En espera                                    | Descarga de los precios de Cuarto café                       |
| Solicitud a Downfall Coffee & Té completado                       | Descarga de precios de Downfall Coffee & Té | Descarga de precios de Downfall Coffee & Té               |
| Después de que se descarguen los precios & downfall Coffee & té              | Envío de una solicitud a Cuarto café              | Comparación de precios                                           |
| Comparación de la versión asincrónica completada                      | En espera                                    | Operación completada                                       |
| Solicitud de la versión sincrónica a Cuarto café completado  | Descarga de los precios de Cuarto café         | N/D                                                      |
| Después de descargar los precios del cuarto café                      | Comparación de precios                             | N/D                                                      |
| Comparación de la versión sincrónica completada                       | Operación completada                         | N/D                                                      |



 

Otro ejemplo sería un explorador web como Microsoft Internet Explorer. Cuando el explorador descarga una página, a menudo necesita descargar otros recursos, como imágenes y archivos de sonido. En modo asincrónico, la página y sus recursos asociados se pueden solicitar y descargar simultáneamente a medida que estén disponibles, en lugar de solicitar y descargar la página y cada recurso de uno en uno.

## <a name="related-topics"></a>Temas relacionados

A continuación se incluyen vínculos relacionados.

Tutoriales

-   [Crear funciones de devolución de llamada de estado](creating-status-callback-functions.md)

Funciones necesarias para configurar la operación asincrónica

-   [**InternetAbrir**](/windows/desktop/api/Wininet/nf-wininet-internetopena)
-   [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)

Funciones que se pueden usar de forma asincrónica

-   [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)
-   [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)
-   [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)
-   [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya)
-   [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)
-   [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)
-   [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)
-   [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)
-   [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)
-   [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya)
-   [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)
-   [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)
-   [**HttpEndRequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta)
-   [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)
-   [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)
-   [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)
-   [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)
-   [**InternetReadFileEx**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)

> [!Note]  
> Las [**funciones FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya), [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya), [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya), [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya), [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)y [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) usan el valor de contexto proporcionado en la llamada a la función [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)

 

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones o servicios de servidor, use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 