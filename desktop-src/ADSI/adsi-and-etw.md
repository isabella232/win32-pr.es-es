---
title: Seguimiento de eventos en ADSI
description: Windows Server 2008 y Windows Vista introducen el seguimiento de eventos en Active Directory interfaces de servicio (ADSI).
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- seguimiento de eventos ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f43c0d840cd1f3f70d293a0a4f5c299fd129efe
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656397"
---
# <a name="event-tracing-in-adsi"></a><span data-ttu-id="ff247-104">Seguimiento de eventos en ADSI</span><span class="sxs-lookup"><span data-stu-id="ff247-104">Event Tracing in ADSI</span></span>

<span data-ttu-id="ff247-105">Windows Server 2008 y Windows Vista introducen el [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) en [Active Directory interfaces de servicio](active-directory-service-interfaces-adsi.md) (ADSI).</span><span class="sxs-lookup"><span data-stu-id="ff247-105">Windows Server 2008 and Windows Vista introduce [Event Tracing](/windows/desktop/ETW/event-tracing-portal) in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="ff247-106">Ciertas áreas del proveedor LDAP de ADSI tienen una implementación subyacente compleja o que implica una secuencia de pasos que dificulta el diagnóstico de problemas.</span><span class="sxs-lookup"><span data-stu-id="ff247-106">Certain areas of the ADSI LDAP Provider have an underlying implementation that is complex or that involves a sequence of steps that makes it difficult to diagnose problems.</span></span> <span data-ttu-id="ff247-107">Para ayudar a los desarrolladores de aplicaciones a solucionar problemas, se ha agregado seguimiento de eventos a las siguientes áreas:</span><span class="sxs-lookup"><span data-stu-id="ff247-107">To help application developers troubleshoot, Event Tracing has been added to the following areas:</span></span>

## <a name="schema-parsing-and-downloading"></a><span data-ttu-id="ff247-108">Análisis y descarga de esquemas</span><span class="sxs-lookup"><span data-stu-id="ff247-108">Schema Parsing and Downloading</span></span>

<span data-ttu-id="ff247-109">La interfaz IADs en ADSI requiere que el esquema LDAP se almacene en caché en el cliente para que se puedan calcular las referencias de los atributos correctamente (como se describe en el [modelo de esquema ADSI](adsi-schema-model.md)).</span><span class="sxs-lookup"><span data-stu-id="ff247-109">The IADs interface in ADSI requires that the LDAP schema be cached on the client so that attributes can be marshaled correctly (as described in the [ADSI Schema Model](adsi-schema-model.md)).</span></span> <span data-ttu-id="ff247-110">Para ello, ADSI carga el esquema de cada proceso (y para cada servidor o dominio LDAP) en la memoria, ya sea desde un archivo de esquema (. SCH) guardado en el disco local o descargándolo desde el servidor LDAP.</span><span class="sxs-lookup"><span data-stu-id="ff247-110">To achieve this, ADSI loads the schema for each process (and for each LDAP server/domain) into memory either from a schema (.sch) file that is saved on the local disk or by downloading it from the LDAP server.</span></span> <span data-ttu-id="ff247-111">Los distintos procesos en el mismo equipo cliente usan el esquema almacenado en caché en disco si está disponible y es aplicable.</span><span class="sxs-lookup"><span data-stu-id="ff247-111">Different processes on the same client machine use the cached schema on disk if it is available and applicable.</span></span>

