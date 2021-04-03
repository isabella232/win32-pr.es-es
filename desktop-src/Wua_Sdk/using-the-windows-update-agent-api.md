---
description: Para usar la API del agente de Windows Update (WUA), cree primero una instancia de una de las interfaces creando el objeto a partir de la coclase adecuada.
ms.assetid: b304971d-584a-4d0f-be5b-26f0ab315ec9
title: Uso de la API del agente Windows Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b5d155a2354b68135d0742f765dffb01e7235f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810201"
---
# <a name="using-the-windows-update-agent-api"></a><span data-ttu-id="a22d8-103">Uso de la API del agente Windows Update</span><span class="sxs-lookup"><span data-stu-id="a22d8-103">Using the Windows Update Agent API</span></span>

<span data-ttu-id="a22d8-104">Para usar la API del agente de Windows Update (WUA), cree primero una instancia de una de las interfaces creando el objeto a partir de la coclase adecuada.</span><span class="sxs-lookup"><span data-stu-id="a22d8-104">To use the Windows Update Agent (WUA) API, first create an instance of one of the interfaces by creating the object from the appropriate coclass.</span></span>

<span data-ttu-id="a22d8-105">En los temas siguientes se describe cómo puede usar la API de WUA:</span><span class="sxs-lookup"><span data-stu-id="a22d8-105">The following topics describe how you can use the WUA API:</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="a22d8-106">Estos scripts están diseñados para mostrar el uso de las API del agente de Windows Update y proporcionan ejemplos de cómo los desarrolladores pueden usar estas API para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="a22d8-106">These scripts are intended to demonstrate the use of the Windows Update Agent APIs, and provide examples of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="a22d8-107">Estos scripts no están diseñados como código de producción y Microsoft no admite los propios scripts (aunque se admiten las API de agente de Windows Update subyacentes).</span><span class="sxs-lookup"><span data-stu-id="a22d8-107">These scripts are not intended as production code, and the scripts themselves are not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 

-   [<span data-ttu-id="a22d8-108">Modelo de objetos del agente Windows Update</span><span class="sxs-lookup"><span data-stu-id="a22d8-108">Windows Update Agent Object Model</span></span>](windows-update-agent-object-model.md)
-   [<span data-ttu-id="a22d8-109">Determinar la versión actual de WUA</span><span class="sxs-lookup"><span data-stu-id="a22d8-109">Determining the Current Version of WUA</span></span>](determining-the-current-version-of-wua.md)
-   [<span data-ttu-id="a22d8-110">Actualización del agente de Windows Update</span><span class="sxs-lookup"><span data-stu-id="a22d8-110">Updating the Windows Update Agent</span></span>](updating-the-windows-update-agent.md)
-   [<span data-ttu-id="a22d8-111">Actualización de los archivos de encabezado del agente Windows Update</span><span class="sxs-lookup"><span data-stu-id="a22d8-111">Updating Windows Update Agent Header Files</span></span>](updating-windows-update-agent-header-files.md)
-   [<span data-ttu-id="a22d8-112">Usar WUA para buscar actualizaciones sin conexión</span><span class="sxs-lookup"><span data-stu-id="a22d8-112">Using WUA to Scan for Updates Offline</span></span>](using-wua-to-scan-for-updates-offline.md)
-   [<span data-ttu-id="a22d8-113">Métodos y propiedades protegidos en la API de WUA</span><span class="sxs-lookup"><span data-stu-id="a22d8-113">Secured Methods and Properties in the WUA API</span></span>](secured-methods-and-properties-in-the-wua-api.md)
-   [<span data-ttu-id="a22d8-114">Buscar, descargar e instalar actualizaciones</span><span class="sxs-lookup"><span data-stu-id="a22d8-114">Searching, Downloading, and Installing Updates</span></span>](searching--downloading--and-installing-updates.md)
-   [<span data-ttu-id="a22d8-115">Búsqueda, descarga e instalación de actualizaciones específicas</span><span class="sxs-lookup"><span data-stu-id="a22d8-115">Searching, Downloading, and Installing Specific Updates</span></span>](searching--downloading--and-installing-specific-updates.md)
-   [<span data-ttu-id="a22d8-116">Usar WUA desde un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="a22d8-116">Using WUA From a Remote Computer</span></span>](using-wua-from-a-remote-computer.md)
-   [<span data-ttu-id="a22d8-117">Instrucciones para las operaciones de WUA asincrónicas</span><span class="sxs-lookup"><span data-stu-id="a22d8-117">Guidelines for Asynchronous WUA Operations</span></span>](guidelines-for-asynchronous-wua-operations.md)
-   [<span data-ttu-id="a22d8-118">Usar WUA desde un proceso de inicio de sesión secundario (ejecutar como)</span><span class="sxs-lookup"><span data-stu-id="a22d8-118">Using WUA from a Secondary Logon (Run As) Process</span></span>](using-wua-from-a-secondary-logon--run-as--process.md)
-   [<span data-ttu-id="a22d8-119">Códigos de error y correctos de WUA</span><span class="sxs-lookup"><span data-stu-id="a22d8-119">WUA Success and Error Codes</span></span>](wua-success-and-error-codes-.md)
-   [<span data-ttu-id="a22d8-120">Códigos de error de red de WUA</span><span class="sxs-lookup"><span data-stu-id="a22d8-120">WUA Networking Error Codes</span></span>](wua-networking-error-codes-.md)

 

 



