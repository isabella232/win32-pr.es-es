---
description: Obtiene el módulo de la parte pública de la clave raíz de almacenamiento de TPM.
ms.assetid: 266AE378-8BF2-4F6E-A055-E15D95E218DC
title: 'Win32_Tpm:: GetSrkPublicKeyModulus (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkPublicKeyModulus
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6d78abb695f2a9bc9de3887c8128395c2403b2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667891"
---
# <a name="win32_tpmgetsrkpublickeymodulus-method"></a><span data-ttu-id="3f75e-103">Win32 \_ TPM:: GetSrkPublicKeyModulus (método)</span><span class="sxs-lookup"><span data-stu-id="3f75e-103">Win32\_Tpm::GetSrkPublicKeyModulus method</span></span>

<span data-ttu-id="3f75e-104">Obtiene el módulo de la parte pública de la clave raíz de almacenamiento de TPM.</span><span class="sxs-lookup"><span data-stu-id="3f75e-104">Gets the modulus of the public portion of the TPM Storage Root Key.</span></span>

<span data-ttu-id="3f75e-105">Este método solo es accesible para los administradores locales.</span><span class="sxs-lookup"><span data-stu-id="3f75e-105">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f75e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f75e-106">Syntax</span></span>


```C++
uint32 GetSrkPublicKeyModulus(
  [out] uint8 SrkPublicKeyModulus
);
```



## <a name="parameters"></a><span data-ttu-id="3f75e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f75e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f75e-108">*SrkPublicKeyModulus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3f75e-108">*SrkPublicKeyModulus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f75e-109">Devuelve una matriz de 256 bytes que contiene el módulo de la parte pública de la clave raíz de almacenamiento de TPM.</span><span class="sxs-lookup"><span data-stu-id="3f75e-109">Returns a 256-byte array containing the modulus of the public portion of the TPM Storage Root Key</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f75e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f75e-110">Return value</span></span>

<span data-ttu-id="3f75e-111">Se pueden devolver todos los errores de TPM, así como los errores específicos de los [servicios base de TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="3f75e-111">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="3f75e-112">A continuación se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="3f75e-112">Common return codes are listed below.</span></span>



| <span data-ttu-id="3f75e-113">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f75e-113">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="3f75e-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f75e-114">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="3f75e-115"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="3f75e-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="3f75e-116">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3f75e-116">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3f75e-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f75e-117">Remarks</span></span>

<span data-ttu-id="3f75e-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="3f75e-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3f75e-119">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="3f75e-119">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="3f75e-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="3f75e-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3f75e-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="3f75e-121">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f75e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f75e-122">Requirements</span></span>



| <span data-ttu-id="3f75e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f75e-123">Requirement</span></span> | <span data-ttu-id="3f75e-124">Value</span><span class="sxs-lookup"><span data-stu-id="3f75e-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f75e-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f75e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3f75e-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="3f75e-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3f75e-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f75e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3f75e-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="3f75e-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3f75e-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3f75e-129">Namespace</span></span><br/>                | <span data-ttu-id="3f75e-130">\\\\.\\ \\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="3f75e-130">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="3f75e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3f75e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f75e-132"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f75e-132"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f75e-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3f75e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f75e-134"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="3f75e-134"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f75e-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f75e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f75e-136">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="3f75e-136">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
