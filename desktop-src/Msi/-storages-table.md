---
description: La \_ tabla Storages enumera los almacenamientos de datos OLE incrustados. Se trata de una tabla temporal que solo se crea cuando se hace referencia a ella mediante una instrucción SQL.
ms.assetid: b2f2907d-6966-4b63-9589-c1580f8db574
title: _Storages tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27995dd61c7d25100fc0e1ae2297695e361f44f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909166"
---
# <a name="_storages-table"></a><span data-ttu-id="a6873-104">\_Tabla Storages</span><span class="sxs-lookup"><span data-stu-id="a6873-104">\_Storages Table</span></span>

<span data-ttu-id="a6873-105">La \_ tabla Storages enumera los almacenamientos de datos OLE incrustados.</span><span class="sxs-lookup"><span data-stu-id="a6873-105">The \_Storages table lists embedded OLE data storages.</span></span> <span data-ttu-id="a6873-106">Se trata de una tabla temporal que solo se crea cuando se hace referencia a ella mediante una instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="a6873-106">This is a temporary table, created only when referenced by a SQL statement.</span></span>



| <span data-ttu-id="a6873-107">Columna</span><span class="sxs-lookup"><span data-stu-id="a6873-107">Column</span></span> | <span data-ttu-id="a6873-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="a6873-108">Type</span></span>                 | <span data-ttu-id="a6873-109">Clave</span><span class="sxs-lookup"><span data-stu-id="a6873-109">Key</span></span> | <span data-ttu-id="a6873-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="a6873-110">Nullable</span></span> |
|--------|----------------------|-----|----------|
| <span data-ttu-id="a6873-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="a6873-111">Name</span></span>   | [<span data-ttu-id="a6873-112">Texto</span><span class="sxs-lookup"><span data-stu-id="a6873-112">Text</span></span>](text.md)     | <span data-ttu-id="a6873-113">Y</span><span class="sxs-lookup"><span data-stu-id="a6873-113">Y</span></span>   | <span data-ttu-id="a6873-114">N</span><span class="sxs-lookup"><span data-stu-id="a6873-114">N</span></span>        |
| <span data-ttu-id="a6873-115">Datos</span><span class="sxs-lookup"><span data-stu-id="a6873-115">Data</span></span>   | [<span data-ttu-id="a6873-116">Binario</span><span class="sxs-lookup"><span data-stu-id="a6873-116">Binary</span></span>](binary.md) | <span data-ttu-id="a6873-117">N</span><span class="sxs-lookup"><span data-stu-id="a6873-117">N</span></span>   | <span data-ttu-id="a6873-118">Y</span><span class="sxs-lookup"><span data-stu-id="a6873-118">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a6873-119">Columnas</span><span class="sxs-lookup"><span data-stu-id="a6873-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a6873-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span><span class="sxs-lookup"><span data-stu-id="a6873-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="a6873-121">Una clave única que identifica el almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="a6873-121">A unique key that identifies the storage.</span></span> <span data-ttu-id="a6873-122">La longitud máxima del nombre es de 31 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a6873-122">The maximum length of Name is 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="a6873-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span><span class="sxs-lookup"><span data-stu-id="a6873-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="a6873-124">Datos binarios sin formato.</span><span class="sxs-lookup"><span data-stu-id="a6873-124">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6873-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6873-125">Remarks</span></span>

<span data-ttu-id="a6873-126">Para agregar un almacenamiento OLE a una base de datos, cree un nuevo registro en la \_ tabla Storages y escriba el nombre del almacenamiento en la columna nombre.</span><span class="sxs-lookup"><span data-stu-id="a6873-126">To add an OLE storage to a database, create a new record in the \_Storages table and enter the name of the storage into the Name column.</span></span> <span data-ttu-id="a6873-127">Use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) para copiar datos en la columna de datos de este registro.</span><span class="sxs-lookup"><span data-stu-id="a6873-127">Use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) to copy data into the Data column of this record.</span></span> <span data-ttu-id="a6873-128">Por último, use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para insertar el registro en la \_ tabla de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="a6873-128">Finally, use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the \_Storages table.</span></span>

<span data-ttu-id="a6873-129">No se pueden leer los datos de la \_ tabla de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="a6873-129">Data cannot be read from the \_Storages table.</span></span> <span data-ttu-id="a6873-130">Sin embargo, \_ se puede consultar la tabla de almacenamiento para comprobar la existencia de un almacenamiento específico.</span><span class="sxs-lookup"><span data-stu-id="a6873-130">However, the \_Storages table can be queried to check for the existence of a specific storage.</span></span> <span data-ttu-id="a6873-131">Esto significa que no es posible trasladar un almacenamiento OLE de una base de datos a otra.</span><span class="sxs-lookup"><span data-stu-id="a6873-131">This means that it is not possible to move an OLE storage from one database to another.</span></span> <span data-ttu-id="a6873-132">En su lugar, debe importar el archivo de almacenamiento original en la nueva base de datos. Para eliminar un almacenamiento OLE, recupere el registro que contiene los datos binarios, establezca la columna de datos de la \_ tabla Storages en NULL y, a continuación, actualice el registro.</span><span class="sxs-lookup"><span data-stu-id="a6873-132">You must instead import the original storage file into the new database.To delete an OLE storage, fetch the record containing the binary data, set the Data column in the \_Storages table to null, and then update the record.</span></span> <span data-ttu-id="a6873-133">Un método alternativo consiste en eliminar simplemente el registro mediante [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o una consulta SQL sin formato.</span><span class="sxs-lookup"><span data-stu-id="a6873-133">An alternative method is to simply delete the record using either [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) or a plain SQL query.</span></span>

<span data-ttu-id="a6873-134">Para cambiar el nombre de un almacenamiento OLE, actualice la columna Nombre del registro.</span><span class="sxs-lookup"><span data-stu-id="a6873-134">To rename an OLE storage, update the Name column of the record.</span></span>

<span data-ttu-id="a6873-135">Si se coloca una retención en esta tabla mediante SQL (ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="a6873-135">If a hold is placed on this table using SQL (ALTER TABLE</span></span> <table> <span data-ttu-id="a6873-136">HOLD) o se agrega una columna con Reverse, la tabla se debe liberar mediante FREE.</span><span class="sxs-lookup"><span data-stu-id="a6873-136">HOLD) or a column is added with HOLD, the table must be released using FREE.</span></span> <span data-ttu-id="a6873-137">Los almacenamientos no se escriben hasta que la tabla se ha liberado o confirmado.</span><span class="sxs-lookup"><span data-stu-id="a6873-137">Storages are not written until the table has been released or committed.</span></span>

 

 



