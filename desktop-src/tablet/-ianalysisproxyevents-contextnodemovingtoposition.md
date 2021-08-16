---
description: Se produce antes de que IInkAnalyzer mueva un objeto IContextNode a una nueva posición dentro de la colección de subnodos de su nodo primario.
ms.assetid: c7a5956e-ffc4-4205-9de3-e8b7d672156d
title: _IAnalysisProxyEvents::ContextNodeMovingToPosition (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeMovingToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4cd814e45692d90c77bad8c46fea5dfd8534bd769a07a9d0bc1648ecafc7b2f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857154"
---
# <a name="_ianalysisproxyeventscontextnodemovingtoposition-event"></a>\_Evento IAnalysisProxyEvents::ContextNodeMovingToPosition

Se produce antes de [**que IInkAnalyzer**](iinkanalyzer.md) mueva un objeto [**IContextNode**](icontextnode.md) a una nueva posición dentro de la colección de subnodos de su nodo primario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ContextNodeMovingToPosition(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pISubNodeToMove,
  [in] IContextNode *pParentContextNode,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInkAnalyzer* \[ En\]
</dt> <dd>

Objeto [**IInkAnalyzer**](iinkanalyzer.md) que mueve el [**objeto IContextNode.**](icontextnode.md)

</dd> <dt>

*pISubNodeToMove* \[ En\]
</dt> <dd>

Objeto [**IContextNode**](icontextnode.md) que se moverá.

</dd> <dt>

*pParentContextNode* \[ En\]
</dt> <dd>

Objeto [**IContextNode primario**](icontextnode.md) de *pISubNodeToMove.*

</dd> <dt>

*ulNewIndex* \[ En\]
</dt> <dd>

Nueva ubicación de *pISubNodeToMove en* la colección de subnodos de su nodo primario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Use este evento cuando la aplicación mantenga su propia estructura de datos, que se sincroniza con la de [**IInkAnalyzer**](iinkanalyzer.md). Este evento se produce durante la fase de conciliación del análisis de entrada de lápiz o en respuesta a un método del analizador de entrada de lápiz que mueve un [**IContextNode**](icontextnode.md) dentro de la colección de subnodos de su nodo primario (vea [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) e [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md)

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [Proxy de datos con análisis de entrada de lápiz.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
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

[**IContextNode::GetParentNode**](icontextnode-getparentnode.md)
</dt> <dt>

[**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




