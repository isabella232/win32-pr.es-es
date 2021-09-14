---
description: Recupera el objeto IContextNode para un identificador único global (GUID) especificado.
ms.assetid: b8340666-98ab-4d8c-93c7-58ed05ef30d2
title: Método IInkAnalyzer::FindNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 66771678253f1724653d87ad9c54d474a9ceceb1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256737"
---
# <a name="iinkanalyzerfindnode-method"></a>IInkAnalyzer::FindNode (método)

Recupera el [**objeto IContextNode**](icontextnode.md) para un identificador único global (GUID) especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindNode(
  [in]  const GUID         *pId,
  [out]       IContextNode **ppContextNodeFound
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pId* \[ En\]
</dt> <dd>

Identificador del objeto [**IContextNode.**](icontextnode.md)

</dd> <dt>

*ppContextNodeFound* \[ out\]
</dt> <dd>

Puntero al objeto [**IContextNode**](icontextnode.md) con el *identificador pId.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodeFound* cuando ya no necesite usar el objeto .

 

Si no existe ningún [**objeto IContextNode**](icontextnode.md) como descendiente del nodo raíz [**IInkAnalyzer,**](iinkanalyzer.md) **se devuelve NULL.**

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

[**IInkAnalyzer::FindInkLeafNodesForStrokes (Método)**](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[**IInkAnalyzer::FindLeafNodes (Método)**](iinkanalyzer-findleafnodes.md)
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

 

