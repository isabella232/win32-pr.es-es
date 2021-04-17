---
description: Las funciones de sesión de administración de red controlan las sesiones de red establecidas entre estaciones de trabajo y servidores. Las funciones requieren que se inicie el servicio servidor en el servidor.
ms.assetid: 931455e3-1301-4a68-93c3-2674b3d4c491
title: Funciones de sesión (administración de recursos compartidos de red)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c672abd7c976cb9f83fa4f387dd40d175879dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677665"
---
# <a name="session-functions-network-share-management"></a><span data-ttu-id="01636-104">Funciones de sesión (administración de recursos compartidos de red)</span><span class="sxs-lookup"><span data-stu-id="01636-104">Session Functions (Network Share Management)</span></span>

<span data-ttu-id="01636-105">Las funciones de sesión de administración de red controlan las sesiones de red establecidas entre estaciones de trabajo y servidores.</span><span class="sxs-lookup"><span data-stu-id="01636-105">The network management session functions control network sessions established between workstations and servers.</span></span> <span data-ttu-id="01636-106">Las funciones requieren que se inicie el servicio servidor en el servidor.</span><span class="sxs-lookup"><span data-stu-id="01636-106">The functions require that the server service be started on the server.</span></span>

<span data-ttu-id="01636-107">A continuación se enumeran las funciones de sesión.</span><span class="sxs-lookup"><span data-stu-id="01636-107">The session functions are listed following.</span></span>



| <span data-ttu-id="01636-108">Función</span><span class="sxs-lookup"><span data-stu-id="01636-108">Function</span></span>                                       | <span data-ttu-id="01636-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="01636-109">Description</span></span>                                                                                       |
|------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01636-110">**NetSessionDel**</span><span class="sxs-lookup"><span data-stu-id="01636-110">**NetSessionDel**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)         | <span data-ttu-id="01636-111">Elimina las conexiones actuales entre una estación de trabajo y un servidor. finaliza la sesión de red.</span><span class="sxs-lookup"><span data-stu-id="01636-111">Deletes the current connections between a workstation and server; terminates the network session.</span></span> |
| [<span data-ttu-id="01636-112">**NetSessionEnum**</span><span class="sxs-lookup"><span data-stu-id="01636-112">**NetSessionEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessionenum)       | <span data-ttu-id="01636-113">Devuelve información acerca de todas las sesiones actuales establecidas para un servidor.</span><span class="sxs-lookup"><span data-stu-id="01636-113">Returns information about all current sessions established for a server.</span></span>                          |
| [<span data-ttu-id="01636-114">**NetSessionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="01636-114">**NetSessionGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessiongetinfo) | <span data-ttu-id="01636-115">Devuelve información sobre una sesión determinada.</span><span class="sxs-lookup"><span data-stu-id="01636-115">Returns information about a particular session.</span></span>                                                   |



 

<span data-ttu-id="01636-116">Una *sesión* es un vínculo entre una estación de trabajo y un servidor.</span><span class="sxs-lookup"><span data-stu-id="01636-116">A *session* is a link between a workstation and a server.</span></span> <span data-ttu-id="01636-117">Una sesión se establece la primera vez que una estación de trabajo realiza una conexión a un recurso compartido en el servidor.</span><span class="sxs-lookup"><span data-stu-id="01636-117">A session is established the first time a workstation makes a connection to a shared resource on the server.</span></span> <span data-ttu-id="01636-118">Hasta que finalice la sesión, todas las conexiones posteriores entre la estación de trabajo y el servidor formarán parte de la misma sesión.</span><span class="sxs-lookup"><span data-stu-id="01636-118">Until the session ends, all further connections between the workstation and the server are part of the same session.</span></span> <span data-ttu-id="01636-119">Para finalizar una sesión, una aplicación en el extremo del servidor de una conexión llama a la función [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel) .</span><span class="sxs-lookup"><span data-stu-id="01636-119">To end a session, an application on the server end of a connection calls the [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel) function.</span></span>

<span data-ttu-id="01636-120">Las funciones de sesión de administración de red administran la información por usuario con el parámetro de *nombre de usuario* .</span><span class="sxs-lookup"><span data-stu-id="01636-120">The network management session functions manage information on a per-user basis with the *username* parameter.</span></span> <span data-ttu-id="01636-121">Dado que puede haber varios usuarios por sesión, este parámetro es necesario para tener acceso a la información específica del usuario para la sesión.</span><span class="sxs-lookup"><span data-stu-id="01636-121">Because there can be multiple users per session, this parameter is necessary to access the user-specific information for the session.</span></span>

<span data-ttu-id="01636-122">Las funciones de sesión están disponibles en cinco niveles de información:</span><span class="sxs-lookup"><span data-stu-id="01636-122">Session functions are available at five information levels:</span></span>

<dl>

[<span data-ttu-id="01636-123">**Información de sesión \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="01636-123">**SESSION\_INFO\_0**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_0)  
[<span data-ttu-id="01636-124">**Información de sesión \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="01636-124">**SESSION\_INFO\_1**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_1)  
[<span data-ttu-id="01636-125">**Información de sesión \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="01636-125">**SESSION\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_2)  
[<span data-ttu-id="01636-126">**Información de la sesión \_ \_ 10**</span><span class="sxs-lookup"><span data-stu-id="01636-126">**SESSION\_INFO\_10**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_10)  
[<span data-ttu-id="01636-127">**Información de sesión \_ \_ 502**</span><span class="sxs-lookup"><span data-stu-id="01636-127">**SESSION\_INFO\_502**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_502)  
</dl>

<span data-ttu-id="01636-128">Si programa para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz de servicio Active Directory (ADSI) para lograr la misma funcionalidad que puede lograr mediante una llamada a las funciones de sesión de administración de red.</span><span class="sxs-lookup"><span data-stu-id="01636-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management session functions.</span></span> <span data-ttu-id="01636-129">Para obtener más información, vea [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) y [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span><span class="sxs-lookup"><span data-stu-id="01636-129">For more information, see [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
