---
description: El método SetPowerState de la \_ clase CIM InfraredController establece el estado de energía deseado para un dispositivo lógico y el momento en que se debe colocar un dispositivo en ese estado.
ms.assetid: dce688f3-b7c2-4e43-a26f-7318ce0011b8
ms.tgt_platform: multiple
title: Método SetPowerState de la clase CIM_InfraredController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InfraredController.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1730071111d1ebf86af229236826647626ca8f71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659576"
---
# <a name="setpowerstate-method-of-the-cim_infraredcontroller-class"></a><span data-ttu-id="f8b9c-103">Método SetPowerState de la \_ clase CIM InfraredController</span><span class="sxs-lookup"><span data-stu-id="f8b9c-103">SetPowerState method of the CIM\_InfraredController class</span></span>

<span data-ttu-id="f8b9c-104">El método **SetPowerState** de la \_ clase CIM InfraredController establece el estado de energía deseado para un dispositivo lógico y el momento en que se debe colocar un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="f8b9c-104">The **SetPowerState** method of the CIM\_InfraredController class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="f8b9c-105">En una subclase, el conjunto de códigos de retorno posibles se debe especificar mediante un calificador **ValueMap** en el método.</span><span class="sxs-lookup"><span data-stu-id="f8b9c-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="f8b9c-106">Las cadenas a las que se traduce el contenido **ValueMap** también se deben especificar en la subclase como calificador de matriz **Values** .</span><span class="sxs-lookup"><span data-stu-id="f8b9c-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="f8b9c-107">Este método se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f8b9c-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f8b9c-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="f8b9c-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f8b9c-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f8b9c-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f8b9c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8b9c-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="f8b9c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8b9c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8b9c-112">*PowerState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f8b9c-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8b9c-113">Un valor **ValueMap** que especifica el estado de energía deseado para el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f8b9c-113">A **ValueMap** value that specifies the desired power state for the logical device.</span></span>

<dt>

<span data-ttu-id="f8b9c-114">1</span><span class="sxs-lookup"><span data-stu-id="f8b9c-114">1</span></span>
</dt> <dd>

<span data-ttu-id="f8b9c-115">Potencia completa.</span><span class="sxs-lookup"><span data-stu-id="f8b9c-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="f8b9c-116">2</span><span class="sxs-lookup"><span data-stu-id="f8b9c-116">2</span></span>
</dt> <dd>

<span data-ttu-id="f8b9c-117">Ahorro de energía: modo de baja energía.</span><span class="sxs-lookup"><span data-stu-id="f8b9c-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="f8b9c-118">3</span><span class="sxs-lookup"><span data-stu-id="f8b9c-118">3</span></span>
</dt> <dd>

<span data-ttu-id="f8b9c-119">Ahorro de energía en espera.</span><span class="sxs-lookup"><span data-stu-id="f8b9c-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="f8b9c-120">4</span><span class="sxs-lookup"><span data-stu-id="f8b9c-120">4</span></span>
</dt> <dd>

<span data-ttu-id="f8b9c-121">Ahorro de energía: otros.</span><span class="sxs-lookup"><span data-stu-id="f8b9c-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="f8b9c-122">5</span><span class="sxs-lookup"><span data-stu-id="f8b9c-122">5</span></span>
</dt> <dd>

<span data-ttu-id="f8b9c-123">Ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="f8b9c-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="f8b9c-124">6</span><span class="sxs-lookup"><span data-stu-id="f8b9c-124">6</span></span>
</dt> <dd>

<span data-ttu-id="f8b9c-125">Desconectar.</span><span class="sxs-lookup"><span data-stu-id="f8b9c-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f8b9c-126">*Hora* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f8b9c-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8b9c-127">Especifica cuándo se debe establecer el estado de energía, ya sea como un valor de fecha y hora normal o como un valor de intervalo (donde el intervalo comienza cuando se recibe la invocación del método).</span><span class="sxs-lookup"><span data-stu-id="f8b9c-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="f8b9c-128">Cuando el parámetro *PowerState* es igual a 5 ("ciclo de energía"), el parámetro *Time* indica cuándo debe encenderse el dispositivo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="f8b9c-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="f8b9c-129">El apagado es inmediato.</span><span class="sxs-lookup"><span data-stu-id="f8b9c-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8b9c-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8b9c-130">Return value</span></span>

<span data-ttu-id="f8b9c-131">Devuelve 0 (cero) si es correcto, 1 (uno) si no se admite la solicitud *PowerState* y *Time* especificada y otro valor si se produjo algún otro error.</span><span class="sxs-lookup"><span data-stu-id="f8b9c-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8b9c-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8b9c-132">Remarks</span></span>

<span data-ttu-id="f8b9c-133">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="f8b9c-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f8b9c-134">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="f8b9c-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f8b9c-135">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="f8b9c-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f8b9c-136">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="f8b9c-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8b9c-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8b9c-137">Requirements</span></span>



| <span data-ttu-id="f8b9c-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8b9c-138">Requirement</span></span> | <span data-ttu-id="f8b9c-139">Value</span><span class="sxs-lookup"><span data-stu-id="f8b9c-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b9c-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8b9c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f8b9c-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8b9c-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f8b9c-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8b9c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f8b9c-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8b9c-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8b9c-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f8b9c-144">Namespace</span></span><br/>                | <span data-ttu-id="f8b9c-145">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f8b9c-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f8b9c-146">MOF</span><span class="sxs-lookup"><span data-stu-id="f8b9c-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8b9c-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8b9c-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8b9c-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f8b9c-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8b9c-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8b9c-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8b9c-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8b9c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8b9c-151">\_INFRAREDCONTROLLER CIM</span><span class="sxs-lookup"><span data-stu-id="f8b9c-151">CIM\_InfraredController</span></span>](setpowerstate-method-in-class-cim-infraredcontroller.md)
</dt> <dt>

[<span data-ttu-id="f8b9c-152">**\_INFRAREDCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="f8b9c-152">**CIM\_InfraredController**</span></span>](cim-infraredcontroller.md)
</dt> </dl>

 

 




