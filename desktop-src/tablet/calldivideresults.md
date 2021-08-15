---
description: Recupera los resultados del análisis del objeto InkDivider.
ms.assetid: 7fc2bb5a-172f-4f4e-84dd-e31925f86982
title: Función CallDivideResults
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResults
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 2e5f3060f261ba84b70272ed358a7c544f2b0e1582de310ed759b4ea40714359
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967764"
---
# <a name="calldivideresults-function"></a>Función CallDivideResults

Recupera los resultados del análisis del [**objeto InkDivider.**](inkdivider-class.md)

Esta función no está pensada para que la utilice el código de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI CallDivideResults(
  _In_  INT_PTR   hDivider,
  _Out_ int       aWordStrokeIds[],
  _Out_ int       aLineStrokeIds[],
  _Out_ int       aParagraphStrokeIds[],
  _Out_ int       aDrawingStrokeIds[],
  _Out_ SAFEARRAY **pastrWords,
  _Out_ SAFEARRAY **pastrLines,
  _Out_ SAFEARRAY **pastrParagraphs,
  _Out_ int       *aWordRotationCenterX,
  _Out_ int       *aWordRotationCenterY,
  _Out_ float     *aWordAngle,
  _Out_ int       *aLineRotationCenterX,
  _Out_ int       *aLineRotationCenterY,
  _Out_ float     *aLineAngle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDivider* \[ En\]
</dt> <dd>

Identificador del objeto [**InkDivider.**](inkdivider-class.md)

</dd> <dt>

*aWordStrokeIds* \[ out\]
</dt> <dd>

Matriz de identificadores asociados a la palabra que se pasa a la [**clase InkDivider.**](inkdivider-class.md)

</dd> <dt>

*aLineStrokeIds* \[ out\]
</dt> <dd>

Matriz de [**propiedades de identificador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) para los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) asociados a la línea que se pasa a la [**clase InkDivider.**](inkdivider-class.md)

</dd> <dt>

*aParagraphStrokeIds* \[ out\]
</dt> <dd>

Matriz de las [**propiedades de identificador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) de los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) asociados al párrafo de la [**clase InkDivider.**](inkdivider-class.md)

</dd> <dt>

*aDrawingStrokeIds* \[ out\]
</dt> <dd>

Matriz de [**propiedades de identificador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) para los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) asociados al dibujo de la [**clase InkDivider.**](inkdivider-class.md)

</dd> <dt>

*pastrWords* \[ out\]
</dt> <dd>

Matriz de palabras devueltas por el análisis de entrada de lápiz.

</dd> <dt>

*pastrLines* \[ out\]
</dt> <dd>

Matriz de líneas devueltas desde el análisis de entrada de lápiz.

</dd> <dt>

*pastrParagraphs* \[ out\]
</dt> <dd>

Matriz de párrafos devueltos por el análisis de entrada de lápiz.

</dd> <dt>

*aWordRotationCenterX* \[ out\]
</dt> <dd>

Matriz de los puntos centrales de las palabras a lo largo del eje X a partir del análisis de lápiz.

</dd> <dt>

*aWordRotationCenterY* \[ out\]
</dt> <dd>

Matriz de los puntos centrales de las palabras a lo largo del eje Y a partir del análisis de lápiz.

</dd> <dt>

*aWordAngle* \[ out\]
</dt> <dd>

Matriz que contiene los ángulos por los que se giran las palabras para obtener los mejores resultados de análisis.

</dd> <dt>

*aLineRotationCenterX* \[ out\]
</dt> <dd>

Matriz que contiene los puntos centrales de las líneas a lo largo del eje X.

</dd> <dt>

*aLineRotationCenterY* \[ out\]
</dt> <dd>

Matriz que contiene los puntos centrales de las líneas a lo largo del eje Y.

</dd> <dt>

*aLineAngle* \[ out\]
</dt> <dd>

Matriz que contiene los ángulos por los que se giran las líneas para obtener los mejores resultados de análisis.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | La función se ha realizado correctamente.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro hDivider* no es válido.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No se pudo asignar suficiente memoria para almacenar los resultados.<br/> |



 

## <a name="remarks"></a>Comentarios

Para evitar pérdidas de memoria, debe liberar los recursos de *pastrWords*, *pastrLines* y *pastrParagraphs.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




