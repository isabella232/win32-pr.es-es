---
title: Objectos (SDK de Windows Media Format 11)
description: de la empresa
ms.assetid: f884e115-d41a-4f36-bcef-dfaef78510af
keywords:
- SDK de Windows Media Format, objetos
- Advanced Systems Format (ASF), objetos
- ASF (formato de sistemas avanzados), objetos
- objetos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d73672891395d6491009e1c62fac1f9eb81dfe
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421869"
---
# <a name="objects-windows-media-format-11-sdk"></a>Objectos (SDK de Windows Media Format 11)

El SDK de Windows Media Format usa varios objetos para leer, escribir, editar e indexar archivos ASF, y para crear y editar perfiles. Cada objeto admite varias interfaces. Algunas interfaces se admiten en varios objetos. En estos casos, las diferencias en la implementación se describen en la sección de referencia de la interfaz.

Los objetos del SDK de Windows Media Format son compatibles con COM. Para facilitar el desarrollo, cada objeto tiene una función o método de creación asociado. Debe crear objetos mediante la función o el método de creación en lugar de usar manualmente la función de COM **CoCreateInstance**.

Algunas interfaces tienen un número anexado a sus nombres, como **IWMProfile2** y **IWMWriter3**. En cada caso, las versiones numeradas heredan todos los métodos de las versiones anteriores y agregan nuevas funcionalidades.

En cada página de objeto de esta referencia, se enumeran primero las interfaces incluidas en el objeto COM principal, seguidas de las interfaces de devolución de llamada que debe implementar la aplicación.

En la tabla siguiente se enumeran los objetos admitidos por este SDK con una descripción de la funcionalidad de cada y la función que se usa para crearlo.



| Object                                                          | Descripción                                                                                                                                              | Función de creación                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Restaurador de copias de seguridad](backup-restorer-object.md)                   | Realiza una copia de seguridad de las licencias, normalmente en medios extraíbles, y después restaura esas licencias en otro equipo.                                           | [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer)                 |
| [Registro de dispositivos](device-registration-object.md)           | Administra la base de datos de registro de dispositivos, que contiene entradas para dispositivos de reproducción multimedia que están disponibles a través de una conexión de red.             | [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration)         |
| [Transcifrador DRM](drm-transcryptor-object.md)                 | Convierte los datos multimedia que están protegidos con DRM en un flujo de datos que se puede enviar a los dispositivos que usan el protocolo Windows Media DRM 10 para dispositivos de red. | [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)               |
| [Indizador](indexer-object.md)                                   | Crea un índice de archivos ASF para habilitar la búsqueda en archivos con secuencias de vídeo.                                                                            | [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)                               |
| [Agente de revocación de licencias](license-revocation-agent-object.md) | Administra la revocación de licencias.                                                                                                                              | [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) |
| [Editor de metadatos](metadata-editor-object.md)                   | Edita los metadatos de un encabezado de archivo ASF.                                                                                                                    | [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)                                 |
| [Administrador de perfiles](profile-manager-object.md)                   | Proporciona interfaces para crear, cargar y guardar perfiles. Se requiere un perfil para escribir un archivo ASF.                                                      | [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)                 |
| [Lector](reader-object.md)                                     | Lee archivos ASF. Este objeto usa un modelo de llamada asincrónica para sus operaciones.                                                                      | [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)                                 |
| [Lector sincrónico](synchronous-reader-object.md)             | Lee archivos ASF mediante llamadas sincrónicas.                                                                                                                 | [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)                         |
| [Escritor](writer-object.md)                                     | Escribe archivos ASF.                                                                                                                                        | [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)                                 |
| [Receptor de archivo de escritor](writer-file-sink-object.md)                 | Controla los archivos ASF escritos por el objeto de escritor.                                                                                                         | [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)                 |
| [Receptor de red del escritor](writer-network-sink-object.md)           | Controla la transmisión por secuencias de red en directo de archivos ASF escritos por el objeto escritor.                                                                               | [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)           |
| [Receptor de inserciones del escritor](writer-push-sink-object.md)                 | Controla la entrega de contenido de streaming a los servidores de publicación.                                                                                            | [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)                 |



 

