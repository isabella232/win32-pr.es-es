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
# <a name="text-archive-files"></a><span data-ttu-id="c6276-103">Archivos de archivo de texto</span><span class="sxs-lookup"><span data-stu-id="c6276-103">Text Archive Files</span></span>

<span data-ttu-id="c6276-104">Las tablas de base de datos de Windows Installer se pueden exportar a archivos de texto ASCII mediante [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) o el método [**Export**](database-export.md) del objeto [**Database**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="c6276-104">The Windows Installer database tables can be exported to ASCII text files by using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) or the [**Export**](database-export.md) method of the [**Database**](database-object.md) object.</span></span> <span data-ttu-id="c6276-105">La información de estos archivos de almacenamiento de texto se puede volver a importar a una base de datos de Windows Installer mediante [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) o el método de [importación](database-import.md) del objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="c6276-105">The information in these text archive files can then be imported back into a Windows Installer database using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) or the [Import](database-import.md) method of the **Database** object.</span></span>

<span data-ttu-id="c6276-106">Herramientas como [msidb.exe](msidb-exe.md) son capaces de exportar e importar archivos de almacenamiento de texto.</span><span class="sxs-lookup"><span data-stu-id="c6276-106">Tools such as [msidb.exe](msidb-exe.md) are capable of exporting and importing text archive files.</span></span> <span data-ttu-id="c6276-107">Vea [exportar archivos](export-files.md) e [importar archivos](import-files.md) para obtener [Windows Installer ejemplos de scripting](windows-installer-scripting-examples.md) que pueden exportar e importar archivos de almacenamiento de texto desde una base de datos.</span><span class="sxs-lookup"><span data-stu-id="c6276-107">See [Export Files](export-files.md) and [Import Files](import-files.md) for [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) that can export and import text archive files from a database.</span></span>

> [!Note]  
> <span data-ttu-id="c6276-108">Los archivos de archivo de texto no están diseñados como un medio para editar la base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="c6276-108">Text archive files are not intended as a means to edit the installation database.</span></span> <span data-ttu-id="c6276-109">Debe utilizar una herramienta de edición de tablas Windows Installer, como [Orca](orca-exe.md) o una herramienta de terceros, para crear y modificar un paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="c6276-109">You should use a Windows Installer table editing tool, such as [Orca](orca-exe.md) or a third-party tool, to create and modify an installation package.</span></span>

 

<span data-ttu-id="c6276-110">Los archivos de texto se pueden usar para los siguientes fines.</span><span class="sxs-lookup"><span data-stu-id="c6276-110">Text archive files can be used for the following purposes.</span></span>

-   <span data-ttu-id="c6276-111">Los archivos de archivo de texto se pueden usar con sistemas de control de versiones.</span><span class="sxs-lookup"><span data-stu-id="c6276-111">Text archive files can be used with version control systems.</span></span>
-   <span data-ttu-id="c6276-112">Para quitar el espacio de almacenamiento desperdiciado y reducir el tamaño final de los archivos. msi.</span><span class="sxs-lookup"><span data-stu-id="c6276-112">To remove wasted storage space and reduce the final size of .msi files.</span></span> <span data-ttu-id="c6276-113">Consulte [reducir el tamaño de un archivo. msi](reducing-the-size-of-an--msi-file.md).</span><span class="sxs-lookup"><span data-stu-id="c6276-113">See [Reducing the Size of an .msi File](reducing-the-size-of-an--msi-file.md).</span></span>
-   <span data-ttu-id="c6276-114">Para agregar información de localización a una base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="c6276-114">To add localization information to an installation database.</span></span> <span data-ttu-id="c6276-115">Para obtener más información, vea [control de páginas de códigos de tablas importadas y exportadas](code-page-handling-of-imported-and-exported-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c6276-115">For more information, see [Code Page Handling of Imported and Exported Tables](code-page-handling-of-imported-and-exported-tables.md).</span></span>

-   <span data-ttu-id="c6276-116">Para determinar la página de códigos de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="c6276-116">To determine the code page of a database.</span></span> <span data-ttu-id="c6276-117">Consulte [determinación de la página de códigos de una base de datos de instalación](determining-an-installation-database-s-code-page.md).</span><span class="sxs-lookup"><span data-stu-id="c6276-117">See [Determining an Installation Database's Code Page](determining-an-installation-database-s-code-page.md).</span></span>
-   <span data-ttu-id="c6276-118">Para establecer la página de códigos de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="c6276-118">To set the code page of a database.</span></span> <span data-ttu-id="c6276-119">Vea [establecer la página de códigos de una base de datos](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="c6276-119">See [Setting the code page of a database](setting-the-code-page-of-a-database.md).</span></span>
-   <span data-ttu-id="c6276-120">Para aumentar el límite de una columna de base de datos.</span><span class="sxs-lookup"><span data-stu-id="c6276-120">To increase the limit of a database column.</span></span> <span data-ttu-id="c6276-121">Exporte la tabla mediante [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), edite el archivo. IDT exportado y, a continuación, importe la tabla con [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="c6276-121">Export the table using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), edit the exported .idt file, and then import the table using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="c6276-122">Los autores no pueden cambiar los tipos de datos de columna, la nulabilidad o los atributos de localización de las columnas de las tablas estándar.</span><span class="sxs-lookup"><span data-stu-id="c6276-122">Authors cannot change the column data types, nullability, or localization attributes of any columns in standard tables.</span></span> <span data-ttu-id="c6276-123">Vea también [crear un paquete de gran tamaño](authoring-a-large-package.md).</span><span class="sxs-lookup"><span data-stu-id="c6276-123">See also [Authoring a Large Package](authoring-a-large-package.md).</span></span>

<span data-ttu-id="c6276-124">En las páginas siguientes se describen las páginas de archivo de texto y sus formatos.</span><span class="sxs-lookup"><span data-stu-id="c6276-124">The following pages describe text archive pages and their formats.</span></span>

-   [<span data-ttu-id="c6276-125">Formato de archivo de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="c6276-125">Archive File Format</span></span>](archive-file-format.md)
-   [<span data-ttu-id="c6276-126">Datos ASCII en archivos de almacenamiento de texto</span><span class="sxs-lookup"><span data-stu-id="c6276-126">ASCII Data in Text Archive Files</span></span>](ascii-data-in-text-archive-files.md)
-   [<span data-ttu-id="c6276-127">\_ForceCodepage</span><span class="sxs-lookup"><span data-stu-id="c6276-127">\_ForceCodepage</span></span>](-forcecodepage.md)
-   [<span data-ttu-id="c6276-128">\_SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="c6276-128">\_SummaryInformation</span></span>](-summaryinformation.md)

 

 



