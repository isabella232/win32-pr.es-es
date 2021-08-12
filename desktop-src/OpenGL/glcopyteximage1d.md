---
title: Función glCopyTexImage1D (Gl.h)
description: La función glCopyTexImage1D copia píxeles del búfer de fotogramas en una imagen de textura unidimensional.
ms.assetid: 3b4d12d5-5efe-40d2-ac5f-95ea5ef243dd
keywords:
- Función GlCopyTexImage1D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e3dd966aa08eb5c74fa15235ed51f07a671c4e6f1378a990c6686fdc801e1d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617353"
---
# <a name="glcopyteximage1d-function"></a>Función glCopyTexImage1D

La **función glCopyTexImage1D** copia píxeles del búfer de fotogramas en una imagen de textura unidimensional.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glCopyTexImage1D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLint   border
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Destino para el que se cambiarán los datos de la imagen. Debe tener el valor GL \_ TEXTURE \_ 1D.

</dd> <dt>

*level* 
</dt> <dd>

Número de nivel de detalle. El nivel 0 es la imagen base. El *nivel n* es la imagen *de* reducción de mipmap n.

</dd> <dt>

*internalFormat* 
</dt> <dd>

Formato interno y resolución de los datos de textura. Este parámetro debe ser uno de los siguientes valores simbólicos.



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

Coordenada del plano x de la ventana de la esquina inferior izquierda de la fila de píxeles que se va a copiar.

</dd> <dt>

*y* 
</dt> <dd>

Coordenada del plano Y de la ventana de la esquina inferior izquierda de la fila de píxeles que se va a copiar.

</dd> <dt>

*width* 
</dt> <dd>

Ancho de la imagen de textura. Debe ser cero o 2n + 2(*borde*) para algún entero *n*. El alto de la imagen de textura es 1.

</dd> <dt>

*Frontera* 
</dt> <dd>

Ancho del borde. Debe ser cero o 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *target* no era un valor aceptado.<br/>                                                                                                           |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *level* era menor que cero o mayor que log2 *max,* donde *max* es el valor devuelto de GL \_ MAX TEXTURE \_ \_ SIZE.<br/>                           |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *border* no era cero o 1.<br/>                                                                                                                   |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *width* era menor que cero, mayor que 2 + GL MAX TEXTURE SIZE, o el ancho no se puede representar como \_ \_ \_ 2n +(*borde*)  para algún entero n .<br/> |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/>                    |



## <a name="remarks"></a>Observaciones

La **función glCopyTexImage1D** define una imagen de textura unidimensional mediante píxeles del búfer de fotogramas actual, en lugar de desde la memoria principal, como es el caso de [**glTexImage1D.**](glteximage1d.md)

Con el nivel de mapa mip especificado con el nivel *,* las matrices de textura se definen como una fila de píxeles alineada con la esquina inferior izquierda de la ventana en las coordenadas especificadas por *x* e *y*, con una longitud igual al ancho *+* 2 borde \* . El formato interno de la matriz de texturas se especifica con el *parámetro internalFormat.*

La función **glCopyTexImage1D** procesa los píxeles de una fila de la misma manera que [**glCopyPixels**](glcopypixels.md), salvo que antes de la conversión final de los píxeles, todos los valores de los componentes de píxeles se fijan al intervalo 0,1 y se convierten al formato interno de la textura para el almacenamiento en la matriz de \[ \] textura. La ordenación de píxeles se determina con coordenadas *x inferiores* correspondientes a coordenadas de textura inferiores. Si alguno de los píxeles de una fila especificada del búfer de fotogramas actual está fuera de la ventana asociada al contexto de representación actual, sus valores no están definidos.

No se pueden incluir llamadas **a glCopyTexImage1D** en listas para mostrar.

> [!Note]  
> La **función glCopyTexImage1D** solo está disponible en OpenGL versión 1.1 o posterior.

 

El texto no tiene ningún efecto en el modo de índice de color. Las [**funciones glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente de la manera en que afectan [**a glDrawPixels.**](gldrawpixels.md)

La función siguiente recupera información relacionada con **glCopyTexImage1D**:

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ TEXTURE \_ 1D

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
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

 

 





