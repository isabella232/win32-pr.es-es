---
title: Función glVertex3sv (Gl.h)
description: Especifica un vértice. | Función glVertex3sv (Gl.h)
ms.assetid: 8b819a95-f834-4c6e-b88a-a96ae9b36c71
keywords:
- Función glVertex3sv OpenGL
topic_type:
- apiref
api_name:
- glVertex3sv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbf8117577067328bc71d519bd5d2a8b30bd264caae7ffe7a81683116e3d95a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035815"
---
# <a name="glvertex3sv-function"></a>Función glVertex3sv

Especifica un vértice.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glVertex3sv(
   const GLshort *v
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*V* 
</dt> <dd>

Puntero a una matriz de tres elementos. Los elementos son las coordenadas x, y y y z de un vértice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

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

 

 





