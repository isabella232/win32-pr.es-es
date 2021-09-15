---
description: Muestra cómo enviar un mensaje cifrado.
ms.assetid: 928b1863-7a54-4bf0-b447-85b8c2868bcd
title: Intercambios manuales de claves de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0114f8173084126a72519d291158f15f3e1c171
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270900"
---
# <a name="manual-session-key-exchanges"></a>Intercambios manuales de claves de sesión

> [!Note]  
> En el procedimiento descrito en esta sección se da por supuesto que [](../secgloss/p-gly.md) los usuarios (o clientes cryptoAPI) ya poseen su propio conjunto de pares de claves públicas y privadas y también han obtenido las claves públicas de los [*demás.*](../secgloss/p-gly.md)

 

En la ilustración siguiente se muestra cómo usar este procedimiento para enviar un mensaje cifrado.

![enviar un mensaje cifrado](images/capi04.png)

Este enfoque es vulnerable a al menos una forma común de ataque. Un alero puede adquirir copias de uno o varios mensajes cifrados y las claves cifradas. A continuación, en algún momento posterior, el alero puede enviar uno de estos mensajes al receptor y el receptor no tendrá ninguna manera de saber que el mensaje no procede directamente del remitente original. Este riesgo se puede reducir mediante la marca de tiempo de todos los mensajes o mediante números de serie.

La manera más fácil de enviar mensajes cifrados a otro usuario es enviar el mensaje cifrado con una clave de sesión aleatoria junto con la clave de sesión cifrada con la clave pública de intercambio de claves [*del receptor.*](../secgloss/k-gly.md)

A continuación se indican los pasos para enviar una clave de sesión cifrada.

**Para enviar una clave de sesión cifrada**

1.  Cree una clave [*de sesión aleatoria*](../secgloss/s-gly.md) mediante la función [**CryptGenKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)
2.  Cifre el mensaje mediante la clave de sesión. Este procedimiento se describe en [Cifrado y descifrado de datos](data-encryption-and-decryption.md).
3.  Exporte la clave de sesión a un [*blob*](../secgloss/k-gly.md) de clave con la función [**CryptExportKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) especificando que la clave se cifrará con la clave pública de intercambio de claves del usuario de destino.
4.  Envíe tanto el mensaje cifrado como el blob de clave cifrada al usuario de destino.
5.  El usuario de destino importa el blob de clave en su CSP mediante la [**función CryptImportKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) Esto descifrará automáticamente la clave de sesión, siempre que se haya especificado la clave pública de intercambio de claves del usuario de destino en el paso 3.
6.  A continuación, el usuario de destino puede descifrar el mensaje mediante la clave de sesión, siguiendo el procedimiento descrito en [Cifrado y descifrado de datos](data-encryption-and-decryption.md).

 

 
