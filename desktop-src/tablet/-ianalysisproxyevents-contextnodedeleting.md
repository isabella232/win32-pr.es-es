---
description: Se produce antes de que IInkAnalyzer elimine un objeto IContextNode.
ms.assetid: 9c89198e-cc64-4041-b7a3-457f94c4aeaf
title: 'Evento _IAnalysisProxyEvents:: ContextNodeDeleting (IACom. h)'
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
ms.openlocfilehash: 26488c5657b6d2765534f82b6eacae774adcf561
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707595"
---
# <a name="_ianalysisproxyeventscontextnodedeleting-event"></a>\_Evento IAnalysisProxyEvents:: ContextNodeDeleting

Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) elimine un objeto [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ContextNodeDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToBeDeleted
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInkAnalyzer* \[ de\]
</dt> <dd>

El objeto [**IInkAnalyzer**](iinkanalyzer.md) que elimina el objeto [**IContextNode**](icontextnode.md) .

</dd> <dt>

*pContextNodeToBeDeleted* \[ de\]
</dt> <dd>

El objeto [**IContextNode**](icontextnode.md) que se va a eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Utilice este evento cuando la aplicación mantiene su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md). Este evento se produce durante la fase de conciliación del análisis de tinta o como respuesta a un método del analizador de tintas que elimina un [**IContextNode**](icontextnode.md).

Antes de que [**IInkAnalyzer**](iinkanalyzer.md) elimine un [**IContextNode**](icontextnode.md), el **IInkAnalyzer** quita todos los trazos del nodo de contexto y quita todos los vínculos a otros nodos de contexto. Antes de que se quite el nodo de contexto, el **IInkAnalyzer** puede generar los siguientes eventos.

-   El evento [**\_ IAnalysisProxyEvents:: StrokeReparented**](-ianalysisproxyevents-strokereparented.md) cuando mueve un trazo desde [**IContextNode**](icontextnode.md).
-   El evento [**\_ IAnalysisProxyEvents:: ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) antes de quitar un [**IContextLink**](icontextlink.md) de [**IContextNode**](icontextnode.md).
-   El evento **\_ IAnalysisProxyEvents:: ContextNodeDeleting** antes de quitar un nodo de contexto primario que ya no tiene nodos secundarios.

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).

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

 

 




