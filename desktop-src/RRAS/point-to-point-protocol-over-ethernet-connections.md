---
title: Protocolo punto a punto sobre conexiones Ethernet
description: Los sistemas operativos Windows Server 2003, Windows XP y versiones posteriores proporcionan compatibilidad con Protocolo punto a punto sobre Ethernet (PPPoE). En el caso de una conexión PPPoE, establezca los valores siguientes en la estructura RASENTRY.
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed66d3a694896bdec9e0f53215a782d5896cd38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995555"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a><span data-ttu-id="3d28e-104">Protocolo punto a punto sobre conexiones Ethernet</span><span class="sxs-lookup"><span data-stu-id="3d28e-104">Point-to-Point Protocol over Ethernet Connections</span></span>

<span data-ttu-id="3d28e-105">Los sistemas operativos Windows Server 2003, Windows XP y versiones posteriores proporcionan compatibilidad con Protocolo punto a punto sobre Ethernet (PPPoE).</span><span class="sxs-lookup"><span data-stu-id="3d28e-105">Windows Server 2003, Windows XP, and later operating systems provide support for Point-to-Point Protocol over Ethernet (PPPoE).</span></span> <span data-ttu-id="3d28e-106">En el caso de una conexión PPPoE, establezca los valores siguientes en la estructura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3d28e-106">For a PPPoE connection, set the following values in the [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) structure.</span></span>



| <span data-ttu-id="3d28e-107">Miembro</span><span class="sxs-lookup"><span data-stu-id="3d28e-107">Member</span></span>                      | <span data-ttu-id="3d28e-108">Valor</span><span class="sxs-lookup"><span data-stu-id="3d28e-108">Value</span></span>             |
|-----------------------------|-------------------|
| <span data-ttu-id="3d28e-109">RASENTRY.dwType</span><span class="sxs-lookup"><span data-stu-id="3d28e-109">RASENTRY.dwType</span></span>             | <span data-ttu-id="3d28e-110">\_Banda ancha Raset</span><span class="sxs-lookup"><span data-stu-id="3d28e-110">RASET\_Broadband</span></span>  |
| <span data-ttu-id="3d28e-111">RAENTRY.szDeviceType</span><span class="sxs-lookup"><span data-stu-id="3d28e-111">RAENTRY.szDeviceType</span></span>        | <span data-ttu-id="3d28e-112">RASDT \_ PPPoE</span><span class="sxs-lookup"><span data-stu-id="3d28e-112">RASDT\_PPPoE</span></span>      |
| <span data-ttu-id="3d28e-113">RASENTRY.szLocalPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="3d28e-113">RASENTRY.szLocalPhoneNumber</span></span> | <span data-ttu-id="3d28e-114">Nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="3d28e-114">The service name.</span></span> |



 

<span data-ttu-id="3d28e-115">Utilice la función [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para establecer estos valores.</span><span class="sxs-lookup"><span data-stu-id="3d28e-115">Use the [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) function to set these values.</span></span>

<span data-ttu-id="3d28e-116">También puede usar [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) y la marca RASEDFLAG \_ NewBroadbandEntry para [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) para mostrar un asistente para crear una entrada de libreta de teléfonos de PPPoE.</span><span class="sxs-lookup"><span data-stu-id="3d28e-116">You can also use [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) and the RASEDFLAG\_NewBroadbandEntry flag for [**RASENTRYDLG**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) to display a wizard for creating a PPPoE phonebook entry.</span></span>

 

 