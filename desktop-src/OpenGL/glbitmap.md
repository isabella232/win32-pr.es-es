---
title: función glBitmap (GL. h)
description: La función glBitmap dibuja un mapa de bits.
ms.assetid: 3cd8e41b-016b-4610-833a-048b5e50ae7c
keywords:
- glBitmap (función) OpenGL
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
ms.openlocfilehash: 7aeb97bb16a1e3c4c29d1dfb1a5320c02f44404d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079478"
---
# <a name="glbitmap-function"></a>glBitmap función)

La función **glBitmap** dibuja un mapa de bits.

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

Ancho en píxeles de la imagen de mapa de bits.

</dd> <dt>

*height* 
</dt> <dd>

Alto en píxeles de la imagen de mapa de bits.

</dd> <dt>

*xorig* 
</dt> <dd>

Ubicación *x* del origen en la imagen de mapa de bits. El origen se mide desde la esquina inferior izquierda del mapa de bits, con las direcciones correctas y hacia arriba que son los ejes positivos.

</dd> <dt>

*yorig* 
</dt> <dd>

Ubicación *y* del origen en la imagen de mapa de bits. El origen se mide desde la esquina inferior izquierda del mapa de bits, con las direcciones correctas y hacia arriba que son los ejes positivos.

</dd> <dt>

*xmove* 
</dt> <dd>

Desplazamiento *x* que se va a agregar a la posición de la cuadrícula actual después de dibujar el mapa de bits.

</dd> <dt>

*ymove* 
</dt> <dd>

Desplazamiento *y* que se va a agregar a la posición de la cuadrícula actual después de dibujar el mapa de bits.

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
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *ancho* o el *alto* es negativo.<br/>                                                                                           |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Un mapa de bits es una imagen binaria. Cuando se dibuja, el mapa de bits se coloca en relación con la posición de la trama actual y los píxeles de fotogramas correspondientes a 1s en el mapa de bits se escriben utilizando el color o el índice de la trama actual. Los píxeles de búfer de fotogramas correspondientes a ceros en el mapa de bits no se modifican.

La imagen de mapa de bits se interpreta como los datos de imagen de la función [**glDrawPixels**](gldrawpixels.md) , con el *ancho* y el *alto* que se corresponden con los argumentos de ancho y alto de esa función, y con el *tipo* establecido en el mapa de bits de contabilidad \_ y el *formato* establecido en Índice de \_ color GL \_ . Los modos que se especifican mediante [**glPixelStore**](glpixelstore-functions.md) afectan a la interpretación de los datos de imagen de mapa de bits. los modos que se especifican con [**glPixelTransfer**](glpixeltransfer.md) no lo hacen.

Si la posición de la trama actual no es válida, se omite **glBitmap** . De lo contrario, la esquina inferior izquierda de la imagen de mapa de bits se coloca en las siguientes coordenadas de la ventana:

*x*<sub>w</sub>  =  *x*<sub>r</sub> *x*

*y*<sub>w</sub>  =  *y*<sub>r</sub> *y*?

En estas coordenadas, (*x*<sub>r</sub> , *y*<sub>r</sub> ) es la posición de la trama y (*x*? , *y*? ) es el origen del mapa de bits. A continuación, se generan fragmentos para cada píxel correspondiente a un 1 en la imagen de mapa de bits. Estos fragmentos se generan utilizando la coordenada *z* de rasterización actual, el color o el índice de color y las coordenadas de textura de rasterizado actuales. A continuación, se tratan como si hubieran sido generados por un punto, línea o polígono, incluida la asignación de texturas, la luneta térmica y todas las operaciones por fragmento, como las pruebas alfa y de profundidad.

Una vez dibujado el mapa de bits, *xmove* y *ymove* desplazan las coordenadas *x* *e y* de la posición de la trama actual. No se realiza ningún cambio en la coordenada *z* de la posición de la trama actual ni en las coordenadas de color, índice o textura de la trama actual.

Las siguientes funciones recuperan información relacionada con la función **glBitmap** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ posición de RASTERIZAción actual de GL \_

 

**glGet** con el argumento \_ \_ color de RASTERIZAdo actual de GL \_

 

**glGet** con el argumento \_ \_ Índice de trama actual de GL \_

 

**glGet** con argumento de \_ \_ textura de RASTERIZAdo actual \_ de GL \_

 

**glGet** con argumento de \_ posición de rasterizado actual de GL \_ \_ \_ válido

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
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

 

 





