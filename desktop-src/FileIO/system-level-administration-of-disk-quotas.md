---
description: El administrador del sistema puede establecer cuotas para usuarios específicos en un volumen. Además, el administrador puede establecer cuotas predeterminadas para el volumen.
ms.assetid: e8fa6a7b-f4b9-48af-9538-d41c12b7c3b6
title: Administración de las cuotas de disco en el nivel de sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4987becce54b75f2bc06710dce85500813520f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275572"
---
# <a name="system-level-administration-of-disk-quotas"></a><span data-ttu-id="c3f10-104">Administración de las cuotas de disco en el nivel de sistema</span><span class="sxs-lookup"><span data-stu-id="c3f10-104">System-level Administration of Disk Quotas</span></span>

<span data-ttu-id="c3f10-105">El administrador del sistema puede establecer cuotas para usuarios específicos en un volumen.</span><span class="sxs-lookup"><span data-stu-id="c3f10-105">The system administrator can set quotas for specific users on a volume.</span></span> <span data-ttu-id="c3f10-106">Además, el administrador puede establecer cuotas predeterminadas para el volumen.</span><span class="sxs-lookup"><span data-stu-id="c3f10-106">The administrator can also set default quotas for the volume.</span></span> <span data-ttu-id="c3f10-107">Un nuevo usuario del volumen recibe la cuota predeterminada a menos que el administrador haya establecido una cuota específicamente para ese usuario.</span><span class="sxs-lookup"><span data-stu-id="c3f10-107">A new user on the volume receives the default quota unless the administrator established a quota specifically for that user.</span></span>

<span data-ttu-id="c3f10-108">El administrador puede consultar el nivel de seguimiento y cumplimiento de la cuota (o Estados de cuota), los límites de cuota predeterminados y la información de cuota por usuario.</span><span class="sxs-lookup"><span data-stu-id="c3f10-108">The administrator can query the level of quota tracking and enforcement (or quota states), the default quota limits, and the per-user quota information.</span></span> <span data-ttu-id="c3f10-109">La información de cuota por usuario contiene el límite de cuota máxima del usuario, el umbral de advertencia y el uso de la cuota.</span><span class="sxs-lookup"><span data-stu-id="c3f10-109">The per-user quota information contains the user's hard quota limit, warning threshold, and the quota usage.</span></span> <span data-ttu-id="c3f10-110">El administrador también puede habilitar o deshabilitar la aplicación de cuotas.</span><span class="sxs-lookup"><span data-stu-id="c3f10-110">The administrator can also enable or disable quota enforcement.</span></span>

<span data-ttu-id="c3f10-111">Hay tres Estados de cuota, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c3f10-111">There are three quota states, as shown in the following table.</span></span>



| <span data-ttu-id="c3f10-112">Estado</span><span class="sxs-lookup"><span data-stu-id="c3f10-112">State</span></span>          | <span data-ttu-id="c3f10-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3f10-113">Description</span></span>                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f10-114">Cuota deshabilitada</span><span class="sxs-lookup"><span data-stu-id="c3f10-114">Quota disabled</span></span> | <span data-ttu-id="c3f10-115">No se realiza el seguimiento de los cambios de uso de cuota, pero los límites de cuota no se quitan.</span><span class="sxs-lookup"><span data-stu-id="c3f10-115">Quota usage changes are not tracked, but the quota limits are not removed.</span></span> <span data-ttu-id="c3f10-116">En este estado, el rendimiento no se ve afectado por las cuotas de disco.</span><span class="sxs-lookup"><span data-stu-id="c3f10-116">In this state, performance is not affected by disk quotas.</span></span> <span data-ttu-id="c3f10-117">Este es el estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c3f10-117">This is the default state.</span></span>                         |
| <span data-ttu-id="c3f10-118">Cuota de seguimiento</span><span class="sxs-lookup"><span data-stu-id="c3f10-118">Quota tracked</span></span>  | <span data-ttu-id="c3f10-119">Se realiza un seguimiento de los cambios de uso de cuota, pero no se aplican los límites de cuota.</span><span class="sxs-lookup"><span data-stu-id="c3f10-119">Quota usage changes are tracked, but quota limits are not enforced.</span></span> <span data-ttu-id="c3f10-120">En este estado, no se genera ningún evento de infracción de cuota y no se produce un error en las operaciones de archivo debido a infracciones de cuota de disco.</span><span class="sxs-lookup"><span data-stu-id="c3f10-120">In this state, no quota violation events are generated and no file operations fail because of disk quota violations.</span></span> |
| <span data-ttu-id="c3f10-121">Cuota aplicada</span><span class="sxs-lookup"><span data-stu-id="c3f10-121">Quota enforced</span></span> | <span data-ttu-id="c3f10-122">Se realiza un seguimiento de los cambios de uso de cuota y se aplican los límites de cuota.</span><span class="sxs-lookup"><span data-stu-id="c3f10-122">Quota usage changes are tracked and quota limits are enforced.</span></span>                                                                                                                           |



 

 

 



