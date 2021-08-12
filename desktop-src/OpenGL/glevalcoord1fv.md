---
title: Función glEvalCoord1fv (Gl.h)
description: La función glEvalCoord1fv evalúa los mapas unidimensionales habilitados.
ms.assetid: d5c1cc99-ecf6-4d78-99bb-953b4c362ff4
keywords:
- Función GlEvalCoord1fv OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord1fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2093925d26471f8f9127382661a6e502b020680d3f67314fecd7a5d28fe77632
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616222"
---
# <a name="glevalcoord1fv-function"></a>Función glEvalCoord1fv

La **función glEvalCoord1fv** evalúa los mapas unidimensionales habilitados.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glEvalCoord1fv(
   const GLfloat *u
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*u* 
</dt> <dd>

Puntero a una matriz que contiene la coordenada de *dominio u*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La [**función glEvalCoord1fv**](glevalcoord1dv.md) evalúa los mapas unidimensionales habilitados en el argumento *u*. Defina mapas con [**glMap1.**](glmap1.md) Habilite o deshabilite con [**glEnable**](glenable.md) [**y glDisable**](gldisable.md).

Cuando se emite una de las funciones **glEvalCoord,** se evalúan todos los mapas habilitados actualmente de la dimensión indicada. A continuación, para cada asignación habilitada, es como si la función OpenGL correspondiente se emitiese con el valor calculado. Es decir, si GL \_ MAP1 \_ INDEX o GL \_ MAP2 INDEX están \_ habilitados, se simula una función [**glIndex.**](glindex-functions.md) Si GL \_ MAP1 \_ COLOR \_ 4 o GL \_ MAP2 \_ COLOR \_ 4 están habilitados, se simula una función **glcolor.** Si GL MAP1 NORMAL o GL MAP2 NORMAL están habilitados, Se genera un vector normal y, si se habilita alguna de LAS FUNCIONES \_ \_ \_ \_ \_ MAP1 \_ TEXTURE \_ COORD \_ 1, GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2, GL \_ \_ MAP1 TEXTURE \_ COORD \_ 3, GL \_ MAP1 TEXTURE \_ \_ \_ COORD 4, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 1, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 2, GL \_ MAP2 TEXTURE \_ \_ COORD 3 y GL \_ MAP2 TEXTURE COORD 4, \_ \_ \_ \_ [](gltexcoord-functions.md) se simula una función glTexCoord adecuada.

OpenGL usa valores evaluados en lugar de valores actuales para las evaluaciones habilitadas y los valores actuales en caso contrario, para las coordenadas de color, índice de color, normal y textura. Sin embargo, los valores evaluados no actualizan los valores actuales. Por lo tanto, si las funciones [**glVertex**](glvertex-functions.md) se intercalan con funciones **glEvalCoord,** las coordenadas de color, normal y textura asociadas a las funciones **glVertex** no se ven afectadas por los valores generados por las funciones **glEvalCoord,** sino solo por las funciones [**glColor**](glcolor-functions.md), [**glIndex,**](glindex-functions.md) [**glNormal**](glnormal-functions.md)y [**glTexCoord**](gltexcoord-functions.md) más recientes.

Las siguientes funciones recuperan información relacionada con **la función glEvalCoord1fv:**

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ VERTEX \_ 3

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ VERTEX \_ 4

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ INDEX

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ COLOR \_ 4

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ NORMAL

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 3

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 4

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ VERTEX \_ 3

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ VERTEX \_ 4

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ INDEX

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ COLOR \_ 4

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ NORMAL

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 1

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 2

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 3

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 4

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ AUTO \_ NORMAL

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

 

 





