---
description: Recupera las propiedades de identificador para los objetos IInkStrokeDisp de la palabra, línea, párrafo o dibujo correspondientes determinados por el análisis de tinta.
ms.assetid: f05ffa3b-2a47-46fe-bb8f-e682aa094b69
title: CallDivideResultsStrokeIds función)
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
ms.openlocfilehash: ee690c9564df3b8c75eca6eec8eeb88b7531f4ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705395"
---
# <a name="calldivideresultsstrokeids-function"></a>CallDivideResultsStrokeIds función)

Recupera las propiedades de [**identificador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) para los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) de la palabra, línea, párrafo o dibujo correspondientes determinados por el análisis de tinta.

Esta función no está pensada para ser utilizada por el código de la aplicación.

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

*hDivider* \[ de\]
</dt> <dd>

Identificador del objeto de [divisor](the-divider-object.md) .

</dd> <dt>

*\[ aWordStrokeIds \]* \[fuera de\]
</dt> <dd>

Matriz de los identificadores de trazo de la tinta de la palabra.

</dd> <dt>

*\[ aLineStrokeIds \]* \[fuera de\]
</dt> <dd>

Matriz de los identificadores de trazo de la entrada de lápiz en la línea.

</dd> <dt>

*\[ aParagraphStrokeIds \]* \[fuera de\]
</dt> <dd>

Matriz de los identificadores de trazo de la entrada de lápiz en el párrafo.

</dd> <dt>

*\[ aDrawingStrokeIds \]* \[fuera de\]
</dt> <dd>

Matriz de los identificadores de trazo de la tinta del dibujo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función puede devolver uno de estos valores.



| Código devuelto                                                                                  | Descripción                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | La función se ha realizado correctamente.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro *hDivider* no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




