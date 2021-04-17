---
description: Convierte la entrada de una frase de contraseña proporcionada por el usuario en una autorización de propietario de 20 bytes que se puede usar para interactuar con el TPM. Los métodos como TakeOwnership y ResetAuthLockOut requieren el valor de autorización de propietario resultante.
ms.assetid: 69eed934-1668-495a-b5b7-cd4a87df1ab3
title: Método ConvertToOwnerAuth de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ConvertToOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: f3de5803d10458156fb453e964d782f7c9760333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687900"
---
# <a name="converttoownerauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="af5c6-104">Método ConvertToOwnerAuth de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="af5c6-104">ConvertToOwnerAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="af5c6-105">El método **ConvertToOwnerAuth** de la clase de [**Win32 \_ TPM**](win32-tpm.md) traduce una entrada de frase de contraseña proporcionada por el usuario en una autorización de propietario de 20 bytes que se puede usar para interactuar con el TPM.</span><span class="sxs-lookup"><span data-stu-id="af5c6-105">The **ConvertToOwnerAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class translates a user-provided passphrase input into a 20-byte owner authorization that can be used to interact with the TPM.</span></span> <span data-ttu-id="af5c6-106">Los métodos como [**TakeOwnerShip**](takeownership-win32-tpm.md) y [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) requieren el valor de autorización de propietario resultante.</span><span class="sxs-lookup"><span data-stu-id="af5c6-106">Methods such as [**TakeOwnership**](takeownership-win32-tpm.md) and [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) require the resulting owner authorization value.</span></span>

<span data-ttu-id="af5c6-107">El proceso de conversión sigue las especificaciones del [Trusted Computing Group](https://www.trustedcomputinggroup.org/).</span><span class="sxs-lookup"><span data-stu-id="af5c6-107">The conversion process follows the specifications from the [Trusted Computing Group](https://www.trustedcomputinggroup.org/).</span></span>

## <a name="syntax"></a><span data-ttu-id="af5c6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af5c6-108">Syntax</span></span>


```mof
uint32 ConvertToOwnerAuth(
  [in]  string OwnerPassPhrase,
  [out] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="af5c6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af5c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af5c6-110">*OwnerPassPhrase* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="af5c6-110">*OwnerPassPhrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af5c6-111">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="af5c6-111">Type: **string**</span></span>

<span data-ttu-id="af5c6-112">Cadena que se va a convertir en un valor de autorización de propietario.</span><span class="sxs-lookup"><span data-stu-id="af5c6-112">A string to convert to an owner authorization value.</span></span> <span data-ttu-id="af5c6-113">La cadena puede contener cualquier número de caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="af5c6-113">The string can contain any number of alphanumeric characters.</span></span>

</dd> <dt>

<span data-ttu-id="af5c6-114">*OwnerAuth* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="af5c6-114">*OwnerAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af5c6-115">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="af5c6-115">Type: **string**</span></span>

<span data-ttu-id="af5c6-116">Cadena derivada del parámetro *OwnerPassPhrase* .</span><span class="sxs-lookup"><span data-stu-id="af5c6-116">A string derived from the *OwnerPassPhrase* parameter.</span></span> <span data-ttu-id="af5c6-117">Este valor es un valor binario de 20 bytes codificado en una cadena terminada en **null** de 28 bytes.</span><span class="sxs-lookup"><span data-stu-id="af5c6-117">This value is a 20-byte binary value encoded to a 28-byte base64 **null**-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af5c6-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af5c6-118">Return value</span></span>

<span data-ttu-id="af5c6-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af5c6-119">Type: **uint32**</span></span>

<span data-ttu-id="af5c6-120">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="af5c6-120">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="af5c6-121">En las tablas siguientes se enumeran algunos de los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="af5c6-121">The following tables lists some of the common return codes.</span></span>



| <span data-ttu-id="af5c6-122">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af5c6-122">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="af5c6-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="af5c6-123">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="af5c6-124"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="af5c6-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="af5c6-125">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="af5c6-125">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="af5c6-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af5c6-126">Remarks</span></span>

<span data-ttu-id="af5c6-127">Una cadena codificada UTF-16LE de Unicode se convierte en el valor de autorización de propietario de TPM de 20 bytes tomando el hash SHA-1 de la representación binaria de la cadena.</span><span class="sxs-lookup"><span data-stu-id="af5c6-127">A Unicode UTF-16LE encoded string is converted to the 20-byte TPM owner authorization value by taking the SHA-1 hash of the string's binary representation.</span></span> <span data-ttu-id="af5c6-128">La terminación **null** de la cadena Unicode no se incluye en el hash.</span><span class="sxs-lookup"><span data-stu-id="af5c6-128">The **null** termination of the Unicode string is not included in the hash.</span></span> <span data-ttu-id="af5c6-129">No se usa ningún valor Salt en el hash SHA-1.</span><span class="sxs-lookup"><span data-stu-id="af5c6-129">No salt is used in the SHA-1 hash.</span></span>

<span data-ttu-id="af5c6-130">Por ejemplo, para convertir la frase de contraseña de propietario de TPM "1Sample" en un valor de autorización de propietario de TPM, el hash de SHA-1 se toma de la siguiente secuencia de bytes:</span><span class="sxs-lookup"><span data-stu-id="af5c6-130">For example, to convert the TPM owner passphrase "1Sample" to a TPM owner authorization value, the SHA-1 hash is taken from the following byte stream:</span></span>

`0x31 0x00 0x53 0x00 0x61 0x00 0x6D 0x00 0x70 0x00 0x6C 0x00 0x65 0x00`

<span data-ttu-id="af5c6-131">Para convertir una frase de contraseña de longitud cero en un valor de autorización de propietario, se toma el hash SHA-1 de la secuencia de bytes **null** .</span><span class="sxs-lookup"><span data-stu-id="af5c6-131">To convert a zero-length passphrase to an owner authorization value, the SHA-1 hash is taken of the **NULL** byte stream.</span></span>

<span data-ttu-id="af5c6-132">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="af5c6-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="af5c6-133">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="af5c6-133">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="af5c6-134">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="af5c6-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="af5c6-135">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="af5c6-135">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af5c6-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af5c6-136">Requirements</span></span>



| <span data-ttu-id="af5c6-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="af5c6-137">Requirement</span></span> | <span data-ttu-id="af5c6-138">Value</span><span class="sxs-lookup"><span data-stu-id="af5c6-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="af5c6-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af5c6-139">Minimum supported client</span></span><br/> | <span data-ttu-id="af5c6-140">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="af5c6-140">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="af5c6-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af5c6-141">Minimum supported server</span></span><br/> | <span data-ttu-id="af5c6-142">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="af5c6-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="af5c6-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="af5c6-143">Namespace</span></span><br/>                | <span data-ttu-id="af5c6-144">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="af5c6-144">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="af5c6-145">MOF</span><span class="sxs-lookup"><span data-stu-id="af5c6-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af5c6-146"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af5c6-146"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="af5c6-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="af5c6-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af5c6-148"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="af5c6-148"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af5c6-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="af5c6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af5c6-150">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="af5c6-150">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="af5c6-151">**TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="af5c6-151">**TakeOwnership**</span></span>](takeownership-win32-tpm.md)
</dt> </dl>

 

 
