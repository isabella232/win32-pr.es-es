---
description: Especifica el número máximo de fotogramas entre fotogramas clave.
ms.assetid: 5a1968e0-4c83-4733-8ea4-18f5eda52860
title: Propiedad AVEncVideoMaxKeyframeDistance (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ca0071b71716c385cebc36f5cc992d9b82da11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161754"
---
# <a name="avencvideomaxkeyframedistance-property"></a>Propiedad AVEncVideoMaxKeyframeDistance

Especifica el número máximo de fotogramas entre fotogramas clave.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoMaxKeyframeDistance**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad se devuelve como un intervalo de valores. Para obtener el intervalo admitido, llame a [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

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

 

 




