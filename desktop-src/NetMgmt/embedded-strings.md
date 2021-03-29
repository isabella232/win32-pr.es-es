---
title: Cadenas incrustadas
description: Las estructuras de información no contendrán cadenas insertadas. Esto mejora la alineación de las estructuras de información y permite la flexibilidad del OEM en las funciones principales.
ms.assetid: a3272a0a-5352-4847-84fd-113b4467c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c71ed50971661f9ad06855024ecba2796f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777113"
---
# <a name="embedded-strings"></a>Cadenas incrustadas

Las estructuras de información no contendrán cadenas insertadas. Esto mejora la alineación de las estructuras de información y permite la flexibilidad del OEM en las funciones principales.

Se garantiza que todos los campos de información que se devuelven en una llamada de enumeración que se pueden usar posteriormente como clave para la llamada a una función de administración de red GetInfo están presentes en el búfer de enumeración. Si la cadena de información de longitud variable que especificaría el valor del campo de clave no cabe, no se devolverá toda la estructura de longitud fija de la entrada. Otros campos de longitud variable se devolverán como un puntero **nulo** para el caso en el que la cadena no cabe.

 

 




