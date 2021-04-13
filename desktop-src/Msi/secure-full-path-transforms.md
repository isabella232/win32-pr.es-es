---
description: Las transformaciones de ruta de acceso completa y segura deben tener un origen ubicado en la ruta de acceso completa especificada en la propiedad Transformations.
ms.assetid: 9c1cd6c5-d246-49d8-a632-991274bb4511
title: Transformaciones de ruta de acceso completas seguras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8a60cf30beffe3831ed6489ea3827124ae319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547094"
---
# <a name="secure-full-path-transforms"></a>Transformaciones de ruta de acceso completas seguras

Las transformaciones de ruta de acceso completa y segura deben tener un origen ubicado en la ruta de acceso completa especificada en la propiedad [**TRANSformations**](transforms.md) . Cuando el paquete se instala o se anuncia, el instalador guarda las transformaciones en una memoria caché donde, en un sistema de archivos seguro, el usuario no tiene acceso de escritura. Si la copia local de la transformación deja de estar disponible, solo puede restaurar la memoria caché mediante la ruta de acceso especificada. La eliminación de un producto por parte de un usuario quita todas las transformaciones seguras para ese producto del equipo del usuario.

Para aplicar transformaciones de rutas de acceso completas y seguras en la instalación de un paquete, establezca la [Directiva TransformsSecure](transformssecure-policy.md) o la propiedad [**TransformsSecure**](transformssecure.md) o haga que \| el primer carácter se pase en la lista de transformación. Las rutas de acceso completas al origen de cada transformación se deben pasar en la cadena de transformaciones. Si alguna de las rutas de acceso relativas está en la lista, se produce un error en la instalación. No es necesario que el origen de la transformación se encuentre con el origen del paquete.

 

 



