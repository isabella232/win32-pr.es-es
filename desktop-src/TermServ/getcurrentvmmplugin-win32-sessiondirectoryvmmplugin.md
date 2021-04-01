---
title: Método GetCurrentVMMPlugin de la clase Win32_SessionDirectoryVMMPlugin
description: Obtiene el complemento de prioridad máxima que está habilitado.
ms.assetid: 7712573f-2252-4a3c-820c-b679be5dfd46
ms.tgt_platform: multiple
keywords:
- Método GetCurrentVMMPlugin Servicios de Escritorio remoto
- Método GetCurrentVMMPlugin Servicios de Escritorio remoto, clase Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin de clase Servicios de Escritorio remoto, método GetCurrentVMMPlugin
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.GetCurrentVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7162322f4e5e3939309d64e27c93cf8d20da540c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905615"
---
# <a name="getcurrentvmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="0a762-106">Método GetCurrentVMMPlugin de la \_ clase SessionDirectoryVMMPlugin de Win32</span><span class="sxs-lookup"><span data-stu-id="0a762-106">GetCurrentVMMPlugin method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="0a762-107">Obtiene el complemento de prioridad máxima que está habilitado.</span><span class="sxs-lookup"><span data-stu-id="0a762-107">Gets the highest priority plug-in that is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a762-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a762-108">Syntax</span></span>


```mof
uint32 GetCurrentVMMPlugin(
  [out] string  sName,
  [out] string  sProvider,
  [out] string  sServiceLocation,
  [out] string  sClassID,
  [out] sint32  Priority,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="0a762-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a762-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a762-110">*sName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0a762-110">*sName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a762-111">Nombre del complemento.</span><span class="sxs-lookup"><span data-stu-id="0a762-111">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="0a762-112">*sProvider* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0a762-112">*sProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a762-113">Nombre del proveedor del complemento.</span><span class="sxs-lookup"><span data-stu-id="0a762-113">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="0a762-114">*sServiceLocation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0a762-114">*sServiceLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a762-115">La ubicación del servicio en la que debe ponerse en contacto el complemento.</span><span class="sxs-lookup"><span data-stu-id="0a762-115">The service location that the plug-in should contact.</span></span>

</dd> <dt>

<span data-ttu-id="0a762-116">*sClassID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0a762-116">*sClassID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a762-117">Identificador de clase del complemento.</span><span class="sxs-lookup"><span data-stu-id="0a762-117">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="0a762-118">*Prioridad* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0a762-118">*Priority* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a762-119">Prioridad del complemento.</span><span class="sxs-lookup"><span data-stu-id="0a762-119">The priority of the plug-in.</span></span> <span data-ttu-id="0a762-120">Cuanto mayor sea el valor, mayor será la prioridad del complemento.</span><span class="sxs-lookup"><span data-stu-id="0a762-120">The higher the value, the higher the priority of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="0a762-121">*Habilitado* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0a762-121">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a762-122">Indica si el complemento está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="0a762-122">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="0a762-123">**True** si el complemento está habilitado o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0a762-123">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a762-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a762-124">Return value</span></span>

<span data-ttu-id="0a762-125">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="0a762-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0a762-126">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0a762-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a762-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a762-127">Requirements</span></span>



| <span data-ttu-id="0a762-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a762-128">Requirement</span></span> | <span data-ttu-id="0a762-129">Value</span><span class="sxs-lookup"><span data-stu-id="0a762-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a762-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a762-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0a762-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0a762-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0a762-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a762-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0a762-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0a762-133">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="0a762-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0a762-134">Namespace</span></span><br/>                | <span data-ttu-id="0a762-135">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0a762-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="0a762-136">MOF</span><span class="sxs-lookup"><span data-stu-id="0a762-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a762-137"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a762-137"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a762-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0a762-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a762-139"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a762-139"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a762-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a762-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a762-141">**Win32 \_ SessionDirectoryVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="0a762-141">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





