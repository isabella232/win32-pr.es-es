---
description: Cambia la alternativa superior actual a la alternativa especificada y borra el tipo de confirmación de todos los objetos IContextNode asociados con la alternativa.
ms.assetid: a4ff7e82-623f-4501-9641-5235c3083757
title: 'IInkAnalyzer:: ModifyTopAlternate (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da2fcde7015e993e13e47673b271c560b6c3d72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715203"
---
# <a name="iinkanalyzermodifytopalternate-method"></a>IInkAnalyzer:: ModifyTopAlternate (método)

Cambia la alternativa superior actual a la alternativa especificada y borra el tipo de confirmación de todos los objetos [**IContextNode**](icontextnode.md) asociados con la alternativa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ModifyTopAlternate(
  [in] IAnalysisAlternate *pAlternate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAlternate* \[ de\]
</dt> <dd>

Objeto [**IAnalysisAlternate**](ianalysisalternate.md) que contiene el nuevo alternativo superior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Para obtener alternativas de análisis, use el método [**IInkAnalyzer:: GetAlternates**](iinkanalyzer-getalternates.md), el método [**IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)o [**IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md). Para obtener los objetos [**IContextNode**](icontextnode.md) asociados a una alternativa de análisis, use el [**método IAnalysisAlternate:: GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).

Para cambiar el tipo de confirmación de un nodo de contexto, use [**IContextNode:: CONFIRM**](icontextnode-confirm.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**ConfirmationType**](confirmationtype.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




