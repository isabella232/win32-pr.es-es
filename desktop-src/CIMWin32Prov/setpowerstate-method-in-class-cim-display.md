---
description: El método SetPowerState de la \_ clase CIM display establece el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.
ms.assetid: 949c300c-b01b-4c91-a902-41e940667ee6
ms.tgt_platform: multiple
title: Método SetPowerState de la clase CIM_Display
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Display.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35bcf49419b934e98c63b2151dcdaf3cb55f8d97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152976"
---
# <a name="setpowerstate-method-of-the-cim_display-class"></a><span data-ttu-id="f7eef-103">Método SetPowerState de la \_ clase CIM display</span><span class="sxs-lookup"><span data-stu-id="f7eef-103">SetPowerState method of the CIM\_Display class</span></span>

<span data-ttu-id="f7eef-104">El método **SetPowerState** de la \_ clase CIM display establece el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="f7eef-104">The **SetPowerState** method of the CIM\_Display class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="f7eef-105">En una subclase, el conjunto de códigos de retorno posibles se debe especificar mediante un calificador **ValueMap** en el método.</span><span class="sxs-lookup"><span data-stu-id="f7eef-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="f7eef-106">Las cadenas a las que se traduce el contenido **ValueMap** también se deben especificar en la subclase como calificador de matriz **Values** .</span><span class="sxs-lookup"><span data-stu-id="f7eef-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f7eef-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="f7eef-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f7eef-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f7eef-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f7eef-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7eef-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="f7eef-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7eef-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7eef-111">*PowerState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f7eef-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7eef-112">Un valor **ValueMap** que especifica el estado de energía deseado para este dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f7eef-112">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="f7eef-113">1</span><span class="sxs-lookup"><span data-stu-id="f7eef-113">1</span></span>
</dt> <dd>

<span data-ttu-id="f7eef-114">Potencia completa.</span><span class="sxs-lookup"><span data-stu-id="f7eef-114">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="f7eef-115">2</span><span class="sxs-lookup"><span data-stu-id="f7eef-115">2</span></span>
</dt> <dd>

<span data-ttu-id="f7eef-116">Ahorro de energía: modo de baja energía.</span><span class="sxs-lookup"><span data-stu-id="f7eef-116">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="f7eef-117">3</span><span class="sxs-lookup"><span data-stu-id="f7eef-117">3</span></span>
</dt> <dd>

<span data-ttu-id="f7eef-118">Ahorro de energía en espera.</span><span class="sxs-lookup"><span data-stu-id="f7eef-118">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="f7eef-119">4</span><span class="sxs-lookup"><span data-stu-id="f7eef-119">4</span></span>
</dt> <dd>

<span data-ttu-id="f7eef-120">Ahorro de energía: otros.</span><span class="sxs-lookup"><span data-stu-id="f7eef-120">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="f7eef-121">5</span><span class="sxs-lookup"><span data-stu-id="f7eef-121">5</span></span>
</dt> <dd>

<span data-ttu-id="f7eef-122">Ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="f7eef-122">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="f7eef-123">6</span><span class="sxs-lookup"><span data-stu-id="f7eef-123">6</span></span>
</dt> <dd>

<span data-ttu-id="f7eef-124">Desconectar.</span><span class="sxs-lookup"><span data-stu-id="f7eef-124">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f7eef-125">*Hora* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f7eef-125">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7eef-126">Especifica cuándo se debe establecer el estado de energía, ya sea como un valor de fecha y hora normal o como un valor de intervalo (donde el intervalo comienza cuando se recibe la invocación del método).</span><span class="sxs-lookup"><span data-stu-id="f7eef-126">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="f7eef-127">Cuando el parámetro *PowerState* es igual a 5 ("ciclo de energía"), el parámetro *Time* indica cuándo debe encenderse el dispositivo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="f7eef-127">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="f7eef-128">El apagado es inmediato.</span><span class="sxs-lookup"><span data-stu-id="f7eef-128">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7eef-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7eef-129">Return value</span></span>

<span data-ttu-id="f7eef-130">Devuelve 0 (cero) si es correcto, 1 (uno) si no se admite la solicitud *PowerState* y *Time* especificada y otro valor si se produjo algún otro error.</span><span class="sxs-lookup"><span data-stu-id="f7eef-130">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7eef-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7eef-131">Remarks</span></span>

<span data-ttu-id="f7eef-132">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="f7eef-132">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f7eef-133">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="f7eef-133">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f7eef-134">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="f7eef-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f7eef-135">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="f7eef-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7eef-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7eef-136">Requirements</span></span>



| <span data-ttu-id="f7eef-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7eef-137">Requirement</span></span> | <span data-ttu-id="f7eef-138">Value</span><span class="sxs-lookup"><span data-stu-id="f7eef-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7eef-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7eef-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f7eef-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7eef-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f7eef-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7eef-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f7eef-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7eef-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f7eef-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f7eef-143">Namespace</span></span><br/>                | <span data-ttu-id="f7eef-144">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f7eef-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f7eef-145">MOF</span><span class="sxs-lookup"><span data-stu-id="f7eef-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7eef-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7eef-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7eef-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f7eef-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7eef-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7eef-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7eef-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7eef-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7eef-150">Presentación de CIM \_</span><span class="sxs-lookup"><span data-stu-id="f7eef-150">CIM\_Display</span></span>](setpowerstate-method-in-class-cim-display.md)
</dt> <dt>

[<span data-ttu-id="f7eef-151">**Presentación de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="f7eef-151">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 

 




