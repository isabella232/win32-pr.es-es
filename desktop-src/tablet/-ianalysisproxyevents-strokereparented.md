---
description: Se produce cuando IInkAnalyzer mueve un trazo de un objeto IContextNode a otro.
ms.assetid: a90214af-c3ea-4e2a-94b4-bb5746a2b476
title: _IAnalysisProxyEvents::StrokeReparented (evento) (IACom.h)
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
ms.openlocfilehash: a587acb6534641d5d64981ab25247b0e23e4f347
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360032"
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

## <a name="remarks"></a>Observaciones

Use este evento cuando la aplicación mantenga su propia estructura de datos, que se sincroniza con la de [**IInkAnalyzer**](iinkanalyzer.md). Este evento se produce durante la fase de conciliación del análisis de entrada de lápiz o en respuesta a un método **IInkAnalyzer** que mueve los datos de trazo de un [**IContextNode**](icontextnode.md) a otro.

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea Proxy de [datos con análisis de entrada de lápiz.](data-proxy-with-ink-analysis.md)

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

 

 




