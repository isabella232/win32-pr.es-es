---
description: 'Aplica los resultados de una operación de análisis de tinta de fondo en el árbol de nodos de contexto para las partes del árbol que no ha sido modificada por la aplicación desde la llamada al método IInkAnalyzer:: BackgroundAnalyze.'
ms.assetid: 60e15d4f-6e81-48b9-b7f3-97d2de5c0c1c
title: 'IInkAnalyzer:: reconcile (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Reconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33229c7da47f294f317d2216d9e9bf4f6b114599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648205"
---
# <a name="iinkanalyzerreconcile-method"></a>IInkAnalyzer:: reconciliate (método)

Aplica los resultados de una operación de análisis de tinta de fondo en el árbol de nodos de contexto para las partes del árbol que no ha sido modificada por la aplicación desde la llamada al [**método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Reconcile();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

De forma predeterminada, el [**IInkAnalyzer**](iinkanalyzer.md) realiza una fase de conciliación automática inmediatamente antes de generar los eventos [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) y [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .

Para deshabilitar la reconciliación automática, desactive la marca **AnalysisModes \_ AutomaticReconciliation** de los modos de análisis del analizador de tinta (consulte [**IInkAnalyzer:: SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md) y [**AnalysisModes**](analysismodes.md)). El método [**IInkAnalyzer:: BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) devuelve un error cuando la reconciliación automática está deshabilitada y la aplicación no controla el evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) . La aplicación debe llamar al método de **método IInkAnalyzer:: Reconciliate** para que [**IInkAnalyzer**](iinkanalyzer.md) pueda continuar procesando los resultados o continuar el análisis de la fase de análisis correspondiente.

La aplicación puede realizar cambios, como agregar o quitar trazos y cambiar los datos del trazo, en el árbol de nodos de contexto del objeto [**IInkAnalyzer**](iinkanalyzer.md) durante el análisis en segundo plano. Estos cambios pueden invalidar partes de los resultados del análisis en segundo plano. Este método aplica solo los resultados del análisis al árbol de nodos de contexto del analizador para las partes del árbol que la aplicación no ha cambiado. Este método también agrega regiones que contienen resultados de análisis invalidados a la región desfasada del objeto **IInkAnalyzer** (vea el [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Para obtener más información acerca del uso de para analizar la entrada manuscrita, consulte [información general del análisis de tinta](ink-analysis-overview.md). [**AnalysisModes**](analysismodes.md)

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

[**IInkAnalyzer:: BackgroundAnalyze (método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




