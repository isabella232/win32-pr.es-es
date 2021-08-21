---
title: Función glBitmap (Gl.h)
description: La función glBitmap dibuja un mapa de bits.
ms.assetid: 3cd8e41b-016b-4610-833a-048b5e50ae7c
keywords:
- Función glBitmap OpenGL
topic_type:
- apiref
api_name:
- glBitmap
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8da90b8e592f8cd9d1702c7810990042b3929ef40e70814e8fb7d3326d902cb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082235"
---
# <a name="glbitmap-function"></a>Función glBitmap

La **función glBitmap** dibuja un mapa de bits.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glBitmap(
         GLSizei width,
         GLSizei height,
         GLfloat xorig,
         GLfloat yorig,
         GLfloat xmove,
         GLfloat ymove,
   const GLubyte *bitmap
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*width* 
</dt> <dd>

Ancho de píxel de la imagen de mapa de bits.

</dd> <dt>

*height* 
</dt> <dd>

Alto de píxeles de la imagen de mapa de bits.

</dd> <dt>

*xorig* 
</dt> <dd>

Ubicación *x* del origen en la imagen de mapa de bits. El origen se mide desde la esquina inferior izquierda del mapa de bits, siendo los ejes positivos las direcciones derecha e superior.

</dd> <dt>

*yorig* 
</dt> <dd>

Ubicación *y del* origen en la imagen de mapa de bits. El origen se mide desde la esquina inferior izquierda del mapa de bits, siendo los ejes positivos las direcciones derecha e superior.

</dd> <dt>

*xmove* 
</dt> <dd>

Desplazamiento *x* que se va a agregar a la posición de trama actual después de dibujar el mapa de bits.

</dd> <dt>

*ymove* 
</dt> <dd>

Desplazamiento *y* que se va a agregar a la posición de trama actual después de dibujar el mapa de bits.

</dd> <dt>

*bitmap* 
</dt> <dd>

Dirección de la imagen de mapa de bits.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *width* o *height es* negativo.<br/>                                                                                           |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

Un mapa de bits es una imagen binaria. Cuando se dibuja, el mapa de bits se coloca en relación con la posición de trama actual y los píxeles de búfer de fotogramas correspondientes a 1 en el mapa de bits se escriben con el color de trama o el índice actuales. No se modifican los píxeles del búfer de fotogramas correspondientes a ceros en el mapa de bits.

La imagen de mapa de bits se interpreta como datos  de  imagen para la función [**glDrawPixels,**](gldrawpixels.md) con ancho y alto correspondientes a los argumentos de ancho y alto de esa función, y con el tipo establecido en GL BITMAP y el formato establecido en GL COLOR  \_  \_ \_ INDEX. Los modos que especifique mediante [**glPixelStore afectan**](glpixelstore-functions.md) a la interpretación de los datos de imagen de mapa de bits; Los modos que especifique mediante [**glPixelTransfer**](glpixeltransfer.md) no lo hacen.

Si la posición de trama actual no es válida, **glBitmap** se omite. De lo contrario, la esquina inferior izquierda de la imagen de mapa de bits se coloca en las siguientes coordenadas de ventana:

*x*<sub>w</sub>  =  *x*<sub>r</sub> x *?*

*y*<sub>w</sub>  =  *y*<sub>r</sub> *y*?

En estas coordenadas, (*x*<sub>r</sub> , *y*<sub>r</sub> ) es la posición del trama y (*x*? , *y*? ) es el origen del mapa de bits. A continuación, se generan fragmentos para cada píxel correspondiente a un 1 en la imagen de mapa de bits. Estos fragmentos se generan mediante la coordenada z del trama *actual,* el índice de color o color y las coordenadas de textura de trama actuales. A continuación, se tratan como si hubieran sido generados por un punto, una línea o un polígono, incluida la asignación de texturas, la afición y todas las operaciones por fragmento, como las pruebas alfa y de profundidad.

Una vez dibujado el mapa de bits, las coordenadas *x* e *y* de la posición de trama actual se desplazan por *xmove* *y ymove*. No se realiza ningún cambio en la coordenada *z* de la posición de trama actual o en las coordenadas de color, índice o textura del trama actual.

Las funciones siguientes recuperan información relacionada con **la función glBitmap:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ CURRENT RASTER \_ \_ POSITION

 

**glGet con** el argumento GL \_ CURRENT RASTER \_ \_ COLOR

 

**glGet con** el argumento GL \_ CURRENT RASTER \_ \_ INDEX

 

**glGet con** el argumento GL \_ CURRENT RASTER TEXTURE \_ \_ \_ COORDS

 

**glGet con** el argumento GL \_ CURRENT RASTER POSITION \_ \_ \_ VALID

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glRasterPos**](glrasterpos-functions.md)
</dt> </dl>

 

 