<span data-ttu-id="ff247-112">Si el esquema no se puede obtener del disco o del servidor, ADSI utiliza un esquema predeterminado codificado de forma rígida.</span><span class="sxs-lookup"><span data-stu-id="ff247-112">If the schema cannot be obtained from the disk or the server, ADSI uses a hardcoded default schema.</span></span> <span data-ttu-id="ff247-113">Cuando esto ocurre, no se pueden calcular las referencias de los atributos que no forman parte de este esquema predeterminado y ADSI devuelve un error al recuperar estos atributos.</span><span class="sxs-lookup"><span data-stu-id="ff247-113">When this occurs, attributes that are not part of this default schema cannot be marshaled and ADSI returns an error while retrieving these attributes.</span></span> <span data-ttu-id="ff247-114">Una serie de factores podría provocar que esto suceda, incluidos los problemas en el análisis del esquema, y privilegios insuficientes para descargar el esquema.</span><span class="sxs-lookup"><span data-stu-id="ff247-114">A number of factors could cause this to happen, including problems in parsing the schema, and insufficient privileges to download the schema.</span></span> <span data-ttu-id="ff247-115">A menudo resulta difícil determinar por qué se está usando cierto esquema predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ff247-115">It is often difficult to determine why a certain default schema is being used.</span></span> <span data-ttu-id="ff247-116">El uso del seguimiento de eventos en esta área le ayudará a diagnosticar más rápidamente el problema y solucionarlo.</span><span class="sxs-lookup"><span data-stu-id="ff247-116">Using Event Tracing in this area will help to more quickly diagnose the problem and fix it.</span></span>

## <a name="changing-and-setting-the-password"></a><span data-ttu-id="ff247-117">Cambiar y establecer la contraseña</span><span class="sxs-lookup"><span data-stu-id="ff247-117">Changing and Setting the Password</span></span>

<span data-ttu-id="ff247-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) y [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) emplean más de un mecanismo para realizar la operación solicitada en función de la configuración disponible (como se describe en [establecer y cambiar las contraseñas de usuario con el proveedor LDAP](setting-user-passwords-for-ldap-providers.md)).</span><span class="sxs-lookup"><span data-stu-id="ff247-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) and [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) employ more than one mechanism to perform the requested operation based on the available configuration (as described in [Setting and Changing User Passwords with the LDAP Provider](setting-user-passwords-for-ldap-providers.md)).</span></span> <span data-ttu-id="ff247-119">Cuando se produce un error en **ChangePassword** y **SetPassword** , puede ser difícil determinar exactamente por qué y el seguimiento de eventos ayuda a solucionar problemas con estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ff247-119">When **ChangePassword** and **SetPassword** fail, it can be difficult to determine exactly why, and Event Tracing will help to troubleshoot problems with these methods.</span></span>

## <a name="adsi-bind-cache"></a><span data-ttu-id="ff247-120">Caché de enlace de ADSI</span><span class="sxs-lookup"><span data-stu-id="ff247-120">ADSI Bind Cache</span></span>

