---
title: Creación de un usuario
description: Para crear un usuario en Active Directory Domain Services, cree un objeto de usuario en el contenedor de dominios del dominio donde desea colocar el usuario.
ms.assetid: fb51895f-71e1-45b6-b8bc-ed674e822734
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory , creación de un usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3422d269351ae29fd15d12585ca02b91a4b9c23
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469232"
---
# <a name="creating-a-user"></a>Creación de un usuario

Para crear un usuario en Active Directory Domain Services, cree un objeto de usuario en el contenedor de dominios del dominio donde desea colocar el usuario. Los usuarios se pueden crear en la raíz del dominio, dentro de una unidad organizativa o dentro de un contenedor.

Al crear un objeto de usuario, también debe establecer los atributos, enumerados en la tabla siguiente, para establecer el objeto como un usuario legal reconocido por Active Directory Domain Services y el Seguridad de Windows sistema.



| Atributo                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cn**](/windows/desktop/ADSchema/a-cn)                         | Especifica el nombre del objeto de usuario en el directorio . Este será el nombre distintivo relativo (RDN) del objeto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) | Especifica una cadena que es el nombre utilizado para admitir clientes y servidores de una versión anterior de Windows. [**SAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) debe tener menos de 20 caracteres para admitir clientes de una versión anterior de Windows.<br/> [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) debe ser único entre todos los objetos de entidad de seguridad del dominio. Debe realizar una consulta en el dominio para comprobar que **sAMAccountName** es único dentro del dominio.<br/> [**sAMAccountName es**](/windows/desktop/ADSchema/a-samaccountname) un atributo opcional. El servidor creará un valor **de sAMAccountName** aleatorio si no se especifica ninguno.<br/> |



 

También puede establecer otros atributos. Los siguientes atributos de usuario se establecen con valores predeterminados si no se establecen explícitamente en el momento de la creación.




| Atributo | Descripción | 
|-----------|-------------|
| <a href="/windows/desktop/ADSchema/a-accountexpires"><strong>accountExpires</strong></a> | Especifica cuándo expirará la cuenta. El valor predeterminado <strong>es TIMEQ_FOREVER</strong>, que indica que la cuenta nunca expirará.<br /> | 
| <a href="/windows/desktop/ADSchema/a-ntsecuritydescriptor"><strong>nTSecurityDescriptor</strong></a> | Se crea un descriptor de seguridad basado en reglas específicas. Para obtener más información, vea <a href="how-security-descriptors-are-set-on-new-directory-objects.md">How Security Descriptors are Set on New Directory Objects</a>.<br /> | 
| <a href="/windows/desktop/ADSchema/a-objectcategory"><strong>objectCategory</strong></a> | Especifica la categoría de usuario. El valor predeterminado es "Person".<br /> | 
| <a href="/windows/desktop/ADSchema/a-name"><strong>Nombre</strong></a> | Especifica el nombre de usuario. El valor predeterminado es el valor establecido para <a href="/windows/desktop/ADSchema/a-cn"><strong>cn</strong></a>.<br /> | 
| <a href="/windows/desktop/ADSchema/a-pwdlastset"><strong>pwdLastSet</strong></a> | Especifica cuándo el usuario estableció la contraseña por última vez. El valor predeterminado es cero, lo que indica que el usuario debe cambiar la contraseña en el siguiente inicio de sesión.<br /> | 
| <a href="/windows/desktop/ADSchema/a-useraccountcontrol"><strong>userAccountControl</strong></a> | Contiene valores que determinan varias características de inicio de sesión y cuenta para el usuario.<br /> De forma predeterminada, se establecen las marcas siguientes:<br /><ul><li><strong>UF_ACCOUNTDISABLE:</strong> la cuenta está deshabilitada.</li><li><strong>UF_PASSWD_NOTREQD:</strong> no se requiere ninguna contraseña.</li><li><strong>UF_NORMAL_ACCOUNT:</strong> tipo de cuenta predeterminado que representa un usuario típico.</li></ul> | 
| <a href="/windows/desktop/ADSchema/a-memberof"><strong>Miembro</strong></a> | Especifica el grupo o grupos de los que el usuario es miembro directo. El valor predeterminado es "Usuarios del dominio".<br /> | 




 

