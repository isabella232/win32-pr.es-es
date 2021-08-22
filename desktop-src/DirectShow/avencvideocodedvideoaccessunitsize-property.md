---
description: Especifica el tamaño de las unidades de acceso de vídeo, en bytes. Esta propiedad solo se aplica a los modos de control de velocidad de bits variable (VBR).
ms.assetid: bb46b171-d70a-4e01-88c4-321a210a0220
title: Propiedad AVEncVideoCodedVideoAccessUnitSize (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce45dbd232226aa5e0013cbead8e4ff2d8d82b5362d1d6a43cf45c2d030407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663178"
---
# <a name="avencvideocodedvideoaccessunitsize-property"></a>Propiedad AVEncVideoCodedVideoAccessUnitSize

Especifica el tamaño de las unidades de acceso de vídeo, en bytes. Esta propiedad solo se aplica a los modos de control de velocidad de bits variable (VBR).

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoCodedVideoAccessUnitSize**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad se devuelve como un intervalo de valores. Para obtener el intervalo admitido, llame a [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




