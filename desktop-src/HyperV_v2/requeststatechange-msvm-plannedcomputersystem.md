---
description: Solicita que el estado del sistema planeado cambie al valor especificado.
ms.assetid: 54ed9514-4f09-458e-8e86-a807ee66df17
title: Método RequestStateChange de la clase Msvm_PlannedComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 172ec383473510a30ccde66b2617e8ef02ffdb72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687471"
---
# <a name="requeststatechange-method-of-the-msvm_plannedcomputersystem-class"></a><span data-ttu-id="11fe5-103">Método RequestStateChange de la \_ clase PlannedComputerSystem de MSVM</span><span class="sxs-lookup"><span data-stu-id="11fe5-103">RequestStateChange method of the Msvm\_PlannedComputerSystem class</span></span>

<span data-ttu-id="11fe5-104">Solicita que el estado del sistema planeado cambie al valor especificado.</span><span class="sxs-lookup"><span data-stu-id="11fe5-104">Requests that the state of the planned system be changed to the value specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="11fe5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11fe5-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="11fe5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11fe5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11fe5-107">*RequestedState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="11fe5-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11fe5-108">Estado solicitado para el sistema planeado.</span><span class="sxs-lookup"><span data-stu-id="11fe5-108">The requested state for the planned system.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="11fe5-109">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="11fe5-109">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="11fe5-110">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="11fe5-110">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="11fe5-111">**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="11fe5-111">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="11fe5-112">**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="11fe5-112">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="11fe5-113">**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="11fe5-113">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="11fe5-114">**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="11fe5-114">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="11fe5-115">Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="11fe5-115">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="11fe5-116">**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="11fe5-116">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="11fe5-117">**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="11fe5-117">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="11fe5-118">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="11fe5-118">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="11fe5-119">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="11fe5-119">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="11fe5-120">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="11fe5-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11fe5-121">Este parámetro no se utiliza y debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="11fe5-121">This parameter is not used and should be **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="11fe5-122">*TimeoutPeriod* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="11fe5-122">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11fe5-123">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="11fe5-123">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11fe5-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11fe5-124">Return value</span></span>

<span data-ttu-id="11fe5-125">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="11fe5-125">This method returns one of the following values.</span></span>



| <span data-ttu-id="11fe5-126">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11fe5-126">Return code/value</span></span>                                                                                                                      | <span data-ttu-id="11fe5-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="11fe5-127">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11fe5-128"><dt></dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="11fe5-128"><dt></dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="11fe5-129">Correcto</span><span class="sxs-lookup"><span data-stu-id="11fe5-129">Success</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="11fe5-130"><dt></dt><dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="11fe5-130"><dt></dt> <dt>4096</dt></span></span> </dl>  |                                                                                    |
| <dl> <span data-ttu-id="11fe5-131"><dt></dt><dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="11fe5-131"><dt></dt> <dt>32768</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="11fe5-132"><dt></dt><dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="11fe5-132"><dt></dt> <dt>32769</dt></span></span> </dl> | <span data-ttu-id="11fe5-133">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="11fe5-133">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="11fe5-134"><dt></dt><dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="11fe5-134"><dt></dt> <dt>32770</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="11fe5-135"><dt></dt><dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="11fe5-135"><dt></dt> <dt>32771</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="11fe5-136"><dt></dt><dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="11fe5-136"><dt></dt> <dt>32772</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="11fe5-137"><dt></dt><dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="11fe5-137"><dt></dt> <dt>32773</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="11fe5-138"><dt></dt><dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="11fe5-138"><dt></dt> <dt>32774</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="11fe5-139"><dt></dt><dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="11fe5-139"><dt></dt> <dt>32775</dt></span></span> </dl> | <span data-ttu-id="11fe5-140">No se admite el valor especificado en el parámetro *RequestedState* .</span><span class="sxs-lookup"><span data-stu-id="11fe5-140">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="11fe5-141"><dt></dt><dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="11fe5-141"><dt></dt> <dt>32776</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="11fe5-142"><dt></dt><dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="11fe5-142"><dt></dt> <dt>32777</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="11fe5-143"><dt></dt><dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="11fe5-143"><dt></dt> <dt>32778</dt></span></span> </dl> |                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="11fe5-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11fe5-144">Requirements</span></span>



| <span data-ttu-id="11fe5-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="11fe5-145">Requirement</span></span> | <span data-ttu-id="11fe5-146">Value</span><span class="sxs-lookup"><span data-stu-id="11fe5-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11fe5-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11fe5-147">Minimum supported client</span></span><br/> | <span data-ttu-id="11fe5-148">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="11fe5-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="11fe5-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11fe5-149">Minimum supported server</span></span><br/> | <span data-ttu-id="11fe5-150">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="11fe5-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="11fe5-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="11fe5-151">Namespace</span></span><br/>                | <span data-ttu-id="11fe5-152">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="11fe5-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="11fe5-153">MOF</span><span class="sxs-lookup"><span data-stu-id="11fe5-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11fe5-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11fe5-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="11fe5-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="11fe5-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11fe5-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="11fe5-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="11fe5-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="11fe5-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11fe5-158">**MSVM \_ PlannedComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="11fe5-158">**Msvm\_PlannedComputerSystem**</span></span>](msvm-plannedcomputersystem.md)
</dt> </dl>

 

 




