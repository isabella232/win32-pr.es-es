---
description: Un almacén de directivas de autorización contiene información sobre la directiva de seguridad de una aplicación o grupo de aplicaciones.
ms.assetid: bce85da8-11de-4bc1-b097-d8efdbd28abf
title: Crear un objeto de almacén de directivas de autorización en script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 409a22df52d2914cd205700afccfc7a59f19031d924a921b5f2e5101621a895a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782200"
---
# <a name="creating-an-authorization-policy-store-object-in-script"></a>Crear un objeto de almacén de directivas de autorización en script

Un almacén de directivas de autorización contiene información sobre la directiva de seguridad de una aplicación o grupo de aplicaciones. La información incluye las aplicaciones, las operaciones, las tareas, los usuarios y los grupos de usuarios asociados al almacén. Cuando se inicializa una aplicación que usa el Administrador de autorización, carga esta información desde el almacén. El almacén de directivas de autorización debe encontrarse en un sistema de confianza porque los administradores de ese sistema tienen un alto grado de acceso al almacén.

El Administrador de autorización admite el almacenamiento de la directiva de autorización Active Directory servicio de directorio o en un archivo XML, como se muestra en los ejemplos siguientes. En la API de Authorization Manager, un almacén de directivas de autorización se representa mediante [**un objeto AzAuthorizationStore.**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) En los ejemplos se muestra cómo crear un **objeto AzAuthorizationStore** para un Active Directory y un almacén XML.

-   [Creación de una Active Directory Store](#creating-an-active-directory-store)
-   [Creación de un SQL Server Store](#creating-a-sql-server-store)
-   [Creación de un almacén XML](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a>Creación de un Active Directory Store

Para usar Active Directory para almacenar la directiva de autorización, el dominio debe estar en el nivel funcional de dominio Windows **Server 2003.** El almacén de directivas de autorización no se puede encontrar en un contexto de nomenclatura que no **sea de dominio** (también denominado partición de aplicación). Se recomienda que el almacén  se encuentra en el contenedor Datos del programa en una nueva unidad organizativa creada específicamente para el almacén de directivas de autorización. También se recomienda que el almacén se encuentra dentro de la misma red de área local que los servidores de aplicaciones que ejecutan aplicaciones que usan el almacén.

En el ejemplo siguiente se muestra cómo crear un [**objeto AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa un almacén de directivas de autorización en Active Directory. En el ejemplo se supone que hay una unidad organizativa Active Directory denominada Datos de programa en un dominio denominado authmanager.com.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, _
    "msldap://CN=MyStore, CN=Program Data,DC=authmanager,DC=com"

'  Save the information to the store.
authStore.Submit
```



## <a name="creating-a-sql-server-store"></a>Creación de una SQL Server Store

El Administrador de autorización admite la creación de un Microsoft SQL Server de directivas de autorización basado en la autorización. Para crear un SQL Server de autorización basado en el servidor, use una dirección URL que comience con el **prefijo MSSQL://**. La dirección URL debe contener una cadena de conexión SQL, un nombre de base de datos y el nombre del almacén de directivas de autorización: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.

Si la instancia de SQL Server no contiene la base de datos del Administrador de autorización especificada, el Administrador de autorización crea una nueva base de datos con ese nombre.

> [!Note]  
> Las conexiones a un almacén de SQL Server no se cifran a menos que configure explícitamente el cifrado de SQL para la conexión o configure el cifrado del tráfico de red que usa seguridad de protocolo de Internet (IPsec).

 

En el ejemplo siguiente se muestra cómo crear un [**objeto AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa un almacén de directivas de autorización en una base SQL Server datos.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, _ 
  "MSSQL://Driver={SQL Server};Server={AzServer};/AzDB/MyStore"

'  Save information to the store.
authStore.Submit
```



## <a name="creating-an-xml-store"></a>Creación de un almacén XML

Authorization Manager admite la creación de un almacén de directivas de autorización en formato XML. El almacén XML se puede encontrar en el mismo equipo donde se ejecuta la aplicación o se puede almacenar de forma remota. No se admite la edición directa del archivo XML. Use el complemento MMC de Authorization Manager o la API de Authorization Manager para editar el almacén de directivas.

El Administrador de autorización no admite la delegación de la administración de un almacén de directivas XML. Para obtener información sobre la delegación, vea [Delegating the Defining of Permissions in Script](delegating-the-defining-of-permissions-in-script.md).

En el ejemplo siguiente se muestra cómo crear un [**objeto AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa un almacén de directivas de autorización en un archivo XML.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, "msxml://C:\MyStore.xml"

'  Save information to the store.
authStore.Submit
```



 

 



