---
title: texreg2rgb-PS
description: Interpreta los componentes de color rojo, verde y azul (RGB) del registro de origen como datos de dirección de textura para que muestren la textura en la fase correspondiente al número de registro de destino. El resultado se almacena en el registro de destino.
ms.assetid: 8ec44014-d796-407c-8fe0-036decaf2a3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8bcd2bbd7e57ba9dc692f34404a5610cdc517f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532878"
---
# <a name="texreg2rgb---ps"></a>texreg2rgb-PS

Interpreta los componentes de color rojo, verde y azul (RGB) del registro de origen como datos de dirección de textura para que muestren la textura en la fase correspondiente al número de registro de destino. El resultado se almacena en el registro de destino.

## <a name="syntax"></a>Sintaxis



| texreg2rgb DST, src |
|---------------------|



 

, donde

-   DST es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2rgb            |      | x    | x    |      |      |      |       |      |       |



 

Esta instrucción es útil para las operaciones de reasignación de espacio de color. Admite coordenadas bidimensionales (2D) y tridimensionales (3D). Se puede usar del mismo modo que [texreg2ar-PS](texreg2ar---ps.md) o [texreg2gb-PS](texreg2gb---ps.md) para reasignar datos 2D. Sin embargo, esta instrucción también admite datos 3D, por lo que se puede usar con mapas de cubos y texturas de volumen 3D.

Este es un ejemplo de la secuencia que sigue la instrucción.


```
 
tex t(n)
texreg2rgb t(m), t(n)     where m > n
```



Aquí encontrará más detalles sobre cómo se realiza la reasignación.

<dl> La primera instrucción carga el color de textura (RGBA) en el registro TN  
Tex TN  
La segunda instrucción reasigna el color  
t (m)<sub>RGBA</sub> = TextureSample (fase m)<sub>RGBA</sub> mediante t (n)<sub>RGB</sub> como coordenadas
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




