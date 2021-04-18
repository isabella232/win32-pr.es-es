---
description: Explica cómo crear un HMAC.
ms.assetid: b1747b7e-a505-4b23-93bc-cef4e77bf825
title: Crear un HMAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364314081bd1d84d6d9bfff889c234470cc6775c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667715"
---
# <a name="creating-an-hmac"></a>Crear un HMAC

**Para calcular un HMAC**

1.  Obtener un puntero al proveedor de [*servicios criptográficos*](../secgloss/c-gly.md) (CSP) de Microsoft llamando a [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).
2.  Cree un identificador para un [](../secgloss/h-gly.md)[*objeto hash*](../secgloss/h-gly.md) HMAC llamando a [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash). Pase CALG \_ HMAC en el parámetro *algid* . Pase el identificador de una [*clave simétrica*](../secgloss/s-gly.md) en el parámetro *hKey* . Esta clave simétrica es la clave utilizada para calcular el HMAC.
3.  Especifique el tipo de hash que se va a usar mediante una llamada a [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) con el parámetro *dwParam* establecido en el valor HP \_ HMAC \_ info. El parámetro *pbData* debe apuntar a una estructura [**de \_ información HMAC**](/windows/desktop/api/Wincrypt/ns-wincrypt-hmac_info) inicializada.
4.  Llame a [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) para empezar a calcular el HMAC de los datos. La primera llamada a **CryptHashData** hace que el valor de clave se combine mediante el operador XOR con la cadena interna y los datos. Se aplica un algoritmo hash al resultado de la operación XOR y, a continuación, se aplica un algoritmo hash a los datos de destino del HMAC (al que apunta el parámetro *pbData* que se pasa en la llamada a **CryptHashData**). En caso necesario, se pueden realizar llamadas subsiguientes a **CryptHashData** para finalizar el hash de los datos de destino.
5.  Llame a [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) con el parámetro *DWPARAM* establecido en HP \_ HASHVAL. Esta llamada hace que se complete el hash interno y la cadena externa se combine con XOR con la clave. Se aplica un algoritmo hash al resultado de la operación XOR y, a continuación, se aplica un algoritmo hash al resultado del hash interno (completado en el paso anterior). Después, el hash externo se completa y se devuelve en el parámetro *pbData* y la longitud en el parámetro *dwDataLen* .

> [!Note]  
> No use la misma clave [*simétrica*](../secgloss/s-gly.md) ([*sesión*](../secgloss/s-gly.md)) para la generación de cifrado de mensajes y [*código de autentificación de mensajes (Mac)*](../secgloss/m-gly.md) (Mac). El uso de la misma clave para aumenta en gran medida el riesgo de que los atacantes descodifiquen los mensajes.

 

 

 
