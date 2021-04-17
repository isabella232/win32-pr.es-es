---
title: función glPixelZoom (GL. h)
description: La función glPixelZoom especifica los factores de zoom de píxeles.
ms.assetid: 57ead7d8-0502-46b4-9f66-dbb3cb75b0f9
keywords:
- glPixelZoom (función) OpenGL
topic_type:
- apiref
api_name:
- glPixelZoom
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 065e1735ca0228046cfb08e2fb441d3cdc02af74
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105670051"
---
# <a name="glpixelzoom-function"></a>glPixelZoom función)

La función **glPixelZoom** especifica los factores de zoom de píxeles.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPixelZoom(
   GLfloat xfactor,
   GLfloat yfactor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*xfactor* 
</dt> <dd>

Factor de zoom *x* para las operaciones de escritura en píxeles.

</dd> <dt>

*yfactor* 
</dt> <dd>

Factor de zoom *y* para las operaciones de escritura en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glPixelZoom** especifica valores para los factores de zoom *x* *e y.* Durante la ejecución de [**glDrawPixels**](gldrawpixels.md) o [**glCopyPixels**](glcopypixels.md), si (*x*<sub>r</sub> ,*y*<sub>r</sub> ) es la posición de la trama actual y un elemento determinado está en la fila *n* y la columna *m* del rectángulo de píxeles, los píxeles cuyos centros se encuentran en el rectángulo con esquinas en

![Ecuación que muestra las ubicaciones en las que los píxeles son candidatos para el reemplazo.](images/pix05.png)

son candidatas para el reemplazo. También se modifica cualquier píxel cuyo centro se encuentre en el borde inferior o izquierdo de esta región rectangular.

Los factores de zoom en píxeles no se limitan a los valores positivos. Los factores de zoom negativos reflejan la imagen resultante sobre la posición de la trama actual.

Las siguientes funciones recuperan información relacionada con **glPixelZoom**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ zoom \_ X

**glGet** con el argumento \_ zoom de GL \_ Y

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

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





