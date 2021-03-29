---
title: Características de Rights Management digital
description: Características de Rights Management digital
ms.assetid: c3c1e59f-8ff9-496c-8e63-0c1cf4ce7092
keywords:
- SDK de Windows Media Format, características DRM
- Administración de derechos digitales (DRM), características
- DRM (administración de derechos digitales), características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd9c30b350fdf430d5b20bbe112c5309ac9da4f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792159"
---
# <a name="digital-rights-management-features"></a>Características de Rights Management digital

\[La característica Windows Media DRM está en desuso y no debe usarse. En su lugar, use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]

La administración de derechos digitales (DRM) es una tecnología que los propietarios de contenido pueden utilizar para proteger los archivos multimedia digitales mediante su cifrado con una clave (un fragmento de datos que bloquea y desbloquea el contenido). Para reproducir un archivo ASF protegido, el consumidor debe obtener una licencia independiente que contenga la clave. Cada licencia también contiene derechos, determinados por el propietario del contenido o el emisor de la licencia, que especifican cómo el consumidor puede utilizar el archivo. Con la tecnología DRM, los propietarios de contenido pueden ofrecer canciones, vídeos y otros archivos multimedia digitales a través de Internet en un formato de archivo protegido y controlar el uso de su contenido digital. La tecnología DRM de Microsoft también es compatible con Windows Media Rights Manager, Windows Media Encoder y Windows Media Player. Para obtener más información general sobre la tecnología DRM de Microsoft, vea el [sitio web de Microsoft Windows Media](https://support.microsoft.com/help/17946/windows-media).

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

En las secciones siguientes se describen las características principales relacionadas con DRM del SDK de Windows Media Format.



| Sección                                                                                            | Descripción                                                                                                                          |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Aspectos básicos de DRM](drm-basics.md)                                                                       | Proporciona una breve introducción a la funcionalidad DRM proporcionada por el SDK de Windows Media Format.                                         |
| [Versiones de DRM](drm-versions.md)                                                                   | Describe las principales diferencias entre las versiones de la protección DRM disponible para las aplicaciones.                                     |
| [DRM en vivo](live-drm.md)                                                                           | Describe los escenarios que se pueden realizar mediante la protección DRM "sobre la marcha".                                                                |
| [Individualización de DRM](drm-individualization.md)                                                 | Describe la actualización de seguridad de la aplicación que pueden requerir los propietarios de contenido o los emisores de licencias de DRM.                                   |
| [Copia de seguridad y restauración de licencias de DRM](backing-up-and-restoring-of-drm-licenses.md)           | Describe las ventajas y desventajas de permitir que los usuarios realicen copias de seguridad de sus licencias de contenido y las restauren.                                       |
| [Ver atributos DRM en el editor de metadatos](viewing-drm-attributes-in-the-metadata-editor.md) | Describe las capacidades de este objeto auxiliar DRM y los escenarios para los que se diseñó la compatibilidad.                                   |
| [Niveles de protección de salida](output-protection-levels.md)                                           | Describe cómo los niveles de protección de salida hacen que las licencias de la versión 10 de DRM sean más flexibles.                                                   |
| [Revocación de licencia](license-revocation.md)                                                       | Describe la revocación de licencias.                                                                                                        |
| [Windows Media DRM 10 para dispositivos de red](windows-media-drm-10-for-network-devices.md)           | Presenta Windows Media DRM 10 para dispositivos de red y su implementación en este SDK.                                              |
| [Ruta de acceso de audio seguro de Microsoft](microsoft-secure-audio-path--deprecated.md)                         | Describe la arquitectura de la ruta de acceso de audio seguro de Microsoft, que proporciona el mayor grado de protección para el contenido de audio protegido. |
| [Grabación de listas de reproducción](playlist-burning.md)                                                           | Describe la característica de grabación de listas de reproducción de DRM y cómo se admite en el SDK de Windows Media Format.                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Habilitar la compatibilidad con DRM**](enabling-drm-support.md)
</dt> <dt>

[**Características**](features.md)
</dt> </dl>

 

 