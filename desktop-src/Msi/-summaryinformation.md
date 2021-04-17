---
description: La \_ tabla SummaryInformation es una tabla especial que se usa con la secuencia de información de resumen. Puede obtener o establecer la secuencia de información de Resumen de una base de datos Windows Installer mediante la exportación o importación de un archivo de almacenamiento de texto denominado \_ SummaryInformation. IDT.
ms.assetid: b1b42e03-7a05-46d4-9c42-b87906535adb
title: _SummaryInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803b89223db8b6fc8074336109221a8300f7c1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652637"
---
# <a name="_summaryinformation"></a><span data-ttu-id="765f5-104">\_SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="765f5-104">\_SummaryInformation</span></span>

<span data-ttu-id="765f5-105">La \_ tabla SummaryInformation es una tabla especial que se usa con la [secuencia de información de Resumen](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="765f5-105">The \_SummaryInformation table is a special table used with the [Summary Information Stream](summary-information-stream.md).</span></span> <span data-ttu-id="765f5-106">Puede obtener o establecer la secuencia de información de Resumen de una base de datos Windows Installer mediante la exportación o importación de un [archivo de almacenamiento de texto](text-archive-files.md) denominado \_ SummaryInformation. IDT.</span><span class="sxs-lookup"><span data-stu-id="765f5-106">You can get or set the Summary Information Stream of a Windows Installer database by exporting or importing a [text archive file](text-archive-files.md) named \_SummaryInformation.idt.</span></span>

<span data-ttu-id="765f5-107">El archivo. IDT de una \_ tabla SummaryInformation exportada tiene el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="765f5-107">The .idt file of an exported \_SummaryInformation table has the following format.</span></span>

-   <span data-ttu-id="765f5-108">La primera fila contiene los nombres de columna de tabla separados por tabulaciones: PropertyId y Value.</span><span class="sxs-lookup"><span data-stu-id="765f5-108">The first row contains the table column names separated by tabs: PropertyId and Value.</span></span> <span data-ttu-id="765f5-109">Vea el tema conjunto de propiedades de [flujo de información de Resumen](summary-information-stream-property-set.md) para obtener una lista de las propiedades y sus identificadores (PID).</span><span class="sxs-lookup"><span data-stu-id="765f5-109">See the [Summary Information Stream Property Set](summary-information-stream-property-set.md) topic for a list of the properties and their ids (PID).</span></span>
-   <span data-ttu-id="765f5-110">La segunda fila contiene las definiciones de columna separadas por tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="765f5-110">The second row contains the column definitions separated by tabs.</span></span> <span data-ttu-id="765f5-111">Las definiciones de columna se especifican de la misma manera que en el [formato de archivo de almacenamiento](archive-file-format.md)Basic. IDT.</span><span class="sxs-lookup"><span data-stu-id="765f5-111">The column definitions are specified in the same way as in the basic .idt [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="765f5-112">La columna PropertyId puede ser un entero corto que no acepta valores NULL.</span><span class="sxs-lookup"><span data-stu-id="765f5-112">The PropertyId column can be a non-nullable short integer.</span></span> <span data-ttu-id="765f5-113">La columna valor puede ser una cadena localizable que no acepta valores NULL 255 caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="765f5-113">The Value column can be a non-nullable localizable string 255 characters long.</span></span>
-   <span data-ttu-id="765f5-114">La tercera fila es el nombre de la tabla y el nombre de la columna de clave principal separados por tabulaciones: \_ SummaryInformation y PropertyId.</span><span class="sxs-lookup"><span data-stu-id="765f5-114">The third row is the table name and the primary key column name separated by tabs: \_SummaryInformation and PropertyId.</span></span>
-   <span data-ttu-id="765f5-115">Las filas restantes del archivo representan el PID y el valor asociado, separados por tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="765f5-115">The remaining rows in the file represent the PID and associated value, separated by tabs.</span></span> <span data-ttu-id="765f5-116">La fecha y la hora de \_ SummaryInformation tienen el formato: AAAA/MM/DD HH:: mm:: SS.</span><span class="sxs-lookup"><span data-stu-id="765f5-116">Date and time in\_SummaryInformation are in the format: YYYY/MM/DD hh::mm::ss.</span></span> <span data-ttu-id="765f5-117">Por ejemplo, 1999/03/22 15:25:45.</span><span class="sxs-lookup"><span data-stu-id="765f5-117">For example, 1999/03/22 15:25:45.</span></span>

<span data-ttu-id="765f5-118">El siguiente es un ejemplo de la [secuencia de información de Resumen](summary-information-stream.md) de una base de datos en formato. IDT.</span><span class="sxs-lookup"><span data-stu-id="765f5-118">The following is an example of the [Summary Information Stream](summary-information-stream.md) of a database in .idt format.</span></span>

``` syntax
PropertyId   Value
i2  l255
_SummaryInformation PropertyId
1   1252
2   Installation Database
3   Internal Quick Test
4   Microsoft Corporation
5   Installer,MSI,Database
6   Installer Internal Release Quick Test
7   Intel;1033
9   {00000002-0001-0000-0000-624474736554}
12  1999/06/21
14  110
15  1
18  Windows Installer
```

<span data-ttu-id="765f5-119">Cuando se usa [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) o el método [Import](database-import.md) del objeto [**Database**](database-object.md) para importar una tabla de archivo de texto denominada \_ SummaryInformation en una base de datos del instalador, se escribe la secuencia "05SummaryInformation" en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="765f5-119">When you use [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) or the [Import](database-import.md) method of the [**Database**](database-object.md) object to import a text archive table named \_SummaryInformation into an installer database, you write the "05SummaryInformation" stream in the database.</span></span>

 

 



