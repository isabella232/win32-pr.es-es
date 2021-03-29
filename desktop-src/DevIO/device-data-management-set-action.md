---
description: Defina el conjunto de acciones para el \_ código de \_ control administrar atributos del conjunto de datos de almacenamiento de ioctl \_ \_ \_ .
ms.assetid: ff688c9a-8669-4699-aab9-1e2e3a5c7fca
title: DEVICE_DATA_MANAGEMENT_SET_ACTION (WinIoCtl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524d1dbd2ecf09dbcfa66fa766089dde7cf04a0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907218"
---
# <a name="device_data_management_set_action"></a><span data-ttu-id="54d1c-103">\_acción de \_ conjunto de administración de datos de dispositivo \_ \_</span><span class="sxs-lookup"><span data-stu-id="54d1c-103">DEVICE\_DATA\_MANAGEMENT\_SET\_ACTION</span></span>

<span data-ttu-id="54d1c-104">Los siguientes valores constantes son el conjunto de valores posibles para el tipo de **\_ \_ \_ \_ acción set de administración de datos del dispositivo** , que se define como tipo **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="54d1c-104">The following constant values are the set of possible values for the **DEVICE\_DATA\_MANAGEMENT\_SET\_ACTION** type, which is defined as type **DWORD**.</span></span>

<dl> <dt>

<span data-ttu-id="54d1c-105"><span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="54d1c-105"><span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction\_None**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d1c-106">0</span><span class="sxs-lookup"><span data-stu-id="54d1c-106">0</span></span>
</dt> <dt>



<span data-ttu-id="54d1c-107">No se realiza ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="54d1c-107">No action is performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54d1c-108"><span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**DeviceDsmAction \_ Trim**</span><span class="sxs-lookup"><span data-stu-id="54d1c-108"><span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**DeviceDsmAction\_Trim**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d1c-109">1</span><span class="sxs-lookup"><span data-stu-id="54d1c-109">1</span></span>
</dt> <dt>



<span data-ttu-id="54d1c-110">Se realiza una acción de recorte.</span><span class="sxs-lookup"><span data-stu-id="54d1c-110">A trim action is performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54d1c-111"><span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**\_Notificación DeviceDsmAction**</span><span class="sxs-lookup"><span data-stu-id="54d1c-111"><span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**DeviceDsmAction\_Notification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d1c-112">2 \| **DeviceDsmActionFlag no \_ destructiva** (0x80000002)</span><span class="sxs-lookup"><span data-stu-id="54d1c-112">2 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000002)</span></span>
</dt> <dt>



<span data-ttu-id="54d1c-113">Se realiza una acción de notificación.</span><span class="sxs-lookup"><span data-stu-id="54d1c-113">A notification action is performed.</span></span> <span data-ttu-id="54d1c-114">Los parámetros se encuentran en una estructura de [**parámetros de notificación de DSM del dispositivo \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) .</span><span class="sxs-lookup"><span data-stu-id="54d1c-114">The parameters are in a [**DEVICE\_DSM\_NOTIFICATION\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) structure.</span></span> <span data-ttu-id="54d1c-115">La **DeviceDsmActionFlag \_ nondestructiva** (0x80000000) es un indicador de bits para indicar a la pila de controladores que esta operación no es destructiva.</span><span class="sxs-lookup"><span data-stu-id="54d1c-115">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54d1c-116"><span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**DeviceDsmAction \_ OffloadRead**</span><span class="sxs-lookup"><span data-stu-id="54d1c-116"><span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**DeviceDsmAction\_OffloadRead**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d1c-117">3 \| **DeviceDsmActionFlag no \_ destructivo** (0x80000003)</span><span class="sxs-lookup"><span data-stu-id="54d1c-117">3 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000003)</span></span>
</dt> <dt>



