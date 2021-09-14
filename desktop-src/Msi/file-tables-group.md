---
description: El grupo de archivos de tablas contiene todas las Windows del instalador que están relacionadas con los archivos.
ms.assetid: 8f56328e-ed58-41a1-94b6-266e9c117246
title: Grupo de tablas de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2667a1b9fe2bd9d2f8260523e2386bf7751dce8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074796"
---
# <a name="file-tables-group"></a>Grupo de tablas de archivos

![grupo de tablas de archivos](images/filegrp.png)

Para obtener más información sobre este diagrama, vea la leyenda del diagrama [de relación de entidad](entity-relationship-diagram-legend.md).

Un desarrollador de paquetes del instalador debe considerar la posibilidad [](components-and-features.md) de rellenar el grupo de tablas de tabla de archivos después de dividir la aplicación en componentes y características y después de rellenar el grupo de [tablas principales](core-tables-group.md). El grupo de tablas de archivos contiene todos los archivos que pertenecen a la instalación y la mayoría de estos archivos se enumeran en la [tabla Archivo](file-table.md). La [tabla Directory](directory-table.md) no se muestra en la ilustración, pero está estrechamente relacionada con el grupo de tablas de archivos. La tabla Directory proporciona la estructura de directorios de la instalación.

El grupo de archivos de tablas contiene todas las tablas relacionadas con los archivos.

-   En [la tabla Archivo](file-table.md) se enumeran los archivos que pertenecen a la instalación. Los archivos que no aparecen en la tabla Archivo incluyen archivos de disco, que se enumeran en la tabla Multimedia. Dado que cada archivo pertenece a un componente, la tabla File tiene una clave externa en la tabla Component.
-   La [tabla RemoveFile](removefile-table.md) contiene una lista de archivos que la acción [RemoveFiles](removefiles-action.md)va a quitar.
-   En [la tabla Fuente](font-table.md) se enumeran los archivos de fuente que se registrarán en el sistema.
-   En [la tabla SelfReg se](selfreg-table.md) enumeran los archivos de módulo de la instalación que se registran de forma automática.
-   En [la tabla Multimedia](media-table.md) se enumeran los discos y los medios de origen que pertenecen a la instalación.
-   En [la tabla BindImage se](bindimage-table.md) enumeran los archivos enlazados a archivos DLL importados por ejecutables.
-   La [tabla MoveFile especifica](movefile-table.md) qué archivos se mueven durante la instalación.
-   La [tabla DuplicateFile](duplicatefile-table.md) especifica qué archivos se duplican durante la instalación.
-   En [la tabla IniFile](inifile-table.md) se enumeran .ini archivos y la información que la aplicación debe establecer en el archivo.
-   La [tabla RemoveIniFile contiene](removeinifile-table.md) la información que una aplicación necesita eliminar de un .ini archivo.
-   La [tabla Entorno](environment-table.md) se usa para establecer los valores de las variables de entorno.
-   La [tabla Icono](icon-table.md) proporciona información de iconos que se copia en un archivo como parte del anuncio del producto.
-   La [tabla FileSFPCatalog asocia](filesfpcatalog-table.md) los archivos especificados a los archivos de catálogo de protección de archivos del sistema.

    **Windows Vista, Windows Server 2003 y Windows XP:** No se admite.

-   La [tabla SFPCatalog contiene](sfpcatalog-table.md) catálogos de protección de archivos del sistema.

    **Windows Vista, Windows Server 2003 y Windows XP:** No se admite.

-   La [tabla MsiFileHash](msifilehash-table.md) se usa para almacenar un hash de 128 bits de un archivo de origen proporcionado por el paquete Windows Installer.

 

 



