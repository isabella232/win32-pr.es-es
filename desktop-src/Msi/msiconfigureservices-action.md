---
description: La acción MsiConfigureServices configura un servicio para el sistema. Esta acción consulta las tablas MsiServiceConfig y MsiServiceConfigFailureActions.
ms.assetid: 63bd4690-0649-4e23-a8cd-527b3c517dae
title: Acción MsiConfigureServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f2321bcdfaeede8e80d7f4c341f5a099690952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653107"
---
# <a name="msiconfigureservices-action"></a><span data-ttu-id="96fbb-104">Acción MsiConfigureServices</span><span class="sxs-lookup"><span data-stu-id="96fbb-104">MsiConfigureServices Action</span></span>

<span data-ttu-id="96fbb-105">La acción MsiConfigureServices configura un servicio para el sistema.</span><span class="sxs-lookup"><span data-stu-id="96fbb-105">The MsiConfigureServices action configures a service for the system.</span></span> <span data-ttu-id="96fbb-106">Esta acción consulta las tablas [MsiServiceConfig](msiserviceconfig-table.md) y [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) .</span><span class="sxs-lookup"><span data-stu-id="96fbb-106">This action queries the [MsiServiceConfig](msiserviceconfig-table.md) and the [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) tables.</span></span>

<span data-ttu-id="96fbb-107">**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="96fbb-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="96fbb-108">Esta acción está disponible a partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="96fbb-108">This action is available beginning with Windows Installer 5.0.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="96fbb-109">Los servicios de Windows proporcionan la capacidad de realizar automáticamente acciones predefinidas en respuesta a un error en un servicio.</span><span class="sxs-lookup"><span data-stu-id="96fbb-109">Windows Services provides the ability to automatically perform predefined actions in response to a failure in a service.</span></span> <span data-ttu-id="96fbb-110">Para admitir la configuración mediante programación de estas **acciones de recuperación** cuando se produce un error en un servicio, se ha agregado [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) a MSI en la versión MSI 5,0.</span><span class="sxs-lookup"><span data-stu-id="96fbb-110">To support programmatically setting up these **Recovery Actions** when a service fails, [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) was added to MSI in version MSI 5.0.</span></span> <span data-ttu-id="96fbb-111">Sin embargo, esta funcionalidad no funciona según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="96fbb-111">However, this functionality is not working as expected.</span></span>
>
> <span data-ttu-id="96fbb-112">Para solucionar este problema, un desarrollador de aplicaciones debe utilizar la funcionalidad de **acción personalizada** en MSI para ejecutar **sc.exe** y establecer las **Opciones de recuperación** de manera adecuada.</span><span class="sxs-lookup"><span data-stu-id="96fbb-112">To workaround this issue, an application developer should use the **Custom Action** functionality in MSI to run **sc.exe** and set the **Recovery Options** appropriately.</span></span>

 

## <a name="sequence-restrictions"></a><span data-ttu-id="96fbb-113">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="96fbb-113">Sequence Restrictions</span></span>

<span data-ttu-id="96fbb-114">Esta acción estándar se debe usar en la secuencia siguiente.</span><span class="sxs-lookup"><span data-stu-id="96fbb-114">This standard action must be used in the following sequence.</span></span>

[<span data-ttu-id="96fbb-115">StopServices</span><span class="sxs-lookup"><span data-stu-id="96fbb-115">StopServices</span></span>](stopservices-action.md)

[<span data-ttu-id="96fbb-116">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="96fbb-116">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="96fbb-117">Cualquiera de las siguientes acciones: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)y [RemoveDuplicateFiles](removeduplicatefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="96fbb-117">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>

[<span data-ttu-id="96fbb-118">InstallServices</span><span class="sxs-lookup"><span data-stu-id="96fbb-118">InstallServices</span></span>](installservices-action.md)

<span data-ttu-id="96fbb-119">MsiConfigureServices</span><span class="sxs-lookup"><span data-stu-id="96fbb-119">MsiConfigureServices</span></span>

[<span data-ttu-id="96fbb-120">StartServices</span><span class="sxs-lookup"><span data-stu-id="96fbb-120">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="96fbb-121">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="96fbb-121">ActionData Messages</span></span>

<span data-ttu-id="96fbb-122">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="96fbb-122">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="96fbb-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96fbb-123">Remarks</span></span>

<span data-ttu-id="96fbb-124">Esta acción requiere que el usuario sea administrador o que tenga privilegios elevados con permisos para instalar servicios o que la aplicación forme parte de una instalación administrada.</span><span class="sxs-lookup"><span data-stu-id="96fbb-124">This action requires that the user be an administrator or have elevated privileges with permission to install services or that the application be part of a managed installation.</span></span>

 

 



