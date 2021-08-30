---
title: Función glPixelZoom (Gl.h)
description: La función glPixelZoom especifica los factores de zoom de píxel.
ms.assetid: 57ead7d8-0502-46b4-9f66-dbb3cb75b0f9
keywords:
- Función glPixelZoom OpenGL
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
ms.openlocfilehash: 07e991b6431a4f1c1752f60f20c46d93e10803d4b2821da5d39162c2eebedfda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081484"
---
# <a name="glpixelzoom-function"></a>Función glPixelZoom

La **función glPixelZoom** especifica los factores de zoom de píxel.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPixelZoom(
   GLfloat xfactor,
   GLfloat yfactor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Xfactor* 
</dt> <dd>

Factor *de zoom x* para las operaciones de escritura de píxeles.

</dd> <dt>

*yfactor* 
</dt> <dd>

Factor de zoom *y* para las operaciones de escritura de píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glPixelZoom** especifica valores para los factores de zoom *x* e *y.* Durante la ejecución de [**glDrawPixels**](gldrawpixels.md) o [**glCopyPixels**](glcopypixels.md), si (*x*<sub>r</sub> ,*y*<sub>r</sub> ) es la posición de trama actual y un elemento determinado está en la *n.ª* fila y la columna *mth* del rectángulo de píxeles, píxeles cuyos centros están en el rectángulo con esquinas en

![Ecuación que muestra las ubicaciones en las que los píxeles son candidatos para su reemplazo.](images/pix05.png)

son candidatos para su reemplazo. También se modifica cualquier píxel cuyo centro se encuentra en el borde inferior o izquierdo de esta región rectangular.

Los factores de zoom de píxeles no se limitan a valores positivos. Los factores de zoom negativos reflejan la imagen resultante sobre la posición de trama actual.

Las siguientes funciones recuperan información relacionada con **glPixelZoom**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ ZOOM \_ X

**glGet con** el argumento GL \_ ZOOM \_ Y

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





