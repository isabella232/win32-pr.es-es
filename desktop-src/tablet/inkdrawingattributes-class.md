---
description: Representa los atributos que se aplican a la entrada manuscrita cuando se dibuja.
ms.assetid: 10ca7ae5-28dd-42a2-98d9-852d4de5869d
title: Clase InkDrawingAttributes (Msinkaut. h)
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
ms.openlocfilehash: 64a45c33e7aa17b381875ac8e8e8d054af2bf086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361180"
---
# <a name="inkdrawingattributes-class"></a>Clase InkDrawingAttributes

Representa los atributos que se aplican a la entrada manuscrita cuando se dibuja.

**InkDrawingAttributes** tiene estos tipos de miembros:

-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="interfaces"></a>Interfaces

La clase **InkDrawingAttributes** define estas interfaces.



| Interfaz                 | Descripción                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **IInkDrawingAttributes** | Este objeto implementa la interfaz com **IInkDrawingAttributes** .<br/> |



 

### <a name="methods"></a>Métodos

La clase **InkDrawingAttributes** tiene estos métodos.



| Método                         | Descripción                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clonar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone) | Crea un objeto [**InkDisp**](inkdisp-class.md), **InkDrawingAttributes** o [**InkRecognizerContext**](inkrecognizercontext-class.md) duplicado.<br/> |



 

### <a name="properties"></a>Propiedades

La clase **InkDrawingAttributes** tiene estas propiedades.



| Propiedad                                                                           | Tipo de acceso           | Descripción                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Sin suavizado**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_antialiased)<br/>                 | Lectura/escritura<br/> | Obtiene o establece el valor que especifica si se mezclan los colores de primer plano y de fondo a lo largo del borde de la tinta para aumentar la suavidad de un trazo de tinta.<br/> |
| [**Color**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color)<br/>                             | Lectura/escritura<br/> | Obtiene o establece el color de la tinta dibujada con este objeto **InkDrawingAttributes** .<br/>                                                                                    |
| [**ExtendedProperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | Solo lectura<br/>  | Obtiene la colección de datos definidos por la aplicación que se almacena en el objeto **InkDrawingAttributes** .<br/>                                                                |
| [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve)<br/>                   | Lectura/escritura<br/> | Obtiene o establece el valor que especifica si la entrada de lápiz se representa como una serie de curvas en lugar de como líneas entre los puntos de ejemplo de lápiz.<br/>                                    |
| [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)<br/>                           | Lectura/escritura<br/> | Obtiene o establece el alto del lápiz al dibujar la entrada manuscrita con este objeto **InkDrawingAttributes** .<br/>                                                                        |
| [**IgnorePressure**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_ignorepressure)<br/>           | Lectura/escritura<br/> | Obtiene o establece el valor que especifica si la tinta dibujada se vuelve más ancha y aumenta la presión de la punta del lápiz en la superficie de la tableta.<br/>                     |
| [**PenTip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip)<br/>                           | Lectura/escritura<br/> | Obtiene o establece la punta del lápiz que se va a usar (bola o rectángulo) al dibujar la entrada manuscrita con este objeto **InkDrawingAttributes** .<br/>                                                       |
| [**RasterOperation**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation)<br/>         | Lectura/escritura<br/> | Obtiene o establece cómo interactúa el color de la pluma con los colores de fondo existentes en la pantalla cuando se dibuja la tinta.<br/>                                                    |
| [**Transparencia**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_transparency)<br/>               | Lectura/escritura<br/> | Obtiene o establece el valor de transparencia de la entrada de lápiz dibujada. Los valores van desde cero (totalmente opaco) hasta 255 (totalmente transparente).<br/>                                               |
| [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)<br/>                             | Lectura/escritura<br/> | Obtiene o establece el ancho del lápiz al dibujar la entrada manuscrita con este objeto **InkDrawingAttributes** .<br/>                                                                         |



 

## <a name="remarks"></a>Observaciones

Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

Estos atributos de dibujo se pueden asociar a un trazo o un cursor y especificar opciones de configuración como el color, el ancho y la transparencia.

Para especificar los atributos de dibujo de un trazo, use la propiedad [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) del objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) . Para especificar los atributos de dibujo de todos los trazos dentro de una colección de trazos, llame al método [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) de la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

Cada objeto [**InkCollector**](inkcollector-class.md) , el objeto [**InkOverlay**](inkoverlay-class.md) y el control [InkPicture](inkpicture-control-reference.md) pueden especificar un conjunto diferente de atributos de dibujo para el mismo cursor. Use la propiedad [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) del objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) para obtener o establecer los atributos de dibujo de un cursor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DrawingAttributes (propiedad)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)
</dt> <dt>

**DrawingAttributes (propiedad)**
</dt> <dt>

**DrawingAttributes (propiedad)**
</dt> <dt>

[**Propiedad DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)
</dt> <dt>

**Propiedad DefaultDrawingAttributes**
</dt> <dt>

**Propiedad DefaultDrawingAttributes**
</dt> <dt>

[**Método ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes)
</dt> <dt>

[**Interfaz IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Clase InkDisp**](inkdisp-class.md)
</dt> <dt>

[**Interfaz IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

