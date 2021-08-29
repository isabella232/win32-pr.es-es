---
description: Cambia la alternativa superior actual al IAnalysisAlternate especificado.
ms.assetid: 0867a662-d172-4ca2-a41f-49c0ea454768
title: Método IInkAnalyzer::ModifyTopAlternateWithConfirmation (IACom.h)
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
ms.openlocfilehash: d7c0b98c0abafeb82e56124dc105ac5204dc4322586db200cb54827173ca6c54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773555"
---
# <a name="iinkanalyzermodifytopalternatewithconfirmation-method"></a>Método IInkAnalyzer::ModifyTopAlternateWithConfirmation

Cambia la alternativa superior actual al valor [**IAnalysisAlternate especificado.**](ianalysisalternate.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ModifyTopAlternateWithConfirmation(
  [in] IAnalysisAlternate *alternate,
  [in] VARIANT_BOOL       fconfirmAutomatically
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*alternativa* \[ En\]
</dt> <dd>

Alternativa de análisis que se establecerá como la nueva alternativa superior.

</dd> <dt>

*fconfirmAutomatically* \[ En\]
</dt> <dd>

**VARIANT \_ TRUE para** establecer todos los nodos de contexto de hoja de lápiz que corresponden al análisis alternativo a un tipo de confirmación **de \_ ConfirmationType NodeTypeAndProperties** (vea [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md) y [**ConfirmationType**](confirmationtype.md)); **VARIANT \_ FALSE** para establecer todos los nodos de contexto de hoja de entrada de lápiz que corresponden a la alternativa de análisis a un tipo de confirmación **confirmationType \_ None**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Para obtener alternativas de análisis, use el método [**IInkAnalyzer::GetAlternates**](iinkanalyzer-getalternates.md), [**IInkAnalyzer::GetAlternatesForContextNodes o**](iinkanalyzer-getalternatesforcontextnodes.md)el método [**IInkAnalyzer::GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md). Para obtener los objetos de nodo de contexto asociados a una alternativa de análisis, use el método [**IAnalysisAlternate::GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).

Para cambiar el tipo de confirmación de un nodo de contexto, use [**IContextNode::Confirm**](icontextnode-confirm.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Ink Analysis ConfirmationType**](confirmationtype.md)
</dt> <dt>

[Referencia](ink-analysis-reference.md)
</dt> </dl>

 

 




