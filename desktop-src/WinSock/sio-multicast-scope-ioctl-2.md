---
description: Usar el \_ \_ código de comando de ámbito de multidifusión de SiO para especificar el ámbito en el que se debe producir la multidifusión.
ms.assetid: 3acec987-9cb4-446c-af6e-ea0e6a96e70c
title: Ioctl SIO_MULTICAST_SCOPE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d1fd6f2bea76d095ea88d66c0ac029fb9168ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697486"
---
# <a name="sio_multicast_scope-ioctl"></a><span data-ttu-id="6131e-103">SIO \_ ámbito de multidifusión \_ ioctl</span><span class="sxs-lookup"><span data-stu-id="6131e-103">SIO\_MULTICAST\_SCOPE Ioctl</span></span>

<span data-ttu-id="6131e-104">Cuando se emplea la multidifusión, normalmente es necesario especificar el ámbito en el que se debe producir la multidifusión.</span><span class="sxs-lookup"><span data-stu-id="6131e-104">When multicasting is employed, it is usually necessary to specify the scope over which the multicast should occur.</span></span> <span data-ttu-id="6131e-105">Aquí el ámbito se define como el número de segmentos de red enrutados que se van a cubrir.</span><span class="sxs-lookup"><span data-stu-id="6131e-105">Here scope is defined to be the number of routed network segments to be covered.</span></span> <span data-ttu-id="6131e-106">El \_ \_ código de comando SiO multidifusión Scope para [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) se usa para controlar esto.</span><span class="sxs-lookup"><span data-stu-id="6131e-106">The SIO\_MULTICAST\_SCOPE command code for [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) is used to control this.</span></span> <span data-ttu-id="6131e-107">Un ámbito de cero indicaría que la transmisión por multidifusión no se colocaría en la conexión, pero podría diseminarse a través de sockets dentro del host local.</span><span class="sxs-lookup"><span data-stu-id="6131e-107">A scope of zero would indicate that the multicast transmission would not be placed on the wire but could be disseminated across sockets within the local host.</span></span> <span data-ttu-id="6131e-108">Un valor de ámbito de uno (valor predeterminado) indica que la transmisión se colocará en la conexión, pero no cruzará ningún enrutador.</span><span class="sxs-lookup"><span data-stu-id="6131e-108">A scope value of one (the default) indicates that the transmission will be placed on the wire, but will not cross any routers.</span></span> <span data-ttu-id="6131e-109">Los valores de ámbito más altos determinan el número de enrutadores que se pueden cruzar.</span><span class="sxs-lookup"><span data-stu-id="6131e-109">Higher scope values determine the number of routers that may be crossed.</span></span> <span data-ttu-id="6131e-110">Tenga en cuenta que esto corresponde al parámetro Time-to-Live (TTL) de la multidifusión IP.</span><span class="sxs-lookup"><span data-stu-id="6131e-110">Note that this corresponds to the time-to-live (TTL) parameter in IP multicasting.</span></span>

 

 
