---
description: La acción InstallODBC instala los controladores, los traductores y los orígenes de datos en la tabla ODBCDriver, la tabla ODBCTranslator y la tabla ODBCDataSource.
ms.assetid: fbcf1fdc-5aef-4431-93fe-3ed02748b5ff
title: Acción InstallODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac9becd2a528646805f4201cfb415a6bc61bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688448"
---
# <a name="installodbc-action"></a><span data-ttu-id="16af2-103">Acción InstallODBC</span><span class="sxs-lookup"><span data-stu-id="16af2-103">InstallODBC Action</span></span>

<span data-ttu-id="16af2-104">La acción InstallODBC instala los controladores, los traductores y los orígenes de datos en la tabla [ODBCDriver](odbcdriver-table.md), la tabla [ODBCTranslator](odbctranslator-table.md)y la tabla [ODBCDataSource](odbcdatasource-table.md).</span><span class="sxs-lookup"><span data-stu-id="16af2-104">The InstallODBC action installs the drivers, translators, and data sources in the [ODBCDriver Table](odbcdriver-table.md), [ODBCTranslator Table](odbctranslator-table.md), and [ODBCDataSource Table](odbcdatasource-table.md).</span></span> <span data-ttu-id="16af2-105">Si ya existe un controlador o un traductor, la acción InstallODBC realiza las llamadas a SQL necesarias para la instalación.</span><span class="sxs-lookup"><span data-stu-id="16af2-105">If a driver or translator already exists, the InstallODBC action makes SQL calls necessary for the installation.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="16af2-106">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="16af2-106">Sequence Restrictions</span></span>

<span data-ttu-id="16af2-107">La acción InstallODBC no copia ni quita archivos, y debe ser después de acciones que copian o quitan archivos.</span><span class="sxs-lookup"><span data-stu-id="16af2-107">The InstallODBC action does not copy or remove files, and must be after actions that copy or remove files.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="16af2-108">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="16af2-108">ActionData Messages</span></span>

<span data-ttu-id="16af2-109">En la tabla siguiente se identifican los mensajes de ActionData para cada controlador instalado.</span><span class="sxs-lookup"><span data-stu-id="16af2-109">The following table identifies the ActionData messages for each installed driver.</span></span>



| <span data-ttu-id="16af2-110">Campo</span><span class="sxs-lookup"><span data-stu-id="16af2-110">Field</span></span>       | <span data-ttu-id="16af2-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="16af2-111">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="16af2-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="16af2-112">\[1\]</span></span>       | <span data-ttu-id="16af2-113">Descripción del controlador.</span><span class="sxs-lookup"><span data-stu-id="16af2-113">Driver description.</span></span> <span data-ttu-id="16af2-114">La clave del controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="16af2-114">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="16af2-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="16af2-115">\[2\]</span></span>       | <span data-ttu-id="16af2-116">ComponentID.</span><span class="sxs-lookup"><span data-stu-id="16af2-116">ComponentId.</span></span>                                                             |
| <span data-ttu-id="16af2-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="16af2-117">\[3\]</span></span>       | <span data-ttu-id="16af2-118">Carpeta.</span><span class="sxs-lookup"><span data-stu-id="16af2-118">Folder.</span></span>                                                                  |
| <span data-ttu-id="16af2-119">\[4, 5,...\]</span><span class="sxs-lookup"><span data-stu-id="16af2-119">\[4, 5, …\]</span></span> | <span data-ttu-id="16af2-120">Pares de atributo y valor de [ODBCAttribute](odbcattribute-table.md).</span><span class="sxs-lookup"><span data-stu-id="16af2-120">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

<span data-ttu-id="16af2-121">En la tabla siguiente se identifican los mensajes de ActionData para cada traductor instalado.</span><span class="sxs-lookup"><span data-stu-id="16af2-121">The following table identifies the ActionData messages for each installed translator.</span></span>



| <span data-ttu-id="16af2-122">Campo</span><span class="sxs-lookup"><span data-stu-id="16af2-122">Field</span></span>       | <span data-ttu-id="16af2-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="16af2-123">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="16af2-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="16af2-124">\[1\]</span></span>       | <span data-ttu-id="16af2-125">Descripción del controlador.</span><span class="sxs-lookup"><span data-stu-id="16af2-125">Driver description.</span></span> <span data-ttu-id="16af2-126">La clave del controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="16af2-126">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="16af2-127">\[2\]</span><span class="sxs-lookup"><span data-stu-id="16af2-127">\[2\]</span></span>       | <span data-ttu-id="16af2-128">ComponentID.</span><span class="sxs-lookup"><span data-stu-id="16af2-128">ComponentId.</span></span>                                                             |
| <span data-ttu-id="16af2-129">\[3\]</span><span class="sxs-lookup"><span data-stu-id="16af2-129">\[3\]</span></span>       | <span data-ttu-id="16af2-130">Carpeta.</span><span class="sxs-lookup"><span data-stu-id="16af2-130">Folder.</span></span>                                                                  |
| <span data-ttu-id="16af2-131">\[4, 5,...\]</span><span class="sxs-lookup"><span data-stu-id="16af2-131">\[4, 5, …\]</span></span> | <span data-ttu-id="16af2-132">Pares de atributo y valor de [ODBCAttribute](odbcattribute-table.md).</span><span class="sxs-lookup"><span data-stu-id="16af2-132">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

