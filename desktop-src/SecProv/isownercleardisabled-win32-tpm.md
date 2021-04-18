---
description: El método IsOwnerClearDisabled de la clase de Win32 \_ TPM indica si el propietario del dispositivo está restringido para borrar el dispositivo.
ms.assetid: 04f98e9b-c1a0-4828-b7cb-67b32d7470ea
title: Método IsOwnerClearDisabled de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnerClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 13e8b7de707cb1b1af4d4ccdb1208c6391e26987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688019"
---
# <a name="isownercleardisabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="ced81-103">Método IsOwnerClearDisabled de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="ced81-103">IsOwnerClearDisabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="ced81-104">El método **IsOwnerClearDisabled** de la clase de [**Win32 \_ TPM**](win32-tpm.md) indica si el propietario del dispositivo está restringido para borrar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ced81-104">The **IsOwnerClearDisabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device owner is restricted from clearing the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ced81-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ced81-105">Syntax</span></span>


```mof
uint32 IsOwnerClearDisabled(
  [out] boolean IsOwnerClearDisabled
);
```



## <a name="parameters"></a><span data-ttu-id="ced81-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ced81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ced81-107">*IsOwnerClearDisabled* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ced81-107">*IsOwnerClearDisabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ced81-108">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ced81-108">Type: **boolean**</span></span>

<span data-ttu-id="ced81-109">Si es **true**, el propietario del dispositivo no puede borrar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ced81-109">If **true**, the device owner is unable to clear the device.</span></span> <span data-ttu-id="ced81-110">Solo un usuario presente físicamente puede borrar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ced81-110">Only a physically present user may be able to clear the device.</span></span> <span data-ttu-id="ced81-111">Si es **false**, el propietario del dispositivo puede borrar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ced81-111">If **false**, the device owner is able to clear the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ced81-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ced81-112">Return value</span></span>

<span data-ttu-id="ced81-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ced81-113">Type: **uint32**</span></span>

<span data-ttu-id="ced81-114">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="ced81-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="ced81-115">A continuación se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="ced81-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="ced81-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ced81-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="ced81-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="ced81-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ced81-118"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="ced81-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="ced81-119">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ced81-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ced81-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ced81-120">Remarks</span></span>

<span data-ttu-id="ced81-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ced81-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ced81-122">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ced81-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ced81-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="ced81-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ced81-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="ced81-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ced81-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ced81-125">Requirements</span></span>



| <span data-ttu-id="ced81-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ced81-126">Requirement</span></span> | <span data-ttu-id="ced81-127">Value</span><span class="sxs-lookup"><span data-stu-id="ced81-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ced81-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ced81-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ced81-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ced81-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ced81-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ced81-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ced81-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ced81-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ced81-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ced81-132">Namespace</span></span><br/>                | <span data-ttu-id="ced81-133">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="ced81-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="ced81-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ced81-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ced81-135"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ced81-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="ced81-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ced81-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ced81-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="ced81-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ced81-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="ced81-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ced81-139">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="ced81-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
