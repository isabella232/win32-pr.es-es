---
title: Función glVertex4sv (Gl.h)
description: Especifica un vértice. | Función glVertex4sv (Gl.h)
ms.assetid: 969ecb41-7e72-4b95-9d84-2d995f60f2a3
keywords:
- Función glVertex4sv OpenGL
topic_type:
- apiref
api_name:
- glVertex4sv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 097cf8b57b3ae9bf197c073595d6695eff05ed5e3f5cad39a19b9a7a92ed8c84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035485"
---
# <a name="glvertex4sv-function"></a>Función glVertex4sv

Especifica un vértice.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glVertex4sv(
   const GLshort *v
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*V* 
</dt> <dd>

Puntero a una matriz de cuatro elementos. Los elementos son las coordenadas x, y, z y w de un vértice.

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

 

 





