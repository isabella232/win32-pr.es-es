---
description: El formato de cadena de moniker es similar al de una ruta de acceso de objeto WMI estándar. Para obtener más información, vea requisitos de ruta de acceso de objeto WMI.
ms.assetid: 1aacc523-2a2f-43f5-96a3-aa0387cbae3e
ms.tgt_platform: multiple
title: Construir una cadena de moniker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e54e29b3c8f14890dc1cedd5907059308e8d22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360586"
---
# <a name="constructing-a-moniker-string"></a><span data-ttu-id="cbfb7-104">Construir una cadena de moniker</span><span class="sxs-lookup"><span data-stu-id="cbfb7-104">Constructing a Moniker String</span></span>

<span data-ttu-id="cbfb7-105">El formato de cadena de moniker es similar al de una ruta de acceso de objeto WMI estándar.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-105">The moniker string format is similar to that of a standard WMI object path.</span></span> <span data-ttu-id="cbfb7-106">Para obtener más información, vea [requisitos de ruta de acceso de objeto WMI](wmi-object-path-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cbfb7-106">For more information, see [WMI Object Path Requirements](wmi-object-path-requirements.md).</span></span>

<span data-ttu-id="cbfb7-107">Un moniker tiene las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="cbfb7-107">A moniker has the following parts:</span></span>

