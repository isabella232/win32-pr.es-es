---
description: Se produce cuando IInkAnalyzer mueve un trazo de un objeto IContextNode a otro.
ms.assetid: a90214af-c3ea-4e2a-94b4-bb5746a2b476
title: _IAnalysisProxyEvents::StrokeReparented (Evento IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.StrokeReparented
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1e9262eb7b4ce2b323669eeb084abb597b5fe00488df90fc5fde0b2876b7e953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967874"
---
# <a name="_ianalysisproxyeventsstrokereparented-event"></a>\_Evento IAnalysisProxyEvents::StrokeReparented

Se produce cuando [**IInkAnalyzer**](iinkanalyzer.md) mueve un trazo de un [**objeto IContextNode**](icontextnode.md) a otro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT StrokeReparented(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] LONG         lStrokeIdToMove,
  [in] IContextNode *pSourceContextNode,
  [in] IContextNode *pDestinationContextNode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInkAnalyzer* \[ En\]
</dt> <dd>

Objeto [**IInkAnalyzer**](iinkanalyzer.md) que mueve el trazo.

</dd> <dt>

*lStrokeIdToMove* \[ En\]
</dt> <dd>

Identificador del trazo que se moverá.

</dd> <dt>

*pSourceContextNode* \[ En\]
</dt> <dd>

Objeto [**IContextNode**](icontextnode.md) desde el que se mueve el trazo.

</dd> <dt>

*pDestinationContextNode* \[ En\]
</dt> <dd>

Objeto [**IContextNode**](icontextnode.md) al que se mueve el trazo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Use este evento cuando la aplicación mantenga su propia estructura de datos, que se sincroniza con la de [**IInkAnalyzer**](iinkanalyzer.md). Este evento se produce durante la fase de conciliación del análisis de entrada de lápiz o en respuesta a un método **IInkAnalyzer** que mueve los datos de trazo de un [**IContextNode**](icontextnode.md) a otro.

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

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




