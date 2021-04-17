---
description: Reordena un objeto IContextNode secundario especificado al índice especificado.
ms.assetid: 1cee73af-8d5b-4d5d-bc67-a3ac6f4b2462
title: 'IContextNode:: MoveSubNodeToPosition (método) (IACom. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696529"
---
# <a name="icontextnodemovesubnodetoposition-method"></a>IContextNode:: MoveSubNodeToPosition (método)

Reordena un objeto [**IContextNode**](icontextnode.md) secundario especificado al índice especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MoveSubNodeToPosition(
  [in] IContextNode *pSubnodeToMove,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSubnodeToMove* \[ de\]
</dt> <dd>

Objeto [**IContextNode**](icontextnode.md) que se va a desplace.

</dd> <dt>

*ulNewIndex* \[ de\]
</dt> <dd>

Índice de la nueva posición del subnodo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Devuelve **E \_ INVALIDARG** si *pSubnodeToMove* no es un nodo secundario de este [**IContextNode**](icontextnode.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




