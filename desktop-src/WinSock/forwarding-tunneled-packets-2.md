---
description: Existe una limitación en el código que recibe paquetes encapsulados (tunelizados) y los desmultiplexa en una interfaz específica.
ms.assetid: 6148fca7-adf4-460d-afd6-79c43285af6c
title: Paquetes de túnel de reenvío IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95f88a90a358317cf46516808a96f93b792dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907950"
---
# <a name="ipv6-forwarding-tunneled-packets"></a><span data-ttu-id="34085-103">Paquetes de túnel de reenvío IPv6</span><span class="sxs-lookup"><span data-stu-id="34085-103">IPv6 Forwarding Tunneled Packets</span></span>

<span data-ttu-id="34085-104">Existe una limitación en el código que recibe paquetes encapsulados (tunelizados) y los desmultiplexa en una interfaz específica.</span><span class="sxs-lookup"><span data-stu-id="34085-104">There is a limitation in the code that receives encapsulated (tunneled) packets and demultiplexes them to a specific interface.</span></span> <span data-ttu-id="34085-105">Si desea reenviar los paquetes de túnel recibidos a través de un túnel configurado, es necesario habilitar el reenvío en cualquier interfaz de 6 a 4, así como en la interfaz \# 2.</span><span class="sxs-lookup"><span data-stu-id="34085-105">If you want to forward tunneled packets received through a configured tunnel, then it is necessary to enable forwarding on any 6-over-4 interfaces as well as interface \#2.</span></span> <span data-ttu-id="34085-106">Simplemente habilitar el reenvío en la interfaz \# 2 no funcionará.</span><span class="sxs-lookup"><span data-stu-id="34085-106">Just enabling forwarding on interface \#2 will not work.</span></span> <span data-ttu-id="34085-107">Normalmente, al configurar un enrutador, se habilita el reenvío en todas las interfaces excepto en bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="34085-107">Typically when configuring a router, you would enable forwarding on all interfaces except loopback.</span></span>

 

 



