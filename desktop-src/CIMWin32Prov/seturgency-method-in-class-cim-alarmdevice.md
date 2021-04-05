---
description: El método SetUrgency establece el nivel de urgencia deseado para una alarma.
ms.assetid: ac2e7fda-1317-440a-adbd-1ef0844d124c
ms.tgt_platform: multiple
title: Método SetUrgency de la clase CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.SetUrgency
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35918677e210ac2fe7ac4798a04db9dc628f5fa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000598"
---
# <a name="seturgency-method-of-the-cim_alarmdevice-class"></a><span data-ttu-id="4adfd-103">Método SetUrgency de la \_ clase AlarmDevice de CIM</span><span class="sxs-lookup"><span data-stu-id="4adfd-103">SetUrgency method of the CIM\_AlarmDevice class</span></span>

<span data-ttu-id="4adfd-104">El método **SetUrgency** establece el nivel de urgencia deseado para una alarma.</span><span class="sxs-lookup"><span data-stu-id="4adfd-104">The **SetUrgency** method sets the desired urgency level for an alarm.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4adfd-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="4adfd-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4adfd-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4adfd-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4adfd-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4adfd-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4adfd-108">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4adfd-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4adfd-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4adfd-109">Syntax</span></span>


```mof
uint32 SetUrgency(
  [in] uint16 RequestedUrgency
);
```



## <a name="parameters"></a><span data-ttu-id="4adfd-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4adfd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4adfd-111">*RequestedUrgency* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4adfd-111">*RequestedUrgency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4adfd-112">Frecuencia relativa con la que la alarma parpadea, vibra o emite tonos sonoros.</span><span class="sxs-lookup"><span data-stu-id="4adfd-112">Relative frequency at which the alarm flashes, vibrates, or emits audible tones.</span></span> <span data-ttu-id="4adfd-113">Los siguientes valores proceden de la propiedad **urgencia** de [**CIM \_ AlarmDevice**](cim-alarmdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4adfd-113">The following values are from the **Urgency** property in [**CIM\_AlarmDevice**](cim-alarmdevice.md).</span></span>

<dt>

<span data-ttu-id="4adfd-114">0</span><span class="sxs-lookup"><span data-stu-id="4adfd-114">0</span></span>
</dt> <dd>

<span data-ttu-id="4adfd-115">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="4adfd-115">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="4adfd-116">1</span><span class="sxs-lookup"><span data-stu-id="4adfd-116">1</span></span>
</dt> <dd>

<span data-ttu-id="4adfd-117">Otros.</span><span class="sxs-lookup"><span data-stu-id="4adfd-117">Other.</span></span>

</dd> <dt>

<span data-ttu-id="4adfd-118">2</span><span class="sxs-lookup"><span data-stu-id="4adfd-118">2</span></span>
</dt> <dd>

<span data-ttu-id="4adfd-119">No se admite.</span><span class="sxs-lookup"><span data-stu-id="4adfd-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4adfd-120">3</span><span class="sxs-lookup"><span data-stu-id="4adfd-120">3</span></span>
</dt> <dd>

<span data-ttu-id="4adfd-121">Informativo.</span><span class="sxs-lookup"><span data-stu-id="4adfd-121">Informational.</span></span>

</dd> <dt>

<span data-ttu-id="4adfd-122">4</span><span class="sxs-lookup"><span data-stu-id="4adfd-122">4</span></span>
</dt> <dd>

<span data-ttu-id="4adfd-123">No crítico.</span><span class="sxs-lookup"><span data-stu-id="4adfd-123">Non-critical.</span></span>

</dd> <dt>

<span data-ttu-id="4adfd-124">5</span><span class="sxs-lookup"><span data-stu-id="4adfd-124">5</span></span>
</dt> <dd>

<span data-ttu-id="4adfd-125">Crítico.</span><span class="sxs-lookup"><span data-stu-id="4adfd-125">Critical.</span></span>

</dd> <dt>

<span data-ttu-id="4adfd-126">6</span><span class="sxs-lookup"><span data-stu-id="4adfd-126">6</span></span>
</dt> <dd>

<span data-ttu-id="4adfd-127">Irrecuperable.</span><span class="sxs-lookup"><span data-stu-id="4adfd-127">Unrecoverable.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4adfd-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4adfd-128">Return value</span></span>

<span data-ttu-id="4adfd-129">Devuelve un valor de 0 (cero) si se realiza correctamente, 1 (uno) si no se admite el nivel de urgencia solicitado y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="4adfd-129">Returns a value of 0 (zero) on success, 1 (one) if the requested urgency level is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="4adfd-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4adfd-130">Remarks</span></span>

<span data-ttu-id="4adfd-131">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="4adfd-131">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4adfd-132">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="4adfd-132">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4adfd-133">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="4adfd-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4adfd-134">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="4adfd-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4adfd-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4adfd-135">Requirements</span></span>



| <span data-ttu-id="4adfd-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="4adfd-136">Requirement</span></span> | <span data-ttu-id="4adfd-137">Value</span><span class="sxs-lookup"><span data-stu-id="4adfd-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4adfd-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4adfd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4adfd-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4adfd-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4adfd-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4adfd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4adfd-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4adfd-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4adfd-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4adfd-142">Namespace</span></span><br/>                | <span data-ttu-id="4adfd-143">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4adfd-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4adfd-144">MOF</span><span class="sxs-lookup"><span data-stu-id="4adfd-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4adfd-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4adfd-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4adfd-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4adfd-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4adfd-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4adfd-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4adfd-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="4adfd-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4adfd-149">\_ALARMDEVICE CIM</span><span class="sxs-lookup"><span data-stu-id="4adfd-149">CIM\_AlarmDevice</span></span>](seturgency-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[<span data-ttu-id="4adfd-150">**\_ALARMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="4adfd-150">**CIM\_AlarmDevice**</span></span>](cim-alarmdevice.md)
</dt> </dl>

 

