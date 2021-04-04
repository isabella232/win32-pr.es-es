---
description: Especifica el número de pasos de codificación que admite el codificador.
ms.assetid: 8b476164-fd44-4277-89bd-ba9929bf93a2
title: Propiedad AVEncCommonMultipassMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4302cf0a9524f16dee8e7b84060065a4c750e4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906792"
---
# <a name="avenccommonmultipassmode-property"></a>Propiedad AVEncCommonMultipassMode

Especifica el número de pasos de codificación que admite el codificador.

Esta propiedad es de solo lectura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonMultipassMode**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad se devuelve como un intervalo de valores. Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Observaciones

La latencia de descodificación se define como la cantidad de datos que el descodificador debe almacenar en búfer. Por ejemplo, si se establece esta propiedad en **Variant \_ true** en un codificador de vídeo MPEG, se limitan los tipos de estructuras GOP que el codificador puede utilizar.

Para establecer la fase de codificación actual, establezca la propiedad [**AVEncCommonPassStart**](avenccommonpassstart-property.md) .

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

 

 




