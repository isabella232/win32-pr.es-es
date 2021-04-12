---
description: Una acción encapsula una función típica realizada durante la instalación o el mantenimiento de una aplicación. Windows Installer tiene muchas acciones estándar integradas. Los desarrolladores de paquetes de instalación también pueden crear sus propias acciones personalizadas.
ms.assetid: 33651988-e371-4258-96a7-bcd7d6762161
title: Acciones estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ed4f9c2a7fc6671442f6b72cd10889e2fcf5e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276368"
---
# <a name="standard-actions"></a>Acciones estándar

Una acción encapsula una función típica realizada durante la instalación o el mantenimiento de una aplicación. Windows Installer tiene muchas acciones estándar integradas. Los desarrolladores de paquetes de instalación también pueden crear sus propias [acciones personalizadas](custom-actions.md).

Algunos ejemplos de acciones estándar del instalador son:

-   [Acción CreateShortcuts](createshortcuts-action.md): administra la creación de accesos directos a los archivos que se instalan con la aplicación actual. Esta acción usa la [tabla de acceso directo](shortcut-table.md) para sus datos.
-   [InstallFiles Action](installfiles-action.md): copia los archivos seleccionados desde el directorio de origen en el directorio de destino. Esta acción utiliza la [tabla de archivos](file-table.md) para sus datos.
-   [Acción WriteRegistryValues](writeregistryvalues-action.md): configura la información del registro que la aplicación requiere en el registro. Esta acción utiliza la [tabla del registro](registry-table.md) para sus datos.

En las secciones siguientes se describen las acciones estándar.

-   [Acerca de las acciones estándar](about-standard-actions.md)
-   [Uso de acciones estándar](using-standard-actions.md)
-   [Referencia de acciones estándar](standard-actions-reference.md)

 

 



