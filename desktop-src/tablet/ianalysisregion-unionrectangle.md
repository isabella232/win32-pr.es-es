---
description: Expande el área de este IAnalysisRegion al área creada por su unión con el rectángulo especificado.
ms.assetid: 9b12f509-4f6a-43b0-9639-bef060fd6d50
title: 'IAnalysisRegion:: UnionRectangle (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3a28a60eae95641225dd9c01791d89a9c38ada82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696546"
---
# <a name="ianalysisregionunionrectangle-method"></a>IAnalysisRegion:: UnionRectangle (método)

Expande el área de este [**IAnalysisRegion**](ianalysisregion.md) al área creada por su unión con el rectángulo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnionRectangle(
  [in] RECT *pRectangle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pRectangle* \[ de\]
</dt> <dd>

Puntero al rectángulo con el que se va a combinar, en coordenadas de espacio de tinta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Las coordenadas del rectángulo están en unidades de HIMETRIC.

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

[**IAnalysisRegion:: UnionRegion (método)**](ianalysisregion-unionregion.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




