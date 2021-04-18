---
description: Tanto las aplicaciones de C++ como los scripts que se ejecutan con una cuenta de administrador completa pueden cambiar el descriptor de seguridad del espacio de nombres
ms.assetid: d3e56b30-d5a8-446a-89aa-645b44a75af6
ms.tgt_platform: multiple
title: Configuración de descriptores de seguridad de espacios de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877b1dfc0ae1a9467b1beb7d169bfa31fdf7395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707270"
---
# <a name="setting-namespace-security-descriptors"></a><span data-ttu-id="06551-103">Configuración de descriptores de seguridad de espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="06551-103">Setting Namespace Security Descriptors</span></span>

<span data-ttu-id="06551-104">Tanto las aplicaciones de C++ como los scripts que se ejecutan con una cuenta de administrador completa pueden cambiar el descriptor de seguridad del espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="06551-104">Both C++ applications and scripts running under a full administrator account can change a namespace security descriptor.</span></span>

## <a name="namespace-security-descriptors"></a><span data-ttu-id="06551-105">Descriptores de seguridad de espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="06551-105">Namespace Security Descriptors</span></span>

<span data-ttu-id="06551-106">Cada espacio de nombres WMI tiene un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly), que permite que cada espacio de nombres tenga una configuración de seguridad única que determine quién tiene acceso a los datos y métodos del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="06551-106">Each WMI namespace has a [*security descriptor*](/windows/desktop/SecGloss/s-gly), which allows each namespace to have unique security settings that determine who has access to the namespace data and methods.</span></span> <span data-ttu-id="06551-107">Para obtener más información sobre la seguridad de acceso de WMI, vea [acceso a objetos protegibles de WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="06551-107">For more information about WMI access security, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span> <span data-ttu-id="06551-108">El [acceso a los espacios de nombres WMI](access-to-wmi-namespaces.md) describe la configuración de seguridad predeterminada para los espacios de nombres WMI y la auditoría de seguridad en WMI.</span><span class="sxs-lookup"><span data-stu-id="06551-108">[Access to WMI Namespaces](access-to-wmi-namespaces.md) describes the default security settings for WMI namespaces and security auditing in WMI.</span></span>

<span data-ttu-id="06551-109">Puede establecer permisos de cuenta para cada espacio de nombres WMI en el repositorio WMI (CIM) de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="06551-109">You can set account permissions for each WMI namespace in the WMI (CIM) repository in the following ways:</span></span>

-   <span data-ttu-id="06551-110">Cuando el espacio de nombres se crea en el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="06551-110">When the namespace is created in the MOF file.</span></span> <span data-ttu-id="06551-111">Para obtener más información, vea [establecer la seguridad del espacio de nombres cuando se crea el espacio de nombres](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="06551-111">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>
-   <span data-ttu-id="06551-112">Manualmente, mediante el control WMI.</span><span class="sxs-lookup"><span data-stu-id="06551-112">Manually, using the WMI Control.</span></span> <span data-ttu-id="06551-113">Para obtener más información, vea [establecer la seguridad del espacio de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="06551-113">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>
-   <span data-ttu-id="06551-114">Mediante programación, llamando a los métodos de la clase [**\_ \_ SystemSecurity**](--systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="06551-114">Programmatically, by calling the methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class.</span></span>

<span data-ttu-id="06551-115">Los métodos siguientes del objeto [**\_ \_ SystemSecurity**](--systemsecurity.md) asociado a cada espacio de nombres permiten leer o cambiar la seguridad de un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="06551-115">The following methods of the [**\_\_SystemSecurity**](--systemsecurity.md) object associated with each namespace allow you to read or change security on a namespace.</span></span>

<dl> <dt>

<span data-ttu-id="06551-116"><span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)</span><span class="sxs-lookup"><span data-stu-id="06551-116"><span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)</span></span>
</dt> <dd>

<span data-ttu-id="06551-117">Establece el parámetro *Rights* como un mapa de bits con cada bit correspondiente a un derecho de acceso.</span><span class="sxs-lookup"><span data-stu-id="06551-117">Sets the *rights* parameter as a bitmap with each bit corresponding to an access right.</span></span>

</dd> <dt>

<span data-ttu-id="06551-118"><span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**Se obtiene**](--systemsecurity-getsd.md)</span><span class="sxs-lookup"><span data-stu-id="06551-118"><span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**GetSD**](--systemsecurity-getsd.md)</span></span>
</dt> <dd>

