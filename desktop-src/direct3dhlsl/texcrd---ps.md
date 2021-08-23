---
title: texcrd - ps
description: Copia los datos de coordenadas de textura del registro del iterador de coordenadas de textura de origen como datos de color en el registro de destino.
ms.assetid: b3330d70-6e18-4494-a01c-51f0a282e305
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 795dacbec01abdfa49527e36fefc9194a6168a99c1d9ab425b30f987e5445096
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118506431"
---
# <a name="texcrd---ps"></a>texcrd - ps

Copia los datos de coordenadas de textura del registro del iterador de coordenadas de textura de origen como datos de color en el registro de destino.

## <a name="syntax"></a>Syntax



| texcrd dst, src |
|-----------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texcrd                |      |      |      | x    |      |      |       |      |       |



 

Esta instrucción interpreta los datos de coordenadas como datos de color (RGBA).

Esta instrucción no muestrea ninguna textura. Solo son pertinentes las coordenadas de textura establecidas en esta fase de textura.

Al usar texcrd, tenga en cuenta los siguientes detalles sobre cómo se copian los datos del registro de origen al registro de destino. El registro de coordenadas de textura de origen (t ) contiene \# datos en el intervalo \[ -D3DCAPS9. MaxTextureRepeat, D3DCAPS9. MaxTextureRepeat , mientras que el registro de destino (r ) solo puede contener datos en el \] \# intervalo (probablemente más pequeño) \[ -D3DCAPS9. PixelShader1xMaxValue, D3DCAPS9. PixelShader1xMaxValue \] . Tenga en cuenta que para el sombreador de píxeles versión 1 \_ 4, D3DCAPS9. PixelShader1xMaxValue debe ser un mínimo de ocho. La instrucción texcrd, en el proceso de fijación de datos de origen que está fuera del intervalo del registro de destino, es probable que se comporte de forma diferente en hardware diferente. El primer hardware de sombreador de píxeles versión 1 4 del mercado realizará una fijación especial para \_ los valores fuera del intervalo. Esta fijación está diseñada para generar un número que pueda caber en el registro de destino, pero también para conservar el comportamiento de direccionamiento de textura para los datos fuera del intervalo (consulte [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) si los datos se usarían posteriormente para el muestreo de textura. Sin embargo, es posible que el nuevo hardware de distintos fabricantes no expondrá este comportamiento y podría simplemente ajustar los datos para ajustarse al intervalo de registro de destino. Por lo tanto, el curso de acción más seguro al usar la versión 1 4 del sombreador de píxeles es proporcionar datos de coordenadas de textura solo en el sombreador de píxeles que ya está dentro del intervalo \_ \[ -8,8 para que no se base en la forma en que se fija el \] hardware.

A diferencia de texcoord, \_ texcrd no fija valores entre 0 y 1.

Reglas para usar texcrd:

1.  Se debe aplicar el mismo modificador .xyz o .xyw a cada lectura de un registro t(n) individual dentro de una instrucción texcrd old.
2.  El cuarto resultado del canal de texcrd es unset/undefined en todos los casos.
3.  El tercer canal no está establecido o no está definido para el caso xyw \_ dw.

## <a name="examples"></a>Ejemplos

A continuación se muestra el conjunto completo de sintaxis permitida para texcrd, teniendo en cuenta todas las combinaciones válidas de modificador/selector de origen y máscara de escritura de destino. Tenga en cuenta que la notación .rgba y .xyzw se puede usar indistintamente.

Copia los tres primeros canales del registro del iterador de coordenadas de textura, t(n), en r(m). El cuarto canal de r(m) no está inicializado.


```
texcrd  r(m).rgb, t(n).xyz  

// Produces the same result as the previous instruction
texcrd  r(m).rgb, t(n)
```



Coloca los componentes first, second y fourth de t(n) en los tres primeros canales de r(m). El cuarto canal de r(m) no está inicializado.


```
texcrd  r(m).rgb, t(n).xyw
```



Este es un ejemplo de división projective mediante el \_ modificador dw.

En este ejemplo se copian x/w e y/w de t(n) en los dos primeros canales de r(m). Los canales tercero y cuarto de r(m) no están inicializados. Se perderán los datos escritos previamente en el tercer canal de r(m). Los datos del cuarto canal de r(m) se pierden debido al marcador de fase. Para la versión 1 4, se omite la marca \_ D3DTTFF \_ PROJECTED.


```
texcrd  r(m).rg,  t(n)_dw.xyw
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 