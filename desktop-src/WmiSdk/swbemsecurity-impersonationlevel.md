---
description: La propiedad ImpersonationLevel es un entero que define el nivel de suplantación COM que se asigna a este objeto.
ms.assetid: cf57620b-7827-4552-a969-d25e5eb13a89
ms.tgt_platform: multiple
title: SWbemSecurity. ImpersonationLevel (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.ImpersonationLevel
- ISWbemSecurity.ImpersonationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3b996d5920aba91fddf880ee9ddf6bf8081fb39f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913361"
---
# <a name="swbemsecurityimpersonationlevel-property"></a><span data-ttu-id="3e90c-103">SWbemSecurity. ImpersonationLevel (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3e90c-103">SWbemSecurity.ImpersonationLevel property</span></span>

<span data-ttu-id="3e90c-104">La propiedad **ImpersonationLevel** es un entero que define el nivel de suplantación com que se asigna a este objeto.</span><span class="sxs-lookup"><span data-stu-id="3e90c-104">The **ImpersonationLevel** property is an integer that defines the COM impersonation level that is assigned to this object.</span></span> <span data-ttu-id="3e90c-105">Esta configuración determina si los procesos propiedad de Instrumental de administración de Windows (WMI) pueden detectar o usar sus credenciales de seguridad al realizar llamadas a otros procesos.</span><span class="sxs-lookup"><span data-stu-id="3e90c-105">This setting determines if processes owned by Windows Management Instrumentation (WMI) can detect or use your security credentials when making calls to other processes.</span></span> <span data-ttu-id="3e90c-106">Para obtener más información sobre los niveles de suplantación, vea [establecer la \_ seguridad del \_ proceso de la aplicación cliente](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="3e90c-106">For more information about impersonation levels, see [Setting Client\_Application\_Process Security](setting-client-application-process-security.md).</span></span>

<span data-ttu-id="3e90c-107">Si no establece el nivel de suplantación específicamente en un moniker o estableciendo la propiedad **SWBemSecurity. ImpersonationLevel** en un objeto protegible, WMI establece el nivel de suplantación predeterminado en el valor especificado en la [clave del registro del nivel de suplantación predeterminado](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="3e90c-107">If you do not set the impersonation level specifically in either a moniker, or by setting the **SWBemSecurity.ImpersonationLevel** property on a securable object, WMI sets the default impersonation level to the value specified in the [default impersonation level registry key](setting-the-default-process-security-level-using-vbscript.md).</span></span> <span data-ttu-id="3e90c-108">Si esta configuración no es suficiente, el proveedor no da servicio a la solicitud y se puede producir un error en la llamada a la API de WMI con un código de error de **wbemErrAccessDenied** (2147749891/0x80041003).</span><span class="sxs-lookup"><span data-stu-id="3e90c-108">If this setting is not sufficient, the provider does not service your request, and the call to the WMI API can fail with an error code of **wbemErrAccessDenied** (2147749891/0x80041003).</span></span>

<span data-ttu-id="3e90c-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3e90c-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="3e90c-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3e90c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e90c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e90c-111">Syntax</span></span>


```VB
SWbemSecurity.ImpersonationLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="3e90c-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3e90c-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="3e90c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e90c-113">Remarks</span></span>

<span data-ttu-id="3e90c-114">Como nivel de suplantación de DCOM, esta propiedad se puede establecer en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="3e90c-114">As a DCOM impersonation level, this property can be set to one of the following values:</span></span>



| <span data-ttu-id="3e90c-115">Value</span><span class="sxs-lookup"><span data-stu-id="3e90c-115">Value</span></span>           | <span data-ttu-id="3e90c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e90c-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e90c-117">**Anónimo**</span><span class="sxs-lookup"><span data-stu-id="3e90c-117">**Anonymous**</span></span>   | <span data-ttu-id="3e90c-118">Oculta las credenciales de la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="3e90c-118">Hides the credentials of the caller.</span></span> <span data-ttu-id="3e90c-119">WMI no admite realmente este nivel de suplantación; Si un script especifica impersonationLevel = Anonymous, WMI actualizará de forma silenciosa el nivel de suplantación para identificar.</span><span class="sxs-lookup"><span data-stu-id="3e90c-119">WMI does not actually support this impersonation level; if a script specifies impersonationLevel=Anonymous, WMI will silently upgrade the impersonation level to Identify.</span></span> <span data-ttu-id="3e90c-120">No obstante, esto se debe a un ejercicio sin sentido, ya que es probable que los scripts que usan el nivel de identificación no funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="3e90c-120">This is in some ways a meaningless exercise, however, because scripts using the Identify level are likely to fail.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="3e90c-121">**Identificar**</span><span class="sxs-lookup"><span data-stu-id="3e90c-121">**Identify**</span></span>    | <span data-ttu-id="3e90c-122">Permite que los objetos consulten las credenciales del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="3e90c-122">Enables objects to query the credentials of the caller.</span></span> <span data-ttu-id="3e90c-123">Es probable que se produzcan errores en los scripts que usan este nivel de suplantación. Normalmente, el nivel de identificación permite no tener que comprobar las listas de control de acceso.</span><span class="sxs-lookup"><span data-stu-id="3e90c-123">Scripts using this impersonation level are likely to fail; the Identify level typically lets you do no more than check access control lists.</span></span> <span data-ttu-id="3e90c-124">No podrá ejecutar scripts en equipos remotos mediante la identificación de.</span><span class="sxs-lookup"><span data-stu-id="3e90c-124">You will not be able to run scripts against remote computers using Identify.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="3e90c-125">**Impersonate**</span><span class="sxs-lookup"><span data-stu-id="3e90c-125">**Impersonate**</span></span> | <span data-ttu-id="3e90c-126">Permite que los objetos usen las credenciales del llamador.</span><span class="sxs-lookup"><span data-stu-id="3e90c-126">Enables objects to use the credentials of the caller.</span></span> <span data-ttu-id="3e90c-127">Se recomienda usar este nivel de suplantación con scripts de WMI.</span><span class="sxs-lookup"><span data-stu-id="3e90c-127">It is recommended that you use this impersonation level with WMI scripts.</span></span> <span data-ttu-id="3e90c-128">Al hacerlo, el script de WMI usará sus credenciales de usuario. como resultado, podrá llevar a cabo las tareas que pueda llevar a cabo.</span><span class="sxs-lookup"><span data-stu-id="3e90c-128">When you do so, the WMI script will use your user credentials; as a result, it will be able to perform any tasks that you are able to perform.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="3e90c-129">**Delegado**</span><span class="sxs-lookup"><span data-stu-id="3e90c-129">**Delegate**</span></span>    | <span data-ttu-id="3e90c-130">Permite a los objetos permitir que otros objetos usen las credenciales del llamador.</span><span class="sxs-lookup"><span data-stu-id="3e90c-130">Enables objects to permit other objects to use the credentials of the caller.</span></span> <span data-ttu-id="3e90c-131">La delegación permite a un script utilizar las credenciales en un equipo remoto y, a continuación, permite a ese equipo remoto usar las credenciales en otro equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="3e90c-131">Delegation allows a script to use your credentials on a remote computer and then enables that remote computer to use your credentials on another remote computer.</span></span> <span data-ttu-id="3e90c-132">Aunque puede usar este nivel de suplantación dentro de los scripts de WMI, debe hacerlo solo si es necesario, ya que podría suponer un riesgo para la seguridad.</span><span class="sxs-lookup"><span data-stu-id="3e90c-132">While you can use this impersonation level within WMI scripts, you should do so only if necessary because it might pose a security risk.</span></span><br/> <span data-ttu-id="3e90c-133">No se puede usar el nivel de suplantación de delegado a menos que todas las cuentas de usuario y las cuentas de equipo implicadas en la transacción se hayan marcado como de confianza para la delegación en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3e90c-133">You cannot use the Delegate impersonation level unless all the user accounts and computer accounts involved in the transaction have all been marked as Trusted for delegation in Active Directory.</span></span> <span data-ttu-id="3e90c-134">Esto ayuda a minimizar los riesgos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3e90c-134">This helps minimize the security risks.</span></span> <span data-ttu-id="3e90c-135">Aunque un equipo remoto puede usar sus credenciales, solo puede hacerlo si ambos equipos implicados en la transacción son de confianza para la delegación.</span><span class="sxs-lookup"><span data-stu-id="3e90c-135">Although a remote computer can use your credentials, it can do so only if both it and any other computers involved in the transaction are trusted for delegation.</span></span><br/> |



 

<span data-ttu-id="3e90c-136">Como se indicó, la suplantación anónima oculta las credenciales e identifica permite que un objeto remoto consulte sus credenciales, pero el objeto remoto no puede suplantar el contexto de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3e90c-136">As noted, Anonymous impersonation hides your credentials and Identify permits a remote object to query your credentials, but the remote object cannot impersonate your security context.</span></span> <span data-ttu-id="3e90c-137">(Es decir, aunque el objeto remoto sepa quién es usted, no puede "fingir" que lo sea). Normalmente, se producirá un error en los scripts de WMI que acceden a equipos remotos mediante una de estas dos configuraciones.</span><span class="sxs-lookup"><span data-stu-id="3e90c-137">(In other words, although the remote object knows who you are, it cannot "pretend" to be you.) WMI scripts accessing remote computers using one of these two settings will generally fail.</span></span> <span data-ttu-id="3e90c-138">De hecho, la mayoría de los scripts que se ejecutan en el equipo local con una de estas dos configuraciones también producirán un error.</span><span class="sxs-lookup"><span data-stu-id="3e90c-138">In fact, most scripts run on the local computer using one of these two settings will also fail.</span></span>

<span data-ttu-id="3e90c-139">Impersonate permite al servicio WMI remoto usar el contexto de seguridad para realizar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="3e90c-139">Impersonate permits the remote WMI service to use your security context to perform the requested operation.</span></span> <span data-ttu-id="3e90c-140">Normalmente, una solicitud de WMI remota que usa la configuración de suplantación se realiza correctamente, siempre que las credenciales tengan privilegios suficientes para realizar la operación deseada.</span><span class="sxs-lookup"><span data-stu-id="3e90c-140">A remote WMI request that uses the Impersonate setting typically succeeds, provided your credentials have sufficient privileges to perform the intended operation.</span></span> <span data-ttu-id="3e90c-141">En otras palabras, no puede usar WMI para realizar una acción (de forma remota o de otro tipo) que no tenga permiso para realizar fuera de WMI.</span><span class="sxs-lookup"><span data-stu-id="3e90c-141">In other words, you cannot use WMI to perform an action (remotely or otherwise) that you do not have permission to perform outside WMI.</span></span>

<span data-ttu-id="3e90c-142">Establecer impersonationLevel en Delegate permite al servicio WMI remoto pasar sus credenciales a otros objetos y generalmente se considera un riesgo para la seguridad.</span><span class="sxs-lookup"><span data-stu-id="3e90c-142">Setting impersonationLevel to Delegate permits the remote WMI service to pass your credentials on to other objects and is generally considered a security risk.</span></span>

<span data-ttu-id="3e90c-143">Puede establecer el nivel de suplantación de un objeto [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)y [**SwbemLocator**](swbemlocator.md) estableciendo la propiedad **ImpersonationLevel** en el valor deseado.</span><span class="sxs-lookup"><span data-stu-id="3e90c-143">You can set the impersonation level of an [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) object by setting the **ImpersonationLevel** property to the desired value.</span></span> <span data-ttu-id="3e90c-144">En el ejemplo siguiente se muestra cómo establecer el nivel de suplantación para un objeto **SWbemObject** :</span><span class="sxs-lookup"><span data-stu-id="3e90c-144">The following example shows you how to set the impersonation level for an **SWbemObject** object:</span></span>


```VB
objinstance.Security_.ImpersonationLevel = _
    wbemImpersonationLevelImpersonate
```



<span data-ttu-id="3e90c-145">También puede especificar los niveles de suplantación como parte de un moniker.</span><span class="sxs-lookup"><span data-stu-id="3e90c-145">You can also specify impersonation levels as part of a moniker.</span></span> <span data-ttu-id="3e90c-146">En el ejemplo siguiente se establece el nivel de autenticación y el nivel de suplantación, y se recupera una instancia del [**\_ servicio de Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="3e90c-146">The following example sets the authentication level and the impersonation level, and retrieves an instance of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,"& _
                         "authenticationLevel=pktPrivacy}"& _
                         "!root/cimv2:Win32_service='ALERTER'")
```



## <a name="requirements"></a><span data-ttu-id="3e90c-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e90c-147">Requirements</span></span>



| <span data-ttu-id="3e90c-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e90c-148">Requirement</span></span> | <span data-ttu-id="3e90c-149">Value</span><span class="sxs-lookup"><span data-stu-id="3e90c-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e90c-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e90c-150">Minimum supported client</span></span><br/> | <span data-ttu-id="3e90c-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e90c-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e90c-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e90c-152">Minimum supported server</span></span><br/> | <span data-ttu-id="3e90c-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e90c-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e90c-154">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3e90c-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="3e90c-155"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3e90c-155"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3e90c-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e90c-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e90c-157"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e90c-157"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3e90c-158">CLSID</span><span class="sxs-lookup"><span data-stu-id="3e90c-158">CLSID</span></span><br/>                    | <span data-ttu-id="3e90c-159">CLSID \_ SWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="3e90c-159">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="3e90c-160">IID</span><span class="sxs-lookup"><span data-stu-id="3e90c-160">IID</span></span><br/>                      | <span data-ttu-id="3e90c-161">\_ISWBEMSECURITY IID</span><span class="sxs-lookup"><span data-stu-id="3e90c-161">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="3e90c-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e90c-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e90c-163">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="3e90c-163">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="3e90c-164">Establecer la \_ seguridad del proceso de la aplicación cliente \_</span><span class="sxs-lookup"><span data-stu-id="3e90c-164">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="3e90c-165">**WbemImpersonationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="3e90c-165">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> </dl>

 

