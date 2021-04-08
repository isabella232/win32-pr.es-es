---
title: Actualización de reglas de detección de aplicaciones de seguridad
description: Actualización de reglas de detección de aplicaciones de seguridad
ms.assetid: A272C09B-A777-4119-BAB9-F91ABC03717A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242c6f9da8d474c16fab7573e216d3157f93b014
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104078501"
---
# <a name="security-app-detection-rules-update"></a><span data-ttu-id="d0eec-103">Actualización de reglas de detección de aplicaciones de seguridad</span><span class="sxs-lookup"><span data-stu-id="d0eec-103">Security app detection rules update</span></span>

## <a name="platforms"></a><span data-ttu-id="d0eec-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="d0eec-104">Platforms</span></span>

<span data-ttu-id="d0eec-105">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="d0eec-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="d0eec-106">**Servidores** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d0eec-106">**Servers** – Windows Server 2012</span></span>  


### <a name="description"></a><span data-ttu-id="d0eec-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0eec-107">Description</span></span>

<span data-ttu-id="d0eec-108">Todas las aplicaciones de la tienda Windows que se agregan en Windows 8 se instalan en una ubicación común en "archivos de programa" (% ProgramFiles%) se denomina \\ archivos de programa \\ WindowsApps.</span><span class="sxs-lookup"><span data-stu-id="d0eec-108">The Windows Store apps being added in Windows 8 are all being installed to a common location under “Program Files” (%programfiles%) called \\program files\\WindowsApps.</span></span>

### <a name="manifestation"></a><span data-ttu-id="d0eec-109">Manifestación</span><span class="sxs-lookup"><span data-stu-id="d0eec-109">Manifestation</span></span>

<span data-ttu-id="d0eec-110">Esto puede producir colisiones con las configuraciones existentes y algunos detectores antivirus/antimalware ven esta ubicación como una posible ubicación que es una causa de preocupación.</span><span class="sxs-lookup"><span data-stu-id="d0eec-110">This can cause collisions with existing configurations, and some antivirus/anti-malware detectors see this location as a potential location that is a cause for concern.</span></span>

### <a name="mitigation"></a><span data-ttu-id="d0eec-111">Mitigación</span><span class="sxs-lookup"><span data-stu-id="d0eec-111">Mitigation</span></span>

<span data-ttu-id="d0eec-112">Las recomendaciones actuales son:</span><span class="sxs-lookup"><span data-stu-id="d0eec-112">The current recommendations are:</span></span>

-   <span data-ttu-id="d0eec-113">Salir de \\ archivos de programa \\ WindowsApps para almacenar cualquier aplicación personalizada</span><span class="sxs-lookup"><span data-stu-id="d0eec-113">Move away from \\program files\\WindowsApps for storing any custom apps</span></span>
-   <span data-ttu-id="d0eec-114">Los proveedores de antivirus o antimalware deben actualizar su heurística para que no identifiquen esa ubicación como una ubicación de malware.</span><span class="sxs-lookup"><span data-stu-id="d0eec-114">Antivirus/antimalware vendors should update their heuristics so they do not identify that location as a malware location</span></span>

 

 