En la tabla siguiente se enumeran los objetos que dependen de otros objetos. Estos objetos se crean mediante métodos de objetos existentes.



| Object                                                        | Descripción                                                                                                                                                                                                                                                                                                                           | Método de creación                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uso compartido de ancho de banda](bandwidth-sharing-object.md)             | Administra la información de uso compartido de ancho de banda en un perfil. Puede haber más de un objeto de uso compartido de ancho de banda para un perfil. Hay distintos métodos para crear un objeto de uso compartido de ancho de banda en función de si desea crear un nuevo objeto de uso compartido de ancho de banda o tener acceso a uno existente.                                           | [**IWMProfile3:: CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) DE<br/> [**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)<br/>                                                                                                                                                                                                                                      |
| [Buffer](buffer-object.md)                                   | Contiene un ejemplo multimedia y cualquier extensión de unidad de datos asociada. Se usa para los ejemplos de escritura y lectura.                                                                                                                                                                                                                           | [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) DE<br/> [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex)<br/> O BIEN<br/> [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex)<br/> O BIEN<br/> Creado automáticamente por el objeto lector o el objeto lector sincrónico para la entrega de ejemplo.<br/> |
| [Propiedades de los medios de entrada](input-media-properties-object.md)   | Administra las propiedades de una entrada. Puede existir un objeto de propiedades de entrada para cada entrada.                                                                                                                                                                                                                                             | [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)                                                                                                                                                                                                                                                                                                                                                                      |
| [Exclusión mutua](mutual-exclusion-object.md)               | Administra la información de exclusión mutua en un perfil. Los usos habituales de la exclusión mutua son el contenido de velocidad de bits y las bandas sonoras en varios idiomas. Hay distintos métodos para crear un objeto de exclusión mutua en función de si desea crear un nuevo objeto de exclusión mutua o tener acceso a uno existente.         | [**IWMProfile:: CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) DE<br/> [**IWMProfile::GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)<br/>                                                                                                                                                                                                                                              |
| [Propiedades de los medios de salida](output-media-properties-object.md) | Administra las propiedades de una salida. Puede existir un objeto de propiedades de medios de salida para cada salida. El lector o el lector sincrónico pueden crear estos objetos.                                                                                                                                                            | [**IWMReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) DE<br/> [**IWMSyncReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)<br/>                                                                                                                                                                                                                                                                      |
| [Perfil](profile-object.md)                                 | Contiene los datos de un perfil mientras se manipulan. Los objetos de perfil se crean cada vez que es necesario manipular el perfil. Hay distintos métodos para crear un objeto de perfil en función de si desea crear un nuevo perfil o tener acceso a uno existente.                                                  | [**IWMProfileManager:: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) DE<br/> [**IWMProfileManager::LoadProfileByData**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)<br/> O BIEN<br/> [**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)<br/> O BIEN<br/> [**IWMProfileManager::LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)<br/>          |
| [Configuración de flujo](stream-configuration-object.md)       | Administra las propiedades de una secuencia dentro de un perfil. Los objetos de configuración de secuencia se crean mediante objetos de secuencia cada vez que se necesita tener acceso a la información sobre un flujo. Hay distintos métodos para crear un objeto de configuración de secuencia en función de si desea crear una nueva secuencia o acceso y otra existente. | [**IWMProfile:: CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream) DE<br/> [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)<br/> O BIEN<br/> [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)<br/>                                                                                                                                                                                   |
| [Priorización de flujos](stream-prioritization-object.md)     | Mantiene la lista de prioridades de flujo para un perfil. Los flujos se quitarán en orden de prioridad creciente si el ancho de banda disponible está restringido. Solo puede haber un objeto de priorización de flujo en un perfil.                                                                                                                  | [**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 





