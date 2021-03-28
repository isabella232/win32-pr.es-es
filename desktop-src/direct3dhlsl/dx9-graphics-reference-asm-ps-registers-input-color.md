---
title: Registro del color de entrada
description: Registro de entrada del sombreador de píxeles que contiene el color del vértice.
ms.assetid: d2e21f87-000e-410a-aaba-172000ed1c5f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73ea16c5aa6b49bce59fe51905734344e4e1cffb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419186"
---
# <a name="input-color-register"></a>Registro del color de entrada

Registro de entrada del sombreador de píxeles que contiene el color del vértice.

## <a name="syntax"></a>Sintaxis


```
dcl v#.writeMask
```



donde:

-   [DCL: (SM2, SM3-PS ASM)](dcl---ps.md) es una instrucción de declaración de registro.
-   v es un registro de entrada y \# es el número de registro. El número de registros permitidos viene determinado por la versión del sombreador.
-   writeMask determina qué componentes (hasta cuatro) están escritos. Los componentes válidos son: (x, y, z, w) o (r, g, b, a).

## <a name="remarks"></a>Observaciones

Los registros de color son registros de solo lectura. Cada registro contiene valores RGBA de cuatro componentes que se iteran desde los vértices de entrada. Tienen una precisión menor que la mayoría de los registros, se garantiza que tienen 8 bits de datos sin signo en el intervalo (0, + 1). No se puede usar más de una en una sola instrucción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registra](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[Registros de PS \_ 2 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[Registros de PS \_ 2 \_ x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[Registros de PS \_ 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




