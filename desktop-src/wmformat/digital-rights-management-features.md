---
title: Características de Rights Management digitales
description: Características de Rights Management digitales
ms.assetid: c3c1e59f-8ff9-496c-8e63-0c1cf4ce7092
keywords:
- Windows SDK de formato multimedia, características de DRM
- administración de derechos digitales (DRM),características
- DRM (administración de derechos digitales),características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e389efdbfd3edef3f3c881cab8482c8ed03b6bb09eb4a7773caa59b4b9b1ad4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704874"
---
# <a name="digital-rights-management-features"></a>Características de Rights Management digitales

\[La Windows DRM multimedia está en desuso y no debe usarse. Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) en su lugar.\]

Administración de derechos digitales (DRM) es una tecnología que los propietarios de contenido pueden usar para proteger los archivos multimedia digitales cifrándolos con una clave (un fragmento de datos que bloquea y desbloquea el contenido). Para reproducir un archivo ASF protegido, un consumidor debe obtener una licencia independiente que contenga la clave. Cada licencia también contiene derechos, determinados por el propietario del contenido o el emisor de la licencia, que especifican cómo el consumidor puede usar el archivo. Con la tecnología DRM, los propietarios de contenido pueden entregar canciones, vídeos y otros archivos multimedia digitales a través de Internet en un formato de archivo protegido y controlar el uso de su contenido digital. La tecnología DRM de Microsoft también es compatible con Windows Media Rights Manager, Windows Media Encoder y Reproductor de Windows Media. Para obtener más información general sobre la tecnología DRM de Microsoft, vea el sitio web [de Microsoft Windows Media](https://support.microsoft.com/help/17946/windows-media).

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

En las secciones siguientes se de abordan las principales características relacionadas con DRM del SDK Windows Media Format.



| Sección                                                                                            | Descripción                                                                                                                          |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Aspectos básicos de DRM](drm-basics.md)                                                                       | Proporciona una breve introducción a la funcionalidad drm proporcionada por el SDK Windows Media Format.                                         |
| [Versiones de DRM](drm-versions.md)                                                                   | Describe las principales diferencias entre las versiones de protección DRM disponibles para las aplicaciones.                                     |
| [DRM en vivo](live-drm.md)                                                                           | Describe los escenarios posibles mediante la protección DRM "sobre la marcha".                                                                |
| [Individualización de DRM](drm-individualization.md)                                                 | Describe la actualización de seguridad de la aplicación que pueden requerir los propietarios de contenido DRM o los emisores de licencias.                                   |
| [Copia de seguridad y restauración de licencias DRM](backing-up-and-restoring-of-drm-licenses.md)           | Describe las ventajas y desventajas de permitir a los usuarios hacer copias de seguridad y restaurar sus licencias de contenido.                                       |
| [Visualización de atributos DRM en el Editor de metadatos](viewing-drm-attributes-in-the-metadata-editor.md) | Describe las funcionalidades de este objeto auxiliar de DRM y los escenarios que se han diseñado para admitir.                                   |
| [Niveles de protección de salida](output-protection-levels.md)                                           | Describe cómo los niveles de protección de salida hacen que las licencias drm de la versión 10 sea más flexible.                                                   |
| [Revocación de licencias](license-revocation.md)                                                       | Describe la revocación de licencias.                                                                                                        |
| [Windows DRM multimedia 10 para dispositivos de red](windows-media-drm-10-for-network-devices.md)           | Presenta Windows DRM 10 multimedia para dispositivos de red y su implementación en este SDK.                                              |
| [Ruta de acceso de audio seguro de Microsoft](microsoft-secure-audio-path--deprecated.md)                         | Describe la arquitectura de la ruta de acceso de audio seguro de Microsoft, que proporciona el mayor grado de protección para el contenido de audio protegido. |
| [Reproducción de listas de reproducción](playlist-burning.md)                                                           | Describe la característica de reproducción de reproducción de DRM y cómo se admite en el SDK Windows Media Format.                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Habilitación de la compatibilidad con DRM**](enabling-drm-support.md)
</dt> <dt>

[**Características**](features.md)
</dt> </dl>

 

 