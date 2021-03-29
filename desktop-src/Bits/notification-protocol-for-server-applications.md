---
title: Protocolo de notificación para aplicaciones de servidor
description: BITS usa la propiedad BITSServerNotificationType para determinar cómo envía BITS el contenido del archivo de carga a la aplicación de servidor.
ms.assetid: d5193d0c-3ab4-47ab-a570-fea2904a4371
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d35f6f5fec1a1de9ebd5c2c244a55bc1806b06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993971"
---
# <a name="notification-protocol-for-server-applications"></a>Protocolo de notificación para aplicaciones de servidor

BITS usa la propiedad [BITSServerNotificationType](bits-iis-extension-properties.md) para determinar cómo envía bits el contenido del archivo de carga a la aplicación de servidor. Si la propiedad BITSServerNotificationType se establece en 1, [bits pasa la ubicación del archivo de carga en un encabezado](#sending-the-location-of-the-upload-file-in-a-header). Si la propiedad BITSServerNotificationType se establece en 2, [bits pasa el contenido del archivo de carga en el cuerpo de la solicitud](#sending-the-upload-file-in-the-body-of-the-request).

Para obtener información detallada sobre cómo BITS controla los errores de la aplicación de servidor, consulte [control de errores de aplicaciones de servidor](#handling-server-application-errors).

## <a name="sending-the-location-of-the-upload-file-in-a-header"></a>Enviar la ubicación del archivo de carga en un encabezado

BITS pasa la ubicación de los archivos de carga y de respuesta a la aplicación de servidor en los encabezados si la propiedad [BITSServerNotificationType](bits-iis-extension-properties.md) está establecida en 1. La aplicación de servidor abre el archivo de carga, procesa los datos y, a continuación, genera el archivo de respuesta. De forma predeterminada, BITS quita los archivos de carga y respuesta del servidor una vez que recibe la respuesta de la aplicación de servidor. Para que BITS copie el archivo de carga en la ubicación especificada por el nombre de archivo remoto en el trabajo, incluya el encabezado BITS-copiar-archivo a destino en la respuesta. Si no incluye el encabezado y desea guardar los archivos de carga y de respuesta, debe copiar los archivos de carga y de respuesta en una nueva ubicación antes de responder. En la tabla siguiente se muestran los encabezados de solicitud.



| Encabezado de solicitud              | Descripción                                                                                |
|-----------------------------|--------------------------------------------------------------------------------------------|
| BITS-original-solicitud-URL   | Contiene el nombre remoto especificado en el trabajo.                                             |
| BITS-request-archivo de nombre de archivo  | Contiene la ruta de acceso completa a los datos cargados.                                               |
| BITS-respuesta-archivo de nombre de archivo | Contiene la ruta de acceso completa a donde BITS espera que la aplicación de servidor escriba la respuesta. |



 

En la tabla siguiente se muestran los encabezados de respuesta.



| Encabezado de respuesta               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BITS-static-Response-URL      | Opcional. Contiene la dirección URL absoluta (no especifique una dirección URL relativa) a un archivo de datos estático que se va a usar como respuesta. El archivo de datos estático debe ser accesible para el cliente de BITS. Si usa este encabezado, no cree el archivo de respuesta especificado en el encabezado de solicitud BITS-respuesta-nombre de archivo. Tenga en cuenta que BITS no elimina este archivo.<br/>                                                                                                           |
| BITS-copiar-archivo a destino | Opcional. De forma predeterminada, si la propiedad [BITSServerNotificationType](bits-iis-extension-properties.md) se establece en 1 o 2, el servidor bits no copia el archivo de carga en la ubicación especificada por el nombre de archivo remoto en el trabajo. Para que BITS copie el archivo en la ubicación especificada por el nombre de archivo remoto en el trabajo, envíe este encabezado de respuesta. Puede especificar cualquier valor; BITS no utiliza el valor. Tenga en cuenta que las carpetas de la ruta de acceso del archivo remoto deben existir. |



 

La siguiente solicitud muestra BITS que envían la ubicación del archivo de carga a la aplicación de servidor.

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
BITS-Request-DataFile-Name: c:\physical-path\BITS-Sessions\{5e53c221-f2d6-4bf2-
b994-1dc43ceaca8d}\request
BITS-Response-DataFile-Name: c:\physical-path\BITS-Sessions\{5e53c221-f2d6-4bf2-
b994-1dc43ceaca8d}\response
Content-Length: 0
```

A continuación se muestra la respuesta de la aplicación de servidor a BITS; la respuesta se coloca en el archivo especificado por el encabezado de solicitud BITS-respuesta-nombre de archivo.

``` syntax
HTTP/1.1 200 - OK
Content-Length: 0
```

## <a name="sending-the-upload-file-in-the-body-of-the-request"></a>Envío del archivo de carga en el cuerpo de la solicitud

BITS envía el archivo de carga en el cuerpo de la solicitud si la propiedad [BITSServerNotificationType](bits-iis-extension-properties.md) está establecida en 2. El envío del archivo de carga en el cuerpo de la solicitud permite que los scripts y las aplicaciones existentes funcionen con modificaciones mínimas. El archivo de carga y el archivo de respuesta se pasan en la solicitud y la respuesta, respectivamente. En la tabla siguiente se muestra el encabezado de la solicitud.



| Encabezado de solicitud            | Descripción                                    |
|---------------------------|------------------------------------------------|
| BITS-original-solicitud-URL | Contiene el nombre remoto especificado en el trabajo. |



 

En la tabla siguiente se muestran los encabezados de respuesta.



| Encabezado de respuesta               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BITS-static-Response-URL      | Opcional. Contiene la dirección URL absoluta (no especifique una dirección URL relativa) a un archivo de datos estático que se va a usar como respuesta. El archivo de datos estático debe ser accesible para el cliente de BITS. Si usa este encabezado, no incluya la respuesta en la secuencia. Tenga en cuenta que BITS no elimina este archivo.<br/>                                                                                                                                      |
| BITS-copiar-archivo a destino | Opcional. Si la propiedad [BITSServerNotificationType](bits-iis-extension-properties.md) se establece en 1 o 2, el servidor bits no copia el archivo de carga en la ubicación especificada por el nombre de archivo remoto en el trabajo. Para que BITS copie el archivo en la ubicación especificada por el nombre de archivo remoto, envíe este encabezado de respuesta. Puede especificar cualquier valor; BITS no utiliza el valor. Tenga en cuenta que las carpetas de la ruta de acceso del archivo remoto deben existir. |



 

La siguiente solicitud muestra BITS que pasan el archivo cargado a la aplicación de servidor en el cuerpo de la solicitud.

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
Content-Length: 80000

80000 bytes of upload data goes here
```

La respuesta siguiente muestra la aplicación de servidor que pasa los datos de respuesta a BITS en el cuerpo de la respuesta.

``` syntax
HTTP/1.1 200 - OK
Content-Length: 100

100 bytes of reply data goes here
```

## <a name="handling-server-application-errors"></a>Control de errores de aplicación de servidor

Consulte [control de errores de aplicaciones de servidor](handling-server-application-errors.md).

 

 





