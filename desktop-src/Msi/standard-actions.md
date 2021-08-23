---
description: Una acción encapsula una función típica realizada durante la instalación o el mantenimiento de una aplicación. Windows El instalador tiene muchas acciones estándar integradas. Los desarrolladores de paquetes de instalación también pueden crear sus propias acciones personalizadas.
ms.assetid: 33651988-e371-4258-96a7-bcd7d6762161
title: Acciones estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e95c3ab95a7bddc1f23dd38108b2cb10978ad5316da60397e6f3ba019a415ac4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627625"
---
# <a name="standard-actions"></a>Acciones estándar

Una acción encapsula una función típica realizada durante la instalación o el mantenimiento de una aplicación. Windows El instalador tiene muchas acciones estándar integradas. Los desarrolladores de paquetes de instalación también pueden crear sus [propias acciones personalizadas.](custom-actions.md)

Entre los ejemplos de acciones estándar del instalador se incluyen:

-   [Acción CreateShortcuts:](createshortcuts-action.md)administra la creación de accesos directos a los archivos instalados con la aplicación actual. Esta acción usa la [tabla Acceso directo](shortcut-table.md) para sus datos.
-   [Acción InstallFiles:](installfiles-action.md)copia los archivos seleccionados del directorio de origen al directorio de destino. Esta acción usa la [tabla File para](file-table.md) sus datos.
-   [Acción WriteRegistryValues:](writeregistryvalues-action.md)configura la información del Registro que la aplicación requiere en el Registro. Esta acción usa la [tabla Registry para](registry-table.md) sus datos.

En las secciones siguientes se deba a las acciones estándar.

-   [Acerca de las acciones estándar](about-standard-actions.md)
-   [Uso de acciones estándar](using-standard-actions.md)
-   [Referencia de acciones estándar](standard-actions-reference.md)

 

 



