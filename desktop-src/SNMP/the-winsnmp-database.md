---
title: La base de datos WinSNMP
description: La implementación de Microsoft WinSNMP mantiene un almacén de información administrativa en una base de datos.
ms.assetid: 0a0d9731-d800-4eaa-8230-25469a0b0285
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea83573cad12c05f6dd4b7e2375df5941e05fadb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486710"
---
# <a name="the-winsnmp-database"></a><span data-ttu-id="e0642-103">La base de datos WinSNMP</span><span class="sxs-lookup"><span data-stu-id="e0642-103">The WinSNMP Database</span></span>

<span data-ttu-id="e0642-104">La implementación de Microsoft WinSNMP mantiene un almacén de información administrativa en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="e0642-104">The Microsoft WinSNMP implementation maintains a store of administrative information in a database.</span></span> <span data-ttu-id="e0642-105">La base de datos incluye la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="e0642-105">The database includes the following information:</span></span>

-   <span data-ttu-id="e0642-106">Propiedades de red y de versión.</span><span class="sxs-lookup"><span data-stu-id="e0642-106">Network and version properties.</span></span>

    <span data-ttu-id="e0642-107">La implementación de utiliza estas propiedades para determinar qué protocolo de transporte de red y versión de SNMP Framework se utiliza para completar las solicitudes de transmisión.</span><span class="sxs-lookup"><span data-stu-id="e0642-107">The implementation uses these properties to determine which network transport protocol and SNMP version framework to use to complete transmission requests.</span></span> <span data-ttu-id="e0642-108">Para obtener más información, consulte [acerca de las versiones de SNMP](about-snmp-versions.md).</span><span class="sxs-lookup"><span data-stu-id="e0642-108">For more information, see [About SNMP Versions](about-snmp-versions.md).</span></span>

-   <span data-ttu-id="e0642-109">Modo de traducción de entidades y contextos.</span><span class="sxs-lookup"><span data-stu-id="e0642-109">Entity and context translation mode.</span></span>

    <span data-ttu-id="e0642-110">La implementación utiliza este modo para interpretar los nombres descriptivos de las entidades y contextos SNMP.</span><span class="sxs-lookup"><span data-stu-id="e0642-110">The implementation uses this mode to interpret user-friendly names for SNMP entities and contexts.</span></span> <span data-ttu-id="e0642-111">Para obtener más información, vea [establecer el modo de traducción de entidades y contextos](setting-the-entity-and-context-translation-mode.md).</span><span class="sxs-lookup"><span data-stu-id="e0642-111">For more information, see [Setting the Entity and Context Translation Mode](setting-the-entity-and-context-translation-mode.md).</span></span>

-   <span data-ttu-id="e0642-112">Configuración de la Directiva de retransmisión.</span><span class="sxs-lookup"><span data-stu-id="e0642-112">Retransmission policy setting.</span></span>

    <span data-ttu-id="e0642-113">La implementación usa esta opción para determinar si debe ejecutar o no la Directiva de retransmisión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e0642-113">The implementation uses this setting to determine whether or not it should execute the application's retransmission policy.</span></span> <span data-ttu-id="e0642-114">La implementación almacena un valor de tiempo de espera y un número de reintentos para cada entidad de destino.</span><span class="sxs-lookup"><span data-stu-id="e0642-114">The implementation stores a time-out value and a retry count for each destination entity.</span></span> <span data-ttu-id="e0642-115">Para obtener más información, vea [acerca de la retransmisión](about-retransmission.md) y [Administración de la Directiva de retransmisión](managing-the-retransmission-policy.md).</span><span class="sxs-lookup"><span data-stu-id="e0642-115">For more information, see [About Retransmission](about-retransmission.md) and [Managing the Retransmission Policy](managing-the-retransmission-policy.md).</span></span>

 

 




