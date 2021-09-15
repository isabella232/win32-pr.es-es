---
description: Los recursos necesarios para la personalización de una aplicación, como las plantillas corporativas, se pueden implementar con la aplicación mediante la inclusión de una transformación con el paquete de instalación de la aplicación.
ms.assetid: 3d9328d0-4d95-449c-bf2b-5487f7ba5971
title: Uso de transformaciones para agregar recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c11fac7ad65601286fb550abd950bf5ac49af1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473915"
---
# <a name="using-transforms-to-add-resources"></a>Uso de transformaciones para agregar recursos

Los recursos necesarios para la personalización de una aplicación, como las plantillas corporativas, se pueden implementar con la aplicación mediante la inclusión de una transformación con el paquete de instalación de la aplicación. Se deben seguir las reglas siguientes al implementar recursos, como archivos, claves del Registro o accesos directos, mediante una transformación.

-   La transformación debe agregar uno o varios componentes nuevos a la base de datos de instalación para contener los recursos adicionales. La transformación no debe agregar recursos a un componente que ya existe en la instalación.
-   La transformación debe agregar una o varias características nuevas a la base de datos de instalación para que contenga estos nuevos componentes. Estas nuevas características no deben ser los elementos primarios de ninguna de las características existentes, pero las nuevas características primarias y secundarias pueden introducirse juntas. A las nuevas características se les deben dar nombres que sean únicos en todas las demás transformaciones de este producto. Ninguna de las dos transformaciones debe agregar nunca una característica a este [](feature-table.md) producto que tenga el mismo nombre enumerado en la columna Característica de la tabla Característica y que contenga distintos componentes o recursos.

 

 



