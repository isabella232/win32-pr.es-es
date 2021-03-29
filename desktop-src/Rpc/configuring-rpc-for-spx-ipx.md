---
title: Configuración de RPC para SPX/IPX
description: Al usar los \_ transportes ncacn SPX y ncadg \_ IPX, el nombre del servidor es exactamente el mismo que el nombre del servidor en Windows.
ms.assetid: b2543046-8cdc-4cba-94e4-40188701fad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90fa82c216413f1ea745b90ae03749ede4331310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486915"
---
# <a name="configuring-rpc-for-spxipx"></a><span data-ttu-id="d8a38-103">Configuración de RPC para SPX/IPX</span><span class="sxs-lookup"><span data-stu-id="d8a38-103">Configuring RPC for SPX/IPX</span></span>

<span data-ttu-id="d8a38-104">Al usar los transportes **ncacn \_ SPX** y **ncadg \_ IPX** , el nombre del servidor es exactamente el mismo que el nombre del servidor en Windows.</span><span class="sxs-lookup"><span data-stu-id="d8a38-104">When using the **ncacn\_spx** and **ncadg\_ipx** transports, the server name is exactly the same as the server name on Windows.</span></span> <span data-ttu-id="d8a38-105">Sin embargo, puesto que los nombres se distribuyen mediante protocolos de Novell, deben cumplir las convenciones de nomenclatura de Novell.</span><span class="sxs-lookup"><span data-stu-id="d8a38-105">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="d8a38-106">Si un nombre de servidor no es un nombre de Novell válido, los servidores no podrán crear extremos con los transportes **ncacn \_ SPX** o **ncadg \_ IPX** .</span><span class="sxs-lookup"><span data-stu-id="d8a38-106">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncacn\_spx** or **ncadg\_ipx** transports.</span></span>

<span data-ttu-id="d8a38-107">Un nombre de servidor Novell válido solo contiene los caracteres entre 0x20 y 0x7F.</span><span class="sxs-lookup"><span data-stu-id="d8a38-107">A valid Novell server name contains only the characters between 0x20 and 0x7f.</span></span> <span data-ttu-id="d8a38-108">Los caracteres en minúsculas se cambian a mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="d8a38-108">Lowercase characters are changed to uppercase.</span></span> <span data-ttu-id="d8a38-109">No se pueden usar los siguientes caracteres:</span><span class="sxs-lookup"><span data-stu-id="d8a38-109">The following characters cannot be used:</span></span>

<span data-ttu-id="d8a38-110">" \* ,./:; <=>?\[\]\\\|\]</span><span class="sxs-lookup"><span data-stu-id="d8a38-110">"\*,./:;<=>?\[\]\\\|\]</span></span>

<span data-ttu-id="d8a38-111">Para mantener la compatibilidad con la primera versión de Windows NT, **ncacn \_ SPX** y **ncadg \_ IPX** también permiten usar un formato especial del nombre del servidor conocido como el nombre de la tilde.</span><span class="sxs-lookup"><span data-stu-id="d8a38-111">To maintain compatibility with the first version of Windows NT, **ncacn\_spx** and **ncadg\_ipx** also enable you to use a special format of the server name known as the tilde name.</span></span> <span data-ttu-id="d8a38-112">El nombre de la tilde se compone de una tilde (~), seguida del número de red de ocho dígitos del servidor y, a continuación, seguido de su dirección Ethernet de 12 dígitos.</span><span class="sxs-lookup"><span data-stu-id="d8a38-112">The tilde name consists of a tilde (~), followed by the server's eight-digit network number, and then followed by its 12-digit Ethernet address.</span></span> <span data-ttu-id="d8a38-113">Los nombres de tildes tienen una ventaja en que no requieren ninguna funcionalidad de servicio de nombres.</span><span class="sxs-lookup"><span data-stu-id="d8a38-113">Tilde names have an advantage in that they do not require any name service capabilities.</span></span> <span data-ttu-id="d8a38-114">Por lo tanto, si está conectado a un servidor, el nombre de la tilde funcionará.</span><span class="sxs-lookup"><span data-stu-id="d8a38-114">Thus, if you are connected to a server, the tilde name will work.</span></span>

<span data-ttu-id="d8a38-115">Las tablas siguientes contienen dos configuraciones de ejemplo que ilustran los puntos descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d8a38-115">The following tables contain two sample configurations that illustrate the points previously described.</span></span>



| <span data-ttu-id="d8a38-116">Componente</span><span class="sxs-lookup"><span data-stu-id="d8a38-116">Component</span></span>                            | <span data-ttu-id="d8a38-117">Configurado como</span><span class="sxs-lookup"><span data-stu-id="d8a38-117">Configured as</span></span>      |
|--------------------------------------|--------------------|
| <span data-ttu-id="d8a38-118">Windows Server</span><span class="sxs-lookup"><span data-stu-id="d8a38-118">Windows server</span></span>                       | <span data-ttu-id="d8a38-119">NWCS</span><span class="sxs-lookup"><span data-stu-id="d8a38-119">NWCS</span></span>               |
| <span data-ttu-id="d8a38-120">Cliente Windows</span><span class="sxs-lookup"><span data-stu-id="d8a38-120">Windows client</span></span>                       | <span data-ttu-id="d8a38-121">NWCS</span><span class="sxs-lookup"><span data-stu-id="d8a38-121">NWCS</span></span>               |
| <span data-ttu-id="d8a38-122">cliente de Windows de 16 bits, cliente de MS-DOS</span><span class="sxs-lookup"><span data-stu-id="d8a38-122">16-bit Windows client, MS-DOS client</span></span> | <span data-ttu-id="d8a38-123">Redirector de NetWare</span><span class="sxs-lookup"><span data-stu-id="d8a38-123">NetWare Redirector</span></span> |



 

