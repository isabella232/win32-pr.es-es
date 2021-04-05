---
title: Método SetClientWallPaper de la clase Win32_TSEnvironmentSetting
description: El método SetClientWallPaper establece la propiedad ClientWallPaper.
ms.assetid: 08c41df4-5a3c-4799-bb64-61f414814d0c
ms.tgt_platform: multiple
keywords:
- Método SetClientWallPaper Servicios de Escritorio remoto
- Método SetClientWallPaper Servicios de Escritorio remoto, clase Win32_TSEnvironmentSetting
- Win32_TSEnvironmentSetting de clase Servicios de Escritorio remoto, método SetClientWallPaper
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.SetClientWallPaper
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ae476134cf526602a059b4714cded6fd6c990e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802095"
---
# <a name="setclientwallpaper-method-of-the-win32_tsenvironmentsetting-class"></a><span data-ttu-id="1a1fb-106">Método SetClientWallPaper de la \_ clase TSEnvironmentSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="1a1fb-106">SetClientWallPaper method of the Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="1a1fb-107">El método **SetClientWallPaper** establece la propiedad **ClientWallPaper** .</span><span class="sxs-lookup"><span data-stu-id="1a1fb-107">The **SetClientWallPaper** method sets the **ClientWallPaper** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a1fb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a1fb-108">Syntax</span></span>


```mof
uint32 SetClientWallPaper(
  [in] uint32 ClientWallPaper
);
```



## <a name="parameters"></a><span data-ttu-id="1a1fb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a1fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a1fb-110">*ClientWallPaper* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1a1fb-110">*ClientWallPaper* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a1fb-111">Marca que deshabilita o habilita la propiedad **ClientWallPaper** , que especifica si se muestra la imagen de fondo (o papel tapiz) en el cliente.</span><span class="sxs-lookup"><span data-stu-id="1a1fb-111">Flag disabling or enabling the **ClientWallPaper** property, which specifies whether the background (or wallpaper) image is displayed on the client.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="1a1fb-112"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="1a1fb-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="1a1fb-113">La imagen de fondo (o papel tapiz) no se muestra en el cliente.</span><span class="sxs-lookup"><span data-stu-id="1a1fb-113">The background (or wallpaper) image is not displayed on the client.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="1a1fb-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="1a1fb-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="1a1fb-115">La imagen de fondo (o papel tapiz) se muestra en el cliente.</span><span class="sxs-lookup"><span data-stu-id="1a1fb-115">The background (or wallpaper) image is displayed on the client.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a1fb-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a1fb-116">Return value</span></span>

<span data-ttu-id="1a1fb-117">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="1a1fb-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="1a1fb-118">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="1a1fb-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="1a1fb-119">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="1a1fb-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a1fb-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a1fb-120">Remarks</span></span>

<span data-ttu-id="1a1fb-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1a1fb-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1a1fb-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1a1fb-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1a1fb-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="1a1fb-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1a1fb-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1a1fb-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a1fb-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a1fb-125">Requirements</span></span>



| <span data-ttu-id="1a1fb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a1fb-126">Requirement</span></span> | <span data-ttu-id="1a1fb-127">Value</span><span class="sxs-lookup"><span data-stu-id="1a1fb-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a1fb-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a1fb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1a1fb-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a1fb-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1a1fb-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a1fb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1a1fb-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a1fb-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1a1fb-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1a1fb-132">Namespace</span></span><br/>                | <span data-ttu-id="1a1fb-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1a1fb-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1a1fb-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1a1fb-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a1fb-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a1fb-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a1fb-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1a1fb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a1fb-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a1fb-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a1fb-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a1fb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a1fb-139">**Win32 \_ TSEnvironmentSetting**</span><span class="sxs-lookup"><span data-stu-id="1a1fb-139">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> </dl>

 

