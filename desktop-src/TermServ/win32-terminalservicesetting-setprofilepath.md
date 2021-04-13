---
title: Método SetProfilePath de la clase Win32_TerminalServiceSetting
description: El método SetProfilePath establece la propiedad ProfilePath para la clase.
ms.assetid: a0dfe6a4-929c-45ec-bd31-7e0ffb6ce5de
ms.tgt_platform: multiple
keywords:
- Método SetProfilePath Servicios de Escritorio remoto
- Método SetProfilePath Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método SetProfilePath
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetProfilePath
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 434909471accc191e79c92287ab6e4ac427bf949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422255"
---
# <a name="setprofilepath-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="1f80a-106">Método SetProfilePath de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="1f80a-106">SetProfilePath method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="1f80a-107">El método **SetProfilePath** establece la propiedad **ProfilePath** para la clase.</span><span class="sxs-lookup"><span data-stu-id="1f80a-107">The **SetProfilePath** method sets the **ProfilePath** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f80a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f80a-108">Syntax</span></span>


```mof
uint32 SetProfilePath(
  [in] string ProfilePath
);
```



## <a name="parameters"></a><span data-ttu-id="1f80a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f80a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f80a-110">*ProfilePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1f80a-110">*ProfilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f80a-111">Nuevo valor de la propiedad **ProfilePath** , que especifica la ruta de acceso del perfil para el equipo.</span><span class="sxs-lookup"><span data-stu-id="1f80a-111">The new value for the **ProfilePath** property, which specifies the profile path for the computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f80a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f80a-112">Return value</span></span>

<span data-ttu-id="1f80a-113">Devuelve SUCCESS si es correcto; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="1f80a-113">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="1f80a-114">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="1f80a-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f80a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f80a-115">Remarks</span></span>

<span data-ttu-id="1f80a-116">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1f80a-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1f80a-117">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1f80a-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1f80a-118">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="1f80a-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1f80a-119">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1f80a-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f80a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f80a-120">Requirements</span></span>



| <span data-ttu-id="1f80a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f80a-121">Requirement</span></span> | <span data-ttu-id="1f80a-122">Value</span><span class="sxs-lookup"><span data-stu-id="1f80a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f80a-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f80a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1f80a-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f80a-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1f80a-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f80a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1f80a-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f80a-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1f80a-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1f80a-127">Namespace</span></span><br/>                | <span data-ttu-id="1f80a-128">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1f80a-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1f80a-129">MOF</span><span class="sxs-lookup"><span data-stu-id="1f80a-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f80a-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f80a-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f80a-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1f80a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f80a-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f80a-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f80a-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f80a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f80a-134">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="1f80a-134">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

