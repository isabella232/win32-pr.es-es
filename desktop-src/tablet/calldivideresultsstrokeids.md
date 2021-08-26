---
description: Recupera las propiedades Id de los objetos IInkStrokeDisp de la palabra, línea, párrafo o dibujo correspondientes determinados por el análisis de entrada de lápiz.
ms.assetid: f05ffa3b-2a47-46fe-bb8f-e682aa094b69
title: Función CallDivideResultsStrokeIds
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResultsStrokeIds
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 64b3e4180a34c45890408f8ba92cc79465fffa7f1028152e27f8d5c0aa40e3e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009135"
---
# <a name="calldivideresultsstrokeids-function"></a>Función CallDivideResultsStrokeIds

Recupera las propiedades [**Id**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) de los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) de la palabra, línea, párrafo o dibujo correspondientes determinados por el análisis de entrada de lápiz.

Esta función no está pensada para que la utilice el código de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI CallDivideResultsStrokeIds(
  _In_  INT_PTR hDivider,
  _Out_ int     aWordStrokeIds[],
  _Out_ int     aLineStrokeIds[],
  _Out_ int     aParagraphStrokeIds[],
  _Out_ int     aDrawingStrokeIds[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDivider* \[ En\]
</dt> <dd>

Identificador del [objeto Divider.](the-divider-object.md)

</dd> <dt>

*aWordStrokeIds \[ \]* \[out\]
</dt> <dd>

Matriz de los IDs de trazo de la entrada de lápiz de la palabra.

</dd> <dt>

*aLineStrokeIds \[ \]* \[out\]
</dt> <dd>

Matriz de los IDs de trazo de la entrada manuscrita en la línea.

</dd> <dt>

*aParagraphStrokeIds \[ \]* \[out\]
</dt> <dd>

Matriz de los IDs de trazo de la entrada manuscrita en el párrafo.

</dd> <dt>

*aDrawingStrokeIds \[ \]* \[out\]
</dt> <dd>

Matriz de los IDs de trazo de la entrada manuscrita en el dibujo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función puede devolver uno de estos valores.



| Código devuelto                                                                                  | Descripción                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | La función se ha realizado correctamente.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El *parámetro hDivider* no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




