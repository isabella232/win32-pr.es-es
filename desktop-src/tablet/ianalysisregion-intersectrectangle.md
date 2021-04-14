---
description: Restringe el área de este IAnalysisRegion al área creada por su intersección con el rectángulo especificado.
ms.assetid: de6b565f-34c1-4551-ab92-db6bacb8608d
title: 'IAnalysisRegion:: IntersectRectangle (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4ce0e514b24aba0331d9ea604333680db1c67c8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542099"
---
# <a name="ianalysisregionintersectrectangle-method"></a>IAnalysisRegion:: IntersectRectangle (método)

Restringe el área de este [**IAnalysisRegion**](ianalysisregion.md) al área creada por su intersección con el rectángulo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IntersectRectangle(
  [in] RECT *pIntersectingRectangle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pIntersectingRectangle* \[ de\]
</dt> <dd>

Puntero al rectángulo con el que se va a formar una intersección en las coordenadas del espacio de tinta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Las coordenadas del rectángulo están en unidades de HIMETRIC.

Si las dos áreas no forman una intersección, el área nueva está vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
</dt> <dt>

[**IAnalysisRegion:: ExcludeRegion (método)**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**IAnalysisRegion:: IntersectRegion (método)**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**IAnalysisRegion:: UnionRectangle (método)**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**IAnalysisRegion:: UnionRegion (método)**](ianalysisregion-unionregion.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




