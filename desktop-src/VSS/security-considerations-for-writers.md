---
description: La infraestructura de VSS requiere procesos de escritura para poder funcionar como clientes COM y como servidores.
ms.assetid: 59bb7a86-e874-45ce-abd6-cafd18802c4d
title: Consideraciones de seguridad para escritores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6f88243adbd62d928170a86ed57b91cbebe134
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696972"
---
# <a name="security-considerations-for-writers"></a><span data-ttu-id="f57b2-103">Consideraciones de seguridad para escritores</span><span class="sxs-lookup"><span data-stu-id="f57b2-103">Security Considerations for Writers</span></span>

<span data-ttu-id="f57b2-104">La infraestructura de VSS requiere procesos de escritura para poder funcionar como clientes COM y como servidores.</span><span class="sxs-lookup"><span data-stu-id="f57b2-104">The VSS infrastructure requires writer processes to be able to function both as COM clients and as servers.</span></span>

<span data-ttu-id="f57b2-105">Cuando actúan como servidores, los escritores de VSS exponen interfaces COM (por ejemplo, los controladores de eventos de VSS como [**CVssWriter::**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)GatherWriterMetadata) y reciben llamadas com entrantes desde procesos de VSS (como solicitantes y el servicio VSS) o llamadas RPC desde procesos externos a VSS, normalmente cuando estos procesos generan eventos VSS (por ejemplo, cuando un solicitante llama a [**IVssBackupComponents::**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata))</span><span class="sxs-lookup"><span data-stu-id="f57b2-105">When acting as servers, VSS writers expose COM interfaces (for example, the VSS event handlers such as [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)) and receive incoming COM calls from VSS processes (such as requesters and the VSS service) or RPC calls from processes that are external to VSS, typically when these processes generate VSS events (for example, when a requester calls [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)).</span></span> <span data-ttu-id="f57b2-106">Por lo tanto, una VSS Writer necesita administrar de forma segura qué clientes COM pueden realizar llamadas COM entrantes en su proceso.</span><span class="sxs-lookup"><span data-stu-id="f57b2-106">Therefore, a VSS writer needs to securely manage which COM clients are able to make incoming COM calls into its process.</span></span>

