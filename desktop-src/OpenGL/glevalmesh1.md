---
title: función glEvalMesh1 (GL. h)
description: Calcula una cuadrícula unidimensional de puntos o líneas.
ms.assetid: 176a4b81-f1a7-42fc-8ecd-bba77a0ec5b3
keywords:
- glEvalMesh1 (función) OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8950dcf397816fca8eb5a6add45c45512c48866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534480"
---
# <a name="glevalmesh1-function"></a>glEvalMesh1 función)

Calcula una cuadrícula unidimensional de puntos o líneas.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glEvalMesh1(
   GLenum mode,
   GLint  i1,
   GLint  i2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mode* 
</dt> <dd>

Valor que especifica si se va a calcular una malla unidimensional de puntos o líneas. Se aceptan las siguientes constantes simbólicas: el \_ punto de contabilidad y la línea de contabilidad \_ .

</dd> <dt>

*I1* 
</dt> <dd>

El primer valor entero para la variable de dominio de cuadrícula i.

</dd> <dt>

*I2* 
</dt> <dd>

El último valor entero para la variable de dominio de cuadrícula i.

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

Use [**glMapGrid**](glmapgrid-functions.md) y [**glEvalMesh**](glevalmesh-functions.md) juntos para generar y evaluar de forma eficaz una serie de valores de dominio de mapa con espaciado uniforme. La función **glEvalMesh** se recorre a través del dominio entero de una cuadrícula de una o dos dimensiones, cuyo intervalo es el dominio de las asignaciones de evaluación especificadas por [**glMap1**](glmap1.md) y [**glMap2**](glmap2.md). El parámetro Mode determina si los vértices resultantes se conectan como puntos, líneas o polígonos rellenos.

En el caso unidimensional, **glEvalMesh1**, la malla se genera como si se ejecutara el siguiente fragmento de código:

[**glBegin**](glbegin.md)(*tipo*);

para (i = i1; i <= I2; i + = 1)

{

[**glEvalCoord1**](glevalcoord1d.md)(i? u + U1)

}

[**glEnd**](glend.md)();

where

? u = (U2 U1)/n

y n, U1 y U2 son los argumentos de la función [**glMapGrid1**](glmapgrid1d.md) más reciente. El parámetro de *tipo* es el de los puntos de contabilidad si el modo \_ es un \_ punto de contabilidad o líneas de contabilidad \_ si el modo es línea de contabilidad \_ . El único requisito absoluto es que si i = n, el valor calculado desde i? u + U1 es exactamente U2.

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
</dt> </dl>

 

 





