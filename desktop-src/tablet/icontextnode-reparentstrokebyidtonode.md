---
description: Mueve los datos de trazo de este IContextNode al IContextNode especificado.
ms.assetid: 583f2de9-d32e-4177-83d1-4abbd0f9f960
title: Método IContextNode::ReparentStrokeByIdToNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ReparentStrokeByIdToNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a915425900bccb15145546658d51d50dcaee14880f8f219bd1908efaa17bd3c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008415"
---
# <a name="icontextnodereparentstrokebyidtonode-method"></a>IContextNode::ReparentStrokeByIdToNode (método)

Mueve los datos de trazo de [**este IContextNode**](icontextnode.md) al **IContextNode especificado.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReparentStrokeByIdToNode(
  [in] LONG         lStrokeId,
  [in] IContextNode *pContextNodeDestination
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lStrokeId* \[ En\]
</dt> <dd>

Identificador del trazo que se moverá.

</dd> <dt>

*pContextNodeDestination* \[ En\]
</dt> <dd>

Objeto [**IContextNode al**](icontextnode.md) que se mueven los datos del trazo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

El objeto [**IContextNode**](icontextnode.md) especificado debe ser uno de los tipos siguientes de las constantes [Tipos](context-node-types.md) de nodo de contexto: **InkWord,** **InkDrawing,** **Ink Ink Inket** o **UnclassifiedInk.** Al intentar mover un trazo a cualquier otro tipo de objeto **IContextNode,** se devuelve un valor devuelto **de E \_ INVALIDARG**.

Se puede llamar a este método desde cualquier [**objeto IContextNode,**](icontextnode.md) incluidos los objetos **IContextNode** hoja que no son de lápiz. Uno de los descendientes de este objeto **IContextNode** debe hacer referencia al trazo especificado o se devuelve **E \_ INVALIDARG.**

Si se confirma [**este IContextNode**](icontextnode.md) o **IContextNode** en *pContextNodeDestination,* se devuelve **E \_ INVALIDARG** (vea [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)).

El analizador de entrada de lápiz no elimina los nodos de contexto vacíos de su árbol de resultados en respuesta a este método.

-   Un nodo hoja de entrada de lápiz que no hace referencia a ningún dato de trazo es un nodo vacío.
-   Un nodo contenedor que no hace referencia a ningún nodo secundario es un nodo vacío.

Un nodo vacío genera errores si está en el árbol durante una operación de análisis de entrada de lápiz. Para quitar un nodo del árbol del analizador de entrada de lápiz, llame al método [**IContextNode::D eleteSubNode**](icontextnode-deletesubnode.md) del nodo primario (vea [**IContextNode::GetParentNode).**](icontextnode-getparentnode.md)

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

[**IContextNode::SetStrokes**](icontextnode-setstrokes.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




