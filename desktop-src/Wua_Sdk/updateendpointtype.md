---
description: Define el tipo de puntos de conexión que se pueden utilizar para conectarse a un servicio.
ms.assetid: 50397D25-7C71-4AA2-89BF-F90CBDCFFA91
title: Enumeración UpdateEndpointType (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: 942bcb5275c6a4f39d6e2828025e5b9a40e52c46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540123"
---
# <a name="updateendpointtype-enumeration"></a><span data-ttu-id="ffef1-103">Enumeración UpdateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ffef1-103">UpdateEndpointType enumeration</span></span>

<span data-ttu-id="ffef1-104">Define el tipo de puntos de conexión que se pueden utilizar para conectarse a un servicio.</span><span class="sxs-lookup"><span data-stu-id="ffef1-104">Defines the type of endpoints that can be used to connect to a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffef1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ffef1-105">Syntax</span></span>


```C++
typedef enum tagEndpointType { 
  uetClientServer          = 0,
  uetReporting             = ( uetClientServer + 1 ),
  uetWuaSelfUpdate         = ( uetReporting + 1 ),
  uetRegulation            = ( uetWuaSelfUpdate + 1 ),
  uetSimpleTargeting       = ( uetRegulation + 1 ),
  uetSecuredClientServer   = ( uetSimpleTargeting + 1 ),
  uetSecondaryServiceAuth  = ( uetSecuredClientServer + 1 )
} UpdateEndpointType;
```



## <a name="constants"></a><span data-ttu-id="ffef1-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ffef1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ffef1-107"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span><span class="sxs-lookup"><span data-stu-id="ffef1-107"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span></span>
</dt> <dd>

<span data-ttu-id="ffef1-108">Un punto de conexión cliente-servidor que se utiliza para conectarse al servicio de actualización, como Windows Update, Microsoft Update y servidor WSUS en un entorno corporativo, para buscar información sobre las actualizaciones que pueden ser aplicables al equipo.</span><span class="sxs-lookup"><span data-stu-id="ffef1-108">A client-server endpoint that is used to connect to the update service, such as Windows Update, Microsoft Update, and WSUS server in a corporate environment, to find information on updates that may be applicable to the computer.</span></span>

<span data-ttu-id="ffef1-109">El servicio de actualización devuelve información sobre las actualizaciones publicadas, revisadas o retiradas desde la última vez que el cliente realizó una sincronización con el servidor.</span><span class="sxs-lookup"><span data-stu-id="ffef1-109">The update service returns information on updates that have been published, revised, or withdrawn since the last time that client performed a sync with the server.</span></span>

</dd> <dt>

<span data-ttu-id="ffef1-110"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span><span class="sxs-lookup"><span data-stu-id="ffef1-110"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span></span>
</dt> <dd>

<span data-ttu-id="ffef1-111">Un punto de conexión de informes que se utiliza cuando el cliente informa de los resultados de los análisis, las descargas y vuelve a instalarse en el servicio de actualización.</span><span class="sxs-lookup"><span data-stu-id="ffef1-111">A reporting endpoint that is used when the client reports the results of scans, downloads, and installs back to the update service.</span></span>

<span data-ttu-id="ffef1-112">En el caso de los servicios públicos (Windows Update y Microsoft Update), esto se hace para la supervisión de la calidad.</span><span class="sxs-lookup"><span data-stu-id="ffef1-112">In the case of public services (Windows Update and Microsoft Update), this is done for quality monitoring purposes.</span></span>

<span data-ttu-id="ffef1-113">En el caso de los servicios privados, como un servidor WSUS corporativo, el tipo de punto de conexión thhis también permite que el servidor recopile el inventario y otra información sobre los equipos cliente que se están controlando.</span><span class="sxs-lookup"><span data-stu-id="ffef1-113">In the case of private services, such as a corporate WSUS server, thhis type of endpoint also allows the server to collect inventory and other information about the client computers under management.</span></span>

</dd> <dt>

<span data-ttu-id="ffef1-114"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span><span class="sxs-lookup"><span data-stu-id="ffef1-114"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="ffef1-115">Un punto de conexión de actualización automática que se utiliza cuando el equipo cliente se pone en contacto con un servicio de actualización para comprobar si hay una nueva versión del software cliente del agente de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="ffef1-115">A self-update endpoint that is used when the client computer contacts an update service to see whether there is a new version of the Windows Update Agent client software.</span></span>

<span data-ttu-id="ffef1-116">El punto de conexión de actualización automática usa un protocolo diferente, el extremo de Client-Server para que se puedan distribuir las actualizaciones automáticas, incluso si hay una condición de error que podría impedir que la sincronización de cliente-servidor normal funcione en un equipo cliente determinado.</span><span class="sxs-lookup"><span data-stu-id="ffef1-116">The Self-update endpoint uses a different protocol then the Client-Server endpoint so that self-updates can be distributed even if there is an error condition that might be preventing the normal client-server sync from working on a particular client computer.</span></span>

</dd> <dt>

<span data-ttu-id="ffef1-117"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span><span class="sxs-lookup"><span data-stu-id="ffef1-117"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span></span>
</dt> <dd>

<span data-ttu-id="ffef1-118">Un punto de conexión de Reglamento que se utiliza cuando el equipo cliente se pone en contacto con el servicio de Reglamento para actuar sobre una actualización determinada que es aplicable al equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="ffef1-118">A regulation endpoint that is used when the client computer contacts the regulation service to act on a particular update that is applicable to the target computer.</span></span>

<span data-ttu-id="ffef1-119">El servicio de regulación puede indicar si la actualización está "regulada" (también conocida como "limitada"); en otras palabras, el servicio de regulación puede indicar al equipo cliente que no debe actuar en una actualización determinada, aunque esa actualización parezca ser aplicable.</span><span class="sxs-lookup"><span data-stu-id="ffef1-119">The regulation service can indicate whether the update is “regulated” (also known as “throttled”) – in other words, the regulation service can tell the client computer that it should not act on a particular update, even though that update appears to be applicable.</span></span>

</dd> <dt>

<span data-ttu-id="ffef1-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span><span class="sxs-lookup"><span data-stu-id="ffef1-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span></span>
</dt> <dd>

<span data-ttu-id="ffef1-121">Un punto de conexión de destino simple que solo se usa con servicios privados (servidores WSUS en entornos corporativos).</span><span class="sxs-lookup"><span data-stu-id="ffef1-121">A simple-targeting endpoint that is used only with private services (WSUS servers in corporate environments).</span></span> <span data-ttu-id="ffef1-122">En un entorno corporativo, los equipos cliente se pueden asignar a grupos de destino concretos y las actualizaciones se pueden aprobar para su instalación en equipos en algunos grupos, pero no en otros.</span><span class="sxs-lookup"><span data-stu-id="ffef1-122">In a corporate environment, client computers can be assigned to particular target groups, and updates can be approved for installation on computers in some groups but not others.</span></span>

<span data-ttu-id="ffef1-123">Por ejemplo, el administrador de WSUS puede crear un grupo de "pruebas" para los equipos que se usan para probar nuevas actualizaciones, y el administrador puede aprobar las actualizaciones recién publicadas para instalarlas en los equipos del grupo de prueba sin que se aprueben para su instalación en otros equipos de la organización.</span><span class="sxs-lookup"><span data-stu-id="ffef1-123">For example, the WSUS administrator may create a “Testing” group for computers that are used to test new updates, and the administrator may approve newly-released updates for installation on computers in the Testing group without approving them for installation on other computers in the organization.</span></span> <span data-ttu-id="ffef1-124">El intercambio de destino sencillo se usa para permitir que un equipo cliente se registre en el servidor WSUS y permitir que el servidor indique al equipo cliente en qué grupo se encuentra.</span><span class="sxs-lookup"><span data-stu-id="ffef1-124">The simple targeting exchange is used to allow a client computer to register itself with the WSUS server, and to allow the server to tell the client computer what group it is in.</span></span>

</dd> <dt>

<span data-ttu-id="ffef1-125"><span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**</span><span class="sxs-lookup"><span data-stu-id="ffef1-125"><span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**</span></span>
</dt> <dd>

<span data-ttu-id="ffef1-126">Un punto de conexión de cliente-servidor protegido que permite a un cliente obtener información sobre las aplicaciones que necesitan licencias para que se puedan usar en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="ffef1-126">A secured-client-server endpoint that allows a client to obtain info on apps that need licensing so they can be used on a client computer.</span></span> <span data-ttu-id="ffef1-127">Actualmente, Windows 8 solo usa este marco de licencias para implementar aplicaciones y actualizaciones que se obtienen a través de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="ffef1-127">This licensing framework is currently only used by Windows 8 to deploy apps and updates that are obtained through the Windows Store.</span></span> <span data-ttu-id="ffef1-128">Windows Update, Microsoft Update o WSUS no usan actualmente el punto de conexión protegido-cliente-servidor.</span><span class="sxs-lookup"><span data-stu-id="ffef1-128">The secured-client-server endpoint is currently not used by Windows Update, Microsoft Update, or WSUS.</span></span>

</dd> <dt>

<span data-ttu-id="ffef1-129"><span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**</span><span class="sxs-lookup"><span data-stu-id="ffef1-129"><span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**</span></span>
</dt> <dd>

<span data-ttu-id="ffef1-130">Un cliente usa el punto de conexión de autenticación de servicio secundario para proporcionar la autenticación antes de obtener información sobre las aplicaciones que necesitan licencias para que se puedan usar en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="ffef1-130">The secondary-service-authentication endpoint is used by a client to provide authentication before it obtains info on apps that need licensing so they can be used on a client computer.</span></span> <span data-ttu-id="ffef1-131">Actualmente, Windows 8 solo emplea este marco de licencias para implementar aplicaciones y actualizaciones que se obtienen a través de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="ffef1-131">This licensing framework is currently only utilized by Windows 8 to deploy apps and updates that are obtained through the Windows Store.</span></span> <span data-ttu-id="ffef1-132">Windows Update, Microsoft Update o WSUS no usan actualmente el punto de conexión de autenticación de servicio secundario.</span><span class="sxs-lookup"><span data-stu-id="ffef1-132">The secondary-service-authentication endpoint is currently not used by Windows Update, Microsoft Update, or WSUS.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ffef1-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffef1-133">Requirements</span></span>



| <span data-ttu-id="ffef1-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffef1-134">Requirement</span></span> | <span data-ttu-id="ffef1-135">Value</span><span class="sxs-lookup"><span data-stu-id="ffef1-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffef1-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffef1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ffef1-137">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ffef1-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="ffef1-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffef1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ffef1-139">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ffef1-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="ffef1-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ffef1-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffef1-141"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffef1-141"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="ffef1-142">IDL</span><span class="sxs-lookup"><span data-stu-id="ffef1-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ffef1-143"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ffef1-143"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



 

 




