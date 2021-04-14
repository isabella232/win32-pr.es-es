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
# <a name="creating-and-executing-a-view"></a><span data-ttu-id="d5e30-105">Crear y ejecutar una vista</span><span class="sxs-lookup"><span data-stu-id="d5e30-105">Creating and Executing a View</span></span>

<span data-ttu-id="d5e30-106">Puede crear una vista para los datos obtenidos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d5e30-106">You can create a view for data obtained from Active Directory.</span></span> <span data-ttu-id="d5e30-107">Tenga en cuenta que solo la definición de la vista se almacena en SQL Server, no el conjunto de resultados real.</span><span class="sxs-lookup"><span data-stu-id="d5e30-107">Be aware that only the view definition is stored in SQL Server, and not the actual result set.</span></span> <span data-ttu-id="d5e30-108">Por lo tanto, es posible que obtenga un resultado diferente al invocar la vista más adelante.</span><span class="sxs-lookup"><span data-stu-id="d5e30-108">Therefore, you may get a different result when you invoke the view at a later time.</span></span>

<span data-ttu-id="d5e30-109">En el siguiente ejemplo de código se muestra cómo crear una vista.</span><span class="sxs-lookup"><span data-stu-id="d5e30-109">The following code sample shows how to create a view.</span></span>


```sql
CREATE VIEW viewADUsers 
AS
SELECT * FROM OpenQuery( ADSI,
    '<LDAP://DC=Fabrikam,DC=com>;(&(objectCategory=Person)(objectClass=user));name, adspath, title;subtree')
```



<span data-ttu-id="d5e30-110">Use el siguiente código para invocar una vista.</span><span class="sxs-lookup"><span data-stu-id="d5e30-110">Use the following code to invoke a view.</span></span>


```sql
SELECT * from viewADUsers
```



## <a name="related-topics"></a><span data-ttu-id="d5e30-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d5e30-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5e30-112">Crear una combinación heterogénea entre SQL Server y Active Directory</span><span class="sxs-lookup"><span data-stu-id="d5e30-112">Creating a Heterogeneous Join between SQL Server and Active Directory</span></span>](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)
</dt> </dl>

 

 




