---
description: Determina si el objeto IAnalysisRegion especificado contiene el mismo valor que el objeto IAnalysisRegion actual.
ms.assetid: 44c09cfe-65fc-4175-ad05-01c605218c58
title: Método IAnalysisRegion::EqualsRegion (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.EqualsRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: aecf7bd065c2da0c507c2424c0305526510c9d4f64844dfa229183cf43d5554a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596805"
---
# <a name="ianalysisregionequalsregion-method"></a>IAnalysisRegion::EqualsRegion (método)

Determina si el objeto [**IAnalysisRegion**](ianalysisregion.md) especificado contiene el mismo valor que el objeto **IAnalysisRegion** actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EqualsRegion(
  [in]  IAnalysisRegion *pOtherRegion,
  [out] VARIANT_BOOL    *pfRegionsEqual
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOtherRegion* \[ En\]
</dt> <dd>

Objeto [**IAnalysisRegion**](ianalysisregion.md) que se comparará con el **objeto IAnalysisRegion actual.**

</dd> <dt>

*pfRegionsEqual* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE** si la [**IAnalysisRegion especificada**](ianalysisregion.md) contiene el mismo valor que la IAnalysisRegion actual; en caso contrario, **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

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
</dt> </dl>

 

 




