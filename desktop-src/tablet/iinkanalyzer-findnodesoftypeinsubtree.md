---
description: Recupera todos los objetos IContextNode del tipo especificado que son descendientes del objeto IContextNode especificado.
ms.assetid: 7e57d6ec-fe04-44c6-904f-7a212bbfcd19
title: Método IInkAnalyzer::FindNodesOfTypeInSubTree (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 16e1516a8da5b4d09b80606bad5cf5f9444d82545394543c46b06a05425befa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939964"
---
# <a name="iinkanalyzerfindnodesoftypeinsubtree-method"></a>IInkAnalyzer::FindNodesOfTypeInSubTree (método)

Recupera todos los objetos [**IContextNode**](icontextnode.md) del tipo especificado que son descendientes del objeto **IContextNode** especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindNodesOfTypeInSubTree(
  [in]  const GUID          *pNodeType,
  [in]        IContextNode  *pContextNodeToSearchFrom,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNodeType* \[ En\]
</dt> <dd>

GUID **que** especifica el tipo de nodo.

</dd> <dt>

*pContextNodeToSearchFrom* \[ En\]
</dt> <dd>

Objeto [**IContextNode**](icontextnode.md) cuyos descendientes se buscan.

</dd> <dt>

*ppContextNodesFound* \[ out\]
</dt> <dd>

Colección [**IContextNodes**](icontextnodes.md) que contiene todos los nodos de tipo *pNodeType que* son descendientes de *pContextNodeToSearchFrom*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodesFound* cuando ya no necesite usar el objeto .

 

Si [**IInkAnalyzer**](iinkanalyzer.md) no contiene el nodo *pContextNodeToSearchFrom,* este método devuelve un código de error.

La *propiedad pNodeType* debe contener un identificador único global (GUID) de las constantes [De tipos de nodo de](context-node-types.md) contexto.

Si [**IInkAnalyzer**](iinkanalyzer.md) no contiene ningún [**IContextNode,**](icontextnode.md)se devuelve una colección [**IContextNodes**](icontextnodes.md) vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[**IInkAnalyzer::FindLeafNodes (Método)**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**IInkAnalyzer::FindNode (Método)**](iinkanalyzer-findnode.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesOfType (Método)**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesOfTypeForStrokes (Método)**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesWithCallBack (Método)**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesWithCallBackInSubTree (Método)**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

