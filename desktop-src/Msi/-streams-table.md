---
description: En la \_ tabla streams se enumeran los flujos de datos OLE incrustados. Se trata de una tabla temporal que solo se crea cuando se hace referencia a ella mediante una instrucción SQL.
ms.assetid: 1e30472d-6ba5-410a-a81b-07ed225dcb69
title: _Streams tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9607097b32acc8a3c2350a00db0b9721a4aa353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667081"
---
# <a name="_streams-table"></a><span data-ttu-id="ca673-104">\_Tabla de secuencias</span><span class="sxs-lookup"><span data-stu-id="ca673-104">\_Streams Table</span></span>

<span data-ttu-id="ca673-105">En la \_ tabla streams se enumeran los flujos de datos OLE incrustados.</span><span class="sxs-lookup"><span data-stu-id="ca673-105">The \_Streams table lists embedded OLE data streams.</span></span> <span data-ttu-id="ca673-106">Se trata de una tabla temporal que solo se crea cuando se hace referencia a ella mediante una instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="ca673-106">This is a temporary table, created only when referenced by a SQL statement.</span></span>



| <span data-ttu-id="ca673-107">Columna</span><span class="sxs-lookup"><span data-stu-id="ca673-107">Column</span></span> | <span data-ttu-id="ca673-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="ca673-108">Type</span></span>                 | <span data-ttu-id="ca673-109">Clave</span><span class="sxs-lookup"><span data-stu-id="ca673-109">Key</span></span> | <span data-ttu-id="ca673-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="ca673-110">Nullable</span></span> |
|--------|----------------------|-----|----------|
| <span data-ttu-id="ca673-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="ca673-111">Name</span></span>   | [<span data-ttu-id="ca673-112">Texto</span><span class="sxs-lookup"><span data-stu-id="ca673-112">Text</span></span>](text.md)     | <span data-ttu-id="ca673-113">Y</span><span class="sxs-lookup"><span data-stu-id="ca673-113">Y</span></span>   | <span data-ttu-id="ca673-114">N</span><span class="sxs-lookup"><span data-stu-id="ca673-114">N</span></span>        |
| <span data-ttu-id="ca673-115">Datos</span><span class="sxs-lookup"><span data-stu-id="ca673-115">Data</span></span>   | [<span data-ttu-id="ca673-116">Binario</span><span class="sxs-lookup"><span data-stu-id="ca673-116">Binary</span></span>](binary.md) | <span data-ttu-id="ca673-117">N</span><span class="sxs-lookup"><span data-stu-id="ca673-117">N</span></span>   | <span data-ttu-id="ca673-118">Y</span><span class="sxs-lookup"><span data-stu-id="ca673-118">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ca673-119">Columnas</span><span class="sxs-lookup"><span data-stu-id="ca673-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ca673-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span><span class="sxs-lookup"><span data-stu-id="ca673-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="ca673-121">Una clave única que identifica la secuencia.</span><span class="sxs-lookup"><span data-stu-id="ca673-121">A unique key that identifies the stream.</span></span> <span data-ttu-id="ca673-122">La longitud máxima del nombre es de 62 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ca673-122">The maximum length of Name is 62 characters.</span></span>

</dd> <dt>

<span data-ttu-id="ca673-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span><span class="sxs-lookup"><span data-stu-id="ca673-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="ca673-124">Datos binarios sin formato.</span><span class="sxs-lookup"><span data-stu-id="ca673-124">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca673-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca673-125">Remarks</span></span>

<span data-ttu-id="ca673-126">Para copiar un flujo de datos OLE (por ejemplo, un objeto del tipo de datos [binario](binary.md) ) de un archivo en una base de datos, cree un registro en la \_ tabla streams y escriba el nombre del flujo de datos en la columna Nombre de este registro y copie los datos del archivo en la columna de datos mediante [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama).</span><span class="sxs-lookup"><span data-stu-id="ca673-126">To copy an OLE data stream (for example, an object of the [Binary](binary.md) data type) from a file into a database, create a record in the \_Streams table and enter the name of the data stream into the Name column of this record and copy the data from the file into the Data column using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama).</span></span> <span data-ttu-id="ca673-127">Use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para insertar el nuevo registro en la tabla.</span><span class="sxs-lookup"><span data-stu-id="ca673-127">Use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the new record into the table.</span></span>

