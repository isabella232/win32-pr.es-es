---
title: función glPushName (GL. h)
description: Las funciones glPushName y glPopName envían y extraen la pila de nombres. | función glPushName (GL. h)
ms.assetid: e4319018-42c0-4567-b67f-31dbdbee9b13
keywords:
- glPushName (función) OpenGL
topic_type:
- apiref
api_name:
- glPushName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff783a108f5cb1ac34141c6c57f47b16e23531a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689777"
---
# <a name="glpushname-function"></a>glPushName función)

Las funciones **glPushName** y [**glPopName**](glpopname.md) envían y extraen la pila de nombres.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPushName(
   GLuint name
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*name* 
</dt> <dd>

Nombre que se va A insertar en la pila de nombres.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**desbordamiento de la pila de GL \_ \_**</dt> </dl>    | Se llamó a la función mientras la pila de matriz actual estaba llena.<br/>                                                           |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glPushName** hace que el nombre se inserte en la pila de nombres, que inicialmente está vacía. La función [**glPopName**](glpopname.md) extrae un nombre de la parte superior de la pila. La pila de nombres se usa durante el modo de selección para permitir que los conjuntos de comandos de representación se identifiquen de forma única. Consta de un conjunto ordenado de enteros sin signo.

La pila de nombres está siempre vacía mientras que el modo de representación no es de selección de libro \_ . Se omiten las llamadas a **glPushName** o [**glPopName**](glpopname.md) mientras que el modo de representación no es Select de GL \_ .

Las siguientes funciones recuperan información relacionada con **glPushName** y [**glPopName**](glpopname.md):

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento de profundidad de la pila de nombre del libro \_ \_ \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento LM \_ Max \_ name \_ stack \_ Depth

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

[**glEnd**](glend.md)
</dt> <dt>

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





