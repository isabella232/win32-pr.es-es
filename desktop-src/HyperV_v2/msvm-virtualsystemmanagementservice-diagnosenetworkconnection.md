---
description: Diagnostica la conectividad de red de una máquina virtual en un entorno de virtualización de red de Windows.
ms.assetid: c18f48bf-1f57-4a23-a495-462afad42750
title: Método DiagnoseNetworkConnection de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DiagnoseNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 70760f771e3908265a4ac70ebc1cbdf957d652c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686591"
---
# <a name="diagnosenetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="647fc-103">Método DiagnoseNetworkConnection de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="647fc-103">DiagnoseNetworkConnection method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="647fc-104">Diagnostica la conectividad de red de una máquina virtual en un entorno de virtualización de red de Windows.</span><span class="sxs-lookup"><span data-stu-id="647fc-104">Diagnoses the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="647fc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="647fc-105">Syntax</span></span>


```mof
uint32 DiagnoseNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  string                                     DiagnosticSettings,
  [out] string                                     DiagnosticInformation,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="647fc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="647fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="647fc-107">*TargetNetworkAdapter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="647fc-107">*TargetNetworkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="647fc-108">Referencia a un [**\_ EthernetPortAllocationSettingData de MSVM**](msvm-ethernetportallocationsettingdata.md) que describe el adaptador de red de destino.</span><span class="sxs-lookup"><span data-stu-id="647fc-108">Reference to an [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) that describes the target network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="647fc-109">*DiagnosticSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="647fc-109">*DiagnosticSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="647fc-110">Configuración de diagnóstico que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="647fc-110">The diagnostic settings to use.</span></span>

</dd> <dt>

<span data-ttu-id="647fc-111">*DiagnosticInformation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="647fc-111">*DiagnosticInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="647fc-112">Si se ejecuta correctamente, devuelve la información de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="647fc-112">On success, returns the diagnostic information.</span></span>

</dd> <dt>

<span data-ttu-id="647fc-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="647fc-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="647fc-114">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="647fc-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="647fc-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="647fc-115">Return value</span></span>

<span data-ttu-id="647fc-116">Devuelve 0 o 4096 en caso de éxito; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="647fc-116">Returns a 0 or 4096 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="647fc-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="647fc-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="647fc-118">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="647fc-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="647fc-119">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="647fc-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="647fc-120">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="647fc-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="647fc-121">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="647fc-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="647fc-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="647fc-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="647fc-123">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="647fc-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="647fc-124">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="647fc-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="647fc-125">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="647fc-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="647fc-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="647fc-126">Requirements</span></span>



| <span data-ttu-id="647fc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="647fc-127">Requirement</span></span> | <span data-ttu-id="647fc-128">Value</span><span class="sxs-lookup"><span data-stu-id="647fc-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="647fc-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="647fc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="647fc-130">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="647fc-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="647fc-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="647fc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="647fc-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="647fc-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="647fc-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="647fc-133">Namespace</span></span><br/>                | <span data-ttu-id="647fc-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="647fc-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="647fc-135">MOF</span><span class="sxs-lookup"><span data-stu-id="647fc-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="647fc-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="647fc-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="647fc-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="647fc-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="647fc-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="647fc-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="647fc-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="647fc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="647fc-140">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="647fc-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

