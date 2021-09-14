---
description: Especifica el número de pases de codificación que admite el codificador.
ms.assetid: 8b476164-fd44-4277-89bd-ba9929bf93a2
title: Propiedad AVEncCommonMultipassMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4302cf0a9524f16dee8e7b84060065a4c750e4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161998"
---
# <a name="avenccommonmultipassmode-property"></a>Propiedad AVEncCommonMultipassMode

Especifica el número de pases de codificación que admite el codificador.

Esta propiedad es de solo lectura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonMultipassMode**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad se devuelve como un intervalo de valores. Para obtener el intervalo admitido, llame a [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Observaciones

La latencia de descodificación se define como la cantidad de datos que el descodificador debe almacenar en búfer. Por ejemplo, establecer esta propiedad en **VARIANT \_ TRUE** en un codificador de vídeo MPEG limita los tipos de estructuras GOP que el codificador puede usar.

Para establecer el paso de codificación actual, establezca la [**propiedad AVEncCommonPassStart.**](avenccommonpassstart-property.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




