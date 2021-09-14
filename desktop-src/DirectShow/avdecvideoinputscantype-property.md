---
description: Especifica cómo se entrelaza la secuencia de vídeo descodificada.
ms.assetid: a2b95b90-1c58-47f3-b6a8-0f3f6f1a416c
title: Propiedad AVDecVideoInputScanType (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 560db1cd1cf0238fc9e50257f2f24559e9a94c8f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162098"
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

## <a name="remarks"></a>Observaciones

Los 16 bits superiores del valor contienen el ancho y los 16 bits inferiores contienen el alto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| aplicaciones para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP de 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

