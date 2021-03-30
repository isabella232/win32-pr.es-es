---
description: Agregue un registro a la tabla CustomAction para la acción personalizada Launch.
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: Adición del inicio a las tablas de CustomAction y binarias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbcd1b483505d7d33981d695ed0d29c3b72a3f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156352"
---
# <a name="adding-launch-to-the-customaction-and-binary-tables"></a><span data-ttu-id="5f2a1-103">Adición del inicio a las tablas de CustomAction y binarias</span><span class="sxs-lookup"><span data-stu-id="5f2a1-103">Adding Launch to the CustomAction and Binary Tables</span></span>

<span data-ttu-id="5f2a1-104">Agregue un registro a la [tabla CustomAction](customaction-table.md) para la acción personalizada Launch.</span><span class="sxs-lookup"><span data-stu-id="5f2a1-104">Add a record to the [CustomAction table](customaction-table.md) for the Launch custom action.</span></span> <span data-ttu-id="5f2a1-105">Escriba el nombre de la acción personalizada en la columna Acción de la tabla CustomAction.</span><span class="sxs-lookup"><span data-stu-id="5f2a1-105">Enter the custom action's name in the Action column of the CustomAction table.</span></span> <span data-ttu-id="5f2a1-106">Escriba el tipo numérico total para el inicio, 65, en la columna tipo de la tabla de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="5f2a1-106">Enter the total numeric type for Launch, 65, into the Type column of the Custom action table.</span></span> <span data-ttu-id="5f2a1-107">La columna de origen de la tabla CustomAction especifica una clave en el registro de la [tabla binaria](binary-table.md) que contiene los datos binarios de la dll.</span><span class="sxs-lookup"><span data-stu-id="5f2a1-107">The Source column of the CustomAction table specifies a key into the record of the [Binary Table](binary-table.md) that contains the binary data for the DLL.</span></span> <span data-ttu-id="5f2a1-108">Escriba Tutorial.dll en la columna origen de la tabla CustomAction.</span><span class="sxs-lookup"><span data-stu-id="5f2a1-108">Enter Tutorial.dll into the Source column of the CustomAction table.</span></span> <span data-ttu-id="5f2a1-109">El punto de entrada especificado en el campo de destino de la tabla CustomAction debe coincidir con el exportado desde el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="5f2a1-109">The entry point specified in the Target field of the CustomAction table must match that exported from the DLL.</span></span> <span data-ttu-id="5f2a1-110">Escriba LaunchTutorial en la columna target de la tabla CustomAction.</span><span class="sxs-lookup"><span data-stu-id="5f2a1-110">Enter LaunchTutorial into the Target column of the CustomAction table.</span></span>

[<span data-ttu-id="5f2a1-111">Tabla CustomAction</span><span class="sxs-lookup"><span data-stu-id="5f2a1-111">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="5f2a1-112">Acción</span><span class="sxs-lookup"><span data-stu-id="5f2a1-112">Action</span></span> | <span data-ttu-id="5f2a1-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f2a1-113">Type</span></span> | <span data-ttu-id="5f2a1-114">Source</span><span class="sxs-lookup"><span data-stu-id="5f2a1-114">Source</span></span>       | <span data-ttu-id="5f2a1-115">Destino</span><span class="sxs-lookup"><span data-stu-id="5f2a1-115">Target</span></span>         |
|--------|------|--------------|----------------|
| <span data-ttu-id="5f2a1-116">Launch</span><span class="sxs-lookup"><span data-stu-id="5f2a1-116">Launch</span></span> | <span data-ttu-id="5f2a1-117">65</span><span class="sxs-lookup"><span data-stu-id="5f2a1-117">65</span></span>   | <span data-ttu-id="5f2a1-118">Tutorial.dll</span><span class="sxs-lookup"><span data-stu-id="5f2a1-118">Tutorial.dll</span></span> | <span data-ttu-id="5f2a1-119">LaunchTutorial</span><span class="sxs-lookup"><span data-stu-id="5f2a1-119">LaunchTutorial</span></span> |



 

<span data-ttu-id="5f2a1-120">Agregue el Tutorial.dll que creó en tutorial. cpp como una secuencia binaria a la tabla binaria.</span><span class="sxs-lookup"><span data-stu-id="5f2a1-120">Add the Tutorial.dll you created from Tutorial.cpp as a binary stream to the Binary table.</span></span>

[<span data-ttu-id="5f2a1-121">Tabla binaria</span><span class="sxs-lookup"><span data-stu-id="5f2a1-121">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="5f2a1-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="5f2a1-122">Name</span></span>         | <span data-ttu-id="5f2a1-123">Datos</span><span class="sxs-lookup"><span data-stu-id="5f2a1-123">Data</span></span>                          |
|--------------|-------------------------------|
| <span data-ttu-id="5f2a1-124">Tutorial.dll</span><span class="sxs-lookup"><span data-stu-id="5f2a1-124">Tutorial.dll</span></span> | <span data-ttu-id="5f2a1-125">{*datos binarios agregados para dll*}</span><span class="sxs-lookup"><span data-stu-id="5f2a1-125">{*binary data added for DLL*}</span></span> |



 

<span data-ttu-id="5f2a1-126">Continúe [agregando un evento de control al final de la instalación para ejecutar el inicio](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).</span><span class="sxs-lookup"><span data-stu-id="5f2a1-126">Continue to [Adding a Control Event at the End of the Installation to Run Launch](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).</span></span>

 

 



