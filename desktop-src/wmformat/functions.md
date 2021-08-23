---
title: Funciones del SDK de Windows Media Format
description: Functions
ms.assetid: 10fa8f96-8030-4727-af5d-7c06229d05d8
keywords:
- Windows SDK de formato multimedia, funciones
- Formato de sistemas avanzados (ASF), funciones
- ASF (formato de sistemas avanzados), funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560756451ee2f5b49d26b5611b38a40a45cac7643b101fdbe8ae492386901689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708265"
---
# <a name="windows-media-format-sdk-functions"></a>Funciones del SDK de Windows Media Format

El SDK Windows Media Format incluye funciones para crear objetos y funciones auxiliares para simplificar algunos procedimientos.

Este SDK admite las siguientes funciones para la creación inicial de objetos. Si un objeto no aparece a continuación, debe crearlo mediante una interfaz de otro objeto. Para más información, consulte [Objetos](objects.md).



| Función                                                                             | Descripción                                                                                                                                             |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMCheckURLExtension**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlextension)                                   | Examina la extensión de nombre de archivo en la dirección URL o el nombre de archivo que se pasa como argumento.                                                               |
| [**WMCheckURLScheme**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlscheme)                                         | Examina un protocolo de red y lo compara con una lista interna de esquemas admitidos.                                                                    |
| [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer)                             | Crea un objeto de restaurador de copia de seguridad.                                                                                                                       |
| [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))                                   | Encapsula los certificados del usuario en un objeto .                                                                                                           |
| [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration)                     | Crea un objeto de registro de dispositivos.                                                                                                                   |
| [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)                           | Crea un objeto transcryptor drm.                                                                                                                      |
| [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)                                             | Crea un objeto del editor de metadatos.                                                                                                                       |
| [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)                                           | Crea un objeto indexador.                                                                                                                              |
| [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent)             | Crea un objeto de agente de revocación de licencias.                                                                                                              |
| [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)                             | Crea un objeto de administrador de perfiles.                                                                                                                       |
| [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)                                             | Crea un objeto de lector.                                                                                                                                |
| [**WMCreateSecureChannel**](/previous-versions/windows/desktop/api/Wmsecure/nf-wmsecure-wmcreatesecurechannel)                               | Crea un objeto que implementa [**IWMSecureChannel.**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)                                                                         |
| [**WMCreateSecureChannel \_ Certified**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_certified)          | Crea un objeto que implementa [**IWMSecureChannel.**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)                                                                         |
| [**WMCreateSecureChannel \_ Certified \_ DES**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_certified_des) | Crea un objeto que implementa [**IWMSecureChannel**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel).                                                                        |
| [**WMCreateSecureChannel \_ DES**](/previous-versions/windows/desktop/api/wmsecure/nf-wmsecure-wmcreatesecurechannel_des)                      | Crea un objeto que implementa [**IWMSecureChannel.**](/previous-versions/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel)                                                                         |
| [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)                                     | Crea un objeto de lector sincrónico.                                                                                                                    |
| [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)                                             | Crea un objeto de escritor.                                                                                                                                |
| [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)                             | Crea un objeto de receptor de archivo de escritura.                                                                                                                      |
| [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)                       | Crea un objeto de receptor de red de escritor.                                                                                                                   |
| [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)                             | Crea un objeto receptor de inserción de escritor.                                                                                                                      |
| [**WMIsAvailableOffline**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmisavailableoffline)                                 | Comprueba que un archivo ASF se puede reproducir desde una copia almacenada en caché.                                                                                             |
| [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected)                                 | Comprueba si hay contenido protegido con DRM en un archivo.                                                                                                                |
| [**WMValidateData**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmvalidatedata)                                             | Comprueba que los datos del principio de un archivo son coherentes con la sección de encabezado de un tipo de archivo compatible con el SDK Windows Media Format. |



 

Las siguientes funciones proporcionan accesos directos cómodos para analizar archivos.



| Función                                             | Descripción                                                                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMCheckURLExtension**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlextension)   | Intenta determinar si los objetos del SDK de formato multimedia de Windows se pueden leer en función de la extensión de nombre de archivo.              |
| [**WMCheckURLScheme**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmcheckurlscheme)         | Determina si los objetos del SDK de formato multimedia de Windows admiten un protocolo de red.                                           |
| [**WMIsAvailableOffline**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmisavailableoffline) | Determina si un archivo está disponible para la reproducción sin conexión.                                                                                 |
| [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected) | Comprueba si hay contenido protegido con DRM en un archivo.                                                                                                     |
| [**WMValidateData**](/previous-versions/windows/desktop/api/wmsdkvalidate/nf-wmsdkvalidate-wmvalidatedata)             | Intenta determinar si los objetos del SDK de formato multimedia de Windows pueden leer un archivo mediante el análisis de datos al principio del archivo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 
