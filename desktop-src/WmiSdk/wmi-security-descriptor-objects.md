---
description: WMI tiene objetos y métodos que le permiten leer y manipular descriptores de seguridad para determinar quién tiene acceso a los objetos protegibles.
ms.assetid: ce4b7c9e-2c16-40d4-8839-76e69ddb2d8c
ms.tgt_platform: multiple
title: Objetos de descriptor de seguridad WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc315e955c2d449d0dea0db97684cc352257cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558749"
---
# <a name="wmi-security-descriptor-objects"></a><span data-ttu-id="42e4a-103">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="42e4a-103">WMI Security Descriptor Objects</span></span>

<span data-ttu-id="42e4a-104">WMI tiene objetos y métodos que le permiten leer y manipular descriptores de seguridad para determinar quién tiene acceso a los objetos protegibles.</span><span class="sxs-lookup"><span data-stu-id="42e4a-104">WMI has objects and methods that allow you to read and manipulate security descriptors to determine who has access to securable objects.</span></span>

-   [<span data-ttu-id="42e4a-105">El rol de los descriptores de seguridad</span><span class="sxs-lookup"><span data-stu-id="42e4a-105">The Role of Security Descriptors</span></span>](#the-role-of-security-descriptors)
-   [<span data-ttu-id="42e4a-106">Objetos de seguridad de Access Control y WMI</span><span class="sxs-lookup"><span data-stu-id="42e4a-106">Access Control and WMI Security Objects</span></span>](#access-control-and-wmi-security-objects)
-   [<span data-ttu-id="42e4a-107">\_Objeto SecurityDescriptor de Win32</span><span class="sxs-lookup"><span data-stu-id="42e4a-107">Win32\_SecurityDescriptor Object</span></span>](/windows)
-   [<span data-ttu-id="42e4a-108">DACL y SACL</span><span class="sxs-lookup"><span data-stu-id="42e4a-108">DACL and SACL</span></span>](#dacl-and-sacl)
-   [<span data-ttu-id="42e4a-109">Win32 \_ ACE, \_ Administrador de confianza de Win32, SID de Win32 \_</span><span class="sxs-lookup"><span data-stu-id="42e4a-109">Win32\_ACE, Win32\_Trustee, Win32\_SID</span></span>](/windows)
-   [<span data-ttu-id="42e4a-110">Ejemplo: comprobar quién tiene acceso a las impresoras</span><span class="sxs-lookup"><span data-stu-id="42e4a-110">Example: Checking Who has Access to Printers</span></span>](#example-checking-who-has-access-to-printers)
-   [<span data-ttu-id="42e4a-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="42e4a-111">Related topics</span></span>](#related-topics)

## <a name="the-role-of-security-descriptors"></a><span data-ttu-id="42e4a-112">El rol de los descriptores de seguridad</span><span class="sxs-lookup"><span data-stu-id="42e4a-112">The Role of Security Descriptors</span></span>

<span data-ttu-id="42e4a-113">Los descriptores de seguridad definen los atributos de seguridad de los objetos protegibles, como los archivos, las claves del registro, los espacios de nombres WMI, las impresoras, los servicios o los recursos compartidos.</span><span class="sxs-lookup"><span data-stu-id="42e4a-113">Security descriptors define the security attributes of securable objects such as files, registry keys, WMI namespaces, printers, services, or shares.</span></span> <span data-ttu-id="42e4a-114">Un descriptor de seguridad contiene información sobre el propietario y el grupo primario de un objeto.</span><span class="sxs-lookup"><span data-stu-id="42e4a-114">A security descriptor contains information about the owner and primary group of an object.</span></span> <span data-ttu-id="42e4a-115">Un proveedor puede comparar el descriptor de seguridad de recursos con la identidad de un usuario solicitante y determinar si el usuario tiene el derecho a acceder al recurso que solicita un usuario.</span><span class="sxs-lookup"><span data-stu-id="42e4a-115">A provider can compare the resource security descriptor to the identity of a requesting user, and determine whether or not the user has the right to access the resource that a user is requesting.</span></span> <span data-ttu-id="42e4a-116">Para obtener más información, vea [acceso a objetos protegibles de WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="42e4a-116">For more information, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>

<span data-ttu-id="42e4a-117">Algunos métodos WMI, como se [**obtienen**](--systemsecurity-getsd.md), devuelven un descriptor de seguridad en el formato de matriz de bytes binaria.</span><span class="sxs-lookup"><span data-stu-id="42e4a-117">Some WMI methods, such as [**GetSD**](--systemsecurity-getsd.md), return a security descriptor in the binary byte array format.</span></span> <span data-ttu-id="42e4a-118">A partir de Windows Vista, use los métodos de la clase [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) para convertir un descriptor de seguridad binario en una instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), que se puede manipular más fácilmente.</span><span class="sxs-lookup"><span data-stu-id="42e4a-118">Starting with Windows Vista, use the methods of the [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class to convert a binary security descriptor to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), which can be manipulated more easily.</span></span> <span data-ttu-id="42e4a-119">Para obtener más información, consulte [cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="42e4a-119">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="access-control-and-wmi-security-objects"></a><span data-ttu-id="42e4a-120">Objetos de seguridad de Access Control y WMI</span><span class="sxs-lookup"><span data-stu-id="42e4a-120">Access Control and WMI Security Objects</span></span>

<span data-ttu-id="42e4a-121">A continuación se muestra una lista de objetos de seguridad WMI:</span><span class="sxs-lookup"><span data-stu-id="42e4a-121">The following is a list of WMI security objects:</span></span>

-   [<span data-ttu-id="42e4a-122">**SecurityDescriptor de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="42e4a-122">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
-   [<span data-ttu-id="42e4a-123">**ACE de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="42e4a-123">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
-   [<span data-ttu-id="42e4a-124">**Administrador de confianza de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="42e4a-124">**Win32\_Trustee**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
-   [<span data-ttu-id="42e4a-125">**SID de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="42e4a-125">**Win32\_SID**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-sid)

<span data-ttu-id="42e4a-126">En el diagrama siguiente se muestran las relaciones existentes entre los objetos de seguridad WMI.</span><span class="sxs-lookup"><span data-stu-id="42e4a-126">The following diagram shows the relationships among WMI security objects.</span></span>

![relaciones entre objetos de seguridad WMI](images/security-descriptor.png)

<span data-ttu-id="42e4a-128">Para obtener más información sobre el rol de seguridad de acceso, consulte [prácticas recomendadas de seguridad](/windows/desktop/SecBP/best-practices-for-the-security-apis), mantenimiento de la [seguridad de WMI](maintaining-wmi-security.md)y [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="42e4a-128">For more information about the role of access security, see [Security Best Practices](/windows/desktop/SecBP/best-practices-for-the-security-apis), [Maintaining WMI Security](maintaining-wmi-security.md), and [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

## <a name="win32_securitydescriptor-object"></a><span data-ttu-id="42e4a-129">\_Objeto SecurityDescriptor de Win32</span><span class="sxs-lookup"><span data-stu-id="42e4a-129">Win32\_SecurityDescriptor Object</span></span>

<span data-ttu-id="42e4a-130">En la tabla siguiente se enumeran las propiedades de la clase [**\_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="42e4a-130">The following table lists the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class properties.</span></span>



| <span data-ttu-id="42e4a-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="42e4a-131">Property</span></span>         | <span data-ttu-id="42e4a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="42e4a-132">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42e4a-133">**ControlFlags**</span><span class="sxs-lookup"><span data-stu-id="42e4a-133">**ControlFlags**</span></span> | <span data-ttu-id="42e4a-134">Conjunto de bits de control que califican el significado de un SD o sus miembros individuales.</span><span class="sxs-lookup"><span data-stu-id="42e4a-134">Set of control bits that qualify the meaning of an SD or its individual members.</span></span> <span data-ttu-id="42e4a-135">Para obtener más información acerca de cómo establecer los valores de bits **ControlFlags** , vea [**\_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="42e4a-135">For more information about setting the **ControlFlags** bit values, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span><br/>                                                                                                                                                                      |
| <span data-ttu-id="42e4a-136">**DACL**</span><span class="sxs-lookup"><span data-stu-id="42e4a-136">**DACL**</span></span>         | <span data-ttu-id="42e4a-137">[Lista de Access Control discrecional (ACL)](/windows/desktop/SecAuthZ/access-control-lists) de usuarios y grupos, así como sus derechos de acceso a un objeto protegido.</span><span class="sxs-lookup"><span data-stu-id="42e4a-137">[Discretionary Access Control List (ACL)](/windows/desktop/SecAuthZ/access-control-lists) of users and groups, and their access rights to a secured object.</span></span> <span data-ttu-id="42e4a-138">Esta propiedad contiene una matriz de instancias de [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) que representan [Access Control entradas](/windows/desktop/SecAuthZ/access-control-entries).</span><span class="sxs-lookup"><span data-stu-id="42e4a-138">This property contains an array of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instances that represent [Access Control Entries](/windows/desktop/SecAuthZ/access-control-entries).</span></span> <span data-ttu-id="42e4a-139">Para obtener más información, vea [crear una DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span><span class="sxs-lookup"><span data-stu-id="42e4a-139">For more information, see [Creating a DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span></span><br/> |
| <span data-ttu-id="42e4a-140">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="42e4a-140">**Group**</span></span>        | <span data-ttu-id="42e4a-141">Grupo al que pertenece este objeto protegido.</span><span class="sxs-lookup"><span data-stu-id="42e4a-141">Group to which this secured object belongs.</span></span> <span data-ttu-id="42e4a-142">Esta propiedad contiene una instancia de [**\_ Administrador de confianza de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) que contiene el nombre, el dominio y el identificador de seguridad (SID) del grupo al que pertenece el propietario.</span><span class="sxs-lookup"><span data-stu-id="42e4a-142">This property contains an instance of [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) that contains the name, domain, and security identifier (SID) of the group to which the owner belongs.</span></span><br/>                                                                                                                                                             |
| <span data-ttu-id="42e4a-143">**Propietario**</span><span class="sxs-lookup"><span data-stu-id="42e4a-143">**Owner**</span></span>        | <span data-ttu-id="42e4a-144">Propietario de este objeto protegido.</span><span class="sxs-lookup"><span data-stu-id="42e4a-144">Owner of this secured object.</span></span> <span data-ttu-id="42e4a-145">Esta propiedad contiene una instancia de [ \_ Administrador de confianza de Win32](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) que contiene el nombre, el dominio y el identificador de seguridad (SID) del propietario.</span><span class="sxs-lookup"><span data-stu-id="42e4a-145">This property contains an instance of [Win32\_Trustee](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) that contains the name, domain, and security identifier (SID) of the owner.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="42e4a-146">**SACL**</span><span class="sxs-lookup"><span data-stu-id="42e4a-146">**SACL**</span></span>         | <span data-ttu-id="42e4a-147">La [lista de Access Control del sistema (ACL)](/windows/desktop/SecAuthZ/access-control-lists) contiene una matriz de instancias [**\_ ACE de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) que representan el tipo de intentos de acceso que generan registros de auditoría para usuarios o grupos.</span><span class="sxs-lookup"><span data-stu-id="42e4a-147">[System Access Control List (ACL)](/windows/desktop/SecAuthZ/access-control-lists) contains an array of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instances that represent the type of access attempts that generate audit records for users or groups.</span></span> <span data-ttu-id="42e4a-148">Para obtener más información, vea [SACL para un nuevo objeto](/windows/desktop/SecAuthZ/sacl-for-a-new-object).</span><span class="sxs-lookup"><span data-stu-id="42e4a-148">For more information, see [SACL for a New Object](/windows/desktop/SecAuthZ/sacl-for-a-new-object).</span></span><br/>                                                                        |



 

## <a name="dacl-and-sacl"></a><span data-ttu-id="42e4a-149">DACL y SACL</span><span class="sxs-lookup"><span data-stu-id="42e4a-149">DACL and SACL</span></span>

<span data-ttu-id="42e4a-150">Las matrices de objetos [**\_ ACE de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) en la lista de control de acceso discrecional (DACL) y en la lista de control de acceso del sistema {SACL) crean un vínculo entre un usuario o un grupo y sus derechos de acceso.</span><span class="sxs-lookup"><span data-stu-id="42e4a-150">The arrays of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) objects in the discretionary access control list (DACL) and system access control list {SACL) create a link between a user or group and their access rights.</span></span>

<span data-ttu-id="42e4a-151">Cuando una propiedad DACL no contiene una entrada de control de acceso (ACE), no se conceden derechos de acceso y se deniega el acceso al objeto.</span><span class="sxs-lookup"><span data-stu-id="42e4a-151">When a DACL property does not contain an access control entry (ACE), access rights are not granted and access to the object is denied.</span></span>

> [!Note]  
> <span data-ttu-id="42e4a-152">Una DACL **null** proporciona acceso completo a todos los usuarios, lo que supone un riesgo de seguridad grave.</span><span class="sxs-lookup"><span data-stu-id="42e4a-152">A **NULL** DACL gives full access to everyone, which is a serious security risk.</span></span> <span data-ttu-id="42e4a-153">Para obtener más información, vea [crear una DACL](/windows/desktop/SecBP/creating-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="42e4a-153">For more information, see [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

 

## <a name="win32_ace-win32_trustee-win32_sid"></a><span data-ttu-id="42e4a-154">Win32 \_ ACE, \_ Administrador de confianza de Win32, SID de Win32 \_</span><span class="sxs-lookup"><span data-stu-id="42e4a-154">Win32\_ACE, Win32\_Trustee, Win32\_SID</span></span>

<span data-ttu-id="42e4a-155">Un [**objeto \_ ACE de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) contiene una instancia de la clase de [**Administrador de \_ confianza de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) que identifica un usuario o grupo, y una propiedad **AccessMask** que es una máscara de máscara, que especifica las acciones que puede realizar un usuario o un grupo.</span><span class="sxs-lookup"><span data-stu-id="42e4a-155">A [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) object contains an instance of the [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) class that identifies a user or group, and an **AccessMask** property that is a bitmask, which specifies the actions that a user or group can take.</span></span> <span data-ttu-id="42e4a-156">Por ejemplo, se puede conceder a un usuario o grupo el derecho a leer un archivo pero no escribir en él.</span><span class="sxs-lookup"><span data-stu-id="42e4a-156">For example, a user or group might be granted the right to read a file but not write to the file.</span></span> <span data-ttu-id="42e4a-157">Un **objeto \_ ACE de Win32** también contiene una ACE que indica si es o no un acceso de permiso o denegación.</span><span class="sxs-lookup"><span data-stu-id="42e4a-157">A **Win32\_ACE** object also contains an ACE that indicates whether or not it is an allow or a deny access.</span></span>

> [!Note]  
> <span data-ttu-id="42e4a-158">El orden de [**\_ ACE de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) en una DACL es importante porque las opciones permitir y denegar entrada de control de acceso (ACE) se permiten en una DACL.</span><span class="sxs-lookup"><span data-stu-id="42e4a-158">The [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) order in a DACL is important because both allow and deny access control entry (ACE) are permitted in a DACL.</span></span> <span data-ttu-id="42e4a-159">Para obtener más información, vea [orden de las ACE en una DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="42e4a-159">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

<span data-ttu-id="42e4a-160">Cada cuenta de usuario o grupo representado por [**un \_ Administrador de confianza de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) tiene un identificador de seguridad (SID) que identifica de forma única una cuenta y especifica los privilegios de acceso de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="42e4a-160">Each user account or group represented by a [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) has a security identifier (SID) that uniquely identifies an account, and specifies the access privileges of the account.</span></span> <span data-ttu-id="42e4a-161">La forma de especificar los datos de SID depende del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="42e4a-161">How you specify the SID data depends on the operating system.</span></span> <span data-ttu-id="42e4a-162">Para obtener más información, consulte [cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="42e4a-162">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="42e4a-163">En el diagrama siguiente se muestra el contenido de una instancia de [**\_ ACE de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="42e4a-163">The following diagram shows the contents of one [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instance.</span></span>

![contenido de una instancia de ACE de Win32 \-](images/win32-ace.png)

## <a name="example-checking-who-has-access-to-printers"></a><span data-ttu-id="42e4a-165">Ejemplo: comprobar quién tiene acceso a las impresoras</span><span class="sxs-lookup"><span data-stu-id="42e4a-165">Example: Checking Who has Access to Printers</span></span>

<span data-ttu-id="42e4a-166">En el ejemplo de código de VBScript siguiente se muestra cómo usar el descriptor de seguridad de la impresora.</span><span class="sxs-lookup"><span data-stu-id="42e4a-166">The following VBScript code example shows how to use the printer security descriptor.</span></span> <span data-ttu-id="42e4a-167">El script llama al método [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) en la [**clase \_ Printer de Win32**](/windows/desktop/CIMWin32Prov/win32-printer) para obtener el descriptor y, a continuación, determina si hay una lista de Access Control discrecional (DACL) presente en el descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="42e4a-167">The script calls the [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) method in the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class to obtain the descriptor then determines if there is a Discretionary Access Control List (DACL) present in the security descriptor.</span></span> <span data-ttu-id="42e4a-168">Si hay una DACL, el script obtiene la lista de entradas de Access Control (ACE) de la DACL.</span><span class="sxs-lookup"><span data-stu-id="42e4a-168">If there is a DACL, then the script obtains the list of Access Control Entries (ACE) from the DACL.</span></span> <span data-ttu-id="42e4a-169">Cada ACE se representa mediante una instancia de [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace).</span><span class="sxs-lookup"><span data-stu-id="42e4a-169">Each ACE is represented by an instance of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace).</span></span> <span data-ttu-id="42e4a-170">El script comprueba cada ACE para obtener el nombre del usuario y determinar si el usuario tiene acceso a la impresora.</span><span class="sxs-lookup"><span data-stu-id="42e4a-170">The script checks every ACE to get the name of the user and determine whether the user has access to the printer.</span></span> <span data-ttu-id="42e4a-171">El usuario se representa en mediante una instancia de [**de \_ confianza de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) incrustada en la instancia de **\_ ACE de Win32** .</span><span class="sxs-lookup"><span data-stu-id="42e4a-171">The user is represented in by an instance of [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) embedded in the **Win32\_ACE** instance.</span></span>


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        colACEs = objSD.DACL
    For Each objACE in colACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="related-topics"></a><span data-ttu-id="42e4a-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="42e4a-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42e4a-173">Cambiar la seguridad de acceso en objetos protegibles</span><span class="sxs-lookup"><span data-stu-id="42e4a-173">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> <dt>

[<span data-ttu-id="42e4a-174">Clase auxiliar de descriptor de seguridad</span><span class="sxs-lookup"><span data-stu-id="42e4a-174">Security Descriptor Helper Class</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[<span data-ttu-id="42e4a-175">Prácticas recomendadas de seguridad</span><span class="sxs-lookup"><span data-stu-id="42e4a-175">Security Best Practices</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[<span data-ttu-id="42e4a-176">Mantenimiento de la seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="42e4a-176">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="42e4a-177">Control de acceso</span><span class="sxs-lookup"><span data-stu-id="42e4a-177">Access Control</span></span>](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[<span data-ttu-id="42e4a-178">Acceso a los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="42e4a-178">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

