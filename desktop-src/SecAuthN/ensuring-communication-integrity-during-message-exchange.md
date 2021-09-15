---
description: Una vez establecido un contexto de seguridad, la aplicación puede usar las funciones de soporte de mensajes para transmitir mensajes resistentes a manipulaciones.
ms.assetid: 43d7b940-1816-429f-be6e-40978efed278
title: Garantizar la integridad de la comunicación durante la Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70545abf11a933cd3bb6d0c32f3312637fcccbe2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271455"
---
# <a name="ensuring-communication-integrity-during-message-exchange"></a>Garantizar la integridad de la comunicación durante la Exchange

Una vez [*establecido un contexto*](/windows/desktop/SecGloss/s-gly) de seguridad, la aplicación puede usar las funciones de soporte [de](authentication-functions.md) mensajes para transmitir mensajes resistentes a manipulaciones.

El cliente o servidor pasa el contexto de seguridad y un mensaje a la función [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para generar una firma segura que impide que el mensaje se modifique mientras está en tránsito. El receptor del mensaje llama a la [**función VerifySignature.**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) **VerifySignature** usa la información de la firma para comprobar que el mensaje recibido no se modificó durante la transmisión. El cliente y el servidor también pueden intercambiar mensajes cifrados [**mediante EncryptMessage (general)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) y [**DecryptMessage (general).**](/windows/win32/api/sspi/nf-sspi-decryptmessage)

El servidor de una conexión autenticada también puede realizar conexiones con otros equipos remotos en el nombre del cliente después de llamar a [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext).

 

 
