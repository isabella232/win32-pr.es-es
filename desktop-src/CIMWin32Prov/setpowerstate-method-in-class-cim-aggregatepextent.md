---
description: El método SetPowerState establece el estado de energía deseado para un dispositivo lógico y el momento en que el dispositivo debe ponerse en ese estado.
ms.assetid: 1a1a8d5e-d685-4b7e-99fb-61fa2e7bdafa
ms.tgt_platform: multiple
title: Método SetPowerState de la clase CIM_AggregatePExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePExtent.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 47c97f30da1c8b6f2fe9a6032ef9be9ae87a7d6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000644"
---
# <a name="setpowerstate-method-of-the-cim_aggregatepextent-class"></a><span data-ttu-id="fdd7f-103">Método SetPowerState de la \_ clase CIM AggregatePExtent</span><span class="sxs-lookup"><span data-stu-id="fdd7f-103">SetPowerState method of the CIM\_AggregatePExtent class</span></span>

<span data-ttu-id="fdd7f-104">El método **SetPowerState** establece el estado de energía deseado para un dispositivo lógico y el momento en que el dispositivo debe ponerse en ese estado.</span><span class="sxs-lookup"><span data-stu-id="fdd7f-104">The **SetPowerState** method sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="fdd7f-105">En una subclase, el conjunto de códigos de retorno posibles se debe especificar mediante un calificador **ValueMap** en el método.</span><span class="sxs-lookup"><span data-stu-id="fdd7f-105">In a subclass, the set of possible return codes should be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="fdd7f-106">Las cadenas a las que se traduce el contenido **ValueMap** también se deben especificar en la subclase como calificador de matriz **Values** .</span><span class="sxs-lookup"><span data-stu-id="fdd7f-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="fdd7f-107">Este método se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fdd7f-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="fdd7f-108">Para obtener más información sobre el uso de este método con C/C++, vea [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fdd7f-108">For more information about using this method with C/C++, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fdd7f-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="fdd7f-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fdd7f-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fdd7f-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fdd7f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fdd7f-111">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="fdd7f-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fdd7f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdd7f-113">*PowerState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fdd7f-113">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdd7f-114">Valor de **ValueMap** que especifica el estado de energía deseado para este dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fdd7f-114">The **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="fdd7f-115">1</span><span class="sxs-lookup"><span data-stu-id="fdd7f-115">1</span></span>
</dt> <dd>

<span data-ttu-id="fdd7f-116">Energía completa</span><span class="sxs-lookup"><span data-stu-id="fdd7f-116">Full power</span></span>

</dd> <dt>

<span data-ttu-id="fdd7f-117">2</span><span class="sxs-lookup"><span data-stu-id="fdd7f-117">2</span></span>
</dt> <dd>

<span data-ttu-id="fdd7f-118">Ahorro de energía: modo de baja energía</span><span class="sxs-lookup"><span data-stu-id="fdd7f-118">Power-save   low-power mode</span></span>

</dd> <dt>

<span data-ttu-id="fdd7f-119">3</span><span class="sxs-lookup"><span data-stu-id="fdd7f-119">3</span></span>
</dt> <dd>

<span data-ttu-id="fdd7f-120">Ahorro de energía en espera</span><span class="sxs-lookup"><span data-stu-id="fdd7f-120">Power-save   standby</span></span>

</dd> <dt>

<span data-ttu-id="fdd7f-121">4</span><span class="sxs-lookup"><span data-stu-id="fdd7f-121">4</span></span>
</dt> <dd>

<span data-ttu-id="fdd7f-122">Ahorro de energía: otro</span><span class="sxs-lookup"><span data-stu-id="fdd7f-122">Power-save   other</span></span>

</dd> <dt>

<span data-ttu-id="fdd7f-123">5</span><span class="sxs-lookup"><span data-stu-id="fdd7f-123">5</span></span>
</dt> <dd>

<span data-ttu-id="fdd7f-124">Ciclo de energía</span><span class="sxs-lookup"><span data-stu-id="fdd7f-124">Power cycle</span></span>

</dd> <dt>

<span data-ttu-id="fdd7f-125">6</span><span class="sxs-lookup"><span data-stu-id="fdd7f-125">6</span></span>
</dt> <dd>

<span data-ttu-id="fdd7f-126">Apagado</span><span class="sxs-lookup"><span data-stu-id="fdd7f-126">Power off</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fdd7f-127">*Hora* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fdd7f-127">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdd7f-128">Cuando se debe establecer el estado de energía, ya sea como un valor de fecha y hora normal o como un valor de intervalo (donde el intervalo comienza cuando se recibe la invocación del método).</span><span class="sxs-lookup"><span data-stu-id="fdd7f-128">When the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="fdd7f-129">Cuando el parámetro *PowerState* es igual a 5 (ciclo de energía), el parámetro *Time* indica cuándo debe volver a encenderse el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fdd7f-129">When the *PowerState* parameter is equal to 5 (power cycle), the *Time* parameter indicates when the device should power-on again.</span></span> <span data-ttu-id="fdd7f-130">El apagado es inmediato.</span><span class="sxs-lookup"><span data-stu-id="fdd7f-130">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdd7f-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fdd7f-131">Return value</span></span>

<span data-ttu-id="fdd7f-132">Devuelve 0 (cero) si es correcto, 1 (uno) si no se admite la solicitud *PowerState* y *Time* especificada y otro valor si se produjo algún otro error.</span><span class="sxs-lookup"><span data-stu-id="fdd7f-132">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdd7f-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fdd7f-133">Remarks</span></span>

<span data-ttu-id="fdd7f-134">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="fdd7f-134">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="fdd7f-135">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="fdd7f-135">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="fdd7f-136">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="fdd7f-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fdd7f-137">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="fdd7f-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdd7f-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdd7f-138">Requirements</span></span>



| <span data-ttu-id="fdd7f-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdd7f-139">Requirement</span></span> | <span data-ttu-id="fdd7f-140">Value</span><span class="sxs-lookup"><span data-stu-id="fdd7f-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd7f-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fdd7f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="fdd7f-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fdd7f-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fdd7f-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fdd7f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="fdd7f-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fdd7f-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fdd7f-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fdd7f-145">Namespace</span></span><br/>                | <span data-ttu-id="fdd7f-146">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="fdd7f-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fdd7f-147">MOF</span><span class="sxs-lookup"><span data-stu-id="fdd7f-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fdd7f-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fdd7f-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fdd7f-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fdd7f-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdd7f-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdd7f-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdd7f-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="fdd7f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdd7f-152">**\_AGGREGATEPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fdd7f-152">**CIM\_AggregatePExtent**</span></span>](setpowerstate-method-in-class-cim-aggregatepextent.md)
</dt> <dt>

[<span data-ttu-id="fdd7f-153">**\_AGGREGATEPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fdd7f-153">**CIM\_AggregatePExtent**</span></span>](cim-aggregatepextent.md)
</dt> </dl>

 

