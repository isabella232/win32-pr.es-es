---
description: Restringe el área de esta región IAnalysisRegion al área creada por su intersección con el rectángulo especificado.
ms.assetid: de6b565f-34c1-4551-ab92-db6bacb8608d
title: Método IAnalysisRegion::IntersectRectangle (IACom.h)
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
ms.openlocfilehash: 074e3cee4cd20a35c780ce0c644b24c7688956d85a631f3563dd678c70c82822
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935495"
---
# <a name="ianalysisregionintersectrectangle-method"></a>IAnalysisRegion::IntersectRectangle (método)

Restringe el área de esta [**región IAnalysisRegion**](ianalysisregion.md) al área creada por su intersección con el rectángulo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IntersectRectangle(
  [in] RECT *pIntersectingRectangle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pIntersectingRectangle* \[ En\]
</dt> <dd>

Puntero al rectángulo con el que se va a formar una intersección, en coordenadas de espacio de entrada de lápiz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Las coordenadas del rectángulo están en unidades HIMETRIC.

Si las dos áreas no se intersecan, el área nueva está vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
</dt> <dt>

[**IAnalysisRegion::ExcludeRegion (Método)**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**IAnalysisRegion::IntersectRegion (Método)**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**IAnalysisRegion::UnionRectangle (Método)**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**IAnalysisRegion::UnionRegion (Método)**](ianalysisregion-unionregion.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




