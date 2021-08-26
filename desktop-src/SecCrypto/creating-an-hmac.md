---
description: Explica cómo crear un HMAC.
ms.assetid: b1747b7e-a505-4b23-93bc-cef4e77bf825
title: Creación de un HMAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb600b00c0bfa3ac8af24cd297b1e2dd67933e2990216dafe84713ee5e831c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876675"
---
# <a name="creating-an-hmac"></a>Creación de un HMAC

**Para calcular un HMAC**

1.  Obtenga un puntero al proveedor de [*servicios criptográficos*](../secgloss/c-gly.md) (CSP) de Microsoft mediante una llamada a [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).
2.  Cree un identificador para un objeto [*hash*](../secgloss/h-gly.md) [*HMAC*](../secgloss/h-gly.md)llamando a [**CryptCreateHash.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) Pase CALG \_ HMAC en el *parámetro Algid.* Pase el identificador de una [*clave simétrica en*](../secgloss/s-gly.md) el *parámetro hKey.* Esta clave simétrica es la clave que se usa para calcular el HMAC.
3.  Especifique el tipo de hash que se va a usar llamando a [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) con el parámetro *dwParam* establecido en el valor HP \_ HMAC \_ INFO. El *parámetro pbData* debe apuntar a una estructura [**info de HMAC \_ inicializada.**](/windows/desktop/api/Wincrypt/ns-wincrypt-hmac_info)
4.  Llame [**a CryptHashData para**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) empezar a calcular el HMAC de los datos. La primera llamada a **CryptHashData hace** que el valor de clave se combine mediante el operador XOR con la cadena interna y los datos. Se aplica un algoritmo hash al resultado de la operación XOR y, a continuación, se aplica un algoritmo hash a los datos de destino del HMAC (a los que apunta el parámetro *pbData* pasado en la llamada a **CryptHashData).** Si es necesario, se pueden realizar llamadas **posteriores a CryptHashData** para finalizar el hash de los datos de destino.
5.  Llame [**a CryptGetHashParam con**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) el parámetro *dwParam* establecido en HP \_ HASHVAL. Esta llamada hace que finalice el hash interno y que la cadena externa se combine mediante XOR con la clave . Se aplica hash al resultado de la operación XOR y, a continuación, se aplica un algoritmo hash al resultado del hash interno (completado en el paso anterior). A continuación, el hash externo finaliza y se devuelve en el *parámetro pbData* y la longitud del *parámetro dwDataLen.*

> [!Note]  
> No use la misma clave [*simétrica*](../secgloss/s-gly.md) [*(sesión)*](../secgloss/s-gly.md)para el cifrado de mensajes y [*la*](../secgloss/m-gly.md) generación de código de autenticación de mensajes (MAC). El uso de la misma clave para ambos aumenta considerablemente el riesgo de que los atacantes descodificaran los mensajes.

 

 

 
