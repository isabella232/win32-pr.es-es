---
description: Restringe el área de IAnalysisRegion a la parte de su área que no forma una intersección con la IAnalysisRegion especificada.
ms.assetid: 7a11d2a8-c2ca-4088-b932-8a6c3e789b7f
title: Método IAnalysisRegion::ExcludeRegion (IACom.h)
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
ms.openlocfilehash: 4a26bc234a5a99d2ba692b02097d348b83878c47ea3c9a1cbd21e1558fc41950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092356"
---
# <a name="ianalysisregionexcluderegion-method"></a>IAnalysisRegion::ExcludeRegion (método)

Restringe el área de [**IAnalysisRegion**](ianalysisregion.md) a la parte de su área que no forma una intersección con el **objeto IAnalysisRegion especificado.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ExcludeRegion(
  [in] IAnalysisRegion *pRegionToExclude
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pRegionToExclude* \[ En\]
</dt> <dd>

[**IAnalysisRegion que se**](ianalysisregion.md) va a excluir de este **IAnalysisRegion.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Si las dos áreas no se cruzan, [**esta IAnalysisRegion**](ianalysisregion.md) no cambia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
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

 

 




