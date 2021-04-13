---
title: función glScissor (GL. h)
description: La función glScissor define el cuadro tijeras.
ms.assetid: c06a1d20-bf7b-4283-b0fe-8bd80bece4ce
keywords:
- glScissor (función) OpenGL
topic_type:
- apiref
api_name:
- glScissor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e18559bb30260dcb4285980d8dc75642a7c9ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493024"
---
# <a name="glscissor-function"></a>glScissor función)

La función **glScissor** define el cuadro tijeras.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glScissor(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*x* 
</dt> <dd>

La coordenada x (eje vertical) de la esquina inferior izquierda del cuadro de tijeras.

</dd> <dt>

*y* 
</dt> <dd>

Coordenada y (eje horizontal) de la esquina inferior izquierda del cuadro de tijeras. Juntos, x e y especifican la esquina inferior izquierda del cuadro de tijeras. Inicialmente (0,0).

</dd> <dt>

*width* 
</dt> <dd>

Ancho del cuadro de tijera.

</dd> <dt>

*height* 
</dt> <dd>

Alto del cuadro de tijeras. Cuando un contexto OpenGL se adjunta *primero* a una ventana, el *ancho* y el *alto* se establecen en las dimensiones de esa ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | El *ancho* o el *alto* era negativo.<br/>                                                                                   |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glScissor** define un rectángulo, denominado el cuadro tijeras, en coordenadas de ventana. Los dos primeros parámetros, *x* e *y*, especifican la esquina inferior izquierda del cuadro. Los parámetros de *ancho* y *alto* especifican el ancho y el alto del cuadro.

La prueba de tijera está habilitada y deshabilitada mediante [**glEnable**](glenable.md) y **glDisable** con la prueba de tijeras GL de argumento \_ \_ . Mientras la prueba de tijeras está habilitada, solo se pueden modificar los píxeles que se encuentran dentro del cuadro de tijera. Las coordenadas de la ventana tienen valores enteros en las esquinas compartidas de fotogramas píxeles, de modo que **glScissor**(0, 0, 1, 1) permite que solo se modifique el píxel inferior izquierdo de la ventana y **glScissor**(0,0, 0, 0) no permite la modificación en todos los píxeles de la ventana.

Cuando la prueba de tijeras está deshabilitada, es como si el cuadro de tijeras incluye toda la ventana.

Las siguientes funciones recuperan información relacionada con **glScissor**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) cuadro con el \_ argumento \_

[**glIsEnabled**](glisenabled.md) con argumento de la \_ prueba de tijeras GL \_

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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





