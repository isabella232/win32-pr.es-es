---
title: Ejemplos de cambios incompatibles
description: 'Cuando se trabaja con cambios incompatibles, la regla de control desafortunada es la siguiente: cualquier cambio puede ser incompatible con las versiones anteriores, a menos que sea muy bien entendido.'
ms.assetid: 5b893d79-b81d-4ede-8d49-71d85219c497
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9498e5c71c7ce9690da0969f234fbb9d094eca50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075877"
---
# <a name="examples-of-incompatible-changes"></a>Ejemplos de cambios incompatibles

Cuando se trabaja con cambios incompatibles, la regla de control de posición desafortunada es la siguiente: cualquier cambio puede ser incompatible con versiones anteriores, a menos que sea muy bien entendido. Esta regla requiere conocimiento de las reglas de NDR. Si no sabe cuál es el NDR, no realice modificaciones. Los ejemplos de cambios que normalmente producen una infracción de acceso en la aplicación, o una \_ excepción de datos de código auxiliar incorrecta \_ \_ generada por el motor de serialización, son las siguientes:

-   Agregar un nuevo método en medio de métodos antiguos.
-   Agregar o quitar parámetros de un método.
-   Cambiar un atributo, por ejemplo un atributo de puntero: cambiar \[ ref \] a \[ Unique \] o PTR, \[ \] o viceversa. Cada tipo de puntero tiene una representación de conexión diferente.
-   Cambiar el tamaño de los datos: de Short a Long, de char a WCHAR \_ t (Unicode), la adición de un campo a una estructura y el cambio del tamaño de una matriz de tamaño fijo.
-   Agregar brazos de unión a una unión con una cláusula default.

Algunos cambios dañinos o discrepancias no deseadas entre un cliente y un servidor se pueden producir de la manera siguiente:

-   Modificar un miembro de un tipo compuesto, como una estructura o una matriz. Por ejemplo, si un \_ identificador de cliente cambia de un entero a un GUID, una \_ estructura de registros de cliente con el \_ campo ID. de cliente es incompatible. Esto puede resultar difícil de detectar si está en cascada a través de varios niveles de inserción en un tipo de parámetro remoto real.
-   Modificar un tipo importado. Es posible que el tipo proceda de un componente diferente que no sea remoto directamente, por lo que se consideró que el cambio era compatible.
-   \#El uso de ifdef en un archivo IDL es una idea mala de las definiciones de tipo en un archivo IDL, es un desastre en espera de producirse. Inevitablemente, debido a la compilación u otros problemas, un cliente se compila con un conjunto diferente de definiciones que el servidor y acaba siendo incompatible.

 

 




