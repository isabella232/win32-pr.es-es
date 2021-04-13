---
title: Método RemoteControl de la clase Win32_TSRemoteControlSetting
description: El método RemoteControl establece la propiedad LevelOfControl.
ms.assetid: 341f4f8d-17be-4482-834a-b771e041cfec
ms.tgt_platform: multiple
keywords:
- Método RemoteControl Servicios de Escritorio remoto
- Método RemoteControl Servicios de Escritorio remoto, clase Win32_TSRemoteControlSetting
- Win32_TSRemoteControlSetting de clase Servicios de Escritorio remoto, método RemoteControl
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting.RemoteControl
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476269c2f619b7ea46bc6546f106d7ccd2a486e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359724"
---
# <a name="remotecontrol-method-of-the-win32_tsremotecontrolsetting-class"></a><span data-ttu-id="0ee1f-106">Método RemoteControl de la \_ clase TSRemoteControlSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="0ee1f-106">RemoteControl method of the Win32\_TSRemoteControlSetting class</span></span>

<span data-ttu-id="0ee1f-107">El método **Remotecontrol** establece la propiedad **LevelOfControl** .</span><span class="sxs-lookup"><span data-stu-id="0ee1f-107">The **RemoteControl** method sets the **LevelOfControl** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee1f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ee1f-108">Syntax</span></span>


```mof
uint32 RemoteControl(
  [in] uint32 LevelOfControl
);
```



## <a name="parameters"></a><span data-ttu-id="0ee1f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ee1f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ee1f-110">*LevelOfControl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ee1f-110">*LevelOfControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ee1f-111">Nuevo valor para la propiedad **LevelOfControl** , que especifica si el usuario remoto solo verá la sesión, o si se puede ver y controlar mediante un teclado y un mouse.</span><span class="sxs-lookup"><span data-stu-id="0ee1f-111">New value for the **LevelOfControl** property, which specifies whether the session will only be viewed by the remote user, or viewed and controlled through a keyboard and mouse.</span></span> <span data-ttu-id="0ee1f-112">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="0ee1f-112">For more information, see the Remarks section.</span></span> <span data-ttu-id="0ee1f-113">Se admiten los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0ee1f-113">The following values are supported.</span></span>

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="0ee1f-114"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deshabilitar** (0)</span><span class="sxs-lookup"><span data-stu-id="0ee1f-114"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0ee1f-115">El control remoto está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="0ee1f-115">Remote control is disabled.</span></span>

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span data-ttu-id="0ee1f-116"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span><span class="sxs-lookup"><span data-stu-id="0ee1f-116"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0ee1f-117">El usuario del control remoto tiene control total sobre la sesión del usuario, con el permiso del usuario.</span><span class="sxs-lookup"><span data-stu-id="0ee1f-117">The user of remote control has full control of the user's session, with the user's permission.</span></span>

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span data-ttu-id="0ee1f-118"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span><span class="sxs-lookup"><span data-stu-id="0ee1f-118"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0ee1f-119">El usuario del control remoto tiene control total sobre la sesión del usuario; el permiso del usuario no es necesario.</span><span class="sxs-lookup"><span data-stu-id="0ee1f-119">The user of remote control has full control of the user's session; the user's permission is not required.</span></span>

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span data-ttu-id="0ee1f-120"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span><span class="sxs-lookup"><span data-stu-id="0ee1f-120"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0ee1f-121">El usuario del control remoto puede ver la sesión de forma remota, con el permiso del usuario; el usuario remoto no puede controlar activamente la sesión.</span><span class="sxs-lookup"><span data-stu-id="0ee1f-121">The user of remote control can view the session remotely, with the user's permission; the remote user cannot actively control the session.</span></span>

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span data-ttu-id="0ee1f-122"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span><span class="sxs-lookup"><span data-stu-id="0ee1f-122"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0ee1f-123">El usuario del control remoto puede ver la sesión de forma remota, pero no controlar activamente la sesión. el permiso del usuario no es necesario.</span><span class="sxs-lookup"><span data-stu-id="0ee1f-123">The user of remote control can view the session remotely, but not actively control the session; the user's permission is not required.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ee1f-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ee1f-124">Return value</span></span>

<span data-ttu-id="0ee1f-125">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="0ee1f-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0ee1f-126">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0ee1f-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="0ee1f-127">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0ee1f-127">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ee1f-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ee1f-128">Remarks</span></span>

<span data-ttu-id="0ee1f-129">Control total de una sesión significa que el usuario remoto puede controlar activamente la sesión del usuario con un teclado y un mouse.</span><span class="sxs-lookup"><span data-stu-id="0ee1f-129">Full control of a session means that the remote user can actively control the user's session with a keyboard and mouse.</span></span>

<span data-ttu-id="0ee1f-130">Cuando un usuario intenta establecer una conexión de control remoto, el sistema muestra un mensaje al cliente remoto, solicitando permiso para ver o participar activamente en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="0ee1f-130">When a user attempts to establish a remote-control connection, the system displays a message to the remote client, requesting permission to either view or participate actively in the remote session.</span></span>

<span data-ttu-id="0ee1f-131">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0ee1f-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0ee1f-132">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0ee1f-132">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0ee1f-133">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="0ee1f-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0ee1f-134">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0ee1f-134">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ee1f-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ee1f-135">Requirements</span></span>



| <span data-ttu-id="0ee1f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ee1f-136">Requirement</span></span> | <span data-ttu-id="0ee1f-137">Value</span><span class="sxs-lookup"><span data-stu-id="0ee1f-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ee1f-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ee1f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0ee1f-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ee1f-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0ee1f-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ee1f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0ee1f-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ee1f-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0ee1f-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0ee1f-142">Namespace</span></span><br/>                | <span data-ttu-id="0ee1f-143">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0ee1f-143">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0ee1f-144">MOF</span><span class="sxs-lookup"><span data-stu-id="0ee1f-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ee1f-145"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ee1f-145"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ee1f-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0ee1f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ee1f-147"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ee1f-147"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ee1f-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ee1f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee1f-149">**Win32 \_ TSRemoteControlSetting**</span><span class="sxs-lookup"><span data-stu-id="0ee1f-149">**Win32\_TSRemoteControlSetting**</span></span>](win32-tsremotecontrolsetting.md)
</dt> </dl>

 

