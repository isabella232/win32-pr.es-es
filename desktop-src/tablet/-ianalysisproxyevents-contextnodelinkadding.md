---
description: Se produce antes de que el analizador de entrada de lápiz agrega un objeto IContextLink entre dos objetos IContextNode.
ms.assetid: ec56cb8e-5154-45ee-911d-e2a240d19dc3
title: _IAnalysisProxyEvents::ContextNodeLinkAdding (evento) (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkAdding
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 341c551064869532e8b51ddecdbe1d5a78878abd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360342"
---
# <a name="_ianalysisproxyeventscontextnodelinkadding-event"></a>\_Evento IAnalysisProxyEvents::ContextNodeLinkAdding

Se produce antes de que el analizador de entrada de lápiz agrega [**un objeto IContextLink**](icontextlink.md) entre dos [**objetos IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ContextNodeLinkAdding(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeAdded
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInkAnalyzer* \[ En\]
</dt> <dd>

[**IInkAnalyzer agrega**](iinkanalyzer.md) el vínculo.

</dd> <dt>

*pContextLinkToBeAdded* \[ En\]
</dt> <dd>

Objeto [**IContextLink que**](icontextlink.md) se va a agregar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

Use este evento cuando la aplicación mantenga su propia estructura de datos, que se sincroniza con la de [**IInkAnalyzer**](iinkanalyzer.md). Este evento tiene lugar durante la fase de conciliación del análisis de entrada de lápiz o en respuesta a un método del analizador de entrada de lápiz que agrega un nuevo [**IContextLink**](icontextlink.md) a [**un IContextNode**](icontextnode.md).

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [Proxy de datos con análisis de entrada de lápiz.](data-proxy-with-ink-analysis.md)

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

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IInkAnalyzer::Analyze (Método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze (Método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




