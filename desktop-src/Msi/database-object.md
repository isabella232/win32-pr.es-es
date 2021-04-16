---
description: El objeto de base de datos tiene acceso a una base de datos del instalador.
ms.assetid: 97765884-3e1c-486a-932c-6430b113fac8
title: Objeto de base de datos
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5b47e4678d9475abe90c4b55d6adb514314dcc0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671681"
---
# <a name="database-object"></a><span data-ttu-id="d1b0a-103">Objeto de base de datos</span><span class="sxs-lookup"><span data-stu-id="d1b0a-103">Database object</span></span>

<span data-ttu-id="d1b0a-104">El objeto de **base de datos** tiene acceso a una base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-104">The **Database** object accesses an installer database.</span></span>

<span data-ttu-id="d1b0a-105">El objeto de **base de datos** se libera cuando se saca del ámbito o cuando la variable de objeto asociada a él está establecida en NULL.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-105">The **Database** object is released when it is either taken out of scope or when the object variable associated with it is set to null.</span></span> <span data-ttu-id="d1b0a-106">Se debe llamar al método [**commit**](database-commit.md) antes de liberar el objeto de **base de datos** para escribir todos los cambios persistentes.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-106">The [**Commit**](database-commit.md) method must be called before the **Database** object is released to write out all persistent changes.</span></span> <span data-ttu-id="d1b0a-107">Si no se llama al método **commit** , el instalador realiza una reversión implícita al destruir el objeto.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-107">If the **Commit** method is not called, the installer performs an implicit rollback upon object destruction.</span></span>

<span data-ttu-id="d1b0a-108">El cliente puede utilizar el siguiente procedimiento para el acceso a los datos.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-108">The client can use the following procedure for data access.</span></span>

<span data-ttu-id="d1b0a-109">**Para consultar la secuenciación de API**</span><span class="sxs-lookup"><span data-stu-id="d1b0a-109">**To Query API Sequencing**</span></span>

