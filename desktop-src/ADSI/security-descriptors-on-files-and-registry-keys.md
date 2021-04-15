---
title: Descriptores de seguridad en archivos y claves del registro
description: Active Directory interfaces de servicio (ADSI) se pueden usar para administrar y proteger los sistemas de archivos de una organización, incluida la capacidad de establecer o modificar las ACL en archivos o recursos compartidos de archivos creados por los usuarios.
ms.assetid: 7233a82f-fc38-4718-b674-4e6a00666184
ms.tgt_platform: multiple
keywords:
- Descriptores de seguridad en archivos y claves del registro ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11600a495b9a70513b9bd401777e9cdd61449ede
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488283"
---
# <a name="security-descriptors-on-files-and-registry-keys"></a><span data-ttu-id="725f2-104">Descriptores de seguridad en archivos y claves del registro</span><span class="sxs-lookup"><span data-stu-id="725f2-104">Security Descriptors on Files and Registry Keys</span></span>

<span data-ttu-id="725f2-105">Active Directory interfaces de servicio (ADSI) se pueden usar para administrar y proteger los sistemas de archivos de una organización, incluida la capacidad de establecer o modificar las ACL en archivos o recursos compartidos de archivos creados por los usuarios.</span><span class="sxs-lookup"><span data-stu-id="725f2-105">Active Directory Service Interfaces (ADSI) can be used to manage and secure file systems within an organization, including the ability to set or modify ACLs on files or file shares created by users.</span></span> <span data-ttu-id="725f2-106">Las interfaces de seguridad, como [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)y [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) establecen ACL en Active Directory, Exchange, archivos, recursos compartidos de archivos o objetos de clave del registro.</span><span class="sxs-lookup"><span data-stu-id="725f2-106">Security interfaces, such as [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist), and [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) set ACLs on Active Directory, Exchange, file, file share, or registry key objects.</span></span> <span data-ttu-id="725f2-107">Antes de utilizar estas interfaces, es posible que sea necesario modificar el descriptor de seguridad si usa un formato diferente de la interfaz, o bien, si no tiene derechos de acceso a la SACL del descriptor de seguridad porque no es miembro del grupo de administradores de seguridad.</span><span class="sxs-lookup"><span data-stu-id="725f2-107">Before using these interfaces, the security descriptor may need to be modified if it uses a different format from the interface, or if you do not have access rights to the SACL of the security descriptor because you are not a member of the security administrator group.</span></span>

<span data-ttu-id="725f2-108">Para obtener, establecer o modificar el descriptor de seguridad, use la interfaz [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) .</span><span class="sxs-lookup"><span data-stu-id="725f2-108">To get, set, or modify the security descriptor, use the [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) interface.</span></span> <span data-ttu-id="725f2-109">Esta interfaz permite recuperar un descriptor de seguridad de varios recursos en su formato original, como el formato ADSI [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), un descriptor de seguridad sin formato o una cadena hexadecimal, tal como se usa en Exchange 5,5.</span><span class="sxs-lookup"><span data-stu-id="725f2-109">This interface enables you to retrieve a security descriptor from various resources in its original format, such as the ADSI format [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), a raw security descriptor, or as a hexadecimal string as used in Exchange 5.5.</span></span> <span data-ttu-id="725f2-110">Cuando se recupera, puede convertirlo a otro formato, por ejemplo, de un descriptor de seguridad sin formato en **IADsSecurityDescriptor**.</span><span class="sxs-lookup"><span data-stu-id="725f2-110">When retrieved, you can convert it to another format, for example, from a raw security descriptor to **IADsSecurityDescriptor**.</span></span> <span data-ttu-id="725f2-111">Después, puede volver a escribir el nuevo formato en el recurso.</span><span class="sxs-lookup"><span data-stu-id="725f2-111">You can then write the new format back to the resource.</span></span>

