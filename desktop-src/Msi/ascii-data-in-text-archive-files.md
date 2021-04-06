---
description: Cuando una tabla que solo contiene caracteres ASCII se exporta a un archivo de almacenamiento de texto, el archivo. IDT se ajusta al formato de archivo de almacenamiento básico.
ms.assetid: 105d2b85-c6e1-4719-83b4-1693c14ef4f4
title: Datos ASCII en archivos de almacenamiento de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43deeb7918b75a71770ab9d09535972f6e8bb4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909082"
---
# <a name="ascii-data-in-text-archive-files"></a><span data-ttu-id="5b004-103">Datos ASCII en archivos de almacenamiento de texto</span><span class="sxs-lookup"><span data-stu-id="5b004-103">ASCII Data in Text Archive Files</span></span>

<span data-ttu-id="5b004-104">Cuando una tabla que solo contiene caracteres ASCII se exporta a un [archivo de almacenamiento de texto](text-archive-files.md), el archivo. IDT se ajusta al [formato de archivo de almacenamiento](archive-file-format.md)básico.</span><span class="sxs-lookup"><span data-stu-id="5b004-104">When a table that contains only ASCII characters is exported to a [text archive file](text-archive-files.md), the .idt file adheres to the basic [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="5b004-105">Si la tabla contiene información que no es ASCII, el formato del archivo de almacenamiento se amplía para incluir información de la página de códigos.</span><span class="sxs-lookup"><span data-stu-id="5b004-105">If the table contains non-ASCII information, the format of the archive file is extended to include code page information.</span></span>

## <a name="text-archive-files-that-contain-only-ascii-characters"></a><span data-ttu-id="5b004-106">Archivos de texto que contienen solo caracteres ASCII</span><span class="sxs-lookup"><span data-stu-id="5b004-106">Text archive files that contain only ASCII characters</span></span>

<span data-ttu-id="5b004-107">Cuando una tabla que solo contiene caracteres ASCII se exporta a un archivo de almacenamiento, el archivo. IDT está en el [formato de archivo de almacenamiento](archive-file-format.md)básico.</span><span class="sxs-lookup"><span data-stu-id="5b004-107">When a table that contains only ASCII characters is exported to an archive file, the .idt file is in the basic [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="5b004-108">Cada secuencia de la tabla se exporta como un archivo con la extensión de nombre de archivo. ibd.</span><span class="sxs-lookup"><span data-stu-id="5b004-108">Each stream in the table is exported as a file with an .ibd file name extension.</span></span> <span data-ttu-id="5b004-109">Los archivos. ibd se almacenan en una carpeta con el mismo nombre que la tabla.</span><span class="sxs-lookup"><span data-stu-id="5b004-109">The .ibd files are stored in a folder with the same name as the table.</span></span> <span data-ttu-id="5b004-110">Por ejemplo, considere la posibilidad de exportar la siguiente tabla [binaria](binary-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5b004-110">For example, consider the export of the following [Binary](binary-table.md) table.</span></span>



| <span data-ttu-id="5b004-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="5b004-111">Name</span></span>  | <span data-ttu-id="5b004-112">Datos</span><span class="sxs-lookup"><span data-stu-id="5b004-112">Data</span></span>      |
|-------|-----------|
| <span data-ttu-id="5b004-113">Libros</span><span class="sxs-lookup"><span data-stu-id="5b004-113">Books</span></span> | <span data-ttu-id="5b004-114">Books. ibd</span><span class="sxs-lookup"><span data-stu-id="5b004-114">Books.ibd</span></span> |
| <span data-ttu-id="5b004-115">Cars</span><span class="sxs-lookup"><span data-stu-id="5b004-115">Cars</span></span>  | <span data-ttu-id="5b004-116">Cars. ibd</span><span class="sxs-lookup"><span data-stu-id="5b004-116">Cars.ibd</span></span>  |



 

<span data-ttu-id="5b004-117">La estructura de directorios después de exportar esta tabla es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="5b004-117">The directory structure after exporting this table is as follows.</span></span> <span data-ttu-id="5b004-118">La información de la tabla de la base de datos se exporta a Binary. IDT.</span><span class="sxs-lookup"><span data-stu-id="5b004-118">The information in the database table is exported to Binary.idt.</span></span> <span data-ttu-id="5b004-119">Las dos secuencias de datos binarios se exportan a Book. ibd y Cars. ibd guardado en la carpeta denominada Binary.</span><span class="sxs-lookup"><span data-stu-id="5b004-119">The two streams of binary data are exported to Book.ibd and Cars.ibd saved in the folder named Binary.</span></span>

``` syntax
Binary.idt
[Binary]
    Books.ibd
    Cars.ibd
```

<span data-ttu-id="5b004-120">El archivo de almacenamiento binario. IDT está en el [formato de archivo de almacenamiento](archive-file-format.md) básico y tendría el aspecto siguiente.</span><span class="sxs-lookup"><span data-stu-id="5b004-120">The Binary.idt archive file is in the basic [archive file format](archive-file-format.md) and would look as follows.</span></span>

``` syntax
Name Data
s72 v0
Binary  Name
Books   Books.ibd
Cars    Cars.ibd
```

## <a name="text-archive-files-that-contain-non--ascii-characters"></a><span data-ttu-id="5b004-121">Archivos de texto que contienen caracteres que no son ASCII</span><span class="sxs-lookup"><span data-stu-id="5b004-121">Text archive files that contain non- ASCII characters</span></span>

<span data-ttu-id="5b004-122">Si el archivo contiene datos que no son ASCII, el [formato de archivo de almacenamiento](archive-file-format.md) básico del archivo. IDT se amplía para incluir información de la página de códigos.</span><span class="sxs-lookup"><span data-stu-id="5b004-122">If the file contains non-ASCII data, the basic [archive file format](archive-file-format.md) of the .idt file is extended to include code page information.</span></span> <span data-ttu-id="5b004-123">La tercera fila de la tabla. IDT es la página de códigos numérica seguida del nombre de tabla y los nombres de columna de clave principal separados por tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="5b004-123">The third row in the .idt table is the numeric code page followed by the table name and primary key column names separated by tabs.</span></span>

> [!Note]  
> <span data-ttu-id="5b004-124">Un archivo. IDT que contiene información no ASCII se debe guardar en formato ASCII.</span><span class="sxs-lookup"><span data-stu-id="5b004-124">An .idt file that contains non-ASCII information should be saved in the ASCII format.</span></span> <span data-ttu-id="5b004-125">Por ejemplo, un archivo de almacenamiento de texto puede contener los nombres de tabla y columna codificados como UTF-8, pero el propio archivo de almacenamiento debe ser ASCII.</span><span class="sxs-lookup"><span data-stu-id="5b004-125">For example, a text archive file can contain the column and table names encoded as UTF-8, but the archive file itself should be ASCII.</span></span>

 

<span data-ttu-id="5b004-126">La siguiente tabla de ActionText localizada en francés incluiría información no ASCII.</span><span class="sxs-lookup"><span data-stu-id="5b004-126">The following ActionText table localized into French would contain non-ASCII information.</span></span> <span data-ttu-id="5b004-127">La página de códigos numérica utilizada para las cadenas en francés es 1252.</span><span class="sxs-lookup"><span data-stu-id="5b004-127">The numeric code page used for French strings is 1252.</span></span>



| <span data-ttu-id="5b004-128">Acción</span><span class="sxs-lookup"><span data-stu-id="5b004-128">Action</span></span>    | <span data-ttu-id="5b004-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b004-129">Description</span></span>                                  | <span data-ttu-id="5b004-130">Plantilla</span><span class="sxs-lookup"><span data-stu-id="5b004-130">Template</span></span> |
|-----------|----------------------------------------------|----------|
| <span data-ttu-id="5b004-131">ANUNCIAR</span><span class="sxs-lookup"><span data-stu-id="5b004-131">ADVERTISE</span></span> | <span data-ttu-id="5b004-132">Publicación d'informations sur l'application</span><span class="sxs-lookup"><span data-stu-id="5b004-132">Publication d'informations sur l'application</span></span> |          |



 

<span data-ttu-id="5b004-133">El archivo de almacenamiento exportado, ActionText. IDT, sería como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="5b004-133">The exported archive file, ActionText.idt, would be as follows.</span></span>

``` syntax
Action   Description Template
s72 L0  L0
1252    ActionText  Action
Advertise   Publication d'informations sur l'application
```

> [!Note]  
> <span data-ttu-id="5b004-134">Si un archivo de almacenamiento de texto contiene datos que no son ASCII, el archivo de almacenamiento incluye información de la página de códigos.</span><span class="sxs-lookup"><span data-stu-id="5b004-134">If a text archive file contains non-ASCII data, the archive file includes code page information.</span></span> <span data-ttu-id="5b004-135">Los archivos de almacenamiento con información de página de códigos solo se pueden volver a importar en una base de datos de esa página de códigos exacta o en una base de datos independiente del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="5b004-135">Archive files with code page information can only be imported back into a database of that exact code page or into a language neutral database.</span></span> <span data-ttu-id="5b004-136">En el caso de una base de datos independiente del lenguaje, la página de códigos se establece en la página de códigos del archivo de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="5b004-136">In the case of a language neutral database, the code page is set to the code page of the archive file.</span></span> <span data-ttu-id="5b004-137">Para obtener más información sobre cómo Windows Installer controla las páginas de códigos, vea la sección [control de páginas de códigos (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="5b004-137">For more information about how Windows Installer handles code pages see the section [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

 

 

 



