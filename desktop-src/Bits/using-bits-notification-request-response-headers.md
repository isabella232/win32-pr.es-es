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
# <a name="using-bits-notification-requestresponse-headers"></a><span data-ttu-id="49a16-103">Usar encabezados de solicitud/respuesta de notificación BITS</span><span class="sxs-lookup"><span data-stu-id="49a16-103">Using BITS Notification Request/Response Headers</span></span>

<span data-ttu-id="49a16-104">BITS puede enviar la ubicación del archivo de carga (por referencia) a la aplicación de servidor o puede enviar el archivo de carga en el cuerpo de la solicitud (por valor).</span><span class="sxs-lookup"><span data-stu-id="49a16-104">BITS can send the location of the upload file (by reference) to your server application or it can send the upload file in the body of the request (by value).</span></span> <span data-ttu-id="49a16-105">Para especificar cómo envía BITS el archivo de carga a la aplicación de servidor, establezca la propiedad [**BITSServerNotificationType**](bits-iis-extension-properties.md)de la metabase de IIS.</span><span class="sxs-lookup"><span data-stu-id="49a16-105">To specify how BITS sends the upload file to your server application, set the IIS metabase property, [**BITSServerNotificationType**](bits-iis-extension-properties.md).</span></span> <span data-ttu-id="49a16-106">Si especifica by Reference, BITS pasa la ubicación del archivo en el encabezado BITS-request-archivo de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="49a16-106">If you specify by reference, BITS passes the location of the file in the BITS-Request-DataFile-Name header.</span></span> <span data-ttu-id="49a16-107">Para enviar una respuesta, cree y escriba la respuesta en el archivo especificado en el encabezado BITS-respuesta-archivo de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="49a16-107">To send a reply, create and write your response to the file specified in the BITS-Response-DataFile-Name header.</span></span>

<span data-ttu-id="49a16-108">Las aplicaciones de servidor que envían la misma respuesta a muchos clientes deben usar por referencia, por lo que solo hay una copia de la respuesta en el servidor.</span><span class="sxs-lookup"><span data-stu-id="49a16-108">Server applications that send the same reply to many clients should use by reference, so there is only one copy of the reply on the server.</span></span> <span data-ttu-id="49a16-109">Por ejemplo, en una aplicación de actualización de software, el cliente cargaría su configuración de software en la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="49a16-109">For example, in a software update application, the client would upload its software configuration to the server application.</span></span> <span data-ttu-id="49a16-110">La aplicación de servidor determina qué paquete necesita el cliente y envía la dirección URL del paquete a BITS.</span><span class="sxs-lookup"><span data-stu-id="49a16-110">The server application determines which package the client needs and sends the URL of the package to BITS.</span></span> <span data-ttu-id="49a16-111">A continuación, BITS descarga el paquete como respuesta.</span><span class="sxs-lookup"><span data-stu-id="49a16-111">Then, BITS downloads the package as the reply.</span></span>

<span data-ttu-id="49a16-112">Las aplicaciones de servidor que generan respuestas únicas para cada cliente deben usar por valor.</span><span class="sxs-lookup"><span data-stu-id="49a16-112">Server applications that generate unique replies for each client should use by value.</span></span> <span data-ttu-id="49a16-113">Por ejemplo, una aplicación de servidor que admita la compra de archivos de música necesitaría enviar un archivo de música firmado al cliente.</span><span class="sxs-lookup"><span data-stu-id="49a16-113">For example, a server application that supports the purchase of music files would need to send a signed music file to the client.</span></span> <span data-ttu-id="49a16-114">Dado que el archivo de música firmado es único para el cliente, la aplicación de servidor no lo almacenaría en el servidor.</span><span class="sxs-lookup"><span data-stu-id="49a16-114">Because the signed music file is unique to the client, the server application would not store it on the server.</span></span> <span data-ttu-id="49a16-115">Por valor también es útil para una aplicación que ya está escrita para aceptar directamente los datos de cliente web.</span><span class="sxs-lookup"><span data-stu-id="49a16-115">By value is also useful for an application that is already written to accept web client data directly.</span></span>

<span data-ttu-id="49a16-116">Para obtener más información sobre los encabezados de solicitud y respuesta utilizados entre BITS y la aplicación de servidor, vea [Protocolo de notificación para aplicaciones de servidor](notification-protocol-for-server-applications.md).</span><span class="sxs-lookup"><span data-stu-id="49a16-116">For details on the request and response headers used between BITS and your server application, see [Notification Protocol for Server Applications](notification-protocol-for-server-applications.md).</span></span>

<span data-ttu-id="49a16-117">En el ejemplo de JavaScript siguiente se muestra cómo obtener acceso a los archivos de solicitud y respuesta en una aplicación de servidor que usa la notificación de referencia (BITS pasa la ubicación de los archivos en los encabezados).</span><span class="sxs-lookup"><span data-stu-id="49a16-117">The following JavaScript example shows how to access the request and response files in a server application that uses by reference notification (BITS passes the location of the files in the headers).</span></span>


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



<span data-ttu-id="49a16-118">Si desea usar un archivo de respuesta diferente del especificado en BITS-Response-archivo de nombre de archivo, llame al método **Response. AddHeader** para agregar la dirección URL de bits-estático-respuesta, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="49a16-118">If you want to use a different response file than the one specified in BITS-Response-DataFile-Name, call the **Response.AddHeader** method to add the BITS-Static-Response-URL as shown in the following example.</span></span> <span data-ttu-id="49a16-119">Si especifica un archivo de respuesta diferente, no cree el archivo de respuesta especificado en BITS-Response-archivo de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="49a16-119">If you specify a different response file, do not create the response file specified in BITS-Response-DataFile-Name.</span></span>


```JavaScript
  Response.AddHeader "BITS-Static-Response-URL" "https://myserver/mypath/myfile"
```
 

 




