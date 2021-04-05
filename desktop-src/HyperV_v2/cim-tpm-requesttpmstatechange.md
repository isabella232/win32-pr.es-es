---
description: Solicita que el estado del TPM cambie al valor especificado en el parámetro RequestedTPMState.
ms.assetid: 7ad8bf4e-6263-45d5-8f33-fb842bbf1f1a
title: Método RequestTPMStateChange de la clase CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.RequestTPMStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 39bded1a43dd547780c3924f3af9c37cfc79aa1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001620"
---
# <a name="requesttpmstatechange-method-of-the-cim_tpm-class"></a><span data-ttu-id="81920-103">Método RequestTPMStateChange de la \_ clase TPM CIM</span><span class="sxs-lookup"><span data-stu-id="81920-103">RequestTPMStateChange method of the CIM\_TPM class</span></span>

<span data-ttu-id="81920-104">Solicita que el estado del TPM cambie al valor especificado en el parámetro *RequestedTPMState* .</span><span class="sxs-lookup"><span data-stu-id="81920-104">Requests that the state of the TPM be changed to the value specified in the *RequestedTPMState* parameter.</span></span> <span data-ttu-id="81920-105">Si la invocación del método se completa correctamente, la propiedad **TPMState** debe ser igual al parámetro **RequestedTPMState** .</span><span class="sxs-lookup"><span data-stu-id="81920-105">If the method invocation completes successfully, the **TPMState** property shall be equal to the **RequestedTPMState** parameter.</span></span> <span data-ttu-id="81920-106">Invocar varias veces al método **RequestTPMStateChange** podría provocar que se sobrescriban o se pierdan solicitudes anteriores.</span><span class="sxs-lookup"><span data-stu-id="81920-106">Invoking the **RequestTPMStateChange** method multiple times could result in earlier requests being overwritten or lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="81920-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81920-107">Syntax</span></span>


