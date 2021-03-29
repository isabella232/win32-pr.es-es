---
description: COM+ proporciona un modelo de objetos de administración que expone toda la funcionalidad de la herramienta administrativa Servicios de componentes, un front-end gráfico escrito sobre los objetos administrativos.
ms.assetid: f302eb02-2ef5-42ee-a18f-59f7e60b38df
title: Automatizar la administración de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ef3f56da64e442594a7685a77efb9a06e3fe08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153269"
---
# <a name="automating-com-administration"></a><span data-ttu-id="7529c-103">Automatizar la administración de COM+</span><span class="sxs-lookup"><span data-stu-id="7529c-103">Automating COM+ Administration</span></span>

<span data-ttu-id="7529c-104">COM+ proporciona un modelo de objetos de administración que expone toda la funcionalidad de la herramienta administrativa Servicios de componentes, un front-end gráfico escrito sobre los objetos administrativos.</span><span class="sxs-lookup"><span data-stu-id="7529c-104">COM+ provides an administration object model that exposes all of the functionality of the Component Services administrative tool, itself a graphical front end written on top of the administrative objects.</span></span> <span data-ttu-id="7529c-105">Puede usar estos objetos, suministrados por la biblioteca de administración de servicios de componentes (COMAdmin), para automatizar todas las tareas en la administración de aplicaciones y servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="7529c-105">You can use these objects, supplied by the Component Services Administration (COMAdmin) Library, to automate all tasks in the administration of COM+ applications and services.</span></span>

<span data-ttu-id="7529c-106">Los objetos COMAdmin permiten leer y escribir información que se almacena en el catálogo de COM+, el almacén de datos subyacente que contiene todos los datos de configuración de COM+.</span><span class="sxs-lookup"><span data-stu-id="7529c-106">The COMAdmin objects enable you to read and write information that is stored on the COM+ catalog, the underlying data store that holds all COM+ configuration data.</span></span>

<span data-ttu-id="7529c-107">Puede usar estos objetos para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7529c-107">You can use these objects to do the following:</span></span>

-   <span data-ttu-id="7529c-108">Crear y configurar aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="7529c-108">Create and configure COM+ applications.</span></span>
-   <span data-ttu-id="7529c-109">Instalar y exportar aplicaciones COM+ existentes.</span><span class="sxs-lookup"><span data-stu-id="7529c-109">Install and export existing COM+ applications.</span></span>
-   <span data-ttu-id="7529c-110">Administrar aplicaciones COM+ instaladas.</span><span class="sxs-lookup"><span data-stu-id="7529c-110">Manage installed COM+ applications.</span></span>
-   <span data-ttu-id="7529c-111">Administrar y configurar servicios.</span><span class="sxs-lookup"><span data-stu-id="7529c-111">Manage and configure services.</span></span>
-   <span data-ttu-id="7529c-112">Administrar servicios de componentes de forma remota en un equipo diferente.</span><span class="sxs-lookup"><span data-stu-id="7529c-112">Remotely administer Component Services on a different machine.</span></span>

<span data-ttu-id="7529c-113">Puede usar los objetos COMAdmin que admiten scripts con cualquier lenguaje compatible con automatización, como Microsoft Visual Basic y Visual Basic Script.</span><span class="sxs-lookup"><span data-stu-id="7529c-113">You can use the scriptable COMAdmin objects with any Automation-compatible language, such as Microsoft Visual Basic and Visual Basic Script.</span></span> <span data-ttu-id="7529c-114">Puede desarrollar scripts ligeros o herramientas de administración de uso general.</span><span class="sxs-lookup"><span data-stu-id="7529c-114">You can develop either lightweight scripts or general-purpose administration tools.</span></span> <span data-ttu-id="7529c-115">Por ejemplo, puede realizar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7529c-115">For example, you can do the following:</span></span>

