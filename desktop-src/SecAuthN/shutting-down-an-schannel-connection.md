---
description: Cerrar una conexión Schannel
ms.assetid: 7081ba1f-df3c-41b4-96da-24d44e74d714
title: Cerrar una conexión Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc61b67083ceee65da714069c2b30ba1bfd5c89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808353"
---
# <a name="shutting-down-an-schannel-connection"></a>Cerrar una conexión Schannel

Cuando un cliente o servidor finaliza con una conexión, debe cerrarla. La otra parte, a su vez, debe reconocer el cierre y eliminar la conexión.

**Para cerrar una conexión Schannel**

1.  Llame a la función [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) , especificando el \_ token de control de cierre Schannel.
2.  Después de recibir un \_ \_ valor de retorno de la s E de la solicitud de cambio de [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken), llame a la función [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (clientes) o [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (Servers), pasando búferes vacíos.
3.  Continúe como si su aplicación estuviera creando una nueva conexión hasta que la función devuelva la fecha en que se \_ \_ \_ ha expirado el contexto o la s y \_ \_ Aceptar para indicar que la conexión se ha cerrado.
4.  Envíe la información de salida final, si existe, a la parte remota.
5.  Llame a [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) para liberar los recursos retenidos por la conexión.

## <a name="recognizing-a-shutdown"></a>Reconocer un apagado

La función [**DecryptMessage (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) devuelve la \_ hora en que contenía el contexto en el que \_ \_ el remitente del mensaje ha cerrado la conexión. Después de recibir este valor devuelto, siga el procedimiento para cerrar una conexión Schannel, anteriormente en este tema.

 

 
