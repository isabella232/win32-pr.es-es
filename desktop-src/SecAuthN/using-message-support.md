---
description: Explica cómo usar la compatibilidad con mensajes SSPI.
ms.assetid: 14d4813e-413e-4ef9-85f0-96986c3c1eca
title: Uso de compatibilidad con mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d75a2475609afed1647d99552a3719479d84fbd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160903"
---
# <a name="using-message-support"></a>Uso de compatibilidad con mensajes

Una vez que se ha completado un protocolo de enlace y se ha establecido una conexión segura, una aplicación puede usar las funciones [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)y [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) para intercambiar datos de aplicación firmados o cifrados con el equipo remoto.

En las secciones siguientes [](../secgloss/s-gly.md) se muestran ejemplos que usan estas funciones después de establecer un contexto de seguridad:

-   [Firmar un mensaje](signing-a-message.md)
-   [Comprobación de un mensaje](verifying-a-message.md)
-   [Cifrado de un mensaje](encrypting-a-message.md)
-   [Descifrar un mensaje](decrypting-a-message.md)

 

 
