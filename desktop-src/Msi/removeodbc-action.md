---
description: La acción RemoveODBC quita los orígenes de datos, los traductores y los controladores que se muestran para su eliminación durante la instalación.
ms.assetid: 548984fd-e4f7-4db8-a625-87b4a0a4bdb2
title: Acción RemoveODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1234ed736a8cb8258bccf3085de92bfb1b324cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667469"
---
# <a name="removeodbc-action"></a><span data-ttu-id="e3fcd-103">Acción RemoveODBC</span><span class="sxs-lookup"><span data-stu-id="e3fcd-103">RemoveODBC Action</span></span>

<span data-ttu-id="e3fcd-104">La acción RemoveODBC quita los orígenes de datos, los traductores y los controladores que se muestran para su eliminación durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="e3fcd-104">The RemoveODBC action removes the data sources, translators, and drivers listed for removal during the installation.</span></span> <span data-ttu-id="e3fcd-105">Esta acción consulta la tabla [ODBCDataSource](odbcdatasource-table.md), la [tabla ODBCTranslator](odbctranslator-table.md)y la tabla [ODBCDriver](odbcdriver-table.md) para cada origen de datos, traductor o controlador programados para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="e3fcd-105">This action queries the [ODBCDataSource table](odbcdatasource-table.md), [ODBCTranslator table](odbctranslator-table.md), and [ODBCDriver table](odbcdriver-table.md) for each data source, translator, or driver scheduled for removal.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e3fcd-106">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="e3fcd-106">Sequence Restrictions</span></span>

<span data-ttu-id="e3fcd-107">No hay restricciones de secuencia.</span><span class="sxs-lookup"><span data-stu-id="e3fcd-107">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e3fcd-108">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="e3fcd-108">ActionData Messages</span></span>

<span data-ttu-id="e3fcd-109">Para cada controlador instalado.</span><span class="sxs-lookup"><span data-stu-id="e3fcd-109">For each driver installed.</span></span>



| <span data-ttu-id="e3fcd-110">Campo</span><span class="sxs-lookup"><span data-stu-id="e3fcd-110">Field</span></span> | <span data-ttu-id="e3fcd-111">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="e3fcd-111">Description of action data</span></span>               |
|-------|------------------------------------------|
| <span data-ttu-id="e3fcd-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="e3fcd-112">\[1\]</span></span> | <span data-ttu-id="e3fcd-113">Descripción del controlador.</span><span class="sxs-lookup"><span data-stu-id="e3fcd-113">Driver description.</span></span> <span data-ttu-id="e3fcd-114">La clave del controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="e3fcd-114">The ODBC driver key.</span></span> |
| <span data-ttu-id="e3fcd-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="e3fcd-115">\[2\]</span></span> | <span data-ttu-id="e3fcd-116">ComponentId</span><span class="sxs-lookup"><span data-stu-id="e3fcd-116">ComponentId</span></span>                              |



 

<span data-ttu-id="e3fcd-117">Para cada traductor instalado.</span><span class="sxs-lookup"><span data-stu-id="e3fcd-117">For each translator installed.</span></span>



| <span data-ttu-id="e3fcd-118">Campo</span><span class="sxs-lookup"><span data-stu-id="e3fcd-118">Field</span></span> | <span data-ttu-id="e3fcd-119">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="e3fcd-119">Description of action data</span></span>               |
|-------|------------------------------------------|
| <span data-ttu-id="e3fcd-120">\[1\]</span><span class="sxs-lookup"><span data-stu-id="e3fcd-120">\[1\]</span></span> | <span data-ttu-id="e3fcd-121">Descripción del controlador.</span><span class="sxs-lookup"><span data-stu-id="e3fcd-121">Driver description.</span></span> <span data-ttu-id="e3fcd-122">La clave del controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="e3fcd-122">The ODBC driver key.</span></span> |
| <span data-ttu-id="e3fcd-123">\[2\]</span><span class="sxs-lookup"><span data-stu-id="e3fcd-123">\[2\]</span></span> | <span data-ttu-id="e3fcd-124">ComponentId</span><span class="sxs-lookup"><span data-stu-id="e3fcd-124">ComponentId</span></span>                              |



 

<span data-ttu-id="e3fcd-125">Para cada origen de datos instalado.</span><span class="sxs-lookup"><span data-stu-id="e3fcd-125">For each data source installed.</span></span>



| <span data-ttu-id="e3fcd-126">Campo</span><span class="sxs-lookup"><span data-stu-id="e3fcd-126">Field</span></span> | <span data-ttu-id="e3fcd-127">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="e3fcd-127">Description of action data</span></span>                              |
|-------|---------------------------------------------------------|
| <span data-ttu-id="e3fcd-128">\[1\]</span><span class="sxs-lookup"><span data-stu-id="e3fcd-128">\[1\]</span></span> | <span data-ttu-id="e3fcd-129">Descripción del controlador.</span><span class="sxs-lookup"><span data-stu-id="e3fcd-129">Driver description.</span></span> <span data-ttu-id="e3fcd-130">La clave del controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="e3fcd-130">The ODBC driver key.</span></span>                |
| <span data-ttu-id="e3fcd-131">\[2\]</span><span class="sxs-lookup"><span data-stu-id="e3fcd-131">\[2\]</span></span> | <span data-ttu-id="e3fcd-132">ComponentId</span><span class="sxs-lookup"><span data-stu-id="e3fcd-132">ComponentId</span></span>                                             |
| <span data-ttu-id="e3fcd-133">\[3\]</span><span class="sxs-lookup"><span data-stu-id="e3fcd-133">\[3\]</span></span> | <span data-ttu-id="e3fcd-134">Registro: SQL \_ Remove \_ DSN o SQL \_ Remove \_ Sys \_ DSN</span><span class="sxs-lookup"><span data-stu-id="e3fcd-134">Registration: SQL\_REMOVE\_DSN or SQL\_REMOVE\_SYS\_DSN</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e3fcd-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3fcd-135">Remarks</span></span>

<span data-ttu-id="e3fcd-136">Si el recuento de uso de ODBC y el recuento de uso de archivo se vuelven cero, se quita el archivo.</span><span class="sxs-lookup"><span data-stu-id="e3fcd-136">If both the ODBC usage count and the file usage count become zero, the file is removed.</span></span> <span data-ttu-id="e3fcd-137">El registro depende de los recuentos de uso de ODBC y la eliminación de archivos se basa en recuentos de referencias clave de dll compartidas.</span><span class="sxs-lookup"><span data-stu-id="e3fcd-137">Registration is dependent on ODBC usage counts and file removal is based on shared DLLs key reference counts.</span></span>

 

 



