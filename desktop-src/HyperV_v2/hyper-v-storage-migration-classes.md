---
description: La API de migración de Hyper-V define los siguientes elementos de programación.
ms.assetid: E1FE7351-2F14-4C8F-AF5C-9009CC61CE22
title: Referencia de la API de migración de Hyper-V
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e40a05bc976cf1722aba558eeca9c7b04cdf7287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687203"
---
# <a name="hyper-v-migration-api-reference"></a><span data-ttu-id="5d427-103">Referencia de la API de migración de Hyper-V</span><span class="sxs-lookup"><span data-stu-id="5d427-103">Hyper-V migration API reference</span></span>

<span data-ttu-id="5d427-104">La API de migración de Hyper-V define los siguientes elementos de programación.</span><span class="sxs-lookup"><span data-stu-id="5d427-104">The Hyper-V migration API defines the following programming elements.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5d427-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5d427-105">In this section</span></span>



| <span data-ttu-id="5d427-106">Tema</span><span class="sxs-lookup"><span data-stu-id="5d427-106">Topic</span></span>                                                                                                                                | <span data-ttu-id="5d427-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d427-107">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d427-108">**MSVM \_ MigrationJob**</span><span class="sxs-lookup"><span data-stu-id="5d427-108">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)<br/>                                                                           | <span data-ttu-id="5d427-109">Esta clase representa un trabajo de operación de migración creado para el almacenamiento o la migración del sistema virtual por el servicio de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5d427-109">This class represents a migration operation job created for storage or virtual system migration by the virtual system migration service.</span></span><br/>                                                 |
| [<span data-ttu-id="5d427-110">**MSVM \_ VirtualSystemMigrationCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5d427-110">**Msvm\_VirtualSystemMigrationCapabilities**</span></span>](msvm-virtualsystemmigrationcapabilities.md)<br/>                               | <span data-ttu-id="5d427-111">Define los medios por los que un cliente puede detectar los métodos proporcionados por el servicio de migración y el intervalo válido de datos de configuración de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5d427-111">Defines the means by which a client can discover the methods provided by the migration service, and valid range of virtual system migration setting data.</span></span><br/>                                |
| [<span data-ttu-id="5d427-112">**MSVM \_ VirtualSystemMigrationNetworkSettingData**</span><span class="sxs-lookup"><span data-stu-id="5d427-112">**Msvm\_VirtualSystemMigrationNetworkSettingData**</span></span>](msvm-virtualsystemmigrationnetworksettingdata.md)<br/>                   | <span data-ttu-id="5d427-113">Representa la red en la que el servicio de migración del sistema virtual está escuchando la migración de sistema virtual entrante.</span><span class="sxs-lookup"><span data-stu-id="5d427-113">Represents the network on which the virtual system migration service is listening for incoming virtual system migration.</span></span><br/>                                                                 |
| [<span data-ttu-id="5d427-114">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="5d427-114">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)<br/>                                         | <span data-ttu-id="5d427-115">Representa el servicio de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5d427-115">Represents the virtual system migration service.</span></span> <span data-ttu-id="5d427-116">Se usa para migrar un sistema virtual o para migrar el almacenamiento de un sistema virtual de una plataforma de virtualización a otra.</span><span class="sxs-lookup"><span data-stu-id="5d427-116">It is used for migrating a virtual system or for migrating the storage of a virtual system from one virtualization platform to another.</span></span><br/> |
| [<span data-ttu-id="5d427-117">**MSVM \_ VirtualSystemMigrationServiceSettingData**</span><span class="sxs-lookup"><span data-stu-id="5d427-117">**Msvm\_VirtualSystemMigrationServiceSettingData**</span></span>](msvm-virtualsystemmigrationservicesettingdata.md)<br/>                   | <span data-ttu-id="5d427-118">Representa la configuración para el servicio de migración del sistema virtual en un host.</span><span class="sxs-lookup"><span data-stu-id="5d427-118">Represents the settings for the virtual system migration service on a host.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="5d427-119">**MSVM \_ VirtualSystemMigrationServiceSettingDataComponent**</span><span class="sxs-lookup"><span data-stu-id="5d427-119">**Msvm\_VirtualSystemMigrationServiceSettingDataComponent**</span></span>](msvm-virtualsystemmigrationservicesettingdatacomponent.md)<br/> | <span data-ttu-id="5d427-120">Asociación que se usa para representar la configuración de red de la migración del sistema virtual del servicio de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5d427-120">An association used to represent virtual system migration network settings of the virtual system migration service.</span></span><br/>                                                                      |
| [<span data-ttu-id="5d427-121">**MSVM \_ VirtualSystemMigrationSettingData**</span><span class="sxs-lookup"><span data-stu-id="5d427-121">**Msvm\_VirtualSystemMigrationSettingData**</span></span>](msvm-virtualsystemmigrationsettingdata.md)<br/>                                 | <span data-ttu-id="5d427-122">Representa la configuración de migración para migrar un sistema virtual y el almacenamiento conectado a un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5d427-122">Represents the migration settings for migrating a virtual system and the storage attached to a virtual system.</span></span><br/>                                                                           |



 

 

 




