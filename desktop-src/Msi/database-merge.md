---
description: El método Merge del objeto Database combina la base de datos de referencia con la base de datos base.
ms.assetid: 777060cf-c672-49d5-a1a8-8674fdc4bde4
title: Database. Merge (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Merge
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0a1d93ba6a9a4dc0304daba11c5868b77ece43b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653773"
---
# <a name="databasemerge-method"></a><span data-ttu-id="80b7f-103">Database. Merge (método)</span><span class="sxs-lookup"><span data-stu-id="80b7f-103">Database.Merge method</span></span>

<span data-ttu-id="80b7f-104">El método **Merge** del objeto [**Database**](database-object.md) combina la base de datos de referencia con la base de datos base.</span><span class="sxs-lookup"><span data-stu-id="80b7f-104">The **Merge** method of the [**Database**](database-object.md) object merges the reference database with the base database.</span></span>

## <a name="syntax"></a><span data-ttu-id="80b7f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80b7f-105">Syntax</span></span>


```JScript
Database.Merge(
  reference,
  errorTable
)
```



## <a name="parameters"></a><span data-ttu-id="80b7f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80b7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80b7f-107">*reference*</span><span class="sxs-lookup"><span data-stu-id="80b7f-107">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="80b7f-108">Objeto de [**base de datos**](database-object.md) necesario que se va a combinar en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="80b7f-108">The required [**Database**](database-object.md) object to be merged into the database.</span></span>

</dd> <dt>

<span data-ttu-id="80b7f-109">*errorTable*</span><span class="sxs-lookup"><span data-stu-id="80b7f-109">*errorTable*</span></span> 
</dt> <dd>

<span data-ttu-id="80b7f-110">Nombre opcional de una tabla que contiene los nombres de las tablas que contienen conflictos de combinación, el número de filas en conflicto dentro de la tabla y una referencia a la tabla con el conflicto de combinación.</span><span class="sxs-lookup"><span data-stu-id="80b7f-110">An optional name of a table to contain the names of the tables containing merge conflicts, the number of conflicting rows within the table, and a reference to the table with the merge conflict.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80b7f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80b7f-111">Return value</span></span>

<span data-ttu-id="80b7f-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="80b7f-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="80b7f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80b7f-113">Remarks</span></span>

<span data-ttu-id="80b7f-114">La función [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) y el método **Merge** del objeto [**Database**](database-object.md) no se pueden usar para combinar un módulo incluido en un paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="80b7f-114">The [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) function and the **Merge** method of the [**Database**](database-object.md) object cannot be used to merge a module included within an installation package.</span></span> <span data-ttu-id="80b7f-115">No se deben usar para fusionar mediante combinación [módulos de combinación](merge-modules.md) en un paquete de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="80b7f-115">They should not be used to merge [Merge Modules](merge-modules.md) into a Windows Installer package.</span></span> <span data-ttu-id="80b7f-116">Para incluir un módulo de combinación en un paquete de instalación, los autores de paquetes de instalación deben seguir las instrucciones descritas en el tema [aplicar módulos de combinación](applying-merge-modules.md) .</span><span class="sxs-lookup"><span data-stu-id="80b7f-116">To include a merge module in an installation package, authors of installation packages should follow the guidelines that are described in the [Applying Merge Modules](applying-merge-modules.md) topic.</span></span>

<span data-ttu-id="80b7f-117">El método **Merge** no copia en la base de datos de destino [los archivos. cab](cabinet-files.md) incrustados o las [transformaciones incrustadas](embedded-transforms.md) de la base de datos de referencia.</span><span class="sxs-lookup"><span data-stu-id="80b7f-117">The **Merge** method does not copy over embedded [cabinet files](cabinet-files.md) or [embedded transforms](embedded-transforms.md) from the reference database into the target database.</span></span> <span data-ttu-id="80b7f-118">Los flujos de datos incrustados que se enumeran en la tabla [binaria](binary-table.md) o la [tabla de iconos](icon-table.md) se copian de la base de datos de referencia en la base de datos de destino.</span><span class="sxs-lookup"><span data-stu-id="80b7f-118">Embedded data streams that are listed in the [Binary Table](binary-table.md) or [Icon Table](icon-table.md) are copied from the reference database to the target database.</span></span> <span data-ttu-id="80b7f-119">Los almacenamientos insertados en la base de datos de referencia no se copian en la base de datos de destino.</span><span class="sxs-lookup"><span data-stu-id="80b7f-119">Storages embedded in the reference database are not copied to the target database.</span></span>

<span data-ttu-id="80b7f-120">Si no se proporciona ninguna tabla, el mensaje de error general proporciona el número de tablas que contienen conflictos de combinación.</span><span class="sxs-lookup"><span data-stu-id="80b7f-120">If no table is provided, the general error message provides the number of tables containing merge conflicts.</span></span> <span data-ttu-id="80b7f-121">Se puede pasar cualquier tabla, pero todas las demás columnas deben admitir valores NULL porque la operación para actualizar la [tabla de errores](error-table.md) produce un error si una columna no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="80b7f-121">Any table can be passed in, but all other columns must be nullable because the operation to update the [Error Table](error-table.md) fails if a column is not nullable.</span></span> <span data-ttu-id="80b7f-122">También se puede pasar una tabla recién creada porque el método **Merge** crea automáticamente las columnas que utiliza si se encuentran conflictos de combinación.</span><span class="sxs-lookup"><span data-stu-id="80b7f-122">A newly created table can be passed in as well because the **Merge** method automatically creates the columns it uses if merge conflicts are found.</span></span> <span data-ttu-id="80b7f-123">Se utilizan dos columnas para presentar conflictos de combinación.</span><span class="sxs-lookup"><span data-stu-id="80b7f-123">Two columns are used to present merge conflicts.</span></span> <span data-ttu-id="80b7f-124">La primera columna es el nombre de la tabla y la columna de clave principal.</span><span class="sxs-lookup"><span data-stu-id="80b7f-124">The first column is the table name and the primary key column.</span></span> <span data-ttu-id="80b7f-125">La segunda columna es el número de filas de la tabla que tienen errores de combinación.</span><span class="sxs-lookup"><span data-stu-id="80b7f-125">The second column is the number of rows of that table that have merge failures.</span></span>

<span data-ttu-id="80b7f-126">Si las tablas con el mismo nombre en ambas bases de datos no coinciden en el número de claves principales, los tipos de columna, el número de columnas o los nombres de columna, se produce un error en el método **Merge** y se envía un mensaje de error que indica lo que ocurrió.</span><span class="sxs-lookup"><span data-stu-id="80b7f-126">If tables of the same name in both databases do not match in the number of primary keys, the column types, the number of columns, or the column names, the **Merge** method fails and posts an error message stating what occurred.</span></span>

<span data-ttu-id="80b7f-127">Para que la tabla de errores permanezca, el controlador de errores debe confirmar la base de datos a la que pertenece la tabla de errores.</span><span class="sxs-lookup"><span data-stu-id="80b7f-127">For the Error table to remain, the error handler must commit the database to which the Error table belongs.</span></span> <span data-ttu-id="80b7f-128">Sin embargo, esta confirmación debe realizarse después de usar la tercera columna para obtener las referencias a las tablas en las que se produjeron conflictos de combinación.</span><span class="sxs-lookup"><span data-stu-id="80b7f-128">However, this commit should be done after using the third column to obtain the references to those tables where merge conflicts occurred.</span></span>

<span data-ttu-id="80b7f-129">Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="80b7f-129">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="80b7f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80b7f-130">Requirements</span></span>



| <span data-ttu-id="80b7f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="80b7f-131">Requirement</span></span> | <span data-ttu-id="80b7f-132">Value</span><span class="sxs-lookup"><span data-stu-id="80b7f-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80b7f-133">Versión</span><span class="sxs-lookup"><span data-stu-id="80b7f-133">Version</span></span><br/> | <span data-ttu-id="80b7f-134">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="80b7f-134">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="80b7f-135">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="80b7f-135">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="80b7f-136">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="80b7f-136">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="80b7f-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="80b7f-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="80b7f-138"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80b7f-138"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="80b7f-139">IID</span><span class="sxs-lookup"><span data-stu-id="80b7f-139">IID</span></span><br/>     | <span data-ttu-id="80b7f-140">IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="80b7f-140">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




