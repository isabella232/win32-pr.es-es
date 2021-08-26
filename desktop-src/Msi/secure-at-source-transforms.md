---
description: Las transformaciones de seguridad en origen deben tener un origen ubicado en la raíz del origen del paquete.
ms.assetid: b5355053-9922-444f-a117-f6af461ef9e9
title: Transformaciones seguras en origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f591e6f30c11ec9fa7edf2f943ef1f660a0a3b12ff87c3c1de0984328652565b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041005"
---
# <a name="secure-at-source-transforms"></a>Transformaciones seguras en origen

Las transformaciones de seguridad en origen deben tener un origen ubicado en la raíz del origen del paquete. Cuando se instala o anuncia el paquete, el instalador guarda las transformaciones en una caché donde, en un sistema de archivos seguro, el usuario no tiene acceso de escritura. Si la copia local de la transformación deja de estar disponible, el instalador busca un origen para restaurar la memoria caché. El método es el mismo que buscar en la lista de origen un .msi archivo. Para obtener más información, vea [Resistencia de origen.](source-resiliency.md) La eliminación de un producto por parte de cualquier usuario quita todas las transformaciones seguras para ese producto del equipo del usuario.

Para aplicar transformaciones seguras en el origen durante la instalación de un paquete, establezca la directiva [TransformsSecure](transformssecure-policy.md) o la propiedad [**TRANSFORMSSECURE,**](transformssecure.md) o bien haga que @ sea el primer carácter pasado en la lista de transformaciones. Cada transformación debe estar indicada por un nombre de archivo y debe encontrarse en la raíz del origen del paquete. Si alguna de las transformaciones no se encuentra en la raíz del origen del paquete, se produce un error en la instalación. Para obtener más información, [vea Aplicar transformaciones.](applying-transforms.md)

 

 



