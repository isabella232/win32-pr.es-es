---
title: DirectShow y Windows Media
description: DirectShow y Windows Media
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Windows Media Format SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- DirectShow, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4ca8eb4b1051d6685efa0bf73052ad9e7b31fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779752"
---
# <a name="directshow-and-windows-media"></a>DirectShow y Windows Media

Como alternativa al uso exclusivo del SDK de Windows Media Format, las aplicaciones también pueden leer y escribir contenido basado en Windows Media mediante la arquitectura de streaming de Microsoft® DirectShow®, tal y como se describe en las secciones siguientes.



| Sección                                                                                   | Descripción                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de DirectShow](about-directshow.md)                                                  | Describe DirectShow en términos generales y indica dónde obtener más información.                                                     |
| [¿Por qué usar DirectShow?](why-use-directshow.md)                                             | Describe cómo DirectShow simplifica ciertas tareas en la creación y reproducción de contenido basado en Windows Media.                              |
| [Leer archivos ASF en DirectShow](reading-asf-files-in-directshow.md)                    | Describe cómo reproducir archivos ASF con DirectShow.                                                                                           |
| [Crear archivos ASF en DirectShow](creating-asf-files-in-directshow.md)                  | Describe cómo crear archivos ASF con DirectShow.                                                                                         |
| [\_Notificación de eventos de estado de WMT en DirectShow](wmt-status-notification-in-directshow.md) | Describe qué eventos de **\_ Estado de WMT** se administran mediante los filtros ASF Reader y ASF Writer, y cómo las aplicaciones pueden recibir esos eventos. |
| [Compatibilidad con DRM en DirectShow](drm-support-in-directshow.md)                                | Describe cómo leer y escribir archivos protegidos con DRM mediante DirectShow.                                                                     |
| [Referencia de QASF de DirectShow](directshow-qasf-reference.md)                                | Contiene la documentación de referencia de los componentes de DirectShow que admiten Windows Media.                                              |



 

Tres aplicaciones de ejemplo del SDK ilustran el uso de DirectShow: DSCopy, DSPlay y DSSeekFM. Para obtener más información, vea [aplicaciones de ejemplo](sample-applications.md).

> [!Note]  
> Las aplicaciones que usan los componentes de QASF incluidos en este SDK requieren que se instale el tiempo de ejecución del SDK de Microsoft DirectX® 8,1 o posterior en los sistemas Windows® 2000, Windows 98 y Windows 95. En concreto, este tiempo de ejecución es necesario para el filtro de contenedor de DMO que hospeda los códecs de Windows Media en un gráfico de filtros de DirectShow.

 

 

 




