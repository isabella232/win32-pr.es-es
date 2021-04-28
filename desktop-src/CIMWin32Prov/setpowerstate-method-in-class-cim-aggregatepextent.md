---
description: 'Método SetPowerState de la clase CIM_AggregatePExtent: el método SetPowerState establece el estado de energía deseado para un dispositivo lógico y cuándo se debe colocar el dispositivo en ese estado.'
ms.assetid: 1a1a8d5e-d685-4b7e-99fb-61fa2e7bdafa
ms.tgt_platform: multiple
title: Método SetPowerState de la CIM_AggregatePExtent clase
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
ms.openlocfilehash: 5ed988e5f58464479aa29d709eb628feb13f0d1c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089543"
---
# <a name="setpowerstate-method-of-the-cim_aggregatepextent-class"></a><span data-ttu-id="8acb2-103">Método SetPowerState de la clase \_ AggregatePExtent de CIM</span><span class="sxs-lookup"><span data-stu-id="8acb2-103">SetPowerState method of the CIM\_AggregatePExtent class</span></span>

<span data-ttu-id="8acb2-104">El **método SetPowerState** establece el estado de energía deseado para un dispositivo lógico y cuándo se debe colocar el dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="8acb2-104">The **SetPowerState** method sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="8acb2-105">En una subclase, el conjunto de códigos de retorno posibles debe especificarse mediante un **calificador ValueMap** en el método .</span><span class="sxs-lookup"><span data-stu-id="8acb2-105">In a subclass, the set of possible return codes should be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="8acb2-106">Las cadenas a las que se traduce el contenido de **ValueMap** también se deben especificar en la subclase como calificador **de matriz Values.**</span><span class="sxs-lookup"><span data-stu-id="8acb2-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="8acb2-107">Este método se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="8acb2-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="8acb2-108">Para obtener más información sobre el uso de este método con C/C++, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8acb2-108">For more information about using this method with C/C++, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8acb2-109">Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI.</span><span class="sxs-lookup"><span data-stu-id="8acb2-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8acb2-110">WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8acb2-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8acb2-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8acb2-111">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="8acb2-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8acb2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8acb2-113">*PowerState* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8acb2-113">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8acb2-114">Valor **valueMap** que especifica el estado de energía deseado para este dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8acb2-114">The **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="8acb2-115">1</span><span class="sxs-lookup"><span data-stu-id="8acb2-115">1</span></span>
</dt> <dd>

<span data-ttu-id="8acb2-116">Potencia completa</span><span class="sxs-lookup"><span data-stu-id="8acb2-116">Full power</span></span>

</dd> <dt>

<span data-ttu-id="8acb2-117">2</span><span class="sxs-lookup"><span data-stu-id="8acb2-117">2</span></span>
</dt> <dd>

<span data-ttu-id="8acb2-118">Modo de bajo consumo de energía con ahorro de energía</span><span class="sxs-lookup"><span data-stu-id="8acb2-118">Power-save   low-power mode</span></span>

</dd> <dt>

<span data-ttu-id="8acb2-119">3</span><span class="sxs-lookup"><span data-stu-id="8acb2-119">3</span></span>
</dt> <dd>

<span data-ttu-id="8acb2-120">Espera de ahorro de energía</span><span class="sxs-lookup"><span data-stu-id="8acb2-120">Power-save   standby</span></span>

</dd> <dt>

<span data-ttu-id="8acb2-121">4</span><span class="sxs-lookup"><span data-stu-id="8acb2-121">4</span></span>
</dt> <dd>

<span data-ttu-id="8acb2-122">Power-save other</span><span class="sxs-lookup"><span data-stu-id="8acb2-122">Power-save   other</span></span>

</dd> <dt>

<span data-ttu-id="8acb2-123">5</span><span class="sxs-lookup"><span data-stu-id="8acb2-123">5</span></span>
</dt> <dd>

<span data-ttu-id="8acb2-124">Ciclo de energía</span><span class="sxs-lookup"><span data-stu-id="8acb2-124">Power cycle</span></span>

</dd> <dt>

<span data-ttu-id="8acb2-125">6</span><span class="sxs-lookup"><span data-stu-id="8acb2-125">6</span></span>
</dt> <dd>

<span data-ttu-id="8acb2-126">Apagado</span><span class="sxs-lookup"><span data-stu-id="8acb2-126">Power off</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8acb2-127">*Hora* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8acb2-127">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8acb2-128">Cuando se debe establecer el estado de energía, ya sea como un valor de fecha y hora normal o como un valor de intervalo (donde el intervalo comienza cuando se recibe la invocación del método).</span><span class="sxs-lookup"><span data-stu-id="8acb2-128">When the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="8acb2-129">Cuando el *parámetro PowerState* es igual a 5 (ciclo de energía), el parámetro *Time* indica cuándo se debe volver a encender el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8acb2-129">When the *PowerState* parameter is equal to 5 (power cycle), the *Time* parameter indicates when the device should power-on again.</span></span> <span data-ttu-id="8acb2-130">El apagado es inmediato.</span><span class="sxs-lookup"><span data-stu-id="8acb2-130">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8acb2-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8acb2-131">Return value</span></span>

<span data-ttu-id="8acb2-132">Devuelve 0 (cero) si se realiza correctamente, 1 (uno) si no se admite la solicitud *PowerState* y *Time* especificadas y otro valor si se produjo cualquier otro error.</span><span class="sxs-lookup"><span data-stu-id="8acb2-132">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="8acb2-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8acb2-133">Remarks</span></span>

<span data-ttu-id="8acb2-134">Wmi no implementa actualmente este método.</span><span class="sxs-lookup"><span data-stu-id="8acb2-134">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8acb2-135">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="8acb2-135">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="8acb2-136">Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf.</span><span class="sxs-lookup"><span data-stu-id="8acb2-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8acb2-137">Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="8acb2-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8acb2-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8acb2-138">Requirements</span></span>



| <span data-ttu-id="8acb2-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="8acb2-139">Requirement</span></span> | <span data-ttu-id="8acb2-140">Valor</span><span class="sxs-lookup"><span data-stu-id="8acb2-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8acb2-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8acb2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8acb2-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8acb2-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8acb2-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8acb2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8acb2-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8acb2-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8acb2-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8acb2-145">Namespace</span></span><br/>                | <span data-ttu-id="8acb2-146">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="8acb2-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8acb2-147">MOF</span><span class="sxs-lookup"><span data-stu-id="8acb2-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8acb2-148"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="8acb2-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8acb2-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8acb2-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8acb2-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8acb2-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8acb2-151">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8acb2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8acb2-152">**Agregado \_ de CIMPExtent**</span><span class="sxs-lookup"><span data-stu-id="8acb2-152">**CIM\_AggregatePExtent**</span></span>](setpowerstate-method-in-class-cim-aggregatepextent.md)
</dt> <dt>

[<span data-ttu-id="8acb2-153">**Agregado \_ de CIMPExtent**</span><span class="sxs-lookup"><span data-stu-id="8acb2-153">**CIM\_AggregatePExtent**</span></span>](cim-aggregatepextent.md)
</dt> </dl>

 

