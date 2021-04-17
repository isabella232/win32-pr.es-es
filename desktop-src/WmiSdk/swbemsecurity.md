---
description: El objeto SWbemSecurity obtiene o establece la configuración de seguridad, como los privilegios, las suplantaciones COM y los niveles de autenticación asignados a un objeto.
ms.assetid: 794587fa-5feb-455b-be28-ecfaa25625ad
ms.tgt_platform: multiple
title: Objeto SWbemSecurity (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity
- ISWbemSecurity
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: da59c3b996a80384c133336503124141f0907f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666823"
---
# <a name="swbemsecurity-object"></a><span data-ttu-id="c2805-103">Objeto SWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="c2805-103">SWbemSecurity object</span></span>

<span data-ttu-id="c2805-104">El objeto **SWbemSecurity** obtiene o establece la configuración de seguridad, como los privilegios, las suplantaciones com y los niveles de autenticación asignados a un objeto.</span><span class="sxs-lookup"><span data-stu-id="c2805-104">The **SWbemSecurity** object gets or sets security settings, such as privileges, COM impersonations, and authentication levels assigned to an object.</span></span> <span data-ttu-id="c2805-105">Los objetos [**SWbemLocator**](swbemlocator.md), [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), [**SWbemLastError**](swbemlasterror.md)y [**SWbemEventSource**](swbemeventsource.md) tienen una propiedad **de \_ seguridad** , que es el objeto **SWbemSecurity** .</span><span class="sxs-lookup"><span data-stu-id="c2805-105">The [**SWbemLocator**](swbemlocator.md), [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), [**SWbemLastError**](swbemlasterror.md), and [**SWbemEventSource**](swbemeventsource.md) objects have a **Security\_** property, which is the **SWbemSecurity** object.</span></span> <span data-ttu-id="c2805-106">Al recuperar una instancia o ver el registro de seguridad de WMI, puede que tenga que establecer las propiedades del objeto de **seguridad \_** .</span><span class="sxs-lookup"><span data-stu-id="c2805-106">When you retrieve an instance or view the WMI security log, you might need to set the properties of the **Security\_** object.</span></span>

<span data-ttu-id="c2805-107">La llamada [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) de VBScript no puede crear el objeto de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c2805-107">The VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call cannot create the Security object.</span></span> <span data-ttu-id="c2805-108">La configuración de seguridad de este objeto no identifica la configuración de autenticación, suplantación o privilegio en una conexión a WMI, o la seguridad activa para el proxy cuando un objeto se entrega a un receptor en una llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c2805-108">The security settings in this object do not identify the authentication, impersonation, or privilege settings on a connection to WMI, or the security in effect for the proxy when an object is delivered to a sink in an asynchronous call.</span></span> <span data-ttu-id="c2805-109">Para obtener más información, vea [mantener la seguridad de WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="c2805-109">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

## <a name="members"></a><span data-ttu-id="c2805-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2805-110">Members</span></span>

<span data-ttu-id="c2805-111">El objeto **SWbemSecurity** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c2805-111">The **SWbemSecurity** object has these types of members:</span></span>

-   [<span data-ttu-id="c2805-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c2805-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2805-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c2805-113">Properties</span></span>

<span data-ttu-id="c2805-114">El objeto **SWbemSecurity** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c2805-114">The **SWbemSecurity** object has these properties.</span></span>



| <span data-ttu-id="c2805-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c2805-115">Property</span></span>                                                                    | <span data-ttu-id="c2805-116">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="c2805-116">Access type</span></span>           | <span data-ttu-id="c2805-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2805-117">Description</span></span>                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2805-118">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="c2805-118">**AuthenticationLevel**</span></span>](swbemsecurity-authenticationlevel.md)<br/> | <span data-ttu-id="c2805-119">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c2805-119">Read/write</span></span><br/> | <span data-ttu-id="c2805-120">Valor numérico que define el nivel de autenticación COM que se asigna a este objeto.</span><span class="sxs-lookup"><span data-stu-id="c2805-120">Numeric value that defines the COM Authentication level that is assigned to this object.</span></span> <span data-ttu-id="c2805-121">Esta configuración determina cómo se protege la información enviada desde WMI.</span><span class="sxs-lookup"><span data-stu-id="c2805-121">This setting determines how you protect information sent from WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="c2805-122">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="c2805-122">**ImpersonationLevel**</span></span>](swbemsecurity-impersonationlevel.md)<br/>   | <span data-ttu-id="c2805-123">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c2805-123">Read/write</span></span><br/> | <span data-ttu-id="c2805-124">Valor numérico que define el nivel de suplantación COM que se asigna a este objeto.</span><span class="sxs-lookup"><span data-stu-id="c2805-124">Numeric value that defines the COM Impersonation level that is assigned to this object.</span></span> <span data-ttu-id="c2805-125">Esta configuración determina si los procesos que pertenecen a WMI pueden detectar o usar sus credenciales de seguridad al realizar llamadas a otros procesos.</span><span class="sxs-lookup"><span data-stu-id="c2805-125">This setting determines if processes owned by WMI can detect or use your security credentials when making calls to other processes.</span></span><br/> |
| [<span data-ttu-id="c2805-126">**Privilegios**</span><span class="sxs-lookup"><span data-stu-id="c2805-126">**Privileges**</span></span>](swbemsecurity-privileges.md)<br/>                   | <span data-ttu-id="c2805-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2805-127">Read-only</span></span><br/>  | <span data-ttu-id="c2805-128">Un objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) que define los privilegios para este objeto.</span><span class="sxs-lookup"><span data-stu-id="c2805-128">An [**SWbemPrivilegeSet**](swbemprivilegeset.md) object that defines privileges for this object.</span></span> <span data-ttu-id="c2805-129">Para obtener más información, vea [ejecutar con privilegios especiales](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="c2805-129">For more information, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="c2805-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2805-130">Requirements</span></span>



| <span data-ttu-id="c2805-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2805-131">Requirement</span></span> | <span data-ttu-id="c2805-132">Value</span><span class="sxs-lookup"><span data-stu-id="c2805-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2805-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2805-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c2805-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2805-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c2805-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2805-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c2805-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2805-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c2805-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2805-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2805-138"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2805-138"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c2805-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c2805-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="c2805-140"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c2805-140"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c2805-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c2805-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2805-142"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2805-142"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c2805-143">CLSID</span><span class="sxs-lookup"><span data-stu-id="c2805-143">CLSID</span></span><br/>                    | <span data-ttu-id="c2805-144">CLSID \_ SWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="c2805-144">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="c2805-145">IID</span><span class="sxs-lookup"><span data-stu-id="c2805-145">IID</span></span><br/>                      | <span data-ttu-id="c2805-146">\_ISWBEMSECURITY IID</span><span class="sxs-lookup"><span data-stu-id="c2805-146">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="c2805-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2805-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2805-148">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="c2805-148">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="c2805-149">Mantenimiento de la seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="c2805-149">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="c2805-150">Establecer la \_ seguridad del proceso de la aplicación cliente \_</span><span class="sxs-lookup"><span data-stu-id="c2805-150">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="c2805-151">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="c2805-151">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="c2805-152">**WbemImpersonationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="c2805-152">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[<span data-ttu-id="c2805-153">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="c2805-153">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> </dl>

 

