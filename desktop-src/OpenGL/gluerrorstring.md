---
title: Función gluErrorString (Glu.h)
description: La función gluErrorString genera una cadena de error a partir de un código de error de OpenGL o GLU. La cadena de error es solo ANSI.
ms.assetid: 6d71a6d5-ac00-49f9-a56c-cfeeb88963eb
keywords:
- Función gluErrorString OpenGL
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
ms.openlocfilehash: beef90cfced2b33b612e15c1ef6918de81997520483acfb141f3a307ad64096d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777655"
---
# <a name="gluerrorstring-function"></a>Función gluErrorString

La **función gluErrorString** genera una cadena de error a partir de un código de error de OpenGL o GLU. La cadena de error es solo ANSI.

## <a name="syntax"></a>Sintaxis


```C++
const GLubyte* WINAPI gluErrorString(
   GLenum errCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Errcode* 
</dt> <dd>

Código de error OpenGL o GLU.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **función gluErrorString** genera una cadena de error a partir de un código de error de OpenGL o GLU. La cadena está en formato ISO Latin 1. Por ejemplo, **gluErrorString**(GL \_ OUT OF \_ \_ MEMORY) devuelve la cadena "fuera de memoria".

Los códigos de error estándar de GLU son GLU \_ INVALID \_ ENUM, GLU \_ INVALID VALUE y GLU OUT OF \_ \_ \_ \_ MEMORY. Algunas otras funciones GLU pueden devolver códigos de error especializados a través de devoluciones de llamada. Para obtener la lista de códigos de error de OpenGL, [**vea glGetError**](glgeterror.md).

La **función gluErrorString** genera cadenas de error solo en ANSI. Siempre que sea posible, **use gluErrorStringWIN**, que permite cadenas de error ANSI o Unicode. Esto facilita la localización del programa para su uso con otro idioma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
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

 

 





