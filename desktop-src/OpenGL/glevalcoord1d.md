---
title: Función glEvalCoord1d (Gl.h)
description: La función glEvalCoord1d evalúa los mapas unidimensionales habilitados.
ms.assetid: 5e884f11-fb3f-4158-8041-6c71509bf7d5
keywords:
- Función GlEvalCoord1d OpenGL
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
ms.openlocfilehash: 54926b6a1a4f09f34034820b576e457a7484f6a3e053607e5a3eed44edbdd110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616232"
---
# <a name="glevalcoord1d-function"></a>Función glEvalCoord1d

La **función glEvalCoord1d** evalúa los mapas unidimensionales habilitados.

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

Valor que es la coordenada *de dominio u* a la función base definida en una función [**glMap1**](glmap1.md) anterior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La **función glEvalCoord1d** evalúa los mapas unidimensionales habilitados en el argumento *u*. Defina mapas con [**glMap1.**](glmap1.md) Habilite o deshabilite con [**glEnable**](glenable.md) [**y glDisable.**](gldisable.md)

Cuando se emite una de las funciones **glEvalCoord,** se evalúan todos los mapas habilitados actualmente de la dimensión indicada. A continuación, para cada asignación habilitada, es como si la función OpenGL correspondiente se emitiese con el valor calculado. Es decir, si GL \_ MAP1 \_ INDEX o GL MAP2 INDEX están habilitados, se simula una función \_ \_ [**glIndex.**](glindex-functions.md) Si GL \_ MAP1 \_ COLOR \_ 4 o GL \_ MAP2 COLOR 4 están habilitados, se simula \_ una función \_ **glcolor.** Si GL MAP1 NORMAL o GL MAP2 NORMAL están habilitados, Se genera un vector normal y, si alguno de los objetos \_ \_ GL \_ \_ \_ MAP1 TEXTURE \_ \_ COORD \_ 1, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 2, GL \_ \_ MAP1 TEXTURE \_ COORD \_ 3, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 4, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 1, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 2, GL \_ MAP2 TEXTURE \_ COORD 3 y GL MAP2 TEXTURE COORD 4 \_ \_ \_ \_ \_ \_ [](gltexcoord-functions.md) están habilitados, se simula una función glTexCoord adecuada.

OpenGL usa valores evaluados en lugar de valores actuales para las evaluaciones que están habilitadas y los valores actuales en caso contrario, para las coordenadas de color, índice de color, normal y textura. Sin embargo, los valores evaluados no actualizan los valores actuales. Por lo tanto, si las funciones [**glVertex**](glvertex-functions.md) se intercalan con funciones **glEvalCoord,** las coordenadas de color, normal y textura asociadas a las funciones **glVertex** no se ven afectadas por los valores generados por las funciones **glEvalCoord,** sino solo por las funciones [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md)y [**glTexCoord**](gltexcoord-functions.md) más recientes.

Las siguientes funciones recuperan información relacionada con **la función glEvalCoord1d:**

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

 

 





