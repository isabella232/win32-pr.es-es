---
description: WMI utiliza las rutas de acceso de objeto en las propiedades de referencia de las clases de Asociación para identificar los objetos relacionados, así como el uso de rutas de acceso de objeto en parámetros de entrada o de salida para varios métodos.
ms.assetid: 07fee6f8-810e-4dec-8f0f-787756ee3beb
ms.tgt_platform: multiple
title: Requisitos de ruta de objeto WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b46195eae3e8351c9c611a34c28cc9d5dd58d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423836"
---
# <a name="wmi-object-path-requirements"></a>Requisitos de ruta de objeto WMI

WMI utiliza las rutas de acceso de objeto en las propiedades de referencia de las clases de Asociación para identificar los objetos relacionados, así como el uso de rutas de acceso de objeto en parámetros de entrada o de salida para varios métodos. Dado que las rutas de acceso a objetos se tratan como cadenas con fines de búsqueda y comparación, el valor de una ruta de acceso de objeto cuando se usa como propiedad de referencia es siempre la cadena en sí y no el objeto desreferenciado. Las comparaciones de cadenas que tratan las rutas de acceso a objetos siempre no distinguen mayúsculas de minúsculas.

Una ruta de acceso de objeto puede utilizar la siguiente sintaxis:

-   Cadenas contenidas entre comillas simples.
-   Las barras diagonales como separadores.
-   Barras diagonales inversas como separadores.
-   Constantes hexadecimales para enteros.
-   Constantes booleanas para las clases con claves que toman valores booleanos.
-   Notación de dirección URL que representa caracteres no imprimibles, como %20 para un espacio en blanco.

Además, una cadena de ruta de acceso de objeto debe cumplir las restricciones siguientes:

-   Un servidor local asumido con una ruta de acceso de espacio de nombres parcial. Por lo tanto, la especificación del espacio de nombres raíz y predeterminado implica el espacio de nombres raíz y predeterminado en el servidor local.
-   Ningún espacio en blanco dentro de un elemento o entre elementos.
-   Se permiten las comillas incrustadas en las rutas de acceso del objeto, pero debe delimitar la comilla con los caracteres de escape, como en una aplicación de C o C++.
-   Solo los valores decimales se reconocen como partes numéricas de las claves.

 

 



