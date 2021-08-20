---
description: Recupera todos los nodos hoja.
ms.assetid: 5534053c-c5b9-4576-857f-c8af39e821a7
title: Método IInkAnalyzer::FindLeafNodes (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e5f97d428ea6de750e7cd94c3a5459f3d874b97c031189ad4d84f6234298a14c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118043961"
---
# <a name="iinkanalyzerfindleafnodes-method"></a>IInkAnalyzer::FindLeafNodes (método)

Recupera todos los nodos hoja.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppContextNodesFound* \[ out\]
</dt> <dd>

Puntero a la colección [**IContextNodes**](icontextnodes.md) que contiene todos los nodos hoja.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodesFound* cuando ya no necesite usar el objeto .

 

Los nodos hoja no contienen nodos secundarios. Algunos ejemplos de nodos hoja de lápiz son los objetos InkWord, TextWord, Image, InkDrawing e [**InkContextet IContextNode.**](icontextnode.md) Para obtener más información, vea [Tipos de nodo de contexto.](context-node-types.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::FindInkLeafNodes (Método)**](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[**IInkAnalyzer::FindInkLeafNodesForStrokes (Método)**](iinkanalyzer-findinkleafnodesforstrokes.md)
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

 

