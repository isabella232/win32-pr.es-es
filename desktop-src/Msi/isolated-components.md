---
description: Los autores de paquetes de instalación pueden especificar que el instalador copie los archivos compartidos (archivos dll compartidos normalmente) de una aplicación en la carpeta de la aplicación en lugar de en una ubicación compartida.
ms.assetid: eb5f7088-30e0-4644-813a-c93e6f56ccbf
title: Componentes aislados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f29f614dfd819e093c5729a9a97a076247d281d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808738"
---
# <a name="isolated-components"></a>Componentes aislados

Los autores de paquetes de instalación pueden especificar que el instalador copie los archivos compartidos (archivos dll compartidos normalmente) de una aplicación en la carpeta de la aplicación en lugar de en una ubicación compartida. Este conjunto privado de archivos (dll) solo se usa en la aplicación. El aislamiento de la aplicación junto con sus componentes compartidos de esta manera presenta las siguientes ventajas:

-   La aplicación siempre usa las versiones de los archivos compartidos con los que se implementó.
-   La instalación de la aplicación no sobrescribe otras versiones de los archivos compartidos por otras aplicaciones.
-   Las instalaciones posteriores de otras aplicaciones que usan versiones diferentes de los archivos compartidos no pueden sobrescribir los archivos usados por esta aplicación.

Dado que la implementación actual de COM mantiene una única ruta de acceso completa en el registro para cada par de CLSID/contexto, obliga a todas las aplicaciones a usar la misma versión de un archivo DLL compartido. Para permitir que una aplicación mantenga una copia privada de un servidor COM, el cargador del sistema de Windows 2000 comprueba la presencia de un. Archivo LOCAL en la carpeta de la aplicación. Si el cargador del sistema detecta un. Archivo LOCAL, modifica la lógica de búsqueda para preferir archivos dll ubicados en la misma carpeta que la aplicación.

Cuando Windows Installer ejecuta la [acción IsolateComponents](isolatecomponents-action.md) , copia los archivos del componente (normalmente, un archivo dll compartido) especificados en la \_ columna compartida componente de la [tabla IsolatedComponent](isolatedcomponent-table.md) en la misma carpeta que el componente (normalmente, un archivo. exe) que se especifica en la \_ columna aplicación de componentes. El instalador crea un archivo en este directorio, de cero bytes de longitud y tiene el nombre corto de archivo del archivo de clave de la aplicación de componentes \_ (normalmente, el nombre es el mismo que el. exe de la aplicación) anexado con. Localizar. El instalador usa el registro para el componente en su ubicación compartida y no escribe información de registro para la copia del componente en la ubicación privada.

Para más información, consulte:

-   [Instalación de componentes aislados](installation-of-isolated-components.md)
-   [Reinstalación de componentes aislados](reinstallation-of-isolated-components.md)
-   [Eliminación de componentes aislados](removal-of-isolated-components.md)
-   [Usar componentes aislados](using-isolated-components.md)

 

 



