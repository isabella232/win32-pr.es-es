---
title: Método SetAllowTSConnections de la clase Win32_TerminalServiceSetting
description: El método SetAllowTSConnections permite o deniega nuevas conexiones de escritorio remoto. Este método modificará la propiedad AllowTSConnections de la clase en consecuencia.
ms.assetid: 6cbaea62-ced0-4788-99fb-5b36816b80a1
ms.tgt_platform: multiple
keywords:
- Método SetAllowTSConnections Servicios de Escritorio remoto
- Método SetAllowTSConnections Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método SetAllowTSConnections
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetAllowTSConnections
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e800f1a47567f16d916563d4d1e62c767016329a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492725"
---
# <a name="setallowtsconnections-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="17292-107">Método SetAllowTSConnections de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="17292-107">SetAllowTSConnections method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="17292-108">El método **SetAllowTSConnections** permite o deniega nuevas conexiones de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="17292-108">The **SetAllowTSConnections** method allows or denies new remote desktop connections.</span></span> <span data-ttu-id="17292-109">Este método modificará la propiedad **AllowTSConnections** de la clase en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="17292-109">This method will modify the **AllowTSConnections** property for the class accordingly.</span></span>

## <a name="syntax"></a><span data-ttu-id="17292-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17292-110">Syntax</span></span>


```mof
uint32 SetAllowTSConnections(
  [in] uint32 AllowTSConnections,
  [in] uint32 ModifyFirewallException
);
```



## <a name="parameters"></a><span data-ttu-id="17292-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17292-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17292-112">*AllowTSConnections* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="17292-112">*AllowTSConnections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17292-113">Especifica si se permiten las nuevas conexiones de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="17292-113">Specifies whether new remote desktop connections are allowed.</span></span> <span data-ttu-id="17292-114">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="17292-114">This must be one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="17292-115"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="17292-115"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="17292-116">No se permiten nuevas conexiones.</span><span class="sxs-lookup"><span data-stu-id="17292-116">New connections are not allowed.</span></span> <span data-ttu-id="17292-117">Si el parámetro *ModifyFirewallException* es 1, la excepción de firewall de escritorio remoto está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="17292-117">If the *ModifyFirewallException* parameter is 1, then the Remote Desktop firewall exception is disabled.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="17292-118"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="17292-118"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="17292-119">Se permiten nuevas conexiones.</span><span class="sxs-lookup"><span data-stu-id="17292-119">New connections are allowed.</span></span> <span data-ttu-id="17292-120">Si el parámetro *ModifyFirewallException* es 1, la excepción de firewall de escritorio remoto está habilitada.</span><span class="sxs-lookup"><span data-stu-id="17292-120">If the *ModifyFirewallException* parameter is 1, then the Remote Desktop firewall exception is enabled.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="17292-121">*ModifyFirewallException* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="17292-121">*ModifyFirewallException* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17292-122">Especifica si el valor de la excepción de Firewall para Escritorio remoto se modificará al estado especificado por el parámetro *AllowTSConnections* .</span><span class="sxs-lookup"><span data-stu-id="17292-122">Specifies if the firewall exception setting for Remote Desktop will be modified to the state specified by the *AllowTSConnections* parameter.</span></span> <span data-ttu-id="17292-123">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="17292-123">This must be one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="17292-124"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="17292-124"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="17292-125">No modifique la configuración de excepción del firewall.</span><span class="sxs-lookup"><span data-stu-id="17292-125">Do not modify the firewall exception setting.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="17292-126"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="17292-126"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="17292-127">Modifique la configuración de la excepción del firewall.</span><span class="sxs-lookup"><span data-stu-id="17292-127">Modify the firewall exception setting.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17292-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17292-128">Return value</span></span>

<span data-ttu-id="17292-129">Devuelve SUCCESS si se realiza correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="17292-129">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="17292-130">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="17292-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="17292-131">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="17292-131">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="17292-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17292-132">Remarks</span></span>

<span data-ttu-id="17292-133">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="17292-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="17292-134">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="17292-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="17292-135">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="17292-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="17292-136">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="17292-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="17292-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17292-137">Requirements</span></span>



| <span data-ttu-id="17292-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="17292-138">Requirement</span></span> | <span data-ttu-id="17292-139">Value</span><span class="sxs-lookup"><span data-stu-id="17292-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17292-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17292-140">Minimum supported client</span></span><br/> | <span data-ttu-id="17292-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17292-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17292-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17292-142">Minimum supported server</span></span><br/> | <span data-ttu-id="17292-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17292-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17292-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="17292-144">Namespace</span></span><br/>                | <span data-ttu-id="17292-145">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="17292-145">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="17292-146">MOF</span><span class="sxs-lookup"><span data-stu-id="17292-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17292-147"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17292-147"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="17292-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="17292-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17292-149"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17292-149"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17292-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="17292-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17292-151">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="17292-151">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

