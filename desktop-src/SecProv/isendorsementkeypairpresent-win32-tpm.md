---
description: El método IsEndorsementKeyPairPresent de la \_ clase Win32 TPM indica si el par de claves de aprobación existe en el dispositivo.
ms.assetid: c36cd0b5-1ac2-4fcf-b140-c5ecb0b3b211
title: Método IsEndorsementKeyPairPresent de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEndorsementKeyPairPresent
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 63561a4971523fd1554e1d973861c3f0737df2ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156833"
---
# <a name="isendorsementkeypairpresent-method-of-the-win32_tpm-class"></a><span data-ttu-id="7adf8-103">Método IsEndorsementKeyPairPresent de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="7adf8-103">IsEndorsementKeyPairPresent method of the Win32\_Tpm class</span></span>

<span data-ttu-id="7adf8-104">El método **IsEndorsementKeyPairPresent** de la clase [**Win32 \_ TPM**](win32-tpm.md) indica si el par de claves de aprobación existe en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7adf8-104">The **IsEndorsementKeyPairPresent** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the endorsement key pair exists on the device.</span></span> <span data-ttu-id="7adf8-105">El par de claves de aprobación es necesario para que el dispositivo pueda ser propiedad.</span><span class="sxs-lookup"><span data-stu-id="7adf8-105">The endorsement key pair is required before the device can be owned.</span></span> <span data-ttu-id="7adf8-106">Este par de claves se puede crear mediante el método [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="7adf8-106">This key pair can be created by the [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) method.</span></span>

<span data-ttu-id="7adf8-107">El dispositivo debe estar habilitado y activado para que este método se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="7adf8-107">The device must be enabled and activated for this method to succeed.</span></span> <span data-ttu-id="7adf8-108">Para habilitar y activar un dispositivo no propietario, vea el método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="7adf8-108">To enable and activate an unowned device, see the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7adf8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7adf8-109">Syntax</span></span>


```mof
uint32 IsEndorsementKeyPairPresent(
  [out] boolean IsEndorsementKeyPairPresent
);
```



## <a name="parameters"></a><span data-ttu-id="7adf8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7adf8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7adf8-111">*IsEndorsementKeyPairPresent* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7adf8-111">*IsEndorsementKeyPairPresent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7adf8-112">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7adf8-112">Type: **boolean**</span></span>

<span data-ttu-id="7adf8-113">Si **es true**, el par de claves de aprobación existe en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7adf8-113">If **true**, the endorsement key pair exists on the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7adf8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7adf8-114">Return value</span></span>

<span data-ttu-id="7adf8-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7adf8-115">Type: **uint32**</span></span>

<span data-ttu-id="7adf8-116">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="7adf8-116">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="7adf8-117">A continuación se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="7adf8-117">Common return codes are listed below.</span></span>



| <span data-ttu-id="7adf8-118">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7adf8-118">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="7adf8-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="7adf8-119">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="7adf8-120"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="7adf8-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="7adf8-121">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7adf8-121">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7adf8-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7adf8-122">Remarks</span></span>

<span data-ttu-id="7adf8-123">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7adf8-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7adf8-124">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7adf8-124">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7adf8-125">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="7adf8-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7adf8-126">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7adf8-126">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7adf8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7adf8-127">Requirements</span></span>



| <span data-ttu-id="7adf8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7adf8-128">Requirement</span></span> | <span data-ttu-id="7adf8-129">Value</span><span class="sxs-lookup"><span data-stu-id="7adf8-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7adf8-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7adf8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7adf8-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7adf8-131">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7adf8-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7adf8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7adf8-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7adf8-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7adf8-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7adf8-134">Namespace</span></span><br/>                | <span data-ttu-id="7adf8-135">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="7adf8-135">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="7adf8-136">MOF</span><span class="sxs-lookup"><span data-stu-id="7adf8-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7adf8-137"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7adf8-137"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="7adf8-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7adf8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7adf8-139"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="7adf8-139"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7adf8-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="7adf8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7adf8-141">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="7adf8-141">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="7adf8-142">**CreateEndorsementKeyPair**</span><span class="sxs-lookup"><span data-stu-id="7adf8-142">**CreateEndorsementKeyPair**</span></span>](createendorsementkeypair-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="7adf8-143">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="7adf8-143">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
