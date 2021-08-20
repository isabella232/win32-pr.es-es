---
description: Si es posible, la mejor manera de especificar la ubicación de destino de un directorio es crear la tabla de directorios en el paquete de instalación para proporcionar la ubicación correcta. Para obtener más información, vea Usar la tabla de directorios.
ms.assetid: 2d16e036-2d7f-431d-b646-1addf2f65f3f
title: Cambiar la ubicación de destino de un directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27adf952faeb4d37d5edb08a04bf25cc640d41e5d87732b30c80d25bba729705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145688"
---
# <a name="changing-the-target-location-for-a-directory"></a>Cambiar la ubicación de destino de un directorio

Si es posible, la mejor manera de especificar la [](directory-table.md) ubicación de destino de un directorio es crear la tabla de directorios en el paquete de instalación para proporcionar la ubicación correcta. Para obtener más información, [vea Usar la tabla de directorios](using-the-directory-table.md).

Si necesita cambiar la ubicación del directorio en el momento de la instalación, tiene las siguientes opciones:

-   Especifique la ubicación de un directorio estableciendo el valor de una [propiedad pública en](public-properties.md) la línea de comandos. Durante la [acción CostFinalize](costfinalize-action.md), las rutas de acceso de directorio internas usadas por el instalador se actualizan al valor de las propiedades enumeradas como claves en la [tabla de directorios](directory-table.md). Para obtener más información, [vea Usar propiedades y](using-properties.md) Establecer valores de propiedad pública en la línea de [comandos](setting-public-property-values-on-the-command-line.md).
-   Especifique la ubicación de un directorio mediante una acción personalizada. Si la acción personalizada se va a ejecutar antes de la acción [CostFinalize](costfinalize-action.md), puede usar un tipo de acción personalizada [51](custom-action-type-51.md) para establecer el valor de una propiedad a partir de una cadena de texto con formato. Si la acción personalizada se ejecuta después de la acción [CostFinalize](costfinalize-action.md), puede usar un tipo de acción personalizada [35](custom-action-type-35.md) para establecer el valor de la ruta de acceso del directorio a partir de una cadena de texto con formato. Las acciones personalizadas [](property-reference.md) que cambian una de las propiedades de carpeta del sistema deben incluirse en las tablas de secuencia de ejecución[(InstallExecuteSequence Table](installexecutesequence-table.md) o [AdminExecuteSequence Table)](adminexecutesequence-table.md) [](b-gly.md) y en las tablas de secuencias de la interfaz de usuario (Tabla[InstallUISequence](installuisequence-table.md) y [AdminUISequence Table)](adminuisequence-table.md)para que la carpeta se cambie durante las instalaciones de interfaz de usuario completa e interfaz de usuario básica. [](f-gly.md)
-   Si la instalación ejecuta una interfaz de usuario [*completa,*](f-gly.md)puede usar [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) o [SetTargetPath ControlEvent](settargetpath-controlevent.md) para establecer la ruta de acceso del directorio. Compruebe la [**propiedad ProductState**](productstate.md) para determinar si el producto que contiene este componente ya está instalado antes de llamar a **MsiSetTargetPath** o a SetTargetPath ControlEvent. No intente cambiar la ruta de acceso del directorio de destino si algunos componentes que usan esa ruta de acceso ya están instalados para el usuario actual o para otro usuario.

Las restricciones siguientes se aplican a todas las opciones anteriores:

-   No intente cambiar la ruta de acceso del directorio de destino si algunos componentes que usan la ruta de acceso ya están instalados para el usuario actual o para otro usuario.
-   No intente cambiar la ruta de acceso del directorio de destino durante una [instalación de mantenimiento](maintenance-installation.md).

 

 



