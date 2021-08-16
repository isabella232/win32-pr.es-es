---
description: Crea una copia de IAnalysisRegion.
ms.assetid: eb94e1ce-7801-409d-9ae6-e7db0a9b861f
title: Método IAnalysisRegion::Clone (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.Clone
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13bd514396c738f2e5367528dc62833bd3a4dcc195aecf30ee723ea9c09b5bcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596795"
---
# <a name="ianalysisregionclone-method"></a>IAnalysisRegion::Clone (método)

Crea una copia de [**IAnalysisRegion.**](ianalysisregion.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clone(
  [out] IAnalysisRegion **pClonedRegion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pClonedRegion* \[ out\]
</dt> <dd>

Puntero a una copia de [**IAnalysisRegion.**](ianalysisregion.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Este método es eqimio para el sistema. Windows. Método Ink.AnalysisCore.AnalysisRegionBase.Clone del .NET Framework.

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *pClonedRegion* cuando ya no necesite usar la región de análisis clonada.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

