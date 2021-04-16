---
title: Habilitar la compatibilidad con DRM
description: Habilitar la compatibilidad con DRM
ms.assetid: 90e92373-7fc2-4478-a179-22f22dbc3a3d
keywords:
- SDK de Windows Media Format, habilitando la compatibilidad con DRM
- Advanced Systems Format (ASF), habilitando la compatibilidad con DRM
- ASF (formato de sistemas avanzados), habilitando la compatibilidad con DRM
- Administración de derechos digitales (DRM), habilitar la compatibilidad
- DRM (administración de derechos digitales), habilitar la compatibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936210eb9d560bffe12acf5cc33fb9f864f8404c
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "105695792"
---
# <a name="enabling-drm-support"></a>Habilitar la compatibilidad con DRM

Puede usar el kit de desarrollo de software (SDK) de Microsoft Windows Media Format para crear aplicaciones que pueden aplicar la protección de administración de derechos digitales (DRM) y reproducir secuencias de DRM en vivo o archivos protegidos con DRM. También se proporciona compatibilidad para realizar copias de seguridad y restaurar las licencias de DRM de un reproductor y para [*individualizar*](wmformat-glossary.md) a los jugadores.

En esta documentación se supone que tiene conocimientos básicos de la tecnología de administración de derechos digitales de Microsoft. En la sección [características de Rights Management digital](digital-rights-management-features.md) de esta documentación se proporciona una introducción básica a DRM de Windows Media. Para obtener más información acerca de DRM, vea la página Rights Management digital en el [sitio web de Microsoft](https://windows.microsoft.com/windows/products/windows-media).

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

En las secciones siguientes se describe cómo habilitar la compatibilidad con DRM.



| Sección                                                                                                                        | Descripción                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Obtención de la biblioteca DRM necesaria](obtaining-the-required-drm-library.md)                                                   | Describe los pasos necesarios para obtener la biblioteca estática necesaria para crear aplicaciones habilitadas para DRM.                                                                               |
| [Protección de DRM y distribución de licencias de contenido](drm-protection-and-content-license-distribution.md)                         | Compara las funciones de DRM del SDK de Windows Media Format con el SDK de Windows Media Rights Manager.                                                                                        |
| [Operaciones de red DRM](drm-network-operations.md)                                                                           | Describe cómo la aplicación debe controlar las operaciones DRM que se comunican a través de Internet u otras redes.                                                                          |
| [Crear archivos protegidos](creating-protected-files.md)                                                                       | Describe cómo crear archivos protegidos con DRM.                                                                                                                                                    |
| [Leer archivos protegidos](reading-protected-files.md)                                                                         | Describe las formas de adquirir licencias para el contenido y las ventajas de implementar la adquisición de licencias silenciosa.                                                                                     |
| [Ver atributos de archivos protegidos](viewing-attributes-of-protected-files.md)                                             | Describe cómo utilizar la interfaz [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) en el objeto de editor de metadatos para ver los atributos de los archivos protegidos sin tener la biblioteca estática necesaria para DRM. |
| [Trabajar con listas de revocación](working-with-revocation-lists.md)                                                             | Describe las listas de revocación y cómo se implementan.                                                                                                                                        |
| [Copia de seguridad y restauración de licencias](backing-up-and-restoring-licenses.md)                                                     | Describe cómo los usuarios pueden administrar sus licencias de contenido realizando copias de seguridad y restaurarlas en su equipo actual o en otros equipos.                                                         |
| [Individualización de aplicaciones DRM](individualizing-drm-applications.md)                                                       | Describe cómo la característica de [*individualización*](wmformat-glossary.md) aumenta la seguridad en un sistema DRM.                                                           |
| [Trabajar con niveles de protección de salida](working-with-output-protection-levels.md)                                             | Describe cómo admitir los niveles de protección de salida, que se usan para registrar las acciones permitidas en las licencias de DRM versión 10.                                                                         |
| [Usar el protocolo DRM 10 de Windows Media para dispositivos de red](using-the-windows-media-drm-10-for-network-devices-protocol.md) | Describe cómo admitir la transmisión por secuencias de dispositivos segura mediante Windows Media DRM 10 para el protocolo de dispositivos de red.                                                                                |
| [Implementación de la revocación de licencias](implementing-license-revocation.md)                                                         | Describe el proceso de revocación de licencias y las acciones que debe realizar la aplicación para implementarla.                                                                                        |
| [Grabación de listas de reproducción que contienen archivos seguros](burning-playlists-that-contain-secure-files.md)                                 | Describe cómo implementar la grabación de listas de reproducción en la aplicación.                                                                                                                                |



 

El SDK incluye varias aplicaciones de ejemplo que muestran cómo leer archivos protegidos. el ejemplo más completo es DRMShow. Para obtener más información, vea [aplicaciones de ejemplo](sample-applications.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características**](features.md)
</dt> </dl>

 

 




