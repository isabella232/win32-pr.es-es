---
title: Escribir un script para configurar el directorio virtual
description: Escribir un script para configurar el directorio virtual
ms.assetid: 0324fbc8-1d64-454c-b021-4e010edcac8d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9ea1de5a0b9f7be9598a4011cbb6cd76f49e6d4bcc3d468093be1479ee2b59e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004605"
---
# <a name="writing-a-script-to-configure-the-virtual-directory"></a>Escribir un script para configurar el directorio virtual

Puede usar los valores de propiedad de IIS bits predeterminados para cargar un archivo en el servidor. El archivo de carga se escribe en la dirección URL como se especifica en el nombre de archivo remoto del trabajo. Para cargar el archivo en una aplicación de servidor y recibir una respuesta, cambie la propiedad [BITSServerNotificationType](bits-iis-extension-properties.md) para enviar los datos por referencia (envía el nombre del archivo que contiene los datos) o por valor (envía los datos en el cuerpo de la solicitud).

Para obtener una lista y una descripción de las propiedades que puede modificar, vea [Bits IIS Extension Properties](bits-iis-extension-properties.md). Use los métodos de [**la interfaz IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) para habilitar y deshabilitar el directorio virtual para las cargas.

En el ejemplo siguiente se muestra cómo usar Windows host de script para crear, configurar y habilitar un directorio virtual de IIS para cargas de BITS.


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



Para cambiar el ejemplo anterior para cargar los datos en una aplicación de servidor, agregue el código siguiente antes **de SetInfo**.


```JScript
VirtualDir.BITSServerNotificationType = 1;
VirtualDir.BITSServerNotificationURL = "https://myserver/mypath/myasp.asp";
```



La ubicación del archivo de carga se pasa a la aplicación de servidor, myasp.asp, en el encabezado BITS-Request-DataFile-Name. Para recibir el archivo de carga en el cuerpo de la solicitud, establezca la [propiedad BITSServerNotificationType](bits-iis-extension-properties.md) en 2.

Para obtener información sobre cómo recibir los datos de carga en la aplicación de servidor, consulte Uso de encabezados de [solicitud/respuesta de notificación de BITS.](using-bits-notification-request-response-headers.md)

 

 




