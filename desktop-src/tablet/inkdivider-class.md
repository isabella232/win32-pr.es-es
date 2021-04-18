---
description: Representa la capacidad de analizar el diseño de una colección de trazos y dividirlos en texto y gráficos.
ms.assetid: 2c8e67fb-1032-4fcc-b419-82bae978daf8
title: Clase InkDivider (Msinkaut15. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDivider
- InkDivider.IInkDivider
api_type:
- COM
api_location:
- Inkdiv.dll
- Inkdiv.dll.dll
ms.openlocfilehash: c0658504303968803bd2abff063694701d121390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688301"
---
# <a name="inkdivider-class"></a>Clase InkDivider

Representa la capacidad de analizar el diseño de una colección de trazos y dividirlos en texto y gráficos.

**InkDivider** tiene estos tipos de miembros:

-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="interfaces"></a>Interfaces

La clase **InkDivider** define estas interfaces.



| Interfaz       | Descripción                                                          |
|:----------------|:---------------------------------------------------------------------|
| **IInkDivider** | Este objeto implementa la interfaz com **IInkDivider** .<br/> |



 

### <a name="methods"></a>Métodos

La clase **InkDivider** tiene estos métodos.



| Método                              | Descripción                                                                                                                                                        |
|:------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dividir**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) | Devuelve un objeto [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) que contiene información estructural sobre los trazos en el objeto **InkDivider** .<br/> |



 

### <a name="properties"></a>Propiedades

La clase **InkDivider** tiene estas propiedades.



| Propiedad                                                             | Tipo de acceso           | Descripción                                                                                                                     |
|:---------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)<br/>               | Lectura/escritura<br/> | Obtiene o establece el alto de escritura a mano esperado en unidades HIMETRIC.<br/>                                                      |
| [**Estableció**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)<br/> | Lectura/escritura<br/> | Obtiene o establece el objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) que se usa para el reconocimiento de escritura a mano.<br/> |
| [**Trazos**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)<br/>                     | Lectura/escritura<br/> | Obtiene o establece la colección [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que contiene el objeto **InkDivider** . <br/>     |



 

## <a name="remarks"></a>Observaciones

Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

El objeto **InkDivider** utiliza el diseño de los trazos, el orden en que se agregan los trazos, la dirección en la que se dibujan los trazos y otros factores para realizar el análisis de la tinta. La colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que analiza el objeto **InkDivider** se encuentra en la propiedad [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) del objeto **InkDivider** . El objeto **InkDivider** analiza dinámicamente la colección InkStrokes a medida que se agrega o se elimina de la colección, pero no realiza ninguna modificación de los trazos.

Los resultados del análisis se devuelven en un objeto [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .

El objeto **InkDivider** usa un objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) para dividir con más precisión los trazos y asignar una cadena de reconocimiento a los resultados.

> [!Note]  
> El objeto **InkDivider** usa los valores de propiedad predeterminados del objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) .

 

Si no asigna un contexto de reconocedor al objeto **InkDivider** , el objeto **InkDivider** sigue analizando la tinta, pero divide los trazos con menos precisión y no asocia el texto con los resultados de la división.

> [!Note]  
> La propiedad [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) debe establecerse antes de agregar trazos a la propiedad [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) . Una vez agregados los trazos al objeto **InkDivider** , no se puede cambiar la propiedad **RecognizerContext** .

 

El **InkDivider** no admite actualmente idiomas verticales. Para que el objeto **InkDivider** reconozca estos idiomas correctamente, el objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) para el lenguaje debe admitir la capacidad de entrada libre y los caracteres deben escribirse de izquierda a derecha.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                               |
| Encabezado<br/>                   | <dl> <dt>Msinkaut15. h (también requiere Msinkaut15 \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Inkdiv.dll</dt> </dl>                                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)
</dt> <dt>

[**Clase InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> <dt>

[Colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

