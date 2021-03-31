---
description: Un almacén de directivas de autorización contiene información sobre la Directiva de seguridad de una aplicación o grupo de aplicaciones.
ms.assetid: bce85da8-11de-4bc1-b097-d8efdbd28abf
title: Crear un objeto de almacén de directivas de autorización en el script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: feb02c80408210b663524e2aa914852a853e80ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908290"
---
# <a name="creating-an-authorization-policy-store-object-in-script"></a>Crear un objeto de almacén de directivas de autorización en el script

Un almacén de directivas de autorización contiene información sobre la Directiva de seguridad de una aplicación o grupo de aplicaciones. La información incluye las aplicaciones, operaciones, tareas, usuarios y grupos de usuarios asociados a la tienda. Cuando una aplicación que usa administrador de autorización se inicializa, carga esta información desde el almacén. El almacén de directivas de autorización debe estar ubicado en un sistema de confianza porque los administradores de ese sistema tienen un alto grado de acceso al almacén.

Administrador de autorización admite el almacenamiento de la Directiva de autorización en el servicio de directorio de Active Directory o en un archivo XML, tal como se muestra en los ejemplos siguientes. En la API de administrador de autorización, un almacén de directivas de autorización se representa mediante un objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) . En los ejemplos se muestra cómo crear un objeto **AzAuthorizationStore** para un almacén de Active Directory y un almacén XML.

-   [Creación de un almacén de Active Directory](#creating-an-active-directory-store)
-   [Creación de un almacén de SQL Server](#creating-a-sql-server-store)
-   [Crear un almacén XML](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a>Creación de un almacén de Active Directory

Para usar Active Directory para almacenar la Directiva de autorización, el dominio debe estar en el nivel funcional del dominio de **Windows Server 2003** . No se encuentra el almacén de directivas de autorización en un **contexto de nomenclatura que no es de dominio** (también denominado partición de aplicación). Se recomienda ubicar el almacén en el contenedor de **datos de programa** en una nueva unidad organizativa creada específicamente para el almacén de directivas de autorización. También se recomienda que el almacén se encuentre en la misma red de área local que los servidores de aplicaciones que ejecutan las aplicaciones que usan el almacén.

En el ejemplo siguiente se muestra cómo crear un objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa un almacén de directivas de autorización en Active Directory. En el ejemplo se supone que hay una unidad organizativa Active Directory denominada datos de programa en un dominio denominado authmanager.com.


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



## <a name="creating-a-sql-server-store"></a>Creación de un almacén de SQL Server

Administrador de autorización admite la creación de un almacén de directivas de autorización basado en Microsoft SQL Server. Para crear un almacén de autorización basado en SQL Server, use una dirección URL que comience con el prefijo **MSSQL://**. La dirección URL debe contener una cadena de conexión SQL válida, un nombre de base de datos y el nombre del almacén de directivas de autorización: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.

Si la instancia de SQL Server no contiene la base de datos de administrador de autorización especificada, el administrador de autorización crea una nueva base de datos con ese nombre.

> [!Note]  
> Las conexiones a un almacén de SQL Server no se cifran a menos que se configure explícitamente el cifrado SQL para la conexión o se configure el cifrado del tráfico de red que usa el protocolo de seguridad de Internet (IPsec).

 

En el ejemplo siguiente se muestra cómo crear un objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa un almacén de directivas de autorización en una base de datos de SQL Server.


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



## <a name="creating-an-xml-store"></a>Crear un almacén XML

Administrador de autorización admite la creación de un almacén de directivas de autorización en formato XML. El almacén XML puede ubicarse en el mismo equipo en el que se ejecuta la aplicación, o bien se puede almacenar de forma remota. No se admite la edición directa del archivo XML. Use el complemento MMC de administrador de autorización o la API de administrador de autorización para editar el almacén de directivas.

Administrador de autorización no admite la delegación de la administración de un almacén de directivas XML. Para obtener información acerca de la delegación, vea [delegar la definición de permisos en el script](delegating-the-defining-of-permissions-in-script.md).

En el ejemplo siguiente se muestra cómo crear un objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa un almacén de directivas de autorización en un archivo XML.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, "msxml://C:\MyStore.xml"

'  Save information to the store.
authStore.Submit
```



 

 



