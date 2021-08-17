---
description: Cambia la alternativa superior actual a la alternativa especificada y borra el tipo de confirmación para todos los objetos IContextNode asociados a la alternativa.
ms.assetid: a4ff7e82-623f-4501-9641-5235c3083757
title: Método IInkAnalyzer::ModifyTopAlternate (IACom.h)
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
ms.openlocfilehash: b35cda4534bc5c791e4815c584f6da5d9972c018283b6c9385f6bad998187505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092045"
---
# <a name="iinkanalyzermodifytopalternate-method"></a>Método IInkAnalyzer::ModifyTopAlternate

Cambia la alternativa superior actual a la alternativa especificada y borra el tipo de confirmación para todos los [**objetos IContextNode**](icontextnode.md) asociados a la alternativa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ModifyTopAlternate(
  [in] IAnalysisAlternate *pAlternate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAlternate* \[ En\]
</dt> <dd>

Objeto [**IAnalysisAlternate**](ianalysisalternate.md) que contiene la nueva alternativa superior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Para obtener alternativas de análisis, use el método [**IInkAnalyzer::GetAlternates**](iinkanalyzer-getalternates.md), [**IInkAnalyzer::GetAlternatesForContextNodes o**](iinkanalyzer-getalternatesforcontextnodes.md)el método [**IInkAnalyzer::GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md). Para obtener los [**objetos IContextNode**](icontextnode.md) asociados a una alternativa de análisis, use el método [**IAnalysisAlternate::GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).

Para cambiar el tipo de confirmación de un nodo de contexto, use [**IContextNode::Confirm**](icontextnode-confirm.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**ConfirmationType**](confirmationtype.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




