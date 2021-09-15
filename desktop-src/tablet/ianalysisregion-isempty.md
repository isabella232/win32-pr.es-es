---
description: Recupera un valor que indica si IAnalysisRegion representa una región vacía.
ms.assetid: 3a536b01-e7ee-4103-88c4-d83377ea9fdb
title: Método IAnalysisRegion::IsEmpty (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsEmpty
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c1fb4ebbe487119c65f153f78e192de38e6393fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572457"
---
# <a name="ianalysisregionisempty-method"></a>IAnalysisRegion::IsEmpty (método)

Recupera un valor que indica si [**IAnalysisRegion**](ianalysisregion.md) representa una región vacía.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsEmpty(
  [out] VARIANT_BOOL *pfIsEmpty
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pfIsEmpty* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE** si la región representada está vacía; en caso contrario, **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IAnalysisRegion::IsInfinite (Método)**](ianalysisregion-isinfinite.md)
</dt> <dt>

[**IAnalysisRegion::MakeEmpty (Método)**](ianalysisregion-makeempty.md)
</dt> <dt>

[**IAnalysisRegion::MakeInfinite (Método)**](ianalysisregion-makeinfinite.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




