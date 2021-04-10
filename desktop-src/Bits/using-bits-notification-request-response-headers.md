---
title: Usar encabezados de solicitud/respuesta de notificación BITS
description: BITS puede enviar la ubicación del archivo de carga (por referencia) a la aplicación de servidor o puede enviar el archivo de carga en el cuerpo de la solicitud (por valor).
ms.assetid: b80f9077-54e7-4d10-909a-dee7d8822627
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 5dcbee8b82d96a4f13db0ae4de6441e9df40ce83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268313"
---
# <a name="using-bits-notification-requestresponse-headers"></a>Usar encabezados de solicitud/respuesta de notificación BITS

BITS puede enviar la ubicación del archivo de carga (por referencia) a la aplicación de servidor o puede enviar el archivo de carga en el cuerpo de la solicitud (por valor). Para especificar cómo envía BITS el archivo de carga a la aplicación de servidor, establezca la propiedad [**BITSServerNotificationType**](bits-iis-extension-properties.md)de la metabase de IIS. Si especifica by Reference, BITS pasa la ubicación del archivo en el encabezado BITS-request-archivo de nombre de archivo. Para enviar una respuesta, cree y escriba la respuesta en el archivo especificado en el encabezado BITS-respuesta-archivo de nombre de archivo.

Las aplicaciones de servidor que envían la misma respuesta a muchos clientes deben usar por referencia, por lo que solo hay una copia de la respuesta en el servidor. Por ejemplo, en una aplicación de actualización de software, el cliente cargaría su configuración de software en la aplicación de servidor. La aplicación de servidor determina qué paquete necesita el cliente y envía la dirección URL del paquete a BITS. A continuación, BITS descarga el paquete como respuesta.

Las aplicaciones de servidor que generan respuestas únicas para cada cliente deben usar por valor. Por ejemplo, una aplicación de servidor que admita la compra de archivos de música necesitaría enviar un archivo de música firmado al cliente. Dado que el archivo de música firmado es único para el cliente, la aplicación de servidor no lo almacenaría en el servidor. Por valor también es útil para una aplicación que ya está escrita para aceptar directamente los datos de cliente web.

Para obtener más información sobre los encabezados de solicitud y respuesta utilizados entre BITS y la aplicación de servidor, vea [Protocolo de notificación para aplicaciones de servidor](notification-protocol-for-server-applications.md).

En el ejemplo de JavaScript siguiente se muestra cómo obtener acceso a los archivos de solicitud y respuesta en una aplicación de servidor que usa la notificación de referencia (BITS pasa la ubicación de los archivos en los encabezados).


```JavaScript
  var fso = new ActiveXObject ("Scripting.FileSystemObject")
  var requestFileName = Request.ServerVariables ("HTTP_BITS-Request-DataFile-Name")
  var responseFileName = Request.ServerVariables ("HTTP_BITS-Response-DataFile-Name")
  var requestStream
  var responseStream
  var ForReading = 1
  var ForWriting = 2
  var TristateUseDefault = -2

  //Open the upload data file as text stream for reading.
  requestStream = fso.OpenTextFile(requestFileName, ForReading, false, TristateUseDefault);

  //Do something with the uploaded data.

  //Close the upload stream.
  requestStream.Close()

  //Open response data file as text stream for writing.
  responseStream = fso.OpenTextFile(responseFileName, ForWriting, true, TristateUseDefault);

  //Write a response to the response file.

  //Close the response text stream
  responseStream.Close()
```



Si desea usar un archivo de respuesta diferente del especificado en BITS-Response-archivo de nombre de archivo, llame al método **Response. AddHeader** para agregar la dirección URL de bits-estático-respuesta, tal como se muestra en el ejemplo siguiente. Si especifica un archivo de respuesta diferente, no cree el archivo de respuesta especificado en BITS-Response-archivo de nombre de archivo.


```JavaScript
  Response.AddHeader "BITS-Static-Response-URL" "https://myserver/mypath/myfile"
```
 

 




