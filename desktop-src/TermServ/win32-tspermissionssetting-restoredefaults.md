---
title: Método RestoreDefaults de la clase Win32_TSPermissionsSetting (Netfw. h)
description: Restaura los valores del conjunto de permisos predeterminados para el terminal.
ms.assetid: bdd01290-7c7c-4355-85dc-ade51b2abd94
ms.tgt_platform: multiple
keywords:
- Método RestoreDefaults Servicios de Escritorio remoto
- Método RestoreDefaults Servicios de Escritorio remoto, clase Win32_TSPermissionsSetting
- Win32_TSPermissionsSetting de clase Servicios de Escritorio remoto, método RestoreDefaults
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.RestoreDefaults
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073a8f8267ab9e7f7cbd50f15f4f3f20594d2e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905152"
---
# <a name="restoredefaults-method-of-the-win32_tspermissionssetting-class"></a><span data-ttu-id="35044-106">Método RestoreDefaults de la \_ clase TSPermissionsSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="35044-106">RestoreDefaults method of the Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="35044-107">El método **RestoreDefaults** restaura los valores del conjunto de permisos predeterminados para el terminal.</span><span class="sxs-lookup"><span data-stu-id="35044-107">The **RestoreDefaults** method restores the default permission set values for the terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="35044-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35044-108">Syntax</span></span>


```mof
uint32 RestoreDefaults();
```



## <a name="parameters"></a><span data-ttu-id="35044-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35044-109">Parameters</span></span>

<span data-ttu-id="35044-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="35044-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="35044-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35044-111">Return value</span></span>

<span data-ttu-id="35044-112">Devuelve SUCCESS si se realizó correctamente; de lo contrario, error.</span><span class="sxs-lookup"><span data-stu-id="35044-112">Returns Success on success, otherwise Failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="35044-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35044-113">Remarks</span></span>

<span data-ttu-id="35044-114">Los permisos predeterminados son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="35044-114">Default permissions are the following:</span></span>

-   <span data-ttu-id="35044-115">Los administradores, el sistema y Escritorio remoto las cuentas del asistente de ayuda tienen todos los [permisos de servicios de escritorio remoto](terminal-services-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="35044-115">The Administrators, System, and Remote Desktop Help Assistant accounts have all [Remote Desktop Services Permissions](terminal-services-permissions.md).</span></span>
-   <span data-ttu-id="35044-116">La cuenta de Escritorio remoto usuarios tiene el permiso de inicio de sesión, conexión, información de consulta y envío de mensaje.</span><span class="sxs-lookup"><span data-stu-id="35044-116">The Remote Desktop Users account has Logon, Connect, Query Information, and Send Message permission.</span></span>
-   <span data-ttu-id="35044-117">Las cuentas servicio local y servicio de red tienen información de consulta y el permiso enviar mensaje.</span><span class="sxs-lookup"><span data-stu-id="35044-117">The Local Service and Network Service accounts have Query Information, and Send Message permission.</span></span>

<span data-ttu-id="35044-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="35044-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="35044-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="35044-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="35044-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="35044-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="35044-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="35044-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="35044-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35044-122">Requirements</span></span>



| <span data-ttu-id="35044-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="35044-123">Requirement</span></span> | <span data-ttu-id="35044-124">Value</span><span class="sxs-lookup"><span data-stu-id="35044-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35044-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35044-125">Minimum supported client</span></span><br/> | <span data-ttu-id="35044-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35044-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35044-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35044-127">Minimum supported server</span></span><br/> | <span data-ttu-id="35044-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35044-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35044-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="35044-129">Namespace</span></span><br/>                | <span data-ttu-id="35044-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="35044-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="35044-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35044-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="35044-132"><dt>Netfw. h</dt></span><span class="sxs-lookup"><span data-stu-id="35044-132"><dt>Netfw.h</dt></span></span> </dl>      |
| <span data-ttu-id="35044-133">MOF</span><span class="sxs-lookup"><span data-stu-id="35044-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35044-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35044-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="35044-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="35044-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35044-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35044-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35044-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="35044-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35044-138">**Win32 \_ TSPermissionsSetting**</span><span class="sxs-lookup"><span data-stu-id="35044-138">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> </dl>

 

