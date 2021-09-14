---
description: Los autores de paquetes de instalación pueden especificar que el instalador copie los archivos compartidos (archivos DLL compartidos normalmente) de una aplicación en la carpeta de esa aplicación en lugar de en una ubicación compartida.
ms.assetid: eb5f7088-30e0-4644-813a-c93e6f56ccbf
title: Componentes aislados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f29f614dfd819e093c5729a9a97a076247d281d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071999"
---
# <a name="isolated-components"></a>Componentes aislados

Los autores de paquetes de instalación pueden especificar que el instalador copie los archivos compartidos (archivos DLL compartidos normalmente) de una aplicación en la carpeta de esa aplicación en lugar de en una ubicación compartida. Este conjunto privado de archivos (DLL) solo lo usa la aplicación. Aislar la aplicación junto con sus componentes compartidos de esta manera tiene las siguientes ventajas:

-   La aplicación siempre usa las versiones de los archivos compartidos con los que se implementó.
-   La instalación de la aplicación no sobrescribe otras versiones de los archivos compartidos por otras aplicaciones.
-   Las instalaciones posteriores de otras aplicaciones que usan versiones diferentes de los archivos compartidos no pueden sobrescribir los archivos usados por esta aplicación.

Dado que la implementación actual de COM mantiene una única ruta de acceso completa en el Registro para cada par CLSID/Context, obliga a todas las aplicaciones a usar la misma versión de un archivo DLL compartido. Para permitir que una aplicación conserve una copia privada de un servidor COM, el cargador del sistema en Windows 2000 comprueba la presencia de . Archivo LOCAL en la carpeta de la aplicación. Si el cargador del sistema detecta un . Archivo LOCAL, modifica su lógica de búsqueda para preferir archivos DLL ubicados en la misma carpeta que la aplicación.

Cuando Windows Installer ejecuta la acción [IsolateComponents,](isolatecomponents-action.md) copian los archivos del componente (normalmente un archivo DLL compartido) especificado en la columna Component Shared de la tabla \_ [IsolatedComponent](isolatedcomponent-table.md) en la misma carpeta que el componente (normalmente un archivo .exe) especificado en la columna Aplicación \_ de componentes. El instalador crea un archivo en este directorio, con una longitud de cero bytes, con el nombre de archivo corto del archivo de clave para la aplicación de componentes (normalmente el nombre es el mismo que el de la aplicación .exe) anexado \_ a . LOCAL. El instalador usa el registro del componente en su ubicación compartida y no escribe ninguna información de registro para la copia del componente en la ubicación privada.

Para más información, consulte:

-   [Instalación de componentes aislados](installation-of-isolated-components.md)
-   [Reinstalación de componentes aislados](reinstallation-of-isolated-components.md)
-   [Eliminación de componentes aislados](removal-of-isolated-components.md)
-   [Uso de componentes aislados](using-isolated-components.md)

 

 



