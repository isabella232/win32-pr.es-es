---
description: Se produce antes de que IInkAnalyzer mueva un objeto IContextNode a una nueva posición dentro de la colección de subnodos de su nodo primario.
ms.assetid: c7a5956e-ffc4-4205-9de3-e8b7d672156d
title: 'Evento _IAnalysisProxyEvents:: ContextNodeMovingToPosition (IACom. h)'
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
ms.openlocfilehash: 462e7428fb43fd998d769dd152e19f8109b04158
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707591"
---
# <a name="_ianalysisproxyeventscontextnodemovingtoposition-event"></a>\_Evento IAnalysisProxyEvents:: ContextNodeMovingToPosition

Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) mueva un objeto [**IContextNode**](icontextnode.md) a una nueva posición dentro de la colección de subnodos de su nodo primario.

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

*pInkAnalyzer* \[ de\]
</dt> <dd>

El objeto [**IInkAnalyzer**](iinkanalyzer.md) que mueve el objeto [**IContextNode**](icontextnode.md) .

</dd> <dt>

*pISubNodeToMove* \[ de\]
</dt> <dd>

Objeto [**IContextNode**](icontextnode.md) que se va a desplace.

</dd> <dt>

*pParentContextNode* \[ de\]
</dt> <dd>

Objeto primario [**IContextNode**](icontextnode.md) de *pISubNodeToMove*.

</dd> <dt>

*ulNewIndex* \[ de\]
</dt> <dd>

La nueva ubicación de *pISubNodeToMove* en la colección de subnodos de su nodo primario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Utilice este evento cuando la aplicación mantiene su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md). Este evento se produce durante la fase de conciliación del análisis de tinta o en respuesta a un método del analizador de tinta que mueve un [**IContextNode**](icontextnode.md) dentro de la colección de subnodos de su nodo primario (vea [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) y [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)).

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

[**IContextNode::GetParentNode**](icontextnode-getparentnode.md)
</dt> <dt>

[**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




