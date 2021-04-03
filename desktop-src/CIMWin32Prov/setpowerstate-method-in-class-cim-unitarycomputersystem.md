---
description: El método SetPowerState de la \_ clase CIM UnitaryComputerSystem establece el estado de energía deseado para un dispositivo lógico y el momento en que se debe colocar un dispositivo en ese estado.
ms.assetid: a02991d5-3c93-4579-b1f5-f70ad7c7052b
ms.tgt_platform: multiple
title: Método SetPowerState de la clase CIM_UnitaryComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UnitaryComputerSystem.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4d9b69306c7bb362dceaee254be5dae8f5d37a52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998071"
---
# <a name="setpowerstate-method-of-the-cim_unitarycomputersystem-class"></a><span data-ttu-id="b76bf-103">Método SetPowerState de la \_ clase CIM UnitaryComputerSystem</span><span class="sxs-lookup"><span data-stu-id="b76bf-103">SetPowerState method of the CIM\_UnitaryComputerSystem class</span></span>

<span data-ttu-id="b76bf-104">El método **SetPowerState** de la \_ clase CIM UnitaryComputerSystem establece el estado de energía deseado para un dispositivo lógico y el momento en que se debe colocar un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="b76bf-104">The **SetPowerState** method of the CIM\_UnitaryComputerSystem class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="b76bf-105">En una subclase, el conjunto de códigos de retorno posibles se debe especificar mediante un calificador **ValueMap** en el método.</span><span class="sxs-lookup"><span data-stu-id="b76bf-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="b76bf-106">Las cadenas a las que se traduce el contenido **ValueMap** también se deben especificar en la subclase como calificador de matriz **Values** .</span><span class="sxs-lookup"><span data-stu-id="b76bf-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="b76bf-107">Este método se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b76bf-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b76bf-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="b76bf-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b76bf-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b76bf-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b76bf-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b76bf-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="b76bf-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b76bf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b76bf-112">*PowerState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b76bf-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b76bf-113">Un valor **ValueMap** que especifica el estado de energía deseado para este dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b76bf-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="b76bf-114"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Potencia completa** (1)</span><span class="sxs-lookup"><span data-stu-id="b76bf-114"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b76bf-115">Potencia completa.</span><span class="sxs-lookup"><span data-stu-id="b76bf-115">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b76bf-116"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (2)</span><span class="sxs-lookup"><span data-stu-id="b76bf-116"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b76bf-117">Ahorro de energía: modo de baja energía.</span><span class="sxs-lookup"><span data-stu-id="b76bf-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b76bf-118"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (3)</span><span class="sxs-lookup"><span data-stu-id="b76bf-118"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b76bf-119">Ahorro de energía en espera.</span><span class="sxs-lookup"><span data-stu-id="b76bf-119">Power save   standby.</span></span>

</dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="b76bf-120"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>Ahorro **de energía: otros** (4)</span><span class="sxs-lookup"><span data-stu-id="b76bf-120"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Power Save - Other** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b76bf-121">Ahorro de energía: otros.</span><span class="sxs-lookup"><span data-stu-id="b76bf-121">Power save   other.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b76bf-122"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (5)</span><span class="sxs-lookup"><span data-stu-id="b76bf-122"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b76bf-123">Ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="b76bf-123">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b76bf-124"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (6** )</span><span class="sxs-lookup"><span data-stu-id="b76bf-124"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b76bf-125">Desconectar.</span><span class="sxs-lookup"><span data-stu-id="b76bf-125">Power off.</span></span>

</dd> <dt>

<span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>

<span data-ttu-id="b76bf-126"><span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>**Hibernación** (7)</span><span class="sxs-lookup"><span data-stu-id="b76bf-126"><span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>**Hibernate** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b76bf-127">Hibernación.</span><span class="sxs-lookup"><span data-stu-id="b76bf-127">Hibernate.</span></span>

</dd> <dt>

<span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>

<span data-ttu-id="b76bf-128"><span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>**Soft off** (8)</span><span class="sxs-lookup"><span data-stu-id="b76bf-128"><span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>**Soft Off** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b76bf-129">Soft off.</span><span class="sxs-lookup"><span data-stu-id="b76bf-129">Soft off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b76bf-130">*Hora* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b76bf-130">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b76bf-131">Especifica cuándo se debe establecer el estado de energía, ya sea como un valor de fecha y hora normal o como un valor de intervalo (donde el intervalo comienza cuando se recibe la invocación del método).</span><span class="sxs-lookup"><span data-stu-id="b76bf-131">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="b76bf-132">Cuando el parámetro *PowerState* es igual a 5 ("ciclo de energía"), el parámetro *Time* indica cuándo debe encenderse el dispositivo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="b76bf-132">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="b76bf-133">El apagado es inmediato.</span><span class="sxs-lookup"><span data-stu-id="b76bf-133">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b76bf-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b76bf-134">Return value</span></span>

<span data-ttu-id="b76bf-135">Devuelve 0 (cero) si es correcto, 1 (uno) si no se admite la solicitud *PowerState* y *Time* especificada y otro valor si se produjo algún otro error.</span><span class="sxs-lookup"><span data-stu-id="b76bf-135">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="b76bf-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b76bf-136">Remarks</span></span>

<span data-ttu-id="b76bf-137">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="b76bf-137">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="b76bf-138">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="b76bf-138">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="b76bf-139">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="b76bf-139">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b76bf-140">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="b76bf-140">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b76bf-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b76bf-141">Requirements</span></span>



| <span data-ttu-id="b76bf-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="b76bf-142">Requirement</span></span> | <span data-ttu-id="b76bf-143">Value</span><span class="sxs-lookup"><span data-stu-id="b76bf-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b76bf-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b76bf-144">Minimum supported client</span></span><br/> | <span data-ttu-id="b76bf-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b76bf-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b76bf-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b76bf-146">Minimum supported server</span></span><br/> | <span data-ttu-id="b76bf-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b76bf-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b76bf-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b76bf-148">Namespace</span></span><br/>                | <span data-ttu-id="b76bf-149">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b76bf-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b76bf-150">MOF</span><span class="sxs-lookup"><span data-stu-id="b76bf-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b76bf-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b76bf-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b76bf-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b76bf-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b76bf-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b76bf-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b76bf-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="b76bf-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b76bf-155">\_UNITARYCOMPUTERSYSTEM CIM</span><span class="sxs-lookup"><span data-stu-id="b76bf-155">CIM\_UnitaryComputerSystem</span></span>](setpowerstate-method-in-class-cim-unitarycomputersystem.md)
</dt> <dt>

[<span data-ttu-id="b76bf-156">**\_UNITARYCOMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="b76bf-156">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> </dl>

 

 




