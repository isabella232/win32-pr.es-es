---
description: Los clientes NLA pueden registrar información de configuración de red en todo el sistema, lo que permite que las consultas futuras devuelvan la información de configuración especificada independientemente de si la red está activa.
ms.assetid: 7e92dd8f-d3a1-4e53-885c-ebc9626fd5dc
title: Registrar una instancia de servicio con NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae2e73e638e4bf0152c2c6c5a4f5ab87dda7312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696932"
---
# <a name="registering-a-service-instance-with-nla"></a><span data-ttu-id="91897-103">Registrar una instancia de servicio con NLA</span><span class="sxs-lookup"><span data-stu-id="91897-103">Registering a Service Instance with NLA</span></span>

<span data-ttu-id="91897-104">Los clientes NLA pueden registrar información de configuración de red en todo el sistema, lo que permite que las consultas futuras devuelvan la información de configuración especificada independientemente de si la red está activa.</span><span class="sxs-lookup"><span data-stu-id="91897-104">NLA clients can record network configuration information on a system-wide basis, enabling future queries to return the specified configuration information regardless of whether the network is active.</span></span> <span data-ttu-id="91897-105">Esta funcionalidad permite que los clientes de NLA afecten a una experiencia de usuario de información de red coherente entre varias aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="91897-105">This capability allows NLA clients to affect a consistent network information user experience across multiple applications.</span></span>

## <a name="parameters"></a><span data-ttu-id="91897-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91897-106">Parameters</span></span>

<span data-ttu-id="91897-107">Para registrar una instancia de servicio con el proveedor de servicios de reconocimiento de ubicación de red, utilice la función [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) .</span><span class="sxs-lookup"><span data-stu-id="91897-107">To register a service instance with the Network Location Awareness service provider, use the [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) function.</span></span> <span data-ttu-id="91897-108">Para registrar correctamente una instancia de servicio, ciertos parámetros de la función **WSASetService** se deben establecer con la información adecuada, como se explica en esta sección.</span><span class="sxs-lookup"><span data-stu-id="91897-108">In order to properly register a service instance certain parameters of the **WSASetService** function must be set with the appropriate information, as explained in this section.</span></span> <span data-ttu-id="91897-109">Para una referencia rápida, la función **WSASetService** tiene la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="91897-109">For quick reference, the **WSASetService** function has the following syntax:</span></span>

``` syntax
INT WSASetService(
  LPWSAQUERYSET lpqsRegInfo,
  WSAESETSERVICEOP essOperation,
  DWORD dwControlFlags
);
```

<span data-ttu-id="91897-110">Para el parámetro *lpqsRegInfo* , proporcione una estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) desde el resultado de una consulta NLA SP o construya el cumplimiento de los requisitos de una consulta de SP NLA, como se especifica en [consultar NLA](querying-nla-2.md).</span><span class="sxs-lookup"><span data-stu-id="91897-110">For the *lpqsRegInfo* parameter, provide a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure from either an NLA SP query result, or constructed adhering to the requirements of an NLA SP query, as specified in [Querying NLA](querying-nla-2.md).</span></span>

<span data-ttu-id="91897-111">Las operaciones admitidas para el parámetro *essOperation* son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="91897-111">Operations supported for the *essOperation* parameter are the following:</span></span>

<dl> <dt>

<span data-ttu-id="91897-112"><span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>registro de RNRSERVICE \_</span><span class="sxs-lookup"><span data-stu-id="91897-112"><span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>RNRSERVICE\_REGISTER</span></span>
</dt> <dd>

<span data-ttu-id="91897-113">La red definida en la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) proporcionada en *lpqsRegInfo* se hace persistente para el usuario activo almacenando la instancia de red en el subárbol del registro para el usuario actual, lo que permite la suplantación.</span><span class="sxs-lookup"><span data-stu-id="91897-113">The network defined in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure provided in *lpqsRegInfo* is made persistent for the active user by storing the network instance in the registry hive for the current user, which allows impersonation.</span></span>

</dd> <dt>

<span data-ttu-id="91897-114"><span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE \_ eliminar</span><span class="sxs-lookup"><span data-stu-id="91897-114"><span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE\_DELETE</span></span>
</dt> <dd>

<span data-ttu-id="91897-115">Si la red definida en la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) proporcionada en *lpqsRegInfo* es persistente, se quitará.</span><span class="sxs-lookup"><span data-stu-id="91897-115">If the network defined in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure provided in *lpqsRegInfo* is persistent, it will be removed.</span></span>

</dd> </dl>

<span data-ttu-id="91897-116">La operación especificada en el parámetro *essOperation* se puede modificar con las siguientes opciones, que se pueden especificar con la lógica OR binaria:</span><span class="sxs-lookup"><span data-stu-id="91897-116">The operation specified in the *essOperation* parameter can be modified by the following options, which can be specified with binary OR logic:</span></span>

<dl> <dt>

<span data-ttu-id="91897-117"><span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>\_nombre descriptivo de NLA \_</span><span class="sxs-lookup"><span data-stu-id="91897-117"><span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>NLA\_FRIENDLY\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="91897-118">Cuando se usa con \_ el registro RNRSERVICE, se comprueba la validez del campo *lpszComment* de la red definida en *lpqsRegInfo* y se almacena de forma persistente.</span><span class="sxs-lookup"><span data-stu-id="91897-118">When used with RNRSERVICE\_REGISTER, the *lpszComment* field of the network defined in *lpqsRegInfo* is checked for validity and stored persistently.</span></span> <span data-ttu-id="91897-119">Cuando se usa con RNRSERVICE \_ Delete y la red definida tiene un nombre descriptivo, se quita el nombre descriptivo pero la entrada de red se deja intacta.</span><span class="sxs-lookup"><span data-stu-id="91897-119">When used with RNRSERVICE\_DELETE and the defined network has a friendly name, the friendly name is removed but the network entry is left intact.</span></span>

