---
description: Configura el origen de medios de ASF para usar la búsqueda iterativa si el archivo de origen no tiene ningún índice.
ms.assetid: 0dd6f202-cdbc-4a28-8907-5530a0a2141b
title: MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cdc22f0b4f5490c7691cc40166cf929a16ba64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468657"
---
# <a name="mfpkey_asfmediasource_iterativeseekifnoindex-property"></a>Propiedad MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex

Configura el origen de medios de ASF para usar la búsqueda iterativa si el archivo de origen no tiene ningún índice.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>Observaciones

Use esta propiedad para configurar el origen de medios de ASF. Para establecer la propiedad , pase un **puntero IPropertyStore** al *solucionador de origen*. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

*La búsqueda iterativa* es un algoritmo para buscar una posición en un archivo ASF sin índice. Usa una serie de aproximaciones, basadas en la velocidad de bits media, para acercarse progresivamente al tiempo de búsqueda de destino. (El algoritmo es similar a una búsqueda binaria). La búsqueda iterativa puede tardar más que la búsqueda por índice, por lo que está deshabilitada de forma predeterminada.

Si establece esta propiedad, use las siguientes propiedades para establecer los parámetros de búsqueda:

-   [MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Max \_ Count](mfpkey-asfmediasource-iterativeseek-max-count.md)
-   [MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Tolerance \_ In \_ MilliSecond](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md)

Estas propiedades establecen el número máximo de iteraciones y la tolerancia, respectivamente. El algoritmo se detiene cuando alcanza el número máximo de iteraciones o cuando encuentra un paquete cuya distancia desde el tiempo de búsqueda está dentro de la tolerancia especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio aplicaciones para \| UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