<span data-ttu-id="d8a38-124">La configuración de la tabla anterior requiere que tenga servidores de archivos de NetWare o enrutadores en la red.</span><span class="sxs-lookup"><span data-stu-id="d8a38-124">The configuration in the previous table requires that you have NetWare file servers or routers on your network.</span></span> <span data-ttu-id="d8a38-125">Generará el mejor rendimiento porque los nombres de servidor se almacenan en el enlace de NetWare.</span><span class="sxs-lookup"><span data-stu-id="d8a38-125">It will produce the best performance because the server names are stored in the NetWare Bindery.</span></span>



| <span data-ttu-id="d8a38-126">Componente</span><span class="sxs-lookup"><span data-stu-id="d8a38-126">Component</span></span>                            | <span data-ttu-id="d8a38-127">Configurado como</span><span class="sxs-lookup"><span data-stu-id="d8a38-127">Configured as</span></span> |
|--------------------------------------|---------------|
| <span data-ttu-id="d8a38-128">Windows Server</span><span class="sxs-lookup"><span data-stu-id="d8a38-128">Windows server</span></span>                       | <span data-ttu-id="d8a38-129">Agente SAP</span><span class="sxs-lookup"><span data-stu-id="d8a38-129">SAP Agent</span></span>     |
| <span data-ttu-id="d8a38-130">Cliente Windows</span><span class="sxs-lookup"><span data-stu-id="d8a38-130">Windows client</span></span>                       | <span data-ttu-id="d8a38-131">IPX/SPX</span><span class="sxs-lookup"><span data-stu-id="d8a38-131">IPX/SPX</span></span>       |
| <span data-ttu-id="d8a38-132">cliente de Windows de 16 bits, cliente de MS-DOS</span><span class="sxs-lookup"><span data-stu-id="d8a38-132">16-bit Windows client, MS-DOS client</span></span> | <span data-ttu-id="d8a38-133">IPX/SPX</span><span class="sxs-lookup"><span data-stu-id="d8a38-133">IPX/SPX</span></span>       |



 

<span data-ttu-id="d8a38-134">La segunda configuración funciona en un entorno que no contiene servidores de archivos de NetWare o enrutadores (por ejemplo, una red de dos equipos: un servidor de Windows y un cliente de MS-DOS).</span><span class="sxs-lookup"><span data-stu-id="d8a38-134">The second configuration works in an environment that does not contain NetWare file servers or routers (for example, a network of two computers: a Windows server and an MS-DOS client).</span></span> <span data-ttu-id="d8a38-135">La resolución de nombres, que se realiza durante la primera llamada a través de un identificador de enlace, será ligeramente más lenta que en la primera configuración.</span><span class="sxs-lookup"><span data-stu-id="d8a38-135">Name resolution, which is accomplished during the first call over a binding handle, will be slightly slower than in the first configuration.</span></span> <span data-ttu-id="d8a38-136">Además, la segunda configuración produce más tráfico generado a través de la red.</span><span class="sxs-lookup"><span data-stu-id="d8a38-136">In addition, the second configuration results in more traffic generated over the network.</span></span>

<span data-ttu-id="d8a38-137">Para implementar la resolución de nombres, cuando un servidor RPC usa un extremo SPX o IPX, el nombre del servidor y el punto de conexión se registran como un servidor de protocolo de anuncio de servicio (SAP) de tipo 640 (hexadecimal).</span><span class="sxs-lookup"><span data-stu-id="d8a38-137">To implement name resolution, when an RPC server uses an SPX or IPX endpoint, the server name and endpoint are registered as a Service Advertising Protocol (SAP) server of type 640 (hexadecimal).</span></span> <span data-ttu-id="d8a38-138">Para resolver un nombre de servidor, el cliente RPC envía una solicitud de SAP para todos los servicios del mismo tipo y, a continuación, examina la lista de respuestas para el nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="d8a38-138">To resolve a server name, the RPC client sends a SAP request for all services of the same type, and then scans the list of responses for the name of the server.</span></span> <span data-ttu-id="d8a38-139">Este proceso se produce durante la primera llamada RPC sobre cada identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="d8a38-139">This process occurs during the first RPC call over each binding handle.</span></span> <span data-ttu-id="d8a38-140">Para obtener más información sobre el protocolo SAP para Novell, consulte la documentación de NetWare.</span><span class="sxs-lookup"><span data-stu-id="d8a38-140">For additional information on the SAP protocol for Novell, see your NetWare documentation.</span></span>

> [!Note]  
> <span data-ttu-id="d8a38-141">Las aplicaciones cliente de Windows de 16 bits que usan los transportes **ncacn \_ SPX** o **ncadg \_ ipx** requieren que el archivo Nwipxspx.dll instalarse para ejecutarse en el subsistema wow.</span><span class="sxs-lookup"><span data-stu-id="d8a38-141">The 16-bit Windows client applications that use the **ncacn\_spx** or **ncadg\_ipx** transports require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="d8a38-142">Póngase en contacto con Novell para obtener este archivo.</span><span class="sxs-lookup"><span data-stu-id="d8a38-142">Contact Novell to obtain this file.</span></span>

 

 

 




