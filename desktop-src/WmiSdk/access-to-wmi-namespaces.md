---
description: WMI usa un descriptor de seguridad de Windows estándar para controlar el acceso a los espacios de nombres de WMI.
ms.assetid: 5cf9886c-04fa-480e-889f-b64a6a70d053
ms.tgt_platform: multiple
title: Acceso a los espacios de nombres WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eaebe5370e97dcb42ddcf79018015ceff9147f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002835"
---
# <a name="access-to-wmi-namespaces"></a><span data-ttu-id="5384c-103">Acceso a los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="5384c-103">Access to WMI Namespaces</span></span>

<span data-ttu-id="5384c-104">WMI usa un *descriptor de seguridad* de Windows estándar para controlar el acceso a los espacios de nombres de WMI.</span><span class="sxs-lookup"><span data-stu-id="5384c-104">WMI uses a standard Windows *security descriptor* to control access to WMI namespaces.</span></span> <span data-ttu-id="5384c-105">Cuando se conecta a WMI, mediante el moniker de WMI "winmgmts" o una llamada a [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) o [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md), se conecta a un espacio de nombres específico.</span><span class="sxs-lookup"><span data-stu-id="5384c-105">When you connect to WMI, either through the WMI "winmgmts" moniker or a call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) or [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), you connect to a specific namespace.</span></span>

<span data-ttu-id="5384c-106">En este tema se describe la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="5384c-106">The following information is discussed in this topic:</span></span>

