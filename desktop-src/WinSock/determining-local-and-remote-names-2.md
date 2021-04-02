---
description: WSPGetSockName se utiliza para recuperar la dirección local para Sockets enlazados.
ms.assetid: 5f3c9aa8-97fe-48a1-a3f5-156c9bddb1b2
title: Determinar los nombres locales y remotos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265cf8013dcadaedbef786ab78f48e63de81a992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082122"
---
# <a name="determining-local-and-remote-names"></a><span data-ttu-id="14503-103">Determinar los nombres locales y remotos</span><span class="sxs-lookup"><span data-stu-id="14503-103">Determining Local and Remote Names</span></span>

<span data-ttu-id="14503-104">[**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)) se utiliza para recuperar la dirección local para Sockets enlazados.</span><span class="sxs-lookup"><span data-stu-id="14503-104">[**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)) is used to retrieve the local address for bound sockets.</span></span> <span data-ttu-id="14503-105">Esto es especialmente útil cuando se ha realizado una llamada a [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) sin hacer un [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)) primero; **WSPGetSockName** proporciona el único medio para determinar la asociación local que el proveedor ha establecido implícitamente.</span><span class="sxs-lookup"><span data-stu-id="14503-105">This is especially useful when a [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) call has been made without doing a [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)) first; **WSPGetSockName** provides the only means to determine the local association which has been set implicitly by the provider.</span></span>

<span data-ttu-id="14503-106">Una vez configurada una conexión, se puede usar [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)) para determinar la dirección del elemento del mismo nivel al que está conectado un socket.</span><span class="sxs-lookup"><span data-stu-id="14503-106">After a connection has been set up, [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)) can be used to determine the address of the peer to which a socket is connected.</span></span>

 

 
