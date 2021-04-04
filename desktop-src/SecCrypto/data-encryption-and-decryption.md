---
description: El cifrado es el proceso de traducir los datos de texto sin formato (texto simple) en algo que parece ser aleatorio e insignificante (texto cifrado). El descifrado es el proceso de convertir texto cifrado de nuevo en texto sin formato.
ms.assetid: 6a4b5c82-f74c-4cc8-b824-690f165453bd
title: Cifrado y descifrado de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa6f9633cabf4a41aec59d9224c2579acb7a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154083"
---
# <a name="data-encryption-and-decryption"></a>Cifrado y descifrado de datos

El cifrado es el proceso de traducir los datos de texto sin formato ([*texto simple*](../secgloss/p-gly.md)) en algo que parece ser aleatorio e insignificante ([*texto cifrado*](../secgloss/c-gly.md)). El descifrado es el proceso de convertir texto cifrado de nuevo en texto sin formato.

Para cifrar más que una pequeña cantidad de datos, se usa el [*cifrado simétrico*](../secgloss/s-gly.md) . Se utiliza una [*clave simétrica*](../secgloss/s-gly.md) durante los procesos de cifrado y descifrado. Para descifrar un fragmento determinado de texto cifrado, se debe usar la clave utilizada para cifrar los datos.

El objetivo de todos los algoritmos de cifrado es que sea lo más difícil posible para descifrar el texto cifrado generado sin utilizar la clave. Si se usa un algoritmo de cifrado realmente bueno, no hay ninguna técnica significativamente mejor que probar cada clave posible. Para este tipo de algoritmo, cuanto más larga sea la clave, más difícil será descifrar un fragmento de texto sin poseer la clave.

Es difícil determinar la calidad de un algoritmo de cifrado. Los algoritmos que buscan el compromiso a veces resultan muy fáciles de romper, dado el ataque adecuado. Al seleccionar un algoritmo de cifrado, se recomienda elegir uno que se haya usado durante varios años y que se hayan aprovechado correctamente todos los ataques.

Para obtener más información, vea [funciones de cifrado y descifrado de datos](cryptography-functions.md).

 

 
