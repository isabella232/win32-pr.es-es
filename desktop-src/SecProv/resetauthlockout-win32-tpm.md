---
description: Restablece el período de tiempo de espera u otro mecanismo que los fabricantes de TPM implementan para protegerse de los ataques de diccionario en los valores de autorización de TPM.
ms.assetid: c2fba6a2-2d03-4ffd-9841-4a9eac0a20ac
title: Método ResetAuthLockOut de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetAuthLockOut
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d28287e410fbaf65ce5b1e617113c35cfece160b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666384"
---
# <a name="resetauthlockout-method-of-the-win32_tpm-class"></a><span data-ttu-id="1fd7f-103">Método ResetAuthLockOut de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="1fd7f-103">ResetAuthLockOut method of the Win32\_Tpm class</span></span>

<span data-ttu-id="1fd7f-104">El método **ResetAuthLockOut** de la clase [**Win32 \_ TPM**](win32-tpm.md) restablece el período de tiempo de espera u otro mecanismo que los fabricantes de TPM implementan para protegerse de los ataques de diccionario en los valores de autorización de TPM.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-104">The **ResetAuthLockOut** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the time-out period or other mechanism that TPM manufacturers implement to protect against dictionary attacks on TPM authorization values.</span></span> <span data-ttu-id="1fd7f-105">En un ataque de diccionario, un atacante intenta adivinar un valor de autorización de TPM correcto al intentar de forma exhaustiva todos los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-105">In a dictionary attack, an attacker tries to guess a correct TPM authorization value by exhaustively attempting all possible values.</span></span>

<span data-ttu-id="1fd7f-106">Use este método si el TPM está bloqueado debido a que hay demasiados intentos incorrectos en especificar la autorización del propietario u otros valores de autorización.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-106">Use this method if the TPM is locked out due to too many incorrect attempts at entering the owner authorization or other authorization values.</span></span> <span data-ttu-id="1fd7f-107">Cuando el TPM está bloqueado, algunos o todos los comandos emitidos para el TPM devolverán un error, y se \_ \_ ejecutará el bloqueo de defender E defender \_ \_ (0x80280803).</span><span class="sxs-lookup"><span data-stu-id="1fd7f-107">When the TPM is locked out, some or all commands issued to the TPM will return an error, TPM\_E\_DEFEND\_LOCK\_RUNNING (0x80280803).</span></span>

> [!Note]  
> <span data-ttu-id="1fd7f-108">Este método solo se puede usar una vez cuando el TPM está bloqueado. Si la autorización del propietario proporcionada a este método es incorrecta, el TPM se bloqueará durante todo el período de tiempo de espera y se producirá un error en el restablecimiento del bloqueo.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-108">This method can only be used exactly once when the TPM is locked out. If the owner authorization provided to this method is incorrect, the TPM will lock out for the entire time-out period and additional attempts at resetting the lock will fail.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1fd7f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1fd7f-109">Syntax</span></span>


