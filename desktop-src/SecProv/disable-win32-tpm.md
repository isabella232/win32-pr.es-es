---
description: Permite al propietario del TPM deshabilitar o suspender TPM.
ms.assetid: d910334d-6da6-423d-ae8d-6e86f300dd52
title: Método Disable de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Disable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 32012c338646ce11c96d2657233642808fdcdaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686660"
---
# <a name="disable-method-of-the-win32_tpm-class"></a><span data-ttu-id="e37b8-103">Método Disable de la \_ clase TPM de Win32</span><span class="sxs-lookup"><span data-stu-id="e37b8-103">Disable method of the Win32\_Tpm class</span></span>

<span data-ttu-id="e37b8-104">El método **Disable** de la clase [**Win32 \_ TPM**](win32-tpm.md) permite que el propietario del TPM deshabilite o suspenda el TPM.</span><span class="sxs-lookup"><span data-stu-id="e37b8-104">The **Disable** method of the [**Win32\_Tpm**](win32-tpm.md) class allows the TPM owner to disable or suspend the TPM.</span></span> <span data-ttu-id="e37b8-105">Este método suspende BitLocker si la llamada puede hacer que se requiera la recuperación de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e37b8-105">This method suspends BitLocker if calling could cause BitLocker recovery to be required.</span></span> <span data-ttu-id="e37b8-106">BitLocker se reanudará automáticamente una vez que se haya aprovisionado TPM.</span><span class="sxs-lookup"><span data-stu-id="e37b8-106">BitLocker would automatically resume once TPM has been provisioned.</span></span>

## <a name="syntax"></a><span data-ttu-id="e37b8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e37b8-107">Syntax</span></span>


```mof
uint32 Disable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="e37b8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e37b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e37b8-109">*OwnerAuth* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e37b8-109">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e37b8-110">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="e37b8-110">Type: **string**</span></span>

<span data-ttu-id="e37b8-111">Cadena que identifica el propietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="e37b8-111">A string that identifies the TPM owner.</span></span> <span data-ttu-id="e37b8-112">Esta cadena debe ser una cadena codificada en Base64 que contenga exactamente 20 bytes de datos binarios.</span><span class="sxs-lookup"><span data-stu-id="e37b8-112">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="e37b8-113">Use el método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una frase de contraseña a este formato esperado.</span><span class="sxs-lookup"><span data-stu-id="e37b8-113">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="e37b8-114">Si no se proporciona ninguno, se lee el parámetro *OwnerAuth* en el registro.</span><span class="sxs-lookup"><span data-stu-id="e37b8-114">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e37b8-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e37b8-115">Return value</span></span>

<span data-ttu-id="e37b8-116">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e37b8-116">Type: **uint32**</span></span>

<span data-ttu-id="e37b8-117">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="e37b8-117">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="e37b8-118">En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="e37b8-118">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="e37b8-119">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e37b8-119">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="e37b8-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="e37b8-120">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e37b8-121"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="e37b8-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="e37b8-122">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e37b8-122">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="e37b8-123"><dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="e37b8-123"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="e37b8-124">El valor de autorización de propietario proporcionado no puede realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e37b8-124">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="e37b8-125"><dt>**TPM \_ E \_ defender \_ LOCK \_ Running**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="e37b8-125"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="e37b8-126">El TPM defiende contra los ataques de diccionario y se encuentra en un período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="e37b8-126">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="e37b8-127">Para obtener más información, vea el método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="e37b8-127">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e37b8-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e37b8-128">Remarks</span></span>

<span data-ttu-id="e37b8-129">Para deshabilitar TPM sin tener el valor de autorización de propietario del TPM, use el método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="e37b8-129">To disable the TPM without having the TPM owner authorization value, use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

<span data-ttu-id="e37b8-130">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e37b8-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e37b8-131">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e37b8-131">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="e37b8-132">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="e37b8-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e37b8-133">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="e37b8-133">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e37b8-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e37b8-134">Requirements</span></span>



| <span data-ttu-id="e37b8-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e37b8-135">Requirement</span></span> | <span data-ttu-id="e37b8-136">Value</span><span class="sxs-lookup"><span data-stu-id="e37b8-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e37b8-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e37b8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e37b8-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e37b8-138">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e37b8-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e37b8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e37b8-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e37b8-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e37b8-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e37b8-141">Namespace</span></span><br/>                | <span data-ttu-id="e37b8-142">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="e37b8-142">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="e37b8-143">MOF</span><span class="sxs-lookup"><span data-stu-id="e37b8-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e37b8-144"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e37b8-144"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="e37b8-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e37b8-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e37b8-146"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="e37b8-146"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e37b8-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="e37b8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e37b8-148">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="e37b8-148">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="e37b8-149">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="e37b8-149">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
