---
description: El método ResetCounter restablece los contadores de error y ADVERTENCIA.
ms.assetid: 5bc6c939-cd97-40ca-a16c-5227e7f27c76
ms.tgt_platform: multiple
title: Método ResetCounter de la clase CIM_DeviceErrorCounts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts.ResetCounter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 386547362f5a7aa52bddfbf9df3af01949aecbdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907019"
---
# <a name="resetcounter-method-of-the-cim_deviceerrorcounts-class"></a><span data-ttu-id="b9226-103">Método ResetCounter de la \_ clase DeviceErrorCounts de CIM</span><span class="sxs-lookup"><span data-stu-id="b9226-103">ResetCounter method of the CIM\_DeviceErrorCounts class</span></span>

<span data-ttu-id="b9226-104">El método **ResetCounter** restablece los contadores de error y ADVERTENCIA.</span><span class="sxs-lookup"><span data-stu-id="b9226-104">The **ResetCounter** method resets the error and warning counters.</span></span> <span data-ttu-id="b9226-105">Se usa un método para que la instrumentación del dispositivo lógico, que tabula los errores y las advertencias, también pueda restablecer su procesamiento interno y sus contadores.</span><span class="sxs-lookup"><span data-stu-id="b9226-105">A method is used so that the logical device's instrumentation, which tabulates the errors and warnings, can also reset its internal processing and counters.</span></span> <span data-ttu-id="b9226-106">En una subclase, se puede especificar el conjunto de códigos de retorno posibles mediante un calificador **ValueMap** en el método.</span><span class="sxs-lookup"><span data-stu-id="b9226-106">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="b9226-107">Las cadenas a las que se traduce el contenido **ValueMap** también se pueden especificar en la subclase como calificador de matriz **Values** .</span><span class="sxs-lookup"><span data-stu-id="b9226-107">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b9226-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="b9226-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b9226-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b9226-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b9226-110">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b9226-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b9226-111">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b9226-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9226-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9226-112">Syntax</span></span>


```mof
uint32 ResetCounter(
  [in] uint16 SelectedCounter
);
```



## <a name="parameters"></a><span data-ttu-id="b9226-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9226-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9226-114">*SelectedCounter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b9226-114">*SelectedCounter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9226-115">Contador de errores que se va a restablecer.</span><span class="sxs-lookup"><span data-stu-id="b9226-115">Error counter to reset.</span></span>

<dt>

<span id="All"></span><span id="all"></span><span id="ALL"></span>

<span data-ttu-id="b9226-116">**Todo** (0)</span><span class="sxs-lookup"><span data-stu-id="b9226-116">**All** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Indeterminate_Error_Counter"></span><span id="indeterminate_error_counter"></span><span id="INDETERMINATE_ERROR_COUNTER"></span>

<span data-ttu-id="b9226-117">**Contador de errores indeterminados** (1)</span><span class="sxs-lookup"><span data-stu-id="b9226-117">**Indeterminate Error Counter** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical_Error_Counter"></span><span id="critical_error_counter"></span><span id="CRITICAL_ERROR_COUNTER"></span>

<span data-ttu-id="b9226-118">**Contador de errores críticos** (2)</span><span class="sxs-lookup"><span data-stu-id="b9226-118">**Critical Error Counter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Major_Error_Counter"></span><span id="major_error_counter"></span><span id="MAJOR_ERROR_COUNTER"></span>

<span data-ttu-id="b9226-119">**Contador de errores principales** (3)</span><span class="sxs-lookup"><span data-stu-id="b9226-119">**Major Error Counter** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Minor_Error_Counter"></span><span id="minor_error_counter"></span><span id="MINOR_ERROR_COUNTER"></span>

<span data-ttu-id="b9226-120">**Contador de errores secundarios** (4)</span><span class="sxs-lookup"><span data-stu-id="b9226-120">**Minor Error Counter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning_Counter"></span><span id="warning_counter"></span><span id="WARNING_COUNTER"></span>

<span data-ttu-id="b9226-121">**Contador de advertencia** (5)</span><span class="sxs-lookup"><span data-stu-id="b9226-121">**Warning Counter** (5)</span></span>


<span data-ttu-id="b9226-122"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b9226-122"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="b9226-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9226-123">Return value</span></span>

<span data-ttu-id="b9226-124">Devuelve 0 (cero) si es correcto, 1 (uno) si no se admite y cualquier otro valor si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="b9226-124">Returns 0 (zero) if successful, 1 (one) if not supported, and any other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9226-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9226-125">Remarks</span></span>

<span data-ttu-id="b9226-126">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="b9226-126">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="b9226-127">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="b9226-127">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="b9226-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="b9226-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b9226-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="b9226-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9226-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9226-130">Requirements</span></span>



| <span data-ttu-id="b9226-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9226-131">Requirement</span></span> | <span data-ttu-id="b9226-132">Value</span><span class="sxs-lookup"><span data-stu-id="b9226-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9226-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9226-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b9226-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9226-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b9226-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9226-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b9226-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9226-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b9226-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b9226-137">Namespace</span></span><br/>                | <span data-ttu-id="b9226-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b9226-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b9226-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b9226-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9226-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9226-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9226-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b9226-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9226-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9226-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9226-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9226-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9226-144">\_DEVICEERRORCOUNTS CIM</span><span class="sxs-lookup"><span data-stu-id="b9226-144">CIM\_DeviceErrorCounts</span></span>](resetcounter-method-in-class-cim-deviceerrorcounts.md)
</dt> <dt>

[<span data-ttu-id="b9226-145">**\_DEVICEERRORCOUNTS CIM**</span><span class="sxs-lookup"><span data-stu-id="b9226-145">**CIM\_DeviceErrorCounts**</span></span>](cim-deviceerrorcounts.md)
</dt> </dl>

 

