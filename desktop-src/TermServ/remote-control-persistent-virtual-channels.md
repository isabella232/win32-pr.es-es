---
title: Canales virtuales persistentes de control remoto
description: Un canal virtual persistente de control remoto no se cierra cuando un control remoto se conecta o se desconecta para la sesión conectada al cliente. Los datos se seguirán transmitiendo y recibiendo a través de este canal.
ms.assetid: 0c3d5429-250e-4272-8cdd-69097acfaff4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d87054a79863df5816b30fced648ab40251a80e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419087"
---
# <a name="remote-control-persistent-virtual-channels"></a><span data-ttu-id="4e0c0-104">Canales virtuales persistentes de control remoto</span><span class="sxs-lookup"><span data-stu-id="4e0c0-104">Remote Control Persistent Virtual Channels</span></span>

<span data-ttu-id="4e0c0-105">En Windows XP, un archivo DLL puede especificar uno o más canales virtuales como *persistentes para el control remoto*.</span><span class="sxs-lookup"><span data-stu-id="4e0c0-105">On Windows XP, a DLL can specify one or more virtual channels as *remote control persistent*.</span></span> <span data-ttu-id="4e0c0-106">Un canal virtual persistente de control remoto no se cierra cuando un control remoto se conecta o se desconecta para la sesión conectada al cliente.</span><span class="sxs-lookup"><span data-stu-id="4e0c0-106">A remote control persistent virtual channel is not closed when a remote control connects or disconnects for the session connected to the client.</span></span> <span data-ttu-id="4e0c0-107">Los datos se seguirán transmitiendo y recibiendo a través de este canal.</span><span class="sxs-lookup"><span data-stu-id="4e0c0-107">Data will continue to be transmitted and received through this channel.</span></span> <span data-ttu-id="4e0c0-108">Los canales virtuales que el archivo DLL no especifica como control remoto persistente se cerrarán en este escenario.</span><span class="sxs-lookup"><span data-stu-id="4e0c0-108">Virtual channels that the DLL does not specify as remote control persistent will close in this scenario.</span></span>

<span data-ttu-id="4e0c0-109">Los canales virtuales persistentes del control remoto se especifican durante la llamada a **VirtualChannelInit**.</span><span class="sxs-lookup"><span data-stu-id="4e0c0-109">Remote control persistent virtual channels are specified during the call to **VirtualChannelInit**.</span></span> <span data-ttu-id="4e0c0-110">Consulte la página de referencia de [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) para obtener información específica sobre este.</span><span class="sxs-lookup"><span data-stu-id="4e0c0-110">Refer to the reference page for [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) for specific information about this.</span></span>

 

 




