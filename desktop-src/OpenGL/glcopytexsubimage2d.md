---
title: Función glCopyTexSubImage2D (Gl.h)
description: La función glCopyTexSubImage2D copia una subimagen de una imagen de textura bidimensional del búfer de fotogramas.
ms.assetid: cbb644d4-6a23-4d66-8599-5f8b48e9b91f
keywords:
- Función GlCopyTexSubImage2D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c966d031bb154b59cc54ae2e5d254347aa88d2a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362086"
---
# <a name="glcopytexsubimage2d-function"></a>Función glCopyTexSubImage2D

La **función glCopyTexSubImage2D** copia una subimagen de una imagen de textura bidimensional del búfer de fotogramas.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glCopyTexSubImage2D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   yoffset,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
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

Número de nivel de detalle. El nivel 0 es la imagen base. El *nivel n* es la *enésima* imagen de reducción de mapa mip.

</dd> <dt>

*xoffset* 
</dt> <dd>

Desplazamiento de texel en la *dirección x* dentro de la matriz de textura.

</dd> <dt>

*yoffset* 
</dt> <dd>

Desplazamiento de textura en la dirección *y* dentro de la matriz de textura.

</dd> <dt>

*x* 
</dt> <dd>

Coordenadas del plano x de la ventana de la esquina inferior izquierda de la fila de píxeles que se va a copiar.

</dd> <dt>

*y* 
</dt> <dd>

Coordenadas del plano Y de la ventana de la esquina inferior izquierda de la fila de píxeles que se va a copiar.

</dd> <dt>

*width* 
</dt> <dd>

Ancho de la sub image de la imagen de textura. Especificar una sub image de textura con ancho cero no tiene ningún efecto.

</dd> <dt>

*height* 
</dt> <dd>

Alto de la sub image de la imagen de textura. Especificar una sub image de textura con ancho cero no tiene ningún efecto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *target* no era un valor aceptado.<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *level* era menor que cero o mayor que *el registro* 2 *(max),* donde *max* es el valor devuelto de GL MAX \_ TEXTURE \_ \_ SIZE.<br/>                                                                                                                                                                                          |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *xoffset* era menor que *border* o (*xoffset*  +  *width*)was greater than (*w*  +  *border*), *yoffset* was less than *border*, o (*yoffset*  +  *height*) was greater than (*h*  +  *border*), where *w* is GL TEXTURE WIDTH \_ and \_ *border* is GL \_ TEXTURE \_ BORDER. Tenga en cuenta *que w* incluye dos veces el *ancho del* borde.<br/> |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *width* era menor que *border o* *y* era menor que *border*, donde *border* es el ancho del borde de la matriz de textura.<br/>                                                                                                                                                                                           |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | La matriz de texturas no se definió mediante una operación [**glTexImage1D**](glteximage1d.md) anterior.<br/>                                                                                                                                                                                                                  |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/>                                                                                                                                                                                       |



## <a name="remarks"></a>Observaciones

La **función glCopyTexSubImage2D** reemplaza una parte rectangular de una imagen de textura bidimensional por píxeles del búfer de fotogramas actual, en lugar de desde la memoria principal, como es el caso de [**glTexSubImage2D.**](gltexsubimage2d.md)

Un rectángulo de píxeles que comienza con las  coordenadas  de ventana *x* e *y* y con el ancho y alto de las dimensiones reemplaza la parte de la matriz de textura por los índices *xoffset* a *xoffset* + (*width* - 1), por los índices *yoffset* a *yoffset* + (*width* - 1) en el nivel mipmap especificado por *level*. El rectángulo de destino de la matriz de texturas no puede incluir ningún elemento de textura fuera de la matriz de texturas especificada originalmente.

La función **glCopyTexSubImage2D** procesa los píxeles de una fila de la misma manera que [**glCopyPixels,**](glcopypixels.md)salvo que antes de la conversión final de los píxeles, todos los valores de los componentes de píxeles se fijan al intervalo 0,1 y se convierten al formato interno de la textura para el almacenamiento en la matriz de \[ \] texturas. La ordenación de píxeles se determina con las *coordenadas x inferiores* correspondientes a las coordenadas de textura inferiores. Si alguno de los píxeles de una fila especificada del búfer de fotogramas actual está fuera de la ventana asociada al contexto de representación actual, sus valores no están definidos.

Si alguno de los píxeles del rectángulo especificado del búfer de fotogramas actual está fuera de la ventana de lectura asociada al contexto de representación actual, los valores obtenidos para esos píxeles no están definidos. No se realiza ningún cambio en el parámetro *internalFormat*, *width,* *height* o *border* de la matriz de textura especificada o en los valores de textura fuera de la sub image de textura especificada.

No se pueden incluir llamadas **a glCopyTexSubImage2D** en listas para mostrar.

> [!Note]  
> La **función glCopyTexSubImage2D** solo está disponible en OpenGL versión 1.1 o posterior.

 

El texturing no tiene ningún efecto en el modo de índice de color. Las [**funciones glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente de la manera en que se dibujan los píxeles mediante [**glDrawPixels**](gldrawpixels.md).

Las siguientes funciones recuperan información relacionada **con glCopyTexSubImage2D**:

[**glGetTexImage**](glgetteximage.md)

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexSubImage1D**](glcopytexsubimage1d.md)
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

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





