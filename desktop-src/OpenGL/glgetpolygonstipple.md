---
title: Función glGetPolygonStipple (Gl.h)
description: La función glGetPolygonStipple devuelve el patrón detippla de polígono.
ms.assetid: 95c1ebfa-8465-4bc1-b3f5-eed696a83816
keywords:
- Función glGetPolygonStipple OpenGL
topic_type:
- apiref
api_name:
- glGetPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 566a2e112b4e9d64487292adafbd4fda016f3a4ceb695a473d958a374c0add8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144198"
---
# <a name="glgetpolygonstipple-function"></a>Función glGetPolygonStipple

La **función glGetPolygonStipple** devuelve el patrón detippla de polígono.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetPolygonStipple(
   GLubyte *mask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mask* 
</dt> <dd>

Devuelve el patrón stipple.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glGetPolygonStipple** devuelve un patrón detippla de polígono de 32 x 32 a través del *parámetro mask.* El patrón se empaqueta en memoria como si  se  llamara [**a glReadPixels**](glreadpixels.md) con un alto y un ancho de 32, el tipo de IMAGEN DE GL y el formato de GL COLOR INDEX, y el patrón detippla se almacenase en un búfer interno de índice de color de  \_  \_ \_ 32 x 32. Sin embargo, a diferencia de **glReadPixels,** las operaciones de transferencia de píxeles (desplazamiento, desplazamiento y mapa de píxeles) no se aplican a la imagen detippla devuelta.

Si se genera un error, no se realiza ningún cambio en el contenido de *mask*.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> </dl>

 

 





