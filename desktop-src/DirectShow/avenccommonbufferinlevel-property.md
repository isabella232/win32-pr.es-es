---
description: Especifica el nivel inicial del búfer de codificación, en bits. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y velocidad de bits variable (VBR).
ms.assetid: 92ec9483-443e-4723-8795-9bf847c36131
title: Propiedad AVEncCommonBufferInLevel (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8219ab951fb68cd5dfc04e0b5415d77fe674e763
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162038"
---
# <a name="avenccommonbufferinlevel-property"></a>Propiedad AVEncCommonBufferInLevel

Especifica el nivel inicial del búfer de codificación, en bits. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y velocidad de bits variable (VBR).

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonBufferInLevel**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad tiene un intervalo lineal de valores. Para obtener el intervalo admitido, llame a [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Observaciones

Para el vídeo MPEG, esta propiedad define la integridad inicial del comprobador de búfer de vídeo (VBV). Admite la concatenación de secuencias durante la codificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




