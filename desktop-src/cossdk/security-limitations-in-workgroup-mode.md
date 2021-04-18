---
description: Limitaciones de seguridad en el modo de grupo de trabajo
ms.assetid: 05c0aba7-b94b-49d4-a0fc-1ff0a23550b3
title: Limitaciones de seguridad en el modo de grupo de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eabe38b8d05c49382ae6dd8337b883a6f4a8079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705297"
---
# <a name="security-limitations-in-workgroup-mode"></a><span data-ttu-id="0a8d9-103">Limitaciones de seguridad en el modo de grupo de trabajo</span><span class="sxs-lookup"><span data-stu-id="0a8d9-103">Security Limitations in Workgroup Mode</span></span>

<span data-ttu-id="0a8d9-104">La configuración del grupo de trabajo de [Message Queue Server](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) no permite que el servicio de componentes en cola com+ admita la seguridad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0a8d9-104">The [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) workgroup configuration does not permit the COM+ queued components service to support application security.</span></span> <span data-ttu-id="0a8d9-105">Si ha instalado Message Queue Server con la configuración del grupo de trabajo, debe [deshabilitar la seguridad](specifying-the-authentication-protocol.md) en cada aplicación en cola a la que se tiene acceso en esta configuración; para ello, seleccione **no autenticar mensajes** en la pestaña **cola** del cuadro de diálogo de **propiedades** de la aplicación com+ mediante la herramienta administrativa Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="0a8d9-105">If you've installed Message Queuing with the workgroup configuration, you must [disable security](specifying-the-authentication-protocol.md) on each queued application accessed in this configuration by selecting **Do not authenticate messages** on the **Queuing** tab for the COM+ application's **Properties** dialog, using the Component Services administrative tool.</span></span> <span data-ttu-id="0a8d9-106">Esto solo debe realizarse en una red de confianza y debe realizarse en el cliente y en el servidor si la aplicación ya se ha exportado.</span><span class="sxs-lookup"><span data-stu-id="0a8d9-106">This should be done only on a trusted network and must be done at both client and server if the application has already been exported.</span></span>

 

 



