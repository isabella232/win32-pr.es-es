---
title: Comparación de funciones de Windows 2000 frente a RRAS Redistributable
description: La API de RAS se distribuye como una característica de los sistemas operativos Windows 2000 y versiones posteriores y está disponible como paquete redistribuible para Windows NT 4,0 con Service Pack 3 (SP3) y versiones anteriores.
ms.assetid: fd6c76b9-52e2-405e-b62e-055cfbdb5ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 745ad0c50654c8269c3e62b03629a7ae12a17476
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105651322"
---
# <a name="function-comparison-windows-2000-vs-rras-redistributable"></a><span data-ttu-id="94e59-103">Comparación de funciones: Windows 2000 frente a RRAS Redistributable</span><span class="sxs-lookup"><span data-stu-id="94e59-103">Function Comparison: Windows 2000 vs. RRAS Redistributable</span></span>

<span data-ttu-id="94e59-104">La API de RAS se distribuye como una característica de los sistemas operativos Windows 2000 y versiones posteriores y está disponible como paquete redistribuible para Windows NT 4,0 con Service Pack 3 (SP3) y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="94e59-104">The RAS API is distributed as a feature of Windows 2000 and later operating systems and is available as a redistributable for Windows NT 4.0 with Service Pack 3 (SP3) and earlier.</span></span> <span data-ttu-id="94e59-105">RAS proporciona la misma funcionalidad en ambas formas, pero la Convención de nomenclatura que se usa es diferente para los elementos de referencia de cada versión de la API de RAS.</span><span class="sxs-lookup"><span data-stu-id="94e59-105">RAS provides the same functionality in both of these forms but the naming convention that is used is different for the reference elements in each version of the RAS API.</span></span>

