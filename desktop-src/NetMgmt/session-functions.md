---
title: Funciones de sesión (administración de red)
description: Las funciones de sesión de administración de red controlan las sesiones de red establecidas entre estaciones de trabajo y servidores. Las funciones requieren que se inicie el servicio servidor en el servidor.
ms.assetid: ef912cd9-be5c-4202-89aa-e60f275e8938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b1e0236881b50f0363a6c872394cfe42f44748
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103904954"
---
# <a name="session-functions-network-management"></a><span data-ttu-id="815f1-104">Funciones de sesión (administración de red)</span><span class="sxs-lookup"><span data-stu-id="815f1-104">Session Functions (Network Management)</span></span>

<span data-ttu-id="815f1-105">Las funciones de sesión de administración de red controlan las sesiones de red establecidas entre estaciones de trabajo y servidores.</span><span class="sxs-lookup"><span data-stu-id="815f1-105">The network management session functions control network sessions established between workstations and servers.</span></span> <span data-ttu-id="815f1-106">Las funciones requieren que se inicie el servicio servidor en el servidor.</span><span class="sxs-lookup"><span data-stu-id="815f1-106">The functions require that the server service be started on the server.</span></span>

<span data-ttu-id="815f1-107">A continuación se enumeran las funciones de sesión.</span><span class="sxs-lookup"><span data-stu-id="815f1-107">The session functions are listed following.</span></span>



| <span data-ttu-id="815f1-108">Función</span><span class="sxs-lookup"><span data-stu-id="815f1-108">Function</span></span>                                      | <span data-ttu-id="815f1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="815f1-109">Description</span></span>                                                                                       |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="815f1-110">**NetSessionDel**</span><span class="sxs-lookup"><span data-stu-id="815f1-110">**NetSessionDel**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel)         | <span data-ttu-id="815f1-111">Elimina las conexiones actuales entre una estación de trabajo y un servidor. finaliza la sesión de red.</span><span class="sxs-lookup"><span data-stu-id="815f1-111">Deletes the current connections between a workstation and server; terminates the network session.</span></span> |
| [<span data-ttu-id="815f1-112">**NetSessionEnum**</span><span class="sxs-lookup"><span data-stu-id="815f1-112">**NetSessionEnum**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netsessionenum)       | <span data-ttu-id="815f1-113">Devuelve información acerca de todas las sesiones actuales establecidas para un servidor.</span><span class="sxs-lookup"><span data-stu-id="815f1-113">Returns information about all current sessions established for a server.</span></span>                          |
| [<span data-ttu-id="815f1-114">**NetSessionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="815f1-114">**NetSessionGetInfo**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) | <span data-ttu-id="815f1-115">Devuelve información sobre una sesión determinada.</span><span class="sxs-lookup"><span data-stu-id="815f1-115">Returns information about a particular session.</span></span>                                                   |



 

<span data-ttu-id="815f1-116">Una *sesión* es un vínculo entre una estación de trabajo y un servidor.</span><span class="sxs-lookup"><span data-stu-id="815f1-116">A *session* is a link between a workstation and a server.</span></span> <span data-ttu-id="815f1-117">Una sesión se establece la primera vez que una estación de trabajo realiza una conexión a un recurso compartido en el servidor.</span><span class="sxs-lookup"><span data-stu-id="815f1-117">A session is established the first time a workstation makes a connection to a shared resource on the server.</span></span> <span data-ttu-id="815f1-118">Hasta que finalice la sesión, todas las conexiones posteriores entre la estación de trabajo y el servidor formarán parte de la misma sesión.</span><span class="sxs-lookup"><span data-stu-id="815f1-118">Until the session ends, all further connections between the workstation and the server are part of the same session.</span></span> <span data-ttu-id="815f1-119">Para finalizar una sesión, una aplicación en el extremo del servidor de una conexión llama a la función [**NetSessionDel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel) .</span><span class="sxs-lookup"><span data-stu-id="815f1-119">To end a session, an application on the server end of a connection calls the [**NetSessionDel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel) function.</span></span>

<span data-ttu-id="815f1-120">Las funciones de sesión de administración de red administran la información por usuario con el parámetro de *nombre de usuario* .</span><span class="sxs-lookup"><span data-stu-id="815f1-120">The network management session functions manage information on a per-user basis with the *username* parameter.</span></span> <span data-ttu-id="815f1-121">Dado que puede haber varios usuarios por sesión, este parámetro es necesario para tener acceso a la información específica del usuario para la sesión.</span><span class="sxs-lookup"><span data-stu-id="815f1-121">Because there can be multiple users per session, this parameter is necessary to access the user-specific information for the session.</span></span>

<span data-ttu-id="815f1-122">Las funciones de sesión están disponibles en los siguientes niveles de información:</span><span class="sxs-lookup"><span data-stu-id="815f1-122">Session functions are available at the following information levels:</span></span>

-   [<span data-ttu-id="815f1-123">**Información de sesión \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="815f1-123">**SESSION\_INFO\_0**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_0)
-   [<span data-ttu-id="815f1-124">**Información de sesión \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="815f1-124">**SESSION\_INFO\_1**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_1)
-   [<span data-ttu-id="815f1-125">**Información de sesión \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="815f1-125">**SESSION\_INFO\_2**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_2)
-   [<span data-ttu-id="815f1-126">**Información de la sesión \_ \_ 10**</span><span class="sxs-lookup"><span data-stu-id="815f1-126">**SESSION\_INFO\_10**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_10)
-   [<span data-ttu-id="815f1-127">**Información de sesión \_ \_ 502**</span><span class="sxs-lookup"><span data-stu-id="815f1-127">**SESSION\_INFO\_502**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_502)

<span data-ttu-id="815f1-128">Si programa para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz de servicio Active Directory (ADSI) para lograr la misma funcionalidad que puede lograr mediante una llamada a las funciones de sesión de administración de red.</span><span class="sxs-lookup"><span data-stu-id="815f1-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management session functions.</span></span> <span data-ttu-id="815f1-129">Para obtener más información, vea [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) y [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span><span class="sxs-lookup"><span data-stu-id="815f1-129">For more information, see [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
