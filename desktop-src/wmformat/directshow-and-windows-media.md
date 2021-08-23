---
title: DirectShow y Windows multimedia
description: DirectShow y Windows multimedia
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Windows SDK de formato multimedia, DirectShow
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados),DirectShow
- DirectShow,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b975347d26414dda0c1f54c0b71ac852541bd58c314e3724725c3768ddfc7bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027913"
---
# <a name="directshow-and-windows-media"></a>DirectShow y Windows multimedia

Como alternativa al uso exclusivo del SDK de formato multimedia de Windows, las aplicaciones también pueden leer y escribir contenido basado en multimedia de Windows mediante la arquitectura de streaming de Microsoft® DirectShow® como se describe en las secciones siguientes.



| Sección                                                                                   | Descripción                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de DirectShow](about-directshow.md)                                                  | Describe DirectShow en términos generales e indica dónde obtener más información sobre él.                                                     |
| [¿Por qué usar DirectShow?](why-use-directshow.md)                                             | Describe cómo DirectShow simplifica ciertas tareas en la creación y reproducción de contenido basado Windows multimedia.                              |
| [Lectura de archivos ASF en DirectShow](reading-asf-files-in-directshow.md)                    | Describe cómo reproducir archivos ASF mediante DirectShow.                                                                                           |
| [Creación de archivos ASF en DirectShow](creating-asf-files-in-directshow.md)                  | Describe cómo crear archivos ASF mediante DirectShow.                                                                                         |
| [Notificación de eventos \_ WMT STATUS en DirectShow](wmt-status-notification-in-directshow.md) | Describe qué **eventos DE ESTADO \_ DE WMT** se controlan mediante los filtros Lector de ASF y Escritor de ASF, y cómo las aplicaciones pueden recibir esos eventos. |
| [Compatibilidad con DRM en DirectShow](drm-support-in-directshow.md)                                | Describe cómo leer y escribir archivos protegidos con DRM a través de DirectShow.                                                                     |
| [DirectShow Referencia de QASF](directshow-qasf-reference.md)                                | Contiene la documentación de referencia de los componentes DirectShow que admiten Windows Media.                                              |



 

Tres aplicaciones de ejemplo en el SDK ilustran el uso de DirectShow: DSCopy, DSPlay y DSSeekFM. Para obtener más información, vea [Aplicaciones de ejemplo.](sample-applications.md)

> [!Note]  
> Las aplicaciones que usan los componentes QASF incluidos en este SDK requieren que el entorno de ejecución del SDK de Microsoft DirectX® 8.1 o posterior se instale en los sistemas Windows® 2000, Windows 98 y Windows 95. En concreto, este tiempo de ejecución lo requiere el filtro DMO Wrapper que hospeda los códecs Windows Media en un gráfico DirectShow filtro.

 

 

 




