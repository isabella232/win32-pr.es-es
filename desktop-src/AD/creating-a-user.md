---
title: Creación de un usuario
description: Para crear un usuario en Active Directory Domain Services, cree un objeto de usuario en el contenedor de dominio del dominio en el que desea colocar el usuario.
ms.assetid: fb51895f-71e1-45b6-b8bc-ed674e822734
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory, crear un usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea10d0142af650d58b61967b008b207abca2c11
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103904866"
---
# <a name="creating-a-user"></a>Creación de un usuario

Para crear un usuario en Active Directory Domain Services, cree un objeto de usuario en el contenedor de dominio del dominio en el que desea colocar el usuario. Los usuarios se pueden crear en la raíz del dominio, dentro de una unidad organizativa o dentro de un contenedor.

Al crear un objeto de usuario, también debe establecer los atributos, que se enumeran en la tabla siguiente, para establecer el objeto como usuario legal reconocido por Active Directory Domain Services y el sistema de seguridad de Windows.



| Atributo                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CN**](/windows/desktop/ADSchema/a-cn)                         | Especifica el nombre del objeto de usuario en el directorio. Este será el nombre distintivo relativo (RDN) del objeto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**Atributo**](/windows/desktop/ADSchema/a-samaccountname) | Especifica una cadena que es el nombre que se usa para admitir clientes y servidores de una versión anterior de Windows. [**SamAccountName**](/windows/desktop/ADSchema/a-samaccountname) debe tener menos de 20 caracteres para admitir clientes de una versión anterior de Windows.<br/> [**SamAccountName**](/windows/desktop/ADSchema/a-samaccountname) debe ser único entre todos los objetos de entidad de seguridad del dominio. Debe realizar una consulta en el dominio para comprobar que **samAccountName** es único en el dominio.<br/> [**samAccountName**](/windows/desktop/ADSchema/a-samaccountname) es un atributo opcional. Si no se especifica ninguno, el servidor creará un valor de **samAccountName** aleatorio.<br/> |



 

También puede establecer otros atributos. Los siguientes atributos de usuario se establecen con valores predeterminados si no se establecen explícitamente en el momento de la creación.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-accountexpires"><strong>accountExpires</strong></a></td>
<td>Especifica cuándo expirará la cuenta. El valor predeterminado es <strong>TIMEQ_FOREVER</strong>, que indica que la cuenta nunca expirará.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/ADSchema/a-ntsecuritydescriptor"><strong>nTSecurityDescriptor</strong></a></td>
<td>Un descriptor de seguridad se crea en función de reglas específicas. Para obtener más información, consulte <a href="how-security-descriptors-are-set-on-new-directory-objects.md">cómo se establecen los descriptores de seguridad en los nuevos objetos de directorio</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-objectcategory"><strong>objectCategory</strong></a></td>
<td>Especifica la categoría de usuario. El valor predeterminado es &quot; Person &quot; .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/ADSchema/a-name"><strong>name</strong></a></td>
<td>Especifica el nombre de usuario. El valor predeterminado es el establecido para <a href="/windows/desktop/ADSchema/a-cn"><strong>CN</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-pwdlastset"><strong>pwdLastSet</strong></a></td>
<td>Especifica el momento en que el usuario estableció la contraseña por última vez. El valor predeterminado es cero, lo que indica que el usuario debe cambiar la contraseña en el siguiente inicio de sesión.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/ADSchema/a-useraccountcontrol"><strong>userAccountControl</strong></a></td>
<td>Contiene valores que determinan varias características de inicio de sesión y de cuenta para el usuario.<br/> De forma predeterminada, se establecen las marcas siguientes:<br/>
<ul>
<li><strong>UF_ACCOUNTDISABLE</strong> - La cuenta está deshabilitada.</li>
<li><strong>UF_PASSWD_NOTREQD</strong> - No se requiere ninguna contraseña.</li>
<li><strong>UF_NORMAL_ACCOUNT</strong> - Tipo de cuenta predeterminado que representa a un usuario típico.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-memberof"><strong>memberOf</strong></a></td>
<td>Especifica el grupo o los grupos de los que el usuario es miembro directo. El valor predeterminado es &quot; usuarios del dominio &quot; .<br/></td>
</tr>
</tbody>
</table>



 

