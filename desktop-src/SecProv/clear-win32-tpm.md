---
description: Restablece el TPM a su estado predeterminado de fábrica.
ms.assetid: 55d6702f-bd57-43e3-b790-617940dd2e01
title: Método Clear de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Clear
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cf75a8af6764e542cecd9bd296c1b1511c4f4513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278232"
---
# <a name="clear-method-of-the-win32_tpm-class"></a><span data-ttu-id="7f3a4-103">Método Clear de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="7f3a4-103">Clear method of the Win32\_Tpm class</span></span>

<span data-ttu-id="7f3a4-104">El método **Clear** de la clase [**Win32 \_ TPM**](win32-tpm.md) restablece el TPM a su estado predeterminado de fábrica.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-104">The **Clear** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the TPM to its factory-default state.</span></span> <span data-ttu-id="7f3a4-105">Un propietario de TPM puede utilizar este método para cancelar la propiedad de TPM e invalidar los materiales criptográficos creados por el propietario anterior.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-105">A TPM owner can use this method to cancel TPM ownership and invalidate cryptographic materials created by the previous owner.</span></span> <span data-ttu-id="7f3a4-106">Este método suspende BitLocker si la llamada puede hacer que se requiera la recuperación de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-106">This method suspends BitLocker if calling could cause BitLocker recovery to be required.</span></span> <span data-ttu-id="7f3a4-107">BitLocker se reanudará automáticamente una vez que se haya aprovisionado TPM.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-107">BitLocker would automatically resume once TPM has been provisioned.</span></span>

> [!Caution]  
> <span data-ttu-id="7f3a4-108">Al borrar el TPM, se perderán todas las claves de TPM creadas y usadas por las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-108">By clearing the TPM, you will lose all TPM keys created and used by applications.</span></span> <span data-ttu-id="7f3a4-109">Si estas claves se usaron para cifrar datos, asegúrese de que tiene otra manera de obtener acceso a los datos antes de borrar el TPM.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-109">If these keys were used to encrypt data, ensure that you have another way to access the data before clearing the TPM.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7f3a4-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f3a4-110">Syntax</span></span>


```mof
uint32 Clear(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="7f3a4-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f3a4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f3a4-112">*OwnerAuth* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7f3a4-112">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7f3a4-113">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="7f3a4-113">Type: **string**</span></span>

<span data-ttu-id="7f3a4-114">Cadena que identifica el propietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-114">A string that identifies the TPM owner.</span></span> <span data-ttu-id="7f3a4-115">Esta cadena debe ser una cadena codificada en Base64 que contenga exactamente 20 bytes de datos binarios.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-115">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="7f3a4-116">Use el método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una frase de contraseña a este formato esperado.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-116">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="7f3a4-117">Si no se proporciona ninguno, se lee el parámetro *OwnerAuth* en el registro.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-117">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f3a4-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f3a4-118">Return value</span></span>

<span data-ttu-id="7f3a4-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f3a4-119">Type: **uint32**</span></span>

<span data-ttu-id="7f3a4-120">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-120">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="7f3a4-121">En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-121">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="7f3a4-122">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f3a4-122">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="7f3a4-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="7f3a4-123">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f3a4-124"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="7f3a4-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="7f3a4-125">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-125">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="7f3a4-126"><dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="7f3a4-126"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="7f3a4-127">El valor de autorización de propietario proporcionado no puede realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-127">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="7f3a4-128"><dt>**TPM \_ E \_ defender \_ LOCK \_ Running**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="7f3a4-128"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="7f3a4-129">El TPM defiende contra los ataques de diccionario y se encuentra en un período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-129">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="7f3a4-130">Para obtener más información, vea el método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="7f3a4-130">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7f3a4-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f3a4-131">Remarks</span></span>

<span data-ttu-id="7f3a4-132">Ejecutar este método puede ayudar a preparar un equipo equipado con TPM para el reciclaje.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-132">Running this method can help prepare a TPM-equipped computer for recycling.</span></span>

<span data-ttu-id="7f3a4-133">Para borrar el TPM pero ya no tiene la autorización de propietario del TPM, necesita acceso físico al equipo.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-133">To clear the TPM but no longer have the TPM owner authorization, you need physical access to the computer.</span></span> <span data-ttu-id="7f3a4-134">El método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) incluye funcionalidad que ayuda a borrar el TPM sin la autorización de propietario de TPM.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-134">The [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method includes functionality to help clear the TPM without TPM owner authorization.</span></span>

<span data-ttu-id="7f3a4-135">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7f3a4-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7f3a4-136">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-136">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7f3a4-137">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7f3a4-138">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7f3a4-138">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f3a4-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f3a4-139">Requirements</span></span>



| <span data-ttu-id="7f3a4-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f3a4-140">Requirement</span></span> | <span data-ttu-id="7f3a4-141">Value</span><span class="sxs-lookup"><span data-stu-id="7f3a4-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f3a4-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f3a4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7f3a4-143">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7f3a4-143">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7f3a4-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f3a4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7f3a4-145">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7f3a4-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7f3a4-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7f3a4-146">Namespace</span></span><br/>                | <span data-ttu-id="7f3a4-147">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="7f3a4-147">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="7f3a4-148">MOF</span><span class="sxs-lookup"><span data-stu-id="7f3a4-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f3a4-149"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f3a4-149"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f3a4-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7f3a4-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f3a4-151"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="7f3a4-151"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f3a4-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f3a4-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f3a4-153">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="7f3a4-153">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
