---
description: Los directorios de la tabla de directorio especifican el diseño de una instalación de.
ms.assetid: 59f6ae09-d013-46d7-a1a7-0543f31ac487
title: Usar una propiedad de directorio en una ruta de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2789f6442072f3db6a96c0abb7db301038673f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678460"
---
# <a name="using-a-directory-property-in-a-path"></a>Usar una propiedad de directorio en una ruta de acceso

Los directorios de la [tabla de directorio](directory-table.md) especifican el diseño de una instalación de. Cuando el Windows Installer resuelve estos directorios durante la [acción CostFinalize](costfinalize-action.md), las claves de la tabla de directorio se convierten en [propiedades](properties.md) establecidas en rutas de acceso de directorio. El instalador también establece siempre un número de [propiedades de carpeta del sistema](property-reference.md) estándar en las rutas de acceso a las carpetas del sistema.

Se garantiza que los valores de las propiedades de la [carpeta del sistema](property-reference.md) terminan en un separador de directorios. Solo se garantiza que los valores de todas las demás propiedades especificadas en la [tabla de directorio](directory-table.md) terminen en un separador de directorios después de que el instalador haya ejecutado la [acción CostFinalize](costfinalize-action.md). Antes de que se haya completado el costo, es posible que los valores de las propiedades especificadas en la tabla del directorio que no sean propiedades de la [carpeta del sistema](property-reference.md) no terminen en un separador de directorios. Por lo tanto, si la instalación establece las propiedades del directorio mediante [acciones personalizadas](custom-actions.md) en el paquete, los valores en referencia podrían no terminar con un separador de directorios.

Por lo tanto, las propiedades de directorio que finalizan con un separador de directorio se pueden usar en una cadena de ruta de acceso sin incluir explícitamente el separador de directorios. Por ejemplo, si el valor de DirectoryProperty termina con un separador de directorios, la cadena siguiente especifica correctamente la ruta de acceso al *archivo* en el *subdirectorio* .

``` syntax
[DirectoryProperty]subdirectory\file
```

y la cadena de ruta de acceso siguiente es incorrecta.

``` syntax
[DirectoryProperty]\subdirectory\file
```

 

 



