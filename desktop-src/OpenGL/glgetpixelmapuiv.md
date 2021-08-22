---
title: Función glGetPixelMapuiv (Gl.h)
description: Las funciones glGetPixelMapfv, glGetPixelMapuiv y glGetPixelMapusv devuelven el mapa de píxeles especificado. | Función glGetPixelMapuiv (Gl.h)
ms.assetid: a49f5fd2-c350-4acc-8f61-ecb92b0164cc
keywords:
- Función glGetPixelMapuiv OpenGL
topic_type:
- apiref
api_name:
- glGetPixelMapuiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57a8c8354cea3fe43854824da5d4a139f648d7e0615b425fbf7945da9d69fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012193"
---
# <a name="glgetpixelmapuiv-function"></a>Función glGetPixelMapuiv

Las [**funciones glGetPixelMapfv**](glgetpixelmapfv.md), **glGetPixelMapuiv** y [**glGetPixelMapusv**](glgetpixelmapusv.md) devuelven el mapa de píxeles especificado.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetPixelMapuiv(
   GLenum map,
   GLuint *values
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*map* 
</dt> <dd>

Nombre del mapa de píxeles que se devolverá. Los valores aceptados son GL \_ PIXEL MAP I TO \_ \_ \_ \_ I, GL PIXEL MAP S \_ \_ TO \_ \_ \_ S, GL PIXEL MAP I \_ TO \_ \_ \_ \_ R, GL PIXEL MAP \_ I TO \_ \_ \_ \_ G, GL PIXEL MAP I \_ TO \_ \_ \_ \_ B, GL PIXEL MAP I \_ TO \_ \_ \_ \_ A, GL PIXEL MAP \_ R TO \_ \_ \_ \_ R, GL PIXEL MAP \_ G TO \_ \_ \_ \_ G, GL PIXEL MAP \_ B TO B y GL PIXEL MAP A \_ TO \_ \_ \_ \_ \_ \_ \_ \_ A.

</dd> <dt>

*Valores* 
</dt> <dd>

Devuelve el contenido del mapa de píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *map* no era un valor aceptado.<br/>                                                                                           |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

Consulte [**glPixelMap para**](glpixelmap.md) obtener una descripción de los valores aceptables para el *parámetro map.* La **función glGetPixelMap** devuelve *en* valores el contenido del mapa de píxeles especificado en *el mapa*. Use mapas de píxeles durante la ejecución de [**glReadPixels,**](glreadpixels.md) [**glDrawPixels,**](gldrawpixels.md) [**glCopyPixels,**](glcopypixels.md) [**glTexImage1D**](glteximage1d.md)y [**glTexImage2D**](glteximage2d.md) para asignar índices de color, índices de galería de símbolos, componentes de color y componentes de profundidad a otros valores.

Los valores enteros sin signo, si se solicitan, se asignan linealmente a partir de la representación interna fija o de punto flotante, de modo que 1,0 se asigna al valor entero representable más grande y 0,0 se asigna a cero. Los valores enteros sin signo devueltos son indefinidos si el valor del mapa no estaba en el \[ intervalo 0,1 \] .

Para determinar el tamaño necesario del *mapa,* llame [**a glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con la constante simbólica adecuada.

Si se genera un error, no se realiza ningún cambio en el contenido de *los valores*.

Las siguientes funciones recuperan información relacionada **con glGetPixelMap**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ PIXEL MAP I TO I \_ \_ \_ \_ \_ SIZE

**glGet** con el argumento GL \_ PIXEL MAP S TO S \_ \_ \_ \_ \_ SIZE

**glGet** con el argumento GL \_ PIXEL MAP I TO R \_ \_ \_ \_ \_ SIZE

**glGet** con el argumento GL \_ PIXEL MAP I TO G \_ \_ \_ \_ \_ SIZE

**glGet** con el argumento GL \_ PIXEL MAP I TO B \_ \_ \_ \_ \_ SIZE

**glGet** con el argumento GL \_ PIXEL MAP I TO A \_ \_ \_ \_ \_ SIZE

**glGet** con el argumento GL \_ PIXEL MAP R TO R \_ \_ \_ \_ \_ SIZE

**glGet** con el argumento GL \_ PIXEL MAP G TO G \_ \_ \_ \_ \_ SIZE

**glGet** con el argumento GL \_ PIXEL MAP B TO B \_ \_ \_ \_ \_ SIZE

**glGet** con el argumento GL \_ PIXEL MAP A TO A \_ \_ \_ \_ \_ SIZE

**glGet con** el argumento GL \_ MAX PIXEL MAP \_ \_ \_ TABLE

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
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





