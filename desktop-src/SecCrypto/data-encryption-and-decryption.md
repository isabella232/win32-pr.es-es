---
description: El cifrado es el proceso de traducir datos de texto sin formato (texto no cifrado) en algo que parece aleatorio y sin sentido (texto cifrado). El descifrado es el proceso de volver a convertir texto cifrado en texto no cifrado.
ms.assetid: 6a4b5c82-f74c-4cc8-b824-690f165453bd
title: Cifrado y descifrado de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba508eeb67570d1f293ae55e1b6bff5217529663a6682a17d9817a9dc0834803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100915"
---
# <a name="data-encryption-and-decryption"></a>Cifrado y descifrado de datos

El cifrado es el proceso de traducir datos de texto sin formato [*(texto*](../secgloss/p-gly.md)no cifrado) en algo que parece aleatorio y sin sentido [*(texto cifrado*](../secgloss/c-gly.md)). El descifrado es el proceso de volver a convertir texto cifrado en texto no cifrado.

Para cifrar más de una pequeña cantidad de datos, [*se usa el cifrado*](../secgloss/s-gly.md) simétrico. Durante [*los procesos de*](../secgloss/s-gly.md) cifrado y descifrado se usa una clave simétrica. Para descifrar un fragmento determinado de texto cifrado, se debe usar la clave que se usó para cifrar los datos.

El objetivo de cada algoritmo de cifrado es hacer que sea lo más difícil posible descifrar el texto cifrado generado sin usar la clave . Si se usa un algoritmo de cifrado realmente bueno, no hay ninguna técnica significativamente mejor que probar metódicomente todas las claves posibles. Para este algoritmo, cuanto más larga sea la clave, más difícil es descifrar un fragmento de texto cifrado sin poseer la clave.

Es difícil determinar la calidad de un algoritmo de cifrado. A veces, los algoritmos que parecen ser pringentas son muy fáciles de interrumpir, dado el ataque adecuado. Al seleccionar un algoritmo de cifrado, es una buena idea elegir uno que haya estado en uso durante varios años y que haya resistido correctamente todos los ataques.

Para obtener más información, vea [Funciones de cifrado y descifrado de datos](cryptography-functions.md).

 

 
