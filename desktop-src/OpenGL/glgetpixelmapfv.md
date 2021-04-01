---
title: función glGetPixelMapfv (GL. h)
description: Las funciones glGetPixelMapfv, glGetPixelMapuiv y glGetPixelMapusv devuelven el mapa de píxeles especificado. | función glGetPixelMapfv (GL. h)
ms.assetid: b09f4799-8e36-4d4f-90d8-4a8ed3d15718
keywords:
- glGetPixelMapfv (función) OpenGL
topic_type:
- apiref
api_name:
- glGetPixelMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f73fb817c347832dfc6a09636173641e5c869b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914401"
---
# <a name="glgetpixelmapfv-function"></a>glGetPixelMapfv función)

Las funciones **glGetPixelMapfv**, [**glGetPixelMapuiv**](glgetpixelmapuiv.md)y [**glGetPixelMapusv**](glgetpixelmapusv.md) devuelven el mapa de píxeles especificado.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetPixelMapfv(
   GLenum  map,
   GLfloat *values
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*map* 
</dt> <dd>

Nombre del mapa de píxeles que se va a devolver. Los valores aceptados son el mapa de \_ píxeles \_ de contabilidad \_ i a i, el mapa de píxeles de GL \_ \_ \_ \_ \_ s \_ a \_ s, el mapa de \_ píxeles de GL \_ \_ i \_ a r, el mapa de píxeles de GL i a g \_ , \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ el mapa de píxeles de contabilidad de la g a la g, el mapa de píxeles de contabilidad B a b y el mapa de píxeles de contabilidad a.

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
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | la *asignación* no era un valor aceptado.<br/>                                                                                           |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Consulte [**glPixelMap**](glpixelmap.md) para obtener una descripción de los valores aceptables para el parámetro *map* . La función **glGetPixelMap** devuelve en *valores* el contenido del mapa de píxeles especificado en la *asignación*. Use mapas de píxeles durante la ejecución de [**glReadPixels**](glreadpixels.md), [**glDrawPixels**](gldrawpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md)y [**glTexImage2D**](glteximage2d.md) para asignar índices de color, índices de estarcido, componentes de color y componentes de profundidad a otros valores.

Los valores enteros sin signo, si se solicitan, se asignan linealmente a partir de la representación interna o de punto flotante, de modo que 1,0 se asigna al valor entero más grande que se puede representar y 0,0 se asigna a cero. Los valores enteros sin signo devueltos no están definidos si el valor del mapa no está en el intervalo \[ 0, 1 \] .

Para determinar el tamaño necesario del *mapa*, llame a [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con la constante simbólica adecuada.

Si se genera un error, no se realiza ningún cambio en el contenido de *los valores*.

Las siguientes funciones recuperan información relacionada con **glGetPixelMap**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con \_ \_ \_ \_ \_ \_ el argumento de mapa de píxeles de contabilidad

**glGet** con el argumento de asignación de píxeles de contabilidad de argumentos \_ \_ \_ \_ a \_ \_ tamaño s

**glGet** con el argumento de mapa de píxeles de GL \_ \_ \_ I \_ a \_ tamaño de R \_

**glGet** con el argumento de la asignación de píxeles de GL \_ \_ \_ I \_ a \_ G \_

**glGet** con el argumento de mapa de píxeles de GL \_ \_ \_ I \_ a \_ B \_

**glGet** con el argumento de \_ la asignación de píxeles de GL \_ \_ I \_ a \_ un \_ tamaño

**glGet** con el argumento de la asignación de píxeles de contabilidad \_ \_ \_ r \_ a \_ \_ tamaño r

**glGet** con el argumento de la asignación de píxeles de GL \_ \_ \_ G \_ a \_ g \_

**glGet** con el tamaño de la asignación de píxeles de contabilidad de argumento \_ \_ \_ b \_ a \_ B \_

**glGet** con el argumento GL de \_ píxel de \_ \_ la asignación \_ a a \_ un \_ tamaño

**glGet** con el argumento \_ \_ tabla de \_ mapa de píxeles máx. \_

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

 

 





