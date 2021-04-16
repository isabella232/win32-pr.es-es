---
description: Restringe el área del IAnalysisRegion a la parte de su área que no forma una intersección con el IAnalysisRegion especificado.
ms.assetid: 7a11d2a8-c2ca-4088-b932-8a6c3e789b7f
title: 'IAnalysisRegion:: ExcludeRegion (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13324d872a76a9184e6ea67b227dbd7444684bb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542102"
---
# <a name="ianalysisregionexcluderegion-method"></a>IAnalysisRegion:: ExcludeRegion (método)

Restringe el área del [**IAnalysisRegion**](ianalysisregion.md) a la parte de su área que no forma una intersección con el **IAnalysisRegion** especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ExcludeRegion(
  [in] IAnalysisRegion *pRegionToExclude
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pRegionToExclude* \[ de\]
</dt> <dd>

[**IAnalysisRegion**](ianalysisregion.md) que se va a excluir de este **IAnalysisRegion**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Si las dos áreas no forman una intersección, este [**IAnalysisRegion**](ianalysisregion.md) no cambia.

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

 

 




