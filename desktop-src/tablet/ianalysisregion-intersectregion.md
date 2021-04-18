---
description: Restringe el área de IAnalysisRegion al área creada por su intersección con el IAnalysisRegion especificado.
ms.assetid: 02b3049f-ada9-4de3-a7a2-f9ff8313fbab
title: 'IAnalysisRegion:: IntersectRegion (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7ff3caad382e54f41685f6102edafdeb86b813c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715243"
---
# <a name="ianalysisregionintersectregion-method"></a>IAnalysisRegion:: IntersectRegion (método)

Restringe el área de [**IAnalysisRegion**](ianalysisregion.md) al área creada por su intersección con el **IAnalysisRegion** especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IntersectRegion(
  [in] IAnalysisRegion *pRegionToIntersect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pRegionToIntersect* \[ de\]
</dt> <dd>

[**IAnalysisRegion**](ianalysisregion.md) con el que se va a formar una intersección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

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

[**IAnalysisRegion:: IntersectRectangle (método)**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**IAnalysisRegion:: UnionRectangle (método)**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**IAnalysisRegion:: UnionRegion (método)**](ianalysisregion-unionregion.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




