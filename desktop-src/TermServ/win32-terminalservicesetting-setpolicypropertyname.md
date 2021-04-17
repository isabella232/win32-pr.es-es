---
title: Método SetPolicyPropertyName de la clase Win32_TerminalServiceSetting
description: El método SetPolicyPropertyName establece la propiedad DeleteTempFolders, UseTempFolders o help para la clase.
ms.assetid: 18d9927a-b7db-46c7-90ee-00da6de06202
ms.tgt_platform: multiple
keywords:
- Método SetPolicyPropertyName Servicios de Escritorio remoto
- Método SetPolicyPropertyName Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método SetPolicyPropertyName
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPolicyPropertyName
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f49732fa916dd3c37539dc35d6cef7a4d920d81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492724"
---
# <a name="setpolicypropertyname-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="25473-106">Método SetPolicyPropertyName de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="25473-106">SetPolicyPropertyName method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="25473-107">El método **SetPolicyPropertyName** establece la propiedad **DeleteTempFolders**, **UseTempFolders** o **Help** para la clase.</span><span class="sxs-lookup"><span data-stu-id="25473-107">The **SetPolicyPropertyName** method sets the **DeleteTempFolders**, **UseTempFolders** or **Help** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="25473-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25473-108">Syntax</span></span>


```mof
uint32 SetPolicyPropertyName(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a><span data-ttu-id="25473-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25473-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25473-110">*NombreDePropiedad* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="25473-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25473-111">Especifica la propiedad de directiva que el método está estableciendo.</span><span class="sxs-lookup"><span data-stu-id="25473-111">Specifies the policy property that the method is setting.</span></span>

<dt>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>

<span data-ttu-id="25473-112"><span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**DeleteTempFolders**</span><span class="sxs-lookup"><span data-stu-id="25473-112"><span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**DeleteTempFolders**</span></span>


</dt> <dd>

<span data-ttu-id="25473-113">El método está estableciendo la propiedad **DeleteTempFolders** .</span><span class="sxs-lookup"><span data-stu-id="25473-113">The method is setting the **DeleteTempFolders** property.</span></span>

</dd> <dt>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>

<span data-ttu-id="25473-114"><span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**UseTempFolders**</span><span class="sxs-lookup"><span data-stu-id="25473-114"><span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**UseTempFolders**</span></span>


</dt> <dd>

<span data-ttu-id="25473-115">El método está estableciendo la propiedad **UseTempFolders** .</span><span class="sxs-lookup"><span data-stu-id="25473-115">The method is setting the **UseTempFolders** property.</span></span>

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>

<span data-ttu-id="25473-116"><span id="Help"></span><span id="help"></span><span id="HELP"></span>**Ayuda**</span><span class="sxs-lookup"><span data-stu-id="25473-116"><span id="Help"></span><span id="help"></span><span id="HELP"></span>**Help**</span></span>


</dt> <dd>

<span data-ttu-id="25473-117">El método está estableciendo la propiedad **Help** .</span><span class="sxs-lookup"><span data-stu-id="25473-117">The method is setting the **Help** property.</span></span>

<span data-ttu-id="25473-118">**Nota:** no se admite la **ayuda**  </span><span class="sxs-lookup"><span data-stu-id="25473-118">**Note**  **Help** is not supported</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="25473-119">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="25473-119">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25473-120">Valor que indica si se debe habilitar o deshabilitar la propiedad especificada por el parámetro *PropertyName* .</span><span class="sxs-lookup"><span data-stu-id="25473-120">Value that indicates whether to enable or disable the property specified by the *PropertyName* parameter.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="25473-121"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="25473-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="25473-122">Deshabilite la propiedad.</span><span class="sxs-lookup"><span data-stu-id="25473-122">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="25473-123"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="25473-123"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="25473-124">Habilite la propiedad.</span><span class="sxs-lookup"><span data-stu-id="25473-124">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25473-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25473-125">Return value</span></span>

<span data-ttu-id="25473-126">Devuelve SUCCESS si es correcto; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="25473-126">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="25473-127">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="25473-127">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="25473-128">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="25473-128">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="25473-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25473-129">Remarks</span></span>

<span data-ttu-id="25473-130">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="25473-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="25473-131">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="25473-131">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="25473-132">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="25473-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="25473-133">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="25473-133">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="25473-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25473-134">Requirements</span></span>



| <span data-ttu-id="25473-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="25473-135">Requirement</span></span> | <span data-ttu-id="25473-136">Value</span><span class="sxs-lookup"><span data-stu-id="25473-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25473-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25473-137">Minimum supported client</span></span><br/> | <span data-ttu-id="25473-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25473-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="25473-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25473-139">Minimum supported server</span></span><br/> | <span data-ttu-id="25473-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25473-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="25473-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="25473-141">Namespace</span></span><br/>                | <span data-ttu-id="25473-142">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="25473-142">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="25473-143">MOF</span><span class="sxs-lookup"><span data-stu-id="25473-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25473-144"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25473-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="25473-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="25473-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25473-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25473-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25473-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="25473-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25473-148">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="25473-148">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

