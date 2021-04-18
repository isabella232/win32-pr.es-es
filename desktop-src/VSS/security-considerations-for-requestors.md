---
description: La infraestructura de VSS requiere que los solicitantes VSS, como las aplicaciones de copia de seguridad, puedan funcionar como clientes COM y como servidor.
ms.assetid: b01145c6-76ba-4a81-bca6-59c4ca488dac
title: Consideraciones de seguridad para los solicitantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e989793dbf5a5dd1fac3224cf6f06958564de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360601"
---
# <a name="security-considerations-for-requesters"></a><span data-ttu-id="c4472-103">Consideraciones de seguridad para los solicitantes</span><span class="sxs-lookup"><span data-stu-id="c4472-103">Security Considerations for Requesters</span></span>

<span data-ttu-id="c4472-104">La infraestructura de VSS requiere que los solicitantes VSS, como las aplicaciones de copia de seguridad, puedan funcionar como clientes COM y como servidor.</span><span class="sxs-lookup"><span data-stu-id="c4472-104">The VSS infrastructure requires VSS requesters, such as backup applications, to be able to function both as COM clients and as a server.</span></span>

<span data-ttu-id="c4472-105">Cuando actúa como un servidor, un solicitante expone un conjunto de interfaces de devolución de llamada COM que se pueden invocar desde procesos externos (como escritores o el servicio VSS).</span><span class="sxs-lookup"><span data-stu-id="c4472-105">When acting as a server, a requester exposes a set of COM callback interfaces that can be invoked from external processes (such as writers or the VSS service).</span></span> <span data-ttu-id="c4472-106">Por lo tanto, los solicitantes necesitan administrar de forma segura qué clientes COM pueden realizar llamadas COM entrantes en su proceso.</span><span class="sxs-lookup"><span data-stu-id="c4472-106">Therefore, requesters need to securely manage which COM clients are able to make incoming COM calls into its process.</span></span>

<span data-ttu-id="c4472-107">Del mismo modo, los solicitantes pueden actuar como cliente COM para las API COM proporcionadas por un VSS Writer o por el servicio VSS.</span><span class="sxs-lookup"><span data-stu-id="c4472-107">Similarly, requesters can act as a COM client for the COM APIs supplied by a VSS writer or by the VSS service.</span></span> <span data-ttu-id="c4472-108">La configuración de seguridad específica del solicitante debe permitir llamadas COM salientes del solicitante a estos otros procesos.</span><span class="sxs-lookup"><span data-stu-id="c4472-108">The requester-specific security settings must allow outgoing COM calls from the requester to these other processes.</span></span>

<span data-ttu-id="c4472-109">El mecanismo más sencillo para administrar los problemas de seguridad de un solicitante implica la selección correcta de la cuenta de usuario en la que se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="c4472-109">The simplest mechanism for managing a requester's security issues involves proper selection of the user account under which it runs.</span></span>

<span data-ttu-id="c4472-110">Normalmente, los solicitantes deben ejecutarse en un usuario que sea miembro del grupo administradores o del grupo operadores de copia de seguridad, o bien ejecutarse como la cuenta del sistema local.</span><span class="sxs-lookup"><span data-stu-id="c4472-110">A requester typically needs to run under a user that is a member of either the Administrators group or the Backup Operators group, or run as the Local System account.</span></span>

<span data-ttu-id="c4472-111">De forma predeterminada, cuando un solicitante actúa como cliente COM, si no se ejecuta en estas cuentas, cualquier llamada COM se rechaza automáticamente con **E \_ ACCESSDENIED**, sin necesidad de llegar a la implementación del método com.</span><span class="sxs-lookup"><span data-stu-id="c4472-111">By default, when a requester is acting as a COM client, if it does not run under these accounts, any COM call is automatically rejected with **E\_ACCESSDENIED**, without even getting to the COM method implementation.</span></span>

## <a name="disabling-com-exception-handling"></a><span data-ttu-id="c4472-112">Deshabilitar el control de excepciones COM</span><span class="sxs-lookup"><span data-stu-id="c4472-112">Disabling COM Exception Handling</span></span>

