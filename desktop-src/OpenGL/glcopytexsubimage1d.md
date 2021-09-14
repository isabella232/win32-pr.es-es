---
title: Función glCopyTexSubImage1D (Gl.h)
description: La función glCopyTexSubImage1D copia una subimagen de una imagen de textura unidimensional del búfer de fotogramas.
ms.assetid: 718aee8a-6dce-49e1-a441-19beccd89f8d
keywords:
- Función GlCopyTexSubImage1D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64006f9cec7e5fd2f3ca6f860249e579b16dbf10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362088"
---
# <a name="glcopytexsubimage1d-function"></a>Función glCopyTexSubImage1D

La **función glCopyTexSubImage1D** copia una subimagen de una imagen de textura unidimensional del búfer de fotogramas.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glCopyTexSubImage1D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   x,
   GLint   y,
   GLsizei width
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Destino al que se cambiarán los datos de la imagen. Debe tener el valor GL \_ TEXTURE \_ 1D.

</dd> <dt>

*level* 
</dt> <dd>

Número de nivel de detalle. El nivel 0 es la imagen base. El *nivel n* es la *enésima* imagen de reducción de mapa mip.

</dd> <dt>

*xoffset* 
</dt> <dd>

Desplazamiento de textura dentro de la matriz de textura.

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

Ancho de la sub image de la imagen de textura. Especificar una sub image de textura con ancho cero no tiene ningún efecto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *target* no era un valor aceptado.<br/>                                                                                                                                                                               |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *level* era menor que cero o *el nivel* es mayor que *el registro* 2(*max*), donde *max* es el valor devuelto de GL MAX \_ TEXTURE \_ \_ SIZE.<br/>                                                                                 |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *xoffset* era menor que *border* o (*xoffset*  +  *width*)was greater than (*w*  +  *border*), donde *w* es GL TEXTURE WIDTH y \_ border es GL TEXTURE \_  \_ \_ BORDER. Tenga en cuenta *que w* incluye dos veces el *ancho del* borde.<br/> |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *width* era menor que *border o* *y* era menor que *border*, donde *border* es el ancho del borde de la matriz de textura.<br/>                                                                                            |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | La matriz de texturas no se definió mediante una operación [**glTexImage1D**](glteximage1d.md) anterior.<br/>                                                                                                                   |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/>                                                                                        |



## <a name="remarks"></a>Observaciones

La **función glCopyTexSubImage1D** reemplaza una parte de una imagen de textura unidimensional mediante píxeles del búfer de fotogramas actual, en lugar de desde la memoria principal, como es el caso de [**glTexSubImage1D.**](gltexsubimage1d.md)

Una fila de píxeles que comienza con las coordenadas  de ventana especificadas por *x* e *y* y por el ancho de longitud reemplaza la parte de la matriz de textura por los índices *xoffset* a *xoffset* + (*width* - 1). El destino de la matriz de texturas no puede incluir ningún elemento de textura fuera de la matriz de texturas especificada originalmente.

La función **glCopyTexSubImage1D** procesa los píxeles de una fila de la misma manera que [**glCopyPixels,**](glcopypixels.md) salvo que antes de la conversión final de los píxeles, todos los valores de los componentes de píxeles se fijan al intervalo 0,1 y se convierten al formato interno de la textura para el almacenamiento en la matriz de \[ \] texturas. La ordenación de píxeles se determina con las *coordenadas x inferiores* correspondientes a las coordenadas de textura inferiores. Si alguno de los píxeles de una fila especificada del búfer de fotogramas actual está fuera de la ventana asociada al contexto de representación actual, sus valores no están definidos.

No se realiza ningún cambio en el *parámetro internalFormat*, *width* o *border* de la matriz de texturas especificada o en valores de textura fuera de la sub image de textura especificada.

No se pueden incluir llamadas **a glCopyTexSubImage1D** en listas para mostrar.

> [!Note]  
> La **función glCopyTexSubImage1D** solo está disponible en OpenGL versión 1.1 o posterior.

 

El texturing no tiene ningún efecto en el modo de índice de color. Las [**funciones glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente de la manera en que se dibujan los píxeles mediante [**glDrawPixels**](gldrawpixels.md).

Las siguientes funciones recuperan información relacionada **con glCopyTexSubImage1D**:

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ TEXTURE \_ 1D

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

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
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

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





