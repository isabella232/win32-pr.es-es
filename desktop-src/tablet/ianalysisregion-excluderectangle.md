---
description: Restringe el área de IAnalysisRegion a la parte de su área que no forma una intersección con el rectángulo especificado.
ms.assetid: a35b8bfc-a87a-4e9a-908f-2b13a128d222
title: Método IAnalysisRegion::ExcludeRectangle (IACom.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579485"
---
# <a name="ianalysisregionexcluderectangle-method"></a>IAnalysisRegion::ExcludeRectangle (método)

Restringe el área de [**IAnalysisRegion**](ianalysisregion.md) a la parte de su área que no forma una intersección con el rectángulo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ExcludeRectangle(
  [in] RECT *pExcludingRectangle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pExcludingRectangle* \[ En\]
</dt> <dd>

Rectángulo que se va a excluir de [**esta región IAnalysisRegion.**](ianalysisregion.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

Las coordenadas del rectángulo están en unidades HIMETRIC.

Si las dos áreas no se intersecan, [**IAnalysisRegion**](ianalysisregion.md) no cambia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IAnalysisRegion::ExcludeRegion (Método)**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**IAnalysisRegion::IntersectRectangle (Método)**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**IAnalysisRegion::IntersectRegion (Método)**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**IAnalysisRegion::UnionRectangle (Método)**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**IAnalysisRegion::UnionRegion (Método)**](ianalysisregion-unionregion.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




