---
description: Indica si está habilitado el aprovisionamiento automático del TPM.
ms.assetid: C908673C-8BDB-4541-85C6-65FED1EBB535
title: 'Win32_Tpm:: IsAutoProvisioningEnabled (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsAutoProvisioningEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cb269247292646464c6126a2588a50d77b19db9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911565"
---
# <a name="win32_tpmisautoprovisioningenabled-method"></a><span data-ttu-id="d175f-103">Win32 \_ TPM:: IsAutoProvisioningEnabled (método)</span><span class="sxs-lookup"><span data-stu-id="d175f-103">Win32\_Tpm::IsAutoProvisioningEnabled method</span></span>

<span data-ttu-id="d175f-104">Indica si está habilitado el aprovisionamiento automático del TPM.</span><span class="sxs-lookup"><span data-stu-id="d175f-104">Indicates if auto provisioning of the TPM is enabled.</span></span> <span data-ttu-id="d175f-105">De forma predeterminada, el aprovisionamiento automático está habilitado para Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="d175f-105">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="d175f-106">Este método solo es accesible para los administradores locales.</span><span class="sxs-lookup"><span data-stu-id="d175f-106">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="d175f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d175f-107">Syntax</span></span>


```C++
uint32 IsAutoProvisioningEnabled(
  [out] BOOL IsAutoProvisioningEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="d175f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d175f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d175f-109">*IsAutoProvisioningEnabled* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d175f-109">*IsAutoProvisioningEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d175f-110">Establézcalo en **true** si está habilitado el aprovisionamiento automático de TPM.</span><span class="sxs-lookup"><span data-stu-id="d175f-110">Set to **TRUE** if the TPM auto provisioning is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d175f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d175f-111">Return value</span></span>

<span data-ttu-id="d175f-112">Se pueden devolver todos los errores de TPM, así como los errores específicos de los [servicios base de TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d175f-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="d175f-113">A continuación se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="d175f-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="d175f-114">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d175f-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="d175f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d175f-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="d175f-116"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="d175f-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="d175f-117">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d175f-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d175f-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d175f-118">Remarks</span></span>

<span data-ttu-id="d175f-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d175f-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d175f-120">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d175f-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d175f-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d175f-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d175f-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="d175f-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d175f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d175f-123">Requirements</span></span>



| <span data-ttu-id="d175f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d175f-124">Requirement</span></span> | <span data-ttu-id="d175f-125">Value</span><span class="sxs-lookup"><span data-stu-id="d175f-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d175f-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d175f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d175f-127">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d175f-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d175f-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d175f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d175f-129">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d175f-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d175f-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d175f-130">Namespace</span></span><br/>                | <span data-ttu-id="d175f-131">\\\\.\\ \\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="d175f-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="d175f-132">MOF</span><span class="sxs-lookup"><span data-stu-id="d175f-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d175f-133"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d175f-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="d175f-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d175f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d175f-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="d175f-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d175f-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="d175f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d175f-137">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="d175f-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
