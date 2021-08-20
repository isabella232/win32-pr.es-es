---
title: Función glPopName (Gl.h)
description: Las funciones glPushName y glPopName insertan y devuelven la pila de nombres. | Función glPopName (Gl.h)
ms.assetid: ee741188-b275-4839-a89d-4d988c547d07
keywords:
- Función glPopName OpenGL
topic_type:
- apiref
api_name:
- glPopName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe30aa09d401fc8ef35a3671e02a898776af26111ae0f8e31cd1f6ad3bff70b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290175"
---
# <a name="glpopname-function"></a>Función glPopName

Las [**funciones glPushName**](glpushname.md) y **glPopName** insertan y abren la pila de nombres.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPopName(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ UNDERFLOW**</dt> </dl>   | Se llamó a la función mientras la pila de matriz actual solo contenía una sola matriz.<br/>                                     |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La [**función glPushName**](glpushname.md) hace que el nombre se inserta en la pila de nombres, que inicialmente está vacía. La **función glPopName** devuelve un nombre de la parte superior de la pila. La pila de nombres se usa durante el modo de selección para permitir que los conjuntos de comandos de representación se identifiquen de forma única. Consta de un conjunto ordenado de enteros sin signo.

La pila de nombres siempre está vacía, mientras que el modo de representación no es GL \_ SELECT. Se [**omiten las llamadas a glPushName**](glpushname.md) **o glPopName** mientras el modo de representación no es GL \_ SELECT.

Las siguientes funciones recuperan información relacionada [**con glPushName**](glpushname.md) y **glPopName**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ NAME STACK \_ \_ DEPTH

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAX NAME STACK \_ \_ \_ DEPTH

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

 

 





