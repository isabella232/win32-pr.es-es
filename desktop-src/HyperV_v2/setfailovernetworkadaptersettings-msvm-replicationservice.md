---
description: Configura los valores de IP de los adaptadores de red que se van a aplicar a una máquina virtual después de una conmutación por error.
ms.assetid: a49d089e-f5dc-4bfb-9f66-2593304b9795
title: Método SetFailoverNetworkAdapterSettings de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetFailoverNetworkAdapterSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: da5bb8c820e1dbca5103c430a7b2ce2a525a8fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687464"
---
# <a name="setfailovernetworkadaptersettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="032df-103">Método SetFailoverNetworkAdapterSettings de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="032df-103">SetFailoverNetworkAdapterSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="032df-104">Configura las opciones de IP del adaptador de red que se van a aplicar a una máquina virtual después de una conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="032df-104">Configures the network adapter's IP settings to be applied to a virtual machine after a failover.</span></span> <span data-ttu-id="032df-105">Estos parámetros de configuración se aplican después de una operación de conmutación por error, inmediatamente después de establecer la comunicación con el componente de integración de Exchange KVP que se ejecuta en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="032df-105">These configuration parameters are applied after a failover operation, immediately upon establishing communication with the KVP Exchange integration component running within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="032df-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="032df-106">Syntax</span></span>


```mof
uint32 SetFailoverNetworkAdapterSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkSettings[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="032df-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="032df-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="032df-108">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="032df-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="032df-109">Una referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual cuyos adaptadores de red se van a configurar.</span><span class="sxs-lookup"><span data-stu-id="032df-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine whose network adapters are to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="032df-110">*NetworkSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="032df-110">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="032df-111">Una matriz de instancias incrustadas de objetos [**\_ FailoverNetworkAdapterSettingData de MSVM**](msvm-failovernetworkadaptersettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="032df-111">An array of embedded instances of [**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) objects.</span></span> <span data-ttu-id="032df-112">Cada instancia de describe los parámetros de configuración de uno de los adaptadores de red de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="032df-112">Each instance describes the configuration parameters for one of the network adapters within the virtual machine.</span></span> <span data-ttu-id="032df-113">Las propiedades **IPAddresses** y **DHCPEnabled** deben especificarse en cada instancia.</span><span class="sxs-lookup"><span data-stu-id="032df-113">The **IPAddresses** and **DHCPEnabled** properties must be specified on each instance.</span></span>

</dd> <dt>

<span data-ttu-id="032df-114">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="032df-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="032df-115">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="032df-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="032df-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="032df-116">Return value</span></span>

<span data-ttu-id="032df-117">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="032df-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="032df-118">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="032df-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="032df-119">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="032df-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="032df-120">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="032df-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="032df-121">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="032df-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="032df-122">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="032df-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="032df-123">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="032df-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="032df-124">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="032df-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="032df-125">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="032df-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="032df-126">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="032df-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="032df-127">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="032df-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="032df-128">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="032df-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="032df-129">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="032df-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="032df-130">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="032df-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="032df-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="032df-131">Requirements</span></span>



| <span data-ttu-id="032df-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="032df-132">Requirement</span></span> | <span data-ttu-id="032df-133">Value</span><span class="sxs-lookup"><span data-stu-id="032df-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="032df-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="032df-134">Minimum supported client</span></span><br/> | <span data-ttu-id="032df-135">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="032df-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="032df-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="032df-136">Minimum supported server</span></span><br/> | <span data-ttu-id="032df-137">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="032df-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="032df-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="032df-138">Namespace</span></span><br/>                | <span data-ttu-id="032df-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="032df-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="032df-140">MOF</span><span class="sxs-lookup"><span data-stu-id="032df-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="032df-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="032df-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="032df-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="032df-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="032df-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="032df-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="032df-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="032df-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="032df-145">**InitiateFailover**</span><span class="sxs-lookup"><span data-stu-id="032df-145">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="032df-146">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="032df-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="032df-147">**RevertFailover**</span><span class="sxs-lookup"><span data-stu-id="032df-147">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)
</dt> </dl>

 

