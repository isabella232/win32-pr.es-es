---
title: Grupos de sensores
description: 'Describe tres posibles grupos de sensores: sistema, privado y sin asignar.'
ms.assetid: d7fd3c39-d719-4cfd-9af0-a87837f3f328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263275af5c7decff37ef70ad3a5396ec562562f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420950"
---
# <a name="sensor-pools"></a><span data-ttu-id="31407-103">Grupos de sensores</span><span class="sxs-lookup"><span data-stu-id="31407-103">Sensor Pools</span></span>

<span data-ttu-id="31407-104">Para admitir escenarios de autenticación de Windows y la autenticación definida por el proveedor, el servicio biométrico de Windows organiza las unidades biométricas en tres grupos de sensores posibles:</span><span class="sxs-lookup"><span data-stu-id="31407-104">To support both Windows authentication scenarios and vendor defined authentication, the Windows Biometric service organizes biometric units into three possible sensor pools:</span></span>

-   <span data-ttu-id="31407-105">**Grupo privado** : colección de unidades biométricas asignadas para uso exclusivo por parte de una aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="31407-105">**Private pool** a collection of biometric units allocated for exclusive use by a client application.</span></span> <span data-ttu-id="31407-106">Los grupos privados pueden admitir escenarios de autenticación que no están basados en Windows y permiten que una aplicación tenga acceso al hardware de una unidad biométrica en un modo definido por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="31407-106">Private pools can support authentication scenarios that are not Windows-based, and they make it possible for an application to access the hardware of a biometric unit in a vendor-defined fashion.</span></span> <span data-ttu-id="31407-107">Puede haber tantos grupos de sensores privados en el sistema como unidades biométricas.</span><span class="sxs-lookup"><span data-stu-id="31407-107">There can be as many private sensor pools on the system as there are biometric units.</span></span>
-   <span data-ttu-id="31407-108">**Grupo de sensores del sistema** : colección de unidades biométricas que se puede compartir y que proporcionan acceso a los servicios de autenticación de Windows.</span><span class="sxs-lookup"><span data-stu-id="31407-108">**System sensor pool** a collection of sharable biometric units that provide access to Windows authentication services.</span></span> <span data-ttu-id="31407-109">Winlogon, UAC y cualquier otro cliente que asocia un SID con una plantilla biométrica específica usan este grupo.</span><span class="sxs-lookup"><span data-stu-id="31407-109">This pool is used by Winlogon, UAC, and any other client that associates a SID with a specific biometric template.</span></span> <span data-ttu-id="31407-110">Cada proveedor de servicios biométricos tiene un grupo de sensores del sistema.</span><span class="sxs-lookup"><span data-stu-id="31407-110">Each biometric service provider has one system sensor pool.</span></span>
-   <span data-ttu-id="31407-111">El **grupo sin asignar** contiene una colección (posiblemente vacía) de unidades biométricas que no están asignadas al grupo de sistema o al grupo privado.</span><span class="sxs-lookup"><span data-stu-id="31407-111">**Unassigned pool** contains a (possibly empty) collection of biometric units that are not assigned to either the system pool or the private pool.</span></span>

<span data-ttu-id="31407-112">Las aplicaciones pueden usar el grupo de sistema compartido o pueden crear un grupo privado compuesto por unidades biométricas quitadas del sistema o de grupos sin asignar.</span><span class="sxs-lookup"><span data-stu-id="31407-112">Applications can use the shared system pool or they can create a private pool made up of biometric units removed from the system or unassigned pools.</span></span> <span data-ttu-id="31407-113">Cuando una aplicación libera su grupo privado, las unidades biométricas se reconfiguran y se devuelven a sus grupos originales.</span><span class="sxs-lookup"><span data-stu-id="31407-113">When an application releases its private pool, the biometric units are reconfigured and returned to their original pools.</span></span> <span data-ttu-id="31407-114">Para evitar ataques de denegación de servicio, solo los usuarios con privilegios pueden quitar el último sensor del grupo del sistema.</span><span class="sxs-lookup"><span data-stu-id="31407-114">To prevent denial of service attacks, only privileged users are permitted to remove the last sensor from the system pool.</span></span> <span data-ttu-id="31407-115">Para obtener más información, vea los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="31407-115">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="31407-116">En esta sección</span><span class="sxs-lookup"><span data-stu-id="31407-116">In this section</span></span>



| <span data-ttu-id="31407-117">Tema</span><span class="sxs-lookup"><span data-stu-id="31407-117">Topic</span></span>                                                       | <span data-ttu-id="31407-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="31407-118">Description</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31407-119">Grupo de sensores privados</span><span class="sxs-lookup"><span data-stu-id="31407-119">Private Sensor Pool</span></span>](private-sensor-pool.md)<br/>   | <span data-ttu-id="31407-120">Colección de unidades biométricas reservadas para uso exclusivo de una aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="31407-120">A collection of biometric units reserved for exclusive use by a client application.</span></span> <span data-ttu-id="31407-121">Los grupos privados admiten métodos de autenticación propietarios y permiten que una aplicación cliente tenga acceso a una unidad biométrica mediante los comandos de control especificados por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="31407-121">Private pools support proprietary authentication methods and enable a client application to access a biometric unit by using vendor-specified control commands.</span></span><br/> |
| [<span data-ttu-id="31407-122">Grupo de sensores del sistema</span><span class="sxs-lookup"><span data-stu-id="31407-122">System Sensor Pool</span></span>](system-sensor-pool.md)<br/>     | <span data-ttu-id="31407-123">Colección de unidades biométricas que se puede compartir y que proporcionan acceso a los servicios de autenticación de Windows.</span><span class="sxs-lookup"><span data-stu-id="31407-123">A collection of sharable biometric units that provide access to Windows authentication services.</span></span> <span data-ttu-id="31407-124">Winlogon, UAC y cualquier otro cliente que asocia un SID con una plantilla biométrica específica usan este grupo.</span><span class="sxs-lookup"><span data-stu-id="31407-124">This pool is used by Winlogon, UAC, and any other client that associates a SID with a specific biometric template.</span></span><br/>                                 |
| [<span data-ttu-id="31407-125">Comportamiento del grupo de sistemas</span><span class="sxs-lookup"><span data-stu-id="31407-125">System Pool Behavior</span></span>](system-pool-behavior.md)<br/> | <span data-ttu-id="31407-126">Debate sobre las acciones realizadas por el grupo del sistema cuando se envían avisos de eventos y cuando no hay ninguna operación biométrica pendiente.</span><span class="sxs-lookup"><span data-stu-id="31407-126">Discussion about the actions taken by the system pool when event notices are sent and when no biometric operations are pending.</span></span><br/>                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="31407-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="31407-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31407-128">Acerca de la API de Plataforma de biometría de Windows</span><span class="sxs-lookup"><span data-stu-id="31407-128">About the Windows Biometric Framework API</span></span>](./biometric-service-api-portal.md)
</dt> </dl>

 

