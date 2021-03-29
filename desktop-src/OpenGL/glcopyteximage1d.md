---
title: función glCopyTexImage1D (GL. h)
description: La función glCopyTexImage1D copia píxeles de la fotogramas en una imagen de textura de una dimensión.
ms.assetid: 3b4d12d5-5efe-40d2-ac5f-95ea5ef243dd
keywords:
- glCopyTexImage1D (función) OpenGL
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
ms.openlocfilehash: e63180386c094f0c4e4de0f1a361bc3bcb1c6e5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666039"
---
# <a name="glcopyteximage1d-function"></a>glCopyTexImage1D función)

La función **glCopyTexImage1D** copia píxeles de la fotogramas en una imagen de textura de una dimensión.

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

Destino para el que se cambiarán los datos de la imagen. Debe tener el valor de GL \_ Texture \_ 1D.

</dd> <dt>

*level* 
</dt> <dd>

El número de nivel de detalle. El nivel 0 es la imagen base. *El nivel* *n* es la imagen de reducción del MIP.

</dd> <dt>

*internalFormat* 
</dt> <dd>

El formato interno y la resolución de los datos de textura. Este parámetro debe ser uno de los siguientes valores simbólicos.



| Constante                 | Bits R | G bits | Bits B | Un bits | Bits L | I bits |
|--------------------------|--------|--------|--------|--------|--------|--------|
| libro \_ de contabilidad                |        |        |        |        |        |        |
| GL \_ ALPHA4               |        |        |        | 4      |        |        |
| GL \_ ALPHA8               |        |        |        | 8      |        |        |
| GL \_ ALPHA12              |        |        |        | 12     |        |        |
| GL \_ ALPHA16              |        |        |        | 16     |        |        |
| luminancia del libro de contabilidad \_            |        |        |        |        |        |        |
| GL \_ LUMINANCE4           |        |        |        |        | 4      |        |
| GL \_ LUMINANCE8           |        |        |        |        | 8      |        |
| GL \_ LUMINANCE12          |        |        |        |        | 12     |        |
| GL \_ LUMINANCE16          |        |        |        |        | 16     |        |
| alfa de luminancia de GL \_ \_     |        |        |        |        |        |        |
| GL \_ LUMINANCE4 \_ ALPHA4   |        |        |        | 4      | 4      |        |
| GL \_ LUMINANCE6 \_ ALPHA2   |        |        |        | 2      | 6      |        |
| GL \_ LUMINANCE8 \_ ALPHA8   |        |        |        | 8      | 8      |        |
| GL \_ LUMINANCE12 \_ ALPHA4  |        |        |        | 4      | 12     |        |
| GL \_ LUMINANCE12 \_ ALPHA12 |        |        |        | 12     | 12     |        |
| GL \_ LUMINANCE16 \_ ALPHA16 |        |        |        | 16     | 16     |        |
| intensidad de contabilidad \_            |        |        |        |        |        |        |
| GL \_ INTENSITY4           |        |        |        |        |        | 4      |
| GL \_ INTENSITY8           |        |        |        |        |        | 8      |
| GL \_ INTENSITY12          |        |        |        |        |        | 12     |
| GL \_ INTENSITY16          |        |        |        |        |        | 16     |
| RGB de GL \_                  |        |        |        |        |        |        |
| GL \_ R3 \_ G3 \_ B2           | 3      | 3      | 2      |        |        |        |
| GL \_ RGB4                 | 4      | 4      | 4      |        |        |        |
| GL \_ RGB5                 | 5      | 5      | 5      |        |        |        |
| GL \_ RGB8                 | 8      | 8      | 8      |        |        |        |
| GL \_ RGB10                | 10     | 10     | 10     |        |        |        |
| GL \_ RGB12                | 12     | 12     | 12     |        |        |        |
| GL \_ RGB16                | 16     | 16     | 16     |        |        |        |
| el \_ RGBA de GL                 |        |        |        |        |        |        |
| GL \_ RGBA2                | 2      | 2      | 2      | 2      |        |        |
| GL \_ RGBA4                | 4      | 4      | 4      | 4      |        |        |
| GL \_ RGB5 \_ a1             | 5      | 5      | 5      | 1      |        |        |
| GL \_ RGBA8                | 8      | 8      | 8      | 8      |        |        |
| GL \_ RGB10 \_ a2            | 10     | 10     | 10     | 2      |        |        |
| GL \_ RGBA12               | 12     | 12     | 12     | 12     |        |        |
| GL \_ RGBA16               | 16     | 16     | 16     | 16     |        |        |



 

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

Ancho de la imagen de textura. Debe ser cero o 2N + 2 (*borde*) para algún entero *n*. El alto de la imagen de textura es 1.

</dd> <dt>

*PDA* 
</dt> <dd>

Ancho del borde. Debe ser cero o 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *destino* no era un valor aceptado.<br/>                                                                                                           |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *nivel* era menor que cero o mayor que LOG2 *Max*, donde *Max* es el valor devuelto del \_ tamaño de textura Max GL \_ \_ .<br/>                           |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *Border* no era cero o 1.<br/>                                                                                                                   |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *ancho* era menor que cero, mayor que 2 + \_ tamaño máximo de textura de GL \_ \_ o el *ancho* no se puede representar como 2n + (*Border*) para algún entero *n*.<br/> |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/>                    |



## <a name="remarks"></a>Observaciones

La función **glCopyTexImage1D** define una imagen de textura de una dimensión mediante píxeles de la fotogramas actual, en lugar de la memoria principal, como es el caso de [**glTexImage1D**](glteximage1d.md).

Mediante el nivel de mipmap especificado con el *nivel*, las matrices de texturas se definen como una fila de píxeles alineada con la esquina inferior izquierda de la ventana en las coordenadas especificadas por *x* *e y*, con una longitud *igual al* \* *borde*+ 2. El formato interno de la matriz de textura se especifica con el parámetro *internalFormat* .

La función **glCopyTexImage1D** procesa los píxeles de una fila de la misma manera que [**glCopyPixels**](glcopypixels.md), salvo que antes de la conversión final de los píxeles, todos los valores de los componentes de píxeles se fijan en el intervalo \[ 0, 1 \] y se convierten al formato interno de la textura para el almacenamiento en la matriz de textura. El orden de los píxeles se determina con las coordenadas *x* inferiores correspondientes a las coordenadas de textura inferiores. Si alguno de los píxeles de una fila especificada del fotogramas actual está fuera de la ventana asociada al contexto de representación actual, sus valores son indefinidos.

No puede incluir llamadas a **glCopyTexImage1D** en las listas de visualización.

> [!Note]  
> La función **glCopyTexImage1D** solo está disponible en la versión 1,1 o posterior de OpenGL.

 

La texturización no tiene ningún efecto en el modo de índice de color. Las funciones [**glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente como afectan a [**glDrawPixels**](gldrawpixels.md).

La siguiente función recupera información relacionada con **glCopyTexImage1D**:

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

 

 





