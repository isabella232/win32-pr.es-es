---
description: Recupera alternativas de análisis para los trazos con los identificadores de trazo especificados.
ms.assetid: e8bc198e-de0b-49b7-9120-4298985dfe64
title: 'IInkAnalyzer:: GetAlternatesForStrokes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 115b2cc1be4ba35614ada6fddd9c9fbcdfa76357
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154416"
---
# <a name="iinkanalyzergetalternatesforstrokes-method"></a>IInkAnalyzer:: GetAlternatesForStrokes (método)

Recupera alternativas de análisis para los trazos con los identificadores de trazo especificados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAlternatesForStrokes(
  [in]  ULONG              ulStrokeIdsCount,
  [in]  LONG               *plStrokes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulStrokeIdsCount* \[ de\]
</dt> <dd>

Número de identificadores de trazo en *plStrokes*.

</dd> <dt>

*plStrokes* \[ de\]
</dt> <dd>

Matriz de identificadores de trazo.

</dd> <dt>

*ulMaximumAlternates* \[ de\]
</dt> <dd>

Número máximo de alternativas de análisis devueltas.

</dd> <dt>

*ppAlternates* \[ enuncia\]
</dt> <dd>

El objeto [**IAnalysisAlternates**](ianalysisalternates.md) que contiene las alternativas de análisis.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppAlternates* cuando ya no necesite usar el objeto.

 

La [**IAnalysisAlternate**](ianalysisalternate.md) superior se devuelve como la primera alternativa de la colección.

Los trazos especificados no tienen que representar áreas adyacentes del documento.

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

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**IInkAnalyzer:: GetAlternates (método)**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**IInkAnalyzer:: GetAlternatesForContextNodes (método)**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**IInkAnalyzer:: ModifyTopAlternate (método)**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**IInkAnalyzer:: ModifyTopAlternateWithConfirmation (método)**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

