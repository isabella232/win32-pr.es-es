---
title: función glGetTexImage (GL. h)
description: La función glGetTexImage devuelve una imagen de textura.
ms.assetid: d7235df4-2dd8-4537-aadd-284c130a3f99
keywords:
- glGetTexImage (función) OpenGL
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
ms.openlocfilehash: da38ca1d6605fdc3cd6cf73cdd017404b71961e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666071"
---
# <a name="glgetteximage-function"></a>glGetTexImage función)

La función **glGetTexImage** devuelve una imagen de textura.

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

Especifica la textura que se va a obtener. Se aceptan las texturas GL \_ \_ 1D y GL Texture \_ \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

El número de nivel de detalle de la imagen deseada. El nivel 0 es el nivel de la imagen base. *El nivel* *n* es la imagen de reducción del MIP.

</dd> <dt>

*format* 
</dt> <dd>

Formato de píxel para los datos devueltos. Los formatos admitidos son GL \_ rojo, GL \_ verde, GL \_ Blue, GL \_ alfa, GL \_ RGB, GL \_ RGBA, GL \_ luminancia, GL \_ BGR \_ ext, GL \_ BGRA \_ EXT y luminancia de GL \_ \_ .

</dd> <dt>

*type* 
</dt> <dd>

Un tipo de píxel para los datos devueltos. Los tipos admitidos son el \_ byte sin signo de GL \_ , GL \_ byte, GL \_ sin signo \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int y GL \_ float.

</dd> <dt>

*píxeles* 
</dt> <dd>

Devuelve la imagen de la textura. Debe ser un puntero a una matriz del tipo especificado por el *tipo*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | *destino*, *formato* o *tipo* no era un valor aceptado.<br/>                                                                    |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *nivel* es menor que cero o mayor que el *registro* 2 (*Max*), donde *Max* es el valor devuelto del \_ tamaño de textura Max GL \_ \_ .<br/>      |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md) .<br/> |



## <a name="remarks"></a>Observaciones

La función **glGetTexImage** devuelve una imagen de textura en *píxeles*. El parámetro de *destino* especifica si la imagen de textura deseada es una especificada por [**glTexImage1D**](glteximage1d.md)**(** GL \_ Texture \_ 1D **)** o por [**glTexImage2D**](glteximage2d.md)**(** GL \_ Texture \_ 2D **)**. El parámetro *LEVEL* especifica el número de nivel de detalle de la imagen deseada. Los parámetros de *tipo* y *formato* especifican el formato y el tipo de la matriz de imágenes deseada. Para obtener una descripción de los valores aceptables para los parámetros de *formato* y *tipo* , respectivamente, vea **glTexImage1D** y [**glDrawPixels**](gldrawpixels.md).

La operación de **glGetTexImage** se entiende mejor teniendo en cuenta que la imagen de textura interna de cuatro componentes seleccionada es un búfer de color RGBA el tamaño de la imagen. La semántica de **glGetTexImage** es idéntica a la de [**glReadPixels**](glreadpixels.md) a la que se llama con el mismo *formato* y *tipo*. con *x* e y establecido en cero, el *ancho* *se establece en* el ancho de la imagen de textura (incluido el borde si se especificó) y el *alto* se establece en uno para las imágenes 1D, o en el alto de la imagen de textura (incluido el borde, si se ha especificado) para las imágenes 2D.

Dado que la imagen de textura interna es una imagen RGBA, no se aceptan los formatos de píxel \_ \_ Índice de color de contabilidad, índice de estarcido de GL \_ \_ y componente de profundidad de libro de contabilidad \_ \_ , y no se acepta el mapa de bits de contabilidad de tipo píxel \_ .

Si la imagen de textura seleccionada no contiene cuatro componentes, se aplican las siguientes asignaciones. Las texturas de un solo componente se tratan como búferes RGBA con el rojo establecido en el valor de un solo componente, y el verde, el azul y el alfa se establecen en cero.

Las texturas de dos componentes se tratan como búferes RGBA, con el rojo establecido en el valor de componente cero, alfa establecido en el valor del componente uno, y en verde y azul establecido en cero. Por último, las texturas de tres componentes se tratan como búferes RGBA con el valor rojo establecido en componente cero, verde establecido en componente uno, azul establecido en componente dos y alfa establecido en cero.

Para determinar el tamaño necesario de los *píxeles*, use [**glGetTexLevelParameter**](glgettexlevelparameter.md) para determinar las dimensiones de la imagen de textura interna y, a continuación, escale el número necesario de píxeles según el almacenamiento necesario para cada píxel, en función del *formato* y el *tipo*. Asegúrese de tener en cuenta los parámetros de almacenamiento de píxeles, especialmente la \_ alineación del paquete GL \_ .

Si se genera un error, no se realiza ningún cambio en el contenido de los *píxeles*.

Las siguientes funciones recuperan información relacionada con **glGetTexImage**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ alineación del paquete GL \_ y otros

[**glGetTexLevelParameter**](glgettexlevelparameter.md) con el argumento \_ ancho de textura de GL \_

**glGetTexLevelParameter** con el argumento \_ alto de textura de GL \_

**glGetTexLevelParameter** con el argumento \_ borde de textura GL \_

**glGetTexLevelParameter** con \_ los componentes de textura GL de argument \_

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

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





