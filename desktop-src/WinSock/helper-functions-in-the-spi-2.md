---
description: NSPGetServiceClassInfo
ms.assetid: 6fbe9c0c-ac1f-4f2b-a542-eae2195b1335
title: Funciones auxiliares en SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e687529bf1ede1598225708cf288e49bb7e9b5c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705613"
---
# <a name="helper-functions-in-the-spi"></a><span data-ttu-id="e476e-103">Funciones auxiliares en SPI</span><span class="sxs-lookup"><span data-stu-id="e476e-103">Helper Functions in the SPI</span></span>

-   [<span data-ttu-id="e476e-104">**NSPGetServiceClassInfo**</span><span class="sxs-lookup"><span data-stu-id="e476e-104">**NSPGetServiceClassInfo**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)

<span data-ttu-id="e476e-105">La función [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) recupera la información de esquema de clase de servicio que un proveedor de espacios de nombres ha conservado.</span><span class="sxs-lookup"><span data-stu-id="e476e-105">The [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) function retrieves service class schema information that has been retained by a namespace provider.</span></span> <span data-ttu-id="e476e-106">También lo usa el archivo DLL de Windows Sockets 2 en su implementación de [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida).</span><span class="sxs-lookup"><span data-stu-id="e476e-106">It is also used by the Windows Sockets 2 DLL in its implementation of [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida).</span></span>

<span data-ttu-id="e476e-107">Las siguientes macros se definen en el archivo de encabezado *Svcguid. h* y pueden ayudar en la asignación entre las clases de servicio conocidas y los espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="e476e-107">The following macros defined in the *Svcguid.h* header file and can aid in mapping between well known service classes and these namespaces.</span></span>

| <span data-ttu-id="e476e-108">Un nombre de macro</span><span class="sxs-lookup"><span data-stu-id="e476e-108">Macro name</span></span>                                                                              | <span data-ttu-id="e476e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e476e-109">Description</span></span>                                                                                                                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e476e-110">**\_TCP SVCID (puerto)**</span><span class="sxs-lookup"><span data-stu-id="e476e-110">**SVCID\_TCP(Port)**</span></span><br/> <span data-ttu-id="e476e-111">**SVCID \_ UDP (puerto)**</span><span class="sxs-lookup"><span data-stu-id="e476e-111">**SVCID\_UDP(Port)**</span></span><br/>                         | <span data-ttu-id="e476e-112">Dado un puerto TCP o UDP para el protocolo de Internet, devuelve el GUID.</span><span class="sxs-lookup"><span data-stu-id="e476e-112">Given a TCP or UDP port for the Internet protocol, returns the GUID.</span></span>                                                                               |
| <span data-ttu-id="e476e-113">**ES \_ SVCID \_ TCP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="e476e-113">**IS\_SVCID\_TCP(GUID)**</span></span><br/> <span data-ttu-id="e476e-114">**ES \_ SVCID \_ UDP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="e476e-114">**IS\_SVCID\_UDP(GUID)**</span></span><br/>                 | <span data-ttu-id="e476e-115">Devuelve **true** si el GUID para TCP o UDP está dentro del intervalo permitido.</span><span class="sxs-lookup"><span data-stu-id="e476e-115">Returns **TRUE** if the GUID for TCP or UDP is within the allowable range.</span></span>                                                                         |
| <span data-ttu-id="e476e-116">**Puerto \_ de \_ SVCID \_ TCP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="e476e-116">**PORT\_FROM\_SVCID\_TCP(GUID)**</span></span><br/> <span data-ttu-id="e476e-117">**Puerto \_ de \_ SVCID \_ UDP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="e476e-117">**PORT\_FROM\_SVCID\_UDP(GUID)**</span></span><br/> | <span data-ttu-id="e476e-118">Devuelve el puerto TCP o UDP asociado al GUID.</span><span class="sxs-lookup"><span data-stu-id="e476e-118">Returns the TCP or UDP port associated with the GUID.</span></span>                                                                                              |
| <span data-ttu-id="e476e-119">**SVCID \_ NetWare (SAPID)**</span><span class="sxs-lookup"><span data-stu-id="e476e-119">**SVCID\_NETWARE(SAPID)**</span></span><br/>                                                    | <span data-ttu-id="e476e-120">Dado el identificador de protocolo de anuncio de servicio (SAP), devuelve el GUID.</span><span class="sxs-lookup"><span data-stu-id="e476e-120">Given the Service Advertising Protocol (SAP) identifier, returns the GUID.</span></span> <span data-ttu-id="e476e-121">Esta macro se usa con el espacio de nombres de SAP en un entorno de NetWare.</span><span class="sxs-lookup"><span data-stu-id="e476e-121">This macro is used with the SAP namespace within a NetWare environment.</span></span> |
| <span data-ttu-id="e476e-122">**SAPID \_ de \_ SVCID \_ NetWare (GUID)**</span><span class="sxs-lookup"><span data-stu-id="e476e-122">**SAPID\_FROM\_SVCID\_NETWARE(GUID)**</span></span><br/>                                        | <span data-ttu-id="e476e-123">Devuelve el identificador de NetWare SAP asociado al GUID.</span><span class="sxs-lookup"><span data-stu-id="e476e-123">Returns the NetWare SAP identifier associated with the GUID.</span></span> <span data-ttu-id="e476e-124">Esta macro se usa con el espacio de nombres de SAP en un entorno de NetWare.</span><span class="sxs-lookup"><span data-stu-id="e476e-124">This macro is used with the SAP namespace within a NetWare environment.</span></span>               |
| <span data-ttu-id="e476e-125">**ES \_ SVCID \_ NetWare (GUID)**</span><span class="sxs-lookup"><span data-stu-id="e476e-125">**IS\_SVCID\_NETWARE(GUID)**</span></span><br/>                                                 | <span data-ttu-id="e476e-126">Devuelve **true** si el GUID para NetWare está dentro del intervalo permitido.</span><span class="sxs-lookup"><span data-stu-id="e476e-126">Returns **TRUE** if the GUID for NetWare is within the allowable range.</span></span> <span data-ttu-id="e476e-127">Esta macro se usa con el espacio de nombres de SAP en un entorno de NetWare.</span><span class="sxs-lookup"><span data-stu-id="e476e-127">This macro is used with the SAP namespace within a NetWare environment.</span></span>    |



 

> [!Note]  
> <span data-ttu-id="e476e-128">El archivo de encabezado *Svcguid. h* no se incluye automáticamente en el archivo de encabezado *WinSock2. h* .</span><span class="sxs-lookup"><span data-stu-id="e476e-128">The *Svcguid.h* header file is not automatically included by the *Winsock2.h* header file.</span></span>

 

 

 




