---
title: Función glVertex2d (Gl.h)
description: Especifica un vértice. | Función glVertex2d (Gl.h)
ms.assetid: 96398c2a-35d9-4e40-8471-28a1630c81fd
keywords:
- Función glVertex2d OpenGL
topic_type:
- apiref
api_name:
- glVertex2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c44a70716fdf19ef40564e359530bbdf5bcdc85
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069325"
---
# <a name="glvertex2d-function"></a>Función glVertex2d

Especifica un vértice.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glVertex2d(
   GLdouble x,
   GLdouble y
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*x* 
</dt> <dd>

Especifica la coordenada X de un vértice.

</dd> <dt>

*y* 
</dt> <dd>

Especifica la coordenada Y de un vértice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los comandos de función glVertex se usan en pares [**glBegin**](glbegin.md)glEnd para especificar vértices de punto, línea / [](glend.md) y polígono. Las coordenadas de color, normal y textura actuales están asociadas al vértice cuando se llama a glVertex. Cuando solo *se especifican x* e *y,* *z* tiene como valor predeterminado 0,0 y *w* el valor predeterminado es 1,0. Cuando *se* especifican x , *y* y *z,* *w* tiene como valor predeterminado 1.0. La invocación de glVertex fuera de **un par glBegin** / **glEnd** produce un comportamiento indefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

 





