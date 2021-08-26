---
title: Función glCallLists (Gl.h)
description: La función glCallLists ejecuta una lista de listas para mostrar.
ms.assetid: 7c0a00df-91ee-44ad-9e02-97c1b078e87f
keywords:
- Función glCallLists OpenGL
topic_type:
- apiref
api_name:
- glCallLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379e15c382b23558786443f03f57349b2504ad251301e3e195885e276d7dbebe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082115"
---
# <a name="glcalllists-function"></a>Función glCallLists

La **función glCallLists** ejecuta una lista de listas para mostrar.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glCallLists(
         GLsizei n,
         GLenum  type,
   const GLvoid  *lists
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*n* 
</dt> <dd>

Número de listas para mostrar que se ejecutarán.

</dd> <dt>

*type* 
</dt> <dd>

El tipo de valores de *enumera*. Se aceptan las siguientes constantes simbólicas.



| Value                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**GL \_ BYTE**</dt> </dl>                                | El *parámetro lists* se trata como una matriz de bytes con firma, cada uno en el intervalo de -128 a 127.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**GL \_ UNSIGNED \_ BYTE**</dt> </dl>    | El *parámetro lists* se trata como una matriz de bytes sin signo, cada uno en el intervalo de 0 a 255.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ SHORT**</dt> </dl>                             | El *parámetro lists* se trata como una matriz de enteros de 2 bytes con signo, cada uno en el intervalo de -32768 a 32767.<br/>                                                                                                                                                                                                                                                                         |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL \_ UNSIGNED \_ SHORT**</dt> </dl> | El *parámetro lists* se trata como una matriz de enteros de 2 bytes sin signo, cada uno en el intervalo comprendido entre 0 y 65535.<br/>                                                                                                                                                                                                                                                                            |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ INT**</dt> </dl>                                   | El *parámetro lists* se trata como una matriz de enteros de 4 bytes con signo.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ UNSIGNED \_ INT**</dt> </dl>       | El *parámetro lists* se trata como una matriz de enteros de 4 bytes sin signo.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ FLOAT**</dt> </dl>                             | El *parámetro lists* se trata como una matriz de valores de punto flotante de 4 bytes.<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="GL_2_BYTES"></span><span id="gl_2_bytes"></span><dl> <dt>**GL \_ 2 \_ BYTES**</dt> </dl>                      | El *parámetro lists* se trata como una matriz de bytes sin signo. Cada par de bytes especifica un único nombre de lista para mostrar. El valor del par se calcula como 256 veces el valor sin signo del primer byte más el valor sin signo del segundo byte.<br/>                                                                                                                                |
| <span id="GL_3_BYTES"></span><span id="gl_3_bytes"></span><dl> <dt>**GL \_ 3 \_ BYTES**</dt> </dl>                      | El *parámetro lists* se trata como una matriz de bytes sin signo. Cada triple de bytes especifica un único nombre de lista para mostrar. El valor del triplete se calcula como 65536 veces el valor sin signo del primer byte, más 256 veces el valor sin signo del segundo byte, más el valor sin signo del tercer byte.<br/>                                                                  |
| <span id="GL_4_BYTES"></span><span id="gl_4_bytes"></span><dl> <dt>**GL \_ 4 \_ BYTES**</dt> </dl>                      | El *parámetro lists* se trata como una matriz de bytes sin signo. Cada uno de los bytes especificados especifica un nombre de lista para mostrar único. El valor del reanual se calcula como 16777216 veces el valor sin signo del primer byte, más 65536 veces el valor sin signo del segundo byte, más 256 veces el valor sin signo del tercer byte, más el valor sin signo del cuarto byte.<br/> |



 

</dd> <dt>

*Listas* 
</dt> <dd>

Dirección de una matriz de desplazamientos de nombre en la lista para mostrar. El tipo de puntero es void porque los desplazamientos pueden ser bytes, shorts, ints o floats, dependiendo del valor de *tipo*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La **función glCallLists** hace que se ejecute cada lista de visualización de la lista de nombres *pasados* como listas. Como resultado, las funciones guardadas en cada lista de visualización se ejecutan en orden, igual que si se llamara a ellas sin usar una lista de visualización. Se omiten los nombres de las listas para mostrar que no se han definido.

La **función glCallLists** proporciona un medio eficaz para ejecutar listas para mostrar. El *parámetro n* especifica el número de listas con varios formatos de nombre (especificados por el parámetro *de* tipo) **que glCallLists** ejecuta.

La lista de nombres de lista para mostrar no termina en NULL. En su lugar, *n* especifica cuántos nombres se van a tomar de *las listas*.

La [**función glListBase**](gllistbase.md) hace que esté disponible un nivel adicional de direccionamiento indirecto. La **función glListBase** especifica un desplazamiento sin signo que se agrega  a cada nombre de lista para mostrar especificado en las listas antes de ejecutar esa lista de visualización.

La **función glCallLists** puede aparecer dentro de una lista de visualización. Para evitar la posibilidad de una recursividad infinita resultante de mostrar listas que se llaman entre sí, se coloca un límite en el nivel de anidamiento de listas para mostrar durante la ejecución de la lista de presentación. Este límite debe ser de al menos 64 y depende de la implementación.

El estado OpenGL no se guarda ni restaura en una llamada a **glCallLists**. Por lo tanto, los cambios realizados en el estado OpenGL durante la ejecución de las listas para mostrar permanecen una vez completada la ejecución. Use [**glPushAttrib,**](glpushattrib.md) [**glPopAttrib,**](glpopattrib.md) [**glPushMatrix**](glpushmatrix.md)y [**glPopMatrix**](glpopmatrix.md) para conservar el estado OpenGL en **las llamadas a glCallLists.**

Puede ejecutar listas para mostrar entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md), siempre y cuando la lista de visualización incluya solo las funciones permitidas en este intervalo.

Las siguientes funciones recuperan información relacionada con **la función glCallLists:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ LIST \_ BASE

**glGet** con el argumento GL \_ MAX \_ LIST \_ NESTING

[**glIsList**](glislist.md)

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glListBase**](gllistbase.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





