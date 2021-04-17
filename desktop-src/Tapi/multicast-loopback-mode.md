---
description: La \_ enumeración de modo de bucle invertido de multidifusión \_ describe el modo de bucle invertido.
ms.assetid: bf9c3665-71cc-4cde-9ad4-1a8b62eddf9f
title: Enumeración MULTICAST_LOOPBACK_MODE (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a15505efcd1a9e399866b104da0582ccf846689
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691114"
---
# <a name="multicast_loopback_mode-enumeration"></a><span data-ttu-id="5ec9d-103">\_Enumeración de modo de bucle invertido \_</span><span class="sxs-lookup"><span data-stu-id="5ec9d-103">MULTICAST\_LOOPBACK\_MODE enumeration</span></span>

<span data-ttu-id="5ec9d-104">\[**Multidifusión \_ El \_ modo de bucle invertido** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5ec9d-104">\[**MULTICAST\_LOOPBACK\_MODE** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5ec9d-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="5ec9d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5ec9d-106">La enumeración de **\_ \_ modo de bucle invertido de multidifusión** describe el modo de bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="5ec9d-106">The **MULTICAST\_LOOPBACK\_MODE** enum describes the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ec9d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ec9d-107">Syntax</span></span>


```C++
} MULTICAST_LOOPBACK_MODE;
```



## <a name="constants"></a><span data-ttu-id="5ec9d-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="5ec9d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5ec9d-109"><span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM \_ sin \_ bucle invertido**</span><span class="sxs-lookup"><span data-stu-id="5ec9d-109"><span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM\_NO\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="5ec9d-110">Bucle invertido de multidifusión deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="5ec9d-110">Multicast loopback is disabled.</span></span> <span data-ttu-id="5ec9d-111">Esto significa que dos aplicaciones en el mismo equipo que se unen al mismo grupo de multidifusión pueden obtener los paquetes de los demás.</span><span class="sxs-lookup"><span data-stu-id="5ec9d-111">That means two applications on the same machine joining the same multicast group can get each other's packets.</span></span>

</dd> <dt>

<span data-ttu-id="5ec9d-112"><span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**\_ \_ bucle invertido completo mm**</span><span class="sxs-lookup"><span data-stu-id="5ec9d-112"><span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**MM\_FULL\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="5ec9d-113">También se recorren en bucle todos los paquetes enviados.</span><span class="sxs-lookup"><span data-stu-id="5ec9d-113">All the packets sent out are looped back as well.</span></span> <span data-ttu-id="5ec9d-114">Este modo solo es útil para realizar pruebas.</span><span class="sxs-lookup"><span data-stu-id="5ec9d-114">This mode is useful only for testing.</span></span>

</dd> <dt>

<span data-ttu-id="5ec9d-115"><span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**\_ \_ bucle invertido de mm selectivo**</span><span class="sxs-lookup"><span data-stu-id="5ec9d-115"><span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**MM\_SELECTIVE\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="5ec9d-116">El bucle invertido selectivo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="5ec9d-116">Selective loopback is enabled.</span></span> <span data-ttu-id="5ec9d-117">Esto significa que varias aplicaciones habilitadas en un equipo pueden unirse al mismo grupo de multidifusión sin confusión.</span><span class="sxs-lookup"><span data-stu-id="5ec9d-117">That means enabled multiple applications on one machine can join the same multicast group without confusion.</span></span> <span data-ttu-id="5ec9d-118">Los paquetes se recorren en bucle desde la pila y cada sesión de RTP es responsable de filtrar los paquetes no deseados.</span><span class="sxs-lookup"><span data-stu-id="5ec9d-118">The packets are looped back from the stack and each RTP session is responsible for filtering out unwanted packets.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ec9d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ec9d-119">Requirements</span></span>



| <span data-ttu-id="5ec9d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ec9d-120">Requirement</span></span> | <span data-ttu-id="5ec9d-121">Value</span><span class="sxs-lookup"><span data-stu-id="5ec9d-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec9d-122">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="5ec9d-122">TAPI version</span></span><br/> | <span data-ttu-id="5ec9d-123">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="5ec9d-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5ec9d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ec9d-124">Header</span></span><br/>       | <dl> <span data-ttu-id="5ec9d-125"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ec9d-125"><dt>Confpriv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ec9d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ec9d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ec9d-127">**IMulticastControl:: get \_ LoopbackMode**</span><span class="sxs-lookup"><span data-stu-id="5ec9d-127">**IMulticastControl::get\_LoopbackMode**</span></span>](imulticastcontrol-get-loopbackmode.md)
</dt> <dt>

[<span data-ttu-id="5ec9d-128">**IMulticastControl::p UT \_ LoopbackMode**</span><span class="sxs-lookup"><span data-stu-id="5ec9d-128">**IMulticastControl::put\_LoopbackMode**</span></span>](imulticastcontrol-put-loopbackmode.md)
</dt> </dl>

 

 




