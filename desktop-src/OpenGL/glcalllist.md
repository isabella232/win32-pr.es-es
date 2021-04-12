---
title: función glCallList (GL. h)
description: La función glCallList ejecuta una lista de visualización.
ms.assetid: 9373d32e-b11e-4a80-8713-da2c1d8d9368
keywords:
- glCallList (función) OpenGL
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
ms.openlocfilehash: f0d356adc5d16ceb0ea10e3834d8dbb98abed2b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150436"
---
# <a name="glcalllist-function"></a>glCallList función)

La función **glCallList** ejecuta una lista de visualización.

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

El nombre entero de la lista de visualización que se va a ejecutar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Al invocar la función **glCallList** se inicia la ejecución de la lista de visualización con nombre. Las funciones guardadas en la lista de visualización se ejecutan en orden, como si se hubieran llamado sin usar una lista de visualización. Si *List* no se ha definido como una lista de visualización, se omite **glCallList** .

La función **glCallList** puede aparecer dentro de una lista de visualización. Para evitar la posibilidad de que se produzca una recursividad infinita como resultado de la llamada a otras listas, se coloca un límite en el nivel de anidamiento de las listas de visualización durante la ejecución de la lista de visualización. Este límite es al menos 64, sin embargo, depende de la implementación.

El estado de OpenGL no se guarda y se restaura a través de una llamada a **glCallList**. Por lo tanto, los cambios realizados en el estado de OpenGL durante la ejecución de una lista de visualización permanecen después de que se complete la ejecución de la lista de visualización. Para conservar el estado de OpenGL en todas las llamadas de **glCallList** , use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md)y [**glPopMatrix**](glpopmatrix.md).

Puede ejecutar listas de visualización entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md), siempre que la lista de visualización incluya solo las funciones que se permiten en este intervalo.

Las siguientes funciones recuperan información relacionada con **glCallList**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ anidamiento de lista Max de contabilidad \_

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

 

 





