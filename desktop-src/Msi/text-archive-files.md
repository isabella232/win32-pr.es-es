---
description: Las Windows de base de datos del instalador se pueden exportar a archivos de texto ASCII mediante MsiDatabaseExport o el método Export del objeto Database.
ms.assetid: 49210242-bd32-4e5c-b782-a132d670fdfe
title: Archivos de archivo de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc232f5523613d62ca595ec55983aeaf9cee8d67408a66b7afb609fa75b69125
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626425"
---
# <a name="text-archive-files"></a>Archivos de archivo de texto

Las Windows de base de datos del instalador se pueden exportar a archivos de texto ASCII mediante [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) o el método [**Export**](database-export.md) del [**objeto Database.**](database-object.md) La información de estos archivos de archivo de texto se puede volver a importar en una base de datos Windows Installer mediante [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) o el método [Import](database-import.md) del **objeto Database.**

Herramientas como [msidb.exe](msidb-exe.md) pueden exportar e importar archivos de archivo de texto. Vea [Export Files](export-files.md) and Import [Files](import-files.md) for Windows Installer Scripting Examples that can export and import text archive files from a database (Exportar archivos e importar archivos para Windows ejemplos de scripting del instalador [que](windows-installer-scripting-examples.md) pueden exportar e importar archivos de archivo de texto desde una base de datos).

> [!Note]  
> Los archivos de archivo de texto no están pensados como medio para editar la base de datos de instalación. Debe usar una herramienta de edición de tablas Windows Installer, como [Orca](orca-exe.md) o una herramienta de terceros, para crear y modificar un paquete de instalación.

 

Los archivos de archivo de texto se pueden usar para los siguientes fines.

-   Los archivos de archivo de texto se pueden usar con sistemas de control de versiones.
-   Para quitar el espacio de almacenamiento desperdiciado y reducir el tamaño final de .msi archivos. Vea [Reducción del tamaño de un .msi archivo](reducing-the-size-of-an--msi-file.md).
-   Para agregar información de localización a una base de datos de instalación. Para obtener más información, vea [Control de páginas de códigos de tablas importadas y exportadas.](code-page-handling-of-imported-and-exported-tables.md)

-   Para determinar la página de códigos de una base de datos. Vea [Determinar la página de códigos de una base de datos de instalación](determining-an-installation-database-s-code-page.md).
-   Para establecer la página de códigos de una base de datos. Vea [Establecer la página de códigos de una base de datos](setting-the-code-page-of-a-database.md).
-   Para aumentar el límite de una columna de base de datos. Exporte la tabla [**mediante MsiDatabaseExport,**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)edite el archivo .idt exportado y, a continuación, importe la tabla [**mediante MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Los autores no pueden cambiar los tipos de datos de columna, la nulabilidad ni los atributos de localización de ninguna columna de las tablas estándar. Consulte también [Creación de un paquete grande.](authoring-a-large-package.md)

En las páginas siguientes se describen las páginas de archivo de texto y sus formatos.

-   [Formato de archivo de archivo](archive-file-format.md)
-   [Datos ASCII en archivos de archivo de texto](ascii-data-in-text-archive-files.md)
-   [\_ForceCodepage](-forcecodepage.md)
-   [\_SummaryInformation](-summaryinformation.md)

 

 



