---
title: Access Control y eliminación de objetos
description: Active Directory permite eliminar un objeto si tiene acceso DELETE al objeto o ads RIGHT DS DELETE CHILD acceso al tipo de objeto \_ \_ en el contenedor \_ \_ primario.
ms.assetid: 87027c25-e3c9-4bad-8df3-cb6205e40ef6
ms.tgt_platform: multiple
keywords:
- Access Control ad y eliminación de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dda8f5eb241515e9428322ea01c6586b6870e7133e96a1cd7b4fcbb32f6f0c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118025640"
---
# <a name="access-control-and-object-deletion"></a>Access Control y eliminación de objetos

Active Directory Domain Services permite eliminar un objeto si tiene uno de los siguientes derechos de acceso:

-   Acceso DELETE al propio objeto
-   ADS RIGHT DS DELETE CHILD access for that object type on the parent container (ADS \_ RIGHT \_ DS DELETE CHILD access for \_ that object type on the parent container) (ADS RIGHT DS DELETE \_ CHILD access for that object type on the parent

Tenga en cuenta que el sistema comprueba el descriptor de seguridad para el objeto y su elemento primario antes de denegar la eliminación. Esto significa que una ACE que deniega explícitamente el acceso DELETE a un usuario no tiene ningún efecto si el usuario tiene acceso DELETE \_ CHILD en el elemento primario. De forma similar, se puede invalidar una ACE que deniegue el acceso DELETE CHILD en el elemento primario si se permite el acceso \_ DELETE en el propio objeto.

Para realizar una operación de eliminación de árbol, por ejemplo mediante el método [**IADsDeleteOps::D eleteObject,**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) debe tener acceso a ADS RIGHT DS DELETE TREE al \_ \_ \_ \_ objeto. Si tiene este derecho de acceso, puede eliminar el objeto y cualquier objeto secundario independientemente de las protecciones en los objetos secundarios. Para eliminar un árbol si no tiene acceso a ADS RIGHT DS DELETE TREE, debe recorrer de forma recursiva el árbol y eliminar \_ \_ cada objeto \_ \_ individualmente. En este caso, debe tener el acceso DELETE o DELETE \_ CHILD necesario para cada objeto del árbol.

> [!WARNING]
> Si los usuarios tienen acceso a ADS RIGHT DS DELETE TREE para un objeto, esto les ofrece la capacidad de eliminar un \_ \_ subárbol \_ \_ completo, incluidos todos los objetos secundarios. Por este motivo, puede considerar la posibilidad de revocar el permiso de acceso "Eliminar subárbol" para todos los usuarios de un contenedor primario.

 

 

 