<span data-ttu-id="06551-119">Obtiene el descriptor de seguridad para el espacio de nombres al que está conectado el usuario.</span><span class="sxs-lookup"><span data-stu-id="06551-119">Gets the security descriptor for the namespace to which the user is connected.</span></span> <span data-ttu-id="06551-120">Este método devuelve un descriptor de seguridad en formato binario de matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="06551-120">This method returns a security descriptor in binary byte array format.</span></span> <span data-ttu-id="06551-121">Si está escribiendo un script, use el método [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) .</span><span class="sxs-lookup"><span data-stu-id="06551-121">If you are writing a script, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="06551-122"><span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**Establecido**](--systemsecurity-setsd.md)</span><span class="sxs-lookup"><span data-stu-id="06551-122"><span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**SetSD**](--systemsecurity-setsd.md)</span></span>
</dt> <dd>

<span data-ttu-id="06551-123">Establece el descriptor de seguridad (SD) del espacio de nombres al que está conectado un usuario.</span><span class="sxs-lookup"><span data-stu-id="06551-123">Sets the security descriptor (SD) for the namespace to which a user is connected.</span></span> <span data-ttu-id="06551-124">Este método requiere un descriptor de seguridad en formato binario de matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="06551-124">This method requires a security descriptor in binary byte array format.</span></span> <span data-ttu-id="06551-125">Si está escribiendo un script, use el método [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="06551-125">If you are writing a script, use the [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="06551-126"><span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)</span><span class="sxs-lookup"><span data-stu-id="06551-126"><span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)</span></span>
</dt> <dd>

<span data-ttu-id="06551-127">Obtiene el descriptor de seguridad que controla el acceso al espacio de nombres WMI asociado a la instancia de [**\_ \_ SystemSecurity**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="06551-127">Gets the security descriptor that controls access to the WMI namespace associated with the instance of [**\_\_SystemSecurity**](--systemsecurity.md).</span></span> <span data-ttu-id="06551-128">El descriptor de seguridad se devuelve como una instancia de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="06551-128">The security descriptor is returned as an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span>

</dd> <dt>

<span data-ttu-id="06551-129"><span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)</span><span class="sxs-lookup"><span data-stu-id="06551-129"><span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)</span></span>
</dt> <dd>

<span data-ttu-id="06551-130">Escribe una versión actualizada del descriptor de seguridad que controla el acceso a la impresora.</span><span class="sxs-lookup"><span data-stu-id="06551-130">Writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="06551-131">El descriptor de seguridad se representa mediante una instancia de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="06551-131">The security descriptor is represented by an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span>

</dd> <dt>

<span data-ttu-id="06551-132"><span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)</span><span class="sxs-lookup"><span data-stu-id="06551-132"><span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)</span></span>
</dt> <dd>

<span data-ttu-id="06551-133">Obtiene los derechos de acceso remoto para una lista de usuarios individuales en equipos que ejecutan versiones obsoletas de Windows, donde el control de acceso a través de los descriptores de seguridad de Windows no está disponible.</span><span class="sxs-lookup"><span data-stu-id="06551-133">Gets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

</dd> <dt>

<span data-ttu-id="06551-134"><span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)</span><span class="sxs-lookup"><span data-stu-id="06551-134"><span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)</span></span>
</dt> <dd>

<span data-ttu-id="06551-135">Establece los derechos de acceso remoto para una lista de usuarios individuales en equipos que ejecutan versiones obsoletas de Windows, donde el control de acceso a través de los descriptores de seguridad de Windows no está disponible.</span><span class="sxs-lookup"><span data-stu-id="06551-135">Sets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

</dd> </dl>

<span data-ttu-id="06551-136">Si está escribiendo scripts, use [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) y [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="06551-136">If you are writing scripts, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) and [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md).</span></span> <span data-ttu-id="06551-137">Puede usar los métodos de la clase [**\_ SecurityDescriptorHelper de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) para modificar los descriptores de seguridad.</span><span class="sxs-lookup"><span data-stu-id="06551-137">You can use the methods of the [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class to alter the security descriptors.</span></span>

<span data-ttu-id="06551-138">Si está programando en C++, puede manipular el descriptor de seguridad binario mediante el [lenguaje de definición de descriptores de seguridad (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language)y los métodos de conversión [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) y [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span><span class="sxs-lookup"><span data-stu-id="06551-138">If you are programming in C++, you can manipulate the binary security descriptor using [Security Descriptor Definition Language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

<span data-ttu-id="06551-139">Tenga en cuenta que, a partir de Windows Vista, el [control de cuentas de usuario](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) (UAC) afecta al acceso a los datos WMI y a lo que se puede configurar con el [*control WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="06551-139">Be aware that, starting with Windows Vista, [User Account Control](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) (UAC) affects access to WMI data and what can be configured with the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="06551-140">Para obtener más información, vea [control de cuentas de usuario y WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="06551-140">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="06551-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06551-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06551-142">Proteger los espacios de nombres de WMI</span><span class="sxs-lookup"><span data-stu-id="06551-142">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="06551-143">Constantes de seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="06551-143">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="06551-144">Acceso a los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="06551-144">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="06551-145">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="06551-145">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
