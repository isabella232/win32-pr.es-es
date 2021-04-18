---
description: Modifica el tipo de confirmación, que controla lo que el objeto IInkAnalyzer puede cambiar sobre IContextNode.
ms.assetid: a506f27e-3909-453e-a2f3-10d4c04d78a4
title: 'IContextNode:: confirm (método) (IACom. h)'
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
ms.openlocfilehash: 3703bb735c0707c412b7c1e41c43819904d83ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652436"
---
# <a name="icontextnodeconfirm-method"></a>IContextNode:: confirm (método)

Modifica el tipo de confirmación, que controla lo que el objeto [**IInkAnalyzer**](iinkanalyzer.md) puede cambiar sobre [**IContextNode**](icontextnode.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Confirm(
  [in] ConfirmationType confirmedType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*confirmedType* \[ de\]
</dt> <dd>

[**ConfirmationType**](confirmationtype.md) que se aplica al nodo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Use este método para permitir que el usuario final confirme que [**IInkAnalyzer**](iinkanalyzer.md) ha analizado correctamente los trazos. Después de llamar a **IContextNode:: CONFIRM** , **IInkAnalyzer** no cambiará los objetos [**IContextNode**](icontextnode.md) para esos trazos durante el análisis posterior.

Use **IContextNode:: CONFIRM** cuando el usuario haya confirmado los resultados del análisis y no desee que [**IInkAnalyzer**](iinkanalyzer.md) cambie un [**IContextNode**](icontextnode.md) durante el análisis posterior. Por ejemplo, si el usuario escribe la palabra "en" y, a continuación, la aplicación llama al [**método IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md), el analizador de tinta genera un nodo InkWord con el valor de "a". Si el usuario agrega entonces "me" después de "to" como una palabra y la aplicación llama de nuevo al **método IInkAnalyzer:: Analyze** , el analizador de tinta puede quitar el nodo InkWord anterior y crear un nuevo nodo InkWord con el valor "Tomé". Sin embargo, si después de la primera llamada al **método IInkAnalyzer:: Analyze**, la aplicación llama a **IContextNode:: CONFIRM** en el nodo InkWord de "to" con el valor [**ConfirmationType**](confirmationtype.md) **NodeTypeAndProperties**, antes de que el usuario agregue "me", cuando la aplicación llama al **método IInkAnalyzer:: Analyze**, el analizador de tinta no quita ni cambia el nodo "to". En su lugar, el analizador de tinta puede reconocer dos nodos InkWord para "to" y "me".

[**IContextNode**](icontextnode.md) solo puede confirmar objetos de tipo InkWord y InkDrawing (consulte [tipos de nodos de contexto](context-node-types.md)). **IContextNode:: CONFIRM** devuelve **E \_ INVALIDARG** cuando el nodo no es un nodo hoja.

El [**método IInkAnalyzer:: RemoveStroke**](iinkanalyzer-removestroke.md) y [**IInkAnalyzer:: RemoveStrokes**](iinkanalyzer-removestrokes.md) no confirman ningún nodo del que se quiten los datos de trazo.

[**IContextNode:: SetStrokes**](icontextnode-setstrokes.md), [**IInkAnalyzer:: SetStrokesType**](iinkanalyzer-setstrokestype.md)y [**IInkAnalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md) devuelven el **núcleo \_ E \_ INVALIDOPERATION** si el objeto [**IContextNode**](icontextnode.md) ya está confirmado.

[**IContextNode:: ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) devuelve un error si se confirma el nodo de origen o de destino.

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

[**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




