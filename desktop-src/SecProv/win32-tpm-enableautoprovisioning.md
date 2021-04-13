---
description: Habilita el aprovisionamiento automático del TPM si está actualmente deshabilitado.
ms.assetid: 70F56A4C-F936-4CB6-83F6-F3B691F43B98
title: 'Win32_Tpm:: EnableAutoProvisioning (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.EnableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5288be5c9822b7e76b0cb25b60ee68dacc36d5e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360212"
---
# <a name="win32_tpmenableautoprovisioning-method"></a><span data-ttu-id="0648b-103">Win32 \_ TPM:: EnableAutoProvisioning (método)</span><span class="sxs-lookup"><span data-stu-id="0648b-103">Win32\_Tpm::EnableAutoProvisioning method</span></span>

<span data-ttu-id="0648b-104">Habilita el aprovisionamiento automático del TPM si está actualmente deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="0648b-104">Enables auto provisioning of the TPM if it is currently disabled.</span></span> <span data-ttu-id="0648b-105">La operación no tiene ningún efecto si el aprovisionamiento automático ya está habilitado.</span><span class="sxs-lookup"><span data-stu-id="0648b-105">The operation has no effect if auto provisioning is already enabled.</span></span> <span data-ttu-id="0648b-106">De forma predeterminada, el aprovisionamiento automático está habilitado para Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="0648b-106">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="0648b-107">Este método solo es accesible para los administradores locales.</span><span class="sxs-lookup"><span data-stu-id="0648b-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="0648b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0648b-108">Syntax</span></span>


```C++
uint32 EnableAutoProvisioning();
```



## <a name="parameters"></a><span data-ttu-id="0648b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0648b-109">Parameters</span></span>

<span data-ttu-id="0648b-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0648b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0648b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0648b-111">Return value</span></span>

<span data-ttu-id="0648b-112">Se pueden devolver todos los errores de TPM, así como los errores específicos de los [servicios base de TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0648b-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="0648b-113">A continuación se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="0648b-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="0648b-114">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0648b-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="0648b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="0648b-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="0648b-116"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="0648b-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="0648b-117">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="0648b-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0648b-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0648b-118">Remarks</span></span>

<span data-ttu-id="0648b-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0648b-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0648b-120">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="0648b-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="0648b-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="0648b-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0648b-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="0648b-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0648b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0648b-123">Requirements</span></span>



| <span data-ttu-id="0648b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0648b-124">Requirement</span></span> | <span data-ttu-id="0648b-125">Value</span><span class="sxs-lookup"><span data-stu-id="0648b-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0648b-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0648b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0648b-127">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0648b-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0648b-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0648b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0648b-129">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0648b-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0648b-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0648b-130">Namespace</span></span><br/>                | <span data-ttu-id="0648b-131">\\\\.\\ \\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="0648b-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="0648b-132">MOF</span><span class="sxs-lookup"><span data-stu-id="0648b-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0648b-133"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0648b-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="0648b-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0648b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0648b-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="0648b-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0648b-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="0648b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0648b-137">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="0648b-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
