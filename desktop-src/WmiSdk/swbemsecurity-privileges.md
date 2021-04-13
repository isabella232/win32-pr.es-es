---
description: La propiedad privileges es un objeto SWbemPrivilegeSet. Esta propiedad se usa para habilitar o deshabilitar privilegios específicos de Windows. Es posible que tenga que establecer uno de estos privilegios para realizar tareas específicas mediante la API de Instrumental de administración de Windows (WMI).
ms.assetid: 6e4cae22-23d6-4981-b38c-d298654e59ab
ms.tgt_platform: multiple
title: Propiedad SWbemSecurity. Privileges (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.Privileges
- ISWbemSecurity.Privileges
- ISWbemSecurity.get_Privileges
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6fd8e1c0f9b6667b49d0956bcea5ac9e187443d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276115"
---
# <a name="swbemsecurityprivileges-property"></a><span data-ttu-id="a864a-105">Propiedad SWbemSecurity. privileges</span><span class="sxs-lookup"><span data-stu-id="a864a-105">SWbemSecurity.Privileges property</span></span>

<span data-ttu-id="a864a-106">La propiedad **privileges** es un objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) .</span><span class="sxs-lookup"><span data-stu-id="a864a-106">The **Privileges** property is an [**SWbemPrivilegeSet**](swbemprivilegeset.md) object.</span></span> <span data-ttu-id="a864a-107">Esta propiedad se usa para habilitar o deshabilitar privilegios específicos de Windows.</span><span class="sxs-lookup"><span data-stu-id="a864a-107">This property is used to enable or disable specific Windows privileges.</span></span> <span data-ttu-id="a864a-108">Es posible que tenga que establecer uno de estos privilegios para realizar tareas específicas mediante la API de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a864a-108">You may need to set one of these privileges to perform specific tasks using the Windows Management Instrumentation (WMI) API.</span></span>

<span data-ttu-id="a864a-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a864a-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="a864a-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a864a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a864a-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a864a-111">Syntax</span></span>


```VB
SWbemSecurity.Privileges As Object
```



## <a name="property-value"></a><span data-ttu-id="a864a-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a864a-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="a864a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a864a-113">Remarks</span></span>

<span data-ttu-id="a864a-114">Esta configuración permite conceder o revocar privilegios como parte de una cadena de moniker WMI.</span><span class="sxs-lookup"><span data-stu-id="a864a-114">This setting allows you to grant or revoke privileges as part of a WMI moniker string.</span></span> <span data-ttu-id="a864a-115">Para obtener una lista completa de los valores aplicables, consulte [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) y las [**constantes de privilegios**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a864a-115">For the complete list of applicable values, see [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) and [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="a864a-116">Puede cambiar los privilegios definidos para los objetos [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)y [**SwbemLocator**](swbemlocator.md) agregando objetos [**SWbemPrivilege**](swbemprivilege.md) a la propiedad **privileges** .</span><span class="sxs-lookup"><span data-stu-id="a864a-116">You can change the privileges defined for the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects by adding [**SWbemPrivilege**](swbemprivilege.md) objects to the **Privileges** property.</span></span>

<span data-ttu-id="a864a-117">Hay diferencias fundamentales en el modo en que las distintas versiones de Windows controlan los cambios en los privilegios.</span><span class="sxs-lookup"><span data-stu-id="a864a-117">There are fundamental differences in how different versions of Windows handle changes to privileges.</span></span> <span data-ttu-id="a864a-118">Si está desarrollando una aplicación que solo se usa en plataformas Windows, puede establecer o revocar los privilegios en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="a864a-118">If you are developing an application that is only used on Windows platforms, you can set or revoke privileges at any time.</span></span>

<span data-ttu-id="a864a-119">En el ejemplo siguiente se establece **SeDebugPrivilege** en la conexión de moniker inicial para obtener un objeto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="a864a-119">The following example sets the **SeDebugPrivilege** on the initial moniker connection to obtain an [**SWbemServices**](swbemservices.md) object.</span></span>


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



<span data-ttu-id="a864a-120">Para obtener más información sobre cómo dar formato a la cadena de seguridad para una conexión de moniker, vea [**constantes de privilegios**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a864a-120">For more information about how to format the security string for a moniker connection, see [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="a864a-121">En el ejemplo siguiente se realiza la misma tarea, pero se establece el privilegio después del inicio de sesión inicial en WMI.</span><span class="sxs-lookup"><span data-stu-id="a864a-121">The following example performs the same task, but it sets the privilege after the initial log on to WMI.</span></span>


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate}")
Service.Security_.Privileges.AddAsString "SeDebugPrivilege", True
```



<span data-ttu-id="a864a-122">Tenga en cuenta que para las llamadas a [**SwbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md), debe usar el nombre completo del privilegio de seguridad, por ejemplo, "SeDebugPrivilege" en lugar de "debug".</span><span class="sxs-lookup"><span data-stu-id="a864a-122">Note that for calls to [**SwbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md), you must use the full name of the security privilege, for example, "SeDebugPrivilege" instead of "Debug".</span></span>

## <a name="requirements"></a><span data-ttu-id="a864a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a864a-123">Requirements</span></span>



| <span data-ttu-id="a864a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a864a-124">Requirement</span></span> | <span data-ttu-id="a864a-125">Value</span><span class="sxs-lookup"><span data-stu-id="a864a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a864a-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a864a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a864a-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a864a-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a864a-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a864a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a864a-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a864a-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a864a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a864a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a864a-131"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a864a-131"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a864a-132">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a864a-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="a864a-133"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a864a-133"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a864a-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a864a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a864a-135"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a864a-135"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a864a-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="a864a-136">CLSID</span></span><br/>                    | <span data-ttu-id="a864a-137">CLSID \_ SWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="a864a-137">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="a864a-138">IID</span><span class="sxs-lookup"><span data-stu-id="a864a-138">IID</span></span><br/>                      | <span data-ttu-id="a864a-139">\_ISWBEMSECURITY IID</span><span class="sxs-lookup"><span data-stu-id="a864a-139">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="a864a-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="a864a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a864a-141">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="a864a-141">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="a864a-142">Ejecutar operaciones con privilegios</span><span class="sxs-lookup"><span data-stu-id="a864a-142">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="a864a-143">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="a864a-143">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> </dl>

 

 




