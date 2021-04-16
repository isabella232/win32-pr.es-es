---
description: El método IsPhysicalPresenceHardwareEnabled de la clase de Win32 \_ TPM indica si la presencia física en la plataforma se puede establecer con una señal de hardware.
ms.assetid: 65dabfa9-bfbe-4b9b-8e80-02269895c7ad
title: Método IsPhysicalPresenceHardwareEnabled de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalPresenceHardwareEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 674dcaa733d8ec70af172359e3dcde0578955dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423760"
---
# <a name="isphysicalpresencehardwareenabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="73f5e-103">Método IsPhysicalPresenceHardwareEnabled de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="73f5e-103">IsPhysicalPresenceHardwareEnabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="73f5e-104">El método **IsPhysicalPresenceHardwareEnabled** de la clase de [**Win32 \_ TPM**](win32-tpm.md) indica si la presencia física en la plataforma se puede establecer con una señal de hardware.</span><span class="sxs-lookup"><span data-stu-id="73f5e-104">The **IsPhysicalPresenceHardwareEnabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether physical presence on the platform can be set with a hardware signal.</span></span> <span data-ttu-id="73f5e-105">El fabricante de la plataforma configura este valor en función del diseño de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="73f5e-105">This value is configured by the platform manufacturer based on the design of the platform.</span></span> <span data-ttu-id="73f5e-106">La documentación del fabricante de la plataforma puede proporcionar información adicional.</span><span class="sxs-lookup"><span data-stu-id="73f5e-106">Documentation from the platform manufacturer may provide additional information.</span></span>

## <a name="syntax"></a><span data-ttu-id="73f5e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73f5e-107">Syntax</span></span>


```mof
uint32 IsPhysicalPresenceHardwareEnabled(
  [out] boolean IsPhysicalPresenceHardwareEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="73f5e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73f5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73f5e-109">*IsPhysicalPresenceHardwareEnabled* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="73f5e-109">*IsPhysicalPresenceHardwareEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73f5e-110">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="73f5e-110">Type: **boolean**</span></span>

<span data-ttu-id="73f5e-111">Si **es true**, la presencia física en la plataforma se puede establecer con una señal de hardware.</span><span class="sxs-lookup"><span data-stu-id="73f5e-111">If **true**, physical presence on the platform can be set with a hardware signal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73f5e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73f5e-112">Return value</span></span>

<span data-ttu-id="73f5e-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73f5e-113">Type: **uint32**</span></span>

<span data-ttu-id="73f5e-114">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="73f5e-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="73f5e-115">A continuación se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="73f5e-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="73f5e-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73f5e-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="73f5e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="73f5e-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="73f5e-118"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="73f5e-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="73f5e-119">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="73f5e-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="73f5e-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73f5e-120">Remarks</span></span>

<span data-ttu-id="73f5e-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="73f5e-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="73f5e-122">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="73f5e-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="73f5e-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="73f5e-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="73f5e-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="73f5e-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73f5e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73f5e-125">Requirements</span></span>



| <span data-ttu-id="73f5e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="73f5e-126">Requirement</span></span> | <span data-ttu-id="73f5e-127">Value</span><span class="sxs-lookup"><span data-stu-id="73f5e-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="73f5e-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73f5e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="73f5e-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="73f5e-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="73f5e-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73f5e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="73f5e-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="73f5e-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="73f5e-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="73f5e-132">Namespace</span></span><br/>                | <span data-ttu-id="73f5e-133">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="73f5e-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="73f5e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="73f5e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73f5e-135"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73f5e-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="73f5e-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="73f5e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73f5e-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="73f5e-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73f5e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="73f5e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73f5e-139">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="73f5e-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
