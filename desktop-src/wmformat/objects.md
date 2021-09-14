---
title: Objectos (SDK de Windows Media Format 11)
description: Objetos
ms.assetid: f884e115-d41a-4f36-bcef-dfaef78510af
keywords:
- Windows SDK de formato multimedia, objetos
- Formato de sistemas avanzados (ASF), objetos
- ASF (formato de sistemas avanzados), objetos
- objects,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d73672891395d6491009e1c62fac1f9eb81dfe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266983"
---
# <a name="objects-windows-media-format-11-sdk"></a>Objectos (SDK de Windows Media Format 11)

El SDK Windows Media Format usa varios objetos para leer, escribir, editar e indexar archivos ASF, y para crear y editar perfiles. Cada objeto admite varias interfaces. Algunas interfaces se admiten en varios objetos. En estos casos, las diferencias en la implementación se de abordan en la sección de referencia de la interfaz .

Los objetos del SDK Windows Media Format son compatibles con COM. Para facilitar el desarrollo, cada objeto tiene una función o un método de creación asociados. Debe crear objetos mediante la función o el método de creación en lugar de usar manualmente la función COM **CoCreateInstance**.

Algunas interfaces tienen un número anexado a sus nombres, como **IWMProfile2** e **IWMWriter3**. En cada caso, las versiones numeradas heredan todos los métodos de las versiones anteriores y agregan nueva funcionalidad.

En cada página de objeto de esta referencia, las interfaces incluidas en el objeto COM principal aparecen en primer lugar, seguidas de las interfaces de devolución de llamada que debe implementar la aplicación.

En la tabla siguiente se enumeran los objetos admitidos por este SDK con una descripción de la funcionalidad de cada uno de ellos y la función utilizada para crearlo.



| Object                                                          | Descripción                                                                                                                                              | Función de creación                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Restaurador de copias de seguridad](backup-restorer-object.md)                   | Realiza copias de seguridad de licencias, normalmente en medios extraíbles y, a continuación, restaura esas licencias en un equipo diferente.                                           | [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer)                 |
| [Registro de dispositivos](device-registration-object.md)           | Administra la base de datos de registro de dispositivos, que contiene entradas para dispositivos de reproducción multimedia que están disponibles a través de una conexión de red.             | [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration)         |
| [DRM Transcryptor](drm-transcryptor-object.md)                 | Convierte los datos multimedia protegidos con DRM en un flujo de datos que se puede enviar a dispositivos que usan el protocolo DRM 10 de Windows Media para dispositivos de red. | [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)               |
| [Indizador](indexer-object.md)                                   | Crea un índice para los archivos ASF para habilitar la búsqueda en archivos con secuencias de vídeo.                                                                            | [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)                               |
| [Agente de revocación de licencias](license-revocation-agent-object.md) | Administra la revocación de licencias.                                                                                                                              | [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) |
| [Editor de metadatos](metadata-editor-object.md)                   | Edita los metadatos en un encabezado de archivo ASF.                                                                                                                    | [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)                                 |
| [Administrador de perfiles](profile-manager-object.md)                   | Proporciona interfaces para crear, cargar y guardar perfiles. Se requiere un perfil para escribir un archivo ASF.                                                      | [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)                 |
| [Lector](reader-object.md)                                     | Lee archivos ASF. Este objeto usa un modelo de llamada asincrónica para sus operaciones.                                                                      | [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)                                 |
| [Lector sincrónico](synchronous-reader-object.md)             | Lee archivos ASF mediante llamadas sincrónicas.                                                                                                                 | [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)                         |
| [Escritor](writer-object.md)                                     | Escribe archivos ASF.                                                                                                                                        | [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)                                 |
| [Receptor de archivos de escritor](writer-file-sink-object.md)                 | Controla los archivos ASF escritos por el objeto de escritor.                                                                                                         | [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)                 |
| [Receptor de red del escritor](writer-network-sink-object.md)           | Controla el streaming de red en vivo de archivos ASF escritos por el objeto de escritor.                                                                               | [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)           |
| [Receptor de inserción de escritor](writer-push-sink-object.md)                 | Controla la entrega de contenido de streaming a los servidores de publicación.                                                                                            | [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)                 |



 

