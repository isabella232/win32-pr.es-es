---
description: Se produce antes de que IInkAnalyzer concilia los resultados del análisis para que una aplicación pueda sincronizar los datos con IInkAnalyzer.
ms.assetid: 9daa8723-5234-40d9-ac41-6dcca988a8b4
title: _IAnalysisProxyEvents::InkAnalyzerStateChanging (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.InkAnalyzerStateChanging
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 92535c34b5d107fb1e435e9abe229df46204f236
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360034"
---
# <a name="_ianalysisproxyeventsinkanalyzerstatechanging-event"></a>\_Evento IAnalysisProxyEvents::InkAnalyzerStateChanging

Se produce antes de [**que IInkAnalyzer**](iinkanalyzer.md) concilia los resultados del análisis para que una aplicación pueda sincronizar los datos con **IInkAnalyzer**.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InkAnalyzerStateChanging(
  [in] IInkAnalyzer *pInkAnalyzer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInkAnalyzer* \[ En\]
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) que está a punto de conciliar sus resultados de análisis.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

Use este evento cuando la aplicación mantenga su propia estructura de datos, que se sincroniza con la de [**IInkAnalyzer**](iinkanalyzer.md). Cuando **IInkAnalyzer** genera este evento, la aplicación debe rellenar los subnodos del nodo raíz del analizador de entrada de lápiz (vea [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) e [**IInkAnalyzer::GetRootNode (método).**](iinkanalyzer-getrootnode.md)

[**IInkAnalyzer**](iinkanalyzer.md) genera este evento después de generar el evento [**\_ IAnalysisEvents::ReadyToReconcile.**](-ianalysisevents-readytoreconcile.md) Genera este evento solo mientras se realiza un análisis en segundo plano.

Bloquee la estructura de datos cuando [**IInkAnalyzer**](iinkanalyzer.md) genera el evento **\_ IAnalysisProxyEvents::InkAnalyzerStateChanging.** Los cambios en la estructura de datos durante esta fase de análisis pueden provocar errores en el análisis de entrada de lápiz y la sincronización. Desbloquee la estructura de datos cuando **IInkAnalyzer** genera el evento [**\_ IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) o [**\_ IAnalysisEvents::Results.**](-ianalysisevents-results.md)

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [Proxy de datos con análisis de entrada de lápiz.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer::Analyze (Método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze (Método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




