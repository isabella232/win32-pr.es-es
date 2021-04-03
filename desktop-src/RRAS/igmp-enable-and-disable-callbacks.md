---
title: Habilitar y deshabilitar devoluciones de llamada de IGMP
description: El administrador del grupo de multidifusión usa dos devoluciones de llamada a IGMP para coordinar los cambios en la propiedad de la interfaz de IGMP a un protocolo de enrutamiento y de un protocolo de enrutamiento a IGMP.
ms.assetid: e4b2be85-6c67-4801-9905-eb1990d4bbb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa58e9b65c67ac5946f5f5e54e611565e59d8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904754"
---
# <a name="igmp-enable-and-disable-callbacks"></a><span data-ttu-id="98c64-103">Habilitar y deshabilitar devoluciones de llamada de IGMP</span><span class="sxs-lookup"><span data-stu-id="98c64-103">IGMP Enable and Disable Callbacks</span></span>

<span data-ttu-id="98c64-104">El administrador del grupo de multidifusión usa dos devoluciones de llamada a IGMP para coordinar los cambios en la propiedad de la interfaz de IGMP a un protocolo de enrutamiento y de un protocolo de enrutamiento a IGMP.</span><span class="sxs-lookup"><span data-stu-id="98c64-104">The multicast group manager uses two callbacks to IGMP to coordinate changes in interface ownership from IGMP to a routing protocol, and from a routing protocol to IGMP.</span></span> <span data-ttu-id="98c64-105">Las devoluciones de llamada permiten que IGMP coexista en una interfaz con otro protocolo de enrutamiento, como DVMRP.</span><span class="sxs-lookup"><span data-stu-id="98c64-105">The callbacks enable IGMP to coexist on an interface with another routing protocol, such as DVMRP.</span></span>

<span data-ttu-id="98c64-106">Una vez que cambia la propiedad de una interfaz, el administrador del grupo de multidifusión invoca primero la devolución de llamada de [**\_ devolución de \_ \_ llamada IGMP PMGM**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) .</span><span class="sxs-lookup"><span data-stu-id="98c64-106">After the ownership of an interface changes, the multicast group manager first invokes the [**PMGM\_DISABLE\_IGMP\_CALLBACK**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) callback.</span></span> <span data-ttu-id="98c64-107">IGMP debe dejar de agregar y eliminar pertenencias a grupos en la interfaz especificada hasta que el administrador del grupo de multidifusión invoque la devolución de llamada de [**\_ devolución de \_ \_ llamada de IGMP PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) .</span><span class="sxs-lookup"><span data-stu-id="98c64-107">IGMP must stop adding and deleting group memberships on the specified interface until the multicast group manager invokes the [**PMGM\_ENABLE\_IGMP\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) callback.</span></span>

<span data-ttu-id="98c64-108">El administrador del grupo de multidifusión invoca la devolución de llamada de [**PMGM \_ habilitar \_ IGMP \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) después de completar el cambio de propiedad de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="98c64-108">The multicast group manager invokes the [**PMGM\_ENABLE\_IGMP\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) callback after the change of interface ownership is complete.</span></span>

 

 