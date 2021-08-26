---
description: Recupera el código de error para la operación de análisis de entrada de lápiz en segundo plano si se produjo un error.
ms.assetid: 0255751e-9b2a-46f1-aa45-6509f9d1c658
title: Método IAnalysisWarning::GetBackgroundError (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetBackgroundError
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: aa8c9c3c60f51ffd854ccdfebb6538337e7676a8c63e45899737333c41d99aad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057965"
---
# <a name="ianalysiswarninggetbackgrounderror-method"></a>IAnalysisWarning::GetBackgroundError (método)

Recupera el código de error para la operación de análisis de entrada de lápiz en segundo plano si se produjo un error.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBackgroundError();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Si se produce un error dentro de una operación de análisis en segundo plano, [**IInkAnalyzer**](iinkanalyzer.md) no puede devolver el código de error porque se está produciendo en un subproceso diferente. En su lugar, el controlador de eventos [**\_ IAnalysisEvents::Results**](-ianalysisevents-results.md) recibe un [**IAnalysisStatus**](ianalysisstatus.md) que contiene [**un objeto IAnalysisWarning**](ianalysiswarning.md) con una [**excepción AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) de **AnalysisWarningCode \_ BackgroundException.** **IAnalysisWarning contiene** el código de error de la operación de análisis en segundo plano. En general, el controlador de eventos **\_ IAnalysisEvents::Results** devolverá este código de error para que se pueda controlar en otra parte de la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze (Método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_IAnalysisEvents::Results**](-ianalysisevents-results.md)
</dt> <dt>

[**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

