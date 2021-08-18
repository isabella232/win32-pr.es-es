---
description: Quita una sugerencia de análisis de IInkAnalyzer.
ms.assetid: ba5498d4-d31c-4b3f-9004-0448e18d4835
title: Método IInkAnalyzer::D eleteAnalysisHint (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.DeleteAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6f514f20ed99f7fc56725f582b815639cb9d8b3179e9e428845d7e066b6e3bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967294"
---
# <a name="iinkanalyzerdeleteanalysishint-method"></a>IInkAnalyzer::D eleteAnalysisHint (método)

Quita una sugerencia de análisis de [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteAnalysisHint(
  [in] IContextNode *pHintToDelete
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pHintToDelete* \[ En\]
</dt> <dd>

Sugerencia de análisis de [**IInkAnalyzer.**](iinkanalyzer.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Quitar una sugerencia de análisis no marca el área de la sugerencia para el reanálisis. Para marcar el área dentro de la sugerencia para reanalysis, use el método [**IInkAnalyzer::SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) para establecer la región desduzca en la unión de la región desusada actual y el área de la sugerencia de análisis.

La sugerencia se quita del analizador; sin embargo, [**el propio IContextNode**](icontextnode.md) no se elimina.

Este método devuelve un código de error cuando *pHintToDelete* es un [**IContextNode**](icontextnode.md) que no es de tipo AnalysisHint (vea [**IContextNode::GetType).**](icontextnode-gettype.md)

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

[**IInkAnalyzer::CreateAnalysisHint (Método)**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer::GetAnalysisHints (Método)**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[**IInkAnalyzer::GetAnalysisHintsByName (Método)**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




