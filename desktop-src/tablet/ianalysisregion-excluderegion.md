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
ms.openlocfilehash: 13324d872a76a9184e6ea67b227dbd7444684bb9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579484"
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

## <a name="remarks"></a>Observaciones

Si las dos áreas no se cruzan, [**esta IAnalysisRegion**](ianalysisregion.md) no cambia.

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

 

 




