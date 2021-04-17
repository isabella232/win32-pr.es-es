---
description: El método IsEnabled de la \_ clase Win32 TPM indica si el dispositivo está habilitado. Este valor se puede cambiar mediante los métodos enable y Disable.
ms.assetid: e1d5513f-33eb-49e3-9582-d6c103ca5d03
title: Método IsEnabled de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d808bb68e53b1a24ff668d1b7a9680b5d57b5e9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686642"
---
# <a name="isenabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="52aca-104">Método IsEnabled de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="52aca-104">IsEnabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="52aca-105">El método **IsEnabled** de la clase [**Win32 \_ TPM**](win32-tpm.md) indica si el dispositivo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="52aca-105">The **IsEnabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device is enabled.</span></span> <span data-ttu-id="52aca-106">Este valor se puede cambiar mediante los métodos [**enable**](enable-win32-tpm.md) y [**Disable**](disable-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="52aca-106">This value can be changed by the [**Enable**](enable-win32-tpm.md) and [**Disable**](disable-win32-tpm.md) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="52aca-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52aca-107">Syntax</span></span>


```mof
uint32 IsEnabled(
  [out] boolean IsEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="52aca-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52aca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52aca-109">*IsEnabled* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="52aca-109">*IsEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52aca-110">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="52aca-110">Type: **boolean**</span></span>

<span data-ttu-id="52aca-111">Si es **true**, el dispositivo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="52aca-111">If **true**, the device is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52aca-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52aca-112">Return value</span></span>

<span data-ttu-id="52aca-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52aca-113">Type: **uint32**</span></span>

<span data-ttu-id="52aca-114">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="52aca-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="52aca-115">A continuación se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="52aca-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="52aca-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52aca-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="52aca-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="52aca-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="52aca-118"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="52aca-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="52aca-119">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="52aca-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="52aca-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52aca-120">Remarks</span></span>

<span data-ttu-id="52aca-121">Según la especificación de Trusted Computing Group (TCG) v 1.2, solo están disponibles los siguientes comandos cuando el dispositivo está en un estado desactivado.</span><span class="sxs-lookup"><span data-stu-id="52aca-121">According to the Trusted Computing Group (TCG) v1.2 specification only the following commands are available when the device is in a deactivated state.</span></span>

-   <span data-ttu-id="52aca-122">ContinueSelfTest de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-122">TPM\_ContinueSelfTest</span></span>
-   <span data-ttu-id="52aca-123">DSAP de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-123">TPM\_DSAP</span></span>
-   <span data-ttu-id="52aca-124">FlushSpecific de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-124">TPM\_FlushSpecific</span></span>
-   <span data-ttu-id="52aca-125">GetCapability de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-125">TPM\_GetCapability</span></span>
-   <span data-ttu-id="52aca-126">GetTestResult de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-126">TPM\_GetTestResult</span></span>
-   <span data-ttu-id="52aca-127">\_Inicialización de TPM</span><span class="sxs-lookup"><span data-stu-id="52aca-127">TPM\_Init</span></span>
-   <span data-ttu-id="52aca-128">OIAP de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-128">TPM\_OIAP</span></span>
-   <span data-ttu-id="52aca-129">OSAP de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-129">TPM\_OSAP</span></span>
-   <span data-ttu-id="52aca-130">OwnerSetDisable de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-130">TPM\_OwnerSetDisable</span></span>
-   <span data-ttu-id="52aca-131">\_Restablecimiento de PCR de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-131">TPM\_PCR\_Reset</span></span>
-   <span data-ttu-id="52aca-132">PhysicalDisable de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-132">TPM\_PhysicalDisable</span></span>
-   <span data-ttu-id="52aca-133">PhysicalEnable de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-133">TPM\_PhysicalEnable</span></span>
-   <span data-ttu-id="52aca-134">PhysicalSetDeactivated de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-134">TPM\_PhysicalSetDeactivated</span></span>
-   <span data-ttu-id="52aca-135">Restablecimiento de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-135">TPM\_Reset</span></span>
-   <span data-ttu-id="52aca-136">\_Savesta TPM</span><span class="sxs-lookup"><span data-stu-id="52aca-136">TPM\_SaveState</span></span>
-   <span data-ttu-id="52aca-137">SelfTestFull de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-137">TPM\_SelfTestFull</span></span>
-   <span data-ttu-id="52aca-138">SetCapability de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-138">TPM\_SetCapability</span></span>
-   <span data-ttu-id="52aca-139">SHA1Complete de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-139">TPM\_SHA1Complete</span></span>
-   <span data-ttu-id="52aca-140">SHA1Start de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-140">TPM\_SHA1Start</span></span>
-   <span data-ttu-id="52aca-141">SHA1Update de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-141">TPM\_SHA1Update</span></span>
-   <span data-ttu-id="52aca-142">Inicio de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-142">TPM\_Startup</span></span>
-   <span data-ttu-id="52aca-143">TakeOwnerShip de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-143">TPM\_TakeOwnership</span></span>
-   <span data-ttu-id="52aca-144">\_Identificador de finalización de TPM \_</span><span class="sxs-lookup"><span data-stu-id="52aca-144">TPM\_Terminate\_Handle</span></span>

<span data-ttu-id="52aca-145">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="52aca-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="52aca-146">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="52aca-146">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="52aca-147">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="52aca-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="52aca-148">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="52aca-148">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52aca-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52aca-149">Requirements</span></span>



| <span data-ttu-id="52aca-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="52aca-150">Requirement</span></span> | <span data-ttu-id="52aca-151">Value</span><span class="sxs-lookup"><span data-stu-id="52aca-151">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="52aca-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52aca-152">Minimum supported client</span></span><br/> | <span data-ttu-id="52aca-153">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="52aca-153">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="52aca-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52aca-154">Minimum supported server</span></span><br/> | <span data-ttu-id="52aca-155">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="52aca-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="52aca-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="52aca-156">Namespace</span></span><br/>                | <span data-ttu-id="52aca-157">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="52aca-157">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="52aca-158">MOF</span><span class="sxs-lookup"><span data-stu-id="52aca-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52aca-159"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52aca-159"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="52aca-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52aca-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52aca-161"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="52aca-161"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52aca-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="52aca-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52aca-163">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="52aca-163">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="52aca-164">**Disable**</span><span class="sxs-lookup"><span data-stu-id="52aca-164">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="52aca-165">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="52aca-165">**Enable**</span></span>](enable-win32-tpm.md)
</dt> </dl>

 

 
