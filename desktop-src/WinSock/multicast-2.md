---
description: Las funciones Multipoint de Winsock genéricas admiten la multidifusión IP.
ms.assetid: 32fffca8-4f13-495b-afb6-bb57a9cce553
title: Multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c6b4ece06119d01e2661028f452985bb20b068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154267"
---
# <a name="multicast"></a><span data-ttu-id="6aba8-103">Multidifusión</span><span class="sxs-lookup"><span data-stu-id="6aba8-103">Multicast</span></span>

<span data-ttu-id="6aba8-104">Las funciones Multipoint de Winsock genéricas admiten la multidifusión IP.</span><span class="sxs-lookup"><span data-stu-id="6aba8-104">Generic Winsock multipoint functions support IP multicast.</span></span> <span data-ttu-id="6aba8-105">Sin embargo, los proveedores de transporte TCP/IP que admiten multidifusión también deben proporcionar el estilo de distribución de software Berkeley (BSD): compatibilidad con multidifusión admitiendo las opciones de multidifusión correspondientes.</span><span class="sxs-lookup"><span data-stu-id="6aba8-105">However, the TCP/IP transport providers that support multicast must also provide Berkeley Software Distribution (BSD) style–multicast support by supporting the corresponding multicast options.</span></span> <span data-ttu-id="6aba8-106">Esto simplifica la migración de aplicaciones de multidifusión existentes a Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="6aba8-106">This simplifies the porting of existing multicast applications to Windows Sockets 2.</span></span>

 

 



