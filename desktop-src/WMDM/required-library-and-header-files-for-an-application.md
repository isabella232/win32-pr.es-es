---
title: Archivos de encabezado y biblioteca necesarios para una aplicación
description: Archivos de encabezado y biblioteca necesarios para una aplicación
ms.assetid: 922627d5-03a8-4b5b-be00-6f2c3500dd66
keywords:
- Windows Media Administrador de dispositivos, bibliotecas
- Administrador de dispositivos, bibliotecas
- Guía de programación, bibliotecas
- aplicaciones de escritorio, bibliotecas
- crear aplicaciones de Windows Media Administrador de dispositivos, bibliotecas
- libraries
- Administrador de dispositivos de Windows Media, archivos de encabezado
- Administrador de dispositivos, archivos de encabezado
- Guía de programación, archivos de encabezado
- aplicaciones de escritorio, archivos de encabezado
- crear aplicaciones de Windows Media Administrador de dispositivos, archivos de encabezado
- archivos de encabezado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a4a8a04ee6c3fe603d52139e83f81a49d78dc45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075851"
---
# <a name="required-library-and-header-files-for-an-application"></a>Archivos de encabezado y biblioteca necesarios para una aplicación

En esta sección se enumeran las bibliotecas, los archivos de encabezado o los archivos IDL que deberá incluir para desarrollar una aplicación o un complemento de Windows Media Administrador de dispositivos. Como se mencionó en [compilar los archivos IDL suministrados con el SDK](compiling-the-idl-files-supplied-with-the-sdk.md), el SDK incluye archivos IDL y archivos de encabezado precompilados, y la aplicación puede usar cualquiera de los dos. (Tenga en cuenta que algunos archivos de encabezado no tienen los archivos IDL correspondientes y no se pueden crear usted mismo). Si va a compilar sus propios archivos IDL, incluya las dependencias enumeradas en compilar los archivos IDL suministrados con el SDK.

No todas las aplicaciones requerirán todos los archivos; Lea la descripción para saber si la aplicación requiere un archivo.



| Encabezado o biblioteca pregenerados       | IDL equivalente                                | Descripción                                                                                                                                                                                                                                               |
|----------------------------------|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp. lib                     | ninguno                                          | Requerido por todas las aplicaciones. Contiene objetos de Administrador de dispositivos de Windows Media.                                                                                                                                                                              |
| wmvcore. lib                      | ninguno                                          | Lo requieren las aplicaciones que usan objetos o funciones del SDK de Windows Media Format.                                                                                                                                                                          |
| initguid. h                       | ninguno (encabezado del SDK de la plataforma)                    | Necesario para que todas las aplicaciones definan los valores de **GUID** mediante el archivo Mswmdm. h creado previamente. Debe incluir initguid. h una vez y solo una vez en el proyecto. Este encabezado vuelve a definir la macro **definir \_ GUID** para evitar problemas de nomenclatura de **GUID** externos. |
| mmreg. h                          | ninguno (encabezado del SDK de la plataforma)                    | Lo requieren las aplicaciones que hacen referencia a varias definiciones de formato de Windows Media estándar, como **WAVEFORMATEX**.                                                                                                                                      |
| mswmdm. h                         | WMDM. idlicomponentauthenticate. idl<br/> | Requerido por todas las aplicaciones. Define todas las interfaces de la aplicación, así como estructuras, metadatos, error y otras constantes.                                                                                                                        |
| SAC. h                            | ninguno                                          | Requerido por todas las aplicaciones. Define los protocolos de SAC.                                                                                                                                                                                                      |
| SCClient. h                       | ninguno                                          | Requerido por todas las aplicaciones. Declara la clase [CSecureChannelClient](csecurechannelclient-class.md) .                                                                                                                                                  |
| wmdmlog. hwmdmlog. \_ c<br/> | Wmdmlog. idl                                   | Lo requieren las aplicaciones que usan la interfaz [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) .                                                                                                                                                                       |
| wmdrmdeviceapp. h                 | WMDRMDeviceApp. idl                            | Lo requieren las aplicaciones o los complementos que actualizan los componentes de DRM o los recuentos de las métricas en los dispositivos.                                                                                                                                                          |
| wmsdk. h                          | ninguno (proporcionado por el SDK de Windows Media Format)   | Se requiere para las aplicaciones que utilizan los métodos del SDK de Windows Media Format.                                                                                                                                                                                      |
| MtpExt. h                         | ninguno                                          | Se requiere para las aplicaciones que llaman a [**IWMDMDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) en dispositivos MTP. Define varias constantes y estructuras MTP estándar.                                                                          |
| Clave. c                            | ninguno                                          | Define una clave y un certificado de Microsoft. La versión suministrada con el SDK incluye una clave ficticia de prueba que permitirá el uso de archivos de Windows Media protegidos no DRM.                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 





