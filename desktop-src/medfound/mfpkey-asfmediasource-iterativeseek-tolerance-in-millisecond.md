---
description: Establece la tolerancia, en milisegundos, que se usa cuando el origen de medios de ASF realiza búsquedas iterativas.
ms.assetid: 3ee4410f-857c-4978-a308-87decfba0e2f
title: MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8cfc1ef656e1cff3da4bb33f19a3c2176729035f94a194a4ede21354f5dbc54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874136"
---
# <a name="mfpkey_asfmediasource_iterativeseek_tolerance_in_millisecond-property"></a>Propiedad MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Tolerance in \_ \_ MilliSecond

Establece la tolerancia, en milisegundos, que se usa cuando el origen de medios de ASF realiza búsquedas iterativas.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Comentarios

Use esta propiedad para configurar el origen de medios de ASF. Para establecer la propiedad , pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

Esta propiedad solo se aplica cuando la búsqueda iterativa está habilitada. Para obtener más información, [vea MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).

El algoritmo de búsqueda iterativo se detiene si encuentra un paquete cuya distancia desde el tiempo de búsqueda está dentro de la tolerancia especificada. El valor predeterminado es 8000 milisegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio \| para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




