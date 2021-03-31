---
description: En esta sección se describen las funciones auxiliares que puede usar para desarrollar monitores personalizados.
ms.assetid: 2c019183-9823-4e34-bb41-cf35f2731b8f
title: Funciones de supervisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9391927104196e282d4438c0b047e233d61f3619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908093"
---
# <a name="monitor-functions"></a><span data-ttu-id="24e04-103">Funciones de supervisión</span><span class="sxs-lookup"><span data-stu-id="24e04-103">Monitor Functions</span></span>

<span data-ttu-id="24e04-104">En esta sección se describen las funciones auxiliares que puede usar para desarrollar monitores personalizados.</span><span class="sxs-lookup"><span data-stu-id="24e04-104">This section describes the helper functions you can use to develop custom monitors.</span></span>



| <span data-ttu-id="24e04-105">Función</span><span class="sxs-lookup"><span data-stu-id="24e04-105">Function</span></span>                                       | <span data-ttu-id="24e04-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="24e04-106">Description</span></span>                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24e04-107">DllGetMonitorObject</span><span class="sxs-lookup"><span data-stu-id="24e04-107">DllGetMonitorObject</span></span>](dllgetmonitorobject.md) | <span data-ttu-id="24e04-108">Crea una instancia del monitor.</span><span class="sxs-lookup"><span data-stu-id="24e04-108">Creates an instance of the monitor.</span></span>                                                                                                                              |
| [<span data-ttu-id="24e04-109">HTMLValueToUnicode</span><span class="sxs-lookup"><span data-stu-id="24e04-109">HTMLValueToUnicode</span></span>](htmlvaluetounicode.md)   | <span data-ttu-id="24e04-110">Convierte una \_ cadena de versión de CP UTF8 HTML en Unicode.</span><span class="sxs-lookup"><span data-stu-id="24e04-110">Converts an HTML CP\_UTF8 version string to Unicode.</span></span>                                                                                                             |
| [<span data-ttu-id="24e04-111">LoadDWORD</span><span class="sxs-lookup"><span data-stu-id="24e04-111">LoadDWORD</span></span>](loaddword.md)                     | <span data-ttu-id="24e04-112">Carga un **valor DWORD** de una cadena de configuración HTML.</span><span class="sxs-lookup"><span data-stu-id="24e04-112">Loads a **DWORD** from an HTML configuration string.</span></span>                                                                                                             |
| [<span data-ttu-id="24e04-113">LoadIPAddresses</span><span class="sxs-lookup"><span data-stu-id="24e04-113">LoadIPAddresses</span></span>](loadipaddresses.md)         | <span data-ttu-id="24e04-114">Carga una lista de direcciones IP desde una cadena de configuración HTML TEXTAREA.</span><span class="sxs-lookup"><span data-stu-id="24e04-114">Loads an IP address list from an HTML TEXTAREA configuration string.</span></span>                                                                                             |
| [<span data-ttu-id="24e04-115">LoadIPXAddresses</span><span class="sxs-lookup"><span data-stu-id="24e04-115">LoadIPXAddresses</span></span>](loadipxaddresses.md)       | <span data-ttu-id="24e04-116">Carga una lista de direcciones IPX desde una cadena de configuración HTML TEXTAREA.</span><span class="sxs-lookup"><span data-stu-id="24e04-116">Loads an IPX address list from an HTML TEXTAREA configuration string.</span></span>                                                                                            |
| [<span data-ttu-id="24e04-117">LoadMACAddresses</span><span class="sxs-lookup"><span data-stu-id="24e04-117">LoadMACAddresses</span></span>](loadmacaddresses.md)       | <span data-ttu-id="24e04-118">Carga una lista de direcciones MAC desde una cadena de configuración HTML TEXTAREA.</span><span class="sxs-lookup"><span data-stu-id="24e04-118">Loads a MAC address list from an HTML TEXTAREA configuration string.</span></span>                                                                                             |
| [<span data-ttu-id="24e04-119">LoadStringAddr</span><span class="sxs-lookup"><span data-stu-id="24e04-119">LoadStringAddr</span></span>](loadstringaddr.md)           | <span data-ttu-id="24e04-120">Transforma una cadena (por ejemplo, "157.54.32.45") en una dirección **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="24e04-120">Transforms a string (such as "157.54.32.45") to a **DWORD** address.</span></span>                                                                                             |
| [<span data-ttu-id="24e04-121">LoadTCHAR</span><span class="sxs-lookup"><span data-stu-id="24e04-121">LoadTCHAR</span></span>](loadtchar.md)                     | <span data-ttu-id="24e04-122">Busca un nombre de variable solicitado en la cadena de configuración y asigna espacio suficiente (mediante **HeapAllocMemory**) para almacenarlo, copiarlo y devolverlo.</span><span class="sxs-lookup"><span data-stu-id="24e04-122">Searches for a requested variable name in the configuration string, and allocates sufficient space (by using **HeapAllocMemory**) to store, copy, and return it.</span></span> |
| [<span data-ttu-id="24e04-123">OnLoadingDLL</span><span class="sxs-lookup"><span data-stu-id="24e04-123">OnLoadingDLL</span></span>](onloadingdll.md)               | <span data-ttu-id="24e04-124">Indica que el archivo DLL comenzó a cargarse.</span><span class="sxs-lookup"><span data-stu-id="24e04-124">Indicates that the DLL has begun to load.</span></span> <span data-ttu-id="24e04-125">El MCSVC llama a esta función cuando carga por primera vez la DLL del monitor.</span><span class="sxs-lookup"><span data-stu-id="24e04-125">The MCSVC calls this function when it first loads the monitor DLL.</span></span>                                                     |



 

 

 



