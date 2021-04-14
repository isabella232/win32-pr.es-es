---
title: texcrd-PS
description: Copia los datos de coordenadas de textura del iterador de la coordenada de textura de origen como datos de color en el registro de destino.
ms.assetid: b3330d70-6e18-4494-a01c-51f0a282e305
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1b7bda7ab06c4af43eaa40393d2c5d64b09d9f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997068"
---
# <a name="texcrd---ps"></a>texcrd-PS

Copia los datos de coordenadas de textura del iterador de la coordenada de textura de origen como datos de color en el registro de destino.

## <a name="syntax"></a>Sintaxis



| texcrd DST, src |
|-----------------|



 

, donde

-   DST es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texcrd                |      |      |      | x    |      |      |       |      |       |



 

Esta instrucción interpreta los datos de coordenadas como datos de color (RGBA).

Esta instrucción no muestrea ninguna textura. Solo se aplican las coordenadas de textura establecidas en esta fase de textura.

Al utilizar texcrd, tenga en cuenta los siguientes detalles sobre cómo se copian los datos del registro de origen en el registro de destino. El registro de coordenadas de textura de origen (t \# ) contiene datos en el intervalo \[ -D3DCAPS9. MaxTextureRepeat, D3DCAPS9. MaxTextureRepeat \] , mientras que el registro de destino (r \# ) solo puede contener datos en el intervalo de D3DCAPS9 (probablemente más pequeño) \[ . PixelShader1xMaxValue, D3DCAPS9. PixelShader1xMaxValue \] . Tenga en cuenta que para el sombreador de píxeles versión 1 \_ 4, D3DCAPS9. PixelShader1xMaxValue debe tener un mínimo de ocho. La instrucción texcrd, en el proceso de compresión de datos de origen que está fuera del intervalo del registro de destino, es probable que se comporte de forma diferente en hardware diferente. El primer hardware del sombreador de píxeles versión 1 \_ 4 en el mercado llevará a cabo una abrazadera especial para los valores fuera del intervalo. Esta abrazadera está diseñada para generar un número que puede caber en el registro de destino, pero también para conservar el comportamiento del direccionamiento de texturas para los datos fuera del intervalo (vea [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) si los datos se van a usar posteriormente para el muestreo de textura. Sin embargo, es posible que el nuevo hardware de distintos fabricantes no muestre este comportamiento y que simplemente Chop los datos para que se ajusten al intervalo de registro de destino. Por lo tanto, el curso de acción más seguro al usar el sombreador de píxeles versión 1 \_ 4 texcrd es proporcionar datos de coordenadas de textura solo en el sombreador de píxeles que ya está dentro del intervalo \[ -8, 8 \] para que no se base en la forma en que se fija el hardware.

A diferencia \_ de texcoord, texcrd no fija valores entre 0 y 1.

Reglas para usar texcrd:

1.  Se debe aplicar el mismo modificador. XYZ o. xyw a cada lectura de un registro t (n) individual dentro de una instrucción texcrd o texld.
2.  El resultado del cuarto canal de texcrd es unset/undefined en todos los casos.
3.  El tercer canal no está establecido o no está definido para el caso de almacenamiento de xyw \_ .

## <a name="examples"></a>Ejemplos

A continuación se muestra el conjunto completo de sintaxis permitida para texcrd, teniendo en cuenta todas las combinaciones válidas de modificador/selector de origen y máscara de escritura de destino. Tenga en cuenta que la notación. RGBA y. xyzw se puede usar indistintamente.

Copia los tres primeros canales de un iterador de la coordenada de textura Register, t (n), en r (m). El cuarto canal de r (m) no está inicializado.


```
texcrd  r(m).rgb, t(n).xyz  

// Produces the same result as the previous instruction
texcrd  r(m).rgb, t(n)
```



Coloca los componentes primero, segundo y cuarto de t (n) en los primeros tres canales de r (m). El cuarto canal de r (m) no está inicializado.


```
texcrd  r(m).rgb, t(n).xyw
```



Este es un ejemplo de división proyectada mediante el \_ modificador DW.

Este ejemplo copia x/w e y/w de t (n) en los dos primeros canales de r (m). Los canales tercero y cuarto de r (m) no están inicializados. Se perderán los datos escritos previamente en el tercer canal de r (m). Los datos del cuarto canal de r (m) se pierden debido al marcador de fase. En el caso de \_ la versión 4, \_ se omite la marca proyectada D3DTTFF.


```
texcrd  r(m).rg,  t(n)_dw.xyw
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 