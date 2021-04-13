---
title: Método RegisterVMMPlugin de la clase Win32_SessionDirectoryVMMPlugin
description: Registra un nuevo complemento de VMM.
ms.assetid: 8fa6109e-6320-4ad1-b313-f100d8383f85
ms.tgt_platform: multiple
keywords:
- Método RegisterVMMPlugin Servicios de Escritorio remoto
- Método RegisterVMMPlugin Servicios de Escritorio remoto, clase Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin de clase Servicios de Escritorio remoto, método RegisterVMMPlugin
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.RegisterVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381be34f9398147b323fa99093479da48adfd480
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422123"
---
# <a name="registervmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="fabab-106">Método RegisterVMMPlugin de la \_ clase SessionDirectoryVMMPlugin de Win32</span><span class="sxs-lookup"><span data-stu-id="fabab-106">RegisterVMMPlugin method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="fabab-107">Registra un nuevo complemento de VMM.</span><span class="sxs-lookup"><span data-stu-id="fabab-107">Registers a new VMM plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="fabab-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fabab-108">Syntax</span></span>


```mof
uint32 RegisterVMMPlugin(
  [in] string  sName,
  [in] string  sProvider,
  [in] string  sServiceLocation,
  [in] string  sClassID,
  [in] sint32  Priority = ,
  [in] boolean Enabled = 
);
```



## <a name="parameters"></a><span data-ttu-id="fabab-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fabab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fabab-110">*sName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fabab-110">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fabab-111">Nombre del complemento.</span><span class="sxs-lookup"><span data-stu-id="fabab-111">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="fabab-112">*sProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fabab-112">*sProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fabab-113">Nombre del proveedor del complemento.</span><span class="sxs-lookup"><span data-stu-id="fabab-113">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="fabab-114">*sServiceLocation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fabab-114">*sServiceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fabab-115">La ubicación del servicio en la que debe ponerse en contacto el complemento.</span><span class="sxs-lookup"><span data-stu-id="fabab-115">The service location that the plug-in should contact.</span></span>

</dd> <dt>

<span data-ttu-id="fabab-116">*sClassID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fabab-116">*sClassID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fabab-117">Identificador de clase del complemento.</span><span class="sxs-lookup"><span data-stu-id="fabab-117">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="fabab-118">*Prioridad* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fabab-118">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fabab-119">Prioridad del complemento.</span><span class="sxs-lookup"><span data-stu-id="fabab-119">The priority of the plug-in.</span></span> <span data-ttu-id="fabab-120">Cuanto mayor sea el valor, mayor será la prioridad del complemento.</span><span class="sxs-lookup"><span data-stu-id="fabab-120">The higher the value, the higher the priority of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="fabab-121">*Habilitado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fabab-121">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fabab-122">Indica si el complemento está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="fabab-122">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="fabab-123">**True** si el complemento está habilitado o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fabab-123">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fabab-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fabab-124">Return value</span></span>

<span data-ttu-id="fabab-125">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="fabab-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="fabab-126">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="fabab-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="fabab-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fabab-127">Requirements</span></span>



| <span data-ttu-id="fabab-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="fabab-128">Requirement</span></span> | <span data-ttu-id="fabab-129">Value</span><span class="sxs-lookup"><span data-stu-id="fabab-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fabab-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fabab-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fabab-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fabab-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fabab-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fabab-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fabab-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fabab-133">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="fabab-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fabab-134">Namespace</span></span><br/>                | <span data-ttu-id="fabab-135">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="fabab-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="fabab-136">MOF</span><span class="sxs-lookup"><span data-stu-id="fabab-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fabab-137"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fabab-137"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="fabab-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fabab-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fabab-139"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fabab-139"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fabab-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="fabab-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fabab-141">**Win32 \_ SessionDirectoryVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="fabab-141">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





