---
description: WMI usa rutas de acceso a objetos en las propiedades de referencia de clases de asociación para identificar objetos relacionados, así como usar rutas de acceso de objeto en parámetros de entrada o salida para varios métodos.
ms.assetid: 07fee6f8-810e-4dec-8f0f-787756ee3beb
ms.tgt_platform: multiple
title: Requisitos de la ruta de acceso del objeto WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b46195eae3e8351c9c611a34c28cc9d5dd58d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172538"
---
# <a name="wmi-object-path-requirements"></a>Requisitos de la ruta de acceso del objeto WMI

WMI usa rutas de acceso a objetos en las propiedades de referencia de clases de asociación para identificar objetos relacionados, así como usar rutas de acceso de objeto en parámetros de entrada o salida para varios métodos. Dado que las rutas de acceso de objeto se tratan como cadenas con fines de búsqueda y comparación, el valor de una ruta de acceso de objeto cuando se usa como una propiedad de referencia siempre es la cadena en sí y no el objeto desreferenciado. Las comparaciones de cadenas que se tratan con las rutas de acceso de objeto siempre no tienen en cuenta las mayúsculas y minúsculas.

Una ruta de acceso de objeto puede usar la sintaxis siguiente:

-   Cadenas contenidas entre comillas simples.
-   Barras diagonales como separadores.
-   Barras diagonales inversas como separadores.
-   Constantes hexadecimales para enteros.
-   Constantes booleanas para clases con claves que toman valores booleanos.
-   Dirección URL para representar caracteres que no se imprimen, como %20 para un espacio en blanco.

Además, una cadena de ruta de acceso de objeto debe cumplir las restricciones siguientes:

-   Un servidor local asumido con una ruta de acceso de espacio de nombres parcial. Por lo tanto, especificar el espacio de nombres raíz y predeterminado implica el espacio de nombres raíz y predeterminado en el servidor local.
-   No hay ningún espacio en blanco dentro de un elemento o entre elementos.
-   Se permiten comillas incrustadas en rutas de acceso de objeto, pero deben delimitar la comilla con caracteres de escape, como en una aplicación de C o C++.
-   Solo los valores decimales se reconocen como partes numéricas de las claves.

 

 



