---
title: Función glGetPixelMapusv (Gl.h)
description: Las funciones glGetPixelMapfv, glGetPixelMapuiv y glGetPixelMapusv devuelven el mapa de píxeles especificado. | Función glGetPixelMapusv (Gl.h)
ms.assetid: 68b71f9b-5666-4183-aeb8-4c9f09bc5d9c
keywords:
- Función glGetPixelMapusv OpenGL
topic_type:
- apiref
api_name:
- glGetPixelMapusv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38f879da92c9c31b4f44a7e65d8648f94c94fcfaaa8ab3a9d88a39ffc15bd57e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494135"
---
# <a name="glgetpixelmapusv-function"></a>Función glGetPixelMapusv

Las [**funciones glGetPixelMapfv**](glgetpixelmapfv.md), [**glGetPixelMapuiv**](glgetpixelmapuiv.md)y **glGetPixelMapusv** devuelven el mapa de píxeles especificado.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetPixelMapusv(
   GLenum   map,
   GLushort *values
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*map* 
</dt> <dd>

Nombre del mapa de píxeles que se devolverá. Los valores aceptados son GL \_ PIXEL MAP I TO \_ \_ \_ \_ I, GL PIXEL MAP \_ S TO \_ \_ \_ \_ S, GL PIXEL MAP \_ I TO \_ \_ \_ \_ R, GL PIXEL MAP I TO G, GL PIXEL MAP \_ I \_ TO \_ \_ \_ \_ \_ \_ \_ \_ B, GL PIXEL MAP \_ I TO \_ \_ \_ \_ A, GL PIXEL MAP R \_ TO \_ \_ \_ \_ R, GL PIXEL MAP \_ G TO G, GL PIXEL MAP B TO \_ \_ B \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ y GL PIXEL MAP A TO A.

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

Consulte [**glPixelMap para**](glpixelmap.md) obtener una descripción de los valores aceptables para el *parámetro map.* La **función glGetPixelMap** devuelve en *valores* el contenido del mapa de píxeles especificado en *el mapa*. Use mapas de píxeles durante la ejecución de [**glReadPixels,**](glreadpixels.md) [**glDrawPixels,**](gldrawpixels.md) [**glCopyPixels,**](glcopypixels.md) [**glTexImage1D**](glteximage1d.md)y [**glTexImage2D**](glteximage2d.md) para asignar índices de color, índices de galería de símbolos, componentes de color y componentes de profundidad a otros valores.

Los valores enteros sin signo, si se solicitan, se asignan linealmente desde la representación interna fija o de punto flotante, de modo que 1,0 se asigna al valor entero representable más grande y 0,0 se asigna a cero. Los valores enteros sin signo devueltos no están definidos si el valor del mapa no estaba en el \[ intervalo 0,1. \]

Para determinar el tamaño necesario del *mapa,* llame [**a glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con la constante simbólica adecuada.

Si se genera un error, no se realiza ningún cambio en el contenido de *los valores*.

Las funciones siguientes recuperan información relacionada **con glGetPixelMap**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ PIXEL MAP I TO I \_ \_ \_ \_ \_ SIZE

**glGet con** el argumento GL \_ PIXEL MAP S TO S \_ \_ \_ \_ \_ SIZE

**glGet con** el argumento GL \_ PIXEL MAP I TO R \_ \_ \_ \_ \_ SIZE

**glGet** con el argumento GL \_ PIXEL MAP I TO G \_ \_ \_ \_ \_ SIZE

**glGet** con el argumento GL \_ PIXEL MAP I TO B \_ \_ \_ \_ \_ SIZE

**glGet** con el argumento GL \_ PIXEL MAP I TO A \_ \_ \_ \_ \_ SIZE

**glGet con** el argumento GL \_ PIXEL MAP R TO R \_ \_ \_ \_ \_ SIZE

**glGet con** el argumento GL \_ PIXEL MAP G TO G \_ \_ \_ \_ \_ SIZE

**glGet con** el argumento GL \_ PIXEL MAP B TO B \_ \_ \_ \_ \_ SIZE

**glGet con** el argumento GL \_ PIXEL MAP A TO A \_ \_ \_ \_ \_ SIZE

**glGet con** el argumento GL \_ MAX PIXEL MAP \_ \_ \_ TABLE

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





