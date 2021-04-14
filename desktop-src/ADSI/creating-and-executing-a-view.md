---
title: Crear y ejecutar una vista
description: Puede crear una vista para los datos obtenidos de Active Directory. Tenga en cuenta que solo la definición de la vista se almacena en SQL Server, no el conjunto de resultados real. Por lo tanto, es posible que obtenga un resultado diferente al invocar la vista más adelante.
ms.assetid: c2892517-11e1-489f-a2f2-5118bccd605b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a47a0956acb8f9d0268240e677f62a2e395b4fed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418357"
---
# <a name="creating-and-executing-a-view"></a>Crear y ejecutar una vista

Puede crear una vista para los datos obtenidos de Active Directory. Tenga en cuenta que solo la definición de la vista se almacena en SQL Server, no el conjunto de resultados real. Por lo tanto, es posible que obtenga un resultado diferente al invocar la vista más adelante.

En el siguiente ejemplo de código se muestra cómo crear una vista.


```sql
CREATE VIEW viewADUsers 
AS
SELECT * FROM OpenQuery( ADSI,
    '<LDAP://DC=Fabrikam,DC=com>;(&(objectCategory=Person)(objectClass=user));name, adspath, title;subtree')
```



Use el siguiente código para invocar una vista.


```sql
SELECT * from viewADUsers
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una combinación heterogénea entre SQL Server y Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)
</dt> </dl>

 

 




