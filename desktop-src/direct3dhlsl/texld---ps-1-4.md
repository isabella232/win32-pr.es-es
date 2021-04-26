---
title: 'texld: ps_1_4'
description: Carga el registro de destino con datos de color (RGBA) muestreados utilizando el contenido del registro de origen como coordenadas de textura. La textura muestreada es la textura asociada al número de registro de destino.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca305b16db0f390354962a3e959f08b6e956f2ef
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996872"
---
# <a name="texld---ps_1_4"></a>texld: ps \_ 1 \_ 4

Carga el registro de destino con datos de color (RGBA) muestreados utilizando el contenido del registro de origen como coordenadas de textura. La textura muestreada es la textura asociada al número de registro de destino.



| texld dst, src |
|----------------|



 

## <a name="registers"></a>Registros



|          |                      | Vn        | Cn  | Tn  | Rn  |              |
|----------|----------------------|-----------|-----|-----|-----|--------------|
| dst      | Registro de destino |           |     |     | x   | 1\_4         |
| src      | Registro de origen      |           |     | x   |     | 1 \_ 4 fase 1 |
|          |                      |           |     | x   | x   | 1 \_ fase 4   |



 

Cuando se usa r(n) como registro de origen, los tres primeros componentes (XYZ) se deben haber inicializado en la fase anterior del sombreador.

Para obtener más información sobre los registros, [vea ps \_ \_ 1 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Comentarios

Esta instrucción muestrea la textura en la fase de textura asociada al número de registro de destino. La textura se muestrea mediante datos de coordenadas de textura del registro de origen.

La sintaxis de las instrucciones texld y texcrd expone compatibilidad con una división projective con un modificador de registro de textura. Para la versión 1.4 del sombreador de píxeles, la marca de transformación de textura PROJECTED de D3DTTFF \_ siempre se omite.

Reglas para usar texld:

1.  El mismo modificador .xyz o .xyw debe aplicarse a cada lectura de un registro t(n) individual dentro de las instrucciones de texcrd o texld. Si se usa .xyw en lecturas de registro t(n), se puede mezclar con otras lecturas del mismo registro t(n) mediante .xyw \_ dw.
2.  El modificador de origen de tipo así solo es válido en el registro de origen \_ r(n) (por lo tanto, solo en la fase 2).
3.  El \_ modificador de origen de color no se puede usar más de dos veces por sombreador.



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texld                 |      |      |      | x    |      |      |       |      |       |



 

## <a name="examples"></a>Ejemplos

La instrucción texld ofrece cierto control sobre qué componentes de los datos de coordenadas de textura de origen se usan. El conjunto completo de sintaxis permitida para texld sigue e incluye todos los modificadores de registro de origen, selectores y combinaciones de máscara de escritura válidos.


```
texld  r(m), t(n).xyz
// Uses xyz from t(n) to sample 1D, 2D, or 3D texture
```




```
texld  r(m), t(n)
// Same as previous
```




```
texld  r(m), t(n).xyw
// Uses xyw (skipping z) from t(n) to sample 1D, 2D or 3D texture
```




```
texld  r(m), t(n)_dw.xyw  
// Samples 1D or 2D texture at x/w, y/w from t(n). The result
// is undefined for a cube-map lookup.
```




```
texld  r(m), r(n).xyz
// Samples 1D, 2D, or 3D texture at xyz from r(m) 
// This is possible in the second phase of the shader
```




```
texld  r(m), r(n)
// Same as previous
```




```
texld  r(m), r(n)_dz.xyz
// Samples 1D or 2D texture at x/z, y/z from r(m)
// Possible only in second phase
// The result is undefined for a cube-map lookup
```




```
texld  r(n), r(n)_dz
// Same as previous
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




