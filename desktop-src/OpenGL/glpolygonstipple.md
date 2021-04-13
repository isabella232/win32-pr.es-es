---
title: función glPolygonStipple (GL. h)
description: La función glPolygonStipple establece el patrón punteado de polígono.
ms.assetid: e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6
keywords:
- glPolygonStipple (función) OpenGL
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
ms.openlocfilehash: 7a2eb0b2e4319f7e3e37191fb197cd7ff86a2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491128"
---
# <a name="glpolygonstipple-function"></a>glPolygonStipple función)

La función **glPolygonStipple** establece el patrón punteado de polígono.

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

Un puntero a un patrón punteado de 32x32 que se desempaquetará de la memoria del mismo modo que [**glDrawPixels**](gldrawpixels.md) desempaqueta los píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glPolygonStipple** establece el patrón punteado de polígono. El punteado de polígonos, como el punteado de línea (vea [**glLineStipple**](gllinestipple.md)), simplifica determinados fragmentos generados por la rasterización y crea un patrón. El punteado es independiente del suavizado de contorno de polígono.

El parámetro *Mask* es un puntero a un patrón punteado de 32x32 que se almacena en memoria, al igual que los datos de píxeles suministrados a **glDrawPixels** con *alto* y *ancho* iguales a 32, un *formato* de píxel del índice de color GL \_ y un \_ *tipo* de datos de mapa de bits de GL \_ . Es decir, el patrón punteado se representa como una matriz 32x32 de índices de color de 1 bit empaquetados en bytes sin signo. Los parámetros de la función [**glPixelStore**](glpixelstore-functions.md) , como los \_ \_ bytes de intercambio \_ de libro de contabilidad y \_ unpack \_ LSB \_ en primer lugar, afectan al montaje de los bits en un patrón punteado. Sin embargo, las operaciones de transferencia de píxeles (desplazamiento, desplazamiento y mapa de píxeles) no se aplican a la imagen de punteado.

El punteado de polígono está habilitado y deshabilitado con [**glEnable**](glenable.md) y **glDisable**, mediante el argumento de la contabilidad de \_ polígonos \_ . Si está habilitado, se envía un fragmento de polígono rasterizado con coordenadas *x*<sub>w</sub> *e y*<sub>w</sub> a la siguiente fase de OpenGL si y solo si el bit (*x*<sub>w</sub> mod 32) de la fila (*y*<sub>w</sub> mod 32) del patrón punteado es uno. Cuando el punteado de polígono está deshabilitado, es como si el patrón punteado fuera todo.

Las siguientes funciones recuperan información relacionada con **glPolygonStipple**:

[**glGetPolygonStipple**](glgetpolygonstipple.md)

[**glIsEnabled**](glisenabled.md) con \_ argumento cont. \_

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

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> </dl>

 

 





