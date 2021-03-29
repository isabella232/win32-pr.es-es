---
description: Un archivo de texto para una base de datos de Windows Installer incluye una extensión de nombre de archivo. IDT.
ms.assetid: 91d81fb2-3a41-477a-85c2-e68bfe482b9c
title: Formato de archivo de almacenamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf39383b961c305bf621793784332342f369a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909089"
---
# <a name="archive-file-format"></a><span data-ttu-id="0e452-103">Formato de archivo de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="0e452-103">Archive File Format</span></span>

<span data-ttu-id="0e452-104">Un [archivo de texto](text-archive-files.md) para una base de datos de Windows Installer incluye una extensión de nombre de archivo. IDT.</span><span class="sxs-lookup"><span data-stu-id="0e452-104">A [text archive file](text-archive-files.md) for a Windows Installer database carries an .idt file name extension.</span></span> <span data-ttu-id="0e452-105">Cuando se exporta una base de datos completa a archivos de almacenamiento, cada tabla de la base de datos tiene un archivo. IDT independiente.</span><span class="sxs-lookup"><span data-stu-id="0e452-105">When an entire database is exported to archive files, each table in the database has a separate .idt file.</span></span> <span data-ttu-id="0e452-106">Si una tabla contiene una columna de secuencia, cada secuencia de la tabla se representa mediante un archivo con la extensión de nombre de archivo. ibd.</span><span class="sxs-lookup"><span data-stu-id="0e452-106">If a table contains a stream column, each stream in the table is represented by a file with an .ibd file name extension.</span></span> <span data-ttu-id="0e452-107">Los archivos. ibd se almacenan en una carpeta con el mismo nombre que la tabla.</span><span class="sxs-lookup"><span data-stu-id="0e452-107">The .ibd files are stored in a folder with the same name as the table.</span></span>

## <a name="idt-file-format"></a><span data-ttu-id="0e452-108">Formato de archivo. IDT</span><span class="sxs-lookup"><span data-stu-id="0e452-108">.idt File Format</span></span>

<span data-ttu-id="0e452-109">El archivo. IDT de una tabla de base de datos exportada que solo contiene caracteres ASCII tiene el formato básico siguiente.</span><span class="sxs-lookup"><span data-stu-id="0e452-109">The .idt file of an exported database table that contains only ASCII characters has the following basic format.</span></span>

-   <span data-ttu-id="0e452-110">La primera fila contiene los nombres de columna de la tabla separados por tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="0e452-110">The first row contains the table column names separated by tabs.</span></span>
-   <span data-ttu-id="0e452-111">La segunda fila contiene las definiciones de columna separadas por tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="0e452-111">The second row contains the column definitions separated by tabs.</span></span>
-   <span data-ttu-id="0e452-112">Si el archivo solo contiene datos ASCII, la tercera fila es el nombre de la tabla y los nombres de columna de clave principal separados por tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="0e452-112">If the file contain only ASCII data, the third row is table name and primary key column names separated by tabs.</span></span>
-   <span data-ttu-id="0e452-113">Las filas restantes del archivo representan las filas de la tabla, con las columnas separadas por tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="0e452-113">The remaining rows in the file represent rows in the table, with columns separated by tabs.</span></span>

