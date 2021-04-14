---
description: El método SetPowerState establece el estado de energía deseado para un dispositivo lógico y el momento en que se debe colocar un dispositivo en ese estado.
ms.assetid: f6c7e731-6642-480d-8b88-d8a3fcbd6e33
ms.tgt_platform: multiple
title: Método SetPowerState de la clase CIM_VoltageSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VoltageSensor.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b206a765f7f843b1296e2971fe73792603689b9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496613"
---
# <a name="setpowerstate-method-of-the-cim_voltagesensor-class"></a><span data-ttu-id="02abc-103">Método SetPowerState de la \_ clase CIM VoltageSensor</span><span class="sxs-lookup"><span data-stu-id="02abc-103">SetPowerState method of the CIM\_VoltageSensor class</span></span>

<span data-ttu-id="02abc-104">El método **SetPowerState** establece el estado de energía deseado para un dispositivo lógico y el momento en que se debe colocar un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="02abc-104">The **SetPowerState** method sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="02abc-105">En una subclase, el conjunto de códigos de retorno posibles se debe especificar mediante un calificador [**ValueMap**](/windows/desktop/WmiSdk/standard-qualifiers) en el método.</span><span class="sxs-lookup"><span data-stu-id="02abc-105">In a subclass, the set of possible return codes should be specified by using a [**ValueMap**](/windows/desktop/WmiSdk/standard-qualifiers) qualifier on the method.</span></span> <span data-ttu-id="02abc-106">Las cadenas a las que se traduce el contenido **ValueMap** también se deben especificar en la subclase como calificador de matriz **Values** .</span><span class="sxs-lookup"><span data-stu-id="02abc-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="02abc-107">Este método se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="02abc-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02abc-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="02abc-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="02abc-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="02abc-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="02abc-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02abc-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="02abc-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02abc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02abc-112">*PowerState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="02abc-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02abc-113">Un valor [**ValueMap**](/windows/desktop/WmiSdk/standard-qualifiers) que especifica el estado de energía deseado para este dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="02abc-113">A [**ValueMap**](/windows/desktop/WmiSdk/standard-qualifiers) value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="02abc-114">1</span><span class="sxs-lookup"><span data-stu-id="02abc-114">1</span></span>
</dt> <dd>

<span data-ttu-id="02abc-115">Potencia completa.</span><span class="sxs-lookup"><span data-stu-id="02abc-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="02abc-116">2</span><span class="sxs-lookup"><span data-stu-id="02abc-116">2</span></span>
</dt> <dd>

<span data-ttu-id="02abc-117">Ahorro de energía: modo de baja energía.</span><span class="sxs-lookup"><span data-stu-id="02abc-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="02abc-118">3</span><span class="sxs-lookup"><span data-stu-id="02abc-118">3</span></span>
</dt> <dd>

<span data-ttu-id="02abc-119">Ahorro de energía en espera.</span><span class="sxs-lookup"><span data-stu-id="02abc-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="02abc-120">4</span><span class="sxs-lookup"><span data-stu-id="02abc-120">4</span></span>
</dt> <dd>

<span data-ttu-id="02abc-121">Ahorro de energía: otros.</span><span class="sxs-lookup"><span data-stu-id="02abc-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="02abc-122">5</span><span class="sxs-lookup"><span data-stu-id="02abc-122">5</span></span>
</dt> <dd>

<span data-ttu-id="02abc-123">Ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="02abc-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="02abc-124">6</span><span class="sxs-lookup"><span data-stu-id="02abc-124">6</span></span>
</dt> <dd>

<span data-ttu-id="02abc-125">Desconectar.</span><span class="sxs-lookup"><span data-stu-id="02abc-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="02abc-126">*Hora* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="02abc-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02abc-127">Especifica cuándo se debe establecer el estado de energía, ya sea como un valor de fecha y hora normal o como un valor de intervalo (donde el intervalo comienza cuando se recibe la invocación del método).</span><span class="sxs-lookup"><span data-stu-id="02abc-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="02abc-128">Cuando el parámetro *PowerState* es igual a 5 ("ciclo de energía"), el parámetro *Time* indica cuándo debe encenderse el dispositivo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="02abc-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="02abc-129">El apagado es inmediato.</span><span class="sxs-lookup"><span data-stu-id="02abc-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02abc-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02abc-130">Return value</span></span>

<span data-ttu-id="02abc-131">Devuelve 0 (cero) si es correcto, 1 (uno) si no se admite la solicitud *PowerState* y *Time* especificada y otro valor si se produjo algún otro error.</span><span class="sxs-lookup"><span data-stu-id="02abc-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="02abc-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02abc-132">Remarks</span></span>

<span data-ttu-id="02abc-133">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="02abc-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="02abc-134">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="02abc-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="02abc-135">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="02abc-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="02abc-136">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="02abc-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="02abc-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02abc-137">Requirements</span></span>



| <span data-ttu-id="02abc-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="02abc-138">Requirement</span></span> | <span data-ttu-id="02abc-139">Value</span><span class="sxs-lookup"><span data-stu-id="02abc-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02abc-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02abc-140">Minimum supported client</span></span><br/> | <span data-ttu-id="02abc-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02abc-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02abc-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02abc-142">Minimum supported server</span></span><br/> | <span data-ttu-id="02abc-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02abc-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02abc-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="02abc-144">Namespace</span></span><br/>                | <span data-ttu-id="02abc-145">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="02abc-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="02abc-146">MOF</span><span class="sxs-lookup"><span data-stu-id="02abc-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02abc-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02abc-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="02abc-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="02abc-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02abc-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02abc-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02abc-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="02abc-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02abc-151">\_VOLTAGESENSOR CIM</span><span class="sxs-lookup"><span data-stu-id="02abc-151">CIM\_VoltageSensor</span></span>](setpowerstate-method-in-class-cim-voltagesensor.md)
</dt> <dt>

[<span data-ttu-id="02abc-152">**\_VOLTAGESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="02abc-152">**CIM\_VoltageSensor**</span></span>](cim-voltagesensor.md)
</dt> </dl>

 

