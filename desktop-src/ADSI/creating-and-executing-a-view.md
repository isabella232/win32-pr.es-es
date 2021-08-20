---
title: Crear y ejecutar una vista
description: Puede crear una vista para los datos obtenidos de Active Directory. Tenga en cuenta que solo la definición de vista se almacena en SQL Server y no en el conjunto de resultados real. Por lo tanto, puede obtener un resultado diferente al invocar la vista más adelante.
ms.assetid: c2892517-11e1-489f-a2f2-5118bccd605b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c4676154ea32dd06e39498e9f943b55d8dbf39694ab9c1005e942cad85f7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082729"
---
# <a name="creating-and-executing-a-view"></a>Crear y ejecutar una vista

Puede crear una vista para los datos obtenidos de Active Directory. Tenga en cuenta que solo la definición de vista se almacena en SQL Server y no en el conjunto de resultados real. Por lo tanto, puede obtener un resultado diferente al invocar la vista más adelante.

En el ejemplo de código siguiente se muestra cómo crear una vista.


```sql
CREATE VIEW viewADUsers 
AS
SELECT * FROM OpenQuery( ADSI,
    '<LDAP://DC=Fabrikam,DC=com>;(&(objectCategory=Person)(objectClass=user));name, adspath, title;subtree')
```



Use el código siguiente para invocar una vista.


```sql
SELECT * from viewADUsers
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una combinación heterogéneo entre SQL Server y Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)
</dt> </dl>

 

 




