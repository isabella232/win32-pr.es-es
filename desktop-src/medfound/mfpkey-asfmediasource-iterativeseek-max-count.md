---
description: Establece el número máximo de iteraciones de búsqueda que usará el origen multimedia de ASF cuando realice búsquedas iterativas.
ms.assetid: 5b596faf-1217-424d-ae16-8c9ec6f31af1
title: MFPKEY_ASFMediaSource_IterativeSeek_Max_Count propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 183ed13143260f9d6d5de67ba38fcff27ebfd5a6afb01c75a07e92497d571cf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874258"
---
# <a name="mfpkey_asfmediasource_iterativeseek_max_count-property"></a>Propiedad MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Max \_ Count

Establece el número máximo de iteraciones de búsqueda que usará el origen multimedia de ASF cuando realice búsquedas iterativas.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Comentarios

Use esta propiedad para configurar el origen de medios de ASF. Para establecer la propiedad , pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

Esta propiedad solo se aplica cuando la búsqueda iterativa está habilitada. Para obtener más información, [vea MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).

El intervalo válido de esta propiedad es \[ 1-10, \] ambos incluidos. Con un número mayor, la búsqueda iterativa tiende a ser más precisa, pero tarda más tiempo.

El valor predeterminado es 5.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




