---
title: función gluErrorString (GLU. h)
description: La función gluErrorString genera una cadena de error a partir de un código de error OpenGL o GLU. La cadena de error es sólo ANSI.
ms.assetid: 6d71a6d5-ac00-49f9-a56c-cfeeb88963eb
keywords:
- gluErrorString (función) OpenGL
topic_type:
- apiref
api_name:
- gluErrorString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cdcfad0e2a943bf3a475317f32d37921878a8f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801988"
---
# <a name="gluerrorstring-function"></a>gluErrorString función)

La función **gluErrorString** genera una cadena de error a partir de un código de error OpenGL o Glu. La cadena de error es sólo ANSI.

## <a name="syntax"></a>Sintaxis


```C++
const GLubyte* WINAPI gluErrorString(
   GLenum errCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*errCode* 
</dt> <dd>

Un código de error de OpenGL o GLU.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La función **gluErrorString** genera una cadena de error a partir de un código de error OpenGL o Glu. La cadena tiene un formato ISO Latín 1. Por ejemplo, **gluErrorString**(libro \_ \_ de memoria insuficiente \_ ) devuelve la cadena "memoria insuficiente".

Los códigos de error de GLU estándar son GLU \_ \_ enumeración no válida, Glu \_ valor no válido \_ y Glu \_ memoria insuficiente \_ \_ . Algunas otras funciones GLU pueden devolver códigos de error especializados a través de las devoluciones de llamada. Para obtener la lista de códigos de error de OpenGL, vea [**glGetError**](glgeterror.md).

La función **gluErrorString** solo genera cadenas de error en ANSI. Siempre que sea posible, use **gluErrorStringWIN**, que permite cadenas de error ANSI o Unicode. De este modo, resulta más fácil localizar el programa para usarlo con otro lenguaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[*gluNurbsCallback*](glunurbs.md)
</dt> <dt>

[*gluQuadricCallback*](gluquadric.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> </dl>

 

 





