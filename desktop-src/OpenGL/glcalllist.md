---
title: Función glCallList (Gl.h)
description: La función glCallList ejecuta una lista de visualización.
ms.assetid: 9373d32e-b11e-4a80-8713-da2c1d8d9368
keywords:
- Función glCallList OpenGL
topic_type:
- apiref
api_name:
- glCallList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67805ff50eb4566e8a2a186c10229f944f4003baaef1274e9d4f52dd3b9c2a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082125"
---
# <a name="glcalllist-function"></a>Función glCallList

La **función glCallList** ejecuta una lista de visualización.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glCallList(
   GLuint list
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*list* 
</dt> <dd>

Nombre entero de la lista para mostrar que se va a ejecutar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La invocación de la **función glCallList** comienza la ejecución de la lista de visualización con nombre. Las funciones guardadas en la lista de visualización se ejecutan en orden, como si las llamara sin usar una lista de visualización. Si *list* no se ha definido como una lista para mostrar, **glCallList** se omite.

La **función glCallList** puede aparecer dentro de una lista de visualización. Para evitar la posibilidad de recursividad infinita resultante de mostrar listas que se llaman entre sí, se coloca un límite en el nivel de anidamiento de las listas de presentación durante la ejecución de la lista de presentación. Sin embargo, este límite es al menos 64, pero depende de la implementación.

El estado OpenGL no se guarda y restaura en una llamada a **glCallList.** Por lo tanto, los cambios realizados en el estado OpenGL durante la ejecución de una lista de visualización permanecen una vez completada la ejecución de la lista de presentación. Para conservar el estado de OpenGL entre llamadas **glCallList,** use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib,**](glpopattrib.md) [**glPushMatrix**](glpushmatrix.md)y [**glPopMatrix.**](glpopmatrix.md)

Puede ejecutar listas de visualización entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md), siempre que la lista de presentación incluya solo las funciones permitidas en este intervalo.

Las siguientes funciones recuperan información relacionada **con glCallList**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAX LIST \_ \_ NESTING

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

[**glCallLists**](glcalllists.md)
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

 

 