<span data-ttu-id="725f2-112">Algunos de los valores de la propiedad [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) , como [**AccessMask**](iadsaccesscontrolentry-property-methods.md) y **AceFlags**, serán diferentes para los distintos tipos de objeto.</span><span class="sxs-lookup"><span data-stu-id="725f2-112">Some of the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) property values, such as [**AccessMask**](iadsaccesscontrolentry-property-methods.md) and **AceFlags**, will be different for different object types.</span></span> <span data-ttu-id="725f2-113">Por ejemplo, un objeto Active Directory usará el miembro **de \_ \_ \_ lectura genérico secundario de ADS** de la enumeración [**ADS \_ Rights \_ enum**](/windows/win32/api/iads/ne-iads-ads_rights_enum) para la propiedad **IADsAccessControlEntry. AccessMask** , pero el derecho de acceso equivalente para un objeto de archivo es **file \_ Generic \_ Read**.</span><span class="sxs-lookup"><span data-stu-id="725f2-113">For example, an Active Directory object will use the **ADS\_RIGHT\_GENERIC\_READ** member of the [**ADS\_RIGHTS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum) enumeration for the **IADsAccessControlEntry.AccessMask** property, but the equivalent access right for a file object is **FILE\_GENERIC\_READ**.</span></span> <span data-ttu-id="725f2-114">No es seguro suponer que todos los valores de propiedad serán los mismos para los objetos de Active Directory y los objetos que no son de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="725f2-114">It is not safe to assume that all property values will be the same for Active Directory objects and non-Active Directory objects.</span></span> <span data-ttu-id="725f2-115">En la lista siguiente se muestran las propiedades de **IADsAccessControlEntry** que difieren en los objetos que no son de Active Directory y donde se pueden obtener los valores adecuados.</span><span class="sxs-lookup"><span data-stu-id="725f2-115">The following list shows the **IADsAccessControlEntry** properties that differ for non-Active Directory objects and where the proper values can be obtained.</span></span>

<dl> <dt>

