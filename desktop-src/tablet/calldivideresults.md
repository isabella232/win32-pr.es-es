---
description: Recupera los resultados del análisis del objeto InkDivider.
ms.assetid: 7fc2bb5a-172f-4f4e-84dd-e31925f86982
title: CallDivideResults función)
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
ms.openlocfilehash: 11878e6a0ac953b9b7eb27ce21bb67001f9d88d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153597"
---
# <a name="calldivideresults-function"></a>CallDivideResults función)

Recupera los resultados del análisis del objeto [**InkDivider**](inkdivider-class.md) .

Esta función no está pensada para ser utilizada por el código de la aplicación.

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

*hDivider* \[ de\]
</dt> <dd>

Identificador del objeto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*aWordStrokeIds* \[ enuncia\]
</dt> <dd>

Matriz de identificadores asociados a la palabra que se pasa a la clase [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*aLineStrokeIds* \[ enuncia\]
</dt> <dd>

Matriz de propiedades de [**identificador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) para los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) asociados a la línea que se pasa a la clase [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*aParagraphStrokeIds* \[ enuncia\]
</dt> <dd>

Una matriz de las propiedades de [**identificador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) para los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) asociados con el párrafo de la clase [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*aDrawingStrokeIds* \[ enuncia\]
</dt> <dd>

Matriz de propiedades de [**identificador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) para los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) asociados al dibujo de la clase [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pastrWords* \[ enuncia\]
</dt> <dd>

Matriz de palabras devuelta por el análisis de tinta.

</dd> <dt>

*pastrLines* \[ enuncia\]
</dt> <dd>

Matriz de líneas devuelta por el análisis de tinta.

</dd> <dt>

*pastrParagraphs* \[ enuncia\]
</dt> <dd>

Matriz de párrafos devuelta por el análisis de tinta.

</dd> <dt>

*aWordRotationCenterX* \[ enuncia\]
</dt> <dd>

Matriz de los puntos centrales de las palabras a lo largo del eje x del análisis de tinta.

</dd> <dt>

*aWordRotationCenterY* \[ enuncia\]
</dt> <dd>

Matriz de los puntos centrales de las palabras a lo largo del eje y del análisis de tinta.

</dd> <dt>

*aWordAngle* \[ enuncia\]
</dt> <dd>

Una matriz que contiene los ángulos por los que se van a girar las palabras para obtener los mejores resultados del análisis.

</dd> <dt>

*aLineRotationCenterX* \[ enuncia\]
</dt> <dd>

Una matriz que contiene los puntos centrales de las líneas a lo largo del eje x.

</dd> <dt>

*aLineRotationCenterY* \[ enuncia\]
</dt> <dd>

Una matriz que contiene los puntos centrales de las líneas a lo largo del eje y.

</dd> <dt>

*aLineAngle* \[ enuncia\]
</dt> <dd>

Una matriz que contiene los ángulos por los que se giran las líneas para obtener los mejores resultados del análisis.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | La función se ha realizado correctamente.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *hDivider* no es válido.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No se pudo asignar suficiente memoria para almacenar los resultados.<br/> |



 

## <a name="remarks"></a>Observaciones

Para evitar pérdidas de memoria, debe liberar los recursos de *pastrWords*, *pastrLines* y *pastrParagraphs*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




