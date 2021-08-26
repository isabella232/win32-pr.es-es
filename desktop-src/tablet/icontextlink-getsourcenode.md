---
description: Recupera el objeto IContextNode que es el origen de este IContextLink.
ms.assetid: 2f55ae9c-9f63-4d49-9bf0-9e169b819e79
title: Método IContextLink::GetSourceNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetSourceNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 609f3012608586f7e6c3279cd0dab4232f58ca3e0e31145124622e87684e06f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940415"
---
# <a name="icontextlinkgetsourcenode-method"></a>IContextLink::GetSourceNode (método)

Recupera el objeto [**IContextNode**](icontextnode.md) que es el origen de [**este objeto IContextLink.**](icontextlink.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSourceNode(
  [out] IContextNode **ppSrcContextNodeId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppSrcContextNodeId* \[ out\]
</dt> <dd>

Puntero al objeto [**IContextNode**](icontextnode.md) que es el origen de [**este objeto IContextLink.**](icontextlink.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppSrcContextNodeId* cuando ya no necesite usar el nodo de origen.

 

Si el [**objeto IContextLink**](icontextlink.md) se vincula entre un nodo que contiene escritura y un nodo que contiene dibujo, el nodo de origen suele ser el nodo que contiene el dibujo.

Si el [**objeto IContextLink**](icontextlink.md) tiene un tipo de vínculo Encloses (vea [**IContextLink::GetContextLinkDirection),**](icontextlink-getcontextlinkdirection.md)el nodo de origen es el nodo que incluye el nodo de destino.

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

[**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

