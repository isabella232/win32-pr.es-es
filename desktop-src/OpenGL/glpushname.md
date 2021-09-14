---
title: Función glPushName (Gl.h)
description: Las funciones glPushName y glPopName insertan y devuelven la pila de nombres. | Función glPushName (Gl.h)
ms.assetid: e4319018-42c0-4567-b67f-31dbdbee9b13
keywords:
- Función glPushName OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245006"
---
# <a name="glpushname-function"></a>Función glPushName

Las **funciones glPushName** y [**glPopName**](glpopname.md) insertan y devuelven la pila de nombres.

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

Nombre que se insertará en la pila de nombres.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ OVERFLOW**</dt> </dl>    | Se llamó a la función mientras la pila de matriz actual estaba llena.<br/>                                                           |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La **función glPushName** hace que el nombre se inserta en la pila de nombres, que inicialmente está vacía. La [**función glPopName**](glpopname.md) devuelve un nombre de la parte superior de la pila. La pila de nombres se usa durante el modo de selección para permitir que los conjuntos de comandos de representación se identifiquen de forma única. Consta de un conjunto ordenado de enteros sin signo.

La pila de nombres siempre está vacía, mientras que el modo de representación no es GL \_ SELECT. Se **omiten las llamadas a glPushName** [**o glPopName**](glpopname.md) mientras el modo de representación no es GL \_ SELECT.

Las siguientes funciones recuperan información relacionada **con glPushName** y [**glPopName**](glpopname.md):

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ NAME STACK \_ \_ DEPTH

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAX NAME STACK \_ \_ \_ DEPTH

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

 

 





