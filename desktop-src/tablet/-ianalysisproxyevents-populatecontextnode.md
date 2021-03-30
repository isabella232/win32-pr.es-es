---
description: Se produce antes de que IInkAnalyzer realice el análisis dentro de la región de un objeto IContextNode parcialmente rellenado.
ms.assetid: c24e8adb-672f-444a-bccb-1e9e55bea432
title: _IAnalysisProxyEvents::P evento opulateContextNode (IACom. h)
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
ms.openlocfilehash: e8aebe4ba777d62f90aa00c45ea0f1644e2b8183
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279862"
---
# <a name="_ianalysisproxyeventspopulatecontextnode-event"></a>\_IAnalysisProxyEvents::P evento opulateContextNode

Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) realice el análisis dentro de la región de un objeto [**IContextNode**](icontextnode.md) parcialmente rellenado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PopulateContextNode(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToPopulate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInkAnalyzer* \[ de\]
</dt> <dd>

Objeto [**IInkAnalyzer**](iinkanalyzer.md) sobre el que se va a realizar el análisis.

</dd> <dt>

*pContextNodeToPopulate* \[ de\]
</dt> <dd>

Objeto [**IContextNode**](icontextnode.md) parcialmente rellenado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Utilice este evento cuando la aplicación mantiene su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md). Cuando **IInkAnalyzer** genera este evento, la aplicación debe rellenar el *pContextNodeToPopulate*. Durante la fase de análisis, el **IInkAnalyzer** genera este evento para obtener información sobre las áreas en las que está analizando la tinta.

Si el documento contiene vínculos para *pContextNodeToPopulate*, la aplicación debe crear y agregar estos vínculos. Este proceso requiere que los nodos de origen y de destino, incluidos sus antecesores, se rellenen por completo antes de que se cierre el controlador de eventos para este evento (vea [**IContextLink:: GetSourceNode**](icontextlink-getsourcenode.md) y [**IContextLink:: GetDestinationNode**](icontextlink-getdestinationnode.md)).

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).

Durante el análisis en segundo plano, [**IInkAnalyzer**](iinkanalyzer.md) genera este evento después de que se genere el evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer:: Analyze (método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer:: BackgroundAnalyze (método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




