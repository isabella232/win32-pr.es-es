---
title: Establecer una conexión de acceso telefónico a Internet
description: Las siguientes funciones se usan para controlar las conexiones de módem.
ms.assetid: dd33ed4b-eb7c-449c-b309-8f5c290a5a93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce03ecc67e27c67bb9807f473aac5210b03f755
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078234"
---
# <a name="establishing-a-dial-up-connection-to-the-internet"></a><span data-ttu-id="7ecb0-103">Establecer una conexión de acceso telefónico a Internet</span><span class="sxs-lookup"><span data-stu-id="7ecb0-103">Establishing a Dial-Up Connection to the Internet</span></span>

<span data-ttu-id="7ecb0-104">Las siguientes funciones se usan para controlar las conexiones de módem.</span><span class="sxs-lookup"><span data-stu-id="7ecb0-104">The following functions are used to handle modem connections.</span></span>

-   [<span data-ttu-id="7ecb0-105">**InternetAutodial**</span><span class="sxs-lookup"><span data-stu-id="7ecb0-105">**InternetAutodial**</span></span>](/windows/win32/api/winineti/nf-winineti-internetautodial)
-   [<span data-ttu-id="7ecb0-106">**InternetAutodialHangup**</span><span class="sxs-lookup"><span data-stu-id="7ecb0-106">**InternetAutodialHangup**</span></span>](/windows/win32/api/winineti/nf-winineti-internetautodialhangup)
-   [<span data-ttu-id="7ecb0-107">**InternetDial**</span><span class="sxs-lookup"><span data-stu-id="7ecb0-107">**InternetDial**</span></span>](/windows/win32/api/winineti/nf-winineti-internetdial)
-   [<span data-ttu-id="7ecb0-108">**InternetGetConnectedState**</span><span class="sxs-lookup"><span data-stu-id="7ecb0-108">**InternetGetConnectedState**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstate)
-   [<span data-ttu-id="7ecb0-109">**InternetGetConnectedStateEx**</span><span class="sxs-lookup"><span data-stu-id="7ecb0-109">**InternetGetConnectedStateEx**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstateex)
-   [<span data-ttu-id="7ecb0-110">**InternetHangUp**</span><span class="sxs-lookup"><span data-stu-id="7ecb0-110">**InternetHangUp**</span></span>](/windows/win32/api/winineti/nf-winineti-internethangup)
-   [<span data-ttu-id="7ecb0-111">**InternetGoOnline**</span><span class="sxs-lookup"><span data-stu-id="7ecb0-111">**InternetGoOnline**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgoonline)

> [!Note]  
> <span data-ttu-id="7ecb0-112">Las funciones de acceso telefónico de WinINet no admiten conexiones de doble marcado, autenticación de tarjeta inteligente ni conexiones que requieran certificación basada en el registro.</span><span class="sxs-lookup"><span data-stu-id="7ecb0-112">WinINet dial-up functions do not support double-dial connections, SmartCard authentication, or connections that require registry-based certification.</span></span>

 

> [!Note]  
> <span data-ttu-id="7ecb0-113">A partir de Windows Vista y Windows Server 2008, las funciones de acceso telefónico de WinINet usan las [funciones RAS](/windows/desktop/RRAS/remote-access-service-functions) para establecer una conexión de acceso telefónico.</span><span class="sxs-lookup"><span data-stu-id="7ecb0-113">Starting on Windows Vista and Windows Server 2008, the WinINet dial-up functions use the [RAS functions](/windows/desktop/RRAS/remote-access-service-functions) to establish a dial-up connection.</span></span> <span data-ttu-id="7ecb0-114">WinINet admite la funcionalidad documentada en la función [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) .</span><span class="sxs-lookup"><span data-stu-id="7ecb0-114">WinINet supports the functionality documented in the [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) function.</span></span>

 

> [!Note]  
> <span data-ttu-id="7ecb0-115">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="7ecb0-115">WinINet does not support server implementations.</span></span> <span data-ttu-id="7ecb0-116">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="7ecb0-116">In addition, it should not be used from a service.</span></span> <span data-ttu-id="7ecb0-117">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="7ecb0-117">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 