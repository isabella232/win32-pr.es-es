---
title: Ejemplos de cambios incompatibles
description: 'Cuando se trabaja con cambios incompatibles, la regla general es la siguiente: cualquier cambio puede ser incompatible con versiones anteriores, a menos que se entienda muy bien.'
ms.assetid: 5b893d79-b81d-4ede-8d49-71d85219c497
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a8736093e8189570026489bc1753145b941b7429b704e2c9c68783ddefef0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930044"
---
# <a name="examples-of-incompatible-changes"></a>Ejemplos de cambios incompatibles

Cuando se trabaja con cambios incompatibles, la regla general desafortunada es la siguiente: cualquier cambio puede ser incompatible con versiones anteriores, a menos que se entienda muy bien. Esta regla requiere conocimientos de las reglas de BAND. Si no sabe cuál es el BAND, no realice modificaciones. A continuación se muestran ejemplos de cambios que suelen dar lugar a una infracción de acceso en la aplicación o una EXCEPCIÓn DE DATOS DE CÓDIGO AUXILIAR NO DESEADOs que genera el motor de \_ \_ \_ serialización:

-   Agregar un nuevo método en medio de métodos antiguos.
-   Agregar o quitar parámetros de un método.
-   Cambiar un atributo, por ejemplo un atributo de puntero: cambiar ref a \[ \] \[ \] unique, \[ ptr \] o viceversa. Cada tipo de puntero tiene una representación de conexión diferente.
-   Cambiar el tamaño de los datos: de short a long, de char a wchar t (Unicode), agregar un campo a una estructura y cambiar el tamaño de una matriz \_ de tamaño fijo.
-   Agregar los escudos de unión a una unión con una cláusula predeterminada.

Algunos cambios insidiosos o discrepancias involuntarias entre un cliente y un servidor pueden producirse de la siguiente manera:

-   Modificar un miembro de un tipo compuesto, como una estructura o una matriz. Por ejemplo, si un identificador de cliente cambia de un entero a un GUID, una estructura CLIENT RECORD con el campo ID de CLIENTE \_ \_ se vuelve \_ incompatible. Esto puede ser difícil de detectar si se inserta en cascada a través de varios niveles de inserción en un tipo de parámetro remoto real.
-   Modificar un tipo importado. El tipo puede ser procedente de un componente diferente que no es remoto directamente, por lo que se ha pensado que el cambio es compatible.
-   Usar ifdef en un archivo IDL es una mala idea para las definiciones de tipo ifdef en un archivo IDL: es un desastre \# esperar a que suceda. Inevitablemente, debido a la compilación u otros problemas, un cliente se compila con un conjunto diferente de define que el servidor y terminan siendo incompatibles.

 

 




