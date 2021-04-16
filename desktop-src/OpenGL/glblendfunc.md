---
title: función glBlendFunc (GL. h)
description: La función glBlendFunc especifica la aritmética de píxeles.
ms.assetid: 6756774b-5eef-419a-a653-0b251aed65a0
keywords:
- glBlendFunc (función) OpenGL
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
ms.openlocfilehash: 6300543bbf589c704da6d941bd743f693e0ed5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686006"
---
# <a name="glblendfunc-function"></a>glBlendFunc función)

La función **glBlendFunc** especifica la aritmética de píxeles.

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

Especifica cómo se calculan los factores de mezcla de origen rojo, verde, azul y alfa. Se aceptan nueve constantes simbólicas: GL \_ Zero, GL \_ One, GL \_ DST \_ color, GL \_ One \_ menos \_ DST \_ color, GL \_ src \_ Alpha, GL \_ One \_ menos \_ src \_ Alpha, GL \_ DST \_ Alpha, GL \_ One \_ menos \_ DST \_ Alpha y GL \_ src \_ alpha \_ .

</dd> <dt>

*dfactor* 
</dt> <dd>

Especifica cómo se calculan los factores de mezcla de destino rojo, verde, azul y alfa. Se aceptan ocho constantes simbólicas: GL \_ Zero, GL \_ One, GL \_ src \_ color, GL \_ One \_ menos \_ src \_ color, GL \_ src \_ Alpha, GL \_ One \_ menos \_ src \_ Alpha, GL \_ DST \_ Alpha y GL \_ One \_ menos \_ DST \_ Alpha.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | *Sfactor* o *dfactor* no era un valor aceptado.<br/>                                                                   |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

