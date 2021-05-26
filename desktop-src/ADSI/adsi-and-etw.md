---
title: Seguimiento de eventos en ADSI
description: Windows Server 2008 y Windows Vista presentan el seguimiento de eventos en Active Directory interfaces de servicio (ADSI).
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- ADSI de seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b26aee00404f5cf97d228698f64fec804c28e62
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423725"
---
# <a name="event-tracing-in-adsi"></a><span data-ttu-id="da948-104">Seguimiento de eventos en ADSI</span><span class="sxs-lookup"><span data-stu-id="da948-104">Event Tracing in ADSI</span></span>

<span data-ttu-id="da948-105">Windows Server 2008 y Windows Vista presentan [el](/windows/desktop/ETW/event-tracing-portal) seguimiento de eventos [Active Directory interfaces de servicio](active-directory-service-interfaces-adsi.md) (ADSI).</span><span class="sxs-lookup"><span data-stu-id="da948-105">Windows Server 2008 and Windows Vista introduce [Event Tracing](/windows/desktop/ETW/event-tracing-portal) in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="da948-106">Algunas áreas del proveedor LDAP adsi tienen una implementación subyacente que es compleja o que implica una secuencia de pasos que dificulta el diagnóstico de problemas.</span><span class="sxs-lookup"><span data-stu-id="da948-106">Certain areas of the ADSI LDAP Provider have an underlying implementation that is complex or that involves a sequence of steps that makes it difficult to diagnose problems.</span></span> <span data-ttu-id="da948-107">Para ayudar a los desarrolladores de aplicaciones a solucionar problemas, el seguimiento de eventos se ha agregado a las áreas siguientes:</span><span class="sxs-lookup"><span data-stu-id="da948-107">To help application developers troubleshoot, Event Tracing has been added to the following areas:</span></span>

## <a name="schema-parsing-and-downloading"></a><span data-ttu-id="da948-108">Análisis y descarga de esquemas</span><span class="sxs-lookup"><span data-stu-id="da948-108">Schema Parsing and Downloading</span></span>

<span data-ttu-id="da948-109">La interfaz IADs de ADSI requiere que el esquema LDAP se almacene en caché en el cliente para que los atributos se puedan serializar correctamente (como se describe en el modelo de esquema [ADSI](adsi-schema-model.md)).</span><span class="sxs-lookup"><span data-stu-id="da948-109">The IADs interface in ADSI requires that the LDAP schema be cached on the client so that attributes can be marshaled correctly (as described in the [ADSI Schema Model](adsi-schema-model.md)).</span></span> <span data-ttu-id="da948-110">Para ello, ADSI carga el esquema para cada proceso (y para cada servidor LDAP o dominio) en memoria desde un archivo de esquema (.sch) guardado en el disco local o descargándose desde el servidor LDAP.</span><span class="sxs-lookup"><span data-stu-id="da948-110">To achieve this, ADSI loads the schema for each process (and for each LDAP server/domain) into memory either from a schema (.sch) file that is saved on the local disk or by downloading it from the LDAP server.</span></span> <span data-ttu-id="da948-111">Los distintos procesos de la misma máquina cliente usan el esquema almacenado en caché en el disco si está disponible y es aplicable.</span><span class="sxs-lookup"><span data-stu-id="da948-111">Different processes on the same client machine use the cached schema on disk if it is available and applicable.</span></span>

<span data-ttu-id="da948-112">Si el esquema no se puede obtener del disco o del servidor, ADSI usa un esquema predeterminado codificado de forma rígida.</span><span class="sxs-lookup"><span data-stu-id="da948-112">If the schema cannot be obtained from the disk or the server, ADSI uses a hardcoded default schema.</span></span> <span data-ttu-id="da948-113">Cuando esto sucede, los atributos que no forman parte de este esquema predeterminado no se pueden serializar y ADSI devuelve un error al recuperar estos atributos.</span><span class="sxs-lookup"><span data-stu-id="da948-113">When this occurs, attributes that are not part of this default schema cannot be marshaled and ADSI returns an error while retrieving these attributes.</span></span> <span data-ttu-id="da948-114">Varios factores podrían provocar que esto suceda, incluidos problemas al analizar el esquema y privilegios insuficientes para descargar el esquema.</span><span class="sxs-lookup"><span data-stu-id="da948-114">A number of factors could cause this to happen, including problems in parsing the schema, and insufficient privileges to download the schema.</span></span> <span data-ttu-id="da948-115">A menudo es difícil determinar por qué se usa un determinado esquema predeterminado.</span><span class="sxs-lookup"><span data-stu-id="da948-115">It is often difficult to determine why a certain default schema is being used.</span></span> <span data-ttu-id="da948-116">El uso del seguimiento de eventos en esta área le ayudará a diagnosticar el problema y corregirlo más rápidamente.</span><span class="sxs-lookup"><span data-stu-id="da948-116">Using Event Tracing in this area will help to more quickly diagnose the problem and fix it.</span></span>

