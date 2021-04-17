---
description: Los recursos necesarios para la personalización de una aplicación, como las plantillas corporativas, se pueden implementar con la aplicación mediante la inclusión de una transformación con el paquete de instalación de la aplicación.
ms.assetid: 3d9328d0-4d95-449c-bf2b-5487f7ba5971
title: Usar transformaciones para agregar recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c11fac7ad65601286fb550abd950bf5ac49af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677908"
---
# <a name="using-transforms-to-add-resources"></a>Usar transformaciones para agregar recursos

Los recursos necesarios para la personalización de una aplicación, como las plantillas corporativas, se pueden implementar con la aplicación mediante la inclusión de una transformación con el paquete de instalación de la aplicación. Se deben seguir las reglas siguientes al implementar recursos, como archivos, claves del registro o accesos directos, mediante una transformación.

-   La transformación debe agregar uno o varios componentes nuevos a la base de datos de instalación para que contenga los recursos adicionales. La transformación no debe agregar recursos a un componente que ya existe en la instalación de.
-   La transformación debe agregar una o varias características nuevas a la base de datos de instalación para que contenga estos componentes nuevos. Estas nuevas características no deben ser los elementos primarios de las características existentes, pero las nuevas características principales y secundarias se pueden introducir juntas. Las nuevas características deben tener nombres que sean únicos en todas las demás transformaciones de este producto. Dos transformaciones no deberían agregar una característica a este producto que tenga el mismo nombre que aparece en la columna característica de la [tabla de características](feature-table.md) y que contiene componentes o recursos diferentes.

 

 