<span data-ttu-id="c4472-113">Al desarrollar un solicitante, establezca la marca de opciones de COMGLB de donot de la \_ excepción \_ de control de excepciones de com \_ para deshabilitar el control de excepciones com.</span><span class="sxs-lookup"><span data-stu-id="c4472-113">When developing a requester, set the COM COMGLB\_EXCEPTION\_DONOT\_HANDLE global options flag to disable COM exception handling.</span></span> <span data-ttu-id="c4472-114">Es importante hacerlo porque el control de excepciones COM puede enmascarar errores irrecuperables en una aplicación de VSS.</span><span class="sxs-lookup"><span data-stu-id="c4472-114">It is important to do this because COM exception handling can mask fatal errors in a VSS application.</span></span> <span data-ttu-id="c4472-115">El error que se enmascara puede dejar el proceso en un estado inestable e impredecible, lo que puede provocar daños y bloqueos.</span><span class="sxs-lookup"><span data-stu-id="c4472-115">The error that is masked can leave the process in an unstable and unpredictable state, which can lead to corruptions and hangs.</span></span> <span data-ttu-id="c4472-116">Para obtener más información acerca de esta marca, vea [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span><span class="sxs-lookup"><span data-stu-id="c4472-116">For more information about this flag, see [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span></span>

## <a name="setting-requester-default-com-access-check-permission"></a><span data-ttu-id="c4472-117">Estableciendo el permiso de comprobación de acceso COM predeterminado del solicitante</span><span class="sxs-lookup"><span data-stu-id="c4472-117">Setting Requester Default COM Access Check Permission</span></span>

<span data-ttu-id="c4472-118">Los solicitantes deben tener en cuenta que cuando su proceso actúa como servidor (por ejemplo, permitir que los escritores modifiquen el documento de componentes de copia de seguridad), deben permitir las llamadas entrantes de otros participantes de VSS, como escritores o el servicio VSS.</span><span class="sxs-lookup"><span data-stu-id="c4472-118">Requesters need to be aware that when their process acts as a server (for example, allowing writers to modify the Backup Components Document), they must allow incoming calls from other VSS participants, such as writers or the VSS service.</span></span>

<span data-ttu-id="c4472-119">Sin embargo, de forma predeterminada, un proceso de Windows solo permitirá clientes COM que se ejecuten en la misma sesión de inicio de sesión (el propio SID) o se ejecuten en la cuenta de sistema local.</span><span class="sxs-lookup"><span data-stu-id="c4472-119">However, by default, a Windows process will allow only COM clients that are running under the same logon session (the SELF SID) or running under the Local System account.</span></span> <span data-ttu-id="c4472-120">Este es un posible problema porque estos valores predeterminados no son adecuados para la infraestructura de VSS.</span><span class="sxs-lookup"><span data-stu-id="c4472-120">This is a potential problem because these defaults are not adequate for the VSS infrastructure.</span></span> <span data-ttu-id="c4472-121">Por ejemplo, los escritores pueden ejecutarse como una cuenta de usuario de "operador de copia de seguridad" que no está en la misma sesión de inicio de sesión que el proceso solicitante ni una cuenta de sistema local.</span><span class="sxs-lookup"><span data-stu-id="c4472-121">For example, writers might run as a "Backup Operator" user account that is neither in the same logon session as the requester process nor a Local System account.</span></span>

<span data-ttu-id="c4472-122">Para controlar este tipo de problema, cada proceso de servidor COM puede ejercer un mayor control sobre si un cliente RPC o COM tiene permiso para realizar un método COM implementado por el servidor (un solicitante en este caso) mediante [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer un "permiso de comprobación de acceso com predeterminado" para todo el proceso.</span><span class="sxs-lookup"><span data-stu-id="c4472-122">To handle this type of problem, every COM server process can exercise further control over whether an RPC or COM client is allowed to perform a COM method implemented by the server (a requester in this case) by using [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set a process-wide "Default COM Access Check Permission".</span></span>

<span data-ttu-id="c4472-123">Los solicitantes pueden hacer lo siguiente explícitamente:</span><span class="sxs-lookup"><span data-stu-id="c4472-123">Requesters can explicitly do the following:</span></span>

-   <span data-ttu-id="c4472-124">Permitir el acceso de todos los procesos para llamar al proceso del solicitante.</span><span class="sxs-lookup"><span data-stu-id="c4472-124">Allow all processes access to call into the requester process.</span></span>

    <span data-ttu-id="c4472-125">Esta opción puede ser adecuada para la mayoría de los solicitantes y se usa en otros servidores COM; por ejemplo, todos los servicios de Windows basados en SVCHOST ya usan esta opción, al igual que todos los servicios COM+ de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c4472-125">This option may be adequate for the vast majority of requesters, and is used by other COM servers—for example, all SVCHOST-based Windows services are already using this option, as are all COM+ Services by default.</span></span>

    <span data-ttu-id="c4472-126">Permitir que todos los procesos realicen llamadas COM entrantes no es necesariamente un punto débil de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c4472-126">Allowing all processes to perform incoming COM calls is not necessarily a security weakness.</span></span> <span data-ttu-id="c4472-127">Un solicitante que actúa como un servidor COM, al igual que todos los demás servidores COM, conserva siempre la opción de autorizar a sus clientes en cada método COM implementado en su proceso.</span><span class="sxs-lookup"><span data-stu-id="c4472-127">A requester acting as a COM server, like all other COM servers, always retains the option to authorize its clients on every COM method implemented in its process.</span></span>

    <span data-ttu-id="c4472-128">Tenga en cuenta que las devoluciones de llamada COM internas implementadas por VSS están protegidas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c4472-128">Note that internal COM callbacks implemented by VSS are secured by default.</span></span>

    <span data-ttu-id="c4472-129">Para permitir que todos los procesos tengan acceso COM a un solicitante, puede pasar un descriptor de seguridad **nulo** como primer parámetro de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="c4472-129">To allow all processes COM access to a requester, you can pass a **NULL** security descriptor as the first parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="c4472-130">(Tenga en cuenta que se debe llamar a **CoInitializeSecurity** como máximo una vez para todo el proceso.</span><span class="sxs-lookup"><span data-stu-id="c4472-130">(Note that **CoInitializeSecurity** must be called at most once for the entire process.</span></span> <span data-ttu-id="c4472-131">Consulte la documentación de COM o MSDN para obtener más información sobre las llamadas a **CoInitializeSecurity** ).</span><span class="sxs-lookup"><span data-stu-id="c4472-131">Please see the COM documentation or MSDN for more information on **CoInitializeSecurity** calls.)</span></span>

    <span data-ttu-id="c4472-132">En el ejemplo de código siguiente se muestra cómo un solicitante debe llamar a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) en Windows 8 y windows Server 2012 y versiones posteriores, para que sea compatible con VSS para recursos compartidos de archivos remotos (RVSS):</span><span class="sxs-lookup"><span data-stu-id="c4472-132">The following code example shows how a requester should call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 8 and Windows Server 2012 and later, in order to be compatible with VSS for remote file shares (RVSS):</span></span>

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IMPERSONATE,   //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_STATIC,                   //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    <span data-ttu-id="c4472-133">Cuando se establece explícitamente la seguridad de nivel COM del solicitante con [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c4472-133">When explicitly setting a requester's COM level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="c4472-134">Establezca el nivel de autenticación en al **menos \_ \_ \_ \_ \_ integridad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="c4472-134">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**.</span></span> <span data-ttu-id="c4472-135">Para mejorar la seguridad, considere el uso de la **\_ \_ \_ \_ \_ privacidad de nivel de autenticación de RPC C**.</span><span class="sxs-lookup"><span data-stu-id="c4472-135">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>
    -   <span data-ttu-id="c4472-136">Establezca el nivel de suplantación en la **\_ \_ \_ \_ suplantación de nivel Imp de RPC C**.</span><span class="sxs-lookup"><span data-stu-id="c4472-136">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IMPERSONATE**.</span></span>
    -   <span data-ttu-id="c4472-137">Establezca las capacidades de seguridad de ocultación en **EOAC \_ static**.</span><span class="sxs-lookup"><span data-stu-id="c4472-137">Set the cloaking security capabilities to **EOAC\_STATIC**.</span></span> <span data-ttu-id="c4472-138">Para obtener más información acerca de la ocultación de la seguridad, consulte [Cloaking](../com/cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="c4472-138">For more information about cloaking security, see [Cloaking](../com/cloaking.md).</span></span>

    <span data-ttu-id="c4472-139">En el ejemplo de código siguiente se muestra cómo un solicitante debe llamar a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) en Windows 7 y windows Server 2008 R2 y versiones anteriores (o en Windows 8 y windows Server 2012 y versiones posteriores, si no es necesaria la compatibilidad con RVSS):</span><span class="sxs-lookup"><span data-stu-id="c4472-139">The following code example shows how a requester should call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 7 and Windows Server 2008 R2 and earlier (or in Windows 8 and Windows Server 2012 and later, if RVSS compatibility is not needed):</span></span>

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IDENTIFY,      //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_NONE,                     //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    <span data-ttu-id="c4472-140">Cuando se establece explícitamente la seguridad de nivel COM del solicitante con [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c4472-140">When explicitly setting a requester's COM level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="c4472-141">Establezca el nivel de autenticación en al menos el nivel de autenticación de **RPC \_ C \_ \_ \_ Connecta**.</span><span class="sxs-lookup"><span data-stu-id="c4472-141">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_CONNECT**.</span></span> <span data-ttu-id="c4472-142">Para mejorar la seguridad, considere el uso de la **\_ \_ \_ \_ \_ privacidad de nivel de autenticación de RPC C**.</span><span class="sxs-lookup"><span data-stu-id="c4472-142">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>
    -   <span data-ttu-id="c4472-143">Establezca el nivel de suplantación **en \_ \_ nivel IMP \_ \_ de RPC C** , a menos que el proceso del solicitante tenga que permitir la suplantación para llamadas RPC o com específicas que no están relacionadas con VSS.</span><span class="sxs-lookup"><span data-stu-id="c4472-143">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IDENTIFY** unless the requester process needs to allow impersonation for specific RPC or COM calls that are unrelated to VSS.</span></span>

-   <span data-ttu-id="c4472-144">Permitir solo el acceso a los procesos especificados para llamar al proceso del solicitante.</span><span class="sxs-lookup"><span data-stu-id="c4472-144">Allow only specified processes access to call into the requester process.</span></span>

    <span data-ttu-id="c4472-145">Un servidor COM (como un solicitante) que llama a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) con un descriptor de seguridad que no **es null** como primer parámetro puede usar el descriptor para configurarlo de modo que acepte las llamadas entrantes solo de los usuarios que pertenecen a un conjunto específico de cuentas.</span><span class="sxs-lookup"><span data-stu-id="c4472-145">A COM server (such as a requester) that is calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) with a non-**NULL** security descriptor as the first parameter can use the descriptor to configure itself to accept incoming calls only from users that belong to a specific set of accounts.</span></span>

    <span data-ttu-id="c4472-146">Un solicitante debe asegurarse de que los clientes COM que se ejecutan en usuarios válidos estén autorizados para llamar a su proceso.</span><span class="sxs-lookup"><span data-stu-id="c4472-146">A requester must ensure that COM clients running under valid users are authorized to call into its process.</span></span> <span data-ttu-id="c4472-147">Un solicitante que especifica un descriptor de seguridad en el primer parámetro debe permitir que los siguientes usuarios realicen llamadas entrantes en el proceso del solicitante:</span><span class="sxs-lookup"><span data-stu-id="c4472-147">A requester that specifies a Security Descriptor in the first parameter must allow the following users to perform incoming calls into the requester process:</span></span>

    -   <span data-ttu-id="c4472-148">Sistema local</span><span class="sxs-lookup"><span data-stu-id="c4472-148">Local System</span></span>
    -   <span data-ttu-id="c4472-149">Servicio local</span><span class="sxs-lookup"><span data-stu-id="c4472-149">Local Service</span></span>

        <span data-ttu-id="c4472-150">**Windows XP:** Este valor no se admite hasta Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c4472-150">**Windows XP:** This value is not supported until Windows Server 2003.</span></span>

    -   <span data-ttu-id="c4472-151">Servicio de red</span><span class="sxs-lookup"><span data-stu-id="c4472-151">Network Service</span></span>

        <span data-ttu-id="c4472-152">**Windows XP:** Este valor no se admite hasta Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c4472-152">**Windows XP:** This value is not supported until Windows Server 2003.</span></span>

    -   <span data-ttu-id="c4472-153">Miembros del grupo local Administradores</span><span class="sxs-lookup"><span data-stu-id="c4472-153">Members of the local Administrators group</span></span>
    -   <span data-ttu-id="c4472-154">Miembros del grupo operadores de copia de seguridad local</span><span class="sxs-lookup"><span data-stu-id="c4472-154">Members of the local Backup Operators group</span></span>
    -   <span data-ttu-id="c4472-155">Usuarios especiales que se especifican en la ubicación del Registro siguiente, con "1" como \_ valor de REG DWORD</span><span class="sxs-lookup"><span data-stu-id="c4472-155">Special users that are specified in the registry location below, with "1" as their REG\_DWORD value</span></span>

## <a name="explicitly-controlling-user-account-access-to-a-requester"></a><span data-ttu-id="c4472-156">Controlar explícitamente el acceso de la cuenta de usuario a un solicitante</span><span class="sxs-lookup"><span data-stu-id="c4472-156">Explicitly Controlling User Account Access to a Requester</span></span>

<span data-ttu-id="c4472-157">Hay casos en los que la restricción de acceso a un solicitante a los procesos que se ejecutan como sistema local, o en los grupos de administradores locales o operadores de copia de seguridad locales, puede ser demasiado restrictivo.</span><span class="sxs-lookup"><span data-stu-id="c4472-157">There are cases where restricting access to a requester to processes running as Local System, or under the local Administrators or local Backup Operators groups, may be too restrictive.</span></span>

<span data-ttu-id="c4472-158">Por ejemplo, un proceso de solicitante especificado podría no tener que ejecutarse normalmente en una cuenta de administrador o de operador de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c4472-158">For example, a specified requester process might not ordinarily need to be run under an Administrator or Backup Operator account.</span></span> <span data-ttu-id="c4472-159">Por motivos de seguridad, sería mejor no promover artificialmente los privilegios de los procesos para admitir VSS.</span><span class="sxs-lookup"><span data-stu-id="c4472-159">For security reasons, it would be best not to artificially promote the processes privileges to support VSS.</span></span>

<span data-ttu-id="c4472-160">En estos casos, se debe modificar la clave del registro **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** para indicar a VSS que un usuario especificado es seguro para ejecutar un solicitante de VSS.</span><span class="sxs-lookup"><span data-stu-id="c4472-160">In these cases, the **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**VSS**\\**VssAccessControl** registry key must be modified to instruct VSS that a specified user is safe to run a VSS requester.</span></span>

<span data-ttu-id="c4472-161">Bajo esta clave, debe crear una subclave con el mismo nombre que la cuenta a la que se va a conceder o denegar el acceso.</span><span class="sxs-lookup"><span data-stu-id="c4472-161">Under this key, you must create a subkey that has the same name as the account that is to be granted or denied access.</span></span> <span data-ttu-id="c4472-162">Esta subclave debe establecerse en uno de los valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c4472-162">This subkey must be set to one of the values in the following table.</span></span>

| <span data-ttu-id="c4472-163">Value</span><span class="sxs-lookup"><span data-stu-id="c4472-163">Value</span></span> | <span data-ttu-id="c4472-164">Significado</span><span class="sxs-lookup"><span data-stu-id="c4472-164">Meaning</span></span>                                             |
|-------|-----------------------------------------------------|
| <span data-ttu-id="c4472-165">0</span><span class="sxs-lookup"><span data-stu-id="c4472-165">0</span></span>     | <span data-ttu-id="c4472-166">Deniegue el acceso del usuario al escritor y al solicitante.</span><span class="sxs-lookup"><span data-stu-id="c4472-166">Deny the user access to your writer and requester.</span></span>  |
| <span data-ttu-id="c4472-167">1</span><span class="sxs-lookup"><span data-stu-id="c4472-167">1</span></span>     | <span data-ttu-id="c4472-168">Conceda al usuario acceso al escritor.</span><span class="sxs-lookup"><span data-stu-id="c4472-168">Grant the user access to your writer.</span></span>               |
| <span data-ttu-id="c4472-169">2</span><span class="sxs-lookup"><span data-stu-id="c4472-169">2</span></span>     | <span data-ttu-id="c4472-170">Conceda al usuario acceso al solicitante.</span><span class="sxs-lookup"><span data-stu-id="c4472-170">Grant the user access to your requester.</span></span>            |
| <span data-ttu-id="c4472-171">3</span><span class="sxs-lookup"><span data-stu-id="c4472-171">3</span></span>     | <span data-ttu-id="c4472-172">Conceda al usuario acceso al escritor y al solicitante.</span><span class="sxs-lookup"><span data-stu-id="c4472-172">Grant the user access to your writer and requester.</span></span> |



 

<span data-ttu-id="c4472-173">En el siguiente ejemplo se concede acceso a la cuenta "midominio mi \\ usuario":</span><span class="sxs-lookup"><span data-stu-id="c4472-173">The following example grants access to the "MyDomain\\MyUser" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 2<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="c4472-174">Este mecanismo también se puede usar para restringir explícitamente que un usuario permitido de otro modo no ejecute un solicitante de VSS.</span><span class="sxs-lookup"><span data-stu-id="c4472-174">This mechanism can also be used to explicitly restrict an otherwise permitted user from running a VSS requester.</span></span> <span data-ttu-id="c4472-175">En el siguiente ejemplo se restringirá el acceso de la cuenta de administrador de ThatDomain \\ :</span><span class="sxs-lookup"><span data-stu-id="c4472-175">The following example will restrict access from the "ThatDomain\\Administrator" account:</span></span>

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

<span data-ttu-id="c4472-176">El administrador de ThatDomain de usuario \\ no podría ejecutar un solicitante de VSS.</span><span class="sxs-lookup"><span data-stu-id="c4472-176">The user ThatDomain\\Administrator would not be able to run a VSS requester.</span></span>

## <a name="performing-a-file-backup-of-the-system-state"></a><span data-ttu-id="c4472-177">Realización de una copia de seguridad de archivos del estado del sistema</span><span class="sxs-lookup"><span data-stu-id="c4472-177">Performing a File Backup of the System State</span></span>

<span data-ttu-id="c4472-178">Si un solicitante realiza una copia de seguridad del estado del sistema mediante la copia de seguridad de archivos individuales en lugar de usar una imagen de volumen para la copia de seguridad, debe llamar a las funciones [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) y [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) para enumerar los vínculos físicos en los archivos que se encuentran en los directorios siguientes:</span><span class="sxs-lookup"><span data-stu-id="c4472-178">If a requester performs system-state backup by backing up individual files instead of using a volume image for the backup, it must call the [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) and [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) functions to enumerate hard links on files that are located in the following directories:</span></span>

-   <span data-ttu-id="c4472-179">Windows \\ system32 \\ WDI \\ perftrack</span><span class="sxs-lookup"><span data-stu-id="c4472-179">Windows\\system32\\WDI\\perftrack</span></span>\\
-   <span data-ttu-id="c4472-180">Windows \\ WINSXS</span><span class="sxs-lookup"><span data-stu-id="c4472-180">Windows\\WINSXS</span></span>\\

<span data-ttu-id="c4472-181">Solo los miembros del grupo administradores pueden tener acceso a estos directorios.</span><span class="sxs-lookup"><span data-stu-id="c4472-181">These directories can only be accessed by members of the Administrators group.</span></span> <span data-ttu-id="c4472-182">Por esta razón, este solicitante debe ejecutarse en la cuenta del sistema o en una cuenta de usuario que sea miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="c4472-182">For this reason, such a requester must run under the system account or a user account that is a member of the Administrators group.</span></span>

<span data-ttu-id="c4472-183">**Windows XP y Windows Server 2003:** Las funciones [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) y [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) no se admiten hasta Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c4472-183">**Windows XP and Windows Server 2003:** The [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) and [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) functions are not supported until Windows Vista and Windows Server 2008.</span></span>

 

 
