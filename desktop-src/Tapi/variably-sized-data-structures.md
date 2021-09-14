---
description: Cuando se usan estructuras de datos de tamaño variable para transmitir información entre TAPI y la aplicación, la aplicación es responsable de asignar la memoria necesaria.
ms.assetid: f1e2e864-fa10-4058-ba56-faa0ba7363a1
title: Estructuras de datos de tamaño variable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873fcbaa1e4e3bda772d92ad2de9b1f6258363cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068701"
---
# <a name="variably-sized-data-structures"></a>Estructuras de datos de tamaño variable

Cuando se usan estructuras de datos de tamaño variable para transmitir información entre TAPI y la aplicación, la aplicación es responsable de asignar la memoria necesaria. La cantidad de memoria asignada debe ser lo suficientemente grande como mínimo para la parte fija de la estructura de datos y la establece la aplicación en el miembro **dwTotalSize** de la estructura de datos. TAPI rellena los miembros **dwUsedSize** y **dwNeededSize.** Si **dwTotalSize** es menor que el tamaño de la parte fija, se devuelve LINEERR/PHONEERR \_ STRUCTURETOOSMALL. Si una función devuelve un resultado correcto, se han rellenado todos los campos de la parte fija. Los **miembros dwUsedSize** y **dwNeededSize** se pueden comparar para determinar si se han rellenado todas las partes variables y cuánto espacio se necesita para rellenarlas todas.

Si **dwNeededSize** es igual a **dwUsedSize**, se han rellenado todas las partes fijas y variables. Si **dwNeededSize** es mayor que **dwUsedSize**, es posible que se hayan rellenado algunas partes variables, pero no se ha definido exactamente en qué campos de tamaño variable se han rellenado. Nunca se trunca ninguna parte de variable y las partes variables que se hubieran truncado debido a un espacio insuficiente se indican al tener sus partes "Offset" y "Size" correspondientes establecidas en cero. Si no son cero (y no se devolvió ningún error), indican el desplazamiento y el tamaño de los datos válidos de la parte variable notruncated.

Una aplicación siempre puede garantizar que todas las partes variables se rellenan asignando e indicando bytes **dwNeededSize** para la estructura y llamando de nuevo a la función "Get" hasta que la función devuelve success y **dwNeededSize** es igual **a dwUsedSize.** Esto debe ocurrir en el segundo intento, excepto en el caso de las condiciones de carrera que provocan cambios en el tamaño de las partes variables entre llamadas, lo que debería ser una repetición poco frecuente.

> [!Note]  
> Todas las cadenas de texto, independientemente de la codificación, en estructuras de tamaño variable deben terminar en **NULL** según las convenciones normales de control de cadenas de C.

 

 

 



