---
description: Apagar una conexión Schannel
ms.assetid: 7081ba1f-df3c-41b4-96da-24d44e74d714
title: Apagar una conexión Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc61b67083ceee65da714069c2b30ba1bfd5c89b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244118"
---
# <a name="shutting-down-an-schannel-connection"></a>Apagar una conexión Schannel

Cuando un cliente o servidor finaliza con una conexión, debe apagarlo. La otra parte, a su vez, debe reconocer el apagado y eliminar la conexión.

**Para apagar una conexión Schannel**

1.  Llame a [**la función ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) y especifique el token de control SCHANNEL \_ SHUTDOWN.
2.  Después de recibir un valor devuelto SEC E OK de ApplyControlToken, llame a la función \_ \_ [**InitializeSecurityContext (Schannel) (clientes)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) o [**AcceptSecurityContext (Schannel) (servidores)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) [](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken)y pase búferes vacíos.
3.  Continúe como si la aplicación estuviera creando una nueva conexión hasta que la función devuelva SEC I CONTEXT EXPIRED o SEC E OK para indicar que la conexión \_ \_ está \_ \_ \_ apagada.
4.  Envíe la información de salida final, si existe, a la parte remota.
5.  Llame [**a DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) para liberar los recursos mantenidos por la conexión.

## <a name="recognizing-a-shutdown"></a>Reconocer un apagado

La [**función DecryptMessage (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) devuelve SEC \_ I CONTEXT EXPIRED cuando el remitente del mensaje ha cerrado la \_ \_ conexión. Después de recibir este valor devuelto, siga el procedimiento Para apagar una conexión Schannel, anteriormente en este tema.

 

 