```mof
uint32 ResetAuthLockOut(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="1fd7f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1fd7f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fd7f-111">*OwnerAuth* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1fd7f-111">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1fd7f-112">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="1fd7f-112">Type: **string**</span></span>

<span data-ttu-id="1fd7f-113">Cadena que identifica el propietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-113">A string that identifies the TPM owner.</span></span>

<span data-ttu-id="1fd7f-114">Esta cadena debe ser una cadena terminada en NULL con codificación Base64 que contenga exactamente 20 bytes de datos binarios.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-114">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="1fd7f-115">Use el método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una frase de contraseña a este formato esperado.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-115">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="1fd7f-116">Si no se proporciona ninguno, se lee el parámetro *OwnerAuth* en el registro.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-116">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fd7f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1fd7f-117">Return value</span></span>

<span data-ttu-id="1fd7f-118">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1fd7f-118">Type: **uint32**</span></span>

<span data-ttu-id="1fd7f-119">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-119">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span> <span data-ttu-id="1fd7f-120">En la tabla siguiente se enumeran algunos de los valores devueltos comunes.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-120">The following table lists some of the common return values.</span></span>



| <span data-ttu-id="1fd7f-121">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1fd7f-121">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="1fd7f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="1fd7f-122">Description</span></span>                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1fd7f-123"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="1fd7f-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                            | <span data-ttu-id="1fd7f-124">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="1fd7f-125"><dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="1fd7f-125"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl> | <span data-ttu-id="1fd7f-126">El valor de autorización de propietario proporcionado es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-126">The provided owner authorization value is incorrect.</span></span> <span data-ttu-id="1fd7f-127">Se producirá un error en los intentos adicionales al restablecer el bloqueo con este mismo error.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-127">Additional attempts at resetting the lock will fail with this same error.</span></span> <span data-ttu-id="1fd7f-128">Espere hasta que el período de tiempo de espera u otro mecanismo específico del fabricante haya expirado antes de reintentar los comandos de TPM bloqueados.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-128">Please wait until the time-out period or other manufacturer-specific mechanism has expired before retrying locked TPM commands.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1fd7f-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1fd7f-129">Remarks</span></span>

<span data-ttu-id="1fd7f-130">Este método llama al \_ comando ResetLockValue de TPM en el TPM.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-130">This method calls the TPM\_ResetLockValue command on the TPM.</span></span> <span data-ttu-id="1fd7f-131">El comportamiento exacto de este método varía entre los fabricantes de TPM.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-131">The exact behavior of this method varies among TPM manufacturers.</span></span> <span data-ttu-id="1fd7f-132">La documentación del fabricante del equipo o del TPM puede proporcionar información adicional sobre la implementación del mecanismo de ataque contra el diccionario.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-132">Documentation from the computer or TPM manufacturer may provide additional information on the implementation of the anti-dictionary attack mechanism.</span></span>

<span data-ttu-id="1fd7f-133">En general, los fabricantes pueden detectar ataques de diccionario realizando un seguimiento de las autenticaciones con errores.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-133">In general, manufacturers can detect dictionary attacks by keeping track of failed authentications.</span></span> <span data-ttu-id="1fd7f-134">Si el número o la frecuencia de los errores se vuelven lo suficientemente altos, el TPM bloqueará más comandos durante un tiempo determinado.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-134">If the number or frequency of failures become high enough, the TPM will lock out further commands for a certain time.</span></span> <span data-ttu-id="1fd7f-135">Por lo general, el período de tiempo de espera inicial será breve, para permitir que un usuario legítimo pueda corregir la situación.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-135">Generally, the initial time-out period will be short, to allow a legitimate user a chance to correct the situation.</span></span> <span data-ttu-id="1fd7f-136">Si los errores continúan, la duración de cada período de tiempo de espera subsiguiente puede aumentar rápidamente.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-136">If failures continue, the duration of each subsequent time-out period may increase rapidly.</span></span>

<span data-ttu-id="1fd7f-137">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1fd7f-137">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1fd7f-138">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-138">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1fd7f-139">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="1fd7f-139">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1fd7f-140">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="1fd7f-140">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fd7f-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fd7f-141">Requirements</span></span>



| <span data-ttu-id="1fd7f-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fd7f-142">Requirement</span></span> | <span data-ttu-id="1fd7f-143">Value</span><span class="sxs-lookup"><span data-stu-id="1fd7f-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fd7f-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fd7f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="1fd7f-145">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1fd7f-145">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1fd7f-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fd7f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="1fd7f-147">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1fd7f-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1fd7f-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1fd7f-148">Namespace</span></span><br/>                | <span data-ttu-id="1fd7f-149">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="1fd7f-149">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="1fd7f-150">MOF</span><span class="sxs-lookup"><span data-stu-id="1fd7f-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fd7f-151"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1fd7f-151"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fd7f-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1fd7f-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fd7f-153"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="1fd7f-153"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fd7f-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fd7f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fd7f-155">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="1fd7f-155">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
