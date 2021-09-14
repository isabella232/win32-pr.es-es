---
description: Recupera todos los objetos IContextNode que coinciden con los criterios especificados y son descendientes del objeto IContextNode especificado.
ms.assetid: 48d0ae97-c4a5-458d-b4c0-fa82f5aed4e5
title: Método IInkAnalyzer::FindNodesWithCallBackInSubTree (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBackInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6b4ba64cd9271158d49ddd72270d4e6f25538672
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251966"
---
# <a name="iinkanalyzerfindnodeswithcallbackinsubtree-method"></a>IInkAnalyzer::FindNodesWithCallBackInSubTree (método)

Recupera todos los objetos [**IContextNode**](icontextnode.md) que coinciden con los criterios especificados y son descendientes del objeto **IContextNode** especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindNodesWithCallBackInSubTree(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [in]  IContextNode             *pContextNodeToSearchFrom,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCriteria* \[ En\]
</dt> <dd>

Objeto [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) que se usa para evaluar si un objeto [**IContextNode**](icontextnode.md) cumple o no los criterios especificados.

</dd> <dt>

*pContextNodeToSearchFrom* \[ En\]
</dt> <dd>

Objeto [**IContextNode**](icontextnode.md) cuyos descendientes se buscan.

</dd> <dt>

*ppContextNodesFound* \[ out\]
</dt> <dd>

Puntero a [**IContextNodes**](icontextnodes.md) que contiene todos los nodos que cumplen los criterios especificados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodesFound* cuando ya no necesite usar el objeto .

 

Si [**IInkAnalyzer**](iinkanalyzer.md) no contiene el nodo *pContextNodeToSearchFrom,* este método devuelve un código de error.

Si [**IInkAnalyzer**](iinkanalyzer.md) no contiene este [**tipo de IContextNode,**](icontextnode.md)se devuelve una colección [**IContextNodes**](icontextnodes.md) vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
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

[**IInkAnalyzer::FindNodesOfTypeInSubTree (Método)**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesWithCallBack (Método)**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

