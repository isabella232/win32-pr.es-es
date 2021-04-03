---
description: Instala un propietario para el TPM.
ms.assetid: 7b4c8785-0925-41a8-a878-7c1f38d31853
title: Método TakeOwnership de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.TakeOwnership
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: acb0cb03f5e422695623bf6e183d1fd89f63ab60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083298"
---
# <a name="takeownership-method-of-the-win32_tpm-class"></a><span data-ttu-id="1dc09-103">Método TakeOwnership de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="1dc09-103">TakeOwnership method of the Win32\_Tpm class</span></span>

<span data-ttu-id="1dc09-104">El método **TakeOwnerShip** de la clase [**Win32 \_ TPM**](win32-tpm.md) instala un propietario para el TPM.</span><span class="sxs-lookup"><span data-stu-id="1dc09-104">The **TakeOwnership** method of the [**Win32\_Tpm**](win32-tpm.md) class installs an owner for the TPM.</span></span> <span data-ttu-id="1dc09-105">El propietario del TPM puede sacar el máximo partido de las funcionalidades de TPM.</span><span class="sxs-lookup"><span data-stu-id="1dc09-105">The owner of the TPM can make full use of TPM capabilities.</span></span> <span data-ttu-id="1dc09-106">Una vez establecido un propietario, ningún otro usuario o software puede reclamar la propiedad del TPM.</span><span class="sxs-lookup"><span data-stu-id="1dc09-106">After an owner is set, no other user or software can claim ownership of the TPM.</span></span>

<span data-ttu-id="1dc09-107">Los métodos [**IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md)y [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) deben ser verdaderos antes de que el método **TakeOwnerShip** pueda realizarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="1dc09-107">The [**IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md), and [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) methods must all be true before the **TakeOwnership** method can succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dc09-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1dc09-108">Syntax</span></span>


