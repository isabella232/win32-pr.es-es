---
title: función glEvalCoord1d (GL. h)
description: La función glEvalCoord1d evalúa las asignaciones unidimensionales habilitadas.
ms.assetid: 5e884f11-fb3f-4158-8041-6c71509bf7d5
keywords:
- glEvalCoord1d (función) OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord1d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 239d0cc6267989bfd4ae020f1f8935c0cca1c192
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685894"
---
# <a name="glevalcoord1d-function"></a>glEvalCoord1d función)

La función **glEvalCoord1d** evalúa las asignaciones unidimensionales habilitadas.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glEvalCoord1d(
   GLdouble u
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*u* 
</dt> <dd>

Un valor que es la coordenada del dominio *u* a la función base definida en una función [**glMap1**](glmap1.md) anterior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **glEvalCoord1d** evalúa las asignaciones unidimensionales habilitadas en el argumento *u*. Definir asignaciones con [**glMap1**](glmap1.md). Habilitarlas o deshabilitarlas con [**glEnable**](glenable.md) y [**glDisable**](gldisable.md).

Cuando se emite una de las funciones **glEvalCoord** , se evalúan todas las asignaciones habilitadas actualmente de la dimensión indicada. A continuación, para cada asignación habilitada, es como si la función de OpenGL correspondiente se hubiera emitido con el valor calculado. Es decir, si \_ \_ se habilita GL MAP1 index o GL \_ MAP2 ( \_ index, se simula una función [**glIndex**](glindex-functions.md) . Si GL \_ MAP1 \_ color \_ 4 o GL \_ MAP2 ( \_ color \_ 4 está habilitado, se simula una función **glcolor** . Si GL \_ MAP1 \_ normal o GL \_ MAP2 ( \_ normal está habilitado, se genera un vector normal, y si alguno de los MAP1 de contabilidad de la textura de GL \_ \_ \_ \_ 1, GL MAP1 Texture 4, GL MAP1 Texture de la textura 3, GL \_ \_ \_ \_ \_ \_ \_ \_ \_ MAP1 \_ Texture \_ \_ 4, GL \_ MAP2 ( \_ Texture \_ 4, \_ GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 2, GL \_ MAP2 (Texture 4 y \_ \_ \_ GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 4 está habilitado, se simula una función [**glTexCoord**](gltexcoord-functions.md) adecuada.

OpenGL usa los valores evaluados en lugar de los valores actuales de las evaluaciones que están habilitadas, y los valores actuales en caso contrario, para las coordenadas de color, índice de color, normal y textura. Sin embargo, los valores evaluados no actualizan los valores actuales. Por lo tanto, si las funciones de [**glVertex**](glvertex-functions.md) se intercalan con las funciones **glEvalCoord** , las coordenadas de color, normal y de textura asociadas con las funciones **glVertex** no se ven afectadas por los valores generados por las funciones **GlEvalCoord** , sino solo por las funciones [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md)y [**glTexCoord**](gltexcoord-functions.md) más recientes.

Las siguientes funciones recuperan información relacionada con la función **glEvalCoord1d** :

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Vertex \_ 3

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Vertex \_ 4

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ index

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ color \_ 4

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ normal

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Texture \_ coordenadas \_ 1

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Texture \_ coordenadas \_ 2

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP1 \_ Texture \_ coordenadas \_ 3

[**glIsEnabled**](glisenabled.md) con el argumento \_ GL \_ MAP1 \_ Texture \_ 4

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Vertex \_ 3

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Vertex \_ 4

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ index

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ color \_ 4

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ normal

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 1

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 2

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ MAP2 ( \_ Texture \_ coordenadas \_ 3

[**glIsEnabled**](glisenabled.md) con el argumento \_ GL \_ MAP2 ( \_ Texture \_ 4

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ auto \_ normal

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





