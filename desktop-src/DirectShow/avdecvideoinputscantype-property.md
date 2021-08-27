---
description: Especifica cómo se entrelaza la secuencia de vídeo descodificada.
ms.assetid: a2b95b90-1c58-47f3-b6a8-0f3f6f1a416c
title: Propiedad AVDecVideoInputScanType (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b86c9499019cdc07f095bf65be5817b828c78d277b02810bc1612cc0365edce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108705"
---
# <a name="avdecvideoinputscantype-property"></a>Propiedad AVDecVideoInputScanType

Especifica cómo se entrelaza la secuencia de vídeo descodificada.

Esta propiedad es de solo lectura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecVideoInputScanType**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la [**enumeración eAVDecVideoInputScanType.**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype)

## <a name="remarks"></a>Comentarios

Los 16 bits superiores del valor contienen el ancho y los 16 bits inferiores contienen el alto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

