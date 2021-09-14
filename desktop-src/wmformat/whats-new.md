---
title: Novedades (SDK Windows Media Format 11)
description: Novedades
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- Windows SDK de formato multimedia, novedades
- Windows SDK de formato multimedia, características
- Windows SDK de formato multimedia, nuevas características
- Windows SDK de formato multimedia, API extendidas de cliente
- Windows SDK de formato multimedia, actualizaciones de DRM
- Windows SDK de formato multimedia, actualizaciones de códecs
- Windows SDK de formato multimedia, imágenes en miniatura
- administración de derechos digitales (DRM), nuevas características
- DRM (administración de derechos digitales), nuevas características
- imágenes en miniatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63d85f00f89f940ab22754d1f6f458430868d7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256161"
---
# <a name="whats-new-windows-media-format-11-sdk"></a>Novedades (SDK Windows Media Format 11)

El SDK Windows Media Format 11 presenta nuevas características de administración de derechos digitales (DRM). Se han realizado los siguientes cambios en el SDK desde la versión 9.5.

## <a name="windows-media-drm-client-extended-apis"></a>Windows API extendidas del cliente DRM multimedia

El SDK Windows Media Format 11 se incluye con un nuevo conjunto de API drm. Estas API se implementan en su propia biblioteca. Muchas de las características de DRM compatibles con los objetos del SDK de Windows Media Format también son compatibles con las API extendidas de Windows Media DRM Client. La diferencia principal en las nuevas API es que no se basan en tener un archivo ASF para funcionar. En su lugar, las nuevas API tratan directamente con el almacén de licencias local, a menudo usando el identificador de clave para identificar las licencias.

Para obtener más información, consulte la documentación Windows API extendidas del cliente [DRM multimedia.](windows-media-drm-client-extended-apis.md)

## <a name="updated-codecs"></a>Códecs actualizados

El Windows de perfil avanzado de Media Video 9 se ha actualizado para generar una secuencia de bits comprimida compatible con el estándar SMPTE VC-1 publicado.

El Windows de Professional media audio 10 también se incluye en esta versión del SDK. El nuevo códec de audio ofrece una calidad mejorada a velocidades de bits más bajas.

## <a name="thumbnail-right"></a>Miniatura derecha

Las aplicaciones pueden solicitar una nueva acción drm para leer desde el vídeo para crear una imagen en miniatura. Esto permite a las aplicaciones crear y mostrar imágenes en miniatura para archivos de vídeo sin abrir el archivo para su reproducción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del SDK Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




