---
title: Habilitación de la compatibilidad con DRM
description: Habilitación de la compatibilidad con DRM
ms.assetid: 90e92373-7fc2-4478-a179-22f22dbc3a3d
keywords:
- Windows SDK de formato multimedia, habilitación de la compatibilidad con DRM
- Formato de sistemas avanzados (ASF), habilitación de la compatibilidad con DRM
- ASF (formato de sistemas avanzados), habilitación de la compatibilidad con DRM
- administración de derechos digitales (DRM), habilitación de la compatibilidad
- DRM (administración de derechos digitales), habilitar la compatibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936210eb9d560bffe12acf5cc33fb9f864f8404c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262183"
---
# <a name="enabling-drm-support"></a>Habilitación de la compatibilidad con DRM

Puede usar el Kit de desarrollo de software (SDK) de formato multimedia (SDK) de Microsoft Windows para compilar aplicaciones que puedan aplicar la protección de administración de derechos digitales (DRM) y reproducir secuencias DRM en vivo o archivos protegidos con DRM. También se proporciona compatibilidad para realizar copias de seguridad y restaurar las licencias DRM de un reproductor y para [*individualizar reproductores.*](wmformat-glossary.md)

En esta documentación se supone que está familiarizado con la tecnología de administración de derechos digitales de Microsoft. En la sección Características de Windows digitales de esta documentación se proporciona información general Windows [Rights Management](digital-rights-management-features.md) DRM multimedia. Para obtener más información sobre DRM, vea la página de Rights Management digital en el [sitio web de Microsoft](https://windows.microsoft.com/windows/products/windows-media).

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

En las secciones siguientes se describe cómo habilitar la compatibilidad con DRM.



| Sección                                                                                                                        | Descripción                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Obtención de la biblioteca DRM requerida](obtaining-the-required-drm-library.md)                                                   | Describe los pasos necesarios para obtener la biblioteca estática necesaria para crear aplicaciones habilitadas para DRM.                                                                               |
| [Protección DRM y distribución de licencias de contenido](drm-protection-and-content-license-distribution.md)                         | Compara las funcionalidades de DRM del SDK Windows Media Format con Windows SDK de Media Rights Manager.                                                                                        |
| [Operaciones de red DRM](drm-network-operations.md)                                                                           | Describe cómo la aplicación debe controlar las operaciones DRM que se comunican a través de Internet u otras redes.                                                                          |
| [Creación de archivos protegidos](creating-protected-files.md)                                                                       | Describe cómo crear archivos protegidos con DRM.                                                                                                                                                    |
| [Leer archivos protegidos](reading-protected-files.md)                                                                         | Describe maneras de adquirir licencias de contenido y las ventajas de implementar la adquisición silenciosa de licencias.                                                                                     |
| [Ver atributos de archivos protegidos](viewing-attributes-of-protected-files.md)                                             | Describe cómo usar la interfaz [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) en el objeto del editor de metadatos para ver los atributos de los archivos protegidos sin tener la biblioteca estática necesaria para DRM. |
| [Trabajar con listas de revocación](working-with-revocation-lists.md)                                                             | Describe las listas de revocación y cómo se implementan.                                                                                                                                        |
| [Copia de seguridad y restauración de licencias](backing-up-and-restoring-licenses.md)                                                     | Describe cómo los usuarios pueden administrar sus licencias de contenido mediante la copia de seguridad y la restauración en su equipo actual o en otros equipos.                                                         |
| [Individualización de aplicaciones DRM](individualizing-drm-applications.md)                                                       | Describe cómo la característica [*de individualización*](wmformat-glossary.md) aumenta la seguridad en un sistema DRM.                                                           |
| [Trabajar con niveles de protección de salida](working-with-output-protection-levels.md)                                             | Describe cómo admitir los niveles de protección de salida, que se usan para registrar las acciones permitidas en licencias drm versión 10.                                                                         |
| [Uso de Windows DRM 10 multimedia para el protocolo de dispositivos de red](using-the-windows-media-drm-10-for-network-devices-protocol.md) | Describe cómo admitir el streaming de dispositivos seguros mediante el Windows drm multimedia 10 para dispositivos de red.                                                                                |
| [Implementación de la revocación de licencias](implementing-license-revocation.md)                                                         | Describe el proceso de revocación de licencias y las acciones que debe realizar la aplicación para implementarla.                                                                                        |
| [Grabación de listas de reproducción que contienen archivos seguros](burning-playlists-that-contain-secure-files.md)                                 | Describe cómo implementar la reproducción de listas de reproducción en la aplicación.                                                                                                                                |



 

El SDK incluye varias aplicaciones de ejemplo que muestran cómo leer archivos protegidos. El ejemplo más completo es DRMShow. Para obtener más información, vea [Aplicaciones de ejemplo.](sample-applications.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características**](features.md)
</dt> </dl>

 

 




