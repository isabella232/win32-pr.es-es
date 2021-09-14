---
description: Recupera 10 alternativas de análisis para toda la entrada de lápiz asociada a IInkAnalyzer.
ms.assetid: 42b702cf-54a3-413b-9f3a-dcdae7c2e89b
title: Método IInkAnalyzer::GetAlternates (IACom.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251961"
---
# <a name="iinkanalyzergetalternates-method"></a>IInkAnalyzer::GetAlternates (método)

Recupera 10 alternativas de análisis para toda la entrada de lápiz asociada a [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAlternates(
  [out] IAnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppAlternates* \[ out\]
</dt> <dd>

Puntero a los 10 objetos [**IAnalysisAlternate**](ianalysisalternate.md) principales para todos los objetos ink asociados a [**IInkAnalyzer.**](iinkanalyzer.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppAlternates* cuando ya no necesite usar el objeto .

 

La alternativa superior se devuelve como la primera alternativa de la colección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**IInkAnalyzer::GetAlternatesForContextNodes (Método)**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**IInkAnalyzer::GetAlternatesForStrokes (Método)**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**IInkAnalyzer::ModifyTopAlternate (Método)**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**IInkAnalyzer::ModifyTopAlternateWithConfirmation (Método)**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

