---
title: texld-ps_1_4
description: Carga el ejemplo de registro de destino con datos de color (RGBA) mediante el contenido del registro de origen como coordenadas de textura. La textura muestreada es la textura asociada al número de registro de destino.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 23827dffc396a40be134be4db3996d2e9f498288
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996940"
---
# <a name="texld---ps_1_4"></a>texld-PS \_ 1 \_ 4

Carga el ejemplo de registro de destino con datos de color (RGBA) mediante el contenido del registro de origen como coordenadas de textura. La textura muestreada es la textura asociada al número de registro de destino.



| texld DST, src |
|----------------|



 

## <a name="registers"></a>Registros



| Argumento | Descripción          | Registros |     |     |     | Versión      |
|----------|----------------------|-----------|-----|-----|-----|--------------|
|          |                      | vn        | CN  | TN  | RN  |              |
| DST      | Registro de destino |           |     |     | x   | 1\_4         |
| src      | Registro de origen      |           |     | x   |     | 1 \_ 4 fase 1 |
|          |                      |           |     | x   | x   | 1 \_ 4 fase   |



 

Al usar r (n) como registro de origen, los tres primeros componentes (XYZ) deben haberse inicializado en la fase anterior del sombreador.

Para obtener más información acerca de los registros, consulte [PS 1 \_ \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Observaciones

Esta instrucción muestrea la textura en la fase de textura asociada al número de registro de destino. La textura se muestrea utilizando los datos de coordenadas de textura del registro de origen.

La sintaxis de las instrucciones texld y texcrd expone la compatibilidad con una división proyectada con un modificador de registro de textura. Para el sombreador de píxeles versión 1,4, la \_ marca de transformación de textura proyectada D3DTTFF siempre se omite.

Reglas para usar texld:

1.  Se debe aplicar el mismo modificador. XYZ o. xyw a cada lectura de un registro t (n) individual en las instrucciones texcrd o texld. Si se usa. xyw en las lecturas de registro t (n), esto se puede mezclar con otras lecturas del mismo registro t (n) mediante el almacenamiento de xyw. \_
2.  El \_ modificador de origen DZ solo es válido en texld con el registro de origen r (n) (solo en la fase 2).
3.  El \_ modificador de origen DZ no se puede usar más de dos veces por sombreador.



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texld                 |      |      |      | x    |      |      |       |      |       |



 

## <a name="examples"></a>Ejemplos

La instrucción texld ofrece cierto control sobre qué componentes de los datos de coordenadas de textura de origen se usan. A continuación se muestra el conjunto completo de sintaxis permitida para texld e incluye todos los modificadores de registro de origen válidos, selectores y combinaciones de máscara de escritura.


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

 

 




