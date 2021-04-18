---
description: Recupera todos los objetos IContextNode del tipo especificado que son descendientes del objeto IContextNode especificado.
ms.assetid: 7e57d6ec-fe04-44c6-904f-7a212bbfcd19
title: 'IInkAnalyzer:: FindNodesOfTypeInSubTree (método) (IACom. h)'
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
ms.openlocfilehash: 545e56d297b053b5b6f5dc61f944d6a4f6d4e03c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715207"
---
# <a name="iinkanalyzerfindnodesoftypeinsubtree-method"></a>IInkAnalyzer:: FindNodesOfTypeInSubTree (método)

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

*pNodeType* \[ de\]
</dt> <dd>

**GUID** que especifica el tipo de nodo.

</dd> <dt>

*pContextNodeToSearchFrom* \[ de\]
</dt> <dd>

Objeto [**IContextNode**](icontextnode.md) cuyos descendientes se buscan.

</dd> <dt>

*ppContextNodesFound* \[ enuncia\]
</dt> <dd>

La colección [**IContextNodes**](icontextnodes.md) que contiene todos los nodos de tipo *pNodeType* que son descendientes de *pContextNodeToSearchFrom*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodesFound* cuando ya no necesite usar el objeto.

 

Si [**IInkAnalyzer**](iinkanalyzer.md) no contiene el nodo *pContextNodeToSearchFrom* , este método devuelve un código de error.

La propiedad *pNodeType* debe contener un identificador único global (GUID) de las constantes de [tipos de nodo de contexto](context-node-types.md) .

Si [**IInkAnalyzer**](iinkanalyzer.md) no contiene este [**IContextNode**](icontextnode.md), se devuelve una colección [**IContextNodes**](icontextnodes.md) vacía.

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

[**IInkAnalyzer:: FindInkLeafNodes (método)**](iinkanalyzer-findinkleafnodes.md)
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

[**IInkAnalyzer:: FindNodesWithCallBack (método)**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer:: FindNodesWithCallBackInSubTree (método)**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

