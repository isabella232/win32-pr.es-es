---
description: Representa los atributos que se aplican a la entrada de lápiz cuando se dibuja.
ms.assetid: 10ca7ae5-28dd-42a2-98d9-852d4de5869d
title: Clase InkDrawingAttributes (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDrawingAttributes
- InkDrawingAttributes.IInkDrawingAttributes
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 44b3ef1115539219f7cbf6b700014117ad180d15fe8cdd6d2afe4a0f783a06df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118042353"
---
# <a name="inkdrawingattributes-class"></a>InkDrawingAttributes (clase)

Representa los atributos que se aplican a la entrada de lápiz cuando se dibuja.

**InkDrawingAttributes** tiene estos tipos de miembros:

-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="interfaces"></a>Interfaces

La **clase InkDrawingAttributes** define estas interfaces.



| Interfaz                 | Descripción                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **IInkDrawingAttributes** | Este objeto implementa la **interfaz COM IInkDrawingAttributes.**<br/> |



 

### <a name="methods"></a>Métodos

La **clase InkDrawingAttributes** tiene estos métodos.



| Método                         | Descripción                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone) | Crea un objeto [**InkDisp**](inkdisp-class.md)duplicado, **InkDrawingAttributes** o [**InkRecognizerContext.**](inkrecognizercontext-class.md)<br/> |



 

### <a name="properties"></a>Propiedades

La **clase InkDrawingAttributes** tiene estas propiedades.



| Propiedad                                                                           | Tipo de acceso           | Descripción                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Suavizado de contorno**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_antialiased)<br/>                 | Lectura/escritura<br/> | Obtiene o establece el valor que especifica si los colores de primer plano y de fondo a lo largo del borde de la entrada de lápiz se mezclan para aumentar la suavizado de un trazo de entrada de lápiz.<br/> |
| [**Color**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color)<br/>                             | Lectura/escritura<br/> | Obtiene o establece el color de la entrada de lápiz dibujada con este **objeto InkDrawingAttributes.**<br/>                                                                                    |
| [**ExtendedProperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | Solo lectura<br/>  | Obtiene la colección de datos definidos por la aplicación que se almacenan en el **objeto InkDrawingAttributes.**<br/>                                                                |
| [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve)<br/>                   | Lectura/escritura<br/> | Obtiene o establece el valor que especifica si la entrada manuscrita se representa como una serie de curvas en lugar de como líneas entre puntos de muestra de lápiz.<br/>                                    |
| [**Alto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)<br/>                           | Lectura/escritura<br/> | Obtiene o establece el alto del lápiz al dibujar lápiz con este **objeto InkDrawingAttributes.**<br/>                                                                        |
| [**IgnorePressure**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_ignorepressure)<br/>           | Lectura/escritura<br/> | Obtiene o establece el valor que especifica si la entrada de lápiz dibujada se vuelve más ancha automáticamente con una mayor presión de la punta del lápiz en la superficie de la tableta.<br/>                     |
| [**PenTip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip)<br/>                           | Lectura/escritura<br/> | Obtiene o establece la punta de lápiz que se va a usar (bola o rectángulo) al dibujar la entrada manuscrita con este **objeto InkDrawingAttributes.**<br/>                                                       |
| [**RasterOperation**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation)<br/>         | Lectura/escritura<br/> | Obtiene o establece cómo interactúa el color del lápiz con los colores de fondo existentes en la pantalla cuando se dibuja la entrada manuscrita.<br/>                                                    |
| [**Transparencia**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_transparency)<br/>               | Lectura/escritura<br/> | Obtiene o establece el valor de transparencia de la entrada manuscrita dibujada. Los valores oscilan entre cero (totalmente opaco) y 255 (totalmente transparente).<br/>                                               |
| [**Ancho**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)<br/>                             | Lectura/escritura<br/> | Obtiene o establece el ancho del lápiz al dibujar entrada manuscrita con este **objeto InkDrawingAttributes.**<br/>                                                                         |



 

## <a name="remarks"></a>Comentarios

Se puede crear una instancia de este objeto llamando al [**método CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

Estos atributos de dibujo se pueden asociar con un trazo o un cursor y especificar valores como el color, el ancho y la transparencia.

Para especificar los atributos de dibujo de un trazo, use la [**propiedad DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) del [**objeto IInkStrokeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) Para especificar los atributos de dibujo de todos los trazos dentro de una colección de trazos, llame al método [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) de la [colección InkStrokes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))

Cada [**objeto InkCollector,**](inkcollector-class.md) [**el objeto InkOverlay**](inkoverlay-class.md) y el control [InkPicture](inkpicture-control-reference.md) pueden especificar un conjunto diferente de atributos de dibujo para el mismo cursor. Use la [**propiedad DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) del [**objeto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) para obtener o establecer los atributos de dibujo de un cursor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Msgniut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedad DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)
</dt> <dt>

**Propiedad DrawingAttributes**
</dt> <dt>

**Propiedad DrawingAttributes**
</dt> <dt>

[**Propiedad DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)
</dt> <dt>

**Propiedad DefaultDrawingAttributes**
</dt> <dt>

**Propiedad DefaultDrawingAttributes**
</dt> <dt>

[**ModifyDrawingAttributes (método)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**InkDisp (clase)**](inkdisp-class.md)
</dt> <dt>

[**IInkStrokeDisp (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

