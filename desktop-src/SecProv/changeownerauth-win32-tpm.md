---
description: Cambia el valor de autorización de propietario de TPM.
ms.assetid: ed280037-2360-4889-baba-cfa9e4fd473e
title: Método ChangeOwnerAuth de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ChangeOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: fc4b044d58dcaca5364f0ba669b09030cf3b34dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154067"
---
# <a name="changeownerauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="f8f3f-103">Método ChangeOwnerAuth de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="f8f3f-103">ChangeOwnerAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="f8f3f-104">El método **ChangeOwnerAuth** de la clase [**Win32 \_ TPM**](win32-tpm.md) cambia el valor de autorización de propietario de TPM.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-104">The **ChangeOwnerAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class changes the TPM owner authorization value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8f3f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8f3f-105">Syntax</span></span>


```mof
uint32 ChangeOwnerAuth(
  [in, optional] string OldOwnerAuth,
  [in, optional] string NewOwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="f8f3f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8f3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8f3f-107">*OldOwnerAuth* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f8f3f-107">*OldOwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f8f3f-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="f8f3f-108">Type: **string**</span></span>

<span data-ttu-id="f8f3f-109">Cadena que nombra el valor de autorización de propietario del TPM actual del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-109">A string that names the current TPM owner authorization value of the device.</span></span> <span data-ttu-id="f8f3f-110">Use el método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una contraseña a este valor de autorización.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-110">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a password to this authorization value.</span></span> <span data-ttu-id="f8f3f-111">No se proporciona el parámetro *OldOwnerAuth* o se proporciona una cadena vacía, este método obtiene el valor del registro, si está presente.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-111">The *OldOwnerAuth* parameter is not supplied or an empty string is provided, this method gets the value from the registry if present.</span></span>

</dd> <dt>

<span data-ttu-id="f8f3f-112">*NewOwnerAuth* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f8f3f-112">*NewOwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f8f3f-113">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="f8f3f-113">Type: **string**</span></span>

<span data-ttu-id="f8f3f-114">Cadena que nombra el nuevo valor de autorización de propietario de TPM.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-114">A string that names the new TPM owner authorization value.</span></span> <span data-ttu-id="f8f3f-115">Use el método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una contraseña a este valor de autorización.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-115">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a password to this authorization value.</span></span> <span data-ttu-id="f8f3f-116">El parámetro *NewOwnerAuth* no puede estar vacío ni ser **nulo.**</span><span class="sxs-lookup"><span data-stu-id="f8f3f-116">The *NewOwnerAuth* parameter cannot be empty or **NULL.**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8f3f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8f3f-117">Return value</span></span>

<span data-ttu-id="f8f3f-118">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f8f3f-118">Type: **uint32**</span></span>

<span data-ttu-id="f8f3f-119">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-119">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="f8f3f-120">En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-120">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="f8f3f-121">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8f3f-121">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="f8f3f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8f3f-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8f3f-123"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="f8f3f-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                              | <span data-ttu-id="f8f3f-124">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="f8f3f-125"><dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="f8f3f-125"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>                   | <span data-ttu-id="f8f3f-126">El valor de autorización de propietario del TPM actual no es correcto.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-126">The current TPM owner authorization value is incorrect.</span></span><br/>                                                                                                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="f8f3f-127"><dt>**TPM \_ E \_ defender \_ LOCK \_ Running**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="f8f3f-127"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl>      | <span data-ttu-id="f8f3f-128">El TPM defiende contra los ataques de diccionario y se encuentra en un período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-128">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="f8f3f-129">Para obtener más información, vea el método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="f8f3f-129">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/>                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="f8f3f-130"><dt>**FVE \_ \_No se \_ \_ ha \_ instalado el esquema de ad**</dt> <dt>2150694922 (0x8031000A)</dt></span><span class="sxs-lookup"><span data-stu-id="f8f3f-130"><dt>**FVE\_E\_AD\_SCHEMA\_NOT\_INSTALLED**</dt> <dt>2150694922 (0x8031000A)</dt></span></span> </dl> | <span data-ttu-id="f8f3f-131">No se puede guardar la información de recuperación en la red.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-131">Cannot save recovery information to the network.</span></span> <span data-ttu-id="f8f3f-132">El equipo se ha configurado para almacenar información de recuperación en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-132">The computer has been configured to store recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="f8f3f-133">Para obtener instrucciones sobre cómo configurar Active Directory, consulte [Guía de configuración de cifrado de unidad BitLocker: copia de seguridad de la información de recuperación de BitLocker y TPM en Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="f8f3f-133">For instructions on how to set up Active Directory, see [BitLocker Drive Encryption Configuration Guide: Backing Up BitLocker and TPM Recovery Information to Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10)).</span></span><br/> |
| <dl> <span data-ttu-id="f8f3f-134"><dt>**Error de conexión**</dt> <dt>2147943755 (0x8007054B)</dt></span><span class="sxs-lookup"><span data-stu-id="f8f3f-134"><dt>**Connection Failed**</dt> <dt>2147943755 (0x8007054B)</dt></span></span> </dl>                  | <span data-ttu-id="f8f3f-135">No se puede guardar la información de recuperación en la red.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-135">Cannot save recovery information to the network.</span></span> <span data-ttu-id="f8f3f-136">El equipo se ha configurado para almacenar información de recuperación en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-136">The computer has been configured to store recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="f8f3f-137">Se necesita una conexión de red para continuar.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-137">A network connection is required to continue.</span></span><br/>                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="f8f3f-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8f3f-138">Remarks</span></span>

<span data-ttu-id="f8f3f-139">El método **ChangeOwnerAuth** realiza una copia de seguridad de la nueva autorización de propietario de TPM en Active Directory Domain Services si se ha configurado la configuración de directiva de grupo adecuada.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-139">The **ChangeOwnerAuth** method backs up the new TPM owner authorization to Active Directory Domain Services if the appropriate Group Policy settings have been configured.</span></span>

<span data-ttu-id="f8f3f-140">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f8f3f-140">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f8f3f-141">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-141">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f8f3f-142">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="f8f3f-142">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f8f3f-143">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f8f3f-143">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8f3f-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8f3f-144">Requirements</span></span>



| <span data-ttu-id="f8f3f-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8f3f-145">Requirement</span></span> | <span data-ttu-id="f8f3f-146">Value</span><span class="sxs-lookup"><span data-stu-id="f8f3f-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f3f-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8f3f-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f8f3f-148">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f8f3f-148">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f8f3f-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8f3f-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f8f3f-150">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f8f3f-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f8f3f-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f8f3f-151">Namespace</span></span><br/>                | <span data-ttu-id="f8f3f-152">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="f8f3f-152">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="f8f3f-153">MOF</span><span class="sxs-lookup"><span data-stu-id="f8f3f-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8f3f-154"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8f3f-154"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8f3f-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f8f3f-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8f3f-156"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="f8f3f-156"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8f3f-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8f3f-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8f3f-158">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="f8f3f-158">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
