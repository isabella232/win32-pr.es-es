---
title: Access Control y eliminación de objetos
description: Active Directory le permite eliminar un objeto si tiene acceso de eliminación al objeto o ADS \_ right \_ DS \_ Delete \_ Child Access al tipo de objeto en el contenedor principal.
ms.assetid: 87027c25-e3c9-4bad-8df3-cb6205e40ef6
ms.tgt_platform: multiple
keywords:
- AD de Access Control y eliminación de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bddcd2b563e144743689f2a26c17bd417db14ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789430"
---
# <a name="access-control-and-object-deletion"></a>Access Control y eliminación de objetos

Active Directory Domain Services le permiten eliminar un objeto si tiene uno de los siguientes derechos de acceso:

-   ELIMINAR el acceso al propio objeto
-   ADS \_ derecho \_ DS \_ eliminar \_ acceso secundario para ese tipo de objeto en el contenedor primario

Tenga en cuenta que el sistema comprueba el descriptor de seguridad para el objeto y su elemento primario antes de denegar la eliminación. Esto significa que una ACE que deniegue explícitamente el acceso de eliminación a un usuario no tiene ningún efecto si el usuario tiene \_ acceso de eliminación secundario en el elemento primario. Del mismo modo, se puede invalidar una ACE que deniegue \_ el acceso de eliminación secundario en el elemento primario si se permite el acceso de eliminación en el propio objeto.

Para realizar una operación de eliminación de árbol, por ejemplo, mediante el método [**IADsDeleteOps::D eleteobject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) , debe tener el \_ acceso de árbol derecho de \_ \_ eliminación DS \_ al objeto. Si tiene este derecho de acceso, puede eliminar el objeto y todos los objetos secundarios, independientemente de las protecciones de los objetos secundarios. Para eliminar un árbol si no tiene ADS \_ derecho \_ DS \_ eliminar \_ árbol, debe recorrer el árbol de forma recursiva y eliminar cada objeto individualmente. En este caso, debe tener el acceso secundario eliminar o eliminar \_ para cada objeto del árbol.

> [!WARNING]
> Si los usuarios tienen \_ derechos \_ \_ \_ de acceso de árbol de eliminación DS correctos para un objeto, esto les da la posibilidad de eliminar un subárbol completo, incluidos todos los objetos secundarios. Por esta razón, puede considerar la posibilidad de revocar el permiso de acceso "eliminar subárbol" para todos los usuarios de un contenedor primario.

 

 

 