---
description: Determina si el IAnalysisRegion especificado contiene el mismo valor que el objeto IAnalysisRegion actual.
ms.assetid: 44c09cfe-65fc-4175-ad05-01c605218c58
title: 'IAnalysisRegion:: EqualsRegion (método) (IACom. h)'
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
ms.openlocfilehash: 6a647c13f1279cd39e4947b9fdbcc9ed4e1ef4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154449"
---
# <a name="ianalysisregionequalsregion-method"></a>IAnalysisRegion:: EqualsRegion (método)

Determina si el [**IAnalysisRegion**](ianalysisregion.md) especificado contiene el mismo valor que el objeto **IAnalysisRegion** actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EqualsRegion(
  [in]  IAnalysisRegion *pOtherRegion,
  [out] VARIANT_BOOL    *pfRegionsEqual
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOtherRegion* \[ de\]
</dt> <dd>

Objeto [**IAnalysisRegion**](ianalysisregion.md) que se va a comparar con el **IAnalysisRegion** actual.

</dd> <dt>

*pfRegionsEqual* \[ enuncia\]
</dt> <dd>

**Variante \_ TRUE** si el [**IAnalysisRegion**](ianalysisregion.md) especificado contiene el mismo valor que el IAnalysisRegion actual; de lo contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

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
</dt> </dl>

 

 




