---
title: Compatibilidad con DRM en DirectShow
description: Compatibilidad con DRM en DirectShow
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- SDK de Windows Media Format, compatibilidad con DRM en DirectShow
- Windows Media Format SDK, DirectShow
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- Advanced Systems Format (ASF), compatibilidad con DRM en DirectShow
- ASF (formato de sistemas avanzados), compatibilidad con DRM en DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Advanced Systems Format (ASF), administración de derechos digitales (DRM)
- ASF (formato de sistemas avanzados), administración de derechos digitales (DRM)
- DirectShow, compatibilidad con DRM
- Administración de derechos digitales (DRM), DirectShow
- DRM (administración de derechos digitales), DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85a211a3d3b438bac246c0bd90759f648818ac2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994935"
---
# <a name="drm-support-in-directshow"></a>Compatibilidad con DRM en DirectShow

La lectura y escritura de archivos protegidos con DRM en DirectShow se realiza básicamente de la misma forma que cuando se usa el SDK de Windows Media Format directamente. Para empezar, necesita la biblioteca estática wmstubdrm, que se obtiene de forma independiente de Microsoft. Además, debe implementar la interfaz **IKeyProvider** para permitir que la aplicación tenga acceso a los objetos de tiempo de ejecución del SDK de Windows Media Format cuando está habilitado DRM.

Al aplicar la protección de DRM versión 1, use la interfaz [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , que se obtiene tal y como se describe en [leer archivos ASF en DirectShow](reading-asf-files-in-directshow.md). Al aplicar la protección de DRM versión 7, obtenga la interfaz [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) llamando a **QueryService** en el filtro del [escritor ASF de WM](wm-asf-writer-filter.md) , tal como se muestra en el fragmento de código más adelante en este tema.

El resto de la configuración específica de DRM es exactamente la misma que la descrita en [habilitación de la compatibilidad con DRM](enabling-drm-support.md). Use **QueryService** para obtener la interfaz [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) del filtro de [lector ASF de WM](wm-asf-reader-filter.md) .

DirectX 9,0 contiene un ejemplo, PlayWndASF, una aplicación de reproductor DirectShow habilitada para DRM que muestra la adquisición de licencias de DRM versión 1 y versión 7. En este ejemplo también se incluye una implementación de la clase **CKeyProvider** , que admite la interfaz **IKeyProvider** .

 

 




