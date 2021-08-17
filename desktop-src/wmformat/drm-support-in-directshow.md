---
title: Compatibilidad con DRM en DirectShow
description: Compatibilidad con DRM en DirectShow
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- Windows SDK de formato multimedia, compatibilidad con DRM en DirectShow
- Windows SDK de formato multimedia, DirectShow
- Windows SDK de formato multimedia, administración de derechos digitales (DRM)
- Formato de sistemas avanzados (ASF), compatibilidad con DRM en DirectShow
- ASF (formato de sistemas avanzados), compatibilidad con DRM en DirectShow
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados),DirectShow
- Formato de sistemas avanzados (ASF), administración de derechos digitales (DRM)
- ASF (formato de sistemas avanzados), administración de derechos digitales (DRM)
- DirectShow, compatibilidad con DRM
- administración de derechos digitales (DRM),DirectShow
- DRM (administración de derechos digitales),DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b3de3ca80d1b3b2fe27c9af590fe0cba0202b1fdd9b6fc322d8ed1c1871536
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930885"
---
# <a name="drm-support-in-directshow"></a>Compatibilidad con DRM en DirectShow

La lectura y escritura de archivos protegidos con DRM en DirectShow se realiza básicamente de la misma manera que cuando se usa el SDK Windows Media Format directamente. Para empezar, necesita la biblioteca estática wmstubdrm, que se obtiene por separado de Microsoft. Además, debe implementar la interfaz **IKeyProvider** para permitir que la aplicación acceda a los objetos en tiempo de ejecución del SDK de formato multimedia de Windows cuando drm está habilitado.

Al aplicar la protección de la versión 1 de DRM, use la interfaz [**IWMHeaderInfo,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) que se obtiene como se describe en Lectura de archivos [ASF en DirectShow](reading-asf-files-in-directshow.md). Al aplicar la protección de la versión 7 de DRM, obtenga la interfaz [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) llamando a **QueryService** en el filtro [WM ASF Writer,](wm-asf-writer-filter.md) como se muestra en el fragmento de código más adelante en este tema.

Todas las demás configuraciones específicas de DRM son exactamente las mismas que se describen en [Habilitación de la compatibilidad con DRM.](enabling-drm-support.md) Use **QueryService para** obtener la [**interfaz IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) del filtro [lector de ASF de WM.](wm-asf-reader-filter.md)

DirectX 9.0 contiene un ejemplo, PlayWndASF, una aplicación de reproductor de DirectShow habilitada para DRM que muestra la adquisición de licencias de DRM versión 1 y versión 7. Este ejemplo también incluye una implementación de la **clase CKeyProvider,** que admite la **interfaz IKeyProvider.**

 

 




