---
title: gbpreg2gb - ps
description: Interpreta los componentes de color verde y azul del registro de origen como datos de dirección de textura para muestrear la textura en la fase correspondiente al número de registro de destino.
ms.assetid: 81d3fb3e-ef53-4d25-b65d-c4c9fea0c74c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb18a2a79132a08e2659c6df426299ce996beba79566af277500ab9eb0a885f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118505753"
---
# <a name="texreg2gb---ps"></a>gbpreg2gb - ps

Interpreta los componentes de color verde y azul del registro de origen como datos de dirección de textura para muestrear la textura en la fase correspondiente al número de registro de destino.

## <a name="syntax"></a>Syntax



| reg2gb dst, src |
|--------------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| reg2gb             |      | x    | x    |      |      |      |       |      |       |



 

Esta instrucción es útil para las operaciones de remapping de espacio de color.

Este es un ejemplo de la secuencia que sigue la instrucción.

<dl> tex t(n)  
reg2gb t(m), t(n) where m > n  
La primera instrucción carga el color de textura (RGBA)  
en register tn  
texas tn  
La segunda instrucción reasigna el color  
t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>GB</sub> as coordinates
</dl>

\_bx2 no se puede usar en el registro src para las instrucciones [dereg2ar- ps](texreg2ar---ps.md) oreg2gb.

Para esta instrucción, el registro de origen debe usar datos sin signo. El uso de datos firmados o mixtos en el registro de origen producirá resultados indefinidos. Para obtener más información, [vea D3DFORMAT.](/windows/desktop/direct3d9/d3dformat)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 