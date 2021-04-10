---
title: Método SetSessionDirectoryExposeServerIP de la clase Win32_TSSessionDirectory
description: Establece la propiedad SessionDirectoryExposeServerIP.
ms.assetid: ae9a0c72-0a0a-42a0-a233-13da1efe60ef
ms.tgt_platform: multiple
keywords:
- Método SetSessionDirectoryExposeServerIP Servicios de Escritorio remoto
- Método SetSessionDirectoryExposeServerIP Servicios de Escritorio remoto, clase Win32_TSSessionDirectory
- Win32_TSSessionDirectory de clase Servicios de Escritorio remoto, método SetSessionDirectoryExposeServerIP
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryExposeServerIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc03f175e780d63eed3881b9146116702a30a02a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996246"
---
# <a name="setsessiondirectoryexposeserverip-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="40f5f-106">Método SetSessionDirectoryExposeServerIP de la \_ clase TSSessionDirectory de Win32</span><span class="sxs-lookup"><span data-stu-id="40f5f-106">SetSessionDirectoryExposeServerIP method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="40f5f-107">Establece la propiedad **SessionDirectoryExposeServerIP** .</span><span class="sxs-lookup"><span data-stu-id="40f5f-107">Sets the **SessionDirectoryExposeServerIP** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="40f5f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40f5f-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryExposeServerIP(
  [in] uint32 SessionDirectoryExposeServerIP
);
```



## <a name="parameters"></a><span data-ttu-id="40f5f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40f5f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40f5f-110">*SessionDirectoryExposeServerIP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="40f5f-110">*SessionDirectoryExposeServerIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40f5f-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40f5f-111">Type: **uint32**</span></span>

<span data-ttu-id="40f5f-112">Marca que deshabilita o habilita la propiedad **SessionDirectoryExposeServerIP** , que permite o deniega la recuperación de la dirección IP para el directorio de sesión.</span><span class="sxs-lookup"><span data-stu-id="40f5f-112">Flag disabling or enabling the **SessionDirectoryExposeServerIP** property which allows or denies retrieval of the IP address for the session directory.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="40f5f-113"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="40f5f-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="40f5f-114">Deshabilite la propiedad.</span><span class="sxs-lookup"><span data-stu-id="40f5f-114">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="40f5f-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="40f5f-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="40f5f-116">Habilite la propiedad.</span><span class="sxs-lookup"><span data-stu-id="40f5f-116">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40f5f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40f5f-117">Return value</span></span>

<span data-ttu-id="40f5f-118">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40f5f-118">Type: **uint32**</span></span>

<span data-ttu-id="40f5f-119">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="40f5f-119">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="40f5f-120">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="40f5f-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="40f5f-121">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="40f5f-121">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="40f5f-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40f5f-122">Remarks</span></span>

<span data-ttu-id="40f5f-123">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="40f5f-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="40f5f-124">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="40f5f-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="40f5f-125">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="40f5f-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="40f5f-126">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="40f5f-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="40f5f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40f5f-127">Requirements</span></span>



| <span data-ttu-id="40f5f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="40f5f-128">Requirement</span></span> | <span data-ttu-id="40f5f-129">Value</span><span class="sxs-lookup"><span data-stu-id="40f5f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40f5f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40f5f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="40f5f-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="40f5f-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="40f5f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40f5f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="40f5f-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40f5f-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40f5f-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="40f5f-134">Namespace</span></span><br/>                | <span data-ttu-id="40f5f-135">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="40f5f-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="40f5f-136">MOF</span><span class="sxs-lookup"><span data-stu-id="40f5f-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40f5f-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40f5f-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="40f5f-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="40f5f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40f5f-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40f5f-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40f5f-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="40f5f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40f5f-141">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="40f5f-141">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

