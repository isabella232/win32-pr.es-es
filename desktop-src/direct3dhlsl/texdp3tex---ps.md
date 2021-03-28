---
title: texdp3tex-PS
description: Realiza un producto de tres componentes y usa el resultado para realizar una búsqueda de texturas 1D.
ms.assetid: vs|directx_sdk|~\texdp3tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dfe74dd0a73bc47cd2855d35b239e80a1b5153c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996856"
---
# <a name="texdp3tex---ps"></a>texdp3tex-PS

Realiza un producto de tres componentes y usa el resultado para realizar una búsqueda de texturas 1D.

## <a name="syntax"></a>Sintaxis



| texdp3tex DST, src |
|--------------------|



 

, donde

-   DST es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdp3tex             |      | x    | x    |      |      |      |       |      |       |



 

Los registros de texturas deben usar la siguiente secuencia.


```
 
tex       t(n)        // Define tn as a standard 3-vector (tn must be 
                      // defined in some way before texdp3tex uses it)
texdp3tex t(m), t(n)  // where m > n                 
                      // Perform a three-component dot product between t(n) and 
                      // the texture coordinate set m. Use the scalar result to
                      // do a 1D texture lookup at texturestage m and place
                      // the result in t(m)
```



Aquí encontrará más detalles sobre cómo se realiza la búsqueda de productos y texturas de punto.

La instrucción texdp3tex realiza un producto de tres componentes.

u ' = TextureCoordinates (Stage m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

El resultado se usa para el muestreo de la textura en la fase de textura m mediante la realización de una búsqueda 1D.

t (m)<sub>RGBA</sub> = TextureSample (fase m)<sub>RGBA</sub> mediante (u ', 0,0) como coordenadas

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




