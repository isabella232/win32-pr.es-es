---
title: Novedades (Windows Media Format 11 SDK)
description: What's New
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- SDK de Windows Media Format, novedades
- Windows Media Format SDK, características
- SDK de Windows Media Format, nuevas características
- SDK de Windows Media Format, API extendidas de cliente
- SDK de Windows Media Format, actualizaciones de DRM
- SDK de Windows Media Format, actualizaciones de códecs
- SDK de Windows Media Format, imágenes en miniatura
- Administración de derechos digitales (DRM), nuevas características
- DRM (administración de derechos digitales), nuevas características
- imágenes en miniatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63d85f00f89f940ab22754d1f6f458430868d7c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800776"
---
# <a name="whats-new-windows-media-format-11-sdk"></a>Novedades (Windows Media Format 11 SDK)

El SDK de Windows Media Format 11 presenta nuevas características de administración de derechos digitales (DRM). Se han realizado los siguientes cambios en el SDK desde la versión 9,5.

## <a name="windows-media-drm-client-extended-apis"></a>API extendidas del cliente DRM de Windows Media

El SDK de Windows Media Format 11 incluye un nuevo conjunto de API de DRM. Estas API se implementan en su propia biblioteca. Muchas de las características DRM admitidas por los objetos del SDK de Windows Media Format también se admiten en las API extendidas del cliente DRM de Windows Media. La principal diferencia en las nuevas API es que no confían en que un archivo ASF funcione. En su lugar, las nuevas API tratan directamente con el almacén de licencias local, a menudo con el identificador de clave para identificar las licencias.

Para obtener más información, consulte la documentación sobre las [API extendidas del cliente DRM de Windows Media](windows-media-drm-client-extended-apis.md) .

## <a name="updated-codecs"></a>Códecs actualizados

El códec de perfil avanzado de Windows Media Video 9 se ha actualizado para generar un flujo de bits comprimido que es compatible con el estándar SMPTE VC-1 publicado.

El códec Windows Media Audio 10 Professional también se incluye en esta versión del SDK. El nuevo códec de audio presenta una calidad mejorada a velocidades de bits inferiores.

## <a name="thumbnail-right"></a>Miniatura derecha

Las aplicaciones pueden solicitar una nueva acción DRM para leer el vídeo y crear una imagen en miniatura. Esto permite que las aplicaciones creen y muestren imágenes en miniatura de archivos de vídeo sin abrir el archivo para su reproducción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del SDK de Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




