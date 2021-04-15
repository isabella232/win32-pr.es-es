---
title: Método SetAllowDwm de la clase Win32_TSClientSetting
description: Establece la propiedad AllowDwm.
ms.assetid: c70d3dc9-c109-4d77-be50-20a0352282d6
ms.tgt_platform: multiple
keywords:
- Método SetAllowDwm Servicios de Escritorio remoto
- Método SetAllowDwm Servicios de Escritorio remoto, clase Win32_TSClientSetting
- Win32_TSClientSetting de clase Servicios de Escritorio remoto, método SetAllowDwm
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetAllowDwm
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39441ba3244f206b057ba47c3cb6f765b5e80604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676731"
---
# <a name="setallowdwm-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="8a1da-106">Método SetAllowDwm de la \_ clase TSClientSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="8a1da-106">SetAllowDwm method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="8a1da-107">Establece la propiedad **AllowDwm** .</span><span class="sxs-lookup"><span data-stu-id="8a1da-107">Sets the **AllowDwm** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a1da-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a1da-108">Syntax</span></span>


```mof
uint32 SetAllowDwm(
  [in] uint32 AllowDwm
);
```



## <a name="parameters"></a><span data-ttu-id="8a1da-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a1da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a1da-110">*AllowDwm* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a1da-110">*AllowDwm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a1da-111">Nuevo valor de la propiedad **AllowDwm** .</span><span class="sxs-lookup"><span data-stu-id="8a1da-111">The new **AllowDwm** property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a1da-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a1da-112">Return value</span></span>

<span data-ttu-id="8a1da-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="8a1da-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="8a1da-114">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="8a1da-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="8a1da-115">El método devuelve un error si el servidor invalida la configuración de conexión del usuario.</span><span class="sxs-lookup"><span data-stu-id="8a1da-115">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a1da-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a1da-116">Requirements</span></span>



| <span data-ttu-id="8a1da-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a1da-117">Requirement</span></span> | <span data-ttu-id="8a1da-118">Value</span><span class="sxs-lookup"><span data-stu-id="8a1da-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1da-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a1da-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8a1da-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8a1da-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8a1da-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a1da-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8a1da-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8a1da-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="8a1da-123">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8a1da-123">End of client support</span></span><br/>    | <span data-ttu-id="8a1da-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8a1da-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8a1da-125">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="8a1da-125">End of server support</span></span><br/>    | <span data-ttu-id="8a1da-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8a1da-126">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="8a1da-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8a1da-127">Namespace</span></span><br/>                | <span data-ttu-id="8a1da-128">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8a1da-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8a1da-129">MOF</span><span class="sxs-lookup"><span data-stu-id="8a1da-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a1da-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a1da-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a1da-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a1da-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a1da-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a1da-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a1da-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a1da-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a1da-134">**Win32 \_ TSClientSetting**</span><span class="sxs-lookup"><span data-stu-id="8a1da-134">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





