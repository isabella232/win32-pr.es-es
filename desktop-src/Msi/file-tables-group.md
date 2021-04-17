---
description: El grupo de archivos de tablas contiene todas las tablas de Windows Installer que están relacionadas con los archivos.
ms.assetid: 8f56328e-ed58-41a1-94b6-266e9c117246
title: Grupo de tablas de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2667a1b9fe2bd9d2f8260523e2386bf7751dce8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687185"
---
# <a name="file-tables-group"></a>Grupo de tablas de archivos

![Grupo de tablas de archivos](images/filegrp.png)

Para obtener más información sobre este diagrama, vea la [leyenda del diagrama de relaciones de entidades](entity-relationship-diagram-legend.md).

Un desarrollador de paquetes de instalador debe considerar la posibilidad de rellenar el grupo de tablas de archivos después de dividir la aplicación en [componentes y características](components-and-features.md) y después de rellenar el [grupo de tablas principales](core-tables-group.md). El grupo de tabla de archivos contiene todos los archivos que pertenecen a la instalación y la mayoría de estos archivos se enumeran en la [tabla de archivos](file-table.md). La [tabla de directorio](directory-table.md) no se muestra en la figura, pero está estrechamente relacionada con el grupo de tablas de archivos. La tabla del directorio proporciona la estructura de directorios de la instalación.

El grupo de archivos de tablas contiene todas las tablas que están relacionadas con los archivos.

-   La [tabla de archivos](file-table.md) muestra los archivos que pertenecen a la instalación. Los archivos que no aparecen en la tabla de archivos incluyen archivos de disco, que se enumeran en la tabla de medios. Dado que cada archivo pertenece a un componente, la tabla de archivos tiene una clave externa en la tabla de componentes.
-   La [tabla RemoveFile](removefile-table.md) contiene una lista de archivos que se van a quitar mediante la [acción RemoveFiles](removefiles-action.md).
-   La [tabla fuente](font-table.md) muestra los archivos de fuente que se van a registrar con el sistema.
-   En la [tabla SelfReg](selfreg-table.md) se muestran los archivos de módulo de la instalación que se han registrado automáticamente.
-   En la [tabla de medios](media-table.md) se enumeran los medios de origen y los discos que pertenecen a la instalación.
-   En la [tabla BindImage](bindimage-table.md) se muestran los archivos que están enlazados a archivos dll importados por ejecutables.
-   La [tabla MoveFile](movefile-table.md) especifica qué archivos se mueven durante la instalación.
-   La [tabla DuplicateFile](duplicatefile-table.md) especifica los archivos que se van a duplicar durante la instalación.
-   La [tabla inifile](inifile-table.md) enumera los archivos. ini y la información que la aplicación necesita para establecer en el archivo.
-   La [tabla RemoveIniFile](removeinifile-table.md) contiene la información que debe eliminar una aplicación de un archivo. ini.
-   La [tabla de entorno](environment-table.md) se utiliza para establecer los valores de las variables de entorno.
-   La [tabla de iconos](icon-table.md) proporciona información de iconos que se copia en un archivo como parte del anuncio del producto.
-   La [tabla FileSFPCatalog](filesfpcatalog-table.md) asocia los archivos especificados con los archivos de catálogo de protección de archivos del sistema.

    **Windows Vista, Windows Server 2003 y Windows XP:** No compatible.

-   La [tabla SFPCatalog](sfpcatalog-table.md) contiene catálogos de protección de archivos del sistema.

    **Windows Vista, Windows Server 2003 y Windows XP:** No compatible.

-   La [tabla MsiFileHash](msifilehash-table.md) se usa para almacenar un hash de 128 bits de un archivo de código fuente proporcionado por el paquete Windows Installer.

 

 