-   [<span data-ttu-id="5384c-107">Seguridad del espacio de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="5384c-107">WMI Namespace Security</span></span>](#wmi-namespace-security)
-   [<span data-ttu-id="5384c-108">Auditoría de espacio de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="5384c-108">WMI Namespace Auditing</span></span>](#wmi-namespace-auditing)
-   [<span data-ttu-id="5384c-109">Tipos de eventos de espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5384c-109">Types of Namespace Events</span></span>](#types-of-namespace-events)
-   [<span data-ttu-id="5384c-110">Configuración de acceso a espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="5384c-110">Namespace Access Settings</span></span>](#namespace-access-settings)
-   [<span data-ttu-id="5384c-111">Permisos predeterminados en espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="5384c-111">Default Permissions on WMI Namespaces</span></span>](#default-permissions-on-wmi-namespaces)
-   [<span data-ttu-id="5384c-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5384c-112">Related topics</span></span>](#related-topics)

## <a name="wmi-namespace-security"></a><span data-ttu-id="5384c-113">Seguridad del espacio de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="5384c-113">WMI Namespace Security</span></span>

<span data-ttu-id="5384c-114">WMI mantiene la seguridad del espacio de nombres mediante la comparación del [*token de acceso*](/windows/desktop/SecGloss/a-gly) del usuario que se conecta al espacio de nombres con el [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="5384c-114">WMI maintains namespace security by comparing the [*access token*](/windows/desktop/SecGloss/a-gly) of the user connecting to the namespace with the [*security descriptor*](/windows/desktop/SecGloss/s-gly) of the namespace.</span></span> <span data-ttu-id="5384c-115">Para obtener más información sobre la seguridad de Windows, consulte [acceso a objetos protegibles de WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5384c-115">For more information about Windows security, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>

<span data-ttu-id="5384c-116">Tenga en cuenta que, a partir de Windows Vista, el [control de cuentas de usuario (UAC)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) afecta al acceso a los datos WMI y a lo que se puede configurar con el [*control WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="5384c-116">Be aware that, starting with Windows Vista, [User Account Control (UAC)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) affects access to WMI data and what can be configured with the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="5384c-117">Para obtener más información, vea [permisos predeterminados en espacios de nombres WMI](#default-permissions-on-wmi-namespaces) y [control de cuentas de usuario y WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="5384c-117">For more information, see [Default Permissions on WMI Namespaces](#default-permissions-on-wmi-namespaces) and [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="5384c-118">El acceso a los espacios de nombres WMI también se ve afectado cuando la conexión procede de un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="5384c-118">Access to WMI namespaces is also affected when the connection is from a remote computer.</span></span> <span data-ttu-id="5384c-119">Para obtener más información, vea [conectarse a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md), [proteger una conexión WMI remota](securing-a-remote-wmi-connection.md)y [conectarse a través de Firewall de Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span><span class="sxs-lookup"><span data-stu-id="5384c-119">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md), [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md), and [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span>

<span data-ttu-id="5384c-120">Los proveedores deben basarse en la configuración de suplantación de la conexión para determinar si la aplicación o el script de cliente deben recibir los datos.</span><span class="sxs-lookup"><span data-stu-id="5384c-120">Providers must rely on the impersonation setting for the connection to determine if the client script or application should receive data.</span></span> <span data-ttu-id="5384c-121">Para obtener más información sobre los scripts y las aplicaciones cliente, vea [establecer la seguridad de procesos de aplicación cliente](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="5384c-121">For more information about script and client applications, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="5384c-122">Para obtener más información sobre la suplantación de [*proveedores*](gloss-p.md) , vea [desarrollar un proveedor WMI](developing-a-wmi-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5384c-122">For more information about [*provider*](gloss-p.md) impersonation, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

## <a name="wmi-namespace-auditing"></a><span data-ttu-id="5384c-123">Auditoría de espacio de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="5384c-123">WMI Namespace Auditing</span></span>

<span data-ttu-id="5384c-124">WMI usa las [*listas de control de acceso de sistema (SACL) del*](/windows/desktop/SecGloss/s-gly) espacio de nombres para auditar la actividad del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="5384c-124">WMI uses the namespace [*System access control lists (SACL)*](/windows/desktop/SecGloss/s-gly) to audit namespace activity.</span></span> <span data-ttu-id="5384c-125">Para habilitar la auditoría de espacios de nombres de WMI, utilice la pestaña **seguridad** del [*control WMI*](gloss-w.md) para cambiar la configuración de auditoría del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="5384c-125">To enable auditing of WMI namespaces, use the **Security** tab on the [*WMI Control*](gloss-w.md) to change the auditing settings for the namespace.</span></span>

<span data-ttu-id="5384c-126">La auditoría no se habilita durante la instalación del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5384c-126">Auditing is not enabled during the installation of the operating system.</span></span> <span data-ttu-id="5384c-127">Para habilitar la auditoría, haga clic en la pestaña **Auditoría** de la ventana **seguridad** estándar.</span><span class="sxs-lookup"><span data-stu-id="5384c-127">To enable auditing, click the **Auditing** tab in the standard **Security** window.</span></span> <span data-ttu-id="5384c-128">Después, puede Agregar una entrada de auditoría.</span><span class="sxs-lookup"><span data-stu-id="5384c-128">Then you can add an auditing entry.</span></span>

<span data-ttu-id="5384c-129">Directiva de grupo para el equipo local debe estar establecido en permitir auditoría.</span><span class="sxs-lookup"><span data-stu-id="5384c-129">Group Policy for the local computer must be set to allow auditing.</span></span> <span data-ttu-id="5384c-130">Puede habilitar la auditoría ejecutando el complemento de MMC gpedit. msc y estableciendo **auditar el acceso a objetos** en **configuración del equipo** configuración de  >  **Windows**  >  **configuración de seguridad**  >  **Directivas locales**  >  **Directiva de auditoría**.</span><span class="sxs-lookup"><span data-stu-id="5384c-130">You can enable auditing by running the Gpedit.msc MMC snap-in and setting **Audit Object Access** under **Computer Configuration** > **Windows Settings** > **Security Settings** > **Local Policies** > **Audit Policy**.</span></span>

<span data-ttu-id="5384c-131">Una entrada de auditoría edita la SACL del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="5384c-131">An auditing entry edits the SACL of the namespace.</span></span> <span data-ttu-id="5384c-132">Cuando se agrega una entrada de auditoría, se trata de un usuario, un grupo, un equipo o una entidad de seguridad integrada.</span><span class="sxs-lookup"><span data-stu-id="5384c-132">When you add an auditing entry, it is either a user, group, computer, or built-in security principal.</span></span> <span data-ttu-id="5384c-133">Después de agregar la entrada, puede establecer las operaciones de acceso que dan como resultado eventos del registro de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5384c-133">After adding the entry, you can set the access operations that result in Security Log events.</span></span> <span data-ttu-id="5384c-134">Por ejemplo, para el grupo usuarios autenticados, puede hacer clic en ejecutar métodos.</span><span class="sxs-lookup"><span data-stu-id="5384c-134">For example, for the group Authenticated Users, you can click Execute Methods.</span></span> <span data-ttu-id="5384c-135">Esta configuración produce eventos de registro de seguridad cada vez que un miembro del grupo usuarios autenticados ejecuta un método en dicho espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="5384c-135">This setting results in Security Log events whenever a member of the Authenticated Users group executes a method in that namespace.</span></span> <span data-ttu-id="5384c-136">El ID. de evento de los eventos WMI es 4662.</span><span class="sxs-lookup"><span data-stu-id="5384c-136">The Event ID for WMI events is 4662.</span></span>

<span data-ttu-id="5384c-137">La cuenta debe estar en el grupo administradores y ejecutarse con privilegios elevados para cambiar la configuración de auditoría.</span><span class="sxs-lookup"><span data-stu-id="5384c-137">Your account must be in the Administrators group and running under elevated privilege to change the auditing settings.</span></span> <span data-ttu-id="5384c-138">La cuenta predefinida Administrador también puede cambiar la seguridad o la auditoría de un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="5384c-138">The built-in Administrator account can also change the security or auditing for a namespace.</span></span> <span data-ttu-id="5384c-139">Para obtener más información acerca de la ejecución en modo elevado, vea [control de cuentas de usuario y WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="5384c-139">For more information about running in elevated mode, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="5384c-140">La auditoría de WMI genera eventos de éxito o error para los intentos de acceso a espacios de nombres WMI.</span><span class="sxs-lookup"><span data-stu-id="5384c-140">WMI auditing generates success or failure events for attempts to access WMI namespaces.</span></span> <span data-ttu-id="5384c-141">El servicio no audita si las operaciones del proveedor se han realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="5384c-141">The service does not audit the success or failure of provider operations.</span></span> <span data-ttu-id="5384c-142">Por ejemplo, cuando un script se conecta a WMI y a un espacio de nombres, puede producirse un error porque la cuenta con la que se está ejecutando el script no tiene acceso al espacio de nombres o puede intentar una operación, como editar la DACL, que no se concede.</span><span class="sxs-lookup"><span data-stu-id="5384c-142">For example, when a script connects to WMI and a namespace, it may fail because the account under which the script is running does not have access to that the namespace or may attempt an operation, such as editing the DACL, that is not granted.</span></span>

<span data-ttu-id="5384c-143">Si está ejecutando en una cuenta del grupo administradores, puede ver los eventos de auditoría de espacio de nombres en la interfaz de usuario de **visor de eventos** .</span><span class="sxs-lookup"><span data-stu-id="5384c-143">If you are running under an account in the Administrators group, you can view the namespace auditing events in the **Event Viewer** user interface.</span></span>

## <a name="types-of-namespace-events"></a><span data-ttu-id="5384c-144">Tipos de eventos de espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5384c-144">Types of Namespace Events</span></span>

<span data-ttu-id="5384c-145">WMI realiza un seguimiento de los siguientes tipos de eventos en el registro de eventos de seguridad:</span><span class="sxs-lookup"><span data-stu-id="5384c-145">WMI traces the following types of events in the Security Event Log:</span></span>

-   <span data-ttu-id="5384c-146">Auditoría correcta</span><span class="sxs-lookup"><span data-stu-id="5384c-146">Audit Success</span></span>

    <span data-ttu-id="5384c-147">La operación debe completar correctamente dos pasos para una auditoría correcta.</span><span class="sxs-lookup"><span data-stu-id="5384c-147">The operation must successfully complete two steps for an Audit Success.</span></span> <span data-ttu-id="5384c-148">En primer lugar, WMI concede acceso a la aplicación cliente o script según el SID del cliente y la DACL del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="5384c-148">First, WMI grants access to the client application or script based on the client SID and the namespace DACL.</span></span> <span data-ttu-id="5384c-149">En segundo lugar, la operación solicitada coincide con los derechos de acceso en la SACL del espacio de nombres para ese usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="5384c-149">Second, the requested operation matches the access rights in the namespace SACL for that user or group.</span></span>

-   <span data-ttu-id="5384c-150">Error de auditoría</span><span class="sxs-lookup"><span data-stu-id="5384c-150">Audit Failure</span></span>

    <span data-ttu-id="5384c-151">WMI deniega el acceso al espacio de nombres, pero la operación solicitada coincide con los derechos de acceso de la SACL del espacio de nombres de ese usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="5384c-151">WMI denies access to the namespace, but the requested operation matches the access rights in the namespace SACL for that user or group.</span></span>

## <a name="namespace-access-settings"></a><span data-ttu-id="5384c-152">Configuración de acceso a espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="5384c-152">Namespace Access Settings</span></span>

<span data-ttu-id="5384c-153">Puede ver los derechos de acceso del espacio de nombres de varias cuentas en el control WMI.</span><span class="sxs-lookup"><span data-stu-id="5384c-153">You can view the namespace access rights for various accounts on the WMI Control.</span></span> <span data-ttu-id="5384c-154">Estas constantes se describen en [**constantes de derechos de acceso de espacio de nombres**](namespace-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5384c-154">These constants are described in [**Namespace Access Rights Constants**](namespace-access-rights-constants.md).</span></span> <span data-ttu-id="5384c-155">Puede cambiar el acceso a un espacio de nombres WMI mediante el control WMI o mediante programación.</span><span class="sxs-lookup"><span data-stu-id="5384c-155">You can change the access to a WMI namespace using the WMI Control or programmatically.</span></span> <span data-ttu-id="5384c-156">Para obtener más información, consulte [cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5384c-156">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="5384c-157">WMI audita los cambios en todos los permisos de acceso que se muestran en la lista siguiente, salvo el permiso Remote enable.</span><span class="sxs-lookup"><span data-stu-id="5384c-157">WMI audits changes in all of the access permissions listed in the following list except for the Remote Enable permission.</span></span> <span data-ttu-id="5384c-158">Los cambios se registran como auditoría de éxito o error correspondiente al permiso editar seguridad.</span><span class="sxs-lookup"><span data-stu-id="5384c-158">The changes are logged as audit success or failure corresponding to the Edit Security permission.</span></span>

<dl> <dt>

<span data-ttu-id="5384c-159"><span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Ejecutar métodos</span><span class="sxs-lookup"><span data-stu-id="5384c-159"><span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Execute Methods</span></span>
</dt> <dd>

<span data-ttu-id="5384c-160">Permite al usuario ejecutar los métodos definidos en las clases WMI.</span><span class="sxs-lookup"><span data-stu-id="5384c-160">Permits the user to execute methods defined on WMI classes.</span></span> <span data-ttu-id="5384c-161">Corresponde a la constante de permiso de acceso de **\_ \_ ejecución del método WBEM** .</span><span class="sxs-lookup"><span data-stu-id="5384c-161">Corresponds to the **WBEM\_METHOD\_EXECUTE** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="5384c-162"><span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Escritura completa</span><span class="sxs-lookup"><span data-stu-id="5384c-162"><span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Full Write</span></span>
</dt> <dd>

<span data-ttu-id="5384c-163">Permite el acceso completo de lectura, escritura y eliminación a clases WMI e instancias de clase, tanto estáticas como dinámicas.</span><span class="sxs-lookup"><span data-stu-id="5384c-163">Permits full read, write, and delete access to WMI classes and class instances, both static and dynamic.</span></span> <span data-ttu-id="5384c-164">Corresponde a la constante de permiso de acceso de **\_ rellenado de \_ escritura \_ completa de WBEM** .</span><span class="sxs-lookup"><span data-stu-id="5384c-164">Corresponds to the **WBEM\_FULL\_WRITE\_REP** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="5384c-165"><span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Escritura parcial</span><span class="sxs-lookup"><span data-stu-id="5384c-165"><span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Partial Write</span></span>
</dt> <dd>

<span data-ttu-id="5384c-166">Permite el acceso de escritura a instancias de clase WMI estáticas.</span><span class="sxs-lookup"><span data-stu-id="5384c-166">Permits write access to static WMI class instances.</span></span> <span data-ttu-id="5384c-167">Corresponde a la constante de permiso de acceso de la **\_ \_ \_ representación parcial de escritura de WBEM** .</span><span class="sxs-lookup"><span data-stu-id="5384c-167">Corresponds to the **WBEM\_PARTIAL\_WRITE\_REP** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="5384c-168"><span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Escritura de proveedor</span><span class="sxs-lookup"><span data-stu-id="5384c-168"><span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Provider Write</span></span>
</dt> <dd>

<span data-ttu-id="5384c-169">Permite el acceso de escritura a instancias de clase WMI dinámicas.</span><span class="sxs-lookup"><span data-stu-id="5384c-169">Permits write access to dynamic WMI class instances.</span></span> <span data-ttu-id="5384c-170">Corresponde a la constante de permiso de acceso de **\_ \_ proveedor de escritura WBEM** .</span><span class="sxs-lookup"><span data-stu-id="5384c-170">Corresponds to the **WBEM\_WRITE\_PROVIDER** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="5384c-171"><span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Habilitar cuenta</span><span class="sxs-lookup"><span data-stu-id="5384c-171"><span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Enable Account</span></span>
</dt> <dd>

<span data-ttu-id="5384c-172">Permite el acceso de lectura a las instancias de clase WMI.</span><span class="sxs-lookup"><span data-stu-id="5384c-172">Permits read access to WMI class instances.</span></span> <span data-ttu-id="5384c-173">Corresponde a la constante de permiso **\_ Habilitar** acceso de WBEM.</span><span class="sxs-lookup"><span data-stu-id="5384c-173">Corresponds to the **WBEM\_ENABLE** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="5384c-174"><span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Habilitación remota</span><span class="sxs-lookup"><span data-stu-id="5384c-174"><span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Remote Enable</span></span>
</dt> <dd>

<span data-ttu-id="5384c-175">Permite el acceso al espacio de nombres de los equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="5384c-175">Permits access to the namespace by remote computers.</span></span> <span data-ttu-id="5384c-176">Corresponde a la constante de permiso de acceso **\_ \_ remoto de WBEM** .</span><span class="sxs-lookup"><span data-stu-id="5384c-176">Corresponds to the **WBEM\_REMOTE\_ACCESS** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="5384c-177"><span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Seguridad de lectura</span><span class="sxs-lookup"><span data-stu-id="5384c-177"><span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Read Security</span></span>
</dt> <dd>

<span data-ttu-id="5384c-178">Permite el acceso de solo lectura a la configuración de DACL.</span><span class="sxs-lookup"><span data-stu-id="5384c-178">Permits read-only access to DACL settings.</span></span> <span data-ttu-id="5384c-179">Corresponde a la constante de permiso de acceso de **\_ control de lectura** .</span><span class="sxs-lookup"><span data-stu-id="5384c-179">Corresponds to the **READ\_CONTROL** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="5384c-180"><span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Editar seguridad</span><span class="sxs-lookup"><span data-stu-id="5384c-180"><span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Edit Security</span></span>
</dt> <dd>

<span data-ttu-id="5384c-181">Permite el acceso de escritura a la configuración de DACL.</span><span class="sxs-lookup"><span data-stu-id="5384c-181">Permits write access to DACL settings.</span></span> <span data-ttu-id="5384c-182">Corresponde a la constante de permiso de acceso de **escritura de \_ DAC** .</span><span class="sxs-lookup"><span data-stu-id="5384c-182">Corresponds to the **WRITE\_DAC** access permission constant.</span></span>

</dd> </dl>

## <a name="default-permissions-on-wmi-namespaces"></a><span data-ttu-id="5384c-183">Permisos predeterminados en espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="5384c-183">Default Permissions on WMI Namespaces</span></span>

<span data-ttu-id="5384c-184">Los grupos de seguridad predeterminados son:</span><span class="sxs-lookup"><span data-stu-id="5384c-184">The default security groups are:</span></span>

-   <span data-ttu-id="5384c-185">Usuarios autenticados</span><span class="sxs-lookup"><span data-stu-id="5384c-185">Authenticated Users</span></span>
-   <span data-ttu-id="5384c-186">SERVICIO LOCAL</span><span class="sxs-lookup"><span data-stu-id="5384c-186">LOCAL SERVICE</span></span>
-   <span data-ttu-id="5384c-187">SERVICIO DE RED</span><span class="sxs-lookup"><span data-stu-id="5384c-187">NETWORK SERVICE</span></span>
-   <span data-ttu-id="5384c-188">Administradores (en el equipo local)</span><span class="sxs-lookup"><span data-stu-id="5384c-188">Administrators (on the local computer)</span></span>

<span data-ttu-id="5384c-189">Los permisos de acceso predeterminados para los usuarios autenticados, el servicio LOCAL y el servicio de red son:</span><span class="sxs-lookup"><span data-stu-id="5384c-189">The default access permissions for the Authenticated Users, LOCAL SERVICE, and NETWORK SERVICE are:</span></span>

-   <span data-ttu-id="5384c-190">Ejecutar métodos</span><span class="sxs-lookup"><span data-stu-id="5384c-190">Execute Methods</span></span>
-   <span data-ttu-id="5384c-191">Escritura completa</span><span class="sxs-lookup"><span data-stu-id="5384c-191">Full Write</span></span>
-   <span data-ttu-id="5384c-192">Habilitar cuenta</span><span class="sxs-lookup"><span data-stu-id="5384c-192">Enable Account</span></span>

<span data-ttu-id="5384c-193">Las cuentas del grupo administradores tienen todos los derechos disponibles, incluida la edición de descriptores de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5384c-193">Accounts in the Administrators group have all rights available to them, including editing security descriptors.</span></span> <span data-ttu-id="5384c-194">Sin embargo, debido a un control de cuentas de usuario (UAC), el control WMI o el script deben ejecutarse con seguridad elevada.</span><span class="sxs-lookup"><span data-stu-id="5384c-194">However, because of User Account Control (UAC), the WMI Control or the script must be running at elevated security.</span></span> <span data-ttu-id="5384c-195">Para obtener más información, vea [control de cuentas de usuario y WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="5384c-195">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="5384c-196">A veces, un script o una aplicación debe habilitar un privilegio de administrador, como **SeSecurityPrivilege**, para llevar a cabo una operación.</span><span class="sxs-lookup"><span data-stu-id="5384c-196">Sometimes a script or application must enable an administrator privilege, such as **SeSecurityPrivilege**, to carry out an operation.</span></span> <span data-ttu-id="5384c-197">Por ejemplo, un script puede ejecutar el método [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) de la [**clase \_ Printer de Win32**](/windows/desktop/CIMWin32Prov/win32-printer) sin **SeSecurityPrivilege** y obtener la información de seguridad en la lista de [*control de acceso discrecional (DACL)*](/windows/desktop/SecGloss/d-gly) del [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly)del objeto Printer.</span><span class="sxs-lookup"><span data-stu-id="5384c-197">For example, a script can execute the [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) method of the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class without **SeSecurityPrivilege** and get the security information in the [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) of the printer object [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="5384c-198">Sin embargo, la información de SACL no se devuelve al script a menos que el privilegio **SeSecurityPrivilege** esté disponible y habilitado para la cuenta.</span><span class="sxs-lookup"><span data-stu-id="5384c-198">However, the SACL information is not returned to the script unless the **SeSecurityPrivilege** privilege is available and enabled for the account.</span></span> <span data-ttu-id="5384c-199">Si la cuenta no tiene el privilegio disponible, no se puede habilitar.</span><span class="sxs-lookup"><span data-stu-id="5384c-199">If the account does not have the privilege available, then it cannot be enabled.</span></span> <span data-ttu-id="5384c-200">Para obtener más información, vea [ejecutar operaciones con privilegios](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="5384c-200">For more information, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5384c-201">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5384c-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5384c-202">Acerca de WMI</span><span class="sxs-lookup"><span data-stu-id="5384c-202">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
