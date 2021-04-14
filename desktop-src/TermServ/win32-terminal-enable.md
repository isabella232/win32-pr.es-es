---
title: Método enable de la clase Win32_Terminal
description: El método enable deshabilita o habilita el terminal.
ms.assetid: f249563b-6fa0-413c-9fc7-01dd16d5c561
ms.tgt_platform: multiple
keywords:
- Habilitar Servicios de Escritorio remoto de método
- Habilitar Servicios de Escritorio remoto de método, clase de Win32_Terminal
- Servicios de Escritorio remoto de clase Win32_Terminal, método enable
topic_type:
- apiref
api_name:
- Win32_Terminal.Enable
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afedef572c65f249c48da850172bb9fc4d222c19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422057"
---
# <a name="enable-method-of-the-win32_terminal-class"></a><span data-ttu-id="9af2b-106">Método enable de la \_ clase de terminal Win32</span><span class="sxs-lookup"><span data-stu-id="9af2b-106">Enable method of the Win32\_Terminal class</span></span>

<span data-ttu-id="9af2b-107">El método **enable** deshabilita o habilita el terminal.</span><span class="sxs-lookup"><span data-stu-id="9af2b-107">The **Enable** method disables or enables the terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="9af2b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9af2b-108">Syntax</span></span>


```mof
uint32 Enable(
  [in] uint32 fEnableTerminal
);
```



## <a name="parameters"></a><span data-ttu-id="9af2b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9af2b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9af2b-110">*fEnableTerminal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9af2b-110">*fEnableTerminal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9af2b-111">Marca que deshabilita o habilita el terminal.</span><span class="sxs-lookup"><span data-stu-id="9af2b-111">Flag that disables or enables the terminal.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="9af2b-112"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="9af2b-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="9af2b-113">El terminal está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="9af2b-113">The terminal is disabled.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="9af2b-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="9af2b-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="9af2b-115">El terminal está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9af2b-115">The terminal is enabled.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9af2b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9af2b-116">Return value</span></span>

<span data-ttu-id="9af2b-117">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="9af2b-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="9af2b-118">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="9af2b-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="9af2b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9af2b-119">Remarks</span></span>

<span data-ttu-id="9af2b-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9af2b-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9af2b-121">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9af2b-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9af2b-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="9af2b-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9af2b-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9af2b-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9af2b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9af2b-124">Requirements</span></span>



| <span data-ttu-id="9af2b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9af2b-125">Requirement</span></span> | <span data-ttu-id="9af2b-126">Value</span><span class="sxs-lookup"><span data-stu-id="9af2b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9af2b-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9af2b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9af2b-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9af2b-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9af2b-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9af2b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9af2b-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9af2b-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9af2b-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9af2b-131">Namespace</span></span><br/>                | <span data-ttu-id="9af2b-132">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9af2b-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9af2b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="9af2b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9af2b-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9af2b-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9af2b-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9af2b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9af2b-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9af2b-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9af2b-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="9af2b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9af2b-138">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="9af2b-138">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

