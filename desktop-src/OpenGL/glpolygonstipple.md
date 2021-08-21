---
title: Función glPolygonStipple (Gl.h)
description: La función glPolygonStipple establece el patrón de ppling de polígono.
ms.assetid: e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6
keywords:
- Función glPolygonStipple OpenGL
topic_type:
- apiref
api_name:
- glPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f9098ab91af5f258f97e0878ae8cbcb19863ec3bc82765c2664683830539fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614911"
---
# <a name="glpolygonstipple-function"></a>Función glPolygonStipple

La **función glPolygonStipple** establece el patrón de ppling de polígono.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPolygonStipple(
   const GLubyte *mask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mask* 
</dt> <dd>

Puntero a un patrón detippla de 32 x 32 que se desempaquetará de la memoria de la misma manera que [**glDrawPixels**](gldrawpixels.md) desempaquete píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La **función glPolygonStipple** establece el patrón de ppling de polígono. El contrapunto de polígonos, como el contrapunto de líneas (consulte [**glLineStipple),**](gllinestipple.md)enmascara ciertos fragmentos generados por la rasterización, creando un patrón. La ppling es independiente del suavizado de contorno de polígono.

El  parámetro *mask* es un puntero a un patrón detippla de 32 x 32 que se almacena  en memoria igual que los  datos de píxel proporcionados a **glDrawPixels** con alto y ancho iguales a 32, un formato de píxeles de GL COLOR INDEX y un tipo de datos de \_ GL \_  \_ BITMAP. Es decir, el patrón de stipple se representa como una matriz de 32 x 32 de índices de color de 1 bit empaquetados en bytes sin signo. Los parámetros de función [**glPixelStore,**](glpixelstore-functions.md) como GL UNPACK SWAP BYTES y \_ GL \_ \_ \_ UNPACK LSB FIRST, afectan al ensamblado de los bits en un patrón \_ \_ detippla. Sin embargo, las operaciones de transferencia de píxeles (desplazamiento, desplazamiento y mapa de píxeles) no se aplican a la imagen detippla.

El uso de polígonos está habilitado y deshabilitado [**con glEnable**](glenable.md) y **glDisable,** mediante el argumento GL \_ POLYGON \_ STIPPLE. Si está habilitada, se envía un fragmento de polígono rasterizado con coordenadas de ventana *x*<sub>w</sub> e *y*<sub>w</sub> a la siguiente fase de OpenGL si y solo si el bit (*x*<sub>w</sub> mod 32) de la fila (*y*<sub>w</sub> mod 32) del patrón de stipple es uno. Cuando se deshabilita la tupido de polígonos, es como si el patrón de estippla fuera el único.

Las siguientes funciones recuperan información relacionada **con glPolygonStipple**:

[**glGetPolygonStipple**](glgetpolygonstipple.md)

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ POLYGON \_ STIPPLE

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

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> </dl>

 

 





