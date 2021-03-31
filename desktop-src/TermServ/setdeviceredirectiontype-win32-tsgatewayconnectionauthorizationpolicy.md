---
title: Método SetDeviceRedirectionType de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Establece la propiedad DeviceRedirectionType, que controla a qué dispositivos se redirigirá.
ms.assetid: d97a0a7d-a08e-4703-b0f0-ba5d20688dc8
ms.tgt_platform: multiple
keywords:
- Método SetDeviceRedirectionType Servicios de Escritorio remoto
- Método SetDeviceRedirectionType Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de clase Servicios de Escritorio remoto, método SetDeviceRedirectionType
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetDeviceRedirectionType
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98b369e0b6031aa503e2f7f55860d004f63b7f93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996309"
---
# <a name="setdeviceredirectiontype-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="cc215-106">Método SetDeviceRedirectionType de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="cc215-106">SetDeviceRedirectionType method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="cc215-107">Establece la propiedad **DeviceRedirectionType** , que controla a qué dispositivos se redirigirá.</span><span class="sxs-lookup"><span data-stu-id="cc215-107">Sets the **DeviceRedirectionType** property, which controls which devices will be redirected.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc215-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc215-108">Syntax</span></span>


```mof
uint32 SetDeviceRedirectionType(
  [in] uint32 DeviceRedirectionType
);
```



## <a name="parameters"></a><span data-ttu-id="cc215-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc215-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc215-110">*DeviceRedirectionType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cc215-110">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc215-111">El tipo de redireccionamiento de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="cc215-111">The device redirection type.</span></span>

<dt>

<span data-ttu-id="cc215-112">0</span><span class="sxs-lookup"><span data-stu-id="cc215-112">0</span></span>
</dt> <dd>

<span data-ttu-id="cc215-113">Se redirigirán todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="cc215-113">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="cc215-114">1</span><span class="sxs-lookup"><span data-stu-id="cc215-114">1</span></span>
</dt> <dd>

<span data-ttu-id="cc215-115">No se redirigirá ningún dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc215-115">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="cc215-116">2</span><span class="sxs-lookup"><span data-stu-id="cc215-116">2</span></span>
</dt> <dd>

<span data-ttu-id="cc215-117">Los dispositivos especificados no se redirigirán.</span><span class="sxs-lookup"><span data-stu-id="cc215-117">Specified devices will not be redirected.</span></span> <span data-ttu-id="cc215-118">Las propiedades **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled** y **PlugAndPlayDevicesDisabled** controlan qué dispositivos no se redirigirán.</span><span class="sxs-lookup"><span data-stu-id="cc215-118">The **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled**, and **PlugAndPlayDevicesDisabled** properties control which devices will not be redirected.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc215-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc215-119">Return value</span></span>

<span data-ttu-id="cc215-120">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="cc215-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="cc215-121">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="cc215-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="cc215-122">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cc215-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cc215-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc215-123">Remarks</span></span>

<span data-ttu-id="cc215-124">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="cc215-124">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="cc215-125">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="cc215-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cc215-126">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="cc215-126">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="cc215-127">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="cc215-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cc215-128">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="cc215-128">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc215-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc215-129">Requirements</span></span>



| <span data-ttu-id="cc215-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc215-130">Requirement</span></span> | <span data-ttu-id="cc215-131">Value</span><span class="sxs-lookup"><span data-stu-id="cc215-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc215-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc215-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cc215-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cc215-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="cc215-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc215-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cc215-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc215-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="cc215-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cc215-136">Namespace</span></span><br/>                | <span data-ttu-id="cc215-137">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="cc215-137">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="cc215-138">MOF</span><span class="sxs-lookup"><span data-stu-id="cc215-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc215-139"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc215-139"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc215-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cc215-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc215-141"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc215-141"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="cc215-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc215-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc215-143">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="cc215-143">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

