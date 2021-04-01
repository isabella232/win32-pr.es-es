---
description: La propiedad Transformations contiene la lista de transformaciones de un paquete de instalación. El instalador aplica todas las transformaciones en la lista de transformaciones en cada instalación, anuncio, instalación a petición o instalación de mantenimiento del paquete.
ms.assetid: dde2ef55-7794-4eb1-984a-ed13e990c97f
title: Aplicar transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2367e02396ec33e517f8abfe579060c0a0986be2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909094"
---
# <a name="applying-transforms"></a>Aplicar transformaciones

La propiedad [**TRANSformations**](transforms.md) contiene la lista de transformaciones de un paquete de instalación. El instalador aplica todas las transformaciones en la lista de transformaciones en cada instalación, anuncio, instalación a petición o instalación de mantenimiento del paquete.

La propiedad [**TRANSformations**](transforms.md) se establece especificando la lista de transformaciones en la línea de comandos. sin embargo, cuando se usa la opción de [línea de comandos](command-line-options.md)/JM o/Ju, se debe especificar la lista de transformaciones mediante la opción/t.

Tenga en cuenta que la lista de transformaciones no se puede modificar una vez instalada y solo se puede quitar desinstalando la aplicación.

> [!Note]  
> Un paquete Windows Installer no puede aplicar más de 255 transformaciones al instalar una aplicación o una actualización. Cuando se necesitan muchas transformaciones, se deben combinar y se deben eliminar las transformaciones obsoletas anteriores.

 

En la tabla siguiente se proporcionan ejemplos de varias cadenas de transformaciones que se pueden agregar a la lista de transformaciones.



| Cadena de transformaciones                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| transform1. MST;: transform2. MST;: transform3. MST                                                                                 | Transform2. MST y transform3. MST son [transformaciones incrustadas](embedded-transforms.md). transform1. MST es una [transformación segura en el código fuente](secure-at-source-transforms.md) solo si se establece la propiedad [**TRANSFORMSSECURE**](transformssecure.md) o la [Directiva TRANSFORMSSECURE](transformssecure-policy.md) , de lo contrario, transform1 es una [transformación no segura](unsecured-transforms.md). |
| \\\\Ruta de acceso del \\ recurso compartido del servidor \\ \\ transform1. MST;: transform2. MST                                                                        | Transform2. MST es una [transformación incrustada](embedded-transforms.md). transform1. MST es una [transformación de ruta de acceso completa y segura](secure-full-path-transforms.md) solo si se establece la propiedad [**TRANSFORMSSECURE**](transformssecure.md) o la [Directiva TRANSFORMSSECURE](transformssecure-policy.md) , de lo contrario transform1 es una [transformación no segura](unsecured-transforms.md).                   |
| @: transform2. MST; transform1. MST @transform1.mst ;: transform2. MST<br/>                                                     | Transform2. MST es una transformación incrustada. transform1. MST es una [transformación de seguridad en el origen](secure-at-source-transforms.md)independiente.                                                                                                                                                                                                                                                |
| \|\\\\Ruta de acceso del \\ recurso compartido del servidor \\ \\ transform1. MST;: transform2. MST \| : transform2. MST; \\ \\ Ruta de acceso del \\ recurso compartido del servidor \\ \\ transform1. MST<br/> | Transform2. MST es una transformación incrustada. transform1. MST es una [transformación de ruta de acceso completa y segura](secure-full-path-transforms.md)independiente.                                                                                                                                                                                                                                                 |



 

 

 




