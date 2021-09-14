---
title: Función glEvalMesh1 (Gl.h)
description: Calcula una cuadrícula unidimensional de puntos o líneas.
ms.assetid: 176a4b81-f1a7-42fc-8ecd-bba77a0ec5b3
keywords:
- Función GlEvalMesh1 OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253809"
---
# <a name="glevalmesh1-function"></a>Función glEvalMesh1

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

Valor que especifica si se debe calcular una malla unidimensional de puntos o líneas. Se aceptan las siguientes constantes simbólicas: GL \_ POINT y GL \_ LINE.

</dd> <dt>

*i1* 
</dt> <dd>

Primer valor entero para la variable de dominio de cuadrícula i.

</dd> <dt>

*i2* 
</dt> <dd>

Último valor entero de la variable de dominio de cuadrícula i.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | Indica que *el modo* no es un valor aceptado. <br/>                                                                            |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md). <br/> |



## <a name="remarks"></a>Observaciones

Use [**glMapGrid**](glmapgrid-functions.md) y [**glEvalMesh**](glevalmesh-functions.md) juntos para generar y evaluar eficazmente una serie de valores de dominio de mapa espaciados uniformemente. La **función glEvalMesh** pasa por el dominio entero de una cuadrícula unidimensional o bidimensional, cuyo intervalo es el dominio de los mapas de evaluación especificados por [**glMap1**](glmap1.md) y [**glMap2.**](glmap2.md) El parámetro mode determina si los vértices resultantes están conectados como puntos, líneas o polígonos rellenos.

En el caso unidimensional, **glEvalMesh1,** la malla se genera como si se ejecutara el siguiente fragmento de código:

[**glBegin**](glbegin.md)*(tipo*);

for (i = i1; i <= i2; i += 1)

{

[**glEvalCoord1**](glevalcoord1d.md)(i?u + u1)

}

[**glEnd**](glend.md)( );

, donde

?u = (u2 u1) / n

y n, u1 y u2 son los argumentos de la función [**glMapGrid1 más**](glmapgrid1d.md) reciente. El *parámetro de* tipo es GL POINTS si el modo es GL POINT o GL LINES si el modo es GL \_ \_ \_ \_ LINE. El único requisito numérico absoluto es que si i = n, el valor calculado a partir de i?u + u1 es exactamente u2.

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
</dt> </dl>

 

 





