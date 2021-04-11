---
description: Quita una sugerencia de análisis de IInkAnalyzer.
ms.assetid: ba5498d4-d31c-4b3f-9004-0448e18d4835
title: IInkAnalyzer::D método eleteAnalysisHint (IACom. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154421"
---
# <a name="iinkanalyzerdeleteanalysishint-method"></a>IInkAnalyzer::D método eleteAnalysisHint

Quita una sugerencia de análisis de [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteAnalysisHint(
  [in] IContextNode *pHintToDelete
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pHintToDelete* \[ de\]
</dt> <dd>

La sugerencia de análisis desde [**IInkAnalyzer**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Al quitar una sugerencia de análisis no se marca el área de la sugerencia para su análisis. Para marcar el área dentro de la sugerencia para su reanálisis, use el [**método IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) para establecer la región desfasada en la Unión de la región desfasada actual y el área de la sugerencia de análisis.

La sugerencia se quita del analizador; sin embargo, el propio [**IContextNode**](icontextnode.md) no se elimina.

Este método devuelve un código de error cuando *pHintToDelete* es un [**IContextNode**](icontextnode.md) que no es de tipo AnalysisHint (vea [**IContextNode:: GetType**](icontextnode-gettype.md)).

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

[**IInkAnalyzer:: CreateAnalysisHint (método)**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer:: GetAnalysisHints (método)**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[**IInkAnalyzer:: GetAnalysisHintsByName (método)**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




