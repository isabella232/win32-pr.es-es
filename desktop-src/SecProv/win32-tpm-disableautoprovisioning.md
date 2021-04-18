---
description: Deshabilita el aprovisionamiento automático del TPM si está habilitado actualmente.
ms.assetid: 30CC2581-9C16-4A11-92F1-625992F2AF20
title: Win32_Tpm::D método isableAutoProvisioning
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.DisableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5387e744ec5f02bf448a997cfe1c8c83342903a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667892"
---
# <a name="win32_tpmdisableautoprovisioning-method"></a><span data-ttu-id="dc373-103">Win32 \_ TPM::D método isableautoprovisioning</span><span class="sxs-lookup"><span data-stu-id="dc373-103">Win32\_Tpm::DisableAutoProvisioning method</span></span>

<span data-ttu-id="dc373-104">Deshabilita el aprovisionamiento automático del TPM si está habilitado actualmente.</span><span class="sxs-lookup"><span data-stu-id="dc373-104">Disables auto provisioning of the TPM if it is currently enabled.</span></span> <span data-ttu-id="dc373-105">La operación no tiene ningún efecto si el aprovisionamiento automático ya está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="dc373-105">The operation has no effect if auto provisioning is already disabled.</span></span> <span data-ttu-id="dc373-106">De forma predeterminada, el aprovisionamiento automático está habilitado para Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="dc373-106">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="dc373-107">Este método solo es accesible para los administradores locales.</span><span class="sxs-lookup"><span data-stu-id="dc373-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc373-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc373-108">Syntax</span></span>


```C++
uint32 DisableAutoProvisioning(
  [in, optional] BOOL OnlyForNextBoot
);
```



## <a name="parameters"></a><span data-ttu-id="dc373-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc373-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc373-110">*OnlyForNextBoot* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dc373-110">*OnlyForNextBoot* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dc373-111">Si se establece en **true**, el aprovisionamiento automático solo se deshabilita para el siguiente arranque.</span><span class="sxs-lookup"><span data-stu-id="dc373-111">If set to **TRUE**, auto provisioning is disabled for only the next boot.</span></span> <span data-ttu-id="dc373-112">Si se establece en **false** o no se especifica, el aprovisionamiento automático está deshabilitado de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="dc373-112">If set to **FALSE** or not specified, auto provisioning is permanently disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc373-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc373-113">Return value</span></span>

<span data-ttu-id="dc373-114">Se pueden devolver todos los errores de TPM, así como los errores específicos de los [servicios base de TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="dc373-114">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="dc373-115">A continuación se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="dc373-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="dc373-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc373-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="dc373-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc373-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="dc373-118"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="dc373-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="dc373-119">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="dc373-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dc373-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc373-120">Remarks</span></span>

<span data-ttu-id="dc373-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="dc373-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="dc373-122">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="dc373-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="dc373-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="dc373-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="dc373-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="dc373-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc373-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc373-125">Requirements</span></span>



| <span data-ttu-id="dc373-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc373-126">Requirement</span></span> | <span data-ttu-id="dc373-127">Value</span><span class="sxs-lookup"><span data-stu-id="dc373-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc373-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc373-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dc373-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="dc373-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dc373-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc373-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dc373-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="dc373-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="dc373-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dc373-132">Namespace</span></span><br/>                | <span data-ttu-id="dc373-133">\\\\.\\ \\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="dc373-133">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="dc373-134">MOF</span><span class="sxs-lookup"><span data-stu-id="dc373-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc373-135"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc373-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc373-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc373-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc373-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="dc373-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc373-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc373-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc373-139">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="dc373-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