## <a name="changing-and-setting-the-password"></a><span data-ttu-id="da948-117">Cambiar y establecer la contraseña</span><span class="sxs-lookup"><span data-stu-id="da948-117">Changing and Setting the Password</span></span>

<span data-ttu-id="da948-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) y [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) emplean más de un mecanismo para realizar la operación solicitada en función de la configuración disponible (como se describe en Establecimiento y cambio de contraseñas de usuario con el [proveedor LDAP).](setting-user-passwords-for-ldap-providers.md)</span><span class="sxs-lookup"><span data-stu-id="da948-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) and [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) employ more than one mechanism to perform the requested operation based on the available configuration (as described in [Setting and Changing User Passwords with the LDAP Provider](setting-user-passwords-for-ldap-providers.md)).</span></span> <span data-ttu-id="da948-119">Cuando se produce un error en **ChangePassword** y **SetPassword,** puede ser difícil determinar exactamente por qué, y el seguimiento de eventos le ayudará a solucionar problemas con estos métodos.</span><span class="sxs-lookup"><span data-stu-id="da948-119">When **ChangePassword** and **SetPassword** fail, it can be difficult to determine exactly why, and Event Tracing will help to troubleshoot problems with these methods.</span></span>

## <a name="adsi-bind-cache"></a><span data-ttu-id="da948-120">Caché de enlace ADSI</span><span class="sxs-lookup"><span data-stu-id="da948-120">ADSI Bind Cache</span></span>

