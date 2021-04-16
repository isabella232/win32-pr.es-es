---
title: Tipos de enumeración de API de Servicios de Escritorio remoto
description: Enumera los tipos de enumeración que se usan con la API de Servicios de Escritorio remoto.
ms.assetid: b5ef61e2-07fa-4963-9b9b-977cc04dab10
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9523a7528fddff4e2dbcf6dde16c29084d4811d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357255"
---
# <a name="remote-desktop-services-api-enumeration-types"></a><span data-ttu-id="1490d-103">Tipos de enumeración de API de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="1490d-103">Remote Desktop Services API Enumeration Types</span></span>

<span data-ttu-id="1490d-104">Se usan los siguientes tipos de enumeración con la API de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="1490d-104">The following enumeration types are used with the Remote Desktop Services API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1490d-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="1490d-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="1490d-106">**\_clase de configuración de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="1490d-106">**WTS\_CONFIG\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_config_class)
</dt> <dd>

<span data-ttu-id="1490d-107">Contiene valores que indican el tipo de información de configuración de usuario que se va a establecer o recuperar en una llamada a las funciones [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) y [**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga) .</span><span class="sxs-lookup"><span data-stu-id="1490d-107">Contains values that indicate the type of user configuration information to set or retrieve in a call to the [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) and [**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="1490d-108">**\_origen de configuración de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="1490d-108">**WTS\_CONFIG\_SOURCE**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_config_source)
</dt> <dd>

<span data-ttu-id="1490d-109">Especifica el origen de la información de configuración devuelta por la función [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) .</span><span class="sxs-lookup"><span data-stu-id="1490d-109">Specifies the source of configuration information returned by the [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) function.</span></span>

</dd> <dt>

[<span data-ttu-id="1490d-110">**\_clase CONNECTSTATE de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="1490d-110">**WTS\_CONNECTSTATE\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_connectstate_class)
</dt> <dd>

<span data-ttu-id="1490d-111">Especifica el estado de conexión de una sesión de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="1490d-111">Specifies the connection state of a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="1490d-112">**\_clase de información de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="1490d-112">**WTS\_INFO\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_info_class)
</dt> <dd>

<span data-ttu-id="1490d-113">Contiene valores que indican el tipo de información de sesión que se va a recuperar en una llamada a la función [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) .</span><span class="sxs-lookup"><span data-stu-id="1490d-113">Contains values that indicate the type of session information to retrieve in a call to the [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) function.</span></span>

</dd> <dt>

[<span data-ttu-id="1490d-114">**\_clase de tipo WTS \_**</span><span class="sxs-lookup"><span data-stu-id="1490d-114">**WTS\_TYPE\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_type_class)
</dt> <dd>

<span data-ttu-id="1490d-115">Especifica el tipo de estructura que una función Servicios de Escritorio remoto ha devuelto en un búfer.</span><span class="sxs-lookup"><span data-stu-id="1490d-115">Specifies the type of structure that a Remote Desktop Services function has returned in a buffer.</span></span>

</dd> <dt>

[<span data-ttu-id="1490d-116">**\_clase virtual de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="1490d-116">**WTS\_VIRTUAL\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_virtual_class)
</dt> <dd>

<span data-ttu-id="1490d-117">Contiene valores que indican el tipo de información de canal virtual que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="1490d-117">Contains values that indicate the type of virtual channel information to retrieve.</span></span>

</dd> <dt>

[<span data-ttu-id="1490d-118">**\_familia de direcciones WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="1490d-118">**WTSSBX\_ADDRESS\_FAMILY**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_address_family)
</dt> <dd>

<span data-ttu-id="1490d-119">Contiene valores que indican la familia de direcciones de una dirección de red que se utiliza para la redirección.</span><span class="sxs-lookup"><span data-stu-id="1490d-119">Contains values that indicate the address family of a network address that is being used for redirection.</span></span>

</dd> <dt>

[<span data-ttu-id="1490d-120">**\_consumo de máquina WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="1490d-120">**WTSSBX\_MACHINE\_DRAIN**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_drain)
</dt> <dd>

<span data-ttu-id="1490d-121">Contiene valores que indican el estado de purga de un servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="1490d-121">Contains values that indicate the drain state of a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="1490d-122">**\_modo de \_ sesión de equipo WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="1490d-122">**WTSSBX\_MACHINE\_SESSION\_MODE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_session_mode)
</dt> <dd>

<span data-ttu-id="1490d-123">Contiene valores que indican el modo de sesión de un servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="1490d-123">Contains values that indicate the session mode of a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="1490d-124">**Estado de la \_ máquina WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="1490d-124">**WTSSBX\_MACHINE\_STATE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_state)
</dt> <dd>

<span data-ttu-id="1490d-125">Contiene valores que indican el estado actual de un servidor.</span><span class="sxs-lookup"><span data-stu-id="1490d-125">Contains values that indicate the current state of a server.</span></span>

</dd> <dt>

[<span data-ttu-id="1490d-126">**\_tipo de notificación WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="1490d-126">**WTSSBX\_NOTIFICATION\_TYPE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_notification_type)
</dt> <dd>

<span data-ttu-id="1490d-127">Contiene valores que indican el tipo de cambio de estado que se produjo en un servidor host de sesión de escritorio remoto o en una sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="1490d-127">Contains values that indicate the type of status change that occurred on a RD Session Host server or a user session.</span></span>

</dd> <dt>

[<span data-ttu-id="1490d-128">**\_Estado de sesión de WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="1490d-128">**WTSSBX\_SESSION\_STATE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_session_state)
</dt> <dd>

<span data-ttu-id="1490d-129">Contiene valores que indican el estado de conexión de una sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="1490d-129">Contains values that indicate the connection state of a user session.</span></span>

</dd> </dl>

 

 




