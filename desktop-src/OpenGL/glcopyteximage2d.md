---
title: Función glCopyTexImage2D (Gl.h)
description: La función glCopyTexImage2D copia píxeles del búfer de fotogramas en una imagen de textura bidimensional.
ms.assetid: 4b9d7be6-054d-4590-b3f0-a2a670786c4b
keywords:
- Función GlCopyTexImage2D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d04a979e9bb026da904687506f3201d12c12c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362091"
---
# <a name="glcopyteximage2d-function"></a>Función glCopyTexImage2D

La **función glCopyTexImage2D** copia píxeles del búfer de fotogramas en una imagen de textura bidimensional.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glCopyTexImage2D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLint   border
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Destino al que se cambiarán los datos de la imagen. Debe tener el valor GL \_ TEXTURE \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

Número de nivel de detalle. El nivel 0 es la imagen base. El *nivel n* es la imagen *de* reducción de mipmap n.

</dd> <dt>

*internalFormat* 
</dt> <dd>

Formato interno y resolución de los datos de textura. Los valores 1, 2, 3 y 4 no se aceptan para *internalFormat*. El parámetro puede asumir uno de los siguientes valores simbólicos.



| Constante                 | R Bits | G Bits | B Bits | A Bits | L Bits | I Bits |
|--------------------------|--------|--------|--------|--------|--------|--------|
| GL \_ ALPHA                |        |        |        |        |        |        |
| GL \_ ALPHA4               |        |        |        | 4      |        |        |
| GL \_ ALPHA8               |        |        |        | 8      |        |        |
| GL \_ ALPHA12              |        |        |        | 12     |        |        |
| GL \_ ALPHA16              |        |        |        | 16     |        |        |
| GL \_ LUMINANCE            |        |        |        |        |        |        |
| GL \_ LUMINANCE4           |        |        |        |        | 4      |        |
| GL \_ LUMINANCE8           |        |        |        |        | 8      |        |
| GL \_ LUMINANCE12          |        |        |        |        | 12     |        |
| GL \_ LUMINANCE16          |        |        |        |        | 16     |        |
| GL \_ LUMINANCE \_ ALPHA     |        |        |        |        |        |        |
| GL \_ LUMINANCE4 \_ ALPHA4   |        |        |        | 4      | 4      |        |
| GL \_ LUMINANCE6 \_ ALPHA2   |        |        |        | 2      | 6      |        |
| GL \_ LUMINANCE8 \_ ALPHA8   |        |        |        | 8      | 8      |        |
| GL \_ LUMINANCE12 \_ ALPHA4  |        |        |        | 4      | 12     |        |
| GL \_ LUMINANCE12 \_ ALPHA12 |        |        |        | 12     | 12     |        |
| GL \_ LUMINANCE16 \_ ALPHA16 |        |        |        | 16     | 16     |        |
| GL \_ INTENSITY            |        |        |        |        |        |        |
| GL \_ INTENSITY4           |        |        |        |        |        | 4      |
| GL \_ INTENSITY8           |        |        |        |        |        | 8      |
| GL \_ INTENSITY12          |        |        |        |        |        | 12     |
| GL \_ INTENSITY16          |        |        |        |        |        | 16     |
| GL \_ RGB                  |        |        |        |        |        |        |
| GL \_ R3 \_ G3 \_ B2           | 3      | 3      | 2      |        |        |        |
| GL \_ RGB4                 | 4      | 4      | 4      |        |        |        |
| GL \_ RGB5                 | 5      | 5      | 5      |        |        |        |
| GL \_ RGB8                 | 8      | 8      | 8      |        |        |        |
| GL \_ RGB10                | 10     | 10     | 10     |        |        |        |
| GL \_ RGB12                | 12     | 12     | 12     |        |        |        |
| GL \_ RGB16                | 16     | 16     | 16     |        |        |        |
| GL \_ RGBA                 |        |        |        |        |        |        |
| GL \_ RGBA2                | 2      | 2      | 2      | 2      |        |        |
| GL \_ RGBA4                | 4      | 4      | 4      | 4      |        |        |
| GL \_ RGB5 \_ A1             | 5      | 5      | 5      | 1      |        |        |
| GL \_ RGBA8                | 8      | 8      | 8      | 8      |        |        |
| GL \_ RGB10 \_ A2            | 10     | 10     | 10     | 2      |        |        |
| GL \_ RGBA12               | 12     | 12     | 12     | 12     |        |        |
| GL \_ RGBA16               | 16     | 16     | 16     | 16     |        |        |



 

</dd> <dt>

*x* 
</dt> <dd>

Coordenada del plano x de la ventana de la esquina inferior izquierda de la región rectangular de píxeles que se va a copiar.

</dd> <dt>

*y* 
</dt> <dd>

Coordenada del plano Y de la ventana de la esquina inferior izquierda de la región rectangular de píxeles que se va a copiar.

</dd> <dt>

*width* 
</dt> <dd>

Ancho de la imagen de textura. Debe ser 2n + 2 \* *borde para* algún entero *n*.

</dd> <dt>

*height* 
</dt> <dd>

Alto de la imagen de textura. Debe ser 2n + 2 \* *borde para* algún entero *n*.

</dd> <dt>

*Frontera* 
</dt> <dd>

Ancho del borde. Debe ser cero o 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *target* no era un valor aceptado.<br/>                                                                                                               |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *level* era menor que cero o mayor que log2 *max*, donde *max* es el valor devuelto de GL \_ MAX TEXTURE \_ \_ SIZE.<br/>                               |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *border* no era cero o 1.<br/>                                                                                                                       |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *width* era menor que cero, mayor que 2 + GL MAX TEXTURE SIZE, o el ancho no se puede representar como \_ \_ \_ 2n + 2  \* *borde* para algún entero *n*.<br/> |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/>                        |



## <a name="remarks"></a>Observaciones

La **función glCopyTexImage2D** define una imagen de textura bidimensional con píxeles del búfer de fotogramas actual, en lugar de desde la memoria principal, como es el caso de [**glTexImage2D.**](glteximage2d.md)

Con el nivel mipmap especificado con el nivel *,* las matrices de textura se definen como un rectángulo de píxeles con la esquina inferior izquierda ubicada en las coordenadas *x* e *y*, ancho igual al ancho *+* (2 borde) y un alto igual a \*  *alto* + (2 \* *borde*). El formato interno de la matriz de texturas se especifica con el *parámetro internalFormat.*

La función **glCopyTexImage2D** procesa los píxeles de una fila de la misma manera que [**glCopyPixels,**](glcopypixels.md) salvo que antes de la conversión final de los píxeles, todos los valores del componente de píxel se fijan al intervalo 0,1 y se convierten al formato interno de la textura para el almacenamiento en la matriz de \[ \] texturas. El orden de los píxeles se determina con las *coordenadas x* *e y inferiores* correspondientes a las coordenadas de textura *s* y *t* inferiores. Si alguno de los píxeles de una fila especificada del búfer de fotogramas actual está fuera de la ventana asociada al contexto de representación actual, sus valores no están definidos.

No se pueden incluir llamadas **a glCopyTexImage2D** en listas para mostrar.

> [!Note]  
> La **función glCopyTexImage2D** solo está disponible en OpenGL versión 1.1 o posterior.

 

El texturing no tiene ningún efecto en el modo de índice de color. Las [**funciones glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente de la manera en que afectan [**a glDrawPixels.**](gldrawpixels.md)

La función siguiente recupera información relacionada con **glCopyTexImage2D**:

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ TEXTURE \_ 2D

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCopyTexImage1D**](glcopyteximage1d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





