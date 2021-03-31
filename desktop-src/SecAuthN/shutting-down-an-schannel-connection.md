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
# <a name="shutting-down-an-schannel-connection"></a><span data-ttu-id="099bf-103">Cerrar una conexión Schannel</span><span class="sxs-lookup"><span data-stu-id="099bf-103">Shutting Down an Schannel Connection</span></span>

<span data-ttu-id="099bf-104">Cuando un cliente o servidor finaliza con una conexión, debe cerrarla.</span><span class="sxs-lookup"><span data-stu-id="099bf-104">When a client or server is finished with a connection, it must shut it down.</span></span> <span data-ttu-id="099bf-105">La otra parte, a su vez, debe reconocer el cierre y eliminar la conexión.</span><span class="sxs-lookup"><span data-stu-id="099bf-105">The other party, in turn, must recognize the shutdown and delete the connection.</span></span>

<span data-ttu-id="099bf-106">**Para cerrar una conexión Schannel**</span><span class="sxs-lookup"><span data-stu-id="099bf-106">**To shut down an Schannel connection**</span></span>

1.  <span data-ttu-id="099bf-107">Llame a la función [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) , especificando el \_ token de control de cierre Schannel.</span><span class="sxs-lookup"><span data-stu-id="099bf-107">Call the [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) function, specifying the SCHANNEL\_SHUTDOWN control token.</span></span>
2.  <span data-ttu-id="099bf-108">Después de recibir un \_ \_ valor de retorno de la s E de la solicitud de cambio de [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken), llame a la función [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (clientes) o [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (Servers), pasando búferes vacíos.</span><span class="sxs-lookup"><span data-stu-id="099bf-108">After receiving an SEC\_E\_OK return value from [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken), call the [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (clients) or [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (servers) function, passing in empty buffers.</span></span>
3.  <span data-ttu-id="099bf-109">Continúe como si su aplicación estuviera creando una nueva conexión hasta que la función devuelva la fecha en que se \_ \_ \_ ha expirado el contexto o la s y \_ \_ Aceptar para indicar que la conexión se ha cerrado.</span><span class="sxs-lookup"><span data-stu-id="099bf-109">Proceed as though your application were creating a new connection until the function returns SEC\_I\_CONTEXT\_EXPIRED or SEC\_E\_OK to indicate that the connection is shut down.</span></span>
4.  <span data-ttu-id="099bf-110">Envíe la información de salida final, si existe, a la parte remota.</span><span class="sxs-lookup"><span data-stu-id="099bf-110">Send the final output information, if any, to the remote party.</span></span>
5.  <span data-ttu-id="099bf-111">Llame a [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) para liberar los recursos retenidos por la conexión.</span><span class="sxs-lookup"><span data-stu-id="099bf-111">Call [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) to free resources held by the connection.</span></span>

## <a name="recognizing-a-shutdown"></a><span data-ttu-id="099bf-112">Reconocer un apagado</span><span class="sxs-lookup"><span data-stu-id="099bf-112">Recognizing a Shutdown</span></span>

<span data-ttu-id="099bf-113">La función [**DecryptMessage (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) devuelve la \_ hora en que contenía el contexto en el que \_ \_ el remitente del mensaje ha cerrado la conexión.</span><span class="sxs-lookup"><span data-stu-id="099bf-113">The [**DecryptMessage (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) function returns SEC\_I\_CONTEXT\_EXPIRED when the message sender has shut down the connection.</span></span> <span data-ttu-id="099bf-114">Después de recibir este valor devuelto, siga el procedimiento para cerrar una conexión Schannel, anteriormente en este tema.</span><span class="sxs-lookup"><span data-stu-id="099bf-114">After receiving this return value, follow the procedure To shut down an Schannel connection, earlier in this topic.</span></span>

 

 
