---
title: Escritura de un script para configurar el directorio virtual
description: Escritura de un script para configurar el directorio virtual
ms.assetid: 0324fbc8-1d64-454c-b021-4e010edcac8d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae23a33c2c91dc0a141c6f377daf89708499aae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993925"
---
# <a name="writing-a-script-to-configure-the-virtual-directory"></a><span data-ttu-id="79663-103">Escritura de un script para configurar el directorio virtual</span><span class="sxs-lookup"><span data-stu-id="79663-103">Writing a Script to Configure the Virtual Directory</span></span>

<span data-ttu-id="79663-104">Puede usar los valores de propiedad de IIS de BITS predeterminados para cargar un archivo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="79663-104">You can use the default BITS IIS property values to upload a file to the server.</span></span> <span data-ttu-id="79663-105">El archivo de carga se escribe en la dirección URL tal y como se especifica en el nombre de archivo remoto del trabajo.</span><span class="sxs-lookup"><span data-stu-id="79663-105">The upload file is written to the URL as specified in the remote file name of the job.</span></span> <span data-ttu-id="79663-106">Para cargar el archivo en una aplicación de servidor y recibir una respuesta, cambie la propiedad [BITSServerNotificationType](bits-iis-extension-properties.md) para enviar los datos por referencia (envía el nombre del archivo que contiene los datos) o por valor (envía los datos en el cuerpo de la solicitud).</span><span class="sxs-lookup"><span data-stu-id="79663-106">To upload the file to a server application and receive a reply, change the [BITSServerNotificationType](bits-iis-extension-properties.md) property to send the data by reference (sends the name of the file that contains the data) or by value (sends the data in the body of the request).</span></span>

<span data-ttu-id="79663-107">Para obtener una lista y una descripción de las propiedades que puede modificar, consulte [propiedades de extensión de IIS de bits](bits-iis-extension-properties.md).</span><span class="sxs-lookup"><span data-stu-id="79663-107">For a list and description of the properties that you can modify, see [BITS IIS Extension Properties](bits-iis-extension-properties.md).</span></span> <span data-ttu-id="79663-108">Use los métodos de la interfaz [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) para habilitar y deshabilitar el directorio virtual para cargas.</span><span class="sxs-lookup"><span data-stu-id="79663-108">Use the methods of the [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) interface to enable and disable the virtual directory for uploads.</span></span>

<span data-ttu-id="79663-109">En el ejemplo siguiente se muestra cómo utilizar Windows Script Host para crear, configurar y habilitar un directorio virtual de IIS para cargas de BITS.</span><span class="sxs-lookup"><span data-stu-id="79663-109">The following example shows how to use Windows Script Host to create, configure, and enable an IIS virtual directory for BITS uploads.</span></span>


```JScript
if (WScript.Arguments.length < 2)
{
    WScript.Echo("Usage: bitsvdir virtual_directory local_directory");
    WScript.Quit(1);
}

VirtualDirectoryName = WScript.Arguments(0);
LocalDirectoryName = WScript.Arguments(1);

ServerObj = GetObject("IIS://LocalHost/W3SVC/1/ROOT");
VirtualDir = ServerObj.Create("IIsWebVirtualDir", VirtualDirectoryName );

VirtualDir.Path = LocalDirectoryName;
VirtualDir.AppIsolated = 0;
VirtualDir.AccessScript = true;
VirtualDir.AccessRead = false;
VirtualDir.AccessWrite = false;
VirtualDir.SetInfo();

//Set BITS specific IIS configuration settings
VirtualDir.EnableBITSUploads();
VirtualDir.BITSMaximumUploadSize = "4294967296";
VirtualDir.SetInfo();

WScript.Echo( "Created virtual directory " + VirtualDirectoryName + 
              " with a local directory of " + LocalDirectoryName );
WScript.Quit( 0 );
```



<span data-ttu-id="79663-110">Para cambiar el ejemplo anterior para cargar los datos en una aplicación de servidor, agregue el código siguiente antes de **SetInfo**.</span><span class="sxs-lookup"><span data-stu-id="79663-110">To change the previous example to upload the data to a server application, add the following code before **SetInfo**.</span></span>


```JScript
VirtualDir.BITSServerNotificationType = 1;
VirtualDir.BITSServerNotificationURL = "https://myserver/mypath/myasp.asp";
```



<span data-ttu-id="79663-111">La ubicación del archivo de carga se pasa a la aplicación de servidor, myasp. asp, en el encabezado BITS-solicitud-archivo de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="79663-111">The location of the upload file is passed to the server application, myasp.asp, in the BITS-Request-DataFile-Name header.</span></span> <span data-ttu-id="79663-112">Para recibir el archivo de carga en el cuerpo de la solicitud, establezca la propiedad [BITSServerNotificationType](bits-iis-extension-properties.md) en 2.</span><span class="sxs-lookup"><span data-stu-id="79663-112">To receive the upload file in the body of the request, set the [BITSServerNotificationType](bits-iis-extension-properties.md) property to 2.</span></span>

<span data-ttu-id="79663-113">Para obtener información sobre cómo recibir los datos de carga en la aplicación de servidor, consulte [usar encabezados de solicitud/respuesta de notificación de bits](using-bits-notification-request-response-headers.md).</span><span class="sxs-lookup"><span data-stu-id="79663-113">For information on receiving the upload data in your server application, see [Using BITS Notification Request/Response Headers](using-bits-notification-request-response-headers.md).</span></span>

 

 




