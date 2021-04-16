---
title: Método SetPromptForPassword de la clase Win32_TSLogonSetting
description: El método SetPromptForPassword establece la propiedad PromptForPassword.
ms.assetid: eeeed374-4a8a-4014-833c-d931be3ef455
ms.tgt_platform: multiple
keywords:
- Método SetPromptForPassword Servicios de Escritorio remoto
- Método SetPromptForPassword Servicios de Escritorio remoto, clase Win32_TSLogonSetting
- Win32_TSLogonSetting de clase Servicios de Escritorio remoto, método SetPromptForPassword
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.SetPromptForPassword
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86dc065a143505ea81bce78d9bf787fae6b0a33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676837"
---
# <a name="setpromptforpassword-method-of-the-win32_tslogonsetting-class"></a><span data-ttu-id="d8208-106">Método SetPromptForPassword de la \_ clase TSLogonSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="d8208-106">SetPromptForPassword method of the Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="d8208-107">El método **SetPromptForPassword** establece la propiedad **PromptForPassword** .</span><span class="sxs-lookup"><span data-stu-id="d8208-107">The **SetPromptForPassword** method sets the **PromptForPassword** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8208-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8208-108">Syntax</span></span>


```mof
uint32 SetPromptForPassword(
  [in] uint32 PromptForPassword
);
```



## <a name="parameters"></a><span data-ttu-id="d8208-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8208-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8208-110">*PromptForPassword* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d8208-110">*PromptForPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8208-111">Marca que deshabilita o habilita la propiedad **PromptForPassword** .</span><span class="sxs-lookup"><span data-stu-id="d8208-111">Flag disabling or enabling the **PromptForPassword** property.</span></span>

<dt>

<span data-ttu-id="d8208-112">0</span><span class="sxs-lookup"><span data-stu-id="d8208-112">0</span></span>
</dt> <dd>

<span data-ttu-id="d8208-113">Deshabilita la solicitud de contraseña.</span><span class="sxs-lookup"><span data-stu-id="d8208-113">Disables password-prompting.</span></span>

</dd> <dt>

<span data-ttu-id="d8208-114">1</span><span class="sxs-lookup"><span data-stu-id="d8208-114">1</span></span>
</dt> <dd>

<span data-ttu-id="d8208-115">Habilita la solicitud de contraseña.</span><span class="sxs-lookup"><span data-stu-id="d8208-115">Enables password-prompting.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8208-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8208-116">Return value</span></span>

<span data-ttu-id="d8208-117">Devuelve SUCCESS si es correcto; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="d8208-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="d8208-118">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="d8208-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="d8208-119">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="d8208-119">The method returns an error if the setting is under group policy control.</span></span>

<dl> <dt>

<span data-ttu-id="d8208-120">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="d8208-120">**FALSE** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d8208-121">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="d8208-121">**TRUE** (1)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="d8208-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8208-122">Remarks</span></span>

<span data-ttu-id="d8208-123">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d8208-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d8208-124">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d8208-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d8208-125">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d8208-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d8208-126">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d8208-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8208-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8208-127">Requirements</span></span>



| <span data-ttu-id="d8208-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8208-128">Requirement</span></span> | <span data-ttu-id="d8208-129">Value</span><span class="sxs-lookup"><span data-stu-id="d8208-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8208-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8208-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d8208-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8208-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d8208-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8208-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d8208-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8208-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d8208-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d8208-134">Namespace</span></span><br/>                | <span data-ttu-id="d8208-135">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d8208-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d8208-136">MOF</span><span class="sxs-lookup"><span data-stu-id="d8208-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8208-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8208-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8208-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d8208-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8208-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8208-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8208-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8208-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8208-141">**Win32 \_ TSLogonSetting**</span><span class="sxs-lookup"><span data-stu-id="d8208-141">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> </dl>

 

