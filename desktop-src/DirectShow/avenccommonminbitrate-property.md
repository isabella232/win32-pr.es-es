---
description: Especifica la velocidad de bits mínima, en bits por segundo. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y velocidad de bits variable (VBR).
ms.assetid: 57ef6c08-3bad-4d8d-8daf-61041b878802
title: Propiedad AVEncCommonMinBitRate (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65488b3a855d4b664c96a1d7abfc1718a35e94c466877c68848a1acf25a3bfe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159861"
---
# <a name="avenccommonminbitrate-property"></a>Propiedad AVEncCommonMinBitRate

Especifica la velocidad de bits mínima, en bits por segundo. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y velocidad de bits variable (VBR).

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonMinBitRate**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad tiene un intervalo lineal de valores. Para obtener el intervalo admitido, llame a [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Comentarios

El codificador aplica la velocidad de bits mínima al aumentar la calidad de codificación según sea necesario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




