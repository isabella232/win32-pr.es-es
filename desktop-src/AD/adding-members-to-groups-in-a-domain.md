---
title: Agregar miembros a grupos de un dominio
description: En este tema se muestra cómo agregar miembros a los grupos de un dominio.
ms.assetid: be65cd4e-df3e-416b-a673-774b71ab6996
ms.tgt_platform: multiple
keywords:
- Agregar miembros a grupos en un dominio AD
- Agrupa AD, agregar miembros a grupos de un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbd454348dc3eb519d03a7c5574746025c79a3f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487518"
---
# <a name="adding-members-to-groups-in-a-domain"></a>Agregar miembros a grupos de un dominio

Un grupo puede contener cualquier número de usuarios, contactos u otros grupos como miembros. En la lista siguiente se enumeran los atributos del objeto de grupo que controlan la pertenencia a grupos.



| Atributo                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**miembro**](/windows/desktop/ADSchema/a-member)<br/>     | El atributo [**member**](/windows/desktop/ADSchema/a-member) contiene los nombres distintivos de los objetos que son miembros del grupo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**memberOf**](/windows/desktop/ADSchema/a-memberof)<br/> | El atributo [**memberOf**](/windows/desktop/ADSchema/a-memberof) contiene los nombres distintivos de los grupos que contienen el grupo como miembro directo. El atributo **memberOf** no contiene ningún dato de pertenencia a grupos heredado. Por ejemplo, si GroupA es un miembro de GroupB y GroupB es un miembro de GroupC, el atributo **memberOf** de GroupA contendrá GroupB, pero no GroupC.<br/> El servidor de Active Directory mantiene esta propiedad. Cuando se agrega un nombre distintivo a la propiedad de [**miembro**](/windows/desktop/ADSchema/a-member) de otro grupo, ese nombre distintivo de otro grupo se agrega a la propiedad [**memberOf**](/windows/desktop/ADSchema/a-memberof) de este grupo.<br/> |



 

Cada uno de los métodos siguientes se puede usar para agregar un miembro a un grupo. Puede Agregar un miembro mediante el nombre distintivo del miembro o el enlace al objeto miembro y, a continuación, agregar el objeto miembro al objeto de grupo.

Para agregar un miembro que pertenezca a un dominio de nivel inferior a un grupo en un dominio de nivel superior, use el formato enlazable de la cadena SID para el nombre distintivo. Para obtener más información y un ejemplo de código que muestra cómo convertir un **objectSid** en una cadena enlazable, consulte la función de ejemplo **GetLDAPSidBindStringFromVariantSID** en el [código de ejemplo para convertir un objectSid en una cadena enlazable](example-code-for-converting-an-objectsid-into-a-bindable-string-.md).

<dl> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IADsGroup"></span><span id="adding_members_to_a_group_by_using_iadsgroup"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IADSGROUP"></span>Agregar miembros a un grupo mediante IADsGroup
</dt> <dd>

La interfaz [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) se puede usar para agregar miembros a un grupo mediante el método [**IADsGroup. Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) . Enlazar y obtener la interfaz **IADsGroup** para el objeto de grupo. A continuación, se puede usar el método **IADsGroup. Add** para agregar miembros al grupo.

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IDirectoryObject"></span><span id="adding_members_to_a_group_by_using_idirectoryobject"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IDIRECTORYOBJECT"></span>Agregar miembros a un grupo mediante IDirectoryObject
</dt> <dd>

La interfaz [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) se puede usar para agregar miembros a un grupo mediante el método [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) para modificar el atributo de [**miembro**](/windows/desktop/ADSchema/a-member) para el grupo. Enlazar y obtener la interfaz **IDirectoryObject** para el objeto de grupo. A continuación, use el método **IDirectoryObject:: SetObjectAttributes** para modificar el atributo de **miembro** .

> [!Note]  
> Dado que el atributo [**member**](/windows/desktop/ADSchema/a-member) tiene varios valores, asegúrese de usar el código de control **ADS \_ ATTR \_ Append** para agregar un nombre distintivo al atributo de **miembro** . El uso del código de control de **\_ \_ actualización de atributos de ADS** hará que se sobrescriban los valores de **miembro** existentes.

 

La interfaz [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) también se puede usar para agregar miembros a un grupo cuando el grupo se crea especificando los miembros en el parámetro *PAttributeEntries* del método [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_System.DirectoryServices"></span><span id="adding_members_to_a_group_by_using_system.directoryservices"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_SYSTEM.DIRECTORYSERVICES"></span>Agregar miembros a un grupo mediante System. DirectoryServices
</dt> <dd>

Puede usar el espacio de nombres [System. DirectoryServices](/dotnet/api/system.directoryservices) para agregar miembros a un grupo mediante el método **PropertyValueCollection. Add** en la propiedad **member** del objeto Group. Para obtener más información, vea [establecer las propiedades de los objetos de directorio](/previous-versions/ms180860(v=vs.90)).

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_the_LDAP_API"></span><span id="adding_members_to_a_group_by_using_the_ldap_api"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_THE_LDAP_API"></span>Agregar miembros a un grupo mediante la API de LDAP
</dt> <dd>

Puede usar la API de [Protocolo ligero de acceso a directorios](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) para agregar miembros a un grupo mediante una de las funciones de [**\_ \* modificación de LDAP**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_s) . Para obtener más información, vea [modificar una entrada de directorio](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry).

</dd> </dl>

 

