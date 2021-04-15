---
title: Método ChangeMode de la clase Win32_TerminalServiceSetting
description: El método ChangeMode establece el tipo de licencia del servidor host de sesión de escritorio remoto (host de sesión de RD) Escritorio remoto actual.
ms.assetid: 293483ee-51ce-4cd4-ba13-6c7c02bbdbbf
ms.tgt_platform: multiple
keywords:
- Método ChangeMode Servicios de Escritorio remoto
- Método ChangeMode Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método ChangeMode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.ChangeMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880fcab8aa68e49c6b3c00278b90635686de6168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422257"
---
# <a name="changemode-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="58e37-106">Método ChangeMode de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="58e37-106">ChangeMode method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="58e37-107">El método **ChangeMode** establece el tipo de licencia del servidor host de sesión de escritorio remoto (host de sesión de RD) escritorio remoto actual.</span><span class="sxs-lookup"><span data-stu-id="58e37-107">The **ChangeMode** method sets the licensing type of the current Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="58e37-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58e37-108">Syntax</span></span>


```mof
uint32 ChangeMode(
  [in] uint32 LicensingType
);
```



## <a name="parameters"></a><span data-ttu-id="58e37-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58e37-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58e37-110">*LicensingType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="58e37-110">*LicensingType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58e37-111">Tipo de licencia que se va a establecer en función del modo de servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="58e37-111">The licensing type to set based on the RD Session Host server mode.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="58e37-112"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="58e37-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="58e37-113">Servidor host de sesión de escritorio remoto personal.</span><span class="sxs-lookup"><span data-stu-id="58e37-113">Personal RD Session Host server.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="58e37-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="58e37-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="58e37-115">Escritorio remoto para administración.</span><span class="sxs-lookup"><span data-stu-id="58e37-115">Remote desktop for administration.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="58e37-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="58e37-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="58e37-117">Por dispositivo/por puesto.</span><span class="sxs-lookup"><span data-stu-id="58e37-117">Per device/per seat.</span></span> <span data-ttu-id="58e37-118">Válido para los servidores de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="58e37-118">Valid for application servers.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="58e37-119"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="58e37-119"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="58e37-120">Por usuario.</span><span class="sxs-lookup"><span data-stu-id="58e37-120">Per User.</span></span> <span data-ttu-id="58e37-121">Válido para los servidores de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="58e37-121">Valid for application servers.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58e37-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58e37-122">Return value</span></span>

<span data-ttu-id="58e37-123">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="58e37-123">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="58e37-124">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="58e37-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="58e37-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58e37-125">Remarks</span></span>

<span data-ttu-id="58e37-126">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="58e37-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="58e37-127">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="58e37-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="58e37-128">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="58e37-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="58e37-129">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="58e37-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="58e37-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58e37-130">Requirements</span></span>



| <span data-ttu-id="58e37-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="58e37-131">Requirement</span></span> | <span data-ttu-id="58e37-132">Value</span><span class="sxs-lookup"><span data-stu-id="58e37-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58e37-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58e37-133">Minimum supported client</span></span><br/> | <span data-ttu-id="58e37-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58e37-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="58e37-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58e37-135">Minimum supported server</span></span><br/> | <span data-ttu-id="58e37-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58e37-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58e37-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="58e37-137">Namespace</span></span><br/>                | <span data-ttu-id="58e37-138">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="58e37-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="58e37-139">MOF</span><span class="sxs-lookup"><span data-stu-id="58e37-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58e37-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58e37-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="58e37-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="58e37-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58e37-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58e37-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58e37-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="58e37-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e37-144">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="58e37-144">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

