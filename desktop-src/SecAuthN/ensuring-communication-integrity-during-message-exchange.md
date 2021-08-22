---
description: Una vez establecido un contexto de seguridad, la aplicación puede usar las funciones de soporte de mensajes para transmitir mensajes resistentes a manipulaciones.
ms.assetid: 43d7b940-1816-429f-be6e-40978efed278
title: Garantizar la integridad de la comunicación durante la Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394f78fcc1e5becf4bdfc7c67db52e1af177a7f3aa427d1c6182a080f0ae87bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008263"
---
# <a name="ensuring-communication-integrity-during-message-exchange"></a>Garantizar la integridad de la comunicación durante la Exchange

Una vez [*establecido un contexto*](/windows/desktop/SecGloss/s-gly) de seguridad, la aplicación puede usar las funciones de soporte [de](authentication-functions.md) mensajes para transmitir mensajes resistentes a manipulaciones.

El cliente o servidor pasa el contexto de seguridad y un mensaje a la función [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para generar una firma segura que impida que el mensaje se modifique mientras está en tránsito. El receptor del mensaje llama a la [**función VerifySignature.**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) **VerifySignature** usa la información de la firma para comprobar que el mensaje recibido no se modificó durante la transmisión. El cliente y el servidor también pueden intercambiar mensajes cifrados [**mediante EncryptMessage (general)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) y [**DecryptMessage (general).**](/windows/win32/api/sspi/nf-sspi-decryptmessage)

El servidor de una conexión autenticada también puede realizar conexiones con otros equipos remotos en el nombre del cliente después de llamar a [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext).

 

 
