---
title: Función glScissor (Gl.h)
description: La función glScissor define el cuadro de diálogo.
ms.assetid: c06a1d20-bf7b-4283-b0fe-8bd80bece4ce
keywords:
- Función glScissor OpenGL
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
ms.openlocfilehash: fafefaaaa3315679af2900808f581324040512816dd2211a0250375c36f824dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777825"
---
# <a name="glscissor-function"></a>Función glScissor

La **función glScissor** define el cuadro de diálogo.

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

Coordenada x (eje vertical) de la esquina inferior izquierda del cuadro de resardenado.

</dd> <dt>

*y* 
</dt> <dd>

Coordenada y (eje horizontal) de la esquina inferior izquierda del cuadro de mosaico. Juntos, x e y especifican la esquina inferior izquierda del cuadro de reanquis. Inicialmente (0,0).

</dd> <dt>

*width* 
</dt> <dd>

Ancho del cuadro de diálogo.

</dd> <dt>

*height* 
</dt> <dd>

Alto del cuadro de resalte. Cuando un contexto OpenGL se adjunta por  *primera* vez a una ventana, *el* ancho y el alto se establecen en las dimensiones de esa ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | El *ancho o* alto *era* negativo.<br/>                                                                                   |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glScissor** define un rectángulo, denominado cuadro de textura, en coordenadas de ventana. Los dos primeros parámetros, *x* *e y*, especifican la esquina inferior izquierda del cuadro. Los *parámetros width* y *height* especifican el ancho y alto del cuadro.

La prueba de desenlace está habilitada y deshabilitada mediante [**glEnable**](glenable.md) y **glDisable** con el argumento GL \_ DE PRUEBA DE DESERCIÓN. \_ Mientras se habilita la prueba de sitiador, los comandos de dibujo solo pueden modificar los píxeles que se encuentran dentro del cuadro de verificación. Las coordenadas de ventana tienen valores enteros en las esquinas compartidas de píxeles del búfer de fotogramas, por lo que **glScissor**(0,0,1,1) solo permite modificar el píxel inferior izquierdo de la ventana y **glScissor**(0,0,0,0) no permite la modificación de todos los píxeles de la ventana.

Cuando se deshabilita la prueba de incoerte, es como si el cuadro de verificación incluyese toda la ventana.

Las siguientes funciones recuperan información relacionada **con glScissor**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ ALCTE BOX \_

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ DE PRUEBA DE INSERTE \_

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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





