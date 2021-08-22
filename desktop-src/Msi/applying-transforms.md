---
description: La propiedad TRANSFORMS contiene la lista de transformaciones de un paquete de instalación. El instalador aplica todas las transformaciones de la lista de transformaciones en cada instalación, anuncio, instalación a petición o instalación de mantenimiento del paquete.
ms.assetid: dde2ef55-7794-4eb1-984a-ed13e990c97f
title: Aplicación de transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daf6c1bd60a084b745df14d89772008867b618f3b21116ca20c5313747950b5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119264255"
---
# <a name="applying-transforms"></a>Aplicación de transformaciones

La [**propiedad TRANSFORMS**](transforms.md) contiene la lista de transformaciones de un paquete de instalación. El instalador aplica todas las transformaciones de la lista de transformaciones en cada instalación, anuncio, instalación a petición o instalación de mantenimiento del paquete.

La [**propiedad TRANSFORMS**](transforms.md) se establece especificando la lista de transformaciones en la línea de comandos; sin embargo, cuando se usa la opción de línea de comandos /jm o [/ju](command-line-options.md), la lista de transformaciones debe especificarse mediante la opción /t.

Tenga en cuenta que la lista de transformaciones no se puede modificar una vez instalada y solo se puede quitar desinstalando la aplicación.

> [!Note]  
> Un Windows installer no puede aplicar más de 255 transformaciones al instalar una aplicación o actualización. Cuando se necesitan muchas transformaciones, se deben combinar y se deben eliminar las transformaciones obsoletas anteriores.

 

En la tabla siguiente se proporcionan ejemplos de varias cadenas de transformaciones que se podrían agregar a la lista de transformaciones.



| Transforma la cadena                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| transform1.mst;:transform2.mst;:transform3.mst                                                                                 | Transform2.mst y transform3.mst son [transformaciones incrustadas.](embedded-transforms.md) transform1.mst es [](secure-at-source-transforms.md) una transformación segura en origen solo si se establece la propiedad [**TRANSFORMSSECURE**](transformssecure.md) o la directiva [TransformsSecure;](transformssecure-policy.md) de lo contrario, transform1 es una transformación no [segura.](unsecured-transforms.md) |
| \\\\ruta \\ de acceso del recurso compartido de servidor \\ \\ transform1.mst;:transform2.mst                                                                        | Transform2.mst es una [transformación incrustada.](embedded-transforms.md) transform1.mst es [](secure-full-path-transforms.md) una transformación de ruta de acceso completa segura solo si se establece la propiedad [**TRANSFORMSSECURE**](transformssecure.md) o la directiva [TransformsSecure;](transformssecure-policy.md) de lo contrario, transform1 es una transformación no [segura.](unsecured-transforms.md)                   |
| @:transform2.mst;transform1.mst @transform1.mst ;:transform2.mst<br/>                                                     | Transform2.mst es una transformación incrustada. transform1.mst es una transformación segura en [origen independiente.](secure-at-source-transforms.md)                                                                                                                                                                                                                                                |
| \|\\\\server \\ share \\ path \\ transform1.mst;:transform2.mst \| :transform2.mst; \\ \\ ruta \\ de acceso del recurso compartido de servidor \\ \\ transform1.mst<br/> | Transform2.mst es una transformación incrustada. transform1.mst es una transformación de ruta de acceso completa [segura independiente.](secure-full-path-transforms.md)                                                                                                                                                                                                                                                 |



 

 

 




