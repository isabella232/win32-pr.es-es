---
title: Uso de encabezados de solicitud/respuesta de notificación de BITS
description: BITS puede enviar la ubicación del archivo de carga (por referencia) a la aplicación de servidor o puede enviar el archivo de carga en el cuerpo de la solicitud (por valor).
ms.assetid: b80f9077-54e7-4d10-909a-dee7d8822627
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 5dcbee8b82d96a4f13db0ae4de6441e9df40ce83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968899"
---
# <a name="using-bits-notification-requestresponse-headers"></a>Uso de encabezados de solicitud/respuesta de notificación de BITS

BITS puede enviar la ubicación del archivo de carga (por referencia) a la aplicación de servidor o puede enviar el archivo de carga en el cuerpo de la solicitud (por valor). Para especificar cómo BITS envía el archivo de carga a la aplicación de servidor, establezca la propiedad de metabase de IIS, [**BITSServerNotificationType**](bits-iis-extension-properties.md). Si especifica por referencia, BITS pasa la ubicación del archivo en el encabezado BITS-Request-DataFile-Name. Para enviar una respuesta, cree y escriba la respuesta en el archivo especificado en el encabezado BITS-Response-DataFile-Name.

Las aplicaciones de servidor que envían la misma respuesta a muchos clientes deben usar por referencia, por lo que solo hay una copia de la respuesta en el servidor. Por ejemplo, en una aplicación de actualización de software, el cliente cargaría su configuración de software en la aplicación de servidor. La aplicación de servidor determina qué paquete necesita el cliente y envía la dirección URL del paquete a BITS. A continuación, BITS descarga el paquete como respuesta.

Las aplicaciones de servidor que generan respuestas únicas para cada cliente deben usar por valor. Por ejemplo, una aplicación de servidor que admita la compra de archivos de música tendría que enviar un archivo de música firmado al cliente. Dado que el archivo de música firmado es único para el cliente, la aplicación de servidor no lo almacenaría en el servidor. Por valor también es útil para una aplicación que ya está escrita para aceptar datos de cliente web directamente.

Para obtener más información sobre los encabezados de solicitud y respuesta usados entre BITS y la aplicación de servidor, vea [Protocolo de notificación para aplicaciones de servidor](notification-protocol-for-server-applications.md).

En el siguiente ejemplo de JavaScript se muestra cómo acceder a los archivos de solicitud y respuesta en una aplicación de servidor que usa mediante notificación de referencia (BITS pasa la ubicación de los archivos en los encabezados).


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



Si desea usar un archivo de respuesta diferente al especificado en BITS-Response-DataFile-Name, llame al método **Response.AddHeader** para agregar la dirección URL de bits-static-response- como se muestra en el ejemplo siguiente. Si especifica otro archivo de respuesta, no cree el archivo de respuesta especificado en BITS-Response-DataFile-Name.


```JavaScript
  Response.AddHeader "BITS-Static-Response-URL" "https://myserver/mypath/myfile"
```
 

 




