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
ms.openlocfilehash: 73ea16c5aa6b49bce59fe51905734344e4e1cffb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264020"
---
# <a name="input-color-register"></a>Registro de color de entrada

Registro de entrada del sombreador de píxeles que contiene el color del vértice.

## <a name="syntax"></a>Sintaxis


```
dcl v#.writeMask
```



donde:

-   [dcl - (sm2, sm3 - ps asm)](dcl---ps.md) es una instrucción de declaración de registro.
-   v es un registro de entrada y \# es el número de registro. El número de registros permitidos viene determinado por la versión del sombreador.
-   writeMask determina qué componentes (hasta cuatro) se escriben. Los componentes válidos son: (x,y,z,w) o (r,g,b,a).

## <a name="remarks"></a>Observaciones

Los registros de color son registros de solo lectura. Cada registro contiene valores RGBA de cuatro componentes iterados a partir de vértices de entrada. Tienen una precisión menor que la mayoría de los registros, con la garantía de tener 8 bits de datos sin signo en el intervalo (0, +1). No se puede usar más de uno en una sola instrucción.

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

 

 




