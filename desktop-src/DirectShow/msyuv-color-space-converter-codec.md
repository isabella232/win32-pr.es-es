---
description: MSYUV es un códec de convertidor de espacio de color YUV a RGB.
ms.assetid: 77b00937-ac63-4b23-b546-c0896b3c57ba
title: Códec del convertidor de espacios de colores MSYUV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 189ff787ee5b28311dd0357c245c7a6ca251d207f2448fc08a88fb856d7c2fce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075745"
---
# <a name="msyuv-color-space-converter-codec"></a>Códec del convertidor de espacios de colores MSYUV

MSYUV es un códec de convertidor de espacio de color YUV a RGB. Permite la reproducción de datos de origen de vídeo en formatos YUV en clientes cuyo adaptador de pantalla de vídeo no se puede usar para las conversiones YUV a RGB en hardware. El códec participa en los gráficos de filtro a través del [filtro contenedor de descompresión AVI.](avi-decompressor-filter.md)

Las cámaras de conferencia digital con interfaces 1394 o USB pueden generar datos de imagen en varios formatos YUV. Si el hardware de pantalla no admite la conversión de YUV a RGB, o si la funcionalidad de conversión de hardware no se puede usar por alguna otra razón, los datos de la imagen YUV se deben convertir al formato RGB antes de enviarse al representador de vídeo.

Debido al requisito del [representador](video-renderer-filter.md)de vídeo para un tipo de entrada RGB en el momento de la conexión, este filtro podría insertarse en un gráfico ascendente desde el representador de vídeo durante la creación automática del grafo. En concreto, si Graph Builder detecta un formato YUV en el tipo de medio del pin de salida del filtro ascendente, Graph Builder insertará el descomprimidor AVI, que cargará el códec MSYUV y lo configurará inicialmente para realizar la conversión a RGB. Una vez que el gráfico realiza la primera transición a un estado de ejecución o en pausa, el filtro Representador de vídeo puede detectar si el adaptador de pantalla de vídeo puede realizar la conversión en hardware. Si es posible, se notifica al descomprimidor AVI y vuelve a configurar MSYUV para que funcione en "modo de paso a través", lo que hace que el códec omita la conversión y copie los datos de la imagen YUV directamente en una superficie superpuesta de DirectDraw en la memoria de vídeo.

Dado que los representadores de mezcla de vídeo (VMR-7 y VMR-9) nunca usan GDI, no requieren un tipo RGB en el momento de la conexión y el convertidor de espacio de colores MSYUV nunca se inserta antes que vmr en un gráfico.

MSYUV convierte los formatos YUV empaquetados en RGB, como se muestra en la lista siguiente:

-   Formatos de entrada: UYVY, YUY2, YVYU
-   Formatos de salida: RGB 8, RGB 16, RGB 24, RGB 32

El códec del convertidor de espacios de colores MSYUV es un códec del Administrador de compresión de vídeo (VCM). Se usa en DirectShow el filtro [de descompresión AVI.](avi-decompressor-filter.md) Para obtener un convertidor de colores de uso general, use el [**DSP del convertidor de colores**](../medfound/colorconverter.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msyuv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 
