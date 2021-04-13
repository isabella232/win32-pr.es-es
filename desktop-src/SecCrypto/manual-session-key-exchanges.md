---
description: Muestra cómo enviar un mensaje cifrado.
ms.assetid: 928b1863-7a54-4bf0-b447-85b8c2868bcd
title: Intercambios de claves de sesión manual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0114f8173084126a72519d291158f15f3e1c171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560619"
---
# <a name="manual-session-key-exchanges"></a>Intercambios de claves de sesión manual

> [!Note]  
> En el procedimiento descrito en esta sección se da por supuesto que los usuarios (o los clientes de CryptoAPI) ya poseen su propio conjunto de [*pares de claves pública y privada*](../secgloss/p-gly.md) , y que también han obtenido [*las claves públicas*](../secgloss/p-gly.md)de los demás.

 

En la ilustración siguiente se muestra cómo usar este procedimiento para enviar un mensaje cifrado.

![envío de un mensaje cifrado](images/capi04.png)

Este enfoque es vulnerable a al menos una forma común de ataque. Un atacante puede adquirir copias de uno o más mensajes cifrados y claves cifradas. Después, en algún momento posterior, el espionaje puede enviar uno de estos mensajes al receptor y el receptor no tendrá forma de saber que el mensaje no procedía directamente del remitente original. Este riesgo puede reducirse con la marca de tiempo de todos los mensajes o mediante el uso de números de serie.

La manera más fácil de enviar mensajes cifrados a otro usuario es enviar el mensaje cifrado con una clave de sesión aleatoria junto con la clave de sesión cifrada con la clave [*pública de intercambio de claves*](../secgloss/k-gly.md)del receptor.

A continuación se indican los pasos para enviar una clave de sesión cifrada.

**Para enviar una clave de sesión cifrada**

1.  Cree una [*clave de sesión*](../secgloss/s-gly.md) aleatoria mediante la función [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .
2.  Cifre el mensaje mediante la clave de sesión. Este procedimiento se describe en [cifrado y descifrado de datos](data-encryption-and-decryption.md).
3.  Exporte la clave de sesión a un [*BLOB de clave*](../secgloss/k-gly.md) con la función [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , especificando que la clave se cifrará con la clave pública de intercambio de claves del usuario de destino.
4.  Envíe el mensaje cifrado y el BLOB de clave cifrada al usuario de destino.
5.  El usuario de destino importa el BLOB de clave a su CSP mediante la función [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) . Esto descifrará automáticamente la clave de sesión, siempre que se haya especificado la clave pública de intercambio de claves del usuario de destino en el paso 3.
6.  Después, el usuario de destino puede descifrar el mensaje mediante la clave de sesión, siguiendo el procedimiento descrito en [cifrado y descifrado de datos](data-encryption-and-decryption.md).

 

 
