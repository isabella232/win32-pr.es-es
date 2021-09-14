---
description: Puede agregar información de localización a una base de datos de instalación importando y exportando archivos de archivo de texto ASCII mediante MsiDatabaseExport y MsiDatabaseImport.
ms.assetid: dc52313b-38e7-43cc-abfd-86966c836fce
title: Control de páginas de códigos de tablas importadas y exportadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b090bead1fa35b451ed12e0e0da0143b98b8918
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158895"
---
# <a name="code-page-handling-of-imported-and-exported-tables"></a>Control de páginas de códigos de tablas importadas y exportadas

Puede agregar información de localización a una base de datos de instalación importando y exportando archivos de archivo de texto ASCII mediante [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) [**y MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Dado que el grupo de cadenas de base de datos usa una página de códigos ANSI, tanto la base de datos como los archivos de archivo de [texto exportados](text-archive-files.md) tienen páginas de códigos.

Cuando se [exporta un archivo de archivo](text-archive-files.md) de texto desde una base de datos, la página de códigos del archivo de archivo es la misma que la base de datos primaria. Para obtener una lista de páginas de códigos numéricos, vea [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md).

> [!Note]  
> Al exportar una tabla a un archivo de archivo de texto, se traducen los caracteres de control para evitar conflictos con delimitadores de archivo.

 

## <a name="ascii-text-archive-files"></a>Archivos de archivo de texto ASCII

Los archivos [de archivo de texto ASCII](text-archive-files.md) exportados por [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) se explican en el siguiente formato:

-   Los nombres de las columnas de tabla se escriben en la primera línea.
-   Los formatos de columna se escriben en la segunda línea.
-   Si la tabla solo contiene datos ASCII, la tercera línea del archivo de texto es el nombre de la tabla seguido de una lista de las claves principales.
-   Si la tabla contiene datos que no son ASCII y la base de datos se marca con una página de códigos numérica, el número de página de códigos aparece al principio de la tercera línea.
-   Si la base de datos contiene datos que no son ASCII, pero la base de datos no se marca con la página de códigos numérica, el número de página de códigos del sistema actual se escribe al principio de la tercera línea.
-   Las líneas restantes del archivo de texto son los datos de la página de códigos especificada.
-   Si una tabla contiene secuencias, [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) exporta cada secuencia de la tabla a un archivo independiente.

### <a name="neutral-and-non-neutral-code-pages"></a>Páginas de códigos neutras y no neutras

Puede facilitar la localización empezando por una base de datos que tenga una página de códigos neutra:

-   Una base de datos en blanco tiene una página de códigos neutra.
-   Una base de datos que no contiene caracteres extendidos que requieren que una página de códigos se represente en ASCII tiene una página de códigos neutra.

Para obtener más información, vea [Crear una base de datos con una página de códigos neutra.](creating-a-database-with-a-neutral-code-page.md)

Las páginas de códigos neutras y no neutras tienen las siguientes características:

-   Si se [importa](text-archive-files.md) un archivo de archivo de texto con una página de códigos no neutra en una base de datos que tiene otra página de códigos no neutra, el instalador devuelve un error cuando se llama a [**MsiDatabaseImport.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
-   Un [archivo de archivo de texto](text-archive-files.md) que tenga una página de códigos neutra se puede importar a una base de datos que tenga cualquier página de códigos.
-   Un [archivo de archivo de texto](text-archive-files.md) que tenga cualquier página de códigos se puede importar a una base de datos que tenga una página de códigos neutra.
-   La importación de un [archivo de archivo de](text-archive-files.md) texto en una base de datos con una página de códigos neutra establece la página de códigos de la base de datos en la página de códigos del archivo de archivo. Todos los archivos de archivo importados posteriormente en la base de datos deben tener la misma página de códigos que el primer archivo.

Para obtener más información, vea [Determinar una página de códigos de base de datos de instalación](determining-an-installation-database-s-code-page.md) y Establecer la página de códigos de una base de [datos](setting-the-code-page-of-a-database.md).

Los [archivos de archivo de](text-archive-files.md) texto exportados por [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) se pueden usar con sistemas de control de versiones. Use funciones de [base de datos o](database-functions.md) un editor de tablas de base de datos para editar la base de datos.

Puede agregar información de localización a una base de datos de instalación mediante un editor de tablas de base de datos o la API Windows Installer. Para obtener más información, vea [Control de páginas de códigos de cadenas de parámetros.](code-page-handling-of-parameter-strings.md)

 

 



