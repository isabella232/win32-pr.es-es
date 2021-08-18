---
description: Muestra cómo enviar un mensaje cifrado.
ms.assetid: 928b1863-7a54-4bf0-b447-85b8c2868bcd
title: Intercambios de claves de sesión manuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c9f7338b40ed1675b2186e478c8c124719b376889ce691d305e246016e0d9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425604"
---
# <a name="manual-session-key-exchanges"></a>Intercambios de claves de sesión manuales

> [!Note]  
> En el procedimiento descrito en esta sección se da por supuesto que [](../secgloss/p-gly.md) los usuarios (o clientes cryptoAPI) ya poseen su propio conjunto de pares de claves pública y privada y también han obtenido las claves públicas de los [*demás.*](../secgloss/p-gly.md)

 

En la ilustración siguiente se muestra cómo usar este procedimiento para enviar un mensaje cifrado.

![enviar un mensaje cifrado](images/capi04.png)

Este enfoque es vulnerable a al menos una forma común de ataque. Un alero puede adquirir copias de uno o varios mensajes cifrados y las claves cifradas. A continuación, en algún momento posterior, el alero puede enviar uno de estos mensajes al receptor y el receptor no tendrá ninguna manera de saber que el mensaje no procede directamente del remitente original. Este riesgo se puede reducir mediante la marca de tiempo de todos los mensajes o mediante números de serie.

La manera más fácil de enviar mensajes cifrados a otro usuario es enviar el mensaje cifrado con una clave de sesión aleatoria junto con la clave de sesión cifrada con la clave pública de intercambio de claves [*del receptor.*](../secgloss/k-gly.md)

A continuación se indican los pasos para enviar una clave de sesión cifrada.

**Para enviar una clave de sesión cifrada**

1.  Cree una clave [*de sesión aleatoria*](../secgloss/s-gly.md) mediante la función [**CryptGenKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)
2.  Cifre el mensaje mediante la clave de sesión. Este procedimiento se describe en [Cifrado y descifrado de datos.](data-encryption-and-decryption.md)
3.  Exporte la clave de sesión a un [*BLOB*](../secgloss/k-gly.md) de clave con la función [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) y especifique que la clave se cifrará con la clave pública de intercambio de claves del usuario de destino.
4.  Envíe tanto el mensaje cifrado como el BLOB de clave cifrada al usuario de destino.
5.  El usuario de destino importa el BLOB de clave en su CSP mediante la [**función CryptImportKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) Esto descifrará automáticamente la clave de sesión, siempre que la clave pública de intercambio de claves del usuario de destino se haya especificado en el paso 3.
6.  A continuación, el usuario de destino puede descifrar el mensaje mediante la clave de sesión, siguiendo el procedimiento descrito en [Cifrado y descifrado de datos](data-encryption-and-decryption.md).

 

 