<span data-ttu-id="ff247-121">ADSI intenta internamente reutilizar las conexiones LDAP siempre que sea posible (consulte [almacenamiento en caché de conexiones](connection-caching.md)).</span><span class="sxs-lookup"><span data-stu-id="ff247-121">ADSI internally tries to reuse LDAP connections whenever possible (see [Connection Caching](connection-caching.md)).</span></span> <span data-ttu-id="ff247-122">Al solucionar problemas, es útil realizar un seguimiento de si se ha abierto una conexión nueva para la comunicación con el servidor o si se ha utilizado una conexión existente.</span><span class="sxs-lookup"><span data-stu-id="ff247-122">When troubleshooting, it is useful to trace whether a new connection was opened for communication with the server or whether an existing connection was used.</span></span> <span data-ttu-id="ff247-123">También puede ser útil para realizar un seguimiento del ciclo de vida de la memoria caché de conexiones (a veces denominada caché de enlace) y su creación o cierre, y si tuvo lugar una referencia de conexión.</span><span class="sxs-lookup"><span data-stu-id="ff247-123">It can also be useful to trace the lifecycle of the connection cache (sometimes referred to as the bind cache) and its creation or closure, and whether a connection referral took place.</span></span> <span data-ttu-id="ff247-124">En el caso de un [enlace sin servidor](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI llama al Ubicador de DC para seleccionar un servidor para el dominio del contexto del usuario.</span><span class="sxs-lookup"><span data-stu-id="ff247-124">In the case of a [serverless bind](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI calls the DC locator to select a server for the domain of the user's context.</span></span> <span data-ttu-id="ff247-125">ADSI mantiene una memoria caché de la asignación de servidor de dominio para las conexiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ff247-125">ADSI then maintains a cache of the domain-server mapping for subsequent connections.</span></span> <span data-ttu-id="ff247-126">El seguimiento de eventos ayuda a realizar un seguimiento de la selección del controlador de dominio y, por tanto, es útil para solucionar problemas relacionados con la conexión.</span><span class="sxs-lookup"><span data-stu-id="ff247-126">Event Tracing helps to trace the selection of the DC, and is therefore helpful in troubleshooting connection-related issues.</span></span>

## <a name="enabling-tracing-and-starting-a-tracing-session"></a><span data-ttu-id="ff247-127">Habilitar el seguimiento e iniciar una sesión de seguimiento</span><span class="sxs-lookup"><span data-stu-id="ff247-127">Enabling Tracing and Starting a Tracing Session</span></span>

<span data-ttu-id="ff247-128">Para activar el seguimiento ADSI, cree la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="ff247-128">To turn on ADSI tracing, create the following registry key:</span></span>

<span data-ttu-id="ff247-129">**HKEY \_ \_** \\  \\  \\  \\  \\ **Seguimiento** \\  ADSI del sistema del equipo local de System CurrentControlSet</span><span class="sxs-lookup"><span data-stu-id="ff247-129">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\***ProcessName***</span></span>

<span data-ttu-id="ff247-130">*ProcessName* es el nombre completo del proceso del que se desea realizar un seguimiento, incluida su extensión (por ejemplo, "Svchost.exe").</span><span class="sxs-lookup"><span data-stu-id="ff247-130">*ProcessName* is the full name of the process that you want to trace, including its extension (for example, "Svchost.exe").</span></span> <span data-ttu-id="ff247-131">Además, puede colocar un valor opcional de tipo **DWORD** denominado PID en esta clave.</span><span class="sxs-lookup"><span data-stu-id="ff247-131">In addition, you can place an optional value of type **DWORD** named PID in this key.</span></span> <span data-ttu-id="ff247-132">Se recomienda establecer este valor y, por tanto, realizar un seguimiento solo de un proceso determinado.</span><span class="sxs-lookup"><span data-stu-id="ff247-132">It is highly recommended that you set this value and thereby trace only a particular process.</span></span> <span data-ttu-id="ff247-133">De lo contrario, se realizará un seguimiento de todas las instancias de la aplicación especificadas por *processName* .</span><span class="sxs-lookup"><span data-stu-id="ff247-133">Otherwise, all instances of the application specified by *ProcessName* will be traced.</span></span>

<span data-ttu-id="ff247-134">Después, ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="ff247-134">Then execute the following command:</span></span>

<span data-ttu-id="ff247-135">**tracelog.exe-Start** *nombresesión*  \* *-GUID \# \* \* \* proveedor \_ GUID* **-f** *nombre* **-marca** *traceFlags* **-LEVEL** *TraceLevel*</span><span class="sxs-lookup"><span data-stu-id="ff247-135">**tracelog.exe -start** *sessionname* \**-guid \#\*\*\*provider\_guid* **-f** *filename* **-flag** *traceFlags* **-level** *traceLevel*</span></span>

<span data-ttu-id="ff247-136">*nombresesión* es simplemente un identificador arbitrario que se usa para etiquetar la sesión de seguimiento (deberá hacer referencia a este nombre de sesión más adelante cuando detenga la sesión de seguimiento).</span><span class="sxs-lookup"><span data-stu-id="ff247-136">*sessionname* is simply an arbitrary identifier that is used to label the tracing session (you will need to refer to this session name later when you stop the tracing session).</span></span> <span data-ttu-id="ff247-137">El GUID del proveedor de seguimiento de ADSI es "7288c9f8-d63c-4932-A345-89d6b060174d".</span><span class="sxs-lookup"><span data-stu-id="ff247-137">The GUID for the ADSI tracking provider is "7288c9f8-d63c-4932-a345-89d6b060174d".</span></span> <span data-ttu-id="ff247-138">*filename* especifica el archivo de registro en el que se escribirán los eventos.</span><span class="sxs-lookup"><span data-stu-id="ff247-138">*filename* specifies the logfile to which events will be written.</span></span> <span data-ttu-id="ff247-139">*traceFlags* debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="ff247-139">*traceFlags* should be one of the following values:</span></span>



|                                 |                       |
|---------------------------------|-----------------------|
| <span data-ttu-id="ff247-140">**esquema de depuración \_**</span><span class="sxs-lookup"><span data-stu-id="ff247-140">**DEBUG\_SCHEMA**</span></span><br/>    | <span data-ttu-id="ff247-141">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ff247-141">0x00000001</span></span><br/> |
| <span data-ttu-id="ff247-142">**depurar \_ CHANGEPWD**</span><span class="sxs-lookup"><span data-stu-id="ff247-142">**DEBUG\_CHANGEPWD**</span></span><br/> | <span data-ttu-id="ff247-143">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ff247-143">0x00000002</span></span><br/> |
| <span data-ttu-id="ff247-144">**depuración \_ SETPWD**</span><span class="sxs-lookup"><span data-stu-id="ff247-144">**DEBUG\_SETPWD**</span></span><br/>    | <span data-ttu-id="ff247-145">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ff247-145">0x00000004</span></span><br/> |
| <span data-ttu-id="ff247-146">**depurar \_ BINDCACHE**</span><span class="sxs-lookup"><span data-stu-id="ff247-146">**DEBUG\_BINDCACHE**</span></span><br/> | <span data-ttu-id="ff247-147">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ff247-147">0x00000008</span></span><br/> |



 

<span data-ttu-id="ff247-148">Estas marcas determinan a qué métodos [ADSI](active-directory-service-interfaces-adsi.md) se realizará un seguimiento, de acuerdo con la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="ff247-148">These flags determine which [ADSI](active-directory-service-interfaces-adsi.md) methods will be traced, according to the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ff247-149"><strong>DEBUG_SCHEMA</strong></span><span class="sxs-lookup"><span data-stu-id="ff247-149"><strong>DEBUG_SCHEMA</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="ff247-150">LdapGetSchema</span><span class="sxs-lookup"><span data-stu-id="ff247-150">LdapGetSchema</span></span></li>
<li><span data-ttu-id="ff247-151">GetSchemaInfoTime</span><span class="sxs-lookup"><span data-stu-id="ff247-151">GetSchemaInfoTime</span></span></li>
<li><span data-ttu-id="ff247-152">LdapReadSchemaInfoFromServer</span><span class="sxs-lookup"><span data-stu-id="ff247-152">LdapReadSchemaInfoFromServer</span></span></li>
<li><span data-ttu-id="ff247-153">ProcessSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="ff247-153">ProcessSchemaInfo</span></span></li>
<li><span data-ttu-id="ff247-154">HelperReadLdapSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="ff247-154">HelperReadLdapSchemaInfo</span></span></li>
<li><span data-ttu-id="ff247-155">ProcessClassInfoArray</span><span class="sxs-lookup"><span data-stu-id="ff247-155">ProcessClassInfoArray</span></span></li>
<li><span data-ttu-id="ff247-156">ReadSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="ff247-156">ReadSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="ff247-157">StoreSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="ff247-157">StoreSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="ff247-158">AttributeTypeDescription</span><span class="sxs-lookup"><span data-stu-id="ff247-158">AttributeTypeDescription</span></span></li>
<li><span data-ttu-id="ff247-159">ObjectClassDescription</span><span class="sxs-lookup"><span data-stu-id="ff247-159">ObjectClassDescription</span></span></li>
<li><span data-ttu-id="ff247-160">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="ff247-160">DITContentRuleDescription</span></span></li>
<li><span data-ttu-id="ff247-161">DirectoryString</span><span class="sxs-lookup"><span data-stu-id="ff247-161">DirectoryString</span></span></li>
<li><span data-ttu-id="ff247-162">DirectoryStrings</span><span class="sxs-lookup"><span data-stu-id="ff247-162">DirectoryStrings</span></span></li>
<li><span data-ttu-id="ff247-163">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="ff247-163">DITContentRuleDescription</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff247-164"><strong>DEBUG_CHANGEPWD</strong></span><span class="sxs-lookup"><span data-stu-id="ff247-164"><strong>DEBUG_CHANGEPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="ff247-165">CADsUser:: ChangePassword</span><span class="sxs-lookup"><span data-stu-id="ff247-165">CADsUser::ChangePassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff247-166"><strong>DEBUG_SETPWD</strong></span><span class="sxs-lookup"><span data-stu-id="ff247-166"><strong>DEBUG_SETPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="ff247-167">CADsUser:: SetPassword</span><span class="sxs-lookup"><span data-stu-id="ff247-167">CADsUser::SetPassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff247-168"><strong>DEBUG_BINDCACHE</strong></span><span class="sxs-lookup"><span data-stu-id="ff247-168"><strong>DEBUG_BINDCACHE</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="ff247-169">GetServerBasedObject</span><span class="sxs-lookup"><span data-stu-id="ff247-169">GetServerBasedObject</span></span></li>
<li><span data-ttu-id="ff247-170">GetServerLessBasedObject</span><span class="sxs-lookup"><span data-stu-id="ff247-170">GetServerLessBasedObject</span></span></li>
<li><span data-ttu-id="ff247-171">GetGCDomainName</span><span class="sxs-lookup"><span data-stu-id="ff247-171">GetGCDomainName</span></span></li>
<li><span data-ttu-id="ff247-172">GetDefaultDomainName</span><span class="sxs-lookup"><span data-stu-id="ff247-172">GetDefaultDomainName</span></span></li>
<li><span data-ttu-id="ff247-173">GetUserDomainFlatName</span><span class="sxs-lookup"><span data-stu-id="ff247-173">GetUserDomainFlatName</span></span></li>
<li><span data-ttu-id="ff247-174">BindCacheLookup</span><span class="sxs-lookup"><span data-stu-id="ff247-174">BindCacheLookup</span></span></li>
<li><span data-ttu-id="ff247-175">EquivalentPortNumbers</span><span class="sxs-lookup"><span data-stu-id="ff247-175">EquivalentPortNumbers</span></span></li>
<li><span data-ttu-id="ff247-176">CanCredentialsBeReused</span><span class="sxs-lookup"><span data-stu-id="ff247-176">CanCredentialsBeReused</span></span></li>
<li><span data-ttu-id="ff247-177">BindCacheAdd</span><span class="sxs-lookup"><span data-stu-id="ff247-177">BindCacheAdd</span></span></li>
<li><span data-ttu-id="ff247-178">BindCacheAddRef</span><span class="sxs-lookup"><span data-stu-id="ff247-178">BindCacheAddRef</span></span></li>
<li><span data-ttu-id="ff247-179">AddReferralLink</span><span class="sxs-lookup"><span data-stu-id="ff247-179">AddReferralLink</span></span></li>
<li><span data-ttu-id="ff247-180">CommonRemoveEntry</span><span class="sxs-lookup"><span data-stu-id="ff247-180">CommonRemoveEntry</span></span></li>
<li><span data-ttu-id="ff247-181">BindCacheDerefHelper</span><span class="sxs-lookup"><span data-stu-id="ff247-181">BindCacheDerefHelper</span></span></li>
<li><span data-ttu-id="ff247-182">NotifyNewConnection</span><span class="sxs-lookup"><span data-stu-id="ff247-182">NotifyNewConnection</span></span></li>
<li><span data-ttu-id="ff247-183">QueryForConnection</span><span class="sxs-lookup"><span data-stu-id="ff247-183">QueryForConnection</span></span></li>
<li><span data-ttu-id="ff247-184">LdapOpenBindWithCredentials</span><span class="sxs-lookup"><span data-stu-id="ff247-184">LdapOpenBindWithCredentials</span></span></li>
<li><span data-ttu-id="ff247-185">LdapOpenBindWithDefaultCredentials</span><span class="sxs-lookup"><span data-stu-id="ff247-185">LdapOpenBindWithDefaultCredentials</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ff247-186">Puede combinar marcas combinando los bits adecuados en el argumento *traceFlags* .</span><span class="sxs-lookup"><span data-stu-id="ff247-186">You can combine flags by combining the appropriate bits in the *traceFlags* argument.</span></span> <span data-ttu-id="ff247-187">Por ejemplo, para especificar el **\_ esquema de depuración** y **depurar las marcas \_ BINDCACHE** , el valor de *traceFlags* adecuado sería 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="ff247-187">For example, to specify the **DEBUG\_SCHEMA** and **DEBUG\_BINDCACHE** flags, the appropriate *traceFlags* value would be 0x00000009.</span></span>

<span data-ttu-id="ff247-188">Por último, la marca *TraceLevel* debe ser uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="ff247-188">Finally, the *traceLevel* flag should be one of the following values:</span></span>



|                                          |                       |
|------------------------------------------|-----------------------|
| <span data-ttu-id="ff247-189">**\_error de nivel de seguimiento \_**</span><span class="sxs-lookup"><span data-stu-id="ff247-189">**TRACE\_LEVEL\_ERROR**</span></span><br/>       | <span data-ttu-id="ff247-190">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ff247-190">0x00000002</span></span><br/> |
| <span data-ttu-id="ff247-191">**\_información del nivel de seguimiento \_**</span><span class="sxs-lookup"><span data-stu-id="ff247-191">**TRACE\_LEVEL\_INFORMATION**</span></span><br/> | <span data-ttu-id="ff247-192">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ff247-192">0x00000004</span></span><br/> |



 

<span data-ttu-id="ff247-193">**Seguimiento \_ de La \_ información de nivel** hace que el proceso de seguimiento grabe todos los eventos, mientras que el **error de \_ nivel \_ de seguimiento** hace que el proceso de seguimiento registre solo los eventos de error.</span><span class="sxs-lookup"><span data-stu-id="ff247-193">**TRACE\_LEVEL\_INFORMATION** causes the tracing process to record all events, whereas **TRACE\_LEVEL\_ERROR** causes the tracing process to record only error events.</span></span>

<span data-ttu-id="ff247-194">Para finalizar el seguimiento, ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="ff247-194">To terminate tracing, run the following command:</span></span>

<span data-ttu-id="ff247-195">**tracelog.exe-STOP** *nombresesión*</span><span class="sxs-lookup"><span data-stu-id="ff247-195">**tracelog.exe -stop** *sessionname*</span></span>

<span data-ttu-id="ff247-196">En el ejemplo anterior, *nombresesión* es el mismo nombre que el que se proporcionó con el comando que inició la sección de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="ff247-196">In the previous example, *sessionname* is the same name as the one that was provided with the command that started the tracing section.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff247-197">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff247-197">Remarks</span></span>

<span data-ttu-id="ff247-198">Es más eficaz realizar un seguimiento de los procesos específicos mediante la especificación de un determinado PID que para realizar el seguimiento de todos los procesos de un equipo.</span><span class="sxs-lookup"><span data-stu-id="ff247-198">It is more effective to trace only specific processes by specifying a particular PID than to trace all processes on a computer.</span></span> <span data-ttu-id="ff247-199">Si necesita realizar un seguimiento de varias aplicaciones en el mismo equipo, puede haber un impacto en el rendimiento. hay una salida de depuración considerable en las secciones orientadas al rendimiento del código.</span><span class="sxs-lookup"><span data-stu-id="ff247-199">If you do need to trace multiple applications on the same machine, there might be a performance impact; there is substantial debugging output in performance-oriented sections of the code.</span></span> <span data-ttu-id="ff247-200">Además, los administradores deben tener cuidado para establecer correctamente los permisos de los archivos de registro al realizar un seguimiento de varios procesos. de lo contrario, cualquier usuario podría leer los registros de seguimiento y otros usuarios podrán realizar un seguimiento de los procesos que contienen información segura.</span><span class="sxs-lookup"><span data-stu-id="ff247-200">Also, administrators must be careful to properly set the permissions of the log files when tracing multiple processes; otherwise, any user might be able to read the tracing logs, and other users will be able to trace processes that contain secure information.</span></span>

<span data-ttu-id="ff247-201">Por ejemplo, supongamos que el administrador configura el seguimiento para una aplicación "Test.exe" y no especifica un PID en el registro para realizar un seguimiento de varias instancias del proceso.</span><span class="sxs-lookup"><span data-stu-id="ff247-201">For example, presume the administrator sets up tracing for an application "Test.exe", and does not specify a PID in the registry to trace multiple instances of the process.</span></span> <span data-ttu-id="ff247-202">Ahora otro usuario desea realizar un seguimiento de la aplicación "Secure.exe".</span><span class="sxs-lookup"><span data-stu-id="ff247-202">Now another user wants to trace the application "Secure.exe".</span></span> <span data-ttu-id="ff247-203">Si los archivos de registro de seguimiento no están restringidos correctamente, lo único que debe hacer el usuario es cambiar el nombre de "Secure.exe" a "Test.exe" y se realizará un seguimiento.</span><span class="sxs-lookup"><span data-stu-id="ff247-203">If the tracing log files are not properly restricted, all that user needs to do is rename "Secure.exe" to "Test.exe", and it will be traced.</span></span> <span data-ttu-id="ff247-204">En general, es mejor realizar un seguimiento solo de procesos específicos durante la solución de problemas y quitar la clave del registro de seguimiento en cuanto se realiza la solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="ff247-204">In general, it is best to trace only specific processes while troubleshooting, and to remove the tracing registry key as soon as troubleshooting is done.</span></span>

<span data-ttu-id="ff247-205">Dado que la habilitación del seguimiento de eventos generará archivos de registro adicionales, los administradores deben supervisar cuidadosamente los tamaños de los archivos de registro. la falta de espacio en disco en el equipo local puede producir una denegación de servicio.</span><span class="sxs-lookup"><span data-stu-id="ff247-205">Since enabling Event Tracing will produce extra log files, administrators should carefully monitor log file sizes; lack of disk space on the local computer can cause a denial-of-service.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="ff247-206">Escenarios de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ff247-206">Example Scenarios</span></span>

<span data-ttu-id="ff247-207">Escenario 1: el administrador ve un error inesperado en una aplicación que establece contraseñas para las cuentas de usuario, por lo que llevaría a cabo los pasos siguientes para solucionar el problema con el seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="ff247-207">Scenario 1: The administrator sees an unexpected error in an application that sets passwords for user accounts, so they would take the following steps to fix the problem using Event Tracing.</span></span>

1.  <span data-ttu-id="ff247-208">Escriba un script que reproduzca el problema y cree la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="ff247-208">Write a script that reproduces the problem, and create the registry key</span></span>

    <span data-ttu-id="ff247-209">**HKEY \_ Sistema \_ equipo local** \\  \\ **CurrentControlSet** \\ **Services** \\  \\ **seguimiento** ADSI \\ **cscript.exe**</span><span class="sxs-lookup"><span data-stu-id="ff247-209">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

2.  <span data-ttu-id="ff247-210">Inicie una sesión de seguimiento, estableciendo *traceFlags* en 0X2 (**Debug \_ CHANGEPASSWD**) y *TraceLevel* en 0x4 (**\_ \_ información del nivel de seguimiento**) con el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="ff247-210">Start a tracing session, setting *traceFlags* to 0x2 (**DEBUG\_CHANGEPASSWD**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**), using the following command:</span></span>

    <span data-ttu-id="ff247-211">**tracelog.exe-Start scripttrace-GUID \# 7288c9f8-d63c-4932-A345-89d6b060174d-f. \\ ADSI. ETL: marca 0X2-nivel 0x4**</span><span class="sxs-lookup"><span data-stu-id="ff247-211">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

3.  <span data-ttu-id="ff247-212">Ejecute cscript.exe con su script de prueba para reproducir el problema y, a continuación, finalice la sesión de seguimiento:</span><span class="sxs-lookup"><span data-stu-id="ff247-212">Run cscript.exe with their test script to reproduce the problem, and then terminate the tracing session:</span></span>

    <span data-ttu-id="ff247-213">**tracelog.exe: detener scripttrace**</span><span class="sxs-lookup"><span data-stu-id="ff247-213">**tracelog.exe -stop scripttrace**</span></span>

4.  <span data-ttu-id="ff247-214">Eliminar la clave del registro</span><span class="sxs-lookup"><span data-stu-id="ff247-214">Delete the registry key</span></span>

    <span data-ttu-id="ff247-215">**HKEY \_ Sistema \_ equipo local** \\  \\ **CurrentControlSet** \\ **Services** \\  \\ **seguimiento** ADSI \\ **cscript.exe**</span><span class="sxs-lookup"><span data-stu-id="ff247-215">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

5.  <span data-ttu-id="ff247-216">Ejecute la herramienta ETW Tracerpt.exe para analizar la información de seguimiento del registro:</span><span class="sxs-lookup"><span data-stu-id="ff247-216">Run the ETW tool Tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="ff247-217">**tracelog.exe-Start scripttrace-GUID \# 7288c9f8-d63c-4932-A345-89d6b060174d-f. \\ ADSI. ETL: marca 0X2-nivel 0x4**</span><span class="sxs-lookup"><span data-stu-id="ff247-217">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

<span data-ttu-id="ff247-218">Escenario 2: el administrador desea realizar un seguimiento de las operaciones de análisis y descarga de esquemas en una aplicación [asp](https://msdn.microsoft.com/asp.net/default.aspx) denominada w3wp.exe que ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="ff247-218">Scenario 2: The administrator wants to trace the schema parsing and download operations in an [ASP](https://msdn.microsoft.com/asp.net/default.aspx) application named w3wp.exe that is already running.</span></span> <span data-ttu-id="ff247-219">Para ello, el administrador llevaría a cabo los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="ff247-219">To do this, the administrator would take the following steps:</span></span>

1.  <span data-ttu-id="ff247-220">Crear la clave del registro</span><span class="sxs-lookup"><span data-stu-id="ff247-220">Create the registry key</span></span>

    <span data-ttu-id="ff247-221">**HKEY \_ Sistema \_ equipo local** \\  \\ **CurrentControlSet** \\ **Services** \\  \\ **seguimiento** ADSI \\ **w3wp.exe**</span><span class="sxs-lookup"><span data-stu-id="ff247-221">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**</span></span>

    <span data-ttu-id="ff247-222">y dentro de esa clave, cree un valor de tipo DWORD que se denomine PID y establézcalo en el ID. de proceso de la instancia de w3wp.exe que se está ejecutando actualmente en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="ff247-222">and inside that key, create a value of type DWORD that is named PID and set it to the process ID of the instance of w3wp.exe that is currently running on the local computer.</span></span>

2.  <span data-ttu-id="ff247-223">A continuación, se crea una sesión de seguimiento, se establece el valor de *traceFlags* en 0x1 (**\_ esquema de depuración**) y *TraceLevel* en 0x4 (**información del \_ nivel \_ de seguimiento**):</span><span class="sxs-lookup"><span data-stu-id="ff247-223">Then they create a tracing session, setting *traceFlags* to 0x1 (**DEBUG\_SCHEMA**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**):</span></span>

    <span data-ttu-id="ff247-224">**tracelog.exe-Start w3wptrace-GUID \# 7288c9f8-d63c-4932-A345-89d6b060174d-f. \\ w3wp. ETL: marca 0x1-nivel 0x4**</span><span class="sxs-lookup"><span data-stu-id="ff247-224">**tracelog.exe -start w3wptrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\w3wp.etl -flag 0x1 -level 0x4**</span></span>

3.  <span data-ttu-id="ff247-225">Reproduzca la operación que necesita solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="ff247-225">Reproduce the operation that needs troubleshooting.</span></span>
4.  <span data-ttu-id="ff247-226">Finalice la sesión de seguimiento:</span><span class="sxs-lookup"><span data-stu-id="ff247-226">Terminate the tracing session:</span></span>

    <span data-ttu-id="ff247-227">**tracelog.exe: detener w3wptrace**</span><span class="sxs-lookup"><span data-stu-id="ff247-227">**tracelog.exe -stop w3wptrace**</span></span>

5.  <span data-ttu-id="ff247-228">Elimine la clave del registro **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **ADSI** \\ **Tracing** \\ **w3wp.exe**.</span><span class="sxs-lookup"><span data-stu-id="ff247-228">Delete the registry key **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**.</span></span>
6.  <span data-ttu-id="ff247-229">Ejecute la herramienta ETW tracerpt.exe para analizar la información de seguimiento del registro:</span><span class="sxs-lookup"><span data-stu-id="ff247-229">Run the ETW tool tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="ff247-230">**tracerpt.exe. \\ w3wp. ETL-o-Report**</span><span class="sxs-lookup"><span data-stu-id="ff247-230">**tracerpt.exe .\\w3wp.etl -o -report**</span></span>

 

