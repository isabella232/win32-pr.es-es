---
description: Indica la acción del usuario que se necesita para realizar la operación de presencia física del Módulo de plataforma segura (TPM). Use el método SetPhysicalPresenceRequest para solicitar una operación.
ms.assetid: abbd9702-c3a7-468a-bc83-2b7739d0b7bf
title: Método GetPhysicalPresenceTransition de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceTransition
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 4e6a3ab2295cc26cd439465b569f594dd1e0580a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688152"
---
# <a name="getphysicalpresencetransition-method-of-the-win32_tpm-class"></a><span data-ttu-id="7a97c-104">Método GetPhysicalPresenceTransition de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="7a97c-104">GetPhysicalPresenceTransition method of the Win32\_Tpm class</span></span>

<span data-ttu-id="7a97c-105">El método **GetPhysicalPresenceTransition** de la clase [**Win32 \_ TPM**](win32-tpm.md) indica la acción del usuario que se necesita para realizar la operación de presencia física del módulo de plataforma segura (TPM).</span><span class="sxs-lookup"><span data-stu-id="7a97c-105">The **GetPhysicalPresenceTransition** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates the user action that is needed to perform the Trusted Platform Module (TPM) physical presence operation.</span></span> <span data-ttu-id="7a97c-106">Use el método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar una operación.</span><span class="sxs-lookup"><span data-stu-id="7a97c-106">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span> <span data-ttu-id="7a97c-107">La acción del usuario requerida se establece para el equipo en el momento de la fabricación.</span><span class="sxs-lookup"><span data-stu-id="7a97c-107">The required user action is set for your computer at the time of manufacture.</span></span> <span data-ttu-id="7a97c-108">Normalmente, es necesario reiniciar el equipo.</span><span class="sxs-lookup"><span data-stu-id="7a97c-108">Usually a computer restart is needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a97c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a97c-109">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceTransition(
  [out] uint32 Transition
);
```



## <a name="parameters"></a><span data-ttu-id="7a97c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a97c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a97c-111">*Transición* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7a97c-111">*Transition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a97c-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7a97c-112">Type: **uint32**</span></span>

<span data-ttu-id="7a97c-113">Valor entero que especifica la transición necesaria para realizar una operación de presencia física de TPM.</span><span class="sxs-lookup"><span data-stu-id="7a97c-113">An integer value that specifies the transition needed to perform a TPM physical presence operation.</span></span>



| <span data-ttu-id="7a97c-114">Value</span><span class="sxs-lookup"><span data-stu-id="7a97c-114">Value</span></span>                                                                        | <span data-ttu-id="7a97c-115">Significado</span><span class="sxs-lookup"><span data-stu-id="7a97c-115">Meaning</span></span>                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7a97c-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7a97c-116"><dt>0</dt></span></span> </dl> | <span data-ttu-id="7a97c-117">No se necesita ninguna acción del usuario para realizar una operación de presencia física de TPM.</span><span class="sxs-lookup"><span data-stu-id="7a97c-117">No user action is needed to perform a TPM physical presence operation.</span></span><br/>                                                                                                                                                                              |
| <dl> <span data-ttu-id="7a97c-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7a97c-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="7a97c-119">Para realizar una operación de presencia física de TPM, el usuario debe apagar el equipo y, a continuación, volver a encenderlo con el botón de encendido.</span><span class="sxs-lookup"><span data-stu-id="7a97c-119">To perform a TPM physical presence operation, the user must shutdown the computer and then turn it back on by using the power button.</span></span> <span data-ttu-id="7a97c-120">El usuario debe estar presente físicamente en el equipo para aceptar o rechazar el cambio cuando se lo solicite el BIOS.</span><span class="sxs-lookup"><span data-stu-id="7a97c-120">The user must be physically present at the computer to accept or reject the change when prompted by the BIOS.</span></span><br/> |
| <dl> <span data-ttu-id="7a97c-121"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7a97c-121"><dt>2</dt></span></span> </dl> | <span data-ttu-id="7a97c-122">Para realizar una operación de presencia física de TPM, el usuario debe reiniciar el equipo con un reinicio en caliente.</span><span class="sxs-lookup"><span data-stu-id="7a97c-122">To perform a TPM physical presence operation, the user must restart the computer by using a warm reboot.</span></span> <span data-ttu-id="7a97c-123">El usuario debe estar presente físicamente en el equipo para aceptar o rechazar el cambio cuando se lo solicite el BIOS.</span><span class="sxs-lookup"><span data-stu-id="7a97c-123">The user must be physically present at the computer to accept or reject the change when prompted by the BIOS.</span></span><br/>                              |
| <dl> <span data-ttu-id="7a97c-124"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7a97c-124"><dt>3</dt></span></span> </dl> | <span data-ttu-id="7a97c-125">Se desconoce la acción del usuario requerida.</span><span class="sxs-lookup"><span data-stu-id="7a97c-125">The required user action is unknown.</span></span><br/>                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a97c-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a97c-126">Return value</span></span>

<span data-ttu-id="7a97c-127">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7a97c-127">Type: **uint32**</span></span>

<span data-ttu-id="7a97c-128">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="7a97c-128">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="7a97c-129">En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="7a97c-129">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="7a97c-130">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a97c-130">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="7a97c-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a97c-131">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7a97c-132"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="7a97c-132"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="7a97c-133">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7a97c-133">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="7a97c-134"><dt>**TPM \_ E \_ PPI \_ ACPI \_ error**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="7a97c-134"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="7a97c-135">Error de hardware.</span><span class="sxs-lookup"><span data-stu-id="7a97c-135">A hardware failure occurred.</span></span> <span data-ttu-id="7a97c-136">Consulte al fabricante del equipo para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="7a97c-136">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7a97c-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a97c-137">Remarks</span></span>

<span data-ttu-id="7a97c-138">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7a97c-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7a97c-139">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7a97c-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7a97c-140">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="7a97c-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7a97c-141">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7a97c-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a97c-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a97c-142">Requirements</span></span>



| <span data-ttu-id="7a97c-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a97c-143">Requirement</span></span> | <span data-ttu-id="7a97c-144">Value</span><span class="sxs-lookup"><span data-stu-id="7a97c-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a97c-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a97c-145">Minimum supported client</span></span><br/> | <span data-ttu-id="7a97c-146">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7a97c-146">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7a97c-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a97c-147">Minimum supported server</span></span><br/> | <span data-ttu-id="7a97c-148">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7a97c-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7a97c-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7a97c-149">Namespace</span></span><br/>                | <span data-ttu-id="7a97c-150">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="7a97c-150">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="7a97c-151">MOF</span><span class="sxs-lookup"><span data-stu-id="7a97c-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a97c-152"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a97c-152"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a97c-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7a97c-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a97c-154"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="7a97c-154"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a97c-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a97c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a97c-156">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="7a97c-156">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="7a97c-157">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="7a97c-157">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
