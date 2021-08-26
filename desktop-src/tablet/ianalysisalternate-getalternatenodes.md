---
description: Obtiene los objetos IContextNode asociados a esta alternativa.
ms.assetid: 6dfae9cc-d9d2-44de-b6cf-80bbcd296390
title: Método IAnalysisAlternate::GetAlternateNodes (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetAlternateNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fbaff3cea515c9636127ce2267b9f05e0c0a0006b96046a7f2474661b3b76f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935525"
---
# <a name="ianalysisalternategetalternatenodes-method"></a>IAnalysisAlternate::GetAlternateNodes (método)

Obtiene los [**objetos IContextNode**](icontextnode.md) asociados a esta alternativa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAlternateNodes(
  [out] IContextNodes **ppAlternateNodes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppAlternateNodes* \[ out\]
</dt> <dd>

Puntero a la colección [**IContextNodes**](icontextnodes.md) que contiene objetos [**IContextNode**](icontextnode.md) asociados a esta alternativa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppAlternateNodes* cuando ya no necesite usar la colección de nodos de contexto.

 

Este método devuelve los nodos de contexto hoja asociados a esta alternativa. Algunos ejemplos de nodos hoja son los nodos de contexto InkWord, TextWord, Image, InkDrawing y InkBulet. Para obtener más información, [**vea IContextNode::GetType**](icontextnode-gettype.md) y [Tipos de nodo de contexto](context-node-types.md).

Dado que corresponden a alternativas, estos objetos [**IContextNode**](icontextnode.md) no son descendientes del **IContextNode** raíz del objeto [**IInkAnalyzer**](iinkanalyzer.md) (vea [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)) a menos que sean la principal alternativa, que es el primer elemento de una colección [**IAnalysisAlternates.**](ianalysisalternates.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> <dt>

[Sistema. Windows. Ink.AnalysisCore.AnalysisAlternateBase.AlternateNodes](ianalysisalternate-getalternatenodes.md)
</dt> </dl>

 

