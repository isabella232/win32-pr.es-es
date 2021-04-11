---
description: Los dos (o más) descriptores que hacen referencia a un socket compartido se pueden usar de forma independiente en lo que respecta a la e/s.
ms.assetid: 25252552-4b62-441a-b564-e7f4a77cf68a
title: Instrucciones de precedencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c2086b2d640e2968c56082c2d8dfff99546fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154256"
---
# <a name="precedence-guidelines"></a><span data-ttu-id="319df-103">Instrucciones de precedencia</span><span class="sxs-lookup"><span data-stu-id="319df-103">Precedence Guidelines</span></span>

<span data-ttu-id="319df-104">Los dos (o más) descriptores que hacen referencia a un socket compartido se pueden usar de forma independiente en lo que respecta a la e/s.</span><span class="sxs-lookup"><span data-stu-id="319df-104">The two (or more) descriptors that reference a shared socket may be used independently as far as I/O is concerned.</span></span> <span data-ttu-id="319df-105">Sin embargo, la interfaz de Windows Sockets no implementa ningún tipo de control de acceso, por lo que depende de los procesos implicados en la coordinación de las operaciones en un socket compartido.</span><span class="sxs-lookup"><span data-stu-id="319df-105">However, the Windows Sockets interface does not implement any type of access control, so it is up to the processes involved to coordinate their operations on a shared socket.</span></span> <span data-ttu-id="319df-106">Un uso típico de los sockets compartidos es disponer de un proceso que sea responsable de la creación de sockets y de establecer conexiones a los sockets en otros procesos responsables del intercambio de información.</span><span class="sxs-lookup"><span data-stu-id="319df-106">A typical use for shared sockets is to have one process that is responsible for creating sockets and establishing connections hand off sockets to other processes that are responsible for information exchange.</span></span>

<span data-ttu-id="319df-107">La directriz general para admitir varias operaciones pendientes en sockets compartidos es que se recomienda que un proveedor de servicios respete todas las operaciones simultáneas en los sockets compartidos, especialmente la operación más reciente en un objeto de socket.</span><span class="sxs-lookup"><span data-stu-id="319df-107">The general guideline for supporting multiple outstanding operations on shared sockets is that a service provider is encouraged to honor all simultaneous operations on shared sockets, especially the most recent operation on a socket object.</span></span> <span data-ttu-id="319df-108">Si es necesario, esto puede ocurrir a costa de que se cancelen algunas de las operaciones anteriores pero todavía pendientes, que devolverán WSAEINTR en este caso.</span><span class="sxs-lookup"><span data-stu-id="319df-108">If need be, this may occur at the expense of canceling some of the previous but still pending operations, which will return WSAEINTR in this case.</span></span>

 

 



