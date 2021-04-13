---
description: El método SetPowerState de la \_ clase CIM TapeDrive establece el estado de energía deseado para un dispositivo lógico y el momento en que se debe colocar un dispositivo en ese estado.
ms.assetid: 73f98d08-49da-4b21-91c4-cbe420c648e4
ms.tgt_platform: multiple
title: Método SetPowerState de la clase CIM_TapeDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a6efcfe08dfddca3477081f65fac35780f713005
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539267"
---
# <a name="setpowerstate-method-of-the-cim_tapedrive-class"></a><span data-ttu-id="d5e74-103">Método SetPowerState de la \_ clase CIM TapeDrive</span><span class="sxs-lookup"><span data-stu-id="d5e74-103">SetPowerState method of the CIM\_TapeDrive class</span></span>

<span data-ttu-id="d5e74-104">El método **SetPowerState** de la \_ clase CIM TapeDrive establece el estado de energía deseado para un dispositivo lógico y el momento en que se debe colocar un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="d5e74-104">The **SetPowerState** method of the CIM\_TapeDrive class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="d5e74-105">En una subclase, el conjunto de códigos de retorno posibles se debe especificar mediante un calificador **ValueMap** en el método.</span><span class="sxs-lookup"><span data-stu-id="d5e74-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="d5e74-106">Las cadenas a las que se traduce el contenido **ValueMap** también se deben especificar en la subclase como calificador de matriz **Values** .</span><span class="sxs-lookup"><span data-stu-id="d5e74-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="d5e74-107">Este método se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d5e74-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5e74-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5e74-108">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="d5e74-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5e74-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5e74-110">*PowerState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5e74-110">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5e74-111">Un valor **ValueMap** que especifica el estado de energía deseado para este dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d5e74-111">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="d5e74-112">1</span><span class="sxs-lookup"><span data-stu-id="d5e74-112">1</span></span>
</dt> <dd>

<span data-ttu-id="d5e74-113">Potencia completa.</span><span class="sxs-lookup"><span data-stu-id="d5e74-113">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="d5e74-114">2</span><span class="sxs-lookup"><span data-stu-id="d5e74-114">2</span></span>
</dt> <dd>

<span data-ttu-id="d5e74-115">Ahorro de energía: modo de baja energía.</span><span class="sxs-lookup"><span data-stu-id="d5e74-115">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="d5e74-116">3</span><span class="sxs-lookup"><span data-stu-id="d5e74-116">3</span></span>
</dt> <dd>

<span data-ttu-id="d5e74-117">Ahorro de energía en espera.</span><span class="sxs-lookup"><span data-stu-id="d5e74-117">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="d5e74-118">4</span><span class="sxs-lookup"><span data-stu-id="d5e74-118">4</span></span>
</dt> <dd>

<span data-ttu-id="d5e74-119">Ahorro de energía: otros.</span><span class="sxs-lookup"><span data-stu-id="d5e74-119">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="d5e74-120">5</span><span class="sxs-lookup"><span data-stu-id="d5e74-120">5</span></span>
</dt> <dd>

<span data-ttu-id="d5e74-121">Ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="d5e74-121">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="d5e74-122">6</span><span class="sxs-lookup"><span data-stu-id="d5e74-122">6</span></span>
</dt> <dd>

<span data-ttu-id="d5e74-123">Desconectar.</span><span class="sxs-lookup"><span data-stu-id="d5e74-123">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d5e74-124">*Hora* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d5e74-124">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5e74-125">Especifica cuándo se debe establecer el estado de energía, ya sea como un valor de fecha y hora normal o como un valor de intervalo (donde el intervalo comienza cuando se recibe la invocación del método).</span><span class="sxs-lookup"><span data-stu-id="d5e74-125">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="d5e74-126">Cuando el parámetro *PowerState* es igual a 5 ("ciclo de energía"), el parámetro *Time* indica cuándo debe encenderse el dispositivo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="d5e74-126">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="d5e74-127">El apagado es inmediato.</span><span class="sxs-lookup"><span data-stu-id="d5e74-127">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5e74-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5e74-128">Return value</span></span>

<span data-ttu-id="d5e74-129">Devuelve 0 (cero) si es correcto, 1 (uno) si no se admite la solicitud *PowerState* y *Time* especificada y otro valor si se produjo algún otro error.</span><span class="sxs-lookup"><span data-stu-id="d5e74-129">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5e74-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5e74-130">Remarks</span></span>

<span data-ttu-id="d5e74-131">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="d5e74-131">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="d5e74-132">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="d5e74-132">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="d5e74-133">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="d5e74-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d5e74-134">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="d5e74-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5e74-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5e74-135">Requirements</span></span>



| <span data-ttu-id="d5e74-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5e74-136">Requirement</span></span> | <span data-ttu-id="d5e74-137">Value</span><span class="sxs-lookup"><span data-stu-id="d5e74-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e74-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5e74-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d5e74-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5e74-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d5e74-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5e74-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d5e74-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5e74-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5e74-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d5e74-142">Namespace</span></span><br/>                | <span data-ttu-id="d5e74-143">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d5e74-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d5e74-144">MOF</span><span class="sxs-lookup"><span data-stu-id="d5e74-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5e74-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5e74-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5e74-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d5e74-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5e74-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5e74-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5e74-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5e74-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5e74-149">CIM \_ TapeDrive</span><span class="sxs-lookup"><span data-stu-id="d5e74-149">CIM\_TapeDrive</span></span>](setpowerstate-method-in-class-cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="d5e74-150">**CIM \_ TapeDrive**</span><span class="sxs-lookup"><span data-stu-id="d5e74-150">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> </dl>

 

 




