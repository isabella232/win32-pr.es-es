---
description: Las propiedades públicas se pueden crear en la base de datos de instalación de la misma manera que las propiedades privadas.
ms.assetid: 032aa55f-d97a-4455-bd32-571b0e05763b
title: Propiedades públicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822dfc55e0ab659e5580580edd04eb156540cb61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909473"
---
# <a name="public-properties"></a>Propiedades públicas

Las propiedades públicas se pueden crear en la base de datos de instalación de la misma manera que [las propiedades privadas](private-properties.md). Además, un usuario o un administrador del sistema puede cambiar los valores de las propiedades públicas mediante el establecimiento de la propiedad en la línea de comandos, la aplicación de una transformación o la interacción con una interfaz de usuario creada. Los nombres de propiedades públicas no pueden contener letras minúsculas. Vea [restricciones en los nombres de propiedad](restrictions-on-property-names.md).

Las propiedades públicas las establecen normalmente los usuarios durante la instalación. Por ejemplo, la propiedad [**INSTALLLEVEL**](installlevel.md) de la propiedad pública se puede especificar en la línea de comandos que se usa para iniciar la instalación o elegirse mediante una interfaz de usuario creada.

Los valores de propiedad pública se pueden reemplazar en una línea de comandos, mediante una acción [estándar](standard-actions.md) o [personalizada](custom-actions.md) , aplicando una transformación o haciendo que el usuario interactúe con una interfaz de usuario creada. Para borrar una propiedad pública en la tabla de propiedades, déjela fuera de la tabla. Las propiedades que va a establecer la interfaz de usuario durante la instalación y que después se pasan a la fase de ejecución de la instalación deben ser públicas.

Para obtener una lista de las propiedades públicas estándar que usa el instalador, vea [referencia de propiedades](property-reference.md). Un autor también puede definir una propiedad pública personalizada especificando el nombre de la propiedad y un valor inicial en la [tabla de propiedades](property-table.md). Todos los usuarios pueden invalidar todas las propiedades públicas si se cumple alguna de las siguientes condiciones.

-   El usuario es un administrador del sistema.
-   La Directiva EnableUserControl por equipo está establecida en 1. Consulte [Directiva del sistema](system-policy.md).
-   La propiedad [**EnableUserControl**](-enableusercontrol.md) se establece en 1.
-   Se trata de una instalación no administrada que no se realiza con privilegios elevados.

Si no se cumple ninguna de las condiciones anteriores, el instalador tiene como valor predeterminado la limitación de las propiedades públicas que un usuario que no es administrador del sistema puede reemplazar. Consulte [**propiedades públicas restringidas**](restricted-public-properties.md).

 

 



