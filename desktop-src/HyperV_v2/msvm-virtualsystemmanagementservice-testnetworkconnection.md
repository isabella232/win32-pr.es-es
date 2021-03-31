---
description: Prueba la conectividad de red de una máquina virtual en un entorno de virtualización de red de Windows.
ms.assetid: 37d4c34d-406e-4c52-afce-b0eef754eeb3
title: Método TestNetworkConnection de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.TestNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e8f15faacb1b8ad683b1ea9abfa9b91f5c376dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153887"
---
# <a name="testnetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="ab08a-103">Método TestNetworkConnection de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="ab08a-103">TestNetworkConnection method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="ab08a-104">Prueba la conectividad de red de una máquina virtual en un entorno de virtualización de red de Windows.</span><span class="sxs-lookup"><span data-stu-id="ab08a-104">Tests the network connectivity of a VM in a Windows network virtualization environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab08a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab08a-105">Syntax</span></span>


```mof
uint32 TestNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  boolean                                    IsSender,
  [in]  string                                     SenderIP,
  [in]  string                                     ReceiverIP,
  [in]  string                                     ReceiverMac,
  [in]  uint32                                     IsolationId,
  [in]  uint32                                     SequenceNumber,
  [out] uint32                                     RoundTripTime,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ab08a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab08a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab08a-107">*TargetNetworkAdapter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab08a-107">*TargetNetworkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab08a-108">Referencia a un [**\_ EthernetPortAllocationSettingData de MSVM**](msvm-ethernetportallocationsettingdata.md) que describe el adaptador de red de destino.</span><span class="sxs-lookup"><span data-stu-id="ab08a-108">Reference to a [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) describing the target network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ab08a-109">*IsSender* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab08a-109">*IsSender* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab08a-110">Indica si este método se invoca en el remitente o en el receptor.</span><span class="sxs-lookup"><span data-stu-id="ab08a-110">Indicates whether this method is being invoked at the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="ab08a-111">*SenderIP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab08a-111">*SenderIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab08a-112">Dirección IP del remitente.</span><span class="sxs-lookup"><span data-stu-id="ab08a-112">The sender IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ab08a-113">*ReceiverIP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab08a-113">*ReceiverIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab08a-114">Dirección Mac del remitente.</span><span class="sxs-lookup"><span data-stu-id="ab08a-114">The sender Mac address.</span></span>

</dd> <dt>

<span data-ttu-id="ab08a-115">*ReceiverMac* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab08a-115">*ReceiverMac* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab08a-116">Dirección Mac del remitente.</span><span class="sxs-lookup"><span data-stu-id="ab08a-116">The sender Mac address.</span></span>

</dd> <dt>

<span data-ttu-id="ab08a-117">*IsolationId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab08a-117">*IsolationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab08a-118">IDENTIFICADOR de aislamiento.</span><span class="sxs-lookup"><span data-stu-id="ab08a-118">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="ab08a-119">*SequenceNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab08a-119">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab08a-120">IDENTIFICADOR de aislamiento.</span><span class="sxs-lookup"><span data-stu-id="ab08a-120">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="ab08a-121">*RoundTripTime* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab08a-121">*RoundTripTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab08a-122">Tiempo de ida y vuelta.</span><span class="sxs-lookup"><span data-stu-id="ab08a-122">The round trip time.</span></span>

</dd> <dt>

<span data-ttu-id="ab08a-123">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab08a-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab08a-124">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ab08a-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab08a-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab08a-125">Return value</span></span>

<span data-ttu-id="ab08a-126">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ab08a-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ab08a-127">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="ab08a-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ab08a-128">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="ab08a-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ab08a-129">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="ab08a-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ab08a-130">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="ab08a-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ab08a-131">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="ab08a-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ab08a-132">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ab08a-132">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ab08a-133">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="ab08a-133">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ab08a-134">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="ab08a-134">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="ab08a-135">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="ab08a-135">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ab08a-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab08a-136">Requirements</span></span>



| <span data-ttu-id="ab08a-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab08a-137">Requirement</span></span> | <span data-ttu-id="ab08a-138">Value</span><span class="sxs-lookup"><span data-stu-id="ab08a-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab08a-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab08a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ab08a-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ab08a-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ab08a-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab08a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ab08a-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ab08a-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ab08a-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ab08a-143">Namespace</span></span><br/>                | <span data-ttu-id="ab08a-144">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ab08a-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ab08a-145">MOF</span><span class="sxs-lookup"><span data-stu-id="ab08a-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab08a-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab08a-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab08a-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ab08a-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab08a-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ab08a-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ab08a-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab08a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab08a-150">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="ab08a-150">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

