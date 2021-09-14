---
description: Un objeto IAzApplicationGroup representa un grupo de usuarios. Después, se pueden asignar roles a este grupo de usuarios de forma colectiva. Un objeto IAzApplicationGroup también puede incluir otros objetos IAzApplicationGroup como miembros.
ms.assetid: 8b445419-7316-4034-b742-a05845af1862
title: Definir grupos de usuarios en script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f0b652530167c71fbea7bc23d27434ae458f9b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073708"
---
# <a name="defining-groups-of-users-in-script"></a>Definir grupos de usuarios en script

En el Administrador de autorización, [**un objeto IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) representa un grupo de usuarios. Después, se pueden asignar roles a este grupo de usuarios de forma colectiva. Un **objeto IAzApplicationGroup** también puede incluir otros **objetos IAzApplicationGroup** como miembros. Para obtener más información sobre los grupos de aplicaciones, vea [Usuarios y grupos.](users-and-groups.md)

Un grupo se puede definir mediante listas explícitas de miembros y no miembros o mediante una consulta del [*Protocolo*](/windows/desktop/SecGloss/l-gly) ligero de acceso a directorios (LDAP). En los ejemplos siguientes se muestra cómo crear cada tipo de grupo de aplicaciones:

-   [Creación de un grupo básico](#creating-a-basic-group)
-   [Creación de un grupo de consultas LDAP](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a>Creación de un grupo básico

Los miembros incluidos en las propiedades [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) y [**NonMembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) del objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) que representa el grupo definen un grupo de aplicaciones básico. Los usuarios y grupos enumerados en la propiedad **Miembros** se incluyen en el grupo de aplicaciones y los usuarios y grupos enumerados en la **propiedad NonMembers** se excluyen del grupo de aplicaciones. Al aparecer en la **propiedad NonMembers,** se sustituye por aparecer en la **propiedad Members.**

En el ejemplo siguiente se muestra cómo crear un grupo de aplicaciones básico y agregar todos los usuarios locales como miembros de ese grupo. En el ejemplo se supone que hay un almacén de directivas XML existente denominado MyStore.xml en el directorio raíz de la unidad C.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("Trusted Users")

'  Add a well-known SID for all local users to the group.
appGroup.AddMember("S-1-1-0")

'  Save the application group to the store.
appGroup.Submit
```



## <a name="creating-an-ldap-query-group"></a>Creación de un grupo de consultas LDAP

Un grupo de consultas LDAP tiene una pertenencia definida por la consulta contenida en el valor de su [**propiedad LdapQuery.**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery)

En el ejemplo siguiente se muestra cómo crear un grupo de aplicaciones de consulta LDAP y agregar todos los usuarios como miembros de ese grupo. En el ejemplo se supone que hay un almacén de directivas XML existente denominado MyStore.xml en el directorio raíz de la unidad C.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("LDAP Trusted Users")

'  Set the Type property of the group to two
'  (AZ_GROUPTYPE_LDAP_QUERY).
appGroup.Type = 2

'  Add LDAP query for all users.
appGroup.LdapQuery = ("&(objectCategory=person)(objectClass=user)")

'  Save the application group to the store.
appGroup.Submit

```



 

 