<span data-ttu-id="54d1c-118">Se realiza una acción de lectura de descarga.</span><span class="sxs-lookup"><span data-stu-id="54d1c-118">An offload read action is performed.</span></span> <span data-ttu-id="54d1c-119">Los parámetros se encuentran en una estructura [**DSM de dispositivo \_ \_ Descargar \_ \_ parámetros de lectura**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) .</span><span class="sxs-lookup"><span data-stu-id="54d1c-119">The parameters are in a [**DEVICE\_DSM\_OFFLOAD\_READ\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) structure.</span></span> <span data-ttu-id="54d1c-120">La salida está en una estructura de [**salida de lectura de descarga de almacenamiento \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) .</span><span class="sxs-lookup"><span data-stu-id="54d1c-120">The output is in a [**STORAGE\_OFFLOAD\_READ\_OUTPUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) structure.</span></span> <span data-ttu-id="54d1c-121">La **DeviceDsmActionFlag \_ nondestructiva** (0x80000000) es un indicador de bits para indicar a la pila de controladores que esta operación no es destructiva.</span><span class="sxs-lookup"><span data-stu-id="54d1c-121">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="54d1c-122">**Windows 7 y Windows Server 2008 R2:** Este valor no se admite antes de Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="54d1c-122">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54d1c-123"><span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**DeviceDsmAction \_ OffloadWrite**</span><span class="sxs-lookup"><span data-stu-id="54d1c-123"><span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**DeviceDsmAction\_OffloadWrite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d1c-124">4</span><span class="sxs-lookup"><span data-stu-id="54d1c-124">4</span></span>
</dt> <dt>



<span data-ttu-id="54d1c-125">Se realiza una acción de escritura de descarga.</span><span class="sxs-lookup"><span data-stu-id="54d1c-125">An offload write action is performed.</span></span> <span data-ttu-id="54d1c-126">Los parámetros se encuentran en una estructura de [**\_ \_ \_ \_ parámetros de escritura del DSM de dispositivo**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) .</span><span class="sxs-lookup"><span data-stu-id="54d1c-126">The parameters are in a [**DEVICE\_DSM\_OFFLOAD\_WRITE\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) structure.</span></span> <span data-ttu-id="54d1c-127">La salida está en una estructura de [**salida de escritura de descarga de almacenamiento \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) .</span><span class="sxs-lookup"><span data-stu-id="54d1c-127">The output is in a [**STORAGE\_OFFLOAD\_WRITE\_OUTPUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) structure.</span></span>

<span data-ttu-id="54d1c-128">**Windows 7 y Windows Server 2008 R2:** Este valor no se admite antes de Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="54d1c-128">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54d1c-129"><span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**Asignación de DeviceDsmAction \_**</span><span class="sxs-lookup"><span data-stu-id="54d1c-129"><span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**DeviceDsmAction\_Allocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d1c-130">5 \| **DeviceDsmActionFlag no \_ destructiva** (0x80000005)</span><span class="sxs-lookup"><span data-stu-id="54d1c-130">5 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000005)</span></span>
</dt> <dt>



<span data-ttu-id="54d1c-131">Se devuelve un mapa de bits de asignación para el primer intervalo de conjunto de datos pasado.</span><span class="sxs-lookup"><span data-stu-id="54d1c-131">An allocation bitmap is returned for the first data set range passed in.</span></span> <span data-ttu-id="54d1c-132">La salida se encuentra en un conjunto de datos de dispositivo estructura de [**\_ \_ \_ \_ \_ Estado de aprovisionamiento lb**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) .</span><span class="sxs-lookup"><span data-stu-id="54d1c-132">The output is in a [**DEVICE\_DATA\_SET\_LB\_PROVISIONING\_STATE**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) structure.</span></span> <span data-ttu-id="54d1c-133">La **DeviceDsmActionFlag \_ nondestructiva** (0x80000000) es un indicador de bits para indicar a la pila de controladores que esta operación no es destructiva.</span><span class="sxs-lookup"><span data-stu-id="54d1c-133">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="54d1c-134">**Windows 7 y Windows Server 2008 R2:** Este valor no se admite antes de Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="54d1c-134">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54d1c-135"><span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**Reparación de DeviceDsmAction \_**</span><span class="sxs-lookup"><span data-stu-id="54d1c-135"><span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**DeviceDsmAction\_Repair**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d1c-136">6 \| **DeviceDsmActionFlag no \_ destructiva** (0x80000006)</span><span class="sxs-lookup"><span data-stu-id="54d1c-136">6 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000006)</span></span>
</dt> <dt>



