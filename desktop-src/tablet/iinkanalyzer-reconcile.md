---
description: Aplica los resultados de una operación de análisis de entrada de lápiz en segundo plano al árbol de nodos de contexto para las partes del árbol que la aplicación no ha modificado desde la llamada al método IInkAnalyzer::BackgroundAnalyze.
ms.assetid: 60e15d4f-6e81-48b9-b7f3-97d2de5c0c1c
title: Método IInkAnalyzer::Reconcile (IACom.h)
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
ms.openlocfilehash: 3b16497a7f7822bf1557e3e686a81497a4e3723e71f115a1a7d6aa59d8381db2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092035"
---
# <a name="iinkanalyzerreconcile-method"></a>IInkAnalyzer::Reconcile (Método)

Aplica los resultados de una operación de análisis de entrada de lápiz en segundo plano al árbol de nodos de contexto para las partes del árbol que la aplicación no ha modificado desde la llamada al método [**IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Reconcile();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

De forma predeterminada, [**IInkAnalyzer**](iinkanalyzer.md) realiza una fase de conciliación automática inmediatamente antes de generar los eventos [**\_ IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) e [**\_ IAnalysisEvents::Results.**](-ianalysisevents-results.md)

Para deshabilitar la conciliación automática, desactive la marca **AnalysisModes \_ AutomaticRecontineation** de los modos de análisis del analizador de lápiz (vea [**IInkAnalyzer::SetAnalysisModes (Método)**](iinkanalyzer-setanalysismodes.md) y [**AnalysisModes**](analysismodes.md)). El [**método IInkAnalyzer::BackgroundAnalyze Devuelve**](iinkanalyzer-backgroundanalyze.md) un error cuando la conciliación automática está deshabilitada y la aplicación no controla el evento [**\_ IAnalysisEvents::ReadyToReconcile.**](-ianalysisevents-readytoreconcile.md) La aplicación debe llamar al método **IInkAnalyzer::Reconcile para** que [**IInkAnalyzer**](iinkanalyzer.md) pueda continuar procesando los resultados o continuar con el análisis para la fase de análisis correspondiente.

La aplicación puede realizar cambios, como agregar o quitar trazos y cambiar los datos del trazo, en el árbol de nodos de contexto del objeto [**IInkAnalyzer**](iinkanalyzer.md) durante el análisis en segundo plano. Estos cambios pueden invalidar partes de los resultados del análisis en segundo plano. Este método aplica los resultados de análisis solo al árbol de nodos de contexto del analizador para las partes del árbol que la aplicación no ha cambiado. Este método también agrega regiones que contienen resultados de análisis invalidados a la región desdumbre del objeto **IInkAnalyzer** (vea [**IInkAnalyzer::GetDirtyRegion (Método).**](iinkanalyzer-getdirtyregion.md)

Para obtener más información sobre el uso de para analizar la entrada de lápiz, vea [Ink Analysis Overview](ink-analysis-overview.md). [**AnalysisModes**](analysismodes.md)

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

[**IInkAnalyzer::BackgroundAnalyze (Método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




