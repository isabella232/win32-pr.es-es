---
description: Los tipos de calificador proporcionan más información sobre un calificador, como si una clase o instancia derivada puede invalidar el valor original de los calificadores.
ms.assetid: 6a0769ac-e16c-45e1-92b6-26e4969bf23d
ms.tgt_platform: multiple
title: Flavors de calificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a48c5ed3c7b695b19c182bcf05a9ce55b31b0bb94081570c58c8d55f7e48994c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050483"
---
# <a name="qualifier-flavors"></a>Flavors de calificador

Los tipos de calificador proporcionan más información sobre un calificador, como si una clase o instancia derivada puede invalidar el valor original del calificador.

Los tipos de calificador se pueden agregar a la parte superior del archivo MOF mediante la sintaxis siguiente, lo que hace que se apliquen a lo largo de la definición. Por ejemplo:

``` syntax
Qualifier Description : ToSubClass Amended;
```

Los **formatos ToSubClass** y **Amended** se aplican a todos los calificadores **Description** del MOF.

En la tabla siguiente se enumeran los tipos de calificador.



| Flavor del calificador    | Significado                                                                                                                                                                                                                                         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Modificado**         | El calificador no se requiere en la definición de clase básica y puede moverse a la modificación que se va a localizar.                                                                                                                                  |
| **DisableOverride** | El calificador no puede invalidarse en una clase o instancia derivada. Tenga en cuenta que el valor predeterminado es poder invalidar un calificador propagado.                                                                                                      |
| **EnableOverride**  | Cuando se propaga a una clase o instancia derivada, se puede invalidar el valor del calificador. La **configuración de EnableOverride** es opcional porque poder invalidar el valor del calificador es la funcionalidad predeterminada para los calificadores propagados. |
| **NotToInstance**   | El calificador no se propaga a instancias de clase.                                                                                                                                                                                             |
| **NotToSubClass**   | El calificador no se propaga a las clases derivadas.                                                                                                                                                                                             |
| **Restringido**      | El calificador no se propaga a instancias o clases derivadas.                                                                                                                                                                                |
| **ToInstance**      | El calificador se propaga a las instancias.                                                                                                                                                                                                       |
| **ToSubClass**      | El calificador se propaga a las clases derivadas. Este tipo solo es adecuado para los calificadores definidos para una clase y no se puede adjuntar a un calificador que describa una instancia de clase.                                                           |



 

 

 



