---
description: Configura el origen de medios ASF para usar búsquedas iterativas si el archivo de origen no tiene ningún índice.
ms.assetid: 0dd6f202-cdbc-4a28-8907-5530a0a2141b
title: Propiedad MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cdc22f0b4f5490c7691cc40166cf929a16ba64
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820287"
---
# <a name="mfpkey_asfmediasource_iterativeseekifnoindex-property"></a>\_ \_ Propiedad ITERATIVESEEKIFNOINDEX de MFPKEY ASFMediaSource

Configura el origen de medios ASF para usar búsquedas iterativas si el archivo de origen no tiene ningún índice.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**VARIANTE \_ bool**

VT \_ bool

**boolVal**



## <a name="remarks"></a>Observaciones

Utilice esta propiedad para configurar el origen de medios ASF. Para establecer la propiedad, pase un puntero **IPropertyStore** a la *resolución de origen*. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

La *búsqueda iterativa* es un algoritmo para encontrar una posición en un archivo ASF sin índice. Usa una serie de aproximaciones, en función de la velocidad de bits media, para que se acerquen progresivamente al tiempo de búsqueda del destino. (El algoritmo es similar a una búsqueda binaria). La búsqueda iterativa puede tardar más que la búsqueda por índice, por lo que está deshabilitada de forma predeterminada.

Si establece esta propiedad, use las siguientes propiedades para establecer los parámetros de búsqueda:

-   [Recuento máximo de MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ \_](mfpkey-asfmediasource-iterativeseek-max-count.md)
-   [MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ tolerancia \_ en \_ milisegundos](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md)

Estas propiedades establecen el número máximo de iteraciones y la tolerancia, respectivamente. El algoritmo se detiene cuando alcanza el número máximo de iteraciones o cuando encuentra un paquete cuya distancia desde el tiempo de búsqueda está dentro de la tolerancia especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




