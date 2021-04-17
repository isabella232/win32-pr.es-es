---
description: Use esta instrucción para crear un paquete de Windows Installer que contenga más de 32767 archivos.
ms.assetid: 3145629f-cc0a-4216-8549-76bb61070772
title: Crear un paquete grande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca09c427336e4ca8a17fd8ebdf803f52ebe6c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667036"
---
# <a name="authoring-a-large-package"></a><span data-ttu-id="56cee-103">Crear un paquete grande</span><span class="sxs-lookup"><span data-stu-id="56cee-103">Authoring a Large Package</span></span>

<span data-ttu-id="56cee-104">Use esta instrucción para crear un paquete de Windows Installer que contenga más de 32767 archivos.</span><span class="sxs-lookup"><span data-stu-id="56cee-104">Use this guideline to author a Windows Installer package that contains more than 32767 files.</span></span>

<span data-ttu-id="56cee-105">Si el paquete de Windows Installer contiene más de 32767 archivos, debe cambiar el esquema de la base de datos para aumentar el límite de las columnas siguientes:</span><span class="sxs-lookup"><span data-stu-id="56cee-105">If your Windows Installer package contains more than 32767 files, you must change the schema of the database to increase the limit of the following columns:</span></span>

-   <span data-ttu-id="56cee-106">Columna de secuencia de la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="56cee-106">The Sequence column of the [File table](file-table.md).</span></span>
-   <span data-ttu-id="56cee-107">La columna LastSequence de la [tabla de medios](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="56cee-107">The LastSequence column of the [Media table](media-table.md).</span></span>
-   <span data-ttu-id="56cee-108">La columna Sequence de la [tabla patch](patch-table.md).</span><span class="sxs-lookup"><span data-stu-id="56cee-108">The Sequence column of the [Patch table](patch-table.md).</span></span>

<span data-ttu-id="56cee-109">Para obtener más información, vea [formato de definición de columna](column-definition-format.md).</span><span class="sxs-lookup"><span data-stu-id="56cee-109">For more information, see [Column Definition Format](column-definition-format.md).</span></span>

<span data-ttu-id="56cee-110">**Para aumentar el límite de una columna de base de datos**</span><span class="sxs-lookup"><span data-stu-id="56cee-110">**To increase the limit of a database column**</span></span>

1.  <span data-ttu-id="56cee-111">Exporte la tabla a un archivo. IDT.</span><span class="sxs-lookup"><span data-stu-id="56cee-111">Export the table to an .idt file.</span></span> <span data-ttu-id="56cee-112">Para obtener más información, vea [Msidb.exe](msidb-exe.md), [exportar archivos](export-files.md)e [importar y exportar](importing-and-exporting.md).</span><span class="sxs-lookup"><span data-stu-id="56cee-112">For details, see [Msidb.exe](msidb-exe.md), [Export Files](export-files.md), and [Importing and Exporting](importing-and-exporting.md).</span></span>
2.  <span data-ttu-id="56cee-113">Edite el archivo. IDT para cambiar el tipo de columna de i2 a I4 o de i2 a I4.</span><span class="sxs-lookup"><span data-stu-id="56cee-113">Edit the .idt file to change the column type from i2 to i4, or from I2 to I4.</span></span>
3.  <span data-ttu-id="56cee-114">Exporte la tabla de [ \_ validación](-validation-table.md) a un archivo. IDT.</span><span class="sxs-lookup"><span data-stu-id="56cee-114">Export the [\_Validation](-validation-table.md) table to an .idt file.</span></span>
4.  <span data-ttu-id="56cee-115">Edite el archivo. IDT para cambiar los valores de la columna MaxValue de la tabla de [ \_ validación](-validation-table.md) para que quepan los mayores anchos de columna.</span><span class="sxs-lookup"><span data-stu-id="56cee-115">Edit the .idt file to change the values in the MaxValue column of the [\_Validation](-validation-table.md) table to accommodate the increased column widths.</span></span>
5.  <span data-ttu-id="56cee-116">Vuelva a importar los archivos. IDT en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="56cee-116">Import the .idt files back into the database.</span></span>

<span data-ttu-id="56cee-117">Tenga en cuenta que las transformaciones y revisiones no se pueden crear entre dos paquetes con tipos de columna diferentes.</span><span class="sxs-lookup"><span data-stu-id="56cee-117">Note that transforms and patches cannot be created between two packages with different column types.</span></span>

 

 



