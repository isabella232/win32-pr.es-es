---
title: Registro de direcciones
description: El registro a0 es un registro de direcciones.
ms.assetid: ad86013c-3358-4770-a01c-544c868691f4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e58f42848034d12063611e14b82cb2f2d132cb43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359336"
---
# <a name="address-register"></a>Registro de direcciones

El registro a0 es un registro de direcciones. Hay un único registro disponible en la versión \_ 1 frente a \_ la 1 1. El registro de direcciones, designado como a0.x en frente \_ a 1 1, se puede usar como desplazamiento entero con signo para el direccionamiento relativo en el archivo \_ de registro constante. En el caso de las versiones 2 0 y posteriores, los cuatro componentes \_ \_ (.x, .y, .z, .w) están disponibles para el direccionamiento relativo.


```
c[a0.x + n]
```



Un sombreador de vértices no puede leer el registro de direcciones, solo se puede usar para el direccionamiento relativo de un registro constante. La lectura de valores fuera del intervalo legal devolverá (0,0, 0,0, 0,0, 0,0). El registro de direcciones solo puede ser un destino para la [instrucción mov - vs.](mov---vs.md) Si un número de punto flotante se mueve a un registro entero, se produce una conversión de ida y vuelta a la más cercana.

Todos los sombreadores deben inicializar el registro de direcciones antes de usarlo. En el caso de la \_ versión \_ 2 0 y posteriores, la instrucción [mova - vs](mova---vs.md) puede mover un valor de punto flotante a un registro de direcciones.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Registro de direcciones       | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




