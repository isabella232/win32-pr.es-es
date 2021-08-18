---
title: dp3tex- ps
description: Realiza un producto de puntos de tres componentes y usa el resultado para realizar una búsqueda de textura 1D.
ms.assetid: vs|directx_sdk|~\texdp3tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91014b52b04417bbb23e76988beeb0bd4c473bd1e1d116433a8fd1dbf09a47ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788041"
---
# <a name="texdp3tex---ps"></a>dp3tex- ps

Realiza un producto de puntos de tres componentes y usa el resultado para realizar una búsqueda de textura 1D.

## <a name="syntax"></a>Syntax



| dp3tex dst, src |
|--------------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp3tex             |      | x    | x    |      |      |      |       |      |       |



 

Los registros de textura deben usar la secuencia siguiente.


```
 
tex       t(n)        // Define tn as a standard 3-vector (tn must be 
                      // defined in some way before texdp3tex uses it)
texdp3tex t(m), t(n)  // where m > n                 
                      // Perform a three-component dot product between t(n) and 
                      // the texture coordinate set m. Use the scalar result to
                      // do a 1D texture lookup at texturestage m and place
                      // the result in t(m)
```



Este es un detalle más detallado sobre cómo se realizan las búsquedas de producto de punto y textura.

La instrucción texdp3tex realiza un producto de punto de tres componentes.

u' = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

El resultado se usa para muestrear la textura en la fase de textura m realizando una búsqueda 1D.

t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using (u',0,0) as coordinates

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




