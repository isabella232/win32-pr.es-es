---
title: función glCopyTexSubImage2D (GL. h)
description: La función glCopyTexSubImage2D copia una subimagen de una imagen de textura bidimensional a partir de fotogramas.
ms.assetid: cbb644d4-6a23-4d66-8599-5f8b48e9b91f
keywords:
- glCopyTexSubImage2D (función) OpenGL
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422393"
---
# <a name="glcopytexsubimage2d-function"></a>glCopyTexSubImage2D función)

La función **glCopyTexSubImage2D** copia una subimagen de una imagen de textura bidimensional a partir de fotogramas.

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

Destino al que se cambiarán los datos de la imagen. Debe tener el valor de la textura de contabilidad \_ \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

El número de nivel de detalle. El nivel 0 es la imagen base. *El nivel* *n* es la imagen de reducción del MIP.

</dd> <dt>

*xoffset* 
</dt> <dd>

Desplazamiento textura en la dirección *x* dentro de la matriz de textura.

</dd> <dt>

*yoffset* 
</dt> <dd>

El desplazamiento textura en la dirección *y* dentro de la matriz de textura.

</dd> <dt>

*x* 
</dt> <dd>

Coordenadas de plano x de la ventana de la esquina inferior izquierda de la fila de píxeles que se va a copiar.

</dd> <dt>

*y* 
</dt> <dd>

Coordenadas y del plano de la ventana de la esquina inferior izquierda de la fila de píxeles que se va a copiar.

</dd> <dt>

*width* 
</dt> <dd>

Ancho de la subimagen de la imagen de textura. Especificar una subimagen de textura con un ancho de cero no tiene ningún efecto.

</dd> <dt>

*height* 
</dt> <dd>

Alto de la imagen secundaria de la imagen de textura. Especificar una subimagen de textura con un ancho de cero no tiene ningún efecto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *destino* no era un valor aceptado.<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *nivel* era menor que cero o mayor que el *registro* 2 (*Max*), donde *Max* es el valor devuelto del \_ tamaño de textura Max GL \_ \_ .<br/>                                                                                                                                                                                          |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *xoffset* era menor que *Border* o (*el*  +  *ancho* de xoffset) era mayor que (*w*  +  *Border*), *YOFFSET* era menor que *Border*, o (el alto de *YOFFSET*  +  ) era mayor que (  +  *borde* h), donde *w* es el \_ \_ ancho y el *borde* de la textura de contabilidad \_ \_ . Tenga en cuenta que *w* incluye dos veces el ancho del *borde* .<br/> |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *ancho* era menor *que Border* o *y* era menor que *Border*, donde *Border* es el ancho del borde de la matriz de textura.<br/>                                                                                                                                                                                           |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Una operación [**glTexImage1D**](glteximage1d.md) anterior no definió la matriz de textura.<br/>                                                                                                                                                                                                                  |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/>                                                                                                                                                                                       |



## <a name="remarks"></a>Observaciones

La función **glCopyTexSubImage2D** reemplaza una parte rectangular de una imagen de textura bidimensional con píxeles de la fotogramas actual, en lugar de la memoria principal, como es el caso de [**glTexSubImage2D**](gltexsubimage2d.md).

Un rectángulo de píxeles que comienza con las coordenadas de la ventana *x* *e y,* y con el *ancho* y el *alto* de las dimensiones reemplaza la parte de la matriz de textura con los índices *xoffset* a *xoffset* + (*width* -1), con los índices *YOFFSET* a *YOFFSET* + (*width* -1) en el nivel de mipmap especificado por *LEVEL*. El rectángulo de destino de la matriz de textura no puede incluir ningún textura fuera de la matriz de textura especificada originalmente.

La función **glCopyTexSubImage2D** procesa los píxeles de una fila de la misma manera que [**glCopyPixels**](glcopypixels.md), salvo que antes de la conversión final de los píxeles, todos los valores de los componentes de píxeles se fijan en el intervalo \[ 0, 1 \] y se convierten al formato interno de la textura para el almacenamiento en la matriz de textura. El orden de los píxeles se determina con las coordenadas *x* inferiores correspondientes a las coordenadas de textura inferiores. Si alguno de los píxeles de una fila especificada del fotogramas actual está fuera de la ventana asociada al contexto de representación actual, sus valores son indefinidos.

Si alguno de los píxeles del rectángulo especificado del fotogramas actual está fuera de la ventana de lectura asociada al contexto de representación actual, los valores obtenidos para esos píxeles serán indefinidos. No se realiza ningún cambio en el parámetro *internalFormat*, *width*, *height* o *Border* de la matriz de textura especificada o en textura valores fuera de la subimagen de textura especificada.

No puede incluir llamadas a **glCopyTexSubImage2D** en las listas de visualización.

> [!Note]  
> La función **glCopyTexSubImage2D** solo está disponible en la versión 1,1 o posterior de OpenGL.

 

La texturización no tiene ningún efecto en el modo de índice de color. Las funciones [**glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente de la forma en que afectan al modo en que se dibujan los píxeles mediante [**glDrawPixels**](gldrawpixels.md).

Las siguientes funciones recuperan información relacionada con **glCopyTexSubImage2D**:

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ Texture \_ 2D

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

 

 





