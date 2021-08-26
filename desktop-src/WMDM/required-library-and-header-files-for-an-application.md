---
title: Archivos de encabezado y biblioteca necesarios para una aplicación
description: Archivos de encabezado y biblioteca necesarios para una aplicación
ms.assetid: 922627d5-03a8-4b5b-be00-6f2c3500dd66
keywords:
- Windows Bibliotecas Administrador de dispositivos,bibliotecas
- Administrador de dispositivos,libraries
- guía de programación, bibliotecas
- aplicaciones de escritorio, bibliotecas
- crear Windows aplicaciones Administrador de dispositivos multimedia, bibliotecas
- libraries
- Windows Archivos Administrador de dispositivos, archivos de encabezado
- Administrador de dispositivos,archivos de encabezado
- guía de programación, archivos de encabezado
- aplicaciones de escritorio, archivos de encabezado
- crear Windows de Administrador de dispositivos, archivos de encabezado
- archivos de encabezado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b6630f4ff752b53ed69633d1e63a62093e4a4fbd16f65ccb1cc709aae120a07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863075"
---
# <a name="required-library-and-header-files-for-an-application"></a>Archivos de encabezado y biblioteca necesarios para una aplicación

En esta sección se enumeran las bibliotecas, los archivos de encabezado o los archivos IDL que deberá incluir para desarrollar una aplicación o complemento de Windows Media Administrador de dispositivos. Como se mencionó en Compilación de los archivos [IDL](compiling-the-idl-files-supplied-with-the-sdk.md)proporcionados con el SDK , el SDK incluye archivos IDL y archivos de encabezado precompilado, y la aplicación puede usar cualquiera de ellos. (Tenga en cuenta que algunos archivos de encabezado no tienen los archivos IDL correspondientes y no puede compilarlos usted mismo). Si compila sus propios archivos IDL, incluya las dependencias enumeradas en Compilación de los archivos IDL proporcionados con el SDK.

No todas las aplicaciones requerirán todos los archivos; lea la descripción para saber si la aplicación requiere un archivo.



| Encabezado o biblioteca precompilado       | IDL equivalente                                | Descripción                                                                                                                                                                                                                                               |
|----------------------------------|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp.lib                     | ninguno                                          | Requerido por todas las aplicaciones. Contiene Windows objetos Administrador de dispositivos multimedia.                                                                                                                                                                              |
| wmvcore.lib                      | ninguno                                          | Lo requieren las aplicaciones que usan Windows o funciones del SDK de formato multimedia.                                                                                                                                                                          |
| initguid.h                       | none (encabezado del SDK de plataforma)                    | Lo requieren todas las aplicaciones para definir los **valores GUID** mediante el archivo Mswmdm.h creado previamente. Debe incluir initguid.h una sola vez en el proyecto. Este encabezado redefine la macro **\_ DEFINE GUID** para evitar problemas **de nomenclatura de GUID** externos. |
| mmreg.h                          | none (encabezado del SDK de plataforma)                    | Requerido por las aplicaciones que hacen referencia a varias definiciones Windows formato multimedia estándar, como **FORMA DE ONDAATEX.**                                                                                                                                      |
| mswmdm.h                         | WMDM.idlicomponentauthenticate.idl<br/> | Requerido por todas las aplicaciones. Define todas las interfaces de aplicación, así como estructuras, metadatos, errores y otras constantes.                                                                                                                        |
| sac.h                            | ninguno                                          | Requerido por todas las aplicaciones. Define los protocolos SAC.                                                                                                                                                                                                      |
| scclient.h                       | ninguno                                          | Requerido por todas las aplicaciones. Declara la [clase CSecureChannelClient.](csecurechannelclient-class.md)                                                                                                                                                  |
| wmdmlog.hwmdmlog \_ i.c<br/> | Wmdmlog.idl                                   | Requerido por las aplicaciones que usan la [**interfaz IWMDMLogger.**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger)                                                                                                                                                                       |
| wmdrmdeviceapp.h                 | WMDRMDeviceApp.idl                            | Requerido por las aplicaciones o complementos que actualizan componentes DRM o recuentos de reproducción de medidores en los dispositivos.                                                                                                                                                          |
| wmsdk.h                          | none (proporcionado por Windows SDK de formato multimedia)   | Se requiere para las aplicaciones que usan Windows DEL SDK de formato multimedia.                                                                                                                                                                                      |
| MtpExt.h                         | ninguno                                          | Necesario para las aplicaciones que [**llaman a IWMDMDevice3::D eviceIoControl**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) en dispositivos MTP. Define varias constantes y estructuras estándar de MTP.                                                                          |
| Key.c                            | ninguno                                          | Define una clave y un certificado de Microsoft. La versión que se incluye con el SDK incluye una clave ficticia de prueba que permitirá el uso de archivos multimedia no protegidos Windows DRM.                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 





