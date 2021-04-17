---
description: MSYUV es un códec de convertidor de espacio de colores YUV a RGB.
ms.assetid: 77b00937-ac63-4b23-b546-c0896b3c57ba
title: MSYUV codec del convertidor de espacio de colores
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838e7cd749042b2fb97adaf0b2b4cd0378a81c07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690915"
---
# <a name="msyuv-color-space-converter-codec"></a>MSYUV codec del convertidor de espacio de colores

MSYUV es un códec de convertidor de espacio de colores YUV a RGB. Permite la reproducción de datos de origen de vídeo en formatos YUV en clientes cuyo adaptador de pantalla de vídeo no se puede usar para conversiones de YUV a RGB en hardware. El códec participa en los gráficos de filtros a través del filtro de contenedor de [descompresor de AVI](avi-decompressor-filter.md) .

Las cámaras de conferencia digital con interfaces 1394 o USB pueden generar datos de imagen en varios formatos YUV. Si el hardware de pantalla no es compatible con la conversión de YUV a RGB incorporada, o si no se puede usar la funcionalidad de conversión de hardware por algún otro motivo, los datos de la imagen YUV se deben convertir al formato RGB antes de enviarlos al representador de vídeo.

Debido al requisito del [representador de vídeo](video-renderer-filter.md)para un tipo de entrada RGB en el momento de la conexión, este filtro podría insertarse en un gráfico de nivel superior desde el representador de vídeo durante la creación automática del gráfico. En concreto, si el generador de gráficos detecta un formato YUV en el tipo de medio del PIN de salida del filtro de nivel superior, el generador de gráficos insertará el descompresor de AVI, que, a continuación, cargará el códec MSYUV y lo configurará inicialmente para realizar la conversión a RGB. Después de que el gráfico pase por primera vez a un estado de ejecución o en pausa, el filtro de representador de vídeo puede detectar si el adaptador de pantalla de vídeo puede realizar la conversión en hardware. Si es posible, se notifica al descompresor de AVI y vuelve a configurar MSYUV para que funcione en "modo de paso a través", que hace que el códec omita la conversión y copie los datos de imagen YUV directamente en una superficie de superposición de DirectDraw en la memoria de vídeo.

Dado que los representadores de mezcla de vídeo (VMR-7 y VMR-9) nunca usan GDI, no requieren un tipo RGB en el momento de la conexión y el convertidor de espacio de colores MSYUV nunca se inserta antes de la VMR en un gráfico.

MSYUV convierte los formatos YUV empaquetados en RGB, tal como se muestra en la lista siguiente:

-   Formatos de entrada: UYVY, YUY2, YVYU
-   Formatos de salida: RGB 8, RGB 16, RGB 24, RGB 32

El códec de convertidor de espacio de colores MSYUV es un códec de administrador de compresión de vídeo (VCM). Se usa en DirectShow a través del filtro de [descompresor de AVI](avi-decompressor-filter.md) . Para un convertidor de colores de uso general, use el [**convertidor de colores DSP**](../medfound/colorconverter.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msyuv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 
