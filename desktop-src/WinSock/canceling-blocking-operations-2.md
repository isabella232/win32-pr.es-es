---
description: Un subproceso puede, en cualquier momento, llamar a WSAIsBlocking para determinar si una llamada de bloqueo está actualmente en curso.
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: Cancelar operaciones de bloqueo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502870b8935dc97c1d6c3714808d1c6532780f7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705649"
---
# <a name="canceling-blocking-operations"></a><span data-ttu-id="f4e72-103">Cancelar operaciones de bloqueo</span><span class="sxs-lookup"><span data-stu-id="f4e72-103">Canceling Blocking Operations</span></span>

<span data-ttu-id="f4e72-104">Un subproceso puede, en cualquier momento, llamar a [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) para determinar si una llamada de bloqueo está actualmente en curso.</span><span class="sxs-lookup"><span data-stu-id="f4e72-104">A thread may, at any time, call [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) to determine whether or not a blocking call is currently in progress.</span></span> <span data-ttu-id="f4e72-105">(Esta función se implementa dentro de las correcciones de compatibilidad de Windows Sockets 1,1 y, por lo tanto, no tiene ningún homólogo SPI). Claramente, esto solo es posible cuando el proveedor de servicios está empleando un pseudo bloqueo, en lugar de un bloqueo real.</span><span class="sxs-lookup"><span data-stu-id="f4e72-105">(This function is implemented within the Windows Sockets 1.1 compatibility shims and hence has no SPI counterpart.) Clearly this is only possible when pseudo blocking, as opposed to true blocking, is being employed by the service provider.</span></span> <span data-ttu-id="f4e72-106">Cuando sea necesario, se puede llamar a [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) en cualquier momento para cancelar cualquier operación de pseudo bloqueo actual.</span><span class="sxs-lookup"><span data-stu-id="f4e72-106">When necessary, [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) may be called at any time to cancel any current pseudo blocking operation.</span></span>

 

 
