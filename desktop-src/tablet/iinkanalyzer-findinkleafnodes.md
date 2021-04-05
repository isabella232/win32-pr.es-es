---
description: Recupera todos los nodos de hoja de tinta.
ms.assetid: 988ae9f9-8fca-4757-8eb0-ae161e5690c9
title: 'IInkAnalyzer:: FindInkLeafNodes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d5ebcfe542ab03f2e3d3a24c29142e41433c9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908014"
---
# <a name="iinkanalyzerfindinkleafnodes-method"></a>IInkAnalyzer:: FindInkLeafNodes (método)

Recupera todos los nodos de hoja de tinta.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindInkLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppContextNodesFound* \[ enuncia\]
</dt> <dd>

Puntero a la colección [**IContextNodes**](icontextnodes.md) que contiene todos los nodos de hoja de tinta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodesFound* cuando ya no necesite usar el objeto.

 

Los nodos hoja no contienen nodos secundarios. Los nodos de tinta contienen datos de trazo. Ejemplos de nodos de hoja de tinta son los objetos InkWord, InkDrawing y InkBullet [**IContextNode**](icontextnode.md) . Para obtener más información, vea [tipos de nodo de contexto](context-node-types.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer:: FindInkLeafNodesForStrokes (método)**](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[**IInkAnalyzer:: FindLeafNodes (método)**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**IInkAnalyzer:: FindNode (método)**](iinkanalyzer-findnode.md)
</dt> <dt>

[**IInkAnalyzer:: FindNodesOfType (método)**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**IInkAnalyzer:: FindNodesOfTypeForStrokes (método)**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**IInkAnalyzer:: FindNodesOfTypeInSubTree (método)**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**IInkAnalyzer:: FindNodesWithCallBack (método)**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer:: FindNodesWithCallBackInSubTree (método)**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

