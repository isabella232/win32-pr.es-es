---
title: Método SetDisableForcibleLogoff de la Win32_TerminalServiceSetting clase
description: 'Método SetDisableForcibleLogoff de la Win32_TerminalServiceSetting clase : este método no se admite.'
ms.assetid: 1b7ac0f2-c242-4ca8-bc4d-8111e63851eb
ms.tgt_platform: multiple
keywords:
- Método SetDisableForcibleLogoff Servicios de Escritorio remoto
- Método SetDisableForcibleLogoff Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto , método SetDisableForcibleLogoff
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetDisableForcibleLogoff
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4be6ace10853ec282f5ab17b1f5f5921ef2c0d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103713"
---
# <a name="setdisableforciblelogoff-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="520ce-106">Método SetDisableForcibleLogoff de la clase \_ TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="520ce-106">SetDisableForcibleLogoff method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="520ce-107">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="520ce-107">This method is not supported.</span></span>

<span data-ttu-id="520ce-108">**Windows Vista y Windows Server 2008:** Habilita o deshabilita si un administrador que ha iniciado sesión en la consola se puede desactivar forzadamente.</span><span class="sxs-lookup"><span data-stu-id="520ce-108">**Windows Vista and Windows Server 2008:** Enables or disables whether an administrator logged onto the console can be forcibly logged off.</span></span>

## <a name="syntax"></a><span data-ttu-id="520ce-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="520ce-109">Syntax</span></span>


```mof
uint32 SetDisableForcibleLogoff(
  [in] uint32 DisableForcibleLogoff
);
```



## <a name="parameters"></a><span data-ttu-id="520ce-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="520ce-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="520ce-111">*DisableForcibleLogoff* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="520ce-111">*DisableForcibleLogoff* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520ce-112">Marca la deshabilitación o habilitación de la propiedad **DisableForcibleLogoff,** que determina si un administrador que ha iniciado sesión en la consola se puede desactivar forzosamente.</span><span class="sxs-lookup"><span data-stu-id="520ce-112">Flag disabling or enabling the **DisableForcibleLogoff** property, which determines whether an administrator that is logged on to the console can be forcibly logged off.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="520ce-113"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="520ce-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="520ce-114">Deshabilite la propiedad .</span><span class="sxs-lookup"><span data-stu-id="520ce-114">Disable the property.</span></span> <span data-ttu-id="520ce-115">El administrador conectado puede estar cerrado forzadamente.</span><span class="sxs-lookup"><span data-stu-id="520ce-115">The connected administrator can be forcibly logged off.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="520ce-116"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="520ce-116"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="520ce-117">Habilite la propiedad .</span><span class="sxs-lookup"><span data-stu-id="520ce-117">Enable the property.</span></span> <span data-ttu-id="520ce-118">El administrador conectado no se puede desactivar forzadamente.</span><span class="sxs-lookup"><span data-stu-id="520ce-118">The connected administrator cannot be forcibly logged off.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="520ce-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="520ce-119">Return value</span></span>

<span data-ttu-id="520ce-120">Devuelve Success si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi.</span><span class="sxs-lookup"><span data-stu-id="520ce-120">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="520ce-121">Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="520ce-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="520ce-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="520ce-122">Requirements</span></span>



| <span data-ttu-id="520ce-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="520ce-123">Requirement</span></span> | <span data-ttu-id="520ce-124">Valor</span><span class="sxs-lookup"><span data-stu-id="520ce-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="520ce-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="520ce-125">Minimum supported client</span></span><br/> | <span data-ttu-id="520ce-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520ce-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="520ce-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="520ce-127">Minimum supported server</span></span><br/> | <span data-ttu-id="520ce-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="520ce-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="520ce-129">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="520ce-129">End of client support</span></span><br/>    | <span data-ttu-id="520ce-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="520ce-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="520ce-131">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="520ce-131">End of server support</span></span><br/>    | <span data-ttu-id="520ce-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="520ce-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="520ce-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="520ce-133">Namespace</span></span><br/>                | <span data-ttu-id="520ce-134">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="520ce-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="520ce-135">MOF</span><span class="sxs-lookup"><span data-stu-id="520ce-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="520ce-136"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="520ce-136"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="520ce-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="520ce-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="520ce-138"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="520ce-138"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="520ce-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="520ce-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="520ce-140">**TerminalServiceSetting de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="520ce-140">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





