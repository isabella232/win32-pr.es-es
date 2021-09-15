---
description: Estos pasos comprueban la firma de los datos firmados.
ms.assetid: 18246cc1-d3c4-4426-a342-ce3864cc412e
title: Comprobar un mensaje firmado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f85a5bcde56df7bb41bb92276123bcd26024e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473449"
---
# <a name="verifying-a-signed-message"></a>Comprobar un mensaje firmado

Estos pasos comprueban la firma de los datos firmados. En la ilustración siguiente se muestran las tareas individuales que deben realizarse, como se muestra en la lista que sigue a ella.

![comprobar un mensaje firmado](images/verifmsg.png)

**Para comprobar la firma de un mensaje firmado**

1.  Obtenga un puntero al mensaje firmado.
2.  Abra un [*almacén de certificados*](../secgloss/c-gly.md).
3.  Con el identificador de firmante contenido en el mensaje, obtenga el certificado del remitente y obtenga un identificador para su [*clave pública*](../secgloss/p-gly.md).

    Como alternativa a los pasos 2 y 3, puede usar el certificado contenido en el mensaje para recuperar la clave pública del firmante.

4.  Con la clave pública del firmante, descifre la firma digital y produzca la síntesis original de los datos del mensaje.
5.  Mediante el algoritmo hash contenido en el mensaje, [*aplica un algoritmo hash*](../secgloss/h-gly.md) a los datos contenidos en el mensaje, lo que produce un nuevo resumen.
6.  Compare el resumen recuperado del mensaje con el nuevo resumen que acaba de crear.
7.  Si los dos resúmenes coinciden, se comprueba la firma. Esto significa que [*la*](../secgloss/p-gly.md) clave privada que se usó para firmar los datos coincide con la clave pública que se acaba de usar para descifrar la firma y que los datos no han cambiado desde que se firmaron los datos.

    Si los dos resúmenes no coinciden, no se comprueba la firma y las claves privadas y públicas no coinciden, o los datos se han cambiado desde que se firmaron los datos, o ambos.

Se puede usar una sola [**función, CryptVerifyMessageSignature,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature)para comprobar una firma, como se muestra en el procedimiento siguiente.

**Para comprobar un mensaje firmado**

1.  Obtenga un puntero al mensaje firmado.
2.  Obtiene el tamaño del mensaje firmado.
3.  Obtener un identificador en un proveedor de servicios criptográficos.
4.  Inicialice la [**estructura CRYPT \_ VERIFY MESSAGE \_ \_ PARA.**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para)
5.  Llame [**a CryptVerifyMessageSignature para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) comprobar la firma.

El código que implementa este procedimiento se incluye en el [Programa de ejemplo C: Firmar un mensaje y comprobar una firma de mensaje](example-c-program-signing-a-message-and-verifying-a-message-signature.md).

 

 
