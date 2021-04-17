---
description: El objeto de vista representa un conjunto de resultados obtenido al procesar una consulta mediante el método OpenView del objeto de base de datos.
ms.assetid: d9d6583a-1cf3-4c33-a851-83e862e2338e
title: Objeto de vista
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c26cfa3c4873913d70fca63537f1d25532648a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680432"
---
# <a name="view-object"></a><span data-ttu-id="28afe-103">Objeto de vista</span><span class="sxs-lookup"><span data-stu-id="28afe-103">View object</span></span>

<span data-ttu-id="28afe-104">El objeto de **vista** representa un conjunto de resultados obtenido al procesar una consulta mediante el método [**OpenView**](database-openview.md) del objeto de [**base de datos**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="28afe-104">The **View** object represents a result set obtained when processing a query using the [**OpenView**](database-openview.md) method of the [**Database**](database-object.md) object.</span></span> <span data-ttu-id="28afe-105">Antes de transferir los datos, se debe ejecutar la consulta mediante el método [**Execute**](view-execute.md) , pasando todos los parámetros reemplazables designados en la cadena de consulta SQL.</span><span class="sxs-lookup"><span data-stu-id="28afe-105">Before any data can be transferred, the query must be executed using the [**Execute**](view-execute.md) method, passing to it all replaceable parameters designated within the SQL query string.</span></span> <span data-ttu-id="28afe-106">La consulta se puede volver a ejecutar, con parámetros diferentes, si es necesario, pero solo después de liberar el conjunto de resultados mediante la captura de todos los registros o mediante una llamada al método [**Close**](view-close.md) .</span><span class="sxs-lookup"><span data-stu-id="28afe-106">The query may be executed again, with different parameters if needed, but only after freeing the result set either by fetching all the records or by calling the [**Close**](view-close.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="28afe-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="28afe-107">Members</span></span>

<span data-ttu-id="28afe-108">El objeto de **vista** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="28afe-108">The **View** object has these types of members:</span></span>

-   [<span data-ttu-id="28afe-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="28afe-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="28afe-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="28afe-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="28afe-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="28afe-111">Methods</span></span>

<span data-ttu-id="28afe-112">El objeto de **vista** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="28afe-112">The **View** object has these methods.</span></span>



| <span data-ttu-id="28afe-113">Método</span><span class="sxs-lookup"><span data-stu-id="28afe-113">Method</span></span>                            | <span data-ttu-id="28afe-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="28afe-114">Description</span></span>                                                                                                                                                                     |
|:----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28afe-115">**Cercanos**</span><span class="sxs-lookup"><span data-stu-id="28afe-115">**Close**</span></span>](view-close.md)       | <span data-ttu-id="28afe-116">Finaliza la ejecución de la consulta y libera los recursos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="28afe-116">Terminates query execution and releases database resources.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="28afe-117">**Ejecut**</span><span class="sxs-lookup"><span data-stu-id="28afe-117">**Execute**</span></span>](view-execute.md)   | <span data-ttu-id="28afe-118">Utiliza el token de signo de interrogación para representar los parámetros de una consulta SQL.</span><span class="sxs-lookup"><span data-stu-id="28afe-118">Uses the question mark token to represent parameters in a SQL query.</span></span> <span data-ttu-id="28afe-119">Los valores de estos parámetros se pasan como los campos correspondientes de un registro de parámetros.</span><span class="sxs-lookup"><span data-stu-id="28afe-119">The values of these parameters are passed in as the corresponding fields of a parameter record.</span></span><br/> |
| [<span data-ttu-id="28afe-120">**Recopila**</span><span class="sxs-lookup"><span data-stu-id="28afe-120">**Fetch**</span></span>](view-fetch.md)       | <span data-ttu-id="28afe-121">Devuelve un objeto de [**registro**](record-object.md) que contiene los datos de la columna solicitada si hay más filas disponibles en el conjunto de resultados; de lo contrario, devuelve NULL.</span><span class="sxs-lookup"><span data-stu-id="28afe-121">Returns a [**Record**](record-object.md) object containing the requested column data if more rows are available in the result set, otherwise, it returns null.</span></span><br/>      |
| [<span data-ttu-id="28afe-122">**GetError**</span><span class="sxs-lookup"><span data-stu-id="28afe-122">**GetError**</span></span>](view-geterror.md) | <span data-ttu-id="28afe-123">Devuelve el error de validación y el nombre de columna para los que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="28afe-123">Returns the Validation error and column name for which the error occurred.</span></span><br/>                                                                                           |
| [<span data-ttu-id="28afe-124">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="28afe-124">**Modify**</span></span>](view-modify.md)     | <span data-ttu-id="28afe-125">Modifica una fila de base de datos con un objeto de [**registro**](record-object.md) modificado obtenido por el método [**Fetch**](view-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="28afe-125">Modifies a database row with a modified [**Record**](record-object.md) object obtained by the [**Fetch**](view-fetch.md) method.</span></span><br/>                                   |



 

### <a name="properties"></a><span data-ttu-id="28afe-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="28afe-126">Properties</span></span>

<span data-ttu-id="28afe-127">El objeto de **vista** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="28afe-127">The **View** object has these properties.</span></span>



| <span data-ttu-id="28afe-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="28afe-128">Property</span></span>                                         | <span data-ttu-id="28afe-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="28afe-129">Description</span></span>                                                                                                                           |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28afe-130">**ColumnInfo**</span><span class="sxs-lookup"><span data-stu-id="28afe-130">**ColumnInfo**</span></span>](view-columninfo.md)<br/> | <span data-ttu-id="28afe-131">Devuelve un objeto de [**registro**](record-object.md) que contiene la información solicitada sobre cada columna del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="28afe-131">Returns a [**Record**](record-object.md) object containing the requested information about each column in the result set.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="28afe-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28afe-132">Requirements</span></span>



| <span data-ttu-id="28afe-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="28afe-133">Requirement</span></span> | <span data-ttu-id="28afe-134">Value</span><span class="sxs-lookup"><span data-stu-id="28afe-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28afe-135">Versión</span><span class="sxs-lookup"><span data-stu-id="28afe-135">Version</span></span><br/> | <span data-ttu-id="28afe-136">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="28afe-136">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="28afe-137">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="28afe-137">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="28afe-138">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="28afe-138">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="28afe-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="28afe-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="28afe-140"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28afe-140"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="28afe-141">IID</span><span class="sxs-lookup"><span data-stu-id="28afe-141">IID</span></span><br/>     | <span data-ttu-id="28afe-142">IID \_ iView se define como 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="28afe-142">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="28afe-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="28afe-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28afe-144">Ejemplos de scripting Windows Installer</span><span class="sxs-lookup"><span data-stu-id="28afe-144">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




