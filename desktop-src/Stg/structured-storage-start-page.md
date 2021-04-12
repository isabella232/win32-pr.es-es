---
title: Almacenamiento estructurado
description: El almacenamiento estructurado proporciona persistencia de archivos y datos en COM mediante el control de un único archivo como una colección estructurada de objetos que se conocen como almacenamientos y secuencias.
ms.assetid: 57a5f34d-c3db-47c5-9836-6e2163732d30
keywords:
- Strctd de almacenamiento estructurado STG
- Strctd de almacenamiento estructurado STG, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606fef01d67cd78997f21dcd9008785d30985315
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359164"
---
# <a name="structured-storage"></a><span data-ttu-id="69a86-105">Almacenamiento estructurado</span><span class="sxs-lookup"><span data-stu-id="69a86-105">Structured Storage</span></span>

## <a name="purpose"></a><span data-ttu-id="69a86-106">Propósito</span><span class="sxs-lookup"><span data-stu-id="69a86-106">Purpose</span></span>

<span data-ttu-id="69a86-107">El almacenamiento estructurado proporciona persistencia de archivos y datos en COM mediante el control de un único archivo como una colección estructurada de objetos que se conocen como almacenamientos y secuencias.</span><span class="sxs-lookup"><span data-stu-id="69a86-107">Structured Storage provides file and data persistence in COM by handling a single file as a structured collection of objects known as storages and streams.</span></span>

<span data-ttu-id="69a86-108">El propósito del almacenamiento estructurado es reducir las penalizaciones de rendimiento y la sobrecarga asociada al almacenamiento de objetos independientes en un único archivo.</span><span class="sxs-lookup"><span data-stu-id="69a86-108">The purpose of Structured Storage is to reduce the performance penalties and overhead associated with storing separate objects in a single file.</span></span> <span data-ttu-id="69a86-109">El almacenamiento estructurado proporciona una solución mediante la definición de cómo controlar una sola entidad de archivo como una colección estructurada de dos tipos de flujos y almacenamiento de objetos a través de una implementación estándar denominada archivos compuestos.</span><span class="sxs-lookup"><span data-stu-id="69a86-109">Structured Storage provides a solution by defining how to handle a single file entity as a structured collection of two types of objects storages and streams through a standard implementation called Compound Files.</span></span> <span data-ttu-id="69a86-110">Esto permite al usuario interactuar con un archivo compuesto y administrarlo como si fuera un único archivo en lugar de una jerarquía anidada de objetos independientes.</span><span class="sxs-lookup"><span data-stu-id="69a86-110">This enables the user to interact with, and manage, a compound file as if it were a single file rather than a nested hierarchy of separate objects.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="69a86-111">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="69a86-111">Where applicable</span></span>

<span data-ttu-id="69a86-112">El almacenamiento estructurado puede usarse en sistemas operativos basados en Microsoft COM.</span><span class="sxs-lookup"><span data-stu-id="69a86-112">Structured Storage can be used on Microsoft COM-based operating systems.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="69a86-113">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="69a86-113">Developer audience</span></span>

<span data-ttu-id="69a86-114">La documentación de almacenamiento estructurado está pensada para programadores de C y C++ con experiencia y desarrolladores de sistemas basados en COM.</span><span class="sxs-lookup"><span data-stu-id="69a86-114">The Structured Storage documentation is intended for experienced C and C++ programmers and COM-based system developers.</span></span>

<span data-ttu-id="69a86-115">El almacenamiento estructurado es compatible principalmente con lenguajes de programación de C y C++; sin embargo, cualquier tecnología basada en COM también admitirá cualquier lenguaje de programación que use punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="69a86-115">Structured Storage primarily supports C and C++ programming languages, however any COM-based technology will also support any programming language that utilizes interface pointers.</span></span>

<span data-ttu-id="69a86-116">Una comprensión sólida de las tecnologías COM es un requisito previo para el uso de almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="69a86-116">A solid understanding of COM technologies is prerequisite to the developmental use of Structured Storage.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="69a86-117">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="69a86-117">Run-time requirements</span></span>

<span data-ttu-id="69a86-118">Para obtener más información sobre los sistemas operativos necesarios para usar un determinado elemento de la API, consulte la sección de requisitos de la documentación del elemento.</span><span class="sxs-lookup"><span data-stu-id="69a86-118">For more information about which operating systems are required to use a particular API element, see the Requirements section of the documentation for the element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="69a86-119">En esta sección</span><span class="sxs-lookup"><span data-stu-id="69a86-119">In this section</span></span>



| <span data-ttu-id="69a86-120">Tema</span><span class="sxs-lookup"><span data-stu-id="69a86-120">Topic</span></span>                                                               | <span data-ttu-id="69a86-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="69a86-121">Description</span></span>                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69a86-122">Información general</span><span class="sxs-lookup"><span data-stu-id="69a86-122">Overview</span></span>](about-structured-storage.md)<br/>                 | <span data-ttu-id="69a86-123">Información general sobre el almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="69a86-123">General information about Structured Storage.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="69a86-124">Uso de almacenamiento estructurado</span><span class="sxs-lookup"><span data-stu-id="69a86-124">Using Structured Storage</span></span>](using-structured-storage.md)<br/> | <span data-ttu-id="69a86-125">Uso de la información para el almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="69a86-125">Using information for Structured Storage.</span></span><br/>                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="69a86-126">Referencia</span><span class="sxs-lookup"><span data-stu-id="69a86-126">Reference</span></span>](structured-storage-reference.md)<br/>            | <span data-ttu-id="69a86-127">Documentación de interfaces, funciones, estructuras y enumeraciones específicas de almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="69a86-127">Documentation of Structured Storage specific interfaces, functions, structures, and enumerations.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="69a86-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="69a86-128">Samples</span></span>](samples.md)<br/>                                   | <span data-ttu-id="69a86-129">Ejemplos de código escritos en C++.</span><span class="sxs-lookup"><span data-stu-id="69a86-129">Code examples written in C++.</span></span> <span data-ttu-id="69a86-130">Para obtener más información, vea [nombres en IStorage](names-in-istorage.md), [encabezado del conjunto de propiedades](property-set-header.md), [sección](section.md), almacenamiento de [conjuntos de propiedades](storing-property-sets.md)y [uso de almacenamiento estructurado](using-structured-storage.md).</span><span class="sxs-lookup"><span data-stu-id="69a86-130">For more information, see [Names in IStorage](names-in-istorage.md), [Property Set Header](property-set-header.md), [Section](section.md), [Storing Property Sets](storing-property-sets.md), and [Using Structured Storage](using-structured-storage.md).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="69a86-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="69a86-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="69a86-132">[The Component Object Model](../com/the-component-object-model.md) [Modelo de objetos componentes (COM)]</span><span class="sxs-lookup"><span data-stu-id="69a86-132">[The Component Object Model](../com/the-component-object-model.md)</span></span>
</dt> </dl>

 

