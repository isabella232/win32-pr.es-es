---
title: Método SetSingleSession de la clase Win32_TerminalServiceSetting
description: El método SetSingleSession establece la propiedad SingleSession para la clase.
ms.assetid: 67ccfa9d-86a5-4501-9d61-c7f1677ec3d5
ms.tgt_platform: multiple
keywords:
- Método SetSingleSession Servicios de Escritorio remoto
- Método SetSingleSession Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método SetSingleSession
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSingleSession
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a6ff702020b7682938b7174c65623eba30076a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686159"
---
# <a name="setsinglesession-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="7a997-106">Método SetSingleSession de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="7a997-106">SetSingleSession method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="7a997-107">El método **SetSingleSession** establece la propiedad **SingleSession** para la clase.</span><span class="sxs-lookup"><span data-stu-id="7a997-107">The **SetSingleSession** method sets the **SingleSession** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a997-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a997-108">Syntax</span></span>


```mof
uint32 SetSingleSession(
  [in] uint32 SingleSession
);
```



## <a name="parameters"></a><span data-ttu-id="7a997-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a997-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a997-110">*SingleSession* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7a997-110">*SingleSession* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a997-111">Marca que deshabilita o habilita la propiedad **SingleSession** , que determina si los usuarios se limitan a una o varias sesiones de servicios de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="7a997-111">Flag disabling or enabling the **SingleSession** property, which determines whether users are limited to one or more Remote Desktop Services sessions.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="7a997-112"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="7a997-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="7a997-113">Deshabilite la propiedad.</span><span class="sxs-lookup"><span data-stu-id="7a997-113">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="7a997-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="7a997-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="7a997-115">Habilite la propiedad.</span><span class="sxs-lookup"><span data-stu-id="7a997-115">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a997-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a997-116">Return value</span></span>

<span data-ttu-id="7a997-117">Devuelve SUCCESS si es correcto; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="7a997-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="7a997-118">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="7a997-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a997-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a997-119">Remarks</span></span>

<span data-ttu-id="7a997-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7a997-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7a997-121">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7a997-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7a997-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="7a997-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7a997-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7a997-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a997-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a997-124">Requirements</span></span>



| <span data-ttu-id="7a997-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a997-125">Requirement</span></span> | <span data-ttu-id="7a997-126">Value</span><span class="sxs-lookup"><span data-stu-id="7a997-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a997-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a997-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7a997-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a997-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7a997-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a997-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7a997-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a997-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7a997-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7a997-131">Namespace</span></span><br/>                | <span data-ttu-id="7a997-132">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="7a997-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7a997-133">MOF</span><span class="sxs-lookup"><span data-stu-id="7a997-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a997-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a997-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a997-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7a997-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a997-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a997-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a997-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a997-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a997-138">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="7a997-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

