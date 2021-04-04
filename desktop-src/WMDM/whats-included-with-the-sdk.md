---
title: Qué se incluye con el SDK
description: Qué se incluye con el SDK
ms.assetid: c17de30b-d4b4-4698-accf-721b6c267769
keywords:
- Windows Media Administrador de dispositivos, kit de desarrollo de software (SDK)
- Administrador de dispositivos, kit de desarrollo de software (SDK)
- SDK de Administrador de dispositivos de Windows Media
- SDK de Administrador de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ac1698336e1cf3966e3ab69ad3ae7c46f95e469
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075350"
---
# <a name="whats-included-with-the-sdk"></a>Qué se incluye con el SDK

En la tabla siguiente se describe el contenido del SDK de Administrador de dispositivos de Windows Media. Todos los archivos o carpetas se describen en relación con la ruta de instalación del SDK raíz.



| Archivo                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM\\                     | Carpeta de nivel superior del SDK de Administrador de dispositivos de Windows Media. Esta carpeta incluye el archivo make para compilar todas las aplicaciones de ejemplo.                                                                                                                                                                                                                                                                                                              |
| IDL\\                      | Carpeta que contiene todos los archivos IDL necesarios para crear los encabezados necesarios para los métodos de Administrador de dispositivos de Windows Media. Sin embargo, en lugar de usar estos archivos, puede usar los archivos de encabezado proporcionados en la \\ carpeta Inc.<br/> Para ver una lista de estos archivos IDL y obtener información sobre qué archivos de encabezado se compilan a partir de qué archivos IDL, vea [compilar los archivos IDL proporcionados con el SDK](compiling-the-idl-files-supplied-with-the-sdk.md).<br/> |
| Inc \\ ....<br/>       | Carpeta que incluye todos los encabezados que definen las interfaces y los tipos de datos de este SDK.                                                                                                                                                                                                                                                                                                                                                         |
| mswmdm. h                   | Define todas las interfaces de aplicación, las interfaces del proveedor de servicios, las interfaces del proveedor de contenido seguro, los códigos de error, las constantes, las estructuras y la interfaz [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .                                                                                                                                                                                                                            |
| mswmdm \_ c                | Define la interfaz [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) .                                                                                                                                                                                                                                                                                                                                                                               |
| MtpExt. h                   | Define las estructuras específicas de MTP necesarias para las aplicaciones que llaman a [**IWMDMDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol).                                                                                                                                                                                                                                                                                                            |
| Resource. h                 | Define varias constantes de recursos que usan los ejemplos del SDK.                                                                                                                                                                                                                                                                                                                                                                                         |
| SAC. h                      | Define los datos de canal autenticados seguros requeridos por todas las aplicaciones y proveedores de servicios.                                                                                                                                                                                                                                                                                                                                                       |
| SCClient. h                 | Define la clase [CSecureChannelClient](csecurechannelclient-class.md) requerida por todas las aplicaciones.                                                                                                                                                                                                                                                                                                                                              |
| scserver. h                 | Define la clase [CSecureChannelServer](csecurechannelserver-class.md) requerida por todos los proveedores de servicios.                                                                                                                                                                                                                                                                                                                                         |
| WMDM \_ ver. h                | Información de versión opcional sobre el Administrador de dispositivos de Windows Media.                                                                                                                                                                                                                                                                                                                                                                                    |
| wmdmlog. h, wmdmlog \_ i. c    | Se requiere para las aplicaciones o proveedores de servicios que usan la interfaz [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) .                                                                                                                                                                                                                                                                                                                                           |
| wmdrmdeviceapp. h           | Se requiere para las aplicaciones que controlan la medición de contenido (vea [uso del contenido de medición](metering-content-usage.md)).                                                                                                                                                                                                                                                                                                                                  |
| wmsstd. h                   | Define macros auxiliares utilizadas por los ejemplos del SDK.                                                                                                                                                                                                                                                                                                                                                                                                      |
| obj\\                      | Carpeta que contiene las bibliotecas de Windows Media Administrador de dispositivos.                                                                                                                                                                                                                                                                                                                                                                                       |
| mssachlp. lib               | Biblioteca estática requerida por todos los proveedores de servicios y aplicaciones de Windows Media Administrador de dispositivos.                                                                                                                                                                                                                                                                                                                                                 |
| drmcrypto. lib              | Biblioteca estática requerida por todas las aplicaciones de Windows Media Administrador de dispositivos y proveedores de servicios que usan DRM.                                                                                                                                                                                                                                                                                                                                    |
| mdsp \\ ....<br/>      | Carpeta que contiene el código para un proveedor de servicios de ejemplo. Para obtener información sobre este ejemplo, incluido cómo compilarlo y ejecutarlo, vea [proveedor de servicios de ejemplo](sample-service-provider.md).                                                                                                                                                                                                                                                    |
| aplicaciones \\ ....<br/>      | Carpeta que contiene dos subcarpetas que contienen dos mitades del código para una aplicación de escritorio de ejemplo que se proporciona con el SDK. Para obtener información sobre este ejemplo, incluido cómo compilarlo, vea [aplicación de escritorio de ejemplo](sample-desktop-application.md).                                                                                                                                                                                      |
| DeviceKit \\ ....<br/> | Carpeta que contiene un conjunto de herramientas para probar el dispositivo portátil con Windows Media Administrador de dispositivos 11. Las pruebas incluyen la enumeración y la transferencia de archivos y dispositivos, las capacidades DRM y el cumplimiento MTP. Estas herramientas tienen su propio archivo de documentación.                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción**](getting-started.md)
</dt> </dl>

 

 





