---
title: Método SetClientProperty de la clase Win32_TSClientSetting
description: El método SetClientProperty establece la propiedad LPTPortMapping, COMPortMapping, AudioMapping, ClipboardMapping, DriveMapping o WindowsPrinterMapping para la clase.
ms.assetid: a8ad922f-d768-4708-9a67-c6b00580baed
ms.tgt_platform: multiple
keywords:
- Método SetClientProperty Servicios de Escritorio remoto
- Método SetClientProperty Servicios de Escritorio remoto, clase Win32_TSClientSetting
- Win32_TSClientSetting de clase Servicios de Escritorio remoto, método SetClientProperty
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetClientProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89bfdfd7c7f2c4b23f76b50ab671d74541f9dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676723"
---
# <a name="setclientproperty-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="bce78-106">Método SetClientProperty de la \_ clase TSClientSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="bce78-106">SetClientProperty method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="bce78-107">El método **SetClientProperty** establece la **propiedad LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping** o **WindowsPrinterMapping** para la clase.</span><span class="sxs-lookup"><span data-stu-id="bce78-107">The **SetClientProperty** method sets the **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping**, or **WindowsPrinterMapping** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="bce78-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bce78-108">Syntax</span></span>


```mof
uint32 SetClientProperty(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a><span data-ttu-id="bce78-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bce78-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bce78-110">*NombreDePropiedad* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bce78-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bce78-111">Especifica la propiedad de cliente que el método está estableciendo.</span><span class="sxs-lookup"><span data-stu-id="bce78-111">Specifies the client property that the method is setting.</span></span>

<dt>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>

<span data-ttu-id="bce78-112"><span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**AudioMapping**</span><span class="sxs-lookup"><span data-stu-id="bce78-112"><span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**AudioMapping**</span></span>


</dt> <dd>

<span data-ttu-id="bce78-113">El método está estableciendo la propiedad **AudioMapping** .</span><span class="sxs-lookup"><span data-stu-id="bce78-113">The method is setting the **AudioMapping** property.</span></span>

</dd> <dt>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>

<span data-ttu-id="bce78-114"><span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**ClipboardMapping**</span><span class="sxs-lookup"><span data-stu-id="bce78-114"><span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**ClipboardMapping**</span></span>


</dt> <dd>

<span data-ttu-id="bce78-115">El método está estableciendo la propiedad **ClipboardMapping** .</span><span class="sxs-lookup"><span data-stu-id="bce78-115">The method is setting the **ClipboardMapping** property.</span></span>

</dd> <dt>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>

<span data-ttu-id="bce78-116"><span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**COMPortMapping**</span><span class="sxs-lookup"><span data-stu-id="bce78-116"><span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**COMPortMapping**</span></span>


</dt> <dd>

<span data-ttu-id="bce78-117">El método está estableciendo la propiedad **COMPortMapping** .</span><span class="sxs-lookup"><span data-stu-id="bce78-117">The method is setting the **COMPortMapping** property.</span></span>

</dd> <dt>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>

<span data-ttu-id="bce78-118"><span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**DriveMapping**</span><span class="sxs-lookup"><span data-stu-id="bce78-118"><span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**DriveMapping**</span></span>


</dt> <dd>

<span data-ttu-id="bce78-119">El método está estableciendo la propiedad **DriveMapping** .</span><span class="sxs-lookup"><span data-stu-id="bce78-119">The method is setting the **DriveMapping** property.</span></span>

</dd> <dt>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>

<span data-ttu-id="bce78-120"><span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**LPTPortMapping**</span><span class="sxs-lookup"><span data-stu-id="bce78-120"><span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**LPTPortMapping**</span></span>


</dt> <dd>

<span data-ttu-id="bce78-121">El método está estableciendo la propiedad **LPTPortMapping** .</span><span class="sxs-lookup"><span data-stu-id="bce78-121">The method is setting the **LPTPortMapping** property.</span></span>

</dd> <dt>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>

<span data-ttu-id="bce78-122"><span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**PNPRedirection**</span><span class="sxs-lookup"><span data-stu-id="bce78-122"><span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**PNPRedirection**</span></span>


</dt> <dd>

<span data-ttu-id="bce78-123">El método está estableciendo la propiedad **PNPRedirection** .</span><span class="sxs-lookup"><span data-stu-id="bce78-123">The method is setting the **PNPRedirection** property.</span></span>

</dd> <dt>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>

<span data-ttu-id="bce78-124"><span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**WindowsPrinterMapping**</span><span class="sxs-lookup"><span data-stu-id="bce78-124"><span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**WindowsPrinterMapping**</span></span>


</dt> <dd>

<span data-ttu-id="bce78-125">El método está estableciendo la propiedad **WindowsPrinterMapping** .</span><span class="sxs-lookup"><span data-stu-id="bce78-125">The method is setting the **WindowsPrinterMapping** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bce78-126">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="bce78-126">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bce78-127">Valor que indica si se debe habilitar o deshabilitar la propiedad especificada por el parámetro *PropertyName* .</span><span class="sxs-lookup"><span data-stu-id="bce78-127">Value that indicates whether to enable or disable the property specified by the *PropertyName* parameter.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="bce78-128"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="bce78-128"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="bce78-129">Deshabilite la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bce78-129">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="bce78-130"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="bce78-130"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="bce78-131">Habilite la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bce78-131">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bce78-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bce78-132">Return value</span></span>

<span data-ttu-id="bce78-133">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="bce78-133">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="bce78-134">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="bce78-134">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="bce78-135">El método devuelve un error si la propiedad de cliente especificada no está bajo el control de directiva de grupo o si la configuración de la propiedad no es válida para la invalidación por parte del servidor.</span><span class="sxs-lookup"><span data-stu-id="bce78-135">The method returns an error if the specified client property is not under group policy control or if the property setting is not eligible for override by the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="bce78-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bce78-136">Remarks</span></span>

<span data-ttu-id="bce78-137">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bce78-137">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bce78-138">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bce78-138">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bce78-139">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="bce78-139">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bce78-140">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bce78-140">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bce78-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bce78-141">Requirements</span></span>



| <span data-ttu-id="bce78-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="bce78-142">Requirement</span></span> | <span data-ttu-id="bce78-143">Value</span><span class="sxs-lookup"><span data-stu-id="bce78-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bce78-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bce78-144">Minimum supported client</span></span><br/> | <span data-ttu-id="bce78-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bce78-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bce78-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bce78-146">Minimum supported server</span></span><br/> | <span data-ttu-id="bce78-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bce78-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bce78-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bce78-148">Namespace</span></span><br/>                | <span data-ttu-id="bce78-149">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="bce78-149">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="bce78-150">MOF</span><span class="sxs-lookup"><span data-stu-id="bce78-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bce78-151"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bce78-151"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="bce78-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bce78-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bce78-153"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bce78-153"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bce78-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="bce78-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bce78-155">**Win32 \_ TSClientSetting**</span><span class="sxs-lookup"><span data-stu-id="bce78-155">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