1.  <span data-ttu-id="d1b0a-110">Obtenga un objeto de **base de datos** mediante una llamada a los objetos [**OpenDatabase**](installer-opendatabase.md) o [**Installer**](installer-object.md) .</span><span class="sxs-lookup"><span data-stu-id="d1b0a-110">Obtain a **Database** object by calling the [**OpenDatabase**](installer-opendatabase.md) or the [**Installer**](installer-object.md) object.</span></span>
2.  <span data-ttu-id="d1b0a-111">Inicie una consulta con una cadena SQL llamando al método [**OpenView**](database-openview.md) del objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="d1b0a-111">Initiate a query using a SQL string by calling the [**OpenView**](database-openview.md) method of the **Database** object.</span></span>
3.  <span data-ttu-id="d1b0a-112">Establezca los parámetros de consulta en un objeto de [**registro**](record-object.md) y ejecute la consulta de base de datos llamando al método [**Execute**](view-execute.md) del objeto [**View**](view-object.md) .</span><span class="sxs-lookup"><span data-stu-id="d1b0a-112">Set query parameters in a [**Record**](record-object.md) object and execute the database query by calling the [**Execute**](view-execute.md) method of the [**View**](view-object.md) object.</span></span> <span data-ttu-id="d1b0a-113">Esto genera un resultado que se puede capturar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-113">This produces a result that can be fetched or updated.</span></span>
4.  <span data-ttu-id="d1b0a-114">Llame a el método [**Fetch**](view-fetch.md) del objeto de [**vista**](view-object.md) varias veces para devolver los objetos de [**registro**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="d1b0a-114">Call the [**Fetch**](view-fetch.md) method of the [**View**](view-object.md) object repeatedly to return [**Record**](record-object.md) objects.</span></span>
5.  <span data-ttu-id="d1b0a-115">Actualice las filas de la base de datos de un objeto de [**registro**](record-object.md) obtenido por el método [**Fetch**](view-fetch.md) con el método [**Modify**](view-modify.md) del objeto [**View**](view-object.md) .</span><span class="sxs-lookup"><span data-stu-id="d1b0a-115">Update database rows of a [**Record**](record-object.md) object obtained by the [**Fetch**](view-fetch.md) method using the [**Modify**](view-modify.md) method of the [**View**](view-object.md) object.</span></span>
6.  <span data-ttu-id="d1b0a-116">Libere la consulta y los registros no capturados llamando al método [**Close**](view-close.md) del objeto [**View**](view-object.md) .</span><span class="sxs-lookup"><span data-stu-id="d1b0a-116">Release the query and any unfetched records by calling the [**Close**](view-close.md) method of the [**View**](view-object.md) object.</span></span>
7.  <span data-ttu-id="d1b0a-117">Conservar cualquier actualización de la base de datos llamando al método [**commit**](database-commit.md) del objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="d1b0a-117">Persist any database updates by calling the [**Commit**](database-commit.md) method of the **Database** object.</span></span>

## <a name="members"></a><span data-ttu-id="d1b0a-118">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1b0a-118">Members</span></span>

<span data-ttu-id="d1b0a-119">El objeto de **base de datos** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d1b0a-119">The **Database** object has these types of members:</span></span>

-   [<span data-ttu-id="d1b0a-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="d1b0a-120">Methods</span></span>](#methods)
-   [<span data-ttu-id="d1b0a-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1b0a-121">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d1b0a-122">Métodos</span><span class="sxs-lookup"><span data-stu-id="d1b0a-122">Methods</span></span>

<span data-ttu-id="d1b0a-123">El objeto de **base de datos** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-123">The **Database** object has these methods.</span></span>



| <span data-ttu-id="d1b0a-124">Método</span><span class="sxs-lookup"><span data-stu-id="d1b0a-124">Method</span></span>                                                                    | <span data-ttu-id="d1b0a-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1b0a-125">Description</span></span>                                                                                                                                                               |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1b0a-126">**ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="d1b0a-126">**ApplyTransform**</span></span>](database-applytransform.md)                         | <span data-ttu-id="d1b0a-127">Aplica la transformación a esta base de datos.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-127">Applies the transform to this database.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="d1b0a-128">**Promete**</span><span class="sxs-lookup"><span data-stu-id="d1b0a-128">**Commit**</span></span>](database-commit.md)                                         | <span data-ttu-id="d1b0a-129">Finaliza el formulario persistente de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-129">Finalizes the persistent form of the database.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="d1b0a-130">**CreateTransformSummaryInfo**</span><span class="sxs-lookup"><span data-stu-id="d1b0a-130">**CreateTransformSummaryInfo**</span></span>](database-createtransformsummaryinfo.md) | <span data-ttu-id="d1b0a-131">Crea y rellena la secuencia de información de Resumen de un archivo de transformación existente.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-131">Creates and populates the summary information stream of an existing transform file.</span></span><br/>                                                                            |
| [<span data-ttu-id="d1b0a-132">**EnableUIPreview**</span><span class="sxs-lookup"><span data-stu-id="d1b0a-132">**EnableUIPreview**</span></span>](database-enableuipreview.md)                       | <span data-ttu-id="d1b0a-133">Facilita la creación de cuadros de diálogo y cartelera al proporcionar la compatibilidad necesaria para ver los cuadros de diálogo de la interfaz de usuario almacenados en la base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-133">Facilitates the authoring of dialog boxes and billboards by providing the support needed to view user interface dialog boxes stored in the installer database.</span></span><br/> |
| [<span data-ttu-id="d1b0a-134">**Exportación**</span><span class="sxs-lookup"><span data-stu-id="d1b0a-134">**Export**</span></span>](database-export.md)                                         | <span data-ttu-id="d1b0a-135">Copia la estructura y los datos de una tabla especificada en un archivo de almacenamiento de texto.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-135">Copies the structure and data from a specified table to a text archive file.</span></span><br/>                                                                                   |
| [<span data-ttu-id="d1b0a-136">**GenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="d1b0a-136">**GenerateTransform**</span></span>](database-generatetransform.md)                   | <span data-ttu-id="d1b0a-137">Crea una transformación.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-137">Creates a transform.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="d1b0a-138">**Importar**</span><span class="sxs-lookup"><span data-stu-id="d1b0a-138">**Import**</span></span>](database-import.md)                                         | <span data-ttu-id="d1b0a-139">Importa una tabla de base de datos de un archivo de almacenamiento de texto.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-139">Imports a database table from a text archive file.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="d1b0a-140">**Sin**</span><span class="sxs-lookup"><span data-stu-id="d1b0a-140">**Merge**</span></span>](database-merge.md)                                           | <span data-ttu-id="d1b0a-141">Combina la base de datos de referencia con la base de datos base.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-141">Merges the reference database with the base database.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="d1b0a-142">**AbrirVista**</span><span class="sxs-lookup"><span data-stu-id="d1b0a-142">**OpenView**</span></span>](database-openview.md)                                     | <span data-ttu-id="d1b0a-143">Devuelve un objeto de [**vista**](view-object.md) que representa la consulta especificada por una cadena SQL.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-143">Returns a [**View**](view-object.md) object representing the query specified by a SQL string.</span></span><br/>                                                                 |



 

### <a name="properties"></a><span data-ttu-id="d1b0a-144">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1b0a-144">Properties</span></span>

<span data-ttu-id="d1b0a-145">El objeto de **base de datos** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-145">The **Database** object has these properties.</span></span>



| <span data-ttu-id="d1b0a-146">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d1b0a-146">Property</span></span>                                                                               | <span data-ttu-id="d1b0a-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1b0a-147">Description</span></span>                                                                                                                                                      |
|:---------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1b0a-148">**DatabaseState**</span><span class="sxs-lookup"><span data-stu-id="d1b0a-148">**DatabaseState**</span></span>](database-databasestate.md)<br/>                             | <span data-ttu-id="d1b0a-149">Devuelve el estado de persistencia de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-149">Returns the persistence state of the database.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="d1b0a-150">**PrimaryKeys**</span><span class="sxs-lookup"><span data-stu-id="d1b0a-150">**PrimaryKeys**</span></span>](database-primarykeys.md)<br/>                                 | <span data-ttu-id="d1b0a-151">Devuelve un objeto de [**registro**](record-object.md) que contiene el nombre de la tabla y los nombres de columna (que comprenden las claves principales).</span><span class="sxs-lookup"><span data-stu-id="d1b0a-151">Returns a [**Record**](record-object.md) object containing the table name and the column names (comprising the primary keys).</span></span><br/>                        |
| [<span data-ttu-id="d1b0a-152">**SummaryInformation (objeto de base de datos)**</span><span class="sxs-lookup"><span data-stu-id="d1b0a-152">**SummaryInformation (Database Object)**</span></span>](database-summaryinformation.md)<br/> | <span data-ttu-id="d1b0a-153">Devuelve un objeto [**SummaryInfo**](summaryinfo-object.md) que se puede utilizar para examinar, actualizar y agregar propiedades a la secuencia de información de resumen.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-153">Returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the summary information stream.</span></span><br/> |
| [<span data-ttu-id="d1b0a-154">**TablePersistent**</span><span class="sxs-lookup"><span data-stu-id="d1b0a-154">**TablePersistent**</span></span>](database-tablepersistent.md)<br/>                         | <span data-ttu-id="d1b0a-155">Devuelve el estado de persistencia de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-155">Returns the persistence state of the table.</span></span><br/>                                                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="d1b0a-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1b0a-156">Requirements</span></span>



| <span data-ttu-id="d1b0a-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1b0a-157">Requirement</span></span> | <span data-ttu-id="d1b0a-158">Value</span><span class="sxs-lookup"><span data-stu-id="d1b0a-158">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b0a-159">Versión</span><span class="sxs-lookup"><span data-stu-id="d1b0a-159">Version</span></span><br/> | <span data-ttu-id="d1b0a-160">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-160">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d1b0a-161">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d1b0a-161">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d1b0a-162">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="d1b0a-162">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d1b0a-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d1b0a-163">DLL</span></span><br/>     | <dl> <span data-ttu-id="d1b0a-164"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1b0a-164"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d1b0a-165">IID</span><span class="sxs-lookup"><span data-stu-id="d1b0a-165">IID</span></span><br/>     | <span data-ttu-id="d1b0a-166">IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d1b0a-166">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="d1b0a-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1b0a-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1b0a-168">Ejemplos de scripting Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d1b0a-168">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