<span data-ttu-id="54d1c-137">Se realiza una acción de reparación.</span><span class="sxs-lookup"><span data-stu-id="54d1c-137">A repair action is performed.</span></span> <span data-ttu-id="54d1c-138">La **DeviceDsmActionFlag \_ nondestructiva** (0x80000000) es un indicador de bits para indicar a la pila de controladores que esta operación no es destructiva.</span><span class="sxs-lookup"><span data-stu-id="54d1c-138">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="54d1c-139">**Windows 7 y Windows Server 2008 R2:** Este valor no se admite antes de Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="54d1c-139">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54d1c-140"><span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**\_Limpieza DeviceDsmAction**</span><span class="sxs-lookup"><span data-stu-id="54d1c-140"><span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**DeviceDsmAction\_Scrub**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d1c-141">7 \| **DeviceDsmActionFlag no \_ destructiva** (0x80000007)</span><span class="sxs-lookup"><span data-stu-id="54d1c-141">7 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000007)</span></span>
</dt> <dt>



<span data-ttu-id="54d1c-142">Se realiza una acción de limpieza.</span><span class="sxs-lookup"><span data-stu-id="54d1c-142">A scrub action is performed.</span></span> <span data-ttu-id="54d1c-143">La **DeviceDsmActionFlag \_ nondestructiva** (0x80000000) es un indicador de bits para indicar a la pila de controladores que esta operación no es destructiva.</span><span class="sxs-lookup"><span data-stu-id="54d1c-143">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="54d1c-144">**Windows 7 y Windows Server 2008 R2:** Este valor no se admite antes de Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="54d1c-144">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54d1c-145"><span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**Resistencia de DeviceDsmAction \_**</span><span class="sxs-lookup"><span data-stu-id="54d1c-145"><span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**DeviceDsmAction\_Resiliency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d1c-146">8 \| **DeviceDsmActionFlag no \_ destructiva** (0x80000008)</span><span class="sxs-lookup"><span data-stu-id="54d1c-146">8 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000008)</span></span>
</dt> <dt>



<span data-ttu-id="54d1c-147">Se realiza una acción de resistencia.</span><span class="sxs-lookup"><span data-stu-id="54d1c-147">A resiliency action is performed.</span></span> <span data-ttu-id="54d1c-148">La **DeviceDsmActionFlag \_ nondestructiva** (0x80000000) es un indicador de bits para indicar a la pila de controladores que esta operación no es destructiva.</span><span class="sxs-lookup"><span data-stu-id="54d1c-148">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="54d1c-149">**Windows 7 y Windows Server 2008 R2:** Este valor no se admite antes de Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="54d1c-149">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54d1c-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54d1c-150">Requirements</span></span>



| <span data-ttu-id="54d1c-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="54d1c-151">Requirement</span></span> | <span data-ttu-id="54d1c-152">Value</span><span class="sxs-lookup"><span data-stu-id="54d1c-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54d1c-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54d1c-153">Minimum supported client</span></span><br/> | <span data-ttu-id="54d1c-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="54d1c-154">Windows 7</span></span><br/>                                                                                      |
| <span data-ttu-id="54d1c-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54d1c-155">Minimum supported server</span></span><br/> | <span data-ttu-id="54d1c-156">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="54d1c-156">Windows Server 2008 R2</span></span><br/>                                                                         |
| <span data-ttu-id="54d1c-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54d1c-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="54d1c-158"><dt>WinIoCtl. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54d1c-158"><dt>WinIoCtl.h (include Windows.h)</dt></span></span> </dl> |



 

 




