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
ms.openlocfilehash: 398a56cf2c30c93a72e061dfe968de24276888f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267684"
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

## <a name="remarks"></a>Observaciones

Devuelve **E \_ INVALIDARG** si *pSubnodeToMove* no es un nodo secundario de [**este IContextNode**](icontextnode.md).

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

[**IContextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