<span data-ttu-id="f57b2-107">Del mismo modo, los escritores de VSS también pueden actuar como clientes COM, realizar llamadas COM salientes a devoluciones de llamada proporcionadas por la infraestructura de VSS o llamadas RPC a procesos externos a VSS.</span><span class="sxs-lookup"><span data-stu-id="f57b2-107">Similarly, VSS writers may also act as COM clients, making outgoing COM calls to callbacks supplied by the VSS infrastructure or RPC calls to processes that are external to VSS.</span></span> <span data-ttu-id="f57b2-108">Estas devoluciones de llamada que son proporcionadas por una aplicación de copia de seguridad o por el servicio VSS permiten al escritor realizar tareas como la actualización del documento componentes de copia de seguridad a través de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .</span><span class="sxs-lookup"><span data-stu-id="f57b2-108">These callbacks that are provided either by a backup application or by the VSS service allow the writer to perform tasks such as updating the Backup Components Document through the [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface.</span></span> <span data-ttu-id="f57b2-109">Por lo tanto, la configuración de seguridad de VSS debe permitir que los escritores realicen llamadas COM salientes en otros procesos de VSS.</span><span class="sxs-lookup"><span data-stu-id="f57b2-109">Therefore, VSS security settings must allow writers to make outgoing COM calls into other VSS processes.</span></span>

<span data-ttu-id="f57b2-110">El mecanismo más sencillo para administrar los problemas de seguridad del sistema de escritura implica la selección adecuada de la cuenta de usuario en la que se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="f57b2-110">The simplest mechanism for managing writer security issues involves the proper selection of the user account under which it runs.</span></span> <span data-ttu-id="f57b2-111">Normalmente, un sistema de escritura necesita ejecutarse en un usuario que sea miembro del grupo administradores o del grupo operadores de copia de seguridad, o bien debe ejecutarse como la cuenta del sistema local.</span><span class="sxs-lookup"><span data-stu-id="f57b2-111">A writer typically needs to run under a user who is a member of either the Administrators group or the Backup Operators group, or it needs to run as the Local System account.</span></span>

<span data-ttu-id="f57b2-112">De forma predeterminada, cuando un escritor actúa como cliente COM, si no se ejecuta en estas cuentas, cualquier llamada COM que realice se rechazará automáticamente con **E \_ ACCESSDENIED** sin necesidad de llegar a la implementación del método com.</span><span class="sxs-lookup"><span data-stu-id="f57b2-112">By default, when a writer is acting as a COM client, if it does not run under these accounts, any COM call it makes is automatically rejected with **E\_ACCESSDENIED** without even getting to the COM method implementation.</span></span>

## <a name="disabling-com-exception-handling"></a><span data-ttu-id="f57b2-113">Deshabilitar el control de excepciones COM</span><span class="sxs-lookup"><span data-stu-id="f57b2-113">Disabling COM Exception Handling</span></span>

<span data-ttu-id="f57b2-114">Al desarrollar un escritor, establezca la marca de COMGLB donot de la \_ excepción \_ \_ de identificador de opciones globales de com para deshabilitar el control de excepciones com.</span><span class="sxs-lookup"><span data-stu-id="f57b2-114">When developing a writer, set the COM COMGLB\_EXCEPTION\_DONOT\_HANDLE global options flag to disable COM exception handling.</span></span> <span data-ttu-id="f57b2-115">Es importante hacerlo porque el control de excepciones COM puede enmascarar errores irrecuperables en una aplicación de VSS.</span><span class="sxs-lookup"><span data-stu-id="f57b2-115">It is important to do this because COM exception handling can mask fatal errors in a VSS application.</span></span> <span data-ttu-id="f57b2-116">El error que se enmascara puede dejar el proceso en un estado inestable e impredecible, lo que puede provocar daños y bloqueos.</span><span class="sxs-lookup"><span data-stu-id="f57b2-116">The error that is masked can leave the process in an unstable and unpredictable state, which can lead to corruptions and hangs.</span></span> <span data-ttu-id="f57b2-117">Para obtener más información acerca de esta marca, vea [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span><span class="sxs-lookup"><span data-stu-id="f57b2-117">For more information about this flag, see [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span></span>

## <a name="setting-writer-default-com-access-check-permission"></a><span data-ttu-id="f57b2-118">Estableciendo el permiso de comprobación de acceso COM predeterminado del escritor</span><span class="sxs-lookup"><span data-stu-id="f57b2-118">Setting Writer Default COM Access Check Permission</span></span>

<span data-ttu-id="f57b2-119">Los escritores deben tener en cuenta que cuando sus procesos actúan como un servidor (por ejemplo, para controlar los eventos de VSS), deben permitir llamadas entrantes de otros participantes de VSS, como solicitantes o el servicio VSS.</span><span class="sxs-lookup"><span data-stu-id="f57b2-119">Writers need to be aware that when their processes act as a server (for example, to handle VSS events), they must allow incoming calls from other VSS participants, such as requesters or the VSS service.</span></span>

<span data-ttu-id="f57b2-120">Sin embargo, de forma predeterminada, un proceso solo permitirá que los clientes COM que se ejecutan en la misma sesión de inicio de sesión sean el propio SID) o que se ejecuten en la cuenta de sistema local.</span><span class="sxs-lookup"><span data-stu-id="f57b2-120">However, by default, a process will allow only COM clients that are running under the same logon session the SELF SID) or running under the Local System account.</span></span> <span data-ttu-id="f57b2-121">Este es un posible problema porque estos valores predeterminados no son suficientes para admitir la infraestructura de VSS.</span><span class="sxs-lookup"><span data-stu-id="f57b2-121">This is a potential problem because these defaults are not sufficient to support the VSS infrastructure.</span></span> <span data-ttu-id="f57b2-122">Por ejemplo, los solicitantes pueden ejecutarse como una cuenta de usuario de "operador de copia de seguridad" que no sea en la misma sesión de inicio de sesión que el proceso de escritor ni una cuenta de sistema local.</span><span class="sxs-lookup"><span data-stu-id="f57b2-122">For example, requesters may run as a "Backup Operator" user account that is neither in the same logon session as the writer process nor a Local System account.</span></span>

<span data-ttu-id="f57b2-123">Para controlar este tipo de problema, cada proceso de servidor COM puede ejercer un mayor control sobre si un cliente RPC o COM tiene permiso para realizar un método COM el servidor (un escritor en este caso) implementa mediante [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer un permiso de comprobación de acceso com predeterminado para todo el proceso.</span><span class="sxs-lookup"><span data-stu-id="f57b2-123">To handle this type of problem, every COM server process can exercise further control over whether an RPC or COM client is allowed to perform a COM method the server (a writer in this case) implements by using [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set a process-wide default COM access check permission.</span></span>

<span data-ttu-id="f57b2-124">Los escritores pueden hacer lo siguiente explícitamente:</span><span class="sxs-lookup"><span data-stu-id="f57b2-124">Writers can explicitly do the following:</span></span>

-   <span data-ttu-id="f57b2-125">Permitir el acceso de todos los procesos para llamar al proceso de escritura.</span><span class="sxs-lookup"><span data-stu-id="f57b2-125">Allow all processes access to call into the writer process.</span></span>

    <span data-ttu-id="f57b2-126">Esta opción puede ser adecuada para muchos escritores y se usa en otros servidores COM; por ejemplo, todos los servicios de Windows basados en SVCHOST ya usan esta opción, al igual que todos los servicios COM+ de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f57b2-126">This option may be adequate for many writers, and is used by other COM servers—for example, all SVCHOST-based Windows services are already using this option, as are all COM+ Services by default.</span></span>

    <span data-ttu-id="f57b2-127">Permitir que todos los procesos realicen llamadas COM entrantes no es necesariamente un punto débil de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f57b2-127">Allowing all processes to perform incoming COM calls is not necessarily a security weakness.</span></span> <span data-ttu-id="f57b2-128">Un escritor que actúa como un servidor COM, al igual que todos los demás servidores COM, conserva siempre la opción de autorizar a sus clientes en cada método COM implementado en su proceso.</span><span class="sxs-lookup"><span data-stu-id="f57b2-128">A writer acting as a COM server, like all other COM servers, always retains the option of authorizing its clients on every COM method implemented in its process.</span></span>

    <span data-ttu-id="f57b2-129">Para permitir que todos los procesos tengan acceso COM a un escritor, puede pasar un descriptor de seguridad **nulo** como primer parámetro de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="f57b2-129">To allow all processes COM access to a writer, you can pass a **NULL** security descriptor as the first parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="f57b2-130">(Tenga en cuenta que se debe llamar a **CoInitializeSecurity** como máximo una vez para todo el proceso.</span><span class="sxs-lookup"><span data-stu-id="f57b2-130">(Note that **CoInitializeSecurity** must be called at most once for the entire process.</span></span> <span data-ttu-id="f57b2-131">Consulte la documentación de COM para obtener más detalles sobre **CoInitializeSecurity**).</span><span class="sxs-lookup"><span data-stu-id="f57b2-131">Please see the COM documentation for more details on **CoInitializeSecurity**.)</span></span>

    <span data-ttu-id="f57b2-132">A continuación se muestra un ejemplo de código que incluye una llamada a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity):</span><span class="sxs-lookup"><span data-stu-id="f57b2-132">The following is a code example that includes a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity):</span></span>

    ``` syntax
    // Initialize COM security.
    hr = CoInitializeSecurity(
           NULL,                          // PSECURITY_DESCRIPTOR          pSecDesc,
           -1,                            // LONG                          cAuthSvc,
           NULL,                          // SOLE_AUTHENTICATION_SERVICE  *asAuthSvc,
           NULL,                          // void                         *pReserved1,
           RPC_C_AUTHN_LEVEL_PKT_PRIVACY, // DWORD                         dwAuthnLevel,
           RPC_C_IMP_LEVEL_IDENTIFY,      // DWORD                         dwImpLevel,
           NULL,                          // void                         *pAuthList,
           EOAC_NONE,                     // DWORD                         dwCapabilities,
           NULL                           // void                         *pReserved3
        );
    ```

    <span data-ttu-id="f57b2-133">Al establecer explícitamente la seguridad de nivel COM de un escritor con [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f57b2-133">When explicitly setting a writer's COM-level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="f57b2-134">Establezca el nivel de autenticación en al menos el nivel de autenticación de **RPC \_ C \_ \_ \_ Connecta**.</span><span class="sxs-lookup"><span data-stu-id="f57b2-134">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_CONNECT**.</span></span>

        <span data-ttu-id="f57b2-135">Para mejorar la seguridad, considere el uso de la **\_ \_ \_ \_ \_ privacidad de nivel de autenticación de RPC C**.</span><span class="sxs-lookup"><span data-stu-id="f57b2-135">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>

    -   <span data-ttu-id="f57b2-136">Establezca el nivel de suplantación **en \_ \_ nivel IMP \_ \_ de RPC C** , a menos que el proceso del escritor necesite permitir la suplantación para llamadas RPC o com específicas que no están relacionadas con VSS.</span><span class="sxs-lookup"><span data-stu-id="f57b2-136">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IDENTIFY** unless the writer process needs to allow impersonation for specific RPC or COM calls that are unrelated to VSS.</span></span>

-   <span data-ttu-id="f57b2-137">Permitir solo el acceso a los procesos especificados para llamar al proceso de escritura.</span><span class="sxs-lookup"><span data-stu-id="f57b2-137">Allow only specified processes access to call into the writer process.</span></span>

    <span data-ttu-id="f57b2-138">Un servidor COM (por ejemplo, un escritor) que llama a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) con un descriptor de seguridad que no **es null** puede usar el descriptor para configurarlo para que acepte llamadas entrantes solo de los usuarios que pertenecen a un conjunto específico de cuentas.</span><span class="sxs-lookup"><span data-stu-id="f57b2-138">A COM server (such as a writer) that is calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) with a non-**NULL** security descriptor can use the descriptor to configure itself to accept incoming calls only from users that belong to a specific set of accounts.</span></span>

    <span data-ttu-id="f57b2-139">Un escritor debe asegurarse de que los clientes COM que se ejecutan en usuarios válidos estén autorizados para llamar a su proceso.</span><span class="sxs-lookup"><span data-stu-id="f57b2-139">A writer must ensure that COM clients running under valid users are authorized to call into its process.</span></span> <span data-ttu-id="f57b2-140">Un escritor que especifica un descriptor de seguridad en el primer parámetro debe permitir que los siguientes usuarios realicen llamadas entrantes en el proceso del solicitante:</span><span class="sxs-lookup"><span data-stu-id="f57b2-140">A writer that specifies a Security Descriptor in the first parameter must allow the following users to perform incoming calls into the requester process:</span></span>

    -   <span data-ttu-id="f57b2-141">Sistema local</span><span class="sxs-lookup"><span data-stu-id="f57b2-141">Local System</span></span>
    -   <span data-ttu-id="f57b2-142">Miembros del grupo local Administradores</span><span class="sxs-lookup"><span data-stu-id="f57b2-142">Members of the local Administrators group</span></span>
    -   <span data-ttu-id="f57b2-143">Miembros del grupo operadores de copia de seguridad local</span><span class="sxs-lookup"><span data-stu-id="f57b2-143">Members of the local Backup Operators group</span></span>
    -   <span data-ttu-id="f57b2-144">La cuenta en la que se está ejecutando el escritor</span><span class="sxs-lookup"><span data-stu-id="f57b2-144">The account under which the writer is running</span></span>