> [!Note]  
> <span data-ttu-id="0e452-114">Si el archivo contiene datos que no son ASCII, la tercera fila es la página de códigos numérica seguida del nombre de tabla y los nombres de columna de clave principal separados por tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="0e452-114">If the file contains non-ASCII data, the third row is the numeric code page followed by the table name and primary key column names separated by tabs.</span></span> <span data-ttu-id="0e452-115">Un archivo. IDT que contiene información no ASCII se debe guardar en formato ASCII.</span><span class="sxs-lookup"><span data-stu-id="0e452-115">An .idt file that contains non-ASCII information should be saved in the ASCII format.</span></span> <span data-ttu-id="0e452-116">Por ejemplo, un archivo de almacenamiento de texto puede contener los nombres de tabla y columna codificados como UTF-8, pero el propio archivo de almacenamiento debe ser ASCII.</span><span class="sxs-lookup"><span data-stu-id="0e452-116">For example, a text archive file can contain the column and table names encoded as UTF-8, but the archive file itself should be ASCII.</span></span> <span data-ttu-id="0e452-117">Vea la sección [datos ASCII en archivos de almacenamiento de texto](ascii-data-in-text-archive-files.md).</span><span class="sxs-lookup"><span data-stu-id="0e452-117">See the section [ASCII Data in Text Archive Files](ascii-data-in-text-archive-files.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="0e452-118">Los archivos especiales [ \_ ForceCodepage](-forcecodepage.md) y [ \_ SummaryInformation](-summaryinformation.md) . IDT usan formatos extendidos.</span><span class="sxs-lookup"><span data-stu-id="0e452-118">The special [\_ForceCodepage](-forcecodepage.md) and [\_SummaryInformation](-summaryinformation.md) .idt files use extended formats.</span></span> <span data-ttu-id="0e452-119">Vea las \_ secciones ForceCodepage y \_ SummaryInformation para obtener descripciones de sus formatos.</span><span class="sxs-lookup"><span data-stu-id="0e452-119">See the \_ForceCodepage and \_SummaryInformation sections for descriptions of their formats.</span></span>

 

## <a name="column-definitions"></a><span data-ttu-id="0e452-120">Definiciones de columna</span><span class="sxs-lookup"><span data-stu-id="0e452-120">Column Definitions</span></span>

<span data-ttu-id="0e452-121">Las definiciones de columna se indican mediante caracteres.</span><span class="sxs-lookup"><span data-stu-id="0e452-121">Column definitions are indicated by characters.</span></span>

-   <span data-ttu-id="0e452-122">El primer carácter indica el tipo de columna.</span><span class="sxs-lookup"><span data-stu-id="0e452-122">The first character indicates the column type.</span></span> <span data-ttu-id="0e452-123">Una letra minúscula indica una columna que no admite valores NULL y una letra mayúscula indica que la columna puede contener valores NULL.</span><span class="sxs-lookup"><span data-stu-id="0e452-123">A lowercase letter indicates a non-nullable column and an uppercase letter indicates that the column can contain null values.</span></span>

    | <span data-ttu-id="0e452-124">Carácter</span><span class="sxs-lookup"><span data-stu-id="0e452-124">Character</span></span> | <span data-ttu-id="0e452-125">Significado</span><span class="sxs-lookup"><span data-stu-id="0e452-125">Meaning</span></span>                   |
    |-----------|---------------------------|
    | <span data-ttu-id="0e452-126">s, S</span><span class="sxs-lookup"><span data-stu-id="0e452-126">s, S</span></span>      | <span data-ttu-id="0e452-127">Columna de cadena</span><span class="sxs-lookup"><span data-stu-id="0e452-127">String Column</span></span>             |
    | <span data-ttu-id="0e452-128">l, L</span><span class="sxs-lookup"><span data-stu-id="0e452-128">l, L</span></span>      | <span data-ttu-id="0e452-129">Columna de cadena localizable</span><span class="sxs-lookup"><span data-stu-id="0e452-129">Localizable String Column</span></span> |
    | <span data-ttu-id="0e452-130">v, V</span><span class="sxs-lookup"><span data-stu-id="0e452-130">v, V</span></span>      | <span data-ttu-id="0e452-131">Columna binaria</span><span class="sxs-lookup"><span data-stu-id="0e452-131">Binary Column</span></span>             |
    | <span data-ttu-id="0e452-132">i, I</span><span class="sxs-lookup"><span data-stu-id="0e452-132">i, I</span></span>      | <span data-ttu-id="0e452-133">Columna de enteros</span><span class="sxs-lookup"><span data-stu-id="0e452-133">Integer Column</span></span>            |

    

     

-   <span data-ttu-id="0e452-134">El segundo carácter indica el tamaño de los datos de la columna.</span><span class="sxs-lookup"><span data-stu-id="0e452-134">The second character indicates the column data size.</span></span>

    > [!Note]  
    > <span data-ttu-id="0e452-135">El Windows Installer no utiliza realmente el tamaño de columna especificado para limitar el tamaño de la cadena que se puede escribir en un campo de columna de cadena.</span><span class="sxs-lookup"><span data-stu-id="0e452-135">The Windows Installer does not actually use the specified column size to limit the size of the string that can be entered into a string column field.</span></span> <span data-ttu-id="0e452-136">Sin embargo, algunas herramientas de creación usan el tamaño de columna especificado para limitar el tamaño de una cadena válida.</span><span class="sxs-lookup"><span data-stu-id="0e452-136">However, some authoring tools do use the specified column size to limit the size of a valid string.</span></span> <span data-ttu-id="0e452-137">Se recomienda que las cadenas especificadas en cualquier columna cumplan el requisito de tamaño especificado.</span><span class="sxs-lookup"><span data-stu-id="0e452-137">It is recommended that strings entered into any column meet the specified size requirement.</span></span>

     

    

    | <span data-ttu-id="0e452-138">Definición de columna</span><span class="sxs-lookup"><span data-stu-id="0e452-138">Column Definition</span></span> | <span data-ttu-id="0e452-139">Significado</span><span class="sxs-lookup"><span data-stu-id="0e452-139">Meaning</span></span>                                    |
    |-------------------|--------------------------------------------|
    | <span data-ttu-id="0e452-140">s255</span><span class="sxs-lookup"><span data-stu-id="0e452-140">s255</span></span>              | <span data-ttu-id="0e452-141">Columna de cadena que no acepta valores NULL 255 Long</span><span class="sxs-lookup"><span data-stu-id="0e452-141">Non-Nullable String Column 255 long</span></span>        |
    | <span data-ttu-id="0e452-142">L50</span><span class="sxs-lookup"><span data-stu-id="0e452-142">L50</span></span>               | <span data-ttu-id="0e452-143">Columna de cadena localizable que acepta valores NULL 50 Long</span><span class="sxs-lookup"><span data-stu-id="0e452-143">Nullable Localizable String Column 50 long</span></span> |
    | <span data-ttu-id="0e452-144">I2, I2</span><span class="sxs-lookup"><span data-stu-id="0e452-144">i2, I2</span></span>            | <span data-ttu-id="0e452-145">Columna de entero corto</span><span class="sxs-lookup"><span data-stu-id="0e452-145">Short Integer Column</span></span>                       |
    | <span data-ttu-id="0e452-146">I4, I4</span><span class="sxs-lookup"><span data-stu-id="0e452-146">i4, I4</span></span>            | <span data-ttu-id="0e452-147">Columna de entero largo</span><span class="sxs-lookup"><span data-stu-id="0e452-147">Long Integer Column</span></span>                        |

    

     

## <a name="control-character-translation"></a><span data-ttu-id="0e452-148">Traducción de caracteres de control</span><span class="sxs-lookup"><span data-stu-id="0e452-148">Control Character Translation</span></span>

<span data-ttu-id="0e452-149">Exportar una tabla a un archivo de almacenamiento de texto traduce los caracteres de control para evitar conflictos con delimitadores de archivos.</span><span class="sxs-lookup"><span data-stu-id="0e452-149">Exporting a table to a text archive file translates the control characters to avoid conflicts with file delimiters.</span></span> <span data-ttu-id="0e452-150">Al escribir en el archivo. IDT, los caracteres de control se convierten como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="0e452-150">While writing into the .idt file, the control characters are translated as follows.</span></span>



| <span data-ttu-id="0e452-151">Carácter de control</span><span class="sxs-lookup"><span data-stu-id="0e452-151">Control Character</span></span> | <span data-ttu-id="0e452-152">Traducción en. IDT</span><span class="sxs-lookup"><span data-stu-id="0e452-152">Translation in .idt</span></span> | <span data-ttu-id="0e452-153">Significado</span><span class="sxs-lookup"><span data-stu-id="0e452-153">Meaning</span></span>         |
|-------------------|---------------------|-----------------|
| <span data-ttu-id="0e452-154">NULL</span><span class="sxs-lookup"><span data-stu-id="0e452-154">NULL</span></span>              | <span data-ttu-id="0e452-155">21</span><span class="sxs-lookup"><span data-stu-id="0e452-155">21</span></span>                  | <span data-ttu-id="0e452-156">Null</span><span class="sxs-lookup"><span data-stu-id="0e452-156">Null</span></span>            |
| <span data-ttu-id="0e452-157">BS</span><span class="sxs-lookup"><span data-stu-id="0e452-157">BS</span></span>                | <span data-ttu-id="0e452-158">27</span><span class="sxs-lookup"><span data-stu-id="0e452-158">27</span></span>                  | <span data-ttu-id="0e452-159">Espacio de retroceso</span><span class="sxs-lookup"><span data-stu-id="0e452-159">Back Space</span></span>      |
| <span data-ttu-id="0e452-160">HT</span><span class="sxs-lookup"><span data-stu-id="0e452-160">HT</span></span>                | <span data-ttu-id="0e452-161">16</span><span class="sxs-lookup"><span data-stu-id="0e452-161">16</span></span>                  | <span data-ttu-id="0e452-162">Pestaña</span><span class="sxs-lookup"><span data-stu-id="0e452-162">Tab</span></span>             |
| <span data-ttu-id="0e452-163">LF</span><span class="sxs-lookup"><span data-stu-id="0e452-163">LF</span></span>                | <span data-ttu-id="0e452-164">25</span><span class="sxs-lookup"><span data-stu-id="0e452-164">25</span></span>                  | <span data-ttu-id="0e452-165">avance de línea</span><span class="sxs-lookup"><span data-stu-id="0e452-165">Line Feed</span></span>       |
| <span data-ttu-id="0e452-166">FF</span><span class="sxs-lookup"><span data-stu-id="0e452-166">FF</span></span>                | <span data-ttu-id="0e452-167">24</span><span class="sxs-lookup"><span data-stu-id="0e452-167">24</span></span>                  | <span data-ttu-id="0e452-168">Avance de formulario</span><span class="sxs-lookup"><span data-stu-id="0e452-168">Form Feed</span></span>       |
| <span data-ttu-id="0e452-169">CR</span><span class="sxs-lookup"><span data-stu-id="0e452-169">CR</span></span>                | <span data-ttu-id="0e452-170">17</span><span class="sxs-lookup"><span data-stu-id="0e452-170">17</span></span>                  | <span data-ttu-id="0e452-171">Retorno de carro</span><span class="sxs-lookup"><span data-stu-id="0e452-171">Carriage Return</span></span> |



 

 

 