En el modo RGB, los píxeles se pueden dibujar con una función que combina los valores RGBA entrantes (origen) con los valores RGBA que ya están en fotogramas (los valores de destino). De forma predeterminada, la combinación está deshabilitada. Use [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento de la \_ fusión en contab para habilitar y deshabilitar la fusión.

Cuando está habilitada, **glBlendFunc** define la operación de fusión. El parámetro *sfactor* especifica los nueve métodos que se usan para escalar los componentes de color de origen. El parámetro *dfactor* especifica los ocho métodos que se usan para escalar los componentes de color de destino. Los once métodos posibles se describen en la tabla siguiente. Cada método define cuatro factores de escala cada uno para rojo, verde, azul y alfa.

En la tabla y en las ecuaciones subsiguientes, los componentes de color de origen y destino se conocen como (*R*? , *G*? , *B*? , *A*? ) y (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ). Se entiende que tienen valores enteros entre cero y (*k*<sub>r</sub> , *k*<sub>G</sub> , *k*<sub>r</sub> , *k*<sub>A</sub> ), donde

*k*<sub>r</sub> = 2 <sup>m</sup>*r* -1

*k*<sub>g</sub> = 2 <sup>m</sup>*g* -1

*k*<sub>b</sub> = 2 <sup>m</sup>*b* -1

*k*<sub>a</sub> = 2 <sup>m</sup>*a* -1

y (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>A</sub> ) es el número de bitplaness rojo, verde, azul y alfa.

Los factores de escala de origen y destino se conocen como (*s*<sub>r</sub> , *s*<sub>g</sub> , *s*<sub>b</sub> , *s*<sub>a</sub> ) y (*d*<sub>r</sub> , *d*<sub>g</sub> *, d*<sub>b</sub> , *d*<sub>a</sub> ). Los factores de escala descritos en la tabla, que se indican (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ), representan los factores de origen o de destino. Todos los factores de escala tienen el intervalo \[ 0, 1 \] .



| Parámetro                  | (*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GL \_ cero                   | (0, 0, 0, 0)                                                                                                                                                    |
| GL \_ uno                    | (1, 1, 1, 1)                                                                                                                                                    |
| \_color de origen del libro de contabilidad \_             | (*R*? / *k*<sub>R</sub> , *G*? / *k*<sub>G</sub> , *B*? / *k*<sub>B</sub> , *A*? / *k*<sub>A</sub> )                                                         |
| GL \_ uno \_ menos \_ el \_ color src | (1, 1, 1, 1)-(*R*? / *k*<sub>R</sub> , *G*? / *k*<sub>G</sub> , *B*? / *k*<sub>B</sub> , *A*? / *k*<sub>A</sub> )                                             |
| \_color de DST de GL \_             | (*R*<sub>d</sub>  /  *k*<sub>R</sub> , *g*<sub>d</sub>  /  *k*<sub>g</sub> , *b*<sub>d</sub>  /  *k*<sub>b</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )             |
| GL \_ uno \_ menos \_ el \_ color de DST | (1, 1, 1, 1)-(*r*<sub>d</sub>  /  *k*<sub>R</sub> , *g*<sub>d</sub>  /  *k*<sub>g</sub> , *b*<sub>d</sub>  /  *k*<sub>b</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> ) |
| CC \_ src \_ alfa             | (*A*? / *k*<sub>a</sub> , *a*? / *k*<sub>a</sub> , *a*? / *k*<sub>a</sub> , *a*? / *k*<sub>A</sub> )                                                         |
| GL \_ uno \_ menos \_ src \_ Alpha | (1, 1, 1, 1)-(*a*? / *k*<sub>a</sub> , *a*? / *k*<sub>a</sub> , *a*? / *k*<sub>a</sub> , *a*? / *k*<sub>A</sub> )                                             |
| GL \_ DST \_ Alpha             | (*A*<sub>d</sub>  /  *k*<sub>a</sub> , *d*<sub></sub>  /  *k*<sub>a</sub> , <sub>d</sub>  /  *k*<sub>a</sub> , <sub>d</sub>  /  *k*<sub>a</sub> )             |
| GL \_ uno \_ menos \_ DST \_ Alpha | (1, 1, 1, 1)-(*a*<sub>d</sub>  /  *k*<sub>a</sub> , <sub>d</sub>  /  *k*<sub>a</sub> , d <sub></sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> ) |
| libro de contabilidad \_ orig \_ alfa \_ saturado   | (*i* , i, 1)                                                                                                                                                 |



 

En la tabla,

*i* = min (*A*? , *k*<sub>a</sub>   -  <sub>d</sub> )/ *k*<sub>a</sub>

Para determinar los valores RGBA combinados de un píxel al dibujar en el modo RGBA, el sistema usa las ecuaciones siguientes:

*R* (*d*) = mín ( *k*<sub>r</sub> , *r*? *s*<sub>r</sub>  +  <sub>d</sub> *d*<sub>r</sub> )

*G* (*d*) = min ( *k*<sub>g</sub> , *g*? *s*<sub>g</sub>  +  <sub>d</sub> <sub>g</sub> )

*B* (*d*) = min ( *k*<sub>B</sub> *, b*? *s*<sub>b</sub>  +  *b*<sub>d</sub> *d*<sub>b</sub> )

*A* (*d*) = min ( *k*<sub>a</sub> , *a*? *s*<sub>a</sub>  +  <sub>d</sub> *d*<sub>a</sub> )

A pesar de la precisión aparente de las ecuaciones anteriores, la aritmética de mezcla no se especifica exactamente, ya que la mezcla funciona con valores de color enteros imprecisos. Sin embargo, se garantiza que un factor de mezcla que debe ser igual a uno no modifique su multiplicando y un factor de mezcla igual a cero reduce su multiplicando a cero. Por lo tanto, por ejemplo, cuando *sfactor* es GL \_ src \_ Alpha, *dfactor* es GL \_ One \_ menos \_ src \_ Alpha y *a*? es igual a *k* a, las ecuaciones se reducen a <sub>un</sub>reemplazo sencillo:

*R*<sub>d</sub>  =  *r*

*G*<sub>d</sub>  =  *g*

B <sub>d</sub>  =  *b*?

*Una*<sub>d</sub>  =  ?

## <a name="examples"></a>Ejemplos

La transparencia se implementa mejor mediante **glBlendFunc**(GL \_ src \_ Alpha, GL \_ One \_ menos \_ src \_ Alpha) con primitivas ordenadas de más lejos a más próxima. Tenga en cuenta que este cálculo de transparencia no requiere la presencia de alfa bitplanes en fotogramas.

También puede usar **glBlendFunc**(GL \_ src \_ Alpha, GL \_ uno \_ menos \_ src \_ Alpha) para representar puntos y líneas con suavizado de contorno en orden arbitrario.

Para optimizar el suavizado de contorno de polígono, use **glBlendFunc**(GL \_ src \_ alfa \_ Saturate, GL \_ uno) con polígonos ordenados de más cercano a más alejados. (Vea el libro de contabilidad \_ \_Argumento de Polígono suave en [**glEnable**](glenable.md) para obtener información sobre el suavizado de contorno de polígono). Destino Alfa bitplanes, que debe estar presente para que esta función de Blend funcione correctamente, almacene la cobertura acumulada.

El alfa entrante (origen) es una opacidad material, que va desde 1,0 (*K*<sub>a</sub> ), que representa la opacidad completa hasta 0,0 (0), que representa una transparencia completa.

Cuando se habilita más de un búfer de color para dibujar, cada búfer habilitado se mezcla por separado y el contenido del búfer se usa para el color de destino. (Consulte [**glDrawBuffer**](gldrawbuffer.md)).

La mezcla solo afecta a la representación RGBA. Lo omiten los representadores de índice de color.

Las siguientes funciones recuperan información relacionada con **glBlendFunc**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento CC \_ Blend \_ src

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ Blend \_ DST

[**glIsEnabled**](glisenabled.md) con argumento de GL \_ Blend

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

 

 





