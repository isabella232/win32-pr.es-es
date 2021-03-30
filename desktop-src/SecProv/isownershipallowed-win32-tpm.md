---
description: El método IsOwnershipAllowed de la clase de Win32 \_ TPM indica si se permite la capacidad de instalar un propietario para el dispositivo.
ms.assetid: dfeb5afe-4169-470b-b5e4-cf1e5781271e
title: Método IsOwnershipAllowed de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnershipAllowed
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c818d5a4e4eb16ac637372f0c7ed0f2e9211ef88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275317"
---
# <a name="isownershipallowed-method-of-the-win32_tpm-class"></a><span data-ttu-id="a5f00-103">Método IsOwnershipAllowed de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="a5f00-103">IsOwnershipAllowed method of the Win32\_Tpm class</span></span>

<span data-ttu-id="a5f00-104">El método **IsOwnershipAllowed** de la clase de [**Win32 \_ TPM**](win32-tpm.md) indica si se permite la capacidad de instalar un propietario para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5f00-104">The **IsOwnershipAllowed** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the ability to install an owner for the device is permitted.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5f00-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5f00-105">Syntax</span></span>


```mof
uint32 IsOwnershipAllowed(
  [out] boolean IsOwnershipAllowed
);
```



## <a name="parameters"></a><span data-ttu-id="a5f00-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5f00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5f00-107">*IsOwnershipAllowed* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a5f00-107">*IsOwnershipAllowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f00-108">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a5f00-108">Type: **boolean**</span></span>

<span data-ttu-id="a5f00-109">Si es **true**, se permite la capacidad de instalar un propietario para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5f00-109">If **true**, the ability to install an owner for the device is permitted.</span></span> <span data-ttu-id="a5f00-110">Si **es false**, el método [**TakeOwnerShip**](takeownership-win32-tpm.md) no podrá instalar un propietario para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5f00-110">If **false**, the method [**TakeOwnership**](takeownership-win32-tpm.md) will fail to install an owner for the device.</span></span>

<span data-ttu-id="a5f00-111">Este valor se puede cambiar con el método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f00-111">This value can be changed with the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span> <span data-ttu-id="a5f00-112">El valor se restablece en **true** después de ejecutar el método [**Clear**](clear-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f00-112">The value is reset to **true** after the [**Clear**](clear-win32-tpm.md) method is run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5f00-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5f00-113">Return value</span></span>

<span data-ttu-id="a5f00-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a5f00-114">Type: **uint32**</span></span>

<span data-ttu-id="a5f00-115">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="a5f00-115">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="a5f00-116">A continuación se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="a5f00-116">Common return codes are listed below.</span></span>



| <span data-ttu-id="a5f00-117">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5f00-117">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="a5f00-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5f00-118">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="a5f00-119"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="a5f00-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="a5f00-120">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a5f00-120">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a5f00-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5f00-121">Remarks</span></span>

<span data-ttu-id="a5f00-122">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a5f00-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a5f00-123">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a5f00-123">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="a5f00-124">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="a5f00-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a5f00-125">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="a5f00-125">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5f00-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5f00-126">Requirements</span></span>



| <span data-ttu-id="a5f00-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5f00-127">Requirement</span></span> | <span data-ttu-id="a5f00-128">Value</span><span class="sxs-lookup"><span data-stu-id="a5f00-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5f00-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5f00-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a5f00-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a5f00-130">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a5f00-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5f00-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a5f00-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5f00-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a5f00-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a5f00-133">Namespace</span></span><br/>                | <span data-ttu-id="a5f00-134">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="a5f00-134">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="a5f00-135">MOF</span><span class="sxs-lookup"><span data-stu-id="a5f00-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5f00-136"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5f00-136"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5f00-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a5f00-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5f00-138"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="a5f00-138"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5f00-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5f00-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5f00-140">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="a5f00-140">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
