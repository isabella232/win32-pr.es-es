---
title: Método SetColorDepthPolicy de la clase Win32_TSClientSetting
description: El método SetColorDepthPolicy establece la propiedad ColorDepthPolicy para la clase.
ms.assetid: 7a8c2b51-5f7a-4188-aae0-0b2d47d043bd
ms.tgt_platform: multiple
keywords:
- Método SetColorDepthPolicy Servicios de Escritorio remoto
- Método SetColorDepthPolicy Servicios de Escritorio remoto, clase Win32_TSClientSetting
- Win32_TSClientSetting de clase Servicios de Escritorio remoto, método SetColorDepthPolicy
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepthPolicy
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2d47280ce303e7eeba401e0eb34c7f7fa5a7bec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422252"
---
# <a name="setcolordepthpolicy-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="5c63d-106">Método SetColorDepthPolicy de la \_ clase TSClientSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="5c63d-106">SetColorDepthPolicy method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="5c63d-107">El método **SetColorDepthPolicy** establece la propiedad **ColorDepthPolicy** para la clase.</span><span class="sxs-lookup"><span data-stu-id="5c63d-107">The **SetColorDepthPolicy** method sets the **ColorDepthPolicy** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c63d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c63d-108">Syntax</span></span>


```mof
uint32 SetColorDepthPolicy(
  [in] uint32 ColorDepthPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="5c63d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c63d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c63d-110">*ColorDepthPolicy* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5c63d-110">*ColorDepthPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c63d-111">Marca que deshabilita o habilita la propiedad **SetColorDepthPolicy** , que especifica si se debe invalidar la configuración de color máxima del usuario.</span><span class="sxs-lookup"><span data-stu-id="5c63d-111">Flag disabling or enabling the **SetColorDepthPolicy** property, which specifies whether to override the user's maximum color setting.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="5c63d-112"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="5c63d-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="5c63d-113">Habilite la propiedad.</span><span class="sxs-lookup"><span data-stu-id="5c63d-113">Enable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="5c63d-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="5c63d-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="5c63d-115">Deshabilite la propiedad.</span><span class="sxs-lookup"><span data-stu-id="5c63d-115">Disable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c63d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c63d-116">Return value</span></span>

<span data-ttu-id="5c63d-117">Devuelve SUCCESS si es correcto; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="5c63d-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="5c63d-118">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="5c63d-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="5c63d-119">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="5c63d-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c63d-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c63d-120">Remarks</span></span>

<span data-ttu-id="5c63d-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5c63d-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5c63d-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5c63d-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5c63d-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="5c63d-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5c63d-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5c63d-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c63d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c63d-125">Requirements</span></span>



| <span data-ttu-id="5c63d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c63d-126">Requirement</span></span> | <span data-ttu-id="5c63d-127">Value</span><span class="sxs-lookup"><span data-stu-id="5c63d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c63d-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c63d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5c63d-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c63d-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5c63d-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c63d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5c63d-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c63d-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5c63d-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5c63d-132">Namespace</span></span><br/>                | <span data-ttu-id="5c63d-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5c63d-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5c63d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5c63d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c63d-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c63d-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c63d-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5c63d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c63d-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c63d-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c63d-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c63d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c63d-139">**Win32 \_ TSClientSetting**</span><span class="sxs-lookup"><span data-stu-id="5c63d-139">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