-   <span data-ttu-id="7529c-116">Escribir scripts para realizar tareas administrativas rutinarias.</span><span class="sxs-lookup"><span data-stu-id="7529c-116">Write scripts to perform routine administrative tasks.</span></span>
-   <span data-ttu-id="7529c-117">Escribir scripts para automatizar procesos en el desarrollo de aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="7529c-117">Write scripts to automate processes in the development of COM+ applications.</span></span>
-   <span data-ttu-id="7529c-118">Desarrollar herramientas de uso general para administrar y supervisar servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="7529c-118">Develop general-purpose tools for administering and monitoring Component Services.</span></span>
-   <span data-ttu-id="7529c-119">Desarrollar ejecutables de configuración para instalar e implementar la aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="7529c-119">Develop setup executables to install and deploy your COM+ application.</span></span>

<span data-ttu-id="7529c-120">La biblioteca COMAdmin proporciona compatibilidad con versiones anteriores de la biblioteca de administración de MTS 2,0.</span><span class="sxs-lookup"><span data-stu-id="7529c-120">The COMAdmin Library provides backward compatibility with the MTS 2.0 Administration Library.</span></span> <span data-ttu-id="7529c-121">La mayoría de los códigos existentes de administración de MTS 2,0 seguirán funcionando, aunque con algunas excepciones.</span><span class="sxs-lookup"><span data-stu-id="7529c-121">Most existing MTS 2.0 administration code will still work, although with some exceptions.</span></span> <span data-ttu-id="7529c-122">(Consulte [biblioteca de administración de MTS](mts-administration-library.md)).</span><span class="sxs-lookup"><span data-stu-id="7529c-122">(See [MTS Administration Library](mts-administration-library.md).)</span></span>

<span data-ttu-id="7529c-123">Para automatizar la administración de forma eficaz, debe estar familiarizado con las tareas de administración que se realizan con la herramienta administrativa Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="7529c-123">To automate administration effectively, you should be familiar with administration tasks as performed with the Component Services administrative tool.</span></span>

<span data-ttu-id="7529c-124">Para obtener descripciones completas de los objetos COMAdmin y de las interfaces correspondientes, vea la documentación de referencia de COM+ para las clases e interfaces siguientes:</span><span class="sxs-lookup"><span data-stu-id="7529c-124">For full descriptions of the COMAdmin objects and the corresponding interfaces, see the COM+ Reference documentation for the following classes and interfaces:</span></span>

-   [<span data-ttu-id="7529c-125">**COMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="7529c-125">**COMAdminCatalog**</span></span>](comadmincatalog.md)
-   [<span data-ttu-id="7529c-126">**COMAdminCatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="7529c-126">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
-   [<span data-ttu-id="7529c-127">**COMAdminCatalogObject**</span><span class="sxs-lookup"><span data-stu-id="7529c-127">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
-   [<span data-ttu-id="7529c-128">**ICOMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="7529c-128">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
-   [<span data-ttu-id="7529c-129">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="7529c-129">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
-   [<span data-ttu-id="7529c-130">**ICatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="7529c-130">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
-   [<span data-ttu-id="7529c-131">**ICatalogObject**</span><span class="sxs-lookup"><span data-stu-id="7529c-131">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)

<span data-ttu-id="7529c-132">Los temas siguientes de esta sección proporcionan información general para la automatización de la administración con los objetos COMAdmin:</span><span class="sxs-lookup"><span data-stu-id="7529c-132">The following topics in this section provide an overview for automating administration using the COMAdmin objects:</span></span>

-   [<span data-ttu-id="7529c-133">Información general de los objetos COMAdmin</span><span class="sxs-lookup"><span data-stu-id="7529c-133">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
-   [<span data-ttu-id="7529c-134">Recuperar recopilaciones en el catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="7529c-134">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
-   [<span data-ttu-id="7529c-135">Establecer propiedades y guardar cambios en el catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="7529c-135">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
-   [<span data-ttu-id="7529c-136">Control de errores de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="7529c-136">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
-   [<span data-ttu-id="7529c-137">Operaciones de administración de COM+ en transacciones</span><span class="sxs-lookup"><span data-stu-id="7529c-137">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
-   [<span data-ttu-id="7529c-138">Ejemplo introductorio con el catálogo de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="7529c-138">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)

 

 



