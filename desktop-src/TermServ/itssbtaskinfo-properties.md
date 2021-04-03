---
title: Propiedades de ITsSbTaskInfo
description: La interfaz ITsSbTaskInfo expone las siguientes propiedades.
ms.assetid: 402B8502-DE17-440B-867D-45922582C30E
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c0e4c8fefc2e443778b2ce177e61a314a3e0ef9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783820"
---
# <a name="itssbtaskinfo-properties"></a><span data-ttu-id="a7525-103">Propiedades de ITsSbTaskInfo</span><span class="sxs-lookup"><span data-stu-id="a7525-103">ITsSbTaskInfo Properties</span></span>

<span data-ttu-id="a7525-104">La interfaz [**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) expone las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="a7525-104">The [**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a7525-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a7525-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="a7525-106">**Propiedad de contexto**</span><span class="sxs-lookup"><span data-stu-id="a7525-106">**Context property**</span></span>](itssbtaskinfo-context.md)
</dt> <dd>

<span data-ttu-id="a7525-107">Recupera los bytes de contexto asociados a la tarea.</span><span class="sxs-lookup"><span data-stu-id="a7525-107">Retrieves the context bytes associated with the task.</span></span>

</dd> <dt>

[<span data-ttu-id="a7525-108">**Propiedad fecha límite**</span><span class="sxs-lookup"><span data-stu-id="a7525-108">**Deadline property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_deadline)
</dt> <dd>

<span data-ttu-id="a7525-109">Recupera la hora en la que se debe iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="a7525-109">Retrieves the time by which the task must be initiated.</span></span> <span data-ttu-id="a7525-110">Se usa para priorizar las revisiones.</span><span class="sxs-lookup"><span data-stu-id="a7525-110">This is used to prioritize patches.</span></span> <span data-ttu-id="a7525-111">En primer lugar, se iniciará la revisión con la fecha límite más temprana.</span><span class="sxs-lookup"><span data-stu-id="a7525-111">The patch with the earliest deadline will get initiated first.</span></span>

</dd> <dt>

[<span data-ttu-id="a7525-112">**EndTime (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="a7525-112">**EndTime property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_endtime)
</dt> <dd>

<span data-ttu-id="a7525-113">Recupera la hora más reciente en la que el agente de tareas puede iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="a7525-113">Retrieves the latest time the task agent can start the task.</span></span>

</dd> <dt>

[<span data-ttu-id="a7525-114">**Propiedad Identificador**</span><span class="sxs-lookup"><span data-stu-id="a7525-114">**Identifier property**</span></span>](itssbtaskinfo-identifier.md)
</dt> <dd>

<span data-ttu-id="a7525-115">Recupera un GUID que el agente de tareas usa como identificador único.</span><span class="sxs-lookup"><span data-stu-id="a7525-115">Retrieves a GUID that is used as a unique identifier by the task agent.</span></span>

</dd> <dt>

[<span data-ttu-id="a7525-116">**propiedad Etiqueta**</span><span class="sxs-lookup"><span data-stu-id="a7525-116">**Label property**</span></span>](itssbtaskinfo-label.md)
</dt> <dd>

<span data-ttu-id="a7525-117">Recupera la etiqueta que describe el propósito de la tarea.</span><span class="sxs-lookup"><span data-stu-id="a7525-117">Retrieves the label that describes the purpose of the task.</span></span>

</dd> <dt>

[<span data-ttu-id="a7525-118">**Propiedad de complemento**</span><span class="sxs-lookup"><span data-stu-id="a7525-118">**Plugin property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_plugin)
</dt> <dd>

<span data-ttu-id="a7525-119">Recupera el nombre para mostrar del agente de tareas.</span><span class="sxs-lookup"><span data-stu-id="a7525-119">Retrieves the display name of the task agent.</span></span>

</dd> <dt>

[<span data-ttu-id="a7525-120">**StartTime (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="a7525-120">**StartTime property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_starttime)
</dt> <dd>

<span data-ttu-id="a7525-121">Recupera la hora más temprana en la que el agente de tareas puede iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="a7525-121">Retrieves the earliest time the task agent can start the task.</span></span>

</dd> <dt>

[<span data-ttu-id="a7525-122">**Propiedad Status**</span><span class="sxs-lookup"><span data-stu-id="a7525-122">**Status property**</span></span>](itssbtaskinfo-status.md)
</dt> <dd>

<span data-ttu-id="a7525-123">Recupera un valor de enumeración de [**\_ \_ Estado de la tarea RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) que representa el estado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="a7525-123">Retrieves an [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

</dd> <dt>

[<span data-ttu-id="a7525-124">**Propiedad TargetId**</span><span class="sxs-lookup"><span data-stu-id="a7525-124">**TargetId property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_targetid)
</dt> <dd>

<span data-ttu-id="a7525-125">Recupera el identificador de destino.</span><span class="sxs-lookup"><span data-stu-id="a7525-125">Retrieves the target identifier.</span></span>

</dd> </dl>

 

 




