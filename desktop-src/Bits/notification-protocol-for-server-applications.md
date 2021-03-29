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
# <a name="notification-protocol-for-server-applications"></a><span data-ttu-id="a2959-103">Protocolo de notificación para aplicaciones de servidor</span><span class="sxs-lookup"><span data-stu-id="a2959-103">Notification Protocol for Server Applications</span></span>

<span data-ttu-id="a2959-104">BITS usa la propiedad [BITSServerNotificationType](bits-iis-extension-properties.md) para determinar cómo envía bits el contenido del archivo de carga a la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="a2959-104">BITS uses the [BITSServerNotificationType](bits-iis-extension-properties.md) property to determine how BITS sends the contents of the upload file to the server application.</span></span> <span data-ttu-id="a2959-105">Si la propiedad BITSServerNotificationType se establece en 1, [bits pasa la ubicación del archivo de carga en un encabezado](#sending-the-location-of-the-upload-file-in-a-header).</span><span class="sxs-lookup"><span data-stu-id="a2959-105">If the BITSServerNotificationType property is set to 1, [BITS passes the location of the upload file in a header](#sending-the-location-of-the-upload-file-in-a-header).</span></span> <span data-ttu-id="a2959-106">Si la propiedad BITSServerNotificationType se establece en 2, [bits pasa el contenido del archivo de carga en el cuerpo de la solicitud](#sending-the-upload-file-in-the-body-of-the-request).</span><span class="sxs-lookup"><span data-stu-id="a2959-106">If the BITSServerNotificationType property is set to 2, [BITS passes the contents of the upload file in the body of the request](#sending-the-upload-file-in-the-body-of-the-request).</span></span>

<span data-ttu-id="a2959-107">Para obtener información detallada sobre cómo BITS controla los errores de la aplicación de servidor, consulte [control de errores de aplicaciones de servidor](#handling-server-application-errors).</span><span class="sxs-lookup"><span data-stu-id="a2959-107">For details on how BITS handles errors from the server application, see [Handling server application errors](#handling-server-application-errors).</span></span>

## <a name="sending-the-location-of-the-upload-file-in-a-header"></a><span data-ttu-id="a2959-108">Enviar la ubicación del archivo de carga en un encabezado</span><span class="sxs-lookup"><span data-stu-id="a2959-108">Sending the location of the upload file in a header</span></span>

<span data-ttu-id="a2959-109">BITS pasa la ubicación de los archivos de carga y de respuesta a la aplicación de servidor en los encabezados si la propiedad [BITSServerNotificationType](bits-iis-extension-properties.md) está establecida en 1.</span><span class="sxs-lookup"><span data-stu-id="a2959-109">BITS passes the location of the upload and reply files to the server application in the headers if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1.</span></span> <span data-ttu-id="a2959-110">La aplicación de servidor abre el archivo de carga, procesa los datos y, a continuación, genera el archivo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2959-110">The server application opens the upload file, processes the data, and then generates the reply file.</span></span> <span data-ttu-id="a2959-111">De forma predeterminada, BITS quita los archivos de carga y respuesta del servidor una vez que recibe la respuesta de la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="a2959-111">By default, BITS removes the upload and reply files from the server after it receives the response from the server application.</span></span> <span data-ttu-id="a2959-112">Para que BITS copie el archivo de carga en la ubicación especificada por el nombre de archivo remoto en el trabajo, incluya el encabezado BITS-copiar-archivo a destino en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2959-112">To have BITS copy the upload file to the location specified by the remote file name in the job, include the BITS-Copy-File-To-Destination header in your response.</span></span> <span data-ttu-id="a2959-113">Si no incluye el encabezado y desea guardar los archivos de carga y de respuesta, debe copiar los archivos de carga y de respuesta en una nueva ubicación antes de responder.</span><span class="sxs-lookup"><span data-stu-id="a2959-113">If you do not include the header and you want to save the upload and reply files, you must copy the upload and reply files to a new location before responding.</span></span> <span data-ttu-id="a2959-114">En la tabla siguiente se muestran los encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2959-114">The following table shows the request headers.</span></span>



| <span data-ttu-id="a2959-115">Encabezado de solicitud</span><span class="sxs-lookup"><span data-stu-id="a2959-115">Request header</span></span>              | <span data-ttu-id="a2959-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2959-116">Description</span></span>                                                                                |
|-----------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2959-117">BITS-original-solicitud-URL</span><span class="sxs-lookup"><span data-stu-id="a2959-117">BITS-Original-Request-URL</span></span>   | <span data-ttu-id="a2959-118">Contiene el nombre remoto especificado en el trabajo.</span><span class="sxs-lookup"><span data-stu-id="a2959-118">Contains the remote name specified in the job.</span></span>                                             |
| <span data-ttu-id="a2959-119">BITS-request-archivo de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="a2959-119">BITS-Request-DataFile-Name</span></span>  | <span data-ttu-id="a2959-120">Contiene la ruta de acceso completa a los datos cargados.</span><span class="sxs-lookup"><span data-stu-id="a2959-120">Contains the full path to the uploaded data.</span></span>                                               |
| <span data-ttu-id="a2959-121">BITS-respuesta-archivo de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="a2959-121">BITS-Response-DataFile-Name</span></span> | <span data-ttu-id="a2959-122">Contiene la ruta de acceso completa a donde BITS espera que la aplicación de servidor escriba la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2959-122">Contains the full path to where BITS expects the server application to write the response.</span></span> |



 

<span data-ttu-id="a2959-123">En la tabla siguiente se muestran los encabezados de respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2959-123">The following table shows the response headers.</span></span>



| <span data-ttu-id="a2959-124">Encabezado de respuesta</span><span class="sxs-lookup"><span data-stu-id="a2959-124">Response header</span></span>               | <span data-ttu-id="a2959-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2959-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2959-126">BITS-static-Response-URL</span><span class="sxs-lookup"><span data-stu-id="a2959-126">BITS-Static-Response-URL</span></span>      | <span data-ttu-id="a2959-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a2959-127">Optional.</span></span> <span data-ttu-id="a2959-128">Contiene la dirección URL absoluta (no especifique una dirección URL relativa) a un archivo de datos estático que se va a usar como respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2959-128">Contains the absolute URL (do not specify a relative URL) to a static data file to use as the response.</span></span> <span data-ttu-id="a2959-129">El archivo de datos estático debe ser accesible para el cliente de BITS.</span><span class="sxs-lookup"><span data-stu-id="a2959-129">The static data file must be accessible by the BITS client.</span></span> <span data-ttu-id="a2959-130">Si usa este encabezado, no cree el archivo de respuesta especificado en el encabezado de solicitud BITS-respuesta-nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="a2959-130">If you use this header, do not create the response file specified in the BITS-Response-DataFile-Name request header.</span></span> <span data-ttu-id="a2959-131">Tenga en cuenta que BITS no elimina este archivo.</span><span class="sxs-lookup"><span data-stu-id="a2959-131">Note that BITS does not delete this file for you.</span></span><br/>                                                                                                           |
| <span data-ttu-id="a2959-132">BITS-copiar-archivo a destino</span><span class="sxs-lookup"><span data-stu-id="a2959-132">BITS-Copy-File-To-Destination</span></span> | <span data-ttu-id="a2959-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a2959-133">Optional.</span></span> <span data-ttu-id="a2959-134">De forma predeterminada, si la propiedad [BITSServerNotificationType](bits-iis-extension-properties.md) se establece en 1 o 2, el servidor bits no copia el archivo de carga en la ubicación especificada por el nombre de archivo remoto en el trabajo.</span><span class="sxs-lookup"><span data-stu-id="a2959-134">By default, if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1 or 2, the BITS server does not copy the upload file to the location specified by the remote file name in the job.</span></span> <span data-ttu-id="a2959-135">Para que BITS copie el archivo en la ubicación especificada por el nombre de archivo remoto en el trabajo, envíe este encabezado de respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2959-135">To have BITS copy the file to the location specified by the remote file name in the job, send this response header.</span></span> <span data-ttu-id="a2959-136">Puede especificar cualquier valor; BITS no utiliza el valor.</span><span class="sxs-lookup"><span data-stu-id="a2959-136">You can specify any value; BITS does not use the value.</span></span> <span data-ttu-id="a2959-137">Tenga en cuenta que las carpetas de la ruta de acceso del archivo remoto deben existir.</span><span class="sxs-lookup"><span data-stu-id="a2959-137">Note that the folders in the remote file path must exist.</span></span> |



 

<span data-ttu-id="a2959-138">La siguiente solicitud muestra BITS que envían la ubicación del archivo de carga a la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="a2959-138">The following request shows BITS sending the location of the upload file to the server application.</span></span>

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

<span data-ttu-id="a2959-139">A continuación se muestra la respuesta de la aplicación de servidor a BITS; la respuesta se coloca en el archivo especificado por el encabezado de solicitud BITS-respuesta-nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="a2959-139">The following shows the server application's reply to BITS; the reply is placed in the file specified by the BITS-Response-DataFile-Name request header.</span></span>

``` syntax
HTTP/1.1 200 - OK
Content-Length: 0
```

## <a name="sending-the-upload-file-in-the-body-of-the-request"></a><span data-ttu-id="a2959-140">Envío del archivo de carga en el cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a2959-140">Sending the upload file in the body of the request</span></span>

<span data-ttu-id="a2959-141">BITS envía el archivo de carga en el cuerpo de la solicitud si la propiedad [BITSServerNotificationType](bits-iis-extension-properties.md) está establecida en 2.</span><span class="sxs-lookup"><span data-stu-id="a2959-141">BITS sends the upload file in the body of the request if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 2.</span></span> <span data-ttu-id="a2959-142">El envío del archivo de carga en el cuerpo de la solicitud permite que los scripts y las aplicaciones existentes funcionen con modificaciones mínimas.</span><span class="sxs-lookup"><span data-stu-id="a2959-142">Sending the upload file in the body of the request lets existing scripts and applications work with minimal modifications.</span></span> <span data-ttu-id="a2959-143">El archivo de carga y el archivo de respuesta se pasan en la solicitud y la respuesta, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a2959-143">The upload file and reply file are passed in the request and response, respectively.</span></span> <span data-ttu-id="a2959-144">En la tabla siguiente se muestra el encabezado de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2959-144">The following table shows the request header.</span></span>



| <span data-ttu-id="a2959-145">Encabezado de solicitud</span><span class="sxs-lookup"><span data-stu-id="a2959-145">Request header</span></span>            | <span data-ttu-id="a2959-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2959-146">Description</span></span>                                    |
|---------------------------|------------------------------------------------|
| <span data-ttu-id="a2959-147">BITS-original-solicitud-URL</span><span class="sxs-lookup"><span data-stu-id="a2959-147">BITS-Original-Request-URL</span></span> | <span data-ttu-id="a2959-148">Contiene el nombre remoto especificado en el trabajo.</span><span class="sxs-lookup"><span data-stu-id="a2959-148">Contains the remote name specified in the job.</span></span> |



 

<span data-ttu-id="a2959-149">En la tabla siguiente se muestran los encabezados de respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2959-149">The following table shows the response headers.</span></span>



| <span data-ttu-id="a2959-150">Encabezado de respuesta</span><span class="sxs-lookup"><span data-stu-id="a2959-150">Response header</span></span>               | <span data-ttu-id="a2959-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2959-151">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2959-152">BITS-static-Response-URL</span><span class="sxs-lookup"><span data-stu-id="a2959-152">BITS-Static-Response-URL</span></span>      | <span data-ttu-id="a2959-153">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a2959-153">Optional.</span></span> <span data-ttu-id="a2959-154">Contiene la dirección URL absoluta (no especifique una dirección URL relativa) a un archivo de datos estático que se va a usar como respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2959-154">Contains the absolute URL (do not specify a relative URL) to a static data file to use as the response.</span></span> <span data-ttu-id="a2959-155">El archivo de datos estático debe ser accesible para el cliente de BITS.</span><span class="sxs-lookup"><span data-stu-id="a2959-155">The static data file must be accessible by the BITS client.</span></span> <span data-ttu-id="a2959-156">Si usa este encabezado, no incluya la respuesta en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="a2959-156">If you use this header, do not include the response in the stream.</span></span> <span data-ttu-id="a2959-157">Tenga en cuenta que BITS no elimina este archivo.</span><span class="sxs-lookup"><span data-stu-id="a2959-157">Note that BITS does not delete this file for you.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="a2959-158">BITS-copiar-archivo a destino</span><span class="sxs-lookup"><span data-stu-id="a2959-158">BITS-Copy-File-To-Destination</span></span> | <span data-ttu-id="a2959-159">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a2959-159">Optional.</span></span> <span data-ttu-id="a2959-160">Si la propiedad [BITSServerNotificationType](bits-iis-extension-properties.md) se establece en 1 o 2, el servidor bits no copia el archivo de carga en la ubicación especificada por el nombre de archivo remoto en el trabajo.</span><span class="sxs-lookup"><span data-stu-id="a2959-160">If the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1 or 2, the BITS server does not copy the upload file to the location specified by the remote file name in the job.</span></span> <span data-ttu-id="a2959-161">Para que BITS copie el archivo en la ubicación especificada por el nombre de archivo remoto, envíe este encabezado de respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2959-161">To have BITS copy the file to the location specified by the remote file name, send this response header.</span></span> <span data-ttu-id="a2959-162">Puede especificar cualquier valor; BITS no utiliza el valor.</span><span class="sxs-lookup"><span data-stu-id="a2959-162">You can specify any value; BITS does not use the value.</span></span> <span data-ttu-id="a2959-163">Tenga en cuenta que las carpetas de la ruta de acceso del archivo remoto deben existir.</span><span class="sxs-lookup"><span data-stu-id="a2959-163">Note that the folders in the remote file path must exist.</span></span> |



 

<span data-ttu-id="a2959-164">La siguiente solicitud muestra BITS que pasan el archivo cargado a la aplicación de servidor en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2959-164">The following request shows BITS passing the uploaded file to the server application in the body of the request.</span></span>

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
Content-Length: 80000

80000 bytes of upload data goes here
```

<span data-ttu-id="a2959-165">La respuesta siguiente muestra la aplicación de servidor que pasa los datos de respuesta a BITS en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2959-165">The following reply shows the server application passing the reply data to BITS in the body of the response.</span></span>

``` syntax
HTTP/1.1 200 - OK
Content-Length: 100

100 bytes of reply data goes here
```

## <a name="handling-server-application-errors"></a><span data-ttu-id="a2959-166">Control de errores de aplicación de servidor</span><span class="sxs-lookup"><span data-stu-id="a2959-166">Handling server application errors</span></span>

<span data-ttu-id="a2959-167">Consulte [control de errores de aplicaciones de servidor](handling-server-application-errors.md).</span><span class="sxs-lookup"><span data-stu-id="a2959-167">See [Handling Server Application Errors](handling-server-application-errors.md).</span></span>

 

 





