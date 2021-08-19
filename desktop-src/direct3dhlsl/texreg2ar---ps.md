---
title: texreg2ar - ps
description: Interpreta los componentes de color alfa y rojo del registro de origen como datos de dirección de textura (u,v) para muestrear la textura en la fase correspondiente al número de registro de destino. El resultado se almacena en el registro de destino.
ms.assetid: b31a2ee4-f9b9-4aee-b3be-7ccc5b8c6f3e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee9516c43f5e8d774ef496a0e66ae1a8ee839ff3df6f2f5436caaf887f95da54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118284006"
---
# <a name="texreg2ar---ps"></a>texreg2ar - ps

Interpreta los componentes de color alfa y rojo del registro de origen como datos de dirección de textura (u,v) para muestrear la textura en la fase correspondiente al número de registro de destino. El resultado se almacena en el registro de destino.

## <a name="syntax"></a>Syntax



| texreg2ar dst, src |
|--------------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2ar             | x    | x    | x    |      |      |      |       |      |       |



 

Esta instrucción es útil para las operaciones de remapping de espacio de color.

Este es un ejemplo de la secuencia que sigue la instrucción:

<dl> tex t(n)  
texreg2ar t(m), t(n) where m > n  
La primera instrucción carga el color de textura (RGBA)  
en register tn  
tex tn  
La segunda instrucción reasigna el color  
t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>AR</sub> as coordinates
</dl>

\_bx2 no se puede usar en el registro src para las instrucciones texreg2ar o [texreg2gb- ps.](texreg2gb---ps.md)

Para esta instrucción, el registro de origen debe usar datos sin signo. El uso de datos firmados o mixtos en el registro de origen producirá resultados no definidos. Para obtener más información, [vea D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 