<span data-ttu-id="da948-121">ADSI intenta reutilizar internamente las conexiones LDAP siempre que sea posible (consulte [Almacenamiento en caché de conexiones).](connection-caching.md)</span><span class="sxs-lookup"><span data-stu-id="da948-121">ADSI internally tries to reuse LDAP connections whenever possible (see [Connection Caching](connection-caching.md)).</span></span> <span data-ttu-id="da948-122">Al solucionar problemas, resulta útil hacer un seguimiento de si se abrió una nueva conexión para la comunicación con el servidor o si se usó una conexión existente.</span><span class="sxs-lookup"><span data-stu-id="da948-122">When troubleshooting, it is useful to trace whether a new connection was opened for communication with the server or whether an existing connection was used.</span></span> <span data-ttu-id="da948-123">También puede ser útil realizar un seguimiento del ciclo de vida de la caché de conexiones (a veces denominada caché de enlace) y su creación o cierre, y si se produjo una referencia de conexión.</span><span class="sxs-lookup"><span data-stu-id="da948-123">It can also be useful to trace the lifecycle of the connection cache (sometimes referred to as the bind cache) and its creation or closure, and whether a connection referral took place.</span></span> <span data-ttu-id="da948-124">En el caso de [un](/windows/desktop/AD/serverless-binding-and-rootdse)enlace sin servidor, ADSI llama al localizador de controlador de dominio para seleccionar un servidor para el dominio del contexto del usuario.</span><span class="sxs-lookup"><span data-stu-id="da948-124">In the case of a [serverless bind](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI calls the DC locator to select a server for the domain of the user's context.</span></span> <span data-ttu-id="da948-125">A continuación, ADSI mantiene una caché de la asignación de dominio-servidor para las conexiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="da948-125">ADSI then maintains a cache of the domain-server mapping for subsequent connections.</span></span> <span data-ttu-id="da948-126">Seguimiento de eventos ayuda a realizar un seguimiento de la selección del controlador de dominio y, por tanto, resulta útil para solucionar problemas relacionados con la conexión.</span><span class="sxs-lookup"><span data-stu-id="da948-126">Event Tracing helps to trace the selection of the DC, and is therefore helpful in troubleshooting connection-related issues.</span></span>

## <a name="enabling-tracing-and-starting-a-tracing-session"></a><span data-ttu-id="da948-127">Habilitar el seguimiento e iniciar una sesión de seguimiento</span><span class="sxs-lookup"><span data-stu-id="da948-127">Enabling Tracing and Starting a Tracing Session</span></span>

<span data-ttu-id="da948-128">Para activar el seguimiento de ADSI, cree la siguiente clave del Registro:</span><span class="sxs-lookup"><span data-stu-id="da948-128">To turn on ADSI tracing, create the following registry key:</span></span>

<span data-ttu-id="da948-129">**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **_ProcessName_**</span><span class="sxs-lookup"><span data-stu-id="da948-129">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**_ProcessName_**</span></span>

<span data-ttu-id="da948-130">*ProcessName* es el nombre completo del proceso del que desea hacer un seguimiento, incluida su extensión (por ejemplo, "Svchost.exe").</span><span class="sxs-lookup"><span data-stu-id="da948-130">*ProcessName* is the full name of the process that you want to trace, including its extension (for example, "Svchost.exe").</span></span> <span data-ttu-id="da948-131">Además, puede colocar un valor opcional de tipo **DWORD** denominado PID en esta clave.</span><span class="sxs-lookup"><span data-stu-id="da948-131">In addition, you can place an optional value of type **DWORD** named PID in this key.</span></span> <span data-ttu-id="da948-132">Se recomienda encarecidamente establecer este valor y, por tanto, realizar un seguimiento solo de un proceso determinado.</span><span class="sxs-lookup"><span data-stu-id="da948-132">It is highly recommended that you set this value and thereby trace only a particular process.</span></span> <span data-ttu-id="da948-133">De lo contrario, se realizará el seguimiento de todas las instancias de la aplicación especificadas por *ProcessName.*</span><span class="sxs-lookup"><span data-stu-id="da948-133">Otherwise, all instances of the application specified by *ProcessName* will be traced.</span></span>

<span data-ttu-id="da948-134">A continuación, ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="da948-134">Then execute the following command:</span></span>

<span data-ttu-id="da948-135">**tracelog.exe -start** *sessionname* **-guid \# provider** _\_ guid_ **-f** *filename* **-flag** *traceFlags* **-level** *traceLevel*</span><span class="sxs-lookup"><span data-stu-id="da948-135">**tracelog.exe -start** *sessionname* **-guid \#**_provider\_guid_ **-f** *filename* **-flag** *traceFlags* **-level** *traceLevel*</span></span>

<span data-ttu-id="da948-136">*sessionname* es simplemente un identificador arbitrario que se usa para etiquetar la sesión de seguimiento (tendrá que hacer referencia a este nombre de sesión más adelante cuando detenga la sesión de seguimiento).</span><span class="sxs-lookup"><span data-stu-id="da948-136">*sessionname* is simply an arbitrary identifier that is used to label the tracing session (you will need to refer to this session name later when you stop the tracing session).</span></span> <span data-ttu-id="da948-137">El GUID del proveedor de seguimiento ADSI es "7288c9f8-d63c-4932-a345-89d6b060174d".</span><span class="sxs-lookup"><span data-stu-id="da948-137">The GUID for the ADSI tracking provider is "7288c9f8-d63c-4932-a345-89d6b060174d".</span></span> <span data-ttu-id="da948-138">*filename* especifica el archivo de registro en el que se escribirán los eventos.</span><span class="sxs-lookup"><span data-stu-id="da948-138">*filename* specifies the logfile to which events will be written.</span></span> <span data-ttu-id="da948-139">*traceFlags* debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="da948-139">*traceFlags* should be one of the following values:</span></span>



|         <span data-ttu-id="da948-140">Marca</span><span class="sxs-lookup"><span data-stu-id="da948-140">Flag</span></span>                        |         <span data-ttu-id="da948-141">Value</span><span class="sxs-lookup"><span data-stu-id="da948-141">Value</span></span>              |
|---------------------------------|-----------------------|
| <span data-ttu-id="da948-142">**ESQUEMA DE \_ DEPURACIÓN**</span><span class="sxs-lookup"><span data-stu-id="da948-142">**DEBUG\_SCHEMA**</span></span><br/>    | <span data-ttu-id="da948-143">0x00000001</span><span class="sxs-lookup"><span data-stu-id="da948-143">0x00000001</span></span><br/> |
| <span data-ttu-id="da948-144">**DEBUG \_ CHANGEPWD**</span><span class="sxs-lookup"><span data-stu-id="da948-144">**DEBUG\_CHANGEPWD**</span></span><br/> | <span data-ttu-id="da948-145">0x00000002</span><span class="sxs-lookup"><span data-stu-id="da948-145">0x00000002</span></span><br/> |
| <span data-ttu-id="da948-146">**DEBUG \_ SETPWD**</span><span class="sxs-lookup"><span data-stu-id="da948-146">**DEBUG\_SETPWD**</span></span><br/>    | <span data-ttu-id="da948-147">0x00000004</span><span class="sxs-lookup"><span data-stu-id="da948-147">0x00000004</span></span><br/> |
| <span data-ttu-id="da948-148">**DEBUG \_ BINDCACHE**</span><span class="sxs-lookup"><span data-stu-id="da948-148">**DEBUG\_BINDCACHE**</span></span><br/> | <span data-ttu-id="da948-149">0x00000008</span><span class="sxs-lookup"><span data-stu-id="da948-149">0x00000008</span></span><br/> |



 

<span data-ttu-id="da948-150">Estas marcas determinan los métodos [ADSI](active-directory-service-interfaces-adsi.md) de los que se realizará el seguimiento, según la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="da948-150">These flags determine which [ADSI](active-directory-service-interfaces-adsi.md) methods will be traced, according to the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="da948-151"><strong>DEBUG_SCHEMA</strong></span><span class="sxs-lookup"><span data-stu-id="da948-151"><strong>DEBUG_SCHEMA</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="da948-152">LdapGetSchema</span><span class="sxs-lookup"><span data-stu-id="da948-152">LdapGetSchema</span></span></li>
<li><span data-ttu-id="da948-153">GetSchemaInfoTime</span><span class="sxs-lookup"><span data-stu-id="da948-153">GetSchemaInfoTime</span></span></li>
<li><span data-ttu-id="da948-154">LdapReadSchemaInfoFromServer</span><span class="sxs-lookup"><span data-stu-id="da948-154">LdapReadSchemaInfoFromServer</span></span></li>
<li><span data-ttu-id="da948-155">ProcessSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="da948-155">ProcessSchemaInfo</span></span></li>
<li><span data-ttu-id="da948-156">HelperReadLdapSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="da948-156">HelperReadLdapSchemaInfo</span></span></li>
<li><span data-ttu-id="da948-157">ProcessClassInfoArray</span><span class="sxs-lookup"><span data-stu-id="da948-157">ProcessClassInfoArray</span></span></li>
<li><span data-ttu-id="da948-158">ReadSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="da948-158">ReadSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="da948-159">StoreSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="da948-159">StoreSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="da948-160">AttributeTypeDescription</span><span class="sxs-lookup"><span data-stu-id="da948-160">AttributeTypeDescription</span></span></li>
<li><span data-ttu-id="da948-161">ObjectClassDescription</span><span class="sxs-lookup"><span data-stu-id="da948-161">ObjectClassDescription</span></span></li>
<li><span data-ttu-id="da948-162">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="da948-162">DITContentRuleDescription</span></span></li>
<li><span data-ttu-id="da948-163">DirectoryString</span><span class="sxs-lookup"><span data-stu-id="da948-163">DirectoryString</span></span></li>
<li><span data-ttu-id="da948-164">DirectoryStrings</span><span class="sxs-lookup"><span data-stu-id="da948-164">DirectoryStrings</span></span></li>
<li><span data-ttu-id="da948-165">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="da948-165">DITContentRuleDescription</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da948-166"><strong>DEBUG_CHANGEPWD</strong></span><span class="sxs-lookup"><span data-stu-id="da948-166"><strong>DEBUG_CHANGEPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="da948-167">CADsUser::ChangePassword</span><span class="sxs-lookup"><span data-stu-id="da948-167">CADsUser::ChangePassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="da948-168"><strong>DEBUG_SETPWD</strong></span><span class="sxs-lookup"><span data-stu-id="da948-168"><strong>DEBUG_SETPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="da948-169">CADsUser::SetPassword</span><span class="sxs-lookup"><span data-stu-id="da948-169">CADsUser::SetPassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="da948-170"><strong>DEBUG_BINDCACHE</strong></span><span class="sxs-lookup"><span data-stu-id="da948-170"><strong>DEBUG_BINDCACHE</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="da948-171">GetServerBasedObject</span><span class="sxs-lookup"><span data-stu-id="da948-171">GetServerBasedObject</span></span></li>
<li><span data-ttu-id="da948-172">GetServerLessBasedObject</span><span class="sxs-lookup"><span data-stu-id="da948-172">GetServerLessBasedObject</span></span></li>
<li><span data-ttu-id="da948-173">GetGCDomainName</span><span class="sxs-lookup"><span data-stu-id="da948-173">GetGCDomainName</span></span></li>
<li><span data-ttu-id="da948-174">GetDefaultDomainName</span><span class="sxs-lookup"><span data-stu-id="da948-174">GetDefaultDomainName</span></span></li>
<li><span data-ttu-id="da948-175">GetUserDomainFlatName</span><span class="sxs-lookup"><span data-stu-id="da948-175">GetUserDomainFlatName</span></span></li>
<li><span data-ttu-id="da948-176">BindCacheLookup</span><span class="sxs-lookup"><span data-stu-id="da948-176">BindCacheLookup</span></span></li>
<li><span data-ttu-id="da948-177">EquivalentPortNumbers</span><span class="sxs-lookup"><span data-stu-id="da948-177">EquivalentPortNumbers</span></span></li>
<li><span data-ttu-id="da948-178">CanCredentialsBeReused</span><span class="sxs-lookup"><span data-stu-id="da948-178">CanCredentialsBeReused</span></span></li>
<li><span data-ttu-id="da948-179">BindCacheAdd</span><span class="sxs-lookup"><span data-stu-id="da948-179">BindCacheAdd</span></span></li>
<li><span data-ttu-id="da948-180">BindCacheAddRef</span><span class="sxs-lookup"><span data-stu-id="da948-180">BindCacheAddRef</span></span></li>
<li><span data-ttu-id="da948-181">AddReferralLink</span><span class="sxs-lookup"><span data-stu-id="da948-181">AddReferralLink</span></span></li>
<li><span data-ttu-id="da948-182">CommonRemoveEntry</span><span class="sxs-lookup"><span data-stu-id="da948-182">CommonRemoveEntry</span></span></li>
<li><span data-ttu-id="da948-183">BindCacheDerefHelper</span><span class="sxs-lookup"><span data-stu-id="da948-183">BindCacheDerefHelper</span></span></li>
<li><span data-ttu-id="da948-184">NotifyNewConnection</span><span class="sxs-lookup"><span data-stu-id="da948-184">NotifyNewConnection</span></span></li>
<li><span data-ttu-id="da948-185">QueryForConnection</span><span class="sxs-lookup"><span data-stu-id="da948-185">QueryForConnection</span></span></li>
<li><span data-ttu-id="da948-186">LdapOpenBindWithCredentials</span><span class="sxs-lookup"><span data-stu-id="da948-186">LdapOpenBindWithCredentials</span></span></li>
<li><span data-ttu-id="da948-187">LdapOpenBindWithDefaultCredentials</span><span class="sxs-lookup"><span data-stu-id="da948-187">LdapOpenBindWithDefaultCredentials</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="da948-188">Puede combinar marcas combinando los bits adecuados en el *argumento traceFlags.*</span><span class="sxs-lookup"><span data-stu-id="da948-188">You can combine flags by combining the appropriate bits in the *traceFlags* argument.</span></span> <span data-ttu-id="da948-189">Por ejemplo, para especificar las marcas **DEBUG \_ SCHEMA** y **DEBUG \_ BINDCACHE,** el valor *traceFlags* adecuado sería 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="da948-189">For example, to specify the **DEBUG\_SCHEMA** and **DEBUG\_BINDCACHE** flags, the appropriate *traceFlags* value would be 0x00000009.</span></span>

<span data-ttu-id="da948-190">Por último, *la marca traceLevel* debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="da948-190">Finally, the *traceLevel* flag should be one of the following values:</span></span>



|      <span data-ttu-id="da948-191">Marca</span><span class="sxs-lookup"><span data-stu-id="da948-191">Flag</span></span>                                    |       <span data-ttu-id="da948-192">Value</span><span class="sxs-lookup"><span data-stu-id="da948-192">Value</span></span>                |
|------------------------------------------|-----------------------|
| <span data-ttu-id="da948-193">**ERROR \_ DE NIVEL DE \_ SEGUIMIENTO**</span><span class="sxs-lookup"><span data-stu-id="da948-193">**TRACE\_LEVEL\_ERROR**</span></span><br/>       | <span data-ttu-id="da948-194">0x00000002</span><span class="sxs-lookup"><span data-stu-id="da948-194">0x00000002</span></span><br/> |
| <span data-ttu-id="da948-195">**INFORMACIÓN DE \_ NIVEL \_ DE SEGUIMIENTO**</span><span class="sxs-lookup"><span data-stu-id="da948-195">**TRACE\_LEVEL\_INFORMATION**</span></span><br/> | <span data-ttu-id="da948-196">0x00000004</span><span class="sxs-lookup"><span data-stu-id="da948-196">0x00000004</span></span><br/> |



 

<span data-ttu-id="da948-197">**TRACE \_ LEVEL \_ INFORMATION hace** que el proceso de seguimiento registre todos los eventos, mientras que TRACE LEVEL **\_ \_ ERROR** hace que el proceso de seguimiento solo registre eventos de error.</span><span class="sxs-lookup"><span data-stu-id="da948-197">**TRACE\_LEVEL\_INFORMATION** causes the tracing process to record all events, whereas **TRACE\_LEVEL\_ERROR** causes the tracing process to record only error events.</span></span>

<span data-ttu-id="da948-198">Para finalizar el seguimiento, ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="da948-198">To terminate tracing, run the following command:</span></span>

<span data-ttu-id="da948-199">**tracelog.exe -stop** *sessionname*</span><span class="sxs-lookup"><span data-stu-id="da948-199">**tracelog.exe -stop** *sessionname*</span></span>

<span data-ttu-id="da948-200">En el ejemplo anterior, *sessionname* es el mismo nombre que el que se proporcionó con el comando que inició la sección de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="da948-200">In the previous example, *sessionname* is the same name as the one that was provided with the command that started the tracing section.</span></span>

## <a name="remarks"></a><span data-ttu-id="da948-201">Comentarios</span><span class="sxs-lookup"><span data-stu-id="da948-201">Remarks</span></span>

<span data-ttu-id="da948-202">Es más eficaz hacer un seguimiento solo de procesos específicos especificando un PID determinado que hacer un seguimiento de todos los procesos de un equipo.</span><span class="sxs-lookup"><span data-stu-id="da948-202">It is more effective to trace only specific processes by specifying a particular PID than to trace all processes on a computer.</span></span> <span data-ttu-id="da948-203">Si necesita realizar un seguimiento de varias aplicaciones en la misma máquina, puede haber un impacto en el rendimiento. hay una salida de depuración considerable en las secciones orientadas al rendimiento del código.</span><span class="sxs-lookup"><span data-stu-id="da948-203">If you do need to trace multiple applications on the same machine, there might be a performance impact; there is substantial debugging output in performance-oriented sections of the code.</span></span> <span data-ttu-id="da948-204">Además, los administradores deben tener cuidado de establecer correctamente los permisos de los archivos de registro al realizar el seguimiento de varios procesos. De lo contrario, cualquier usuario podría leer los registros de seguimiento y otros usuarios podrán realizar un seguimiento de los procesos que contienen información segura.</span><span class="sxs-lookup"><span data-stu-id="da948-204">Also, administrators must be careful to properly set the permissions of the log files when tracing multiple processes; otherwise, any user might be able to read the tracing logs, and other users will be able to trace processes that contain secure information.</span></span>

<span data-ttu-id="da948-205">Por ejemplo, supone que el administrador configura el seguimiento de una aplicación "Test.exe" y no especifica un PID en el Registro para realizar un seguimiento de varias instancias del proceso.</span><span class="sxs-lookup"><span data-stu-id="da948-205">For example, presume the administrator sets up tracing for an application "Test.exe", and does not specify a PID in the registry to trace multiple instances of the process.</span></span> <span data-ttu-id="da948-206">Ahora, otro usuario quiere hacer un seguimiento de la aplicación "Secure.exe".</span><span class="sxs-lookup"><span data-stu-id="da948-206">Now another user wants to trace the application "Secure.exe".</span></span> <span data-ttu-id="da948-207">Si los archivos de registro de seguimiento no están restringidos correctamente, lo único que debe hacer el usuario es cambiar el nombre de "Secure.exe" a "Test.exe" y se realizará el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="da948-207">If the tracing log files are not properly restricted, all that user needs to do is rename "Secure.exe" to "Test.exe", and it will be traced.</span></span> <span data-ttu-id="da948-208">En general, es mejor realizar un seguimiento solo de procesos específicos durante la solución de problemas y quitar la clave del Registro de seguimiento en cuanto se realiza la solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="da948-208">In general, it is best to trace only specific processes while troubleshooting, and to remove the tracing registry key as soon as troubleshooting is done.</span></span>

<span data-ttu-id="da948-209">Puesto que la habilitación del seguimiento de eventos producirá archivos de registro adicionales, los administradores deben supervisar cuidadosamente los tamaños de los archivos de registro. la falta de espacio en disco en el equipo local puede provocar una denegación de servicio.</span><span class="sxs-lookup"><span data-stu-id="da948-209">Since enabling Event Tracing will produce extra log files, administrators should carefully monitor log file sizes; lack of disk space on the local computer can cause a denial-of-service.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="da948-210">Escenarios de ejemplo</span><span class="sxs-lookup"><span data-stu-id="da948-210">Example Scenarios</span></span>

<span data-ttu-id="da948-211">Escenario 1: el administrador ve un error inesperado en una aplicación que establece contraseñas para las cuentas de usuario, por lo que realizaría los pasos siguientes para corregir el problema mediante el seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="da948-211">Scenario 1: The administrator sees an unexpected error in an application that sets passwords for user accounts, so they would take the following steps to fix the problem using Event Tracing.</span></span>

1.  <span data-ttu-id="da948-212">Escribir un script que reproduzca el problema y crear la clave del Registro</span><span class="sxs-lookup"><span data-stu-id="da948-212">Write a script that reproduces the problem, and create the registry key</span></span>

    <span data-ttu-id="da948-213">**HKEY \_ Sistema \_ DE MÁQUINA LOCAL** \\  \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **cscript.exe**</span><span class="sxs-lookup"><span data-stu-id="da948-213">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

2.  <span data-ttu-id="da948-214">Inicie una sesión de seguimiento, estableciendo *traceFlags* en 0x2 (**DEBUG \_ CHANGEPASSWD**) y *traceLevel* en 0x4 (**TRACE LEVEL \_ \_ INFORMATION**), mediante el comando siguiente:</span><span class="sxs-lookup"><span data-stu-id="da948-214">Start a tracing session, setting *traceFlags* to 0x2 (**DEBUG\_CHANGEPASSWD**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**), using the following command:</span></span>

    <span data-ttu-id="da948-215">**tracelog.exe -start scripttrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ adsi.etl -flag 0x2 -level 0x4**</span><span class="sxs-lookup"><span data-stu-id="da948-215">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

3.  <span data-ttu-id="da948-216">Ejecute cscript.exe con su script de prueba para reproducir el problema y, a continuación, finalice la sesión de seguimiento:</span><span class="sxs-lookup"><span data-stu-id="da948-216">Run cscript.exe with their test script to reproduce the problem, and then terminate the tracing session:</span></span>

    <span data-ttu-id="da948-217">**tracelog.exe -stop scripttrace**</span><span class="sxs-lookup"><span data-stu-id="da948-217">**tracelog.exe -stop scripttrace**</span></span>

4.  <span data-ttu-id="da948-218">Eliminación de la clave del Registro</span><span class="sxs-lookup"><span data-stu-id="da948-218">Delete the registry key</span></span>

    <span data-ttu-id="da948-219">**HKEY \_ Sistema \_ DE MÁQUINA LOCAL** \\  \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **cscript.exe**</span><span class="sxs-lookup"><span data-stu-id="da948-219">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

5.  <span data-ttu-id="da948-220">Ejecute la herramienta ETW Tracerpt.exe analizar la información de seguimiento del registro:</span><span class="sxs-lookup"><span data-stu-id="da948-220">Run the ETW tool Tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="da948-221">**tracelog.exe -start scripttrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ adsi.etl -flag 0x2 -level 0x4**</span><span class="sxs-lookup"><span data-stu-id="da948-221">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

<span data-ttu-id="da948-222">Escenario 2: el administrador desea realizar un seguimiento de las operaciones de análisis y descarga de esquemas en una aplicación [ASP](https://msdn.microsoft.com/asp.net/default.aspx) denominada w3wp.exe que ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="da948-222">Scenario 2: The administrator wants to trace the schema parsing and download operations in an [ASP](https://msdn.microsoft.com/asp.net/default.aspx) application named w3wp.exe that is already running.</span></span> <span data-ttu-id="da948-223">Para ello, el administrador realizaría los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="da948-223">To do this, the administrator would take the following steps:</span></span>

1.  <span data-ttu-id="da948-224">Creación de la clave del Registro</span><span class="sxs-lookup"><span data-stu-id="da948-224">Create the registry key</span></span>

    <span data-ttu-id="da948-225">**HKEY \_ Sistema \_ LOCAL MACHINE** \\  \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **w3wp.exe**</span><span class="sxs-lookup"><span data-stu-id="da948-225">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**</span></span>

    <span data-ttu-id="da948-226">y dentro de esa clave, cree un valor de tipo DWORD denominado PID y estadúzcalo en el identificador de proceso de la instancia de w3wp.exe que se ejecuta actualmente en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="da948-226">and inside that key, create a value of type DWORD that is named PID and set it to the process ID of the instance of w3wp.exe that is currently running on the local computer.</span></span>

2.  <span data-ttu-id="da948-227">A continuación, crean una sesión de seguimiento, estableciendo *traceFlags* en 0x1 (**DEBUG \_ SCHEMA**) y *traceLevel* en 0x4 (**TRACE LEVEL \_ \_ INFORMATION**):</span><span class="sxs-lookup"><span data-stu-id="da948-227">Then they create a tracing session, setting *traceFlags* to 0x1 (**DEBUG\_SCHEMA**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**):</span></span>

    <span data-ttu-id="da948-228">**tracelog.exe -start w3wptrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ w3wp.etl -flag 0x1 -level 0x4**</span><span class="sxs-lookup"><span data-stu-id="da948-228">**tracelog.exe -start w3wptrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\w3wp.etl -flag 0x1 -level 0x4**</span></span>

3.  <span data-ttu-id="da948-229">Reproduzca la operación que necesita solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="da948-229">Reproduce the operation that needs troubleshooting.</span></span>
4.  <span data-ttu-id="da948-230">Finalice la sesión de seguimiento:</span><span class="sxs-lookup"><span data-stu-id="da948-230">Terminate the tracing session:</span></span>

    <span data-ttu-id="da948-231">**tracelog.exe -stop w3wptrace**</span><span class="sxs-lookup"><span data-stu-id="da948-231">**tracelog.exe -stop w3wptrace**</span></span>

5.  <span data-ttu-id="da948-232">Elimine la clave del Registro **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **w3wp.exe**.</span><span class="sxs-lookup"><span data-stu-id="da948-232">Delete the registry key **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**.</span></span>
6.  <span data-ttu-id="da948-233">Ejecute la herramienta ETW tracerpt.exe analizar la información de seguimiento del registro:</span><span class="sxs-lookup"><span data-stu-id="da948-233">Run the ETW tool tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="da948-234">**tracerpt.exe . \\ w3wp.etl -o -report**</span><span class="sxs-lookup"><span data-stu-id="da948-234">**tracerpt.exe .\\w3wp.etl -o -report**</span></span>

 

