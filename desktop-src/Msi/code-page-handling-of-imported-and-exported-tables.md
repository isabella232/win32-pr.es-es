---
description: Puede agregar información de localización a una base de datos de instalación importando y exportando archivos de archivo de texto ASCII mediante MsiDatabaseExport y MsiDatabaseImport.
ms.assetid: dc52313b-38e7-43cc-abfd-86966c836fce
title: Control de páginas de códigos de tablas importadas y exportadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b090bead1fa35b451ed12e0e0da0143b98b8918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666686"
---
# <a name="code-page-handling-of-imported-and-exported-tables"></a>Control de páginas de códigos de tablas importadas y exportadas

Puede agregar información de localización a una base de datos de instalación importando y exportando archivos de archivo de texto ASCII mediante [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) y [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Dado que el grupo de cadenas de base de datos utiliza una página de códigos ANSI, los archivos de base de datos y de [archivo de texto](text-archive-files.md) exportado tienen páginas de códigos.

Cuando se exporta un [archivo de almacenamiento de texto](text-archive-files.md) desde una base de datos, la página de códigos del archivo de almacenamiento es la misma que la base de datos primaria. Para obtener una lista de páginas de códigos numéricas, consulte [localizar las tablas de error y ActionText](localizing-the-error-and-actiontext-tables.md).

> [!Note]  
> Exportar una tabla a un archivo de almacenamiento de texto traduce los caracteres de control para evitar conflictos con delimitadores de archivos.

 

## <a name="ascii-text-archive-files"></a>Archivos de archivo de texto ASCII

Los [archivos de almacenamiento de texto](text-archive-files.md) ASCII exportados por [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) se explican en el siguiente formato:

-   Los nombres de las columnas de la tabla se escriben en la primera línea.
-   Los formatos de columna se escriben en la segunda línea.
-   Si la tabla solo contiene datos ASCII, la tercera línea del archivo de texto es el nombre de la tabla seguido de una lista de las claves principales.
-   Si la tabla contiene datos que no son ASCII y la base de datos se marca con una página de códigos numérica, el número de la página de códigos aparece al principio de la tercera línea.
-   Si la base de datos contiene datos que no son ASCII, pero la base de datos no está marcada con la página de códigos numérica, el número de página de códigos del sistema actual se escribe al principio de la tercera línea.
-   Las líneas restantes del archivo de texto son los datos de la página de códigos especificada.
-   Si una tabla contiene secuencias, [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) exporta cada secuencia de la tabla a un archivo independiente.

### <a name="neutral-and-non-neutral-code-pages"></a>Páginas de códigos neutras y no neutras

Puede facilitar la localización iniciando con una base de datos que tenga una página de códigos neutra:

-   Una base de datos vacía tiene una página de códigos neutra.
-   Una base de datos que no contiene caracteres extendidos que requieren que una página de códigos se represente en ASCII tiene una página de códigos neutra.

Para obtener más información, vea [crear una base de datos con una página de códigos neutra](creating-a-database-with-a-neutral-code-page.md).

Las páginas de códigos neutras y no neutras tienen las siguientes características:

-   Si se importa un [archivo de texto](text-archive-files.md) con una página de códigos no neutra en una base de datos que tiene una página de códigos distinta de neutra, el instalador devuelve un error cuando se llama a [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) .
-   Un [archivo de texto](text-archive-files.md) que tiene una página de códigos neutra se puede importar en una base de datos que tiene cualquier página de códigos.
-   Un [archivo de almacenamiento de texto](text-archive-files.md) que tiene cualquier página de códigos se puede importar en una base de datos que tenga una página de códigos neutra.
-   Al importar un [archivo de texto](text-archive-files.md) en una base de datos con una página de códigos neutra, la página de códigos de la base de datos se establece en la página de códigos del archivo de almacenamiento. Todos los archivos de almacenamiento importados posteriormente en la base de datos deben tener la misma página de códigos que el primer archivo.

Para obtener más información, vea [determinar una página de códigos](determining-an-installation-database-s-code-page.md) [de la base de datos de instalación y establecer la página de códigos de una base de datos](setting-the-code-page-of-a-database.md).

Los [archivos de almacenamiento de texto](text-archive-files.md) exportados por [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) se pueden usar con sistemas de control de versiones. Utilice las [funciones de base](database-functions.md) de datos o un editor de tablas de base de datos para editar la base de datos.

Puede agregar información de localización a una base de datos de instalación mediante el editor de tablas de base de datos o la API de Windows Installer. Para obtener más información, vea [control de páginas de códigos de cadenas de parámetros](code-page-handling-of-parameter-strings.md).

 

 



