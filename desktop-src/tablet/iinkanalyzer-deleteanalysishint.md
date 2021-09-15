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
ms.openlocfilehash: f84f718701abd5bc76b55427aab9df072f758c3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572408"
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

## <a name="remarks"></a>Observaciones

Quitar una sugerencia de análisis no marca el área de la sugerencia para el reanálisis. Para marcar el área dentro de la sugerencia para el reanálisis, use el método [**IInkAnalyzer::SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) para establecer la región desusada en la unión de la región desusada actual y el área de la sugerencia de análisis.

La sugerencia se quita del analizador; sin embargo, [**el propio IContextNode**](icontextnode.md) no se elimina.

Este método devuelve un código de error cuando *pHintToDelete* es un [**IContextNode**](icontextnode.md) que no es de tipo AnalysisHint (vea [**IContextNode::GetType**](icontextnode-gettype.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

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

 

 




