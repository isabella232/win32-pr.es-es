---
description: Configura los adaptadores de red en el sistema operativo invitado.
ms.assetid: 698e0c17-f8bd-433f-b982-5481f9701ba6
title: Método SetGuestNetworkAdapterConfiguration de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetGuestNetworkAdapterConfiguration
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 02c79df7aa08faa842e2b702b4cf18944e96bdfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545414"
---
# <a name="setguestnetworkadapterconfiguration-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="75dc0-103">Método SetGuestNetworkAdapterConfiguration de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="75dc0-103">SetGuestNetworkAdapterConfiguration method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="75dc0-104">Configura los adaptadores de red en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="75dc0-104">Configures the network adapters within the guest operating system.</span></span> <span data-ttu-id="75dc0-105">Estos parámetros de configuración se aplican de forma inmediata al establecer la comunicación con el componente de integración de Exchange KVP que se ejecuta en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="75dc0-105">These configuration parameters are applied immediately upon establishing communication with the KVP Exchange integration component running within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="75dc0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75dc0-106">Syntax</span></span>


```mof
uint32 SetGuestNetworkAdapterConfiguration(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkConfiguration[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="75dc0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75dc0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75dc0-108">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="75dc0-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75dc0-109">Referencia a la instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) cuyos adaptadores de red se van a configurar.</span><span class="sxs-lookup"><span data-stu-id="75dc0-109">A reference to the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance whose network adapters are to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="75dc0-110">*NetworkConfiguration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="75dc0-110">*NetworkConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75dc0-111">Una matriz de instancias incrustadas de la clase [**MSVM \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="75dc0-111">An array of embedded instances of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class.</span></span> <span data-ttu-id="75dc0-112">Cada instancia de describe los parámetros de configuración de uno de los adaptadores de red de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="75dc0-112">Each instance describes the configuration parameters for one of the network adapters within the virtual machine.</span></span> <span data-ttu-id="75dc0-113">Se debe especificar la propiedad **DHCPEnabled** para cada instancia.</span><span class="sxs-lookup"><span data-stu-id="75dc0-113">The **DHCPEnabled** property must be specified for each instance.</span></span>

</dd> <dt>

<span data-ttu-id="75dc0-114">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="75dc0-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75dc0-115">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="75dc0-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75dc0-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75dc0-116">Return value</span></span>

<span data-ttu-id="75dc0-117">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="75dc0-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="75dc0-118">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="75dc0-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="75dc0-119">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="75dc0-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="75dc0-120">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="75dc0-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="75dc0-121">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="75dc0-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="75dc0-122">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="75dc0-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="75dc0-123">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="75dc0-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="75dc0-124">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="75dc0-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="75dc0-125">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="75dc0-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="75dc0-126">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="75dc0-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="75dc0-127">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="75dc0-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="75dc0-128">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="75dc0-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="75dc0-129">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="75dc0-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="75dc0-130">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="75dc0-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="75dc0-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75dc0-131">Requirements</span></span>



| <span data-ttu-id="75dc0-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="75dc0-132">Requirement</span></span> | <span data-ttu-id="75dc0-133">Value</span><span class="sxs-lookup"><span data-stu-id="75dc0-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75dc0-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75dc0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="75dc0-135">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="75dc0-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="75dc0-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75dc0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="75dc0-137">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="75dc0-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="75dc0-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="75dc0-138">Namespace</span></span><br/>                | <span data-ttu-id="75dc0-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="75dc0-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="75dc0-140">MOF</span><span class="sxs-lookup"><span data-stu-id="75dc0-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75dc0-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75dc0-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="75dc0-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75dc0-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75dc0-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="75dc0-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="75dc0-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="75dc0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75dc0-145">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="75dc0-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

