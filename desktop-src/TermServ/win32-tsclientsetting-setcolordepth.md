---
title: Método SetColorDepth de la clase Win32_TSClientSetting
description: El método SetColorDepth establece la propiedad ColorDepth para la clase.
ms.assetid: 1ab8ac41-cbbf-4077-b91e-692856ccba42
ms.tgt_platform: multiple
keywords:
- Método SetColorDepth Servicios de Escritorio remoto
- Método SetColorDepth Servicios de Escritorio remoto, clase Win32_TSClientSetting
- Win32_TSClientSetting de clase Servicios de Escritorio remoto, método SetColorDepth
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepth
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f2b05c6b8ff02b78f48ff45751bdc8e57ef46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996979"
---
# <a name="setcolordepth-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="52ba7-106">Método SetColorDepth de la \_ clase TSClientSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="52ba7-106">SetColorDepth method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="52ba7-107">El método **SetColorDepth** establece la propiedad **colorDepth** para la clase.</span><span class="sxs-lookup"><span data-stu-id="52ba7-107">The **SetColorDepth** method sets the **ColorDepth** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="52ba7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52ba7-108">Syntax</span></span>


```mof
uint32 SetColorDepth(
  [in] uint32 ColorDepth
);
```



## <a name="parameters"></a><span data-ttu-id="52ba7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52ba7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52ba7-110">*ColorDepth* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="52ba7-110">*ColorDepth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52ba7-111">Nuevo valor de la propiedad **colorDepth** .</span><span class="sxs-lookup"><span data-stu-id="52ba7-111">The new value for the **ColorDepth** property.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="52ba7-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="52ba7-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="52ba7-113">8 bits por píxel</span><span class="sxs-lookup"><span data-stu-id="52ba7-113">8 bits per pixel</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="52ba7-114"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="52ba7-114"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="52ba7-115">15 bits por píxel</span><span class="sxs-lookup"><span data-stu-id="52ba7-115">15 bits per pixel</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="52ba7-116"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="52ba7-116"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="52ba7-117">16 bits por píxel</span><span class="sxs-lookup"><span data-stu-id="52ba7-117">16 bits per pixel</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="52ba7-118"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="52ba7-118"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="52ba7-119">24 bits por píxel</span><span class="sxs-lookup"><span data-stu-id="52ba7-119">24 bits per pixel</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="52ba7-120"><span id="5"></span>**5**</span><span class="sxs-lookup"><span data-stu-id="52ba7-120"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="52ba7-121">32 bits por píxel</span><span class="sxs-lookup"><span data-stu-id="52ba7-121">32 bits per pixel</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52ba7-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52ba7-122">Return value</span></span>

<span data-ttu-id="52ba7-123">Devuelve SUCCESS si es correcto; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="52ba7-123">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="52ba7-124">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="52ba7-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="52ba7-125">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="52ba7-125">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="52ba7-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52ba7-126">Remarks</span></span>

<span data-ttu-id="52ba7-127">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="52ba7-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="52ba7-128">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="52ba7-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="52ba7-129">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="52ba7-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="52ba7-130">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="52ba7-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="52ba7-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52ba7-131">Requirements</span></span>



| <span data-ttu-id="52ba7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="52ba7-132">Requirement</span></span> | <span data-ttu-id="52ba7-133">Value</span><span class="sxs-lookup"><span data-stu-id="52ba7-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52ba7-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52ba7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="52ba7-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52ba7-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="52ba7-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52ba7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="52ba7-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52ba7-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="52ba7-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="52ba7-138">Namespace</span></span><br/>                | <span data-ttu-id="52ba7-139">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="52ba7-139">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="52ba7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="52ba7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52ba7-141"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52ba7-141"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="52ba7-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52ba7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52ba7-143"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52ba7-143"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52ba7-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="52ba7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52ba7-145">**Win32 \_ TSClientSetting**</span><span class="sxs-lookup"><span data-stu-id="52ba7-145">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

