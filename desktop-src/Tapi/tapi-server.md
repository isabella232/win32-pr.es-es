---
description: El servidor TAPI (TAPISRV) es el repositorio central de datos de telefonía en un equipo de usuario.
ms.assetid: 794d230c-abe8-429d-bbf5-91ba364b16ab
title: Servidor TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a6886a5d8e56519f10fc370ed15adc3b1af7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911530"
---
# <a name="tapi-server"></a><span data-ttu-id="299ba-103">Servidor TAPI</span><span class="sxs-lookup"><span data-stu-id="299ba-103">TAPI Server</span></span>

<span data-ttu-id="299ba-104">El servidor TAPI (TAPISRV) es el repositorio central de datos de telefonía en un equipo de usuario.</span><span class="sxs-lookup"><span data-stu-id="299ba-104">The TAPI server (TAPISRV) is the central repository of telephony data on a user computer.</span></span> <span data-ttu-id="299ba-105">Este proceso de servicio realiza un seguimiento de los recursos de telefonía locales y remotos, las aplicaciones registradas para administrar las solicitudes de telefonía asistidas y las funciones asincrónicas pendientes, además de habilitar una interfaz coherente con los proveedores de servicios de telefonía (profesionales).</span><span class="sxs-lookup"><span data-stu-id="299ba-105">This service process tracks local and remote telephony resources, applications registered to handle Assisted Telephony requests, and pending asynchronous functions, and it also enables a consistent interface with telephony service providers (TSPs).</span></span> <span data-ttu-id="299ba-106">Para obtener más información y un diagrama que muestra la relación entre el servidor TAPI y otros componentes, así como información general de sus roles, vea [modelo de programación de telefonía de Microsoft](microsoft-telephony-programming-model.md).</span><span class="sxs-lookup"><span data-stu-id="299ba-106">For more information and a diagram that illustrates the relationship of the TAPI Server to other components and an overview of their roles, see [Microsoft Telephony Programming Model](microsoft-telephony-programming-model.md).</span></span>

<span data-ttu-id="299ba-107">En el caso de los equipos que se ejecutan en sistemas operativos Windows Server 2003, Windows XP y Windows 2000, TAPISRV se ejecuta en el contexto de Svchost.exe.</span><span class="sxs-lookup"><span data-stu-id="299ba-107">For computers running on Windows Server 2003 operating systems, Windows XP, and Windows 2000, TAPISRV runs within the context of Svchost.exe.</span></span> <span data-ttu-id="299ba-108">En el caso de los equipos que ejecutan Windows NT, se ejecuta como un proceso de servicio independiente.</span><span class="sxs-lookup"><span data-stu-id="299ba-108">For computers running on Windows NT, it runs as a separate service process.</span></span> <span data-ttu-id="299ba-109">Cuando una aplicación carga una DLL de TAPI en su espacio de proceso y realiza una operación de inicialización, el archivo DLL establece un vínculo RPC al servidor TAPI.</span><span class="sxs-lookup"><span data-stu-id="299ba-109">When an application loads a TAPI DLL into its process space and performs an initialization operation, the DLL establishes an RPC link to the TAPI Server.</span></span> <span data-ttu-id="299ba-110">El servidor TAPI carga los proveedores de servicios telefónicos (profesionales) en su espacio de proceso.</span><span class="sxs-lookup"><span data-stu-id="299ba-110">The TAPI Server loads telephone service providers (TSPs) into its process space.</span></span> <span data-ttu-id="299ba-111">Independientemente del número de aplicaciones que accedan a los dispositivos de un proveedor determinado, solo existirá una instancia de un TSP determinado.</span><span class="sxs-lookup"><span data-stu-id="299ba-111">Regardless of how many applications access a given provider's devices, only one instance of a given TSP will exist.</span></span>

 

 



