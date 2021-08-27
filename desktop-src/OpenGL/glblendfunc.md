---
title: Función glBlendFunc (Gl.h)
description: La función glBlendFunc especifica aritmética de píxeles.
ms.assetid: 6756774b-5eef-419a-a653-0b251aed65a0
keywords:
- Función glBlendFunc OpenGL
topic_type:
- apiref
api_name:
- glBlendFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4b079d0eb83f401eb7e906cb399fab18e5b2fd22f06299fcc62b1e6b4a02e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082135"
---
# <a name="glblendfunc-function"></a>Función glBlendFunc

La **función glBlendFunc** especifica aritmética de píxeles.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glBlendFunc(
   GLenum sfactor,
   GLenum dfactor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sfactor* 
</dt> <dd>

Especifica cómo se calculan los factores de combinación de origen rojo, verde, azul y alfa. Se aceptan nueve constantes simbólicas: GL \_ ZERO, GL \_ ONE, GL \_ DST \_ COLOR, GL \_ ONE MINUS \_ \_ DST \_ COLOR, GL \_ SRC \_ ALPHA, GL ONE MINUS \_ \_ \_ SRC \_ ALPHA, GL \_ DST \_ ALPHA, GL ONE MINUS DST ALPHA y GL \_ \_ \_ \_ \_ SRC \_ ALPHA \_ SATURATE.

</dd> <dt>

*dfactor* 
</dt> <dd>

Especifica cómo se calculan los factores de combinación de destino rojo, verde, azul y alfa. Se aceptan ocho constantes simbólicas: GL \_ ZERO, GL \_ ONE, GL \_ SRC \_ COLOR, GL \_ ONE MINUS \_ \_ SRC \_ COLOR, GL \_ SRC \_ ALPHA, GL ONE MINUS \_ \_ \_ SRC \_ ALPHA, GL DST ALPHA y GL ONE MINUS \_ \_ \_ \_ \_ DST \_ ALPHA.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | Sfactor *o* *dfactor* no era un valor aceptado.<br/>                                                                   |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

En el modo RGB, los píxeles se pueden dibujar mediante una función que combina los valores RGBA entrantes (origen) con los valores RGBA que ya están en el búfer de fotogramas (los valores de destino). De forma predeterminada, la combinación está deshabilitada. Use [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento BLEND de GL \_ para habilitar y deshabilitar la combinación.

Cuando se habilita, **glBlendFunc** define el funcionamiento de la combinación. El *parámetro sfactor* especifica cuál de los nueve métodos se usa para escalar los componentes de color de origen. El *parámetro dfactor* especifica cuál de los ocho métodos se usa para escalar los componentes de color de destino. Los once métodos posibles se describen en la tabla siguiente. Cada método define cuatro factores de escala, uno para rojo, verde, azul y alfa.

En la tabla y en las ecuaciones posteriores, los componentes de color de origen y destino se conocen como (*R*? , *G*? , *B*? , *A*? ) y (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ). Se entiende que tienen valores enteros entre cero y (*k*<sub>R</sub> , *k*<sub>G</sub> , *k*<sub>R</sub> , *k*<sub>A</sub> ), donde

*k*<sub>R</sub> = 2 <sup>m</sup>*R* - 1

*k*<sub>G</sub> = 2 <sup>m</sup>*G* - 1

*k*<sub>B</sub> = 2 <sup>m B</sup> - 1

*k*<sub>A</sub> = 2 <sup>m</sup>*A* - 1

y (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>A</sub> ) es el número de bits rojos, verdes, azules y alfa.

Los factores de escala de origen y destino se conocen como (*s*<sub>R</sub> , *s*<sub>G</sub> , *s*<sub>B</sub> , *s*<sub>A</sub> ) y (*d*<sub>R</sub> , *d*<sub>G</sub> , *d*<sub>B</sub> , *d*<sub>A</sub> ). Los factores de escala descritos en la tabla, indicados *(f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A),</sub> representan factores de origen o de destino. Todos los factores de escala tienen un \[ intervalo de 0,1 \] .



| Parámetro                  | (*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GL \_ ZERO                   | (0,0,0,0)                                                                                                                                                    |
| GL \_ ONE                    | (1,1,1,1)                                                                                                                                                    |
| GL \_ SRC \_ COLOR             | (*R*? / *k*<sub>R</sub> , *G*? / *k*<sub>G</sub> , *B*? / *k*<sub>B</sub> , *A*? / *k*<sub>A</sub> )                                                         |
| GL \_ ONE MENOS COLOR \_ \_ SRC \_ | (1,1,1,1) - (*R*? / *k*<sub>R</sub> , *G*? / *k*<sub>G</sub> , *B*? / *k*<sub>B</sub> , *A*? / *k*<sub>A</sub> )                                             |
| GL \_ DST \_ COLOR             | (*R*<sub>d</sub>  /  *k*<sub>R,</sub> *G*<sub>d</sub>  /  *k*<sub>G,</sub> *B*<sub>d</sub>  /  *k*<sub>B</sub> , *A* d <sub></sub>  /  *k*<sub>A</sub> )             |
| GL \_ ONE MENOS COLOR \_ \_ DST \_ | (1,1,1,1) - (*R*<sub>d</sub>  /  *k*<sub>R</sub> , *G*<sub>d</sub>  /  *k*<sub>G</sub> , *B*<sub>d</sub>  /  *k*<sub>B</sub> , *A*<sub>d</sub>  /  *k*<sub>A</sub> ) |
| GL \_ SRC \_ ALPHA             | (*A*? / *k*<sub>A</sub> , *A*? / *k*<sub>A</sub> , *A*? / *k*<sub>A</sub> , *A*? / *k*<sub>A</sub> )                                                         |
| GL \_ ONE \_ MENOS \_ SRC \_ ALPHA | (1,1,1,1) - (*A*? / *k*<sub>A</sub> , *A*? / *k*<sub>A</sub> , *A*? / *k*<sub>A</sub> , *A*? / *k*<sub>A</sub> )                                             |
| GL \_ DST \_ ALPHA             | (*A*<sub>d</sub>  /  *k*<sub>A,</sub> *A*<sub>d</sub>  /  *k*<sub>A,</sub> *A*<sub>d</sub>  /  *k*<sub>A,</sub> *A*<sub>d</sub>  /  *k*<sub>A</sub> )             |
| GL \_ ONE \_ MENOS \_ DST \_ ALPHA | (1,1,1,1) - (*A*<sub>d</sub>  /  *k*<sub>A</sub> , *A*<sub>d</sub>  /  *k*<sub>A</sub> , *A*<sub>d</sub>  /  *k*<sub>A</sub> , *A*<sub>d</sub>  /  *k*<sub>A</sub> ) |
| SATURACIÓN ALFA de GL \_ SRC \_ \_   | (*i,i,i,* 1)                                                                                                                                                 |



 

En la tabla,

*i* = min (*A*? , *k*<sub>A</sub>   -  *D*<sub>)</sub> / *k*<sub>A</sub>

Para determinar los valores RGBA combinados de un píxel al dibujar en modo RGBA, el sistema usa las ecuaciones siguientes:

*R* (*d*) = min( *k*<sub>R</sub> , *R*? *s*<sub>R</sub>  +  *R*<sub>d</sub> *d*<sub>R</sub> )

*G* (*d*) = min( *k*<sub>G</sub> , *G*? *s*<sub>G</sub>  +  *G*<sub>d</sub> *d*<sub>G</sub> )

*B* (*d*) = min( *k*<sub>B</sub> *, B*? *s*<sub>B</sub>  +  *B*<sub>d</sub> *d*<sub>B</sub> )

*A* (*d*) = min( *k*<sub>A</sub> , *A*? *s*<sub>A</sub>  +  *D*<sub>d</sub> *D*<sub>D</sub> )

A pesar de la precisión aparente de las ecuaciones anteriores, la aritmética de mezcla no se especifica exactamente, porque la combinación funciona con valores de color entero imprecisos. Sin embargo, se garantiza que un factor de mezcla que debe ser igual a uno no modifique su multiplicando, y un factor de mezcla igual a cero reduce su multiplicación a cero. Por ejemplo, cuando *sfactor* es GL \_ SRC \_ ALPHA, *dfactor* es GL \_ ONE MENOS SRC ALPHA y A ? es igual a \_ k \_ \_ <sub>A,</sub> las ecuaciones se reducen a reemplazo simple:

*R*<sub>d</sub>  =  *R*?

*G*<sub>d</sub>  =  *G*?

B <sub>d</sub>  =  *B*?

*A*<sub>d</sub>  =  *A*?

## <a name="examples"></a>Ejemplos

La transparencia se implementa mejor mediante **glBlendFunc**(GL \_ SRC \_ ALPHA, GL ONE MINUS SRC ALPHA) con primitivas ordenadas de más lejanas a \_ \_ más \_ \_ cercanas. Tenga en cuenta que este cálculo de transparencia no requiere la presencia de bitplanes alfa en el búfer de fotogramas.

También puede usar **glBlendFunc**(GL \_ SRC \_ ALPHA, GL \_ ONE MINUS \_ \_ SRC \_ ALPHA) para representar puntos y líneas suavizados en orden arbitrario.

Para optimizar el suavizado de contorno de polígonos, use **glBlendFunc**(GL \_ SRC \_ ALPHA \_ SATURATE, GL ONE) con polígonos ordenados de más cercanos a \_ más lejanos. (Consulte el GL). \_ Argumento \_ POLYGON SMOOTH en [**glEnable para**](glenable.md) obtener información sobre el suavizado de contorno de polígono). Los bitplanes alfa de destino, que deben estar presentes para que esta función blend funcione correctamente, almacenan la cobertura acumulada.

El alfa entrante (origen) es una opacidad material, que va desde 1,0 *(K*<sub>A),</sub> que representa la opacidad completa, hasta 0,0 (0), lo que representa una transparencia completa.

Cuando se habilita más de un búfer de color para dibujar, cada búfer habilitado se mezcla por separado y el contenido del búfer se usa para el color de destino. (Vea [**glDrawBuffer).**](gldrawbuffer.md)

La combinación solo afecta a la representación RGBA. Los representadores de índice de color lo omiten.

Las siguientes funciones recuperan información relacionada **con glBlendFunc**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ BLEND \_ SRC

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ BLEND \_ DST

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ BLEND

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

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





