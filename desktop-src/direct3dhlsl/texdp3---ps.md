---
title: texdp3-PS
description: Realiza un producto de tres componentes entre los datos del número de registro de textura y el conjunto de coordenadas de textura correspondiente al número de registro de destino.
ms.assetid: 82e02f3f-4b88-4007-b4be-0c66223d9c66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64cc14ee66123ea3e25941579b9838977a753174
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358466"
---
# <a name="texdp3---ps"></a>texdp3-PS

Realiza un producto de tres componentes entre los datos del número de registro de textura y el conjunto de coordenadas de textura correspondiente al número de registro de destino.

## <a name="syntax"></a>Sintaxis



| texdp3 DST, src |
|-----------------|



 

, donde

-   DST es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdp3                |      | x    | x    |      |      |      |       |      |       |



 

Los registros de texturas deben usar la siguiente secuencia.


```
 
tex    t(n)        // Define tn as a standard 3-vector (tn must be 
                   //   defined in some way before texdp3 uses it)
texdp3 t(m), t(n)  // where m > n
                   // Perform a three-component dot product between tn and 
                   //   the texture coordinate set m. The scalar result is
                   //   replicated to all components of t(m)
```



Aquí encontrará más detalles sobre cómo se logra el producto de punto.

La instrucción texdp3 realiza un producto de tres componentes y lo replica en los cuatro canales de color.

t (m)<sub>RGBA</sub> = TextureCoordinates (fase m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




