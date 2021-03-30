---
description: Describe la sesión de inicio de sesión o las sesiones asociadas a un usuario que ha iniciado sesión en un equipo que ejecuta Windows.
ms.assetid: d09a115b-95a3-47c7-a04d-c810d044ccc8
ms.tgt_platform: multiple
title: Win32_LogonSession (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogonSession
- Win32_LogonSession.Caption
- Win32_LogonSession.Description
- Win32_LogonSession.InstallDate
- Win32_LogonSession.Name
- Win32_LogonSession.Status
- Win32_LogonSession.StartTime
- Win32_LogonSession.AuthenticationPackage
- Win32_LogonSession.LogonId
- Win32_LogonSession.LogonType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78e14bbd41c2fd8bb0c10a7bfeeda0dc9d426b0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807136"
---
# <a name="win32_logonsession-class"></a><span data-ttu-id="13b0c-103">\_Clase Win32 LogonSession</span><span class="sxs-lookup"><span data-stu-id="13b0c-103">Win32\_LogonSession class</span></span>

<span data-ttu-id="13b0c-104">La clase WMI **\_ LogonSession de Win32** (vea [recuperación de una clase WMI](/windows/desktop/wmisdk/retrieving-a-class)) describe la sesión de inicio de sesión o las sesiones asociadas a un usuario que ha iniciado sesión en un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="13b0c-104">The **Win32\_LogonSession** WMI class (see [Retrieving a WMI class](/windows/desktop/wmisdk/retrieving-a-class)) describes the logon session or sessions associated with a user logged on to a computer system running Windows.</span></span>

<span data-ttu-id="13b0c-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="13b0c-105">The following syntax is simplified from Managed Object Format (MOF) code, and includes all of the inherited properties.</span></span> <span data-ttu-id="13b0c-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="13b0c-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="13b0c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13b0c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{9083C21E-7D58-4e0e-BC30-0BC8922AFB8B}"), AMENDMENT]
class Win32_LogonSession : Win32_Session
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime StartTime;
  string   AuthenticationPackage;
  string   LogonId;
  uint32   LogonType;
};
```

## <a name="members"></a><span data-ttu-id="13b0c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="13b0c-108">Members</span></span>

<span data-ttu-id="13b0c-109">La **clase \_ LogonSession de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="13b0c-109">The **Win32\_LogonSession** class has these types of members:</span></span>

-   [<span data-ttu-id="13b0c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="13b0c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13b0c-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="13b0c-111">Properties</span></span>

<span data-ttu-id="13b0c-112">La **clase \_ LogonSession de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="13b0c-112">The **Win32\_LogonSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13b0c-113">**AuthenticationPackage**</span><span class="sxs-lookup"><span data-stu-id="13b0c-113">**AuthenticationPackage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b0c-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="13b0c-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13b0c-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="13b0c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13b0c-116">Nombre del subsistema utilizado para autenticar la sesión de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="13b0c-116">Name of the subsystem used to authenticate the logon session.</span></span>

</dd> <dt>

<span data-ttu-id="13b0c-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="13b0c-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b0c-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="13b0c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13b0c-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="13b0c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b0c-120">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="13b0c-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="13b0c-121">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="13b0c-121">A short textual description of the object.</span></span>

<span data-ttu-id="13b0c-122">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13b0c-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13b0c-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13b0c-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b0c-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="13b0c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13b0c-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="13b0c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b0c-126">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="13b0c-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="13b0c-127">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="13b0c-127">A textual description of the object.</span></span>

<span data-ttu-id="13b0c-128">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13b0c-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13b0c-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="13b0c-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b0c-130">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="13b0c-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="13b0c-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="13b0c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b0c-132">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="13b0c-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="13b0c-133">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="13b0c-133">Indicates when the object was installed.</span></span> <span data-ttu-id="13b0c-134">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="13b0c-134">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="13b0c-135">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13b0c-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13b0c-136">**LogonId**</span><span class="sxs-lookup"><span data-stu-id="13b0c-136">**LogonId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b0c-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="13b0c-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13b0c-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="13b0c-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b0c-139">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="13b0c-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="13b0c-140">IDENTIFICADOR asignado a la sesión de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="13b0c-140">ID assigned to the logon session.</span></span>

</dd> <dt>

<span data-ttu-id="13b0c-141">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="13b0c-141">**LogonType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b0c-142">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13b0c-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13b0c-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="13b0c-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13b0c-144">Valor numérico que indica el tipo de sesión de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="13b0c-144">Numeric value that indicates the type of logon session.</span></span>

<dt>

<span data-ttu-id="13b0c-145">0</span><span class="sxs-lookup"><span data-stu-id="13b0c-145">0</span></span>
</dt> <dd>

<span data-ttu-id="13b0c-146">Solo lo usa la cuenta del sistema.</span><span class="sxs-lookup"><span data-stu-id="13b0c-146">Used only by the System account.</span></span>

</dd> <dt>

<span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>

<span data-ttu-id="13b0c-147"><span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>**Interactivo** (2)</span><span class="sxs-lookup"><span data-stu-id="13b0c-147"><span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>**Interactive** (2)</span></span>


</dt> <dd>

<span data-ttu-id="13b0c-148">Diseñado para usuarios que utilizan el equipo de forma interactiva, como un usuario que inicia sesión en un servidor de Terminal Server, un shell remoto o un proceso similar.</span><span class="sxs-lookup"><span data-stu-id="13b0c-148">Intended for users who are interactively using the machine, such as a user being logged on by a terminal server, remote shell, or similar process.</span></span>

</dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

<span data-ttu-id="13b0c-149"><span id="Network"></span><span id="network"></span><span id="NETWORK"></span>**Red** (3)</span><span class="sxs-lookup"><span data-stu-id="13b0c-149"><span id="Network"></span><span id="network"></span><span id="NETWORK"></span>**Network** (3)</span></span>


</dt> <dd>

<span data-ttu-id="13b0c-150">Diseñado para servidores de alto rendimiento para autenticar contraseñas de texto no cifrado.</span><span class="sxs-lookup"><span data-stu-id="13b0c-150">Intended for high-performance servers to authenticate clear text passwords.</span></span> <span data-ttu-id="13b0c-151">LogonUser no almacena en caché las credenciales para este tipo de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="13b0c-151">LogonUser does not cache credentials for this logon type.</span></span>

</dd> <dt>

<span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>

<span data-ttu-id="13b0c-152"><span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>**Lote** (4)</span><span class="sxs-lookup"><span data-stu-id="13b0c-152"><span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>**Batch** (4)</span></span>


</dt> <dd>

<span data-ttu-id="13b0c-153">Diseñado para servidores de batch, donde los procesos se pueden ejecutar en nombre de un usuario sin su intervención directa; o para servidores de mayor rendimiento que procesan muchos intentos de autenticación de texto no cifrado a la vez, como servidores web o de correo.</span><span class="sxs-lookup"><span data-stu-id="13b0c-153">Intended for batch servers, where processes can be executed on behalf of a user without their direct intervention; or for higher performance servers that process many clear-text authentication attempts at a time, such as mail or web servers.</span></span> <span data-ttu-id="13b0c-154">LogonUser no almacena en caché las credenciales para este tipo de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="13b0c-154">LogonUser does not cache credentials for this logon type.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="13b0c-155"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio** (5)</span><span class="sxs-lookup"><span data-stu-id="13b0c-155"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (5)</span></span>


</dt> <dd>

<span data-ttu-id="13b0c-156">Indica un inicio de sesión de tipo de servicio.</span><span class="sxs-lookup"><span data-stu-id="13b0c-156">Indicates a service-type logon.</span></span> <span data-ttu-id="13b0c-157">La cuenta proporcionada debe tener habilitado el privilegio de servicio.</span><span class="sxs-lookup"><span data-stu-id="13b0c-157">The account provided must have the service privilege enabled.</span></span>

</dd> <dt>

<span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>

<span data-ttu-id="13b0c-158"><span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>**Proxy** (6)</span><span class="sxs-lookup"><span data-stu-id="13b0c-158"><span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>**Proxy** (6)</span></span>


</dt> <dd>

<span data-ttu-id="13b0c-159">Indica un inicio de sesión de tipo proxy.</span><span class="sxs-lookup"><span data-stu-id="13b0c-159">Indicates a proxy-type logon.</span></span>

</dd> <dt>

<span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>

<span data-ttu-id="13b0c-160"><span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>**Desbloquear** (7)</span><span class="sxs-lookup"><span data-stu-id="13b0c-160"><span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>**Unlock** (7)</span></span>


</dt> <dd>

<span data-ttu-id="13b0c-161">Este tipo de inicio de sesión está pensado para el registro de archivos dll GINA en los usuarios que usan el equipo de forma interactiva.</span><span class="sxs-lookup"><span data-stu-id="13b0c-161">This logon type is intended for GINA DLLs logging on users who are interactively using the machine.</span></span> <span data-ttu-id="13b0c-162">Este tipo de inicio de sesión permite generar un registro de auditoría único que muestra Cuándo se desbloqueó la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="13b0c-162">This logon type allows a unique audit record to be generated that shows when the workstation was unlocked.</span></span>

</dd> <dt>

<span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>

<span data-ttu-id="13b0c-163"><span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>**NetworkCleartext** (8)</span><span class="sxs-lookup"><span data-stu-id="13b0c-163"><span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>**NetworkCleartext** (8)</span></span>


</dt> <dd>

<span data-ttu-id="13b0c-164">Conserva el nombre y la contraseña en los paquetes de autenticación, lo que permite que el servidor realice conexiones a otros servidores de red durante la suplantación del cliente.</span><span class="sxs-lookup"><span data-stu-id="13b0c-164">Preserves the name and password in the authentication packages, allowing the server to make connections to other network servers while impersonating the client.</span></span> <span data-ttu-id="13b0c-165">Esto permite a un servidor aceptar credenciales de texto sin cifrar de un cliente, llamar a LogonUser, comprobar que el usuario puede tener acceso al sistema a través de la red y seguir comunicándose con otros servidores.</span><span class="sxs-lookup"><span data-stu-id="13b0c-165">This allows a server to accept clear text credentials from a client, call LogonUser, verify that the user can access the system across the network, and still communicate with other servers.</span></span>

</dd> <dt>

<span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>

<span data-ttu-id="13b0c-166"><span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>**NewCredentials** (9)</span><span class="sxs-lookup"><span data-stu-id="13b0c-166"><span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>**NewCredentials** (9)</span></span>


</dt> <dd>

<span data-ttu-id="13b0c-167">Permite que el autor de la llamada Clone su token actual y especifique nuevas credenciales para las conexiones salientes.</span><span class="sxs-lookup"><span data-stu-id="13b0c-167">Allows the caller to clone its current token and specify new credentials for outbound connections.</span></span> <span data-ttu-id="13b0c-168">La nueva sesión de inicio de sesión tiene la misma identidad local, pero usa credenciales diferentes para otras conexiones de red.</span><span class="sxs-lookup"><span data-stu-id="13b0c-168">The new logon session has the same local identify, but uses different credentials for other network connections.</span></span>

</dd> <dt>

<span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>

<span data-ttu-id="13b0c-169"><span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>**RemoteInteractive** (10)</span><span class="sxs-lookup"><span data-stu-id="13b0c-169"><span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>**RemoteInteractive** (10)</span></span>


</dt> <dd>

<span data-ttu-id="13b0c-170">Terminal Services sesión remota e interactiva.</span><span class="sxs-lookup"><span data-stu-id="13b0c-170">Terminal Services session that is both remote and interactive.</span></span>

</dd> <dt>

<span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>

<span data-ttu-id="13b0c-171"><span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>**CachedInteractive** (11)</span><span class="sxs-lookup"><span data-stu-id="13b0c-171"><span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>**CachedInteractive** (11)</span></span>


</dt> <dd>

<span data-ttu-id="13b0c-172">Intentos de credenciales en caché sin acceso a la red.</span><span class="sxs-lookup"><span data-stu-id="13b0c-172">Attempt cached credentials without accessing the network.</span></span>

</dd> <dt>

<span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>

<span data-ttu-id="13b0c-173"><span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>**CachedRemoteInteractive** (12)</span><span class="sxs-lookup"><span data-stu-id="13b0c-173"><span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>**CachedRemoteInteractive** (12)</span></span>


</dt> <dd>

<span data-ttu-id="13b0c-174">Igual que RemoteInteractive.</span><span class="sxs-lookup"><span data-stu-id="13b0c-174">Same as RemoteInteractive.</span></span> <span data-ttu-id="13b0c-175">Se utiliza para la auditoría interna.</span><span class="sxs-lookup"><span data-stu-id="13b0c-175">This is used for internal auditing.</span></span>

</dd> <dt>

<span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>

<span data-ttu-id="13b0c-176"><span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>**CachedUnlock** (13)</span><span class="sxs-lookup"><span data-stu-id="13b0c-176"><span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>**CachedUnlock** (13)</span></span>


</dt> <dd>

<span data-ttu-id="13b0c-177">Inicio de sesión de estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="13b0c-177">Workstation logon.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="13b0c-178">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="13b0c-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b0c-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="13b0c-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13b0c-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="13b0c-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b0c-181">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="13b0c-181">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="13b0c-182">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="13b0c-182">Label by which the object is known.</span></span> <span data-ttu-id="13b0c-183">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="13b0c-183">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="13b0c-184">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13b0c-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13b0c-185">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="13b0c-185">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b0c-186">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="13b0c-186">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="13b0c-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="13b0c-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13b0c-188">Hora a la que se inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="13b0c-188">Time at which the session started.</span></span>

<span data-ttu-id="13b0c-189">Esta propiedad se hereda de [**la \_ sesión de Win32**](win32-session.md).</span><span class="sxs-lookup"><span data-stu-id="13b0c-189">This property is inherited from [**Win32\_Session**](win32-session.md).</span></span>

</dd> <dt>

<span data-ttu-id="13b0c-190">**Estado**</span><span class="sxs-lookup"><span data-stu-id="13b0c-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13b0c-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="13b0c-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13b0c-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="13b0c-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13b0c-193">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="13b0c-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="13b0c-194">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="13b0c-194">String that indicates the current status of the object.</span></span> <span data-ttu-id="13b0c-195">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="13b0c-195">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="13b0c-196">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="13b0c-196">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="13b0c-197">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="13b0c-197">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="13b0c-198">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="13b0c-198">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="13b0c-199">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="13b0c-199">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="13b0c-200">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="13b0c-200">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="13b0c-201">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13b0c-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="13b0c-202">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="13b0c-202">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="13b0c-203">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="13b0c-203">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="13b0c-204">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="13b0c-204">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="13b0c-205">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="13b0c-205">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13b0c-206">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="13b0c-206">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="13b0c-207">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="13b0c-207">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="13b0c-208">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="13b0c-208">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="13b0c-209">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="13b0c-209">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="13b0c-210">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="13b0c-210">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="13b0c-211">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="13b0c-211">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="13b0c-212">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="13b0c-212">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="13b0c-213">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="13b0c-213">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="13b0c-214">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="13b0c-214">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="13b0c-215"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="13b0c-215"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="examples"></a><span data-ttu-id="13b0c-216">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="13b0c-216">Examples</span></span>

<span data-ttu-id="13b0c-217">En el ejemplo de [información de sesión de inicio](https://Gallery.TechNet.Microsoft.Com/scriptcenter/64cc7ab5-f1cd-460c-9d37-e6f989444de3) de sesión de PowerShell se devuelve información acerca de las sesiones de inicio de sesión asociadas al usuario que ha iniciado sesión en un equipo.</span><span class="sxs-lookup"><span data-stu-id="13b0c-217">The [List Logon Session Information](https://Gallery.TechNet.Microsoft.Com/scriptcenter/64cc7ab5-f1cd-460c-9d37-e6f989444de3) PowerShell sample returns information about logon sessions associated with the user currently logged on to a computer.</span></span>

<span data-ttu-id="13b0c-218">En el siguiente ejemplo de PowerShell se comprueba si hay una sesión remota abierta para un usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="13b0c-218">The following PowerShell example checks for remote session open for a specified user.</span></span>


```PowerShell
$user = "<user name>"
$servers = gci servers.txt 

     foreach ($server in $servers){
     $logons = gwmi win32_loggedonuser -computername $server

          foreach ($logon in $logons){
               if ($logon.antecedent -match $user){
               $logonid = $logon.dependent.split("=")[1] 
               $session =gwmi win32_logonsession |? {$_.logonid -match $logonid}
               if ($session.logontype -eq "10"){
               Write-host "You have an active Terminal Server session on server $($server)"
                }
          }
```



## <a name="requirements"></a><span data-ttu-id="13b0c-219">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13b0c-219">Requirements</span></span>



| <span data-ttu-id="13b0c-220">Requisito</span><span class="sxs-lookup"><span data-stu-id="13b0c-220">Requirement</span></span> | <span data-ttu-id="13b0c-221">Value</span><span class="sxs-lookup"><span data-stu-id="13b0c-221">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13b0c-222">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13b0c-222">Minimum supported client</span></span><br/> | <span data-ttu-id="13b0c-223">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13b0c-223">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="13b0c-224">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13b0c-224">Minimum supported server</span></span><br/> | <span data-ttu-id="13b0c-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13b0c-225">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13b0c-226">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="13b0c-226">Namespace</span></span><br/>                | <span data-ttu-id="13b0c-227">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="13b0c-227">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="13b0c-228">MOF</span><span class="sxs-lookup"><span data-stu-id="13b0c-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13b0c-229"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13b0c-229"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="13b0c-230">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13b0c-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13b0c-231"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13b0c-231"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13b0c-232">Vea también</span><span class="sxs-lookup"><span data-stu-id="13b0c-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13b0c-233">**\_Sesión Win32**</span><span class="sxs-lookup"><span data-stu-id="13b0c-233">**Win32\_Session**</span></span>](win32-session.md)
</dt> <dt>

<span data-ttu-id="13b0c-234">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="13b0c-234">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

