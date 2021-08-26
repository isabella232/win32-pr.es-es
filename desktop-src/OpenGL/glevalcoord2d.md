---
title: Función glEvalCoord2d (Gl.h)
description: La función glEvalCoord2d evalúa los mapas bidimensionales habilitados.
ms.assetid: 95963abc-841a-4154-92d5-5ae3e6de0f97
keywords:
- Función GlEvalCoord2d OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 845379985a95fe7514d197bc62a97cb67aa1a7f560f136ab8b9cda7caf31560e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081535"
---
# <a name="glevalcoord2d-function"></a>Función glEvalCoord2d

La **función glEvalCoord2d** evalúa los mapas bidimensionales habilitados.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glEvalCoord2d(
   GLdouble u,
   GLdouble v
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*u* 
</dt> <dd>

Valor que es la coordenada *de dominio u* a la función base definida en una función [**glMap2**](glmap2.md) anterior.

</dd> <dt>

*V* 
</dt> <dd>

Valor que es la coordenada de dominio *v* a la función base definida en una función [**glMap2**](glmap2.md) anterior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La **función glEvalCoord2d** evalúa los mapas bidimensionales habilitados mediante dos valores de dominio, *u* y *v*. Defina mapas con [**glMap1**](glmap1.md) y [**glMap2.**](glmap2.md) Habilite o deshabilite con [**glEnable**](glenable.md) [**y glDisable.**](gldisable.md)

Cuando se emite una de las funciones **glEvalCoord,** se evalúan todos los mapas habilitados actualmente de la dimensión indicada. A continuación, para cada asignación habilitada, es como si la función OpenGL correspondiente se emitiese con el valor calculado. Es decir, si GL MAP1 INDEX o \_ \_ GL \_ MAP2 INDEX están \_ habilitados, se simula una función [**glIndex.**](glindex-functions.md) Si GL \_ MAP1 \_ COLOR \_ 4 o GL \_ MAP2 COLOR 4 están habilitados, se simula \_ una función \_ **glcolor.** Si GL MAP1 NORMAL o GL MAP2 NORMAL están habilitados, Se genera un vector normal y, si alguno de los objetos \_ \_ GL \_ \_ \_ MAP1 TEXTURE \_ \_ COORD \_ 1, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 2, GL \_ \_ MAP1 TEXTURE \_ COORD \_ 3, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 4, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 1, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 2, GL \_ MAP2 TEXTURE \_ COORD 3 y GL MAP2 TEXTURE COORD 4 \_ \_ \_ \_ \_ \_ [](gltexcoord-functions.md) están habilitados, se simula una función glTexCoord adecuada.

OpenGL usa valores evaluados en lugar de valores actuales para las evaluaciones que están habilitadas y los valores actuales en caso contrario, para las coordenadas de color, índice de color, normal y textura. Sin embargo, los valores evaluados no actualizan los valores actuales. Por lo tanto, si las funciones [**glVertex**](glvertex-functions.md) se intercalan con funciones **glEvalCoord,** las coordenadas de color, normal y textura asociadas a las funciones **glVertex** no se ven afectadas por los valores generados por las funciones **glEvalCoord,** sino solo por las funciones [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md)y [**glTexCoord**](gltexcoord-functions.md) más recientes.

Si la generación normal automática está habilitada, **glEvalCoord2d** llama a [**glEnable**](glenable.md) con el argumento GL AUTO NORMAL para generar las normales de superficie de forma analítica, independientemente del contenido o de la habilitación del mapa \_ NORMAL de GL \_ \_ \_ MAP2. Let

![Ecuación que muestra un valor entre productos para un mapa m.](images/evlcrd01.png)

El n normal **generado es**

![Ecuación que muestra el n normal generado para el mapa.](images/evlcrd02.png)

Las siguientes funciones recuperan información relacionada con **la función glEvalCoord2d:**

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

 

 





