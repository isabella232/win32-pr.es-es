---
title: Función glEvalMesh2 (Gl.h)
description: Calcula una cuadrícula bidimensional de puntos o líneas.
ms.assetid: 21e94388-903e-4b9d-8e54-9c914d0ce372
keywords:
- Función GlEvalMesh2 OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 531e9f1f6288116d052c728654cd2cf03f38550a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253803"
---
# <a name="glevalmesh2-function"></a>Función glEvalMesh2

Calcula una cuadrícula bidimensional de puntos o líneas.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glEvalMesh2(
   GLenum mode,
   GLint  i1,
   GLint  i2,
   GLint  j1,
   GLint  j2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mode* 
</dt> <dd>

Valor que especifica si se debe calcular una malla bidimensional de puntos, líneas o polígonos. Se aceptan las siguientes constantes simbólicas: GL \_ POINT, GL \_ LINE y GL \_ FILL.

</dd> <dt>

*i1* 
</dt> <dd>

Primer valor entero para la variable de dominio de cuadrícula i.

</dd> <dt>

*i2* 
</dt> <dd>

Último valor entero para la variable de dominio de cuadrícula i.

</dd> <dt>

*j1* 
</dt> <dd>

Primer valor entero para la variable de dominio de cuadrícula j.

</dd> <dt>

*j2* 
</dt> <dd>

Último valor entero para la variable de dominio de cuadrícula j.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | Indica que *el modo* no es un valor aceptado. <br/>                                                                            |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md). <br/> |



## <a name="remarks"></a>Observaciones

Use [**glMapGrid**](glmapgrid-functions.md) y [**glEvalMesh**](glevalmesh-functions.md) conjuntamente para generar y evaluar eficazmente una serie de valores de dominio de mapa espaciados uniformemente. La **función glEvalMesh** atraviesa el dominio entero de una cuadrícula unidimensional, cuyo intervalo es el dominio de los mapas de evaluación especificados por [**glMap1**](glmap1.md) y [**glMap2.**](glmap2.md) El parámetro mode determina si los vértices resultantes están conectados como puntos, líneas o polígonos rellenos.

En el caso bidimensional, **glEvalMesh2**, let

? u = (u2 u1)/n

? v = (v2 v1)/m,

donde n, u1, u2, m, v1 y v2 son los argumentos de la función [**glMapGrid2**](glmapgrid-functions.md) más reciente. A continuación, *si el modo* es GL \_ FILL, **glEvalMesh2** equivale a:

for (j = j1; j < j2; j += 1)

{

[**glBegin**](glbegin.md)(GL \_ QUAD \_ STRIP);

for (i = i1; i <= i2; i += 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , j ? v + v1);

[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , (j+1) ? v + v1);

}

[**glEnd**](glend.md)( ); }

Si *el modo* es GL \_ LINE, una llamada a **glEvalMesh2** equivale a:

for (j = j1; j <= j2; j += 1)

{

[**glBegin**](glbegin.md)(GL \_ LINE \_ STRIP);

for (i = i1; i <= i2; i += 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);

}

[**glEnd**](glend.md)( );

}

for (i = i1; i <= i2; i += 1)

{

[**glBegin**](glbegin.md)(GL \_ LINE \_ STRIP);

for (j = j1; j <= j1; j += 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);

}

glEnd( );

}

Por último, si *el modo* es GL \_ POINT, una llamada a **glEvalMesh2** equivale a:

[**glBegin**](glbegin.md)(GL \_ POINTS);

for (j = j1; j <= j2; j += 1)

{

for (i = i1; i <= i2; i += 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);

}

}

[**glEnd**](glend.md)( );

En los tres casos, los únicos requisitos numéricos absolutos son que, si i = n, el valor calculado a partir de i? u + u1 es exactamente u2 y, si j = m, ¿el valor calculado a partir de j? v + v1 es exactamente v2. Las siguientes funciones recuperan información relacionada **con glEvalMesh**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAP1 \_ GRID \_ DOMAIN

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ MAP2 \_ GRID \_ DOMAIN

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAP1 \_ GRID \_ SEGMENTS

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAP2 \_ GRID \_ SEGMENTS

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

 





