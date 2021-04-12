---
description: Restablece el valor de autorización de la clave raíz de almacenamiento (SRK) para que sea compatible con el sistema operativo.
ms.assetid: af008733-b43c-4017-9e79-bdd98f2e20b6
title: Método ResetSrkAuth de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetSrkAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 7d838ded7051511b6a8f9117327ee7cdb1a00d7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361381"
---
# <a name="resetsrkauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="64409-103">Método ResetSrkAuth de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="64409-103">ResetSrkAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="64409-104">El método **ResetSrkAuth** de la clase [**Win32 \_ TPM**](win32-tpm.md) restablece el valor de autorización de la clave raíz de almacenamiento (SRK) para que sea compatible con el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="64409-104">The **ResetSrkAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the Storage Root Key (SRK) authorization value to be compatible with the operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="64409-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64409-105">Syntax</span></span>


```mof
uint32 ResetSrkAuth(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="64409-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64409-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64409-107">*OwnerAuth* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="64409-107">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="64409-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="64409-108">Type: **string**</span></span>

<span data-ttu-id="64409-109">Cadena que identifica el propietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="64409-109">A string that identifies the TPM owner.</span></span> <span data-ttu-id="64409-110">Esta cadena debe ser una cadena terminada en NULL con codificación Base64 que contenga exactamente 20 bytes de datos binarios.</span><span class="sxs-lookup"><span data-stu-id="64409-110">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="64409-111">Use el método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una frase de contraseña a este formato esperado.</span><span class="sxs-lookup"><span data-stu-id="64409-111">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="64409-112">Si no se proporciona ninguno, se lee el parámetro *OwnerAuth* en el registro.</span><span class="sxs-lookup"><span data-stu-id="64409-112">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64409-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64409-113">Return value</span></span>

<span data-ttu-id="64409-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64409-114">Type: **uint32**</span></span>

<span data-ttu-id="64409-115">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="64409-115">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="64409-116">En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="64409-116">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="64409-117">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64409-117">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="64409-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="64409-118">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="64409-119"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="64409-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="64409-120">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="64409-120">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="64409-121"><dt> **TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="64409-121"><dt>**TPM\_E\_AUTHFAIL** </dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>             | <span data-ttu-id="64409-122">El valor de autorización de propietario proporcionado no puede satisfacer la solicitud.</span><span class="sxs-lookup"><span data-stu-id="64409-122">The provided owner authorization value cannot fulfill the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="64409-123"><dt>**TPM \_ E \_ defender \_ LOCK \_ Running**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="64409-123"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="64409-124">El TPM defiende contra los ataques de diccionario y se encuentra en un período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="64409-124">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="64409-125">Para obtener más información, vea el método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="64409-125">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="64409-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64409-126">Remarks</span></span>

<span data-ttu-id="64409-127">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="64409-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="64409-128">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="64409-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="64409-129">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="64409-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="64409-130">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="64409-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64409-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64409-131">Requirements</span></span>



| <span data-ttu-id="64409-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="64409-132">Requirement</span></span> | <span data-ttu-id="64409-133">Value</span><span class="sxs-lookup"><span data-stu-id="64409-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="64409-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64409-134">Minimum supported client</span></span><br/> | <span data-ttu-id="64409-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="64409-135">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="64409-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64409-136">Minimum supported server</span></span><br/> | <span data-ttu-id="64409-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="64409-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="64409-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="64409-138">Namespace</span></span><br/>                | <span data-ttu-id="64409-139">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="64409-139">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="64409-140">MOF</span><span class="sxs-lookup"><span data-stu-id="64409-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64409-141"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64409-141"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="64409-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="64409-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64409-143"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="64409-143"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64409-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="64409-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64409-145">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="64409-145">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
