---
description: Se produce antes de que IInkAnalyzer mueva un objeto IContextNode cambiando su nodo primario.
ms.assetid: 91261270-aa7c-4f0a-a790-1b2bf322a3ad
title: _IAnalysisProxyEvents::ContextNodeReparenting (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeReparenting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eafb37fd4083f0ecf7c68eaf45fc3339a730e818864f4be15eca4b94d4bd5b7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857123"
---
# <a name="_ianalysisproxyeventscontextnodereparenting-event"></a>\_Evento IAnalysisProxyEvents::ContextNodeReparenting

Se produce antes de [**que IInkAnalyzer**](iinkanalyzer.md) mueva un [**objeto IContextNode**](icontextnode.md) cambiando su nodo primario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ContextNodeReparenting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pNewParentContextNode,
  [in] IContextNode *pContextNodeToBeReparented
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInkAnalyzer* \[ En\]
</dt> <dd>

Objeto [**IInkAnalyzer**](iinkanalyzer.md) que mueve el [**objeto IContextNode.**](icontextnode.md)

</dd> <dt>

*pNewParentContextNode* \[ En\]
</dt> <dd>

Nuevo objeto [**IContextNode**](icontextnode.md) primario.

</dd> <dt>

*pContextNodeToBeReparented* \[ En\]
</dt> <dd>

Objeto [**IContextNode que**](icontextnode.md) se va a mover.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Use este evento cuando la aplicación mantenga su propia estructura de datos, que se sincroniza con la de [**IInkAnalyzer**](iinkanalyzer.md). Este evento tiene lugar durante la fase de conciliación del análisis de lápiz, o en respuesta a un método que mueve un [**IContextNode**](icontextnode.md) de una colección de subnodos a otro (vea [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) e [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md)

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea Proxy de [datos con análisis de entrada de lápiz.](data-proxy-with-ink-analysis.md)

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

[**IContextNode::GetParentNode**](icontextnode-getparentnode.md)
</dt> <dt>

[**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[**IInkAnalyzer::Analyze (Método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze (Método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




