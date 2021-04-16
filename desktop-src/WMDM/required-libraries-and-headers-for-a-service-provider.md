---
title: Bibliotecas y encabezados necesarios para un proveedor de servicios
description: Bibliotecas y encabezados necesarios para un proveedor de servicios
ms.assetid: 13ef830d-c1cf-4e4c-8fbd-20b5c38b9208
keywords:
- Windows Media Administrador de dispositivos, bibliotecas
- Administrador de dispositivos, bibliotecas
- Guía de programación, bibliotecas
- proveedores de servicios, bibliotecas
- crear proveedores de servicios, bibliotecas
- libraries
- Administrador de dispositivos de Windows Media, archivos de encabezado
- Administrador de dispositivos, archivos de encabezado
- Guía de programación, archivos de encabezado
- proveedores de servicios, archivos de encabezado
- crear proveedores de servicios, archivos de encabezado
- archivos de encabezado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b987d389216a3349c6797517b48c03bbb4d0f1eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357196"
---
# <a name="required-libraries-and-headers-for-a-service-provider"></a>Bibliotecas y encabezados necesarios para un proveedor de servicios

En esta sección se enumeran las bibliotecas, los archivos de encabezado o los archivos IDL que deberá incluir para desarrollar una aplicación o un complemento de Windows Media Administrador de dispositivos. Como se mencionó en [compilar los archivos IDL suministrados con el SDK](compiling-the-idl-files-supplied-with-the-sdk.md), el SDK incluye archivos IDL y archivos de encabezado precompilados, y la aplicación puede usar cualquiera de los dos. (Tenga en cuenta que algunos archivos de encabezado no tienen los archivos IDL correspondientes y no se pueden crear usted mismo). Si va a compilar sus propios archivos IDL, incluya las dependencias enumeradas en compilar los archivos IDL suministrados con el SDK.

No todas las aplicaciones requerirán todos los archivos; Lea la descripción para saber si la aplicación requiere un archivo.



| Encabezado o biblioteca pregenerados       | IDL equivalente                                                                | Descripción                                                                                                                                                                                                                                                    |
|----------------------------------|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp. lib                     | ninguno                                                                          | Requerido por todos los proveedores de servicios. Define objetos de Administrador de dispositivos de Windows Media.                                                                                                                                                                               |
| initguid. h                       | ninguno (encabezado del SDK de la plataforma)                                                    | Lo requieren todos los proveedores de servicios para definir los valores de **GUID** mediante el archivo Mswmdm. h creado previamente. Debe incluir initguid. h una vez y solo una vez en el proyecto. Este encabezado vuelve a definir la macro **definir \_ GUID** para evitar problemas de nomenclatura de **GUID** externos. |
| mswmdm. h                         | WMDM. idl<br/> WMSP. idl<br/> icomponentauthenticate. idl<br/> | Requerido por todos los proveedores de servicios. Define todas las interfaces, estructuras, metadatos, códigos de error y otras constantes del proveedor de servicios.                                                                                                                        |
| SAC. h                            | ninguno                                                                          | Requerido por todos los proveedores de servicios. Define los protocolos de SAC.                                                                                                                                                                                                      |
| scserver. h                       | ninguno                                                                          | Requerido por todos los proveedores de servicios. Declara la clase [CSecureChannelServer](csecurechannelserver-class.md) .                                                                                                                                                  |
| wmdmlog. hwmdmlog. \_ c<br/> | Wmdmlog. idl                                                                   | Lo requieren los proveedores de servicios que usan la interfaz [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) .                                                                                                                                                                       |
| wmsdk. h                          | ninguno (proporcionado por el SDK de Windows Media Format)                                   | Se requiere para los proveedores de servicios que usan los métodos del SDK de formato de Windows Media.                                                                                                                                                                                      |
| wmvcore. lib                      | ninguno                                                                          | Lo requieren los proveedores de servicios que usan objetos o funciones del SDK de Windows Media Format.                                                                                                                                                                          |
| mmreg. h                          | ninguno (encabezado del SDK de la plataforma)                                                    | Lo requieren los proveedores de servicios que hacen referencia a varias definiciones de formato de Windows Media estándar, como **WAVEFORMATEX**.                                                                                                                                      |
| MtpExt. h                         | ninguno                                                                          | Se requiere para los proveedores de servicios que administran [**IMDSPDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-deviceiocontrol) en dispositivos MTP. Define varias constantes y estructuras MTP estándar.                                                                        |
| Clave. c                            | ninguno                                                                          | Define una clave y un certificado de Microsoft. La versión suministrada con el SDK incluye una clave ficticia de prueba que permitirá el uso de archivos de Windows Media protegidos no DRM.                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un proveedor de servicios**](creating-a-service-provider.md)
</dt> </dl>

 

 





