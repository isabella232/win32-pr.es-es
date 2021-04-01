---
description: Establece el estado de energía del equipo. El uso de este método está en desuso. En su lugar, use el método SetPowerState en la clase PowerManagementService asociada.
ms.assetid: c2196f35-f687-4d82-a068-f8499f77473a
title: Método SetPowerState de la clase CIM_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem.SetPowerState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9c9e264e8ec62c1e49e92226d1abc8ac902c0b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082796"
---
# <a name="setpowerstate-method-of-the-cim_computersystem-class"></a><span data-ttu-id="dc820-105">Método SetPowerState de la clase de ComputerSystem de CIM \_</span><span class="sxs-lookup"><span data-stu-id="dc820-105">SetPowerState method of the CIM\_ComputerSystem class</span></span>

<span data-ttu-id="dc820-106">Establece el estado de energía del equipo.</span><span class="sxs-lookup"><span data-stu-id="dc820-106">Sets the power state of the computer.</span></span> <span data-ttu-id="dc820-107">El uso de este método está en desuso.</span><span class="sxs-lookup"><span data-stu-id="dc820-107">The use of this method has been deprecated.</span></span> <span data-ttu-id="dc820-108">En su lugar, use el método **SetPowerState** en la clase **PowerManagementService** asociada.</span><span class="sxs-lookup"><span data-stu-id="dc820-108">Instead, use the **SetPowerState** method in the associated **PowerManagementService** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc820-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc820-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint32   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="dc820-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc820-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc820-111">*PowerState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dc820-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc820-112">Estado deseado del equipo.</span><span class="sxs-lookup"><span data-stu-id="dc820-112">The desired state for the computer system.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="dc820-113">**Potencia completa** (1)</span><span class="sxs-lookup"><span data-stu-id="dc820-113">**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="dc820-114">Ahorro **de energía: modo de baja energía** (2)</span><span class="sxs-lookup"><span data-stu-id="dc820-114">**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="dc820-115">Ahorro **de energía: en espera** (3)</span><span class="sxs-lookup"><span data-stu-id="dc820-115">**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="dc820-116">Ahorro **de energía: otros** (4)</span><span class="sxs-lookup"><span data-stu-id="dc820-116">**Power Save - Other** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="dc820-117">**Ciclo de energía** (5)</span><span class="sxs-lookup"><span data-stu-id="dc820-117">**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="dc820-118">**Desconectar (6** )</span><span class="sxs-lookup"><span data-stu-id="dc820-118">**Power Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>

<span data-ttu-id="dc820-119">**Hibernación** (7)</span><span class="sxs-lookup"><span data-stu-id="dc820-119">**Hibernate** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>

<span data-ttu-id="dc820-120">**Soft off** (8)</span><span class="sxs-lookup"><span data-stu-id="dc820-120">**Soft Off** (8)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="dc820-121">*Hora* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="dc820-121">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc820-122">Time indica cuándo debe establecerse el estado de energía, ya sea como un valor de fecha y hora normal o como un valor de intervalo (donde el intervalo comienza cuando se recibe la invocación del método).</span><span class="sxs-lookup"><span data-stu-id="dc820-122">Time indicates when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc820-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc820-123">Requirements</span></span>



| <span data-ttu-id="dc820-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc820-124">Requirement</span></span> | <span data-ttu-id="dc820-125">Value</span><span class="sxs-lookup"><span data-stu-id="dc820-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc820-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc820-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dc820-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dc820-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="dc820-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc820-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dc820-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dc820-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="dc820-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dc820-130">Namespace</span></span><br/>                | <span data-ttu-id="dc820-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="dc820-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dc820-132">MOF</span><span class="sxs-lookup"><span data-stu-id="dc820-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc820-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc820-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc820-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc820-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc820-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dc820-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dc820-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc820-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc820-137">**ComputerSystem de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="dc820-137">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

 




