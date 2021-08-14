---
description: Representa la capacidad de analizar el diseño de una colección de trazos y dividirlos en texto y gráficos.
ms.assetid: 2c8e67fb-1032-4fcc-b419-82bae978daf8
title: Clase InkDivider (Msyecciónut15.h)
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
ms.openlocfilehash: d7dd98aaef627bac6a26340464c14c4e46c07d6a23f32c2664651503b5d79014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220836"
---
# <a name="inkdivider-class"></a>InkDivider (clase)

Representa la capacidad de analizar el diseño de una colección de trazos y dividirlos en texto y gráficos.

**InkDivider tiene** estos tipos de miembros:

-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="interfaces"></a>Interfaces

La **clase InkDivider** define estas interfaces.



| Interfaz       | Descripción                                                          |
|:----------------|:---------------------------------------------------------------------|
| **IInkDivider** | Este objeto implementa la **interfaz COM IInkDivider.**<br/> |



 

### <a name="methods"></a>Métodos

La **clase InkDivider** tiene estos métodos.



| Método                              | Descripción                                                                                                                                                        |
|:------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dividir**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) | Devuelve un [**objeto IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) que contiene información estructural sobre los trazos del **objeto InkDivider.**<br/> |



 

### <a name="properties"></a>Propiedades

La **clase InkDivider** tiene estas propiedades.



| Propiedad                                                             | Tipo de acceso           | Descripción                                                                                                                     |
|:---------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)<br/>               | Lectura/escritura<br/> | Obtiene o establece el alto de escritura a mano esperado en unidades HIMETRIC.<br/>                                                      |
| [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)<br/> | Lectura/escritura<br/> | Obtiene o establece el [**objeto InkRecognizerContext**](inkrecognizercontext-class.md) usado para el reconocimiento de escritura a mano.<br/> |
| [**Trazos**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)<br/>                     | Lectura/escritura<br/> | Obtiene o establece la [**colección InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) contenida en el **objeto InkDivider.** <br/>     |



 

## <a name="remarks"></a>Comentarios

Se puede crear una instancia de este objeto llamando al [**método CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

El **objeto InkDivider** usa el diseño de los trazos, el orden en el que se agregan los trazos, la dirección en la que se dibujan los trazos y otros factores para realizar el análisis de la entrada de lápiz. La [colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que analiza el objeto **InkDivider** se encuentra en la propiedad [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) del **objeto InkDivider.** El **objeto InkDivider** analiza dinámicamente la colección InkStrokes a medida que agrega o elimina de la colección, pero no realiza ninguna modificación de los trazos.

Los resultados del análisis se devuelven en [**un objeto IInkDivisionResult.**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)

El **objeto InkDivider** usa un objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) para dividir con más precisión los trazos y asignar una cadena de reconocimiento a los resultados.

> [!Note]  
> El **objeto InkDivider** usa la configuración de propiedad predeterminada del [**objeto InkRecognizerContext.**](inkrecognizercontext-class.md)

 

Si no asigna un contexto de reconocedor al objeto **InkDivider,** el objeto **InkDivider** sigue analizando la entrada de lápiz, pero divide los trazos con menos precisión y no asocia texto a los resultados de división.

> [!Note]  
> La [**propiedad RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) debe establecerse antes de agregar trazos a la [**propiedad Strokes.**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) Después de agregar trazos al **objeto InkDivider,** no se puede cambiar la propiedad **RecognizerContext.**

 

**InkDivider** no admite actualmente idiomas verticales. Para que el objeto **InkDivider** reconozca estos idiomas correctamente, el objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) del lenguaje debe admitir la funcionalidad de entrada libre y los caracteres deben escribirse de izquierda a derecha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                               |
| Header<br/>                   | <dl> <dt>Msgniut15.h (también requiere Ms ashut15 \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Inkdiv.dll</dt> </dl>                                   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkDivisionResult (interfaz)**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)
</dt> <dt>

[**InkRecognizerContext (clase)**](inkrecognizercontext-class.md)
</dt> <dt>

[Colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

