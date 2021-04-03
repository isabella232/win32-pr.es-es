---
description: Modifica la configuración del servicio réplica de Hyper-V.
ms.assetid: e203f9f5-da4b-4ba7-8637-add7169990d3
title: Método ModifyServiceSettings de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe20f8e6f113dce05961eb11fbafdc7841f39e38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810310"
---
# <a name="modifyservicesettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="32f17-103">Método ModifyServiceSettings de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="32f17-103">ModifyServiceSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="32f17-104">Modifica la configuración del servicio réplica de Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="32f17-104">Modifies the settings for the Hyper-V Replica service.</span></span>

## <a name="syntax"></a><span data-ttu-id="32f17-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32f17-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="32f17-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32f17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32f17-107">*SettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32f17-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32f17-108">Representación de cadena de la clase [**MSVM \_ ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md) que contiene los datos de configuración modificados para el servicio.</span><span class="sxs-lookup"><span data-stu-id="32f17-108">A string representation of the [**Msvm\_ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="32f17-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="32f17-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32f17-110">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="32f17-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32f17-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32f17-111">Return value</span></span>

<span data-ttu-id="32f17-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="32f17-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="32f17-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="32f17-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="32f17-114">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="32f17-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="32f17-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="32f17-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="32f17-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="32f17-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="32f17-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="32f17-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="32f17-118">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="32f17-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="32f17-119">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="32f17-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="32f17-120">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="32f17-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="32f17-121">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="32f17-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="32f17-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="32f17-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="32f17-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="32f17-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="32f17-124">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="32f17-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="32f17-125">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="32f17-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="32f17-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32f17-126">Requirements</span></span>



| <span data-ttu-id="32f17-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="32f17-127">Requirement</span></span> | <span data-ttu-id="32f17-128">Value</span><span class="sxs-lookup"><span data-stu-id="32f17-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32f17-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32f17-129">Minimum supported client</span></span><br/> | <span data-ttu-id="32f17-130">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="32f17-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="32f17-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32f17-131">Minimum supported server</span></span><br/> | <span data-ttu-id="32f17-132">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="32f17-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="32f17-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="32f17-133">Namespace</span></span><br/>                | <span data-ttu-id="32f17-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="32f17-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="32f17-135">MOF</span><span class="sxs-lookup"><span data-stu-id="32f17-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32f17-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32f17-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="32f17-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="32f17-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32f17-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="32f17-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="32f17-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="32f17-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32f17-140">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="32f17-140">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