<span data-ttu-id="ca673-128">Para leer un flujo de datos binarios incrustado en una base de datos, utilice una consulta SQL para buscar y recuperar el registro que contiene los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="ca673-128">To read a binary data stream embedded in a database, use a SQL query to find and to fetch the record containing the binary data.</span></span> <span data-ttu-id="ca673-129">Use [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) para leer los datos binarios en un búfer.</span><span class="sxs-lookup"><span data-stu-id="ca673-129">Use [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) to read the binary data into a buffer.</span></span>

<span data-ttu-id="ca673-130">Para trasladar un flujo de datos binarios de una base de datos a otra, exporte primero los datos a un archivo.</span><span class="sxs-lookup"><span data-stu-id="ca673-130">To move a binary data stream from one database to another, first export the data to a file.</span></span> <span data-ttu-id="ca673-131">Use una consulta SQL para buscar el flujo de datos en el archivo y use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) para copiar los datos del archivo en la columna de datos de \_ la tabla de secuencias de la segunda base de datos.</span><span class="sxs-lookup"><span data-stu-id="ca673-131">Use a SQL query to find the data stream in the file and use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) to copy the data from the file into Data column of \_Streams table of the second database.</span></span> <span data-ttu-id="ca673-132">Esto garantiza que cada base de datos tiene su propia copia de los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="ca673-132">This ensures that each database has its own copy of the binary data.</span></span> <span data-ttu-id="ca673-133">No se pueden trasladar datos binarios de una base de datos a otra simplemente mediante la captura de un registro con los datos de la primera base de datos y su inserción en la segunda base de datos.</span><span class="sxs-lookup"><span data-stu-id="ca673-133">You cannot move binary data from one database to another simply by fetching a record with the data from the first database and inserting it into the second database.</span></span>

<span data-ttu-id="ca673-134">Para eliminar un flujo de datos, recupere el registro y establezca la columna de datos en NULL antes de actualizar el registro.</span><span class="sxs-lookup"><span data-stu-id="ca673-134">To delete a data stream, fetch the record and set the Data column to null before updating the record.</span></span> <span data-ttu-id="ca673-135">Otro método consiste en quitar el registro de la tabla y eliminarlo mediante [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o una consulta SQL sin formato.</span><span class="sxs-lookup"><span data-stu-id="ca673-135">Another method is to remove the record from the table, deleting it using either [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) or a plain SQL query.</span></span> <span data-ttu-id="ca673-136">No se debe capturar un flujo en un registro si se elimina la secuencia de la tabla.</span><span class="sxs-lookup"><span data-stu-id="ca673-136">A stream should not be fetched into a record if the stream is deleted from the table.</span></span>

<span data-ttu-id="ca673-137">Para cambiar el nombre de un flujo de datos OLE, actualice la columna ' name ' del registro.</span><span class="sxs-lookup"><span data-stu-id="ca673-137">To rename an OLE data stream, update the 'Name' column of the record.</span></span>

<span data-ttu-id="ca673-138">Si se coloca una retención en esta tabla mediante SQL (ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="ca673-138">If a hold is placed on this table using SQL (ALTER TABLE</span></span> <table> <span data-ttu-id="ca673-139">HOLD) o se agrega una columna con Reverse, la tabla se debe liberar mediante FREE.</span><span class="sxs-lookup"><span data-stu-id="ca673-139">HOLD) or a column is added with HOLD, the table must be released using FREE.</span></span> <span data-ttu-id="ca673-140">Las secuencias no se escriben hasta que la tabla se ha liberado o confirmado.</span><span class="sxs-lookup"><span data-stu-id="ca673-140">Streams are not written until the table has been released or committed.</span></span>

 

 



