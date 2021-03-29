---
title: Funciones DLL de administración de RAS
description: 'Un archivo DLL de administración de RAS debe implementar y exportar todas las funciones siguientes:'
ms.assetid: bf2bd4d4-6da2-471e-843c-c0f0563d3795
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a02c8dc9212f3cfd173c9a236f81fcf766658424
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792975"
---
# <a name="ras-administration-dll-functions"></a><span data-ttu-id="a9124-103">Funciones DLL de administración de RAS</span><span class="sxs-lookup"><span data-stu-id="a9124-103">RAS administration DLL functions</span></span>

<span data-ttu-id="a9124-104">Un archivo DLL de administración de RAS debe implementar y exportar todas las funciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="a9124-104">A RAS administration DLL must implement and export all of the following functions:</span></span>

-   [<span data-ttu-id="a9124-105">**MprAdminAcceptNewLink**</span><span class="sxs-lookup"><span data-stu-id="a9124-105">**MprAdminAcceptNewLink**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)
-   <span data-ttu-id="a9124-106">[**MprAdminAcceptReauthentication**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthentication) o [ **MprAdminAcceptReauthenticationEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthenticationex)</span><span class="sxs-lookup"><span data-stu-id="a9124-106">[**MprAdminAcceptReauthentication**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthentication) or [**MprAdminAcceptReauthenticationEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthenticationex)</span></span>
-   <span data-ttu-id="a9124-107">[**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) o [ **MprAdminInitializeDllEx**](/windows/win32/api/mprapi/nf-mprapi-mpradmininitializedllex)</span><span class="sxs-lookup"><span data-stu-id="a9124-107">[**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) or [**MprAdminInitializeDllEx**](/windows/win32/api/mprapi/nf-mprapi-mpradmininitializedllex)</span></span>
-   [<span data-ttu-id="a9124-108">**MprAdminLinkHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="a9124-108">**MprAdminLinkHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)
-   [<span data-ttu-id="a9124-109">**MprAdminTerminateDll**</span><span class="sxs-lookup"><span data-stu-id="a9124-109">**MprAdminTerminateDll**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll)

<span data-ttu-id="a9124-110">**Windows 2000/NT:** La DLL de administración de RAS también debe implementar y exportar el siguiente par de funciones: [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) y [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span><span class="sxs-lookup"><span data-stu-id="a9124-110">**Windows 2000/NT:** The RAS administration DLL must also implement and export the following pair of functions: [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) and [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span></span>

<span data-ttu-id="a9124-111">Además, la DLL de administración de RAS debe implementar y exportar uno de los siguientes pares de funciones:</span><span class="sxs-lookup"><span data-stu-id="a9124-111">In addition, the RAS administration DLL must implement and export one of the following pairs of functions:</span></span>

-   <span data-ttu-id="a9124-112">[**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) y [ **MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)</span><span class="sxs-lookup"><span data-stu-id="a9124-112">[**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) and [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)</span></span>
-   <span data-ttu-id="a9124-113">[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) y [ **MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)</span><span class="sxs-lookup"><span data-stu-id="a9124-113">[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) and [**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)</span></span>
-   <span data-ttu-id="a9124-114">[**MprAdminAcceptNewConnection3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection3) y [ **MprAdminConnectionHangupNotification3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification3)</span><span class="sxs-lookup"><span data-stu-id="a9124-114">[**MprAdminAcceptNewConnection3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection3) and [**MprAdminConnectionHangupNotification3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification3)</span></span>
-   <span data-ttu-id="a9124-115">[**MprAdminAcceptNewConnectionEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnectionex) y [ **MprAdminConnectionHangupNotificationEx**](/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotificationex)</span><span class="sxs-lookup"><span data-stu-id="a9124-115">[**MprAdminAcceptNewConnectionEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnectionex) and [**MprAdminConnectionHangupNotificationEx**](/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotificationex)</span></span>

<span data-ttu-id="a9124-116">Si no se implementa una de las funciones necesarias, el servicio de acceso remoto no se inicia.</span><span class="sxs-lookup"><span data-stu-id="a9124-116">If one of the required functions is not implemented, the remote access service fails to start.</span></span>

<span data-ttu-id="a9124-117">No es necesario que un archivo DLL de administración implemente los siguientes pares de funciones:</span><span class="sxs-lookup"><span data-stu-id="a9124-117">An administration DLL is not required to implement the following pairs of functions:</span></span>

-   <span data-ttu-id="a9124-118">[**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) y [ **MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span><span class="sxs-lookup"><span data-stu-id="a9124-118">[**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) and [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)</span></span>
-   <span data-ttu-id="a9124-119">[*MprAdminGetIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipv6addressforuser) y [ *MprAdminReleaseIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipv6addressforuser)</span><span class="sxs-lookup"><span data-stu-id="a9124-119">[*MprAdminGetIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipv6addressforuser) and [*MprAdminReleaseIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipv6addressforuser)</span></span>

<span data-ttu-id="a9124-120">Sin embargo, si el archivo DLL implementa una función en un par enumerado anteriormente, también debe implementar la otra función en el par.</span><span class="sxs-lookup"><span data-stu-id="a9124-120">However, if the DLL implements one function in a pair listed above, it must implement the other function in the pair as well.</span></span>

<span data-ttu-id="a9124-121">Para obtener más información acerca de los archivos dll de administración de RAS, consulte el tema de información general, [dll de administración de Ras](ras-administration-dll.md).</span><span class="sxs-lookup"><span data-stu-id="a9124-121">For more information on RAS Administration DLLs, see the overview topic, [RAS Administration DLL](ras-administration-dll.md).</span></span>

 

 