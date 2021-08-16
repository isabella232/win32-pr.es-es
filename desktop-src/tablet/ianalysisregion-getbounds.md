---
description: Obtiene el rectángulo delimitador de IAnalysisRegion.
ms.assetid: 6b9deff7-12e9-4b30-86cb-25b94737d28d
title: Método IAnalysisRegion::GetBounds (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetBounds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8481ddda9d0d278d2f24873a0c7d8a993c924c816d58153c38de8ef1063e986b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092336"
---
# <a name="ianalysisregiongetbounds-method"></a>IAnalysisRegion::GetBounds (método)

Obtiene el rectángulo delimitador de [**IAnalysisRegion.**](ianalysisregion.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBounds(
  [out] RECT *pBoundingRectangle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pBoundingRectangle* \[ out\]
</dt> <dd>

Rectángulo delimitador de [**IAnalysisRegion**](ianalysisregion.md) en coordenadas de espacio de entrada de lápiz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Los límites están en coordenadas de espacio de entrada de lápiz.

Si [**IAnalysisRegion representa**](ianalysisregion.md) un área infinita, los límites izquierdo y superior son **INT \_ MIN** y los límites derecho e inferior son **INT \_ MAX.**

Si [**IAnalysisRegion representa**](ianalysisregion.md) un área vacía, todos los límites del rectángulo son 0.

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

[**IAnalysisRegion::GetRegionScans (Método)**](ianalysisregion-getregionscans.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




