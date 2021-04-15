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
# <a name="security-descriptors-on-files-and-registry-keys"></a>Descriptores de seguridad en archivos y claves del registro

Active Directory interfaces de servicio (ADSI) se pueden usar para administrar y proteger los sistemas de archivos de una organización, incluida la capacidad de establecer o modificar las ACL en archivos o recursos compartidos de archivos creados por los usuarios. Las interfaces de seguridad, como [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)y [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) establecen ACL en Active Directory, Exchange, archivos, recursos compartidos de archivos o objetos de clave del registro. Antes de utilizar estas interfaces, es posible que sea necesario modificar el descriptor de seguridad si usa un formato diferente de la interfaz, o bien, si no tiene derechos de acceso a la SACL del descriptor de seguridad porque no es miembro del grupo de administradores de seguridad.

Para obtener, establecer o modificar el descriptor de seguridad, use la interfaz [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) . Esta interfaz permite recuperar un descriptor de seguridad de varios recursos en su formato original, como el formato ADSI [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), un descriptor de seguridad sin formato o una cadena hexadecimal, tal como se usa en Exchange 5,5. Cuando se recupera, puede convertirlo a otro formato, por ejemplo, de un descriptor de seguridad sin formato en **IADsSecurityDescriptor**. Después, puede volver a escribir el nuevo formato en el recurso.

Algunos de los valores de la propiedad [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) , como [**AccessMask**](iadsaccesscontrolentry-property-methods.md) y **AceFlags**, serán diferentes para los distintos tipos de objeto. Por ejemplo, un objeto Active Directory usará el miembro **de \_ \_ \_ lectura genérico secundario de ADS** de la enumeración [**ADS \_ Rights \_ enum**](/windows/win32/api/iads/ne-iads-ads_rights_enum) para la propiedad **IADsAccessControlEntry. AccessMask** , pero el derecho de acceso equivalente para un objeto de archivo es **file \_ Generic \_ Read**. No es seguro suponer que todos los valores de propiedad serán los mismos para los objetos de Active Directory y los objetos que no son de Active Directory. En la lista siguiente se muestran las propiedades de **IADsAccessControlEntry** que difieren en los objetos que no son de Active Directory y donde se pueden obtener los valores adecuados.

<dl> <dt>

<span id="AccessMask"></span><span id="accessmask"></span><span id="ACCESSMASK"></span>[**AccessMask**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Para obtener más información y una lista de los posibles valores para los objetos de recurso compartido de archivos o archivos, vea [seguridad de archivos y derechos de acceso](/windows/desktop/FileIO/file-security-and-access-rights).

Para obtener más información y una lista de los posibles valores de los objetos del registro, consulte [seguridad y derechos de acceso de la clave del registro](/windows/desktop/SysInfo/registry-key-security-and-access-rights).

</dd> <dt>

<span id="AceType"></span><span id="acetype"></span><span id="ACETYPE"></span>[**AceType**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Para obtener más información, vea el miembro **AceType** de la estructura de [**\_ encabezado ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .

</dd> <dt>

<span id="AceFlags"></span><span id="aceflags"></span><span id="ACEFLAGS"></span>[**AceFlags**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Para obtener más información, vea el miembro **AceFlags** de la estructura de [**\_ encabezado ACE**](/windows/desktop/api/winnt/ns-winnt-ace_header) .

</dd> <dt>

<span id="Flags"></span><span id="flags"></span><span id="FLAGS"></span>[**Marcas**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Contiene cero o una combinación de uno o varios de los valores siguientes de Winnt. h.

<dl> <dt>

<span id="ACE_OBJECT_TYPE_PRESENT__1_"></span><span id="ace_object_type_present__1_"></span>**ACE \_ Tipo de objeto \_ \_ presente** (1)
</dt> <dd>

[**Objecttype**](iadsaccesscontrolentry-property-methods.md) contiene un valor válido.

</dd> <dt>

<span id="ACE_INHERITED_OBJECT_TYPE_PRESENT__2_"></span><span id="ace_inherited_object_type_present__2_"></span>**ACE \_ Tipo de objeto HEREDAdo \_ \_ \_ presente** (2)
</dt> <dd>

[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md) contiene un valor válido.

</dd> </dl> </dd> <dt>

<span id="ObjectType"></span><span id="objecttype"></span><span id="OBJECTTYPE"></span>[**Tipodeobjeto**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Para obtener más información, vea el miembro **objecttype** de la [**ACE del objeto de acceso \_ denegado \_ \_**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), el [**acceso a la \_ \_ \_ ACE del objeto permitido**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)y las estructuras similares. Esta propiedad no se debe establecer ni modificar para objetos que no son de Active Directory.

</dd> <dt>

<span id="InheritedObjectType"></span><span id="inheritedobjecttype"></span><span id="INHERITEDOBJECTTYPE"></span>[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Para obtener más información, vea el miembro **InheritedObjectType** de la [**ACE del objeto de acceso \_ denegado \_ \_**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), el [**acceso a la \_ \_ \_ ACE del objeto permitido**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)y las estructuras similares. Esta propiedad no se debe establecer ni modificar para objetos que no son de Active Directory.

</dd> </dl>

Normalmente, [**IADsSecurityUtility. GetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-getsecuritydescriptor) recuperará todas las partes del descriptor de seguridad, como propietario, grupo, SACL o DACL. De forma similar, [**IADsSecurityUtility. SetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-setsecuritydescriptor) sobrescribirá todas las partes del descriptor de seguridad de forma predeterminada. Puede usar la propiedad [**IADsSecurityUtility. SecurityMask**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-get_securitymask) para especificar partes individuales del descriptor de seguridad que se van a recuperar o establecer. Por ejemplo, puede establecer **SecurityMask** en la [**\_ DACL de \_ información \_ de seguridad de ADS**](/windows/win32/api/iads/ne-iads-ads_security_info_enum) antes de llamar a **GetSecurityDescriptor** para recuperar solo la DACL sin recuperar las otras partes del descriptor de seguridad.

Para obtener más información y un ejemplo de código que usa la interfaz [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) para agregar una ACE a un archivo, consulte el [código de ejemplo para agregar una ACE a un archivo](example-code-for-adding-an-ace-to-a-file.md).

En el ejemplo de código siguiente se proporcionan los identificadores constantes para los objetos de archivo, recurso compartido de archivos y registro para las propiedades [**AccessMask**](iadsaccesscontrolentry-property-methods.md), **AceType**, **AceFlags** y **Flags** para su uso con Visual Basic y Microsoft Visual Basic Scripting Edition.


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



 

 