<span data-ttu-id="16af2-133">En la tabla siguiente se identifican los mensajes ActionData de cada origen de datos instalado.</span><span class="sxs-lookup"><span data-stu-id="16af2-133">The following table identifies the ActionData messages for each installed data source.</span></span>



| <span data-ttu-id="16af2-134">Campo</span><span class="sxs-lookup"><span data-stu-id="16af2-134">Field</span></span>       | <span data-ttu-id="16af2-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="16af2-135">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="16af2-136">\[1\]</span><span class="sxs-lookup"><span data-stu-id="16af2-136">\[1\]</span></span>       | <span data-ttu-id="16af2-137">Descripción del controlador.</span><span class="sxs-lookup"><span data-stu-id="16af2-137">Driver description.</span></span> <span data-ttu-id="16af2-138">La clave del controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="16af2-138">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="16af2-139">\[2\]</span><span class="sxs-lookup"><span data-stu-id="16af2-139">\[2\]</span></span>       | <span data-ttu-id="16af2-140">ComponentID.</span><span class="sxs-lookup"><span data-stu-id="16af2-140">ComponentId.</span></span>                                                             |
| <span data-ttu-id="16af2-141">\[3\]</span><span class="sxs-lookup"><span data-stu-id="16af2-141">\[3\]</span></span>       | <span data-ttu-id="16af2-142">Registro: ODBC \_ Add \_ DSN u ODBC \_ Add \_ Sys \_ DSN.</span><span class="sxs-lookup"><span data-stu-id="16af2-142">Registration: ODBC\_ADD\_DSN or ODBC\_ADD\_SYS\_DSN.</span></span>                     |
| <span data-ttu-id="16af2-143">\[4, 5,...\]</span><span class="sxs-lookup"><span data-stu-id="16af2-143">\[4, 5, …\]</span></span> | <span data-ttu-id="16af2-144">Pares de atributo y valor de [ODBCAttribute](odbcattribute-table.md).</span><span class="sxs-lookup"><span data-stu-id="16af2-144">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="16af2-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16af2-145">Remarks</span></span>

<span data-ttu-id="16af2-146">El administrador de controladores ODBC debe estar creado en el paquete de Microsoft Installer y debe incluirse un componente denominado ODBCDriverManager.</span><span class="sxs-lookup"><span data-stu-id="16af2-146">The ODBC Driver Manager must be authored in the Microsoft Installer package and a component named ODBCDriverManager must be included.</span></span> <span data-ttu-id="16af2-147">Si es necesario, el administrador se instala.</span><span class="sxs-lookup"><span data-stu-id="16af2-147">The manager is installed if necessary.</span></span>

<span data-ttu-id="16af2-148">Para cambiar el nombre del componente, establezca una propiedad denominada ODBCDriverManager en el nuevo nombre del componente.</span><span class="sxs-lookup"><span data-stu-id="16af2-148">To rename the component, set a property named ODBCDriverManager to the new name of the component.</span></span> <span data-ttu-id="16af2-149">Si se va a instalar el administrador de controladores ODBC de 64 bits, el componente que lo lleva debe denominarse ODBCDriverManager64.</span><span class="sxs-lookup"><span data-stu-id="16af2-149">If a 64-bit ODBC Driver Manager is to be installed, the component that carries it should be named ODBCDriverManager64.</span></span>

-   <span data-ttu-id="16af2-150">La acción InstallODBC consulta la [tabla ODBCDataSource](odbcdatasource-table.md) y la [tabla ODBCSourceAttribute](odbcsourceattribute-table.md) de cada origen de datos que se va a instalar, así como los atributos del origen de datos.</span><span class="sxs-lookup"><span data-stu-id="16af2-150">The InstallODBC action queries the [ODBCDataSource Table](odbcdatasource-table.md) and the [ODBCSourceAttribute Table](odbcsourceattribute-table.md) for each data source to be installed, and the attributes of the data source.</span></span>
-   <span data-ttu-id="16af2-151">La acción InstallODBC consulta la [tabla ODBCDriver](odbcdriver-table.md) y la [tabla ODBCTranslator](odbctranslator-table.md) para cada controlador y traductor que se selecciona para su instalación.</span><span class="sxs-lookup"><span data-stu-id="16af2-151">The InstallODBC action queries the [ODBCDriver Table](odbcdriver-table.md) and the [ODBCTranslator Table](odbctranslator-table.md) for each driver and translator that is selected for installation.</span></span>
-   <span data-ttu-id="16af2-152">La acción InstallODBC consulta en la [tabla ODBCAttribute](odbcattribute-table.md) los atributos de los controladores y traductores.</span><span class="sxs-lookup"><span data-stu-id="16af2-152">The InstallODBC action queries the [ODBCAttribute Table](odbcattribute-table.md) for the attributes of the drivers and translators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16af2-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="16af2-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16af2-154">Ejemplos de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="16af2-154">Windows Installer Examples</span></span>](windows-installer-examples.md)
</dt> </dl>

 

 



