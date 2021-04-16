---
description: Recupera 10 alternativas de análisis para todas las entradas de lápiz asociadas a IInkAnalyzer.
ms.assetid: 42b702cf-54a3-413b-9f3a-dcdae7c2e89b
title: 'IInkAnalyzer:: GetAlternates (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 37219226e651e286a6d1d63accbd7e548b3b7807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686832"
---
# <a name="iinkanalyzergetalternates-method"></a>IInkAnalyzer:: GetAlternates (método)

Recupera 10 alternativas de análisis para todas las entradas de lápiz asociadas a [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAlternates(
  [out] IAnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppAlternates* \[ enuncia\]
</dt> <dd>

Un puntero a los 10 principales objetos [**IAnalysisAlternate**](ianalysisalternate.md) para todas las entradas de lápiz asociadas a [**IInkAnalyzer**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppAlternates* cuando ya no necesite usar el objeto.

 

La alternativa superior se devuelve como la primera alternativa de la colección.

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

[**IInkAnalyzer:: GetAlternatesForContextNodes (método)**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**IInkAnalyzer:: GetAlternatesForStrokes (método)**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**IInkAnalyzer:: ModifyTopAlternate (método)**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**IInkAnalyzer:: ModifyTopAlternateWithConfirmation (método)**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

