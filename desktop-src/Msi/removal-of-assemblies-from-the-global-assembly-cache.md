---
description: El Windows Installer determina si se permite la eliminación de un ensamblado Common Language Runtime basado en una lista de clientes que se mantiene independientemente del ensamblado.
ms.assetid: 3f83ad88-e6a4-484b-bcf5-8e2e65f1f41f
title: Eliminación de ensamblados de la caché global de ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d50bc2856891c67952a27b27a27cf1cf2d1d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276839"
---
# <a name="removal-of-assemblies-from-the-global-assembly-cache"></a><span data-ttu-id="0197e-103">Eliminación de ensamblados de la caché global de ensamblados</span><span class="sxs-lookup"><span data-stu-id="0197e-103">Removal of Assemblies from the Global Assembly Cache</span></span>

<span data-ttu-id="0197e-104">El Windows Installer determina si se permite la eliminación de un ensamblado Common Language Runtime basado en una lista de clientes que se mantiene independientemente del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="0197e-104">The Windows Installer determines whether to allow the removal of a common language runtime assembly based upon a client list it keeps independently of the assembly.</span></span> <span data-ttu-id="0197e-105">El Windows Installer mantiene un bit de anclaje para representar a los clientes de Windows Installer del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="0197e-105">The Windows Installer keeps one pin bit to represent Windows Installer clients of the assembly.</span></span> <span data-ttu-id="0197e-106">El instalador ancla el ensamblado para el primer Windows Installer cliente y lo desancla cuando se quita el último cliente de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0197e-106">The installer pins the assembly for the first Windows Installer client and unpins it when the last Windows Installer client is removed.</span></span> <span data-ttu-id="0197e-107">El ensamblado mantiene un bit de anclaje por cada cliente de un ensamblado.</span><span class="sxs-lookup"><span data-stu-id="0197e-107">The assembly maintains a pin bit for every client of an assembly.</span></span>

<span data-ttu-id="0197e-108">El Windows Installer no es responsable directamente de la eliminación física de los ensamblados de Common Language Runtime del equipo.</span><span class="sxs-lookup"><span data-stu-id="0197e-108">The Windows Installer is not directly responsible for the physical removal of common language runtime assemblies from the computer.</span></span> <span data-ttu-id="0197e-109">El instalador desancla el ensamblado cuando se quita el último Windows Installer cliente.</span><span class="sxs-lookup"><span data-stu-id="0197e-109">The installer unpins the assembly when the last Windows Installer client is removed.</span></span> <span data-ttu-id="0197e-110">Si el Windows Installer es el último cliente del ensamblado, el Common Language Runtime proporciona la opción de forzar una limpieza sincrónica del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="0197e-110">If the Windows Installer is the last client of the assembly, the common language runtime provides the option to force a synchronous cleanup of the assembly.</span></span> <span data-ttu-id="0197e-111">El proceso de limpieza es atómico y no hay ningún aprovisionamiento para una "reversión" en este momento.</span><span class="sxs-lookup"><span data-stu-id="0197e-111">The cleanup process is atomic and there is no provision for a "rollback" at this point.</span></span> <span data-ttu-id="0197e-112">Todo desanclaje de ensamblados de Common Language Runtime debe producirse después de que el usuario haya tenido la oportunidad de cancelar la instalación o la eliminación.</span><span class="sxs-lookup"><span data-stu-id="0197e-112">All unpinning of common language runtime assemblies must occur after the user has had a chance to cancel the installation or removal.</span></span>

 

 



