---
description: Las transformaciones seguras en el origen deben tener un origen ubicado en la raíz del origen del paquete.
ms.assetid: b5355053-9922-444f-a117-f6af461ef9e9
title: Transformaciones seguras en el origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec59d551489fa1699c20c24d09b7ecbff99f8ca4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913661"
---
# <a name="secure-at-source-transforms"></a>Transformaciones seguras en el origen

Las transformaciones seguras en el origen deben tener un origen ubicado en la raíz del origen del paquete. Cuando el paquete se instala o se anuncia, el instalador guarda las transformaciones en una memoria caché donde, en un sistema de archivos seguro, el usuario no tiene acceso de escritura. Si la copia local de la transformación deja de estar disponible, el instalador busca un origen para restaurar la memoria caché. El método es el mismo que para buscar un archivo. msi en la lista de origen. Para obtener más información, consulte [resistencia del origen](source-resiliency.md). La eliminación de un producto por parte de un usuario quita todas las transformaciones seguras para ese producto del equipo del usuario.

Para aplicar transformaciones seguras en el origen a la instalación de un paquete, establezca la [Directiva TransformsSecure](transformssecure-policy.md) o la propiedad [**TransformsSecure**](transformssecure.md) , o bien haga que @ sea el primer carácter pasado en la lista de transformación. Cada transformación se debe indicar mediante un nombre de archivo y debe estar ubicada en la raíz del origen del paquete. Si alguna de las transformaciones no se encuentra en la raíz del origen del paquete, se produce un error en la instalación. Para obtener más información, vea [aplicar transformaciones](applying-transforms.md).

 

 



