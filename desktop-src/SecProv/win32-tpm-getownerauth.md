---
description: Obtiene la información de autorización del propietario de un TPM, si hay alguno disponible en el registro.
ms.assetid: 3E2C28C8-4154-4B1B-9C47-AEDFD5622979
title: 'Win32_Tpm:: GetOwnerAuth (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: a441b07af31758212152b657ccb033d8abdeebbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540915"
---
# <a name="win32_tpmgetownerauth-method"></a><span data-ttu-id="7c2d0-103">Win32 \_ TPM:: GetOwnerAuth (método)</span><span class="sxs-lookup"><span data-stu-id="7c2d0-103">Win32\_Tpm::GetOwnerAuth method</span></span>

<span data-ttu-id="7c2d0-104">Obtiene la información de autorización del propietario de un TPM, si hay alguno disponible en el registro.</span><span class="sxs-lookup"><span data-stu-id="7c2d0-104">Gets the owner authorization information for a TPM if one is available in the registry.</span></span> <span data-ttu-id="7c2d0-105">Si un TPM es propiedad o se aprovisiona en Windows 8 con la configuración predeterminada, la información de autorización del propietario del TPM se almacena en el registro y está disponible para su uso por este método.</span><span class="sxs-lookup"><span data-stu-id="7c2d0-105">If a TPM is owned or provisioned in Windows 8 with the default settings, the TPM owner authorization information is stored in the registry and is available for use by this method.</span></span>

<span data-ttu-id="7c2d0-106">Este método solo es accesible para los administradores locales.</span><span class="sxs-lookup"><span data-stu-id="7c2d0-106">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c2d0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c2d0-107">Syntax</span></span>


```C++
uint32 GetOwnerAuth(
  [out] STRING OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="7c2d0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c2d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c2d0-109">*OwnerAuth* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7c2d0-109">*OwnerAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c2d0-110">La información de autorización del propietario de un TPM, si está disponible en el registro.</span><span class="sxs-lookup"><span data-stu-id="7c2d0-110">The owner authorization information for a TPM, if one is available in the registry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c2d0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c2d0-111">Return value</span></span>

<span data-ttu-id="7c2d0-112">Se pueden devolver todos los errores de TPM, así como los errores específicos de los [servicios base de TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="7c2d0-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="7c2d0-113">A continuación se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="7c2d0-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="7c2d0-114">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c2d0-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="7c2d0-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c2d0-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="7c2d0-116"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="7c2d0-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="7c2d0-117">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7c2d0-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7c2d0-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c2d0-118">Remarks</span></span>

<span data-ttu-id="7c2d0-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7c2d0-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7c2d0-120">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7c2d0-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7c2d0-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="7c2d0-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7c2d0-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7c2d0-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c2d0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c2d0-123">Requirements</span></span>



| <span data-ttu-id="7c2d0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c2d0-124">Requirement</span></span> | <span data-ttu-id="7c2d0-125">Value</span><span class="sxs-lookup"><span data-stu-id="7c2d0-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c2d0-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c2d0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7c2d0-127">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="7c2d0-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7c2d0-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c2d0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7c2d0-129">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="7c2d0-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7c2d0-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7c2d0-130">Namespace</span></span><br/>                | <span data-ttu-id="7c2d0-131">\\\\.\\ \\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="7c2d0-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="7c2d0-132">MOF</span><span class="sxs-lookup"><span data-stu-id="7c2d0-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c2d0-133"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c2d0-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c2d0-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7c2d0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c2d0-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="7c2d0-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c2d0-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c2d0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c2d0-137">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="7c2d0-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
