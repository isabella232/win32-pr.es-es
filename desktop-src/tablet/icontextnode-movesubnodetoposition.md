---
description: Reordena un objeto IContextNode secundario especificado para el índice especificado.
ms.assetid: 1cee73af-8d5b-4d5d-bc67-a3ac6f4b2462
title: Método IContextNode::MoveSubNodeToPosition (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.MoveSubNodeToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8d48876be10a2c45daca62b3175a358d31ed128ddd3bcb045c052e2d51308c66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773825"
---
# <a name="icontextnodemovesubnodetoposition-method"></a>IContextNode::MoveSubNodeToPosition (método)

Reordena un objeto [**IContextNode secundario**](icontextnode.md) especificado para el índice especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MoveSubNodeToPosition(
  [in] IContextNode *pSubnodeToMove,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSubnodeToMove* \[ En\]
</dt> <dd>

Objeto [**IContextNode**](icontextnode.md) que se moverá.

</dd> <dt>

*ulNewIndex* \[ En\]
</dt> <dd>

Índice de la nueva posición del subnodo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Devuelve **E \_ INVALIDARG** si *pSubnodeToMove* no es un nodo secundario de [**este IContextNode**](icontextnode.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




