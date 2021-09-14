---
description: Recupera los nodos hoja de entrada de lápiz que contienen los trazos especificados.
ms.assetid: d9ebc57d-63f5-4175-8bb6-a688b98823d4
title: Método IInkAnalyzer::FindInkLeafNodesForStrokes (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d19bed823f5385533dfc938eb9f6013b4a5640c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256742"
---
# <a name="iinkanalyzerfindinkleafnodesforstrokes-method"></a>Método IInkAnalyzer::FindInkLeafNodesForStrokes

Recupera los nodos hoja de entrada de lápiz que contienen los trazos especificados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindInkLeafNodesForStrokes(
  [in]  ULONG         ulStrokeIdsCount,
  [in]  LONG          *plStrokeIds,
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulStrokeIdsCount* \[ En\]
</dt> <dd>

Número de identificadores de trazo pasados.

</dd> <dt>

*plStrokeIds* \[ En\]
</dt> <dd>

Matriz de los identificadores de trazo.

</dd> <dt>

*ppContextNodesFound* \[ out\]
</dt> <dd>

Colección de objetos [**IContextNode**](icontextnode.md) que contienen todos los nodos hoja de entrada de lápiz que contienen los trazos con identificadores de la *matriz plStrokeIds.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodesFound* cuando ya no necesite usar el objeto .

 

Los nodos hoja no contienen nodos secundarios. Los nodos de entrada de lápiz contienen datos de trazo. Algunos ejemplos de nodos hoja de entrada de lápiz son los objetos InkWord, InkDrawing yInk Adret [**IContextNode.**](icontextnode.md) Para obtener más información, vea [Tipos de nodo de contexto.](context-node-types.md)

Si ningún nodo contiene los trazos especificados, se devuelve una colección [**IContextNodes**](icontextnodes.md) vacía. De forma similar, *si ulStrokeIdsCount* es cero, se devuelve una colección **IContextNodes** vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::FindInkLeafNodes (Método)**](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[**IInkAnalyzer::FindLeafNodes (Método)**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**IInkAnalyzer::FindNode (Método)**](iinkanalyzer-findnode.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesOfType (Método)**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesOfTypeForStrokes (Método)**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesOfTypeInSubTree (Método)**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesWithCallBack (Método)**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesWithCallBackInSubTree (Método)**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

