---
description: Agrega un nuevo IContextLink a la colección de vínculos de contexto del objeto IContextNode.
ms.assetid: b7b9da10-3015-4976-bc4e-1a7f69b7c85b
title: Método IContextNode::AddContextLink (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 515ade35baed591060e76818d2b3e00a3654a89a9d42dda21d170ee54b2773ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967444"
---
# <a name="icontextnodeaddcontextlink-method"></a>IContextNode::AddContextLink (método)

Agrega un nuevo [**IContextLink a**](icontextlink.md) la colección de vínculos de contexto del objeto [**IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddContextLink(
  [in]  IContextNode         *pDestinationNode,
  [in]  ContextLinkDirection linkDirection,
  [out] IContextLink         **ppContextLinkToAdd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDestinationNode* \[ En\]
</dt> <dd>

[**IContextNode de destino**](icontextnode.md) para el nuevo [**IContextLink.**](icontextlink.md)

</dd> <dt>

*linkDirection* \[ En\]
</dt> <dd>

Dirección del objeto [**IContextLink**](icontextlink.md) que se creará.

</dd> <dt>

*ppContextLinkToAdd* \[ out\]
</dt> <dd>

Puntero al nuevo [**objeto IContextLink.**](icontextlink.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppContextLinkToAdd* cuando ya no necesite usar el nodo de contexto.

 

Este [**objeto IContextNode**](icontextnode.md) es el nodo de origen (vea [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md)) para el nuevo [**objeto IContextLink.**](icontextlink.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[**IContextNode::D eleteContextLink**](icontextnode-deletecontextlink.md)
</dt> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

