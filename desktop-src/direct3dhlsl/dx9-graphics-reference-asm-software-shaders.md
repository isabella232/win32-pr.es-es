---
title: Sombreadores de software
description: Los sombreadores de software se implementan para permitir el desarrollo de sombreadores sin compatibilidad con hardware subyacente. Admiten el conjunto de características completo. Dado que se implementan en software, no producirán el mejor rendimiento.
ms.assetid: 0153732d-a487-473b-ad77-32ab457979f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36676517a1979c2bd876ad3afdb84e83d596322f25015ac2cd934d48f23c5b33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949985"
---
# <a name="software-shaders"></a>Sombreadores de software

Los sombreadores de software se implementan para permitir el desarrollo de sombreadores sin compatibilidad con hardware subyacente. Admiten el conjunto de características completo. Dado que se implementan en software, no producirán el mejor rendimiento.



| Versión   | Conjunto de características                  | Requisitos                                                         |
|-----------|------------------------------|----------------------------------------------------------------------|
| vs \_ 2 \_ sw | Todas las características de frente \_ a 2 \_ x | Solo es compatible con el procesamiento de vértices de software y un dispositivo de referencia. |
| vs \_ 3 \_ sw | Todas las características de frente \_ a 3 \_ 0 | Solo es compatible con el procesamiento de vértices de software y un dispositivo de referencia. |
| ps \_ 2 \_ sw | Todas las características de ps \_ 2 \_ x | Solo es compatible con un dispositivo de referencia.                                |
| ps \_ 3 \_ sw | Todas las características de ps \_ 3 \_ 0 | Solo es compatible con un dispositivo de referencia.                                |



 

Algunas validaciones son relajadas para los sombreadores de software. Esto es útil para fines de depuración y creación de prototipos. Las validaciones siguientes son relajadas: (todas las demás validaciones siguen siendo las mismas)



| Tipo de validación                                 | Relajación                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Recuentos de instrucciones:                             | Esto es relajada para vs \_ 2 \_ sw, vs \_ 3 \_ sw y ps \_ 2 \_ sw, ps \_ 3 \_ sw. Se permiten instrucciones ilimitadas.                                                                                                              |
| Recuentos de constantes float:                          | Esto es relajada para vs \_ 2 \_ sw, vs \_ 3 \_ sw y ps \_ 2 \_ sw, ps \_ 3 \_ sw. Se permiten hasta 8192 constantes.                                                                                                                |
| Recuentos constantes enteros:                        | Esto es relajada para vs \_ 2 \_ sw, vs \_ 3 \_ sw y ps \_ 2 \_ sw, ps \_ 3 \_ sw. Se permiten hasta 2048 constantes.                                                                                                                |
| Recuentos de constantes booleanos:                        | Esto es relajada para vs \_ 2 \_ sw, vs \_ 3 \_ sw y ps \_ 2 \_ sw, ps \_ 3 \_ sw. Se permiten hasta 2048 constantes.                                                                                                                |
| Profundidad de lectura dependiente:                           | Esto es relajada para ps \_ 2 \_ sw. Al igual que \_ en vs 3 \_ 0 y ps \_ 3 \_ 0, se permiten lecturas dependientes ilimitadas.                                                                                                                |
| Número de instrucciones y etiquetas de control de flujo: | Esto es relajada para vs \_ 2 \_ sw. Se permiten instrucciones de control de flujo ilimitadas y hasta 2048 etiquetas.                                                                                                                |
| Recuento de bucles/inicio/paso:                          | Son relajadas para vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw y ps \_ 3 \_ sw. El tamaño del paso de inicio e intercalación de iteración para las instrucciones de repetición y bucle son intercaladores con firma de 32 bits. El recuento de interaciones puede ser de hasta MAX \_ INT/64. |
| Límites de puerto de lectura:                               | frente \_ a 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 sw y ps \_ \_ 3 sw no tienen límite de puerto \_ de lectura.                                                                                                                                              |
| Número de interpoladores:                        | Hay 16 registros, frente [ \_ a 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o ) en vs 3 sw y \# \_ \_ 10 [ps \_ 3 \_ 0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# ) para ps \_ 3 \_ sw.     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de sombreador de Asm](dx9-graphics-reference-asm.md)
</dt> </dl>

 

 




