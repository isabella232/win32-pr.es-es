---
description: Mueve este objeto IContextNode de la colección de subnodos del nodo de contexto primario a la colección de subnodos del nodo de contexto especificado.
ms.assetid: e19ecbe3-f7aa-499c-86a1-236dc9056fd9
title: 'Método IContextNode:: reparent (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Reparent
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 805b96b2a392a4f7b70aa4ce5913b48ffaf33551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082156"
---
# <a name="icontextnodereparent-method"></a>IContextNode:: reparent (método)

Mueve este objeto [**IContextNode**](icontextnode.md) de la colección de subnodos del nodo de contexto primario a la colección de subnodos del nodo de contexto especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Reparent(
  [in] IContextNode *pNewParent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNewParent* \[ de\]
</dt> <dd>

Nuevo nodo primario de este objeto [**IContextNode**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

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

[**IContextNode::GetParentNode**](icontextnode-getparentnode.md)
</dt> <dt>

[**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




