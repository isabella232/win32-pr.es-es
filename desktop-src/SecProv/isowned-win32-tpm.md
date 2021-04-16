---
description: El método IsOwned de la clase de Win32 \_ TPM indica si el dispositivo tiene un propietario. El método TakeOwnership cambia este valor.
ms.assetid: 04a9394f-98de-43e3-8a19-7a8f409823b8
title: Método IsOwned de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwned
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6ad2d7d03059d8f96fe726d50ea18c2a70db64f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540926"
---
# <a name="isowned-method-of-the-win32_tpm-class"></a><span data-ttu-id="50f0e-104">Método IsOwned de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="50f0e-104">IsOwned method of the Win32\_Tpm class</span></span>

<span data-ttu-id="50f0e-105">El método **IsOwned** de la clase de [**Win32 \_ TPM**](win32-tpm.md) indica si el dispositivo tiene un propietario.</span><span class="sxs-lookup"><span data-stu-id="50f0e-105">The **IsOwned** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device has an owner.</span></span> <span data-ttu-id="50f0e-106">El método [**TakeOwnerShip**](takeownership-win32-tpm.md) cambia este valor.</span><span class="sxs-lookup"><span data-stu-id="50f0e-106">This value is changed by the [**TakeOwnership**](takeownership-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="50f0e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50f0e-107">Syntax</span></span>


```mof
uint32 IsOwned(
  [out] boolean IsOwned
);
```



## <a name="parameters"></a><span data-ttu-id="50f0e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50f0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50f0e-109">*IsOwned* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="50f0e-109">*IsOwned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50f0e-110">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="50f0e-110">Type: **boolean**</span></span>

<span data-ttu-id="50f0e-111">Si **es true**, el dispositivo tiene un propietario.</span><span class="sxs-lookup"><span data-stu-id="50f0e-111">If **true**, the device has an owner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50f0e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50f0e-112">Return value</span></span>

<span data-ttu-id="50f0e-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50f0e-113">Type: **uint32**</span></span>

<span data-ttu-id="50f0e-114">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="50f0e-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="50f0e-115">A continuación se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="50f0e-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="50f0e-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50f0e-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="50f0e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="50f0e-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="50f0e-118"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="50f0e-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="50f0e-119">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="50f0e-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="50f0e-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50f0e-120">Remarks</span></span>

<span data-ttu-id="50f0e-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="50f0e-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="50f0e-122">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="50f0e-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="50f0e-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="50f0e-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="50f0e-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="50f0e-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="50f0e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50f0e-125">Requirements</span></span>



| <span data-ttu-id="50f0e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="50f0e-126">Requirement</span></span> | <span data-ttu-id="50f0e-127">Value</span><span class="sxs-lookup"><span data-stu-id="50f0e-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="50f0e-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50f0e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="50f0e-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="50f0e-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="50f0e-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50f0e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="50f0e-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="50f0e-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="50f0e-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="50f0e-132">Namespace</span></span><br/>                | <span data-ttu-id="50f0e-133">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="50f0e-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="50f0e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="50f0e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50f0e-135"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50f0e-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="50f0e-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="50f0e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50f0e-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="50f0e-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50f0e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="50f0e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50f0e-139">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="50f0e-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
