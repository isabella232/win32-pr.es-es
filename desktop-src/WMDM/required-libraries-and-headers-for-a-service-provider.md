---
title: Bibliotecas y encabezados necesarios para un proveedor de servicios
description: Bibliotecas y encabezados necesarios para un proveedor de servicios
ms.assetid: 13ef830d-c1cf-4e4c-8fbd-20b5c38b9208
keywords:
- Windows Archivos Administrador de dispositivos,bibliotecas
- Administrador de dispositivos,libraries
- guía de programación, bibliotecas
- proveedores de servicios, bibliotecas
- crear proveedores de servicios, bibliotecas
- libraries
- Windows Archivos Administrador de dispositivos, archivos de encabezado
- Administrador de dispositivos,archivos de encabezado
- guía de programación, archivos de encabezado
- proveedores de servicios, archivos de encabezado
- crear proveedores de servicios, archivos de encabezado
- archivos de encabezado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b987d389216a3349c6797517b48c03bbb4d0f1eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967784"
---
# <a name="required-libraries-and-headers-for-a-service-provider"></a>Bibliotecas y encabezados necesarios para un proveedor de servicios

En esta sección se enumeran las bibliotecas, los archivos de encabezado o los archivos IDL que deberá incluir para desarrollar una aplicación o complemento Windows Media Administrador de dispositivos o un complemento. Como se mencionó en Compilar los archivos IDL proporcionados con el [SDK,](compiling-the-idl-files-supplied-with-the-sdk.md)el SDK incluye archivos IDL y archivos de encabezado precompilado, y la aplicación puede usar cualquiera de ellos. (Tenga en cuenta que algunos archivos de encabezado no tienen los archivos IDL correspondientes y no puede compilarlos usted mismo). Si compila sus propios archivos IDL, incluya las dependencias enumeradas en Compilación de los archivos IDL proporcionados con el SDK.

No todas las aplicaciones requerirán todos los archivos; lea la descripción para saber si la aplicación requiere un archivo.



| Encabezado o biblioteca precompilado       | IDL equivalente                                                                | Descripción                                                                                                                                                                                                                                                    |
|----------------------------------|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp.lib                     | ninguno                                                                          | Requerido por todos los proveedores de servicios. Define Windows objetos Administrador de dispositivos multimedia.                                                                                                                                                                               |
| initguid.h                       | none (encabezado del SDK de plataforma)                                                    | Requerido por todos los proveedores de servicios para definir los **valores GUID** mediante el archivo Mswmdm.h creado previamente. Debe incluir initguid.h una vez y solo una vez en el proyecto. Este encabezado redefine la macro **DEFINE \_ GUID** para evitar problemas **de nomenclatura de GUID** externos. |
| mswmdm.h                         | WMDM.idl<br/> WMSP.idl<br/> icomponentauthenticate.idl<br/> | Requerido por todos los proveedores de servicios. Define todas las interfaces, estructuras, metadatos, códigos de error y otras constantes del proveedor de servicios.                                                                                                                        |
| sac.h                            | ninguno                                                                          | Requerido por todos los proveedores de servicios. Define protocolos SAC.                                                                                                                                                                                                      |
| scserver.h                       | ninguno                                                                          | Requerido por todos los proveedores de servicios. Declara la [clase CSecureChannelServer.](csecurechannelserver-class.md)                                                                                                                                                  |
| wmdmlog.hwmdmlog \_ i.c<br/> | Wmdmlog.idl                                                                   | Requerido por los proveedores de servicios que usan [**la interfaz IWMDMLogger.**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger)                                                                                                                                                                       |
| wmsdk.h                          | none (proporcionado por el SDK Windows Media Format)                                   | Se requiere para los proveedores de servicios que usan Windows métodos del SDK de formato multimedia.                                                                                                                                                                                      |
| wmvcore.lib                      | ninguno                                                                          | Requerido por los proveedores de servicios que usan Windows o funciones del SDK de formato multimedia.                                                                                                                                                                          |
| mmreg.h                          | none (encabezado del SDK de plataforma)                                                    | Requerido por los proveedores de servicios que hacen referencia a varias definiciones Windows de formato multimedia estándar, como **ESTANDOATEX.**                                                                                                                                      |
| MtpExt.h                         | ninguno                                                                          | Se requiere para los proveedores de servicios que controlan [**IMDSPDevice3::D eviceIoControl**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-deviceiocontrol) en dispositivos MTP. Define varias constantes y estructuras estándar de MTP.                                                                        |
| Key.c                            | ninguno                                                                          | Define una clave y un certificado de Microsoft. La versión que se incluye con el SDK incluye una clave ficticia de prueba que permitirá el uso de archivos multimedia no protegidos Windows DRM.                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un proveedor de servicios**](creating-a-service-provider.md)
</dt> </dl>

 

 





