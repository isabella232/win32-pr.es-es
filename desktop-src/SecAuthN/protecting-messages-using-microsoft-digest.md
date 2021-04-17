---
description: Explica cómo proteger los mensajes mediante Microsoft Digest.
ms.assetid: 15509d51-80c0-4d5c-aa24-4dc17de3f12c
title: Protección de mensajes mediante Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573eafcf66e23188546abd3acd316095ec100187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652759"
---
# <a name="protecting-messages-using-microsoft-digest"></a>Protección de mensajes mediante Microsoft Digest

## <a name="http-and-sasl"></a>HTTP y SASL

Como forma de detectar ciertos tipos de infracciones de seguridad, el cliente y el servidor usan las funciones de [*integridad*](../secgloss/i-gly.md) de mensajes [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) y [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) de la interfaz del proveedor de [compatibilidad para seguridad](sspi.md) (SSPI) para proteger los mensajes.

Un cliente llama a la función [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para firmar un mensaje mediante su [*contexto de seguridad*](../secgloss/s-gly.md). El servidor utiliza la función [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) para comprobar el origen del mensaje. Además de comprobar la [*firma*](../secgloss/d-gly.md) que acompaña al mensaje, la función **VerifySignature** también comprueba que el número de [*nonce*](../secgloss/n-gly.md) (especificado por la Directiva de NC) es uno mayor que el último recuento enviado para el nonce. Si no es así, la función **VerifySignature** devuelve un \_ \_ \_ código de error seg. de secuencia.

## <a name="sasl-only"></a>Solo SASL

Las funciones [**EncryptMessage (general)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) y [**DecryptMessage (general)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) proporcionan confidencialidad para los mensajes posteriores a la autenticación intercambiados entre el cliente y el servidor.

Para poder usar las funciones de confidencialidad de mensajes, el servidor y el cliente deben haber establecido un [*contexto de seguridad*](../secgloss/s-gly.md) con los siguientes atributos:

-   La calidad de protección, especificada por la Directiva qop, debe ser "auth-conf".
-   Se debe haber especificado un mecanismo de cifrado mediante la Directiva Cipher.

 

 
