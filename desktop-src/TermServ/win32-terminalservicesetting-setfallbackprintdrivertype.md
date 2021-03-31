---
title: Método SetFallbackPrintDriverType de la clase Win32_TerminalServiceSetting
description: El método SetFallbackPrintDriverType establece la propiedad FallbackPrintDriverType para la clase.
ms.assetid: be738134-199a-41a6-b2f8-cccfa14fa02b
ms.tgt_platform: multiple
keywords:
- Método SetFallbackPrintDriverType Servicios de Escritorio remoto
- Método SetFallbackPrintDriverType Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método SetFallbackPrintDriverType
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetFallbackPrintDriverType
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e445fef86970e89d5b0f09abebecd40f49ab7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079694"
---
# <a name="setfallbackprintdrivertype-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="fd905-106">Método SetFallbackPrintDriverType de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="fd905-106">SetFallbackPrintDriverType method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="fd905-107">El método **SetFallbackPrintDriverType** establece la propiedad **FallbackPrintDriverType** para la clase.</span><span class="sxs-lookup"><span data-stu-id="fd905-107">The **SetFallbackPrintDriverType** method sets the **FallbackPrintDriverType** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd905-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd905-108">Syntax</span></span>


```mof
uint32 SetFallbackPrintDriverType(
  [in] uint32 FallbackPrintDriverType
);
```



## <a name="parameters"></a><span data-ttu-id="fd905-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd905-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd905-110">*FallbackPrintDriverType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fd905-110">*FallbackPrintDriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd905-111">Establece la propiedad **FallbackPrintDriverType** , que permite o deniega las nuevas conexiones servicios de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fd905-111">Sets the **FallbackPrintDriverType** property which allows or denies new Remote Desktop Services connections.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="fd905-112"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="fd905-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="fd905-113">No hay controladores de reserva.</span><span class="sxs-lookup"><span data-stu-id="fd905-113">No fallback drivers.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="fd905-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="fd905-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="fd905-115">Mejor aproximación.</span><span class="sxs-lookup"><span data-stu-id="fd905-115">Best guess.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="fd905-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="fd905-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="fd905-117">Mejor aproximación.</span><span class="sxs-lookup"><span data-stu-id="fd905-117">Best guess.</span></span> <span data-ttu-id="fd905-118">Si no se encuentra ninguna coincidencia, retroceder a Hewlett-Packard el lenguaje de control de impresoras (PCL).</span><span class="sxs-lookup"><span data-stu-id="fd905-118">If no match is found, fallback to Hewlett-Packard Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="fd905-119"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="fd905-119"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="fd905-120">Mejor aproximación.</span><span class="sxs-lookup"><span data-stu-id="fd905-120">Best guess.</span></span> <span data-ttu-id="fd905-121">Si no se encuentra ninguna coincidencia, retroceder a PostScript (PS).</span><span class="sxs-lookup"><span data-stu-id="fd905-121">If no match is found, fallback to Postscript (PS).</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="fd905-122"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="fd905-122"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="fd905-123">Mejor aproximación.</span><span class="sxs-lookup"><span data-stu-id="fd905-123">Best guess.</span></span> <span data-ttu-id="fd905-124">Si no se encuentra ninguna coincidencia, muestre los controladores PS y PCL.</span><span class="sxs-lookup"><span data-stu-id="fd905-124">If no match is found, show both PS and PCL drivers.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd905-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd905-125">Return value</span></span>

<span data-ttu-id="fd905-126">Devuelve SUCCESS si es correcto; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="fd905-126">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="fd905-127">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="fd905-127">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="fd905-128">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="fd905-128">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd905-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd905-129">Remarks</span></span>

<span data-ttu-id="fd905-130">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fd905-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fd905-131">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fd905-131">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fd905-132">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="fd905-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fd905-133">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fd905-133">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd905-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd905-134">Requirements</span></span>



| <span data-ttu-id="fd905-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd905-135">Requirement</span></span> | <span data-ttu-id="fd905-136">Value</span><span class="sxs-lookup"><span data-stu-id="fd905-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd905-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd905-137">Minimum supported client</span></span><br/> | <span data-ttu-id="fd905-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd905-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fd905-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd905-139">Minimum supported server</span></span><br/> | <span data-ttu-id="fd905-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd905-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fd905-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fd905-141">Namespace</span></span><br/>                | <span data-ttu-id="fd905-142">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="fd905-142">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="fd905-143">MOF</span><span class="sxs-lookup"><span data-stu-id="fd905-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd905-144"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd905-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd905-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fd905-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd905-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd905-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd905-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd905-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd905-148">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="fd905-148">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

