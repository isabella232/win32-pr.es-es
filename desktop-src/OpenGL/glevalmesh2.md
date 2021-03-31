---
title: función glEvalMesh2 (GL. h)
description: Calcula una cuadrícula bidimensional de puntos o líneas.
ms.assetid: 21e94388-903e-4b9d-8e54-9c914d0ce372
keywords:
- glEvalMesh2 (función) OpenGL
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801652"
---
# <a name="glevalmesh2-function"></a>glEvalMesh2 función)

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

Valor que especifica si se va a calcular una malla bidimensional de puntos, líneas o polígonos. Se aceptan las siguientes constantes simbólicas: \_ punto de contabilidad, línea de libro de contabilidad \_ y relleno de contabilidad \_ .

</dd> <dt>

*I1* 
</dt> <dd>

El primer valor entero para la variable de dominio de cuadrícula i.

</dd> <dt>

*I2* 
</dt> <dd>

El último valor entero para la variable de dominio de cuadrícula i.

</dd> <dt>

*j1* 
</dt> <dd>

El primer valor entero para la variable de dominio de cuadrícula j.

</dd> <dt>

*J2* 
</dt> <dd>

Último valor entero para la variable de dominio de cuadrícula j.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | Indica que el *modo* no es un valor aceptado. <br/>                                                                            |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md). <br/> |



## <a name="remarks"></a>Observaciones

Use [**glMapGrid**](glmapgrid-functions.md) y [**glEvalMesh**](glevalmesh-functions.md) en tándem para generar y evaluar eficazmente una serie de valores de dominio de mapa con espaciado uniforme. La función **glEvalMesh** se recorre a través del dominio entero de una cuadrícula de una o dos dimensiones, cuyo intervalo es el dominio de las asignaciones de evaluación especificadas por [**glMap1**](glmap1.md) y [**glMap2**](glmap2.md). El parámetro Mode determina si los vértices resultantes se conectan como puntos, líneas o polígonos rellenos.

En el caso bidimensional, **glEvalMesh2**, Let

? u = (U2 U1)/n

? v = (V2 V1)/m,

donde n, U1, U2, m, V1 y V2 son los argumentos de la función [**glMapGrid2**](glmapgrid-functions.md) más reciente. A continuación, si el *modo* es \_ relleno de contabilidad, **glEvalMesh2** es equivalente a:

para (j = J1; j < J2; j + = 1)

{

[**glBegin**](glbegin.md)( \_ banda cuádruple de GL \_ );

para (i = i1; i <= I2; i + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1 (), j? v + v1);

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1 (), (j + 1)? v + v1);

}

[**glEnd**](glend.md)(); }

Si el *modo* es \_ línea de contabilidad, una llamada a **glEvalMesh2** es equivalente a:

para (j = J1; j <= J2; j + = 1)

{

[**glBegin**](glbegin.md)(franja de línea de contabilidad \_ \_ );

para (i = i1; i <= I2; i + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);

}

[**glEnd**](glend.md)();

}

para (i = i1; i <= I2; i + = 1)

{

[**glBegin**](glbegin.md)(franja de línea de contabilidad \_ \_ );

para (j = J1; j <= J1; j + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);

}

glEnd( );

}

Y, por último, si el *modo* es \_ el punto de contabilidad, una llamada a **glEvalMesh2** es equivalente a:

[**glBegin**](glbegin.md)(puntos de contabilidad \_ );

para (j = J1; j <= J2; j + = 1)

{

para (i = i1; i <= I2; i + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);

}

}

[**glEnd**](glend.md)();

En los tres casos, los únicos requisitos numéricos absolutos son que si i = n, el valor calculado desde i? u + U1 es exactamente U2 y, si j = m, el valor calculado a partir de j? v + v1 es exactamente V2. Las siguientes funciones recuperan información relacionada con **glEvalMesh**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ MAP1 \_ Grid \_ Domain

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ MAP2 ( \_ Grid \_ Domain

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ MAP1 \_ segmentos de cuadrícula de GL \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ MAP2 ( \_ segmentos de cuadrícula de GL \_

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

 