-   <span data-ttu-id="cbfb7-108">El prefijo WinMgmts: (obligatorio).</span><span class="sxs-lookup"><span data-stu-id="cbfb7-108">The prefix WinMgmts: (mandatory).</span></span> <span data-ttu-id="cbfb7-109">El prefijo indica a Windows Script Host (WSH) que el siguiente código utilizará los [objetos de API de scripting](scripting-api-objects.md).</span><span class="sxs-lookup"><span data-stu-id="cbfb7-109">The prefix instructs the Windows Script Host (WSH) that the following code will be using the [Scripting API objects](scripting-api-objects.md).</span></span>
-   <span data-ttu-id="cbfb7-110">Un componente de configuración de seguridad (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbfb7-110">A security settings component (optional)</span></span>
-   <span data-ttu-id="cbfb7-111">Un componente de ruta de acceso de objeto WMI (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbfb7-111">A WMI object path component (optional)</span></span>

<span data-ttu-id="cbfb7-112">No se puede especificar una contraseña en una cadena de moniker de WMI.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-112">You cannot specify a password in a WMI moniker string.</span></span> <span data-ttu-id="cbfb7-113">Si debe cambiar la contraseña (parámetro *strPassword* ) o el tipo de autenticación (parámetro *strAuthority* ) al conectarse a WMI, llame a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="cbfb7-113">If you must change the password (*strPassword* parameter) or the type of authentication (*strAuthority* parameter) when connecting to WMI, then call [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="cbfb7-114">Tenga en cuenta que solo puede especificar la contraseña y la autoridad en las conexiones a equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-114">Be aware that you can only specify the password and authority in connections to remote computers.</span></span> <span data-ttu-id="cbfb7-115">Si intenta establecerlos en un script que se esté ejecutando en el equipo local, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-115">Attempting to set these in a script that is running on the local computer results in a error.</span></span> <span data-ttu-id="cbfb7-116">Para obtener más información sobre cuándo se utilizan la configuración de seguridad y los componentes de la ruta de acceso del objeto, vea [configuración de seguridad de WMI](/previous-versions/tn-archive/ee156574(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="cbfb7-116">For more information about when the security settings and object path components are used, see [WMI Security Settings](/previous-versions/tn-archive/ee156574(v=technet.10)).</span></span>

<span data-ttu-id="cbfb7-117">El moniker siguiente especifica el objeto [**SWbemServices**](swbemservices.md) que representa el valor predeterminado de la raíz del espacio de nombres \\ , con suplantación en y el privilegio wbemPrivilegeDebug (SeDebugPrivilege) habilitado, y el privilegio wbemPrivilegeSecurity (SeSecurityPrivilege) deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-117">The following moniker specifies the [**SWbemServices**](swbemservices.md) object that represents the namespace root\\default, with impersonation on and the wbemPrivilegeDebug (SeDebugPrivilege) privilege enabled, and the wbemPrivilegeSecurity (SeSecurityPrivilege) privilege disabled.</span></span>


```VB
"winmgmts:{impersonationLevel=impersonate," & "(debug,!security)}!root\default"
```



> [!Note]
>
> <span data-ttu-id="cbfb7-118">Todos los literales de cadena no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-118">All string literals are case-insensitive.</span></span>
>
> <span data-ttu-id="cbfb7-119">El prefijo "!" de un privilegio indica que se va a deshabilitar el privilegio; la omisión de este prefijo implica que se va a habilitar el privilegio.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-119">The "!" prefix on a privilege indicates that the privilege is to be disabled; the omission of this prefix implies that the privilege is to be enabled.</span></span>
>
> <span data-ttu-id="cbfb7-120">El prefijo "!" se usa en el nombre de equipo o espacio de nombres cuando la configuración de seguridad se especifica entre corchetes antes del nombre o espacio de nombres del equipo.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-120">The "!" prefix is used on the computer name or namespace when security settings are specified in brackets before the computer name or namespace.</span></span>

 

<span data-ttu-id="cbfb7-121">Se permiten las siguientes asignaciones predeterminadas al especificar la ruta de acceso del objeto:</span><span class="sxs-lookup"><span data-stu-id="cbfb7-121">The following default assignments are allowed when specifying the object path:</span></span>

-   <span data-ttu-id="cbfb7-122">El nombre del equipo se puede omitir en la ruta de acceso del objeto, en cuyo caso se presupone el nombre del equipo local.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-122">The computer machine name can be omitted from the object path, in which case the local machine name is assumed.</span></span>
-   <span data-ttu-id="cbfb7-123">El espacio de nombres se puede omitir en la ruta de acceso del objeto, en cuyo caso se supone que se trata del espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-123">The namespace can be omitted from the object path, in which case the default namespace is assumed.</span></span>

    <span data-ttu-id="cbfb7-124">Esto viene determinado por el valor de la clave del registro **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **scripting** \\ **default namespace**, el valor predeterminado es "root \\ CIMv2".</span><span class="sxs-lookup"><span data-stu-id="cbfb7-124">This is determined by the value of the registry key **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Namespace**, the default value is "Root\\CIMv2".</span></span>

-   <span data-ttu-id="cbfb7-125">También se puede especificar una clase o una instancia, en cuyo caso el objeto devuelto es un objeto WMI en lugar de un objeto de servicios.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-125">A class or instance can also be specified, in which case the returned object is a WMI object rather than a services object.</span></span>

> [!Note]  
> <span data-ttu-id="cbfb7-126">Si se especifica una clase o instancia, no se puede omitir el espacio de nombres al especificar el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-126">If a class or instance is specified, you cannot omit the namespace when specifying the computer machine name.</span></span>

 

<span data-ttu-id="cbfb7-127">Para obtener una referencia de las constantes de privilegio usadas en la cadena de moniker de WMI, vea [constantes de privilegios](privilege-constants.md)y los descriptores "nombre corto de scripting".</span><span class="sxs-lookup"><span data-stu-id="cbfb7-127">For a reference of the Privilege Constants used on WMI moniker string, see [Privilege Constants](privilege-constants.md), and the "Scripting short name" descriptors.</span></span>

## <a name="valid-moniker-strings"></a><span data-ttu-id="cbfb7-128">Cadenas de moniker válidas</span><span class="sxs-lookup"><span data-stu-id="cbfb7-128">Valid Moniker Strings</span></span>

<span data-ttu-id="cbfb7-129">En los ejemplos siguientes se muestran cadenas de moniker válidas.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-129">The following examples show valid moniker strings.</span></span>

<span data-ttu-id="cbfb7-130">El moniker siguiente identifica el espacio de nombres predeterminado en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-130">The following moniker identifies the default namespace on the local computer.</span></span> <span data-ttu-id="cbfb7-131">Se devuelve un objeto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="cbfb7-131">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
WinMgmts:
```



<span data-ttu-id="cbfb7-132">El moniker siguiente identifica el espacio de nombres predeterminado en el equipo Server.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-132">The following moniker identifies the default namespace on the computer myServer.</span></span> <span data-ttu-id="cbfb7-133">Se devuelve un objeto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="cbfb7-133">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts://myServer"
```



<span data-ttu-id="cbfb7-134">El moniker siguiente identifica el \\ espacio de nombres root cimv2 en el equipo de servidor.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-134">The following moniker identifies the root\\cimv2 namespace on the myServer computer.</span></span> <span data-ttu-id="cbfb7-135">Se devuelve un objeto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="cbfb7-135">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts://myServer/root/cimv2"
```



<span data-ttu-id="cbfb7-136">El moniker siguiente identifica el \\ espacio de nombres root cimv2 en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-136">The following moniker identifies the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="cbfb7-137">Se devuelve un objeto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="cbfb7-137">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts:root/cimv2"
```



<span data-ttu-id="cbfb7-138">El moniker siguiente identifica la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en el \\ espacio de nombres root cimv2 en el servidor de servidor.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-138">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the root\\cimv2 namespace on the myServer server.</span></span> <span data-ttu-id="cbfb7-139">Se devuelve un objeto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="cbfb7-139">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" _
    & "!//myServer/root/cimv2:Win32_LogicalDisk"
```



<span data-ttu-id="cbfb7-140">El moniker siguiente identifica la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en el \\ espacio de nombres root cimv2 en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-140">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="cbfb7-141">Se devuelve un objeto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="cbfb7-141">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk"
```



<span data-ttu-id="cbfb7-142">El moniker siguiente identifica la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en el espacio de nombres predeterminado en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-142">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the default namespace on the local server.</span></span> <span data-ttu-id="cbfb7-143">Se devuelve un objeto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="cbfb7-143">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk"
```



<span data-ttu-id="cbfb7-144">El moniker siguiente identifica la instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondiente a la unidad C: en el espacio de nombres de scripting predeterminado en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-144">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the default scripting namespace on the local server.</span></span> <span data-ttu-id="cbfb7-145">Se devuelve un objeto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="cbfb7-145">An [**SWbemObject**](swbemobject.md) object is returned.</span></span> <span data-ttu-id="cbfb7-146">El espacio de nombres predeterminado para scripting viene determinado por el valor predeterminado de configuración del espacio de nombres, tal y como se especifica en el control WMI.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-146">The default namespace for scripting is determined by the default namespace configuration setting as specified in the WMI Control.</span></span> <span data-ttu-id="cbfb7-147">Para obtener más información, vea [establecer la seguridad del espacio de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="cbfb7-147">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>


```VB
"WinMgmts::Win32_LogicalDisk='C:'"
```



<span data-ttu-id="cbfb7-148">El moniker siguiente identifica la instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondiente a la unidad C: en el \\ espacio de nombres root cimv2 en el servidor de servidor.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-148">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the root\\cimv2 namespace on the myServer server.</span></span> <span data-ttu-id="cbfb7-149">Se devuelve un objeto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="cbfb7-149">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!//myServer/root/cimv2:Win32_LogicalDisk="C:""
```



<span data-ttu-id="cbfb7-150">El moniker siguiente identifica la instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondiente a la unidad C: en el \\ espacio de nombres root cimv2 en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-150">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="cbfb7-151">Se devuelve un objeto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="cbfb7-151">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk="C:""
```



<span data-ttu-id="cbfb7-152">El moniker siguiente identifica la instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondiente a la unidad C: en el espacio de nombres predeterminado en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-152">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the default namespace on the local server.</span></span> <span data-ttu-id="cbfb7-153">Se devuelve un objeto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="cbfb7-153">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk="C:""
```



<span data-ttu-id="cbfb7-154">El moniker siguiente establece el nivel de suplantación en Impersonate y establece el \_ privilegio de depuración se.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-154">The following moniker sets the impersonation level to impersonate and sets the SE\_DEBUG privilege.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate, (Debug)}"
```



<span data-ttu-id="cbfb7-155">El moniker siguiente establece el nivel de suplantación en Impersonate y establece el \_ privilegio de depuración se.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-155">The following moniker sets the impersonation level to impersonate and sets the SE\_DEBUG privilege.</span></span> <span data-ttu-id="cbfb7-156">También revoca el privilegio de cierre de SE \_ .</span><span class="sxs-lookup"><span data-stu-id="cbfb7-156">It also revokes the SE\_SHUTDOWN privilege.</span></span>


```VB
"WinMgmts:{impersonate,(Debug,!Shutdown)}"
```



<span data-ttu-id="cbfb7-157">El moniker siguiente recupera las descripciones localizadas en Inglés de Estados Unidos de la clase **MyClass** del \\ espacio de nombres WMI raíz.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-157">The following moniker retrieves American English localized descriptions for the **myclass** class from the root\\wmi namespace.</span></span>


```VB
"WinMgmts:[locale=ms_409]!root/wmi:myclass"
```



<span data-ttu-id="cbfb7-158">El moniker siguiente solicita la autenticación Kerberos mediante el \\ servidor dominio principal.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-158">The following moniker requests Kerberos authentication using the principal mydomain\\server.</span></span>


```VB
"Winmgmts:{impersonationLevel=delegate," _
    & "authority=kerberos:mydomain\server}" _
    & "!//myserver/root/default:__cimomidentification=@"
```



<span data-ttu-id="cbfb7-159">El moniker siguiente solicita la autenticación NTLM mediante el dominio midominio.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-159">The following moniker requests NTLM authentication using the mydomain domain.</span></span>


```VB
"Winmgmts:{impersonationLevel=impersonate," & _
    "authority=ntlmdomain:mydomain} " & _
    "!//myserver/root/default:__cimomidentification=@
```



<span data-ttu-id="cbfb7-160">En el ejemplo de código de VBScript siguiente se muestra cómo combinar parámetros de configuración regional y seguridad en un moniker.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-160">The following VBScript code example shows how to combine security and locale parameters in a moniker.</span></span>


```VB
'*****************************************************************
'   Name    :  Moniker.vbs
'
'   Purpose :  This example shows how to set various 
'              parameters in a moniker. 
'****************************************************************

Set myobj = GetObject("WINMGMTS:" _
            & "{impersonationLevel=impersonate," _
            & "authenticationLevel=pktPrivacy," _
            & "authority=ntlmdomain:mydomain," _
            & "(Debug,!Shutdown)}" _
            & "[locale=ms_409]" _
            & "!\\User1\ROOT\CIMV2:Win32_LogicalDisk=""C:""")

wscript.echo "File system = " & myobj.filesystem
```



> [!Note]
>
> Aunque los monikers proporcionan un acceso directo a los objetos, en determinadas circunstancias, el uso repetido de monikers puede ser menos eficaz que el código equivalente que se conecta explícitamente a WMI. <span data-ttu-id="cbfb7-162">Si el rendimiento de la aplicación es una consideración, considere la posibilidad de usar los mecanismos alternativos.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-162">If application performance is a consideration, consider using the alternative mechanisms.</span></span>
>
> <span data-ttu-id="cbfb7-163">No es posible usar la función **GetObject** proporcionada por VBScript para actualizar o establecer los datos al ejecutar scripts incrustados en una página HTML, ya que Microsoft Internet Explorer deniega el uso de esta llamada por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="cbfb7-163">It is not possible to use the **GetObject** function provided by VBScript to update or set data when running scripts embedded within an HTML page, as Microsoft Internet Explorer denies the use of this call for security reasons.</span></span>

 

 

 
