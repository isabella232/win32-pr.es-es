---
title: Función glVertex4i (Gl.h)
description: Especifica un vértice. | Función glVertex4i (Gl.h)
ms.assetid: eb73c5eb-c03d-489f-b323-bb2245d9b34c
keywords:
- Función glVertex4i OpenGL
topic_type:
- apiref
api_name:
- glVertex4i
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2974bfb823d71003d418a6e08a3c04b80a8bfb707e630cc1a45fc719b7abde99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035585"
---
# <a name="glvertex4i-function"></a>Función glVertex4i

Especifica un vértice.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glVertex4i(
   GLint x,
   GLint y,
   GLint z,
   GLint w
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*x* 
</dt> <dd>

Especifica la coordenada x de un vértice.

</dd> <dt>

*y* 
</dt> <dd>

Especifica la coordenada y de un vértice.

</dd> <dt>

*Z* 
</dt> <dd>

Especifica la coordenada z de un vértice.

</dd> <dt>

*w* 
</dt> <dd>

Especifica la coordenada w de un vértice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Los comandos de función glVertex se usan en pares [**glBegin**](glbegin.md)glEnd para especificar vértices de punto, línea / [](glend.md) y polígono. Las coordenadas de color, normal y textura actuales se asocian al vértice cuando se llama a glVertex. Cuando solo *se especifican x* e *y,* *z* tiene como valor predeterminado 0,0 y *w* el valor predeterminado es 1,0. Cuando *se* especifican x , *y* y *z,* *w* tiene como valor predeterminado 1.0. La invocación de glVertex fuera de un par **glBegin** / **glEnd** produce un comportamiento indefinido.

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glRect**](glrect-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> </dl>

 

 