En la tabla siguiente se enumeran los objetos que dependen de otros objetos. Estos objetos se crean mediante métodos de objetos existentes.



| Object                                                        | Descripción                                                                                                                                                                                                                                                                                                                           | Método de creación                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uso compartido de ancho de banda](bandwidth-sharing-object.md)             | Administra la información de uso compartido de ancho de banda en un perfil. Puede haber más de un objeto de uso compartido de ancho de banda para un perfil. Hay diferentes métodos para crear un objeto de uso compartido de ancho de banda en función de si desea crear un nuevo objeto de uso compartido de ancho de banda o acceder a uno existente.                                           | [**IWMProfile3::CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) O<br/> [**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)<br/>                                                                                                                                                                                                                                      |
| [Buffer](buffer-object.md)                                   | Contiene un ejemplo multimedia y las extensiones de unidad de datos asociadas. Se usa para escribir y leer ejemplos.                                                                                                                                                                                                                           | [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) O<br/> [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex)<br/> O BIEN<br/> [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex)<br/> O BIEN<br/> Creado automáticamente por el objeto lector o el objeto de lector sincrónico para la entrega de ejemplo.<br/> |
| [Propiedades de medios de entrada](input-media-properties-object.md)   | Administra las propiedades de una entrada. Puede existir un objeto de propiedades de entrada para cada entrada.                                                                                                                                                                                                                                             | [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)                                                                                                                                                                                                                                                                                                                                                                      |
| [Exclusión mutua](mutual-exclusion-object.md)               | Administra la información de exclusión mutua en un perfil. Los usos comunes para la exclusión mutua son contenido de velocidad de bits múltiple y resaltes en varios idiomas. Hay distintos métodos para crear un objeto de exclusión mutua en función de si desea crear un nuevo objeto de exclusión mutua o acceder a uno existente.         | [**IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) O<br/> [**IWMProfile::GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)<br/>                                                                                                                                                                                                                                              |
| [Propiedades de medios de salida](output-media-properties-object.md) | Administra las propiedades de una salida. Puede existir un objeto de propiedades de medios de salida para cada salida. El lector o el lector sincrónico pueden crear estos objetos.                                                                                                                                                            | [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) O<br/> [**IWMSyncReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)<br/>                                                                                                                                                                                                                                                                      |
| [Perfil](profile-object.md)                                 | Contiene los datos de un perfil mientras se manipulan. Los objetos de perfil se crean cada vez que es necesario manipular el perfil. Hay diferentes métodos para crear un objeto de perfil en función de si desea crear un nuevo perfil o acceder a uno existente.                                                  | [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) O<br/> [**IWMProfileManager::LoadProfileByData**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)<br/> O BIEN<br/> [**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)<br/> O BIEN<br/> [**IWMProfileManager::LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)<br/>          |
| [Configuración de flujo](stream-configuration-object.md)       | Administra las propiedades de una secuencia dentro de un perfil. Los objetos de configuración de secuencias crean objetos de secuencia cada vez que necesite acceder a la información sobre una secuencia. Hay diferentes métodos para crear un objeto de configuración de flujo en función de si desea crear una nueva secuencia o acceso y una existente. | [**IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream) O<br/> [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)<br/> O BIEN<br/> [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)<br/>                                                                                                                                                                                   |
| [Priorización de secuencias](stream-prioritization-object.md)     | Mantiene la lista de prioridad de flujo para un perfil. Las secuencias se descartarán en orden de prioridad creciente si el ancho de banda disponible está restringido. Solo puede haber un objeto de priorización de secuencias en un perfil.                                                                                                                  | [**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 





