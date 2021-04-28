---
description: Eliminación de windows Movie Maker
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: Eliminación de windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36df5ffe4498e05de9fcbbaadf49f8fc32c91b0f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116273"
---
# <a name="removal-of-windows-movie-maker"></a><span data-ttu-id="85374-103">Eliminación de windows Movie Maker</span><span class="sxs-lookup"><span data-stu-id="85374-103">Removal of Windows Movie Maker</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="85374-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="85374-104">Affected Platforms</span></span>

<span data-ttu-id="85374-105">**Clientes:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="85374-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="85374-106">**Servidores:** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="85374-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="85374-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="85374-107">Feature Impact</span></span>

 <span data-ttu-id="85374-108">**Gravedad:** alta</span><span class="sxs-lookup"><span data-stu-id="85374-108">**Severity** - High</span></span>  
<span data-ttu-id="85374-109">**Frecuencia:** media</span><span class="sxs-lookup"><span data-stu-id="85374-109">**Frequency** - Medium</span></span>  


## <a name="description"></a><span data-ttu-id="85374-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="85374-110">Description</span></span>

<span data-ttu-id="85374-111">Microsoft está desusando y quitando la utilidad Movie Maker Windows.</span><span class="sxs-lookup"><span data-stu-id="85374-111">Microsoft is deprecating and removing the Windows Movie Maker utility.</span></span> <span data-ttu-id="85374-112">Esto incluye:</span><span class="sxs-lookup"><span data-stu-id="85374-112">This includes:</span></span>

-   <span data-ttu-id="85374-113">Todos los puntos de entrada a Windows Movie Maker (por ejemplo, menú Inicio, Iniciar > ejecutar)</span><span class="sxs-lookup"><span data-stu-id="85374-113">All entry points to Windows Movie Maker (for example, Start Menu, Start > Run)</span></span>
-   <span data-ttu-id="85374-114">Todos los archivos binarios usados por Windows Movie Maker (todo lo que estaba en %ProgramFiles% \\ Movie Maker)</span><span class="sxs-lookup"><span data-stu-id="85374-114">All binaries that were used by Windows Movie Maker (everything that was in %ProgramFiles%\\Movie Maker)</span></span>

<span data-ttu-id="85374-115">Sin embargo, los archivos de proyecto Movie Maker usuario permanecerán en el sistema y serán accesibles para otras aplicaciones que admitan este formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="85374-115">However, a user's Movie Maker project files will remain on the system and be accessible to other applications that support this file format.</span></span>

## <a name="manifestation"></a><span data-ttu-id="85374-116">Manifestación</span><span class="sxs-lookup"><span data-stu-id="85374-116">Manifestation</span></span>

<span data-ttu-id="85374-117">La eliminación de windows Movie Maker da como resultado lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="85374-117">Remove of Windows Movie Maker results in the following:</span></span>

-   <span data-ttu-id="85374-118">Cualquier intento de iniciar Windows Movie Maker con sus argumentos de línea de comandos producirá un error</span><span class="sxs-lookup"><span data-stu-id="85374-118">Any attempt to launch Windows Movie Maker with its command line arguments will fail</span></span>
-   <span data-ttu-id="85374-119">Los complementos que se instalaron para habilitar nuevas transformaciones y animaciones permanecerán instalados, pero no se exponen al usuario final.</span><span class="sxs-lookup"><span data-stu-id="85374-119">Any plug-ins that were installed to enable new transforms and animations will remain installed but will not be exposed to the end user</span></span>

## <a name="solution"></a><span data-ttu-id="85374-120">Solución</span><span class="sxs-lookup"><span data-stu-id="85374-120">Solution</span></span>

<span data-ttu-id="85374-121">Para tener esta funcionalidad en el futuro, un usuario deberá instalar una aplicación similar de Microsoft u otro proveedor de software.</span><span class="sxs-lookup"><span data-stu-id="85374-121">To have such functionality in the future, a user will need to install a similar application from Microsoft or another software provider.</span></span>

 

 



