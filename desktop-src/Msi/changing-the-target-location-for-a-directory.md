---
description: Si es posible, la mejor manera de especificar la ubicación de destino para un directorio es crear la tabla de directorio en el paquete de instalación para proporcionar la ubicación correcta. Para obtener más información, consulte uso de la tabla de directorios.
ms.assetid: 2d16e036-2d7f-431d-b646-1addf2f65f3f
title: Cambiar la ubicación de destino de un directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818c4e9d555244dd1637e19eb249478f13ea2d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276511"
---
# <a name="changing-the-target-location-for-a-directory"></a>Cambiar la ubicación de destino de un directorio

Si es posible, la mejor manera de especificar la ubicación de destino para un directorio es crear la [tabla de directorio](directory-table.md) en el paquete de instalación para proporcionar la ubicación correcta. Para obtener más información, consulte [uso de la tabla de directorios](using-the-directory-table.md).

Si necesita cambiar la ubicación del directorio en el momento de la instalación, tiene las siguientes opciones:

-   Especifique la ubicación de un directorio mediante el establecimiento del valor de una [propiedad pública](public-properties.md) en la línea de comandos. Durante la [acción CostFinalize](costfinalize-action.md), las rutas de acceso de directorio internas usadas por el instalador se actualizan al valor de las propiedades enumeradas como claves en la [tabla de directorios](directory-table.md). Para obtener más información, vea [usar propiedades](using-properties.md) y [establecer valores de propiedades públicas en la línea de comandos](setting-public-property-values-on-the-command-line.md).
-   Especifique la ubicación de un directorio mediante una acción personalizada. Si la acción personalizada se va a ejecutar antes de la [acción CostFinalize](costfinalize-action.md), puede usar un [tipo de acción personalizada 51](custom-action-type-51.md) para establecer el valor de una propiedad a partir de una cadena de texto con formato. Si la acción personalizada se ejecuta después de la [acción CostFinalize](costfinalize-action.md), puede usar un [tipo de acción personalizada 35](custom-action-type-35.md) para establecer el valor de la ruta de acceso del directorio a partir de una cadena de texto con formato. Las acciones personalizadas que cambian una de las propiedades de la [carpeta del sistema](property-reference.md) deben incluirse en las tablas de secuencia de ejecución (tabla [InstallExecuteSequence](installexecutesequence-table.md) o [AdminExecuteSequence](adminexecutesequence-table.md)), y en las tablas de secuencia de la interfaz de usuario (tabla [InstallUISequence](installuisequence-table.md) y tabla [AdminUISequence](adminuisequence-table.md)) para que la carpeta se cambie durante las instalaciones de IU [*completa*](f-gly.md) e interfaz de usuario [*básica*](b-gly.md) .
-   Si la instalación ejecuta una [*interfaz de usuario completa*](f-gly.md), puede usar [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) o [SetTargetPath ControlEvent,](settargetpath-controlevent.md) para establecer la ruta de acceso del directorio. Compruebe la propiedad [**ProductState**](productstate.md) para determinar si el producto que contiene este componente ya está instalado antes de llamar a **MsiSetTargetPath** o SetTargetPath ControlEvent,. No intente cambiar la ruta de acceso del directorio de destino si algunos componentes que usan esa ruta de acceso ya están instalados para el usuario actual o para otro usuario.

Las restricciones siguientes se aplican a todas las opciones anteriores:

-   No intente cambiar la ruta de acceso del directorio de destino si algunos componentes que utilizan la ruta de acceso ya están instalados para el usuario actual o para otro usuario.
-   No intente cambiar la ruta de acceso del directorio de destino durante una [instalación de mantenimiento](maintenance-installation.md).

 

 



