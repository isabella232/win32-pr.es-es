---
title: Método SetSessionDirectoryActive de la clase Win32_TSSessionDirectory
description: El método SetSessionDirectoryActive establece la propiedad SessionDirectoryActive.
ms.assetid: b2175d1a-b62f-4bdf-9122-76e85233fba4
ms.tgt_platform: multiple
keywords:
- Método SetSessionDirectoryActive Servicios de Escritorio remoto
- Método SetSessionDirectoryActive Servicios de Escritorio remoto, clase Win32_TSSessionDirectory
- Win32_TSSessionDirectory de clase Servicios de Escritorio remoto, método SetSessionDirectoryActive
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca8709028ee90db549c7cdeb053b04dc88b52ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422204"
---
# <a name="setsessiondirectoryactive-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="94486-106">Método SetSessionDirectoryActive de la \_ clase TSSessionDirectory de Win32</span><span class="sxs-lookup"><span data-stu-id="94486-106">SetSessionDirectoryActive method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="94486-107">El método **SetSessionDirectoryActive** establece la propiedad **SessionDirectoryActive** .</span><span class="sxs-lookup"><span data-stu-id="94486-107">The **SetSessionDirectoryActive** method sets the **SessionDirectoryActive** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="94486-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94486-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryActive(
  [in] uint32 SessionDirectoryActive
);
```



## <a name="parameters"></a><span data-ttu-id="94486-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94486-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94486-110">*SessionDirectoryActive* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="94486-110">*SessionDirectoryActive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94486-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94486-111">Type: **uint32**</span></span>

<span data-ttu-id="94486-112">Marca que deshabilita o habilita el servicio de directorio de sesión.</span><span class="sxs-lookup"><span data-stu-id="94486-112">Flag disabling or enabling the Session Directory service.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="94486-113"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="94486-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="94486-114">Deshabilite el servicio Directorio de sesión.</span><span class="sxs-lookup"><span data-stu-id="94486-114">Disable the Session Directory service.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="94486-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="94486-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="94486-116">Habilite el servicio Directorio de sesión.</span><span class="sxs-lookup"><span data-stu-id="94486-116">Enable the Session Directory service.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94486-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94486-117">Return value</span></span>

<span data-ttu-id="94486-118">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94486-118">Type: **uint32**</span></span>

<span data-ttu-id="94486-119">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="94486-119">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="94486-120">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="94486-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="94486-121">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="94486-121">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="94486-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94486-122">Remarks</span></span>

<span data-ttu-id="94486-123">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="94486-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="94486-124">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="94486-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="94486-125">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="94486-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="94486-126">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="94486-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="94486-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94486-127">Requirements</span></span>



| <span data-ttu-id="94486-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="94486-128">Requirement</span></span> | <span data-ttu-id="94486-129">Value</span><span class="sxs-lookup"><span data-stu-id="94486-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94486-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94486-130">Minimum supported client</span></span><br/> | <span data-ttu-id="94486-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="94486-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="94486-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94486-132">Minimum supported server</span></span><br/> | <span data-ttu-id="94486-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94486-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94486-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="94486-134">Namespace</span></span><br/>                | <span data-ttu-id="94486-135">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="94486-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="94486-136">MOF</span><span class="sxs-lookup"><span data-stu-id="94486-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94486-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94486-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="94486-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="94486-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94486-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94486-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94486-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="94486-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94486-141">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="94486-141">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