## <a name="explicitly-controlling-user-account-access-to-a-writer"></a><span data-ttu-id="f57b2-145">Controlar explícitamente el acceso de la cuenta de usuario a un escritor</span><span class="sxs-lookup"><span data-stu-id="f57b2-145">Explicitly Controlling User Account Access to a Writer</span></span>

<span data-ttu-id="f57b2-146">Hay casos en los que es necesario restringir el acceso a un sistema de escritura a los procesos que se ejecutan como sistema local, o en los grupos locales de administradores locales o operadores de copia de seguridad locales, que pueden ser demasiado restrictivos.</span><span class="sxs-lookup"><span data-stu-id="f57b2-146">There are cases where restricting access to a writer to processes running as Local System, or under the local Administrators or local Backup Operators local groups, may be too restrictive.</span></span>

<span data-ttu-id="f57b2-147">Por ejemplo, un proceso de escritor (quizás un escritor que no sea del sistema de terceros) podría no tener normalmente que ejecutarse en una cuenta de administrador o de operador de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f57b2-147">For example, a writer process (perhaps a third-party non-system writer) might not ordinarily need to be run under an Administrator or Backup Operator account.</span></span> <span data-ttu-id="f57b2-148">Por motivos de seguridad, sería mejor no promover artificialmente los privilegios del proceso para admitir VSS.</span><span class="sxs-lookup"><span data-stu-id="f57b2-148">For security reasons, it would be best not to artificially promote the process's privileges to support VSS.</span></span>

