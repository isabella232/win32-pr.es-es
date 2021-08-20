---
description: Se produce antes de que IInkAnalyzer elimine un objeto IContextNode.
ms.assetid: 9c89198e-cc64-4041-b7a3-457f94c4aeaf
title: _IAnalysisProxyEvents::ContextNodeDeleting (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 0610aa6a68814e291b3d0da09669eb6834ed78de0bcfc88044668733e325b033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675581"
---
# <a name="_ianalysisproxyeventscontextnodedeleting-event"></a>\_Evento IAnalysisProxyEvents::ContextNodeDeleting

Se produce antes de [**que IInkAnalyzer**](iinkanalyzer.md) elimine un [**objeto IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ContextNodeDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToBeDeleted
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInkAnalyzer* \[ En\]
</dt> <dd>

Objeto [**IInkAnalyzer**](iinkanalyzer.md) que elimina el [**objeto IContextNode.**](icontextnode.md)

</dd> <dt>

*pContextNodeToBeDeleted* \[ En\]
</dt> <dd>

Objeto [**IContextNode**](icontextnode.md) que se va a eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Use este evento cuando la aplicación mantenga su propia estructura de datos, que se sincroniza con la de [**IInkAnalyzer**](iinkanalyzer.md). Este evento tiene lugar durante la fase de conciliación del análisis de entrada de lápiz o en respuesta a un método del analizador de entrada de lápiz que elimina un [**IContextNode**](icontextnode.md).

Antes de [**que IInkAnalyzer**](iinkanalyzer.md) elimine un [**IContextNode**](icontextnode.md), **IInkAnalyzer** quita todos los trazos del nodo de contexto y quita todos los vínculos a otros nodos de contexto. Antes de quitar el nodo de contexto, **IInkAnalyzer** puede generar los siguientes eventos.

-   Evento [**\_ IAnalysisProxyEvents::StrokeReparented**](-ianalysisproxyevents-strokereparented.md) cuando mueve un trazo desde [**IContextNode**](icontextnode.md).
-   Evento [**\_ IAnalysisProxyEvents::ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) antes de quitar un [**IContextLink**](icontextlink.md) de [**IContextNode**](icontextnode.md).
-   El **\_ evento IAnalysisProxyEvents::ContextNodeDeleting** antes de quitar un nodo de contexto primario que ya no tiene nodos secundarios.

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea Proxy de [datos con análisis de entrada de lápiz.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
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

 

 




