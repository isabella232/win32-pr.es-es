---
title: Secuencia de conexión
description: Ilustración que muestra las llamadas de método realizadas entre el servicio de Servicios de Escritorio remoto y el protocolo durante la secuencia de conexión de cliente.
ms.assetid: 60e56093-c457-43bc-b152-15c5acbfb016
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fe18d1a3b305a99fb0aaa35c51696f66de5c09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419049"
---
# <a name="connection-sequence"></a><span data-ttu-id="76e68-103">Secuencia de conexión</span><span class="sxs-lookup"><span data-stu-id="76e68-103">Connection Sequence</span></span>

<span data-ttu-id="76e68-104">En la ilustración siguiente se muestran las llamadas a métodos realizadas entre el servicio de Servicios de Escritorio remoto y el protocolo durante la secuencia de conexión de cliente.</span><span class="sxs-lookup"><span data-stu-id="76e68-104">The following illustration shows the method calls made between the Remote Desktop Services service and your protocol during the client connection sequence.</span></span> <span data-ttu-id="76e68-105">Las acciones que se muestran aquí siguen la [secuencia de inicio](start-sequence.md).</span><span class="sxs-lookup"><span data-stu-id="76e68-105">The actions shown here follow the [Start Sequence](start-sequence.md).</span></span> <span data-ttu-id="76e68-106">La interacción entre el servicio y el objeto [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) representa el protocolo de enlace de licencias para el cliente.</span><span class="sxs-lookup"><span data-stu-id="76e68-106">The interaction between the service and the [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) object represents the licensing handshake for the client.</span></span>

![secuencia de conexión de cliente](images/protocol-connectionsequence.png)

## <a name="related-topics"></a><span data-ttu-id="76e68-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76e68-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76e68-109">Secuencia de llamada al método</span><span class="sxs-lookup"><span data-stu-id="76e68-109">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="76e68-110">Secuencia de reconexión</span><span class="sxs-lookup"><span data-stu-id="76e68-110">Reconnect Sequence</span></span>](reconnect-sequence.md)
</dt> <dt>

[<span data-ttu-id="76e68-111">Secuencia de inicio</span><span class="sxs-lookup"><span data-stu-id="76e68-111">Start Sequence</span></span>](start-sequence.md)
</dt> </dl>

 

 