</dd> <dt>

<span data-ttu-id="91897-120"><span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>\_red de AllUsers de NLA \_</span><span class="sxs-lookup"><span data-stu-id="91897-120"><span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>NLA\_ALLUSERS\_NETWORK</span></span>
</dt> <dd>

<span data-ttu-id="91897-121">Cuando se usa con \_ el registro RNRSERVICE, la entrada se almacena de forma persistente en HKEY \_ local \_ Machine, lo que lo pone a disposición durante las consultas a todos los usuarios en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="91897-121">When used with RNRSERVICE\_REGISTER, the entry is stored persistently under HKEY\_LOCAL\_MACHINE, making it available during queries to all users on the local computer.</span></span> <span data-ttu-id="91897-122">Cuando se usa con RNRSERVICE \_ Delete, la red especificada se quita de \_ la \_ máquina local HKEY.</span><span class="sxs-lookup"><span data-stu-id="91897-122">When used with RNRSERVICE\_DELETE, the specified network is removed from HKEY\_LOCAL\_MACHINE.</span></span> <span data-ttu-id="91897-123">Se devuelve un error si la red especificada no está presente.</span><span class="sxs-lookup"><span data-stu-id="91897-123">An error is returned if the specified network is not present.</span></span> <span data-ttu-id="91897-124">Para eliminar una red del subárbol del registro del usuario actual, no se debe especificar esta marca.</span><span class="sxs-lookup"><span data-stu-id="91897-124">In order to delete a network from the registry hive of the current user, this flag must not be specified.</span></span> <span data-ttu-id="91897-125">Esta marca solo es válida en el contexto de seguridad de un administrador del sistema local.</span><span class="sxs-lookup"><span data-stu-id="91897-125">This flag is only valid in the security context of a local system administrator.</span></span>

</dd> </dl>

<span data-ttu-id="91897-126">NLA admite los siguientes códigos de error para las llamadas a la función [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) :</span><span class="sxs-lookup"><span data-stu-id="91897-126">NLA supports the following error codes for [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) function calls:</span></span>

| <span data-ttu-id="91897-127">Error</span><span class="sxs-lookup"><span data-stu-id="91897-127">Error</span></span>             | <span data-ttu-id="91897-128">Significado</span><span class="sxs-lookup"><span data-stu-id="91897-128">Meaning</span></span>                                                                                                                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91897-129">WSANOTINITIALISED</span><span class="sxs-lookup"><span data-stu-id="91897-129">WSANOTINITIALISED</span></span> | <span data-ttu-id="91897-130">No se realizó una llamada correcta a la función [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar NLA.</span><span class="sxs-lookup"><span data-stu-id="91897-130">A successful call to the [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function to initialize NLA was not performed.</span></span>                                                                  |
| <span data-ttu-id="91897-131">WSAEACCESS</span><span class="sxs-lookup"><span data-stu-id="91897-131">WSAEACCESS</span></span>        | <span data-ttu-id="91897-132">\_La red AllUsers de NLA \_ se especificó en *dwControlFlags* mientras no se encontraba en el contexto de seguridad de un administrador del sistema local.</span><span class="sxs-lookup"><span data-stu-id="91897-132">NLA\_ALLUSERS\_NETWORK was specified in *dwControlFlags* while not in the security context of a local system administrator.</span></span>                                                |
| <span data-ttu-id="91897-133">WSAEALREADY</span><span class="sxs-lookup"><span data-stu-id="91897-133">WSAEALREADY</span></span>       | <span data-ttu-id="91897-134">La red especificada ya está almacenada de forma persistente en la manera solicitada y no se ha especificado ninguna marca en *dwControlFlags* para indicar una actualización de la entrada existente.</span><span class="sxs-lookup"><span data-stu-id="91897-134">The specified network is already persistently stored in the requested manner, and no flags were specified in *dwControlFlags* to indicate an update to the existing entry.</span></span> |
| <span data-ttu-id="91897-135">WSAEAFNOSUPPORT</span><span class="sxs-lookup"><span data-stu-id="91897-135">WSAEAFNOSUPPORT</span></span>   | <span data-ttu-id="91897-136">Se especificó una familia de protocolos para la que no se admite.</span><span class="sxs-lookup"><span data-stu-id="91897-136">A protocol family was specified for which there is no support.</span></span> <span data-ttu-id="91897-137">Solo se admiten familias de protocolo IP en NLA.</span><span class="sxs-lookup"><span data-stu-id="91897-137">Only IP protocol families are supported in NLA.</span></span>                                                             |
| <span data-ttu-id="91897-138">WSAEPFNOSUPPORT</span><span class="sxs-lookup"><span data-stu-id="91897-138">WSAEPFNOSUPPORT</span></span>   | <span data-ttu-id="91897-139">Se especificó un protocolo para el que no se admite.</span><span class="sxs-lookup"><span data-stu-id="91897-139">A protocol was specified for which there is no support.</span></span> <span data-ttu-id="91897-140">Solo se admite el protocolo IP en NLA.</span><span class="sxs-lookup"><span data-stu-id="91897-140">Only IP protocol is supported in NLA.</span></span>                                                                              |



 

 

 



