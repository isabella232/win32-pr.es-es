---
description: Restringe el área del IAnalysisRegion a la parte de su área que no forma una intersección con el rectángulo especificado.
ms.assetid: a35b8bfc-a87a-4e9a-908f-2b13a128d222
title: 'IAnalysisRegion:: ExcludeRectangle (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 684ce2ceb57c7954c732fb2816aca50fcbae5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715244"
---
# <a name="ianalysisregionexcluderectangle-method"></a>IAnalysisRegion:: ExcludeRectangle (método)

Restringe el área del [**IAnalysisRegion**](ianalysisregion.md) a la parte de su área que no forma una intersección con el rectángulo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ExcludeRectangle(
  [in] RECT *pExcludingRectangle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pExcludingRectangle* \[ de\]
</dt> <dd>

Rectángulo que se va a excluir de este [**IAnalysisRegion**](ianalysisregion.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Las coordenadas del rectángulo están en unidades de HIMETRIC.

Si las dos áreas no forman una intersección, el [**IAnalysisRegion**](ianalysisregion.md) no cambia.

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

[**IAnalysisRegion:: ExcludeRegion (método)**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**IAnalysisRegion:: IntersectRectangle (método)**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**IAnalysisRegion:: IntersectRegion (método)**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**IAnalysisRegion:: UnionRectangle (método)**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**IAnalysisRegion:: UnionRegion (método)**](ianalysisregion-unionregion.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




