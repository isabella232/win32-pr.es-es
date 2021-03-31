---
description: Cuando se usan estructuras de datos de tamaño variable para transmitir información entre TAPI y la aplicación, la aplicación es responsable de asignar la memoria necesaria.
ms.assetid: f1e2e864-fa10-4058-ba56-faa0ba7363a1
title: Estructuras de datos de tamaño variable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873fcbaa1e4e3bda772d92ad2de9b1f6258363cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278557"
---
# <a name="variably-sized-data-structures"></a>Estructuras de datos de tamaño variable

Cuando se usan estructuras de datos de tamaño variable para transmitir información entre TAPI y la aplicación, la aplicación es responsable de asignar la memoria necesaria. La cantidad de memoria asignada debe ser lo suficientemente grande como para la parte fija de la estructura de datos y la establece la aplicación en el miembro **dwTotalSize** de la estructura de datos. Los miembros **dwUsedSize** y **dwNeededSize** se rellenan con TAPI. Si **dwTotalSize** es menor que el tamaño de la parte fija, se devuelve LINEERR/PHONEERR \_ STRUCTURETOOSMALL. Si una función devuelve Success, se han rellenado todos los campos de la parte fija. Los miembros **dwUsedSize** y **dwNeededSize** pueden compararse para determinar si se han rellenado todas las partes variables y cuánto espacio se necesitaría para rellenarlos todo en.

Si **dwNeededSize** es igual a **dwUsedSize**, se han rellenado todos los elementos fijos y variables. Si **dwNeededSize** es mayor que **dwUsedSize**, es posible que se hayan rellenado algunas partes variables, pero que los campos de tamaño de variable se hayan rellenado no estén definidos. Ninguna parte variable se trunca nunca y las partes variables que se habrían truncado debido a la falta de espacio se indican al tener las partes de "desplazamiento" y "tamaño" correspondientes establecidas en cero. Si no son cero (y no se devolvió ningún error), indican el desplazamiento y el tamaño de los datos de partes variables no truncados válidos.

Una aplicación siempre puede garantizar que todas las partes variables se rellenan asignando e indicando **dwNeededSize** bytes para la estructura y llamando a la función "Get" hasta que la función devuelve Success y **dwNeededSize** es igual a **dwUsedSize**. Esto debe ocurrir en el segundo intento excepto en las condiciones de carrera que producen cambios en el tamaño de las partes variables entre las llamadas, que deben ser una situación poco frecuente.

> [!Note]  
> Todas las cadenas de texto, independientemente de la codificación, en las estructuras de tamaño de variable deben terminar en **null** según las convenciones normales de control de cadenas de C.

 

 

 



