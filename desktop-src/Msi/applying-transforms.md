---
description: La propiedad TRANSFORMS contiene la lista de transformaciones para un paquete de instalación. El instalador aplica todas las transformaciones de la lista de transformaciones en cada instalación, anuncio, instalación a petición o instalación de mantenimiento del paquete.
ms.assetid: dde2ef55-7794-4eb1-984a-ed13e990c97f
title: Aplicar transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2367e02396ec33e517f8abfe579060c0a0986be2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159110"
---
# <a name="applying-transforms"></a>Aplicar transformaciones

La [**propiedad TRANSFORMS**](transforms.md) contiene la lista de transformaciones para un paquete de instalación. El instalador aplica todas las transformaciones de la lista de transformaciones en cada instalación, anuncio, instalación a petición o instalación de mantenimiento del paquete.

La [**propiedad TRANSFORMS**](transforms.md) se establece especificando la lista de transformaciones en la línea de comandos; sin embargo, cuando se usa la opción de línea de comandos /jm o [/ju](command-line-options.md), la lista de transformaciones debe especificarse mediante la opción /t.

Tenga en cuenta que la lista de transformaciones no se puede modificar una vez instalada y solo se puede quitar desinstalando la aplicación.

> [!Note]  
> Un Windows installer no puede aplicar más de 255 transformaciones al instalar una aplicación o actualización. Cuando se necesitan muchas transformaciones, se deben combinar y se deben eliminar las transformaciones obsoletas anteriores.

 

En la tabla siguiente se proporcionan ejemplos de varias cadenas de transformaciones que se podrían agregar a la lista de transformaciones.



| Cadena de transformaciones                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| transform1.mst;:transform2.mst;:transform3.mst                                                                                 | Transform2.mst y transform3.mst son [transformaciones incrustadas.](embedded-transforms.md) transform1.mst es [](secure-at-source-transforms.md) una transformación segura en origen solo si se establece la directiva [**TRANSFORMSSECURE**](transformssecure.md) o [TransformsSecure;](transformssecure-policy.md) de lo contrario, transform1 es una transformación no [segura.](unsecured-transforms.md) |
| \\\\ruta \\ de acceso del recurso compartido de servidor \\ \\ transform1.mst;:transform2.mst                                                                        | Transform2.mst es una [transformación incrustada.](embedded-transforms.md) transform1.mst es [](secure-full-path-transforms.md) una transformación de ruta de acceso completa segura solo si se establece la directiva [**TRANSFORMSSECURE**](transformssecure.md) o [TransformsSecure;](transformssecure-policy.md) de lo contrario, transform1 es una transformación no [segura.](unsecured-transforms.md)                   |
| @:transform2.mst;transform1.mst @transform1.mst ;:transform2.mst<br/>                                                     | Transform2.mst es una transformación incrustada. transform1.mst es una transformación segura en [origen independiente.](secure-at-source-transforms.md)                                                                                                                                                                                                                                                |
| \|\\\\ruta \\ de acceso del recurso compartido de servidor \\ \\ transform1.mst;:transform2.mst \| :transform2.mst; \\ \\ ruta \\ de acceso del recurso compartido de servidor \\ \\ transform1.mst<br/> | Transform2.mst es una transformación incrustada. transform1.mst es una transformación de ruta de acceso completa [segura independiente.](secure-full-path-transforms.md)                                                                                                                                                                                                                                                 |



 

 

 




