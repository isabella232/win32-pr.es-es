---
description: Estos pasos comprueban la firma de datos firmados.
ms.assetid: 18246cc1-d3c4-4426-a342-ce3864cc412e
title: Comprobación de un mensaje firmado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f85a5bcde56df7bb41bb92276123bcd26024e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668478"
---
# <a name="verifying-a-signed-message"></a>Comprobación de un mensaje firmado

Estos pasos comprueban la firma de datos firmados. En la ilustración siguiente se muestran las tareas individuales que se deben realizar, tal y como se muestra en la lista siguiente.

![comprobación de un mensaje firmado](images/verifmsg.png)

**Para comprobar la firma de un mensaje firmado**

1.  Obtiene un puntero al mensaje firmado.
2.  Abra un [*almacén de certificados*](../secgloss/c-gly.md).
3.  Con el identificador de firmante incluido en el mensaje, obtenga el certificado del remitente y obtenga un identificador de su [*clave pública*](../secgloss/p-gly.md).

    Como alternativa a los pasos 2 y 3, puede usar el certificado contenido en el mensaje para recuperar la clave pública del firmante.

4.  Mediante la clave pública del firmante, descifre la firma digital y genere el Resumen original de los datos en el mensaje.
5.  Mediante el algoritmo hash incluido en el mensaje, se [*aplica un algoritmo hash*](../secgloss/h-gly.md) a los datos contenidos en el mensaje, lo que produce una nueva síntesis.
6.  Compare la síntesis recuperada del mensaje con la nueva síntesis que acaba de crear.
7.  Si los dos resúmenes coinciden, se comprueba la firma. Esto significa que la [*clave privada*](../secgloss/p-gly.md) que se usó para firmar los datos coincide con la clave pública que se acaba de usar para descifrar la firma y que los datos no han cambiado desde que se firmaron los datos.

    Si los dos resúmenes no coinciden, no se comprueba la firma y las claves privada y pública no coinciden, o los datos han cambiado desde que se firmaron los datos, o ambos.

Se puede usar una sola función, [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature), para comprobar una firma, como se muestra en el procedimiento siguiente.

**Para comprobar un mensaje firmado**

1.  Obtiene un puntero al mensaje firmado.
2.  Obtiene el tamaño del mensaje firmado.
3.  Obtiene un identificador en un proveedor de servicios criptográficos.
4.  Inicialice el [**mensaje de comprobación de cifrado \_ \_ \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) la estructura.
5.  Llame a [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) para comprobar la firma.

El código que implementa este procedimiento se incluye en el [ejemplo C programa: firmar un mensaje y comprobar la firma de un mensaje](example-c-program-signing-a-message-and-verifying-a-message-signature.md).

 

 
