---
title: función glCopyTexSubImage1D (GL. h)
description: La función glCopyTexSubImage1D copia una subimagen de una imagen de textura de una dimensión de fotogramas.
ms.assetid: 718aee8a-6dce-49e1-a441-19beccd89f8d
keywords:
- glCopyTexSubImage1D (función) OpenGL
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996624"
---
# <a name="glcopytexsubimage1d-function"></a>glCopyTexSubImage1D función)

La función **glCopyTexSubImage1D** copia una subimagen de una imagen de textura de una dimensión de fotogramas.

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

Destino al que se cambiarán los datos de la imagen. Debe tener el valor de GL \_ Texture \_ 1D.

</dd> <dt>

*level* 
</dt> <dd>

El número de nivel de detalle. El nivel 0 es la imagen base. *El nivel* *n* es la imagen de reducción del MIP.

</dd> <dt>

*xoffset* 
</dt> <dd>

Desplazamiento textura dentro de la matriz de textura.

</dd> <dt>

*x* 
</dt> <dd>

Coordenada x del plano de la ventana de la esquina inferior izquierda de la fila de píxeles que se va a copiar.

</dd> <dt>

*y* 
</dt> <dd>

Coordenada y del plano de la ventana de la esquina inferior izquierda de la fila de píxeles que se va a copiar.

</dd> <dt>

*width* 
</dt> <dd>

Ancho de la subimagen de la imagen de textura. Especificar una subimagen de textura con un ancho de cero no tiene ningún efecto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *destino* no era un valor aceptado.<br/>                                                                                                                                                                               |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *nivel* era menor que cero o el *nivel* es mayor que el *registro* 2 (*Max*), donde *Max* es el valor devuelto del \_ tamaño de textura Max GL \_ \_ .<br/>                                                                                 |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *xoffset* era menor que *Border* o (el  +  *ancho* de xoffset) era mayor que (*w*  +  *Border*), donde *w* es el \_ ancho y el borde de la textura GL \_ es  \_ Border Texture \_ Border. Tenga en cuenta que *w* incluye dos veces el ancho del *borde* .<br/> |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *ancho* era menor *que Border* o *y* era menor que *Border*, donde *Border* es el ancho del borde de la matriz de textura.<br/>                                                                                            |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Una operación [**glTexImage1D**](glteximage1d.md) anterior no definió la matriz de textura.<br/>                                                                                                                   |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/>                                                                                        |



## <a name="remarks"></a>Observaciones

La función **glCopyTexSubImage1D** reemplaza una parte de una imagen de textura de una dimensión mediante píxeles de la fotogramas actual, en lugar de la memoria principal, como es el caso de [**glTexSubImage1D**](gltexsubimage1d.md).

Una fila de píxeles que comienza con las coordenadas de la ventana especificadas por *x* *e y y con* el *ancho* de longitud reemplaza a la parte de la matriz de textura con los índices *xoffset* a *xoffset* + (*width* -1). El destino de la matriz de textura no puede incluir ningún textura fuera de la matriz de textura especificada originalmente.

La función **glCopyTexSubImage1D** procesa los píxeles de una fila de la misma manera que [**glCopyPixels**](glcopypixels.md) , salvo que antes de la conversión final de los píxeles, todos los valores de los componentes de píxeles se fijan en el intervalo \[ 0, 1 \] y se convierten al formato interno de la textura para el almacenamiento en la matriz de textura. El orden de los píxeles se determina con las coordenadas *x* inferiores correspondientes a las coordenadas de textura inferiores. Si alguno de los píxeles de una fila especificada del fotogramas actual está fuera de la ventana asociada al contexto de representación actual, sus valores son indefinidos.

No se realiza ningún cambio en el parámetro *internalFormat*, *width* o *Border* de la matriz de textura especificada o en textura valores fuera de la subimagen de textura especificada.

No puede incluir llamadas a **glCopyTexSubImage1D** en las listas de visualización.

> [!Note]  
> La función **glCopyTexSubImage1D** solo está disponible en la versión 1,1 o posterior de OpenGL.

 

La texturización no tiene ningún efecto en el modo de índice de color. Las funciones [**glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente de la forma en que afectan al modo en que se dibujan los píxeles mediante [**glDrawPixels**](gldrawpixels.md).

Las siguientes funciones recuperan información relacionada con **glCopyTexSubImage1D**:

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ Texture \_ 1D

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

 

 





