---
title: Función glGetTexImage (Gl.h)
description: La función glGetTexImage devuelve una imagen de textura.
ms.assetid: d7235df4-2dd8-4537-aadd-284c130a3f99
keywords:
- Función glGetTexImage OpenGL
topic_type:
- apiref
api_name:
- glGetTexImage
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b116bc4ae517d0767d794767ad5232d8537033d62a099a3906f9f2ca96a7166c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493755"
---
# <a name="glgetteximage-function"></a>Función glGetTexImage

La **función glGetTexImage** devuelve una imagen de textura.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetTexImage(
   GLenum target,
   GLint  level,
   GLenum format,
   GLenum type,
   GLvoid *pixels
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Especifica qué textura se va a obtener. Se \_ aceptan GL TEXTURE \_ 1D y GL \_ TEXTURE \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

Número de nivel de detalle de la imagen deseada. El nivel 0 es el nivel de imagen base. El *nivel n* es la imagen *de* reducción de mipmap n.

</dd> <dt>

*format* 
</dt> <dd>

Formato de píxel para los datos devueltos. Los formatos admitidos son GL \_ RED, GL \_ GREEN, GL \_ BLUE, GL \_ ALPHA, GL \_ RGB, GL \_ RGBA, GL \_ LUMINANCE, GL \_ BGR \_ EXT, GL BGRA EXT y GL \_ \_ \_ LUMINANCE \_ ALPHA.

</dd> <dt>

*type* 
</dt> <dd>

Tipo de píxel para los datos devueltos. Los tipos admitidos son GL \_ \_ UNSIGNED BYTE, GL \_ BYTE, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT y GL \_ FLOAT.

</dd> <dt>

*píxeles* 
</dt> <dd>

Devuelve la imagen de textura. Debe ser un puntero a una matriz del tipo especificado por *el tipo*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *target,* *format* o *type* no era un valor aceptado.<br/>                                                                    |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *level* es menor que cero o mayor que *el registro* 2 *(max),* donde *max* es el valor devuelto de GL MAX \_ TEXTURE \_ \_ SIZE.<br/>      |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md) .<br/> |



## <a name="remarks"></a>Comentarios

La **función glGetTexImage** devuelve una imagen de textura en *píxeles.* El  parámetro de destino especifica si la imagen de textura deseada es una especificada por [**glTexImage1D**](glteximage1d.md)**(** GL \_ TEXTURE \_ 1D **)** o [**por glTexImage2D**](glteximage2d.md)**(** GL \_ TEXTURE \_ 2D **).** El *parámetro level* especifica el número de nivel de detalle de la imagen deseada. Los *parámetros de* formato *y* tipo especifican el formato y el tipo de la matriz de imágenes deseada. Para obtener una descripción de los  valores aceptables para los parámetros *de* formato y tipo, respectivamente, vea **glTexImage1D** y [**glDrawPixels**](gldrawpixels.md).

El funcionamiento **de glGetTexImage** se entiende mejor si se considera que la imagen de textura interna de cuatro componentes seleccionada es un búfer de color RGBA del tamaño de la imagen. La semántica de **glGetTexImage** es entonces idéntica a la de  [**glReadPixels**](glreadpixels.md) llamada con el mismo formato y tipo , con *x* e *y* establecido  en *cero,* ancho establecido en el ancho de la imagen de textura (incluido el borde si se especificó) y alto establecido en uno para imágenes 1D, o en el alto de la imagen de textura (incluido el borde, si se especificó uno) para imágenes 2D. 

Dado que la imagen de textura interna es una imagen RGBA, no se aceptan los formatos de píxel GL \_ COLOR \_ INDEX, GL \_ STENCIL INDEX y GL DEPTH COMPONENT, y no se acepta el tipo de píxel \_ GL \_ \_ \_ BITMAP.

Si la imagen de textura seleccionada no contiene cuatro componentes, se aplican las siguientes asignaciones. Las texturas de componente único se tratan como búferes RGBA con rojo establecido en el valor de componente único y verde, azul y alfa establecido en cero.

Las texturas de dos componentes se tratan como búferes RGBA, con rojo establecido en el valor del componente cero, alfa establecido en el valor del componente uno y verde y azul establecido en cero. Por último, las texturas de tres componentes se tratan como búferes RGBA con rojo establecido en el componente cero, verde establecido en componente uno, azul establecido en el componente dos y alfa establecido en cero.

Para determinar el tamaño necesario de píxeles, use [**glGetTexLevelParameter**](glgettexlevelparameter.md) para determinar las dimensiones de la imagen de textura interna  y, a continuación, escale el número necesario de píxeles por el almacenamiento necesario para cada píxel, según el formato y el tipo *.*  Asegúrese de tener en cuenta los parámetros de almacenamiento de píxeles, especialmente GL \_ PACK \_ ALIGNMENT.

Si se genera un error, no se realiza ningún cambio en el contenido de *píxeles*.

Las siguientes funciones recuperan información relacionada **con glGetTexImage**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ PACK ALIGNMENT y \_ otros

[**glGetTexLevelParameter con**](glgettexlevelparameter.md) el argumento GL \_ TEXTURE \_ WIDTH

**glGetTexLevelParameter con** el argumento GL \_ TEXTURE \_ HEIGHT

**glGetTexLevelParameter con** el argumento GL \_ TEXTURE \_ BORDER

**glGetTexLevelParameter con** el argumento GL \_ TEXTURE \_ COMPONENTS

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

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





