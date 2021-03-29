---
title: Devoluciones de llamada de alerta de interfaz errónea
description: Una vez que el reenviador de kernel recibe datos de multidifusión de un origen específico en la interfaz equivocada, se lo notifica al administrador del grupo de multidifusión.
ms.assetid: 7b20625e-286b-4c4f-8452-4d21563fd030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12906d836ca994e90347ea78cf22e50f8f2f00d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779447"
---
# <a name="wrong-interface-alert-callbacks"></a><span data-ttu-id="1418d-103">Devoluciones de llamada de alerta de interfaz errónea</span><span class="sxs-lookup"><span data-stu-id="1418d-103">Wrong Interface Alert Callbacks</span></span>

<span data-ttu-id="1418d-104">Una vez que el reenviador de kernel recibe datos de multidifusión de un origen específico en la interfaz equivocada, se lo notifica al administrador del grupo de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="1418d-104">After the kernel forwarder receives multicast data from a specific source on the wrong interface, it notifies the multicast group manager.</span></span> <span data-ttu-id="1418d-105">A continuación, el administrador del grupo de multidifusión invoca el [**PMGM \_ incorrecto \_ si \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback) la devolución de llamada de devolución de llamada al Protocolo de enrutamiento que posee la interfaz en la que los datos llegaron incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="1418d-105">The multicast group manager then invokes the [**PMGM\_WRONG\_IF\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback) callback to the routing protocol that owns the interface on which the data incorrectly arrived.</span></span>

> [!Note]  
> <span data-ttu-id="1418d-106">Esta devolución de llamada no está implementada actualmente en esta versión de la API MGM.</span><span class="sxs-lookup"><span data-stu-id="1418d-106">This callback is not currently implemented in this version of the MGM API.</span></span>

 

 

 




