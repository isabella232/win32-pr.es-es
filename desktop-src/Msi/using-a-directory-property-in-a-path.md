---
description: Los directorios de la tabla Directory especifican el diseño de una instalación.
ms.assetid: 59f6ae09-d013-46d7-a1a7-0543f31ac487
title: Usar una propiedad de directorio en una ruta de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2789f6442072f3db6a96c0abb7db301038673f83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069587"
---
# <a name="using-a-directory-property-in-a-path"></a>Usar una propiedad de directorio en una ruta de acceso

Los directorios de la [tabla Directory especifican](directory-table.md) el diseño de una instalación. Cuando el instalador Windows resuelve estos directorios durante la acción [CostFinalize](costfinalize-action.md), [](properties.md) las claves de la tabla Directory se convierten en propiedades establecidas en rutas de acceso de directorio. El instalador también siempre establece una serie de propiedades de [carpetas](property-reference.md) del sistema estándar en las rutas de acceso de carpeta del sistema.

Se garantiza que los valores [de las propiedades de la carpeta del](property-reference.md) sistema terminan en un separador de directorios. Solo se garantiza que los valores de todas las demás propiedades especificadas en la tabla [Directory](directory-table.md) terminen en un separador de directorios después de que el instalador haya ejecutado [la acción CostFinalize](costfinalize-action.md). Antes de que se complete el costo, es posible que los valores de las propiedades especificadas en la tabla Directorio que no son Propiedades de carpeta del [sistema](property-reference.md) no terminen en un separador de directorios. Por lo tanto, si [](custom-actions.md) la instalación establece propiedades de directorio mediante acciones personalizadas en el paquete, es posible que los valores de referencia no terminen con un separador de directorios.

Por lo tanto, las propiedades de directorio que terminan con un separador de directorios se pueden usar en una cadena de ruta de acceso sin incluir explícitamente el separador de directorios. Por ejemplo, si el valor de DirectoryProperty termina con un separador de directorios, la siguiente cadena especifica correctamente la ruta de acceso al archivo *en* *el subdirectorio*

``` syntax
[DirectoryProperty]subdirectory\file
```

y la siguiente cadena de ruta de acceso es incorrecta.

``` syntax
[DirectoryProperty]\subdirectory\file
```

 

 