<span data-ttu-id="94e59-106">Las funciones RAS para Windows NT 4,0 con SP3 y versiones anteriores normalmente comienzan con el prefijo "RasAdmin".</span><span class="sxs-lookup"><span data-stu-id="94e59-106">The RAS functions for Windows NT 4.0 with SP3 and earlier typically begin with the "RasAdmin" prefix.</span></span> <span data-ttu-id="94e59-107">Las funciones análogas para el servicio de enrutamiento y acceso remoto (RRAS) comienzan con el prefijo "MprAdmin".</span><span class="sxs-lookup"><span data-stu-id="94e59-107">The analogous functions for Routing and Remote Access Service (RRAS) begin with the "MprAdmin" prefix.</span></span> <span data-ttu-id="94e59-108">Por ejemplo, RAS proporciona una función denominada [**RasAdminPortGetInfo**](rasadminportgetinfo.md).</span><span class="sxs-lookup"><span data-stu-id="94e59-108">For example, RAS provides a function called [**RasAdminPortGetInfo**](rasadminportgetinfo.md).</span></span> <span data-ttu-id="94e59-109">La función análoga en RRAS se denomina [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo).</span><span class="sxs-lookup"><span data-stu-id="94e59-109">The analogous function in RRAS is called [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo).</span></span> <span data-ttu-id="94e59-110">Como ejemplo similar, RAS proporciona la función de devolución de llamada [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span><span class="sxs-lookup"><span data-stu-id="94e59-110">As a similar example, RAS provides the callback function [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span></span> <span data-ttu-id="94e59-111">RRAS proporciona una función de devolución de llamada similar denominada [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser).</span><span class="sxs-lookup"><span data-stu-id="94e59-111">RRAS provides a similar callback function called [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser).</span></span> <span data-ttu-id="94e59-112">Las excepciones a esta regla son [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md), que en RRAS es [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)y [**RasAdminFreeBuffer**](rasadminfreebuffer.md), que en RRAS es [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree).</span><span class="sxs-lookup"><span data-stu-id="94e59-112">Exceptions to this rule are [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md), which under RRAS is [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats), and [**RasAdminFreeBuffer**](rasadminfreebuffer.md), which under RRAS is [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree).</span></span>

<span data-ttu-id="94e59-113">En la tabla siguiente se enumeran las funciones RAS de Windows NT 4,0 SP3 y las funciones RRAS correspondientes.</span><span class="sxs-lookup"><span data-stu-id="94e59-113">The following table lists the Windows NT 4.0 SP3 RAS functions and the corresponding RRAS functions.</span></span>



| <span data-ttu-id="94e59-114">Windows NT 4,0 RAS</span><span class="sxs-lookup"><span data-stu-id="94e59-114">Windows NT 4.0 RAS</span></span>                                                                   | <span data-ttu-id="94e59-115">RRAS</span><span class="sxs-lookup"><span data-stu-id="94e59-115">RRAS</span></span>                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="94e59-116">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="94e59-116">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)                   | [<span data-ttu-id="94e59-117">**MprAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="94e59-117">**MprAdminAcceptNewConnection**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection)                   |
| [<span data-ttu-id="94e59-118">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="94e59-118">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md) | [<span data-ttu-id="94e59-119">**MprAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="94e59-119">**MprAdminConnectionHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) |
| [<span data-ttu-id="94e59-120">**RasAdminFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="94e59-120">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)                                     | [<span data-ttu-id="94e59-121">**MprAdminBufferFree**</span><span class="sxs-lookup"><span data-stu-id="94e59-121">**MprAdminBufferFree**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)                                     |
| [<span data-ttu-id="94e59-122">**RasAdminGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="94e59-122">**RasAdminGetErrorString**</span></span>](rasadmingeterrorstring.md)                             | [<span data-ttu-id="94e59-123">**MprAdminGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="94e59-123">**MprAdminGetErrorString**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)                             |
| [<span data-ttu-id="94e59-124">**RasAdminGetIpAddressForUser**</span><span class="sxs-lookup"><span data-stu-id="94e59-124">**RasAdminGetIpAddressForUser**</span></span>](rasadmingetipaddressforuser.md)                   | [<span data-ttu-id="94e59-125">**MprAdminGetIpAddressForUser**</span><span class="sxs-lookup"><span data-stu-id="94e59-125">**MprAdminGetIpAddressForUser**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser)                   |
| [<span data-ttu-id="94e59-126">**RasAdminPortClearStatistics**</span><span class="sxs-lookup"><span data-stu-id="94e59-126">**RasAdminPortClearStatistics**</span></span>](rasadminportclearstatistics.md)                   | [<span data-ttu-id="94e59-127">**MprAdminPortClearStats**</span><span class="sxs-lookup"><span data-stu-id="94e59-127">**MprAdminPortClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)                             |
| [<span data-ttu-id="94e59-128">**RasAdminPortDisconnect**</span><span class="sxs-lookup"><span data-stu-id="94e59-128">**RasAdminPortDisconnect**</span></span>](rasadminportdisconnect.md)                             | [<span data-ttu-id="94e59-129">**MprAdminPortDisconnect**</span><span class="sxs-lookup"><span data-stu-id="94e59-129">**MprAdminPortDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)                             |
| [<span data-ttu-id="94e59-130">**RasAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="94e59-130">**RasAdminPortEnum**</span></span>](rasadminportenum.md)                                         | [<span data-ttu-id="94e59-131">**MprAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="94e59-131">**MprAdminPortEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)                                         |
| [<span data-ttu-id="94e59-132">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="94e59-132">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)                                   | [<span data-ttu-id="94e59-133">**MprAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="94e59-133">**MprAdminPortGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)                                   |
| [<span data-ttu-id="94e59-134">**RasAdminReleaseIpAddress**</span><span class="sxs-lookup"><span data-stu-id="94e59-134">**RasAdminReleaseIpAddress**</span></span>](rasadminreleaseipaddress.md)                         | [<span data-ttu-id="94e59-135">**MprAdminReleaseIpAddress**</span><span class="sxs-lookup"><span data-stu-id="94e59-135">**MprAdminReleaseIpAddress**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)                         |
| [<span data-ttu-id="94e59-136">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="94e59-136">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)                                   | [<span data-ttu-id="94e59-137">**MprAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="94e59-137">**MprAdminUserGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)                                   |
| [<span data-ttu-id="94e59-138">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="94e59-138">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)                                   | [<span data-ttu-id="94e59-139">**MprAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="94e59-139">**MprAdminUserSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)                                   |



 

<span data-ttu-id="94e59-140">Aunque las funciones RRAS son similares a las de Windows NT 4,0 con SP3 y versiones anteriores de RAS en la funcionalidad, las funciones RRAS suelen tomar un conjunto diferente de parámetros.</span><span class="sxs-lookup"><span data-stu-id="94e59-140">Although the RRAS functions are similar to their Windows NT 4.0 with SP3 and earlier RAS counterparts in functionality, RRAS functions often take a different set of parameters.</span></span> <span data-ttu-id="94e59-141">Vea la página de referencia de una función determinada para obtener información completa sobre la lista de parámetros de esa función.</span><span class="sxs-lookup"><span data-stu-id="94e59-141">See the reference page for a particular function for complete information on that function's parameter list.</span></span>

<span data-ttu-id="94e59-142">RRAS Redistributable para Windows NT 4,0 con SP3 y versiones anteriores agrega las siguientes funciones, que no tienen homólogos RAS:</span><span class="sxs-lookup"><span data-stu-id="94e59-142">The RRAS redistributable for Windows NT 4.0 with SP3 and earlier adds the following functions, which have no RAS counterparts:</span></span>

[<span data-ttu-id="94e59-143">**MprAdminAcceptNewLink**</span><span class="sxs-lookup"><span data-stu-id="94e59-143">**MprAdminAcceptNewLink**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[<span data-ttu-id="94e59-144">**MprAdminConnectionClearStats**</span><span class="sxs-lookup"><span data-stu-id="94e59-144">**MprAdminConnectionClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)

[<span data-ttu-id="94e59-145">**MprAdminConnectionEnum**</span><span class="sxs-lookup"><span data-stu-id="94e59-145">**MprAdminConnectionEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)

[<span data-ttu-id="94e59-146">**MprAdminConnectionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="94e59-146">**MprAdminConnectionGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)

[<span data-ttu-id="94e59-147">**MprAdminGetPDCServer**</span><span class="sxs-lookup"><span data-stu-id="94e59-147">**MprAdminGetPDCServer**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)

[<span data-ttu-id="94e59-148">**MprAdminIsServiceRunning**</span><span class="sxs-lookup"><span data-stu-id="94e59-148">**MprAdminIsServiceRunning**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)

[<span data-ttu-id="94e59-149">**MprAdminLinkHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="94e59-149">**MprAdminLinkHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[<span data-ttu-id="94e59-150">**MprAdminPortReset**</span><span class="sxs-lookup"><span data-stu-id="94e59-150">**MprAdminPortReset**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

[<span data-ttu-id="94e59-151">**MprAdminServerConnect**</span><span class="sxs-lookup"><span data-stu-id="94e59-151">**MprAdminServerConnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)

[<span data-ttu-id="94e59-152">**MprAdminServerDisconnect**</span><span class="sxs-lookup"><span data-stu-id="94e59-152">**MprAdminServerDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

<span data-ttu-id="94e59-153">Además de las funciones anteriores, Windows 2000 y los sistemas operativos posteriores agregan las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="94e59-153">In addition to the preceding functions, Windows 2000 and later operating systems add the following functions:</span></span>

[<span data-ttu-id="94e59-154">**MprAdminSendUserMessage**</span><span class="sxs-lookup"><span data-stu-id="94e59-154">**MprAdminSendUserMessage**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)

[<span data-ttu-id="94e59-155">**MprAdminAcceptNewConnection2**</span><span class="sxs-lookup"><span data-stu-id="94e59-155">**MprAdminAcceptNewConnection2**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)

[<span data-ttu-id="94e59-156">**MprAdminConnectionHangupNotification2**</span><span class="sxs-lookup"><span data-stu-id="94e59-156">**MprAdminConnectionHangupNotification2**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

 

 




