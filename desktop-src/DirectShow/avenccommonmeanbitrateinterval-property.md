---
description: Especifica el intervalo de tiempo durante el que se aplica la velocidad de bits promedio. Esta propiedad se usa junto con la propiedad AVEncCommonMeanBitRate.
ms.assetid: 3cf26f46-e8ac-448a-a031-800915cad1ef
title: Propiedad AVEncCommonMeanBitRateInterval (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffee31b0ac54d195051f1cc973d2fdcb058f202
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495646"
---
# <a name="avenccommonmeanbitrateinterval-property"></a>Propiedad AVEncCommonMeanBitRateInterval

Especifica el intervalo de tiempo durante el que se aplica la velocidad de bits promedio. Esta propiedad se usa junto con la propiedad [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) .

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT64** (**VT \_ UI8**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonMeanBitRateInterval**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad tiene un intervalo de valores lineal. Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Observaciones

En el caso de la codificación de velocidad de bits variable (VBR) de dos pasos, el valor cero indica que el intervalo de tiempo es toda la duración del contenido. En el caso de la codificación de velocidad de bits constante (CBR) de un solo paso, el valor cero indica que el codificador selecciona el intervalo (normalmente 0,5 segundos).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                     |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**Interfaz ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




