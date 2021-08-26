---
title: Qué se incluye con el SDK
description: Qué se incluye con el SDK
ms.assetid: c17de30b-d4b4-4698-accf-721b6c267769
keywords:
- Windows Media Administrador de dispositivos,software development kit (SDK)
- Administrador de dispositivos,software development kit (SDK)
- Windows SDK de Administrador de dispositivos multimedia
- Administrador de dispositivos SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36e621ac4de7fee296bf9d2c3ffb4e1d357824510b37a6ded73efd66b91f38d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004905"
---
# <a name="whats-included-with-the-sdk"></a>Qué se incluye con el SDK

En la tabla siguiente se describe el contenido del SDK Windows Media Administrador de dispositivos. Todos los archivos o carpetas se describen en relación con la ruta de instalación del SDK raíz.



| Archivo                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM\\                     | Carpeta de nivel superior para el SDK Windows Media Administrador de dispositivos. Esta carpeta incluye el archivo Make para compilar todas las aplicaciones de ejemplo.                                                                                                                                                                                                                                                                                                              |
| Idl\\                      | Carpeta que contiene todos los archivos IDL necesarios para compilar los encabezados necesarios para Windows métodos Administrador de dispositivos multimedia. Sin embargo, en lugar de usar estos archivos, puede usar los archivos de encabezado proporcionados en la carpeta \\ inc.<br/> Para ver una lista de estos archivos IDL y saber qué archivos de encabezado se compilan a partir de los archivos IDL, consulte Compilación de los archivos IDL proporcionados con el [SDK.](compiling-the-idl-files-supplied-with-the-sdk.md)<br/> |
| \\inc......<br/>       | Carpeta que incluye todos los encabezados que definen las interfaces y los tipos de datos de este SDK.                                                                                                                                                                                                                                                                                                                                                         |
| mswmdm.h                   | Define todas las interfaces de aplicación, interfaces de proveedor de servicios, interfaces de proveedor de contenido seguro, códigos de error, constantes, estructuras y la [**interfaz IComponentAuthenticate.**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)                                                                                                                                                                                                                            |
| mswmdm \_ i.c                | Define la [**interfaz IWMDMNotification.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                                                                                                                                                                                                                                                                                               |
| MtpExt.h                   | Define las estructuras específicas de MTP necesarias para las aplicaciones que [**llaman a IWMDMDevice3::D eviceIoControl**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol).                                                                                                                                                                                                                                                                                                            |
| resource.h                 | Define varias constantes de recursos que usan los ejemplos del SDK.                                                                                                                                                                                                                                                                                                                                                                                         |
| sac.h                      | Define los datos de canal autenticados seguros requeridos por todas las aplicaciones y proveedores de servicios.                                                                                                                                                                                                                                                                                                                                                       |
| scclient.h                 | Define la [clase CSecureChannelClient](csecurechannelclient-class.md) requerida por todas las aplicaciones.                                                                                                                                                                                                                                                                                                                                              |
| scserver.h                 | Define la [clase CSecureChannelServer](csecurechannelserver-class.md) requerida por todos los proveedores de servicios.                                                                                                                                                                                                                                                                                                                                         |
| wmdm \_ ver.h                | Información de versión opcional sobre Windows Media Administrador de dispositivos.                                                                                                                                                                                                                                                                                                                                                                                    |
| wmdmlog.h, wmdmlog \_ i.c    | Necesario para las aplicaciones o proveedores de servicios que usan la [**interfaz IWMDMLogger.**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger)                                                                                                                                                                                                                                                                                                                                           |
| wmdrmdeviceapp.h           | Necesario para las aplicaciones que controlan la medición de contenido (vea [Uso de contenido de medición).](metering-content-usage.md)                                                                                                                                                                                                                                                                                                                                  |
| wmsstd.h                   | Define las macros auxiliares que usan los ejemplos del SDK.                                                                                                                                                                                                                                                                                                                                                                                                      |
| Lib\\                      | Carpeta que contiene las bibliotecas Windows de Administrador de dispositivos multimedia.                                                                                                                                                                                                                                                                                                                                                                                       |
| mssachlp.lib               | La biblioteca estática requerida por todos los Windows media Administrador de dispositivos aplicaciones y proveedores de servicios.                                                                                                                                                                                                                                                                                                                                                 |
| drmcrypto.lib              | La biblioteca estática requerida por todos los Windows media Administrador de dispositivos aplicaciones y proveedores de servicios que usan DRM.                                                                                                                                                                                                                                                                                                                                    |
| mdsp \\ ......<br/>      | Carpeta que contiene el código de un proveedor de servicios de ejemplo. Para obtener información sobre este ejemplo, incluido cómo compilarlo y ejecutarlo, vea [Proveedor de servicios de ejemplo](sample-service-provider.md).                                                                                                                                                                                                                                                    |
| \\aplicaciones...<br/>      | Carpeta que contiene dos subcarpetas que contienen dos mitades del código para una aplicación de escritorio de ejemplo proporcionada con el SDK. Para obtener información sobre este ejemplo, incluido cómo compilarlo, vea [Aplicación de escritorio de ejemplo](sample-desktop-application.md).                                                                                                                                                                                      |
| \\devicekit......<br/> | Carpeta que contiene un conjunto de herramientas para probar el dispositivo portátil mediante Windows Media Administrador de dispositivos 11. Las pruebas incluyen la enumeración y transferencia de archivos y dispositivos, las funcionalidades DRM y el cumplimiento de MTP. Estas herramientas tienen su propio archivo de documentación.                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tareas iniciales**](getting-started.md)
</dt> </dl>

 

 





