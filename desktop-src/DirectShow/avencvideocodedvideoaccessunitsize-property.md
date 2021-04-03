---
description: Especifica el tamaño de las unidades de acceso al vídeo, en bytes. Esta propiedad solo se aplica a los modos de control de velocidad de bits variable (VBR).
ms.assetid: bb46b171-d70a-4e01-88c4-321a210a0220
title: Propiedad AVEncVideoCodedVideoAccessUnitSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be3a6e499749d862fdcc63f28b1a9a02f476d1c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997656"
---
# <a name="avencvideocodedvideoaccessunitsize-property"></a>Propiedad AVEncVideoCodedVideoAccessUnitSize

Especifica el tamaño de las unidades de acceso al vídeo, en bytes. Esta propiedad solo se aplica a los modos de control de velocidad de bits variable (VBR).

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoCodedVideoAccessUnitSize**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad se devuelve como un intervalo de valores. Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

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

 

 




