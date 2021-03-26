---
title: texreg2gb-PS
description: Interpreta los componentes de color verde y azul del registro de origen como datos de dirección de textura para muestrear la textura en la fase correspondiente al número de registro de destino.
ms.assetid: 81d3fb3e-ef53-4d25-b65d-c4c9fea0c74c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8d6c428ee5a532919916f0a714db7f81a1c75c12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984006"
---
# <a name="texreg2gb---ps"></a>texreg2gb-PS

Interpreta los componentes de color verde y azul del registro de origen como datos de dirección de textura para muestrear la textura en la fase correspondiente al número de registro de destino.

## <a name="syntax"></a>Sintaxis



| texreg2gb DST, src |
|--------------------|



 

, donde

-   DST es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2gb             |      | x    | x    |      |      |      |       |      |       |



 

Esta instrucción es útil para las operaciones de reasignación de espacio de color.

Este es un ejemplo de la secuencia que sigue la instrucción.

<dl> Tex t (n)  
texreg2gb t (m), t (n), donde m > n  
La primera instrucción carga el color de la textura (RGBA)  
en el registro TN  
Tex TN  
La segunda instrucción reasigna el color  
t (m)<sub>RGBA</sub> = TextureSample (fase m)<sub>RGBA</sub> mediante t (n)<sub>GB</sub> como coordenadas
</dl>

\_no se puede usar BX2 en el registro src para instrucciones [texreg2ar-PS](texreg2ar---ps.md) o texreg2gb.

Para esta instrucción, el registro de origen debe utilizar datos sin firmar. El uso de datos firmados o mixtos en el registro de origen generará resultados indefinidos. Para obtener más información, vea [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 