<span data-ttu-id="f57b2-149">En estos casos, se debe modificar la clave del registro **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** para indicar a VSS que un usuario especificado es seguro para ejecutar una VSS Writer.</span><span class="sxs-lookup"><span data-stu-id="f57b2-149">In these cases, the **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**VSS**\\**VssAccessControl** registry key must be modified to instruct VSS that a specified user is safe to run a VSS writer.</span></span>

<span data-ttu-id="f57b2-150">Bajo esta clave, debe crear una subclave con el mismo nombre que la cuenta a la que se va a conceder o denegar el acceso.</span><span class="sxs-lookup"><span data-stu-id="f57b2-150">Under this key, you must create a subkey that has the same name as the account that is to be granted or denied access.</span></span> <span data-ttu-id="f57b2-151">Esta subclave debe establecerse en uno de los valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f57b2-151">This subkey must be set to one of the values in the following table.</span></span>

| <span data-ttu-id="f57b2-152">Value</span><span class="sxs-lookup"><span data-stu-id="f57b2-152">Value</span></span> | <span data-ttu-id="f57b2-153">Significado</span><span class="sxs-lookup"><span data-stu-id="f57b2-153">Meaning</span></span>                                             |
|-------|-----------------------------------------------------|
| <span data-ttu-id="f57b2-154">0</span><span class="sxs-lookup"><span data-stu-id="f57b2-154">0</span></span>     | <span data-ttu-id="f57b2-155">Deniegue el acceso del usuario al escritor y al solicitante.</span><span class="sxs-lookup"><span data-stu-id="f57b2-155">Deny the user access to your writer and requester.</span></span>  |
| <span data-ttu-id="f57b2-156">1</span><span class="sxs-lookup"><span data-stu-id="f57b2-156">1</span></span>     | <span data-ttu-id="f57b2-157">Conceda al usuario acceso al escritor.</span><span class="sxs-lookup"><span data-stu-id="f57b2-157">Grant the user access to your writer.</span></span>               |
| <span data-ttu-id="f57b2-158">2</span><span class="sxs-lookup"><span data-stu-id="f57b2-158">2</span></span>     | <span data-ttu-id="f57b2-159">Conceda al usuario acceso al solicitante.</span><span class="sxs-lookup"><span data-stu-id="f57b2-159">Grant the user access to your requester.</span></span>            |
| <span data-ttu-id="f57b2-160">3</span><span class="sxs-lookup"><span data-stu-id="f57b2-160">3</span></span>     | <span data-ttu-id="f57b2-161">Conceda al usuario acceso al escritor y al solicitante.</span><span class="sxs-lookup"><span data-stu-id="f57b2-161">Grant the user access to your writer and requester.</span></span> |



 

<span data-ttu-id="f57b2-162">En el siguiente ejemplo se concede acceso a la cuenta "midominio mi \\ usuario":</span><span class="sxs-lookup"><span data-stu-id="f57b2-162">The following example grants access to the "MyDomain\\MyUser" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 1<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="f57b2-163">Este mecanismo también se puede usar para restringir explícitamente que un usuario permitido de otro modo no ejecute un VSS Writer.</span><span class="sxs-lookup"><span data-stu-id="f57b2-163">This mechanism can also be used to explicitly restrict an otherwise permitted user from running a VSS writer.</span></span> <span data-ttu-id="f57b2-164">En el siguiente ejemplo se restringirá el acceso de la cuenta de administrador de ThatDomain \\ :</span><span class="sxs-lookup"><span data-stu-id="f57b2-164">The following example will restrict access from the "ThatDomain\\Administrator" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  ThatDomain\Administrator = 0<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="f57b2-165">El administrador de ThatDomain de usuario \\ no podría ejecutar un VSS Writer.</span><span class="sxs-lookup"><span data-stu-id="f57b2-165">The user ThatDomain\\Administrator would not be able to run a VSS writer.</span></span>

 

 
