---
title: Referencia de la interfaz de protocolo de enrutamiento
description: En esta documentación se describen las funciones y estructuras que se usan para implementar un protocolo de enrutamiento como un archivo DLL de modo usuario.
ms.assetid: 0429f5ca-6574-48f5-85ab-70b4677ca539
keywords:
- Servicio de enrutamiento y acceso remoto RRAS, interfaz de protocolo de enrutamiento, referencia
- Interfaz de protocolo de enrutamiento RRAS, referencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9341dd8dbd304da84fd675aee92e378a44271056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903450"
---
# <a name="routing-protocol-interface-reference"></a><span data-ttu-id="4c424-105">Referencia de la interfaz de protocolo de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="4c424-105">Routing Protocol Interface Reference</span></span>

<span data-ttu-id="4c424-106">En esta documentación se describen las funciones y estructuras que se usan para implementar un protocolo de enrutamiento como un archivo DLL de modo usuario.</span><span class="sxs-lookup"><span data-stu-id="4c424-106">This documentation describes the functions and structures that are used to implement a routing protocol as a user-mode DLL.</span></span>

<span data-ttu-id="4c424-107">MPR50 debe definirse en el archivo make para el protocolo de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="4c424-107">MPR50 should be defined in the make file for the routing protocol.</span></span>

<span data-ttu-id="4c424-108">La macro **sizeof \_ IP \_ Binding (x)** calcula el tamaño, en bytes, de una estructura de [**\_ información de \_ enlace \_ del adaptador de IP**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) que contiene el número de direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="4c424-108">The **SIZEOF\_IP\_BINDING(x)** macro computes the size, in bytes, of an [**IP\_ADAPTER\_BINDING\_INFO**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) structure that contains the number of IP addresses.</span></span>

<span data-ttu-id="4c424-109">Estos elementos de referencia se describen en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="4c424-109">These reference elements are described in the following topics:</span></span>

-   [<span data-ttu-id="4c424-110">Funciones de interfaz de protocolo de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="4c424-110">Routing Protocol Interface Functions</span></span>](routing-protocol-interface-functions.md)
-   [<span data-ttu-id="4c424-111">Estructuras de interfaz de protocolo de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="4c424-111">Routing Protocol Interface Structures</span></span>](routing-protocol-interface-structures.md)
-   [<span data-ttu-id="4c424-112">Administración de tablas del servicio IPX</span><span class="sxs-lookup"><span data-stu-id="4c424-112">IPX Service Table Management</span></span>](ipx-service-table-management.md)

 

 




