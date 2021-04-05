---
title: función glCallLists (GL. h)
description: La función glCallLists ejecuta una lista de listas de presentación.
ms.assetid: 7c0a00df-91ee-44ad-9e02-97c1b078e87f
keywords:
- glCallLists (función) OpenGL
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
ms.openlocfilehash: a119f3a63b0f04140a72cc5ca818833ae9ea8b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996530"
---
# <a name="glcalllists-function"></a>glCallLists función)

La función **glCallLists** ejecuta una lista de listas de presentación.

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

El número de listas de presentación que se van a ejecutar.

</dd> <dt>

*type* 
</dt> <dd>

Tipo de valores de *las listas*. Se aceptan las siguientes constantes simbólicas.



| Value                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**BYTE de GL \_**</dt> </dl>                                | El parámetro *lists* se trata como una matriz de bytes con signo, cada uno en el intervalo de-128 a 127.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**\_byte sin signo de \_ GL**</dt> </dl>    | El parámetro *lists* se trata como una matriz de bytes sin signo, cada uno en el intervalo comprendido entre 0 y 255.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**CONTABILIDAD \_ breve**</dt> </dl>                             | El parámetro *lists* se trata como una matriz de enteros de 2 bytes con signo, cada uno en el intervalo de-32768 a 32767.<br/>                                                                                                                                                                                                                                                                         |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**libro de contabilidad \_ corto sin signo \_**</dt> </dl> | El parámetro *lists* se trata como una matriz de enteros de 2 bytes sin signo, cada uno en el intervalo comprendido entre 0 y 65535.<br/>                                                                                                                                                                                                                                                                            |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ int**</dt> </dl>                                   | El parámetro *lists* se trata como una matriz de enteros de 4 bytes con signo.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**libro de contabilidad \_ sin signo \_**</dt> </dl>       | El parámetro *lists* se trata como una matriz de enteros de 4 bytes sin signo.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**valor \_ float de GL**</dt> </dl>                             | El parámetro *lists* se trata como una matriz de valores de punto flotante de 4 bytes.<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="GL_2_BYTES"></span><span id="gl_2_bytes"></span><dl> <dt>**GL \_ 2 \_ bytes**</dt> </dl>                      | El parámetro *lists* se trata como una matriz de bytes sin signo. Cada par de bytes especifica un nombre de lista de presentación único. El valor del par se calcula como 256 veces el valor sin signo del primer byte más el valor sin signo del segundo byte.<br/>                                                                                                                                |
| <span id="GL_3_BYTES"></span><span id="gl_3_bytes"></span><dl> <dt>**GL \_ 3 \_ bytes**</dt> </dl>                      | El parámetro *lists* se trata como una matriz de bytes sin signo. Cada triple de bytes especifica un nombre de lista de presentación único. El valor del tripledo se calcula como 65536 veces el valor sin signo del primer byte, más 256 veces el valor sin signo del segundo byte, más el valor sin signo del tercer byte.<br/>                                                                  |
| <span id="GL_4_BYTES"></span><span id="gl_4_bytes"></span><dl> <dt>**CONT. \_ 4 \_ bytes**</dt> </dl>                      | El parámetro *lists* se trata como una matriz de bytes sin signo. Cada cuádruple de bytes especifica un nombre de lista de presentación único. El valor de quadruplet se calcula como 16777216 veces el valor sin signo del primer byte, más 65536 veces el valor sin signo del segundo byte, más 256 veces el valor sin signo del tercer byte, más el valor sin signo del cuarto byte, más el valor sin signo.<br/> |



 

</dd> <dt>

*Coge* 
</dt> <dd>

Dirección de una matriz de desplazamientos de nombre de la lista de visualización. El tipo de puntero es void porque los desplazamientos pueden ser bytes, cortos, ints o Float, dependiendo del valor de *tipo*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **glCallLists** hace que cada lista de visualización de la lista de nombres pasados como *listas* se ejecute. Como resultado, las funciones guardadas en cada lista de visualización se ejecutan en orden, como si se hubiesen llamado sin usar una lista de visualización. Se omiten los nombres de las listas de visualización que no se han definido.

La función **glCallLists** proporciona un medio eficaz para ejecutar listas de presentación. El parámetro *n* especifica el número de listas con distintos formatos de nombre (especificados por el parámetro de *tipo* ) **glCallLists** ejecuta.

La lista de nombres de lista de visualización no termina en NULL. En su lugar, *n* especifica el número de nombres que se tomarán de *las listas*.

La función [**glListBase**](gllistbase.md) hace que un nivel adicional de direccionamiento indirecto esté disponible. La función **glListBase** especifica un desplazamiento sin signo que se agrega a cada nombre de la lista de visualización especificado en *las listas* antes de que se ejecute la lista de visualización.

La función **glCallLists** puede aparecer dentro de una lista de visualización. Para evitar la posibilidad de que se produzca una recursividad infinita como resultado de la llamada a otras listas, se coloca un límite en el nivel de anidamiento de las listas de visualización durante la ejecución de la lista de visualización. Este límite debe ser al menos 64 y depende de la implementación.

El estado de OpenGL no se guarda y se restaura a través de una llamada a **glCallLists**. Por lo tanto, los cambios realizados en el estado de OpenGL durante la ejecución de las listas de visualización permanecen una vez completada la ejecución. Use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md)y [**glPopMatrix**](glpopmatrix.md) para conservar el estado de OpenGL en las llamadas a **glCallLists** .

Puede ejecutar listas de visualización entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md), siempre que la lista de visualización incluya solo las funciones que se permiten en este intervalo.

Las siguientes funciones recuperan información relacionada con la función **glCallLists** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento base de la lista de contabilidad \_ \_

**glGet** con el argumento \_ \_ anidamiento de lista Max de contabilidad \_

[**glIsList**](glislist.md)

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

 

 





