---
description: WSPEventSelect se comporta exactamente igual que WSPAsyncSelect, salvo que, en lugar de hacer que se envíe un mensaje de Windows tras la aparición de cualquier \_ evento de red FD XXX designado (por ejemplo, FD \_ Read, FD \_ de escritura, etc.), se establece un objeto de evento designado.
ms.assetid: 28f6eb78-1bb8-4eda-aac5-017975890502
title: Señalización del objeto de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42854a1f4e116c8dba100025007362898d183f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705629"
---
# <a name="event-object-signaling"></a><span data-ttu-id="8b888-103">Señalización del objeto de evento</span><span class="sxs-lookup"><span data-stu-id="8b888-103">Event Object Signaling</span></span>

<span data-ttu-id="8b888-104">[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) se comporta exactamente igual que [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) , salvo que, en lugar de hacer que se envíe un mensaje de Windows tras la aparición de cualquier \_ evento de red FD XXX designado (por ejemplo, FD \_ Read, FD \_ de escritura, etc.), se establece un objeto de evento designado.</span><span class="sxs-lookup"><span data-stu-id="8b888-104">[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) behaves exactly like [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) except that, rather than cause a Windows message to be sent upon the occurrence of any nominated FD\_XXX network event (for example, FD\_READ, FD\_WRITE, etc.), a designated event object is set.</span></span>

<span data-ttu-id="8b888-105">Además, el proveedor de servicios recuerda el hecho de que se \_ ha producido un evento de red FD XXX determinado.</span><span class="sxs-lookup"><span data-stu-id="8b888-105">Also, the fact that a particular FD\_XXX network event has occurred is remembered by the service provider.</span></span> <span data-ttu-id="8b888-106">Esto es necesario, ya que la repetición de todos los eventos de red nominados dará lugar a la señalización de un objeto de evento único.</span><span class="sxs-lookup"><span data-stu-id="8b888-106">This is needed since the occurrence of any and all nominated network events will result in a single event object becoming signaled.</span></span> <span data-ttu-id="8b888-107">Una llamada a [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) hace que el contenido actual de la memoria de eventos de red se copie en un búfer proporcionado por el cliente y la memoria de eventos de red que se va a borrar.</span><span class="sxs-lookup"><span data-stu-id="8b888-107">A call to [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) causes the current contents of the network event memory to be copied to a client-supplied buffer and the network event memory to be cleared.</span></span> <span data-ttu-id="8b888-108">El cliente también puede designar un objeto de evento determinado que se va a borrar de forma atómica junto con la memoria de eventos de red.</span><span class="sxs-lookup"><span data-stu-id="8b888-108">The client may also designate a particular event object to be cleared atomically along with the network event memory.</span></span>

 

 
