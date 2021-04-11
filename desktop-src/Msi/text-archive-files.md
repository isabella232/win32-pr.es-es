---
description: Las tablas de base de datos de Windows Installer se pueden exportar a archivos de texto ASCII mediante MsiDatabaseExport o el método Export del objeto Database.
ms.assetid: 49210242-bd32-4e5c-b782-a132d670fdfe
title: Archivos de archivo de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8baba814fd182a7da5e13fbb26eec257be96ab1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910362"
---
# <a name="text-archive-files"></a>Archivos de archivo de texto

Las tablas de base de datos de Windows Installer se pueden exportar a archivos de texto ASCII mediante [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) o el método [**Export**](database-export.md) del objeto [**Database**](database-object.md) . La información de estos archivos de almacenamiento de texto se puede volver a importar a una base de datos de Windows Installer mediante [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) o el método de [importación](database-import.md) del objeto de **base de datos** .

Herramientas como [msidb.exe](msidb-exe.md) son capaces de exportar e importar archivos de almacenamiento de texto. Vea [exportar archivos](export-files.md) e [importar archivos](import-files.md) para obtener [Windows Installer ejemplos de scripting](windows-installer-scripting-examples.md) que pueden exportar e importar archivos de almacenamiento de texto desde una base de datos.

> [!Note]  
> Los archivos de archivo de texto no están diseñados como un medio para editar la base de datos de instalación. Debe utilizar una herramienta de edición de tablas Windows Installer, como [Orca](orca-exe.md) o una herramienta de terceros, para crear y modificar un paquete de instalación.

 

Los archivos de texto se pueden usar para los siguientes fines.

-   Los archivos de archivo de texto se pueden usar con sistemas de control de versiones.
-   Para quitar el espacio de almacenamiento desperdiciado y reducir el tamaño final de los archivos. msi. Consulte [reducir el tamaño de un archivo. msi](reducing-the-size-of-an--msi-file.md).
-   Para agregar información de localización a una base de datos de instalación. Para obtener más información, vea [control de páginas de códigos de tablas importadas y exportadas](code-page-handling-of-imported-and-exported-tables.md).

-   Para determinar la página de códigos de una base de datos. Consulte [determinación de la página de códigos de una base de datos de instalación](determining-an-installation-database-s-code-page.md).
-   Para establecer la página de códigos de una base de datos. Vea [establecer la página de códigos de una base de datos](setting-the-code-page-of-a-database.md).
-   Para aumentar el límite de una columna de base de datos. Exporte la tabla mediante [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), edite el archivo. IDT exportado y, a continuación, importe la tabla con [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Los autores no pueden cambiar los tipos de datos de columna, la nulabilidad o los atributos de localización de las columnas de las tablas estándar. Vea también [crear un paquete de gran tamaño](authoring-a-large-package.md).

En las páginas siguientes se describen las páginas de archivo de texto y sus formatos.

-   [Formato de archivo de almacenamiento](archive-file-format.md)
-   [Datos ASCII en archivos de almacenamiento de texto](ascii-data-in-text-archive-files.md)
-   [\_ForceCodepage](-forcecodepage.md)
-   [\_SummaryInformation](-summaryinformation.md)

 

 