```mof
uint32 RequestTPMStateChange(
  [in]  uint16              RequestedTPMState,
  [in]  string              AuthorizationToken,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="81920-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81920-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81920-109">*RequestedTPMState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="81920-109">*RequestedTPMState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81920-110">Estados de TPM solicitados.</span><span class="sxs-lookup"><span data-stu-id="81920-110">The requested TPM states.</span></span>

<dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="81920-111">**S1 habilitada: propiedad activa** (2)</span><span class="sxs-lookup"><span data-stu-id="81920-111">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="81920-112">**S2 deshabilitado-propiedad activa** (3)</span><span class="sxs-lookup"><span data-stu-id="81920-112">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="81920-113">**S3 habilitado: inactivo-propiedad** (4)</span><span class="sxs-lookup"><span data-stu-id="81920-113">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="81920-114">**S4 deshabilitado-inactivo-propiedad** (5)</span><span class="sxs-lookup"><span data-stu-id="81920-114">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="81920-115">**S5 habilitado-activo-no propietario** (6)</span><span class="sxs-lookup"><span data-stu-id="81920-115">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="81920-116">**S6 deshabilitado-activo-no propietario** (7)</span><span class="sxs-lookup"><span data-stu-id="81920-116">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="81920-117">**S7 habilitado: inactivo:** no tiene propiedad (8)</span><span class="sxs-lookup"><span data-stu-id="81920-117">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="81920-118">**S8 deshabilitado-inactivo:** no tiene propiedad (9)</span><span class="sxs-lookup"><span data-stu-id="81920-118">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="81920-119">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="81920-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="81920-120">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="81920-120">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="81920-121">*AuthorizationToken* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="81920-121">*AuthorizationToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81920-122">Token de autorización que puede ser necesario para que la acción surta efecto.</span><span class="sxs-lookup"><span data-stu-id="81920-122">Authorization token that may be required for the action to take effect.</span></span> <span data-ttu-id="81920-123">El parámetro *AuthorizationToken* puede ser necesario para establecer la presencia física o para pasar OwnerAuth, la contraseña de autorización de propietario definida por TCG.</span><span class="sxs-lookup"><span data-stu-id="81920-123">The *AuthorizationToken* parameter may be required to establish Physical Presence, or to pass the OwnerAuth, the TCG defined owner authorization password.</span></span> <span data-ttu-id="81920-124">En el caso de OwnerAuth, \_ es posible que se requiera el SharedCredential de CIM con un valor que no sea NULL de CIM \_ SharedCredential. Secret.</span><span class="sxs-lookup"><span data-stu-id="81920-124">In the case of OwnerAuth, the CIM\_SharedCredential with non-null value of the CIM\_SharedCredential.Secret may be required.</span></span> <span data-ttu-id="81920-125">La \_ propiedad CIM SharedCredential. algorithm también se puede especificar en función de la propiedad CIM \_ TPMCapabilities. SupportedPasswordAlgorithms.</span><span class="sxs-lookup"><span data-stu-id="81920-125">The CIM\_SharedCredential.Algorithm property may also be specified based on the property CIM\_TPMCapabilities.SupportedPasswordAlgorithms.</span></span>

</dd> <dt>

<span data-ttu-id="81920-126">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="81920-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81920-127">Puede contener una referencia al [**\_ ConcreteJob de CIM**](cim-concretejob.md) creado para realizar el seguimiento de la transición de estado iniciada por la invocación del método.</span><span class="sxs-lookup"><span data-stu-id="81920-127">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="81920-128">*TimeoutPeriod* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="81920-128">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81920-129">Un período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se realice la transición al nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="81920-129">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="81920-130">El formato de intervalo debe usarse para especificar el *TimeoutPeriod*.</span><span class="sxs-lookup"><span data-stu-id="81920-130">The interval format must be used to specify the *TimeoutPeriod*.</span></span> <span data-ttu-id="81920-131">Un valor de 0 o un parámetro null indica que el cliente no tiene ningún requisito de tiempo para la transición.</span><span class="sxs-lookup"><span data-stu-id="81920-131">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81920-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81920-132">Return value</span></span>

<span data-ttu-id="81920-133">Si se ejecuta correctamente, devuelve 0 o 4096; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="81920-133">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="81920-134">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="81920-134">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81920-135">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="81920-135">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="81920-136">**Error desconocido o no especificado** (2)</span><span class="sxs-lookup"><span data-stu-id="81920-136">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81920-137">**No se puede completar en el período de tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="81920-137">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81920-138">**Error** (4)</span><span class="sxs-lookup"><span data-stu-id="81920-138">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="81920-139">**Parámetro no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="81920-139">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="81920-140">**En uso** (6)</span><span class="sxs-lookup"><span data-stu-id="81920-140">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="81920-141">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="81920-141">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="81920-142">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="81920-142">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="81920-143">**Transición de estado no válida** (4097)</span><span class="sxs-lookup"><span data-stu-id="81920-143">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="81920-144">**No se admite el uso de parámetros de tiempo de espera** (4098)</span><span class="sxs-lookup"><span data-stu-id="81920-144">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="81920-145">**Ocupado** (4099)</span><span class="sxs-lookup"><span data-stu-id="81920-145">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="81920-146">**Método reservado** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="81920-146">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="81920-147">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="81920-147">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="81920-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81920-148">Requirements</span></span>



| <span data-ttu-id="81920-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="81920-149">Requirement</span></span> | <span data-ttu-id="81920-150">Value</span><span class="sxs-lookup"><span data-stu-id="81920-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81920-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81920-151">Minimum supported client</span></span><br/> | <span data-ttu-id="81920-152">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="81920-152">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="81920-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81920-153">Minimum supported server</span></span><br/> | <span data-ttu-id="81920-154">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="81920-154">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="81920-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="81920-155">Namespace</span></span><br/>                | <span data-ttu-id="81920-156">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="81920-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="81920-157">MOF</span><span class="sxs-lookup"><span data-stu-id="81920-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81920-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81920-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81920-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="81920-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81920-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81920-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="81920-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="81920-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81920-162">**TPM de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="81920-162">**CIM\_TPM**</span></span>](cim-tpm.md)
</dt> </dl>

 

 




