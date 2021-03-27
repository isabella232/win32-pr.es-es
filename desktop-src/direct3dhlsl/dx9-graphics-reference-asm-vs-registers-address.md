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
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903693"
---
# <a name="address-register"></a>Registro de direcciones

El registro a0 es un registro de direcciones. Un único registro está disponible en la versión vs \_ 1 \_ 1. El registro de dirección, designado como a0. x en vs \_ 1 \_ 1, se puede usar como desplazamiento de entero con signo para el direccionamiento relativo en el archivo de registro de constantes. En el caso de las versiones de vs \_ 2 \_ 0 y posteriores, los cuatro componentes (. x,. y,. z,. w) están disponibles para el direccionamiento relativo.


```
c[a0.x + n]
```



Un sombreador de vértices no puede leer el registro de direcciones, solo se puede usar para el direccionamiento relativo de un registro de constantes. La lectura de valores fuera del intervalo legal devolverá (0,0, 0,0, 0,0, 0,0). El registro de dirección solo puede ser un destino para la instrucción [MOV-vs](mov---vs.md) . Si un número de punto flotante se mueve a un registro entero, se produce una conversión de ida a vuelta más cercana.

Todos los sombreadores deben inicializar el registro de direcciones antes de usarlo. En el caso de la versión de vs \_ 2 \_ 0 y versiones posteriores, la instrucción [mova-vs](mova---vs.md) puede trasladar un valor de punto flotante a un registro de direcciones.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro de direcciones       | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




