---
description: Los tipos de calificador proporcionan más información sobre un calificador, por ejemplo, si una clase derivada o una instancia pueden reemplazar el valor original de los calificadores.
ms.assetid: 6a0769ac-e16c-45e1-92b6-26e4969bf23d
ms.tgt_platform: multiple
title: Tipos de calificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8ddf6c2daea59931e533174c532e3d07b147a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707281"
---
# <a name="qualifier-flavors"></a>Tipos de calificador

Los tipos de calificador proporcionan más información sobre un calificador, por ejemplo, si una clase derivada o una instancia pueden reemplazar el valor original del calificador.

Se pueden agregar tipos de calificador a la parte superior del archivo MOF mediante la siguiente sintaxis, lo que hace que se apliquen a lo largo de la definición. Por ejemplo:

``` syntax
Qualifier Description : ToSubClass Amended;
```

La **ToSubClass** y los tipos **modificados** se aplican a todos los calificadores de **Descripción** del MOF.

En la tabla siguiente se enumeran los tipos de calificador.



| Tipo de calificador    | Significado                                                                                                                                                                                                                                         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Modifique**         | El calificador no se requiere en la definición de clase básica y puede moverse a la modificación que se va a localizar.                                                                                                                                  |
| **DisableOverride** | El calificador no puede invalidarse en una clase o instancia derivada. Tenga en cuenta que el valor predeterminado es poder invalidar un calificador propagado.                                                                                                      |
| **EnableOverride**  | Cuando se propagan a una clase derivada o una instancia, se puede invalidar el valor del calificador. Establecer **EnableOverride** es opcional porque poder invalidar el valor del calificador es la funcionalidad predeterminada para los calificadores propagados. |
| **NotToInstance**   | El calificador no se propaga a las instancias de clase.                                                                                                                                                                                             |
| **NotToSubClass**   | El calificador no se propaga a las clases derivadas.                                                                                                                                                                                             |
| **Restringido**      | El calificador no se propaga a instancias o clases derivadas.                                                                                                                                                                                |
| **ToInstance**      | El calificador se propaga a las instancias.                                                                                                                                                                                                       |
| **ToSubClass**      | El calificador se propaga a las clases derivadas. Este tipo solo es adecuado para los calificadores definidos para una clase y no se puede adjuntar a un calificador que describa una instancia de clase.                                                           |



 

 

 



