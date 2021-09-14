---
description: Especifica el intervalo de tiempo durante el que se aplica la velocidad de bits media. Esta propiedad se usa junto con la propiedad AVEncCommonMeanBitRate.
ms.assetid: 3cf26f46-e8ac-448a-a031-800915cad1ef
title: Propiedad AVEncCommonMeanBitRateInterval (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffee31b0ac54d195051f1cc973d2fdcb058f202
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162010"
---
# <a name="avenccommonmeanbitrateinterval-property"></a>AvEncCommonMeanBitRateInterval, propiedad

Especifica el intervalo de tiempo durante el que se aplica la velocidad de bits media. Esta propiedad se usa junto con la [**propiedad AVEncCommonMeanBitRate.**](avenccommonmeanbitrate-property.md)

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT64** (**VT \_ UI8**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonMeanBitRateInterval**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad tiene un intervalo lineal de valores. Para obtener el intervalo admitido, llame a [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Observaciones

Para la codificación de velocidad de bits variable (VBR) de dos pases, el valor cero indica que el intervalo de tiempo es la duración completa del contenido. Para la codificación de velocidad de bits constante de paso único (CBR), el valor cero indica que el codificador selecciona el intervalo (normalmente 0,5 segundos).

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

 

 




