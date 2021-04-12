---
description: El método IsActivated de la clase de Win32 \_ TPM indica si el dispositivo está activado.
ms.assetid: 862c386c-c5b5-44d2-89a5-3735b99bf8bc
title: Método IsActivated de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsActivated
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6482163a27f211b4f4ce24284a8339f2b7254f3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278230"
---
# <a name="isactivated-method-of-the-win32_tpm-class"></a><span data-ttu-id="ecbd8-103">Método IsActivated de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="ecbd8-103">IsActivated method of the Win32\_Tpm class</span></span>

<span data-ttu-id="ecbd8-104">El método **IsActivated** de la clase de [**Win32 \_ TPM**](win32-tpm.md) indica si el dispositivo está activado.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-104">The **IsActivated** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecbd8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ecbd8-105">Syntax</span></span>


```mof
uint32 IsActivated(
  [out] boolean IsActivated
);
```



## <a name="parameters"></a><span data-ttu-id="ecbd8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ecbd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecbd8-107">*IsActivated* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ecbd8-107">*IsActivated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecbd8-108">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ecbd8-108">Type: **boolean**</span></span>

<span data-ttu-id="ecbd8-109">Si es **true**, el dispositivo está activado.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-109">If **true**, the device is activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecbd8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ecbd8-110">Return value</span></span>

<span data-ttu-id="ecbd8-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ecbd8-111">Type: **uint32**</span></span>

<span data-ttu-id="ecbd8-112">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="ecbd8-113">A continuación se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="ecbd8-114">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ecbd8-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="ecbd8-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="ecbd8-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ecbd8-116"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="ecbd8-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="ecbd8-117">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ecbd8-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ecbd8-118">Remarks</span></span>

<span data-ttu-id="ecbd8-119">La desactivación es similar a deshabilitada, pero se pueden realizar cambios de estado operativo.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-119">Deactivation is similar to disabled, but operational state changes are possible.</span></span> <span data-ttu-id="ecbd8-120">Según la especificación de Trusted Computing Group (TCG) v 1.2, solo están disponibles los siguientes comandos cuando el dispositivo está en un estado desactivado.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-120">According to the Trusted Computing Group (TCG) v1.2 specification only the following commands are available when the device is in a deactivated state.</span></span>

-   <span data-ttu-id="ecbd8-121">ContinueSelfTest de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-121">TPM\_ContinueSelfTest</span></span>
-   <span data-ttu-id="ecbd8-122">DSAP de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-122">TPM\_DSAP</span></span>
-   <span data-ttu-id="ecbd8-123">FlushSpecific de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-123">TPM\_FlushSpecific</span></span>
-   <span data-ttu-id="ecbd8-124">GetCapability de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-124">TPM\_GetCapability</span></span>
-   <span data-ttu-id="ecbd8-125">GetTestResult de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-125">TPM\_GetTestResult</span></span>
-   <span data-ttu-id="ecbd8-126">\_Inicialización de TPM</span><span class="sxs-lookup"><span data-stu-id="ecbd8-126">TPM\_Init</span></span>
-   <span data-ttu-id="ecbd8-127">OIAP de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-127">TPM\_OIAP</span></span>
-   <span data-ttu-id="ecbd8-128">OSAP de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-128">TPM\_OSAP</span></span>
-   <span data-ttu-id="ecbd8-129">OwnerSetDisable de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-129">TPM\_OwnerSetDisable</span></span>
-   <span data-ttu-id="ecbd8-130">\_Restablecimiento de PCR de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-130">TPM\_PCR\_Reset</span></span>
-   <span data-ttu-id="ecbd8-131">PhysicalDisable de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-131">TPM\_PhysicalDisable</span></span>
-   <span data-ttu-id="ecbd8-132">PhysicalEnable de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-132">TPM\_PhysicalEnable</span></span>
-   <span data-ttu-id="ecbd8-133">PhysicalSetDeactivated de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-133">TPM\_PhysicalSetDeactivated</span></span>
-   <span data-ttu-id="ecbd8-134">Restablecimiento de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-134">TPM\_Reset</span></span>
-   <span data-ttu-id="ecbd8-135">\_Savesta TPM</span><span class="sxs-lookup"><span data-stu-id="ecbd8-135">TPM\_SaveState</span></span>
-   <span data-ttu-id="ecbd8-136">SelfTestFull de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-136">TPM\_SelfTestFull</span></span>
-   <span data-ttu-id="ecbd8-137">SetCapability de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-137">TPM\_SetCapability</span></span>
-   <span data-ttu-id="ecbd8-138">SHA1Complete de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-138">TPM\_SHA1Complete</span></span>
-   <span data-ttu-id="ecbd8-139">SHA1Start de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-139">TPM\_SHA1Start</span></span>
-   <span data-ttu-id="ecbd8-140">SHA1Update de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-140">TPM\_SHA1Update</span></span>
-   <span data-ttu-id="ecbd8-141">Inicio de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-141">TPM\_Startup</span></span>
-   <span data-ttu-id="ecbd8-142">TakeOwnerShip de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-142">TPM\_TakeOwnership</span></span>
-   <span data-ttu-id="ecbd8-143">\_Identificador de finalización de TPM \_</span><span class="sxs-lookup"><span data-stu-id="ecbd8-143">TPM\_Terminate\_Handle</span></span>

<span data-ttu-id="ecbd8-144">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ecbd8-144">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ecbd8-145">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-145">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ecbd8-146">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-146">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ecbd8-147">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="ecbd8-147">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ecbd8-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecbd8-148">Requirements</span></span>



| <span data-ttu-id="ecbd8-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecbd8-149">Requirement</span></span> | <span data-ttu-id="ecbd8-150">Value</span><span class="sxs-lookup"><span data-stu-id="ecbd8-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecbd8-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecbd8-151">Minimum supported client</span></span><br/> | <span data-ttu-id="ecbd8-152">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ecbd8-152">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ecbd8-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecbd8-153">Minimum supported server</span></span><br/> | <span data-ttu-id="ecbd8-154">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ecbd8-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ecbd8-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ecbd8-155">Namespace</span></span><br/>                | <span data-ttu-id="ecbd8-156">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="ecbd8-156">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="ecbd8-157">MOF</span><span class="sxs-lookup"><span data-stu-id="ecbd8-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ecbd8-158"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ecbd8-158"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="ecbd8-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ecbd8-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecbd8-160"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="ecbd8-160"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecbd8-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecbd8-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecbd8-162">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="ecbd8-162">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
