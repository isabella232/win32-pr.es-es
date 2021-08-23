---
description: Recupera el objeto IContextNode que es el destino de este IContextLink.
ms.assetid: 7e185e69-821b-409b-bc58-d89a4aefeb23
title: Método IContextLink::GetDestinationNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetDestinationNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1a11d9021d4299a1823fee57ed9a80237b4896459b0396a8ba4b140bd377bb80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967461"
---
# <a name="icontextlinkgetdestinationnode-method"></a>IContextLink::GetDestinationNode (método)

Recupera el objeto [**IContextNode**](icontextnode.md) que es el destino de [**este objeto IContextLink.**](icontextlink.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDestinationNode(
  [out] IContextNode **ppDstContextNodeId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDstContextNodeId* \[ out\]
</dt> <dd>

Puntero al objeto [**IContextNode**](icontextnode.md) que es el destino de [**este objeto IContextLink.**](icontextlink.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppDstContextNodeId* cuando ya no necesite usar el nodo de destino.

 

Si el [**objeto IContextLink**](icontextlink.md) se vincula entre un nodo que contiene escritura y un nodo que contiene dibujo, el nodo de destino suele ser el nodo que contiene escritura.

Si el [**objeto IContextLink**](icontextlink.md) tiene un tipo de vínculo Encloses (vea [**IContextLink::GetContextLinkDirection),**](icontextlink-getcontextlinkdirection.md)el nodo de destino es el objeto [**IContextNode**](icontextnode.md) que se incluye.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

