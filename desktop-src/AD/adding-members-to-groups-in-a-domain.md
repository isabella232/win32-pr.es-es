---
title: Agregar miembros a grupos en un dominio
description: En este tema se muestra cómo agregar miembros a grupos de un dominio.
ms.assetid: be65cd4e-df3e-416b-a673-774b71ab6996
ms.tgt_platform: multiple
keywords:
- Agregar miembros a grupos en un dominio de AD
- Agrupa AD , agregar miembros a grupos en un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c9f0c85943752b42cf3d9d8b88d385aaba9e014b21aa9f538955cb49b1a750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024762"
---
# <a name="adding-members-to-groups-in-a-domain"></a>Agregar miembros a grupos en un dominio

Un grupo puede contener cualquier número de usuarios, contactos u otros grupos como miembros. En la lista siguiente se enumeran los atributos del objeto de grupo que controlan la pertenencia a grupos.



| Atributo                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Miembro**](/windows/desktop/ADSchema/a-member)<br/>     | El [**atributo**](/windows/desktop/ADSchema/a-member) miembro contiene los nombres distintivos de los objetos que son miembros del grupo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Miembro**](/windows/desktop/ADSchema/a-memberof)<br/> | El [**atributo memberOf**](/windows/desktop/ADSchema/a-memberof) contiene los nombres distintivos de los grupos que contienen el grupo como miembro directo. El **atributo memberOf** no contiene datos de pertenencia a grupos heredados. Por ejemplo, si GroupA es miembro de GroupB y GroupB es miembro de GroupC, el atributo **memberOf** de GroupA contendrá GroupB, pero no GroupC.<br/> El Active Directory mantiene esta propiedad. Cuando se agrega un nombre [](/windows/desktop/ADSchema/a-member) distintivo a la propiedad miembro de otro grupo, el nombre distintivo de ese otro grupo se agrega a la propiedad [**memberOf de este**](/windows/desktop/ADSchema/a-memberof) grupo.<br/> |



 

Cada uno de los métodos siguientes se puede usar para agregar un miembro a un grupo. Puede agregar un miembro mediante el nombre distintivo del miembro o el enlace al objeto de miembro y, a continuación, agregar el objeto miembro al objeto de grupo.

Para agregar un miembro que pertenece a un dominio de nivel inferior a un grupo de un dominio de nivel superior, use la forma enlazable de la cadena SID para el nombre distintivo. Para obtener más información y un ejemplo de código que muestra cómo convertir **un objectSid** en una cadena enlazable, vea la función de ejemplo **GetLDAPSidBindStringFromVariantSID** en Código de ejemplo para convertir [un objectSid](example-code-for-converting-an-objectsid-into-a-bindable-string-.md)en una cadena enlazable .

<dl> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IADsGroup"></span><span id="adding_members_to_a_group_by_using_iadsgroup"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IADSGROUP"></span>Agregar miembros a un grupo mediante IADsGroup
</dt> <dd>

La [**interfaz IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) se puede usar para agregar miembros a un grupo mediante el [**método IADsGroup.Add.**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) Enlace a y obtenga la **interfaz IADsGroup** para el objeto de grupo. A **continuación, se puede usar el método IADsGroup.Add** para agregar miembros al grupo.

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IDirectoryObject"></span><span id="adding_members_to_a_group_by_using_idirectoryobject"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IDIRECTORYOBJECT"></span>Agregar miembros a un grupo mediante IDirectoryObject
</dt> <dd>

La [**interfaz IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) se puede usar para agregar miembros a un grupo mediante el [](/windows/desktop/ADSchema/a-member) método [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) para modificar el atributo miembro del grupo. Enlace a y obtenga la **interfaz IDirectoryObject** para el objeto de grupo. A continuación, **use el método IDirectoryObject::SetObjectAttributes** para modificar el **atributo miembro.**

> [!Note]  
> Dado que [**el atributo**](/windows/desktop/ADSchema/a-member) de miembro tiene varios valores, asegúrese de usar el código de control APPEND de **ADS \_ ATTR \_** para agregar un nombre distintivo al atributo **miembro.** El uso del código de control  **\_ UPDATE \_ de ADS ATTR** hará que se sobrescriban los valores de miembro existentes.

 

La [**interfaz IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) también se puede usar para agregar miembros a un grupo cuando se crea el grupo especificando los miembros en el *parámetro pAttributeEntries* del método [**IDirectoryObject::CreateDSObject.**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject)

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_System.DirectoryServices"></span><span id="adding_members_to_a_group_by_using_system.directoryservices"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_SYSTEM.DIRECTORYSERVICES"></span>Agregar miembros a un grupo mediante System.DirectoryServices
</dt> <dd>

Puede usar el espacio de nombres [System.DirectoryServices](/dotnet/api/system.directoryservices) para agregar miembros a un  grupo mediante el método **PropertyValueCollection.Add** en la propiedad miembro del objeto de grupo. Para obtener más información, vea [Establecer propiedades en objetos de directorio.](/previous-versions/ms180860(v=vs.90))

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_the_LDAP_API"></span><span id="adding_members_to_a_group_by_using_the_ldap_api"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_THE_LDAP_API"></span>Agregar miembros a un grupo mediante la API LDAP
</dt> <dd>

Puede usar la API [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) para agregar miembros a un grupo mediante una de las funciones de modificación [**\_ ldap. \***](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_s) Para obtener más información, [vea Modificar una entrada de directorio.](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry)

</dd> </dl>

 

