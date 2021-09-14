---
description: Crea un nuevo objeto IContextNode secundario.
ms.assetid: 35d2b641-fada-418b-9374-0303c7d318e5
title: Método IContextNode::CreateSubNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreateSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 02c10cc50b90b96cc1ce4aadfa97f86a6c516ed3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267692"
---
# <a name="icontextnodecreatesubnode-method"></a>IContextNode::CreateSubNode (método)

Crea un nuevo objeto [**IContextNode**](icontextnode.md) secundario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateSubNode(
  [in]  const GUID         *pNodeType,
  [out]       IContextNode **ppContextNodeCreated
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNodeType* \[ En\]
</dt> <dd>

GUID **que** representa el tipo de [**IContextNode**](icontextnode.md) que se creará.

</dd> <dt>

*ppContextNodeCreated* \[ out\]
</dt> <dd>

Puntero al nuevo [**IContextNode**](icontextnode.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppContextNodeCreated* cuando ya no necesite usar el nodo de contexto.

 

El nuevo [**IContextNode**](icontextnode.md) se agrega a la colección de nodos secundarios de este nodo de contexto (vea [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md) Cuando hay nodos secundarios existentes, el **IContextNode** recién creado se agrega como el último nodo secundario.

Para obtener una lista de tipos de nodo de contexto, vea [Tipos de nodo de contexto.](context-node-types.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::D eleteSubNode**](icontextnode-deletesubnode.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

