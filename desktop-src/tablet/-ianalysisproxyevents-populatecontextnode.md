---
description: Se produce antes de que IInkAnalyzer realice el análisis dentro de la región de un objeto IContextNode parcialmente rellenado.
ms.assetid: c24e8adb-672f-444a-bccb-1e9e55bea432
title: _IAnalysisProxyEvents::P opulateContextNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.PopulateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ff6378f7ecf3ff597f4c02740e30544ff65651d0a7fcd6d6d490ebabf2161ef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967934"
---
# <a name="_ianalysisproxyeventspopulatecontextnode-event"></a>\_Evento IAnalysisProxyEvents::P opulateContextNode

Se produce antes de [**que IInkAnalyzer**](iinkanalyzer.md) realice el análisis dentro de la región de un objeto [**IContextNode parcialmente**](icontextnode.md) rellenado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PopulateContextNode(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToPopulate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInkAnalyzer* \[ En\]
</dt> <dd>

Objeto [**IInkAnalyzer**](iinkanalyzer.md) a punto de realizar el análisis.

</dd> <dt>

*pContextNodeToPopulate* \[ En\]
</dt> <dd>

Objeto [**IContextNode**](icontextnode.md) parcialmente rellenado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Use este evento cuando la aplicación mantenga su propia estructura de datos, que se sincroniza con la de [**IInkAnalyzer**](iinkanalyzer.md). Cuando **IInkAnalyzer** genera este evento, la aplicación debe rellenar *el elemento pContextNodeToPopulate.* Durante la fase de análisis, **IInkAnalyzer** genera este evento para obtener información de las áreas en las que está analizando la entrada de lápiz.

Si el documento contiene vínculos para *pContextNodeToPopulate,* la aplicación debe crear y agregar estos vínculos. Este proceso requiere que los nodos de origen y de destino, incluidos sus antecesores, se rellenen por completo antes de que se cierre el controlador de eventos para este evento (vea [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) e [**IContextLink::GetDestinationNode).**](icontextlink-getdestinationnode.md)

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [Proxy de datos con análisis de entrada de lápiz.](data-proxy-with-ink-analysis.md)

Durante el análisis en segundo plano, [**IInkAnalyzer**](iinkanalyzer.md) genera este evento después de generar el evento [**\_ IAnalysisEvents::ReadyToReconcile.**](-ianalysisevents-readytoreconcile.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
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

 

 




