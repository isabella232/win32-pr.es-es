---
description: Comprenda las funciones de sesión en la administración de recursos compartidos de red. Estas funciones controlan las sesiones de red establecidas entre estaciones de trabajo y servidores.
ms.assetid: 931455e3-1301-4a68-93c3-2674b3d4c491
title: Funciones de sesión (Administración de recursos compartidos de red)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdde451eb2942171569b24c36aae5d5742208e5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409728"
---
# <a name="session-functions-network-share-management"></a><span data-ttu-id="fce27-104">Funciones de sesión (Administración de recursos compartidos de red)</span><span class="sxs-lookup"><span data-stu-id="fce27-104">Session Functions (Network Share Management)</span></span>

<span data-ttu-id="fce27-105">Las funciones de sesión de administración de red controlan las sesiones de red establecidas entre estaciones de trabajo y servidores.</span><span class="sxs-lookup"><span data-stu-id="fce27-105">The network management session functions control network sessions established between workstations and servers.</span></span> <span data-ttu-id="fce27-106">Las funciones requieren que el servicio de servidor se pueda iniciar en el servidor.</span><span class="sxs-lookup"><span data-stu-id="fce27-106">The functions require that the server service be started on the server.</span></span>

<span data-ttu-id="fce27-107">Las funciones de sesión se enumeran a continuación.</span><span class="sxs-lookup"><span data-stu-id="fce27-107">The session functions are listed following.</span></span>



| <span data-ttu-id="fce27-108">Función</span><span class="sxs-lookup"><span data-stu-id="fce27-108">Function</span></span>                                       | <span data-ttu-id="fce27-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="fce27-109">Description</span></span>                                                                                       |
|------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fce27-110">**NetSessionDel**</span><span class="sxs-lookup"><span data-stu-id="fce27-110">**NetSessionDel**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)         | <span data-ttu-id="fce27-111">Elimina las conexiones actuales entre una estación de trabajo y un servidor; finaliza la sesión de red.</span><span class="sxs-lookup"><span data-stu-id="fce27-111">Deletes the current connections between a workstation and server; terminates the network session.</span></span> |
| [<span data-ttu-id="fce27-112">**NetSessionEnum**</span><span class="sxs-lookup"><span data-stu-id="fce27-112">**NetSessionEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessionenum)       | <span data-ttu-id="fce27-113">Devuelve información sobre todas las sesiones actuales establecidas para un servidor.</span><span class="sxs-lookup"><span data-stu-id="fce27-113">Returns information about all current sessions established for a server.</span></span>                          |
| [<span data-ttu-id="fce27-114">**NetSessionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="fce27-114">**NetSessionGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessiongetinfo) | <span data-ttu-id="fce27-115">Devuelve información sobre una sesión determinada.</span><span class="sxs-lookup"><span data-stu-id="fce27-115">Returns information about a particular session.</span></span>                                                   |



 

<span data-ttu-id="fce27-116">Una *sesión* es un vínculo entre una estación de trabajo y un servidor.</span><span class="sxs-lookup"><span data-stu-id="fce27-116">A *session* is a link between a workstation and a server.</span></span> <span data-ttu-id="fce27-117">Se establece una sesión la primera vez que una estación de trabajo realiza una conexión a un recurso compartido en el servidor.</span><span class="sxs-lookup"><span data-stu-id="fce27-117">A session is established the first time a workstation makes a connection to a shared resource on the server.</span></span> <span data-ttu-id="fce27-118">Hasta que finalice la sesión, todas las conexiones lejos entre la estación de trabajo y el servidor forman parte de la misma sesión.</span><span class="sxs-lookup"><span data-stu-id="fce27-118">Until the session ends, all further connections between the workstation and the server are part of the same session.</span></span> <span data-ttu-id="fce27-119">Para finalizar una sesión, una aplicación en el extremo del servidor de una conexión llama a la [**función NetSessionDel.**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)</span><span class="sxs-lookup"><span data-stu-id="fce27-119">To end a session, an application on the server end of a connection calls the [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel) function.</span></span>

<span data-ttu-id="fce27-120">Las funciones de sesión de administración de red administran la información por usuario con el parámetro *username.*</span><span class="sxs-lookup"><span data-stu-id="fce27-120">The network management session functions manage information on a per-user basis with the *username* parameter.</span></span> <span data-ttu-id="fce27-121">Dado que puede haber varios usuarios por sesión, este parámetro es necesario para tener acceso a la información específica del usuario para la sesión.</span><span class="sxs-lookup"><span data-stu-id="fce27-121">Because there can be multiple users per session, this parameter is necessary to access the user-specific information for the session.</span></span>

<span data-ttu-id="fce27-122">Las funciones de sesión están disponibles en cinco niveles de información:</span><span class="sxs-lookup"><span data-stu-id="fce27-122">Session functions are available at five information levels:</span></span>

<dl>

[<span data-ttu-id="fce27-123">**INFORMACIÓN \_ DE SESIÓN \_ 0**</span><span class="sxs-lookup"><span data-stu-id="fce27-123">**SESSION\_INFO\_0**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_0)  
[<span data-ttu-id="fce27-124">**INFORMACIÓN \_ DE SESIÓN \_ 1**</span><span class="sxs-lookup"><span data-stu-id="fce27-124">**SESSION\_INFO\_1**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_1)  
[<span data-ttu-id="fce27-125">**INFORMACIÓN \_ DE SESIÓN \_ 2**</span><span class="sxs-lookup"><span data-stu-id="fce27-125">**SESSION\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_2)  
[<span data-ttu-id="fce27-126">**INFORMACIÓN \_ DE SESIÓN \_ 10**</span><span class="sxs-lookup"><span data-stu-id="fce27-126">**SESSION\_INFO\_10**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_10)  
[<span data-ttu-id="fce27-127">**INFORMACIÓN \_ DE SESIÓN \_ 502**</span><span class="sxs-lookup"><span data-stu-id="fce27-127">**SESSION\_INFO\_502**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_502)  
</dl>

<span data-ttu-id="fce27-128">Si está programando para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz de servicio (ADSI) de Active Directory para lograr la misma funcionalidad que puede lograr llamando a las funciones de sesión de administración de red.</span><span class="sxs-lookup"><span data-stu-id="fce27-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management session functions.</span></span> <span data-ttu-id="fce27-129">Para obtener más información, [**vea IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span><span class="sxs-lookup"><span data-stu-id="fce27-129">For more information, see [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
