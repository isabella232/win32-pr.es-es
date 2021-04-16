---
title: Método SetHomeDirectory de la clase Win32_TerminalServiceSetting
description: Establece la propiedad TerminalServicesHomeDirectory para la clase.
ms.assetid: 8173cd5b-965e-41bc-97cf-70d8729b8cea
ms.tgt_platform: multiple
keywords:
- Método SetHomeDirectory Servicios de Escritorio remoto
- Método SetHomeDirectory Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método SetHomeDirectory
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetHomeDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1be732cae76b0681afd77693a07f673ef37c4a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534065"
---
# <a name="sethomedirectory-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="8fd54-106">Método SetHomeDirectory de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="8fd54-106">SetHomeDirectory method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="8fd54-107">El método **SetHomeDirectory** establece la propiedad **TerminalServicesHomeDirectory** para la clase.</span><span class="sxs-lookup"><span data-stu-id="8fd54-107">The **SetHomeDirectory** method sets the **TerminalServicesHomeDirectory** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fd54-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8fd54-108">Syntax</span></span>


```mof
uint32 SetHomeDirectory(
  [in] string HomeDirectory
);
```



## <a name="parameters"></a><span data-ttu-id="8fd54-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8fd54-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fd54-110">*HomeDirectory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8fd54-110">*HomeDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fd54-111">Nuevo valor de la propiedad **TerminalServicesHomeDirectory** , que especifica el directorio raíz del equipo.</span><span class="sxs-lookup"><span data-stu-id="8fd54-111">The new value for the **TerminalServicesHomeDirectory** property, which specifies the computer's root directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fd54-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8fd54-112">Return value</span></span>

<span data-ttu-id="8fd54-113">Devuelve SUCCESS si se realiza correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="8fd54-113">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="8fd54-114">Para obtener una lista de códigos de error de WMI, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8fd54-114">For a list of WMI error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8fd54-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8fd54-115">Remarks</span></span>

<span data-ttu-id="8fd54-116">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8fd54-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8fd54-117">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8fd54-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8fd54-118">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="8fd54-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8fd54-119">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8fd54-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8fd54-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fd54-120">Requirements</span></span>



| <span data-ttu-id="8fd54-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fd54-121">Requirement</span></span> | <span data-ttu-id="8fd54-122">Value</span><span class="sxs-lookup"><span data-stu-id="8fd54-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fd54-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8fd54-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8fd54-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8fd54-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8fd54-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8fd54-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8fd54-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fd54-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8fd54-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8fd54-127">Namespace</span></span><br/>                | <span data-ttu-id="8fd54-128">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8fd54-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8fd54-129">MOF</span><span class="sxs-lookup"><span data-stu-id="8fd54-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fd54-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fd54-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fd54-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8fd54-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fd54-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fd54-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fd54-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fd54-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fd54-134">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="8fd54-134">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

