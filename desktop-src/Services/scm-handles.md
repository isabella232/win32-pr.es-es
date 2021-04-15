---
description: El SCM es compatible con los tipos de controladores para permitir el acceso a los siguientes objetos.
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: Identificadores de SCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8a84fb09dbc95f3e1b5f5cee432de616f5ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669722"
---
# <a name="scm-handles"></a><span data-ttu-id="d5230-103">Identificadores de SCM</span><span class="sxs-lookup"><span data-stu-id="d5230-103">SCM Handles</span></span>

<span data-ttu-id="d5230-104">El SCM es compatible con los tipos de controladores para permitir el acceso a los siguientes objetos.</span><span class="sxs-lookup"><span data-stu-id="d5230-104">The SCM supports handle types to allow access to the following objects.</span></span>

-   <span data-ttu-id="d5230-105">La base de datos de servicios instalados.</span><span class="sxs-lookup"><span data-stu-id="d5230-105">The database of installed services.</span></span>
-   <span data-ttu-id="d5230-106">Un servicio de.</span><span class="sxs-lookup"><span data-stu-id="d5230-106">A service.</span></span>
-   <span data-ttu-id="d5230-107">Bloqueo de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d5230-107">The database lock.</span></span>

<span data-ttu-id="d5230-108">Un objeto SCManager representa la base de datos de servicios instalados.</span><span class="sxs-lookup"><span data-stu-id="d5230-108">An SCManager object represents the database of installed services.</span></span> <span data-ttu-id="d5230-109">Es un objeto contenedor que contiene objetos de servicio.</span><span class="sxs-lookup"><span data-stu-id="d5230-109">It is a container object that holds service objects.</span></span> <span data-ttu-id="d5230-110">La función [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) devuelve un identificador a un objeto SCManager en un equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="d5230-110">The [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function returns a handle to an SCManager object on a specified computer.</span></span> <span data-ttu-id="d5230-111">Este identificador se usa al instalar, eliminar, abrir y enumerar servicios y al bloquear la base de datos de servicios.</span><span class="sxs-lookup"><span data-stu-id="d5230-111">This handle is used when installing, deleting, opening, and enumerating services and when locking the services database.</span></span>

<span data-ttu-id="d5230-112">Un objeto de servicio representa un servicio instalado.</span><span class="sxs-lookup"><span data-stu-id="d5230-112">A service object represents an installed service.</span></span> <span data-ttu-id="d5230-113">Las funciones [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) y [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) devuelven los identificadores de los servicios instalados.</span><span class="sxs-lookup"><span data-stu-id="d5230-113">The [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) functions return handles to installed services.</span></span>

<span data-ttu-id="d5230-114">Las funciones [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera), [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)y [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) pueden solicitar distintos tipos de acceso a los objetos de servicio y SCManager.</span><span class="sxs-lookup"><span data-stu-id="d5230-114">The [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera), [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea), and [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) functions can request different types of access to SCManager and service objects.</span></span> <span data-ttu-id="d5230-115">El acceso solicitado se concede o se deniega según el token de acceso del proceso de llamada y el descriptor de seguridad asociado al objeto SCManager o Service.</span><span class="sxs-lookup"><span data-stu-id="d5230-115">The requested access is granted or denied depending on the access token of the calling process and the security descriptor associated with the SCManager or service object.</span></span>

<span data-ttu-id="d5230-116">La función [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) cierra los identificadores de SCManager y los objetos de servicio.</span><span class="sxs-lookup"><span data-stu-id="d5230-116">The [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) function closes handles to SCManager and service objects.</span></span> <span data-ttu-id="d5230-117">Cuando ya no necesite estos identificadores, asegúrese de cerrarlos.</span><span class="sxs-lookup"><span data-stu-id="d5230-117">When you no longer need these handles, be sure to close them.</span></span>

 

 