Un usuario se crea enlazando al contenedor deseado y, a continuación, utilizando uno de los métodos siguientes. Los [**atributos cn**](/windows/desktop/ADSchema/a-cn) y [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) deben establecerse antes de que el usuario se haya confirmado en el servidor.



| Método                                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)                        | El [**atributo cn**](/windows/desktop/ADSchema/a-cn) se toma del parámetro *bstrRelativeName.* El nuevo usuario debe estar confirmado mediante una [**llamada a IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) o no se creará el objeto. Para obtener más información, vea [Ejemplo de código para crear un usuario.](example-code-for-creating-a-user.md)<br/>                                                                                            |
| [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) | El [**atributo cn**](/windows/desktop/ADSchema/a-cn) se toma del parámetro *pszRDNName.* El nuevo usuario se confirma cuando se llama a [**CreateDSObject.**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) Para obtener más información, vea [Ejemplo de código para crear un usuario.](example-code-for-creating-a-user.md)<br/>                                                                                                                |
| [DirectoryEntries.Add](/dotnet/api/system.directoryservices.directoryentries.add?view=dotnet-plat-ext-3.1)       | El [**atributo cn**](/windows/desktop/ADSchema/a-cn) se toma del parámetro *name.* El nuevo objeto de usuario debe confirmarse mediante una llamada [a DirectoryEntry.CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) o el objeto no se creará. Para obtener más información, vea [Adding Directory Objects](/previous-versions/ms180851(v=vs.90)).<br/> |



 

El nuevo usuario debe estar confirmado en el servidor antes de que se puedan modificar los atributos que no sean [**cn**](/windows/desktop/ADSchema/a-cn) y [**sAMAccountName.**](/windows/desktop/ADSchema/a-samaccountname) Esto se debe a que la cuenta de usuario no existe realmente hasta que se confirma el usuario. Si se recupera o modifica un atributo para un objeto que no existe en el servidor, se producirá un error. Esto incluye llamar al [**método IADsUser.SetPassword.**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) Por ejemplo, se seguiría la siguiente secuencia al crear un usuario con [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create):

1.  Llame [**a IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) para crear el usuario en la memoria caché local con el [**cn especificado.**](/windows/desktop/ADSchema/a-cn)
2.  Establezca el [**atributo sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) en el valor deseado con el [**método IADs.Put.**](/windows/desktop/api/iads/nf-iads-iads-put)
3.  Ahora modifique otros atributos, como [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol). Esta restricción también se aplica a las propiedades adsi, como [**IADsUser.AccountDisabled,**](/windows/desktop/ADSI/iadsuser-property-methods)y a los métodos como [**IADsUser.SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword).
4.  Llame [**a IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar el nuevo usuario en el servidor.

Cuando se crea una nueva cuenta de usuario, se deshabilita de forma predeterminada. La cuenta debe habilitarse manualmente o mediante programación. Para habilitar una cuenta de usuario mediante programación, quite la marca **\_ ADS UF \_ ACCOUNTDISABLE** del [**atributo userAccountControl.**](/windows/desktop/ADSchema/a-useraccountcontrol)

Cuando se crea una nueva cuenta de usuario, el atributo [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) de la cuenta tiene automáticamente la marca **UF \_ PASSWD \_ NOTREQD** establecida, lo que indica que no se requiere ninguna contraseña para la cuenta. Si las directivas de seguridad del dominio en el que se crea la cuenta requieren una contraseña para todas las cuentas de usuario, la marca **UF \_ PASSWD \_ NOTREQD** debe quitarse del atributo **userAccountControl** de la cuenta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Código de ejemplo para crear un usuario](example-code-for-creating-a-user.md)
</dt> </dl>