Para crear un usuario, se enlaza al contenedor deseado y, a continuación, se usa uno de los métodos siguientes. Los atributos [**CN**](/windows/desktop/ADSchema/a-cn) y [**samAccountName**](/windows/desktop/ADSchema/a-samaccountname) se deben establecer antes de que el usuario se confirme en el servidor.



| Método                                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)                        | El atributo [**CN**](/windows/desktop/ADSchema/a-cn) se toma del parámetro *bstrRelativeName* . El nuevo usuario debe confirmarse llamando a [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) o el objeto no se creará. Para obtener más información, consulte [ejemplo de código para crear un usuario](example-code-for-creating-a-user.md).<br/>                                                                                            |
| [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) | El atributo [**CN**](/windows/desktop/ADSchema/a-cn) se toma del parámetro *pszRDNName* . El nuevo usuario se confirma cuando se llama a [**CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) . Para obtener más información, consulte [ejemplo de código para crear un usuario](example-code-for-creating-a-user.md).<br/>                                                                                                                |
| [DirectoryEntries. Add](/dotnet/api/system.directoryservices.directoryentries.add?view=dotnet-plat-ext-3.1)       | El atributo [**CN**](/windows/desktop/ADSchema/a-cn) se toma del parámetro *Name* . El nuevo objeto de usuario se debe confirmar mediante una llamada a [DirectoryEntry. commitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) o el objeto no se creará. Para obtener más información, consulte [agregar objetos de directorio](/previous-versions/ms180851(v=vs.90)).<br/> |



 

El nuevo usuario debe confirmarse en el servidor antes de que se puedan modificar los atributos que no sean [**CN**](/windows/desktop/ADSchema/a-cn) y [**samAccountName**](/windows/desktop/ADSchema/a-samaccountname) . Esto se debe a que la cuenta de usuario no existe realmente hasta que se confirma el usuario. Si se recupera o modifica un atributo para un objeto que no existe en el servidor, se producirá un error. Esto incluye llamar al método [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) . Por ejemplo, se seguiría la siguiente secuencia al crear un usuario con [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create):

1.  Llame a [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) para crear el usuario en la memoria caché local con el [**CN**](/windows/desktop/ADSchema/a-cn)especificado.
2.  Establezca el atributo [**samAccountName**](/windows/desktop/ADSchema/a-samaccountname) en el valor deseado con el método [**IADs. put**](/windows/desktop/api/iads/nf-iads-iads-put) .
3.  Ahora modifique otros atributos, como [**UserAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol). Esta restricción también se aplica a las propiedades ADSI, como [**IADsUser. AccountDisabled**](/windows/desktop/ADSI/iadsuser-property-methods), y métodos como [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword).
4.  Llame a [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar el nuevo usuario en el servidor.

Cuando se crea una nueva cuenta de usuario, está deshabilitada de forma predeterminada. La cuenta debe habilitarse manualmente o mediante programación. Para habilitar una cuenta de usuario mediante programación, quite la marca **ADS \_ up \_ ACCOUNTDISABLE** del atributo [**UserAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) .

Cuando se crea una nueva cuenta de usuario, el atributo [**UserAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) de la cuenta tiene establecida automáticamente la marca de **\_ \_ NOTREQD passwd** , que indica que no se requiere ninguna contraseña para la cuenta. Si las directivas de seguridad del dominio en el que se crea la cuenta requieren una contraseña para todas las cuentas de usuario, se debe quitar la marca de **fi \_ passwd \_ NOTREQD** del atributo **UserAccountControl** de la cuenta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Código de ejemplo para crear un usuario](example-code-for-creating-a-user.md)
</dt> </dl>