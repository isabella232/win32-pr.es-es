---
description: Explica cómo usar la compatibilidad con mensajes SSPI.
ms.assetid: 14d4813e-413e-4ef9-85f0-96986c3c1eca
title: Uso de la compatibilidad con mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d75a2475609afed1647d99552a3719479d84fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668124"
---
# <a name="using-message-support"></a><span data-ttu-id="27132-103">Uso de la compatibilidad con mensajes</span><span class="sxs-lookup"><span data-stu-id="27132-103">Using Message Support</span></span>

<span data-ttu-id="27132-104">Una vez que se ha completado un protocolo de enlace y se ha establecido una conexión segura, una aplicación puede usar las funciones [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**EncryptMessage (general)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)y [**DecryptMessage (general)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) para intercambiar datos de aplicación firmados o cifrados con el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="27132-104">After a handshake has been completed and a secure connection has been established, an application can use the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature), and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) functions to exchange signed or encrypted application data with the remote computer.</span></span>

<span data-ttu-id="27132-105">En las secciones siguientes se muestran ejemplos que usan estas funciones después de establecer un [*contexto de seguridad*](../secgloss/s-gly.md) :</span><span class="sxs-lookup"><span data-stu-id="27132-105">Examples that use these functions after a [*security context*](../secgloss/s-gly.md) has been established are demonstrated in the following sections:</span></span>

-   [<span data-ttu-id="27132-106">Firmar un mensaje</span><span class="sxs-lookup"><span data-stu-id="27132-106">Signing a Message</span></span>](signing-a-message.md)
-   [<span data-ttu-id="27132-107">Comprobación de un mensaje</span><span class="sxs-lookup"><span data-stu-id="27132-107">Verifying a Message</span></span>](verifying-a-message.md)
-   [<span data-ttu-id="27132-108">Cifrado de un mensaje</span><span class="sxs-lookup"><span data-stu-id="27132-108">Encrypting a Message</span></span>](encrypting-a-message.md)
-   [<span data-ttu-id="27132-109">Descifrado de un mensaje</span><span class="sxs-lookup"><span data-stu-id="27132-109">Decrypting a Message</span></span>](decrypting-a-message.md)

 

 
