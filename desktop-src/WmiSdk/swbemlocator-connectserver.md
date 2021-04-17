---
description: Se conecta al espacio de nombres en el equipo especificado en el parámetro strServer.
ms.assetid: 31364c68-b031-4cf0-851f-b4e302f077e0
ms.tgt_platform: multiple
title: Método SWbemLocator. ConnectServer (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 31c2e6de8cf1504543727cad056a3616a51182d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697684"
---
# <a name="swbemlocatorconnectserver-method"></a><span data-ttu-id="d4865-103">SWbemLocator. ConnectServer, método</span><span class="sxs-lookup"><span data-stu-id="d4865-103">SWbemLocator.ConnectServer method</span></span>

<span data-ttu-id="d4865-104">El método **ConnectServer** del objeto [**SWbemLocator**](swbemlocator.md) se conecta al espacio de nombres en el equipo especificado en el parámetro *strServer* .</span><span class="sxs-lookup"><span data-stu-id="d4865-104">The **ConnectServer** method of the [**SWbemLocator**](swbemlocator.md) object connects to the namespace on the computer that is specified in the *strServer* parameter.</span></span> <span data-ttu-id="d4865-105">El equipo de destino puede ser local o remoto, pero debe tener WMI instalado.</span><span class="sxs-lookup"><span data-stu-id="d4865-105">The target computer can be either local or remote, but it must have WMI installed.</span></span> <span data-ttu-id="d4865-106">Para obtener ejemplos y una comparación con el tipo de moniker de conexión, vea [crear un script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="d4865-106">For examples and a comparison with the moniker type of connection, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span>

<span data-ttu-id="d4865-107">A partir de Windows Vista, **SWbemLocator. ConnectServer** puede conectarse con equipos que ejecutan IPv6 mediante una dirección IPv6 en el parámetro *strServer* .</span><span class="sxs-lookup"><span data-stu-id="d4865-107">Starting with Windows Vista, **SWbemLocator.ConnectServer** can connect with computers running IPv6 using an IPv6 address in the *strServer* parameter.</span></span> <span data-ttu-id="d4865-108">Para obtener más información, consulte [compatibilidad con IPv6 e IPv4 en WMI](ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="d4865-108">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="d4865-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d4865-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d4865-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4865-110">Syntax</span></span>


```VB
objwbemServices = .ConnectServer( _
  [ ByVal strServer ], _
  [ ByVal strNamespace ], _
  [ ByVal strUser ], _
  [ ByVal strPassword ], _
  [ ByVal strLocale ], _
  [ ByVal strAuthority ], _
  [ ByVal iSecurityFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d4865-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4865-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4865-112">*strServer* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d4865-112">*strServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4865-113">Nombre del equipo al que se está conectando.</span><span class="sxs-lookup"><span data-stu-id="d4865-113">Computer name to which you are connecting.</span></span> <span data-ttu-id="d4865-114">Si el equipo remoto está en un dominio diferente al de la cuenta de usuario en la que inicia sesión, use el nombre de equipo completo.</span><span class="sxs-lookup"><span data-stu-id="d4865-114">If the remote computer is in a different domain than the user account under which you log in, then use the fully qualified computer name.</span></span> <span data-ttu-id="d4865-115">Si no proporciona este parámetro, la llamada tiene como valor predeterminado el equipo local.</span><span class="sxs-lookup"><span data-stu-id="d4865-115">If you do not provide this parameter, the call defaults to the local computer.</span></span>

<span data-ttu-id="d4865-116">Ejemplo: `server1.network.fabrikam`</span><span class="sxs-lookup"><span data-stu-id="d4865-116">Example: `server1.network.fabrikam`</span></span>

<span data-ttu-id="d4865-117">También puede usar una dirección IP en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="d4865-117">You also can use an IP address in this parameter.</span></span> <span data-ttu-id="d4865-118">Si la dirección IP está en formato IPv6, el equipo de destino debe ejecutar IPv6.</span><span class="sxs-lookup"><span data-stu-id="d4865-118">If the IP address is in IPv6 format, the target computer must be running IPv6.</span></span> <span data-ttu-id="d4865-119">Una dirección en IPv4 tiene el siguiente aspecto `123.123.123.123`</span><span class="sxs-lookup"><span data-stu-id="d4865-119">An address in IPv4 looks like `123.123.123.123`</span></span>

<span data-ttu-id="d4865-120">Una dirección IP en formato IPv6 tiene el siguiente aspecto `2010:836B:4179::836B:4179`</span><span class="sxs-lookup"><span data-stu-id="d4865-120">An IP address in IPv6 format looks like `2010:836B:4179::836B:4179`</span></span>

<span data-ttu-id="d4865-121">Para obtener más información sobre DNS e IPv4, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="d4865-121">For more information on DNS and IPv4, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="d4865-122">*strNamespace* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d4865-122">*strNamespace* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4865-123">Cadena que especifica el espacio de nombres en el que se inicia la sesión.</span><span class="sxs-lookup"><span data-stu-id="d4865-123">String that specifies the namespace to which you log on.</span></span> <span data-ttu-id="d4865-124">Por ejemplo, para iniciar sesión en el \\ espacio de nombres predeterminado raíz, use la raíz \\ predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d4865-124">For example, to log on to the root\\default namespace, use root\\default.</span></span> <span data-ttu-id="d4865-125">Si no se especifica este parámetro, el valor predeterminado es el espacio de nombres configurado como espacio de nombres predeterminado para el scripting.</span><span class="sxs-lookup"><span data-stu-id="d4865-125">If you do not specify this parameter, it defaults to the namespace that is configured as the default namespace for scripting.</span></span> <span data-ttu-id="d4865-126">Para obtener más información, vea [crear una aplicación o un script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="d4865-126">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

<span data-ttu-id="d4865-127">Ejemplo: "root \\ cimv2"</span><span class="sxs-lookup"><span data-stu-id="d4865-127">Example: "root\\CIMV2"</span></span>

</dd> <dt>

<span data-ttu-id="d4865-128">*strUser* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d4865-128">*strUser* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4865-129">Nombre de usuario que se va a usar para conectarse.</span><span class="sxs-lookup"><span data-stu-id="d4865-129">User name to use to connect.</span></span> <span data-ttu-id="d4865-130">La cadena puede tener la forma de un nombre de usuario o un nombre de usuario de dominio \\ .</span><span class="sxs-lookup"><span data-stu-id="d4865-130">The string can be in the form of either a user name or a Domain\\Username.</span></span> <span data-ttu-id="d4865-131">Deje este parámetro en blanco para utilizar el contexto de seguridad actual.</span><span class="sxs-lookup"><span data-stu-id="d4865-131">Leave this parameter blank to use the current security context.</span></span> <span data-ttu-id="d4865-132">El parámetro *strUser* solo debe usarse con conexiones a servidores WMI remotos.</span><span class="sxs-lookup"><span data-stu-id="d4865-132">The *strUser* parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="d4865-133">Si intenta especificar *strUser* para una conexión WMI local, se producirá un error en el intento de conexión.</span><span class="sxs-lookup"><span data-stu-id="d4865-133">If you attempt to specify *strUser* for a local WMI connection, the connection attempt fails.</span></span> <span data-ttu-id="d4865-134">Si la autenticación Kerberos está en uso, el nombre de usuario y la contraseña que se especifican en *strUser* y *strPassword* no se pueden interceptar en una red.</span><span class="sxs-lookup"><span data-stu-id="d4865-134">If Kerberos authentication is in use, then the username and password that is specified in *strUser* and *strPassword* cannot be intercepted on a network.</span></span> <span data-ttu-id="d4865-135">Puede usar el formato UPN para especificar *strUser*.</span><span class="sxs-lookup"><span data-stu-id="d4865-135">You can use the UPN format to specify the *strUser*.</span></span>

<span data-ttu-id="d4865-136">Ejemplo: "nombreDeDominio \\ nombreDeUsuario"</span><span class="sxs-lookup"><span data-stu-id="d4865-136">Example: "DomainName\\UserName"</span></span>

> [!Note]  
> <span data-ttu-id="d4865-137">Si se especifica un dominio en *strAuthority*, el dominio no debe especificarse aquí.</span><span class="sxs-lookup"><span data-stu-id="d4865-137">If a domain is specified in *strAuthority*, then the domain must not be specified here.</span></span> <span data-ttu-id="d4865-138">Si se especifica el dominio en ambos parámetros, se producirá un error de parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="d4865-138">Specifying the domain in both parameters results in an Invalid Parameter error.</span></span>

 

</dd> <dt>

<span data-ttu-id="d4865-139">*strPassword* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d4865-139">*strPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4865-140">Cadena que especifica la contraseña que se va a usar al intentar conectarse.</span><span class="sxs-lookup"><span data-stu-id="d4865-140">String that specifies the password to use when attempting to connect.</span></span> <span data-ttu-id="d4865-141">Deje el parámetro en blanco para utilizar el contexto de seguridad actual.</span><span class="sxs-lookup"><span data-stu-id="d4865-141">Leave the parameter blank to use the current security context.</span></span> <span data-ttu-id="d4865-142">El parámetro *strPassword* solo debe usarse con conexiones a servidores WMI remotos.</span><span class="sxs-lookup"><span data-stu-id="d4865-142">The *strPassword* parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="d4865-143">Si intenta especificar *strPassword* para una conexión WMI local, se producirá un error en el intento de conexión.</span><span class="sxs-lookup"><span data-stu-id="d4865-143">If you attempt to specify *strPassword* for a local WMI connection, the connection attempt fails.</span></span> <span data-ttu-id="d4865-144">Si se usa la autenticación Kerberos, el nombre de usuario y la contraseña que se especifican en *strUser* y *strPassword* no se pueden interceptar en la red.</span><span class="sxs-lookup"><span data-stu-id="d4865-144">If Kerberos authentication is in use then the username and password that is specified in *strUser* and *strPassword* cannot be intercepted on the network.</span></span>

</dd> <dt>

<span data-ttu-id="d4865-145">*strLocale* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d4865-145">*strLocale* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4865-146">Cadena que especifica el código de localización.</span><span class="sxs-lookup"><span data-stu-id="d4865-146">String that specifies the localization code.</span></span> <span data-ttu-id="d4865-147">Si desea usar la configuración regional actual, déjela en blanco.</span><span class="sxs-lookup"><span data-stu-id="d4865-147">If you want to use the current locale, leave it blank.</span></span> <span data-ttu-id="d4865-148">Si no está en blanco, este parámetro debe ser una cadena que indica la configuración regional deseada en la que se debe recuperar la información.</span><span class="sxs-lookup"><span data-stu-id="d4865-148">If not blank, this parameter must be a string that indicates the desired locale where information must be retrieved.</span></span> <span data-ttu-id="d4865-149">En el caso de los identificadores de configuración regional de Microsoft, el formato de la cadena es "MS \_ xxxx", donde XXXX es una cadena en formato hexadecimal que indica el LCID.</span><span class="sxs-lookup"><span data-stu-id="d4865-149">For Microsoft locale identifiers, the format of the string is "MS\_xxxx", where xxxx is a string in the hexadecimal form that indicates the LCID.</span></span> <span data-ttu-id="d4865-150">Por ejemplo, el inglés americano aparecería como "MS \_ 409".</span><span class="sxs-lookup"><span data-stu-id="d4865-150">For example, American English would appear as "MS\_409".</span></span>

</dd> <dt>

<span data-ttu-id="d4865-151">*strAuthority* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d4865-151">*strAuthority* \[in, optional\]</span></span>
</dt> <dd>

<dt>

<span data-ttu-id="d4865-152">""</span><span class="sxs-lookup"><span data-stu-id="d4865-152">""</span></span>
</dt> <dd>

<span data-ttu-id="d4865-153">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="d4865-153">This parameter is optional.</span></span> <span data-ttu-id="d4865-154">Sin embargo, si se especifica, solo se puede usar Kerberos o NTLMDomain.</span><span class="sxs-lookup"><span data-stu-id="d4865-154">However, if it is specified, only Kerberos or NTLMDomain can be used.</span></span>

</dd> <dt>

<span data-ttu-id="d4865-155">V5</span><span class="sxs-lookup"><span data-stu-id="d4865-155">Kerberos:</span></span>
</dt> <dd>

<span data-ttu-id="d4865-156">Si el parámetro *strAuthority* comienza con la cadena "Kerberos:", se usa la autenticación Kerberos y este parámetro debe contener un nombre de entidad de seguridad Kerberos.</span><span class="sxs-lookup"><span data-stu-id="d4865-156">If the *strAuthority* parameter begins with the string "Kerberos:", then Kerberos authentication is used and this parameter should contain a Kerberos principal name.</span></span> <span data-ttu-id="d4865-157">El nombre de la entidad de seguridad de Kerberos se especifica como Kerberos:*dominio*, por ejemplo, `Kerberos:fabrikam` donde `fabrikam` es el servidor al que está intentando conectarse.</span><span class="sxs-lookup"><span data-stu-id="d4865-157">The Kerberos principal name is specified as Kerberos:*domain*, such as `Kerberos:fabrikam` where `fabrikam` is the server to which you are attempting to connect.</span></span>

<span data-ttu-id="d4865-158">Ejemplo: "Kerberos: dominio"</span><span class="sxs-lookup"><span data-stu-id="d4865-158">Example: "Kerberos:DOMAIN"</span></span>

</dd> <dt>

<span data-ttu-id="d4865-159">NTLMDomain</span><span class="sxs-lookup"><span data-stu-id="d4865-159">NTLMDomain:</span></span>
</dt> <dd>

<span data-ttu-id="d4865-160">Para usar la autenticación de NT LAN Manager (NTLM), debe especificarla como NTLMDomain:*Domain*, como, por ejemplo, `NTLMDomain:fabrikam` donde `fabrikam` es el nombre del dominio.</span><span class="sxs-lookup"><span data-stu-id="d4865-160">To use NT Lan Manager (NTLM) authentication, you must specify it as NTLMDomain:*domain*, such as `NTLMDomain:fabrikam` where `fabrikam` is the name of the domain.</span></span>

<span data-ttu-id="d4865-161">Ejemplo: "NTLMDomain: dominio"</span><span class="sxs-lookup"><span data-stu-id="d4865-161">Example: "NTLMDomain:DOMAIN"</span></span>

</dd> </dl>

<span data-ttu-id="d4865-162">Si deja este parámetro en blanco, el sistema operativo negocia con COM para determinar si se utiliza la autenticación NTLM o Kerberos.</span><span class="sxs-lookup"><span data-stu-id="d4865-162">If you leave this parameter blank, the operating system negotiates with COM to determine whether NTLM or Kerberos authentication is used.</span></span> <span data-ttu-id="d4865-163">Este parámetro solo debe usarse con conexiones a servidores WMI remotos.</span><span class="sxs-lookup"><span data-stu-id="d4865-163">This parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="d4865-164">Si intenta establecer la autoridad para una conexión WMI local, se producirá un error en el intento de conexión.</span><span class="sxs-lookup"><span data-stu-id="d4865-164">If you attempt to set the authority for a local WMI connection, the connection attempt fails.</span></span>

> [!Note]  
> <span data-ttu-id="d4865-165">Si el dominio se especifica en *strUser*, que es la ubicación preferida, no debe especificarse aquí.</span><span class="sxs-lookup"><span data-stu-id="d4865-165">If the domain is specified in *strUser*, which is the preferred location, then it must not be specified here.</span></span> <span data-ttu-id="d4865-166">Si se especifica el dominio en ambos parámetros, se producirá un error de parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="d4865-166">Specifying the domain in both parameters results in an Invalid Parameter error.</span></span>

 

</dd> <dt>

<span data-ttu-id="d4865-167">*iSecurityFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d4865-167">*iSecurityFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4865-168">Se usa para pasar valores de marca a **ConnectServer**.</span><span class="sxs-lookup"><span data-stu-id="d4865-168">Used to pass flag values to **ConnectServer**.</span></span>

<dt>

<span data-ttu-id="d4865-169">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="d4865-169">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="d4865-170">Un valor de 0 para este parámetro hace que la llamada a **ConnectServer** se devuelva solo después de que se establezca la conexión al servidor.</span><span class="sxs-lookup"><span data-stu-id="d4865-170">A value of 0 for this parameter causes the call to **ConnectServer** to return only after the connection to the server is established.</span></span> <span data-ttu-id="d4865-171">Esto podría hacer que el programa dejara de responder indefinidamente si no se puede establecer la conexión.</span><span class="sxs-lookup"><span data-stu-id="d4865-171">This could cause your program to stop responding indefinitely if the connection cannot be established.</span></span>

</dd> <dt>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>

<span data-ttu-id="d4865-172"><span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>wbemConnectFlagUseMaxWait \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="d4865-172"><span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>\*\*\*\*wbemConnectFlagUseMaxWait\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="d4865-173">Se garantiza que la llamada a **ConnectServer** se devuelve en 2 minutos o menos.</span><span class="sxs-lookup"><span data-stu-id="d4865-173">The **ConnectServer** call is guaranteed to return in 2 minutes or less.</span></span> <span data-ttu-id="d4865-174">Utilice esta marca para evitar que el programa deje de responder indefinidamente si no se puede establecer la conexión.</span><span class="sxs-lookup"><span data-stu-id="d4865-174">Use this flag to prevent your program from ceasing to respond indefinitely if the connection cannot be established.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d4865-175">*objwbemNamedValueSet* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d4865-175">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4865-176">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="d4865-176">Typically, this is undefined.</span></span> <span data-ttu-id="d4865-177">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d4865-177">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="d4865-178">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="d4865-178">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4865-179">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4865-179">Return value</span></span>

<span data-ttu-id="d4865-180">Si es correcto, WMI devuelve un objeto [**SWbemServices**](swbemservices.md) que está enlazado al espacio de nombres especificado en *strNamespace* en el equipo que se especifica en *strServer*.</span><span class="sxs-lookup"><span data-stu-id="d4865-180">If successful, WMI returns an [**SWbemServices**](swbemservices.md) object that is bound to the namespace that is specified in *strNamespace* on the computer that is specified in *strServer*.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d4865-181">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d4865-181">Error codes</span></span>

<span data-ttu-id="d4865-182">Después de completar el método **ConnectServer** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="d4865-182">After the completion of the **ConnectServer** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d4865-183">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="d4865-183">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="d4865-184">El nombre de usuario y la contraseña actuales o especificados no son válidos o están autorizados para realizar la conexión.</span><span class="sxs-lookup"><span data-stu-id="d4865-184">The current or specified user name and password were not valid or authorized to make the connection.</span></span>

</dd> <dt>

<span data-ttu-id="d4865-185">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d4865-185">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d4865-186">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="d4865-186">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d4865-187">**wbemErrInvalidNamespace** -2147749902 (0x8004100E)</span><span class="sxs-lookup"><span data-stu-id="d4865-187">**wbemErrInvalidNamespace** - 2147749902 (0x8004100E)</span></span>
</dt> <dd>

<span data-ttu-id="d4865-188">El espacio de nombres especificado no existía en el servidor.</span><span class="sxs-lookup"><span data-stu-id="d4865-188">The specified namespace did not exist on the server.</span></span>

</dd> <dt>

<span data-ttu-id="d4865-189">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d4865-189">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d4865-190">Se especificó un parámetro no válido o no se pudo analizar el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="d4865-190">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="d4865-191">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d4865-191">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d4865-192">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="d4865-192">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d4865-193">**wbemErrTransportFailure** -2147749909</span><span class="sxs-lookup"><span data-stu-id="d4865-193">**wbemErrTransportFailure** - 2147749909</span></span>
</dt> <dd>

<span data-ttu-id="d4865-194">Se produjo un error de red que impide el funcionamiento normal.</span><span class="sxs-lookup"><span data-stu-id="d4865-194">A networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4865-195">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4865-195">Remarks</span></span>

<span data-ttu-id="d4865-196">El método **ConnectServer** se usa a menudo al conectarse a una cuenta con un nombre de usuario y unas credenciales de contraseña diferentes en un equipo remoto, ya que no se puede especificar una contraseña diferente en una cadena de [moniker](constructing-a-moniker-string.md) .</span><span class="sxs-lookup"><span data-stu-id="d4865-196">The **ConnectServer** method is often used when connecting to an account with a different username and password credentials on a remote computer because you cannot specify a different password in a [moniker](constructing-a-moniker-string.md) string.</span></span> <span data-ttu-id="d4865-197">Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).</span><span class="sxs-lookup"><span data-stu-id="d4865-197">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="d4865-198">El uso de una dirección IPv4 para conectarse a un servidor remoto puede producir un comportamiento inesperado.</span><span class="sxs-lookup"><span data-stu-id="d4865-198">Using an IPv4 address to connect to a remote server may result in unexpected behavior.</span></span> <span data-ttu-id="d4865-199">La causa probable es que las entradas DNS estén obsoletas en su entorno.</span><span class="sxs-lookup"><span data-stu-id="d4865-199">The likely cause is stale DNS entries in your environment.</span></span> <span data-ttu-id="d4865-200">En estas circunstancias, se usará la entrada PTR obsoleta para el equipo, con resultados imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="d4865-200">In these circumstances, the stale PTR entry for the machine will be used, with unpredictable results.</span></span> <span data-ttu-id="d4865-201">Para evitar este comportamiento, puede anexar un punto (".") a la dirección IP antes de llamar a ConnectServer.</span><span class="sxs-lookup"><span data-stu-id="d4865-201">To avoid this behavior, you can append a period (".") to the IP address before calling ConnectServer.</span></span> <span data-ttu-id="d4865-202">Esto hace que se produzca un error en la búsqueda inversa de DNS, pero puede permitir que la llamada **ConnectServer** se realice correctamente en el equipo correcto.</span><span class="sxs-lookup"><span data-stu-id="d4865-202">This causes the reverse DNS lookup to fail, but may allow the **ConnectServer** call to succeed on the correct machine.</span></span>

## <a name="examples"></a><span data-ttu-id="d4865-203">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d4865-203">Examples</span></span>

<span data-ttu-id="d4865-204">En el siguiente ejemplo de código de VBScript se describe cómo conectarse a un equipo remoto para obtener datos de [**\_ IP4RouteTable de Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) .</span><span class="sxs-lookup"><span data-stu-id="d4865-204">The following VBScript code example describes how to connect to a remote computer to obtain [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) data.</span></span> <span data-ttu-id="d4865-205">El nombre de dominio que se especifica en *strDomain* se usa en *strAuthority*.</span><span class="sxs-lookup"><span data-stu-id="d4865-205">The domain name that is specified in *strDomain* is used in *strAuthority*.</span></span>


```VB
Const intMin = 3600
strComputer = "RemoteComputer" 
strDomain = "DomainName"  
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
Wscript.Echo

Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
                                                  "root\CIMV2", _ 
                                                  strUser, _ 
                                                  strPassword, _ 
                                                  "MS_409", _ 
                                                  "NTLMDomain:" + strDomain) 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_IP4RouteTable",,48) 
For Each objItem in colItems
    WScript.Echo "Age in Minutes: " & int(objItem.Age/intMin) & VBNewLine _
               & "Description:    " & objItem.Description & VBNewLine _
               & "Destination:    " & objItem.Destination & VBNewLine _
               & "InterfaceIndex: " & objItem.InterfaceIndex & VBNewLine _
               & "Mask:           " & objItem.Mask & VBNewLine _
               & "Metric1:        " & objItem.Metric1 & VBNewLine _
               & "Metric2:        " & objItem.Metric2 & VBNewLine _
               & "Metric3:        " & objItem.Metric3 & VBNewLine _
               & "Metric4:        " & objItem.Metric4 & VBNewLine _
               & "Metric5:        " & objItem.Metric5 & VBNewLine _
               & "Name:           " & objItem.Name & VBNewLine _
               & "NextHop:        " & objItem.NextHop & VBNewLine _
               & "Protocol:       " & objItem.Protocol & VBNewLine _
               & "Type: " & objItem.Type
    WScript.Echo
   </example>
Next
```



<span data-ttu-id="d4865-206">El siguiente fragmento de código de PowerShell accede a un servidor remoto y enumera las clases WMI disponibles.</span><span class="sxs-lookup"><span data-stu-id="d4865-206">The following PowerShell snippet access a remote server and lists the available WMI classes.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="d4865-207">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4865-207">Requirements</span></span>



| <span data-ttu-id="d4865-208">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4865-208">Requirement</span></span> | <span data-ttu-id="d4865-209">Value</span><span class="sxs-lookup"><span data-stu-id="d4865-209">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4865-210">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4865-210">Minimum supported client</span></span><br/> | <span data-ttu-id="d4865-211">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4865-211">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d4865-212">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4865-212">Minimum supported server</span></span><br/> | <span data-ttu-id="d4865-213">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4865-213">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d4865-214">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4865-214">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4865-215"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4865-215"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4865-216">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d4865-216">Type library</span></span><br/>             | <dl> <span data-ttu-id="d4865-217"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d4865-217"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d4865-218">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d4865-218">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4865-219"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4865-219"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d4865-220">CLSID</span><span class="sxs-lookup"><span data-stu-id="d4865-220">CLSID</span></span><br/>                    | <span data-ttu-id="d4865-221">CLSID \_ SWbemLocator</span><span class="sxs-lookup"><span data-stu-id="d4865-221">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="d4865-222">IID</span><span class="sxs-lookup"><span data-stu-id="d4865-222">IID</span></span><br/>                      | <span data-ttu-id="d4865-223">\_ISWBEMLOCATOR IID</span><span class="sxs-lookup"><span data-stu-id="d4865-223">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="d4865-224">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4865-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4865-225">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="d4865-225">**SWbemLocator**</span></span>](swbemlocator.md)
</dt> <dt>

[<span data-ttu-id="d4865-226">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="d4865-226">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="d4865-227">Conexión a WMI en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="d4865-227">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="d4865-228">Creación de un script de WMI</span><span class="sxs-lookup"><span data-stu-id="d4865-228">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> </dl>

 

