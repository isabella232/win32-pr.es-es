---
description: Cambia la alternativa superior actual al IAnalysisAlternate especificado.
ms.assetid: 0867a662-d172-4ca2-a41f-49c0ea454768
title: 'IInkAnalyzer:: ModifyTopAlternateWithConfirmation (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternateWithConfirmation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 60b0221e7d27cfd5d601dcf77e80a297045d39a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360337"
---
# <a name="iinkanalyzermodifytopalternatewithconfirmation-method"></a>IInkAnalyzer:: ModifyTopAlternateWithConfirmation (método)

Cambia la alternativa superior actual al [**IAnalysisAlternate**](ianalysisalternate.md)especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ModifyTopAlternateWithConfirmation(
  [in] IAnalysisAlternate *alternate,
  [in] VARIANT_BOOL       fconfirmAutomatically
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*alternativa* \[ de\]
</dt> <dd>

Alternativa de análisis que se va a establecer como la nueva alternativa superior.

</dd> <dt>

*fconfirmAutomatically* \[ de\]
</dt> <dd>

**Variante \_ TRUE** para establecer todos los nodos de contexto de hoja de tinta que corresponden al análisis alternativo a un tipo de confirmación de **ConfirmationType \_ NodeTypeAndProperties** (vea [**IContextNode:: IsConfirmed**](icontextnode-isconfirmed.md) y [**ConfirmationType**](confirmationtype.md)); **Variante \_ FALSE** para establecer todos los nodos de contexto de hoja de tinta que corresponden al análisis alternativo a un tipo de confirmación de **ConfirmationType \_ ninguno**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Para obtener alternativas de análisis, use el método [**IInkAnalyzer:: GetAlternates**](iinkanalyzer-getalternates.md), el método [**IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)o [**IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md). Para obtener los objetos de nodo de contexto asociados a una alternativa de análisis, use el [**método IAnalysisAlternate:: GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).

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

[**ConfirmationType de análisis de tinta**](confirmationtype.md)
</dt> <dt>

[Referencia](ink-analysis-reference.md)
</dt> </dl>

 

 




