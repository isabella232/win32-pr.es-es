---
description: Obtiene los objetos IContextNode asociados a esta alternativa.
ms.assetid: 6dfae9cc-d9d2-44de-b6cf-80bbcd296390
title: 'IAnalysisAlternate:: GetAlternateNodes (método) (IACom. h)'
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
ms.openlocfilehash: dd24581774c2115c9f7ccb6857d0cd4d9e1bfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686834"
---
# <a name="ianalysisalternategetalternatenodes-method"></a>IAnalysisAlternate:: GetAlternateNodes (método)

Obtiene los objetos [**IContextNode**](icontextnode.md) asociados a esta alternativa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAlternateNodes(
  [out] IContextNodes **ppAlternateNodes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppAlternateNodes* \[ enuncia\]
</dt> <dd>

Un puntero a la colección [**IContextNodes**](icontextnodes.md) que contiene objetos [**IContextNode**](icontextnode.md) que están asociados a esta alternativa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppAlternateNodes* cuando ya no necesite usar la colección de nodos de contexto.

 

Este método devuelve los nodos de contexto hoja que están asociados a esta alternativa. Ejemplos de nodos hoja son los nodos de contexto InkWord, TextWord, Image, InkDrawing y InkBullet. Para obtener más información, vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [tipos de nodo de contexto](context-node-types.md).

Dado que se corresponden con alternativas, estos [**objetos IContextNode**](icontextnode.md) no son descendientes del **IContextNode** raíz del objeto [**IInkAnalyzer**](iinkanalyzer.md) (vea el [**método IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)) a menos que sean la alternativa superior, que es el primer elemento de una colección [**IAnalysisAlternates**](ianalysisalternates.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> <dt>

[System. Windows. Ink. AnalysisCore. AnalysisAlternateBase. AlternateNodes](ianalysisalternate-getalternatenodes.md)
</dt> </dl>

 

