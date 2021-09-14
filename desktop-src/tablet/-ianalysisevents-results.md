---
description: Se produce cuando finaliza la fase de análisis final.
ms.assetid: 97318c2d-980e-436c-b97d-e064bace5bf0
title: _IAnalysisEvents::Results (evento, IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Results
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bd52a5ce4563827fb22a00f79113fe1e80e852b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256850"
---
# <a name="_ianalysiseventsresults-event"></a>\_Evento IAnalysisEvents::Results

Se produce cuando finaliza la fase de análisis final.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Results(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInkAnalyzer* \[ En\]
</dt> <dd>

[**IInkAnalyzer que**](iinkanalyzer.md) genera los resultados del análisis.

</dd> <dt>

*pAnalysisStatus* \[ En\]
</dt> <dd>

Objeto [**IAnalysisStatus**](ianalysisstatus.md) que representa el estado del análisis.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

[**IInkAnalyzer**](iinkanalyzer.md) genera este evento después de haber conciliado los resultados de la fase de análisis final.

Si la aplicación llama [**al método IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md), este evento indica cuándo están listos los resultados del análisis.

Si la aplicación mantiene su propia estructura de datos, que se sincroniza con la de [**IInkAnalyzer,**](iinkanalyzer.md)este evento indica que **IInkAnalyzer** ha terminado de realizar cambios en sus datos internos para esta fase de análisis.

Bloquee la estructura de datos cuando [**IInkAnalyzer**](iinkanalyzer.md) genera el evento [**\_ IAnalysisProxyEvents::InkAnalyzerStateChanging.**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Los cambios en la estructura de datos durante esta fase de análisis pueden provocar errores en el análisis de entrada de lápiz y la sincronización. Desbloquee la estructura de datos cuando **IInkAnalyzer** genera el evento [**\_ IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) o **\_ IAnalysisEvents::Results.**

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea Proxy de [datos con análisis de entrada de lápiz.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::Analyze (Método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze (Método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




