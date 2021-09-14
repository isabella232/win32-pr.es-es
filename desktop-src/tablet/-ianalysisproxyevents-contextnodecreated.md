---
description: Se produce después de que IInkAnalyzer crea un objeto IContextNode.
ms.assetid: b4ba0d3b-da91-4cc7-b071-240155687b83
title: _IAnalysisProxyEvents::ContextNodeCreated (evento) (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeCreated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac06a7fc45604e93408b1bb144ee7e884efd351e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256839"
---
# <a name="_ianalysisproxyeventscontextnodecreated-event"></a>\_Evento IAnalysisProxyEvents::ContextNodeCreated

Se produce después de [**que IInkAnalyzer**](iinkanalyzer.md) crea un [**objeto IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ContextNodeCreated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeCreated
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInkAnalyzer* \[ En\]
</dt> <dd>

[**IInkAnalyzer que crea**](iinkanalyzer.md) el [**objeto IContextNode.**](icontextnode.md)

</dd> <dt>

*pContextNodeCreated* \[ En\]
</dt> <dd>

Nuevo objeto [**IContextNode.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

Use este evento cuando la aplicación mantenga su propia estructura de datos, que se sincroniza con la de [**IInkAnalyzer**](iinkanalyzer.md). Este evento tiene lugar durante la fase de conciliación del análisis de entrada de lápiz o en respuesta a un método del analizador de entrada de lápiz que crea [**un IContextNode**](icontextnode.md).

Cuando [**IInkAnalyzer**](iinkanalyzer.md) crea un [**IContextNode**](icontextnode.md), el nuevo **IContextNode** no contiene trazos, no contiene vínculos a otros objetos **IContextNode** y es posible que no tenga todas sus propiedades establecidas. Además, el nuevo **IContextNode** se agrega al final de la colección de subnodos de su nodo primario (vea [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) e [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md) Después de este evento, **IInkAnalyzer** puede generar los siguientes eventos.

-   Evento [**\_ IAnalysisProxyEvents::StrokeReparented**](-ianalysisproxyevents-strokereparented.md) cuando mueve un trazo de un nodo de contexto a otro.
-   El [**\_ evento IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) cuando agrega un [**IContextLink**](icontextlink.md) a [**un IContextNode**](icontextnode.md).
-   Evento [**\_ IAnalysisProxyEvents::ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) cuando cambia el orden de un [**IContextNode**](icontextnode.md) dentro de la colección de subnodos de su nodo primario.
-   [**IInkAnalyzer**](iinkanalyzer.md) genera el evento [**\_ IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) después de resolver el estado de [**IContextNode**](icontextnode.md) para esta fase de análisis.

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

 

 




