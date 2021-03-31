---
title: Novedades de SNMP
description: SNMP admite el uso de IPv6 a partir de Windows Vista.
ms.assetid: 38d71c0a-8de1-45a7-958c-aa44411451bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913f71cdf0b23800340f2c43f7b7fa22f45883a2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793486"
---
# <a name="new-in-snmp"></a><span data-ttu-id="42ae9-103">Novedades de SNMP</span><span class="sxs-lookup"><span data-stu-id="42ae9-103">New in SNMP</span></span>

<span data-ttu-id="42ae9-104">\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="42ae9-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="42ae9-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="42ae9-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="42ae9-106">En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]</span><span class="sxs-lookup"><span data-stu-id="42ae9-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="42ae9-107">SNMP admite el uso de IPv6 a partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="42ae9-107">SNMP supports the use of IPv6 starting with Windows Vista.</span></span> <span data-ttu-id="42ae9-108">Sin embargo, SNMP solo es compatible con IPv6 para redes que ejecutan Windows Server 2008 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="42ae9-108">However, SNMP supports IPv6 only for networks running Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="42ae9-109">Esto se debe a que SNMP requiere que la pila de protocolos actualizada esté disponible en estos sistemas operativos para su compatibilidad con IPv6.</span><span class="sxs-lookup"><span data-stu-id="42ae9-109">This is because SNMP requires the updated protocol stack available in these operating systems for its IPv6 support.</span></span>

<span data-ttu-id="42ae9-110">A menos que la red sea únicamente una red de Windows Server 2008, se producirá un error en las comunicaciones IPv6, incluso si una pila de protocolo IPv6 se instala por separado en los equipos que ejecutan versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="42ae9-110">Unless your network is solely a Windows Server 2008 network, IPv6 communications will fail, even if an IPv6 protocol stack is separately installed on those computers that run earlier versions of Windows.</span></span> <span data-ttu-id="42ae9-111">Por ejemplo, los agentes SNMP que se ejecutan en Windows Server 2003 o Windows XP o Windows 2000, solo responden a las consultas que se realizan en sus direcciones IPv4.</span><span class="sxs-lookup"><span data-stu-id="42ae9-111">For example, SNMP agents that run on Windows Server 2003, or Windows XP, or Windows 2000, respond only to queries that are made to their IPv4 addresses.</span></span>

 

 