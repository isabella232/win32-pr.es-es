---
title: Registro de color de entrada
description: Registro de entrada del sombreador de píxeles que contiene el color del vértice.
ms.assetid: d2e21f87-000e-410a-aaba-172000ed1c5f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fcabc6dcf5043c23be252fe6ac25c99da505e33b7c670c95ee5672b50ddb74bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744635"
---
# <a name="input-color-register"></a>Registro de color de entrada

Registro de entrada del sombreador de píxeles que contiene el color del vértice.

## <a name="syntax"></a>Syntax


```
dcl v#.writeMask
```



donde:

-   [dcl - (sm2, sm3 - ps asm)](dcl---ps.md) es una instrucción de declaración de registro.
-   v es un registro de entrada y \# es el número de registro. El número de registros permitidos viene determinado por la versión del sombreador.
-   writeMask determina qué componentes (hasta cuatro) se escriben. Los componentes válidos son: (x,y,z,w) o (r,g,b,a).

## <a name="remarks"></a>Comentarios

Los registros de color son registros de solo lectura. Cada registro contiene valores RGBA de cuatro componentes iterados a partir de los vértices de entrada. Tienen una precisión menor que la mayoría de los registros, con la garantía de tener 8 bits de datos sin signo en el intervalo (0, +1). No se puede usar más de uno en una sola instrucción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[ps \_ 2 \_ 0 Registros](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[ps \_ 2 \_ x Registros](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[ps \_ 3 \_ 0 Registros](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