```mof
uint32 TakeOwnership(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="1dc09-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1dc09-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dc09-110">*OwnerAuth* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1dc09-110">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1dc09-111">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="1dc09-111">Type: **string**</span></span>

<span data-ttu-id="1dc09-112">Cadena que identifica el propietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="1dc09-112">A string that identifies the TPM owner.</span></span> <span data-ttu-id="1dc09-113">Esta cadena debe ser una cadena terminada en NULL con codificación Base64 que contenga exactamente 20 bytes de datos binarios.</span><span class="sxs-lookup"><span data-stu-id="1dc09-113">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="1dc09-114">Use el método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una frase de contraseña a este formato esperado.</span><span class="sxs-lookup"><span data-stu-id="1dc09-114">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="1dc09-115">Si no se proporciona ninguno, se lee el parámetro *OwnerAuth* en el registro.</span><span class="sxs-lookup"><span data-stu-id="1dc09-115">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dc09-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1dc09-116">Return value</span></span>

<span data-ttu-id="1dc09-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1dc09-117">Type: **uint32**</span></span>

<span data-ttu-id="1dc09-118">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="1dc09-118">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="1dc09-119">En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="1dc09-119">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="1dc09-120">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1dc09-120">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="1dc09-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="1dc09-121">Description</span></span>                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1dc09-122"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="1dc09-122"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="1dc09-123">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1dc09-123">The method was successful.</span></span><br/>                                                                                                                                                                              |
| <dl> <span data-ttu-id="1dc09-124"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="1dc09-124"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="1dc09-125">El parámetro *OwnerAuth* no es válido.</span><span class="sxs-lookup"><span data-stu-id="1dc09-125">The *OwnerAuth* parameter is not valid.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="1dc09-126"><dt>**TPM \_ E \_ propietario \_ set**</dt> <dt>2150105108 (0x80280014)</dt></span><span class="sxs-lookup"><span data-stu-id="1dc09-126"><dt>**TPM\_E\_OWNER\_SET**</dt> <dt>2150105108 (0x80280014)</dt></span></span> </dl>            | <span data-ttu-id="1dc09-127">Ya existe un propietario en el TPM.</span><span class="sxs-lookup"><span data-stu-id="1dc09-127">An owner already exists on the TPM.</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="1dc09-128"><dt>**TPM \_ E \_ sin \_ aprobación**</dt> <dt>2150105123 (0x80280023)</dt></span><span class="sxs-lookup"><span data-stu-id="1dc09-128"><dt>**TPM\_E\_NO\_ENDORSEMENT**</dt> <dt>2150105123 (0x80280023)</dt></span></span> </dl>       | <span data-ttu-id="1dc09-129">No se puede encontrar ninguna clave de aprobación en el TPM.</span><span class="sxs-lookup"><span data-stu-id="1dc09-129">No endorsement key can be found on the TPM.</span></span><br/> <span data-ttu-id="1dc09-130">Para crear un par de claves de aprobación en el TPM, vea el método [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="1dc09-130">To create an endorsement key pair on the TPM, see the [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) method.</span></span><br/>             |
| <dl> <span data-ttu-id="1dc09-131"><dt>**TPM \_ E \_ instalación \_ deshabilitada**</dt> <dt>2150105099 (0x8028000B)</dt></span><span class="sxs-lookup"><span data-stu-id="1dc09-131"><dt>**TPM\_E\_INSTALL\_DISABLED**</dt> <dt>2150105099 (0x8028000B)</dt></span></span> </dl>     | <span data-ttu-id="1dc09-132">No se puede instalar un propietario en este TPM.</span><span class="sxs-lookup"><span data-stu-id="1dc09-132">An owner cannot be installed on this TPM.</span></span><br/> <span data-ttu-id="1dc09-133">Para obtener información sobre cómo permitir la instalación de un propietario de dispositivo, vea [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md).</span><span class="sxs-lookup"><span data-stu-id="1dc09-133">For information about how to allow installation of a device owner, see [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md).</span></span><br/> |
| <dl> <span data-ttu-id="1dc09-134"><dt>**TPM \_ E \_ defender \_ LOCK \_ Running**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="1dc09-134"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="1dc09-135">El TPM defiende contra los ataques de diccionario y se encuentra en un período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="1dc09-135">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="1dc09-136">Para obtener más información, vea el método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="1dc09-136">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="1dc09-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1dc09-137">Remarks</span></span>

<span data-ttu-id="1dc09-138">Los métodos [**IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md)y [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) deben ser verdaderos antes de que **TakeOwnerShip** pueda realizarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="1dc09-138">The methods [**IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md), and [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) must all be true before **TakeOwnership** can succeed.</span></span>

<span data-ttu-id="1dc09-139">Debe usar el método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para cambiar una frase de contraseña en el valor de entrada que se usa para el parámetro *OwnerAuth* .</span><span class="sxs-lookup"><span data-stu-id="1dc09-139">You should use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to change a passphrase into the input value used for the *OwnerAuth* parameter.</span></span>

<span data-ttu-id="1dc09-140">El método **TakeOwnerShip** realiza una copia de seguridad del valor de autorización de propietario en Active Directory si se ha configurado la configuración de directiva de grupo adecuada.</span><span class="sxs-lookup"><span data-stu-id="1dc09-140">The **TakeOwnership** method backs up the owner authorization value to Active Directory if the appropriate Group Policy settings have been configured.</span></span>

<span data-ttu-id="1dc09-141">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1dc09-141">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1dc09-142">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="1dc09-142">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1dc09-143">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="1dc09-143">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1dc09-144">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="1dc09-144">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1dc09-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dc09-145">Requirements</span></span>



| <span data-ttu-id="1dc09-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dc09-146">Requirement</span></span> | <span data-ttu-id="1dc09-147">Value</span><span class="sxs-lookup"><span data-stu-id="1dc09-147">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc09-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1dc09-148">Minimum supported client</span></span><br/> | <span data-ttu-id="1dc09-149">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1dc09-149">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1dc09-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1dc09-150">Minimum supported server</span></span><br/> | <span data-ttu-id="1dc09-151">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1dc09-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1dc09-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1dc09-152">Namespace</span></span><br/>                | <span data-ttu-id="1dc09-153">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="1dc09-153">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="1dc09-154">MOF</span><span class="sxs-lookup"><span data-stu-id="1dc09-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1dc09-155"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1dc09-155"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="1dc09-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1dc09-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dc09-157"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="1dc09-157"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dc09-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="1dc09-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dc09-159">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="1dc09-159">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
