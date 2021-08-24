---
description: Las transformaciones de ruta de acceso completa segura deben tener un origen ubicado en la ruta de acceso completa especificada en la propiedad TRANSFORMS.
ms.assetid: 9c1cd6c5-d246-49d8-a632-991274bb4511
title: Transformaciones de ruta de acceso completa seguras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f55e16f40d99deceb8b625297cf447ebf5ec7dfb14a25518554804cf35b572e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040905"
---
# <a name="secure-full-path-transforms"></a>Transformaciones de ruta de acceso completa seguras

Las transformaciones de ruta de acceso completa segura deben tener un origen ubicado en la ruta de acceso completa especificada en la [**propiedad TRANSFORMS.**](transforms.md) Cuando el paquete se instala o se anuncia, el instalador guarda las transformaciones en una caché donde, en un sistema de archivos seguro, el usuario no tiene acceso de escritura. Si la copia local de la transformación deja de estar disponible, solo puede restaurar la memoria caché mediante la ruta de acceso especificada. La eliminación de un producto por parte de cualquier usuario quita todas las transformaciones seguras para ese producto del equipo del usuario.

Para aplicar transformaciones de rutas de acceso completas seguras durante la instalación de un paquete, establezca la directiva [TransformsSecure](transformssecure-policy.md) o la propiedad [**TRANSFORMSSECURE**](transformssecure.md) o haga que el primer carácter se pase en la lista \| de transformaciones. Las rutas de acceso completas al origen de cada transformación deben pasarse en la cadena de transformaciones. Si hay rutas de acceso relativas en la lista, se produce un error en la instalación. El origen de transformación no tiene que encontrarse con el origen del paquete.

 

 



