---
description: WMI usa rutas de acceso a objetos en las propiedades de referencia de las clases de asociación para identificar objetos relacionados, así como usar rutas de acceso de objeto en parámetros de entrada o salida para varios métodos.
ms.assetid: 07fee6f8-810e-4dec-8f0f-787756ee3beb
ms.tgt_platform: multiple
title: Requisitos de la ruta de acceso del objeto WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d278ece21840c019ae9747926dcd513f0fd1a2fcd59c408ecd8614fc19efeed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117921123"
---
# <a name="wmi-object-path-requirements"></a>Requisitos de la ruta de acceso del objeto WMI

WMI usa rutas de acceso a objetos en las propiedades de referencia de las clases de asociación para identificar objetos relacionados, así como usar rutas de acceso de objeto en parámetros de entrada o salida para varios métodos. Dado que las rutas de acceso de objeto se tratan como cadenas para la búsqueda y la comparación, el valor de una ruta de acceso de objeto cuando se usa como propiedad de referencia siempre es la propia cadena y no el objeto desreferenciado. Las comparaciones de cadenas que se tratan con rutas de acceso de objeto siempre no tienen en cuenta mayúsculas de minúsculas.

Una ruta de acceso de objeto puede usar la sintaxis siguiente:

-   Cadenas contenidas entre comillas simples.
-   Barras diagonales como separadores.
-   Barras diagonales inversas como separadores.
-   Constantes hexadecimales para enteros.
-   Constantes booleanas para clases con claves que toman valores booleanos.
-   La notación de dirección URL para representar caracteres que no son de impresión, como %20 para un espacio en blanco.

Además, una cadena de ruta de acceso de objeto debe cumplir las restricciones siguientes:

-   Un servidor local asumido con una ruta de acceso de espacio de nombres parcial. Por lo tanto, especificar el espacio de nombres raíz y predeterminado implica el espacio de nombres raíz y predeterminado en el servidor local.
-   No hay ningún espacio en blanco dentro de un elemento o entre elementos.
-   Se permiten comillas incrustadas en rutas de acceso de objeto, pero deben delimitar las comillas con caracteres de escape, como en una aplicación de C o C++.
-   Solo los valores decimales se reconocen como partes numéricas de las claves.

 

 



