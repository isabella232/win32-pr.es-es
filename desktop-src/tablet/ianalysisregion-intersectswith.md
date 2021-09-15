---
description: Determina si el área de IAnalysisRegion forma una intersección con el rectángulo especificado.
ms.assetid: 683c3ad8-0236-474e-a16d-6164c2244cfb
title: Método IAnalysisRegion::IntersectsWith (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectsWith
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 99ff1ce8d3039b04d83f9cdd5c1d6aebe00be407
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570413"
---
# <a name="ianalysisregionintersectswith-method"></a>IAnalysisRegion::IntersectsWith (método)

Determina si el área de [**IAnalysisRegion**](ianalysisregion.md) forma una intersección con el rectángulo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IntersectsWith(
  [in]  RECT         *pRectangle,
  [out] VARIANT_BOOL *pfIsIntersecting
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pRectangle* \[ En\]
</dt> <dd>

Puntero al rectángulo con el que se va a comparar, en coordenadas de espacio de entrada de lápiz.

</dd> <dt>

*pfIsIntersecting* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE** si el área de [**IAnalysisRegion**](ianalysisregion.md) forma una intersección con el rectángulo especificado; en caso contrario, **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

La comparación se realiza en coordenadas de espacio de entrada de lápiz.

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

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




