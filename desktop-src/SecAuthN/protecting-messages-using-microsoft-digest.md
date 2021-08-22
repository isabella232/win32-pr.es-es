---
description: Explica cómo proteger los mensajes mediante Microsoft Digest.
ms.assetid: 15509d51-80c0-4d5c-aa24-4dc17de3f12c
title: Protección de mensajes mediante Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab0add351287b6c90cfe0781151c0378da56f309214b03ed12d1325a6e55d88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920744"
---
# <a name="protecting-messages-using-microsoft-digest"></a>Protección de mensajes mediante Microsoft Digest

## <a name="http-and-sasl"></a>HTTP y SASL

Como medio para detectar determinados tipos de infracciones de seguridad, el cliente y [](../secgloss/i-gly.md) el servidor usan las funciones de integridad de mensajes de la interfaz del proveedor de compatibilidad de seguridad [](sspi.md) (SSPI) [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) y [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) para proteger los mensajes.

Un cliente llama a [**la función MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para firmar un mensaje mediante su contexto [*de seguridad*](../secgloss/s-gly.md). El servidor usa la [**función VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) para comprobar el origen del mensaje. Además de comprobar [](../secgloss/d-gly.md) la firma que acompaña al mensaje, la función **VerifySignature** también comprueba que el recuento [*de nonce*](../secgloss/n-gly.md) (especificado por la directiva nc) es mayor que el último recuento enviado para el valor nonce. Si este no es el caso, la **función VerifySignature** devuelve un código de \_ error SEC OUT OF \_ \_ SEQUENCE.

## <a name="sasl-only"></a>Solo SASL

Las [**funciones EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) y [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) suministran confidencialidad para los mensajes posteriores a la autenticación intercambiados entre el cliente y el servidor.

Para usar las funciones de confidencialidad del mensaje, el servidor y el cliente deben haber establecido un contexto [*de seguridad*](../secgloss/s-gly.md) con los atributos siguientes:

-   La calidad de protección, especificada por la directiva qop, debe ser "auth-conf".
-   Un mecanismo de cifrado se debe haber especificado mediante la directiva de cifrado.

 

 
