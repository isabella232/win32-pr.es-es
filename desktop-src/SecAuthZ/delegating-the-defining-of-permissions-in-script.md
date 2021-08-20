---
description: Puede delegar la administración de los almacenes de directivas de autorización que se almacenan en Active Directory.
ms.assetid: a7b43dfe-f03e-4795-bbd3-746eb3449fd0
title: Delegación de la definición de permisos en el script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69cf0793a48a572ec4b37cbf3634f65b04ff3565f3205bf0380c68914abb4530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782069"
---
# <a name="delegating-the-defining-of-permissions-in-script"></a>Delegación de la definición de permisos en el script

Puede delegar la administración de los almacenes de directivas de autorización que se almacenan en Active Directory. La administración se puede delegar a usuarios y grupos en el nivel de almacén, aplicación o ámbito.

En cada nivel, hay una lista de administradores y lectores. Los administradores de un almacén, aplicación o ámbito pueden leer y modificar el almacén de directivas en el nivel delegado. Los lectores pueden leer el almacén de directivas en el nivel delegado, pero no pueden modificar el almacén.

También se debe agregar un usuario o grupo que sea administrador o lector de una aplicación como usuario delegado del almacén de directivas que contiene esa aplicación. De forma similar, se debe agregar un usuario o grupo que sea administrador o lector de un ámbito como usuario delegado de la aplicación que contiene ese ámbito.

**Para delegar la administración de un ámbito**

1.  Agregue el usuario o grupo a la lista de usuarios delegados del almacén que contiene el ámbito llamando al [**método AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) del objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que contiene el ámbito.
2.  Agregue el usuario o grupo a la lista de usuarios delegados de la aplicación que contiene el ámbito llamando al [**método AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) del objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) que contiene el ámbito.
3.  Agregue el usuario o grupo a la lista de administradores del ámbito mediante una llamada al [**método AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) del [**objeto IAzScope.**](/windows/desktop/api/Azroles/nn-azroles-iazscope)

> [!Note]  
> Los almacenes de directivas basados en XML no admiten la delegación en ningún nivel.

 

Si un ámbito dentro de un almacén de autorización almacenado en Active Directory contiene definiciones de tareas que incluyen reglas de autorización o definiciones de roles que incluyen reglas de autorización, el ámbito no se puede delegar.

En el ejemplo siguiente se muestra cómo delegar la administración de una aplicación. En el ejemplo se da por supuesto que hay un almacén de directivas de autorización de Active Directory existente en la ubicación especificada, que este almacén de directivas contiene una aplicación denominada Expense y que esta aplicación no contiene tareas con scripts de reglas de negocios.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, _
    "msldap://CN=MyStore,CN=Program Data,DC=authmanager,DC=com"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Add a delegated policy user to the store.
AzManStore.AddDelegatedPolicyUserName("ExampleDomain\\UserName")

'  Add the user as an administrator of the application.
expenseApp.AddPolicyAdministratorName("ExampleDomain\\UserName")

'  Save changes to the store.
AzManStore.Submit
```



 

 



