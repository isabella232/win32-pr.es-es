---
title: Sombreadores de software
description: Los sombreadores de software se implementan para permitir el desarrollo de sombreadores sin soporte de hardware subyacente. Admiten el conjunto completo de características. Dado que se implementan en el software, no producirán el mejor rendimiento.
ms.assetid: 0153732d-a487-473b-ad77-32ab457979f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df101edd0362321847fb9c0baf7feb3cc865e2da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076394"
---
# <a name="software-shaders"></a>Sombreadores de software

Los sombreadores de software se implementan para permitir el desarrollo de sombreadores sin soporte de hardware subyacente. Admiten el conjunto completo de características. Dado que se implementan en el software, no producirán el mejor rendimiento.



| Versión   | Conjunto de características                  | Requisitos                                                         |
|-----------|------------------------------|----------------------------------------------------------------------|
| vs \_ 2 \_ SW | Todas las características de vs \_ 2 \_ x | Solo es compatible con el procesamiento de vértices de software y un dispositivo de referencia. |
| vs \_ 3 \_ SW | Todas las características de vs \_ 3 \_ 0 | Solo es compatible con el procesamiento de vértices de software y un dispositivo de referencia. |
| PS \_ 2 \_ SW | Todas las características de PS \_ 2 \_ x | Solo se admite en un dispositivo de referencia.                                |
| PS \_ 3 \_ SW | Todas las características de PS \_ 3 \_ 0 | Solo se admite en un dispositivo de referencia.                                |



 

Se relajan algunas validaciones para los sombreadores de software. Esto resulta útil para la depuración y la generación de prototipos. Las validaciones siguientes son relajadas: (todas las demás validaciones siguen siendo las mismas)



| Tipo de validación                                 | Flexibiliza                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Recuentos de instrucciones:                             | Esto es flexible para vs \_ 2 \_ SW, vs \_ 3 SW \_ y PS \_ 2 \_ SW, PS \_ 3 \_ SW. Se permiten instrucciones ilimitadas.                                                                                                              |
| Recuentos de constantes float:                          | Esto es flexible para vs \_ 2 \_ SW, vs \_ 3 SW \_ y PS \_ 2 \_ SW, PS \_ 3 \_ SW. Se permiten hasta 8192 constantes.                                                                                                                |
| Recuentos de constantes de enteros:                        | Esto es flexible para vs \_ 2 \_ SW, vs \_ 3 SW \_ y PS \_ 2 \_ SW, PS \_ 3 \_ SW. Se permiten hasta 2048 constantes.                                                                                                                |
| Recuentos de constantes booleanas:                        | Esto es flexible para vs \_ 2 \_ SW, vs \_ 3 SW \_ y PS \_ 2 \_ SW, PS \_ 3 \_ SW. Se permiten hasta 2048 constantes.                                                                                                                |
| Dependiente: profundidad de lectura:                           | Esto es flexible para el \_ SW PS 2 \_ . Al igual que en vs \_ 3 \_ 0 y PS \_ 3 \_ 0, se permiten lecturas dependientes ilimitadas.                                                                                                                |
| Número de instrucciones de control de flujo y etiquetas: | Esto es relajado para vs \_ 2 \_ SW. Instrucciones de control de flujo ilimitado y se permiten las etiquetas 2048.                                                                                                                |
| Recuento de bucles/Inicio/paso:                          | Estos son relajados para vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW y PS \_ 3 \_ SW. El inicio de la iteración y el tamaño del paso de interoperabilidad para instrucciones REP y Loop son intergers con signo de 32 bits. El recuento de interconexiones puede ser hasta el máximo de \_ int/64. |
| Límites de puerto de lectura:                               | vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW y PS \_ 3 \_ SW no tienen límite de puerto de lectura.                                                                                                                                              |
| Número de interpoladores:                        | Hay 16 [registros-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) en vs \_ 3 \_ SW y 10 [PS \_ 3 \_ 0 registros](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# ) para el \_ Software PS 3 \_ .     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia del sombreador de ASM](dx9-graphics-reference-asm.md)
</dt> </dl>

 

 




