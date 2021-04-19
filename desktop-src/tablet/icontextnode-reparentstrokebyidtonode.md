---
description: Mueve los datos de trazo desde este IContextNode al IContextNode especificado.
ms.assetid: 583f2de9-d32e-4177-83d1-4abbd0f9f960
title: 'IContextNode:: ReparentStrokeByIdToNode (método) (IACom. h)'
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
ms.openlocfilehash: 3984153a0551de999563b8775ceb5acba1696e39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696528"
---
# <a name="icontextnodereparentstrokebyidtonode-method"></a>IContextNode:: ReparentStrokeByIdToNode (método)

Mueve los datos de trazo desde este [**IContextNode**](icontextnode.md) al **IContextNode** especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReparentStrokeByIdToNode(
  [in] LONG         lStrokeId,
  [in] IContextNode *pContextNodeDestination
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lStrokeId* \[ de\]
</dt> <dd>

Identificador del trazo que se va a desplace.

</dd> <dt>

*pContextNodeDestination* \[ de\]
</dt> <dd>

Objeto [**IContextNode**](icontextnode.md) al que se van a trasladar los datos del trazo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

El objeto [**IContextNode**](icontextnode.md) especificado debe ser uno de los siguientes tipos de las constantes de [tipos de nodo de contexto](context-node-types.md) : **InkWord**, **InkDrawing**, **InkBullet** o **UnclassifiedInk**. Al intentar desplace un trazo a cualquier otro tipo de objeto **IContextNode** , se obtiene un valor devuelto de **E \_ INVALIDARG**.

Se puede llamar a este método desde cualquier objeto [**IContextNode**](icontextnode.md) , incluidos los objetos **IContextNode** de hojas que no son de tinta. Uno de los descendientes de este objeto **IContextNode** debe hacer referencia al trazo especificado o se devuelve **E \_ INVALIDARG** .

Si se confirma este [**IContextNode**](icontextnode.md) o **IContextNode** en *pContextNodeDestination* , se devuelve **E \_ INVALIDARG** (vea [**IContextNode:: IsConfirmed**](icontextnode-isconfirmed.md)).

El analizador de tinta no elimina los nodos de contexto vacíos de su árbol de resultados en respuesta a este método.

-   Un nodo de hoja de tinta que no hace referencia a ningún dato de trazo es un nodo vacío.
-   Un nodo contenedor que no hace referencia A los nodos secundarios es un nodo vacío.

Un nodo vacío genera errores si se encuentra en el árbol durante una operación de análisis de tinta. Para quitar un nodo del árbol del analizador de tinta, llame al método [**IContextNode::D eletesubnode**](icontextnode-deletesubnode.md) del nodo primario (consulte [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md)).

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

[**IContextNode::SetStrokes**](icontextnode-setstrokes.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




