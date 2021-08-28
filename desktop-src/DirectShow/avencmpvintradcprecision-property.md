---
description: Especifica la precisión de los coeficientes de controlador de dominio, en bits. Esta propiedad se aplica a los codificadores de vídeo MPEG.
ms.assetid: 2b4d11c1-767c-4466-8291-7959d841ae65
title: Propiedad AVEncMPVIntraDCPrecision (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e50d4a6b222d9860a16216a1395b9f5a2b10d23e6242315a61e8224d37810c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276135"
---
# <a name="avencmpvintradcprecision-property"></a>AvEncMPVIntraDCPrecision, propiedad

Especifica la precisión de los coeficientes de controlador de dominio, en bits. Esta propiedad se aplica a los codificadores de vídeo MPEG.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncMPVIntraDCPrecision**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad tiene un intervalo lineal de valores. Para obtener el intervalo admitido, llame a [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Comentarios

El intervalo habitual para esta propiedad es de 8 a 11 bits. Si el valor es cero, el codificador selecciona la precisión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 




