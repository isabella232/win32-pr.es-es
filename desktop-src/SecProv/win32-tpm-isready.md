---
description: Indica si el TPM está listo para su uso.
ms.assetid: 70E9EB90-DC13-4431-97E5-D77B4E345373
title: 'Win32_Tpm:: IsReady (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsReady
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 37c9d579e424c89f8670838b09ed1c557514ca00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540910"
---
# <a name="win32_tpmisready-method"></a><span data-ttu-id="1c231-103">Win32 \_ TPM:: isReady (método)</span><span class="sxs-lookup"><span data-stu-id="1c231-103">Win32\_Tpm::IsReady method</span></span>

<span data-ttu-id="1c231-104">Indica si el TPM está listo para su uso.</span><span class="sxs-lookup"><span data-stu-id="1c231-104">Indicates whether the TPM is ready for use.</span></span>

<span data-ttu-id="1c231-105">Este método solo es accesible para los administradores locales.</span><span class="sxs-lookup"><span data-stu-id="1c231-105">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c231-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c231-106">Syntax</span></span>


```C++
uint32 IsReady(
  [out] BOOL IsReady
);
```



## <a name="parameters"></a><span data-ttu-id="1c231-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c231-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c231-108">*IsReady* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1c231-108">*IsReady* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c231-109">Establézcalo en **true** si el TPM y el sistema están totalmente aprovisionados para el uso de TPM.</span><span class="sxs-lookup"><span data-stu-id="1c231-109">Set to **TRUE** if the TPM and system are fully provisioned for TPM use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c231-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c231-110">Return value</span></span>

<span data-ttu-id="1c231-111">Se pueden devolver todos los errores de TPM, así como los errores específicos de los [servicios base de TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="1c231-111">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="1c231-112">A continuación se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="1c231-112">Common return codes are listed below.</span></span>



| <span data-ttu-id="1c231-113">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c231-113">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="1c231-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c231-114">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="1c231-115"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="1c231-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="1c231-116">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1c231-116">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1c231-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c231-117">Remarks</span></span>

<span data-ttu-id="1c231-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1c231-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1c231-119">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="1c231-119">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1c231-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="1c231-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1c231-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="1c231-121">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c231-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c231-122">Requirements</span></span>



| <span data-ttu-id="1c231-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c231-123">Requirement</span></span> | <span data-ttu-id="1c231-124">Value</span><span class="sxs-lookup"><span data-stu-id="1c231-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c231-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c231-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1c231-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c231-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1c231-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c231-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1c231-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c231-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1c231-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1c231-129">Namespace</span></span><br/>                | <span data-ttu-id="1c231-130">\\\\.\\ \\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="1c231-130">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="1c231-131">MOF</span><span class="sxs-lookup"><span data-stu-id="1c231-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c231-132"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c231-132"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c231-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1c231-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c231-134"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="1c231-134"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c231-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c231-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c231-136">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="1c231-136">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