<span data-ttu-id="725f2-116"><span id="AccessMask"></span><span id="accessmask"></span><span id="ACCESSMASK"></span>[**AccessMask**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="725f2-116"><span id="AccessMask"></span><span id="accessmask"></span><span id="ACCESSMASK"></span>[**AccessMask**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="725f2-117">Para obtener más información y una lista de los posibles valores para los objetos de recurso compartido de archivos o archivos, vea [seguridad de archivos y derechos de acceso](/windows/desktop/FileIO/file-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="725f2-117">For more information and a list of possible values for file or file share objects, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights).</span></span>

<span data-ttu-id="725f2-118">Para obtener más información y una lista de los posibles valores de los objetos del registro, consulte [seguridad y derechos de acceso de la clave del registro](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="725f2-118">For more information and a list of possible values for registry objects, see [Registry Key Security and Access Rights](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span></span>

</dd> <dt>

<span data-ttu-id="725f2-119"><span id="AceType"></span><span id="acetype"></span><span id="ACETYPE"></span>[**AceType**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="725f2-119"><span id="AceType"></span><span id="acetype"></span><span id="ACETYPE"></span>[**AceType**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="725f2-120">Para obtener más información, vea el miembro **AceType** de la estructura de [**\_ encabezado ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="725f2-120">For more information, see the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

</dd> <dt>

<span data-ttu-id="725f2-121"><span id="AceFlags"></span><span id="aceflags"></span><span id="ACEFLAGS"></span>[**AceFlags**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="725f2-121"><span id="AceFlags"></span><span id="aceflags"></span><span id="ACEFLAGS"></span>[**AceFlags**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="725f2-122">Para obtener más información, vea el miembro **AceFlags** de la estructura de [**\_ encabezado ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="725f2-122">For more information, see the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

</dd> <dt>

<span data-ttu-id="725f2-123"><span id="Flags"></span><span id="flags"></span><span id="FLAGS"></span>[**Marcas**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="725f2-123"><span id="Flags"></span><span id="flags"></span><span id="FLAGS"></span>[**Flags**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="725f2-124">Contiene cero o una combinación de uno o varios de los valores siguientes de Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="725f2-124">Contains zero or a combination of one or more of the following values from WinNT.h.</span></span>

<dl> <dt>

<span data-ttu-id="725f2-125"><span id="ACE_OBJECT_TYPE_PRESENT__1_"></span><span id="ace_object_type_present__1_"></span>**ACE \_ Tipo de objeto \_ \_ presente** (1)</span><span class="sxs-lookup"><span data-stu-id="725f2-125"><span id="ACE_OBJECT_TYPE_PRESENT__1_"></span><span id="ace_object_type_present__1_"></span>**ACE\_OBJECT\_TYPE\_PRESENT** (1)</span></span>
</dt> <dd>

<span data-ttu-id="725f2-126">[**Objecttype**](iadsaccesscontrolentry-property-methods.md) contiene un valor válido.</span><span class="sxs-lookup"><span data-stu-id="725f2-126">[**ObjectType**](iadsaccesscontrolentry-property-methods.md) contains a valid value.</span></span>

</dd> <dt>

<span data-ttu-id="725f2-127"><span id="ACE_INHERITED_OBJECT_TYPE_PRESENT__2_"></span><span id="ace_inherited_object_type_present__2_"></span>**ACE \_ Tipo de objeto HEREDAdo \_ \_ \_ presente** (2)</span><span class="sxs-lookup"><span data-stu-id="725f2-127"><span id="ACE_INHERITED_OBJECT_TYPE_PRESENT__2_"></span><span id="ace_inherited_object_type_present__2_"></span>**ACE\_INHERITED\_OBJECT\_TYPE\_PRESENT** (2)</span></span>
</dt> <dd>

<span data-ttu-id="725f2-128">[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md) contiene un valor válido.</span><span class="sxs-lookup"><span data-stu-id="725f2-128">[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md) contains a valid value.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="725f2-129"><span id="ObjectType"></span><span id="objecttype"></span><span id="OBJECTTYPE"></span>[**Tipodeobjeto**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="725f2-129"><span id="ObjectType"></span><span id="objecttype"></span><span id="OBJECTTYPE"></span>[**ObjectType**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="725f2-130">Para obtener más información, vea el miembro **objecttype** de la [**ACE del objeto de acceso \_ denegado \_ \_**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), el [**acceso a la \_ \_ \_ ACE del objeto permitido**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)y las estructuras similares.</span><span class="sxs-lookup"><span data-stu-id="725f2-130">For more information, see the **ObjectType** member of the [**ACCESS\_DENIED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace), and similar structures.</span></span> <span data-ttu-id="725f2-131">Esta propiedad no se debe establecer ni modificar para objetos que no son de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="725f2-131">This property should not be set or modified for non-Active Directory objects.</span></span>

</dd> <dt>

<span data-ttu-id="725f2-132"><span id="InheritedObjectType"></span><span id="inheritedobjecttype"></span><span id="INHERITEDOBJECTTYPE"></span>[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="725f2-132"><span id="InheritedObjectType"></span><span id="inheritedobjecttype"></span><span id="INHERITEDOBJECTTYPE"></span>[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="725f2-133">Para obtener más información, vea el miembro **InheritedObjectType** de la [**ACE del objeto de acceso \_ denegado \_ \_**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), el [**acceso a la \_ \_ \_ ACE del objeto permitido**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)y las estructuras similares.</span><span class="sxs-lookup"><span data-stu-id="725f2-133">For more information, see the **InheritedObjectType** member of the [**ACCESS\_DENIED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace), and similar structures.</span></span> <span data-ttu-id="725f2-134">Esta propiedad no se debe establecer ni modificar para objetos que no son de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="725f2-134">This property should not be set or modified for non-Active Directory objects.</span></span>

</dd> </dl>

<span data-ttu-id="725f2-135">Normalmente, [**IADsSecurityUtility. GetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-getsecuritydescriptor) recuperará todas las partes del descriptor de seguridad, como propietario, grupo, SACL o DACL.</span><span class="sxs-lookup"><span data-stu-id="725f2-135">Normally, [**IADsSecurityUtility.GetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-getsecuritydescriptor) will retrieve all parts of the security descriptor, such as owner, group, SACL, or DACL.</span></span> <span data-ttu-id="725f2-136">De forma similar, [**IADsSecurityUtility. SetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-setsecuritydescriptor) sobrescribirá todas las partes del descriptor de seguridad de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="725f2-136">Similarly, [**IADsSecurityUtility.SetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-setsecuritydescriptor) will overwrite all parts of the security descriptor by default.</span></span> <span data-ttu-id="725f2-137">Puede usar la propiedad [**IADsSecurityUtility. SecurityMask**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-get_securitymask) para especificar partes individuales del descriptor de seguridad que se van a recuperar o establecer.</span><span class="sxs-lookup"><span data-stu-id="725f2-137">You can use the [**IADsSecurityUtility.SecurityMask**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-get_securitymask) property to specify individual parts of the security descriptor to retrieve or set.</span></span> <span data-ttu-id="725f2-138">Por ejemplo, puede establecer **SecurityMask** en la [**\_ DACL de \_ información \_ de seguridad de ADS**](/windows/win32/api/iads/ne-iads-ads_security_info_enum) antes de llamar a **GetSecurityDescriptor** para recuperar solo la DACL sin recuperar las otras partes del descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="725f2-138">For example, you can set **SecurityMask** to [**ADS\_SECURITY\_INFO\_DACL**](/windows/win32/api/iads/ne-iads-ads_security_info_enum) before calling **GetSecurityDescriptor** to only retrieve the DACL without retrieving the other parts of the security descriptor.</span></span>

<span data-ttu-id="725f2-139">Para obtener más información y un ejemplo de código que usa la interfaz [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) para agregar una ACE a un archivo, consulte el [código de ejemplo para agregar una ACE a un archivo](example-code-for-adding-an-ace-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="725f2-139">For more information and a code example that uses the [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) interface to add an ACE to a file, see [Example Code for Adding an ACE to a File](example-code-for-adding-an-ace-to-a-file.md).</span></span>

<span data-ttu-id="725f2-140">En el ejemplo de código siguiente se proporcionan los identificadores constantes para los objetos de archivo, recurso compartido de archivos y registro para las propiedades [**AccessMask**](iadsaccesscontrolentry-property-methods.md), **AceType**, **AceFlags** y **Flags** para su uso con Visual Basic y Microsoft Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="725f2-140">The following example code provides the constant identifiers for file, file share and registry objects for the [**AccessMask**](iadsaccesscontrolentry-property-methods.md), **AceType**, **AceFlags**, and **Flags** properties for use with Visual Basic and Microsoft Visual Basic Scripting Edition.</span></span>


```VB
' Identifiers for the IADsAccessControlEntry.AccessMask property for file,
' file share, and registry objects.
Const DELETE = &H10000
Const READ_CONTROL = &H20000
Const WRITE_DAC = &H40000
Const WRITE_OWNER = &H80000
Const SYNCHRONIZE = &H100000

Const STANDARD_RIGHTS_REQUIRED = &HF0000

Const STANDARD_RIGHTS_READ = &H20000
Const STANDARD_RIGHTS_WRITE = &H20000
Const STANDARD_RIGHTS_EXECUTE = &H20000

Const STANDARD_RIGHTS_ALL = &H1F0000

Const SPECIFIC_RIGHTS_ALL = &HFFFF

' Identifiers for the IADsAccessControlEntry.AccessMask property for file and
' file share objects.
Const FILE_READ_DATA = &H1                  '  file & pipe
Const FILE_LIST_DIRECTORY = &H1             '  directory

Const FILE_WRITE_DATA = &H2                 '  file & pipe
Const FILE_ADD_FILE = &H2                   '  directory

Const FILE_APPEND_DATA = &H4                '  file
Const FILE_ADD_SUBDIRECTORY = &H4           '  directory
Const FILE_CREATE_PIPE_INSTANCE = &H4       '  named pipe

Const FILE_READ_EA = &H8                    '  file & directory

Const FILE_WRITE_EA = &H10                  '  file & directory

Const FILE_EXECUTE = &H20                   '  file
Const FILE_TRAVERSE = &H20                  '  directory

Const FILE_DELETE_CHILD = &H40              '  directory

Const FILE_READ_ATTRIBUTES = &H80           '  all

Const FILE_WRITE_ATTRIBUTES = &H100         '  all

Const FILE_ALL_ACCESS = STANDARD_RIGHTS_REQUIRED Or SYNCHRONIZE Or &H1FF

Const FILE_GENERIC_READ = STANDARD_RIGHTS_READ Or FILE_READ_DATA Or FILE_READ_ATTRIBUTES Or _
                          FILE_READ_EA Or SYNCHRONIZE

Const FILE_GENERIC_WRITE = STANDARD_RIGHTS_WRITE Or FILE_WRITE_DATA Or FILE_WRITE_ATTRIBUTES Or _
                           FILE_WRITE_EA Or FILE_APPEND_DATA Or SYNCHRONIZE

Const FILE_GENERIC_EXECUTE = STANDARD_RIGHTS_EXECUTE Or FILE_READ_ATTRIBUTES Or FILE_EXECUTE Or SYNCHRONIZE


' Identifiers for the IADsAccessControlEntry.AccessMask property for registry
' objects.
Const KEY_QUERY_VALUE = &H1
Const KEY_SET_VALUE = &H2
Const KEY_CREATE_SUB_KEY = &H4
Const KEY_ENUMERATE_SUB_KEYS = &H8
Const KEY_NOTIFY = &H10
Const KEY_CREATE_LINK = &H20
Const KEY_WOW64_32KEY = &H200
Const KEY_WOW64_64KEY = &H100
Const KEY_WOW64_RES = &H300

Const KEY_READ = ((STANDARD_RIGHTS_READ Or KEY_QUERY_VALUE Or KEY_ENUMERATE_SUB_KEYS Or KEY_NOTIFY) And _
                  (Not SYNCHRONIZE))

Const KEY_WRITE = ((STANDARD_RIGHTS_WRITE Or KEY_SET_VALUE Or KEY_CREATE_SUB_KEY) And (Not SYNCHRONIZE))

Const KEY_EXECUTE = ((KEY_READ) And (Not SYNCHRONIZE))

Const KEY_ALL_ACCESS = ((STANDARD_RIGHTS_ALL Or KEY_QUERY_VALUE Or KEY_SET_VALUE Or KEY_CREATE_SUB_KEY Or _
                         KEY_ENUMERATE_SUB_KEYS Or KEY_NOTIFY Or KEY_CREATE_LINK) And (Not SYNCHRONIZE))
    

' Identifiers for the IADsAccessControlEntry.AceFlags property for file and
' file share objects.
Const OBJECT_INHERIT_ACE = &H1
Const CONTAINER_INHERIT_ACE = &H2
Const NO_PROPAGATE_INHERIT_ACE = &H4
Const INHERIT_ONLY_ACE = &H8
Const INHERITED_ACE = &H10
    

' Identifiers for the IADsAccessControlEntry.Flags property.
Const ACE_OBJECT_TYPE_PRESENT = 1
Const ACE_INHERITED_OBJECT_TYPE_PRESENT = 2
```



 

 