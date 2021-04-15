---
title: función glGetColorTableParameterivEXT (GL. h)
description: Las funciones glGetColorTableParameterfvEXT y glGetColorTableParameterivEXT obtienen parámetros de paleta de las tablas de color. | función glGetColorTableParameterivEXT (GL. h)
ms.assetid: 39a0b346-d103-4426-8536-95e7e1548f7a
keywords:
- glGetColorTableParameterivEXT (función) OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableParameterivEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 897dd11781968838bb8c26a716e3857acc119e9c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689819"
---
# <a name="glgetcolortableparameterivext-function"></a>glGetColorTableParameterivEXT función)

Las funciones [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) y **glGetColorTableParameterivEXT** obtienen parámetros de paleta de las tablas de color.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetColorTableParameterivEXT(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Textura de destino de la paleta para la que desea obtener datos de parámetros. Debe ser la textura \_ 1D, textura \_ 2D, \_ textura de proxy \_ 1D o \_ textura de proxy \_ 2D.

</dd> <dt>

*PName* 
</dt> <dd>

Constante simbólica para el tipo de los datos de parámetro de la paleta a los que apuntan los *parámetros.*

A continuación se indican las constantes simbólicas aceptadas y su significado.



| Value                                                                                                                                                                                                             | Significado                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <dt>**\_ \_ ext formato de tabla de color de \_ GL \_**</dt> </dl>              | Devuelve el formato interno especificado por la llamada más reciente a [**glColorTableEXT**](glcolortableext.md) o el valor predeterminado.<br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <dt>**\_ \_ ext ancho de tabla de color de \_ GL \_**</dt> </dl>                 | Devuelve el ancho de la paleta actual.<br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <dt>**\_tamaño rojo de la tabla de colores GL \_ \_ \_ \_ ext**</dt> </dl>       | Devuelve el tamaño real utilizado internamente para almacenar el componente rojo de los datos de la paleta.<br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <dt>**\_ \_ \_ tamaño verde de tabla \_ de \_ colores de contabilidad general**</dt> </dl> | Devuelve el tamaño real utilizado internamente para almacenar el componente verde de los datos de la paleta.<br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <dt>**tamaño azul de la tabla de colores de GL \_ \_ \_ \_ \_ ext**</dt> </dl>    | Devuelve el tamaño real utilizado internamente para almacenar el componente azul de los datos de la paleta.<br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <dt>**tabla de colores de contabilidad de \_ \_ \_ \_ tamaño alfa \_ ext**</dt> </dl> | Devuelve el tamaño real utilizado internamente para almacenar el componente alfa de los datos de la paleta.<br/>                                         |



 

</dd> <dt>

*params* 
</dt> <dd>

Apunta a los datos de parámetro de la tabla de colores especificados por el parámetro *PName* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las funciones **glGetColorTableParameterivEXT** y [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) se usan para recuperar datos de parámetros específicos de las tablas de color establecidas con [**glColorTableEXT**](glcolortableext.md) para las paletas de texturas de destino. También puede usar estas funciones para determinar el número de entradas de la tabla de colores que devuelve **glGetColorTableEXT** .

Cuando el parámetro de *destino* es \_ GL \_ proxy Texture \_ 1D o GL \_ proxy \_ Texture \_ 2D, y la implementación no admite los valores especificados para el *formato* o el *ancho*, **glColorTableEXT** puede generar un error al crear la tabla de colores solicitada. En este caso, la tabla de colores está vacía y todos los parámetros recuperados serán cero. Puede determinar si OpenGL admite un formato y un tamaño de tabla de colores determinados mediante una llamada a **glColorTableEXT** con un destino de proxy y, a continuación, llamar a **glGetColorTableParameterivEXT** o [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) para determinar si el parámetro de ancho coincide con el establecido por **glColorTableEXT**. Si el ancho recuperado es cero, se produce un error en la solicitud de tabla de colores por **glColorTable** . Si el ancho recuperado no es cero, puede llamar a **glColorTable** con el destino real con la textura \_ 1D o textura \_ 2D para establecer la tabla de colores.

Las funciones **glGetColorTableParameterivEXT** y [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) son funciones de extensión que no forman parte de la biblioteca estándar de OpenGL, pero que forman parte de la extensión de textura de paleta de GL \_ ext \_ \_ . Para comprobar si la implementación de OpenGL es compatible con **glGetColorTableParameterivEXT** y **glGetColorTableParameterfvEXT**, llame a [**glGetString**](glgetstring.md)**(** extensiones de GL \_ **)**. Si devuelve la \_ \_ textura de paleta ext \_ de GL, se admiten **glGetColorTableParameterivEXT** y **glGetColorTableParameterfvEXT** . Para obtener la dirección de la función de una función de extensión, llame a [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                            |
| Encabezado<br/>                   | <dl> <dt>GL. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glColorSubTableEXT**](glcolorsubtableext.md)
</dt> <dt>

[**glColorTableEXT**](glcolortableext.md)
</dt> <dt>

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





