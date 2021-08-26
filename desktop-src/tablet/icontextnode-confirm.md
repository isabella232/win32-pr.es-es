---
description: Modifica el tipo de confirmación, que controla lo que el objeto IInkAnalyzer puede cambiar sobre el IContextNode.
ms.assetid: a506f27e-3909-453e-a2f3-10d4c04d78a4
title: Método IContextNode::Confirm (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Confirm
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 248eb78f364f7e938d78846c3e830cc170587961b81dfedcc046e10c59e4fd18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008455"
---
# <a name="icontextnodeconfirm-method"></a>IContextNode::Confirm (método)

Modifica el tipo de confirmación, que controla lo que [**el objeto IInkAnalyzer**](iinkanalyzer.md) puede cambiar sobre [**IContextNode**](icontextnode.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Confirm(
  [in] ConfirmationType confirmedType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*confirmedType* \[ En\]
</dt> <dd>

ConfirmationType [**que**](confirmationtype.md) se aplica al nodo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Use este método para permitir que el usuario final confirme que [**IInkAnalyzer**](iinkanalyzer.md) ha analizado correctamente los trazos. Después de llamar a **IContextNode::Confirm,** **IInkAnalyzer** no cambiará los objetos [**IContextNode**](icontextnode.md) para esos trazos durante el análisis posterior.

Use **IContextNode::Confirm** cuando el usuario haya confirmado los resultados del análisis y no desee que [**IInkAnalyzer**](iinkanalyzer.md) cambie un [**IContextNode**](icontextnode.md) durante el análisis posterior. Por ejemplo, si el usuario escribe la palabra "to" y, a continuación, la aplicación llama al método [**IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md), el analizador de entrada de lápiz genera un nodo InkWord con el valor "to". Si el usuario agrega "me" después de "to" como una palabra y la aplicación llama de nuevo al método **IInkAnalyzer::Analyze,** el analizador de entrada de lápiz puede quitar el nodo InkWord anterior y crear un nuevo nodo InkWord con el valor "tome". Sin embargo, si después de la primera llamada a **IInkAnalyzer::Analyze**(Método), la aplicación llama a **IContextNode::Confirm** en el nodo InkWord para "to" con el valor [**ConfirmationType**](confirmationtype.md) **NodeTypeAndProperties**, antes de que el usuario agrega "me", después, cuando la aplicación llama al método **IInkAnalyzer::Analyze**, el analizador de entrada de lápiz no quita ni cambia el nodo "a". En su lugar, el analizador de entrada de lápiz puede reconocer dos nodos InkWord para "to" y "me".

[**IContextNode solo**](icontextnode.md) puede confirmar objetos de tipo InkWord e InkDrawing (vea [Tipos de nodos de contexto).](context-node-types.md) **IContextNode::Confirm** devuelve **E \_ INVALIDARG** cuando el nodo no es un nodo hoja.

[**El método IInkAnalyzer::RemoveStroke y**](iinkanalyzer-removestroke.md) el método [**IInkAnalyzer::RemoveStrokes**](iinkanalyzer-removestrokes.md) no confirman ningún nodo del que quiten los datos del trazo.

[**IContextNode::SetStrokes**](icontextnode-setstrokes.md), [**IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md)e [**IInkAnalyzer::SetStrokeType**](iinkanalyzer-setstroketype.md) **devuelven CORE \_ E \_ INVALIDOPERATION** si el objeto [**IContextNode**](icontextnode.md) ya está confirmado.

[**IContextNode::ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) devuelve un error si se confirma el nodo de origen o de destino.

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

[**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




