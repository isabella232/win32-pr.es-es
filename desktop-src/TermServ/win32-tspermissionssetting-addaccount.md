---
title: Método AddAccount de la clase Win32_TSPermissionsSetting (Faxcomex. h)
description: El método AddAccount se prepara para agregar una cuenta al terminal con el conjunto de permisos especificado. Puede Agregar usuarios, grupos o equipos.
ms.assetid: da4d8f5b-7aa2-4b55-bf0f-b3e98b70a06b
ms.tgt_platform: multiple
keywords:
- Método AddAccount Servicios de Escritorio remoto
- Método AddAccount Servicios de Escritorio remoto, clase Win32_TSPermissionsSetting
- Win32_TSPermissionsSetting de clase Servicios de Escritorio remoto, método AddAccount
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.AddAccount
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de89c34bd7aab20fbfbcbdedfd9d2f91bba866bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491590"
---
# <a name="addaccount-method-of-the-win32_tspermissionssetting-class"></a><span data-ttu-id="93701-107">Método AddAccount de la \_ clase TSPermissionsSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="93701-107">AddAccount method of the Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="93701-108">El método **AddAccount** se prepara para agregar una cuenta al terminal con el conjunto de permisos especificado.</span><span class="sxs-lookup"><span data-stu-id="93701-108">The **AddAccount** method prepares to add an account to the terminal with the specified permission set.</span></span> <span data-ttu-id="93701-109">Puede Agregar usuarios, grupos o equipos.</span><span class="sxs-lookup"><span data-stu-id="93701-109">You can add users, groups, or computers.</span></span>

## <a name="syntax"></a><span data-ttu-id="93701-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93701-110">Syntax</span></span>


```mof
uint32 AddAccount(
  [in] string AccountName,
  [in] uint32 PermissionPreSet
);
```



## <a name="parameters"></a><span data-ttu-id="93701-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93701-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93701-112">*AccountName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="93701-112">*AccountName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93701-113">Nombre de la cuenta que se va a agregar al terminal.</span><span class="sxs-lookup"><span data-stu-id="93701-113">The name of the account to add to the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="93701-114">*PermissionPreSet* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="93701-114">*PermissionPreSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93701-115">Conjunto de permisos que se va a asociar a la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="93701-115">The set of permissions to associate with the specified account.</span></span> <span data-ttu-id="93701-116">Este parámetro puede ser uno o todos los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="93701-116">This parameter can be any or all of the following values.</span></span> <span data-ttu-id="93701-117">Para obtener más información, vea [permisos de servicios de escritorio remoto](terminal-services-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="93701-117">For more information, see [Remote Desktop Services Permissions](terminal-services-permissions.md).</span></span>

<dt>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>

<span data-ttu-id="93701-118"><span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**Estación \_ de \_Acceso de invitado** (0)</span><span class="sxs-lookup"><span data-stu-id="93701-118"><span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WINSTATION\_GUEST\_ACCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="93701-119">La cuenta tiene permiso de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="93701-119">The account has Logon permission.</span></span>

</dd> <dt>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>

<span data-ttu-id="93701-120"><span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**Estación \_ de \_Acceso de usuario** (1)</span><span class="sxs-lookup"><span data-stu-id="93701-120"><span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WINSTATION\_USER\_ACCESS** (1)</span></span>


</dt> <dd>

<span data-ttu-id="93701-121">La cuenta tiene los siguientes permisos: Inicio de sesión, información de consulta, enviar mensaje y conectar.</span><span class="sxs-lookup"><span data-stu-id="93701-121">The account has the following permissions: Logon, Query Information, Send Message, and Connect.</span></span>

</dd> <dt>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>

<span data-ttu-id="93701-122"><span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**Estación \_ de TODO el \_ acceso** (2)</span><span class="sxs-lookup"><span data-stu-id="93701-122"><span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WINSTATION\_ALL\_ACCESS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="93701-123">La cuenta tiene todos los permisos de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="93701-123">The account has all Remote Desktop Services Permissions.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93701-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93701-124">Return value</span></span>

<span data-ttu-id="93701-125">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="93701-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="93701-126">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="93701-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="93701-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93701-127">Remarks</span></span>

<span data-ttu-id="93701-128">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="93701-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="93701-129">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="93701-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="93701-130">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="93701-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="93701-131">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="93701-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="93701-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93701-132">Requirements</span></span>



| <span data-ttu-id="93701-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="93701-133">Requirement</span></span> | <span data-ttu-id="93701-134">Value</span><span class="sxs-lookup"><span data-stu-id="93701-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93701-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93701-135">Minimum supported client</span></span><br/> | <span data-ttu-id="93701-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93701-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93701-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93701-137">Minimum supported server</span></span><br/> | <span data-ttu-id="93701-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93701-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93701-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="93701-139">Namespace</span></span><br/>                | <span data-ttu-id="93701-140">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="93701-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="93701-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93701-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="93701-142"><dt>Faxcomex. h</dt></span><span class="sxs-lookup"><span data-stu-id="93701-142"><dt>Faxcomex.h</dt></span></span> </dl>   |
| <span data-ttu-id="93701-143">MOF</span><span class="sxs-lookup"><span data-stu-id="93701-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93701-144"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93701-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="93701-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="93701-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93701-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93701-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93701-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="93701-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93701-148">**Win32 \_ TSPermissionsSetting**</span><span class="sxs-lookup"><span data-stu-id="93701-148">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> </dl>

 

