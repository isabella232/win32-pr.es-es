---
description: Expande el área de este IAnalysisRegion al área creada por su unión con el IAnalysisRegion especificado.
ms.assetid: cc3ec5c6-98ff-442e-a1e8-d1a57752ad56
title: 'IAnalysisRegion:: UnionRegion (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 587986973c4ae4bebaeed3c031c746bc4f842c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715239"
---
# <a name="ianalysisregionunionregion-method"></a>IAnalysisRegion:: UnionRegion (método)

Expande el área de este [**IAnalysisRegion**](ianalysisregion.md) al área creada por su unión con el **IAnalysisRegion** especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnionRegion(
  [in] IAnalysisRegion *pRegionToUnion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pRegionToUnion* \[ de\]
</dt> <dd>

[**IAnalysisRegion**](ianalysisregion.md) con el que se va a combinar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Si alguna de las áreas es infinita, la nueva área también es infinita.

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

[**IAnalysisRegion:: IntersectRegion (método)**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**IAnalysisRegion:: UnionRectangle (método)**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




