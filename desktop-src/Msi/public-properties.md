---
description: Las propiedades públicas se pueden crear en la base de datos de instalación de la misma manera que las propiedades privadas.
ms.assetid: 032aa55f-d97a-4455-bd32-571b0e05763b
title: Propiedades públicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0138db2fcbe664ac9a4064379486c42c3d52a6896fc53a608b99192a8d70c75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828435"
---
# <a name="public-properties"></a>Propiedades públicas

Las propiedades públicas se pueden crear en la base de datos de instalación de la misma manera que [las propiedades privadas](private-properties.md). Además, un usuario o administrador del sistema puede cambiar los valores de las propiedades públicas estableciendo la propiedad en la línea de comandos, aplicando una transformación o interactuando con una interfaz de usuario autora. Los nombres de propiedad pública no pueden contener letras minúsculas. Vea [Restricciones en los nombres de propiedad.](restrictions-on-property-names.md)

Las propiedades públicas las establecen normalmente los usuarios durante la instalación. Por ejemplo, la propiedad [**pública INSTALLLEVEL**](installlevel.md) se puede especificar en la línea de comandos que se usa para iniciar la instalación o se elige mediante una interfaz de usuario de creación.

Los valores de propiedad pública se pueden invalidar [](standard-actions.md) en [](custom-actions.md) una línea de comandos, mediante una acción estándar o personalizada, aplicando una transformación o haciendo que el usuario interactúe con una interfaz de usuario autora. Para borrar una propiedad pública en la tabla de propiedades, déjela fuera de la tabla. Las propiedades que la interfaz de usuario va a establecer durante la instalación y, a continuación, pasar a la fase de ejecución de la instalación deben ser públicas.

Para obtener una lista de las propiedades públicas estándar utilizadas por el instalador, vea [Referencia de propiedad](property-reference.md). Un autor también puede definir una propiedad pública personalizada especificando el nombre de la propiedad y un valor inicial en la [tabla Property](property-table.md). Todos los usuarios pueden invalidar todas las propiedades públicas si se cumple alguna de las condiciones siguientes.

-   El usuario es un administrador del sistema.
-   La directiva EnableUserControl por equipo se establece en 1. Vea [Directiva del sistema](system-policy.md).
-   La [**propiedad EnableUserControl**](-enableusercontrol.md) se establece en 1.
-   Se trata de una instalación no administrada que no se realiza con privilegios elevados.

Si no se cumple ninguna de las condiciones anteriores, el instalador limita de forma predeterminada las propiedades públicas que puede reemplazar un usuario que no es un administrador del sistema. Vea [**Propiedades públicas restringidas.**](restricted-public-properties.md)

 

 



