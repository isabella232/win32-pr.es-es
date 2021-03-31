---
title: Método SetDisableForcibleLogoff de la clase Win32_TerminalServiceSetting
description: No se admite este método.
ms.assetid: 1b7ac0f2-c242-4ca8-bc4d-8111e63851eb
ms.tgt_platform: multiple
keywords:
- Método SetDisableForcibleLogoff Servicios de Escritorio remoto
- Método SetDisableForcibleLogoff Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método SetDisableForcibleLogoff
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
ms.openlocfilehash: d4ae62db188d0e3aa31ffd8e3993e793e9bb2bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490295"
---
# <a name="setdisableforciblelogoff-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="6823b-106">Método SetDisableForcibleLogoff de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="6823b-106">SetDisableForcibleLogoff method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="6823b-107">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="6823b-107">This method is not supported.</span></span>

<span data-ttu-id="6823b-108">**Windows Vista y Windows Server 2008:** Habilita o deshabilita si un administrador que ha iniciado sesión en la consola de se puede cerrar la sesión forzosamente.</span><span class="sxs-lookup"><span data-stu-id="6823b-108">**Windows Vista and Windows Server 2008:** Enables or disables whether an administrator logged onto the console can be forcibly logged off.</span></span>

## <a name="syntax"></a><span data-ttu-id="6823b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6823b-109">Syntax</span></span>


```mof
uint32 SetDisableForcibleLogoff(
  [in] uint32 DisableForcibleLogoff
);
```



## <a name="parameters"></a><span data-ttu-id="6823b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6823b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6823b-111">*DisableForcibleLogoff* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6823b-111">*DisableForcibleLogoff* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6823b-112">Marca que deshabilita o habilita la propiedad **DisableForcibleLogoff** , que determina si un administrador que ha iniciado sesión en la consola puede cerrar la sesión con fuerza.</span><span class="sxs-lookup"><span data-stu-id="6823b-112">Flag disabling or enabling the **DisableForcibleLogoff** property, which determines whether an administrator that is logged on to the console can be forcibly logged off.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="6823b-113"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="6823b-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="6823b-114">Deshabilite la propiedad.</span><span class="sxs-lookup"><span data-stu-id="6823b-114">Disable the property.</span></span> <span data-ttu-id="6823b-115">El administrador conectado puede cerrar la sesión con fuerza.</span><span class="sxs-lookup"><span data-stu-id="6823b-115">The connected administrator can be forcibly logged off.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="6823b-116"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="6823b-116"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="6823b-117">Habilite la propiedad.</span><span class="sxs-lookup"><span data-stu-id="6823b-117">Enable the property.</span></span> <span data-ttu-id="6823b-118">No se puede cerrar la sesión del administrador conectado.</span><span class="sxs-lookup"><span data-stu-id="6823b-118">The connected administrator cannot be forcibly logged off.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6823b-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6823b-119">Return value</span></span>

<span data-ttu-id="6823b-120">Devuelve SUCCESS si se realiza correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="6823b-120">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="6823b-121">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="6823b-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="6823b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6823b-122">Requirements</span></span>



| <span data-ttu-id="6823b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6823b-123">Requirement</span></span> | <span data-ttu-id="6823b-124">Value</span><span class="sxs-lookup"><span data-stu-id="6823b-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6823b-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6823b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6823b-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6823b-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6823b-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6823b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6823b-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6823b-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6823b-129">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6823b-129">End of client support</span></span><br/>    | <span data-ttu-id="6823b-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6823b-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6823b-131">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="6823b-131">End of server support</span></span><br/>    | <span data-ttu-id="6823b-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6823b-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6823b-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6823b-133">Namespace</span></span><br/>                | <span data-ttu-id="6823b-134">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6823b-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6823b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="6823b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6823b-136"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6823b-136"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6823b-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6823b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6823b-138"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6823b-138"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6823b-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="6823b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6823b-140">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="6823b-140">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





