---
description: Un identificador de dispositivo es un identificador independiente de la aplicación para un dispositivo de comunicaciones específico.
ms.assetid: c7ca72a6-97fa-441f-92ce-a4c77a53765c
title: Identificador de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb9c88820ecfe26d3ecd971489d709a34af10f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545462"
---
# <a name="device-identifier"></a><span data-ttu-id="ad2f9-103">Identificador de dispositivo</span><span class="sxs-lookup"><span data-stu-id="ad2f9-103">Device Identifier</span></span>

<span data-ttu-id="ad2f9-104">Un *identificador de dispositivo* es un identificador independiente de la aplicación para un dispositivo de comunicaciones específico.</span><span class="sxs-lookup"><span data-stu-id="ad2f9-104">A *device ID* is an application-independent identifier for a specific communications device.</span></span> <span data-ttu-id="ad2f9-105">Normalmente solo es necesario cuando una aplicación TAPI necesita entregar parte del procesamiento que implica una sesión de comunicaciones a las funciones de una API diferente.</span><span class="sxs-lookup"><span data-stu-id="ad2f9-105">It is typically needed only when a TAPI application needs to hand off part of the processing involving in a communications session to the functions of a different API.</span></span> <span data-ttu-id="ad2f9-106">Por ejemplo, es posible que las aplicaciones TAPI 2,2 no puedan tener acceso directamente a un flujo multimedia y que puedan usar Wave API.</span><span class="sxs-lookup"><span data-stu-id="ad2f9-106">For example, TAPI 2.2 applications may be unable to directly access a media stream and might use the Wave API.</span></span>

<span data-ttu-id="ad2f9-107">**TAPI 2. x:** Vea [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid).</span><span class="sxs-lookup"><span data-stu-id="ad2f9-107">**TAPI 2.x:** See [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid).</span></span>

<span data-ttu-id="ad2f9-108">**TAPI 3. x:** Vea [**ITAddressCapabilities:: get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*AddressCap* establecido en el miembro **AC \_ PERMANENTDEVICEID** de [**la \_ capacidad Address**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)).</span><span class="sxs-lookup"><span data-stu-id="ad2f9-108">**TAPI 3.x:** See [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*AddressCap* set to the **AC\_PERMANENTDEVICEID** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)).</span></span>

 

 
