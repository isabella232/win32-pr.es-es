---
description: Obtiene el rectángulo delimitador de IAnalysisRegion.
ms.assetid: 6b9deff7-12e9-4b30-86cb-25b94737d28d
title: 'IAnalysisRegion:: GetBounds (método) (IACom. h)'
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
ms.openlocfilehash: 12bbb8163aa866648a83effc75d668bc4032c8d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810057"
---
# <a name="ianalysisregiongetbounds-method"></a>IAnalysisRegion:: GetBounds (método)

Obtiene el rectángulo delimitador de [**IAnalysisRegion**](ianalysisregion.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBounds(
  [out] RECT *pBoundingRectangle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pBoundingRectangle* \[ enuncia\]
</dt> <dd>

Rectángulo delimitador del [**IAnalysisRegion**](ianalysisregion.md) en coordenadas de espacio de la entrada de lápiz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Los límites se encuentran en coordenadas de espacio de tinta.

Si [**IAnalysisRegion**](ianalysisregion.md) representa un área infinita, los límites izquierdo y superior son **int \_ min**; y los límites derecho e inferior son **int \_ Max**.

Si [**IAnalysisRegion**](ianalysisregion.md) representa un área vacía, todos los límites del rectángulo son 0.

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
</dt> <dt>

[**IAnalysisRegion:: GetRegionScans (método)**](ianalysisregion-getregionscans.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




