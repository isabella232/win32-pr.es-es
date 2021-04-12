---
description: Permite al propietario del TPM habilitar o reanudar el TPM.
ms.assetid: 9fb0b0aa-a569-4c0c-859e-8640480dbb3e
title: Método enable de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Enable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6fe79ee44cb2ef6494b770a53cb57f7b88943dc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276997"
---
# <a name="enable-method-of-the-win32_tpm-class"></a><span data-ttu-id="60783-103">Método enable de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="60783-103">Enable method of the Win32\_Tpm class</span></span>

<span data-ttu-id="60783-104">El método **enable** de la clase [**Win32 \_ TPM**](win32-tpm.md) permite que el propietario del TPM habilite o reanude el TPM.</span><span class="sxs-lookup"><span data-stu-id="60783-104">The **Enable** method of the [**Win32\_Tpm**](win32-tpm.md) class allows the TPM owner to enable or resume the TPM.</span></span>

<span data-ttu-id="60783-105">Para ejecutar este método, el TPM ya debe tener un propietario.</span><span class="sxs-lookup"><span data-stu-id="60783-105">To run this method, the TPM must already have an owner.</span></span> <span data-ttu-id="60783-106">Para habilitar un TPM que aún no tiene un propietario, use el método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="60783-106">To enable a TPM that does not already have an owner, use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="60783-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60783-107">Syntax</span></span>


```mof
uint32 Enable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="60783-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60783-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60783-109">*OwnerAuth* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="60783-109">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="60783-110">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="60783-110">Type: **string**</span></span>

<span data-ttu-id="60783-111">Cadena que identifica el propietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="60783-111">A string that identifies the TPM owner.</span></span> <span data-ttu-id="60783-112">Esta cadena debe ser una cadena codificada en Base64 que contenga exactamente 20 bytes de datos binarios.</span><span class="sxs-lookup"><span data-stu-id="60783-112">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="60783-113">Use el método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una frase de contraseña a este formato esperado.</span><span class="sxs-lookup"><span data-stu-id="60783-113">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="60783-114">Si no se proporciona ninguno, se lee el parámetro *OwnerAuth* en el registro.</span><span class="sxs-lookup"><span data-stu-id="60783-114">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60783-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60783-115">Return value</span></span>

<span data-ttu-id="60783-116">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60783-116">Type: **uint32**</span></span>

<span data-ttu-id="60783-117">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="60783-117">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="60783-118">En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="60783-118">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="60783-119">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60783-119">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="60783-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="60783-120">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="60783-121"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="60783-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="60783-122">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="60783-122">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="60783-123"><dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="60783-123"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="60783-124">El valor de autorización de propietario proporcionado no puede realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="60783-124">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="60783-125"><dt>**TPM \_ E \_ defender \_ LOCK \_ Running**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="60783-125"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="60783-126">El TPM defiende contra los ataques de diccionario y se encuentra en un período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="60783-126">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="60783-127">Para obtener más información, vea el método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="60783-127">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="60783-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60783-128">Remarks</span></span>

<span data-ttu-id="60783-129">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="60783-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="60783-130">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="60783-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="60783-131">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="60783-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="60783-132">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="60783-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60783-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60783-133">Requirements</span></span>



| <span data-ttu-id="60783-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="60783-134">Requirement</span></span> | <span data-ttu-id="60783-135">Value</span><span class="sxs-lookup"><span data-stu-id="60783-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="60783-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60783-136">Minimum supported client</span></span><br/> | <span data-ttu-id="60783-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="60783-137">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="60783-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60783-138">Minimum supported server</span></span><br/> | <span data-ttu-id="60783-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="60783-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="60783-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="60783-140">Namespace</span></span><br/>                | <span data-ttu-id="60783-141">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="60783-141">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="60783-142">MOF</span><span class="sxs-lookup"><span data-stu-id="60783-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60783-143"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60783-143"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="60783-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60783-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60783-145"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="60783-145"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60783-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="60783-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60783-147">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="60783-147">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="60783-148">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="60783-148">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
