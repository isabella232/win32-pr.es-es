---
description: La base de datos del instalador permite al desarrollador de un paquete de instalación controlar la transferencia de una aplicación desde un origen a una imagen de destino.
ms.assetid: 058cefcd-83dd-4a13-bd55-11d52f9d41f5
title: Usar la base de datos del instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb22b9c66547c849b4c9cbd012e78b22d9301756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677909"
---
# <a name="using-the-installer-database"></a><span data-ttu-id="8a9dc-103">Usar la base de datos del instalador</span><span class="sxs-lookup"><span data-stu-id="8a9dc-103">Using the Installer Database</span></span>

<span data-ttu-id="8a9dc-104">La [base de datos del instalador](installer-database.md) permite al desarrollador de un paquete de instalación controlar la transferencia de una aplicación desde un origen a una imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="8a9dc-104">The [Installer Database](installer-database.md) enables the developer of an installation package to control the transfer of an application from a source to a target image.</span></span> <span data-ttu-id="8a9dc-105">El diseño de las imágenes de origen y de destino de la aplicación se especifica en la tabla del [directorio](directory-table.md) y las acciones que instalan la aplicación se especifican en seis tablas de secuencia:</span><span class="sxs-lookup"><span data-stu-id="8a9dc-105">The layout of both the source and target images of the application are specified in the [Directory](directory-table.md) table and the actions that install the application are specified in six sequence tables:</span></span>

-   <span data-ttu-id="8a9dc-106">Tabla [InstallUISequence](installuisequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="8a9dc-106">[InstallUISequence](installuisequence-table.md) table</span></span>
-   <span data-ttu-id="8a9dc-107">Tabla [InstallExecuteSequence](installexecutesequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="8a9dc-107">[InstallExecuteSequence](installexecutesequence-table.md) table</span></span>
-   <span data-ttu-id="8a9dc-108">Tabla [AdminUISequence](adminuisequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="8a9dc-108">[AdminUISequence](adminuisequence-table.md) table</span></span>
-   <span data-ttu-id="8a9dc-109">Tabla [AdminExecuteSequence](adminexecutesequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="8a9dc-109">[AdminExecuteSequence](adminexecutesequence-table.md) table</span></span>
-   <span data-ttu-id="8a9dc-110">Tabla [AdvtUISequence](advtuisequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="8a9dc-110">[AdvtUISequence](advtuisequence-table.md) table</span></span>
-   <span data-ttu-id="8a9dc-111">Tabla [AdvtExecuteSequence](advtexecutesequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="8a9dc-111">[AdvtExecuteSequence](advtexecutesequence-table.md) table</span></span>

<span data-ttu-id="8a9dc-112">En las secciones siguientes se describe cómo usar la [base de datos del instalador](installer-database.md):</span><span class="sxs-lookup"><span data-stu-id="8a9dc-112">The following sections describe how to use the [Installer Database](installer-database.md):</span></span>

-   [<span data-ttu-id="8a9dc-113">Usar la tabla de directorio</span><span class="sxs-lookup"><span data-stu-id="8a9dc-113">Using the Directory Table</span></span>](using-the-directory-table.md)
-   [<span data-ttu-id="8a9dc-114">Usar una tabla de secuencia</span><span class="sxs-lookup"><span data-stu-id="8a9dc-114">Using a Sequence Table</span></span>](using-a-sequence-table.md)
-   [<span data-ttu-id="8a9dc-115">Obtener un identificador de base de datos</span><span class="sxs-lookup"><span data-stu-id="8a9dc-115">Obtaining a Database Handle</span></span>](obtaining-a-database-handle.md)
-   [<span data-ttu-id="8a9dc-116">Confirmar bases de datos</span><span class="sxs-lookup"><span data-stu-id="8a9dc-116">Committing Databases</span></span>](committing-databases.md)
-   [<span data-ttu-id="8a9dc-117">Importar y exportar</span><span class="sxs-lookup"><span data-stu-id="8a9dc-117">Importing and Exporting</span></span>](importing-and-exporting.md)
-   [<span data-ttu-id="8a9dc-118">Combinar bases de datos</span><span class="sxs-lookup"><span data-stu-id="8a9dc-118">Merging Databases</span></span>](merging-databases.md)
-   [<span data-ttu-id="8a9dc-119">Asignar nombres a tablas, propiedades y acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="8a9dc-119">Naming Custom Tables, Properties, and Actions</span></span>](naming-custom-tables-properties-and-actions.md)
-   [<span data-ttu-id="8a9dc-120">Limitaciones de OLE en secuencias</span><span class="sxs-lookup"><span data-stu-id="8a9dc-120">OLE Limitations on Streams</span></span>](ole-limitations-on-streams.md)
-   [<span data-ttu-id="8a9dc-121">Trabajar con consultas</span><span class="sxs-lookup"><span data-stu-id="8a9dc-121">Working with Queries</span></span>](working-with-queries.md)
-   [<span data-ttu-id="8a9dc-122">Agregar datos binarios a una tabla mediante SQL</span><span class="sxs-lookup"><span data-stu-id="8a9dc-122">Adding Binary Data to a Table Using SQL</span></span>](adding-binary-data-to-a-table-using-sql.md)
-   [<span data-ttu-id="8a9dc-123">Trabajar con registros</span><span class="sxs-lookup"><span data-stu-id="8a9dc-123">Working with Records</span></span>](working-with-records.md)
-   [<span data-ttu-id="8a9dc-124">Trabajar con ubicaciones de carpetas</span><span class="sxs-lookup"><span data-stu-id="8a9dc-124">Working with Folder Locations</span></span>](working-with-folder-locations.md)
-   [<span data-ttu-id="8a9dc-125">Especificar el orden de registro automático</span><span class="sxs-lookup"><span data-stu-id="8a9dc-125">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
-   [<span data-ttu-id="8a9dc-126">Acciones de acondicionamiento que se ejecutan durante la eliminación</span><span class="sxs-lookup"><span data-stu-id="8a9dc-126">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
-   [<span data-ttu-id="8a9dc-127">Llamar a funciones de base de datos desde programas</span><span class="sxs-lookup"><span data-stu-id="8a9dc-127">Calling Database Functions from Programs</span></span>](calling-database-functions-from-programs.md)
-   [<span data-ttu-id="8a9dc-128">Sintaxis de la instrucción condicional</span><span class="sxs-lookup"><span data-stu-id="8a9dc-128">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
-   [<span data-ttu-id="8a9dc-129">Formato de definición de columna</span><span class="sxs-lookup"><span data-stu-id="8a9dc-129">Column Definition Format</span></span>](column-definition-format.md)
-   [<span data-ttu-id="8a9dc-130">Determinar si una columna es una clave principal o externa</span><span class="sxs-lookup"><span data-stu-id="8a9dc-130">Determining Whether a Column is a Primary or External Key</span></span>](determining-whether-a-column-is-a-primary-or-external-key.md)

 

 



