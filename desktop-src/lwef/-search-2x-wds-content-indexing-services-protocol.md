---
title: Protocolo de servicios de indexación de contenido
description: Este documento es una especificación del protocolo del servicio de indización de contenido.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c22bbda912333368e50d3e4a8ace2cd98856ea
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "103789316"
---
# <a name="content-indexing-services-protocol"></a><span data-ttu-id="8457e-103">Protocolo de servicios de indexación de contenido</span><span class="sxs-lookup"><span data-stu-id="8457e-103">Content Indexing Services Protocol</span></span>

> [!NOTE]
> <span data-ttu-id="8457e-104">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8457e-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="8457e-105">En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="8457e-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="8457e-106">Especificación del Protocolo, versión 0,12</span><span class="sxs-lookup"><span data-stu-id="8457e-106">Protocol Specification, Version 0.12</span></span>

-   [<span data-ttu-id="8457e-107">1 Introducción</span><span class="sxs-lookup"><span data-stu-id="8457e-107">1 Introduction</span></span>](#1-introduction)
    -   [<span data-ttu-id="8457e-108">1.1 Glosario</span><span class="sxs-lookup"><span data-stu-id="8457e-108">1.1 Glossary</span></span>](#11-glossary)
    -   [<span data-ttu-id="8457e-109">1.2 Referencias</span><span class="sxs-lookup"><span data-stu-id="8457e-109">1.2 References</span></span>](#12-references)
    -   [<span data-ttu-id="8457e-110">Información general del protocolo 1,3 (Sinopsis)</span><span class="sxs-lookup"><span data-stu-id="8457e-110">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
    -   [<span data-ttu-id="8457e-111">1.4 Relación con otros protocolos</span><span class="sxs-lookup"><span data-stu-id="8457e-111">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
    -   [<span data-ttu-id="8457e-112">1,5 requisitos previos y condiciones previas</span><span class="sxs-lookup"><span data-stu-id="8457e-112">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
    -   [<span data-ttu-id="8457e-113">1.6 Declaración de aplicabilidad</span><span class="sxs-lookup"><span data-stu-id="8457e-113">1.6 Applicability Statement</span></span>](#16-applicability-statement)
    -   [<span data-ttu-id="8457e-114">1.7 Control de versiones y negociación de funcionalidad</span><span class="sxs-lookup"><span data-stu-id="8457e-114">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
    -   [<span data-ttu-id="8457e-115">1.8 Campos extensibles por el proveedor</span><span class="sxs-lookup"><span data-stu-id="8457e-115">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
    -   [<span data-ttu-id="8457e-116">1.9 Asignaciones de estándares</span><span class="sxs-lookup"><span data-stu-id="8457e-116">1.9 Standards Assignments</span></span>](#19-standards-assignments)
-   [<span data-ttu-id="8457e-117">2 Mensajes</span><span class="sxs-lookup"><span data-stu-id="8457e-117">2 Messages</span></span>](#2-messages)
    -   [<span data-ttu-id="8457e-118">2.1 Transporte</span><span class="sxs-lookup"><span data-stu-id="8457e-118">2.1 Transport</span></span>](#21-transport)
    -   [<span data-ttu-id="8457e-119">2.2 Sintaxis de mensajes</span><span class="sxs-lookup"><span data-stu-id="8457e-119">2.2 Message Syntax</span></span>](#22-message-syntax)
-   [<span data-ttu-id="8457e-120">3 Detalles del protocolo</span><span class="sxs-lookup"><span data-stu-id="8457e-120">3 Protocol Details</span></span>](#3-protocol-details)
    -   [<span data-ttu-id="8457e-121">Detalles del servidor 3,1</span><span class="sxs-lookup"><span data-stu-id="8457e-121">3.1 Server Details</span></span>](#31-server-details)
    -   [<span data-ttu-id="8457e-122">Detalles del cliente 3,2</span><span class="sxs-lookup"><span data-stu-id="8457e-122">3.2 Client Details</span></span>](#32-client-details)
-   [<span data-ttu-id="8457e-123">4 Ejemplos de protocolo</span><span class="sxs-lookup"><span data-stu-id="8457e-123">4 Protocol Examples</span></span>](#4-protocol-examples)
    -   [<span data-ttu-id="8457e-124">4,1 ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="8457e-124">4.1 Example 1</span></span>](#41-example-1)
    -   [<span data-ttu-id="8457e-125">ejemplo 2 de 4,2</span><span class="sxs-lookup"><span data-stu-id="8457e-125">4.2 Example 2</span></span>](#42-example-2)
-   [<span data-ttu-id="8457e-126">5 Seguridad</span><span class="sxs-lookup"><span data-stu-id="8457e-126">5 Security</span></span>](#5-security)
    -   [<span data-ttu-id="8457e-127">5.1 Consideraciones de seguridad para los implementadores</span><span class="sxs-lookup"><span data-stu-id="8457e-127">5.1 Security Considerations for Implementers</span></span>](#51-security-considerations-for-implementers)
    -   [<span data-ttu-id="8457e-128">5.2 Índice de parámetros de seguridad</span><span class="sxs-lookup"><span data-stu-id="8457e-128">5.2 Index of Security Parameters</span></span>](#52-index-of-security-parameters)
-   [<span data-ttu-id="8457e-129">6 índice de comportamiento específico de la versión</span><span class="sxs-lookup"><span data-stu-id="8457e-129">6 Index of Version Specific Behavior</span></span>](#6-index-of-version-specific-behavior)

<span data-ttu-id="8457e-130">Este documento es una especificación del protocolo del servicio de indización de contenido.</span><span class="sxs-lookup"><span data-stu-id="8457e-130">This document is a specification of the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="8457e-131">La documentación del programa de protocolo de servidor de grupo de trabajo (WSPP) está pensada para su uso junto con la documentación de estándares públicos, material de programación para redes y conceptos de sistemas distribuidos de Windows Workgroup, y da por supuesto que el lector está familiarizado con el material mencionado anteriormente o tiene acceso inmediato a él.</span><span class="sxs-lookup"><span data-stu-id="8457e-131">The Workgroup Server Protocol Program (WSPP) documentation is intended for use in conjunction with public standards documentation, network programming art, and Windows workgroup distributed systems concepts, and assumes that the reader either is familiar with the aforementioned material or has immediate access to it.</span></span>

<span data-ttu-id="8457e-132">Una especificación del protocolo WSPP no requiere el uso de las herramientas de programación de Microsoft o los entornos de programación para que un licenciatario desarrolle una implementación.</span><span class="sxs-lookup"><span data-stu-id="8457e-132">A WSPP protocol specification does not require the use of Microsoft programming tools or programming environments in order for a Licensee to develop an implementation.</span></span> <span data-ttu-id="8457e-133">Los licenciatarios que tienen acceso a las herramientas y los entornos de programación de Microsoft pueden aprovecharlos de forma gratuita.</span><span class="sxs-lookup"><span data-stu-id="8457e-133">Licensees who have access to Microsoft programming tools and environments are free to take advantage of them.</span></span>

## <a name="1-introduction"></a><span data-ttu-id="8457e-134">1 Introducción</span><span class="sxs-lookup"><span data-stu-id="8457e-134">1 Introduction</span></span>

-   [<span data-ttu-id="8457e-135">1.1 Glosario</span><span class="sxs-lookup"><span data-stu-id="8457e-135">1.1 Glossary</span></span>](#11-glossary)
-   [<span data-ttu-id="8457e-136">1.2 Referencias</span><span class="sxs-lookup"><span data-stu-id="8457e-136">1.2 References</span></span>](#12-references)
-   [<span data-ttu-id="8457e-137">Información general del protocolo 1,3 (Sinopsis)</span><span class="sxs-lookup"><span data-stu-id="8457e-137">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
-   [<span data-ttu-id="8457e-138">1.4 Relación con otros protocolos</span><span class="sxs-lookup"><span data-stu-id="8457e-138">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
-   [<span data-ttu-id="8457e-139">1,5 requisitos previos y condiciones previas</span><span class="sxs-lookup"><span data-stu-id="8457e-139">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
-   [<span data-ttu-id="8457e-140">1.6 Declaración de aplicabilidad</span><span class="sxs-lookup"><span data-stu-id="8457e-140">1.6 Applicability Statement</span></span>](#16-applicability-statement)
-   [<span data-ttu-id="8457e-141">1.7 Control de versiones y negociación de funcionalidad</span><span class="sxs-lookup"><span data-stu-id="8457e-141">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
-   [<span data-ttu-id="8457e-142">1.8 Campos extensibles por el proveedor</span><span class="sxs-lookup"><span data-stu-id="8457e-142">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
-   [<span data-ttu-id="8457e-143">1.9 Asignaciones de estándares</span><span class="sxs-lookup"><span data-stu-id="8457e-143">1.9 Standards Assignments</span></span>](#19-standards-assignments)

### <a name="11-glossary"></a><span data-ttu-id="8457e-144">1.1 Glosario</span><span class="sxs-lookup"><span data-stu-id="8457e-144">1.1 Glossary</span></span>

> [!Note]  
> <span data-ttu-id="8457e-145">Los siguientes términos se definen en la sección Glosario de \[ MS-sys \] :</span><span class="sxs-lookup"><span data-stu-id="8457e-145">The following terms are defined in the Glossary section of \[MS-SYS\]:</span></span>
>
> -   <span data-ttu-id="8457e-146">GUID</span><span class="sxs-lookup"><span data-stu-id="8457e-146">GUID</span></span>
> -   <span data-ttu-id="8457e-147">Little endian</span><span class="sxs-lookup"><span data-stu-id="8457e-147">Little Endian</span></span>
> -   <span data-ttu-id="8457e-148">Canalización con nombre</span><span class="sxs-lookup"><span data-stu-id="8457e-148">Named Pipe</span></span>
> -   <span data-ttu-id="8457e-149">Ruta</span><span class="sxs-lookup"><span data-stu-id="8457e-149">Path</span></span>

 

<span data-ttu-id="8457e-150">**Binding**: una solicitud para incluir una **columna** determinada en un **conjunto de filas** devuelto.</span><span class="sxs-lookup"><span data-stu-id="8457e-150">**Binding**: A request to include a particular **column** in a returned **rowset** .</span></span> <span data-ttu-id="8457e-151">El **enlace** especifica una propiedad que se va a incluir en los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8457e-151">The **binding** specifies a property to be included in the search results.</span></span>

<span data-ttu-id="8457e-152">**Marcador**: un marcador que identifica de forma única una fila dentro de un conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-152">**Bookmark**: A marker that uniquely identifies a row within a set of rows.</span></span>

<span data-ttu-id="8457e-153">**Catálogo**: la unidad de la organización de nivel superior del servicio de Index Server.</span><span class="sxs-lookup"><span data-stu-id="8457e-153">**Catalog**: The highest-level unit of organization in the indexing service.</span></span> <span data-ttu-id="8457e-154">Representa un conjunto de documentos indizados en los que se pueden ejecutar consultas mediante el protocolo del servicio de indización de contenido.</span><span class="sxs-lookup"><span data-stu-id="8457e-154">It represents a set of indexed documents against which queries can be executed using the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="8457e-155">**Categoría**: una agrupación jerárquica de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-155">**Category**: A hierarchical grouping of rows.</span></span> <span data-ttu-id="8457e-156">Por ejemplo, el resultado de una consulta que contiene columnas de autor y título se puede clasificar en función del autor.</span><span class="sxs-lookup"><span data-stu-id="8457e-156">For example, a query result containing author and title columns can be categorized based on author.</span></span> <span data-ttu-id="8457e-157">Cada grupo de filas que contiene el mismo valor para autor constituiría una categoría.</span><span class="sxs-lookup"><span data-stu-id="8457e-157">Each group of rows containing the same value for author would constitute a category.</span></span>

<span data-ttu-id="8457e-158">**Chapter** : un intervalo de **filas** dentro de un conjunto de **filas** .</span><span class="sxs-lookup"><span data-stu-id="8457e-158">**Chapter** : A range of **rows** within a set of **rows** .</span></span>

<span data-ttu-id="8457e-159">**Columna**: el contenedor para un único tipo de información de una **fila** .</span><span class="sxs-lookup"><span data-stu-id="8457e-159">**Column**: The container for a single type of information in a **row** .</span></span> <span data-ttu-id="8457e-160">Las columnas se asignan a los nombres de propiedad y especifican las propiedades que se usan para los elementos de **árbol** de **comandos** de la consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8457e-160">Columns map to property names, and specify which properties are used for the search query's **command** **tree** elements.</span></span>

<span data-ttu-id="8457e-161">**Árbol de comandos**: combinación de **restricciones** , **categorías** y **criterios de ordenación** especificados para la consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8457e-161">**Command Tree**: A combination of **restrictions** , **categories** , and **sort orders** specified for the search query.</span></span>

<span data-ttu-id="8457e-162">**Cursor**: una entidad que se usa como mecanismo para trabajar con una **fila** o un pequeño bloque de **filas** a la vez en un conjunto de datos devueltos en un conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="8457e-162">**Cursor**: An entity that is used as a mechanism to work with one **row** or a small block of **rows** at a time in a set of data returned in a result set.</span></span> <span data-ttu-id="8457e-163">Un **cursor** se coloca en una única **fila** dentro del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="8457e-163">A **cursor** is positioned on a single **row** within the result set.</span></span> <span data-ttu-id="8457e-164">Una vez que el **cursor** se coloca en una fila, se pueden realizar operaciones en esa **fila** o en un bloque de **filas** a partir de esa posición.</span><span class="sxs-lookup"><span data-stu-id="8457e-164">After the **cursor** is positioned on a row, operations can be performed on that **row** , or on a block of **rows** starting at that position.</span></span>

<span data-ttu-id="8457e-165">**Handle**: un token que se puede usar para identificar y tener acceso a **cursores** , **capítulos** y **marcadores** .</span><span class="sxs-lookup"><span data-stu-id="8457e-165">**Handle**: A token that can be used to identify and access **cursors** , **chapters** , and **bookmarks** .</span></span>

<span data-ttu-id="8457e-166">**Index**: estructura persistente que contiene el contenido de texto extraído de archivos por un **servicio de indización** .</span><span class="sxs-lookup"><span data-stu-id="8457e-166">**Index**: A persistent structure that contains the text content pulled out of files by an **indexing service** .</span></span> <span data-ttu-id="8457e-167">Esto incluye la lista de palabras, que se almacenan junto con el nombre de archivo contenedor, la ubicación de la palabra y la **configuración regional** .</span><span class="sxs-lookup"><span data-stu-id="8457e-167">This includes the list of words, which are stored along with the containing file name, word location, and **locale** .</span></span>

<span data-ttu-id="8457e-168">**Indexación**: proceso de extracción de texto y propiedades de archivos y almacenamiento de los valores extraídos en los **índices** (para texto) y **en la caché de propiedades** (para propiedades).</span><span class="sxs-lookup"><span data-stu-id="8457e-168">**Indexing**: The process of extracting text and properties from files and storing the extracted values into the **indexes** (for text), and the **property cache** (for properties).</span></span>

<span data-ttu-id="8457e-169">**Servicio de indexación**: servicio que crea **catálogos** indexados para el contenido y las propiedades de los sistemas de archivos.</span><span class="sxs-lookup"><span data-stu-id="8457e-169">**Indexing Service**: A service that creates indexed **catalogs** for the contents and properties of file systems.</span></span> <span data-ttu-id="8457e-170">Las aplicaciones pueden buscar información en los catálogos de los archivos del sistema de archivos indizado.</span><span class="sxs-lookup"><span data-stu-id="8457e-170">Applications can search the catalogs for information from the files on the indexed file system.</span></span>

<span data-ttu-id="8457e-171">**Locale**: un identificador, como se especifica en el apéndice a de \[ MS-GPSI \] , que especifica las preferencias relacionadas con el idioma.</span><span class="sxs-lookup"><span data-stu-id="8457e-171">**Locale**: An identifier, as specified in \[MS-GPSI\] Appendix A, that specifies preferences related to language.</span></span> <span data-ttu-id="8457e-172">Estas preferencias indican cómo se va a dar formato a las fechas y horas, los elementos se ordenarán alfabéticamente, las cadenas se compararán, etc.</span><span class="sxs-lookup"><span data-stu-id="8457e-172">These preferences indicate how dates and times are to be formatted, items are to be sorted alphabetically, strings are to be compared, and so on.</span></span>

<span data-ttu-id="8457e-173">**Consulta en lenguaje natural**: consulta construida con la sintaxis de consulta de lenguaje humano en lugar de.</span><span class="sxs-lookup"><span data-stu-id="8457e-173">**Natural Language Query**: A query constructed using human language instead of query syntax.</span></span>

<span data-ttu-id="8457e-174">**Palabra irrelevante**: palabra omitida por el servicio de indización cuando está presente en las **restricciones** especificadas para la consulta de búsqueda porque tiene un pequeño valor discriminado.</span><span class="sxs-lookup"><span data-stu-id="8457e-174">**Noise word**: A word that is ignored by the indexing service when present in the **restrictions** specified for the search query because it has little discriminatory value.</span></span> <span data-ttu-id="8457e-175">Entre los ejemplos en inglés se incluyen "a", "and" y "The".</span><span class="sxs-lookup"><span data-stu-id="8457e-175">English examples include "a", "and" and "the".</span></span>

<span data-ttu-id="8457e-176">**Caché** de propiedades: memoria caché de propiedades de archivo extraídas por un **servicio de indización** .</span><span class="sxs-lookup"><span data-stu-id="8457e-176">**Property Cache**: A cache of file properties extracted by an **indexing service** .</span></span>

<span data-ttu-id="8457e-177">**Indexación de propiedades**: proceso de creación de un **Índice** de propiedades de **tipo de valor** de un documento, incluidos el autor, el asunto, el tipo, el recuento de palabras, el recuento de páginas impresas y cualquier otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-177">**Property Indexing**: The process of creating an **index** of **value-type properties** of a document, including author, subject, type, word count, printed page count, and any other properties.</span></span>

<span data-ttu-id="8457e-178">**Restricción**: un conjunto de condiciones que un archivo debe cumplir para que se incluyan en los resultados de búsqueda devueltos por el **servicio de indización** en respuesta a una consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8457e-178">**Restriction**: A set of conditions that a file must meet to be included in the search results returned by the **indexing service** in response to a search query.</span></span> <span data-ttu-id="8457e-179">Una **restricción** reduce el foco de una consulta de búsqueda, limitando los archivos que el **servicio de indexación** incluirá en los resultados de la búsqueda a solo aquellos que cumplan las condiciones.</span><span class="sxs-lookup"><span data-stu-id="8457e-179">A **restriction** narrows the focus of a search query, limiting the files that the **indexing service** will include in the search results to only those that match the conditions.</span></span>

<span data-ttu-id="8457e-180">**Row**: la colección de **columnas** , que contiene los valores de propiedad que describen un solo archivo del conjunto de archivos que coinciden con las **restricciones** especificadas en la consulta de búsqueda enviada al **servicio de indización** .</span><span class="sxs-lookup"><span data-stu-id="8457e-180">**Row**: The collection of **columns** , containing the property values that describe a single file from the set of files that matched the **restrictions** specified in the search query submitted to the **indexing service** .</span></span>

<span data-ttu-id="8457e-181">Conjunto de **filas**: conjunto de **filas** devueltas en los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8457e-181">**Rowset**: A set of **rows** returned in the search results.</span></span>

<span data-ttu-id="8457e-182">Criterio de **ordenación**: conjunto de reglas de una consulta de búsqueda que definen el orden de las filas en el resultado de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8457e-182">**Sort Order**: The set of rules in a search query that define the ordering of rows in the search result.</span></span> <span data-ttu-id="8457e-183">Cada regla se compone de una propiedad (nombre, tamaño, etc.) y una dirección para la ordenación (ascendente o descendente).</span><span class="sxs-lookup"><span data-stu-id="8457e-183">Each rule consists of a property (name, size, etc.) and a direction for the ordering (ascending or descending).</span></span> <span data-ttu-id="8457e-184">Varias reglas se aplican secuencialmente</span><span class="sxs-lookup"><span data-stu-id="8457e-184">Multiple rules are applied sequentially</span></span>

<span data-ttu-id="8457e-185">**Propiedad de tipo de texto**: una propiedad que describe el contenido de un documento y solo tiene texto sin formato asociado a su nombre.</span><span class="sxs-lookup"><span data-stu-id="8457e-185">**Text-type Property**: A property that describes the content of a document and has only unformatted text associated with its name.</span></span>

<span data-ttu-id="8457e-186">**Propiedad de tipo de valor**: una propiedad que describe un solo atributo de un documento completo.</span><span class="sxs-lookup"><span data-stu-id="8457e-186">**Value-type Property**: A property that describes a single attribute of an entire document.</span></span> <span data-ttu-id="8457e-187">Una propiedad de tipo de valor tiene un identificador de tipo de datos y un valor de ese tipo de datos asociado a su nombre.</span><span class="sxs-lookup"><span data-stu-id="8457e-187">A value-type property has a data type ID and a value of that data type associated with its name.</span></span>

<span data-ttu-id="8457e-188">**Raíz virtual**: ruta de acceso alternativa a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="8457e-188">**Virtual Root**: An alternate path to a folder.</span></span> <span data-ttu-id="8457e-189">Una carpeta física puede tener cero o más raíces virtuales.</span><span class="sxs-lookup"><span data-stu-id="8457e-189">A physical folder can have zero or more virtual roots.</span></span> <span data-ttu-id="8457e-190">Las rutas de acceso que comienzan por una raíz virtual se denominan rutas de acceso virtuales.</span><span class="sxs-lookup"><span data-stu-id="8457e-190">Paths beginning with a virtual root are called virtual paths.</span></span> <span data-ttu-id="8457e-191">Por ejemplo,/Server/vanityroot podría ser una raíz virtual de C: \\ IIS \\ Web \\ Folder1.</span><span class="sxs-lookup"><span data-stu-id="8457e-191">For example, /server/vanityroot might be a virtual root of C:\\IIS\\web\\folder1.</span></span> <span data-ttu-id="8457e-192">A continuación, el archivo C: \\ IIS \\ web \\ Folder1 \\default.htm tendría una ruta de acceso virtual de/Server/vanityroot/default.htm.</span><span class="sxs-lookup"><span data-stu-id="8457e-192">Then the file C:\\IIS\\web\\folder1\\default.htm would have a virtual path of /server/vanityroot/default.htm.</span></span>

<span data-ttu-id="8457e-193">**Mayo,** debe, no debe, no debe: estos términos (en mayúsculas) se usan tal y como se describe en \[ RFC2119 \] .</span><span class="sxs-lookup"><span data-stu-id="8457e-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT**: These terms (in all caps) are used as described in \[RFC2119\].</span></span> <span data-ttu-id="8457e-194">Todas las instrucciones de comportamiento opcional utilizan MAY, SHOULD o SHOULD NOT.</span><span class="sxs-lookup"><span data-stu-id="8457e-194">All statements of optional behavior use either MAY, SHOULD, or SHOULD NOT.</span></span>

### <a name="12-references"></a><span data-ttu-id="8457e-195">1.2 Referencias</span><span class="sxs-lookup"><span data-stu-id="8457e-195">1.2 References</span></span>

### <a name="121-normative-references"></a><span data-ttu-id="8457e-196">1.2.1 Referencias de normativa</span><span class="sxs-lookup"><span data-stu-id="8457e-196">1.2.1 Normative References</span></span>

<span data-ttu-id="8457e-197">\[IEEE754 \] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point aritmético", IEEE 754-1985, 1985 de octubre, https://standards.ieee.org/standard/754-1985.html</span><span class="sxs-lookup"><span data-stu-id="8457e-197">\[IEEE754\] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span></span>

<span data-ttu-id="8457e-198">\[MS-DCOM \] Microsoft Corporation, "protocolos remotos del modelo de objetos de componentes distribuidos", el 2006 de junio.</span><span class="sxs-lookup"><span data-stu-id="8457e-198">\[MS-DCOM\] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", June 2006.</span></span>

<span data-ttu-id="8457e-199">\[MS-GPSI \] Microsoft Corporation, "Directiva de grupo de instalación de software Extension", junio 2006.</span><span class="sxs-lookup"><span data-stu-id="8457e-199">\[MS-GPSI\] Microsoft Corporation, "Group Policy Software Installation Extension", June 2006.</span></span>

<span data-ttu-id="8457e-200">\[MS-SMB \] Microsoft Corporation, "Protocolo de bloque de mensajes del servidor de Microsoft (SMB) y extensiones", 2006 de mayo.</span><span class="sxs-lookup"><span data-stu-id="8457e-200">\[MS-SMB\] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions," May 2006.</span></span>

<span data-ttu-id="8457e-201">\[MS-SYS \] Microsoft Corporation, "información general del sistema V4", 2006 de julio.</span><span class="sxs-lookup"><span data-stu-id="8457e-201">\[MS-SYS\] Microsoft Corporation, "System Overview v4", July 2006.</span></span>

<span data-ttu-id="8457e-202">\[SALTon \] salon, G., "procesamiento de texto automático: el análisis y la recuperación de la información por equipo", 1988 y ISBN 0-201-2227-8.</span><span class="sxs-lookup"><span data-stu-id="8457e-202">\[SALTON\] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span></span>

<span data-ttu-id="8457e-203">\[Unicode \] (Unicode Consortium), "The Unicode Standard, Version 2,0", 1996, https://www.unicode.org</span><span class="sxs-lookup"><span data-stu-id="8457e-203">\[UNICODE\] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span></span>

### <a name="122-informative-references"></a><span data-ttu-id="8457e-204">1.2.2 Referencias informativas</span><span class="sxs-lookup"><span data-stu-id="8457e-204">1.2.2 Informative References</span></span>

<span data-ttu-id="8457e-205">\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .</span><span class="sxs-lookup"><span data-stu-id="8457e-205">\[MSDN-OLEDB\] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp.</span></span>

<span data-ttu-id="8457e-206">\[MSDN-QUERYERR \] Microsoft Corporation, Query-Execution valores, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span><span class="sxs-lookup"><span data-stu-id="8457e-206">\[MSDN-QUERYERR\] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span></span>

### <a name="13-protocol-overview-synopsis"></a><span data-ttu-id="8457e-207">Información general del protocolo 1,3 (Sinopsis)</span><span class="sxs-lookup"><span data-stu-id="8457e-207">1.3 Protocol Overview (Synopsis)</span></span>

<span data-ttu-id="8457e-208">Un **servicio de indización** de contenido ayuda a organizar de manera eficaz las características extraídas de una colección de documentos.</span><span class="sxs-lookup"><span data-stu-id="8457e-208">A content **indexing service** helps efficiently organize the extracted features of a collection of documents.</span></span> <span data-ttu-id="8457e-209">El protocolo del servicio de indización de contenido (CISP) permite a un cliente comunicarse con un servidor que hospeda un servicio de indización para emitir consultas y permitir que un administrador administre el servidor de indexación.</span><span class="sxs-lookup"><span data-stu-id="8457e-209">The Content Indexing Service Protocol (CISP) allows a client to communicate with a server hosting an indexing service to issue queries and to allow an administrator to manage the indexing server.</span></span>

<span data-ttu-id="8457e-210">Al procesar archivos, un servicio de indización analiza un conjunto de documentos y reorganiza su contenido de tal forma que **las propiedades** de esos documentos se pueden devolver eficazmente en respuesta a las consultas.</span><span class="sxs-lookup"><span data-stu-id="8457e-210">When processing files, an indexing service analyzes a set of documents and reorganizes their content in such a way that **properties** of those documents can be efficiently returned in response to queries.</span></span> <span data-ttu-id="8457e-211">Una colección de documentos que se pueden consultar se compone de un **Catálogo** .</span><span class="sxs-lookup"><span data-stu-id="8457e-211">A collection of documents that can be queried comprises a **catalog** .</span></span> <span data-ttu-id="8457e-212">Un catálogo puede contener un **Índice** (para una referencia rápida a texto) y una **caché de propiedades** (para una recuperación rápida de los valores de propiedad).</span><span class="sxs-lookup"><span data-stu-id="8457e-212">A catalog may contain an **index** (for quick reference to text) and a **property cache** (for quick retrieval of property values).</span></span>

<span data-ttu-id="8457e-213">Conceptualmente, un catálogo consta de una "tabla" lógica de propiedades con el texto o el valor y la configuración regional correspondiente almacenada en **las columnas** de la tabla.</span><span class="sxs-lookup"><span data-stu-id="8457e-213">Conceptually, a catalog consists of a logical "table" of properties with the text or value and corresponding locale stored in **columns** of the table.</span></span> <span data-ttu-id="8457e-214">Cada "fila" de la tabla corresponde a un documento independiente en el ámbito del catálogo y cada "columna" de la tabla corresponde a una propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-214">Each "row" of the table corresponds to a separate document in the scope of the catalog and each "column" of the table corresponds to a property.</span></span>

<span data-ttu-id="8457e-215">Las tareas específicas realizadas por CISP se agrupan en dos áreas funcionales:</span><span class="sxs-lookup"><span data-stu-id="8457e-215">The specific tasks performed by CISP are grouped into two functional areas:</span></span>

-   <span data-ttu-id="8457e-216">Administración remota de catálogos de servicios de Index Server,</span><span class="sxs-lookup"><span data-stu-id="8457e-216">Remote administration of indexing service catalogs,</span></span>
-   <span data-ttu-id="8457e-217">Consulta remota de catálogos de servicios de Index Server.</span><span class="sxs-lookup"><span data-stu-id="8457e-217">Remote querying of indexing service catalogs.</span></span>

### <a name="131-remote-administration-tasks"></a><span data-ttu-id="8457e-218">1.3.1 tareas de administración remota</span><span class="sxs-lookup"><span data-stu-id="8457e-218">1.3.1 Remote Administration Tasks</span></span>

<span data-ttu-id="8457e-219">CISP permite las siguientes tareas de administración de catálogos de servicios de Index Server desde un cliente:</span><span class="sxs-lookup"><span data-stu-id="8457e-219">CISP enables the following indexing service catalog management tasks from a client:</span></span>

-   <span data-ttu-id="8457e-220">Consultar el estado actual de un catálogo de servicios de Index Server en el servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-220">Query the current state of an indexing service catalog on the server.</span></span>
-   <span data-ttu-id="8457e-221">Actualice el estado de un catálogo de servicios de Index Server.</span><span class="sxs-lookup"><span data-stu-id="8457e-221">Update the state of an indexing service catalog.</span></span>
-   <span data-ttu-id="8457e-222">Inicia el proceso de indización de un conjunto determinado de archivos.</span><span class="sxs-lookup"><span data-stu-id="8457e-222">Launch the indexing process for a particular set of files.</span></span>
-   <span data-ttu-id="8457e-223">Inicie la optimización de un índice con el fin de mejorar el rendimiento de las consultas.</span><span class="sxs-lookup"><span data-stu-id="8457e-223">Initiate optimization of an index in order to improve query performance.</span></span>

<span data-ttu-id="8457e-224">Todas las tareas de administración remota siguen un modelo de solicitud/respuesta simple.</span><span class="sxs-lookup"><span data-stu-id="8457e-224">All remote administration tasks follow a simple request/response model.</span></span> <span data-ttu-id="8457e-225">No se mantiene ningún estado en el cliente para ninguna llamada de administración y las llamadas administrativas se pueden realizar en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="8457e-225">No state is maintained on the client for any administration call and administrative calls can be made in any order.</span></span>

### <a name="132-remote-querying"></a><span data-ttu-id="8457e-226">1.3.2 consultas remotas</span><span class="sxs-lookup"><span data-stu-id="8457e-226">1.3.2 Remote Querying</span></span>

<span data-ttu-id="8457e-227">CISP permite a los clientes realizar consultas de búsqueda en un servidor remoto que hospeda un servicio de indexación.</span><span class="sxs-lookup"><span data-stu-id="8457e-227">CISP enables clients to perform search queries against a remote server hosting an indexing service.</span></span>

<span data-ttu-id="8457e-228">El envío de una consulta de búsqueda es un proceso de varios pasos Iniciado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-228">Sending a search query is a multi-step process initiated by the client.</span></span> <span data-ttu-id="8457e-229">Los pasos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="8457e-229">The steps are as follows:</span></span>

1.  <span data-ttu-id="8457e-230">El cliente solicita una conexión a un servidor que hospeda un servicio de indización.</span><span class="sxs-lookup"><span data-stu-id="8457e-230">The client requests a connection to a server hosting an indexing service.</span></span>
2.  <span data-ttu-id="8457e-231">El cliente envía los parámetros de la consulta de búsqueda, que incluyen:</span><span class="sxs-lookup"><span data-stu-id="8457e-231">The client sends the parameters for the search query, which include:</span></span>
    -   <span data-ttu-id="8457e-232">Las **restricciones** para especificar qué documentos se van a incluir o excluir de los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8457e-232">The **restrictions** to specify which documents are to be included and/or excluded from the search results.</span></span>
    -   <span data-ttu-id="8457e-233">El orden en el que se van a devolver los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8457e-233">The order in which the search results are to be returned.</span></span>
    -   <span data-ttu-id="8457e-234">Columnas que se van a devolver en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="8457e-234">The columns to be returned in the result set.</span></span>
    -   <span data-ttu-id="8457e-235">Número máximo de **filas** que se deben devolver para la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-235">The maximum number of **rows** that should be returned for the query.</span></span>
    -   <span data-ttu-id="8457e-236">Tiempo máximo de ejecución de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-236">The maximum time for query execution.</span></span>

        <span data-ttu-id="8457e-237">Una vez que el servidor ha confirmado la solicitud del cliente para iniciar la consulta, el cliente puede solicitar información de estado sobre la consulta, pero no es un paso necesario.</span><span class="sxs-lookup"><span data-stu-id="8457e-237">Once the server has acknowledged the client's request to initiate the query, the client can request status information about the query, but this is not a required step.</span></span>

3.  <span data-ttu-id="8457e-238">Después, el cliente especifica las propiedades que el servidor debe incluir en los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8457e-238">The client then specifies which properties the server should include in the search results.</span></span>
4.  <span data-ttu-id="8457e-239">El cliente solicita un conjunto de resultados del servidor y el servidor responde enviando al cliente los valores de propiedad de los archivos incluidos en los resultados de la consulta de búsqueda del cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-239">The client requests a result set from the server, and the server responds by sending the client the property values for files that were included in the results for the client's search query.</span></span> <span data-ttu-id="8457e-240">Si el valor de una propiedad es demasiado grande para caber en un búfer de respuesta único, el servidor no enviará la propiedad pero, en su lugar, establecerá el estado de la propiedad en diferido.</span><span class="sxs-lookup"><span data-stu-id="8457e-240">If the value of a property is too large to fit in a single response buffer the server will not send the property but instead will set the property status to deferred.</span></span> <span data-ttu-id="8457e-241">Después, el cliente solicita el valor de propiedad por separado usando una serie de solicitudes para fragmentos sucesivos del valor y, a continuación, reanuda la solicitud de otros valores.</span><span class="sxs-lookup"><span data-stu-id="8457e-241">The client then requests the property value separately using a series of requests for successive chunks of the value, and then resumes requesting other values.</span></span>
5.  <span data-ttu-id="8457e-242">Una vez que el cliente finaliza con la consulta de búsqueda y ya no requiere resultados adicionales, el cliente se pone en contacto con el servidor para liberar la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-242">Once the client is finished with the search query and no longer requires additional results, the client contacts the server to release the query.</span></span>
6.  <span data-ttu-id="8457e-243">Una vez que el servidor haya lanzado la consulta, el cliente puede enviar una solicitud para desconectarse del servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-243">Once the server has released the query, the client may send a request to disconnect from the server.</span></span> <span data-ttu-id="8457e-244">A continuación, se cierra la conexión.</span><span class="sxs-lookup"><span data-stu-id="8457e-244">The connection is then closed.</span></span> <span data-ttu-id="8457e-245">Como alternativa, el cliente puede emitir otra consulta y repetir la secuencia del paso 2.</span><span class="sxs-lookup"><span data-stu-id="8457e-245">Alternatively, the client may issue another query and repeat the sequence from the step 2.</span></span>

<span data-ttu-id="8457e-246">Comportamiento de Windows: este protocolo se implementa en Windows 2000, Windows XP, Windows Server 2003 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8457e-246">Windows Behavior: This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span>

### <a name="14-relationship-to-other-protocols"></a><span data-ttu-id="8457e-247">1.4 Relación con otros protocolos</span><span class="sxs-lookup"><span data-stu-id="8457e-247">1.4 Relationship to Other Protocols</span></span>

<span data-ttu-id="8457e-248">CISP se basa en el protocolo SMB \[ MS-SMB \] para el transporte de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8457e-248">The CISP relies on the SMB \[MS-SMB\] protocol for message transport.</span></span> <span data-ttu-id="8457e-249">Ningún otro protocolo depende directamente del protocolo del servicio de indización de contenido.</span><span class="sxs-lookup"><span data-stu-id="8457e-249">No other protocol depends directly on the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="8457e-250">*Comportamiento de Windows: las aplicaciones suelen interactuar con un contenedor de interfaz OLE DB \[ MSDN-OleDb \] (por ejemplo, un cliente de protocolo) y no directamente con el protocolo.*</span><span class="sxs-lookup"><span data-stu-id="8457e-250">*Windows Behavior: Applications typically interact with an OLE DB interface wrapper \[MSDN-OLEDB\] (e.g., a protocol client) and not directly with the protocol.*</span></span>

### <a name="15-prerequisites-and-preconditions"></a><span data-ttu-id="8457e-251">1,5 requisitos previos y condiciones previas</span><span class="sxs-lookup"><span data-stu-id="8457e-251">1.5 Prerequisites and Preconditions</span></span>

<span data-ttu-id="8457e-252">Se supone que el cliente ha obtenido el nombre del servidor y un nombre de catálogo antes de que se invoque este protocolo.</span><span class="sxs-lookup"><span data-stu-id="8457e-252">It is assumed that the client has obtained the name of the server and a catalog name before this protocol is invoked.</span></span> <span data-ttu-id="8457e-253">Cómo hace un cliente esto está fuera del ámbito de esta especificación.</span><span class="sxs-lookup"><span data-stu-id="8457e-253">How a client does this is outside of the scope of this specification.</span></span>

<span data-ttu-id="8457e-254">También se supone que el cliente y el servidor tienen una asociación de seguridad que se puede usar con las canalizaciones con nombre \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="8457e-254">It is also assumed that the client and server have a security association usable with named pipes \[MS-SMB\].</span></span>

### <a name="16-applicability-statement"></a><span data-ttu-id="8457e-255">1.6 Declaración de aplicabilidad</span><span class="sxs-lookup"><span data-stu-id="8457e-255">1.6 Applicability Statement</span></span>

<span data-ttu-id="8457e-256">CISP está diseñado para consultar y administrar catálogos en un servidor remoto desde un cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-256">CISP is designed for querying and managing catalogs on a remote server from a client.</span></span> <span data-ttu-id="8457e-257">CISP está en desuso en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8457e-257">CISP is deprecated on Windows Vista.</span></span>

### <a name="17-versioning-and-capability-negotiation"></a><span data-ttu-id="8457e-258">1.7 Control de versiones y negociación de funcionalidad</span><span class="sxs-lookup"><span data-stu-id="8457e-258">1.7 Versioning and Capability Negotiation</span></span>

<span data-ttu-id="8457e-259">Este protocolo no tiene ningún mecanismo de control de versiones o de negociación de capacidad.</span><span class="sxs-lookup"><span data-stu-id="8457e-259">This protocol has no versioning or capability negotiation mechanisms.</span></span>

### <a name="18-vendor-extensible-fields"></a><span data-ttu-id="8457e-260">1.8 Campos extensibles por el proveedor</span><span class="sxs-lookup"><span data-stu-id="8457e-260">1.8 Vendor-Extensible Fields</span></span>

<span data-ttu-id="8457e-261">Este protocolo usa Valores HRESULT que son extensibles.</span><span class="sxs-lookup"><span data-stu-id="8457e-261">This protocol uses HRESULTs which are vendor-extensible.</span></span> <span data-ttu-id="8457e-262">Los proveedores pueden elegir sus propios valores para este campo, siempre que el bit C (0x20000000) esté establecido como se especifica en la sección 4.1.1 de \[ MS-sys \] , lo que indica que es un código de cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-262">Vendors are free to choose their own values for this field, as long as the C bit (0x20000000) is set as specified in Section 4.1.1 of \[MS-SYS\], indicating it is a customer code.</span></span>

<span data-ttu-id="8457e-263">Este protocolo también usa los valores de NTSTATUS tomados del espacio de número de NTSTATUS definido en \[ MS-sys \] .</span><span class="sxs-lookup"><span data-stu-id="8457e-263">This protocol also uses NTSTATUS values taken from the NTSTATUS number space defined in \[MS-SYS\].</span></span> <span data-ttu-id="8457e-264">Los proveedores deben reutilizar esos valores con el significado indicado.</span><span class="sxs-lookup"><span data-stu-id="8457e-264">Vendors SHOULD reuse those values with their indicated meaning.</span></span> <span data-ttu-id="8457e-265">Al elegir cualquier otro valor se corre el riesgo de una colisión en el futuro.</span><span class="sxs-lookup"><span data-stu-id="8457e-265">Choosing any other value runs the risk of a collision in the future.</span></span>

<span data-ttu-id="8457e-266">*Comportamiento de Windows: Windows solo usa los valores especificados en la sección 4.1.3 de \[ MS-sys \] .*</span><span class="sxs-lookup"><span data-stu-id="8457e-266">*Windows Behavior: Windows only uses the values specified in Section 4.1.3 of \[MS-SYS\].*</span></span>

### <a name="181-property-ids"></a><span data-ttu-id="8457e-267">Identificadores de propiedad de 1.8.1</span><span class="sxs-lookup"><span data-stu-id="8457e-267">1.8.1 Property IDs</span></span>

<span data-ttu-id="8457e-268">Las propiedades se representan mediante identificadores conocidos como identificadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-268">Properties are represented by IDs known as Property IDs.</span></span> <span data-ttu-id="8457e-269">Cada propiedad debe tener un identificador único global.</span><span class="sxs-lookup"><span data-stu-id="8457e-269">Each property must have a globally unique identifier.</span></span> <span data-ttu-id="8457e-270">Este identificador se compone de un **GUID** que representa una colección de propiedades denominada un conjunto de propiedades más una cadena o un entero de 32 bits para identificar la propiedad dentro del conjunto.</span><span class="sxs-lookup"><span data-stu-id="8457e-270">This identifier consists of a **GUID** representing a collection of properties called a property set plus either a string or 32-bit integer to identify the property within the set.</span></span> <span data-ttu-id="8457e-271">Si se utiliza la forma de entero de ID, se considera que los valores 0x00000000, 0xFFFFFFFF y 0xFFFFFFFE no son válidos.</span><span class="sxs-lookup"><span data-stu-id="8457e-271">If the integer form of ID is used, then the values 0x00000000, 0xFFFFFFFF and 0xFFFFFFFE are considered invalid.</span></span>

<span data-ttu-id="8457e-272">Los proveedores pueden garantizar que sus propiedades se definen de forma exclusiva colocándolas en un conjunto de propiedades definido por su propio GUID.</span><span class="sxs-lookup"><span data-stu-id="8457e-272">Vendors can guarantee their properties are uniquely defined by placing them in a property set defined by their own GUID.</span></span>

### <a name="19-standards-assignments"></a><span data-ttu-id="8457e-273">1.9 Asignaciones de estándares</span><span class="sxs-lookup"><span data-stu-id="8457e-273">1.9 Standards Assignments</span></span>

<span data-ttu-id="8457e-274">Este protocolo no tiene asignaciones de estándares, solo las asignaciones privadas realizadas por Microsoft mediante procedimientos de asignación especificados en otros protocolos.</span><span class="sxs-lookup"><span data-stu-id="8457e-274">This protocol has no standards assignments, only private assignments made by Microsoft using allocation procedures specified in other protocols.</span></span>

<span data-ttu-id="8457e-275">Microsoft ha asignado a este protocolo una canalización con nombre, tal y como se especifica en \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="8457e-275">Microsoft has allocated this protocol a named pipe as specified in \[MS-SMB\].</span></span> <span data-ttu-id="8457e-276">La asignación es:</span><span class="sxs-lookup"><span data-stu-id="8457e-276">The assignment is:</span></span>



| <span data-ttu-id="8457e-277">Parámetro</span><span class="sxs-lookup"><span data-stu-id="8457e-277">Parameter</span></span> | <span data-ttu-id="8457e-278">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-278">Value</span></span>             | <span data-ttu-id="8457e-279">Referencia</span><span class="sxs-lookup"><span data-stu-id="8457e-279">Reference</span></span>  |
|-----------|-------------------|------------|
| <span data-ttu-id="8457e-280">Nombre de canalización</span><span class="sxs-lookup"><span data-stu-id="8457e-280">Pipe name</span></span> | <span data-ttu-id="8457e-281">\\canalización de \\ CI \_ SKADS</span><span class="sxs-lookup"><span data-stu-id="8457e-281">\\pipe\\CI\_SKADS</span></span> | <span data-ttu-id="8457e-282">\[SMB DE MS\]</span><span class="sxs-lookup"><span data-stu-id="8457e-282">\[MS-SMB\]</span></span> |



 

## <a name="2-messages"></a><span data-ttu-id="8457e-283">2 Mensajes</span><span class="sxs-lookup"><span data-stu-id="8457e-283">2 Messages</span></span>

-   [<span data-ttu-id="8457e-284">2.1 Transporte</span><span class="sxs-lookup"><span data-stu-id="8457e-284">2.1 Transport</span></span>](#21-transport)
-   [<span data-ttu-id="8457e-285">2.2 Sintaxis de mensajes</span><span class="sxs-lookup"><span data-stu-id="8457e-285">2.2 Message Syntax</span></span>](#22-message-syntax)

### <a name="21-transport"></a><span data-ttu-id="8457e-286">2.1 Transporte</span><span class="sxs-lookup"><span data-stu-id="8457e-286">2.1 Transport</span></span>

<span data-ttu-id="8457e-287">Todos los mensajes se deben transportar mediante una canalización con nombre, como se especifica en \[ MS-SMB \] .</span><span class="sxs-lookup"><span data-stu-id="8457e-287">All messages MUST be transported using a named pipe, as specified in \[MS-SMB\].</span></span> <span data-ttu-id="8457e-288">Se usa el siguiente nombre de canalización:</span><span class="sxs-lookup"><span data-stu-id="8457e-288">The following pipe name is used:</span></span>

-   <span data-ttu-id="8457e-289">\\canalización de \\ CI \_ SKADS</span><span class="sxs-lookup"><span data-stu-id="8457e-289">\\pipe\\CI\_SKADS</span></span>

<span data-ttu-id="8457e-290">Este protocolo usa el protocolo de canalización con nombre SMB subyacente para recuperar la identidad del autor de la llamada que realizó la conexión como se especifica en la sección 2.2.8 de \[ MS-SMB \] ; el cliente debe establecer la identificación de seguridad \_ como ImpersonationLevel en la solicitud para abrir la canalización con nombre.</span><span class="sxs-lookup"><span data-stu-id="8457e-290">This protocol uses the underlying SMB named pipe protocol to retrieve the identity of the caller that made the connection as specified in Section 2.2.8 of \[MS-SMB\]; the client MUST set SECURITY\_IDENTIFICATION as the ImpersonationLevel in the request to open the named pipe.</span></span>

### <a name="22-message-syntax"></a><span data-ttu-id="8457e-291">2.2 Sintaxis de mensajes</span><span class="sxs-lookup"><span data-stu-id="8457e-291">2.2 Message Syntax</span></span>

<span data-ttu-id="8457e-292">Varias estructuras y mensajes en las secciones siguientes hacen referencia a los identificadores de capítulo o marcador.</span><span class="sxs-lookup"><span data-stu-id="8457e-292">Several structures and messages in the following sections refer to chapter or bookmark handles.</span></span> <span data-ttu-id="8457e-293">Un identificador es una estructura opaca larga de 32 bits que identifica de forma única un capítulo o marcador.</span><span class="sxs-lookup"><span data-stu-id="8457e-293">A handle is a 32-bit long opaque structure which uniquely identifies a chapter or bookmark.</span></span> <span data-ttu-id="8457e-294">Normalmente, las aplicaciones cliente reciben valores de identificador a través de llamadas a métodos. sin embargo, hay varios valores bien conocidos que no es necesario obtener de un servidor, cuyo significado se especifica en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-294">Typically, client applications receive handle values via method calls; however there are several well known values which need not be obtained from a server, the meaning of which is specified in the following table:</span></span>



| <span data-ttu-id="8457e-295">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-295">Value</span></span>                         | <span data-ttu-id="8457e-296">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-296">Meaning</span></span>                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-297">DB \_ null \_ HCHAPTER 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8457e-297">DB\_NULL\_HCHAPTER 0x00000000</span></span> | <span data-ttu-id="8457e-298">Identificador de capítulo del conjunto de filas no chaptered, que contiene todos los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-298">A chapter handle to the unchaptered rowset, containing all query results.</span></span>    |
| <span data-ttu-id="8457e-299">DBBMK \_ primero 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-299">DBBMK\_FIRST 0x00000001</span></span>       | <span data-ttu-id="8457e-300">Identificador de marcador de un marcador que identifica la primera fila del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-300">A bookmark handle to a bookmark that identifies the first row in the rowset.</span></span> |
| <span data-ttu-id="8457e-301">DBBMK \_ Last 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8457e-301">DBBMK\_LAST 0x00000002</span></span>        | <span data-ttu-id="8457e-302">Identificador de marcador de un marcador que identifica la última fila del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-302">A bookmark handle to a bookmark that identifies the last row in the rowset.</span></span>  |



 

### <a name="221-structures"></a><span data-ttu-id="8457e-303">2.2.1 estructuras</span><span class="sxs-lookup"><span data-stu-id="8457e-303">2.2.1 Structures</span></span>

<span data-ttu-id="8457e-304">En esta sección se detallan las estructuras de datos que CISP define y usa.</span><span class="sxs-lookup"><span data-stu-id="8457e-304">This section details data structures that are defined and used by CISP.</span></span>

<span data-ttu-id="8457e-305">Todos los enteros con y sin signo de 2, 4 y 8 bytes de las siguientes estructuras deben transferirse en orden de bytes Little-Endian.</span><span class="sxs-lookup"><span data-stu-id="8457e-305">All 2-, 4- and 8-byte signed and unsigned integers in the following structures MUST be transferred in little-endian byte order.</span></span>

<span data-ttu-id="8457e-306">En la tabla siguiente se resumen las estructuras de datos definidas en esta sección.</span><span class="sxs-lookup"><span data-stu-id="8457e-306">The following table summarizes the data structures defined in this section.</span></span>



| <span data-ttu-id="8457e-307">Estructura</span><span class="sxs-lookup"><span data-stu-id="8457e-307">Structure</span></span>                    | <span data-ttu-id="8457e-308">Descripción</span><span class="sxs-lookup"><span data-stu-id="8457e-308">Description</span></span>                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-309">CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="8457e-309">CBaseStorageVariant</span></span>          | <span data-ttu-id="8457e-310">Contiene el valor en el que se realiza una operación de coincidencia para una propiedad especificada en una estructura CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="8457e-310">Contains the value on which to perform a match operation for a property specified in a CPropertyRestriction structure.</span></span> |
| <span data-ttu-id="8457e-311">SAFEARRAY, SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="8457e-311">SAFEARRAY, SAFEARRAY2</span></span>        | <span data-ttu-id="8457e-312">Contiene una matriz multidimensional.</span><span class="sxs-lookup"><span data-stu-id="8457e-312">Contains a multidimensional array.</span></span>                                                                                     |
| <span data-ttu-id="8457e-313">SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="8457e-313">SAFEARRAYBOUND</span></span>               | <span data-ttu-id="8457e-314">Representa los límites de una dimensión de una matriz especificada en una estructura SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="8457e-314">Represents the bounds for a dimension of an array specified in a SAFEARRAY structure.</span></span>                                  |
| <span data-ttu-id="8457e-315">CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="8457e-315">CFullPropSpec</span></span>                | <span data-ttu-id="8457e-316">Contiene una especificación de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-316">Contains a property specification.</span></span>                                                                                     |
| <span data-ttu-id="8457e-317">CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-317">CContentRestriction</span></span>          | <span data-ttu-id="8457e-318">Contiene una cadena que debe coincidir con un valor de propiedad en la caché de propiedades.</span><span class="sxs-lookup"><span data-stu-id="8457e-318">Contains a string to match for a property value in the property cache.</span></span>                                                 |
| <span data-ttu-id="8457e-319">CKey</span><span class="sxs-lookup"><span data-stu-id="8457e-319">CKey</span></span>                         | <span data-ttu-id="8457e-320">Contiene un valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-320">Contains a property value.</span></span>                                                                                             |
| <span data-ttu-id="8457e-321">CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-321">CInternalPropertyRestriction</span></span> | <span data-ttu-id="8457e-322">Contiene un valor de propiedad que debe coincidir con una operación.</span><span class="sxs-lookup"><span data-stu-id="8457e-322">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="8457e-323">CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-323">CNatLanguageRestriction</span></span>      | <span data-ttu-id="8457e-324">Contiene una coincidencia de consulta de lenguaje natural para una propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-324">Contains a natural language query match for a property.</span></span>                                                                |
| <span data-ttu-id="8457e-325">CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-325">CNodeRestriction</span></span>             | <span data-ttu-id="8457e-326">Contiene una matriz de nodos de árbol de comandos que especifican las restricciones de una consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-326">Contains an array of command tree nodes specifying the restrictions for a query.</span></span>                                       |
| <span data-ttu-id="8457e-327">COccRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-327">COccRestriction</span></span>              | <span data-ttu-id="8457e-328">Contiene la ubicación de una palabra en una frase.</span><span class="sxs-lookup"><span data-stu-id="8457e-328">Contains the location of a word in a phrase.</span></span>                                                                           |
| <span data-ttu-id="8457e-329">CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-329">CPropertyRestriction</span></span>         | <span data-ttu-id="8457e-330">Contiene un valor de propiedad que debe coincidir con una operación.</span><span class="sxs-lookup"><span data-stu-id="8457e-330">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="8457e-331">CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-331">CRangeRestriction</span></span>            | <span data-ttu-id="8457e-332">Contiene una restricción de un intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="8457e-332">Contains a restriction on a range of values.</span></span>                                                                           |
| <span data-ttu-id="8457e-333">CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-333">CScopeRestriction</span></span>            | <span data-ttu-id="8457e-334">Contiene una restricción de los archivos que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="8457e-334">Contains a restriction on the files to be searched.</span></span>                                                                    |
| <span data-ttu-id="8457e-335">CSort</span><span class="sxs-lookup"><span data-stu-id="8457e-335">CSort</span></span>                        | <span data-ttu-id="8457e-336">Identifica una columna que se va a ordenar.</span><span class="sxs-lookup"><span data-stu-id="8457e-336">Identifies a column to sort.</span></span>                                                                                           |
| <span data-ttu-id="8457e-337">CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-337">CSynRestriction</span></span>              | <span data-ttu-id="8457e-338">Contiene una palabra o sus sinónimos para una frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-338">Contains a word or its synonyms for a query phrase.</span></span>                                                                    |
| <span data-ttu-id="8457e-339">CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-339">CVectorRestriction</span></span>           | <span data-ttu-id="8457e-340">Contiene una operación ponderada o en un nodo de árbol de comandos.</span><span class="sxs-lookup"><span data-stu-id="8457e-340">Contains a weighted OR operation on a command tree node.</span></span>                                                               |
| <span data-ttu-id="8457e-341">CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-341">CWordRestriction</span></span>             | <span data-ttu-id="8457e-342">Contiene una palabra para una frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-342">Contains a word for a query phrase.</span></span>                                                                                    |
| <span data-ttu-id="8457e-343">CRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-343">CRestriction</span></span>                 | <span data-ttu-id="8457e-344">Contiene un nodo de un árbol de comandos de consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-344">Contains a node of a query command tree.</span></span>                                                                               |
| <span data-ttu-id="8457e-345">CColumnSet</span><span class="sxs-lookup"><span data-stu-id="8457e-345">CColumnSet</span></span>                   | <span data-ttu-id="8457e-346">Indica el número de columnas que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="8457e-346">Indicates the number of columns to return.</span></span>                                                                             |
| <span data-ttu-id="8457e-347">CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="8457e-347">CCategorizationSet</span></span>           | <span data-ttu-id="8457e-348">Contiene información acerca de la agrupación de un conjunto de resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-348">Contains information about the grouping of a set of query results.</span></span>                                                     |
| <span data-ttu-id="8457e-349">CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="8457e-349">CCategorizationSpec</span></span>          | <span data-ttu-id="8457e-350">Contiene una definición de categorías en las que se clasificarán los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-350">Contains a definition of categories into which query results will be categorized.</span></span>                                      |
| <span data-ttu-id="8457e-351">CDbColId</span><span class="sxs-lookup"><span data-stu-id="8457e-351">CDbColId</span></span>                     | <span data-ttu-id="8457e-352">Contiene una columna.</span><span class="sxs-lookup"><span data-stu-id="8457e-352">Contains a column.</span></span>                                                                                                     |
| <span data-ttu-id="8457e-353">CDbProp</span><span class="sxs-lookup"><span data-stu-id="8457e-353">CDbProp</span></span>                      | <span data-ttu-id="8457e-354">Contiene una propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-354">Contains a property.</span></span>                                                                                                   |
| <span data-ttu-id="8457e-355">CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="8457e-355">CDbPropSet</span></span>                   | <span data-ttu-id="8457e-356">Contiene un conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="8457e-356">Contains a set of properties.</span></span>                                                                                          |
| <span data-ttu-id="8457e-357">CPidMapper</span><span class="sxs-lookup"><span data-stu-id="8457e-357">CPidMapper</span></span>                   | <span data-ttu-id="8457e-358">Contiene una matriz de identificadores de propiedad que especifican las propiedades que se van a devolver en un conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-358">Contains an array of property IDs specifying the properties to return in a rowset.</span></span>                                     |
| <span data-ttu-id="8457e-359">CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="8457e-359">CRowSeekAt</span></span>                   | <span data-ttu-id="8457e-360">Contiene el desplazamiento en el que se recuperan filas en un mensaje CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="8457e-360">Contains the offset at which to retrieve rows in a CPMGetRowsIn message</span></span>                                                |
| <span data-ttu-id="8457e-361">CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="8457e-361">CRowSeekAtRatio</span></span>              | <span data-ttu-id="8457e-362">Identifica el punto en el que se va a iniciar la recuperación de un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-362">Identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>                                           |
| <span data-ttu-id="8457e-363">CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="8457e-363">CRowSeekByBookmark</span></span>           | <span data-ttu-id="8457e-364">Identifica los marcadores de los que se van a recuperar filas de un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-364">Identifies the bookmarks from which to retrieve rows for a CPMGetRowsIn message.</span></span>                                       |
| <span data-ttu-id="8457e-365">CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="8457e-365">CRowSeekNext</span></span>                 | <span data-ttu-id="8457e-366">Contiene el número de filas que se van a omitir en un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-366">Contains the number of rows to skip in a CPMGetRowsIn message.</span></span>                                                         |
| <span data-ttu-id="8457e-367">CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="8457e-367">CRowsetProperties</span></span>            | <span data-ttu-id="8457e-368">Contiene la información de configuración de una consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-368">Contains the configuration information for a query.</span></span>                                                                    |
| <span data-ttu-id="8457e-369">CSortSet</span><span class="sxs-lookup"><span data-stu-id="8457e-369">CSortSet</span></span>                     | <span data-ttu-id="8457e-370">Contiene el criterio de ordenación de una consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-370">Contains the sort order for a query.</span></span>                                                                                   |
| <span data-ttu-id="8457e-371">CTableColumn</span><span class="sxs-lookup"><span data-stu-id="8457e-371">CTableColumn</span></span>                 | <span data-ttu-id="8457e-372">Contiene una columna para el mensaje CPMSetBindings.</span><span class="sxs-lookup"><span data-stu-id="8457e-372">Contains a column for the CPMSetBindings message.</span></span>                                                                      |
| <span data-ttu-id="8457e-373">SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="8457e-373">SERIALIZEDPROPERTYVALUE</span></span>      | <span data-ttu-id="8457e-374">Contiene un valor serializado.</span><span class="sxs-lookup"><span data-stu-id="8457e-374">Contains a serialized value.</span></span>                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a><span data-ttu-id="8457e-375">2.2.1.1 CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="8457e-375">2.2.1.1 CBaseStorageVariant</span></span>

<span data-ttu-id="8457e-376">La estructura CBaseStorageVariant contiene el valor en el que se realiza una operación de coincidencia para una propiedad especificada en la estructura CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="8457e-376">The CBaseStorageVariant structure contains the value on which to perform a match operation for a property specified in the CPropertyRestriction structure.</span></span>



<span data-ttu-id="8457e-377">0</span><span class="sxs-lookup"><span data-stu-id="8457e-377">0</span></span>

<span data-ttu-id="8457e-378">1</span><span class="sxs-lookup"><span data-stu-id="8457e-378">1</span></span>

<span data-ttu-id="8457e-379">2</span><span class="sxs-lookup"><span data-stu-id="8457e-379">2</span></span>

<span data-ttu-id="8457e-380">3</span><span class="sxs-lookup"><span data-stu-id="8457e-380">3</span></span>

<span data-ttu-id="8457e-381">4</span><span class="sxs-lookup"><span data-stu-id="8457e-381">4</span></span>

<span data-ttu-id="8457e-382">5</span><span class="sxs-lookup"><span data-stu-id="8457e-382">5</span></span>

<span data-ttu-id="8457e-383">6</span><span class="sxs-lookup"><span data-stu-id="8457e-383">6</span></span>

<span data-ttu-id="8457e-384">7</span><span class="sxs-lookup"><span data-stu-id="8457e-384">7</span></span>

<span data-ttu-id="8457e-385">8</span><span class="sxs-lookup"><span data-stu-id="8457e-385">8</span></span>

<span data-ttu-id="8457e-386">9</span><span class="sxs-lookup"><span data-stu-id="8457e-386">9</span></span>

<span data-ttu-id="8457e-387">1</span><span class="sxs-lookup"><span data-stu-id="8457e-387">1</span></span><br/> <span data-ttu-id="8457e-388">0</span><span class="sxs-lookup"><span data-stu-id="8457e-388">0</span></span><br/>

<span data-ttu-id="8457e-389">1</span><span class="sxs-lookup"><span data-stu-id="8457e-389">1</span></span>

<span data-ttu-id="8457e-390">2</span><span class="sxs-lookup"><span data-stu-id="8457e-390">2</span></span>

<span data-ttu-id="8457e-391">3</span><span class="sxs-lookup"><span data-stu-id="8457e-391">3</span></span>

<span data-ttu-id="8457e-392">4</span><span class="sxs-lookup"><span data-stu-id="8457e-392">4</span></span>

<span data-ttu-id="8457e-393">5</span><span class="sxs-lookup"><span data-stu-id="8457e-393">5</span></span>

<span data-ttu-id="8457e-394">6</span><span class="sxs-lookup"><span data-stu-id="8457e-394">6</span></span>

<span data-ttu-id="8457e-395">7</span><span class="sxs-lookup"><span data-stu-id="8457e-395">7</span></span>

<span data-ttu-id="8457e-396">8</span><span class="sxs-lookup"><span data-stu-id="8457e-396">8</span></span>

<span data-ttu-id="8457e-397">9</span><span class="sxs-lookup"><span data-stu-id="8457e-397">9</span></span>

<span data-ttu-id="8457e-398">2</span><span class="sxs-lookup"><span data-stu-id="8457e-398">2</span></span><br/> <span data-ttu-id="8457e-399">0</span><span class="sxs-lookup"><span data-stu-id="8457e-399">0</span></span><br/>

<span data-ttu-id="8457e-400">1</span><span class="sxs-lookup"><span data-stu-id="8457e-400">1</span></span>

<span data-ttu-id="8457e-401">2</span><span class="sxs-lookup"><span data-stu-id="8457e-401">2</span></span>

<span data-ttu-id="8457e-402">3</span><span class="sxs-lookup"><span data-stu-id="8457e-402">3</span></span>

<span data-ttu-id="8457e-403">4</span><span class="sxs-lookup"><span data-stu-id="8457e-403">4</span></span>

<span data-ttu-id="8457e-404">5</span><span class="sxs-lookup"><span data-stu-id="8457e-404">5</span></span>

<span data-ttu-id="8457e-405">6</span><span class="sxs-lookup"><span data-stu-id="8457e-405">6</span></span>

<span data-ttu-id="8457e-406">7</span><span class="sxs-lookup"><span data-stu-id="8457e-406">7</span></span>

<span data-ttu-id="8457e-407">8</span><span class="sxs-lookup"><span data-stu-id="8457e-407">8</span></span>

<span data-ttu-id="8457e-408">9</span><span class="sxs-lookup"><span data-stu-id="8457e-408">9</span></span>

<span data-ttu-id="8457e-409">3</span><span class="sxs-lookup"><span data-stu-id="8457e-409">3</span></span><br/> <span data-ttu-id="8457e-410">0</span><span class="sxs-lookup"><span data-stu-id="8457e-410">0</span></span><br/>

<span data-ttu-id="8457e-411">1</span><span class="sxs-lookup"><span data-stu-id="8457e-411">1</span></span>

<span data-ttu-id="8457e-412">vType</span><span class="sxs-lookup"><span data-stu-id="8457e-412">vType</span></span>

<span data-ttu-id="8457e-413">vData1</span><span class="sxs-lookup"><span data-stu-id="8457e-413">vData1</span></span>

<span data-ttu-id="8457e-414">vData2</span><span class="sxs-lookup"><span data-stu-id="8457e-414">vData2</span></span>

<span data-ttu-id="8457e-415">vValue (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-415">vValue (variable)</span></span>



 

<span data-ttu-id="8457e-416">**vType**: un indicador de tipo que indica el tipo de vValue.</span><span class="sxs-lookup"><span data-stu-id="8457e-416">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="8457e-417">DEBE ser uno de los valores de VARENUM especificados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8457e-417">It MUST be one of the VARENUM values specified in the following table.</span></span>



| <span data-ttu-id="8457e-418">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-418">Value</span></span>                 | <span data-ttu-id="8457e-419">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-419">Meaning</span></span>                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-420">VT \_ vacío (0x0000)</span><span class="sxs-lookup"><span data-stu-id="8457e-420">VT\_EMPTY (0x0000)</span></span>    | <span data-ttu-id="8457e-421">vValue no está presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-421">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="8457e-422">VT \_ null (0x0001)</span><span class="sxs-lookup"><span data-stu-id="8457e-422">VT\_NULL (0x0001)</span></span>     | <span data-ttu-id="8457e-423">vValue no está presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-423">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="8457e-424">VT \_ I1 (0x0010)</span><span class="sxs-lookup"><span data-stu-id="8457e-424">VT\_I1 (0x0010)</span></span>       | <span data-ttu-id="8457e-425">Entero de 1 byte con signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-425">A 1-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="8457e-426">VT \_ UI1 (0x0011)</span><span class="sxs-lookup"><span data-stu-id="8457e-426">VT\_UI1 (0x0011)</span></span>      | <span data-ttu-id="8457e-427">Entero de 1 byte sin signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-427">A 1-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="8457e-428">VT \_ i2 (0x0002)</span><span class="sxs-lookup"><span data-stu-id="8457e-428">VT\_I2 (0x0002)</span></span>       | <span data-ttu-id="8457e-429">Entero de 2 bytes con signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-429">A 2-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="8457e-430">VT \_ UI2 (0x0012)</span><span class="sxs-lookup"><span data-stu-id="8457e-430">VT\_UI2 (0x0012)</span></span>      | <span data-ttu-id="8457e-431">Entero de 2 bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-431">A 2-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="8457e-432">VT \_ bool (0x000B)</span><span class="sxs-lookup"><span data-stu-id="8457e-432">VT\_BOOL (0x000B)</span></span>     | <span data-ttu-id="8457e-433">Valor booleano; entero de 2 bytes que contiene 0x0000 (FALSE) o 0xFFFF (TRUE).</span><span class="sxs-lookup"><span data-stu-id="8457e-433">A boolean value; a 2-byte integer containing 0x0000 (FALSE) or 0xFFFF (TRUE).</span></span>                                                        |
| <span data-ttu-id="8457e-434">VT \_ I4 (0x0003)</span><span class="sxs-lookup"><span data-stu-id="8457e-434">VT\_I4 (0x0003)</span></span>       | <span data-ttu-id="8457e-435">Entero de 4 bytes con signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-435">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="8457e-436">VT \_ UI4 (0x0013)</span><span class="sxs-lookup"><span data-stu-id="8457e-436">VT\_UI4 (0x0013)</span></span>      | <span data-ttu-id="8457e-437">Entero de 4 bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-437">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="8457e-438">VT \_ R4 (0x0004)</span><span class="sxs-lookup"><span data-stu-id="8457e-438">VT\_R4 (0x0004)</span></span>       | <span data-ttu-id="8457e-439">Número de punto flotante de IEEE 32 bits, tal y como se define en \[ IEEE754 \] .</span><span class="sxs-lookup"><span data-stu-id="8457e-439">An IEEE 32-bit floating-point number, as defined in \[IEEE754\].</span></span>                                                                     |
| <span data-ttu-id="8457e-440">VT \_ int (0x0016)</span><span class="sxs-lookup"><span data-stu-id="8457e-440">VT\_INT (0x0016)</span></span>      | <span data-ttu-id="8457e-441">Entero de 4 bytes con signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-441">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="8457e-442">VT \_ uint (0x0017)</span><span class="sxs-lookup"><span data-stu-id="8457e-442">VT\_UINT (0x0017)</span></span>     | <span data-ttu-id="8457e-443">Entero de 4 bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-443">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="8457e-444">\_Error VT (0x000a)</span><span class="sxs-lookup"><span data-stu-id="8457e-444">VT\_ERROR (0x000A)</span></span>    | <span data-ttu-id="8457e-445">Entero sin signo de 4 bytes que contiene un valor HRESULT, tal como se especifica en \[ MS-sys \] .</span><span class="sxs-lookup"><span data-stu-id="8457e-445">A 4-byte unsigned integer containing an HRESULT, as specified in \[MS-SYS\].</span></span>                                                         |
| <span data-ttu-id="8457e-446">VT \_ i8 (0x0014)</span><span class="sxs-lookup"><span data-stu-id="8457e-446">VT\_I8 (0x0014)</span></span>       | <span data-ttu-id="8457e-447">Entero de 8 bytes con signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-447">An 8 byte signed integer.</span></span>                                                                                                            |
| <span data-ttu-id="8457e-448">VT \_ UI8 (0x0015)</span><span class="sxs-lookup"><span data-stu-id="8457e-448">VT\_UI8 (0x0015)</span></span>      | <span data-ttu-id="8457e-449">Entero de 8 bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-449">An 8-byte unsigned integer.</span></span>                                                                                                          |
| <span data-ttu-id="8457e-450">VT \_ R8 (0x0005)</span><span class="sxs-lookup"><span data-stu-id="8457e-450">VT\_R8 (0x0005)</span></span>       | <span data-ttu-id="8457e-451">Número de punto flotante de IEEE 64 bits tal y como se define en \[ IEEE754 \] .</span><span class="sxs-lookup"><span data-stu-id="8457e-451">An IEEE 64-bit floating-point number as defined in \[IEEE754\].</span></span>                                                                      |
| <span data-ttu-id="8457e-452">VT \_ CY (0x0006)</span><span class="sxs-lookup"><span data-stu-id="8457e-452">VT\_CY (0x0006)</span></span>       | <span data-ttu-id="8457e-453">Entero del complemento de dos bytes de 8 bytes (escalado por 10.000).</span><span class="sxs-lookup"><span data-stu-id="8457e-453">An 8-byte two's complement integer (scaled by 10,000).</span></span>                                                                               |
| <span data-ttu-id="8457e-454">Fecha de VT \_ (0x0007)</span><span class="sxs-lookup"><span data-stu-id="8457e-454">VT\_DATE (0x0007)</span></span>     | <span data-ttu-id="8457e-455">Número de punto flotante de 64 bits que representa el número de días transcurridos desde 00:00:00 el 31 de diciembre de 1899 (hora universal coordinada).</span><span class="sxs-lookup"><span data-stu-id="8457e-455">A 64-bit floating-point number representing the number of days since 00:00:00 on December 31, 1899 (Coordinated Universal Time).</span></span>     |
| <span data-ttu-id="8457e-456">VT \_ FILETIME (0x0040)</span><span class="sxs-lookup"><span data-stu-id="8457e-456">VT\_FILETIME (0x0040)</span></span> | <span data-ttu-id="8457e-457">Entero de 64 bits que representa el número de intervalos de 100-nanosegundos 00:00:00 desde el 1 de enero de 1601 (hora universal coordinada).</span><span class="sxs-lookup"><span data-stu-id="8457e-457">A 64-bit integer representing the number of 100-nanosecond intervals since 00:00:00 on January 1, 1601 (Coordinated Universal Time).</span></span> |
| <span data-ttu-id="8457e-458">VT \_ decimal (0x000E)</span><span class="sxs-lookup"><span data-stu-id="8457e-458">VT\_DECIMAL (0x000E)</span></span>  | <span data-ttu-id="8457e-459">Una estructura DECIMAL como se especifica en la sección 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="8457e-459">A DECIMAL structure as specified in section 2.2.1.1.1.1.</span></span>                                                                             |
| <span data-ttu-id="8457e-460">VT \_ CLSID (0x0048)</span><span class="sxs-lookup"><span data-stu-id="8457e-460">VT\_CLSID (0x0048)</span></span>    | <span data-ttu-id="8457e-461">Un valor binario de 16 bytes que contiene un GUID.</span><span class="sxs-lookup"><span data-stu-id="8457e-461">A 16-byte binary value containing a GUID.</span></span>                                                                                            |
| <span data-ttu-id="8457e-462">BLOB de VT \_ (0x0041)</span><span class="sxs-lookup"><span data-stu-id="8457e-462">VT\_BLOB (0x0041)</span></span>     | <span data-ttu-id="8457e-463">Un número entero sin signo de 4 bytes de bytes en el BLOB, seguido de muchos bytes de datos.</span><span class="sxs-lookup"><span data-stu-id="8457e-463">A 4-byte unsigned integer count of bytes in the blob, followed by that many bytes of data.</span></span>                                           |
| <span data-ttu-id="8457e-464">VT \_ BSTR (0x0008)</span><span class="sxs-lookup"><span data-stu-id="8457e-464">VT\_BSTR (0x0008)</span></span>     | <span data-ttu-id="8457e-465">Un número entero sin signo de 4 bytes de bytes en la cadena, seguido de una cadena, tal y como se especifica a continuación en vValue.</span><span class="sxs-lookup"><span data-stu-id="8457e-465">A 4-byte unsigned integer count of bytes in the string, followed by a string, as specified below under vValue.</span></span>                       |
| <span data-ttu-id="8457e-466">VT \_ LPSTR (0x001E)</span><span class="sxs-lookup"><span data-stu-id="8457e-466">VT\_LPSTR (0x001E)</span></span>    | <span data-ttu-id="8457e-467">Una cadena ANSI terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="8457e-467">A null-terminated ANSI string.</span></span>                                                                                                       |
| <span data-ttu-id="8457e-468">VT \_ LPWStr (0x001F)</span><span class="sxs-lookup"><span data-stu-id="8457e-468">VT\_LPWSTR (0x001F)</span></span>   | <span data-ttu-id="8457e-469">Una cadena Unicode de Unicode terminada en NULL \[ \] .</span><span class="sxs-lookup"><span data-stu-id="8457e-469">A null-terminated Unicode \[UNICODE\] string.</span></span>                                                                                        |
| <span data-ttu-id="8457e-470">VT \_ (variante de 0x000C)</span><span class="sxs-lookup"><span data-stu-id="8457e-470">VT\_VARIANT (0x000C)</span></span>  | <span data-ttu-id="8457e-471">CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="8457e-471">CBaseStorageVariant.</span></span> <span data-ttu-id="8457e-472">DEBE combinarse con un modificador de tipo de \_ matriz VT o un \_ Vector VT.</span><span class="sxs-lookup"><span data-stu-id="8457e-472">MUST be combined with a type modifier of VT\_ARRAY or VT\_VECTOR.</span></span>                                               |



 

<span data-ttu-id="8457e-473">En la tabla siguiente se especifican los modificadores de tipo para vType.</span><span class="sxs-lookup"><span data-stu-id="8457e-473">The following table specifies the type modifiers for vType.</span></span> <span data-ttu-id="8457e-474">Los modificadores de tipo pueden ser binarios ORed con vType, para cambiar el significado de vValue para indicar que es uno de los dos tipos de matriz posibles.</span><span class="sxs-lookup"><span data-stu-id="8457e-474">Type modifiers can be binary ORed with vType, to change the meaning of vValue to indicate it is one of two possible array types.</span></span>



| <span data-ttu-id="8457e-475">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-475">Value</span></span>               | <span data-ttu-id="8457e-476">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-476">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-477">VT \_ (vector) (0x1000)</span><span class="sxs-lookup"><span data-stu-id="8457e-477">VT\_VECTOR (0x1000)</span></span> | <span data-ttu-id="8457e-478">Si el indicador de tipo se combina con VT \_ Vector mediante un operador OR, vValue es una matriz contada de valores del tipo indicado.</span><span class="sxs-lookup"><span data-stu-id="8457e-478">If the type indicator is combined with VT\_VECTOR by using an OR operator, vValue is a counted array of values of the indicated type.</span></span> <span data-ttu-id="8457e-479">Vea la sección 2.2.1.1.1.2 para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8457e-479">See section 2.2.1.1.1.2 for details.</span></span> <br/> <span data-ttu-id="8457e-480">Este modificador de tipo no debe combinarse con los tipos siguientes: VT \_ int, VT \_ uint, VT \_ decimal, \_ BLOB de VT, objeto de BLOB de VT \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8457e-480">This type modifier MUST NOT be combined with the following types: VT\_INT, VT\_UINT, VT\_DECIMAL, VT\_BLOB, VT\_BLOB\_OBJECT.</span></span><br/>                                    |
| <span data-ttu-id="8457e-481">\_Matriz VT (0x2000)</span><span class="sxs-lookup"><span data-stu-id="8457e-481">VT\_ARRAY (0x2000)</span></span>  | <span data-ttu-id="8457e-482">Si el indicador de tipo se combina con \_ una matriz de VT mediante un operador OR, el valor es un SafeArray (como se especifica en la sección 2.2.1.1.1.3) que contiene valores del tipo indicado.</span><span class="sxs-lookup"><span data-stu-id="8457e-482">If the type indicator is combined with VT\_ARRAY by an OR operator, the value is a SAFEARRAY (as specified in section 2.2.1.1.1.3) containing values of the indicated type.</span></span> <br/> <span data-ttu-id="8457e-483">Este modificador de tipo no debe combinarse con los siguientes tipos: VT \_ i8, VT \_ UI8, VT \_ FILETIME, VT \_ CLSID, VT \_ BLOB, VT \_ BLOB \_ Object, VT \_ LPSTR, VT \_ LPWStr.</span><span class="sxs-lookup"><span data-stu-id="8457e-483">This type modifier MUST NOT be combined with the following types: VT\_I8, VT\_UI8, VT\_FILETIME, VT\_CLSID, VT\_BLOB, VT\_BLOB\_OBJECT, VT\_LPSTR, VT\_LPWSTR.</span></span> <br/> |



 

<span data-ttu-id="8457e-484">**vData1**: cuando VTYPE es VT \_ decimal, el valor de este campo se especifica como el campo Scale en la sección 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="8457e-484">**vData1**: When vType is VT\_DECIMAL, the value of this field is specified as the Scale field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="8457e-485">Para el resto de vTypes, el valor debe establecerse en 0x00.</span><span class="sxs-lookup"><span data-stu-id="8457e-485">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="8457e-486">**vData2**: cuando VTYPE es VT \_ decimal, el valor de este campo se especifica como el campo Sign en la sección 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="8457e-486">**vData2**: When vType is VT\_DECIMAL, the value of this field is specified as the Sign field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="8457e-487">Para el resto de vTypes, el valor debe establecerse en 0x00.</span><span class="sxs-lookup"><span data-stu-id="8457e-487">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="8457e-488">**vValue**: el valor de la operación de coincidencia.</span><span class="sxs-lookup"><span data-stu-id="8457e-488">**vValue**: The value for the match operation.</span></span> <span data-ttu-id="8457e-489">La sintaxis debe ser la indicada en el campo vType.</span><span class="sxs-lookup"><span data-stu-id="8457e-489">The syntax MUST be as indicated in the vType field.</span></span>

<span data-ttu-id="8457e-490">En la tabla siguiente se resumen los tamaños del campo vValue, según el campo vType para tipos de datos de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="8457e-490">The following table summarizes sizes for the vValue field, dependent upon the vType field for fixed-length data types.</span></span> <span data-ttu-id="8457e-491">El tamaño está en bytes.</span><span class="sxs-lookup"><span data-stu-id="8457e-491">The size is in bytes.</span></span>



| <span data-ttu-id="8457e-492">vType</span><span class="sxs-lookup"><span data-stu-id="8457e-492">vType</span></span>                                                   | <span data-ttu-id="8457e-493">Tamaño</span><span class="sxs-lookup"><span data-stu-id="8457e-493">Size</span></span> |
|---------------------------------------------------------|------|
| <span data-ttu-id="8457e-494">VT \_ I1, VT, \_ UI1</span><span class="sxs-lookup"><span data-stu-id="8457e-494">VT\_I1, VT,\_UI1</span></span>                                        | <span data-ttu-id="8457e-495">1</span><span class="sxs-lookup"><span data-stu-id="8457e-495">1</span></span>    |
| <span data-ttu-id="8457e-496">VT \_ I2, VT \_ UI2, VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="8457e-496">VT\_I2, VT\_UI2, VT\_BOOL</span></span>                               | <span data-ttu-id="8457e-497">2</span><span class="sxs-lookup"><span data-stu-id="8457e-497">2</span></span>    |
| <span data-ttu-id="8457e-498">VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ int, VT \_ uint, error de VT \_</span><span class="sxs-lookup"><span data-stu-id="8457e-498">VT\_I4, VT\_UI4, VT\_R4, VT\_INT, VT\_UINT, VT\_ERROR</span></span>   | <span data-ttu-id="8457e-499">4</span><span class="sxs-lookup"><span data-stu-id="8457e-499">4</span></span>    |
| <span data-ttu-id="8457e-500">VT \_ i8, VT \_ UI8, VT \_ R8, VT \_ CY, VT \_ Date, VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="8457e-500">VT\_I8, VT\_UI8, VT\_R8, VT\_CY, VT\_DATE, VT\_FILETIME</span></span> | <span data-ttu-id="8457e-501">8</span><span class="sxs-lookup"><span data-stu-id="8457e-501">8</span></span>    |
| <span data-ttu-id="8457e-502">VT \_ decimal, VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="8457e-502">VT\_DECIMAL, VT\_CLSID</span></span>                                  | <span data-ttu-id="8457e-503">16</span><span class="sxs-lookup"><span data-stu-id="8457e-503">16</span></span>   |



 

<span data-ttu-id="8457e-504">Si vType se establece en VT \_ BLOB, VT \_ BSTR o VT \_ LPSTR, se especifica la estructura de vValue en el diagrama siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-504">If vType is set to VT\_BLOB, VT\_BSTR or VT\_LPSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="8457e-505">0</span><span class="sxs-lookup"><span data-stu-id="8457e-505">0</span></span>

<span data-ttu-id="8457e-506">1</span><span class="sxs-lookup"><span data-stu-id="8457e-506">1</span></span>

<span data-ttu-id="8457e-507">2</span><span class="sxs-lookup"><span data-stu-id="8457e-507">2</span></span>

<span data-ttu-id="8457e-508">3</span><span class="sxs-lookup"><span data-stu-id="8457e-508">3</span></span>

<span data-ttu-id="8457e-509">4</span><span class="sxs-lookup"><span data-stu-id="8457e-509">4</span></span>

<span data-ttu-id="8457e-510">5</span><span class="sxs-lookup"><span data-stu-id="8457e-510">5</span></span>

<span data-ttu-id="8457e-511">6</span><span class="sxs-lookup"><span data-stu-id="8457e-511">6</span></span>

<span data-ttu-id="8457e-512">7</span><span class="sxs-lookup"><span data-stu-id="8457e-512">7</span></span>

<span data-ttu-id="8457e-513">8</span><span class="sxs-lookup"><span data-stu-id="8457e-513">8</span></span>

<span data-ttu-id="8457e-514">9</span><span class="sxs-lookup"><span data-stu-id="8457e-514">9</span></span>

<span data-ttu-id="8457e-515">1</span><span class="sxs-lookup"><span data-stu-id="8457e-515">1</span></span><br/> <span data-ttu-id="8457e-516">0</span><span class="sxs-lookup"><span data-stu-id="8457e-516">0</span></span><br/>

<span data-ttu-id="8457e-517">1</span><span class="sxs-lookup"><span data-stu-id="8457e-517">1</span></span>

<span data-ttu-id="8457e-518">2</span><span class="sxs-lookup"><span data-stu-id="8457e-518">2</span></span>

<span data-ttu-id="8457e-519">3</span><span class="sxs-lookup"><span data-stu-id="8457e-519">3</span></span>

<span data-ttu-id="8457e-520">4</span><span class="sxs-lookup"><span data-stu-id="8457e-520">4</span></span>

<span data-ttu-id="8457e-521">5</span><span class="sxs-lookup"><span data-stu-id="8457e-521">5</span></span>

<span data-ttu-id="8457e-522">6</span><span class="sxs-lookup"><span data-stu-id="8457e-522">6</span></span>

<span data-ttu-id="8457e-523">7</span><span class="sxs-lookup"><span data-stu-id="8457e-523">7</span></span>

<span data-ttu-id="8457e-524">8</span><span class="sxs-lookup"><span data-stu-id="8457e-524">8</span></span>

<span data-ttu-id="8457e-525">9</span><span class="sxs-lookup"><span data-stu-id="8457e-525">9</span></span>

<span data-ttu-id="8457e-526">2</span><span class="sxs-lookup"><span data-stu-id="8457e-526">2</span></span><br/> <span data-ttu-id="8457e-527">0</span><span class="sxs-lookup"><span data-stu-id="8457e-527">0</span></span><br/>

<span data-ttu-id="8457e-528">1</span><span class="sxs-lookup"><span data-stu-id="8457e-528">1</span></span>

<span data-ttu-id="8457e-529">2</span><span class="sxs-lookup"><span data-stu-id="8457e-529">2</span></span>

<span data-ttu-id="8457e-530">3</span><span class="sxs-lookup"><span data-stu-id="8457e-530">3</span></span>

<span data-ttu-id="8457e-531">4</span><span class="sxs-lookup"><span data-stu-id="8457e-531">4</span></span>

<span data-ttu-id="8457e-532">5</span><span class="sxs-lookup"><span data-stu-id="8457e-532">5</span></span>

<span data-ttu-id="8457e-533">6</span><span class="sxs-lookup"><span data-stu-id="8457e-533">6</span></span>

<span data-ttu-id="8457e-534">7</span><span class="sxs-lookup"><span data-stu-id="8457e-534">7</span></span>

<span data-ttu-id="8457e-535">8</span><span class="sxs-lookup"><span data-stu-id="8457e-535">8</span></span>

<span data-ttu-id="8457e-536">9</span><span class="sxs-lookup"><span data-stu-id="8457e-536">9</span></span>

<span data-ttu-id="8457e-537">3</span><span class="sxs-lookup"><span data-stu-id="8457e-537">3</span></span><br/> <span data-ttu-id="8457e-538">0</span><span class="sxs-lookup"><span data-stu-id="8457e-538">0</span></span><br/>

<span data-ttu-id="8457e-539">1</span><span class="sxs-lookup"><span data-stu-id="8457e-539">1</span></span>

<span data-ttu-id="8457e-540">cbSize</span><span class="sxs-lookup"><span data-stu-id="8457e-540">cbSize</span></span>

<span data-ttu-id="8457e-541">blobData (variable, opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-541">blobData (variable, optional)</span></span>



 

<span data-ttu-id="8457e-542">**cbSize**: entero de 32 bits sin signo, que indica el tamaño del campo blobData en bytes.</span><span class="sxs-lookup"><span data-stu-id="8457e-542">**cbSize**: Unsigned 32-bit integer, indicating the size of the blobData field in bytes.</span></span> <span data-ttu-id="8457e-543">Si vType se establece en VT \_ BSTR o VT \_ LPSTR, cbSize debe establecerse en 0x00000000 cuando la cadena representada sea una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="8457e-543">If vType is set to VT\_BSTR or VT\_LPSTR, cbSize MUST be set to 0x00000000 when the string represented is an empty string.</span></span>

<span data-ttu-id="8457e-544">**blobData**: debe tener una longitud de cbSize en bytes.</span><span class="sxs-lookup"><span data-stu-id="8457e-544">**blobData**: MUST be of length cbSize in bytes.</span></span>

<span data-ttu-id="8457e-545">En el caso de vType establecido en VT \_ BLOB, este campo es datos de blobs binarios opacos.</span><span class="sxs-lookup"><span data-stu-id="8457e-545">For vType set to VT\_BLOB, this field is opaque binary blob data.</span></span>

<span data-ttu-id="8457e-546">En el caso de vType establecido en VT \_ BSTR, este campo es un juego de caracteres en un juego de caracteres OEM seleccionado.</span><span class="sxs-lookup"><span data-stu-id="8457e-546">For vType set to VT\_BSTR, this field is a set of characters in an OEM selected character set.</span></span> <span data-ttu-id="8457e-547">El cliente y el servidor deben estar configurados para tener conjuntos de caracteres interoperables (fuera de banda del Protocolo).</span><span class="sxs-lookup"><span data-stu-id="8457e-547">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span> <span data-ttu-id="8457e-548">No es necesario terminar en NULL.</span><span class="sxs-lookup"><span data-stu-id="8457e-548">There is no requirement that it be null-terminated.</span></span>

<span data-ttu-id="8457e-549">Para vType establecido en VT \_ LPSTR, este campo es una cadena de caracteres terminada en null en un juego de caracteres OEM seleccionado.</span><span class="sxs-lookup"><span data-stu-id="8457e-549">For vType set to VT\_LPSTR this field is a null-terminated character string in an OEM selected character set.</span></span> <span data-ttu-id="8457e-550">El cliente y el servidor deben estar configurados para tener conjuntos de caracteres interoperables (fuera de banda del Protocolo).</span><span class="sxs-lookup"><span data-stu-id="8457e-550">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span>

<span data-ttu-id="8457e-551">Si vType se establece en VT \_ LPWStr, se especifica la estructura de vValue en el diagrama siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-551">If vType is set to VT\_LPWSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="8457e-552">0</span><span class="sxs-lookup"><span data-stu-id="8457e-552">0</span></span>

<span data-ttu-id="8457e-553">1</span><span class="sxs-lookup"><span data-stu-id="8457e-553">1</span></span>

<span data-ttu-id="8457e-554">2</span><span class="sxs-lookup"><span data-stu-id="8457e-554">2</span></span>

<span data-ttu-id="8457e-555">3</span><span class="sxs-lookup"><span data-stu-id="8457e-555">3</span></span>

<span data-ttu-id="8457e-556">4</span><span class="sxs-lookup"><span data-stu-id="8457e-556">4</span></span>

<span data-ttu-id="8457e-557">5</span><span class="sxs-lookup"><span data-stu-id="8457e-557">5</span></span>

<span data-ttu-id="8457e-558">6</span><span class="sxs-lookup"><span data-stu-id="8457e-558">6</span></span>

<span data-ttu-id="8457e-559">7</span><span class="sxs-lookup"><span data-stu-id="8457e-559">7</span></span>

<span data-ttu-id="8457e-560">8</span><span class="sxs-lookup"><span data-stu-id="8457e-560">8</span></span>

<span data-ttu-id="8457e-561">9</span><span class="sxs-lookup"><span data-stu-id="8457e-561">9</span></span>

<span data-ttu-id="8457e-562">1</span><span class="sxs-lookup"><span data-stu-id="8457e-562">1</span></span><br/> <span data-ttu-id="8457e-563">0</span><span class="sxs-lookup"><span data-stu-id="8457e-563">0</span></span><br/>

<span data-ttu-id="8457e-564">1</span><span class="sxs-lookup"><span data-stu-id="8457e-564">1</span></span>

<span data-ttu-id="8457e-565">2</span><span class="sxs-lookup"><span data-stu-id="8457e-565">2</span></span>

<span data-ttu-id="8457e-566">3</span><span class="sxs-lookup"><span data-stu-id="8457e-566">3</span></span>

<span data-ttu-id="8457e-567">4</span><span class="sxs-lookup"><span data-stu-id="8457e-567">4</span></span>

<span data-ttu-id="8457e-568">5</span><span class="sxs-lookup"><span data-stu-id="8457e-568">5</span></span>

<span data-ttu-id="8457e-569">6</span><span class="sxs-lookup"><span data-stu-id="8457e-569">6</span></span>

<span data-ttu-id="8457e-570">7</span><span class="sxs-lookup"><span data-stu-id="8457e-570">7</span></span>

<span data-ttu-id="8457e-571">8</span><span class="sxs-lookup"><span data-stu-id="8457e-571">8</span></span>

<span data-ttu-id="8457e-572">9</span><span class="sxs-lookup"><span data-stu-id="8457e-572">9</span></span>

<span data-ttu-id="8457e-573">2</span><span class="sxs-lookup"><span data-stu-id="8457e-573">2</span></span><br/> <span data-ttu-id="8457e-574">0</span><span class="sxs-lookup"><span data-stu-id="8457e-574">0</span></span><br/>

<span data-ttu-id="8457e-575">1</span><span class="sxs-lookup"><span data-stu-id="8457e-575">1</span></span>

<span data-ttu-id="8457e-576">2</span><span class="sxs-lookup"><span data-stu-id="8457e-576">2</span></span>

<span data-ttu-id="8457e-577">3</span><span class="sxs-lookup"><span data-stu-id="8457e-577">3</span></span>

<span data-ttu-id="8457e-578">4</span><span class="sxs-lookup"><span data-stu-id="8457e-578">4</span></span>

<span data-ttu-id="8457e-579">5</span><span class="sxs-lookup"><span data-stu-id="8457e-579">5</span></span>

<span data-ttu-id="8457e-580">6</span><span class="sxs-lookup"><span data-stu-id="8457e-580">6</span></span>

<span data-ttu-id="8457e-581">7</span><span class="sxs-lookup"><span data-stu-id="8457e-581">7</span></span>

<span data-ttu-id="8457e-582">8</span><span class="sxs-lookup"><span data-stu-id="8457e-582">8</span></span>

<span data-ttu-id="8457e-583">9</span><span class="sxs-lookup"><span data-stu-id="8457e-583">9</span></span>

<span data-ttu-id="8457e-584">3</span><span class="sxs-lookup"><span data-stu-id="8457e-584">3</span></span><br/> <span data-ttu-id="8457e-585">0</span><span class="sxs-lookup"><span data-stu-id="8457e-585">0</span></span><br/>

<span data-ttu-id="8457e-586">1</span><span class="sxs-lookup"><span data-stu-id="8457e-586">1</span></span>

<span data-ttu-id="8457e-587">ccLen</span><span class="sxs-lookup"><span data-stu-id="8457e-587">ccLen</span></span>

<span data-ttu-id="8457e-588">String (variable, opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-588">string (variable, optional)</span></span>



 

<span data-ttu-id="8457e-589">**ccLen**: entero de 32 bits sin signo, que indica el tamaño del campo de cadena en caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="8457e-589">**ccLen**: Unsigned 32-bit integer, indicating the size of the string field in Unicode characters.</span></span> <span data-ttu-id="8457e-590">DEBE establecerse en 0x00000000 para una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="8457e-590">MUST be set to 0x00000000 for an empty string.</span></span>

<span data-ttu-id="8457e-591">**cadena**: cadena Unicode terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="8457e-591">**string**: Null-terminated Unicode string.</span></span>

### <a name="22111-cbasestoragevariant-structures"></a><span data-ttu-id="8457e-592">2.2.1.1.1 estructuras CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="8457e-592">2.2.1.1.1 CBaseStorageVariant Structures</span></span>

<span data-ttu-id="8457e-593">Se usan las siguientes estructuras en la estructura CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="8457e-593">The following structures are used in the CBaseStorageVariant structure.</span></span>

### <a name="221111-decimal"></a><span data-ttu-id="8457e-594">2.2.1.1.1.1 DECIMAL</span><span class="sxs-lookup"><span data-stu-id="8457e-594">2.2.1.1.1.1 DECIMAL</span></span>

<span data-ttu-id="8457e-595">DECIMAL se usa para representar un valor numérico exacto con una precisión fija y una escala fija.</span><span class="sxs-lookup"><span data-stu-id="8457e-595">DECIMAL is used to represent an exact numeric value with a fixed precision and fixed scale.</span></span>

<span data-ttu-id="8457e-596">Cuando vType se establece en VT \_ decimal (0x0000E), los campos vData1 y vData2 de CBaseStorageVariant se deben interpretar de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-596">When vType is set to VT\_DECIMAL (0x0000E), the vData1 and vData2 fields of CBaseStorageVariant MUST be interpreted as follows:</span></span>

<span data-ttu-id="8457e-597">**vData1**: número de dígitos a la derecha del separador decimal.</span><span class="sxs-lookup"><span data-stu-id="8457e-597">**vData1**: The number of digits to the right of the decimal point.</span></span> <span data-ttu-id="8457e-598">DEBE estar en el intervalo comprendido entre 0 y 28.</span><span class="sxs-lookup"><span data-stu-id="8457e-598">MUST be in the range 0 to 28.</span></span>

<span data-ttu-id="8457e-599">**vData2**: el signo del valor numérico.</span><span class="sxs-lookup"><span data-stu-id="8457e-599">**vData2**: The sign of the numeric value.</span></span> <span data-ttu-id="8457e-600">Establézcalo en 0x00 si es positivo, 0x80 si es negativo.</span><span class="sxs-lookup"><span data-stu-id="8457e-600">Set to 0x00 if positive, 0x80 if negative.</span></span>

<span data-ttu-id="8457e-601">El formato del campo vValue es:</span><span class="sxs-lookup"><span data-stu-id="8457e-601">The format of the vValue field is:</span></span>



<span data-ttu-id="8457e-602">0</span><span class="sxs-lookup"><span data-stu-id="8457e-602">0</span></span>

<span data-ttu-id="8457e-603">1</span><span class="sxs-lookup"><span data-stu-id="8457e-603">1</span></span>

<span data-ttu-id="8457e-604">2</span><span class="sxs-lookup"><span data-stu-id="8457e-604">2</span></span>

<span data-ttu-id="8457e-605">3</span><span class="sxs-lookup"><span data-stu-id="8457e-605">3</span></span>

<span data-ttu-id="8457e-606">4</span><span class="sxs-lookup"><span data-stu-id="8457e-606">4</span></span>

<span data-ttu-id="8457e-607">5</span><span class="sxs-lookup"><span data-stu-id="8457e-607">5</span></span>

<span data-ttu-id="8457e-608">6</span><span class="sxs-lookup"><span data-stu-id="8457e-608">6</span></span>

<span data-ttu-id="8457e-609">7</span><span class="sxs-lookup"><span data-stu-id="8457e-609">7</span></span>

<span data-ttu-id="8457e-610">8</span><span class="sxs-lookup"><span data-stu-id="8457e-610">8</span></span>

<span data-ttu-id="8457e-611">9</span><span class="sxs-lookup"><span data-stu-id="8457e-611">9</span></span>

<span data-ttu-id="8457e-612">1</span><span class="sxs-lookup"><span data-stu-id="8457e-612">1</span></span><br/> <span data-ttu-id="8457e-613">0</span><span class="sxs-lookup"><span data-stu-id="8457e-613">0</span></span><br/>

<span data-ttu-id="8457e-614">1</span><span class="sxs-lookup"><span data-stu-id="8457e-614">1</span></span>

<span data-ttu-id="8457e-615">2</span><span class="sxs-lookup"><span data-stu-id="8457e-615">2</span></span>

<span data-ttu-id="8457e-616">3</span><span class="sxs-lookup"><span data-stu-id="8457e-616">3</span></span>

<span data-ttu-id="8457e-617">4</span><span class="sxs-lookup"><span data-stu-id="8457e-617">4</span></span>

<span data-ttu-id="8457e-618">5</span><span class="sxs-lookup"><span data-stu-id="8457e-618">5</span></span>

<span data-ttu-id="8457e-619">6</span><span class="sxs-lookup"><span data-stu-id="8457e-619">6</span></span>

<span data-ttu-id="8457e-620">7</span><span class="sxs-lookup"><span data-stu-id="8457e-620">7</span></span>

<span data-ttu-id="8457e-621">8</span><span class="sxs-lookup"><span data-stu-id="8457e-621">8</span></span>

<span data-ttu-id="8457e-622">9</span><span class="sxs-lookup"><span data-stu-id="8457e-622">9</span></span>

<span data-ttu-id="8457e-623">2</span><span class="sxs-lookup"><span data-stu-id="8457e-623">2</span></span><br/> <span data-ttu-id="8457e-624">0</span><span class="sxs-lookup"><span data-stu-id="8457e-624">0</span></span><br/>

<span data-ttu-id="8457e-625">1</span><span class="sxs-lookup"><span data-stu-id="8457e-625">1</span></span>

<span data-ttu-id="8457e-626">2</span><span class="sxs-lookup"><span data-stu-id="8457e-626">2</span></span>

<span data-ttu-id="8457e-627">3</span><span class="sxs-lookup"><span data-stu-id="8457e-627">3</span></span>

<span data-ttu-id="8457e-628">4</span><span class="sxs-lookup"><span data-stu-id="8457e-628">4</span></span>

<span data-ttu-id="8457e-629">5</span><span class="sxs-lookup"><span data-stu-id="8457e-629">5</span></span>

<span data-ttu-id="8457e-630">6</span><span class="sxs-lookup"><span data-stu-id="8457e-630">6</span></span>

<span data-ttu-id="8457e-631">7</span><span class="sxs-lookup"><span data-stu-id="8457e-631">7</span></span>

<span data-ttu-id="8457e-632">8</span><span class="sxs-lookup"><span data-stu-id="8457e-632">8</span></span>

<span data-ttu-id="8457e-633">9</span><span class="sxs-lookup"><span data-stu-id="8457e-633">9</span></span>

<span data-ttu-id="8457e-634">3</span><span class="sxs-lookup"><span data-stu-id="8457e-634">3</span></span><br/> <span data-ttu-id="8457e-635">0</span><span class="sxs-lookup"><span data-stu-id="8457e-635">0</span></span><br/>

<span data-ttu-id="8457e-636">1</span><span class="sxs-lookup"><span data-stu-id="8457e-636">1</span></span>

<span data-ttu-id="8457e-637">Hi32</span><span class="sxs-lookup"><span data-stu-id="8457e-637">Hi32</span></span>

<span data-ttu-id="8457e-638">Lo32</span><span class="sxs-lookup"><span data-stu-id="8457e-638">Lo32</span></span>

<span data-ttu-id="8457e-639">Mid32</span><span class="sxs-lookup"><span data-stu-id="8457e-639">Mid32</span></span>



 

<span data-ttu-id="8457e-640">**Hi32**: los 32 bits más altos del entero de 96 bits.</span><span class="sxs-lookup"><span data-stu-id="8457e-640">**Hi32**: The highest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="8457e-641">**Lo32**: los 32 bits más bajos del entero de 96 bits.</span><span class="sxs-lookup"><span data-stu-id="8457e-641">**Lo32**: The lowest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="8457e-642">**Mid32**: el medio 32 bits del entero de 96 bits.</span><span class="sxs-lookup"><span data-stu-id="8457e-642">**Mid32**: The middle 32 bits of the 96 bit integer.</span></span>

### <a name="221112-vt_vector"></a><span data-ttu-id="8457e-643">Vector 2.2.1.1.1.2 VT \_</span><span class="sxs-lookup"><span data-stu-id="8457e-643">2.2.1.1.1.2 VT\_VECTOR</span></span>

<span data-ttu-id="8457e-644">El \_ Vector VT se usa para pasar Matrices unidimensionales.</span><span class="sxs-lookup"><span data-stu-id="8457e-644">VT\_Vector is used to pass one-dimensional arrays.</span></span>



<span data-ttu-id="8457e-645">0</span><span class="sxs-lookup"><span data-stu-id="8457e-645">0</span></span>

<span data-ttu-id="8457e-646">1</span><span class="sxs-lookup"><span data-stu-id="8457e-646">1</span></span>

<span data-ttu-id="8457e-647">2</span><span class="sxs-lookup"><span data-stu-id="8457e-647">2</span></span>

<span data-ttu-id="8457e-648">3</span><span class="sxs-lookup"><span data-stu-id="8457e-648">3</span></span>

<span data-ttu-id="8457e-649">4</span><span class="sxs-lookup"><span data-stu-id="8457e-649">4</span></span>

<span data-ttu-id="8457e-650">5</span><span class="sxs-lookup"><span data-stu-id="8457e-650">5</span></span>

<span data-ttu-id="8457e-651">6</span><span class="sxs-lookup"><span data-stu-id="8457e-651">6</span></span>

<span data-ttu-id="8457e-652">7</span><span class="sxs-lookup"><span data-stu-id="8457e-652">7</span></span>

<span data-ttu-id="8457e-653">8</span><span class="sxs-lookup"><span data-stu-id="8457e-653">8</span></span>

<span data-ttu-id="8457e-654">9</span><span class="sxs-lookup"><span data-stu-id="8457e-654">9</span></span>

<span data-ttu-id="8457e-655">1</span><span class="sxs-lookup"><span data-stu-id="8457e-655">1</span></span><br/> <span data-ttu-id="8457e-656">0</span><span class="sxs-lookup"><span data-stu-id="8457e-656">0</span></span><br/>

<span data-ttu-id="8457e-657">1</span><span class="sxs-lookup"><span data-stu-id="8457e-657">1</span></span>

<span data-ttu-id="8457e-658">2</span><span class="sxs-lookup"><span data-stu-id="8457e-658">2</span></span>

<span data-ttu-id="8457e-659">3</span><span class="sxs-lookup"><span data-stu-id="8457e-659">3</span></span>

<span data-ttu-id="8457e-660">4</span><span class="sxs-lookup"><span data-stu-id="8457e-660">4</span></span>

<span data-ttu-id="8457e-661">5</span><span class="sxs-lookup"><span data-stu-id="8457e-661">5</span></span>

<span data-ttu-id="8457e-662">6</span><span class="sxs-lookup"><span data-stu-id="8457e-662">6</span></span>

<span data-ttu-id="8457e-663">7</span><span class="sxs-lookup"><span data-stu-id="8457e-663">7</span></span>

<span data-ttu-id="8457e-664">8</span><span class="sxs-lookup"><span data-stu-id="8457e-664">8</span></span>

<span data-ttu-id="8457e-665">9</span><span class="sxs-lookup"><span data-stu-id="8457e-665">9</span></span>

<span data-ttu-id="8457e-666">2</span><span class="sxs-lookup"><span data-stu-id="8457e-666">2</span></span><br/> <span data-ttu-id="8457e-667">0</span><span class="sxs-lookup"><span data-stu-id="8457e-667">0</span></span><br/>

<span data-ttu-id="8457e-668">1</span><span class="sxs-lookup"><span data-stu-id="8457e-668">1</span></span>

<span data-ttu-id="8457e-669">2</span><span class="sxs-lookup"><span data-stu-id="8457e-669">2</span></span>

<span data-ttu-id="8457e-670">3</span><span class="sxs-lookup"><span data-stu-id="8457e-670">3</span></span>

<span data-ttu-id="8457e-671">4</span><span class="sxs-lookup"><span data-stu-id="8457e-671">4</span></span>

<span data-ttu-id="8457e-672">5</span><span class="sxs-lookup"><span data-stu-id="8457e-672">5</span></span>

<span data-ttu-id="8457e-673">6</span><span class="sxs-lookup"><span data-stu-id="8457e-673">6</span></span>

<span data-ttu-id="8457e-674">7</span><span class="sxs-lookup"><span data-stu-id="8457e-674">7</span></span>

<span data-ttu-id="8457e-675">8</span><span class="sxs-lookup"><span data-stu-id="8457e-675">8</span></span>

<span data-ttu-id="8457e-676">9</span><span class="sxs-lookup"><span data-stu-id="8457e-676">9</span></span>

<span data-ttu-id="8457e-677">3</span><span class="sxs-lookup"><span data-stu-id="8457e-677">3</span></span><br/> <span data-ttu-id="8457e-678">0</span><span class="sxs-lookup"><span data-stu-id="8457e-678">0</span></span><br/>

<span data-ttu-id="8457e-679">1</span><span class="sxs-lookup"><span data-stu-id="8457e-679">1</span></span>

<span data-ttu-id="8457e-680">vVectorElements</span><span class="sxs-lookup"><span data-stu-id="8457e-680">vVectorElements</span></span>

<span data-ttu-id="8457e-681">vVectorData</span><span class="sxs-lookup"><span data-stu-id="8457e-681">vVectorData</span></span>



 

<span data-ttu-id="8457e-682">**vVectorElements**: entero de 32 bits sin signo, que indica el número de elementos del campo vVectorData.</span><span class="sxs-lookup"><span data-stu-id="8457e-682">**vVectorElements**: Unsigned 32-bit integer, indicating the number of elements in the vVectorData field.</span></span>

<span data-ttu-id="8457e-683">**vVectorData**: una matriz de elementos que tienen un tipo indicado por vType con el bit de 0x1000 desactivado.</span><span class="sxs-lookup"><span data-stu-id="8457e-683">**vVectorData**: An array of items which have a type indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="8457e-684">El tamaño de un elemento de longitud fija individual se puede obtener a partir de la tabla de tipos de datos de longitud fija, como se especifica en la sección 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="8457e-684">The size of an individual fixed-length item can be obtained from the fixed-length data type table, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="8457e-685">La longitud de este campo, en bytes, se puede calcular multiplicando vVectorElements por el tamaño de cada elemento individual.</span><span class="sxs-lookup"><span data-stu-id="8457e-685">The length of this field, in bytes, can be calculated by multiplying vVectorElements by the size of individual item.</span></span>

<span data-ttu-id="8457e-686">En el caso de los tipos de datos de longitud variable vVectorData contiene una secuencia de tipos simples de serialización consecutiva donde el tipo se indica mediante vType con el bit de 0x1000 desactivado.</span><span class="sxs-lookup"><span data-stu-id="8457e-686">For variable-length data types vVectorData contains a sequence of consecutively marshaled simple types where the type is indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="8457e-687">Esto incluye un caso especial indicado por vType VT \_ array \| VT \_ Variant (es decir, 0x100C).</span><span class="sxs-lookup"><span data-stu-id="8457e-687">This includes a special case indicated by vType VT\_ARRAY \| VT\_VARIANT (i.e., 0x100C).</span></span>

<span data-ttu-id="8457e-688">Los elementos del campo vVectorData se deben separar entre 0 y 3 bytes de relleno, de modo que cada elemento comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta matriz.</span><span class="sxs-lookup"><span data-stu-id="8457e-688">The elements in the vVectorData field MUST be separated by 0 to 3 padding bytes such that each element begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="8457e-689">Si los bytes de relleno están presentes, el valor que contienen es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8457e-689">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="8457e-690">El receptor debe omitir el contenido de los bytes de relleno.</span><span class="sxs-lookup"><span data-stu-id="8457e-690">The content of the padding bytes MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8457e-691">En el caso de una vType establecida en VT \_ array \| VT \_ Variant, el tipo de los elementos de esta secuencia es CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="8457e-691">For a vType set to VT\_ARRAY \| VT\_VARIANT, the type for items in this sequence is CBaseStorageVariant.</span></span>

### <a name="221113-safearray"></a><span data-ttu-id="8457e-692">SAFEARRAY 2.2.1.1.1.3</span><span class="sxs-lookup"><span data-stu-id="8457e-692">2.2.1.1.1.3 SAFEARRAY</span></span>

<span data-ttu-id="8457e-693">SAFEARRAY se utiliza para pasar matrices multidimensionales.</span><span class="sxs-lookup"><span data-stu-id="8457e-693">SAFEARRAY is used to pass multidimensional arrays.</span></span> <span data-ttu-id="8457e-694">La estructura contiene información sobre el tamaño de la matriz, así como los datos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="8457e-694">The structure contains array size information as well as the data in the array.</span></span>



<span data-ttu-id="8457e-695">0</span><span class="sxs-lookup"><span data-stu-id="8457e-695">0</span></span>

<span data-ttu-id="8457e-696">1</span><span class="sxs-lookup"><span data-stu-id="8457e-696">1</span></span>

<span data-ttu-id="8457e-697">2</span><span class="sxs-lookup"><span data-stu-id="8457e-697">2</span></span>

<span data-ttu-id="8457e-698">3</span><span class="sxs-lookup"><span data-stu-id="8457e-698">3</span></span>

<span data-ttu-id="8457e-699">4</span><span class="sxs-lookup"><span data-stu-id="8457e-699">4</span></span>

<span data-ttu-id="8457e-700">5</span><span class="sxs-lookup"><span data-stu-id="8457e-700">5</span></span>

<span data-ttu-id="8457e-701">6</span><span class="sxs-lookup"><span data-stu-id="8457e-701">6</span></span>

<span data-ttu-id="8457e-702">7</span><span class="sxs-lookup"><span data-stu-id="8457e-702">7</span></span>

<span data-ttu-id="8457e-703">8</span><span class="sxs-lookup"><span data-stu-id="8457e-703">8</span></span>

<span data-ttu-id="8457e-704">9</span><span class="sxs-lookup"><span data-stu-id="8457e-704">9</span></span>

<span data-ttu-id="8457e-705">1</span><span class="sxs-lookup"><span data-stu-id="8457e-705">1</span></span><br/> <span data-ttu-id="8457e-706">0</span><span class="sxs-lookup"><span data-stu-id="8457e-706">0</span></span><br/>

<span data-ttu-id="8457e-707">1</span><span class="sxs-lookup"><span data-stu-id="8457e-707">1</span></span>

<span data-ttu-id="8457e-708">2</span><span class="sxs-lookup"><span data-stu-id="8457e-708">2</span></span>

<span data-ttu-id="8457e-709">3</span><span class="sxs-lookup"><span data-stu-id="8457e-709">3</span></span>

<span data-ttu-id="8457e-710">4</span><span class="sxs-lookup"><span data-stu-id="8457e-710">4</span></span>

<span data-ttu-id="8457e-711">5</span><span class="sxs-lookup"><span data-stu-id="8457e-711">5</span></span>

<span data-ttu-id="8457e-712">6</span><span class="sxs-lookup"><span data-stu-id="8457e-712">6</span></span>

<span data-ttu-id="8457e-713">7</span><span class="sxs-lookup"><span data-stu-id="8457e-713">7</span></span>

<span data-ttu-id="8457e-714">8</span><span class="sxs-lookup"><span data-stu-id="8457e-714">8</span></span>

<span data-ttu-id="8457e-715">9</span><span class="sxs-lookup"><span data-stu-id="8457e-715">9</span></span>

<span data-ttu-id="8457e-716">2</span><span class="sxs-lookup"><span data-stu-id="8457e-716">2</span></span><br/> <span data-ttu-id="8457e-717">0</span><span class="sxs-lookup"><span data-stu-id="8457e-717">0</span></span><br/>

<span data-ttu-id="8457e-718">1</span><span class="sxs-lookup"><span data-stu-id="8457e-718">1</span></span>

<span data-ttu-id="8457e-719">2</span><span class="sxs-lookup"><span data-stu-id="8457e-719">2</span></span>

<span data-ttu-id="8457e-720">3</span><span class="sxs-lookup"><span data-stu-id="8457e-720">3</span></span>

<span data-ttu-id="8457e-721">4</span><span class="sxs-lookup"><span data-stu-id="8457e-721">4</span></span>

<span data-ttu-id="8457e-722">5</span><span class="sxs-lookup"><span data-stu-id="8457e-722">5</span></span>

<span data-ttu-id="8457e-723">6</span><span class="sxs-lookup"><span data-stu-id="8457e-723">6</span></span>

<span data-ttu-id="8457e-724">7</span><span class="sxs-lookup"><span data-stu-id="8457e-724">7</span></span>

<span data-ttu-id="8457e-725">8</span><span class="sxs-lookup"><span data-stu-id="8457e-725">8</span></span>

<span data-ttu-id="8457e-726">9</span><span class="sxs-lookup"><span data-stu-id="8457e-726">9</span></span>

<span data-ttu-id="8457e-727">3</span><span class="sxs-lookup"><span data-stu-id="8457e-727">3</span></span><br/> <span data-ttu-id="8457e-728">0</span><span class="sxs-lookup"><span data-stu-id="8457e-728">0</span></span><br/>

<span data-ttu-id="8457e-729">1</span><span class="sxs-lookup"><span data-stu-id="8457e-729">1</span></span>

<span data-ttu-id="8457e-730">cDims</span><span class="sxs-lookup"><span data-stu-id="8457e-730">cDims</span></span>

<span data-ttu-id="8457e-731">fFeatures</span><span class="sxs-lookup"><span data-stu-id="8457e-731">fFeatures</span></span>

<span data-ttu-id="8457e-732">cbElements</span><span class="sxs-lookup"><span data-stu-id="8457e-732">cbElements</span></span>

<span data-ttu-id="8457e-733">Rgsabound (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-733">Rgsabound (variable)</span></span>

<span data-ttu-id="8457e-734">vData (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-734">vData (variable)</span></span>



 

<span data-ttu-id="8457e-735">**cDims**: entero de 16 bits sin signo, que indica el número de dimensiones de la matriz multidimensional.</span><span class="sxs-lookup"><span data-stu-id="8457e-735">**cDims**: Unsigned 16-bit integer, indicating the number of dimensions of the multidimensional array.</span></span>

<span data-ttu-id="8457e-736">**fFeatures**: un campo de bits de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8457e-736">**fFeatures**: A 16-bit bitfield.</span></span> <span data-ttu-id="8457e-737">Los valores representan características, definidas por aplicaciones de nivel superior y deben omitirse.</span><span class="sxs-lookup"><span data-stu-id="8457e-737">The values represent features, defined by upper layer applications and MUST be ignored.</span></span>

<span data-ttu-id="8457e-738">**cbElements**: entero de 32 bits sin signo que especifica el tamaño de cada elemento de la matriz.</span><span class="sxs-lookup"><span data-stu-id="8457e-738">**cbElements**: A 32-bit unsigned integer specifying the size of each element of the array.</span></span>

<span data-ttu-id="8457e-739">**Rgsabound**: una matriz que contiene una estructura SAFEARRAYBOUND, como se especifica en la sección 2.2.1.1.1.4, por dimensión en SafeArray.</span><span class="sxs-lookup"><span data-stu-id="8457e-739">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4, per dimension in the SAFEARRAY.</span></span> <span data-ttu-id="8457e-740">En primer lugar, esta matriz tiene la dimensión situada más a la izquierda y la dimensión situada más a la derecha.</span><span class="sxs-lookup"><span data-stu-id="8457e-740">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="8457e-741">**vData**: un vector de elementos de serialización de un tipo determinado, indicado por el VType de CBaseStorageVariant que contiene, con el bit 0x2000 desactivado.</span><span class="sxs-lookup"><span data-stu-id="8457e-741">**vData**: A vector of marshaled items of a particular type, indicated by the vType of the containing CBaseStorageVariant, with the bit 0x2000 cleared.</span></span>

<span data-ttu-id="8457e-742">vData se calcula de forma similar a VT \_ Vector, como se especifica en la sección 2.2.1.1.1.2, con la diferencia de que el número de elementos no se almacena delante del vector.</span><span class="sxs-lookup"><span data-stu-id="8457e-742">vData is marshaled similarly to VT\_VECTOR, as specified in Section 2.2.1.1.1.2, with the difference that the number of items is not stored in front of the vector.</span></span> <span data-ttu-id="8457e-743">En su lugar, el número de elementos se calcula multiplicando el valor de cElements por todos los límites de matriz seguros que se proporcionan en el campo Rgsabound.</span><span class="sxs-lookup"><span data-stu-id="8457e-743">Rather the number of items is calculated by multiplying the cElements value with all safe array bounds given in the Rgsabound field.</span></span> <span data-ttu-id="8457e-744">Los elementos se almacenan en un vector en orden de dimensiones, iterando a partir de la dimensión situada más a la derecha.</span><span class="sxs-lookup"><span data-stu-id="8457e-744">Elements are stored in a vector in order of dimensions, iterating beginning with the right-most dimension.</span></span>

<span data-ttu-id="8457e-745">El siguiente diagrama representa visualmente una matriz bidimensional de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8457e-745">The following diagram visually represents a sample two-dimensional array.</span></span> <span data-ttu-id="8457e-746">La primera dimensión tiene cElements igual a 4 (representada horizontalmente) y lLbound igual a 0, y la segunda dimensión tiene cElements igual a 2 (representada verticalmente) y lLbound igual a 0.</span><span class="sxs-lookup"><span data-stu-id="8457e-746">The first dimension has cElements equal to 4 (represented horizontally) and lLbound equal to 0, and the second dimension has cElements equal to 2 (represented vertically) and lLbound equal to 0.</span></span>



|            |            |            |            |
|------------|------------|------------|------------|
| <span data-ttu-id="8457e-747">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-747">0x00000001</span></span> | <span data-ttu-id="8457e-748">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8457e-748">0x00000002</span></span> | <span data-ttu-id="8457e-749">0x00000003</span><span class="sxs-lookup"><span data-stu-id="8457e-749">0x00000003</span></span> | <span data-ttu-id="8457e-750">0x00000005</span><span class="sxs-lookup"><span data-stu-id="8457e-750">0x00000005</span></span> |
| <span data-ttu-id="8457e-751">0x00000007</span><span class="sxs-lookup"><span data-stu-id="8457e-751">0x00000007</span></span> | <span data-ttu-id="8457e-752">0x00000011</span><span class="sxs-lookup"><span data-stu-id="8457e-752">0x00000011</span></span> | <span data-ttu-id="8457e-753">0x00000013</span><span class="sxs-lookup"><span data-stu-id="8457e-753">0x00000013</span></span> | <span data-ttu-id="8457e-754">0x00000017</span><span class="sxs-lookup"><span data-stu-id="8457e-754">0x00000017</span></span> |



 

<span data-ttu-id="8457e-755">Con el diagrama anterior, vData contendrá la siguiente secuencia: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (recorrer en iteración la dimensión situada más a la derecha y, a continuación, incrementar la dimensión siguiente).</span><span class="sxs-lookup"><span data-stu-id="8457e-755">Using the diagram above, vData will contain the following sequence: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterating through the rightmost dimension first, then incrementing the next dimension).</span></span> <span data-ttu-id="8457e-756">El Rgsabound anterior (que registra cElements y LBound) sería: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-756">The preceding Rgsabound (which records cElements and Lbound) would be: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span></span>

### <a name="221114-safearraybound"></a><span data-ttu-id="8457e-757">2.2.1.1.1.4 SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="8457e-757">2.2.1.1.1.4 SAFEARRAYBOUND</span></span>

<span data-ttu-id="8457e-758">La estructura SAFEARRAYBOUND representa los límites de una dimensión de un SAFEARRAY o de un SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="8457e-758">The SAFEARRAYBOUND structure represents the bounds of one dimension of a SAFEARRAY or SAFEARRAY2.</span></span> <span data-ttu-id="8457e-759">Su formato es:</span><span class="sxs-lookup"><span data-stu-id="8457e-759">Its format is:</span></span>



<span data-ttu-id="8457e-760">0</span><span class="sxs-lookup"><span data-stu-id="8457e-760">0</span></span>

<span data-ttu-id="8457e-761">1</span><span class="sxs-lookup"><span data-stu-id="8457e-761">1</span></span>

<span data-ttu-id="8457e-762">2</span><span class="sxs-lookup"><span data-stu-id="8457e-762">2</span></span>

<span data-ttu-id="8457e-763">3</span><span class="sxs-lookup"><span data-stu-id="8457e-763">3</span></span>

<span data-ttu-id="8457e-764">4</span><span class="sxs-lookup"><span data-stu-id="8457e-764">4</span></span>

<span data-ttu-id="8457e-765">5</span><span class="sxs-lookup"><span data-stu-id="8457e-765">5</span></span>

<span data-ttu-id="8457e-766">6</span><span class="sxs-lookup"><span data-stu-id="8457e-766">6</span></span>

<span data-ttu-id="8457e-767">7</span><span class="sxs-lookup"><span data-stu-id="8457e-767">7</span></span>

<span data-ttu-id="8457e-768">8</span><span class="sxs-lookup"><span data-stu-id="8457e-768">8</span></span>

<span data-ttu-id="8457e-769">9</span><span class="sxs-lookup"><span data-stu-id="8457e-769">9</span></span>

<span data-ttu-id="8457e-770">1</span><span class="sxs-lookup"><span data-stu-id="8457e-770">1</span></span><br/> <span data-ttu-id="8457e-771">0</span><span class="sxs-lookup"><span data-stu-id="8457e-771">0</span></span><br/>

<span data-ttu-id="8457e-772">1</span><span class="sxs-lookup"><span data-stu-id="8457e-772">1</span></span>

<span data-ttu-id="8457e-773">2</span><span class="sxs-lookup"><span data-stu-id="8457e-773">2</span></span>

<span data-ttu-id="8457e-774">3</span><span class="sxs-lookup"><span data-stu-id="8457e-774">3</span></span>

<span data-ttu-id="8457e-775">4</span><span class="sxs-lookup"><span data-stu-id="8457e-775">4</span></span>

<span data-ttu-id="8457e-776">5</span><span class="sxs-lookup"><span data-stu-id="8457e-776">5</span></span>

<span data-ttu-id="8457e-777">6</span><span class="sxs-lookup"><span data-stu-id="8457e-777">6</span></span>

<span data-ttu-id="8457e-778">7</span><span class="sxs-lookup"><span data-stu-id="8457e-778">7</span></span>

<span data-ttu-id="8457e-779">8</span><span class="sxs-lookup"><span data-stu-id="8457e-779">8</span></span>

<span data-ttu-id="8457e-780">9</span><span class="sxs-lookup"><span data-stu-id="8457e-780">9</span></span>

<span data-ttu-id="8457e-781">2</span><span class="sxs-lookup"><span data-stu-id="8457e-781">2</span></span><br/> <span data-ttu-id="8457e-782">0</span><span class="sxs-lookup"><span data-stu-id="8457e-782">0</span></span><br/>

<span data-ttu-id="8457e-783">1</span><span class="sxs-lookup"><span data-stu-id="8457e-783">1</span></span>

<span data-ttu-id="8457e-784">2</span><span class="sxs-lookup"><span data-stu-id="8457e-784">2</span></span>

<span data-ttu-id="8457e-785">3</span><span class="sxs-lookup"><span data-stu-id="8457e-785">3</span></span>

<span data-ttu-id="8457e-786">4</span><span class="sxs-lookup"><span data-stu-id="8457e-786">4</span></span>

<span data-ttu-id="8457e-787">5</span><span class="sxs-lookup"><span data-stu-id="8457e-787">5</span></span>

<span data-ttu-id="8457e-788">6</span><span class="sxs-lookup"><span data-stu-id="8457e-788">6</span></span>

<span data-ttu-id="8457e-789">7</span><span class="sxs-lookup"><span data-stu-id="8457e-789">7</span></span>

<span data-ttu-id="8457e-790">8</span><span class="sxs-lookup"><span data-stu-id="8457e-790">8</span></span>

<span data-ttu-id="8457e-791">9</span><span class="sxs-lookup"><span data-stu-id="8457e-791">9</span></span>

<span data-ttu-id="8457e-792">3</span><span class="sxs-lookup"><span data-stu-id="8457e-792">3</span></span><br/> <span data-ttu-id="8457e-793">0</span><span class="sxs-lookup"><span data-stu-id="8457e-793">0</span></span><br/>

<span data-ttu-id="8457e-794">1</span><span class="sxs-lookup"><span data-stu-id="8457e-794">1</span></span>

<span data-ttu-id="8457e-795">cElements</span><span class="sxs-lookup"><span data-stu-id="8457e-795">cElements</span></span>

<span data-ttu-id="8457e-796">lLbound</span><span class="sxs-lookup"><span data-stu-id="8457e-796">lLbound</span></span>



 

<span data-ttu-id="8457e-797">**cElements**: entero de 32 bits sin signo, que especifica el número de elementos de la dimensión.</span><span class="sxs-lookup"><span data-stu-id="8457e-797">**cElements**: A 32-bit unsigned integer, specifying the number of elements in the dimension.</span></span>

<span data-ttu-id="8457e-798">**lLbound**: entero de 32 bits sin signo, que especifica el límite inferior de la dimensión.</span><span class="sxs-lookup"><span data-stu-id="8457e-798">**lLbound**: A 32-bit unsigned integer, specifying the lower bound of the dimension.</span></span>

### <a name="221115-safearray2"></a><span data-ttu-id="8457e-799">2.2.1.1.1.5 SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="8457e-799">2.2.1.1.1.5 SAFEARRAY2</span></span>

<span data-ttu-id="8457e-800">SAFEARRAY2 se usa para pasar matrices multidimensionales en SERIALIZEDPROPERTYVALUE.</span><span class="sxs-lookup"><span data-stu-id="8457e-800">SAFEARRAY2 is used to pass multidimensional arrays in SERIALIZEDPROPERTYVALUE.</span></span> <span data-ttu-id="8457e-801">La estructura contiene información sobre los límites y los datos.</span><span class="sxs-lookup"><span data-stu-id="8457e-801">The structure contains boundary information as well as the data.</span></span>



<span data-ttu-id="8457e-802">0</span><span class="sxs-lookup"><span data-stu-id="8457e-802">0</span></span>

<span data-ttu-id="8457e-803">1</span><span class="sxs-lookup"><span data-stu-id="8457e-803">1</span></span>

<span data-ttu-id="8457e-804">2</span><span class="sxs-lookup"><span data-stu-id="8457e-804">2</span></span>

<span data-ttu-id="8457e-805">3</span><span class="sxs-lookup"><span data-stu-id="8457e-805">3</span></span>

<span data-ttu-id="8457e-806">4</span><span class="sxs-lookup"><span data-stu-id="8457e-806">4</span></span>

<span data-ttu-id="8457e-807">5</span><span class="sxs-lookup"><span data-stu-id="8457e-807">5</span></span>

<span data-ttu-id="8457e-808">6</span><span class="sxs-lookup"><span data-stu-id="8457e-808">6</span></span>

<span data-ttu-id="8457e-809">7</span><span class="sxs-lookup"><span data-stu-id="8457e-809">7</span></span>

<span data-ttu-id="8457e-810">8</span><span class="sxs-lookup"><span data-stu-id="8457e-810">8</span></span>

<span data-ttu-id="8457e-811">9</span><span class="sxs-lookup"><span data-stu-id="8457e-811">9</span></span>

<span data-ttu-id="8457e-812">1</span><span class="sxs-lookup"><span data-stu-id="8457e-812">1</span></span><br/> <span data-ttu-id="8457e-813">0</span><span class="sxs-lookup"><span data-stu-id="8457e-813">0</span></span><br/>

<span data-ttu-id="8457e-814">1</span><span class="sxs-lookup"><span data-stu-id="8457e-814">1</span></span>

<span data-ttu-id="8457e-815">2</span><span class="sxs-lookup"><span data-stu-id="8457e-815">2</span></span>

<span data-ttu-id="8457e-816">3</span><span class="sxs-lookup"><span data-stu-id="8457e-816">3</span></span>

<span data-ttu-id="8457e-817">4</span><span class="sxs-lookup"><span data-stu-id="8457e-817">4</span></span>

<span data-ttu-id="8457e-818">5</span><span class="sxs-lookup"><span data-stu-id="8457e-818">5</span></span>

<span data-ttu-id="8457e-819">6</span><span class="sxs-lookup"><span data-stu-id="8457e-819">6</span></span>

<span data-ttu-id="8457e-820">7</span><span class="sxs-lookup"><span data-stu-id="8457e-820">7</span></span>

<span data-ttu-id="8457e-821">8</span><span class="sxs-lookup"><span data-stu-id="8457e-821">8</span></span>

<span data-ttu-id="8457e-822">9</span><span class="sxs-lookup"><span data-stu-id="8457e-822">9</span></span>

<span data-ttu-id="8457e-823">2</span><span class="sxs-lookup"><span data-stu-id="8457e-823">2</span></span><br/> <span data-ttu-id="8457e-824">0</span><span class="sxs-lookup"><span data-stu-id="8457e-824">0</span></span><br/>

<span data-ttu-id="8457e-825">1</span><span class="sxs-lookup"><span data-stu-id="8457e-825">1</span></span>

<span data-ttu-id="8457e-826">2</span><span class="sxs-lookup"><span data-stu-id="8457e-826">2</span></span>

<span data-ttu-id="8457e-827">3</span><span class="sxs-lookup"><span data-stu-id="8457e-827">3</span></span>

<span data-ttu-id="8457e-828">4</span><span class="sxs-lookup"><span data-stu-id="8457e-828">4</span></span>

<span data-ttu-id="8457e-829">5</span><span class="sxs-lookup"><span data-stu-id="8457e-829">5</span></span>

<span data-ttu-id="8457e-830">6</span><span class="sxs-lookup"><span data-stu-id="8457e-830">6</span></span>

<span data-ttu-id="8457e-831">7</span><span class="sxs-lookup"><span data-stu-id="8457e-831">7</span></span>

<span data-ttu-id="8457e-832">8</span><span class="sxs-lookup"><span data-stu-id="8457e-832">8</span></span>

<span data-ttu-id="8457e-833">9</span><span class="sxs-lookup"><span data-stu-id="8457e-833">9</span></span>

<span data-ttu-id="8457e-834">3</span><span class="sxs-lookup"><span data-stu-id="8457e-834">3</span></span><br/> <span data-ttu-id="8457e-835">0</span><span class="sxs-lookup"><span data-stu-id="8457e-835">0</span></span><br/>

<span data-ttu-id="8457e-836">1</span><span class="sxs-lookup"><span data-stu-id="8457e-836">1</span></span>

<span data-ttu-id="8457e-837">cDims</span><span class="sxs-lookup"><span data-stu-id="8457e-837">cDims</span></span>

<span data-ttu-id="8457e-838">Rgsabound (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-838">Rgsabound (variable)</span></span>

<span data-ttu-id="8457e-839">vData (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-839">vData (variable)</span></span>



 

<span data-ttu-id="8457e-840">**cDims**: entero de 32 bits sin signo, que indica el número de dimensiones de SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="8457e-840">**cDims**: Unsigned 32-bit integer, indicating the number of dimensions of the SAFEARRAY2.</span></span>

<span data-ttu-id="8457e-841">**Rgsabound**: una matriz que contiene una estructura SAFEARRAYBOUND, como se especifica en la sección 2.2.1.1.1.4 por dimensión en SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="8457e-841">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4 per dimension in the SAFEARRAY2.</span></span> <span data-ttu-id="8457e-842">En primer lugar, esta matriz tiene la dimensión situada más a la izquierda y la dimensión situada más a la derecha.</span><span class="sxs-lookup"><span data-stu-id="8457e-842">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="8457e-843">**vData**: un vector de elementos de serialización de un tipo determinado, indicado por el valor de DWTYPE del SERIALIZEDPROPERTYVALUE contenedor, con el bit 0x2000 desactivado.</span><span class="sxs-lookup"><span data-stu-id="8457e-843">**vData**: A vector of marshaled items of a particular type, indicated by the dwType of the containing SERIALIZEDPROPERTYVALUE, with bit 0x2000 cleared.</span></span> <span data-ttu-id="8457e-844">El formato de vData es el mismo que el especificado para el campo vData de SAFEARRAY en la sección 2.2.1.1.1.3.</span><span class="sxs-lookup"><span data-stu-id="8457e-844">The format of vData the same as that specified for the vData field of SAFEARRAY in Section 2.2.1.1.1.3.</span></span>

### <a name="2212-cfullpropspec"></a><span data-ttu-id="8457e-845">2.2.1.2 CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="8457e-845">2.2.1.2 CFullPropSpec</span></span>

<span data-ttu-id="8457e-846">La estructura CFullPropSpec contiene un GUID del conjunto de propiedades y un identificador de propiedad para identificar de forma única la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-846">The CFullPropSpec structure contains a property set GUID and a property identifier to uniquely identify property.</span></span>



<span data-ttu-id="8457e-847">0</span><span class="sxs-lookup"><span data-stu-id="8457e-847">0</span></span>

<span data-ttu-id="8457e-848">1</span><span class="sxs-lookup"><span data-stu-id="8457e-848">1</span></span>

<span data-ttu-id="8457e-849">2</span><span class="sxs-lookup"><span data-stu-id="8457e-849">2</span></span>

<span data-ttu-id="8457e-850">3</span><span class="sxs-lookup"><span data-stu-id="8457e-850">3</span></span>

<span data-ttu-id="8457e-851">4</span><span class="sxs-lookup"><span data-stu-id="8457e-851">4</span></span>

<span data-ttu-id="8457e-852">5</span><span class="sxs-lookup"><span data-stu-id="8457e-852">5</span></span>

<span data-ttu-id="8457e-853">6</span><span class="sxs-lookup"><span data-stu-id="8457e-853">6</span></span>

<span data-ttu-id="8457e-854">7</span><span class="sxs-lookup"><span data-stu-id="8457e-854">7</span></span>

<span data-ttu-id="8457e-855">8</span><span class="sxs-lookup"><span data-stu-id="8457e-855">8</span></span>

<span data-ttu-id="8457e-856">9</span><span class="sxs-lookup"><span data-stu-id="8457e-856">9</span></span>

<span data-ttu-id="8457e-857">1</span><span class="sxs-lookup"><span data-stu-id="8457e-857">1</span></span><br/> <span data-ttu-id="8457e-858">0</span><span class="sxs-lookup"><span data-stu-id="8457e-858">0</span></span><br/>

<span data-ttu-id="8457e-859">1</span><span class="sxs-lookup"><span data-stu-id="8457e-859">1</span></span>

<span data-ttu-id="8457e-860">2</span><span class="sxs-lookup"><span data-stu-id="8457e-860">2</span></span>

<span data-ttu-id="8457e-861">3</span><span class="sxs-lookup"><span data-stu-id="8457e-861">3</span></span>

<span data-ttu-id="8457e-862">4</span><span class="sxs-lookup"><span data-stu-id="8457e-862">4</span></span>

<span data-ttu-id="8457e-863">5</span><span class="sxs-lookup"><span data-stu-id="8457e-863">5</span></span>

<span data-ttu-id="8457e-864">6</span><span class="sxs-lookup"><span data-stu-id="8457e-864">6</span></span>

<span data-ttu-id="8457e-865">7</span><span class="sxs-lookup"><span data-stu-id="8457e-865">7</span></span>

<span data-ttu-id="8457e-866">8</span><span class="sxs-lookup"><span data-stu-id="8457e-866">8</span></span>

<span data-ttu-id="8457e-867">9</span><span class="sxs-lookup"><span data-stu-id="8457e-867">9</span></span>

<span data-ttu-id="8457e-868">2</span><span class="sxs-lookup"><span data-stu-id="8457e-868">2</span></span><br/> <span data-ttu-id="8457e-869">0</span><span class="sxs-lookup"><span data-stu-id="8457e-869">0</span></span><br/>

<span data-ttu-id="8457e-870">1</span><span class="sxs-lookup"><span data-stu-id="8457e-870">1</span></span>

<span data-ttu-id="8457e-871">2</span><span class="sxs-lookup"><span data-stu-id="8457e-871">2</span></span>

<span data-ttu-id="8457e-872">3</span><span class="sxs-lookup"><span data-stu-id="8457e-872">3</span></span>

<span data-ttu-id="8457e-873">4</span><span class="sxs-lookup"><span data-stu-id="8457e-873">4</span></span>

<span data-ttu-id="8457e-874">5</span><span class="sxs-lookup"><span data-stu-id="8457e-874">5</span></span>

<span data-ttu-id="8457e-875">6</span><span class="sxs-lookup"><span data-stu-id="8457e-875">6</span></span>

<span data-ttu-id="8457e-876">7</span><span class="sxs-lookup"><span data-stu-id="8457e-876">7</span></span>

<span data-ttu-id="8457e-877">8</span><span class="sxs-lookup"><span data-stu-id="8457e-877">8</span></span>

<span data-ttu-id="8457e-878">9</span><span class="sxs-lookup"><span data-stu-id="8457e-878">9</span></span>

<span data-ttu-id="8457e-879">3</span><span class="sxs-lookup"><span data-stu-id="8457e-879">3</span></span><br/> <span data-ttu-id="8457e-880">0</span><span class="sxs-lookup"><span data-stu-id="8457e-880">0</span></span><br/>

<span data-ttu-id="8457e-881">1</span><span class="sxs-lookup"><span data-stu-id="8457e-881">1</span></span>

<span data-ttu-id="8457e-882">\_guidPropSet</span><span class="sxs-lookup"><span data-stu-id="8457e-882">\_guidPropSet</span></span>

<span data-ttu-id="8457e-883">...</span><span class="sxs-lookup"><span data-stu-id="8457e-883">...</span></span>

<span data-ttu-id="8457e-884">...</span><span class="sxs-lookup"><span data-stu-id="8457e-884">...</span></span>

<span data-ttu-id="8457e-885">...</span><span class="sxs-lookup"><span data-stu-id="8457e-885">...</span></span>

<span data-ttu-id="8457e-886">ulKind</span><span class="sxs-lookup"><span data-stu-id="8457e-886">ulKind</span></span>

<span data-ttu-id="8457e-887">PrSpec</span><span class="sxs-lookup"><span data-stu-id="8457e-887">PrSpec</span></span>

<span data-ttu-id="8457e-888">Nombre de propiedad (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-888">Property name (variable)</span></span>



 

<span data-ttu-id="8457e-889">**\_ guidPropSet**: el GUID del conjunto de propiedades al que pertenece la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-889">**\_guidPropSet**: The GUID of the property set to which the property belongs.</span></span>

<span data-ttu-id="8457e-890">**ulKind**: entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-890">**ulKind**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="8457e-891">Uno de los siguientes valores, que indica el contenido de PrSpec.</span><span class="sxs-lookup"><span data-stu-id="8457e-891">One of the following values below, that indicates the contents of PrSpec.</span></span>



| <span data-ttu-id="8457e-892">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-892">Value</span></span>                                            | <span data-ttu-id="8457e-893">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-893">Meaning</span></span>                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-894">PRSPEC \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="8457e-894">PRSPEC\_ LPWSTR</span></span><br/> <span data-ttu-id="8457e-895">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8457e-895">0x00000000</span></span><br/> | <span data-ttu-id="8457e-896">El campo PrSpec especifica el número de caracteres no NULOs en el campo Nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-896">The PrSpec field specifies the number of non-NULL characters in the Property name field.</span></span> |
| <span data-ttu-id="8457e-897">PRSPEC \_ PROPID</span><span class="sxs-lookup"><span data-stu-id="8457e-897">PRSPEC\_PROPID</span></span><br/> <span data-ttu-id="8457e-898">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-898">0x00000001</span></span><br/>  | <span data-ttu-id="8457e-899">El campo PrSpec especifica el identificador de propiedad (PROPID).</span><span class="sxs-lookup"><span data-stu-id="8457e-899">The PrSpec field specifies the property ID (PROPID).</span></span>                                     |



 

<span data-ttu-id="8457e-900">**PrSpec**: entero de 32 bits sin signo con un significado indicado por el campo ulKind.</span><span class="sxs-lookup"><span data-stu-id="8457e-900">**PrSpec**: A 32-bit unsigned integer with a meaning as indicated by the ulKind field.</span></span>

<span data-ttu-id="8457e-901">**Nombre de propiedad**: si ulKind está establecido en PRSPEC \_ PROPID, este campo no debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-901">**Property name**: If ulKind is set to PRSPEC\_PROPID, this field MUST NOT be present.</span></span> <span data-ttu-id="8457e-902">Si ulKind se establece en PRSPEC \_ LPWStr, este campo debe contener una matriz sin distinción entre mayúsculas y minúsculas de PRSPEC caracteres Unicode que no sean NULL y que contenga el nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-902">If ulKind is set to PRSPEC\_LPWSTR, then this field MUST contain a case-insensitive array of PrSpec non-null Unicode characters, containing the name of the property.</span></span>

### <a name="2213-ccontentrestriction"></a><span data-ttu-id="8457e-903">2.2.1.3 CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-903">2.2.1.3 CContentRestriction</span></span>

<span data-ttu-id="8457e-904">La estructura CContentRestriction contiene una cadena que debe coincidir con una propiedad de la memoria caché de propiedades.</span><span class="sxs-lookup"><span data-stu-id="8457e-904">The CContentRestriction structure contains a string to match for a property in the property cache.</span></span>



<span data-ttu-id="8457e-905">0</span><span class="sxs-lookup"><span data-stu-id="8457e-905">0</span></span>

<span data-ttu-id="8457e-906">1</span><span class="sxs-lookup"><span data-stu-id="8457e-906">1</span></span>

<span data-ttu-id="8457e-907">2</span><span class="sxs-lookup"><span data-stu-id="8457e-907">2</span></span>

<span data-ttu-id="8457e-908">3</span><span class="sxs-lookup"><span data-stu-id="8457e-908">3</span></span>

<span data-ttu-id="8457e-909">4</span><span class="sxs-lookup"><span data-stu-id="8457e-909">4</span></span>

<span data-ttu-id="8457e-910">5</span><span class="sxs-lookup"><span data-stu-id="8457e-910">5</span></span>

<span data-ttu-id="8457e-911">6</span><span class="sxs-lookup"><span data-stu-id="8457e-911">6</span></span>

<span data-ttu-id="8457e-912">7</span><span class="sxs-lookup"><span data-stu-id="8457e-912">7</span></span>

<span data-ttu-id="8457e-913">8</span><span class="sxs-lookup"><span data-stu-id="8457e-913">8</span></span>

<span data-ttu-id="8457e-914">9</span><span class="sxs-lookup"><span data-stu-id="8457e-914">9</span></span>

<span data-ttu-id="8457e-915">1</span><span class="sxs-lookup"><span data-stu-id="8457e-915">1</span></span><br/> <span data-ttu-id="8457e-916">0</span><span class="sxs-lookup"><span data-stu-id="8457e-916">0</span></span><br/>

<span data-ttu-id="8457e-917">1</span><span class="sxs-lookup"><span data-stu-id="8457e-917">1</span></span>

<span data-ttu-id="8457e-918">2</span><span class="sxs-lookup"><span data-stu-id="8457e-918">2</span></span>

<span data-ttu-id="8457e-919">3</span><span class="sxs-lookup"><span data-stu-id="8457e-919">3</span></span>

<span data-ttu-id="8457e-920">4</span><span class="sxs-lookup"><span data-stu-id="8457e-920">4</span></span>

<span data-ttu-id="8457e-921">5</span><span class="sxs-lookup"><span data-stu-id="8457e-921">5</span></span>

<span data-ttu-id="8457e-922">6</span><span class="sxs-lookup"><span data-stu-id="8457e-922">6</span></span>

<span data-ttu-id="8457e-923">7</span><span class="sxs-lookup"><span data-stu-id="8457e-923">7</span></span>

<span data-ttu-id="8457e-924">8</span><span class="sxs-lookup"><span data-stu-id="8457e-924">8</span></span>

<span data-ttu-id="8457e-925">9</span><span class="sxs-lookup"><span data-stu-id="8457e-925">9</span></span>

<span data-ttu-id="8457e-926">2</span><span class="sxs-lookup"><span data-stu-id="8457e-926">2</span></span><br/> <span data-ttu-id="8457e-927">0</span><span class="sxs-lookup"><span data-stu-id="8457e-927">0</span></span><br/>

<span data-ttu-id="8457e-928">1</span><span class="sxs-lookup"><span data-stu-id="8457e-928">1</span></span>

<span data-ttu-id="8457e-929">2</span><span class="sxs-lookup"><span data-stu-id="8457e-929">2</span></span>

<span data-ttu-id="8457e-930">3</span><span class="sxs-lookup"><span data-stu-id="8457e-930">3</span></span>

<span data-ttu-id="8457e-931">4</span><span class="sxs-lookup"><span data-stu-id="8457e-931">4</span></span>

<span data-ttu-id="8457e-932">5</span><span class="sxs-lookup"><span data-stu-id="8457e-932">5</span></span>

<span data-ttu-id="8457e-933">6</span><span class="sxs-lookup"><span data-stu-id="8457e-933">6</span></span>

<span data-ttu-id="8457e-934">7</span><span class="sxs-lookup"><span data-stu-id="8457e-934">7</span></span>

<span data-ttu-id="8457e-935">8</span><span class="sxs-lookup"><span data-stu-id="8457e-935">8</span></span>

<span data-ttu-id="8457e-936">9</span><span class="sxs-lookup"><span data-stu-id="8457e-936">9</span></span>

<span data-ttu-id="8457e-937">3</span><span class="sxs-lookup"><span data-stu-id="8457e-937">3</span></span><br/> <span data-ttu-id="8457e-938">0</span><span class="sxs-lookup"><span data-stu-id="8457e-938">0</span></span><br/>

<span data-ttu-id="8457e-939">1</span><span class="sxs-lookup"><span data-stu-id="8457e-939">1</span></span>

<span data-ttu-id="8457e-940">\_Propiedad (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-940">\_Property (variable)</span></span>

<span data-ttu-id="8457e-941">...</span><span class="sxs-lookup"><span data-stu-id="8457e-941">...</span></span>

<span data-ttu-id="8457e-942">Padding1 (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-942">Padding1 (variable)</span></span>

<span data-ttu-id="8457e-943">CC</span><span class="sxs-lookup"><span data-stu-id="8457e-943">Cc</span></span>

<span data-ttu-id="8457e-944">\_pwcsPhrase (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-944">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="8457e-945">...</span><span class="sxs-lookup"><span data-stu-id="8457e-945">...</span></span>

<span data-ttu-id="8457e-946">Padding2 (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-946">Padding2 (variable)</span></span>

<span data-ttu-id="8457e-947">lcid</span><span class="sxs-lookup"><span data-stu-id="8457e-947">lcid</span></span>

<span data-ttu-id="8457e-948">\_ulGenerateMethod</span><span class="sxs-lookup"><span data-stu-id="8457e-948">\_ulGenerateMethod</span></span>



 

<span data-ttu-id="8457e-949">**\_ Property**: una estructura CFullPropSpec, como se especifica en la sección 2.2.1.2.</span><span class="sxs-lookup"><span data-stu-id="8457e-949">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2.</span></span> <span data-ttu-id="8457e-950">Este campo indica la propiedad en la que se va a realizar una operación de coincidencia.</span><span class="sxs-lookup"><span data-stu-id="8457e-950">This field indicates the property on which to perform a match operation.</span></span>

<span data-ttu-id="8457e-951">**Padding1**: este campo debe tener una longitud de 0 a 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="8457e-951">**Padding1**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="8457e-952">La longitud de este campo debe ser tal que el campo siguiente comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="8457e-952">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="8457e-953">Si este campo está presente (es decir, longitud distinto de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8457e-953">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="8457e-954">El receptor debe omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="8457e-954">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8457e-955">**CC**: un entero de 32 bits sin signo, que especifica el número de caracteres en el \_ campo pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="8457e-955">**Cc**: A 32-bit unsigned integer, specifying the number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="8457e-956">**\_ pwcsPhrase**: una cadena Unicode terminada en null que representa la palabra o frase que debe coincidir con la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-956">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="8457e-957">Este campo no debe estar vacío.</span><span class="sxs-lookup"><span data-stu-id="8457e-957">This field MUST NOT be empty.</span></span> <span data-ttu-id="8457e-958">El campo CC contiene la longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="8457e-958">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="8457e-959">**Padding2**: este campo debe tener una longitud de 0 a 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="8457e-959">**Padding2**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="8457e-960">La longitud de este campo debe ser tal que el campo siguiente comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="8457e-960">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="8457e-961">Si este campo está presente (es decir, longitud distinto de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8457e-961">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="8457e-962">El receptor debe omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="8457e-962">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8457e-963">**LCID**: un entero de 32 bits sin signo, que indica la configuración regional de \_ pwcsPhrase, como se especifica en el \[ apéndice a de MS-GPSI \] .</span><span class="sxs-lookup"><span data-stu-id="8457e-963">**Lcid**: A 32-bit unsigned integer, indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

<span data-ttu-id="8457e-964">**\_ ulGenerateMethod**: un entero de 32 bits sin signo, que especifica el método que se va a usar al generar formas de palabras alternativas</span><span class="sxs-lookup"><span data-stu-id="8457e-964">**\_ulGenerateMethod**: A 32-bit unsigned integer, specifying the method to use when generating alternate word forms</span></span>



| <span data-ttu-id="8457e-965">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-965">Value</span></span>                                                       | <span data-ttu-id="8457e-966">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-966">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-967">GENERAR \_ método \_ exactamente</span><span class="sxs-lookup"><span data-stu-id="8457e-967">GENERATE\_METHOD\_EXACT</span></span><br/> <span data-ttu-id="8457e-968">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8457e-968">0x00000000</span></span><br/>    | <span data-ttu-id="8457e-969">Coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="8457e-969">Exact match.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="8457e-970">GENERAR \_ \_ Prefijo de método</span><span class="sxs-lookup"><span data-stu-id="8457e-970">GENERATE\_METHOD\_PREFIX</span></span><br/> <span data-ttu-id="8457e-971">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-971">0x00000001</span></span> <br/>  | <span data-ttu-id="8457e-972">Coincidencia de prefijo.</span><span class="sxs-lookup"><span data-stu-id="8457e-972">Prefix match.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="8457e-973">\_derivación de método de generación \_</span><span class="sxs-lookup"><span data-stu-id="8457e-973">GENERATE\_METHOD\_INFLECT</span></span> <br/> <span data-ttu-id="8457e-974">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8457e-974">0x00000002</span></span><br/> | <span data-ttu-id="8457e-975">Coincide con las inflexiones de una palabra.</span><span class="sxs-lookup"><span data-stu-id="8457e-975">Matches inflections of a word.</span></span> <span data-ttu-id="8457e-976">Una inflexión de una palabra es una variante de la palabra raíz en la misma parte de la voz que se ha modificado según las reglas lingüísticas de un idioma determinado.</span><span class="sxs-lookup"><span data-stu-id="8457e-976">An inflection of a word is a variant of the root word in the same part of speech that has been modified according to linguistic rules of a given language.</span></span> <span data-ttu-id="8457e-977">Por ejemplo, las inflexiones del verbo "nadar" en inglés son "nadar", "nadar", "natación" y "Swam".</span><span class="sxs-lookup"><span data-stu-id="8457e-977">For example, inflections of the verb "swim" in English include "swim", "swims", "swimming", and "swam".</span></span> |



 

### <a name="2214-ckey"></a><span data-ttu-id="8457e-978">2.2.1.4 CKey</span><span class="sxs-lookup"><span data-stu-id="8457e-978">2.2.1.4 CKey</span></span>

<span data-ttu-id="8457e-979">La estructura CKey contiene un valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-979">The CKey structure contains a property value.</span></span>



<span data-ttu-id="8457e-980">0</span><span class="sxs-lookup"><span data-stu-id="8457e-980">0</span></span>

<span data-ttu-id="8457e-981">1</span><span class="sxs-lookup"><span data-stu-id="8457e-981">1</span></span>

<span data-ttu-id="8457e-982">2</span><span class="sxs-lookup"><span data-stu-id="8457e-982">2</span></span>

<span data-ttu-id="8457e-983">3</span><span class="sxs-lookup"><span data-stu-id="8457e-983">3</span></span>

<span data-ttu-id="8457e-984">4</span><span class="sxs-lookup"><span data-stu-id="8457e-984">4</span></span>

<span data-ttu-id="8457e-985">5</span><span class="sxs-lookup"><span data-stu-id="8457e-985">5</span></span>

<span data-ttu-id="8457e-986">6</span><span class="sxs-lookup"><span data-stu-id="8457e-986">6</span></span>

<span data-ttu-id="8457e-987">7</span><span class="sxs-lookup"><span data-stu-id="8457e-987">7</span></span>

<span data-ttu-id="8457e-988">8</span><span class="sxs-lookup"><span data-stu-id="8457e-988">8</span></span>

<span data-ttu-id="8457e-989">9</span><span class="sxs-lookup"><span data-stu-id="8457e-989">9</span></span>

<span data-ttu-id="8457e-990">1</span><span class="sxs-lookup"><span data-stu-id="8457e-990">1</span></span><br/> <span data-ttu-id="8457e-991">0</span><span class="sxs-lookup"><span data-stu-id="8457e-991">0</span></span><br/>

<span data-ttu-id="8457e-992">1</span><span class="sxs-lookup"><span data-stu-id="8457e-992">1</span></span>

<span data-ttu-id="8457e-993">2</span><span class="sxs-lookup"><span data-stu-id="8457e-993">2</span></span>

<span data-ttu-id="8457e-994">3</span><span class="sxs-lookup"><span data-stu-id="8457e-994">3</span></span>

<span data-ttu-id="8457e-995">4</span><span class="sxs-lookup"><span data-stu-id="8457e-995">4</span></span>

<span data-ttu-id="8457e-996">5</span><span class="sxs-lookup"><span data-stu-id="8457e-996">5</span></span>

<span data-ttu-id="8457e-997">6</span><span class="sxs-lookup"><span data-stu-id="8457e-997">6</span></span>

<span data-ttu-id="8457e-998">7</span><span class="sxs-lookup"><span data-stu-id="8457e-998">7</span></span>

<span data-ttu-id="8457e-999">8</span><span class="sxs-lookup"><span data-stu-id="8457e-999">8</span></span>

<span data-ttu-id="8457e-1000">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1000">9</span></span>

<span data-ttu-id="8457e-1001">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1001">2</span></span><br/> <span data-ttu-id="8457e-1002">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1002">0</span></span><br/>

<span data-ttu-id="8457e-1003">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1003">1</span></span>

<span data-ttu-id="8457e-1004">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1004">2</span></span>

<span data-ttu-id="8457e-1005">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1005">3</span></span>

<span data-ttu-id="8457e-1006">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1006">4</span></span>

<span data-ttu-id="8457e-1007">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1007">5</span></span>

<span data-ttu-id="8457e-1008">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1008">6</span></span>

<span data-ttu-id="8457e-1009">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1009">7</span></span>

<span data-ttu-id="8457e-1010">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1010">8</span></span>

<span data-ttu-id="8457e-1011">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1011">9</span></span>

<span data-ttu-id="8457e-1012">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1012">3</span></span><br/> <span data-ttu-id="8457e-1013">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1013">0</span></span><br/>

<span data-ttu-id="8457e-1014">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1014">1</span></span>

<span data-ttu-id="8457e-1015">PROPID</span><span class="sxs-lookup"><span data-stu-id="8457e-1015">PROPID</span></span>

<span data-ttu-id="8457e-1016">CB</span><span class="sxs-lookup"><span data-stu-id="8457e-1016">Cb</span></span>

<span data-ttu-id="8457e-1017">buf (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1017">buf (variable)</span></span>



 

<span data-ttu-id="8457e-1018">**PROPID**: entero de 32 bits sin signo que representa el identificador de propiedad como se describe en la sección 1.8.1.</span><span class="sxs-lookup"><span data-stu-id="8457e-1018">**PROPID**: A 32-bit unsigned integer, representing the property ID as discussed in section 1.8.1.</span></span> <span data-ttu-id="8457e-1019">Los valores conocidos son:</span><span class="sxs-lookup"><span data-stu-id="8457e-1019">Well-known values are:</span></span>



| <span data-ttu-id="8457e-1020">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-1020">Value</span></span>      | <span data-ttu-id="8457e-1021">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-1021">Meaning</span></span>                                                 |
|------------|---------------------------------------------------------|
| <span data-ttu-id="8457e-1022">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="8457e-1022">0xFFFFFFFF</span></span> | <span data-ttu-id="8457e-1023">Representa un identificador de propiedad no válido y no se debe utilizar.</span><span class="sxs-lookup"><span data-stu-id="8457e-1023">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="8457e-1024">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="8457e-1024">0xFFFFFFFE</span></span> | <span data-ttu-id="8457e-1025">Representa un identificador de propiedad no válido y no se debe utilizar.</span><span class="sxs-lookup"><span data-stu-id="8457e-1025">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="8457e-1026">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8457e-1026">0x00000000</span></span> | <span data-ttu-id="8457e-1027">Representa cualquier identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1027">Represents any property ID.</span></span>                             |



 

<span data-ttu-id="8457e-1028">**CB**: entero de 32 bits sin signo que contiene la longitud de buf, en bytes.</span><span class="sxs-lookup"><span data-stu-id="8457e-1028">**Cb**: A 32-bit unsigned integer containing the length of buf, in bytes.</span></span>

<span data-ttu-id="8457e-1029">**BUF**: secuencia de bytes que representa el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1029">**buf**: A sequence of bytes representing the value of the property.</span></span>

### <a name="2215-cinternalpropertyrestriction"></a><span data-ttu-id="8457e-1030">2.2.1.5 CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-1030">2.2.1.5 CInternalPropertyRestriction</span></span>

<span data-ttu-id="8457e-1031">La estructura CInternalPropertyRestriction contiene un valor de propiedad que debe coincidir con una operación.</span><span class="sxs-lookup"><span data-stu-id="8457e-1031">The CInternalPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="8457e-1032">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1032">0</span></span>

<span data-ttu-id="8457e-1033">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1033">1</span></span>

<span data-ttu-id="8457e-1034">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1034">2</span></span>

<span data-ttu-id="8457e-1035">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1035">3</span></span>

<span data-ttu-id="8457e-1036">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1036">4</span></span>

<span data-ttu-id="8457e-1037">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1037">5</span></span>

<span data-ttu-id="8457e-1038">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1038">6</span></span>

<span data-ttu-id="8457e-1039">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1039">7</span></span>

<span data-ttu-id="8457e-1040">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1040">8</span></span>

<span data-ttu-id="8457e-1041">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1041">9</span></span>

<span data-ttu-id="8457e-1042">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1042">1</span></span><br/> <span data-ttu-id="8457e-1043">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1043">0</span></span><br/>

<span data-ttu-id="8457e-1044">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1044">1</span></span>

<span data-ttu-id="8457e-1045">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1045">2</span></span>

<span data-ttu-id="8457e-1046">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1046">3</span></span>

<span data-ttu-id="8457e-1047">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1047">4</span></span>

<span data-ttu-id="8457e-1048">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1048">5</span></span>

<span data-ttu-id="8457e-1049">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1049">6</span></span>

<span data-ttu-id="8457e-1050">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1050">7</span></span>

<span data-ttu-id="8457e-1051">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1051">8</span></span>

<span data-ttu-id="8457e-1052">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1052">9</span></span>

<span data-ttu-id="8457e-1053">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1053">2</span></span><br/> <span data-ttu-id="8457e-1054">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1054">0</span></span><br/>

<span data-ttu-id="8457e-1055">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1055">1</span></span>

<span data-ttu-id="8457e-1056">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1056">2</span></span>

<span data-ttu-id="8457e-1057">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1057">3</span></span>

<span data-ttu-id="8457e-1058">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1058">4</span></span>

<span data-ttu-id="8457e-1059">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1059">5</span></span>

<span data-ttu-id="8457e-1060">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1060">6</span></span>

<span data-ttu-id="8457e-1061">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1061">7</span></span>

<span data-ttu-id="8457e-1062">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1062">8</span></span>

<span data-ttu-id="8457e-1063">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1063">9</span></span>

<span data-ttu-id="8457e-1064">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1064">3</span></span><br/> <span data-ttu-id="8457e-1065">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1065">0</span></span><br/>

<span data-ttu-id="8457e-1066">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1066">1</span></span>

<span data-ttu-id="8457e-1067">\_relop</span><span class="sxs-lookup"><span data-stu-id="8457e-1067">\_relop</span></span>

<span data-ttu-id="8457e-1068">\_ID</span><span class="sxs-lookup"><span data-stu-id="8457e-1068">\_pid</span></span>

<span data-ttu-id="8457e-1069">\_prval (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1069">\_prval (variable)</span></span>

<span data-ttu-id="8457e-1070">restrictionPresent</span><span class="sxs-lookup"><span data-stu-id="8457e-1070">restrictionPresent</span></span>

<span data-ttu-id="8457e-1071">nextRestriction (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1071">nextRestriction (variable)</span></span>



 

<span data-ttu-id="8457e-1072">**\_ relop**: entero de 32 bits que especifica la relación que se va a realizar en la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1072">**\_relop**: A 32-bit integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="8457e-1073">DEBE ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="8457e-1073">MUST be one of the following values:</span></span>



| <span data-ttu-id="8457e-1074">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-1074">Value</span></span>                 | <span data-ttu-id="8457e-1075">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-1075">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-1076">PRLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8457e-1076">PRLT 0x00000000</span></span>       | <span data-ttu-id="8457e-1077">Una comparación de menor que.</span><span class="sxs-lookup"><span data-stu-id="8457e-1077">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="8457e-1078">PRLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-1078">PRLE 0x00000001</span></span>       | <span data-ttu-id="8457e-1079">Comparación menor o igual que.</span><span class="sxs-lookup"><span data-stu-id="8457e-1079">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="8457e-1080">PRGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8457e-1080">PRGT 0x00000002</span></span>       | <span data-ttu-id="8457e-1081">Una comparación mayor que.</span><span class="sxs-lookup"><span data-stu-id="8457e-1081">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="8457e-1082">PRGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8457e-1082">PRGE 0x00000003</span></span>       | <span data-ttu-id="8457e-1083">Comparación mayor o igual que.</span><span class="sxs-lookup"><span data-stu-id="8457e-1083">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="8457e-1084">PREQ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8457e-1084">PREQ 0x00000004</span></span>       | <span data-ttu-id="8457e-1085">Una comparación de igualdad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1085">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="8457e-1086">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="8457e-1086">PRNE 0x00000005</span></span>       | <span data-ttu-id="8457e-1087">Comparación no igual.</span><span class="sxs-lookup"><span data-stu-id="8457e-1087">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="8457e-1088">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="8457e-1088">PRRE 0x00000006</span></span>       | <span data-ttu-id="8457e-1089">Una comparación de expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="8457e-1089">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="8457e-1090">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="8457e-1090">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="8457e-1091">Una operación and bit a bit que devuelve el operando derecho.</span><span class="sxs-lookup"><span data-stu-id="8457e-1091">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="8457e-1092">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="8457e-1092">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="8457e-1093">Una operación bit a bit y que devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8457e-1093">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="8457e-1094">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="8457e-1094">PRAll 0x00000100</span></span>      | <span data-ttu-id="8457e-1095">La operación se realiza en una columna de un conjunto de filas y solo es true si la operación es true para todas las filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-1095">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="8457e-1096">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="8457e-1096">PRAny 0x00000200</span></span>      | <span data-ttu-id="8457e-1097">La operación se realiza en una columna de un conjunto de filas y es true si la operación es true para cualquier fila.</span><span class="sxs-lookup"><span data-stu-id="8457e-1097">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="8457e-1098">**\_ PID**: un entero de 32 bits sin signo que representa el identificador de propiedad (consulte PROPID en la sección 2.2.1.4).</span><span class="sxs-lookup"><span data-stu-id="8457e-1098">**\_pid**: A 32-bit unsigned integer, representing the property ID (see PROPID in section 2.2.1.4).</span></span>

<span data-ttu-id="8457e-1099">**\_ prval**: un CBaseStorageVariant que contiene el valor que se va a relacionar con la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1099">**\_prval**: A CBaseStorageVariant containing the value to relate to the property.</span></span>

<span data-ttu-id="8457e-1100">**restrictionPresent**: un valor de tipo byte que indica si el campo nextRestriction está presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-1100">**restrictionPresent**: A byte value indicating if the nextRestriction field is present.</span></span> <span data-ttu-id="8457e-1101">DEBE establecerse en 0x00 o 0x01.</span><span class="sxs-lookup"><span data-stu-id="8457e-1101">MUST be set to either 0x00 or 0x01.</span></span> <span data-ttu-id="8457e-1102">Si se establece en 0x01, restrictionPresent indica que el campo nextRestriction está presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-1102">If set to 0x01, restrictionPresent indicates that the nextRestriction field is present.</span></span> <span data-ttu-id="8457e-1103">Si se establece en 0x00, restrictionPresent indica que el campo nextRestriction no está presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-1103">If set to 0x00, restrictionPresent indicates that the nextRestriction field is not present.</span></span>

<span data-ttu-id="8457e-1104">**nextRestriction**: una estructura CRestriction, como se especifica en la sección 2.2.1.16, que especifica una restricción adicional.</span><span class="sxs-lookup"><span data-stu-id="8457e-1104">**nextRestriction**: A CRestriction structure, as specified in section 2.2.1.16, specifying a further restriction.</span></span>

### <a name="2216-cnatlanguagerestriction"></a><span data-ttu-id="8457e-1105">2.2.1.6 CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-1105">2.2.1.6 CNatLanguageRestriction</span></span>

<span data-ttu-id="8457e-1106">La estructura CNatLanguageRestriction contiene una coincidencia de **consulta de lenguaje natural** para una propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1106">The CNatLanguageRestriction structure contains a **natural language query** match for a property.</span></span>



<span data-ttu-id="8457e-1107">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1107">0</span></span>

<span data-ttu-id="8457e-1108">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1108">1</span></span>

<span data-ttu-id="8457e-1109">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1109">2</span></span>

<span data-ttu-id="8457e-1110">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1110">3</span></span>

<span data-ttu-id="8457e-1111">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1111">4</span></span>

<span data-ttu-id="8457e-1112">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1112">5</span></span>

<span data-ttu-id="8457e-1113">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1113">6</span></span>

<span data-ttu-id="8457e-1114">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1114">7</span></span>

<span data-ttu-id="8457e-1115">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1115">8</span></span>

<span data-ttu-id="8457e-1116">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1116">9</span></span>

<span data-ttu-id="8457e-1117">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1117">1</span></span><br/> <span data-ttu-id="8457e-1118">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1118">0</span></span><br/>

<span data-ttu-id="8457e-1119">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1119">1</span></span>

<span data-ttu-id="8457e-1120">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1120">2</span></span>

<span data-ttu-id="8457e-1121">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1121">3</span></span>

<span data-ttu-id="8457e-1122">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1122">4</span></span>

<span data-ttu-id="8457e-1123">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1123">5</span></span>

<span data-ttu-id="8457e-1124">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1124">6</span></span>

<span data-ttu-id="8457e-1125">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1125">7</span></span>

<span data-ttu-id="8457e-1126">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1126">8</span></span>

<span data-ttu-id="8457e-1127">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1127">9</span></span>

<span data-ttu-id="8457e-1128">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1128">2</span></span><br/> <span data-ttu-id="8457e-1129">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1129">0</span></span><br/>

<span data-ttu-id="8457e-1130">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1130">1</span></span>

<span data-ttu-id="8457e-1131">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1131">2</span></span>

<span data-ttu-id="8457e-1132">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1132">3</span></span>

<span data-ttu-id="8457e-1133">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1133">4</span></span>

<span data-ttu-id="8457e-1134">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1134">5</span></span>

<span data-ttu-id="8457e-1135">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1135">6</span></span>

<span data-ttu-id="8457e-1136">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1136">7</span></span>

<span data-ttu-id="8457e-1137">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1137">8</span></span>

<span data-ttu-id="8457e-1138">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1138">9</span></span>

<span data-ttu-id="8457e-1139">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1139">3</span></span><br/> <span data-ttu-id="8457e-1140">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1140">0</span></span><br/>

<span data-ttu-id="8457e-1141">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1141">1</span></span>

<span data-ttu-id="8457e-1142">\_Propiedad (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1142">\_Property (variable)</span></span>

<span data-ttu-id="8457e-1143">...</span><span class="sxs-lookup"><span data-stu-id="8457e-1143">...</span></span>

<span data-ttu-id="8457e-1144">\_relleno \_ CC (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1144">\_padding\_cc (variable)</span></span>

<span data-ttu-id="8457e-1145">CC</span><span class="sxs-lookup"><span data-stu-id="8457e-1145">Cc</span></span>

<span data-ttu-id="8457e-1146">\_pwcsPhrase (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1146">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="8457e-1147">...</span><span class="sxs-lookup"><span data-stu-id="8457e-1147">...</span></span>

<span data-ttu-id="8457e-1148">\_LCID de relleno \_ (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1148">\_padding\_lcid (variable)</span></span>

<span data-ttu-id="8457e-1149">Lcid</span><span class="sxs-lookup"><span data-stu-id="8457e-1149">Lcid</span></span>



 

<span data-ttu-id="8457e-1150">**\_ Property**: una estructura CFullPropSpec, como se especifica en la sección 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="8457e-1150">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.3.</span></span> <span data-ttu-id="8457e-1151">Este campo indica la propiedad en la que se va a realizar la operación de coincidencia.</span><span class="sxs-lookup"><span data-stu-id="8457e-1151">This field indicates the property on which to perform the match operation.</span></span>

<span data-ttu-id="8457e-1152">**\_ relleno \_ CC**: este campo debe tener una longitud de 0 a 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="8457e-1152">**\_padding\_cc**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="8457e-1153">La longitud de este campo debe ser tal que el campo siguiente comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="8457e-1153">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="8457e-1154">Si este campo está presente (es decir, longitud distinto de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8457e-1154">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="8457e-1155">El receptor debe omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="8457e-1155">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8457e-1156">**CC**: entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-1156">**Cc**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="8457e-1157">Número de caracteres del \_ campo pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="8457e-1157">The number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="8457e-1158">**\_ pwcsPhrase**: una cadena Unicode terminada en null que representa la palabra o frase que debe coincidir con la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1158">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="8457e-1159">NO debe estar vacío.</span><span class="sxs-lookup"><span data-stu-id="8457e-1159">MUST NOT be empty.</span></span> <span data-ttu-id="8457e-1160">El campo CC contiene la longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="8457e-1160">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="8457e-1161">**\_ \_ LCID de relleno**: este campo debe tener una longitud de 0 a 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="8457e-1161">**\_padding\_lcid**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="8457e-1162">La longitud de este campo debe ser tal que el campo siguiente comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="8457e-1162">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="8457e-1163">Si este campo está presente (es decir, longitud distinto de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8457e-1163">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="8457e-1164">El receptor debe omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="8457e-1164">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8457e-1165">**LCID**: entero de 32 bits sin signo que indica la configuración regional de \_ pwcsPhrase, tal y como se especifica en el \[ apéndice a de MS-GPSI \] .</span><span class="sxs-lookup"><span data-stu-id="8457e-1165">**Lcid**: A 32-bit unsigned integer indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

### <a name="2217-cnoderestriction"></a><span data-ttu-id="8457e-1166">2.2.1.7 CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-1166">2.2.1.7 CNodeRestriction</span></span>

<span data-ttu-id="8457e-1167">La estructura CNodeRestriction contiene una matriz de nodos de **árbol de comandos** que especifican las restricciones de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-1167">The CNodeRestriction structure contains an array of **command tree** nodes that specify the restrictions for the query.</span></span>



<span data-ttu-id="8457e-1168">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1168">0</span></span>

<span data-ttu-id="8457e-1169">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1169">1</span></span>

<span data-ttu-id="8457e-1170">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1170">2</span></span>

<span data-ttu-id="8457e-1171">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1171">3</span></span>

<span data-ttu-id="8457e-1172">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1172">4</span></span>

<span data-ttu-id="8457e-1173">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1173">5</span></span>

<span data-ttu-id="8457e-1174">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1174">6</span></span>

<span data-ttu-id="8457e-1175">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1175">7</span></span>

<span data-ttu-id="8457e-1176">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1176">8</span></span>

<span data-ttu-id="8457e-1177">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1177">9</span></span>

<span data-ttu-id="8457e-1178">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1178">1</span></span><br/> <span data-ttu-id="8457e-1179">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1179">0</span></span><br/>

<span data-ttu-id="8457e-1180">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1180">1</span></span>

<span data-ttu-id="8457e-1181">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1181">2</span></span>

<span data-ttu-id="8457e-1182">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1182">3</span></span>

<span data-ttu-id="8457e-1183">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1183">4</span></span>

<span data-ttu-id="8457e-1184">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1184">5</span></span>

<span data-ttu-id="8457e-1185">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1185">6</span></span>

<span data-ttu-id="8457e-1186">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1186">7</span></span>

<span data-ttu-id="8457e-1187">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1187">8</span></span>

<span data-ttu-id="8457e-1188">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1188">9</span></span>

<span data-ttu-id="8457e-1189">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1189">2</span></span><br/> <span data-ttu-id="8457e-1190">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1190">0</span></span><br/>

<span data-ttu-id="8457e-1191">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1191">1</span></span>

<span data-ttu-id="8457e-1192">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1192">2</span></span>

<span data-ttu-id="8457e-1193">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1193">3</span></span>

<span data-ttu-id="8457e-1194">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1194">4</span></span>

<span data-ttu-id="8457e-1195">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1195">5</span></span>

<span data-ttu-id="8457e-1196">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1196">6</span></span>

<span data-ttu-id="8457e-1197">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1197">7</span></span>

<span data-ttu-id="8457e-1198">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1198">8</span></span>

<span data-ttu-id="8457e-1199">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1199">9</span></span>

<span data-ttu-id="8457e-1200">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1200">3</span></span><br/> <span data-ttu-id="8457e-1201">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1201">0</span></span><br/>

<span data-ttu-id="8457e-1202">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1202">1</span></span>

<span data-ttu-id="8457e-1203">\_cNode</span><span class="sxs-lookup"><span data-stu-id="8457e-1203">\_cNode</span></span>

<span data-ttu-id="8457e-1204">\_panode (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1204">\_paNode (variable)</span></span>



 

<span data-ttu-id="8457e-1205">**\_ cNode**: entero de 32 bits sin signo que especifica el número de estructuras CRestriction contenidas en el \_ campo panode.</span><span class="sxs-lookup"><span data-stu-id="8457e-1205">**\_cNode**: A 32-bit unsigned integer specifying the number of CRestriction structures contained in the \_paNode field.</span></span>

<span data-ttu-id="8457e-1206">**\_ panode**: una matriz de estructuras CRestriction.</span><span class="sxs-lookup"><span data-stu-id="8457e-1206">**\_paNode**: An array of CRestriction structures.</span></span> <span data-ttu-id="8457e-1207">Las estructuras de la matriz se deben separar entre 0 y 3 bytes de relleno, de modo que cada estructura comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta matriz.</span><span class="sxs-lookup"><span data-stu-id="8457e-1207">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="8457e-1208">Si los bytes de relleno están presentes, el valor que contienen es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8457e-1208">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="8457e-1209">El receptor debe omitir el contenido de los bytes de relleno.</span><span class="sxs-lookup"><span data-stu-id="8457e-1209">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="2218-coccrestriction"></a><span data-ttu-id="8457e-1210">2.2.1.8 COccRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-1210">2.2.1.8 COccRestriction</span></span>

<span data-ttu-id="8457e-1211">La estructura COccRestriction contiene la ubicación de una palabra en una frase.</span><span class="sxs-lookup"><span data-stu-id="8457e-1211">The COccRestriction structure contains the location of a word in a phrase.</span></span>



<span data-ttu-id="8457e-1212">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1212">0</span></span>

<span data-ttu-id="8457e-1213">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1213">1</span></span>

<span data-ttu-id="8457e-1214">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1214">2</span></span>

<span data-ttu-id="8457e-1215">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1215">3</span></span>

<span data-ttu-id="8457e-1216">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1216">4</span></span>

<span data-ttu-id="8457e-1217">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1217">5</span></span>

<span data-ttu-id="8457e-1218">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1218">6</span></span>

<span data-ttu-id="8457e-1219">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1219">7</span></span>

<span data-ttu-id="8457e-1220">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1220">8</span></span>

<span data-ttu-id="8457e-1221">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1221">9</span></span>

<span data-ttu-id="8457e-1222">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1222">1</span></span><br/> <span data-ttu-id="8457e-1223">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1223">0</span></span><br/>

<span data-ttu-id="8457e-1224">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1224">1</span></span>

<span data-ttu-id="8457e-1225">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1225">2</span></span>

<span data-ttu-id="8457e-1226">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1226">3</span></span>

<span data-ttu-id="8457e-1227">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1227">4</span></span>

<span data-ttu-id="8457e-1228">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1228">5</span></span>

<span data-ttu-id="8457e-1229">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1229">6</span></span>

<span data-ttu-id="8457e-1230">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1230">7</span></span>

<span data-ttu-id="8457e-1231">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1231">8</span></span>

<span data-ttu-id="8457e-1232">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1232">9</span></span>

<span data-ttu-id="8457e-1233">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1233">2</span></span><br/> <span data-ttu-id="8457e-1234">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1234">0</span></span><br/>

<span data-ttu-id="8457e-1235">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1235">1</span></span>

<span data-ttu-id="8457e-1236">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1236">2</span></span>

<span data-ttu-id="8457e-1237">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1237">3</span></span>

<span data-ttu-id="8457e-1238">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1238">4</span></span>

<span data-ttu-id="8457e-1239">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1239">5</span></span>

<span data-ttu-id="8457e-1240">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1240">6</span></span>

<span data-ttu-id="8457e-1241">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1241">7</span></span>

<span data-ttu-id="8457e-1242">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1242">8</span></span>

<span data-ttu-id="8457e-1243">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1243">9</span></span>

<span data-ttu-id="8457e-1244">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1244">3</span></span><br/> <span data-ttu-id="8457e-1245">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1245">0</span></span><br/>

<span data-ttu-id="8457e-1246">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1246">1</span></span>

<span data-ttu-id="8457e-1247">\_OCC</span><span class="sxs-lookup"><span data-stu-id="8457e-1247">\_occ</span></span>

<span data-ttu-id="8457e-1248">\_cPrevNoiseWords</span><span class="sxs-lookup"><span data-stu-id="8457e-1248">\_cPrevNoiseWords</span></span>

<span data-ttu-id="8457e-1249">\_cNextNoiseWords</span><span class="sxs-lookup"><span data-stu-id="8457e-1249">\_cNextNoiseWords</span></span>



 

<span data-ttu-id="8457e-1250">**\_ OCC**: entero de 32 bits sin signo que especifica el desplazamiento de la palabra en una cadena de consulta, en unidades de palabras.</span><span class="sxs-lookup"><span data-stu-id="8457e-1250">**\_occ**: A 32-bit unsigned integer specifying the offset of the word in a query string, in units of words.</span></span> <span data-ttu-id="8457e-1251">Una palabra, como se usa en esta especificación, es una unidad de idioma en cualquier configuración regional que lleve el significado.</span><span class="sxs-lookup"><span data-stu-id="8457e-1251">A word, as used in this specification, is a unit of language in any locale that carries meaning.</span></span>

<span data-ttu-id="8457e-1252">**\_ cPrevNoiseWords**: entero de 32 bits sin signo que contiene el número de **palabras irrelevantes** que se producen entre esta palabra y la palabra anterior en la frase.</span><span class="sxs-lookup"><span data-stu-id="8457e-1252">**\_cPrevNoiseWords**: A 32-bit unsigned integer containing the number of **noise words** that occur between this word and the previous word in the phrase.</span></span>

<span data-ttu-id="8457e-1253">**\_ cNextNoiseWords**: entero de 32 bits sin signo que contiene el número de palabras irrelevantes que se producen entre esta palabra y la siguiente palabra de la frase.</span><span class="sxs-lookup"><span data-stu-id="8457e-1253">**\_cNextNoiseWords**: A 32-bit unsigned integer containing the number of noise words that occur between this word and the next word in the phrase.</span></span>

### <a name="2219-cpropertyrestriction"></a><span data-ttu-id="8457e-1254">2.2.1.9 CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-1254">2.2.1.9 CPropertyRestriction</span></span>

<span data-ttu-id="8457e-1255">La estructura CPropertyRestriction contiene un valor de propiedad que debe coincidir con una operación.</span><span class="sxs-lookup"><span data-stu-id="8457e-1255">The CPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="8457e-1256">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1256">0</span></span>

<span data-ttu-id="8457e-1257">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1257">1</span></span>

<span data-ttu-id="8457e-1258">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1258">2</span></span>

<span data-ttu-id="8457e-1259">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1259">3</span></span>

<span data-ttu-id="8457e-1260">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1260">4</span></span>

<span data-ttu-id="8457e-1261">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1261">5</span></span>

<span data-ttu-id="8457e-1262">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1262">6</span></span>

<span data-ttu-id="8457e-1263">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1263">7</span></span>

<span data-ttu-id="8457e-1264">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1264">8</span></span>

<span data-ttu-id="8457e-1265">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1265">9</span></span>

<span data-ttu-id="8457e-1266">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1266">1</span></span><br/> <span data-ttu-id="8457e-1267">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1267">0</span></span><br/>

<span data-ttu-id="8457e-1268">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1268">1</span></span>

<span data-ttu-id="8457e-1269">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1269">2</span></span>

<span data-ttu-id="8457e-1270">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1270">3</span></span>

<span data-ttu-id="8457e-1271">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1271">4</span></span>

<span data-ttu-id="8457e-1272">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1272">5</span></span>

<span data-ttu-id="8457e-1273">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1273">6</span></span>

<span data-ttu-id="8457e-1274">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1274">7</span></span>

<span data-ttu-id="8457e-1275">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1275">8</span></span>

<span data-ttu-id="8457e-1276">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1276">9</span></span>

<span data-ttu-id="8457e-1277">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1277">2</span></span><br/> <span data-ttu-id="8457e-1278">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1278">0</span></span><br/>

<span data-ttu-id="8457e-1279">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1279">1</span></span>

<span data-ttu-id="8457e-1280">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1280">2</span></span>

<span data-ttu-id="8457e-1281">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1281">3</span></span>

<span data-ttu-id="8457e-1282">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1282">4</span></span>

<span data-ttu-id="8457e-1283">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1283">5</span></span>

<span data-ttu-id="8457e-1284">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1284">6</span></span>

<span data-ttu-id="8457e-1285">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1285">7</span></span>

<span data-ttu-id="8457e-1286">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1286">8</span></span>

<span data-ttu-id="8457e-1287">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1287">9</span></span>

<span data-ttu-id="8457e-1288">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1288">3</span></span><br/> <span data-ttu-id="8457e-1289">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1289">0</span></span><br/>

<span data-ttu-id="8457e-1290">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1290">1</span></span>

<span data-ttu-id="8457e-1291">\_relop</span><span class="sxs-lookup"><span data-stu-id="8457e-1291">\_relop</span></span>

<span data-ttu-id="8457e-1292">\_Propiedad (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1292">\_Property (variable)</span></span>

<span data-ttu-id="8457e-1293">\_prval (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1293">\_prval (variable)</span></span>



 

<span data-ttu-id="8457e-1294">**\_ relop**: entero de 32 bits sin signo que especifica la relación que se va a realizar en la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1294">**\_relop**: A 32-bit unsigned integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="8457e-1295">DEBE ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8457e-1295">MUST be one of the following values.</span></span>



| <span data-ttu-id="8457e-1296">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-1296">Value</span></span>                 | <span data-ttu-id="8457e-1297">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-1297">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-1298">PRLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8457e-1298">PRLT 0x00000000</span></span>       | <span data-ttu-id="8457e-1299">Una comparación de menor que.</span><span class="sxs-lookup"><span data-stu-id="8457e-1299">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="8457e-1300">PRLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-1300">PRLE 0x00000001</span></span>       | <span data-ttu-id="8457e-1301">Comparación menor o igual que.</span><span class="sxs-lookup"><span data-stu-id="8457e-1301">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="8457e-1302">PRGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8457e-1302">PRGT 0x00000002</span></span>       | <span data-ttu-id="8457e-1303">Una comparación mayor que.</span><span class="sxs-lookup"><span data-stu-id="8457e-1303">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="8457e-1304">PRGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8457e-1304">PRGE 0x00000003</span></span>       | <span data-ttu-id="8457e-1305">Comparación mayor o igual que.</span><span class="sxs-lookup"><span data-stu-id="8457e-1305">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="8457e-1306">PREQ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8457e-1306">PREQ 0x00000004</span></span>       | <span data-ttu-id="8457e-1307">Una comparación de igualdad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1307">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="8457e-1308">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="8457e-1308">PRNE 0x00000005</span></span>       | <span data-ttu-id="8457e-1309">Comparación no igual.</span><span class="sxs-lookup"><span data-stu-id="8457e-1309">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="8457e-1310">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="8457e-1310">PRRE 0x00000006</span></span>       | <span data-ttu-id="8457e-1311">Una comparación de expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="8457e-1311">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="8457e-1312">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="8457e-1312">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="8457e-1313">Una operación and bit a bit que devuelve el operando derecho.</span><span class="sxs-lookup"><span data-stu-id="8457e-1313">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="8457e-1314">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="8457e-1314">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="8457e-1315">Una operación bit a bit y que devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8457e-1315">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="8457e-1316">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="8457e-1316">PRAll 0x00000100</span></span>      | <span data-ttu-id="8457e-1317">La operación se realiza en una columna de un conjunto de filas y solo es true si la operación es true para todas las filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-1317">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="8457e-1318">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="8457e-1318">PRAny 0x00000200</span></span>      | <span data-ttu-id="8457e-1319">La operación se realiza en una columna de un conjunto de filas y es true si la operación es true para cualquier fila.</span><span class="sxs-lookup"><span data-stu-id="8457e-1319">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="8457e-1320">**\_ Property**: una estructura CFullPropSpec, como se especifica en la sección 2.2.1.2, que indica la propiedad en la que se va a realizar una operación de coincidencia.</span><span class="sxs-lookup"><span data-stu-id="8457e-1320">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2, indicating the property on which to perform a match operation.</span></span>

<span data-ttu-id="8457e-1321">**\_ prval**: una estructura CBaseStorageVariant, como se especifica en la sección 2.2.1.1, que contiene el valor que se va a relacionar con la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1321">**\_prval**: A CBaseStorageVariant structure, as specified in Section 2.2.1.1, containing the value to relate to the property.</span></span>

### <a name="22110-crangerestriction"></a><span data-ttu-id="8457e-1322">2.2.1.10 CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-1322">2.2.1.10 CRangeRestriction</span></span>

<span data-ttu-id="8457e-1323">La estructura CRangeRestriction contiene una restricción en un intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="8457e-1323">The CRangeRestriction structure contains a restriction on a range of values.</span></span>



<span data-ttu-id="8457e-1324">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1324">0</span></span>

<span data-ttu-id="8457e-1325">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1325">1</span></span>

<span data-ttu-id="8457e-1326">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1326">2</span></span>

<span data-ttu-id="8457e-1327">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1327">3</span></span>

<span data-ttu-id="8457e-1328">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1328">4</span></span>

<span data-ttu-id="8457e-1329">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1329">5</span></span>

<span data-ttu-id="8457e-1330">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1330">6</span></span>

<span data-ttu-id="8457e-1331">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1331">7</span></span>

<span data-ttu-id="8457e-1332">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1332">8</span></span>

<span data-ttu-id="8457e-1333">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1333">9</span></span>

<span data-ttu-id="8457e-1334">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1334">1</span></span><br/> <span data-ttu-id="8457e-1335">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1335">0</span></span><br/>

<span data-ttu-id="8457e-1336">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1336">1</span></span>

<span data-ttu-id="8457e-1337">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1337">2</span></span>

<span data-ttu-id="8457e-1338">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1338">3</span></span>

<span data-ttu-id="8457e-1339">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1339">4</span></span>

<span data-ttu-id="8457e-1340">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1340">5</span></span>

<span data-ttu-id="8457e-1341">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1341">6</span></span>

<span data-ttu-id="8457e-1342">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1342">7</span></span>

<span data-ttu-id="8457e-1343">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1343">8</span></span>

<span data-ttu-id="8457e-1344">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1344">9</span></span>

<span data-ttu-id="8457e-1345">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1345">2</span></span><br/> <span data-ttu-id="8457e-1346">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1346">0</span></span><br/>

<span data-ttu-id="8457e-1347">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1347">1</span></span>

<span data-ttu-id="8457e-1348">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1348">2</span></span>

<span data-ttu-id="8457e-1349">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1349">3</span></span>

<span data-ttu-id="8457e-1350">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1350">4</span></span>

<span data-ttu-id="8457e-1351">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1351">5</span></span>

<span data-ttu-id="8457e-1352">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1352">6</span></span>

<span data-ttu-id="8457e-1353">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1353">7</span></span>

<span data-ttu-id="8457e-1354">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1354">8</span></span>

<span data-ttu-id="8457e-1355">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1355">9</span></span>

<span data-ttu-id="8457e-1356">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1356">3</span></span><br/> <span data-ttu-id="8457e-1357">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1357">0</span></span><br/>

<span data-ttu-id="8457e-1358">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1358">1</span></span>

<span data-ttu-id="8457e-1359">\_keyStart (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1359">\_keyStart (variable)</span></span>

<span data-ttu-id="8457e-1360">\_keyEnd (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1360">\_keyEnd (variable)</span></span>



 

<span data-ttu-id="8457e-1361">**\_ keyStart**: una estructura CKey, como se especifica en la sección 2.2.1.4, que contiene el principio del intervalo.</span><span class="sxs-lookup"><span data-stu-id="8457e-1361">**\_keyStart**: A CKey structure, as specified in section 2.2.1.4, containing the beginning of the range.</span></span>

<span data-ttu-id="8457e-1362">**\_ keyEnd**: estructura CKey que contiene el final del intervalo.</span><span class="sxs-lookup"><span data-stu-id="8457e-1362">**\_keyEnd**: A CKey structure containing the end of the range.</span></span>

### <a name="22111-cscoperestriction"></a><span data-ttu-id="8457e-1363">2.2.1.11 CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-1363">2.2.1.11 CScopeRestriction</span></span>

<span data-ttu-id="8457e-1364">La estructura CScopeRestriction contiene una restricción en los archivos que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="8457e-1364">The CScopeRestriction structure contains a restriction on the files to be searched</span></span>



<span data-ttu-id="8457e-1365">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1365">0</span></span>

<span data-ttu-id="8457e-1366">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1366">1</span></span>

<span data-ttu-id="8457e-1367">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1367">2</span></span>

<span data-ttu-id="8457e-1368">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1368">3</span></span>

<span data-ttu-id="8457e-1369">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1369">4</span></span>

<span data-ttu-id="8457e-1370">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1370">5</span></span>

<span data-ttu-id="8457e-1371">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1371">6</span></span>

<span data-ttu-id="8457e-1372">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1372">7</span></span>

<span data-ttu-id="8457e-1373">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1373">8</span></span>

<span data-ttu-id="8457e-1374">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1374">9</span></span>

<span data-ttu-id="8457e-1375">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1375">1</span></span><br/> <span data-ttu-id="8457e-1376">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1376">0</span></span><br/>

<span data-ttu-id="8457e-1377">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1377">1</span></span>

<span data-ttu-id="8457e-1378">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1378">2</span></span>

<span data-ttu-id="8457e-1379">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1379">3</span></span>

<span data-ttu-id="8457e-1380">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1380">4</span></span>

<span data-ttu-id="8457e-1381">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1381">5</span></span>

<span data-ttu-id="8457e-1382">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1382">6</span></span>

<span data-ttu-id="8457e-1383">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1383">7</span></span>

<span data-ttu-id="8457e-1384">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1384">8</span></span>

<span data-ttu-id="8457e-1385">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1385">9</span></span>

<span data-ttu-id="8457e-1386">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1386">2</span></span><br/> <span data-ttu-id="8457e-1387">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1387">0</span></span><br/>

<span data-ttu-id="8457e-1388">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1388">1</span></span>

<span data-ttu-id="8457e-1389">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1389">2</span></span>

<span data-ttu-id="8457e-1390">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1390">3</span></span>

<span data-ttu-id="8457e-1391">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1391">4</span></span>

<span data-ttu-id="8457e-1392">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1392">5</span></span>

<span data-ttu-id="8457e-1393">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1393">6</span></span>

<span data-ttu-id="8457e-1394">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1394">7</span></span>

<span data-ttu-id="8457e-1395">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1395">8</span></span>

<span data-ttu-id="8457e-1396">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1396">9</span></span>

<span data-ttu-id="8457e-1397">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1397">3</span></span><br/> <span data-ttu-id="8457e-1398">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1398">0</span></span><br/>

<span data-ttu-id="8457e-1399">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1399">1</span></span>

<span data-ttu-id="8457e-1400">CcLowerPath</span><span class="sxs-lookup"><span data-stu-id="8457e-1400">CcLowerPath</span></span>

<span data-ttu-id="8457e-1401">\_lowerPath (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1401">\_lowerPath (variable)</span></span>

<span data-ttu-id="8457e-1402">...</span><span class="sxs-lookup"><span data-stu-id="8457e-1402">...</span></span>

<span data-ttu-id="8457e-1403">\_padding (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1403">\_padding ( variable)</span></span>

<span data-ttu-id="8457e-1404">\_longitud</span><span class="sxs-lookup"><span data-stu-id="8457e-1404">\_length</span></span>

<span data-ttu-id="8457e-1405">\_fRecursive</span><span class="sxs-lookup"><span data-stu-id="8457e-1405">\_fRecursive</span></span>

<span data-ttu-id="8457e-1406">\_fVirtual</span><span class="sxs-lookup"><span data-stu-id="8457e-1406">\_fVirtual</span></span>



 

<span data-ttu-id="8457e-1407">**CcLowerPath**: entero de 32 bits sin signo que contiene el número de caracteres Unicode en el \_ campo lowerPath.</span><span class="sxs-lookup"><span data-stu-id="8457e-1407">**CcLowerPath**: A 32-bit unsigned integer containing the number of Unicode characters in the \_lowerPath field.</span></span>

<span data-ttu-id="8457e-1408">**\_ lowerPath**: cadena Unicode terminada en null que representa la **ruta** de acceso en la que se debe restringir la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-1408">**\_lowerPath**: A non null-terminated Unicode string representing the **path** to which the query should be restricted.</span></span> <span data-ttu-id="8457e-1409">El campo CcLowerPath contiene la longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="8457e-1409">The CcLowerPath field contains the length of the string.</span></span>

<span data-ttu-id="8457e-1410">**\_ padding**: este campo debe tener una longitud de 0 a 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="8457e-1410">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="8457e-1411">La longitud de este campo debe ser tal que el campo siguiente comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="8457e-1411">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="8457e-1412">Si este campo está presente (es decir, longitud distinto de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8457e-1412">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="8457e-1413">El receptor debe omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="8457e-1413">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8457e-1414">**\_ length**: entero de 32 bits sin signo que contiene la longitud de \_ lowerPath, en caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="8457e-1414">**\_length**: A 32-bit unsigned integer containing the length of \_lowerPath, in Unicode characters.</span></span> <span data-ttu-id="8457e-1415">DEBE ser el mismo valor que CcLowerPath.</span><span class="sxs-lookup"><span data-stu-id="8457e-1415">This MUST be the same value as CcLowerPath.</span></span>

<span data-ttu-id="8457e-1416">**\_ fRecursive**: entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-1416">**\_fRecursive**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="8457e-1417">DEBE establecerse en 0x00000001 o 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-1417">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="8457e-1418">Si se establece en 0x00000001, el servidor examina de forma recursiva todos los subdirectorios de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="8457e-1418">If set to 0x00000001, the server is to recursively examine all subdirectories of the path.</span></span> <span data-ttu-id="8457e-1419">Si se establece en 0x00000000, el servidor no examinará ningún subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="8457e-1419">If set to 0x00000000, the server is to not examine any subdirectories.</span></span>

<span data-ttu-id="8457e-1420">**\_ fVirtual**: entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-1420">**\_fVirtual**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="8457e-1421">DEBE establecerse en 0x00000001 o 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-1421">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="8457e-1422">Si se establece en 0x00000001, \_ lowerPath es una ruta de acceso virtual (el localizador uniforme de recursos (URL) asociado a un directorio físico en el sistema de archivos) para un sitio Web.</span><span class="sxs-lookup"><span data-stu-id="8457e-1422">If set to 0x00000001, \_lowerPath is a virtual path (the Uniform Resource Locator (URL) associated with a physical directory on the file system) for a web site.</span></span> <span data-ttu-id="8457e-1423">Si se establece en 0x00000000, \_ lowerPath es una ruta de acceso del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="8457e-1423">If set to 0x00000000, \_lowerPath is a file system path.</span></span>

### <a name="22112-csort"></a><span data-ttu-id="8457e-1424">2.2.1.12 CSort</span><span class="sxs-lookup"><span data-stu-id="8457e-1424">2.2.1.12 CSort</span></span>

<span data-ttu-id="8457e-1425">La estructura CSort identifica una columna que se va a ordenar.</span><span class="sxs-lookup"><span data-stu-id="8457e-1425">The CSort structure identifies a column to sort.</span></span>



<span data-ttu-id="8457e-1426">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1426">0</span></span>

<span data-ttu-id="8457e-1427">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1427">1</span></span>

<span data-ttu-id="8457e-1428">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1428">2</span></span>

<span data-ttu-id="8457e-1429">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1429">3</span></span>

<span data-ttu-id="8457e-1430">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1430">4</span></span>

<span data-ttu-id="8457e-1431">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1431">5</span></span>

<span data-ttu-id="8457e-1432">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1432">6</span></span>

<span data-ttu-id="8457e-1433">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1433">7</span></span>

<span data-ttu-id="8457e-1434">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1434">8</span></span>

<span data-ttu-id="8457e-1435">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1435">9</span></span>

<span data-ttu-id="8457e-1436">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1436">1</span></span><br/> <span data-ttu-id="8457e-1437">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1437">0</span></span><br/>

<span data-ttu-id="8457e-1438">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1438">1</span></span>

<span data-ttu-id="8457e-1439">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1439">2</span></span>

<span data-ttu-id="8457e-1440">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1440">3</span></span>

<span data-ttu-id="8457e-1441">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1441">4</span></span>

<span data-ttu-id="8457e-1442">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1442">5</span></span>

<span data-ttu-id="8457e-1443">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1443">6</span></span>

<span data-ttu-id="8457e-1444">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1444">7</span></span>

<span data-ttu-id="8457e-1445">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1445">8</span></span>

<span data-ttu-id="8457e-1446">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1446">9</span></span>

<span data-ttu-id="8457e-1447">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1447">2</span></span><br/> <span data-ttu-id="8457e-1448">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1448">0</span></span><br/>

<span data-ttu-id="8457e-1449">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1449">1</span></span>

<span data-ttu-id="8457e-1450">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1450">2</span></span>

<span data-ttu-id="8457e-1451">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1451">3</span></span>

<span data-ttu-id="8457e-1452">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1452">4</span></span>

<span data-ttu-id="8457e-1453">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1453">5</span></span>

<span data-ttu-id="8457e-1454">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1454">6</span></span>

<span data-ttu-id="8457e-1455">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1455">7</span></span>

<span data-ttu-id="8457e-1456">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1456">8</span></span>

<span data-ttu-id="8457e-1457">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1457">9</span></span>

<span data-ttu-id="8457e-1458">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1458">3</span></span><br/> <span data-ttu-id="8457e-1459">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1459">0</span></span><br/>

<span data-ttu-id="8457e-1460">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1460">1</span></span>

<span data-ttu-id="8457e-1461">pidColumn</span><span class="sxs-lookup"><span data-stu-id="8457e-1461">pidColumn</span></span>

<span data-ttu-id="8457e-1462">dwOrd</span><span class="sxs-lookup"><span data-stu-id="8457e-1462">dwOrder</span></span>

<span data-ttu-id="8457e-1463">locale</span><span class="sxs-lookup"><span data-stu-id="8457e-1463">locale</span></span>



 

<span data-ttu-id="8457e-1464">**pidColumn**: entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-1464">**pidColumn**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="8457e-1465">Número de la columna por la que se va a ordenar.</span><span class="sxs-lookup"><span data-stu-id="8457e-1465">The number of the column to sort by.</span></span>

<span data-ttu-id="8457e-1466">**DWORD**: entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-1466">**dwOrder**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="8457e-1467">DEBE ser uno de los siguientes valores, especificando cómo ordenar en función de la columna.</span><span class="sxs-lookup"><span data-stu-id="8457e-1467">MUST be one of the following values, specifying how to sort based on the column.</span></span>



| <span data-ttu-id="8457e-1468">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-1468">Value</span></span>                        | <span data-ttu-id="8457e-1469">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-1469">Meaning</span></span>                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-1470">CONSULTA \_ SORTASCEND 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8457e-1470">QUERY\_SORTASCEND 0x00000000</span></span> | <span data-ttu-id="8457e-1471">Las filas se van a ordenar en orden ascendente en función de los valores de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="8457e-1471">The rows are to be sorted in ascending order based on the values in the column specified.</span></span>  |
| <span data-ttu-id="8457e-1472">QUERY \_ Descending 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-1472">QUERY\_DESCEND 0x00000001</span></span>    | <span data-ttu-id="8457e-1473">Las filas se van a ordenar en orden descendente en función de los valores de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="8457e-1473">The rows are to be sorted in descending order based on the values in the column specified.</span></span> |



 

<span data-ttu-id="8457e-1474">**locale**: un entero de 32 bits sin signo que indica la configuración regional, tal como se especifica en \[ \] el apéndice a de MS-GPSI, de la columna.</span><span class="sxs-lookup"><span data-stu-id="8457e-1474">**locale**: A 32-bit unsigned integer indicating the locale, as specified in \[MS-GPSI\] Appendix A, of the column.</span></span>

### <a name="22113-csynrestriction"></a><span data-ttu-id="8457e-1475">2.2.1.13 CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-1475">2.2.1.13 CSynRestriction</span></span>

<span data-ttu-id="8457e-1476">La estructura CSynRestriction contiene una palabra o sus sinónimos para una frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-1476">The CSynRestriction structure contains a word or its synonyms for a query phrase.</span></span>



<span data-ttu-id="8457e-1477">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1477">0</span></span>

<span data-ttu-id="8457e-1478">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1478">1</span></span>

<span data-ttu-id="8457e-1479">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1479">2</span></span>

<span data-ttu-id="8457e-1480">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1480">3</span></span>

<span data-ttu-id="8457e-1481">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1481">4</span></span>

<span data-ttu-id="8457e-1482">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1482">5</span></span>

<span data-ttu-id="8457e-1483">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1483">6</span></span>

<span data-ttu-id="8457e-1484">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1484">7</span></span>

<span data-ttu-id="8457e-1485">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1485">8</span></span>

<span data-ttu-id="8457e-1486">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1486">9</span></span>

<span data-ttu-id="8457e-1487">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1487">1</span></span><br/> <span data-ttu-id="8457e-1488">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1488">0</span></span><br/>

<span data-ttu-id="8457e-1489">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1489">1</span></span>

<span data-ttu-id="8457e-1490">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1490">2</span></span>

<span data-ttu-id="8457e-1491">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1491">3</span></span>

<span data-ttu-id="8457e-1492">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1492">4</span></span>

<span data-ttu-id="8457e-1493">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1493">5</span></span>

<span data-ttu-id="8457e-1494">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1494">6</span></span>

<span data-ttu-id="8457e-1495">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1495">7</span></span>

<span data-ttu-id="8457e-1496">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1496">8</span></span>

<span data-ttu-id="8457e-1497">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1497">9</span></span>

<span data-ttu-id="8457e-1498">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1498">2</span></span><br/> <span data-ttu-id="8457e-1499">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1499">0</span></span><br/>

<span data-ttu-id="8457e-1500">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1500">1</span></span>

<span data-ttu-id="8457e-1501">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1501">2</span></span>

<span data-ttu-id="8457e-1502">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1502">3</span></span>

<span data-ttu-id="8457e-1503">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1503">4</span></span>

<span data-ttu-id="8457e-1504">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1504">5</span></span>

<span data-ttu-id="8457e-1505">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1505">6</span></span>

<span data-ttu-id="8457e-1506">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1506">7</span></span>

<span data-ttu-id="8457e-1507">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1507">8</span></span>

<span data-ttu-id="8457e-1508">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1508">9</span></span>

<span data-ttu-id="8457e-1509">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1509">3</span></span><br/> <span data-ttu-id="8457e-1510">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1510">0</span></span><br/>

<span data-ttu-id="8457e-1511">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1511">1</span></span>

<span data-ttu-id="8457e-1512">Restricción</span><span class="sxs-lookup"><span data-stu-id="8457e-1512">Restriction</span></span>

<span data-ttu-id="8457e-1513">...</span><span class="sxs-lookup"><span data-stu-id="8457e-1513">...</span></span>

<span data-ttu-id="8457e-1514">...</span><span class="sxs-lookup"><span data-stu-id="8457e-1514">...</span></span>

<span data-ttu-id="8457e-1515">cKey</span><span class="sxs-lookup"><span data-stu-id="8457e-1515">cKey</span></span>

<span data-ttu-id="8457e-1516">\_keyArray (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1516">\_keyArray (variable)</span></span>

<span data-ttu-id="8457e-1517">\_isRange</span><span class="sxs-lookup"><span data-stu-id="8457e-1517">\_isRange</span></span>



 

<span data-ttu-id="8457e-1518">**Restriction**: una estructura COccRestriction que especifica la ubicación de la palabra.</span><span class="sxs-lookup"><span data-stu-id="8457e-1518">**Restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="8457e-1519">**cKey**: entero de 32 bits sin signo que especifica el número de elementos de la \_ matriz de keyArray.</span><span class="sxs-lookup"><span data-stu-id="8457e-1519">**cKey**: A 32-bit unsigned integer specifying the number of elements in the \_keyArray array.</span></span>

<span data-ttu-id="8457e-1520">**\_ keyArray**: una matriz de estructuras CKey que especifica una palabra y sus sinónimos.</span><span class="sxs-lookup"><span data-stu-id="8457e-1520">**\_keyArray**: An array of CKey structures specifying a word and its synonyms.</span></span>

<span data-ttu-id="8457e-1521">**\_ isRange**: si se establece en 0x01, las claves son prefijos que deben coincidir.</span><span class="sxs-lookup"><span data-stu-id="8457e-1521">**\_isRange**: If set to 0x01, the keys are prefixes to match.</span></span> <span data-ttu-id="8457e-1522">Si se establece en 0x00, las claves son valores exactos que deben coincidir.</span><span class="sxs-lookup"><span data-stu-id="8457e-1522">If set to 0x00, the keys are exact values to match.</span></span> <span data-ttu-id="8457e-1523">\_isRange no debe establecerse en ningún otro valor.</span><span class="sxs-lookup"><span data-stu-id="8457e-1523">\_isRange MUST NOT be set to any other values.</span></span>

### <a name="22114-cvectorrestriction"></a><span data-ttu-id="8457e-1524">2.2.1.14 CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-1524">2.2.1.14 CVectorRestriction</span></span>

<span data-ttu-id="8457e-1525">La estructura CVectorRestriction contiene una operación ponderada o en un nodo de árbol de comandos.</span><span class="sxs-lookup"><span data-stu-id="8457e-1525">The CVectorRestriction structure contains a weighted OR operation on a command tree node.</span></span>



<span data-ttu-id="8457e-1526">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1526">0</span></span>

<span data-ttu-id="8457e-1527">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1527">1</span></span>

<span data-ttu-id="8457e-1528">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1528">2</span></span>

<span data-ttu-id="8457e-1529">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1529">3</span></span>

<span data-ttu-id="8457e-1530">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1530">4</span></span>

<span data-ttu-id="8457e-1531">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1531">5</span></span>

<span data-ttu-id="8457e-1532">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1532">6</span></span>

<span data-ttu-id="8457e-1533">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1533">7</span></span>

<span data-ttu-id="8457e-1534">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1534">8</span></span>

<span data-ttu-id="8457e-1535">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1535">9</span></span>

<span data-ttu-id="8457e-1536">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1536">1</span></span><br/> <span data-ttu-id="8457e-1537">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1537">0</span></span><br/>

<span data-ttu-id="8457e-1538">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1538">1</span></span>

<span data-ttu-id="8457e-1539">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1539">2</span></span>

<span data-ttu-id="8457e-1540">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1540">3</span></span>

<span data-ttu-id="8457e-1541">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1541">4</span></span>

<span data-ttu-id="8457e-1542">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1542">5</span></span>

<span data-ttu-id="8457e-1543">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1543">6</span></span>

<span data-ttu-id="8457e-1544">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1544">7</span></span>

<span data-ttu-id="8457e-1545">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1545">8</span></span>

<span data-ttu-id="8457e-1546">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1546">9</span></span>

<span data-ttu-id="8457e-1547">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1547">2</span></span><br/> <span data-ttu-id="8457e-1548">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1548">0</span></span><br/>

<span data-ttu-id="8457e-1549">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1549">1</span></span>

<span data-ttu-id="8457e-1550">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1550">2</span></span>

<span data-ttu-id="8457e-1551">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1551">3</span></span>

<span data-ttu-id="8457e-1552">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1552">4</span></span>

<span data-ttu-id="8457e-1553">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1553">5</span></span>

<span data-ttu-id="8457e-1554">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1554">6</span></span>

<span data-ttu-id="8457e-1555">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1555">7</span></span>

<span data-ttu-id="8457e-1556">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1556">8</span></span>

<span data-ttu-id="8457e-1557">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1557">9</span></span>

<span data-ttu-id="8457e-1558">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1558">3</span></span><br/> <span data-ttu-id="8457e-1559">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1559">0</span></span><br/>

<span data-ttu-id="8457e-1560">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1560">1</span></span>

<span data-ttu-id="8457e-1561">\_Pres (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1561">\_pres (variable)</span></span>

<span data-ttu-id="8457e-1562">...</span><span class="sxs-lookup"><span data-stu-id="8457e-1562">...</span></span>

<span data-ttu-id="8457e-1563">\_padding (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1563">\_padding (variable)</span></span>

<span data-ttu-id="8457e-1564">\_ulRankMethod</span><span class="sxs-lookup"><span data-stu-id="8457e-1564">\_ulRankMethod</span></span>



 

<span data-ttu-id="8457e-1565">**\_ Pres**: un árbol de comandos CNodeRestriction en el que se va a realizar una operación de clasificación.</span><span class="sxs-lookup"><span data-stu-id="8457e-1565">**\_pres**: A CNodeRestriction command tree upon which a ranked OR operation is to be performed.</span></span>

<span data-ttu-id="8457e-1566">**\_ padding**: este campo debe tener una longitud de 0 a 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="8457e-1566">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="8457e-1567">La longitud de este campo debe ser tal que el campo siguiente comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="8457e-1567">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="8457e-1568">Si este campo está presente (es decir, longitud distinto de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8457e-1568">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="8457e-1569">El receptor debe omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="8457e-1569">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8457e-1570">**\_ ulRankMethod**: entero de 32 bits sin signo que especifica un algoritmo de clasificación.</span><span class="sxs-lookup"><span data-stu-id="8457e-1570">**\_ulRankMethod**: A 32-bit unsigned integer specifying a ranking algorithm.</span></span> <span data-ttu-id="8457e-1571">DEBE establecerse en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8457e-1571">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="8457e-1572">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-1572">Value</span></span>                            | <span data-ttu-id="8457e-1573">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-1573">Meaning</span></span>                                       |
|----------------------------------|-----------------------------------------------|
| <span data-ttu-id="8457e-1574">Rango del VECTOR \_ \_ min 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8457e-1574">VECTOR\_RANK\_MIN 0x00000000</span></span>     | <span data-ttu-id="8457e-1575">Use el algoritmo mínimo \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="8457e-1575">Use minimum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="8457e-1576">Rango de VECTOR \_ \_ máximo 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-1576">VECTOR\_RANK\_MAX 0x00000001</span></span>     | <span data-ttu-id="8457e-1577">Use la sal máxima del algoritmo \[ \] .</span><span class="sxs-lookup"><span data-stu-id="8457e-1577">Use maximum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="8457e-1578">VECTOR de \_ clasificación \_ interior 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8457e-1578">VECTOR\_RANK\_INNER 0x00000002</span></span>   | <span data-ttu-id="8457e-1579">Usar el algoritmo de producto interior \[ salon \] .</span><span class="sxs-lookup"><span data-stu-id="8457e-1579">Use inner product algorithm \[SALTON\].</span></span>       |
| <span data-ttu-id="8457e-1580">Índices de rango de VECTOR \_ \_ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8457e-1580">VECTOR\_RANK\_DICE 0x00000003</span></span>    | <span data-ttu-id="8457e-1581">Usar el algoritmo de coeficiente de los dados \[ . salon \] .</span><span class="sxs-lookup"><span data-stu-id="8457e-1581">Use Dice coefficient algorithm \[SALTON\].</span></span>    |
| <span data-ttu-id="8457e-1582">VECTOR \_ Rank \_ JACCARD 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8457e-1582">VECTOR\_RANK\_JACCARD 0x00000004</span></span> | <span data-ttu-id="8457e-1583">Use el algoritmo de coeficiente Jaccard \[ Salton \] .</span><span class="sxs-lookup"><span data-stu-id="8457e-1583">Use Jaccard coefficient algorithm \[SALTON\].</span></span> |



 

### <a name="22115-cwordrestriction"></a><span data-ttu-id="8457e-1584">2.2.1.15 CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-1584">2.2.1.15 CWordRestriction</span></span>

<span data-ttu-id="8457e-1585">La estructura CWordRestriction contiene una palabra para una frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-1585">The CWordRestriction structure contains a word for a query phrase.</span></span>



<span data-ttu-id="8457e-1586">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1586">0</span></span>

<span data-ttu-id="8457e-1587">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1587">1</span></span>

<span data-ttu-id="8457e-1588">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1588">2</span></span>

<span data-ttu-id="8457e-1589">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1589">3</span></span>

<span data-ttu-id="8457e-1590">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1590">4</span></span>

<span data-ttu-id="8457e-1591">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1591">5</span></span>

<span data-ttu-id="8457e-1592">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1592">6</span></span>

<span data-ttu-id="8457e-1593">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1593">7</span></span>

<span data-ttu-id="8457e-1594">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1594">8</span></span>

<span data-ttu-id="8457e-1595">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1595">9</span></span>

<span data-ttu-id="8457e-1596">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1596">1</span></span><br/> <span data-ttu-id="8457e-1597">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1597">0</span></span><br/>

<span data-ttu-id="8457e-1598">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1598">1</span></span>

<span data-ttu-id="8457e-1599">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1599">2</span></span>

<span data-ttu-id="8457e-1600">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1600">3</span></span>

<span data-ttu-id="8457e-1601">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1601">4</span></span>

<span data-ttu-id="8457e-1602">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1602">5</span></span>

<span data-ttu-id="8457e-1603">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1603">6</span></span>

<span data-ttu-id="8457e-1604">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1604">7</span></span>

<span data-ttu-id="8457e-1605">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1605">8</span></span>

<span data-ttu-id="8457e-1606">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1606">9</span></span>

<span data-ttu-id="8457e-1607">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1607">2</span></span><br/> <span data-ttu-id="8457e-1608">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1608">0</span></span><br/>

<span data-ttu-id="8457e-1609">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1609">1</span></span>

<span data-ttu-id="8457e-1610">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1610">2</span></span>

<span data-ttu-id="8457e-1611">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1611">3</span></span>

<span data-ttu-id="8457e-1612">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1612">4</span></span>

<span data-ttu-id="8457e-1613">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1613">5</span></span>

<span data-ttu-id="8457e-1614">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1614">6</span></span>

<span data-ttu-id="8457e-1615">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1615">7</span></span>

<span data-ttu-id="8457e-1616">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1616">8</span></span>

<span data-ttu-id="8457e-1617">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1617">9</span></span>

<span data-ttu-id="8457e-1618">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1618">3</span></span><br/> <span data-ttu-id="8457e-1619">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1619">0</span></span><br/>

<span data-ttu-id="8457e-1620">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1620">1</span></span>

<span data-ttu-id="8457e-1621">restricción</span><span class="sxs-lookup"><span data-stu-id="8457e-1621">restriction</span></span>

<span data-ttu-id="8457e-1622">...</span><span class="sxs-lookup"><span data-stu-id="8457e-1622">...</span></span>

<span data-ttu-id="8457e-1623">...</span><span class="sxs-lookup"><span data-stu-id="8457e-1623">...</span></span>

<span data-ttu-id="8457e-1624">\_Key (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1624">\_key (variable)</span></span>

<span data-ttu-id="8457e-1625">\_isRange</span><span class="sxs-lookup"><span data-stu-id="8457e-1625">\_isRange</span></span>



 

<span data-ttu-id="8457e-1626">**Restriction**: una estructura COccRestriction que especifica la ubicación de la palabra.</span><span class="sxs-lookup"><span data-stu-id="8457e-1626">**restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="8457e-1627">**\_ key**: una estructura CKey que especifica una palabra.</span><span class="sxs-lookup"><span data-stu-id="8457e-1627">**\_key**: A CKey structure specifying a word.</span></span>

<span data-ttu-id="8457e-1628">**\_ isRange**: si se establece en 0x01, la clave es un prefijo que debe coincidir.</span><span class="sxs-lookup"><span data-stu-id="8457e-1628">**\_isRange**: If set to 0x01, the key is a prefix to match.</span></span> <span data-ttu-id="8457e-1629">Si se establece en 0x00, la clave es un valor exacto que debe coincidir.</span><span class="sxs-lookup"><span data-stu-id="8457e-1629">If set to 0x00, the key is an exact value to match.</span></span> <span data-ttu-id="8457e-1630">\_isRange no debe establecerse en ningún otro valor.</span><span class="sxs-lookup"><span data-stu-id="8457e-1630">\_isRange MUST NOT be set to any other value.</span></span>

### <a name="22116-crestriction"></a><span data-ttu-id="8457e-1631">2.2.1.16 CRestriction</span><span class="sxs-lookup"><span data-stu-id="8457e-1631">2.2.1.16 CRestriction</span></span>

<span data-ttu-id="8457e-1632">La estructura CRestriction contiene un nodo de un árbol de comandos de consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-1632">The CRestriction structure contains a node of a query command tree.</span></span>



<span data-ttu-id="8457e-1633">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1633">0</span></span>

<span data-ttu-id="8457e-1634">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1634">1</span></span>

<span data-ttu-id="8457e-1635">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1635">2</span></span>

<span data-ttu-id="8457e-1636">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1636">3</span></span>

<span data-ttu-id="8457e-1637">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1637">4</span></span>

<span data-ttu-id="8457e-1638">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1638">5</span></span>

<span data-ttu-id="8457e-1639">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1639">6</span></span>

<span data-ttu-id="8457e-1640">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1640">7</span></span>

<span data-ttu-id="8457e-1641">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1641">8</span></span>

<span data-ttu-id="8457e-1642">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1642">9</span></span>

<span data-ttu-id="8457e-1643">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1643">1</span></span><br/> <span data-ttu-id="8457e-1644">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1644">0</span></span><br/>

<span data-ttu-id="8457e-1645">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1645">1</span></span>

<span data-ttu-id="8457e-1646">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1646">2</span></span>

<span data-ttu-id="8457e-1647">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1647">3</span></span>

<span data-ttu-id="8457e-1648">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1648">4</span></span>

<span data-ttu-id="8457e-1649">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1649">5</span></span>

<span data-ttu-id="8457e-1650">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1650">6</span></span>

<span data-ttu-id="8457e-1651">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1651">7</span></span>

<span data-ttu-id="8457e-1652">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1652">8</span></span>

<span data-ttu-id="8457e-1653">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1653">9</span></span>

<span data-ttu-id="8457e-1654">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1654">2</span></span><br/> <span data-ttu-id="8457e-1655">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1655">0</span></span><br/>

<span data-ttu-id="8457e-1656">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1656">1</span></span>

<span data-ttu-id="8457e-1657">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1657">2</span></span>

<span data-ttu-id="8457e-1658">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1658">3</span></span>

<span data-ttu-id="8457e-1659">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1659">4</span></span>

<span data-ttu-id="8457e-1660">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1660">5</span></span>

<span data-ttu-id="8457e-1661">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1661">6</span></span>

<span data-ttu-id="8457e-1662">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1662">7</span></span>

<span data-ttu-id="8457e-1663">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1663">8</span></span>

<span data-ttu-id="8457e-1664">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1664">9</span></span>

<span data-ttu-id="8457e-1665">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1665">3</span></span><br/> <span data-ttu-id="8457e-1666">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1666">0</span></span><br/>

<span data-ttu-id="8457e-1667">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1667">1</span></span>

<span data-ttu-id="8457e-1668">\_ulType</span><span class="sxs-lookup"><span data-stu-id="8457e-1668">\_ulType</span></span>

<span data-ttu-id="8457e-1669">Peso</span><span class="sxs-lookup"><span data-stu-id="8457e-1669">Weight</span></span>

<span data-ttu-id="8457e-1670">Restricción</span><span class="sxs-lookup"><span data-stu-id="8457e-1670">Restriction</span></span>



 

<span data-ttu-id="8457e-1671">**\_ ulType**: entero de 32 bits sin signo que indica el tipo de restricción que se usa para el nodo de árbol de comandos.</span><span class="sxs-lookup"><span data-stu-id="8457e-1671">**\_ulType**: A 32-bit unsigned integer indicating the restriction type used for the command tree node.</span></span> <span data-ttu-id="8457e-1672">DEBE establecerse en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8457e-1672">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="8457e-1673">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-1673">Value</span></span>                    | <span data-ttu-id="8457e-1674">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-1674">Meaning</span></span>                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-1675">RTNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8457e-1675">RTNone 0x00000000</span></span>        | <span data-ttu-id="8457e-1676">El nodo representa una palabra irrelevante en una consulta de vector.</span><span class="sxs-lookup"><span data-stu-id="8457e-1676">The node represents a noise word in a vector query.</span></span>                                         |
| <span data-ttu-id="8457e-1677">RTAnd 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-1677">RTAnd 0x00000001</span></span>         | <span data-ttu-id="8457e-1678">El nodo contiene un CNodeRestriction en el que se realiza una operación AND lógica que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="8457e-1678">The node contains a CNodeRestriction upon which a logical AND operation it to be performed.</span></span> |
| <span data-ttu-id="8457e-1679">RTOr 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8457e-1679">RTOr 0x00000002</span></span>          | <span data-ttu-id="8457e-1680">El nodo contiene un CNodeRestriction en el que se va a realizar una operación OR lógica.</span><span class="sxs-lookup"><span data-stu-id="8457e-1680">The node contains a CNodeRestriction upon which a logical OR operation is to be performed.</span></span>  |
| <span data-ttu-id="8457e-1681">RTNot 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8457e-1681">RTNot 0x00000003</span></span>         | <span data-ttu-id="8457e-1682">El nodo contiene un CRestriction en el que se va a realizar una operación NOT.</span><span class="sxs-lookup"><span data-stu-id="8457e-1682">The node contains a CRestriction upon which a NOT operation is to be performed.</span></span>             |
| <span data-ttu-id="8457e-1683">RTContent 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8457e-1683">RTContent 0x00000004</span></span>     | <span data-ttu-id="8457e-1684">El nodo contiene una CContentRestriction.</span><span class="sxs-lookup"><span data-stu-id="8457e-1684">The node contains a CContentRestriction.</span></span>                                                    |
| <span data-ttu-id="8457e-1685">RTProperty 0x00000005</span><span class="sxs-lookup"><span data-stu-id="8457e-1685">RTProperty 0x00000005</span></span>    | <span data-ttu-id="8457e-1686">El nodo contiene una CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="8457e-1686">The node contains a CPropertyRestriction.</span></span>                                                   |
| <span data-ttu-id="8457e-1687">RTProximity 0x00000006</span><span class="sxs-lookup"><span data-stu-id="8457e-1687">RTProximity 0x00000006</span></span>   | <span data-ttu-id="8457e-1688">El nodo contiene un CNodeRestriction sobre el que se va a realizar una clasificación de proximidad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1688">The node contains a CNodeRestriction upon which a proximity ranking is to be performed,</span></span>     |
| <span data-ttu-id="8457e-1689">RTVector 0x00000007</span><span class="sxs-lookup"><span data-stu-id="8457e-1689">RTVector 0x00000007</span></span>      | <span data-ttu-id="8457e-1690">El nodo contiene una CVectorRestriction.</span><span class="sxs-lookup"><span data-stu-id="8457e-1690">The node contains a CVectorRestriction.</span></span>                                                     |
| <span data-ttu-id="8457e-1691">RTNatLanguage 0x00000008</span><span class="sxs-lookup"><span data-stu-id="8457e-1691">RTNatLanguage 0x00000008</span></span> | <span data-ttu-id="8457e-1692">El nodo contiene una CNatLanguageRestriction.</span><span class="sxs-lookup"><span data-stu-id="8457e-1692">The node contains a CNatLanguageRestriction.</span></span>                                                |
| <span data-ttu-id="8457e-1693">RTScope 0x00000009</span><span class="sxs-lookup"><span data-stu-id="8457e-1693">RTScope 0x00000009</span></span>       | <span data-ttu-id="8457e-1694">El nodo contiene una CScopeRestriction.</span><span class="sxs-lookup"><span data-stu-id="8457e-1694">The node contains a CScopeRestriction.</span></span>                                                      |
| <span data-ttu-id="8457e-1695">PRAny 0xFFFFFFFA</span><span class="sxs-lookup"><span data-stu-id="8457e-1695">PRAny 0xFFFFFFFA</span></span>         | <span data-ttu-id="8457e-1696">El nodo contiene una CInternalPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="8457e-1696">The node contains a CInternalPropertyRestriction.</span></span>                                           |
| <span data-ttu-id="8457e-1697">RTRange 0xFFFFFFFC</span><span class="sxs-lookup"><span data-stu-id="8457e-1697">RTRange 0xFFFFFFFC</span></span>       | <span data-ttu-id="8457e-1698">El nodo contiene una CRangeRestriction.</span><span class="sxs-lookup"><span data-stu-id="8457e-1698">The node contains a CRangeRestriction.</span></span>                                                      |
| <span data-ttu-id="8457e-1699">RTPhrase 0xFFFFFFFD</span><span class="sxs-lookup"><span data-stu-id="8457e-1699">RTPhrase 0xFFFFFFFD</span></span>      | <span data-ttu-id="8457e-1700">El nodo contiene un CNodeRestriction sobre el que se va a realizar una coincidencia de frase.</span><span class="sxs-lookup"><span data-stu-id="8457e-1700">The node contains a CNodeRestriction upon which a phrase match is to be performed.</span></span>          |
| <span data-ttu-id="8457e-1701">RTSynonym 0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="8457e-1701">RTSynonym 0xFFFFFFFE</span></span>     | <span data-ttu-id="8457e-1702">El nodo contiene una CSynRestriction.</span><span class="sxs-lookup"><span data-stu-id="8457e-1702">The node contains a CSynRestriction.</span></span>                                                        |
| <span data-ttu-id="8457e-1703">RTWord 0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="8457e-1703">RTWord 0xFFFFFFFF</span></span>        | <span data-ttu-id="8457e-1704">El nodo contiene una CWordRestriction.</span><span class="sxs-lookup"><span data-stu-id="8457e-1704">The node contains a CWordRestriction.</span></span>                                                       |



 

<span data-ttu-id="8457e-1705">**Weight**: entero de 32 bits sin signo que representa el peso del nodo.</span><span class="sxs-lookup"><span data-stu-id="8457e-1705">**Weight**: A 32-bit unsigned integer representing the weight of the node.</span></span> <span data-ttu-id="8457e-1706">Weight indica la importancia del nodo en relación con otros nodos del árbol de comandos de consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-1706">Weight indicates the node's importance relative to other nodes in the query command tree.</span></span> <span data-ttu-id="8457e-1707">Los valores de peso mayores son más importantes.</span><span class="sxs-lookup"><span data-stu-id="8457e-1707">Higher weight values are more important.</span></span>

<span data-ttu-id="8457e-1708">**Restriction**: el tipo de restricción para el nodo de árbol de comandos.</span><span class="sxs-lookup"><span data-stu-id="8457e-1708">**Restriction**: The restriction type for the command tree node.</span></span> <span data-ttu-id="8457e-1709">La sintaxis debe ser la indicada por el \_ campo ulType.</span><span class="sxs-lookup"><span data-stu-id="8457e-1709">The syntax MUST be as indicated by the \_ulType field.</span></span>

### <a name="22117-ccolumnset"></a><span data-ttu-id="8457e-1710">2.2.1.17 CColumnSet</span><span class="sxs-lookup"><span data-stu-id="8457e-1710">2.2.1.17 CColumnSet</span></span>

<span data-ttu-id="8457e-1711">La estructura CColumnSet especifica los números de columna que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="8457e-1711">The CColumnSet structure specifies the column numbers to be returned.</span></span> <span data-ttu-id="8457e-1712">Esta estructura siempre se usa en referencia a una estructura CPidMapper específica (sección 2.2.1.23).</span><span class="sxs-lookup"><span data-stu-id="8457e-1712">This structure is always used in reference to a specific CPidMapper structure (section 2.2.1.23).</span></span>



<span data-ttu-id="8457e-1713">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1713">0</span></span>

<span data-ttu-id="8457e-1714">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1714">1</span></span>

<span data-ttu-id="8457e-1715">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1715">2</span></span>

<span data-ttu-id="8457e-1716">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1716">3</span></span>

<span data-ttu-id="8457e-1717">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1717">4</span></span>

<span data-ttu-id="8457e-1718">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1718">5</span></span>

<span data-ttu-id="8457e-1719">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1719">6</span></span>

<span data-ttu-id="8457e-1720">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1720">7</span></span>

<span data-ttu-id="8457e-1721">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1721">8</span></span>

<span data-ttu-id="8457e-1722">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1722">9</span></span>

<span data-ttu-id="8457e-1723">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1723">1</span></span><br/> <span data-ttu-id="8457e-1724">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1724">0</span></span><br/>

<span data-ttu-id="8457e-1725">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1725">1</span></span>

<span data-ttu-id="8457e-1726">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1726">2</span></span>

<span data-ttu-id="8457e-1727">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1727">3</span></span>

<span data-ttu-id="8457e-1728">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1728">4</span></span>

<span data-ttu-id="8457e-1729">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1729">5</span></span>

<span data-ttu-id="8457e-1730">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1730">6</span></span>

<span data-ttu-id="8457e-1731">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1731">7</span></span>

<span data-ttu-id="8457e-1732">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1732">8</span></span>

<span data-ttu-id="8457e-1733">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1733">9</span></span>

<span data-ttu-id="8457e-1734">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1734">2</span></span><br/> <span data-ttu-id="8457e-1735">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1735">0</span></span><br/>

<span data-ttu-id="8457e-1736">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1736">1</span></span>

<span data-ttu-id="8457e-1737">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1737">2</span></span>

<span data-ttu-id="8457e-1738">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1738">3</span></span>

<span data-ttu-id="8457e-1739">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1739">4</span></span>

<span data-ttu-id="8457e-1740">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1740">5</span></span>

<span data-ttu-id="8457e-1741">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1741">6</span></span>

<span data-ttu-id="8457e-1742">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1742">7</span></span>

<span data-ttu-id="8457e-1743">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1743">8</span></span>

<span data-ttu-id="8457e-1744">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1744">9</span></span>

<span data-ttu-id="8457e-1745">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1745">3</span></span><br/> <span data-ttu-id="8457e-1746">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1746">0</span></span><br/>

<span data-ttu-id="8457e-1747">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1747">1</span></span>

<span data-ttu-id="8457e-1748">count</span><span class="sxs-lookup"><span data-stu-id="8457e-1748">count</span></span>

<span data-ttu-id="8457e-1749">índices (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1749">indexes (variable)</span></span>



 

<span data-ttu-id="8457e-1750">**Count**: entero de 32 bits sin signo que especifica el número de elementos de la matriz de índices.</span><span class="sxs-lookup"><span data-stu-id="8457e-1750">**count**: A 32-bit unsigned integer specifying the number of elements in the indexes array.</span></span>

<span data-ttu-id="8457e-1751">**Indexes**: matriz de enteros de 4 bytes sin signo que representan índices de base cero en la matriz aPropSpec de la estructura CPidMapper correspondiente.</span><span class="sxs-lookup"><span data-stu-id="8457e-1751">**indexes**: Array of 4-byte unsigned integers representing zero-based indexes into the aPropSpec array in the corresponding CPidMapper structure.</span></span>

### <a name="22118-ccategorizationset"></a><span data-ttu-id="8457e-1752">2.2.1.18 CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="8457e-1752">2.2.1.18 CCategorizationSet</span></span>

<span data-ttu-id="8457e-1753">La estructura CCategorizationSet contiene información sobre la agrupación de un conjunto de resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-1753">The CCategorizationSet structure contains information about the grouping of a query result set.</span></span>



<span data-ttu-id="8457e-1754">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1754">0</span></span>

<span data-ttu-id="8457e-1755">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1755">1</span></span>

<span data-ttu-id="8457e-1756">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1756">2</span></span>

<span data-ttu-id="8457e-1757">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1757">3</span></span>

<span data-ttu-id="8457e-1758">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1758">4</span></span>

<span data-ttu-id="8457e-1759">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1759">5</span></span>

<span data-ttu-id="8457e-1760">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1760">6</span></span>

<span data-ttu-id="8457e-1761">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1761">7</span></span>

<span data-ttu-id="8457e-1762">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1762">8</span></span>

<span data-ttu-id="8457e-1763">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1763">9</span></span>

<span data-ttu-id="8457e-1764">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1764">1</span></span><br/> <span data-ttu-id="8457e-1765">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1765">0</span></span><br/>

<span data-ttu-id="8457e-1766">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1766">1</span></span>

<span data-ttu-id="8457e-1767">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1767">2</span></span>

<span data-ttu-id="8457e-1768">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1768">3</span></span>

<span data-ttu-id="8457e-1769">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1769">4</span></span>

<span data-ttu-id="8457e-1770">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1770">5</span></span>

<span data-ttu-id="8457e-1771">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1771">6</span></span>

<span data-ttu-id="8457e-1772">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1772">7</span></span>

<span data-ttu-id="8457e-1773">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1773">8</span></span>

<span data-ttu-id="8457e-1774">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1774">9</span></span>

<span data-ttu-id="8457e-1775">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1775">2</span></span><br/> <span data-ttu-id="8457e-1776">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1776">0</span></span><br/>

<span data-ttu-id="8457e-1777">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1777">1</span></span>

<span data-ttu-id="8457e-1778">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1778">2</span></span>

<span data-ttu-id="8457e-1779">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1779">3</span></span>

<span data-ttu-id="8457e-1780">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1780">4</span></span>

<span data-ttu-id="8457e-1781">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1781">5</span></span>

<span data-ttu-id="8457e-1782">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1782">6</span></span>

<span data-ttu-id="8457e-1783">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1783">7</span></span>

<span data-ttu-id="8457e-1784">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1784">8</span></span>

<span data-ttu-id="8457e-1785">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1785">9</span></span>

<span data-ttu-id="8457e-1786">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1786">3</span></span><br/> <span data-ttu-id="8457e-1787">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1787">0</span></span><br/>

<span data-ttu-id="8457e-1788">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1788">1</span></span>

<span data-ttu-id="8457e-1789">count</span><span class="sxs-lookup"><span data-stu-id="8457e-1789">count</span></span>

<span data-ttu-id="8457e-1790">categorías (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1790">categories (variable)</span></span>



 

<span data-ttu-id="8457e-1791">**Count**: entero de 32 bits sin signo que contiene el número de elementos de la matriz de categorías.</span><span class="sxs-lookup"><span data-stu-id="8457e-1791">**count**: A 32-bit unsigned integer containing the number of elements in the categories array.</span></span>

<span data-ttu-id="8457e-1792">**Categories**: matriz de estructuras CCategorizationSpec que especifican la agrupación de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-1792">**categories**: Array of CCategorizationSpec structures specifying the grouping of the query.</span></span>

### <a name="22119-ccategorizationspec"></a><span data-ttu-id="8457e-1793">2.2.1.19 CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="8457e-1793">2.2.1.19 CCategorizationSpec</span></span>

<span data-ttu-id="8457e-1794">La estructura CCategorizationSpec contiene una agrupación para un conjunto de resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-1794">The CCategorizationSpec structure contains a grouping for a query result set.</span></span>



<span data-ttu-id="8457e-1795">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1795">0</span></span>

<span data-ttu-id="8457e-1796">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1796">1</span></span>

<span data-ttu-id="8457e-1797">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1797">2</span></span>

<span data-ttu-id="8457e-1798">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1798">3</span></span>

<span data-ttu-id="8457e-1799">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1799">4</span></span>

<span data-ttu-id="8457e-1800">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1800">5</span></span>

<span data-ttu-id="8457e-1801">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1801">6</span></span>

<span data-ttu-id="8457e-1802">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1802">7</span></span>

<span data-ttu-id="8457e-1803">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1803">8</span></span>

<span data-ttu-id="8457e-1804">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1804">9</span></span>

<span data-ttu-id="8457e-1805">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1805">1</span></span><br/> <span data-ttu-id="8457e-1806">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1806">0</span></span><br/>

<span data-ttu-id="8457e-1807">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1807">1</span></span>

<span data-ttu-id="8457e-1808">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1808">2</span></span>

<span data-ttu-id="8457e-1809">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1809">3</span></span>

<span data-ttu-id="8457e-1810">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1810">4</span></span>

<span data-ttu-id="8457e-1811">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1811">5</span></span>

<span data-ttu-id="8457e-1812">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1812">6</span></span>

<span data-ttu-id="8457e-1813">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1813">7</span></span>

<span data-ttu-id="8457e-1814">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1814">8</span></span>

<span data-ttu-id="8457e-1815">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1815">9</span></span>

<span data-ttu-id="8457e-1816">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1816">2</span></span><br/> <span data-ttu-id="8457e-1817">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1817">0</span></span><br/>

<span data-ttu-id="8457e-1818">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1818">1</span></span>

<span data-ttu-id="8457e-1819">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1819">2</span></span>

<span data-ttu-id="8457e-1820">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1820">3</span></span>

<span data-ttu-id="8457e-1821">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1821">4</span></span>

<span data-ttu-id="8457e-1822">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1822">5</span></span>

<span data-ttu-id="8457e-1823">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1823">6</span></span>

<span data-ttu-id="8457e-1824">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1824">7</span></span>

<span data-ttu-id="8457e-1825">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1825">8</span></span>

<span data-ttu-id="8457e-1826">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1826">9</span></span>

<span data-ttu-id="8457e-1827">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1827">3</span></span><br/> <span data-ttu-id="8457e-1828">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1828">0</span></span><br/>

<span data-ttu-id="8457e-1829">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1829">1</span></span>

<span data-ttu-id="8457e-1830">\_csColumns (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1830">\_csColumns (variable)</span></span>

<span data-ttu-id="8457e-1831">\_ulCategType</span><span class="sxs-lookup"><span data-stu-id="8457e-1831">\_ulCategType</span></span>



 

<span data-ttu-id="8457e-1832">**\_ csColumns**: una estructura CColumnSet que indica las columnas por las que se va a agrupar la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-1832">**\_csColumns**: A CColumnSet structure indicating the columns by which to group the query.</span></span>

<span data-ttu-id="8457e-1833">**\_ ulCategType**: entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-1833">**\_ulCategType**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="8457e-1834">DEBE establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-1834">MUST be set to 0x00000000.</span></span>

### <a name="22120-cdbcolid"></a><span data-ttu-id="8457e-1835">2.2.1.20 CDbColId</span><span class="sxs-lookup"><span data-stu-id="8457e-1835">2.2.1.20 CDbColId</span></span>

<span data-ttu-id="8457e-1836">La estructura CDbColId contiene una columna.</span><span class="sxs-lookup"><span data-stu-id="8457e-1836">The CDbColId structure contains a column.</span></span>



<span data-ttu-id="8457e-1837">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1837">0</span></span>

<span data-ttu-id="8457e-1838">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1838">1</span></span>

<span data-ttu-id="8457e-1839">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1839">2</span></span>

<span data-ttu-id="8457e-1840">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1840">3</span></span>

<span data-ttu-id="8457e-1841">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1841">4</span></span>

<span data-ttu-id="8457e-1842">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1842">5</span></span>

<span data-ttu-id="8457e-1843">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1843">6</span></span>

<span data-ttu-id="8457e-1844">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1844">7</span></span>

<span data-ttu-id="8457e-1845">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1845">8</span></span>

<span data-ttu-id="8457e-1846">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1846">9</span></span>

<span data-ttu-id="8457e-1847">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1847">1</span></span><br/> <span data-ttu-id="8457e-1848">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1848">0</span></span><br/>

<span data-ttu-id="8457e-1849">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1849">1</span></span>

<span data-ttu-id="8457e-1850">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1850">2</span></span>

<span data-ttu-id="8457e-1851">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1851">3</span></span>

<span data-ttu-id="8457e-1852">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1852">4</span></span>

<span data-ttu-id="8457e-1853">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1853">5</span></span>

<span data-ttu-id="8457e-1854">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1854">6</span></span>

<span data-ttu-id="8457e-1855">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1855">7</span></span>

<span data-ttu-id="8457e-1856">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1856">8</span></span>

<span data-ttu-id="8457e-1857">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1857">9</span></span>

<span data-ttu-id="8457e-1858">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1858">2</span></span><br/> <span data-ttu-id="8457e-1859">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1859">0</span></span><br/>

<span data-ttu-id="8457e-1860">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1860">1</span></span>

<span data-ttu-id="8457e-1861">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1861">2</span></span>

<span data-ttu-id="8457e-1862">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1862">3</span></span>

<span data-ttu-id="8457e-1863">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1863">4</span></span>

<span data-ttu-id="8457e-1864">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1864">5</span></span>

<span data-ttu-id="8457e-1865">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1865">6</span></span>

<span data-ttu-id="8457e-1866">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1866">7</span></span>

<span data-ttu-id="8457e-1867">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1867">8</span></span>

<span data-ttu-id="8457e-1868">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1868">9</span></span>

<span data-ttu-id="8457e-1869">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1869">3</span></span><br/> <span data-ttu-id="8457e-1870">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1870">0</span></span><br/>

<span data-ttu-id="8457e-1871">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1871">1</span></span>

<span data-ttu-id="8457e-1872">eKind</span><span class="sxs-lookup"><span data-stu-id="8457e-1872">eKind</span></span>

<span data-ttu-id="8457e-1873">GUID</span><span class="sxs-lookup"><span data-stu-id="8457e-1873">GUID</span></span>

<span data-ttu-id="8457e-1874">...</span><span class="sxs-lookup"><span data-stu-id="8457e-1874">...</span></span>

<span data-ttu-id="8457e-1875">...</span><span class="sxs-lookup"><span data-stu-id="8457e-1875">...</span></span>

<span data-ttu-id="8457e-1876">...</span><span class="sxs-lookup"><span data-stu-id="8457e-1876">...</span></span>

<span data-ttu-id="8457e-1877">ulId</span><span class="sxs-lookup"><span data-stu-id="8457e-1877">ulId</span></span>

<span data-ttu-id="8457e-1878">vString (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1878">vString (variable)</span></span>



 

<span data-ttu-id="8457e-1879">**eKind**: debe establecerse en uno de los valores siguientes que indique el contenido de GUID y vValue.</span><span class="sxs-lookup"><span data-stu-id="8457e-1879">**eKind**: MUST be set to one of the values below that indicates the contents of GUID and vValue.</span></span>



| <span data-ttu-id="8457e-1880">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-1880">Value</span></span>                            | <span data-ttu-id="8457e-1881">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-1881">Meaning</span></span>                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-1882">DBKIND \_ \_ nombre GUID 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8457e-1882">DBKIND\_GUID\_NAME 0x00000000</span></span>    | <span data-ttu-id="8457e-1883">vString contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1883">vString contains a property name.</span></span>                                                                               |
| <span data-ttu-id="8457e-1884">GUID de DBKIND \_ \_ PROPID 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-1884">DBKIND\_GUID\_PROPID 0x00000001</span></span>  | <span data-ttu-id="8457e-1885">ulId contiene un entero de 4 bytes que indica el identificador de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1885">ulId contains a 4-byte integer indicating the property ID.</span></span>                                                      |
| <span data-ttu-id="8457e-1886">DBKIND \_ PGUID \_ nombre 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8457e-1886">DBKIND\_PGUID\_NAME 0x00000003</span></span>   | <span data-ttu-id="8457e-1887">vString contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1887">vString contains a property name.</span></span> <span data-ttu-id="8457e-1888">Este valor se debe tratar igual que el nombre del GUID de DBKIND \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8457e-1888">This value MUST be treated the same as DBKIND\_GUID\_NAME.</span></span>                    |
| <span data-ttu-id="8457e-1889">DBKIND \_ PGUID \_ PROPID 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8457e-1889">DBKIND\_PGUID\_PROPID 0x00000004</span></span> | <span data-ttu-id="8457e-1890">ulId contiene un entero de 4 bytes que indica el identificador de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1890">ulId contains a 4-byte integer indicating the property ID.</span></span> <span data-ttu-id="8457e-1891">Este valor debe ser el mismo que el \_ GUID de DBKIND \_ .</span><span class="sxs-lookup"><span data-stu-id="8457e-1891">This value MUST be the same as DBKIND\_GUID\_PROPID.</span></span> |



 

<span data-ttu-id="8457e-1892">**GUID**: el GUID de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1892">**GUID**: The property GUID.</span></span>

<span data-ttu-id="8457e-1893">**ulId**: si EKIND es DBKIND \_ GUID \_ PROPID o DBKIND \_ PGUID \_ PROPID, este campo contiene un entero sin signo que especifica el identificador de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1893">**ulId**: If eKind is DBKIND\_GUID\_PROPID or DBKIND\_PGUID\_PROPID, this field contains an unsigned integer, specifying the property ID.</span></span> <span data-ttu-id="8457e-1894">Si eKind es DBKIND \_ \_ nombre GUID o DBKIND \_ PGUID \_ nombre, este campo contiene un entero sin signo que especifica el número de caracteres Unicode contenidos en el campo vString.</span><span class="sxs-lookup"><span data-stu-id="8457e-1894">If eKind is DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME, this field contains an unsigned integer specifying the number of Unicode characters contained in the vString field.</span></span>

<span data-ttu-id="8457e-1895">**vString**: cadena Unicode terminada en null que representa el nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1895">**vString**: A non null-terminated Unicode string representing the property name.</span></span> <span data-ttu-id="8457e-1896">Se debe omitir a menos que el campo eKind se establezca en DBKIND \_ GUID \_ Name o DBKIND \_ PGUID \_ Name.</span><span class="sxs-lookup"><span data-stu-id="8457e-1896">It MUST be omitted unless the eKind field is set to DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME.</span></span>

### <a name="22121-cdbprop"></a><span data-ttu-id="8457e-1897">2.2.1.21 CDbProp</span><span class="sxs-lookup"><span data-stu-id="8457e-1897">2.2.1.21 CDbProp</span></span>

<span data-ttu-id="8457e-1898">La estructura CDbProp contiene una propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1898">The CDbProp structure contains a property.</span></span>



<span data-ttu-id="8457e-1899">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1899">0</span></span>

<span data-ttu-id="8457e-1900">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1900">1</span></span>

<span data-ttu-id="8457e-1901">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1901">2</span></span>

<span data-ttu-id="8457e-1902">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1902">3</span></span>

<span data-ttu-id="8457e-1903">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1903">4</span></span>

<span data-ttu-id="8457e-1904">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1904">5</span></span>

<span data-ttu-id="8457e-1905">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1905">6</span></span>

<span data-ttu-id="8457e-1906">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1906">7</span></span>

<span data-ttu-id="8457e-1907">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1907">8</span></span>

<span data-ttu-id="8457e-1908">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1908">9</span></span>

<span data-ttu-id="8457e-1909">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1909">1</span></span><br/> <span data-ttu-id="8457e-1910">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1910">0</span></span><br/>

<span data-ttu-id="8457e-1911">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1911">1</span></span>

<span data-ttu-id="8457e-1912">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1912">2</span></span>

<span data-ttu-id="8457e-1913">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1913">3</span></span>

<span data-ttu-id="8457e-1914">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1914">4</span></span>

<span data-ttu-id="8457e-1915">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1915">5</span></span>

<span data-ttu-id="8457e-1916">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1916">6</span></span>

<span data-ttu-id="8457e-1917">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1917">7</span></span>

<span data-ttu-id="8457e-1918">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1918">8</span></span>

<span data-ttu-id="8457e-1919">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1919">9</span></span>

<span data-ttu-id="8457e-1920">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1920">2</span></span><br/> <span data-ttu-id="8457e-1921">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1921">0</span></span><br/>

<span data-ttu-id="8457e-1922">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1922">1</span></span>

<span data-ttu-id="8457e-1923">2</span><span class="sxs-lookup"><span data-stu-id="8457e-1923">2</span></span>

<span data-ttu-id="8457e-1924">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1924">3</span></span>

<span data-ttu-id="8457e-1925">4</span><span class="sxs-lookup"><span data-stu-id="8457e-1925">4</span></span>

<span data-ttu-id="8457e-1926">5</span><span class="sxs-lookup"><span data-stu-id="8457e-1926">5</span></span>

<span data-ttu-id="8457e-1927">6</span><span class="sxs-lookup"><span data-stu-id="8457e-1927">6</span></span>

<span data-ttu-id="8457e-1928">7</span><span class="sxs-lookup"><span data-stu-id="8457e-1928">7</span></span>

<span data-ttu-id="8457e-1929">8</span><span class="sxs-lookup"><span data-stu-id="8457e-1929">8</span></span>

<span data-ttu-id="8457e-1930">9</span><span class="sxs-lookup"><span data-stu-id="8457e-1930">9</span></span>

<span data-ttu-id="8457e-1931">3</span><span class="sxs-lookup"><span data-stu-id="8457e-1931">3</span></span><br/> <span data-ttu-id="8457e-1932">0</span><span class="sxs-lookup"><span data-stu-id="8457e-1932">0</span></span><br/>

<span data-ttu-id="8457e-1933">1</span><span class="sxs-lookup"><span data-stu-id="8457e-1933">1</span></span>

<span data-ttu-id="8457e-1934">DBPROPID</span><span class="sxs-lookup"><span data-stu-id="8457e-1934">DBPROPID</span></span>

<span data-ttu-id="8457e-1935">DBPROPOPTIONS</span><span class="sxs-lookup"><span data-stu-id="8457e-1935">DBPROPOPTIONS</span></span>

<span data-ttu-id="8457e-1936">DBPROPSTATUS</span><span class="sxs-lookup"><span data-stu-id="8457e-1936">DBPROPSTATUS</span></span>

<span data-ttu-id="8457e-1937">colid (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1937">colid (variable)</span></span>

<span data-ttu-id="8457e-1938">vValue (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-1938">vValue (variable)</span></span>



 

<span data-ttu-id="8457e-1939">**DBPROPID**: entero de 32 bits sin signo, que indica el identificador de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1939">**DBPROPID**: A 32-bit unsigned integer, indicating the property ID.</span></span>

<span data-ttu-id="8457e-1940">**DBPROPOPTIONS** : debe establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-1940">**DBPROPOPTIONS** : MUST be set to 0x00000000.</span></span>

<span data-ttu-id="8457e-1941">**DBPROPSTATUS**: debe establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-1941">**DBPROPSTATUS**: MUST be set to 0x00000000.</span></span>

<span data-ttu-id="8457e-1942">**colid**: una estructura CDbColId, como se especifica en la sección 2.2.1.20, que indica la columna a la que se aplica la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1942">**colid**: A CDbColId structure, as specified in section 2.2.1.20, indicating the column to which the property applies.</span></span>

<span data-ttu-id="8457e-1943">**vValue**: un CBaseStorageVariant que contiene el valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-1943">**vValue**: A CBaseStorageVariant containing the property value.</span></span>

### <a name="221211-properties"></a><span data-ttu-id="8457e-1944">propiedades de 2.2.1.21.1</span><span class="sxs-lookup"><span data-stu-id="8457e-1944">2.2.1.21.1 Properties</span></span>

<span data-ttu-id="8457e-1945">En esta sección se detallan las propiedades que usa CISP.</span><span class="sxs-lookup"><span data-stu-id="8457e-1945">This section details the properties that are used by CISP.</span></span> <span data-ttu-id="8457e-1946">Estas propiedades se agrupan en tres conjuntos de propiedades: ident 2.2.1.21.1 ified en el campo guidPropertySet de la estructura CDbPropSet (sección 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="8457e-1946">These properties are grouped into three property sets, ident2.2.1.21.1 ified in the guidPropertySet field of the CDbPropSet structure (Section 2.2.1.22).</span></span>

<span data-ttu-id="8457e-1947">En la tabla siguiente se enumeran las propiedades que forman parte \_ del \_ conjunto de propiedades ext de DBPROPSET FSCIFRMWRK.</span><span class="sxs-lookup"><span data-stu-id="8457e-1947">The following table lists the properties that are part of the DBPROPSET\_FSCIFRMWRK\_EXT property set.</span></span>



| <span data-ttu-id="8457e-1948">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-1948">Value</span></span>                                  | <span data-ttu-id="8457e-1949">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-1949">Meaning</span></span>                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-1950">Nombre del catálogo de CI de DBPROP \_ \_ \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8457e-1950">DBPROP\_CI\_CATALOG\_NAME 0x00000002</span></span>   | <span data-ttu-id="8457e-1951">Especifica el nombre del catálogo o los catálogos que se van a consultar.</span><span class="sxs-lookup"><span data-stu-id="8457e-1951">Specifies the name of the catalog or catalogs to query.</span></span> <span data-ttu-id="8457e-1952">El valor debe ser un VT \_ LPWStr o un VT \_ Vector \| VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="8457e-1952">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR</span></span>                                   |
| <span data-ttu-id="8457e-1953">DBPROP \_ CI \_ incluye \_ ámbitos 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8457e-1953">DBPROP\_CI\_INCLUDE\_SCOPES 0x00000003</span></span> | <span data-ttu-id="8457e-1954">Especifica una o más rutas de acceso que se van a incluir en la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-1954">Specifies one or more paths to be included in the query.</span></span> <span data-ttu-id="8457e-1955">El valor debe ser un VT \_ LPWStr o un \_ Vector \| VT \_ LPWStr LPWStr.</span><span class="sxs-lookup"><span data-stu-id="8457e-1955">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR.</span></span>                                 |
| <span data-ttu-id="8457e-1956">DBPROP \_ marcas de ámbito de CI \_ \_ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8457e-1956">DBPROP\_CI\_SCOPE\_FLAGS 0x00000004</span></span>    | <span data-ttu-id="8457e-1957">Especifica cómo se tratarán las rutas de acceso especificadas por la \_ propiedad ámbitos de inclusión de DBPROP CI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8457e-1957">Specifies how the paths specified by the DBPROP\_CI\_INCLUDE\_SCOPES property are to be treated.</span></span> <span data-ttu-id="8457e-1958">El valor debe ser VT \_ I4 o VT \_ Vector \| VT \_ I4.</span><span class="sxs-lookup"><span data-stu-id="8457e-1958">Value MUST be a VT\_I4 or a VT\_VECTOR \| VT\_I4.</span></span> |
| <span data-ttu-id="8457e-1959">DBPROP \_ tipo de consulta de CI \_ \_ 0x00000007</span><span class="sxs-lookup"><span data-stu-id="8457e-1959">DBPROP\_CI\_QUERY\_TYPE 0x00000007</span></span>     | <span data-ttu-id="8457e-1960">Especifica el tipo de consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-1960">Specifies the type of query.</span></span> <span data-ttu-id="8457e-1961">CDbColId debe establecerse en DB \_ NULLID.</span><span class="sxs-lookup"><span data-stu-id="8457e-1961">The CDbColId MUST be set to DB\_NULLID.</span></span>                                                                               |



 

<span data-ttu-id="8457e-1962">En la tabla siguiente se enumeran las marcas de la propiedad de marcas de ámbito de CI de DBPROP \_ \_ \_ :</span><span class="sxs-lookup"><span data-stu-id="8457e-1962">The following table lists the flags for the DBPROP\_CI\_SCOPE\_FLAGS property:</span></span>



| <span data-ttu-id="8457e-1963">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-1963">Value</span></span>                     | <span data-ttu-id="8457e-1964">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-1964">Meaning</span></span>                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-1965">BÚSQUEDA \_ profunda de consulta 0x01</span><span class="sxs-lookup"><span data-stu-id="8457e-1965">QUERY\_DEEP 0x01</span></span>          | <span data-ttu-id="8457e-1966">Si se establece, indica que los archivos del directorio de ámbito y todos los subdirectorios se incluyen en los resultados.</span><span class="sxs-lookup"><span data-stu-id="8457e-1966">If set, indicates that files in the scope directory and all subdirectories are included in the results.</span></span> <span data-ttu-id="8457e-1967">Si está desactivada, solo los archivos del directorio de ámbito se incluyen en los resultados.</span><span class="sxs-lookup"><span data-stu-id="8457e-1967">If clear, only files in the scope directory are included in the results.</span></span> <span data-ttu-id="8457e-1968">NO se debe combinar con Deep de consulta \_ .</span><span class="sxs-lookup"><span data-stu-id="8457e-1968">MUST NOT be combined with QUERY\_DEEP.</span></span> |
| <span data-ttu-id="8457e-1969">\_Ruta de acceso virtual de consulta \_ 0x02</span><span class="sxs-lookup"><span data-stu-id="8457e-1969">QUERY\_VIRTUAL\_PATH 0x02</span></span> | <span data-ttu-id="8457e-1970">Si se establece, indica que el ámbito es una ruta de acceso virtual.</span><span class="sxs-lookup"><span data-stu-id="8457e-1970">If set, indicates that the scope is a virtual path.</span></span> <span data-ttu-id="8457e-1971">Si está desactivada, indica que el ámbito es un directorio físico.</span><span class="sxs-lookup"><span data-stu-id="8457e-1971">If clear, indicates that the scope is a physical directory.</span></span>                                                                                                         |



 

<span data-ttu-id="8457e-1972">En la tabla siguiente se enumeran los tipos de consulta para la \_ \_ propiedad tipo de consulta DBPROP CI \_ :</span><span class="sxs-lookup"><span data-stu-id="8457e-1972">The following table lists the query types for the DBPROP\_CI\_QUERY\_TYPE property:</span></span>



| <span data-ttu-id="8457e-1973">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-1973">Value</span></span>                     | <span data-ttu-id="8457e-1974">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-1974">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-1975">CiNormal 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8457e-1975">CiNormal 0x00000000</span></span>       | <span data-ttu-id="8457e-1976">Una consulta normal.</span><span class="sxs-lookup"><span data-stu-id="8457e-1976">A regular query.</span></span>                                                                                                   |
| <span data-ttu-id="8457e-1977">CiVirtualRoots 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-1977">CiVirtualRoots 0x00000001</span></span> | <span data-ttu-id="8457e-1978">La consulta solicita una lista de las raíces virtuales del catálogo.</span><span class="sxs-lookup"><span data-stu-id="8457e-1978">The query is requesting a list of the virtual roots of the catalog.</span></span> <span data-ttu-id="8457e-1979">Este valor requiere privilegios administrativos.</span><span class="sxs-lookup"><span data-stu-id="8457e-1979">This value requires administrative privileges.</span></span> |
| <span data-ttu-id="8457e-1980">CiProperties 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8457e-1980">CiProperties 0x00000003</span></span>   | <span data-ttu-id="8457e-1981">La consulta solicita una lista de todas las propiedades admitidas por el servicio de indización.</span><span class="sxs-lookup"><span data-stu-id="8457e-1981">The query is requesting a list of all the properties supported by the indexing service.</span></span>                            |
| <span data-ttu-id="8457e-1982">CiAdminOp 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8457e-1982">CiAdminOp 0x00000004</span></span>      | <span data-ttu-id="8457e-1983">La consulta es una operación administrativa.</span><span class="sxs-lookup"><span data-stu-id="8457e-1983">The query is an administrative operation.</span></span> <span data-ttu-id="8457e-1984">Este valor requiere privilegios administrativos.</span><span class="sxs-lookup"><span data-stu-id="8457e-1984">This value requires administrative privileges.</span></span>                           |



 

<span data-ttu-id="8457e-1985">En la tabla siguiente se enumeran las propiedades que forman parte del \_ conjunto de propiedades DBPROPSET QUERYEXT.</span><span class="sxs-lookup"><span data-stu-id="8457e-1985">The following table lists the properties that are part of the DBPROPSET\_QUERYEXT property set.</span></span>



| <span data-ttu-id="8457e-1986">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-1986">Value</span></span>                                      | <span data-ttu-id="8457e-1987">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-1987">Meaning</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-1988">DBPROP \_ USECONTENTINDEX 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8457e-1988">DBPROP\_USECONTENTINDEX 0x00000002</span></span>         | <span data-ttu-id="8457e-1989">Especifica cómo el servicio de indización controla las consultas lentas.</span><span class="sxs-lookup"><span data-stu-id="8457e-1989">Specifies how the indexing service is to handle slow queries.</span></span> <span data-ttu-id="8457e-1990">El valor debe ser un VT \_ bool.</span><span class="sxs-lookup"><span data-stu-id="8457e-1990">Value MUST be a VT\_BOOL.</span></span> <span data-ttu-id="8457e-1991">Si es TRUE, se permite que el servidor no pueda realizar estas consultas.</span><span class="sxs-lookup"><span data-stu-id="8457e-1991">If TRUE, the server is allowed to fail these queries.</span></span>                                                                                    |
| <span data-ttu-id="8457e-1992">DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8457e-1992">DBPROP\_DEFERNONINDEXEDTRIMMING 0x00000003</span></span> | <span data-ttu-id="8457e-1993">Indica si el servicio de indización va a realizar el recorte de los resultados.</span><span class="sxs-lookup"><span data-stu-id="8457e-1993">Indicates whether the indexing service is to perform results trimming.</span></span> <span data-ttu-id="8457e-1994">Si es TRUE, el servidor debe considerar la posibilidad de realizar un recorte de los resultados de forma que se optimice el tiempo de respuesta para el cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-1994">If TRUE, the server is to consider performing results trimming in a way that optimizes response time to the client.</span></span> <span data-ttu-id="8457e-1995">El valor debe ser un VT \_ bool.</span><span class="sxs-lookup"><span data-stu-id="8457e-1995">Value MUST be a VT\_BOOL.</span></span>             |
| <span data-ttu-id="8457e-1996">DBPROP \_ USEEXTENDEDDBTYPES 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8457e-1996">DBPROP\_USEEXTENDEDDBTYPES 0x00000004</span></span>      | <span data-ttu-id="8457e-1997">Indica si el cliente admite los \_ tipos de datos de vector VT.</span><span class="sxs-lookup"><span data-stu-id="8457e-1997">Indicates whether the client supports VT\_VECTOR data types.</span></span> <span data-ttu-id="8457e-1998">Si es TRUE, el cliente admite el \_ Vector VT; si es false, el servidor debe convertir los \_ tipos de datos de vector VT en \_ tipos de datos de matriz VT.</span><span class="sxs-lookup"><span data-stu-id="8457e-1998">If TRUE, then the client supports VT\_VECTOR; if FALSE, then the server is to convert VT\_VECTOR data types to VT\_ARRAY data types.</span></span>  <span data-ttu-id="8457e-1999">El valor debe ser un VT \_ bool.</span><span class="sxs-lookup"><span data-stu-id="8457e-1999">The value MUST be a VT\_BOOL.</span></span> |
| <span data-ttu-id="8457e-2000">DBPROP \_ FIRSTROWS 0x00000007</span><span class="sxs-lookup"><span data-stu-id="8457e-2000">DBPROP\_FIRSTROWS 0x00000007</span></span>               | <span data-ttu-id="8457e-2001">Indica las coincidencias de filas que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="8457e-2001">Indicates the row matches to return.</span></span> <span data-ttu-id="8457e-2002">Si es TRUE, el servidor devuelve el primer conjunto de filas coincidentes.</span><span class="sxs-lookup"><span data-stu-id="8457e-2002">If TRUE, the server is to return the first set of matching rows.</span></span> <span data-ttu-id="8457e-2003">Si es FALSE, se deben devolver las filas coincidentes más adecuadas.</span><span class="sxs-lookup"><span data-stu-id="8457e-2003">If FALSE, the best matching rows should be returned.</span></span> <span data-ttu-id="8457e-2004">El valor debe ser un VT \_ bool.</span><span class="sxs-lookup"><span data-stu-id="8457e-2004">Value MUST be a VT\_BOOL.</span></span>                                             |



 

<span data-ttu-id="8457e-2005">En la tabla siguiente se enumeran las propiedades que forman parte \_ del \_ conjunto de propiedades ext de DBPROPSET CIFRMWRKCORE.</span><span class="sxs-lookup"><span data-stu-id="8457e-2005">The following table lists the properties that are part of the DBPROPSET\_CIFRMWRKCORE\_EXT property set.</span></span>



| <span data-ttu-id="8457e-2006">Valor/DBPROPID</span><span class="sxs-lookup"><span data-stu-id="8457e-2006">Value / DBPROPID</span></span>                 | <span data-ttu-id="8457e-2007">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-2007">Meaning</span></span>                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-2008">\_Máquina DBPROP 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8457e-2008">DBPROP\_MACHINE 0x00000002</span></span>       | <span data-ttu-id="8457e-2009">Especifica los nombres de los equipos en los que se va a procesar una consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-2009">Specifies the names of the computer(s) on which a query is to be processed.</span></span> <span data-ttu-id="8457e-2010">El valor debe ser VT \_ BSTR o VT \_ matriz \| VT \_ .</span><span class="sxs-lookup"><span data-stu-id="8457e-2010">The value MUST be either VT\_BSTR or VT\_ARRAY \| VT\_BSTR.</span></span> |
| <span data-ttu-id="8457e-2011">\_CLSID de cliente DBPROP \_ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8457e-2011">DBPROP\_CLIENT\_CLSID 0x00000003</span></span> | <span data-ttu-id="8457e-2012">Especifica una constante de conexión para el servicio de indización.</span><span class="sxs-lookup"><span data-stu-id="8457e-2012">Specifies a connection constant for the indexing service.</span></span> <span data-ttu-id="8457e-2013">El valor debe ser un CLSID de VT \_ que contenga 0x2A4880706FD911D0A80800A0C906241A.</span><span class="sxs-lookup"><span data-stu-id="8457e-2013">The value MUST be a VT\_CLSID containing 0x2A4880706FD911D0A80800A0C906241A.</span></span>  |



 

### <a name="22122-cdbpropset"></a><span data-ttu-id="8457e-2014">2.2.1.22 CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="8457e-2014">2.2.1.22 CDbPropSet</span></span>

<span data-ttu-id="8457e-2015">La estructura CDbPropSet contiene un conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="8457e-2015">The CDbPropSet structure contains a set of properties.</span></span> <span data-ttu-id="8457e-2016">Tenga en cuenta que el primer campo tiene un tamaño fijo, pero es posible que no esté alineado en un desplazamiento que sea un múltiplo de 4 bytes desde el inicio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="8457e-2016">Note that the first field is fixed-size, but may not be aligned at an offset that is a 4-byte multiple from the start of the message containing this structure.</span></span> <span data-ttu-id="8457e-2017">Sin embargo, el campo cProperties se alinea como tal y, por lo tanto, el formato se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="8457e-2017">However, the cProperties field is aligned as such, and hence the format is depicted as follows:</span></span>



<span data-ttu-id="8457e-2018">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2018">0</span></span>

<span data-ttu-id="8457e-2019">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2019">1</span></span>

<span data-ttu-id="8457e-2020">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2020">2</span></span>

<span data-ttu-id="8457e-2021">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2021">3</span></span>

<span data-ttu-id="8457e-2022">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2022">4</span></span>

<span data-ttu-id="8457e-2023">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2023">5</span></span>

<span data-ttu-id="8457e-2024">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2024">6</span></span>

<span data-ttu-id="8457e-2025">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2025">7</span></span>

<span data-ttu-id="8457e-2026">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2026">8</span></span>

<span data-ttu-id="8457e-2027">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2027">9</span></span>

<span data-ttu-id="8457e-2028">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2028">1</span></span><br/> <span data-ttu-id="8457e-2029">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2029">0</span></span><br/>

<span data-ttu-id="8457e-2030">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2030">1</span></span>

<span data-ttu-id="8457e-2031">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2031">2</span></span>

<span data-ttu-id="8457e-2032">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2032">3</span></span>

<span data-ttu-id="8457e-2033">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2033">4</span></span>

<span data-ttu-id="8457e-2034">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2034">5</span></span>

<span data-ttu-id="8457e-2035">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2035">6</span></span>

<span data-ttu-id="8457e-2036">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2036">7</span></span>

<span data-ttu-id="8457e-2037">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2037">8</span></span>

<span data-ttu-id="8457e-2038">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2038">9</span></span>

<span data-ttu-id="8457e-2039">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2039">2</span></span><br/> <span data-ttu-id="8457e-2040">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2040">0</span></span><br/>

<span data-ttu-id="8457e-2041">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2041">1</span></span>

<span data-ttu-id="8457e-2042">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2042">2</span></span>

<span data-ttu-id="8457e-2043">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2043">3</span></span>

<span data-ttu-id="8457e-2044">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2044">4</span></span>

<span data-ttu-id="8457e-2045">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2045">5</span></span>

<span data-ttu-id="8457e-2046">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2046">6</span></span>

<span data-ttu-id="8457e-2047">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2047">7</span></span>

<span data-ttu-id="8457e-2048">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2048">8</span></span>

<span data-ttu-id="8457e-2049">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2049">9</span></span>

<span data-ttu-id="8457e-2050">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2050">3</span></span><br/> <span data-ttu-id="8457e-2051">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2051">0</span></span><br/>

<span data-ttu-id="8457e-2052">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2052">1</span></span>

<span data-ttu-id="8457e-2053">guidPropertySet</span><span class="sxs-lookup"><span data-stu-id="8457e-2053">guidPropertySet</span></span>

<span data-ttu-id="8457e-2054">...</span><span class="sxs-lookup"><span data-stu-id="8457e-2054">...</span></span>

<span data-ttu-id="8457e-2055">...</span><span class="sxs-lookup"><span data-stu-id="8457e-2055">...</span></span>

<span data-ttu-id="8457e-2056">...</span><span class="sxs-lookup"><span data-stu-id="8457e-2056">...</span></span>

<span data-ttu-id="8457e-2057">...</span><span class="sxs-lookup"><span data-stu-id="8457e-2057">...</span></span>

<span data-ttu-id="8457e-2058">\_padding (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-2058">\_padding (variable)</span></span>

<span data-ttu-id="8457e-2059">cProperties</span><span class="sxs-lookup"><span data-stu-id="8457e-2059">cProperties</span></span>

<span data-ttu-id="8457e-2060">aProps (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-2060">aProps (variable)</span></span>



 

<span data-ttu-id="8457e-2061">**guidPropertySet**: un GUID que identifica el conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="8457e-2061">**guidPropertySet**: A GUID identifying the property set.</span></span> <span data-ttu-id="8457e-2062">DEBE establecerse en el formato binario correspondiente a uno de los siguientes valores (se muestra en formato de representación de cadena), identificando el conjunto de propiedades de las propiedades contenidas en el campo aProps.</span><span class="sxs-lookup"><span data-stu-id="8457e-2062">MUST be set to the binary form corresponding to one of the following values (shown in string representation form), identifying the property set of the properties contained in the aProps field.</span></span>



| <span data-ttu-id="8457e-2063">Valor/GUID</span><span class="sxs-lookup"><span data-stu-id="8457e-2063">Value / GUID</span></span>                                                                              | <span data-ttu-id="8457e-2064">Nombre</span><span class="sxs-lookup"><span data-stu-id="8457e-2064">Name</span></span>                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="8457e-2065">DBPROPSET \_ FSCIFRMWRK \_ ext</span><span class="sxs-lookup"><span data-stu-id="8457e-2065">DBPROPSET\_FSCIFRMWRK\_EXT</span></span><br/> <span data-ttu-id="8457e-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span><span class="sxs-lookup"><span data-stu-id="8457e-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span></span><br/>   | <span data-ttu-id="8457e-2067">Conjunto de propiedades del marco de índice de contenido del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="8457e-2067">File System Content Index Framework Property Set</span></span> |
| <span data-ttu-id="8457e-2068">DBPROPSET \_ QUERYEXT</span><span class="sxs-lookup"><span data-stu-id="8457e-2068">DBPROPSET\_QUERYEXT</span></span><br/> <span data-ttu-id="8457e-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span><span class="sxs-lookup"><span data-stu-id="8457e-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span></span><br/>          | <span data-ttu-id="8457e-2070">Conjunto de propiedades de extensión de consulta</span><span class="sxs-lookup"><span data-stu-id="8457e-2070">Query Extension Property Set</span></span>                     |
| <span data-ttu-id="8457e-2071">DBPROPSET \_ CIFRMWRKCORE \_ ext</span><span class="sxs-lookup"><span data-stu-id="8457e-2071">DBPROPSET\_CIFRMWRKCORE\_EXT</span></span><br/> <span data-ttu-id="8457e-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span><span class="sxs-lookup"><span data-stu-id="8457e-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span></span><br/> | <span data-ttu-id="8457e-2073">Conjunto de propiedades Core de content index Framework</span><span class="sxs-lookup"><span data-stu-id="8457e-2073">Content Index Framework Core Property Set</span></span>        |



 

<span data-ttu-id="8457e-2074">**\_ padding**: este campo debe tener una longitud de 0 a 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="8457e-2074">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="8457e-2075">La longitud de este campo debe ser tal que el campo siguiente comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="8457e-2075">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="8457e-2076">Si este campo está presente (es decir, la longitud es distinto de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8457e-2076">If this field is present (i.e., length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="8457e-2077">El receptor debe omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="8457e-2077">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8457e-2078">**cProperties**: entero de 32 bits sin signo que contiene el número de elementos de la matriz de aProps.</span><span class="sxs-lookup"><span data-stu-id="8457e-2078">**cProperties**: A 32-bit unsigned integer containing the number of elements in the aProps array.</span></span>

<span data-ttu-id="8457e-2079">**aProps**: una matriz de estructuras CDbProp, como se especifica en la sección 0, que contiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="8457e-2079">**aProps**: An array of CDbProp structures, as specified in section 0, containing properties.</span></span> <span data-ttu-id="8457e-2080">Las estructuras de la matriz se deben separar entre 0 y 3 bytes de relleno, de modo que cada estructura comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta matriz.</span><span class="sxs-lookup"><span data-stu-id="8457e-2080">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="8457e-2081">Si los bytes de relleno están presentes, el valor que contienen es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8457e-2081">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="8457e-2082">El receptor debe omitir el contenido de los bytes de relleno.</span><span class="sxs-lookup"><span data-stu-id="8457e-2082">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="22123-cpidmapper"></a><span data-ttu-id="8457e-2083">2.2.1.23 CPidMapper</span><span class="sxs-lookup"><span data-stu-id="8457e-2083">2.2.1.23 CPidMapper</span></span>

<span data-ttu-id="8457e-2084">La estructura CPidMapper contiene una matriz de identificadores de propiedad que especifican las propiedades que se van a devolver en un conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-2084">The CPidMapper structure contains an array of property IDs specifying the properties to return in a rowset.</span></span>



<span data-ttu-id="8457e-2085">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2085">0</span></span>

<span data-ttu-id="8457e-2086">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2086">1</span></span>

<span data-ttu-id="8457e-2087">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2087">2</span></span>

<span data-ttu-id="8457e-2088">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2088">3</span></span>

<span data-ttu-id="8457e-2089">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2089">4</span></span>

<span data-ttu-id="8457e-2090">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2090">5</span></span>

<span data-ttu-id="8457e-2091">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2091">6</span></span>

<span data-ttu-id="8457e-2092">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2092">7</span></span>

<span data-ttu-id="8457e-2093">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2093">8</span></span>

<span data-ttu-id="8457e-2094">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2094">9</span></span>

<span data-ttu-id="8457e-2095">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2095">1</span></span><br/> <span data-ttu-id="8457e-2096">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2096">0</span></span><br/>

<span data-ttu-id="8457e-2097">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2097">1</span></span>

<span data-ttu-id="8457e-2098">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2098">2</span></span>

<span data-ttu-id="8457e-2099">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2099">3</span></span>

<span data-ttu-id="8457e-2100">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2100">4</span></span>

<span data-ttu-id="8457e-2101">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2101">5</span></span>

<span data-ttu-id="8457e-2102">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2102">6</span></span>

<span data-ttu-id="8457e-2103">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2103">7</span></span>

<span data-ttu-id="8457e-2104">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2104">8</span></span>

<span data-ttu-id="8457e-2105">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2105">9</span></span>

<span data-ttu-id="8457e-2106">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2106">2</span></span><br/> <span data-ttu-id="8457e-2107">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2107">0</span></span><br/>

<span data-ttu-id="8457e-2108">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2108">1</span></span>

<span data-ttu-id="8457e-2109">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2109">2</span></span>

<span data-ttu-id="8457e-2110">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2110">3</span></span>

<span data-ttu-id="8457e-2111">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2111">4</span></span>

<span data-ttu-id="8457e-2112">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2112">5</span></span>

<span data-ttu-id="8457e-2113">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2113">6</span></span>

<span data-ttu-id="8457e-2114">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2114">7</span></span>

<span data-ttu-id="8457e-2115">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2115">8</span></span>

<span data-ttu-id="8457e-2116">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2116">9</span></span>

<span data-ttu-id="8457e-2117">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2117">3</span></span><br/> <span data-ttu-id="8457e-2118">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2118">0</span></span><br/>

<span data-ttu-id="8457e-2119">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2119">1</span></span>

<span data-ttu-id="8457e-2120">count</span><span class="sxs-lookup"><span data-stu-id="8457e-2120">count</span></span>

<span data-ttu-id="8457e-2121">aPropSpec</span><span class="sxs-lookup"><span data-stu-id="8457e-2121">aPropSpec</span></span>

<span data-ttu-id="8457e-2122">... variable</span><span class="sxs-lookup"><span data-stu-id="8457e-2122">... (variable)</span></span>



 

<span data-ttu-id="8457e-2123">**Count**: entero de 32 bits sin signo que contiene el número de elementos de la matriz aPropSpec.</span><span class="sxs-lookup"><span data-stu-id="8457e-2123">**count**: A 32-bit unsigned integer containing the number of elements in the aPropSpec array.</span></span>

<span data-ttu-id="8457e-2124">**aPropSpec**: matriz de estructuras CFullPropSpec que indica las propiedades que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="8457e-2124">**aPropSpec**: Array of CFullPropSpec structures indicating the properties to return.</span></span> <span data-ttu-id="8457e-2125">Las estructuras de la matriz deben estar separadas entre 0 y 3 bytes de relleno, de modo que cada estructura tenga una alineación de 4 bytes desde el principio de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-2125">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="8457e-2126">Estos bytes de relleno pueden ser cualquier valor arbitrario y deben omitirse en la recepción.</span><span class="sxs-lookup"><span data-stu-id="8457e-2126">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22124-crowseekat"></a><span data-ttu-id="8457e-2127">2.2.1.24 CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="8457e-2127">2.2.1.24 CRowSeekAt</span></span>

<span data-ttu-id="8457e-2128">La estructura CRowSeekAt contiene el desplazamiento en el que se recuperan las filas de un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-2128">The CRowSeekAt structure contains the offset at which to retrieve rows in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="8457e-2129">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2129">0</span></span>

<span data-ttu-id="8457e-2130">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2130">1</span></span>

<span data-ttu-id="8457e-2131">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2131">2</span></span>

<span data-ttu-id="8457e-2132">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2132">3</span></span>

<span data-ttu-id="8457e-2133">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2133">4</span></span>

<span data-ttu-id="8457e-2134">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2134">5</span></span>

<span data-ttu-id="8457e-2135">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2135">6</span></span>

<span data-ttu-id="8457e-2136">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2136">7</span></span>

<span data-ttu-id="8457e-2137">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2137">8</span></span>

<span data-ttu-id="8457e-2138">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2138">9</span></span>

<span data-ttu-id="8457e-2139">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2139">1</span></span><br/> <span data-ttu-id="8457e-2140">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2140">0</span></span><br/>

<span data-ttu-id="8457e-2141">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2141">1</span></span>

<span data-ttu-id="8457e-2142">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2142">2</span></span>

<span data-ttu-id="8457e-2143">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2143">3</span></span>

<span data-ttu-id="8457e-2144">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2144">4</span></span>

<span data-ttu-id="8457e-2145">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2145">5</span></span>

<span data-ttu-id="8457e-2146">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2146">6</span></span>

<span data-ttu-id="8457e-2147">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2147">7</span></span>

<span data-ttu-id="8457e-2148">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2148">8</span></span>

<span data-ttu-id="8457e-2149">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2149">9</span></span>

<span data-ttu-id="8457e-2150">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2150">2</span></span><br/> <span data-ttu-id="8457e-2151">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2151">0</span></span><br/>

<span data-ttu-id="8457e-2152">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2152">1</span></span>

<span data-ttu-id="8457e-2153">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2153">2</span></span>

<span data-ttu-id="8457e-2154">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2154">3</span></span>

<span data-ttu-id="8457e-2155">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2155">4</span></span>

<span data-ttu-id="8457e-2156">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2156">5</span></span>

<span data-ttu-id="8457e-2157">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2157">6</span></span>

<span data-ttu-id="8457e-2158">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2158">7</span></span>

<span data-ttu-id="8457e-2159">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2159">8</span></span>

<span data-ttu-id="8457e-2160">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2160">9</span></span>

<span data-ttu-id="8457e-2161">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2161">3</span></span><br/> <span data-ttu-id="8457e-2162">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2162">0</span></span><br/>

<span data-ttu-id="8457e-2163">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2163">1</span></span>

<span data-ttu-id="8457e-2164">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="8457e-2164">\_hRegion</span></span>

<span data-ttu-id="8457e-2165">\_cskip</span><span class="sxs-lookup"><span data-stu-id="8457e-2165">\_cskip</span></span>

<span data-ttu-id="8457e-2166">\_bmkOffset</span><span class="sxs-lookup"><span data-stu-id="8457e-2166">\_bmkOffset</span></span>



 

<span data-ttu-id="8457e-2167">**\_ hRegion**: debe establecerse en 0x00000000 y debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="8457e-2167">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="8457e-2168">**\_ cskip**: entero de 32 bits sin signo que contiene el número de filas que se van a omitir en el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-2168">**\_cskip**: A 32-bit unsigned integer containing the number of rows to skip in the rowset.</span></span>

<span data-ttu-id="8457e-2169">**\_ bmkOffset**: un valor de 32 bits que representa el identificador del **marcador** que indica la posición inicial desde la que se omitirá el número de filas especificado en \_ cskip antes de comenzar la recuperación.</span><span class="sxs-lookup"><span data-stu-id="8457e-2169">**\_bmkOffset**: A 32-bit value representing the handle of the **bookmark** indicating the starting position from which to skip the number of rows specified in \_cskip, before beginning retrieval.</span></span>

### <a name="22125-crowseekatratio"></a><span data-ttu-id="8457e-2170">2.2.1.25 CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="8457e-2170">2.2.1.25 CRowSeekAtRatio</span></span>

<span data-ttu-id="8457e-2171">La estructura CRowSeekAtRatio identifica el punto en el que se va a iniciar la recuperación de un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-2171">The CRowSeekAtRatio structure identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="8457e-2172">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2172">0</span></span>

<span data-ttu-id="8457e-2173">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2173">1</span></span>

<span data-ttu-id="8457e-2174">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2174">2</span></span>

<span data-ttu-id="8457e-2175">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2175">3</span></span>

<span data-ttu-id="8457e-2176">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2176">4</span></span>

<span data-ttu-id="8457e-2177">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2177">5</span></span>

<span data-ttu-id="8457e-2178">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2178">6</span></span>

<span data-ttu-id="8457e-2179">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2179">7</span></span>

<span data-ttu-id="8457e-2180">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2180">8</span></span>

<span data-ttu-id="8457e-2181">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2181">9</span></span>

<span data-ttu-id="8457e-2182">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2182">1</span></span><br/> <span data-ttu-id="8457e-2183">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2183">0</span></span><br/>

<span data-ttu-id="8457e-2184">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2184">1</span></span>

<span data-ttu-id="8457e-2185">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2185">2</span></span>

<span data-ttu-id="8457e-2186">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2186">3</span></span>

<span data-ttu-id="8457e-2187">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2187">4</span></span>

<span data-ttu-id="8457e-2188">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2188">5</span></span>

<span data-ttu-id="8457e-2189">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2189">6</span></span>

<span data-ttu-id="8457e-2190">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2190">7</span></span>

<span data-ttu-id="8457e-2191">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2191">8</span></span>

<span data-ttu-id="8457e-2192">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2192">9</span></span>

<span data-ttu-id="8457e-2193">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2193">2</span></span><br/> <span data-ttu-id="8457e-2194">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2194">0</span></span><br/>

<span data-ttu-id="8457e-2195">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2195">1</span></span>

<span data-ttu-id="8457e-2196">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2196">2</span></span>

<span data-ttu-id="8457e-2197">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2197">3</span></span>

<span data-ttu-id="8457e-2198">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2198">4</span></span>

<span data-ttu-id="8457e-2199">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2199">5</span></span>

<span data-ttu-id="8457e-2200">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2200">6</span></span>

<span data-ttu-id="8457e-2201">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2201">7</span></span>

<span data-ttu-id="8457e-2202">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2202">8</span></span>

<span data-ttu-id="8457e-2203">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2203">9</span></span>

<span data-ttu-id="8457e-2204">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2204">3</span></span><br/> <span data-ttu-id="8457e-2205">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2205">0</span></span><br/>

<span data-ttu-id="8457e-2206">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2206">1</span></span>

<span data-ttu-id="8457e-2207">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="8457e-2207">CiTblChapt</span></span>

<span data-ttu-id="8457e-2208">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="8457e-2208">\_hRegion</span></span>

<span data-ttu-id="8457e-2209">\_ulNumerator</span><span class="sxs-lookup"><span data-stu-id="8457e-2209">\_ulNumerator</span></span>

<span data-ttu-id="8457e-2210">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="8457e-2210">\_ulDenominator</span></span>



 

<span data-ttu-id="8457e-2211">**CiTblChapt**: entero de 32 bits sin signo que indica el capítulo del conjunto de filas del que se van a recuperar filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-2211">**CiTblChapt**: A 32-bit unsigned integer indicating the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="8457e-2212">**\_ hRegion**: debe establecerse en 0x00000000 y debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="8457e-2212">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="8457e-2213">**\_ ulNumerator**: entero de 32 bits sin signo que representa el numerador de la proporción de filas del capítulo en la que se va a comenzar la recuperación.</span><span class="sxs-lookup"><span data-stu-id="8457e-2213">**\_ulNumerator**: Unsigned 32-bit integer representing the numerator of the ratio of rows in the chapter at which to begin retrieval.</span></span>

<span data-ttu-id="8457e-2214">**\_ ulDenominator**: entero de 32 bits sin signo que representa el denominador de la proporción de filas del capítulo en la que se va a comenzar la recuperación.</span><span class="sxs-lookup"><span data-stu-id="8457e-2214">**\_ulDenominator**: Unsigned 32-bit integer representing the denominator of the ratio of rows in the chapter at which to begin retrieval.</span></span> <span data-ttu-id="8457e-2215">DEBE ser mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="8457e-2215">MUST be greater than zero.</span></span>

### <a name="22126-crowseekbybookmark"></a><span data-ttu-id="8457e-2216">2.2.1.26 CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="8457e-2216">2.2.1.26 CRowSeekByBookmark</span></span>

<span data-ttu-id="8457e-2217">La estructura CRowSeekByBookmark identifica los marcadores desde los que se van a empezar a recuperar filas para un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-2217">The CRowSeekByBookmark structure identifies the bookmarks from which to begin retrieving rows for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="8457e-2218">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2218">0</span></span>

<span data-ttu-id="8457e-2219">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2219">1</span></span>

<span data-ttu-id="8457e-2220">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2220">2</span></span>

<span data-ttu-id="8457e-2221">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2221">3</span></span>

<span data-ttu-id="8457e-2222">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2222">4</span></span>

<span data-ttu-id="8457e-2223">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2223">5</span></span>

<span data-ttu-id="8457e-2224">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2224">6</span></span>

<span data-ttu-id="8457e-2225">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2225">7</span></span>

<span data-ttu-id="8457e-2226">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2226">8</span></span>

<span data-ttu-id="8457e-2227">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2227">9</span></span>

<span data-ttu-id="8457e-2228">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2228">1</span></span><br/> <span data-ttu-id="8457e-2229">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2229">0</span></span><br/>

<span data-ttu-id="8457e-2230">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2230">1</span></span>

<span data-ttu-id="8457e-2231">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2231">2</span></span>

<span data-ttu-id="8457e-2232">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2232">3</span></span>

<span data-ttu-id="8457e-2233">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2233">4</span></span>

<span data-ttu-id="8457e-2234">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2234">5</span></span>

<span data-ttu-id="8457e-2235">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2235">6</span></span>

<span data-ttu-id="8457e-2236">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2236">7</span></span>

<span data-ttu-id="8457e-2237">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2237">8</span></span>

<span data-ttu-id="8457e-2238">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2238">9</span></span>

<span data-ttu-id="8457e-2239">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2239">2</span></span><br/> <span data-ttu-id="8457e-2240">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2240">0</span></span><br/>

<span data-ttu-id="8457e-2241">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2241">1</span></span>

<span data-ttu-id="8457e-2242">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2242">2</span></span>

<span data-ttu-id="8457e-2243">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2243">3</span></span>

<span data-ttu-id="8457e-2244">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2244">4</span></span>

<span data-ttu-id="8457e-2245">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2245">5</span></span>

<span data-ttu-id="8457e-2246">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2246">6</span></span>

<span data-ttu-id="8457e-2247">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2247">7</span></span>

<span data-ttu-id="8457e-2248">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2248">8</span></span>

<span data-ttu-id="8457e-2249">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2249">9</span></span>

<span data-ttu-id="8457e-2250">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2250">3</span></span><br/> <span data-ttu-id="8457e-2251">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2251">0</span></span><br/>

<span data-ttu-id="8457e-2252">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2252">1</span></span>

<span data-ttu-id="8457e-2253">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="8457e-2253">\_hRegion</span></span>

<span data-ttu-id="8457e-2254">\_cBookmarks</span><span class="sxs-lookup"><span data-stu-id="8457e-2254">\_cBookmarks</span></span>

<span data-ttu-id="8457e-2255">\_maxRet</span><span class="sxs-lookup"><span data-stu-id="8457e-2255">\_maxRet</span></span>

<span data-ttu-id="8457e-2256">\_cValidRet</span><span class="sxs-lookup"><span data-stu-id="8457e-2256">\_cValidRet</span></span>

<span data-ttu-id="8457e-2257">\_aBookmarks (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-2257">\_aBookmarks (variable)</span></span>

<span data-ttu-id="8457e-2258">\_ascRet (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-2258">\_ascRet (variable)</span></span>



 

<span data-ttu-id="8457e-2259">**\_ hRegion**: debe establecerse en 0x00000000 y debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="8457e-2259">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="8457e-2260">**\_ cBookmarks**: entero de 32 bits sin signo que representa el número de elementos de la \_ matriz de aBookmarks.</span><span class="sxs-lookup"><span data-stu-id="8457e-2260">**\_cBookmarks**: Unsigned 32-bit integer representing the number of elements in \_aBookmarks array.</span></span>

<span data-ttu-id="8457e-2261">**\_ maxRet**: entero de 32 bits sin signo que representa el número de elementos de la \_ matriz de ascRet.</span><span class="sxs-lookup"><span data-stu-id="8457e-2261">**\_maxRet**: Unsigned 32-bit integer representing the number of elements in \_ascRet array.</span></span>

<span data-ttu-id="8457e-2262">**\_ cValidRet**: entero de 32 bits sin signo que representa el número de elementos de la \_ matriz ascRet que son válidos.</span><span class="sxs-lookup"><span data-stu-id="8457e-2262">**\_cValidRet**: Unsigned 32-bit integer representing the number of elements in the \_ascRet array which are valid.</span></span> <span data-ttu-id="8457e-2263">Los elementos válidos se han definido en la matriz, mientras que los elementos no válidos no están definidos.</span><span class="sxs-lookup"><span data-stu-id="8457e-2263">Valid elements have been defined in the array, while invalid elements are undefined.</span></span>

<span data-ttu-id="8457e-2264">**\_ aBookmarks**: una matriz de identificadores de marcador (cada uno representado por 4 bytes), tal y como se obtiene de un mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-2264">**\_aBookmarks**: An array of bookmark handles (each represented by 4 bytes), as obtained from a CPMGetRowsOut message.</span></span>

<span data-ttu-id="8457e-2265">**\_ ascRet**: una matriz de Valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="8457e-2265">**\_ascRet**: An array of HRESULT values.</span></span> <span data-ttu-id="8457e-2266">Cuando CRowSeekByBookMark se envía como parte de la solicitud CPMGetRowsIn, el número de entradas de la matriz debe ser igual a \_ cBookMarks.</span><span class="sxs-lookup"><span data-stu-id="8457e-2266">When the CRowSeekByBookMark is sent as part of the CPMGetRowsIn request, the number of entries in the array MUST be equal to \_cBookMarks.</span></span> <span data-ttu-id="8457e-2267">Cuando lo envía el cliente, los valores deben establecerse en cero y el servidor debe omitir el contenido de la matriz.</span><span class="sxs-lookup"><span data-stu-id="8457e-2267">When sent by the client, the values MUST be set zero, and the server MUST ignore the contents of the array.</span></span> <span data-ttu-id="8457e-2268">Cuando lo envía el servidor (como parte del mensaje CPMGetRowsOut), los valores de la matriz indican el estado del resultado para cada recuperación de fila.</span><span class="sxs-lookup"><span data-stu-id="8457e-2268">When sent by the server (as part of the CPMGetRowsOut message), the values in the array indicate the result status for each row retrieval.</span></span>

### <a name="22127-crowseeknext"></a><span data-ttu-id="8457e-2269">2.2.1.27 CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="8457e-2269">2.2.1.27 CRowSeekNext</span></span>

<span data-ttu-id="8457e-2270">La estructura CRowSeekNext contiene el número de filas que se van a omitir en un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-2270">The CRowSeekNext structure contains the number of rows to skip in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="8457e-2271">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2271">0</span></span>

<span data-ttu-id="8457e-2272">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2272">1</span></span>

<span data-ttu-id="8457e-2273">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2273">2</span></span>

<span data-ttu-id="8457e-2274">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2274">3</span></span>

<span data-ttu-id="8457e-2275">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2275">4</span></span>

<span data-ttu-id="8457e-2276">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2276">5</span></span>

<span data-ttu-id="8457e-2277">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2277">6</span></span>

<span data-ttu-id="8457e-2278">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2278">7</span></span>

<span data-ttu-id="8457e-2279">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2279">8</span></span>

<span data-ttu-id="8457e-2280">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2280">9</span></span>

<span data-ttu-id="8457e-2281">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2281">1</span></span><br/> <span data-ttu-id="8457e-2282">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2282">0</span></span><br/>

<span data-ttu-id="8457e-2283">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2283">1</span></span>

<span data-ttu-id="8457e-2284">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2284">2</span></span>

<span data-ttu-id="8457e-2285">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2285">3</span></span>

<span data-ttu-id="8457e-2286">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2286">4</span></span>

<span data-ttu-id="8457e-2287">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2287">5</span></span>

<span data-ttu-id="8457e-2288">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2288">6</span></span>

<span data-ttu-id="8457e-2289">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2289">7</span></span>

<span data-ttu-id="8457e-2290">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2290">8</span></span>

<span data-ttu-id="8457e-2291">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2291">9</span></span>

<span data-ttu-id="8457e-2292">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2292">2</span></span><br/> <span data-ttu-id="8457e-2293">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2293">0</span></span><br/>

<span data-ttu-id="8457e-2294">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2294">1</span></span>

<span data-ttu-id="8457e-2295">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2295">2</span></span>

<span data-ttu-id="8457e-2296">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2296">3</span></span>

<span data-ttu-id="8457e-2297">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2297">4</span></span>

<span data-ttu-id="8457e-2298">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2298">5</span></span>

<span data-ttu-id="8457e-2299">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2299">6</span></span>

<span data-ttu-id="8457e-2300">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2300">7</span></span>

<span data-ttu-id="8457e-2301">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2301">8</span></span>

<span data-ttu-id="8457e-2302">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2302">9</span></span>

<span data-ttu-id="8457e-2303">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2303">3</span></span><br/> <span data-ttu-id="8457e-2304">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2304">0</span></span><br/>

<span data-ttu-id="8457e-2305">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2305">1</span></span>

<span data-ttu-id="8457e-2306">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="8457e-2306">CiTblChapt</span></span>

<span data-ttu-id="8457e-2307">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="8457e-2307">\_hRegion</span></span>

<span data-ttu-id="8457e-2308">\_cskip</span><span class="sxs-lookup"><span data-stu-id="8457e-2308">\_cskip</span></span>



 

<span data-ttu-id="8457e-2309">**CiTblChapt**: entero de 32 bits sin signo que especifica el capítulo del conjunto de filas del que se van a recuperar filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-2309">**CiTblChapt**: Unsigned 32-bit integer specifying the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="8457e-2310">**\_ hRegion**: debe establecerse en 0x00000000 y debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="8457e-2310">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="8457e-2311">**\_ cskip**: entero de 32 bits sin signo que representa el número de filas que se van a omitir en el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-2311">**\_cskip**: Unsigned 32-bit integer representing the number of rows to skip in the rowset.</span></span>

### <a name="22128-crowsetproperties"></a><span data-ttu-id="8457e-2312">2.2.1.28 CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="8457e-2312">2.2.1.28 CRowsetProperties</span></span>

<span data-ttu-id="8457e-2313">La estructura CRowsetProperties contiene información de configuración de una consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-2313">The CRowsetProperties structure contains configuration information for a query.</span></span>



<span data-ttu-id="8457e-2314">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2314">0</span></span>

<span data-ttu-id="8457e-2315">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2315">1</span></span>

<span data-ttu-id="8457e-2316">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2316">2</span></span>

<span data-ttu-id="8457e-2317">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2317">3</span></span>

<span data-ttu-id="8457e-2318">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2318">4</span></span>

<span data-ttu-id="8457e-2319">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2319">5</span></span>

<span data-ttu-id="8457e-2320">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2320">6</span></span>

<span data-ttu-id="8457e-2321">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2321">7</span></span>

<span data-ttu-id="8457e-2322">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2322">8</span></span>

<span data-ttu-id="8457e-2323">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2323">9</span></span>

<span data-ttu-id="8457e-2324">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2324">1</span></span><br/> <span data-ttu-id="8457e-2325">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2325">0</span></span><br/>

<span data-ttu-id="8457e-2326">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2326">1</span></span>

<span data-ttu-id="8457e-2327">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2327">2</span></span>

<span data-ttu-id="8457e-2328">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2328">3</span></span>

<span data-ttu-id="8457e-2329">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2329">4</span></span>

<span data-ttu-id="8457e-2330">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2330">5</span></span>

<span data-ttu-id="8457e-2331">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2331">6</span></span>

<span data-ttu-id="8457e-2332">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2332">7</span></span>

<span data-ttu-id="8457e-2333">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2333">8</span></span>

<span data-ttu-id="8457e-2334">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2334">9</span></span>

<span data-ttu-id="8457e-2335">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2335">2</span></span><br/> <span data-ttu-id="8457e-2336">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2336">0</span></span><br/>

<span data-ttu-id="8457e-2337">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2337">1</span></span>

<span data-ttu-id="8457e-2338">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2338">2</span></span>

<span data-ttu-id="8457e-2339">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2339">3</span></span>

<span data-ttu-id="8457e-2340">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2340">4</span></span>

<span data-ttu-id="8457e-2341">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2341">5</span></span>

<span data-ttu-id="8457e-2342">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2342">6</span></span>

<span data-ttu-id="8457e-2343">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2343">7</span></span>

<span data-ttu-id="8457e-2344">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2344">8</span></span>

<span data-ttu-id="8457e-2345">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2345">9</span></span>

<span data-ttu-id="8457e-2346">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2346">3</span></span><br/> <span data-ttu-id="8457e-2347">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2347">0</span></span><br/>

<span data-ttu-id="8457e-2348">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2348">1</span></span>

<span data-ttu-id="8457e-2349">\_uBooleanOptions</span><span class="sxs-lookup"><span data-stu-id="8457e-2349">\_uBooleanOptions</span></span>

<span data-ttu-id="8457e-2350">\_ulMaxOpenRows</span><span class="sxs-lookup"><span data-stu-id="8457e-2350">\_ulMaxOpenRows</span></span>

<span data-ttu-id="8457e-2351">\_ulMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="8457e-2351">\_ulMemoryUsage</span></span>

<span data-ttu-id="8457e-2352">\_cMaxResults</span><span class="sxs-lookup"><span data-stu-id="8457e-2352">\_cMaxResults</span></span>

<span data-ttu-id="8457e-2353">\_cCmdTimeout</span><span class="sxs-lookup"><span data-stu-id="8457e-2353">\_cCmdTimeout</span></span>



 

<span data-ttu-id="8457e-2354">**\_ uBooleanOptions**: los 3 bits menos significativos de este campo deben contener uno de los tres valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="8457e-2354">**\_uBooleanOptions**: The least significant 3 bits of this field MUST contain one of the following three values:</span></span>



| <span data-ttu-id="8457e-2355">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-2355">Value</span></span>                  | <span data-ttu-id="8457e-2356">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-2356">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8457e-2357">eSequential 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-2357">eSequential 0x00000001</span></span> | <span data-ttu-id="8457e-2358">El cursor solo se puede transferir hacia delante.</span><span class="sxs-lookup"><span data-stu-id="8457e-2358">The cursor can only be moved forwards.</span></span>                              |
| <span data-ttu-id="8457e-2359">eLocatable 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8457e-2359">eLocatable 0x00000003</span></span>  | <span data-ttu-id="8457e-2360">El cursor se puede mover a cualquier posición.</span><span class="sxs-lookup"><span data-stu-id="8457e-2360">The cursor can be moved to any position.</span></span>                            |
| <span data-ttu-id="8457e-2361">eScrollable 0x00000007</span><span class="sxs-lookup"><span data-stu-id="8457e-2361">eScrollable 0x00000007</span></span> | <span data-ttu-id="8457e-2362">El cursor se puede mover a cualquier posición y captura en cualquier dirección.</span><span class="sxs-lookup"><span data-stu-id="8457e-2362">The cursor can be moved to any position and fetch in any direction.</span></span> |



 

<span data-ttu-id="8457e-2363">Los bits restantes pueden estar claros o establecerse en cualquier combinación de los siguientes valores lógicamente o juntos:</span><span class="sxs-lookup"><span data-stu-id="8457e-2363">The remaining bits may either be clear, or set to any combination of the following values logically OR'd together:</span></span>



| <span data-ttu-id="8457e-2364">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-2364">Value</span></span>                     | <span data-ttu-id="8457e-2365">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-2365">Meaning</span></span>                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-2366">eAsynchronous 0x00000008</span><span class="sxs-lookup"><span data-stu-id="8457e-2366">eAsynchronous 0x00000008</span></span>  | <span data-ttu-id="8457e-2367">El cliente no esperará a que se complete la ejecución.</span><span class="sxs-lookup"><span data-stu-id="8457e-2367">The client will not wait for execution completion.</span></span>                                                          |
| <span data-ttu-id="8457e-2368">eFirstRows 0x00000080</span><span class="sxs-lookup"><span data-stu-id="8457e-2368">eFirstRows 0x00000080</span></span>     | <span data-ttu-id="8457e-2369">Devuelve las primeras filas encontradas, no las mejores coincidencias.</span><span class="sxs-lookup"><span data-stu-id="8457e-2369">Return the first rows encountered, not the best matches.</span></span>                                                    |
| <span data-ttu-id="8457e-2370">eHoldRows 0x00000200</span><span class="sxs-lookup"><span data-stu-id="8457e-2370">eHoldRows 0x00000200</span></span>      | <span data-ttu-id="8457e-2371">El servidor no debe descartar las filas hasta que el cliente haya terminado de realizar una consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-2371">The server MUST NOT discard rows until the client is done with a query.</span></span>                                     |
| <span data-ttu-id="8457e-2372">eChaptered 0x00000800</span><span class="sxs-lookup"><span data-stu-id="8457e-2372">eChaptered 0x00000800</span></span>     | <span data-ttu-id="8457e-2373">El conjunto de filas admite capítulos.</span><span class="sxs-lookup"><span data-stu-id="8457e-2373">The rowset supports chapters.</span></span>                                                                               |
| <span data-ttu-id="8457e-2374">eUseCI 0x00001000</span><span class="sxs-lookup"><span data-stu-id="8457e-2374">eUseCI 0x00001000</span></span>         | <span data-ttu-id="8457e-2375">Solo responde a la consulta del índice, no del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="8457e-2375">Only answer the query from the index, not the file system.</span></span>                                                  |
| <span data-ttu-id="8457e-2376">eDeferTrimming 0x00002000</span><span class="sxs-lookup"><span data-stu-id="8457e-2376">eDeferTrimming 0x00002000</span></span> | <span data-ttu-id="8457e-2377">El servicio de Index Server es la posibilidad de optimizar el tiempo de respuesta al cliente al realizar la eliminación de los resultados.</span><span class="sxs-lookup"><span data-stu-id="8457e-2377">The indexing service is to consider optimizing response time to the client when performing results removal.</span></span> |



 

<span data-ttu-id="8457e-2378">**\_ ulMaxOpenRows**: entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-2378">**\_ulMaxOpenRows**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="8457e-2379">Debe establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-2379">Must be set to 0x00000000.</span></span> <span data-ttu-id="8457e-2380">No se utiliza y se debe omitir.</span><span class="sxs-lookup"><span data-stu-id="8457e-2380">Not used and MUST be ignored.</span></span>

<span data-ttu-id="8457e-2381">**\_ ulMemoryUsage**: entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-2381">**\_ulMemoryUsage**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="8457e-2382">Debe establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-2382">Must be set to 0x00000000.</span></span> <span data-ttu-id="8457e-2383">No se utiliza y se debe omitir.</span><span class="sxs-lookup"><span data-stu-id="8457e-2383">Not used and MUST be ignored.</span></span>

<span data-ttu-id="8457e-2384">**\_ cMaxResults**: entero de 32 bits sin signo que especifica el número máximo de filas que se van a devolver para la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-2384">**\_cMaxResults**: A 32-bit unsigned integer specifying the maximum number of rows that are to be returned for the query.</span></span>

<span data-ttu-id="8457e-2385">**\_ cCmdTimeout**: un entero de 32 bits sin signo, que especifica el número de segundos durante los que se agotará el tiempo de espera de una consulta y se terminará automáticamente, contando desde el momento en que se inicia la ejecución de la consulta en el servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-2385">**\_cCmdTimeout**: A 32-bit unsigned integer, specifying the number of seconds at which a query is to time out and automatically terminate, counting from the time the query starts executing on the server.</span></span> <span data-ttu-id="8457e-2386">Un valor de 0x00000000 significa que no se agotará el tiempo de espera de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-2386">A value of 0x00000000 means that the query is not to time out.</span></span>

### <a name="22129-crowvariant"></a><span data-ttu-id="8457e-2387">2.2.1.29 CRowVariant</span><span class="sxs-lookup"><span data-stu-id="8457e-2387">2.2.1.29 CRowVariant</span></span>

<span data-ttu-id="8457e-2388">La estructura CRowVariant contiene la parte de tamaño fijo de un tipo de datos de longitud variable almacenado en el mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-2388">The CRowVariant structure contains the fixed-size portion of a variable length data type stored in the CPMGetRowsOut message.</span></span>



<span data-ttu-id="8457e-2389">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2389">0</span></span>

<span data-ttu-id="8457e-2390">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2390">1</span></span>

<span data-ttu-id="8457e-2391">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2391">2</span></span>

<span data-ttu-id="8457e-2392">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2392">3</span></span>

<span data-ttu-id="8457e-2393">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2393">4</span></span>

<span data-ttu-id="8457e-2394">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2394">5</span></span>

<span data-ttu-id="8457e-2395">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2395">6</span></span>

<span data-ttu-id="8457e-2396">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2396">7</span></span>

<span data-ttu-id="8457e-2397">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2397">8</span></span>

<span data-ttu-id="8457e-2398">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2398">9</span></span>

<span data-ttu-id="8457e-2399">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2399">1</span></span><br/> <span data-ttu-id="8457e-2400">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2400">0</span></span><br/>

<span data-ttu-id="8457e-2401">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2401">1</span></span>

<span data-ttu-id="8457e-2402">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2402">2</span></span>

<span data-ttu-id="8457e-2403">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2403">3</span></span>

<span data-ttu-id="8457e-2404">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2404">4</span></span>

<span data-ttu-id="8457e-2405">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2405">5</span></span>

<span data-ttu-id="8457e-2406">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2406">6</span></span>

<span data-ttu-id="8457e-2407">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2407">7</span></span>

<span data-ttu-id="8457e-2408">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2408">8</span></span>

<span data-ttu-id="8457e-2409">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2409">9</span></span>

<span data-ttu-id="8457e-2410">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2410">2</span></span><br/> <span data-ttu-id="8457e-2411">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2411">0</span></span><br/>

<span data-ttu-id="8457e-2412">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2412">1</span></span>

<span data-ttu-id="8457e-2413">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2413">2</span></span>

<span data-ttu-id="8457e-2414">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2414">3</span></span>

<span data-ttu-id="8457e-2415">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2415">4</span></span>

<span data-ttu-id="8457e-2416">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2416">5</span></span>

<span data-ttu-id="8457e-2417">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2417">6</span></span>

<span data-ttu-id="8457e-2418">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2418">7</span></span>

<span data-ttu-id="8457e-2419">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2419">8</span></span>

<span data-ttu-id="8457e-2420">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2420">9</span></span>

<span data-ttu-id="8457e-2421">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2421">3</span></span><br/> <span data-ttu-id="8457e-2422">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2422">0</span></span><br/>

<span data-ttu-id="8457e-2423">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2423">1</span></span>

<span data-ttu-id="8457e-2424">vType</span><span class="sxs-lookup"><span data-stu-id="8457e-2424">vType</span></span>

<span data-ttu-id="8457e-2425">reserved1</span><span class="sxs-lookup"><span data-stu-id="8457e-2425">reserved1</span></span>

<span data-ttu-id="8457e-2426">reserved2</span><span class="sxs-lookup"><span data-stu-id="8457e-2426">reserved2</span></span>

<span data-ttu-id="8457e-2427">Desplazamiento (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-2427">Offset (optional)</span></span>



 

<span data-ttu-id="8457e-2428">**vType**: un indicador de tipo que indica el tipo de vValue.</span><span class="sxs-lookup"><span data-stu-id="8457e-2428">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="8457e-2429">DEBE ser uno de los valores de VARENUM especificados en la sección 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="8457e-2429">It MUST be one of the VARENUM values specified in section 2.2.1.1.</span></span>

<span data-ttu-id="8457e-2430">**reserved1**: no se usa.</span><span class="sxs-lookup"><span data-stu-id="8457e-2430">**reserved1**: Not used.</span></span> <span data-ttu-id="8457e-2431">El valor se puede establecer en cualquier valor arbitrario y debe omitirse en la recepción.</span><span class="sxs-lookup"><span data-stu-id="8457e-2431">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="8457e-2432">**reserved2**: no se usa.</span><span class="sxs-lookup"><span data-stu-id="8457e-2432">**reserved2**: Not used.</span></span> <span data-ttu-id="8457e-2433">El valor se puede establecer en cualquier valor arbitrario y debe omitirse en la recepción.</span><span class="sxs-lookup"><span data-stu-id="8457e-2433">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="8457e-2434">**Offset**: desplazamiento de datos de longitud variable (por ejemplo, una cadena).</span><span class="sxs-lookup"><span data-stu-id="8457e-2434">**Offset**: An offset to variable length data (e.g. a string).</span></span>  <span data-ttu-id="8457e-2435">DEBE ser un valor de 32 bits (longitud de 4 bytes) si se usan desplazamientos de 32 bits (según las reglas de la sección 2.2.3.16) o un valor de 64 bytes (8 bytes de longitud) si se usan desplazamientos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8457e-2435">This MUST be a 32-bit value (4 bytes long) if 32-bit offsets are being used (per the rules in section 2.2.3.16), or a 64-byte value (8 bytes long) if 64-bit offsets are being used.</span></span>

### <a name="22130-csortset"></a><span data-ttu-id="8457e-2436">2.2.1.30 CSortSet</span><span class="sxs-lookup"><span data-stu-id="8457e-2436">2.2.1.30 CSortSet</span></span>

<span data-ttu-id="8457e-2437">La estructura CSortSet contiene el criterio de ordenación de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-2437">The CSortSet structure contains the sort order of the query.</span></span>



<span data-ttu-id="8457e-2438">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2438">0</span></span>

<span data-ttu-id="8457e-2439">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2439">1</span></span>

<span data-ttu-id="8457e-2440">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2440">2</span></span>

<span data-ttu-id="8457e-2441">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2441">3</span></span>

<span data-ttu-id="8457e-2442">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2442">4</span></span>

<span data-ttu-id="8457e-2443">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2443">5</span></span>

<span data-ttu-id="8457e-2444">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2444">6</span></span>

<span data-ttu-id="8457e-2445">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2445">7</span></span>

<span data-ttu-id="8457e-2446">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2446">8</span></span>

<span data-ttu-id="8457e-2447">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2447">9</span></span>

<span data-ttu-id="8457e-2448">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2448">1</span></span><br/> <span data-ttu-id="8457e-2449">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2449">0</span></span><br/>

<span data-ttu-id="8457e-2450">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2450">1</span></span>

<span data-ttu-id="8457e-2451">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2451">2</span></span>

<span data-ttu-id="8457e-2452">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2452">3</span></span>

<span data-ttu-id="8457e-2453">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2453">4</span></span>

<span data-ttu-id="8457e-2454">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2454">5</span></span>

<span data-ttu-id="8457e-2455">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2455">6</span></span>

<span data-ttu-id="8457e-2456">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2456">7</span></span>

<span data-ttu-id="8457e-2457">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2457">8</span></span>

<span data-ttu-id="8457e-2458">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2458">9</span></span>

<span data-ttu-id="8457e-2459">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2459">2</span></span><br/> <span data-ttu-id="8457e-2460">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2460">0</span></span><br/>

<span data-ttu-id="8457e-2461">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2461">1</span></span>

<span data-ttu-id="8457e-2462">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2462">2</span></span>

<span data-ttu-id="8457e-2463">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2463">3</span></span>

<span data-ttu-id="8457e-2464">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2464">4</span></span>

<span data-ttu-id="8457e-2465">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2465">5</span></span>

<span data-ttu-id="8457e-2466">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2466">6</span></span>

<span data-ttu-id="8457e-2467">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2467">7</span></span>

<span data-ttu-id="8457e-2468">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2468">8</span></span>

<span data-ttu-id="8457e-2469">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2469">9</span></span>

<span data-ttu-id="8457e-2470">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2470">3</span></span><br/> <span data-ttu-id="8457e-2471">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2471">0</span></span><br/>

<span data-ttu-id="8457e-2472">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2472">1</span></span>

<span data-ttu-id="8457e-2473">Count</span><span class="sxs-lookup"><span data-stu-id="8457e-2473">Count</span></span>

<span data-ttu-id="8457e-2474">sortArray (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-2474">sortArray (variable)</span></span>



 

<span data-ttu-id="8457e-2475">**Count**: entero de 32 bits sin signo que especifica el número de elementos de sortArray.</span><span class="sxs-lookup"><span data-stu-id="8457e-2475">**count**: A 32-bit unsigned integer specifying number of elements in sortArray.</span></span>

<span data-ttu-id="8457e-2476">**sortArray**: una matriz de estructuras CSort que describe el orden en el que se ordenan los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-2476">**sortArray**: An array of CSort structures describing the order in which to sort the results of the query.</span></span> <span data-ttu-id="8457e-2477">Las estructuras de la matriz deben estar separadas entre 0 y 3 bytes de relleno, de modo que cada estructura tenga una alineación de 4 bytes desde el principio de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-2477">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="8457e-2478">Estos bytes de relleno pueden ser cualquier valor arbitrario y deben omitirse en la recepción.</span><span class="sxs-lookup"><span data-stu-id="8457e-2478">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22131-ctablecolumn"></a><span data-ttu-id="8457e-2479">2.2.1.31 CTableColumn</span><span class="sxs-lookup"><span data-stu-id="8457e-2479">2.2.1.31 CTableColumn</span></span>

<span data-ttu-id="8457e-2480">La estructura CTableColumn contiene una columna de un mensaje CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="8457e-2480">The CTableColumn structure contains a column of a CPMSetBindingsIn message</span></span>



<span data-ttu-id="8457e-2481">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2481">0</span></span>

<span data-ttu-id="8457e-2482">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2482">1</span></span>

<span data-ttu-id="8457e-2483">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2483">2</span></span>

<span data-ttu-id="8457e-2484">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2484">3</span></span>

<span data-ttu-id="8457e-2485">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2485">4</span></span>

<span data-ttu-id="8457e-2486">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2486">5</span></span>

<span data-ttu-id="8457e-2487">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2487">6</span></span>

<span data-ttu-id="8457e-2488">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2488">7</span></span>

<span data-ttu-id="8457e-2489">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2489">8</span></span>

<span data-ttu-id="8457e-2490">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2490">9</span></span>

<span data-ttu-id="8457e-2491">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2491">1</span></span><br/> <span data-ttu-id="8457e-2492">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2492">0</span></span><br/>

<span data-ttu-id="8457e-2493">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2493">1</span></span>

<span data-ttu-id="8457e-2494">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2494">2</span></span>

<span data-ttu-id="8457e-2495">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2495">3</span></span>

<span data-ttu-id="8457e-2496">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2496">4</span></span>

<span data-ttu-id="8457e-2497">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2497">5</span></span>

<span data-ttu-id="8457e-2498">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2498">6</span></span>

<span data-ttu-id="8457e-2499">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2499">7</span></span>

<span data-ttu-id="8457e-2500">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2500">8</span></span>

<span data-ttu-id="8457e-2501">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2501">9</span></span>

<span data-ttu-id="8457e-2502">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2502">2</span></span><br/> <span data-ttu-id="8457e-2503">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2503">0</span></span><br/>

<span data-ttu-id="8457e-2504">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2504">1</span></span>

<span data-ttu-id="8457e-2505">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2505">2</span></span>

<span data-ttu-id="8457e-2506">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2506">3</span></span>

<span data-ttu-id="8457e-2507">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2507">4</span></span>

<span data-ttu-id="8457e-2508">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2508">5</span></span>

<span data-ttu-id="8457e-2509">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2509">6</span></span>

<span data-ttu-id="8457e-2510">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2510">7</span></span>

<span data-ttu-id="8457e-2511">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2511">8</span></span>

<span data-ttu-id="8457e-2512">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2512">9</span></span>

<span data-ttu-id="8457e-2513">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2513">3</span></span><br/> <span data-ttu-id="8457e-2514">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2514">0</span></span><br/>

<span data-ttu-id="8457e-2515">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2515">1</span></span>

<span data-ttu-id="8457e-2516">PropSpec</span><span class="sxs-lookup"><span data-stu-id="8457e-2516">PropSpec</span></span>

<span data-ttu-id="8457e-2517">... variable</span><span class="sxs-lookup"><span data-stu-id="8457e-2517">...(variable)</span></span>

<span data-ttu-id="8457e-2518">vType</span><span class="sxs-lookup"><span data-stu-id="8457e-2518">vType</span></span>

<span data-ttu-id="8457e-2519">ValueUsed</span><span class="sxs-lookup"><span data-stu-id="8457e-2519">ValueUsed</span></span>

<span data-ttu-id="8457e-2520">\_padding1 (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-2520">\_padding1 (optional)</span></span>

<span data-ttu-id="8457e-2521">ValueOffset (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-2521">ValueOffset (optional)</span></span>

<span data-ttu-id="8457e-2522">Valuen (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-2522">ValueSize (optional)</span></span>

<span data-ttu-id="8457e-2523">StatusUsed</span><span class="sxs-lookup"><span data-stu-id="8457e-2523">StatusUsed</span></span>

<span data-ttu-id="8457e-2524">\_padding2 (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-2524">\_padding2 (optional)</span></span>

<span data-ttu-id="8457e-2525">StatusOffset (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-2525">StatusOffset (optional)</span></span>

<span data-ttu-id="8457e-2526">LengthUsed</span><span class="sxs-lookup"><span data-stu-id="8457e-2526">LengthUsed</span></span>

<span data-ttu-id="8457e-2527">\_padding3 (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-2527">\_padding3 (optional)</span></span>

<span data-ttu-id="8457e-2528">LengthOffset (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-2528">LengthOffset (optional)</span></span>



 

<span data-ttu-id="8457e-2529">**PropSpec**: una estructura CFullPropSpec tal como se especifica en la sección 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="8457e-2529">**PropSpec**: A CFullPropSpec structure as specified in Section 2.2.1.3.</span></span>

<span data-ttu-id="8457e-2530">**vType**: especifica el tipo de valor de datos contenido en la columna.</span><span class="sxs-lookup"><span data-stu-id="8457e-2530">**vType**: Specifies the type of data value contained in the column.</span></span> <span data-ttu-id="8457e-2531">Vea el campo vType de la sección 2.2.1.1 para obtener la lista de valores de este campo.</span><span class="sxs-lookup"><span data-stu-id="8457e-2531">See the vType field in Section 2.2.1.1 for the list of values for this field.</span></span>

<span data-ttu-id="8457e-2532">**ValueUsed**: un campo de un byte que debe establecerse en 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="8457e-2532">**ValueUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="8457e-2533">Si se establece en 0x01, la columna se transfiere dentro de la fila de tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="8457e-2533">If set to 0x01, the column is transferred within the fixed size row.</span></span> <span data-ttu-id="8457e-2534">Si se establece en 0x00, el valor de la columna se transfiere en la sección de longitud variable al final del búfer.</span><span class="sxs-lookup"><span data-stu-id="8457e-2534">If set to 0x00, the value of the column is transferred in the variable-length section at the end of the buffer.</span></span>

<span data-ttu-id="8457e-2535">**\_ padding1**: un campo de un byte que se debe insertar antes de ValueOffset si, sin él, ValueOffset no comenzará en un desplazamiento uniforme desde el principio del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-2535">**\_padding1**: A one byte field that MUST be inserted before ValueOffset if, without it, ValueOffset would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="8457e-2536">El valor de este byte es arbitrario y se debe omitir.</span><span class="sxs-lookup"><span data-stu-id="8457e-2536">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="8457e-2537">Si ValueUsed se establece en 0x00, este campo no debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-2537">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="8457e-2538">**ValueOffset**: entero de 2 bytes sin signo que especifica el desplazamiento del valor de la columna en la fila.</span><span class="sxs-lookup"><span data-stu-id="8457e-2538">**ValueOffset**: An unsigned 2-byte integer specifying the offset of the column value in the row.</span></span> <span data-ttu-id="8457e-2539">Si ValueUsed se establece en 0x00, este campo no debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-2539">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="8457e-2540">Sizeof **: entero** de 2 bytes sin signo que especifica el tamaño del valor de la columna en bytes.</span><span class="sxs-lookup"><span data-stu-id="8457e-2540">**ValueSize**: An unsigned 2-byte integer specifying the size of the column value in bytes.</span></span> <span data-ttu-id="8457e-2541">Si ValueUsed se establece en 0x00, este campo no debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-2541">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="8457e-2542">**StatusUsed**: un campo de un byte que debe establecerse en 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="8457e-2542">**StatusUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="8457e-2543">Si se establece en 0x01, el estado de la columna se transfiere dentro de la fila.</span><span class="sxs-lookup"><span data-stu-id="8457e-2543">If set to 0x01, the status of the column is transferred within the row.</span></span> <span data-ttu-id="8457e-2544">Si 0x00, el estado de la columna no se transfiere dentro de la fila.</span><span class="sxs-lookup"><span data-stu-id="8457e-2544">If 0x00, the status of the column is not transferred within the row.</span></span>

<span data-ttu-id="8457e-2545">**\_ padding2**: un campo de un byte que se debe insertar antes de StatusOffset si, sin él, el campo StatusOffset no comenzará en un desplazamiento uniforme desde el principio del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-2545">**\_padding2**: A one byte field that MUST be inserted before StatusOffset if, without it,the StatusOffset field would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="8457e-2546">El valor de este byte es arbitrario y se debe omitir.</span><span class="sxs-lookup"><span data-stu-id="8457e-2546">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="8457e-2547">Si StatusUsed se establece en 0x00, este campo no debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-2547">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="8457e-2548">**StatusOffset**: entero de 2 bytes sin signo que especifica el desplazamiento del estado de la columna en la fila.</span><span class="sxs-lookup"><span data-stu-id="8457e-2548">**StatusOffset**: An unsigned 2-byte integer specifying the offset of the column status in the row.</span></span> <span data-ttu-id="8457e-2549">Si StatusUsed se establece en 0x00, este campo no debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-2549">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="8457e-2550">**LengthUsed**: un campo de un byte que debe establecerse en 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="8457e-2550">**LengthUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="8457e-2551">Si se establece en 0x01, la longitud de la columna se transfiere dentro de la fila.</span><span class="sxs-lookup"><span data-stu-id="8457e-2551">If set to 0x01, the length of the column is transferred within the row.</span></span> <span data-ttu-id="8457e-2552">Si 0x00, no se debe transferir la longitud de la columna dentro de la fila.</span><span class="sxs-lookup"><span data-stu-id="8457e-2552">If 0x00, the length of the column MUST NOT be transferred within the row.</span></span>

<span data-ttu-id="8457e-2553">**\_ padding3**: un campo de un byte que se debe insertar antes de LengthOffset si, sin él, LengthOffset no comenzará en un desplazamiento uniforme desde el principio de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-2553">**\_padding3**: A one byte field which MUST be inserted before LengthOffset if, without it, LengthOffset would not begin at an even offset from the beginning of a message.</span></span> <span data-ttu-id="8457e-2554">El valor de este byte es arbitrario y se debe omitir.</span><span class="sxs-lookup"><span data-stu-id="8457e-2554">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="8457e-2555">Si LengthUsed se establece en 0x00, este campo no debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-2555">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="8457e-2556">**LengthOffset**: entero de 2 bytes sin signo que especifica el desplazamiento de la longitud de la columna en la fila.</span><span class="sxs-lookup"><span data-stu-id="8457e-2556">**LengthOffset**: An unsigned 2-byte integer specifying the offset of the column length in the row.</span></span> <span data-ttu-id="8457e-2557">Si LengthUsed se establece en 0x00, este campo no debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-2557">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

### <a name="22132-serializedpropertyvalue"></a><span data-ttu-id="8457e-2558">2.2.1.32 SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="8457e-2558">2.2.1.32 SERIALIZEDPROPERTYVALUE</span></span>

<span data-ttu-id="8457e-2559">La estructura SERIALIZEDPROPERTYVALUE contiene un valor serializado.</span><span class="sxs-lookup"><span data-stu-id="8457e-2559">The SERIALIZEDPROPERTYVALUE structure contains a serialized value.</span></span>



<span data-ttu-id="8457e-2560">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2560">0</span></span>

<span data-ttu-id="8457e-2561">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2561">1</span></span>

<span data-ttu-id="8457e-2562">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2562">2</span></span>

<span data-ttu-id="8457e-2563">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2563">3</span></span>

<span data-ttu-id="8457e-2564">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2564">4</span></span>

<span data-ttu-id="8457e-2565">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2565">5</span></span>

<span data-ttu-id="8457e-2566">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2566">6</span></span>

<span data-ttu-id="8457e-2567">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2567">7</span></span>

<span data-ttu-id="8457e-2568">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2568">8</span></span>

<span data-ttu-id="8457e-2569">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2569">9</span></span>

<span data-ttu-id="8457e-2570">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2570">1</span></span><br/> <span data-ttu-id="8457e-2571">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2571">0</span></span><br/>

<span data-ttu-id="8457e-2572">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2572">1</span></span>

<span data-ttu-id="8457e-2573">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2573">2</span></span>

<span data-ttu-id="8457e-2574">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2574">3</span></span>

<span data-ttu-id="8457e-2575">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2575">4</span></span>

<span data-ttu-id="8457e-2576">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2576">5</span></span>

<span data-ttu-id="8457e-2577">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2577">6</span></span>

<span data-ttu-id="8457e-2578">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2578">7</span></span>

<span data-ttu-id="8457e-2579">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2579">8</span></span>

<span data-ttu-id="8457e-2580">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2580">9</span></span>

<span data-ttu-id="8457e-2581">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2581">2</span></span><br/> <span data-ttu-id="8457e-2582">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2582">0</span></span><br/>

<span data-ttu-id="8457e-2583">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2583">1</span></span>

<span data-ttu-id="8457e-2584">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2584">2</span></span>

<span data-ttu-id="8457e-2585">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2585">3</span></span>

<span data-ttu-id="8457e-2586">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2586">4</span></span>

<span data-ttu-id="8457e-2587">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2587">5</span></span>

<span data-ttu-id="8457e-2588">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2588">6</span></span>

<span data-ttu-id="8457e-2589">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2589">7</span></span>

<span data-ttu-id="8457e-2590">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2590">8</span></span>

<span data-ttu-id="8457e-2591">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2591">9</span></span>

<span data-ttu-id="8457e-2592">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2592">3</span></span><br/> <span data-ttu-id="8457e-2593">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2593">0</span></span><br/>

<span data-ttu-id="8457e-2594">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2594">1</span></span>

<span data-ttu-id="8457e-2595">dwType</span><span class="sxs-lookup"><span data-stu-id="8457e-2595">dwType</span></span>

<span data-ttu-id="8457e-2596">RGB (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-2596">rgb (variable)</span></span>



 

<span data-ttu-id="8457e-2597">**dwType**: uno de los tipos Variant, definido en la sección 2.2.1.1, que se puede combinar con modificadores de tipo variante.</span><span class="sxs-lookup"><span data-stu-id="8457e-2597">**dwType**: One of the variant types, defined in section 2.2.1.1, which can be combined with variant type modifiers.</span></span> <span data-ttu-id="8457e-2598">En todos los tipos de variante, excepto los \_ que se combinan con la matriz de VT, SERIALIZEDPROPERTYVALUE tiene el mismo diseño que CBaseStorageVariant, como se especifica en la sección 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="8457e-2598">For all variant types, except those combined with VT\_ARRAY, SERIALIZEDPROPERTYVALUE has the same layout as CBaseStorageVariant, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="8457e-2599">Si el tipo Variant se combina con el \_ modificador de tipo de matriz VT, se usa SAFEARRAY2, especificado en la sección 2.2.1.2.1.1, en lugar de SAFEARRAY en el campo vValue de CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="8457e-2599">If the variant type is combined with the VT\_ARRAY type modifier, then SAFEARRAY2, specified in Section 2.2.1.2.1.1, is used instead of SAFEARRAY in CBaseStorageVariant's vValue field.</span></span>

<span data-ttu-id="8457e-2600">**RGB**: valor serializado.</span><span class="sxs-lookup"><span data-stu-id="8457e-2600">**rgb**: Serialized value.</span></span> <span data-ttu-id="8457e-2601">Vea los detalles de la serialización de vValue en 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="8457e-2601">See details of serialization for vValue in 2.2.1.1.</span></span>

### <a name="222-message-headers"></a><span data-ttu-id="8457e-2602">2.2.2 encabezados de mensaje</span><span class="sxs-lookup"><span data-stu-id="8457e-2602">2.2.2 Message Headers</span></span>

<span data-ttu-id="8457e-2603">Todos los mensajes del protocolo del servicio de indización de contenido tienen un encabezado de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="8457e-2603">All Content Indexing Service Protocol messages have a 16 byte header.</span></span>

<span data-ttu-id="8457e-2604">A continuación se muestra un diagrama que muestra el formato del encabezado de mensaje del protocolo del servicio de indización de contenido.</span><span class="sxs-lookup"><span data-stu-id="8457e-2604">Below is a diagram showing the Content Indexing Service Protocol message header format.</span></span>



<span data-ttu-id="8457e-2605">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2605">0</span></span>

<span data-ttu-id="8457e-2606">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2606">1</span></span>

<span data-ttu-id="8457e-2607">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2607">2</span></span>

<span data-ttu-id="8457e-2608">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2608">3</span></span>

<span data-ttu-id="8457e-2609">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2609">4</span></span>

<span data-ttu-id="8457e-2610">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2610">5</span></span>

<span data-ttu-id="8457e-2611">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2611">6</span></span>

<span data-ttu-id="8457e-2612">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2612">7</span></span>

<span data-ttu-id="8457e-2613">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2613">8</span></span>

<span data-ttu-id="8457e-2614">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2614">9</span></span>

<span data-ttu-id="8457e-2615">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2615">1</span></span><br/> <span data-ttu-id="8457e-2616">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2616">0</span></span><br/>

<span data-ttu-id="8457e-2617">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2617">1</span></span>

<span data-ttu-id="8457e-2618">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2618">2</span></span>

<span data-ttu-id="8457e-2619">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2619">3</span></span>

<span data-ttu-id="8457e-2620">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2620">4</span></span>

<span data-ttu-id="8457e-2621">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2621">5</span></span>

<span data-ttu-id="8457e-2622">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2622">6</span></span>

<span data-ttu-id="8457e-2623">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2623">7</span></span>

<span data-ttu-id="8457e-2624">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2624">8</span></span>

<span data-ttu-id="8457e-2625">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2625">9</span></span>

<span data-ttu-id="8457e-2626">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2626">2</span></span><br/> <span data-ttu-id="8457e-2627">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2627">0</span></span><br/>

<span data-ttu-id="8457e-2628">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2628">1</span></span>

<span data-ttu-id="8457e-2629">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2629">2</span></span>

<span data-ttu-id="8457e-2630">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2630">3</span></span>

<span data-ttu-id="8457e-2631">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2631">4</span></span>

<span data-ttu-id="8457e-2632">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2632">5</span></span>

<span data-ttu-id="8457e-2633">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2633">6</span></span>

<span data-ttu-id="8457e-2634">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2634">7</span></span>

<span data-ttu-id="8457e-2635">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2635">8</span></span>

<span data-ttu-id="8457e-2636">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2636">9</span></span>

<span data-ttu-id="8457e-2637">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2637">3</span></span><br/> <span data-ttu-id="8457e-2638">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2638">0</span></span><br/>

<span data-ttu-id="8457e-2639">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2639">1</span></span>

<span data-ttu-id="8457e-2640">\_mensaje</span><span class="sxs-lookup"><span data-stu-id="8457e-2640">\_msg</span></span>

<span data-ttu-id="8457e-2641">\_estatus</span><span class="sxs-lookup"><span data-stu-id="8457e-2641">\_status</span></span>

<span data-ttu-id="8457e-2642">\_ulChecksum</span><span class="sxs-lookup"><span data-stu-id="8457e-2642">\_ulChecksum</span></span>

<span data-ttu-id="8457e-2643">\_ulReserved2</span><span class="sxs-lookup"><span data-stu-id="8457e-2643">\_ulReserved2</span></span>



 

<span data-ttu-id="8457e-2644">\_**MSG**: un entero de 32 bits que identifica el tipo de mensaje que sigue al encabezado.</span><span class="sxs-lookup"><span data-stu-id="8457e-2644">\_**msg**: A 32 bit integer that identifies the type of message following the header.</span></span> <span data-ttu-id="8457e-2645">En la tabla siguiente se enumeran los mensajes de protocolo del servicio de indización de contenido y los valores enteros especificados para cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-2645">The following table lists the Content Indexing Service Protocol messages and the integer values specified for each message.</span></span> <span data-ttu-id="8457e-2646">Como se muestra en la tabla, algunos valores identifican dos mensajes en la tabla.</span><span class="sxs-lookup"><span data-stu-id="8457e-2646">As shown in the table, some values identify 2 messages in the table.</span></span> <span data-ttu-id="8457e-2647">En esas instancias, el mensaje que sigue al encabezado puede identificarse por la dirección del flujo de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8457e-2647">In those instances the message following the header can be identified by the direction of the message flow.</span></span> <span data-ttu-id="8457e-2648">Si la dirección es cliente a servidor, se indica el mensaje con "in" anexado al nombre del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-2648">If the direction is client to server, the message with "In" appended to the message name is indicated.</span></span> <span data-ttu-id="8457e-2649">Si la dirección es servidor a cliente, se indica el mensaje con la marca "out" anexada al nombre del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-2649">If the direction is server to client, the message with "Out" appended to the message name is indicated.</span></span>



| <span data-ttu-id="8457e-2650">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-2650">Value</span></span>      | <span data-ttu-id="8457e-2651">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-2651">Meaning</span></span>                                                     |
|------------|-------------------------------------------------------------|
| <span data-ttu-id="8457e-2652">0x000000C8</span><span class="sxs-lookup"><span data-stu-id="8457e-2652">0x000000C8</span></span> | <span data-ttu-id="8457e-2653">CPMConnectIn o CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="8457e-2653">CPMConnectIn or CPMConnectOut</span></span>                               |
| <span data-ttu-id="8457e-2654">0x000000C9</span><span class="sxs-lookup"><span data-stu-id="8457e-2654">0x000000C9</span></span> | <span data-ttu-id="8457e-2655">CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="8457e-2655">CPMDisconnect</span></span>                                               |
| <span data-ttu-id="8457e-2656">0x000000CA</span><span class="sxs-lookup"><span data-stu-id="8457e-2656">0x000000CA</span></span> | <span data-ttu-id="8457e-2657">CPMCreateQueryIn o CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="8457e-2657">CPMCreateQueryIn or CPMCreateQueryOut</span></span>                       |
| <span data-ttu-id="8457e-2658">0x000000CB</span><span class="sxs-lookup"><span data-stu-id="8457e-2658">0x000000CB</span></span> | <span data-ttu-id="8457e-2659">CPMFreeCursorIn o CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="8457e-2659">CPMFreeCursorIn or CPMFreeCursorOut</span></span>                         |
| <span data-ttu-id="8457e-2660">0x000000CC</span><span class="sxs-lookup"><span data-stu-id="8457e-2660">0x000000CC</span></span> | <span data-ttu-id="8457e-2661">CPMGetRowsIn o CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="8457e-2661">CPMGetRowsIn or CPMGetRowsOut</span></span>                               |
| <span data-ttu-id="8457e-2662">0x000000CD</span><span class="sxs-lookup"><span data-stu-id="8457e-2662">0x000000CD</span></span> | <span data-ttu-id="8457e-2663">CPMRatioFinishedIn o CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="8457e-2663">CPMRatioFinishedIn or CPMRatioFinishedOut</span></span>                   |
| <span data-ttu-id="8457e-2664">0x000000CE</span><span class="sxs-lookup"><span data-stu-id="8457e-2664">0x000000CE</span></span> | <span data-ttu-id="8457e-2665">CPMCompareBmkIn o CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="8457e-2665">CPMCompareBmkIn or CPMCompareBmkOut</span></span>                         |
| <span data-ttu-id="8457e-2666">0x000000CF</span><span class="sxs-lookup"><span data-stu-id="8457e-2666">0x000000CF</span></span> | <span data-ttu-id="8457e-2667">CPMGetApproximatePositionIn o CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="8457e-2667">CPMGetApproximatePositionIn or CPMGetApproximatePositionOut</span></span> |
| <span data-ttu-id="8457e-2668">0x000000D0</span><span class="sxs-lookup"><span data-stu-id="8457e-2668">0x000000D0</span></span> | <span data-ttu-id="8457e-2669">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="8457e-2669">CPMSetBindingsIn</span></span>                                            |
| <span data-ttu-id="8457e-2670">0x000000D1</span><span class="sxs-lookup"><span data-stu-id="8457e-2670">0x000000D1</span></span> | <span data-ttu-id="8457e-2671">CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="8457e-2671">CPMGetNotify</span></span>                                                |
| <span data-ttu-id="8457e-2672">0x000000D2</span><span class="sxs-lookup"><span data-stu-id="8457e-2672">0x000000D2</span></span> | <span data-ttu-id="8457e-2673">CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="8457e-2673">CPMSendNotifyOut</span></span>                                            |
| <span data-ttu-id="8457e-2674">0x000000D7</span><span class="sxs-lookup"><span data-stu-id="8457e-2674">0x000000D7</span></span> | <span data-ttu-id="8457e-2675">CPMGetQueryStatusIn o CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="8457e-2675">CPMGetQueryStatusIn or CPMGetQueryStatusOut</span></span>                 |
| <span data-ttu-id="8457e-2676">0x000000D9</span><span class="sxs-lookup"><span data-stu-id="8457e-2676">0x000000D9</span></span> | <span data-ttu-id="8457e-2677">CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="8457e-2677">CPMCiStateInOut</span></span>                                             |
| <span data-ttu-id="8457e-2678">0x000000E1</span><span class="sxs-lookup"><span data-stu-id="8457e-2678">0x000000E1</span></span> | <span data-ttu-id="8457e-2679">CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="8457e-2679">CPMForceMergeIn</span></span>                                             |
| <span data-ttu-id="8457e-2680">0x000000E4</span><span class="sxs-lookup"><span data-stu-id="8457e-2680">0x000000E4</span></span> | <span data-ttu-id="8457e-2681">CPMFetchValueIn o CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="8457e-2681">CPMFetchValueIn or CPMFetchValueOut</span></span>                         |
| <span data-ttu-id="8457e-2682">0x000000E6</span><span class="sxs-lookup"><span data-stu-id="8457e-2682">0x000000E6</span></span> | <span data-ttu-id="8457e-2683">CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="8457e-2683">CPMUpdateDocumentsIn</span></span>                                        |
| <span data-ttu-id="8457e-2684">0x000000E7</span><span class="sxs-lookup"><span data-stu-id="8457e-2684">0x000000E7</span></span> | <span data-ttu-id="8457e-2685">CPMGetQueryStatusExIn o PMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="8457e-2685">CPMGetQueryStatusExIn or PMGetQueryStatusExOut</span></span>              |
| <span data-ttu-id="8457e-2686">0x000000E8</span><span class="sxs-lookup"><span data-stu-id="8457e-2686">0x000000E8</span></span> | <span data-ttu-id="8457e-2687">CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="8457e-2687">CPMRestartPositionIn</span></span>                                        |
| <span data-ttu-id="8457e-2688">0x000000E9</span><span class="sxs-lookup"><span data-stu-id="8457e-2688">0x000000E9</span></span> | <span data-ttu-id="8457e-2689">CPMStopAsynchIn</span><span class="sxs-lookup"><span data-stu-id="8457e-2689">CPMStopAsynchIn</span></span>                                             |
| <span data-ttu-id="8457e-2690">0x000000EC</span><span class="sxs-lookup"><span data-stu-id="8457e-2690">0x000000EC</span></span> | <span data-ttu-id="8457e-2691">CPMSetCatStateIn o CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="8457e-2691">CPMSetCatStateIn or CPMSetCatStateOut</span></span>                       |



 

<span data-ttu-id="8457e-2692">\_**status**: HRESULT \[ MS-sys \] , que indica el estado de la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="8457e-2692">\_**status**: An HRESULT \[MS-SYS\], indicating the status of the requested operation.</span></span>

\* *

<span data-ttu-id="8457e-2693">*Comportamiento de Windows: el cliente siempre establece el \_ campo de estado en 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="8457e-2693">*Windows Behavior: The client always sets the \_status field to 0x00000000.*</span></span>

<span data-ttu-id="8457e-2694">**\_ ulChecksum**: el \_ ulChecksum debe calcularse como se especifica en la sección 3.2.4 para los siguientes mensajes:</span><span class="sxs-lookup"><span data-stu-id="8457e-2694">**\_ulChecksum**: The \_ulChecksum MUST be calculated as specified in Section 3.2.4 for the following messages:</span></span>

-   <span data-ttu-id="8457e-2695">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="8457e-2695">CPMConnectIn</span></span>
-   <span data-ttu-id="8457e-2696">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="8457e-2696">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="8457e-2697">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="8457e-2697">CPMSetBindingsIn</span></span>
-   <span data-ttu-id="8457e-2698">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="8457e-2698">CPMGetRowsIn</span></span>
-   <span data-ttu-id="8457e-2699">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="8457e-2699">CPMFetchValueIn</span></span>

<span data-ttu-id="8457e-2700">Para todos los demás mensajes, \_ ULCHECKSUM debe establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-2700">For all other messages, \_ulChecksum MUST be set to 0x00000000.</span></span> <span data-ttu-id="8457e-2701">Un cliente debe omitir el \_ campo ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="8457e-2701">A client MUST ignore the\_ulChecksum field.</span></span>

<span data-ttu-id="8457e-2702">**\_ ulReserved2**: debe establecerse en 0 y el receptor lo omitirá.</span><span class="sxs-lookup"><span data-stu-id="8457e-2702">**\_ulReserved2**: MUST be set to 0, and ignored by the receiver.</span></span>

### <a name="223-messages"></a><span data-ttu-id="8457e-2703">2.2.3 mensajes</span><span class="sxs-lookup"><span data-stu-id="8457e-2703">2.2.3 Messages</span></span>

### <a name="2231-cpmcistateinout"></a><span data-ttu-id="8457e-2704">2.2.3.1 CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="8457e-2704">2.2.3.1 CPMCiStateInOut</span></span>

<span data-ttu-id="8457e-2705">El mensaje CPMCiStateInOut contiene información sobre el estado del servicio de indización.</span><span class="sxs-lookup"><span data-stu-id="8457e-2705">The CPMCiStateInOut message contains information about the state of the indexing service.</span></span> <span data-ttu-id="8457e-2706">El formato del mensaje CPMCiStateInOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-2706">The format of the CPMCiStateInOut message that follows the header is:</span></span>



<span data-ttu-id="8457e-2707">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2707">0</span></span>

<span data-ttu-id="8457e-2708">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2708">1</span></span>

<span data-ttu-id="8457e-2709">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2709">2</span></span>

<span data-ttu-id="8457e-2710">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2710">3</span></span>

<span data-ttu-id="8457e-2711">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2711">4</span></span>

<span data-ttu-id="8457e-2712">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2712">5</span></span>

<span data-ttu-id="8457e-2713">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2713">6</span></span>

<span data-ttu-id="8457e-2714">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2714">7</span></span>

<span data-ttu-id="8457e-2715">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2715">8</span></span>

<span data-ttu-id="8457e-2716">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2716">9</span></span>

<span data-ttu-id="8457e-2717">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2717">1</span></span><br/> <span data-ttu-id="8457e-2718">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2718">0</span></span><br/>

<span data-ttu-id="8457e-2719">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2719">1</span></span>

<span data-ttu-id="8457e-2720">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2720">2</span></span>

<span data-ttu-id="8457e-2721">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2721">3</span></span>

<span data-ttu-id="8457e-2722">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2722">4</span></span>

<span data-ttu-id="8457e-2723">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2723">5</span></span>

<span data-ttu-id="8457e-2724">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2724">6</span></span>

<span data-ttu-id="8457e-2725">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2725">7</span></span>

<span data-ttu-id="8457e-2726">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2726">8</span></span>

<span data-ttu-id="8457e-2727">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2727">9</span></span>

<span data-ttu-id="8457e-2728">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2728">2</span></span><br/> <span data-ttu-id="8457e-2729">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2729">0</span></span><br/>

<span data-ttu-id="8457e-2730">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2730">1</span></span>

<span data-ttu-id="8457e-2731">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2731">2</span></span>

<span data-ttu-id="8457e-2732">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2732">3</span></span>

<span data-ttu-id="8457e-2733">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2733">4</span></span>

<span data-ttu-id="8457e-2734">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2734">5</span></span>

<span data-ttu-id="8457e-2735">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2735">6</span></span>

<span data-ttu-id="8457e-2736">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2736">7</span></span>

<span data-ttu-id="8457e-2737">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2737">8</span></span>

<span data-ttu-id="8457e-2738">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2738">9</span></span>

<span data-ttu-id="8457e-2739">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2739">3</span></span><br/> <span data-ttu-id="8457e-2740">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2740">0</span></span><br/>

<span data-ttu-id="8457e-2741">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2741">1</span></span>

<span data-ttu-id="8457e-2742">cbStruct</span><span class="sxs-lookup"><span data-stu-id="8457e-2742">cbStruct</span></span>

<span data-ttu-id="8457e-2743">cWordList</span><span class="sxs-lookup"><span data-stu-id="8457e-2743">cWordList</span></span>

<span data-ttu-id="8457e-2744">cPersistentIndex</span><span class="sxs-lookup"><span data-stu-id="8457e-2744">cPersistentIndex</span></span>

<span data-ttu-id="8457e-2745">cQueries</span><span class="sxs-lookup"><span data-stu-id="8457e-2745">cQueries</span></span>

<span data-ttu-id="8457e-2746">cDocuments</span><span class="sxs-lookup"><span data-stu-id="8457e-2746">cDocuments</span></span>

<span data-ttu-id="8457e-2747">cFreshTest</span><span class="sxs-lookup"><span data-stu-id="8457e-2747">cFreshTest</span></span>

<span data-ttu-id="8457e-2748">dwMergeProgress</span><span class="sxs-lookup"><span data-stu-id="8457e-2748">dwMergeProgress</span></span>

<span data-ttu-id="8457e-2749">eState</span><span class="sxs-lookup"><span data-stu-id="8457e-2749">eState</span></span>

<span data-ttu-id="8457e-2750">cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="8457e-2750">cFilteredDocuments</span></span>

<span data-ttu-id="8457e-2751">cTotalDocuments</span><span class="sxs-lookup"><span data-stu-id="8457e-2751">cTotalDocuments</span></span>

<span data-ttu-id="8457e-2752">cPendingScans</span><span class="sxs-lookup"><span data-stu-id="8457e-2752">cPendingScans</span></span>

<span data-ttu-id="8457e-2753">dwIndexSize</span><span class="sxs-lookup"><span data-stu-id="8457e-2753">dwIndexSize</span></span>

<span data-ttu-id="8457e-2754">cUniqueKeys</span><span class="sxs-lookup"><span data-stu-id="8457e-2754">cUniqueKeys</span></span>

<span data-ttu-id="8457e-2755">cSecQDocuments</span><span class="sxs-lookup"><span data-stu-id="8457e-2755">cSecQDocuments</span></span>

<span data-ttu-id="8457e-2756">dwPropCacheSize</span><span class="sxs-lookup"><span data-stu-id="8457e-2756">dwPropCacheSize</span></span>



 

<span data-ttu-id="8457e-2757">**cbStruct**: entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="8457e-2757">**cbStruct**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="8457e-2758">Tamaño en bytes de este mensaje (sin incluir el encabezado común).</span><span class="sxs-lookup"><span data-stu-id="8457e-2758">The size in bytes of this message (excluding the common header).</span></span> <span data-ttu-id="8457e-2759">DEBE establecerse en 0x0000003C.</span><span class="sxs-lookup"><span data-stu-id="8457e-2759">MUST be set to 0x0000003C.</span></span>

<span data-ttu-id="8457e-2760">**cWordList**: entero de 32 bits sin signo que indica el recuento de los índices iniciales creados para documentos indexados recientemente.</span><span class="sxs-lookup"><span data-stu-id="8457e-2760">**cWordList**: A 32-bit unsigned integer indicating the count of initial indexes created for recently indexed documents.</span></span>

<span data-ttu-id="8457e-2761">**cPersistentIndex**: entero de 32 bits sin signo que indica el recuento de índices persistentes.</span><span class="sxs-lookup"><span data-stu-id="8457e-2761">**cPersistentIndex**: A 32-bit unsigned integer indicating the count of persistent indexes.</span></span>

<span data-ttu-id="8457e-2762">**cQueries**: entero de 32 bits sin signo que indica un número de consultas que se ejecutan activamente.</span><span class="sxs-lookup"><span data-stu-id="8457e-2762">**cQueries**: A 32-bit unsigned integer indicating a number of actively running queries.</span></span>

<span data-ttu-id="8457e-2763">**cDocuments**: entero de 32 bits sin signo que indica el número total de documentos que están en espera de ser indexados.</span><span class="sxs-lookup"><span data-stu-id="8457e-2763">**cDocuments**: A 32-bit unsigned integer indicating the total number of documents waiting to be indexed.</span></span>

<span data-ttu-id="8457e-2764">**cFreshTest**: entero de 32 bits sin signo que indica el número de documentos únicos con información en índices que no están totalmente optimizados para el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8457e-2764">**cFreshTest**: A 32-bit unsigned integer indicating the number of unique documents with information in indexes that are not fully optimized for performance.</span></span>

<span data-ttu-id="8457e-2765">**dwMergeProgress**: entero de 32 bits sin signo que especifica el porcentaje de finalización de la optimización completa actual de los índices, si la optimización está en curso actualmente.</span><span class="sxs-lookup"><span data-stu-id="8457e-2765">**dwMergeProgress**: Unsigned 32-bit integer specifying the completion percentage of current full optimization of indexes, if optimization is currently in progress.</span></span> <span data-ttu-id="8457e-2766">DEBE ser menor o igual que 100.</span><span class="sxs-lookup"><span data-stu-id="8457e-2766">MUST be less than or equal to 100.</span></span>

<span data-ttu-id="8457e-2767">**inmobiliaria**: el estado de la indización de contenido dado por una o varias de las constantes de estado de CI \_ \_ \* , definidas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8457e-2767">**eState**: State of content indexing as given by one or more of the CI\_STATE\_\* constants, defined in the table below.</span></span>



| <span data-ttu-id="8457e-2768">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-2768">Value</span></span>                                         | <span data-ttu-id="8457e-2769">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-2769">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-2770">\_Combinación de instantáneas de estado de CI \_ \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-2770">CI\_STATE\_SHADOW\_MERGE 0x00000001</span></span>           | <span data-ttu-id="8457e-2771">El servicio de indización está en proceso de optimizar algunos de los índices para reducir el uso de memoria y mejorar el rendimiento de las consultas.</span><span class="sxs-lookup"><span data-stu-id="8457e-2771">The indexing service is in the process of optimizing some of the indexes to reduce memory usage and improve query performance.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="8457e-2772">\_ \_ \_ Fusión mediante combinación maestra de estado de CI</span><span class="sxs-lookup"><span data-stu-id="8457e-2772">CI\_STATE\_MASTER\_MERGE 0x00000002</span></span>           | <span data-ttu-id="8457e-2773">El servicio de indización está en proceso de optimización completa de todos los índices.</span><span class="sxs-lookup"><span data-stu-id="8457e-2773">The indexing service is in the process of full optimization for all indexes.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="8457e-2774">Examen de contenido de estado de CI \_ \_ \_ \_ requerido 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8457e-2774">CI\_STATE\_CONTENT\_SCAN\_REQUIRED 0x00000004</span></span> | <span data-ttu-id="8457e-2775">Algunos documentos del índice han cambiado y el servicio de indexación debe determinar cuáles se han agregado, cambiado o eliminado.</span><span class="sxs-lookup"><span data-stu-id="8457e-2775">Some documents in the index have changed and the indexing service needs to determine which have been added, changed, or deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="8457e-2776">Recocido de estado de CI \_ \_ \_ Merge 0x00000008</span><span class="sxs-lookup"><span data-stu-id="8457e-2776">CI\_STATE\_ANNEALING\_MERGE 0x00000008</span></span>        | <span data-ttu-id="8457e-2777">El servicio de indización está en proceso de optimizar los índices para reducir el uso de memoria y mejorar el rendimiento de las consultas.</span><span class="sxs-lookup"><span data-stu-id="8457e-2777">The indexing service is in the process of optimizing indexes to reduce memory usage and improve query performance.</span></span> <span data-ttu-id="8457e-2778">Este proceso es más completo que el identificado por el valor de la \_ combinación de instantáneas de estado de CI \_ \_ , pero no es tan completo como lo especifica el valor de combinación del maestro de estado de CI \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8457e-2778">This process is more comprehensive than the one identified by the CI\_STATE\_SHADOW\_MERGE value, but it is not as comprehensive as specified by the CI\_STATE\_MASTER\_MERGE value.</span></span> <span data-ttu-id="8457e-2779">Estas optimizaciones son específicas de la implementación, ya que dependen de la forma en que se almacenan internamente los datos. las optimizaciones no afectan al Protocolo de ningún modo que no sea el tiempo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8457e-2779">Such optimizations are implementation-specific as they depend on the way data is stored internally; the optimizations do not affect the protocol in any way other than response time.</span></span> |
| <span data-ttu-id="8457e-2780">Análisis de estado de CI \_ \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="8457e-2780">CI\_STATE\_SCANNING 0x00000010</span></span>                | <span data-ttu-id="8457e-2781">El servicio de indización está examinando un directorio o un conjunto de directorios para ver si se ha agregado, eliminado o actualizado algún archivo desde la última vez que se indizó el directorio.</span><span class="sxs-lookup"><span data-stu-id="8457e-2781">The indexing service is examining a directory or a set of directories to see if any files have been added, deleted, or updated since the last time the directory was indexed.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="8457e-2782">Recuperación de estado de CI \_ \_ 0x00000020</span><span class="sxs-lookup"><span data-stu-id="8457e-2782">CI\_STATE\_RECOVERING 0x00000020</span></span>              | <span data-ttu-id="8457e-2783">El servicio se está iniciando desde el último estado guardado y está en proceso de recuperación.</span><span class="sxs-lookup"><span data-stu-id="8457e-2783">The service is starting from the last saved state and is in the process of recovering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="8457e-2784">\_Memoria insuficiente de estado de CI \_ \_ 0x00000080</span><span class="sxs-lookup"><span data-stu-id="8457e-2784">CI\_STATE\_LOW\_MEMORY 0x00000080</span></span>             | <span data-ttu-id="8457e-2785">La mayor parte de la memoria virtual del servidor está en uso.</span><span class="sxs-lookup"><span data-stu-id="8457e-2785">Most of the virtual memory of the server is in use.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="8457e-2786">\_ \_ Alta e/s de estado de CI \_ 0x00000100</span><span class="sxs-lookup"><span data-stu-id="8457e-2786">CI\_STATE\_HIGH\_IO 0x00000100</span></span>                | <span data-ttu-id="8457e-2787">El nivel de actividad de entrada/salida (e/s) en el servidor es relativamente alto.</span><span class="sxs-lookup"><span data-stu-id="8457e-2787">The level of input/output (I/O) activity on the server is relatively high.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="8457e-2788">Combinación del maestro de estado de CI en \_ \_ \_ \_ pausa 0x00000200</span><span class="sxs-lookup"><span data-stu-id="8457e-2788">CI\_STATE\_MASTER\_MERGE\_PAUSED 0x00000200</span></span>   | <span data-ttu-id="8457e-2789">El proceso de optimización completa de todos los índices en curso se ha puesto en pausa.</span><span class="sxs-lookup"><span data-stu-id="8457e-2789">The process of full optimization for all indexes that was in progress has been paused.</span></span> <span data-ttu-id="8457e-2790">Esto se proporciona solo con fines informativos y no afecta a CISP.</span><span class="sxs-lookup"><span data-stu-id="8457e-2790">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="8457e-2791">Estado de CI \_ \_ \_ solo lectura 0x00000400</span><span class="sxs-lookup"><span data-stu-id="8457e-2791">CI\_STATE\_READ\_ONLY 0x00000400</span></span>              | <span data-ttu-id="8457e-2792">La parte del servicio de indexación que recoge nuevos documentos para el índice se ha puesto en pausa.</span><span class="sxs-lookup"><span data-stu-id="8457e-2792">The portion of the indexing service that picks up new documents to index has been paused.</span></span> <span data-ttu-id="8457e-2793">Esto se proporciona solo con fines informativos y no afecta a CISP.</span><span class="sxs-lookup"><span data-stu-id="8457e-2793">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="8457e-2794">Energía de la batería de estado de CI \_ \_ \_ 0x00000800</span><span class="sxs-lookup"><span data-stu-id="8457e-2794">CI\_STATE\_BATTERY\_POWER 0x00000800</span></span>          | <span data-ttu-id="8457e-2795">La parte del servicio de indexación que recoge nuevos documentos para el índice se ha pausado para conservar la duración de la batería, pero sigue respondiendo a las consultas.</span><span class="sxs-lookup"><span data-stu-id="8457e-2795">The portion of the indexing service that picks up new documents to index has been paused to conserve battery lifetime but still replies to the queries.</span></span> <span data-ttu-id="8457e-2796">Esto se proporciona solo con fines informativos y no afecta a CISP.</span><span class="sxs-lookup"><span data-stu-id="8457e-2796">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="8457e-2797">\_ \_ 0x00001000 activo de usuario de estado de CI \_</span><span class="sxs-lookup"><span data-stu-id="8457e-2797">CI\_STATE\_USER\_ACTIVE 0x00001000</span></span>            | <span data-ttu-id="8457e-2798">La parte del servicio de indización que recoge nuevos documentos para el índice se ha puesto en pausa debido a la alta actividad por parte del usuario (teclado o del mouse) pero sigue respondiendo a las consultas.</span><span class="sxs-lookup"><span data-stu-id="8457e-2798">The portion of the indexing service that picks up new documents to index has been paused due to high activity by the user (keyboard or mouse) but still replies to the queries.</span></span> <span data-ttu-id="8457e-2799">Esto se proporciona solo con fines informativos y no afecta a CISP.</span><span class="sxs-lookup"><span data-stu-id="8457e-2799">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="8457e-2800">Estado de CI \_ \_ iniciando 0x00002000</span><span class="sxs-lookup"><span data-stu-id="8457e-2800">CI\_STATE\_STARTING 0x00002000</span></span>                | <span data-ttu-id="8457e-2801">El servicio está iniciándose.</span><span class="sxs-lookup"><span data-stu-id="8457e-2801">The service is starting.</span></span> <span data-ttu-id="8457e-2802">Se pueden ejecutar consultas, pero aún no se ha habilitado el examen y la notificación.</span><span class="sxs-lookup"><span data-stu-id="8457e-2802">Queries can be run, but scanning and notification have not been enabled yet.</span></span> <span data-ttu-id="8457e-2803">Esto se proporciona solo con fines informativos y no afecta a CISP.</span><span class="sxs-lookup"><span data-stu-id="8457e-2803">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="8457e-2804">Estado de CI \_ \_ leyendo \_ USN 0x00004000</span><span class="sxs-lookup"><span data-stu-id="8457e-2804">CI\_STATE\_READING\_USNS 0x00004000</span></span>           | <span data-ttu-id="8457e-2805">El servicio no ha leído el registro mantenido por el sistema de archivos para realizar un seguimiento de los cambios en los archivos o directorios de un volumen, por lo que es posible que el índice no esté actualizado.</span><span class="sxs-lookup"><span data-stu-id="8457e-2805">The service has not read the log kept by the file system to keep track of changes to files or directories in a volume, so the index might not be up to date.</span></span>                                                                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="8457e-2806">**cFilteredDocuments**: entero de 32 bits sin signo que indica el número de documentos indizados desde que se inició la indización de contenido.</span><span class="sxs-lookup"><span data-stu-id="8457e-2806">**cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents indexed since content indexing was begun.</span></span>

<span data-ttu-id="8457e-2807">**cTotalDocuments**: entero de 32 bits sin signo que indica el número total de documentos en el sistema.</span><span class="sxs-lookup"><span data-stu-id="8457e-2807">**cTotalDocuments**: A 32-bit unsigned integer indicating the total number of documents in the system.</span></span>

<span data-ttu-id="8457e-2808">**cPendingScans**: entero de 32 bits sin signo que indica el número de operaciones pendientes de indización de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="8457e-2808">**cPendingScans**: A 32-bit unsigned integer indicating the number of pending high level indexing operations.</span></span> <span data-ttu-id="8457e-2809">El significado de este valor es específico del proveedor, pero se espera que los números mayores indiquen que se mantiene más indexación.</span><span class="sxs-lookup"><span data-stu-id="8457e-2809">The meaning of this value is provider-specific but larger numbers are expected to indicate more indexing remains.</span></span>

<span data-ttu-id="8457e-2810">*Comportamiento de Windows*: este valor suele ser cero, excepto inmediatamente después de que se haya iniciado la indexación o después de que se desborde una cola de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="8457e-2810">*Windows Behavior*: This value is usually zero, except immediately after indexing has been started or after a notification queue overflows.</span></span>

<span data-ttu-id="8457e-2811">**dwIndexSize**: entero de 32 bits sin signo que indica el tamaño, en megabytes, del índice (excluida la memoria caché de propiedades).</span><span class="sxs-lookup"><span data-stu-id="8457e-2811">**dwIndexSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the index (excluding the property cache).</span></span>

<span data-ttu-id="8457e-2812">**cUniqueKeys**: entero de 32 bits sin signo que indica el número aproximado de claves únicas en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="8457e-2812">**cUniqueKeys**: A 32-bit unsigned integer indicating the approximate number of unique keys in the catalog.</span></span>

<span data-ttu-id="8457e-2813">**cSecQDocuments**: entero de 32 bits sin signo que indica el número de documentos que el servicio de indización volverá a intentar indizar debido a un error durante el intento de indexación inicial.</span><span class="sxs-lookup"><span data-stu-id="8457e-2813">**cSecQDocuments**: A 32-bit unsigned integer indicating the number of documents that the indexing service will re-attempt to index because of a failure during the initial indexing attempt.</span></span>

<span data-ttu-id="8457e-2814">**dwPropCacheSize**: entero de 32 bits sin signo que indica el tamaño, en megabytes, de la memoria caché de propiedades.</span><span class="sxs-lookup"><span data-stu-id="8457e-2814">**dwPropCacheSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the property cache.</span></span>

### <a name="2232-cpmsetcatstatein"></a><span data-ttu-id="8457e-2815">2.2.3.2 CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="8457e-2815">2.2.3.2 CPMSetCatStateIn</span></span>

<span data-ttu-id="8457e-2816">El mensaje CPMSetCatStateIn establece el estado de un catálogo.</span><span class="sxs-lookup"><span data-stu-id="8457e-2816">The CPMSetCatStateIn message sets the state of a catalog.</span></span> <span data-ttu-id="8457e-2817">El formato del mensaje CPMSetCatStateIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-2817">The format of the CPMSetCatStateIn message that follows the header is:</span></span>



<span data-ttu-id="8457e-2818">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2818">0</span></span>

<span data-ttu-id="8457e-2819">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2819">1</span></span>

<span data-ttu-id="8457e-2820">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2820">2</span></span>

<span data-ttu-id="8457e-2821">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2821">3</span></span>

<span data-ttu-id="8457e-2822">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2822">4</span></span>

<span data-ttu-id="8457e-2823">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2823">5</span></span>

<span data-ttu-id="8457e-2824">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2824">6</span></span>

<span data-ttu-id="8457e-2825">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2825">7</span></span>

<span data-ttu-id="8457e-2826">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2826">8</span></span>

<span data-ttu-id="8457e-2827">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2827">9</span></span>

<span data-ttu-id="8457e-2828">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2828">1</span></span><br/> <span data-ttu-id="8457e-2829">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2829">0</span></span><br/>

<span data-ttu-id="8457e-2830">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2830">1</span></span>

<span data-ttu-id="8457e-2831">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2831">2</span></span>

<span data-ttu-id="8457e-2832">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2832">3</span></span>

<span data-ttu-id="8457e-2833">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2833">4</span></span>

<span data-ttu-id="8457e-2834">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2834">5</span></span>

<span data-ttu-id="8457e-2835">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2835">6</span></span>

<span data-ttu-id="8457e-2836">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2836">7</span></span>

<span data-ttu-id="8457e-2837">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2837">8</span></span>

<span data-ttu-id="8457e-2838">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2838">9</span></span>

<span data-ttu-id="8457e-2839">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2839">2</span></span><br/> <span data-ttu-id="8457e-2840">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2840">0</span></span><br/>

<span data-ttu-id="8457e-2841">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2841">1</span></span>

<span data-ttu-id="8457e-2842">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2842">2</span></span>

<span data-ttu-id="8457e-2843">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2843">3</span></span>

<span data-ttu-id="8457e-2844">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2844">4</span></span>

<span data-ttu-id="8457e-2845">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2845">5</span></span>

<span data-ttu-id="8457e-2846">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2846">6</span></span>

<span data-ttu-id="8457e-2847">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2847">7</span></span>

<span data-ttu-id="8457e-2848">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2848">8</span></span>

<span data-ttu-id="8457e-2849">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2849">9</span></span>

<span data-ttu-id="8457e-2850">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2850">3</span></span><br/> <span data-ttu-id="8457e-2851">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2851">0</span></span><br/>

<span data-ttu-id="8457e-2852">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2852">1</span></span>

<span data-ttu-id="8457e-2853">\_partID</span><span class="sxs-lookup"><span data-stu-id="8457e-2853">\_partID</span></span>

<span data-ttu-id="8457e-2854">\_dwNewState</span><span class="sxs-lookup"><span data-stu-id="8457e-2854">\_dwNewState</span></span>

<span data-ttu-id="8457e-2855">\_CatName (variable, opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-2855">\_CatName (variable, optional)</span></span>



 

<span data-ttu-id="8457e-2856">el valor de **\_ este: debe** establecerse en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8457e-2856">**\_partID**: MUST be set to 0x00000001.</span></span>

<span data-ttu-id="8457e-2857">**\_ dwNewState**: debe establecerse en uno de los siguientes valores, que indica el nuevo estado del catálogo.</span><span class="sxs-lookup"><span data-stu-id="8457e-2857">**\_dwNewState**: MUST be set to one of the following values, indicating the new state of the catalog.</span></span>



| <span data-ttu-id="8457e-2858">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-2858">Value</span></span>                         | <span data-ttu-id="8457e-2859">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-2859">Meaning</span></span>                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-2860">CICAT \_ detuvo 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-2860">CICAT\_STOPPED 0x00000001</span></span>     | <span data-ttu-id="8457e-2861">El catálogo se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="8457e-2861">The catalog is stopped.</span></span> <span data-ttu-id="8457e-2862">Este estado significa que no se va a indizar ningún archivo nuevo y no se procesará ninguna consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8457e-2862">This state means no new files are to be indexed, and no search queries are to be processed.</span></span>                                                     |
| <span data-ttu-id="8457e-2863">CICAT \_ ReadOnly 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8457e-2863">CICAT\_READONLY 0x00000002</span></span>    | <span data-ttu-id="8457e-2864">El catálogo es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8457e-2864">The catalog is read-only.</span></span> <span data-ttu-id="8457e-2865">No se va a indizar ningún archivo nuevo.</span><span class="sxs-lookup"><span data-stu-id="8457e-2865">No new files are to be indexed.</span></span>                                                                                                               |
| <span data-ttu-id="8457e-2866">CICAT \_ grabable 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8457e-2866">CICAT\_WRITABLE 0x00000004</span></span>    | <span data-ttu-id="8457e-2867">El catálogo es grabable.</span><span class="sxs-lookup"><span data-stu-id="8457e-2867">The catalog is writable.</span></span> <span data-ttu-id="8457e-2868">Los nuevos archivos se pueden indexar y las consultas de búsqueda se procesarán.</span><span class="sxs-lookup"><span data-stu-id="8457e-2868">New files can be indexed, and search queries are to be processed.</span></span>                                                                              |
| <span data-ttu-id="8457e-2869">CICAT \_ no \_ query 0x00000008</span><span class="sxs-lookup"><span data-stu-id="8457e-2869">CICAT\_NO\_QUERY 0x00000008</span></span>   | <span data-ttu-id="8457e-2870">El catálogo no está disponible para realizar consultas.</span><span class="sxs-lookup"><span data-stu-id="8457e-2870">The catalog is not available for querying.</span></span>                                                                                                                              |
| <span data-ttu-id="8457e-2871">CICAT \_ Get \_ State 0x00000010</span><span class="sxs-lookup"><span data-stu-id="8457e-2871">CICAT\_GET\_STATE 0x00000010</span></span>  | <span data-ttu-id="8457e-2872">No se puede cambiar el estado del catálogo, solo se recupera.</span><span class="sxs-lookup"><span data-stu-id="8457e-2872">The state of the catalog is not to be changed, only retrieved.</span></span>                                                                                                          |
| <span data-ttu-id="8457e-2873">CICAT \_ todo \_ abierto 0x00000020</span><span class="sxs-lookup"><span data-stu-id="8457e-2873">CICAT\_ALL\_OPENED 0x00000020</span></span> | <span data-ttu-id="8457e-2874">Una comprobación para ver si se han iniciado todos los catálogos.</span><span class="sxs-lookup"><span data-stu-id="8457e-2874">A check to see if all of the catalogs have been started.</span></span> <span data-ttu-id="8457e-2875">En ese caso, el \_ campo dwOldState enviado en la respuesta CPMSetCatStateOut a este mensaje se indicará como distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8457e-2875">If so, the \_dwOldState field sent in the CPMSetCatStateOut reply to this message will be reported as nonzero.</span></span> |



 

<span data-ttu-id="8457e-2876">**\_ CatName**: el nombre del catálogo cuyo estado se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="8457e-2876">**\_CatName**: The name of the catalog which is to have its state modified.</span></span> <span data-ttu-id="8457e-2877">El nombre debe ser una cadena Unicode terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="8457e-2877">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="8457e-2878">Este campo se debe omitir si \_ dwNewState está establecido en CiCAT \_ todos \_ abiertos.</span><span class="sxs-lookup"><span data-stu-id="8457e-2878">This field MUST be omitted if \_dwNewState is set to CICAT\_ALL\_OPENED.</span></span>

### <a name="2233-cpmsetcatstateout"></a><span data-ttu-id="8457e-2879">2.2.3.3 CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="8457e-2879">2.2.3.3 CPMSetCatStateOut</span></span>

<span data-ttu-id="8457e-2880">El mensaje CPMSetCatStateOut es una respuesta a un mensaje CPMSetCatStateIn con el estado anterior del catálogo.</span><span class="sxs-lookup"><span data-stu-id="8457e-2880">The CPMSetCatStateOut message is a reply to a CPMSetCatStateIn message with the old state of the catalog.</span></span> <span data-ttu-id="8457e-2881">El formato del mensaje CPMSetCatStateOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-2881">The format of the CPMSetCatStateOut message that follows the header is:</span></span>



<span data-ttu-id="8457e-2882">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2882">0</span></span>

<span data-ttu-id="8457e-2883">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2883">1</span></span>

<span data-ttu-id="8457e-2884">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2884">2</span></span>

<span data-ttu-id="8457e-2885">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2885">3</span></span>

<span data-ttu-id="8457e-2886">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2886">4</span></span>

<span data-ttu-id="8457e-2887">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2887">5</span></span>

<span data-ttu-id="8457e-2888">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2888">6</span></span>

<span data-ttu-id="8457e-2889">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2889">7</span></span>

<span data-ttu-id="8457e-2890">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2890">8</span></span>

<span data-ttu-id="8457e-2891">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2891">9</span></span>

<span data-ttu-id="8457e-2892">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2892">1</span></span><br/> <span data-ttu-id="8457e-2893">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2893">0</span></span><br/>

<span data-ttu-id="8457e-2894">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2894">1</span></span>

<span data-ttu-id="8457e-2895">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2895">2</span></span>

<span data-ttu-id="8457e-2896">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2896">3</span></span>

<span data-ttu-id="8457e-2897">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2897">4</span></span>

<span data-ttu-id="8457e-2898">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2898">5</span></span>

<span data-ttu-id="8457e-2899">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2899">6</span></span>

<span data-ttu-id="8457e-2900">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2900">7</span></span>

<span data-ttu-id="8457e-2901">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2901">8</span></span>

<span data-ttu-id="8457e-2902">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2902">9</span></span>

<span data-ttu-id="8457e-2903">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2903">2</span></span><br/> <span data-ttu-id="8457e-2904">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2904">0</span></span><br/>

<span data-ttu-id="8457e-2905">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2905">1</span></span>

<span data-ttu-id="8457e-2906">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2906">2</span></span>

<span data-ttu-id="8457e-2907">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2907">3</span></span>

<span data-ttu-id="8457e-2908">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2908">4</span></span>

<span data-ttu-id="8457e-2909">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2909">5</span></span>

<span data-ttu-id="8457e-2910">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2910">6</span></span>

<span data-ttu-id="8457e-2911">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2911">7</span></span>

<span data-ttu-id="8457e-2912">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2912">8</span></span>

<span data-ttu-id="8457e-2913">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2913">9</span></span>

<span data-ttu-id="8457e-2914">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2914">3</span></span><br/> <span data-ttu-id="8457e-2915">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2915">0</span></span><br/>

<span data-ttu-id="8457e-2916">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2916">1</span></span>

<span data-ttu-id="8457e-2917">\_dwOldState</span><span class="sxs-lookup"><span data-stu-id="8457e-2917">\_dwOldState</span></span>



 

<span data-ttu-id="8457e-2918">**\_ dwOldState**: uno de los siguientes valores, que indica el estado anterior del catálogo.</span><span class="sxs-lookup"><span data-stu-id="8457e-2918">**\_dwOldState**: One of the following values, indicating the old state of the catalog.</span></span>



| <span data-ttu-id="8457e-2919">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-2919">Value</span></span>                       | <span data-ttu-id="8457e-2920">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-2920">Meaning</span></span>                                    |
|-----------------------------|--------------------------------------------|
| <span data-ttu-id="8457e-2921">CICAT \_ detuvo 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-2921">CICAT\_STOPPED 0x00000001</span></span>   | <span data-ttu-id="8457e-2922">El catálogo se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="8457e-2922">The catalog is stopped.</span></span>                    |
| <span data-ttu-id="8457e-2923">CICAT \_ ReadOnly 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8457e-2923">CICAT\_READONLY 0x00000002</span></span>  | <span data-ttu-id="8457e-2924">El catálogo es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8457e-2924">The catalog is read-only.</span></span>                  |
| <span data-ttu-id="8457e-2925">CICAT \_ grabable 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8457e-2925">CICAT\_WRITABLE 0x00000004</span></span>  | <span data-ttu-id="8457e-2926">El catálogo es grabable.</span><span class="sxs-lookup"><span data-stu-id="8457e-2926">The catalog is writable.</span></span>                   |
| <span data-ttu-id="8457e-2927">CICAT \_ no \_ query 0x00000008</span><span class="sxs-lookup"><span data-stu-id="8457e-2927">CICAT\_NO\_QUERY 0x00000008</span></span> | <span data-ttu-id="8457e-2928">El catálogo no está disponible para realizar consultas.</span><span class="sxs-lookup"><span data-stu-id="8457e-2928">The catalog is not available for querying.</span></span> |



 

### <a name="2234-cpmupdatedocumentsin"></a><span data-ttu-id="8457e-2929">2.2.3.4 CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="8457e-2929">2.2.3.4 CPMUpdateDocumentsIn</span></span>

<span data-ttu-id="8457e-2930">El mensaje CPMUpdateDocumentsIn dirige el servidor para indizar la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="8457e-2930">The CPMUpdateDocumentsIn message directs the server to index the specified path.</span></span>

<span data-ttu-id="8457e-2931">El servidor responderá con el encabezado del mensaje del mensaje CPMUpdateDocumentsOut, con los resultados de la solicitud contenidos en el \_ campo Estado del encabezado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-2931">The server will reply with the message header of the CPMUpdateDocumentsOut message, with the results of the request contained in the \_status field of the message header.</span></span>

<span data-ttu-id="8457e-2932">El formato del mensaje CPMUpdateDocumentsIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-2932">The format of the CPMUpdateDocumentsIn message that follows the header is:</span></span>



<span data-ttu-id="8457e-2933">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2933">0</span></span>

<span data-ttu-id="8457e-2934">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2934">1</span></span>

<span data-ttu-id="8457e-2935">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2935">2</span></span>

<span data-ttu-id="8457e-2936">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2936">3</span></span>

<span data-ttu-id="8457e-2937">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2937">4</span></span>

<span data-ttu-id="8457e-2938">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2938">5</span></span>

<span data-ttu-id="8457e-2939">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2939">6</span></span>

<span data-ttu-id="8457e-2940">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2940">7</span></span>

<span data-ttu-id="8457e-2941">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2941">8</span></span>

<span data-ttu-id="8457e-2942">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2942">9</span></span>

<span data-ttu-id="8457e-2943">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2943">1</span></span><br/> <span data-ttu-id="8457e-2944">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2944">0</span></span><br/>

<span data-ttu-id="8457e-2945">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2945">1</span></span>

<span data-ttu-id="8457e-2946">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2946">2</span></span>

<span data-ttu-id="8457e-2947">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2947">3</span></span>

<span data-ttu-id="8457e-2948">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2948">4</span></span>

<span data-ttu-id="8457e-2949">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2949">5</span></span>

<span data-ttu-id="8457e-2950">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2950">6</span></span>

<span data-ttu-id="8457e-2951">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2951">7</span></span>

<span data-ttu-id="8457e-2952">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2952">8</span></span>

<span data-ttu-id="8457e-2953">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2953">9</span></span>

<span data-ttu-id="8457e-2954">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2954">2</span></span><br/> <span data-ttu-id="8457e-2955">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2955">0</span></span><br/>

<span data-ttu-id="8457e-2956">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2956">1</span></span>

<span data-ttu-id="8457e-2957">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2957">2</span></span>

<span data-ttu-id="8457e-2958">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2958">3</span></span>

<span data-ttu-id="8457e-2959">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2959">4</span></span>

<span data-ttu-id="8457e-2960">5</span><span class="sxs-lookup"><span data-stu-id="8457e-2960">5</span></span>

<span data-ttu-id="8457e-2961">6</span><span class="sxs-lookup"><span data-stu-id="8457e-2961">6</span></span>

<span data-ttu-id="8457e-2962">7</span><span class="sxs-lookup"><span data-stu-id="8457e-2962">7</span></span>

<span data-ttu-id="8457e-2963">8</span><span class="sxs-lookup"><span data-stu-id="8457e-2963">8</span></span>

<span data-ttu-id="8457e-2964">9</span><span class="sxs-lookup"><span data-stu-id="8457e-2964">9</span></span>

<span data-ttu-id="8457e-2965">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2965">3</span></span><br/> <span data-ttu-id="8457e-2966">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2966">0</span></span><br/>

<span data-ttu-id="8457e-2967">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2967">1</span></span>

<span data-ttu-id="8457e-2968">\_marca (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-2968">\_flag (optional)</span></span>

<span data-ttu-id="8457e-2969">\_fRootPath (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-2969">\_fRootPath (optional)</span></span>

<span data-ttu-id="8457e-2970">RootPath (variable, opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-2970">RootPath (variable, optional)</span></span>



 

<span data-ttu-id="8457e-2971">**\_ marca**: el tipo de actualización que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="8457e-2971">**\_flag**: The type of update to be performed.</span></span> <span data-ttu-id="8457e-2972">Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-2972">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="8457e-2973">Este campo debe establecerse en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="8457e-2973">This field MUST be set to one of the following values:</span></span>



| <span data-ttu-id="8457e-2974">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-2974">Value</span></span>                  | <span data-ttu-id="8457e-2975">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-2975">Meaning</span></span>                                   |
|------------------------|-------------------------------------------|
| <span data-ttu-id="8457e-2976">UPD \_ INCREM 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8457e-2976">UPD\_INCREM 0x00000000</span></span> | <span data-ttu-id="8457e-2977">Se realiza una actualización incremental.</span><span class="sxs-lookup"><span data-stu-id="8457e-2977">An incremental update is to be performed.</span></span> |
| <span data-ttu-id="8457e-2978">UPD \_ completo 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-2978">UPD\_FULL 0x00000001</span></span>   | <span data-ttu-id="8457e-2979">Se debe realizar una actualización completa.</span><span class="sxs-lookup"><span data-stu-id="8457e-2979">A full update is to be performed.</span></span>         |
| <span data-ttu-id="8457e-2980">UPD \_ init 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8457e-2980">UPD\_INIT 0x00000002</span></span>   | <span data-ttu-id="8457e-2981">Se debe realizar una nueva inicialización.</span><span class="sxs-lookup"><span data-stu-id="8457e-2981">A new initialization is to be performed.</span></span>  |



 

<span data-ttu-id="8457e-2982">**\_ fRootPath**: un valor booleano que indica si el campo RootPath especifica una ruta de acceso en la que se va a realizar la actualización.</span><span class="sxs-lookup"><span data-stu-id="8457e-2982">**\_fRootPath**: A boolean value indicating if the RootPath field specifies a path on which to perform the update.</span></span> <span data-ttu-id="8457e-2983">Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-2983">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="8457e-2984">Este campo debe establecerse en 0x00000001 o 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-2984">This field MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="8457e-2985">Si se establece en 0x00000001, se incluye en RootPath una ruta de acceso en la que se va a realizar la actualización.</span><span class="sxs-lookup"><span data-stu-id="8457e-2985">If set to 0x00000001, then a path on which to perform the update is included in RootPath.</span></span> <span data-ttu-id="8457e-2986">Si se establece en 0x00000000, la actualización se realizará en todas las rutas de acceso indizadas.</span><span class="sxs-lookup"><span data-stu-id="8457e-2986">If set to 0x00000000, then the update is to be performed on all indexed paths.</span></span>

<span data-ttu-id="8457e-2987">**RootPath**: nombre de la ruta de acceso que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="8457e-2987">**RootPath**: The name of the path to be updated.</span></span> <span data-ttu-id="8457e-2988">Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-2988">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="8457e-2989">El nombre debe ser una cadena Unicode terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="8457e-2989">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="8457e-2990">Este campo se debe omitir si \_ fRootPath está establecido en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-2990">This field MUST be omitted if \_fRootPath is set to 0x00000000.</span></span>

### <a name="2235-cpmforcemergein"></a><span data-ttu-id="8457e-2991">2.2.3.5 CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="8457e-2991">2.2.3.5 CPMForceMergeIn</span></span>

<span data-ttu-id="8457e-2992">El mensaje CPMForceMergeIn solicita a un servidor que realice el mantenimiento necesario para mejorar el rendimiento de las consultas.</span><span class="sxs-lookup"><span data-stu-id="8457e-2992">The CPMForceMergeIn message requests a server to perform any maintenance necessary to improve query performance.</span></span> <span data-ttu-id="8457e-2993">El servidor responderá con el encabezado del mensaje del mensaje CPMForceMergeIn, con los resultados de la solicitud contenidos en el \_ campo Estado.</span><span class="sxs-lookup"><span data-stu-id="8457e-2993">The server will reply with the message header of the CPMForceMergeIn message, with the results of the request contained in the \_status field.</span></span>

<span data-ttu-id="8457e-2994">El formato del mensaje CPMForceMergeIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-2994">The format of the CPMForceMergeIn message that follows the header is:</span></span>



<span data-ttu-id="8457e-2995">0</span><span class="sxs-lookup"><span data-stu-id="8457e-2995">0</span></span>

<span data-ttu-id="8457e-2996">1</span><span class="sxs-lookup"><span data-stu-id="8457e-2996">1</span></span>

<span data-ttu-id="8457e-2997">2</span><span class="sxs-lookup"><span data-stu-id="8457e-2997">2</span></span>

<span data-ttu-id="8457e-2998">3</span><span class="sxs-lookup"><span data-stu-id="8457e-2998">3</span></span>

<span data-ttu-id="8457e-2999">4</span><span class="sxs-lookup"><span data-stu-id="8457e-2999">4</span></span>

<span data-ttu-id="8457e-3000">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3000">5</span></span>

<span data-ttu-id="8457e-3001">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3001">6</span></span>

<span data-ttu-id="8457e-3002">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3002">7</span></span>

<span data-ttu-id="8457e-3003">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3003">8</span></span>

<span data-ttu-id="8457e-3004">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3004">9</span></span>

<span data-ttu-id="8457e-3005">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3005">1</span></span><br/> <span data-ttu-id="8457e-3006">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3006">0</span></span><br/>

<span data-ttu-id="8457e-3007">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3007">1</span></span>

<span data-ttu-id="8457e-3008">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3008">2</span></span>

<span data-ttu-id="8457e-3009">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3009">3</span></span>

<span data-ttu-id="8457e-3010">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3010">4</span></span>

<span data-ttu-id="8457e-3011">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3011">5</span></span>

<span data-ttu-id="8457e-3012">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3012">6</span></span>

<span data-ttu-id="8457e-3013">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3013">7</span></span>

<span data-ttu-id="8457e-3014">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3014">8</span></span>

<span data-ttu-id="8457e-3015">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3015">9</span></span>

<span data-ttu-id="8457e-3016">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3016">2</span></span><br/> <span data-ttu-id="8457e-3017">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3017">0</span></span><br/>

<span data-ttu-id="8457e-3018">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3018">1</span></span>

<span data-ttu-id="8457e-3019">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3019">2</span></span>

<span data-ttu-id="8457e-3020">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3020">3</span></span>

<span data-ttu-id="8457e-3021">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3021">4</span></span>

<span data-ttu-id="8457e-3022">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3022">5</span></span>

<span data-ttu-id="8457e-3023">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3023">6</span></span>

<span data-ttu-id="8457e-3024">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3024">7</span></span>

<span data-ttu-id="8457e-3025">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3025">8</span></span>

<span data-ttu-id="8457e-3026">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3026">9</span></span>

<span data-ttu-id="8457e-3027">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3027">3</span></span><br/> <span data-ttu-id="8457e-3028">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3028">0</span></span><br/>

<span data-ttu-id="8457e-3029">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3029">1</span></span>

<span data-ttu-id="8457e-3030">\_bajo (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-3030">\_partID (optional)</span></span>



 

<span data-ttu-id="8457e-3031">**\_ enescribir: este** campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-3031">**\_partID**: This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="8457e-3032">Cuando este campo está presente, debe establecerse en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8457e-3032">When this field is present, it MUST be set to 0x00000001.</span></span>

### <a name="2236-cpmconnectin"></a><span data-ttu-id="8457e-3033">2.2.3.6 CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="8457e-3033">2.2.3.6 CPMConnectIn</span></span>

<span data-ttu-id="8457e-3034">El mensaje CPMConnectIn inicia una sesión entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-3034">The CPMConnectIn message begins a session between the client and server.</span></span>

<span data-ttu-id="8457e-3035">El formato del mensaje CPMConnectIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-3035">The format of the CPMConnectIn message that follows the header is:</span></span>



<span data-ttu-id="8457e-3036">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3036">0</span></span>

<span data-ttu-id="8457e-3037">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3037">1</span></span>

<span data-ttu-id="8457e-3038">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3038">2</span></span>

<span data-ttu-id="8457e-3039">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3039">3</span></span>

<span data-ttu-id="8457e-3040">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3040">4</span></span>

<span data-ttu-id="8457e-3041">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3041">5</span></span>

<span data-ttu-id="8457e-3042">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3042">6</span></span>

<span data-ttu-id="8457e-3043">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3043">7</span></span>

<span data-ttu-id="8457e-3044">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3044">8</span></span>

<span data-ttu-id="8457e-3045">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3045">9</span></span>

<span data-ttu-id="8457e-3046">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3046">1</span></span><br/> <span data-ttu-id="8457e-3047">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3047">0</span></span><br/>

<span data-ttu-id="8457e-3048">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3048">1</span></span>

<span data-ttu-id="8457e-3049">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3049">2</span></span>

<span data-ttu-id="8457e-3050">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3050">3</span></span>

<span data-ttu-id="8457e-3051">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3051">4</span></span>

<span data-ttu-id="8457e-3052">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3052">5</span></span>

<span data-ttu-id="8457e-3053">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3053">6</span></span>

<span data-ttu-id="8457e-3054">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3054">7</span></span>

<span data-ttu-id="8457e-3055">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3055">8</span></span>

<span data-ttu-id="8457e-3056">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3056">9</span></span>

<span data-ttu-id="8457e-3057">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3057">2</span></span><br/> <span data-ttu-id="8457e-3058">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3058">0</span></span><br/>

<span data-ttu-id="8457e-3059">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3059">1</span></span>

<span data-ttu-id="8457e-3060">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3060">2</span></span>

<span data-ttu-id="8457e-3061">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3061">3</span></span>

<span data-ttu-id="8457e-3062">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3062">4</span></span>

<span data-ttu-id="8457e-3063">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3063">5</span></span>

<span data-ttu-id="8457e-3064">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3064">6</span></span>

<span data-ttu-id="8457e-3065">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3065">7</span></span>

<span data-ttu-id="8457e-3066">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3066">8</span></span>

<span data-ttu-id="8457e-3067">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3067">9</span></span>

<span data-ttu-id="8457e-3068">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3068">3</span></span><br/> <span data-ttu-id="8457e-3069">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3069">0</span></span><br/>

<span data-ttu-id="8457e-3070">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3070">1</span></span>

<span data-ttu-id="8457e-3071">\_iClientVersion</span><span class="sxs-lookup"><span data-stu-id="8457e-3071">\_iClientVersion</span></span>

<span data-ttu-id="8457e-3072">\_fClientIsRemote</span><span class="sxs-lookup"><span data-stu-id="8457e-3072">\_fClientIsRemote</span></span>

<span data-ttu-id="8457e-3073">\_cbBlob1</span><span class="sxs-lookup"><span data-stu-id="8457e-3073">\_cbBlob1</span></span>

<span data-ttu-id="8457e-3074">\_cbBlob2</span><span class="sxs-lookup"><span data-stu-id="8457e-3074">\_cbBlob2</span></span>

<span data-ttu-id="8457e-3075">\_acolcha</span><span class="sxs-lookup"><span data-stu-id="8457e-3075">\_padding</span></span>

<span data-ttu-id="8457e-3076">...</span><span class="sxs-lookup"><span data-stu-id="8457e-3076">...</span></span>

<span data-ttu-id="8457e-3077">...</span><span class="sxs-lookup"><span data-stu-id="8457e-3077">...</span></span>

<span data-ttu-id="8457e-3078">MachineName</span><span class="sxs-lookup"><span data-stu-id="8457e-3078">MachineName</span></span>

<span data-ttu-id="8457e-3079">... variable</span><span class="sxs-lookup"><span data-stu-id="8457e-3079">... (variable)</span></span>

<span data-ttu-id="8457e-3080">UserName</span><span class="sxs-lookup"><span data-stu-id="8457e-3080">UserName</span></span>

<span data-ttu-id="8457e-3081">... variable</span><span class="sxs-lookup"><span data-stu-id="8457e-3081">... (variable)</span></span>

<span data-ttu-id="8457e-3082">\_paddingcPropSets (opcional, variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-3082">\_paddingcPropSets (optional, variable)</span></span>

<span data-ttu-id="8457e-3083">cPropSets</span><span class="sxs-lookup"><span data-stu-id="8457e-3083">cPropSets</span></span>

<span data-ttu-id="8457e-3084">PropertySet1 (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-3084">PropertySet1 (variable)</span></span>

<span data-ttu-id="8457e-3085">PropertySet2 (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-3085">PropertySet2 (variable)</span></span>

<span data-ttu-id="8457e-3086">\_paddingExtPropset (opcional, variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-3086">\_paddingExtPropset (optional, variable)</span></span>

<span data-ttu-id="8457e-3087">cExtPropSet</span><span class="sxs-lookup"><span data-stu-id="8457e-3087">cExtPropSet</span></span>

<span data-ttu-id="8457e-3088">aPropertySets (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-3088">aPropertySets (variable)</span></span>



 

<span data-ttu-id="8457e-3089">**\_ iClientVersion**: entero de 32 bits que indica si el servidor debe validar el valor de suma de comprobación especificado en el \_ campo ulChecksum de los encabezados de mensaje para los mensajes enviados por el cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3089">**\_iClientVersion**: A 32-bit integer indicating whether the server is to validate the checksum value specified in the \_ulChecksum field of the message headers for messages sent by the client.</span></span> <span data-ttu-id="8457e-3090">Si el \_ campo iClientVersion está establecido en 0x00000008 o superior, el servidor debe validar el \_ valor del campo ulChecksum para los siguientes mensajes:</span><span class="sxs-lookup"><span data-stu-id="8457e-3090">If the \_iClientVersion field is set to 0x00000008 or greater, the server MUST validate the \_ulChecksum field value for the following messages:</span></span>

-   <span data-ttu-id="8457e-3091">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="8457e-3091">CPMConnectIn</span></span>
-   <span data-ttu-id="8457e-3092">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="8457e-3092">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="8457e-3093">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="8457e-3093">CPMFetchValueIn</span></span>
-   <span data-ttu-id="8457e-3094">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="8457e-3094">CPMGetRowsIn</span></span>
-   <span data-ttu-id="8457e-3095">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="8457e-3095">CPMSetBindingsIn</span></span>

<span data-ttu-id="8457e-3096">Para obtener más información sobre cómo el servidor valida el valor especificado por el cliente en el campo ulChecksum para los mensajes enumerados anteriormente, consulte la sección 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="8457e-3096">For details about how the server validates the value specified by the client in the ulChecksum field for the messages listed above, see Section 3.2.5.</span></span>

<span data-ttu-id="8457e-3097">Si el valor es mayor que 0x00000008, se supone que el cliente es capaz de controlar desplazamientos de 64 bits en los mensajes CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-3097">If the value is greater than 0x00000008 then the client is assumed capable of handling 64-bit offsets in CPMGetRowsOut messages.</span></span> <span data-ttu-id="8457e-3098">Vea la sección 2.2.3.16 para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8457e-3098">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="8457e-3099">*Comportamiento de Windows: en los clientes de Windows, iClientVersion se establece de la manera siguiente*:</span><span class="sxs-lookup"><span data-stu-id="8457e-3099">*Windows Behavior: On Windows clients, the iClientVersion is set as follows*:</span></span>



| <span data-ttu-id="8457e-3100">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-3100">Value</span></span>      | <span data-ttu-id="8457e-3101">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-3101">Meaning</span></span>                                                              |
|------------|----------------------------------------------------------------------|
| <span data-ttu-id="8457e-3102">0x00000005</span><span class="sxs-lookup"><span data-stu-id="8457e-3102">0x00000005</span></span> | <span data-ttu-id="8457e-3103">El sistema operativo de cliente es Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8457e-3103">Client OS is Windows 2000.</span></span>                                           |
| <span data-ttu-id="8457e-3104">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8457e-3104">0x00000008</span></span> | <span data-ttu-id="8457e-3105">El sistema operativo de cliente es de 32 de Windows XP o de 32 bits de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8457e-3105">Client OS is either 32-bit Windows XP or 32-bit Windows Server 2003.</span></span> |
| <span data-ttu-id="8457e-3106">0x00010008</span><span class="sxs-lookup"><span data-stu-id="8457e-3106">0x00010008</span></span> | <span data-ttu-id="8457e-3107">El sistema operativo de cliente es de 64 de Windows XP o de 64 bits de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8457e-3107">Client OS is either 64-bit Windows XP or 64-bit Windows Server 2003.</span></span> |



 

<span data-ttu-id="8457e-3108">\_**fClientIsRemote**: un valor booleano que indica si el cliente se está ejecutando en un equipo diferente que el servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-3108">\_**fClientIsRemote**: A boolean value indicating whether the client is running on a different machine than the server.</span></span> <span data-ttu-id="8457e-3109">DEBE establecerse en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8457e-3109">MUST be set to 0x00000001.</span></span>

<span data-ttu-id="8457e-3110">\_**cbBlob1**: entero de 32 bits sin signo que indica el tamaño en bytes de los campos CPropSet, PropertySet1 y PropertySet2, combinados.</span><span class="sxs-lookup"><span data-stu-id="8457e-3110">\_**cbBlob1**: A 32-bit unsigned integer indicating the size in bytes of cPropSet, PropertySet1, and PropertySet2 fields, combined.</span></span>

<span data-ttu-id="8457e-3111">\_**cbBlob2**: entero de 32 bits sin signo que indica el tamaño en bytes de los campos CExPropSet y aPropertySet, combinados.</span><span class="sxs-lookup"><span data-stu-id="8457e-3111">\_**cbBlob2**: A 32-bit unsigned integer indicating the size in bytes of cExPropSet and aPropertySet fields, combined.</span></span>

<span data-ttu-id="8457e-3112">\_**padding**: 12 bytes de relleno que pueden contener valores arbitrarios y deben omitirse.</span><span class="sxs-lookup"><span data-stu-id="8457e-3112">\_**padding**: 12 bytes of padding which can contain arbitrary values and MUST be ignored.</span></span>

<span data-ttu-id="8457e-3113">**MachineName**: el nombre de equipo del cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3113">**MachineName**: The machine name of the client.</span></span> <span data-ttu-id="8457e-3114">La cadena de nombre debe ser una matriz terminada en NULL de menos de 512 caracteres Unicode, incluido el terminador NULL.</span><span class="sxs-lookup"><span data-stu-id="8457e-3114">The name string MUST be a null-terminated array of less than 512 Unicode characters, including the NULL terminator.</span></span>

<span data-ttu-id="8457e-3115">**Username**: una cadena que representa el nombre de usuario de la persona que ejecuta la aplicación que invocó este protocolo.</span><span class="sxs-lookup"><span data-stu-id="8457e-3115">**UserName**: A string that represents the user name of the person who is running the application that invoked this protocol.</span></span> <span data-ttu-id="8457e-3116">La cadena de nombre debe ser una matriz terminada en NULL de menos de 512 caracteres Unicode cuando se concatena con MachineName.</span><span class="sxs-lookup"><span data-stu-id="8457e-3116">The name string MUST be a null-terminated array of less than 512 Unicode characters when concatenated with MachineName.</span></span>

<span data-ttu-id="8457e-3117">**\_ paddingcPropSets**: este campo debe tener una longitud de 0 a 7 bytes.</span><span class="sxs-lookup"><span data-stu-id="8457e-3117">**\_paddingcPropSets**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="8457e-3118">El número de bytes debe ser el número necesario para que el desplazamiento de bytes del campo cPropSets desde el principio del mensaje que contiene esta estructura sea un múltiplo de 8.</span><span class="sxs-lookup"><span data-stu-id="8457e-3118">The number of bytes MUST be the number required to make the byte offset of the cPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="8457e-3119">El valor de los bytes puede ser cualquier valor arbitrario y el receptor debe pasarlo por alto.</span><span class="sxs-lookup"><span data-stu-id="8457e-3119">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8457e-3120">**cPropSets**: entero de 32 bits sin signo que indica el número de estructuras CDbPropSet que siguen a este campo.</span><span class="sxs-lookup"><span data-stu-id="8457e-3120">**cPropSets**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span> <span data-ttu-id="8457e-3121">Este valor debe establecerse en 0x0000002.</span><span class="sxs-lookup"><span data-stu-id="8457e-3121">This value MUST be set to 0x0000002.</span></span>

<span data-ttu-id="8457e-3122">**PropertySet1**: una estructura CDbPropSet con guidPropertySet que contiene DBPROPSET \_ FSCIFRMWRK \_ EXT (consulte la sección 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="8457e-3122">**PropertySet1**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_FSCIFRMWRK\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="8457e-3123">**PropertySet2**: una estructura CDbPropSet con guidPropertySet que contiene DBPROPSET \_ CIFRMWRKCORE \_ EXT (consulte la sección 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="8457e-3123">**PropertySet2**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_CIFRMWRKCORE\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="8457e-3124">\_**PaddingExtPropset**: este campo debe tener una longitud de 0 a 7 bytes.</span><span class="sxs-lookup"><span data-stu-id="8457e-3124">\_**PaddingExtPropset**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="8457e-3125">El número de bytes debe ser el número necesario para que el desplazamiento de bytes del campo cExtPropSets desde el principio del mensaje que contiene esta estructura sea un múltiplo de 8.</span><span class="sxs-lookup"><span data-stu-id="8457e-3125">The number of bytes MUST be the number required to make the byte offset of the cExtPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="8457e-3126">El valor de los bytes puede ser cualquier valor arbitrario y el receptor debe pasarlo por alto.</span><span class="sxs-lookup"><span data-stu-id="8457e-3126">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8457e-3127">**cExtPropSet**: entero de 32 bits sin signo que indica el número de estructuras CDbPropSet que siguen a este campo.</span><span class="sxs-lookup"><span data-stu-id="8457e-3127">**cExtPropSet**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span>

<span data-ttu-id="8457e-3128">**aPropertySets**: una matriz de estructuras CDbPropSet que especifica otras propiedades.</span><span class="sxs-lookup"><span data-stu-id="8457e-3128">**aPropertySets**: An array of CDbPropSet structures specifying other properties.</span></span> <span data-ttu-id="8457e-3129">El número de elementos de esta matriz debe ser igual a cExtPropSet.</span><span class="sxs-lookup"><span data-stu-id="8457e-3129">The number of elements in this array MUST be equal to cExtPropSet.</span></span>

### <a name="2237-cpmconnectout"></a><span data-ttu-id="8457e-3130">2.2.3.7 CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="8457e-3130">2.2.3.7 CPMConnectOut</span></span>

<span data-ttu-id="8457e-3131">El mensaje CPMConnectOut contiene una respuesta a un mensaje CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-3131">The CPMConnectOut message contains a response to a CPMConnectIn message.</span></span>

<span data-ttu-id="8457e-3132">El formato del mensaje CPMConnectOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-3132">The format of the CPMConnectOut message that follows the header is:</span></span>



<span data-ttu-id="8457e-3133">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3133">0</span></span>

<span data-ttu-id="8457e-3134">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3134">1</span></span>

<span data-ttu-id="8457e-3135">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3135">2</span></span>

<span data-ttu-id="8457e-3136">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3136">3</span></span>

<span data-ttu-id="8457e-3137">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3137">4</span></span>

<span data-ttu-id="8457e-3138">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3138">5</span></span>

<span data-ttu-id="8457e-3139">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3139">6</span></span>

<span data-ttu-id="8457e-3140">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3140">7</span></span>

<span data-ttu-id="8457e-3141">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3141">8</span></span>

<span data-ttu-id="8457e-3142">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3142">9</span></span>

<span data-ttu-id="8457e-3143">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3143">1</span></span><br/> <span data-ttu-id="8457e-3144">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3144">0</span></span><br/>

<span data-ttu-id="8457e-3145">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3145">1</span></span>

<span data-ttu-id="8457e-3146">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3146">2</span></span>

<span data-ttu-id="8457e-3147">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3147">3</span></span>

<span data-ttu-id="8457e-3148">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3148">4</span></span>

<span data-ttu-id="8457e-3149">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3149">5</span></span>

<span data-ttu-id="8457e-3150">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3150">6</span></span>

<span data-ttu-id="8457e-3151">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3151">7</span></span>

<span data-ttu-id="8457e-3152">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3152">8</span></span>

<span data-ttu-id="8457e-3153">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3153">9</span></span>

<span data-ttu-id="8457e-3154">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3154">2</span></span><br/> <span data-ttu-id="8457e-3155">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3155">0</span></span><br/>

<span data-ttu-id="8457e-3156">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3156">1</span></span>

<span data-ttu-id="8457e-3157">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3157">2</span></span>

<span data-ttu-id="8457e-3158">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3158">3</span></span>

<span data-ttu-id="8457e-3159">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3159">4</span></span>

<span data-ttu-id="8457e-3160">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3160">5</span></span>

<span data-ttu-id="8457e-3161">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3161">6</span></span>

<span data-ttu-id="8457e-3162">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3162">7</span></span>

<span data-ttu-id="8457e-3163">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3163">8</span></span>

<span data-ttu-id="8457e-3164">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3164">9</span></span>

<span data-ttu-id="8457e-3165">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3165">3</span></span><br/> <span data-ttu-id="8457e-3166">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3166">0</span></span><br/>

<span data-ttu-id="8457e-3167">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3167">1</span></span>

<span data-ttu-id="8457e-3168">\_serverVersion</span><span class="sxs-lookup"><span data-stu-id="8457e-3168">\_serverVersion</span></span>

<span data-ttu-id="8457e-3169">\_reservado (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-3169">\_reserved (variable)</span></span>



 

<span data-ttu-id="8457e-3170">**\_ serverVersion**:</span><span class="sxs-lookup"><span data-stu-id="8457e-3170">**\_serverVersion**:</span></span>

<span data-ttu-id="8457e-3171">Entero de 32 bits, que indica si el servidor puede admitir desplazamientos de 64 bits *.*</span><span class="sxs-lookup"><span data-stu-id="8457e-3171">A 32-bit integer, indicating whether the server can support 64-bit offsets *.*</span></span> <span data-ttu-id="8457e-3172">Vea la sección 2.2.3.16 para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8457e-3172">See section 2.2.3.16 for details.</span></span>



| <span data-ttu-id="8457e-3173">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-3173">Value</span></span>      | <span data-ttu-id="8457e-3174">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-3174">Meaning</span></span>                                 |
|------------|-----------------------------------------|
| <span data-ttu-id="8457e-3175">0x00000007</span><span class="sxs-lookup"><span data-stu-id="8457e-3175">0x00000007</span></span> | <span data-ttu-id="8457e-3176">El servidor solo puede enviar desplazamientos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8457e-3176">Server is can only send 32-bit offsets.</span></span> |
| <span data-ttu-id="8457e-3177">0x00010007</span><span class="sxs-lookup"><span data-stu-id="8457e-3177">0x00010007</span></span> | <span data-ttu-id="8457e-3178">El servidor puede enviar desplazamientos de 32 o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8457e-3178">Server can send 32 or 64-bit offsets.</span></span>   |



 

<span data-ttu-id="8457e-3179">**\_ reservado**: reservado.</span><span class="sxs-lookup"><span data-stu-id="8457e-3179">**\_reserved**: Reserved.</span></span> <span data-ttu-id="8457e-3180">El servidor puede enviar un número arbitrario de valores arbitrarios y el cliente debe omitir estos valores si están presentes.</span><span class="sxs-lookup"><span data-stu-id="8457e-3180">The server MAY send an arbitrary number of arbitrary values and the client MUST ignore these values if present.</span></span>

### <a name="2238-cpmcreatequeryin"></a><span data-ttu-id="8457e-3181">2.2.3.8 CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="8457e-3181">2.2.3.8 CPMCreateQueryIn</span></span>

<span data-ttu-id="8457e-3182">El mensaje CPMCreateQueryIn crea una nueva consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3182">The CPMCreateQueryIn message creates a new query.</span></span> <span data-ttu-id="8457e-3183">El formato del mensaje CPMCreateQueryIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-3183">The format of the CPMCreateQueryIn message that follows the header is:</span></span>



<span data-ttu-id="8457e-3184">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3184">0</span></span>

<span data-ttu-id="8457e-3185">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3185">1</span></span>

<span data-ttu-id="8457e-3186">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3186">2</span></span>

<span data-ttu-id="8457e-3187">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3187">3</span></span>

<span data-ttu-id="8457e-3188">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3188">4</span></span>

<span data-ttu-id="8457e-3189">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3189">5</span></span>

<span data-ttu-id="8457e-3190">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3190">6</span></span>

<span data-ttu-id="8457e-3191">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3191">7</span></span>

<span data-ttu-id="8457e-3192">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3192">8</span></span>

<span data-ttu-id="8457e-3193">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3193">9</span></span>

<span data-ttu-id="8457e-3194">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3194">1</span></span><br/> <span data-ttu-id="8457e-3195">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3195">0</span></span><br/>

<span data-ttu-id="8457e-3196">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3196">1</span></span>

<span data-ttu-id="8457e-3197">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3197">2</span></span>

<span data-ttu-id="8457e-3198">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3198">3</span></span>

<span data-ttu-id="8457e-3199">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3199">4</span></span>

<span data-ttu-id="8457e-3200">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3200">5</span></span>

<span data-ttu-id="8457e-3201">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3201">6</span></span>

<span data-ttu-id="8457e-3202">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3202">7</span></span>

<span data-ttu-id="8457e-3203">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3203">8</span></span>

<span data-ttu-id="8457e-3204">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3204">9</span></span>

<span data-ttu-id="8457e-3205">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3205">2</span></span><br/> <span data-ttu-id="8457e-3206">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3206">0</span></span><br/>

<span data-ttu-id="8457e-3207">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3207">1</span></span>

<span data-ttu-id="8457e-3208">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3208">2</span></span>

<span data-ttu-id="8457e-3209">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3209">3</span></span>

<span data-ttu-id="8457e-3210">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3210">4</span></span>

<span data-ttu-id="8457e-3211">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3211">5</span></span>

<span data-ttu-id="8457e-3212">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3212">6</span></span>

<span data-ttu-id="8457e-3213">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3213">7</span></span>

<span data-ttu-id="8457e-3214">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3214">8</span></span>

<span data-ttu-id="8457e-3215">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3215">9</span></span>

<span data-ttu-id="8457e-3216">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3216">3</span></span><br/> <span data-ttu-id="8457e-3217">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3217">0</span></span><br/>

<span data-ttu-id="8457e-3218">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3218">1</span></span>

<span data-ttu-id="8457e-3219">Tamaño</span><span class="sxs-lookup"><span data-stu-id="8457e-3219">Size</span></span>

<span data-ttu-id="8457e-3220">CColumnSetPresent</span><span class="sxs-lookup"><span data-stu-id="8457e-3220">CColumnSetPresent</span></span>

<span data-ttu-id="8457e-3221">ColumnSet (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-3221">ColumnSet (optional)</span></span>

<span data-ttu-id="8457e-3222">... variable</span><span class="sxs-lookup"><span data-stu-id="8457e-3222">... (variable)</span></span>

<span data-ttu-id="8457e-3223">CRestrictionPresent.</span><span class="sxs-lookup"><span data-stu-id="8457e-3223">CRestrictionPresent.</span></span>

<span data-ttu-id="8457e-3224">Restricción (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-3224">Restriction (optional)</span></span>

<span data-ttu-id="8457e-3225">... variable</span><span class="sxs-lookup"><span data-stu-id="8457e-3225">... (variable)</span></span>

<span data-ttu-id="8457e-3226">CSortSetPresent</span><span class="sxs-lookup"><span data-stu-id="8457e-3226">CSortSetPresent</span></span>

<span data-ttu-id="8457e-3227">SortSet (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-3227">SortSet (optional)</span></span>

<span data-ttu-id="8457e-3228">... variable</span><span class="sxs-lookup"><span data-stu-id="8457e-3228">... (variable)</span></span>

<span data-ttu-id="8457e-3229">CCategorizationSetPresent</span><span class="sxs-lookup"><span data-stu-id="8457e-3229">CCategorizationSetPresent</span></span>

<span data-ttu-id="8457e-3230">CategorizationSet (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-3230">CategorizationSet (optional)</span></span>

<span data-ttu-id="8457e-3231">... variable</span><span class="sxs-lookup"><span data-stu-id="8457e-3231">... (variable)</span></span>

<span data-ttu-id="8457e-3232">RowSetProperties</span><span class="sxs-lookup"><span data-stu-id="8457e-3232">RowSetProperties</span></span>

<span data-ttu-id="8457e-3233">...</span><span class="sxs-lookup"><span data-stu-id="8457e-3233">...</span></span>

<span data-ttu-id="8457e-3234">...</span><span class="sxs-lookup"><span data-stu-id="8457e-3234">...</span></span>

<span data-ttu-id="8457e-3235">...</span><span class="sxs-lookup"><span data-stu-id="8457e-3235">...</span></span>

<span data-ttu-id="8457e-3236">...</span><span class="sxs-lookup"><span data-stu-id="8457e-3236">...</span></span>

<span data-ttu-id="8457e-3237">PidMapper (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-3237">PidMapper (variable)</span></span>



 

<span data-ttu-id="8457e-3238">**Tamaño**: entero de 32 bits sin signo que indica el número de bytes desde el principio de este campo hasta el final del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-3238">**Size**: A 32-bit unsigned integer indicating the number of bytes from the beginning of this field to the end of the message.</span></span>

<span data-ttu-id="8457e-3239">**CColumnSetPresent**: un campo de byte que indica si el campo ColumnSet está presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3239">**CColumnSetPresent**: A byte field indicating if the ColumnSet field is present.</span></span> <span data-ttu-id="8457e-3240">Este campo debe establecerse en 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="8457e-3240">This field MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="8457e-3241">Si se establece en 0x01, el campo CColumnSet debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3241">If set to 0x01 the CColumnSet field MUST be present.</span></span> <span data-ttu-id="8457e-3242">Si se establece en 0x00, debe estar ausente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3242">If set to 0x00, it MUST be absent.</span></span>

<span data-ttu-id="8457e-3243">**ColumnSet**: estructura CColumnSet que contiene los números de columna en los que se van a devolver las propiedades de CPidMapper.</span><span class="sxs-lookup"><span data-stu-id="8457e-3243">**ColumnSet**: A CColumnSet structure containing the column numbers in which the properties of CPidMapper is to be returned.</span></span>

<span data-ttu-id="8457e-3244">**CRestrictionPresent**: un campo de byte que indica si el campo de restricción está presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3244">**CRestrictionPresent**: A byte field indicating if the Restriction field is present.</span></span> <span data-ttu-id="8457e-3245">Si se establece en un valor distinto de cero, el campo de restricción debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3245">If set to any nonzero value, the Restriction field MUST be present.</span></span> <span data-ttu-id="8457e-3246">Si se establece en 0x00, la restricción debe estar ausente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3246">If set to 0x00, Restriction MUST be absent.</span></span>

<span data-ttu-id="8457e-3247">**Restriction**: una estructura CRestriction que contiene el árbol de comandos de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3247">**Restriction**: A CRestriction structure containing the command tree of the query.</span></span>

<span data-ttu-id="8457e-3248">**CSortSetPresent**: un campo de byte que indica si el campo SortSet está presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3248">**CSortSetPresent**: A byte field indicating if the SortSet field is present.</span></span> <span data-ttu-id="8457e-3249">Si se establece en un valor distinto de cero, el campo SortSet debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3249">If set to any nonzero value, the SortSet field MUST be present.</span></span> <span data-ttu-id="8457e-3250">Si se establece en 0x00, SortSet debe estar ausente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3250">If set to 0x00, SortSet MUST be absent.</span></span>

<span data-ttu-id="8457e-3251">**SortSet**: una estructura CSortSet que indica el criterio de ordenación de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3251">**SortSet**: A CSortSet structure indicating the sort order of the query.</span></span>

<span data-ttu-id="8457e-3252">**CCategorizationSetPresent**: un campo de byte que indica si el campo CCategorizationSet está presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3252">**CCategorizationSetPresent**: A byte field indicating if the CCategorizationSet field is present.</span></span> <span data-ttu-id="8457e-3253">Si se establece en un valor distinto de cero, el campo CCategorizationSet debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3253">If set to any nonzero value, the CCategorizationSet field MUST be present.</span></span> <span data-ttu-id="8457e-3254">Si se establece en 0x00, CCategorizationSet debe estar ausente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3254">If set to 0x00, CCategorizationSet MUST be absent.</span></span>

<span data-ttu-id="8457e-3255">**CCategorizationSet**: una estructura CCategorizationSet que contiene los grupos de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3255">**CCategorizationSet**: A CCategorizationSet structure that contains the groups for the query.</span></span>

<span data-ttu-id="8457e-3256">**RowSetProperties**: una estructura CRowsetProperties que proporciona información de configuración para la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3256">**RowSetProperties**: A CRowsetProperties structure providing configuration information for the query.</span></span>

<span data-ttu-id="8457e-3257">**PidMapper**: estructura CPidMapper que contiene las propiedades que se van a devolver en un conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-3257">**PidMapper**: A CPidMapper structure containing properties to return in a rowset.</span></span>

### <a name="2239-cpmcreatequeryout"></a><span data-ttu-id="8457e-3258">2.2.3.9 CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="8457e-3258">2.2.3.9 CPMCreateQueryOut</span></span>

<span data-ttu-id="8457e-3259">El mensaje CPMCreateQueryOut contiene una respuesta a un mensaje CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-3259">The CPMCreateQueryOut message contains a response to a CPMCreateQueryIn message.</span></span>

<span data-ttu-id="8457e-3260">El formato del mensaje CPMCreateQueryOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-3260">The format of the CPMCreateQueryOut message that follows the header is:</span></span>



<span data-ttu-id="8457e-3261">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3261">0</span></span>

<span data-ttu-id="8457e-3262">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3262">1</span></span>

<span data-ttu-id="8457e-3263">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3263">2</span></span>

<span data-ttu-id="8457e-3264">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3264">3</span></span>

<span data-ttu-id="8457e-3265">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3265">4</span></span>

<span data-ttu-id="8457e-3266">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3266">5</span></span>

<span data-ttu-id="8457e-3267">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3267">6</span></span>

<span data-ttu-id="8457e-3268">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3268">7</span></span>

<span data-ttu-id="8457e-3269">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3269">8</span></span>

<span data-ttu-id="8457e-3270">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3270">9</span></span>

<span data-ttu-id="8457e-3271">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3271">1</span></span><br/> <span data-ttu-id="8457e-3272">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3272">0</span></span><br/>

<span data-ttu-id="8457e-3273">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3273">1</span></span>

<span data-ttu-id="8457e-3274">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3274">2</span></span>

<span data-ttu-id="8457e-3275">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3275">3</span></span>

<span data-ttu-id="8457e-3276">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3276">4</span></span>

<span data-ttu-id="8457e-3277">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3277">5</span></span>

<span data-ttu-id="8457e-3278">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3278">6</span></span>

<span data-ttu-id="8457e-3279">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3279">7</span></span>

<span data-ttu-id="8457e-3280">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3280">8</span></span>

<span data-ttu-id="8457e-3281">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3281">9</span></span>

<span data-ttu-id="8457e-3282">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3282">2</span></span><br/> <span data-ttu-id="8457e-3283">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3283">0</span></span><br/>

<span data-ttu-id="8457e-3284">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3284">1</span></span>

<span data-ttu-id="8457e-3285">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3285">2</span></span>

<span data-ttu-id="8457e-3286">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3286">3</span></span>

<span data-ttu-id="8457e-3287">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3287">4</span></span>

<span data-ttu-id="8457e-3288">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3288">5</span></span>

<span data-ttu-id="8457e-3289">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3289">6</span></span>

<span data-ttu-id="8457e-3290">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3290">7</span></span>

<span data-ttu-id="8457e-3291">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3291">8</span></span>

<span data-ttu-id="8457e-3292">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3292">9</span></span>

<span data-ttu-id="8457e-3293">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3293">3</span></span><br/> <span data-ttu-id="8457e-3294">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3294">0</span></span><br/>

<span data-ttu-id="8457e-3295">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3295">1</span></span>

<span data-ttu-id="8457e-3296">\_fTrueSequential</span><span class="sxs-lookup"><span data-stu-id="8457e-3296">\_fTrueSequential</span></span>

<span data-ttu-id="8457e-3297">\_fWorkIdUnique</span><span class="sxs-lookup"><span data-stu-id="8457e-3297">\_fWorkIdUnique</span></span>

<span data-ttu-id="8457e-3298">aCursors</span><span class="sxs-lookup"><span data-stu-id="8457e-3298">aCursors</span></span>



 

<span data-ttu-id="8457e-3299">**\_ fTrueSequential**: un valor booleano informativo que indica si se puede esperar que la consulta proporcione resultados más rápido.</span><span class="sxs-lookup"><span data-stu-id="8457e-3299">**\_fTrueSequential**: An informative boolean value indicating if the query can be expected to provide results faster.</span></span> <span data-ttu-id="8457e-3300">Cuando se establece en 0x00000001 para la consulta proporcionada en CPMCreateQueryIn, el servidor puede usar el índice de tal forma que los resultados de la consulta se entreguen más rápido.</span><span class="sxs-lookup"><span data-stu-id="8457e-3300">When set to 0x00000001 for the query provided in CPMCreateQueryIn, the server can use the index in such a way that query results will likely be delivered faster.</span></span> <span data-ttu-id="8457e-3301">Cuando se establece en 0x00000000, habrá una latencia mayor en la entrega de los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3301">When set to 0x00000000, there would be a bigger latency in delivering query results.</span></span> <span data-ttu-id="8457e-3302">No debe establecerse en ningún otro valor.</span><span class="sxs-lookup"><span data-stu-id="8457e-3302">MUST not be set to any other value.</span></span>

<span data-ttu-id="8457e-3303">**\_ fWorkIdUnique**: un valor booleano que indica si los identificadores de documento a los que apuntan los cursores son únicos en todos los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3303">**\_fWorkIdUnique**: A boolean value indicating if the document identifiers pointed by the cursors are unique throughout query results.</span></span> <span data-ttu-id="8457e-3304">Si se establece en 0x00000001, los identificadores son únicos.</span><span class="sxs-lookup"><span data-stu-id="8457e-3304">If set to 0x00000001, the identifiers are unique.</span></span> <span data-ttu-id="8457e-3305">Si se establece en 0x00000000, solo son únicos en todo el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-3305">If set to 0x00000000, they are unique only throughout the rowset.</span></span>

<span data-ttu-id="8457e-3306">**aCursors**: matriz de enteros de 32 bits sin signo que representa los identificadores de los cursores, con el número de elementos igual al número de categorías en el campo CategorizationSet del mensaje CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-3306">**aCursors**: An array of 32-bit unsigned integers representing the handles to cursors, with the number of elements equal to the number of categories in the CategorizationSet field of CPMCreateQueryIn message.</span></span>

### <a name="22310-cpmgetquerystatusin"></a><span data-ttu-id="8457e-3307">2.2.3.10 CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="8457e-3307">2.2.3.10 CPMGetQueryStatusIn</span></span>

<span data-ttu-id="8457e-3308">El mensaje CPMGetQueryStatusIn solicita el estado de una consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3308">The CPMGetQueryStatusIn message requests the status of a query.</span></span> <span data-ttu-id="8457e-3309">El formato del mensaje CPMGetQueryStatusIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-3309">The format of the CPMGetQueryStatusIn message that follows the header is:</span></span>



<span data-ttu-id="8457e-3310">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3310">0</span></span>

<span data-ttu-id="8457e-3311">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3311">1</span></span>

<span data-ttu-id="8457e-3312">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3312">2</span></span>

<span data-ttu-id="8457e-3313">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3313">3</span></span>

<span data-ttu-id="8457e-3314">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3314">4</span></span>

<span data-ttu-id="8457e-3315">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3315">5</span></span>

<span data-ttu-id="8457e-3316">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3316">6</span></span>

<span data-ttu-id="8457e-3317">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3317">7</span></span>

<span data-ttu-id="8457e-3318">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3318">8</span></span>

<span data-ttu-id="8457e-3319">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3319">9</span></span>

<span data-ttu-id="8457e-3320">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3320">1</span></span><br/> <span data-ttu-id="8457e-3321">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3321">0</span></span><br/>

<span data-ttu-id="8457e-3322">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3322">1</span></span>

<span data-ttu-id="8457e-3323">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3323">2</span></span>

<span data-ttu-id="8457e-3324">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3324">3</span></span>

<span data-ttu-id="8457e-3325">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3325">4</span></span>

<span data-ttu-id="8457e-3326">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3326">5</span></span>

<span data-ttu-id="8457e-3327">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3327">6</span></span>

<span data-ttu-id="8457e-3328">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3328">7</span></span>

<span data-ttu-id="8457e-3329">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3329">8</span></span>

<span data-ttu-id="8457e-3330">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3330">9</span></span>

<span data-ttu-id="8457e-3331">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3331">2</span></span><br/> <span data-ttu-id="8457e-3332">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3332">0</span></span><br/>

<span data-ttu-id="8457e-3333">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3333">1</span></span>

<span data-ttu-id="8457e-3334">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3334">2</span></span>

<span data-ttu-id="8457e-3335">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3335">3</span></span>

<span data-ttu-id="8457e-3336">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3336">4</span></span>

<span data-ttu-id="8457e-3337">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3337">5</span></span>

<span data-ttu-id="8457e-3338">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3338">6</span></span>

<span data-ttu-id="8457e-3339">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3339">7</span></span>

<span data-ttu-id="8457e-3340">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3340">8</span></span>

<span data-ttu-id="8457e-3341">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3341">9</span></span>

<span data-ttu-id="8457e-3342">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3342">3</span></span><br/> <span data-ttu-id="8457e-3343">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3343">0</span></span><br/>

<span data-ttu-id="8457e-3344">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3344">1</span></span>

<span data-ttu-id="8457e-3345">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="8457e-3345">\_hCursor</span></span>



 

<span data-ttu-id="8457e-3346">**\_ hCursor**: entero de 32 bits sin signo que representa el identificador del mensaje CPMCreateQueryOut que identifica la consulta para la que se va a recuperar información de estado.</span><span class="sxs-lookup"><span data-stu-id="8457e-3346">**\_hCursor**: A 32-bit unsigned integer representing the handle from CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

### <a name="22311-cpmgetquerystatusout"></a><span data-ttu-id="8457e-3347">2.2.3.11 CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="8457e-3347">2.2.3.11 CPMGetQueryStatusOut</span></span>

<span data-ttu-id="8457e-3348">El mensaje CPMGetQueryStatusOut responde a un mensaje CPMGetQueryStatusIn con el estado de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3348">The CPMGetQueryStatusOut message replies to a CPMGetQueryStatusIn message with the status of the query.</span></span> <span data-ttu-id="8457e-3349">El formato del mensaje CPMGetQueryStatusOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-3349">The format of the CPMGetQueryStatusOut message that follows the header is:</span></span>



<span data-ttu-id="8457e-3350">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3350">0</span></span>

<span data-ttu-id="8457e-3351">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3351">1</span></span>

<span data-ttu-id="8457e-3352">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3352">2</span></span>

<span data-ttu-id="8457e-3353">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3353">3</span></span>

<span data-ttu-id="8457e-3354">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3354">4</span></span>

<span data-ttu-id="8457e-3355">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3355">5</span></span>

<span data-ttu-id="8457e-3356">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3356">6</span></span>

<span data-ttu-id="8457e-3357">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3357">7</span></span>

<span data-ttu-id="8457e-3358">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3358">8</span></span>

<span data-ttu-id="8457e-3359">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3359">9</span></span>

<span data-ttu-id="8457e-3360">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3360">1</span></span><br/> <span data-ttu-id="8457e-3361">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3361">0</span></span><br/>

<span data-ttu-id="8457e-3362">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3362">1</span></span>

<span data-ttu-id="8457e-3363">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3363">2</span></span>

<span data-ttu-id="8457e-3364">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3364">3</span></span>

<span data-ttu-id="8457e-3365">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3365">4</span></span>

<span data-ttu-id="8457e-3366">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3366">5</span></span>

<span data-ttu-id="8457e-3367">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3367">6</span></span>

<span data-ttu-id="8457e-3368">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3368">7</span></span>

<span data-ttu-id="8457e-3369">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3369">8</span></span>

<span data-ttu-id="8457e-3370">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3370">9</span></span>

<span data-ttu-id="8457e-3371">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3371">2</span></span><br/> <span data-ttu-id="8457e-3372">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3372">0</span></span><br/>

<span data-ttu-id="8457e-3373">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3373">1</span></span>

<span data-ttu-id="8457e-3374">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3374">2</span></span>

<span data-ttu-id="8457e-3375">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3375">3</span></span>

<span data-ttu-id="8457e-3376">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3376">4</span></span>

<span data-ttu-id="8457e-3377">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3377">5</span></span>

<span data-ttu-id="8457e-3378">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3378">6</span></span>

<span data-ttu-id="8457e-3379">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3379">7</span></span>

<span data-ttu-id="8457e-3380">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3380">8</span></span>

<span data-ttu-id="8457e-3381">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3381">9</span></span>

<span data-ttu-id="8457e-3382">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3382">3</span></span><br/> <span data-ttu-id="8457e-3383">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3383">0</span></span><br/>

<span data-ttu-id="8457e-3384">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3384">1</span></span>

<span data-ttu-id="8457e-3385">\_Status</span><span class="sxs-lookup"><span data-stu-id="8457e-3385">\_Status</span></span>



 

<span data-ttu-id="8457e-3386">**\_ Status**: máscara de máscara de valores definidos en las tablas siguientes, que describe la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3386">**\_Status**: A bitmask of values defined in the tables below, that describes the query.</span></span>

<span data-ttu-id="8457e-3387">En la tabla siguiente se enumeran \_ \* los valores estadísticos obtenidos realizando una operación and bit a bit \_ con el estado con 0x00000007.</span><span class="sxs-lookup"><span data-stu-id="8457e-3387">The following table lists STAT\_\* values obtained by performing a bitwise AND operation on \_Status with 0x00000007.</span></span> <span data-ttu-id="8457e-3388">El resultado debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="8457e-3388">The result MUST be one of the following:</span></span>



| <span data-ttu-id="8457e-3389">Constante</span><span class="sxs-lookup"><span data-stu-id="8457e-3389">Constant</span></span>                 | <span data-ttu-id="8457e-3390">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-3390">Meaning</span></span>                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-3391">STAT \_ busy ocupado</span><span class="sxs-lookup"><span data-stu-id="8457e-3391">STAT\_BUSY 0x00000000</span></span>    | <span data-ttu-id="8457e-3392">La consulta asincrónica todavía se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="8457e-3392">The asynchronous query is still running.</span></span>                                          |
| <span data-ttu-id="8457e-3393">ERROR de STAT \_ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-3393">STAT\_ERROR 0x00000001</span></span>   | <span data-ttu-id="8457e-3394">La consulta está en un estado de error.</span><span class="sxs-lookup"><span data-stu-id="8457e-3394">The query is in an error state.</span></span>                                                   |
| <span data-ttu-id="8457e-3395">STAT \_ Done 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8457e-3395">STAT\_DONE 0x00000002</span></span>    | <span data-ttu-id="8457e-3396">La consulta se ha completado.</span><span class="sxs-lookup"><span data-stu-id="8457e-3396">The query is complete.</span></span>                                                            |
| <span data-ttu-id="8457e-3397">\_Actualizar la actualización de 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8457e-3397">STAT\_REFRESH 0x00000003</span></span> | <span data-ttu-id="8457e-3398">La consulta se ha completado, pero las actualizaciones tienen como resultado un cálculo de consulta adicional.</span><span class="sxs-lookup"><span data-stu-id="8457e-3398">The query is complete, but updates are resulting in additional query computation.</span></span> |



 

<span data-ttu-id="8457e-3399">En la tabla siguiente se enumeran los \_ \* bits de estadísticas adicionales que se pueden establecer de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3399">The following table lists additional STAT\_\* bits that can be set independently.</span></span>



| <span data-ttu-id="8457e-3400">Constante</span><span class="sxs-lookup"><span data-stu-id="8457e-3400">Constant</span></span>                                    | <span data-ttu-id="8457e-3401">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-3401">Meaning</span></span>                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8457e-3402">\_Palabras irrelevantes de estadísticas \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="8457e-3402">STAT\_NOISE\_WORDS 0x00000010</span></span>               | <span data-ttu-id="8457e-3403">Las palabras irrelevantes se reemplazaron por caracteres comodín en la consulta de contenido.</span><span class="sxs-lookup"><span data-stu-id="8457e-3403">Noise words were replaced by wildcard characters in the content query.</span></span>                                                              |
| <span data-ttu-id="8457e-3404">\_Contenido estadístico \_ no \_ \_ actualizado</span><span class="sxs-lookup"><span data-stu-id="8457e-3404">STAT\_CONTENT\_OUT\_OF\_DATE 0x00000020</span></span>     | <span data-ttu-id="8457e-3405">Los resultados de la consulta podrían ser incorrectos porque la consulta implicaba archivos modificados, pero no indexados.</span><span class="sxs-lookup"><span data-stu-id="8457e-3405">The results of the query might be incorrect because the query involved modified, but un-indexed, files.</span></span>                             |
| <span data-ttu-id="8457e-3406">ESTADÍSTICAS de \_ actualización \_ incompleta 0x00000040</span><span class="sxs-lookup"><span data-stu-id="8457e-3406">STAT\_REFRESH\_INCOMPLETE 0x00000040</span></span>        | <span data-ttu-id="8457e-3407">Los resultados de la consulta podrían ser incorrectos porque la consulta contenía archivos modificados y reindexados cuyo contenido no se incluía.</span><span class="sxs-lookup"><span data-stu-id="8457e-3407">The results of the query might be incorrect because the query involved modified and re-indexed files whose content wasn't included.</span></span> |
| <span data-ttu-id="8457e-3408">Consulta de contenido de STAT \_ \_ \_ incompleta 0x00000080</span><span class="sxs-lookup"><span data-stu-id="8457e-3408">STAT\_CONTENT\_QUERY\_INCOMPLETE 0x00000080</span></span> | <span data-ttu-id="8457e-3409">La consulta de contenido era demasiado compleja para completarse o era necesaria para la enumeración en lugar de usar el índice de contenido.</span><span class="sxs-lookup"><span data-stu-id="8457e-3409">The content query was too complex to complete or required enumeration instead of use of the content index.</span></span>                          |
| <span data-ttu-id="8457e-3410">Límite de tiempo de STAT \_ \_ \_ superado 0x00000100</span><span class="sxs-lookup"><span data-stu-id="8457e-3410">STAT\_TIME\_LIMIT\_EXCEEDED 0x00000100</span></span>      | <span data-ttu-id="8457e-3411">Los resultados de la consulta pueden ser incorrectos porque el tiempo de ejecución de la consulta alcanzó el tiempo máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="8457e-3411">The results of the query might be incorrect because the query execution time reached the maximum allowable time.</span></span>                    |



 

### <a name="22312-cpmgetquerystatusexin"></a><span data-ttu-id="8457e-3412">2.2.3.12 CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="8457e-3412">2.2.3.12 CPMGetQueryStatusExIn</span></span>

<span data-ttu-id="8457e-3413">El mensaje CPMGetQueryStatusExIn solicita el estado de una consulta e información adicional, como el número de documentos que se han indizado, el número de documentos que quedan por indizar, etc.</span><span class="sxs-lookup"><span data-stu-id="8457e-3413">The CPMGetQueryStatusExIn message requests the status of a query and additional information, such as the number of documents that have been indexed, the number of documents remaining to be indexed, and so on.</span></span> <span data-ttu-id="8457e-3414">El formato del mensaje CPMGetQueryStatusExIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-3414">The format of the CPMGetQueryStatusExIn message that follows the header is:</span></span>



<span data-ttu-id="8457e-3415">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3415">0</span></span>

<span data-ttu-id="8457e-3416">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3416">1</span></span>

<span data-ttu-id="8457e-3417">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3417">2</span></span>

<span data-ttu-id="8457e-3418">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3418">3</span></span>

<span data-ttu-id="8457e-3419">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3419">4</span></span>

<span data-ttu-id="8457e-3420">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3420">5</span></span>

<span data-ttu-id="8457e-3421">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3421">6</span></span>

<span data-ttu-id="8457e-3422">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3422">7</span></span>

<span data-ttu-id="8457e-3423">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3423">8</span></span>

<span data-ttu-id="8457e-3424">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3424">9</span></span>

<span data-ttu-id="8457e-3425">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3425">1</span></span><br/> <span data-ttu-id="8457e-3426">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3426">0</span></span><br/>

<span data-ttu-id="8457e-3427">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3427">1</span></span>

<span data-ttu-id="8457e-3428">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3428">2</span></span>

<span data-ttu-id="8457e-3429">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3429">3</span></span>

<span data-ttu-id="8457e-3430">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3430">4</span></span>

<span data-ttu-id="8457e-3431">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3431">5</span></span>

<span data-ttu-id="8457e-3432">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3432">6</span></span>

<span data-ttu-id="8457e-3433">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3433">7</span></span>

<span data-ttu-id="8457e-3434">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3434">8</span></span>

<span data-ttu-id="8457e-3435">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3435">9</span></span>

<span data-ttu-id="8457e-3436">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3436">2</span></span><br/> <span data-ttu-id="8457e-3437">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3437">0</span></span><br/>

<span data-ttu-id="8457e-3438">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3438">1</span></span>

<span data-ttu-id="8457e-3439">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3439">2</span></span>

<span data-ttu-id="8457e-3440">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3440">3</span></span>

<span data-ttu-id="8457e-3441">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3441">4</span></span>

<span data-ttu-id="8457e-3442">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3442">5</span></span>

<span data-ttu-id="8457e-3443">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3443">6</span></span>

<span data-ttu-id="8457e-3444">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3444">7</span></span>

<span data-ttu-id="8457e-3445">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3445">8</span></span>

<span data-ttu-id="8457e-3446">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3446">9</span></span>

<span data-ttu-id="8457e-3447">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3447">3</span></span><br/> <span data-ttu-id="8457e-3448">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3448">0</span></span><br/>

<span data-ttu-id="8457e-3449">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3449">1</span></span>

<span data-ttu-id="8457e-3450">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="8457e-3450">\_hCursor</span></span>

<span data-ttu-id="8457e-3451">\_bmk</span><span class="sxs-lookup"><span data-stu-id="8457e-3451">\_bmk</span></span>



 

<span data-ttu-id="8457e-3452">**\_ hCursor**: un valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut que identifica la consulta para la que se va a recuperar información de estado.</span><span class="sxs-lookup"><span data-stu-id="8457e-3452">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

<span data-ttu-id="8457e-3453">**\_ BMK**: un valor de 32 bits que indica el identificador de un marcador cuya posición se debe recuperar.</span><span class="sxs-lookup"><span data-stu-id="8457e-3453">**\_bmk**: A 32-bit value indicating the handle of a bookmark whose position should be retrieved.</span></span>

### <a name="22313-cpmgetquerystatusexout"></a><span data-ttu-id="8457e-3454">2.2.3.13 CPMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="8457e-3454">2.2.3.13 CPMGetQueryStatusExOut</span></span>

<span data-ttu-id="8457e-3455">El mensaje CPMGetQueryStatusExOut responde a un mensaje CPMGetQueryStatusExIn con el estado de la consulta y otra información de estado, como se describe en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3455">The CPMGetQueryStatusExOut message replies to a CPMGetQueryStatusExIn message with both the status of the query and other status information, as outlined in the diagram below.</span></span> <span data-ttu-id="8457e-3456">El formato del mensaje CPMGetQueryStatusExOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-3456">The format of the CPMGetQueryStatusExOut message that follows the header is:</span></span>



<span data-ttu-id="8457e-3457">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3457">0</span></span>

<span data-ttu-id="8457e-3458">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3458">1</span></span>

<span data-ttu-id="8457e-3459">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3459">2</span></span>

<span data-ttu-id="8457e-3460">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3460">3</span></span>

<span data-ttu-id="8457e-3461">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3461">4</span></span>

<span data-ttu-id="8457e-3462">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3462">5</span></span>

<span data-ttu-id="8457e-3463">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3463">6</span></span>

<span data-ttu-id="8457e-3464">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3464">7</span></span>

<span data-ttu-id="8457e-3465">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3465">8</span></span>

<span data-ttu-id="8457e-3466">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3466">9</span></span>

<span data-ttu-id="8457e-3467">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3467">1</span></span><br/> <span data-ttu-id="8457e-3468">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3468">0</span></span><br/>

<span data-ttu-id="8457e-3469">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3469">1</span></span>

<span data-ttu-id="8457e-3470">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3470">2</span></span>

<span data-ttu-id="8457e-3471">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3471">3</span></span>

<span data-ttu-id="8457e-3472">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3472">4</span></span>

<span data-ttu-id="8457e-3473">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3473">5</span></span>

<span data-ttu-id="8457e-3474">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3474">6</span></span>

<span data-ttu-id="8457e-3475">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3475">7</span></span>

<span data-ttu-id="8457e-3476">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3476">8</span></span>

<span data-ttu-id="8457e-3477">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3477">9</span></span>

<span data-ttu-id="8457e-3478">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3478">2</span></span><br/> <span data-ttu-id="8457e-3479">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3479">0</span></span><br/>

<span data-ttu-id="8457e-3480">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3480">1</span></span>

<span data-ttu-id="8457e-3481">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3481">2</span></span>

<span data-ttu-id="8457e-3482">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3482">3</span></span>

<span data-ttu-id="8457e-3483">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3483">4</span></span>

<span data-ttu-id="8457e-3484">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3484">5</span></span>

<span data-ttu-id="8457e-3485">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3485">6</span></span>

<span data-ttu-id="8457e-3486">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3486">7</span></span>

<span data-ttu-id="8457e-3487">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3487">8</span></span>

<span data-ttu-id="8457e-3488">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3488">9</span></span>

<span data-ttu-id="8457e-3489">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3489">3</span></span><br/> <span data-ttu-id="8457e-3490">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3490">0</span></span><br/>

<span data-ttu-id="8457e-3491">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3491">1</span></span>

<span data-ttu-id="8457e-3492">\_Status</span><span class="sxs-lookup"><span data-stu-id="8457e-3492">\_Status</span></span>

<span data-ttu-id="8457e-3493">\_cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="8457e-3493">\_cFilteredDocuments</span></span>

<span data-ttu-id="8457e-3494">\_cDocumentsToFilter</span><span class="sxs-lookup"><span data-stu-id="8457e-3494">\_cDocumentsToFilter</span></span>

<span data-ttu-id="8457e-3495">\_dwRatioFinishedDenominator</span><span class="sxs-lookup"><span data-stu-id="8457e-3495">\_dwRatioFinishedDenominator</span></span>

<span data-ttu-id="8457e-3496">\_dwRatioFinishedNumerator</span><span class="sxs-lookup"><span data-stu-id="8457e-3496">\_dwRatioFinishedNumerator</span></span>

<span data-ttu-id="8457e-3497">\_iRowBmk</span><span class="sxs-lookup"><span data-stu-id="8457e-3497">\_iRowBmk</span></span>

<span data-ttu-id="8457e-3498">\_cRowsTotal</span><span class="sxs-lookup"><span data-stu-id="8457e-3498">\_cRowsTotal</span></span>



 

<span data-ttu-id="8457e-3499">**\_ Estado**: una de las estadísticas \_ \* los valores especificados en la sección 2.2.3.11.</span><span class="sxs-lookup"><span data-stu-id="8457e-3499">**\_Status**: One of the STAT\_\* values specified in Section 2.2.3.11.</span></span>

<span data-ttu-id="8457e-3500">**\_ cFilteredDocuments**: entero de 32 bits sin signo que indica el número de documentos que se han indexado.</span><span class="sxs-lookup"><span data-stu-id="8457e-3500">**\_cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents that have been indexed</span></span>

<span data-ttu-id="8457e-3501">**\_ cDocumentsToFilter**: entero de 32 bits sin signo que indica el número de documentos que todavía quedan indexados.</span><span class="sxs-lookup"><span data-stu-id="8457e-3501">**\_cDocumentsToFilter**: A 32-bit unsigned integer indicating the number of documents that still remain to be indexed.</span></span>

<span data-ttu-id="8457e-3502">**\_ dwRatioFinishedDenominator**: entero de 32 bits sin signo que indica el denominador de la relación de los documentos que ha finalizado el procesamiento de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3502">**\_dwRatioFinishedDenominator**: A 32-bit unsigned integer indicating the denominator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="8457e-3503">**\_ dwRatioFinishedNumerator**: entero de 32 bits sin signo que indica el numerador de la relación de los documentos que ha finalizado el procesamiento de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3503">**\_dwRatioFinishedNumerator**: A 32-bit unsigned integer indicating the numerator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="8457e-3504">**\_ iRowBmk**: entero de 32 bits sin signo que indica la posición aproximada del marcador en el conjunto de filas en términos de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-3504">**\_iRowBmk**: A 32-bit unsigned integer indicating the approximate position of the bookmark in the rowset in terms of rows.</span></span>

<span data-ttu-id="8457e-3505">**\_ cRowsTotal**: entero de 32 bits sin signo que especifica el número total de filas del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-3505">**\_cRowsTotal**: A 32-bit unsigned integer specifying the total number of rows in the rowset.</span></span>

### <a name="22314-cpmsetbindingsin"></a><span data-ttu-id="8457e-3506">2.2.3.14 CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="8457e-3506">2.2.3.14 CPMSetBindingsIn</span></span>

<span data-ttu-id="8457e-3507">El mensaje CPMSetBindingsIn solicita el enlace de las columnas a un conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-3507">The CPMSetBindingsIn message requests the binding of columns to a rowset.</span></span> <span data-ttu-id="8457e-3508">El servidor responderá al mensaje de solicitud CPMSetBindingsIn mediante la sección de encabezado del mensaje CPMBindingsIn con los resultados de la solicitud incluida en el \_ campo Estado.</span><span class="sxs-lookup"><span data-stu-id="8457e-3508">The server will reply to the CPMSetBindingsIn request message using the header section of the CPMBindingsIn message with the results of the request contained in the \_status field.</span></span> <span data-ttu-id="8457e-3509">El formato del mensaje CPMSetBindingsIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-3509">The format of the CPMSetBindingsIn message that follows the header is:</span></span>



<span data-ttu-id="8457e-3510">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3510">0</span></span>

<span data-ttu-id="8457e-3511">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3511">1</span></span>

<span data-ttu-id="8457e-3512">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3512">2</span></span>

<span data-ttu-id="8457e-3513">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3513">3</span></span>

<span data-ttu-id="8457e-3514">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3514">4</span></span>

<span data-ttu-id="8457e-3515">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3515">5</span></span>

<span data-ttu-id="8457e-3516">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3516">6</span></span>

<span data-ttu-id="8457e-3517">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3517">7</span></span>

<span data-ttu-id="8457e-3518">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3518">8</span></span>

<span data-ttu-id="8457e-3519">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3519">9</span></span>

<span data-ttu-id="8457e-3520">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3520">1</span></span><br/> <span data-ttu-id="8457e-3521">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3521">0</span></span><br/>

<span data-ttu-id="8457e-3522">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3522">1</span></span>

<span data-ttu-id="8457e-3523">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3523">2</span></span>

<span data-ttu-id="8457e-3524">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3524">3</span></span>

<span data-ttu-id="8457e-3525">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3525">4</span></span>

<span data-ttu-id="8457e-3526">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3526">5</span></span>

<span data-ttu-id="8457e-3527">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3527">6</span></span>

<span data-ttu-id="8457e-3528">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3528">7</span></span>

<span data-ttu-id="8457e-3529">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3529">8</span></span>

<span data-ttu-id="8457e-3530">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3530">9</span></span>

<span data-ttu-id="8457e-3531">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3531">2</span></span><br/> <span data-ttu-id="8457e-3532">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3532">0</span></span><br/>

<span data-ttu-id="8457e-3533">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3533">1</span></span>

<span data-ttu-id="8457e-3534">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3534">2</span></span>

<span data-ttu-id="8457e-3535">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3535">3</span></span>

<span data-ttu-id="8457e-3536">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3536">4</span></span>

<span data-ttu-id="8457e-3537">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3537">5</span></span>

<span data-ttu-id="8457e-3538">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3538">6</span></span>

<span data-ttu-id="8457e-3539">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3539">7</span></span>

<span data-ttu-id="8457e-3540">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3540">8</span></span>

<span data-ttu-id="8457e-3541">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3541">9</span></span>

<span data-ttu-id="8457e-3542">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3542">3</span></span><br/> <span data-ttu-id="8457e-3543">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3543">0</span></span><br/>

<span data-ttu-id="8457e-3544">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3544">1</span></span>

<span data-ttu-id="8457e-3545">\_hCursor (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-3545">\_hCursor (optional)</span></span>

<span data-ttu-id="8457e-3546">\_cbRow (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-3546">\_cbRow (optional)</span></span>

<span data-ttu-id="8457e-3547">\_cbBindingDesc (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-3547">\_cbBindingDesc (optional)</span></span>

<span data-ttu-id="8457e-3548">\_ficticio (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-3548">\_dummy (optional)</span></span>

<span data-ttu-id="8457e-3549">cColumns (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-3549">cColumns (optional)</span></span>

<span data-ttu-id="8457e-3550">aColumns (variable, opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-3550">aColumns (variable, optional)</span></span>



 

<span data-ttu-id="8457e-3551">**\_ hCursor**: un valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut que identifica la fila para la que se van a establecer enlaces.</span><span class="sxs-lookup"><span data-stu-id="8457e-3551">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message that identifies the row for which to set bindings.</span></span> <span data-ttu-id="8457e-3552">Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-3552">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="8457e-3553">**\_ cbRow**: entero de 32 bits sin signo que indica el tamaño, en bytes, de una fila.</span><span class="sxs-lookup"><span data-stu-id="8457e-3553">**\_cbRow**: A 32-bit unsigned integer indicating the size, in bytes, of a row.</span></span> <span data-ttu-id="8457e-3554">Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-3554">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="8457e-3555">**\_ cbBindingDesc**: entero de 32 bits sin signo que indica la longitud, en bytes, de los campos que siguen al \_ campo ficticio.</span><span class="sxs-lookup"><span data-stu-id="8457e-3555">**\_cbBindingDesc**: A 32-bit unsigned integer indicating the length, in bytes, of the fields following the \_dummy field.</span></span> <span data-ttu-id="8457e-3556">Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-3556">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="8457e-3557">**\_ ficticio**: este campo no se utiliza y se debe omitir.</span><span class="sxs-lookup"><span data-stu-id="8457e-3557">**\_dummy**: This field is unused and MUST be ignored.</span></span> <span data-ttu-id="8457e-3558">Se puede establecer en cualquier valor arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8457e-3558">It can be set to any arbitrary value.</span></span> <span data-ttu-id="8457e-3559">Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-3559">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="8457e-3560">**cColumns**: entero de 32 bits sin signo que indica el número de elementos de la matriz aColumns.</span><span class="sxs-lookup"><span data-stu-id="8457e-3560">**cColumns**: A 32-bit unsigned integer indicating the number of elements in the aColumns array.</span></span> <span data-ttu-id="8457e-3561">Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-3561">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="8457e-3562">**aColumns**: una matriz de las estructuras CTableColumn que describen las columnas de una fila del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-3562">**aColumns**: An array of the CTableColumn structures describing the columns of a row in the rowset.</span></span> <span data-ttu-id="8457e-3563">Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-3563">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="8457e-3564">Las estructuras de la matriz deben estar separadas entre 0 y 3 bytes de relleno, de modo que cada estructura tenga una alineación de 4 bytes desde el principio de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-3564">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="8457e-3565">Estos bytes de relleno pueden ser cualquier valor arbitrario y deben omitirse en la recepción.</span><span class="sxs-lookup"><span data-stu-id="8457e-3565">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22315-cpmgetrowsin"></a><span data-ttu-id="8457e-3566">2.2.3.15 CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="8457e-3566">2.2.3.15 CPMGetRowsIn</span></span>

<span data-ttu-id="8457e-3567">El mensaje CPMGetRowsIn solicita filas de una consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3567">The CPMGetRowsIn message requests rows from a query.</span></span> <span data-ttu-id="8457e-3568">El formato del mensaje CPMGetRowsIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-3568">The format of the CPMGetRowsIn message that follows the header is:</span></span>



<span data-ttu-id="8457e-3569">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3569">0</span></span>

<span data-ttu-id="8457e-3570">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3570">1</span></span>

<span data-ttu-id="8457e-3571">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3571">2</span></span>

<span data-ttu-id="8457e-3572">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3572">3</span></span>

<span data-ttu-id="8457e-3573">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3573">4</span></span>

<span data-ttu-id="8457e-3574">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3574">5</span></span>

<span data-ttu-id="8457e-3575">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3575">6</span></span>

<span data-ttu-id="8457e-3576">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3576">7</span></span>

<span data-ttu-id="8457e-3577">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3577">8</span></span>

<span data-ttu-id="8457e-3578">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3578">9</span></span>

<span data-ttu-id="8457e-3579">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3579">1</span></span><br/> <span data-ttu-id="8457e-3580">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3580">0</span></span><br/>

<span data-ttu-id="8457e-3581">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3581">1</span></span>

<span data-ttu-id="8457e-3582">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3582">2</span></span>

<span data-ttu-id="8457e-3583">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3583">3</span></span>

<span data-ttu-id="8457e-3584">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3584">4</span></span>

<span data-ttu-id="8457e-3585">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3585">5</span></span>

<span data-ttu-id="8457e-3586">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3586">6</span></span>

<span data-ttu-id="8457e-3587">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3587">7</span></span>

<span data-ttu-id="8457e-3588">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3588">8</span></span>

<span data-ttu-id="8457e-3589">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3589">9</span></span>

<span data-ttu-id="8457e-3590">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3590">2</span></span><br/> <span data-ttu-id="8457e-3591">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3591">0</span></span><br/>

<span data-ttu-id="8457e-3592">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3592">1</span></span>

<span data-ttu-id="8457e-3593">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3593">2</span></span>

<span data-ttu-id="8457e-3594">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3594">3</span></span>

<span data-ttu-id="8457e-3595">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3595">4</span></span>

<span data-ttu-id="8457e-3596">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3596">5</span></span>

<span data-ttu-id="8457e-3597">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3597">6</span></span>

<span data-ttu-id="8457e-3598">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3598">7</span></span>

<span data-ttu-id="8457e-3599">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3599">8</span></span>

<span data-ttu-id="8457e-3600">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3600">9</span></span>

<span data-ttu-id="8457e-3601">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3601">3</span></span><br/> <span data-ttu-id="8457e-3602">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3602">0</span></span><br/>

<span data-ttu-id="8457e-3603">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3603">1</span></span>

<span data-ttu-id="8457e-3604">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="8457e-3604">\_hCursor</span></span>

<span data-ttu-id="8457e-3605">\_cRowsToTransfer</span><span class="sxs-lookup"><span data-stu-id="8457e-3605">\_cRowsToTransfer</span></span>

<span data-ttu-id="8457e-3606">\_cbRowWidth</span><span class="sxs-lookup"><span data-stu-id="8457e-3606">\_cbRowWidth</span></span>

<span data-ttu-id="8457e-3607">\_cbSeek</span><span class="sxs-lookup"><span data-stu-id="8457e-3607">\_cbSeek</span></span>

<span data-ttu-id="8457e-3608">\_cbReserved</span><span class="sxs-lookup"><span data-stu-id="8457e-3608">\_cbReserved</span></span>

<span data-ttu-id="8457e-3609">\_cbReadBuffer</span><span class="sxs-lookup"><span data-stu-id="8457e-3609">\_cbReadBuffer</span></span>

<span data-ttu-id="8457e-3610">\_ulClientBase</span><span class="sxs-lookup"><span data-stu-id="8457e-3610">\_ulClientBase</span></span>

<span data-ttu-id="8457e-3611">\_fBwdFetch</span><span class="sxs-lookup"><span data-stu-id="8457e-3611">\_fBwdFetch</span></span>

<span data-ttu-id="8457e-3612">eType</span><span class="sxs-lookup"><span data-stu-id="8457e-3612">eType</span></span>

<span data-ttu-id="8457e-3613">\_chapt</span><span class="sxs-lookup"><span data-stu-id="8457e-3613">\_chapt</span></span>

<span data-ttu-id="8457e-3614">SeekDescription</span><span class="sxs-lookup"><span data-stu-id="8457e-3614">SeekDescription</span></span>

<span data-ttu-id="8457e-3615">...</span><span class="sxs-lookup"><span data-stu-id="8457e-3615">...</span></span>

<span data-ttu-id="8457e-3616">... variable</span><span class="sxs-lookup"><span data-stu-id="8457e-3616">... (variable)</span></span>



 

<span data-ttu-id="8457e-3617">**\_ hCursor**: un valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut que identifica la consulta para la que se van a recuperar filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-3617">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve rows.</span></span>

<span data-ttu-id="8457e-3618">**\_ cRowsToTransfer**: entero de 32 bits sin signo que indica el número máximo de filas que el cliente desea recibir en respuesta a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-3618">**\_cRowsToTransfer**: A 32-bit unsigned integer indicating the maximum number of rows the client wishes to receive in response to this message.</span></span>

<span data-ttu-id="8457e-3619">**\_ cbRowWidth**: entero de 32 bits sin signo que indica la longitud de una fila, en bytes.</span><span class="sxs-lookup"><span data-stu-id="8457e-3619">**\_cbRowWidth**: A 32-bit unsigned integer indicating the length of a row, in bytes.</span></span>

<span data-ttu-id="8457e-3620">**\_ cbSeek**: entero de 32 bits sin signo que indica el tamaño del mensaje que empieza por ETYPE.</span><span class="sxs-lookup"><span data-stu-id="8457e-3620">**\_cbSeek**: A 32-bit unsigned integer indicating the size of the message beginning with eType.</span></span>

<span data-ttu-id="8457e-3621">**\_ cbReserved**: entero de 32 bits sin signo que indica el tamaño, en bytes, de un mensaje CPMGetRowsOut (sin los campos Rows y SeekDescriptions).</span><span class="sxs-lookup"><span data-stu-id="8457e-3621">**\_cbReserved**: A 32-bit unsigned integer indicating the size, in bytes, of a CPMGetRowsOut message (without the Rows and SeekDescriptions fields).</span></span> <span data-ttu-id="8457e-3622">Este valor de este campo se agrega al valor del \_ campo cbSeek y, a continuación, se utiliza para calcular el desplazamiento del campo de filas en el mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-3622">This value in this field is added to the value of the \_cbSeek field, and then is to be used to calculate the offset of Rows field in CPMGetRowsOut message.</span></span>

<span data-ttu-id="8457e-3623">**\_ cbReadBuffer**: entero de 32 bits sin signo que se debe establecer en el valor máximo del valor de \_ cbRowWidth o 1000 veces el valor de \_ cRowsToTransfer, redondeado al múltiplo más cercano de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="8457e-3623">**\_cbReadBuffer**: A 32-bit unsigned integer which MUST be set to the maximum of the value of \_cbRowWidth or 1000 times the value of \_cRowsToTransfer, rounded up to the nearest 512 byte multiple.</span></span> <span data-ttu-id="8457e-3624">El valor no debe ser mayor que 0x00004000.</span><span class="sxs-lookup"><span data-stu-id="8457e-3624">The value MUST NOT exceed 0x00004000.</span></span>

<span data-ttu-id="8457e-3625">**\_ ulClientBase**: entero de 32 bits sin signo que indica el valor base que se va a usar para los cálculos de puntero en el búfer de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-3625">**\_ulClientBase**: A 32-bit unsigned integer indicating the base value to use for pointer calculations in the row buffer.</span></span> <span data-ttu-id="8457e-3626">Si se usan desplazamientos de 64 bits, el campo reserved2 del encabezado del mensaje se usa como los 32 bits superiores y \_ ulClientBase como los 32 bits inferiores de un valor de bit de 64.</span><span class="sxs-lookup"><span data-stu-id="8457e-3626">If 64-bit offsets are being used, then the reserved2 field of the message header is used as the upper 32-bits and \_ulClientBase as the lower 32-bits of a 64-bit value.</span></span> <span data-ttu-id="8457e-3627">Vea la sección 2.2.3.16 para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8457e-3627">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="8457e-3628">**\_ fBwdFetch**: entero de 32 bits sin signo que indica el orden en el que se van a capturar las filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-3628">**\_fBwdFetch**: A 32-bit unsigned integer indicating the order in which to fetch the rows.</span></span> <span data-ttu-id="8457e-3629">Si se establece en 0x00000001, las filas se van a capturar en orden inverso.</span><span class="sxs-lookup"><span data-stu-id="8457e-3629">If set to 0x00000001, the rows are to be fetched in reverse order.</span></span> <span data-ttu-id="8457e-3630">Si se establece en 0x00000000, las filas se van a capturar en orden hacia delante.</span><span class="sxs-lookup"><span data-stu-id="8457e-3630">If set to 0x00000000, the rows are to be fetched in forward order.</span></span> <span data-ttu-id="8457e-3631">NO debe establecerse en ningún otro valor.</span><span class="sxs-lookup"><span data-stu-id="8457e-3631">MUST NOT be set to any other values.</span></span>

<span data-ttu-id="8457e-3632">**ETYPE**: entero de 32 bits sin signo que contiene uno de los valores siguientes para indicar el tipo de operación que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="8457e-3632">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of operation to perform.</span></span>



| <span data-ttu-id="8457e-3633">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-3633">Value</span></span>                         | <span data-ttu-id="8457e-3634">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-3634">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="8457e-3635">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-3635">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="8457e-3636">SeekDescription contiene una estructura CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="8457e-3636">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="8457e-3637">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8457e-3637">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="8457e-3638">SeekDescription contiene una estructura CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="8457e-3638">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="8457e-3639">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8457e-3639">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="8457e-3640">SeekDescription contiene una estructura CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="8457e-3640">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="8457e-3641">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8457e-3641">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="8457e-3642">SeekDescription contiene una estructura CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="8457e-3642">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="8457e-3643">**\_ chapt**: un valor de 32 bits que representa el identificador del capítulo del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-3643">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="8457e-3644">**SeekDescription**: este campo debe contener una estructura del tipo indicado por el valor ETYPE.</span><span class="sxs-lookup"><span data-stu-id="8457e-3644">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType value.</span></span>

### <a name="22316-cpmgetrowsout"></a><span data-ttu-id="8457e-3645">2.2.3.16 CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="8457e-3645">2.2.3.16 CPMGetRowsOut</span></span>

<span data-ttu-id="8457e-3646">El mensaje CPMGetRowsOut responde a un mensaje CPMGetRowsIn con las filas de una consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3646">The CPMGetRowsOut message replies to a CPMGetRowsIn message with the rows of a query.</span></span> <span data-ttu-id="8457e-3647">Los servidores deben dar formato a los desplazamientos de los tipos de datos de longitud variable en el campo filas como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8457e-3647">Servers MUST format offsets to variable length data types in the Rows field as follows:</span></span>

-   <span data-ttu-id="8457e-3648">El cliente indicó que era un sistema de 32 bits (0x00000008 o menos en el campo iClientVersion de CPMConnectIn): los desplazamientos son enteros de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8457e-3648">Client indicated it was a 32-bit system (0x00000008 or less in the iClientVersion field of CPMConnectIn): Offsets are 32-bit integers.</span></span>
-   <span data-ttu-id="8457e-3649">El cliente indicó que era un sistema de 64 bits ( \_ iClientVersion > 0x00000008 en CPMConnectIn) y el servidor indicó que era un sistema de 32 bits ( \_ serverVersion establecido en 0X00000007 en CPMConnectOut): los desplazamientos son enteros de 32 bits</span><span class="sxs-lookup"><span data-stu-id="8457e-3649">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 32-bit system (\_serverVersion set to 0x00000007 in CPMConnectOut): Offsets are 32-bit integers</span></span>
-   <span data-ttu-id="8457e-3650">El cliente indicó que era un sistema de 64 bits ( \_ iClientVersion > 0x00000008 en CPMConnectIn) y el servidor indicó que era un sistema de 64 bits ( \_ serverVersion establecido en 0X00010007 en CPMConnectOut): los desplazamientos son enteros de 64 bits</span><span class="sxs-lookup"><span data-stu-id="8457e-3650">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 64-bit system (\_serverVersion set to 0x00010007 in CPMConnectOut): Offsets are 64-bit integers</span></span>

<span data-ttu-id="8457e-3651">El formato del mensaje CPMGetRowsOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-3651">The format of the CPMGetRowsOut message that follows the header is:</span></span>



<span data-ttu-id="8457e-3652">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3652">0</span></span>

<span data-ttu-id="8457e-3653">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3653">1</span></span>

<span data-ttu-id="8457e-3654">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3654">2</span></span>

<span data-ttu-id="8457e-3655">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3655">3</span></span>

<span data-ttu-id="8457e-3656">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3656">4</span></span>

<span data-ttu-id="8457e-3657">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3657">5</span></span>

<span data-ttu-id="8457e-3658">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3658">6</span></span>

<span data-ttu-id="8457e-3659">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3659">7</span></span>

<span data-ttu-id="8457e-3660">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3660">8</span></span>

<span data-ttu-id="8457e-3661">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3661">9</span></span>

<span data-ttu-id="8457e-3662">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3662">1</span></span><br/> <span data-ttu-id="8457e-3663">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3663">0</span></span><br/>

<span data-ttu-id="8457e-3664">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3664">1</span></span>

<span data-ttu-id="8457e-3665">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3665">2</span></span>

<span data-ttu-id="8457e-3666">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3666">3</span></span>

<span data-ttu-id="8457e-3667">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3667">4</span></span>

<span data-ttu-id="8457e-3668">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3668">5</span></span>

<span data-ttu-id="8457e-3669">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3669">6</span></span>

<span data-ttu-id="8457e-3670">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3670">7</span></span>

<span data-ttu-id="8457e-3671">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3671">8</span></span>

<span data-ttu-id="8457e-3672">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3672">9</span></span>

<span data-ttu-id="8457e-3673">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3673">2</span></span><br/> <span data-ttu-id="8457e-3674">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3674">0</span></span><br/>

<span data-ttu-id="8457e-3675">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3675">1</span></span>

<span data-ttu-id="8457e-3676">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3676">2</span></span>

<span data-ttu-id="8457e-3677">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3677">3</span></span>

<span data-ttu-id="8457e-3678">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3678">4</span></span>

<span data-ttu-id="8457e-3679">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3679">5</span></span>

<span data-ttu-id="8457e-3680">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3680">6</span></span>

<span data-ttu-id="8457e-3681">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3681">7</span></span>

<span data-ttu-id="8457e-3682">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3682">8</span></span>

<span data-ttu-id="8457e-3683">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3683">9</span></span>

<span data-ttu-id="8457e-3684">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3684">3</span></span><br/> <span data-ttu-id="8457e-3685">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3685">0</span></span><br/>

<span data-ttu-id="8457e-3686">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3686">1</span></span>

<span data-ttu-id="8457e-3687">\_cRowsReturned</span><span class="sxs-lookup"><span data-stu-id="8457e-3687">\_cRowsReturned</span></span>

<span data-ttu-id="8457e-3688">eType</span><span class="sxs-lookup"><span data-stu-id="8457e-3688">eType</span></span>

<span data-ttu-id="8457e-3689">\_chapt</span><span class="sxs-lookup"><span data-stu-id="8457e-3689">\_chapt</span></span>

<span data-ttu-id="8457e-3690">SeekDescription (opcional, variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-3690">SeekDescription (optional, variable)</span></span>

<span data-ttu-id="8457e-3691">...</span><span class="sxs-lookup"><span data-stu-id="8457e-3691">...</span></span>

<span data-ttu-id="8457e-3692">...</span><span class="sxs-lookup"><span data-stu-id="8457e-3692">...</span></span>

<span data-ttu-id="8457e-3693">paddingRows (opcional, variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-3693">paddingRows (optional, variable)</span></span>

<span data-ttu-id="8457e-3694">Filas</span><span class="sxs-lookup"><span data-stu-id="8457e-3694">Rows</span></span>



 

<span data-ttu-id="8457e-3695">**\_ cRowsReturned**: entero de 32 bits sin signo que indica el número de filas devueltas en filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-3695">**\_cRowsReturned**: A 32-bit unsigned integer indicating the number of rows returned in Rows.</span></span>

<span data-ttu-id="8457e-3696">**ETYPE**: entero de 32 bits sin signo que contiene uno de los valores siguientes para indicar el tipo de operación de rowseek que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="8457e-3696">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of rowseek operation to perform</span></span>



| <span data-ttu-id="8457e-3697">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-3697">Value</span></span>                         | <span data-ttu-id="8457e-3698">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-3698">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="8457e-3699">eRowsSeekNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8457e-3699">eRowsSeekNone 0x00000000</span></span>      | <span data-ttu-id="8457e-3700">No SeekDescription, ignore el campo SeekDescription.</span><span class="sxs-lookup"><span data-stu-id="8457e-3700">No SeekDescription, ignore SeekDescription field.</span></span>        |
| <span data-ttu-id="8457e-3701">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-3701">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="8457e-3702">SeekDescription contiene una estructura CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="8457e-3702">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="8457e-3703">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8457e-3703">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="8457e-3704">SeekDescription contiene una estructura CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="8457e-3704">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="8457e-3705">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8457e-3705">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="8457e-3706">SeekDescription contiene una estructura CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="8457e-3706">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="8457e-3707">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8457e-3707">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="8457e-3708">SeekDescription contiene una estructura CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="8457e-3708">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="8457e-3709">**\_ chapt**: un valor de 32 bits que representa el identificador del capítulo del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-3709">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="8457e-3710">**SeekDescription**: este campo debe contener una estructura del tipo indicado por el campo ETYPE.</span><span class="sxs-lookup"><span data-stu-id="8457e-3710">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType field.</span></span>

<span data-ttu-id="8457e-3711">**paddingRows**: este campo debe tener una longitud suficiente (de 0 a \_ cbReserved-1 bytes) para rellenar el campo de filas en el \_ desplazamiento de cbReserved desde el principio de un mensaje, donde \_ cbReserved es el valor del mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-3711">**paddingRows**: This field MUST be of sufficient length (0 to \_cbReserved-1 bytes) to pad the Rows field to \_cbReserved offset from the beginning of a message, where \_cbReserved is the value in the CPMGetRowsIn message.</span></span> <span data-ttu-id="8457e-3712">Los bytes de relleno usados en este campo pueden ser cualquier valor arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8457e-3712">Padding bytes used in this field can be any arbitrary value.</span></span> <span data-ttu-id="8457e-3713">El receptor debe omitir este campo.</span><span class="sxs-lookup"><span data-stu-id="8457e-3713">This field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="8457e-3714">**Rows**: los datos de fila, tienen el formato que indica la información de columna en el mensaje CPMSetBindingsIn más reciente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3714">**Rows**: Row data, is formatted as prescribed by column information in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="8457e-3715">Las filas deben almacenarse en orden directo (por ejemplo, la fila 1 antes de la fila 2).</span><span class="sxs-lookup"><span data-stu-id="8457e-3715">Rows MUST be stored in forward order (e.g. row 1 before row 2).</span></span>

<span data-ttu-id="8457e-3716">Las columnas de tamaño fijo deben almacenarse en los desplazamientos especificados por el mensaje CPMSetBindingsIn más reciente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3716">Fixed-sized columns MUST be stored at the offsets specified by the most recent CPMSetBindingsIn message.</span></span>

<span data-ttu-id="8457e-3717">Las columnas de tamaño variable (por ejemplo, cadenas) deben almacenarse de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-3717">Variable-sized columns (e.g., strings) MUST be stored as follows:</span></span>

-   <span data-ttu-id="8457e-3718">Los datos de la variable (por ejemplo, la cadena) se almacenan cerca del final del búfer en orden descendente (por ejemplo, la colección de todos los datos variables de la fila 1 está al final, la fila 2 siguiente más cercana, etc.).</span><span class="sxs-lookup"><span data-stu-id="8457e-3718">The variable data itself (e.g. the string) is stored near the end of the buffer in descending order (e.g. the collection of all variable data for row 1 is at the end, row 2 next closest, etc.).</span></span>
-   <span data-ttu-id="8457e-3719">El área de tamaño fijo (al principio del búfer de filas) debe contener una CRowVariant para cada columna, almacenada en el desplazamiento especificado en el mensaje de CPMSetBindingsIn más reciente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3719">The fixed sized area (at the beginning of the row buffer) MUST contain a CRowVariant for each column, stored at the offset specified in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="8457e-3720">vType debe contener el tipo de datos (por ejemplo: VT \_ LPWStr).</span><span class="sxs-lookup"><span data-stu-id="8457e-3720">vType MUST contain the data type (ex: VT\_LPWSTR).</span></span> <span data-ttu-id="8457e-3721">Si, según lo determinado por las reglas al principio de la sección, se usan desplazamientos de 32 bits, el campo de desplazamiento de CRowVariant debe contener un valor de 32 bits que sea el desplazamiento de los datos variables desde el principio del mensaje CPMGetRowsOut, más el valor de \_ ulClientBase especificado en el mensaje CPMGetRowsIn más reciente.</span><span class="sxs-lookup"><span data-stu-id="8457e-3721">If, as determined by the rules at the beginning of section this section, 32-bit offsets are being used then the Offset field in CRowVariant MUST contain a 32-bit value that is the offset of the variable data from the beginning of the CPMGetRowsOut message, plus the value of \_ulClientBase specified in the most recent CPMGetRowsIn message.</span></span> <span data-ttu-id="8457e-3722">Si se usan desplazamientos de 64 bits, el campo de desplazamiento de CRowVariant debe contener un valor de 64 bits, que es el desplazamiento desde el principio del mensaje CPMGetRowsOut, que se agrega a un valor de 64 bits compuesto por el uso de \_ ulClientBase como el nivel de 32-bits bajo y \_ ulReserved2 como el alto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8457e-3722">If 64-bit offsets are being used then the Offset field in CRowVariant MUST contain a 64-bit value that is the offset from the beginning of the CPMGetRowsOut message, added to a 64-bit value composed by using \_ulClientBase as the low 32-bits and \_ulReserved2 as the high 32-bits.</span></span>

<span data-ttu-id="8457e-3723">Por ejemplo, si el mensaje CPMSetBindingsIn especifica dos columnas: Size (VT \_ I4) y title (VT \_ LPWStr)-y \_ ulClientBase de CPMGetRowsIn se 0x10000, entonces dos filas tendrían el siguiente aspecto.</span><span class="sxs-lookup"><span data-stu-id="8457e-3723">For example, if the CPMSetBindingsIn message specified two columns-Size (VT\_I4) and Title (VT\_LPWSTR)-and \_ulClientBase from CPMGetRowsIn was 0x10000 then two rows would appear as follows.</span></span> <span data-ttu-id="8457e-3724">La sección marcada en gris es la parte de longitud fija del búfer.</span><span class="sxs-lookup"><span data-stu-id="8457e-3724">The section marked in grey is the fixed-length part of the buffer.</span></span>

![ejemplo de mensaje de cpmsetbindingsin](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a><span data-ttu-id="8457e-3726">2.2.3.17 CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="8457e-3726">2.2.3.17 CPMRatioFinishedIn</span></span>

<span data-ttu-id="8457e-3727">El mensaje CPMRatioFinishedIn solicita el porcentaje de finalización de una consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3727">The CPMRatioFinishedIn message requests the completion percentage of a query.</span></span> <span data-ttu-id="8457e-3728">El formato del mensaje CPMRatioFinishedIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-3728">The format of the CPMRatioFinishedIn message that follows the header is:</span></span>



<span data-ttu-id="8457e-3729">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3729">0</span></span>

<span data-ttu-id="8457e-3730">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3730">1</span></span>

<span data-ttu-id="8457e-3731">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3731">2</span></span>

<span data-ttu-id="8457e-3732">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3732">3</span></span>

<span data-ttu-id="8457e-3733">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3733">4</span></span>

<span data-ttu-id="8457e-3734">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3734">5</span></span>

<span data-ttu-id="8457e-3735">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3735">6</span></span>

<span data-ttu-id="8457e-3736">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3736">7</span></span>

<span data-ttu-id="8457e-3737">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3737">8</span></span>

<span data-ttu-id="8457e-3738">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3738">9</span></span>

<span data-ttu-id="8457e-3739">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3739">1</span></span><br/> <span data-ttu-id="8457e-3740">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3740">0</span></span><br/>

<span data-ttu-id="8457e-3741">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3741">1</span></span>

<span data-ttu-id="8457e-3742">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3742">2</span></span>

<span data-ttu-id="8457e-3743">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3743">3</span></span>

<span data-ttu-id="8457e-3744">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3744">4</span></span>

<span data-ttu-id="8457e-3745">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3745">5</span></span>

<span data-ttu-id="8457e-3746">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3746">6</span></span>

<span data-ttu-id="8457e-3747">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3747">7</span></span>

<span data-ttu-id="8457e-3748">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3748">8</span></span>

<span data-ttu-id="8457e-3749">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3749">9</span></span>

<span data-ttu-id="8457e-3750">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3750">2</span></span><br/> <span data-ttu-id="8457e-3751">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3751">0</span></span><br/>

<span data-ttu-id="8457e-3752">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3752">1</span></span>

<span data-ttu-id="8457e-3753">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3753">2</span></span>

<span data-ttu-id="8457e-3754">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3754">3</span></span>

<span data-ttu-id="8457e-3755">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3755">4</span></span>

<span data-ttu-id="8457e-3756">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3756">5</span></span>

<span data-ttu-id="8457e-3757">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3757">6</span></span>

<span data-ttu-id="8457e-3758">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3758">7</span></span>

<span data-ttu-id="8457e-3759">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3759">8</span></span>

<span data-ttu-id="8457e-3760">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3760">9</span></span>

<span data-ttu-id="8457e-3761">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3761">3</span></span><br/> <span data-ttu-id="8457e-3762">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3762">0</span></span><br/>

<span data-ttu-id="8457e-3763">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3763">1</span></span>

<span data-ttu-id="8457e-3764">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="8457e-3764">\_hCursor</span></span>

<span data-ttu-id="8457e-3765">\_fQuick</span><span class="sxs-lookup"><span data-stu-id="8457e-3765">\_fQuick</span></span>



 

<span data-ttu-id="8457e-3766">**\_ hCursor**: identificador del mensaje CPMCreateQueryOut que identifica la consulta para la que se va a solicitar la información de finalización.</span><span class="sxs-lookup"><span data-stu-id="8457e-3766">**\_hCursor**: The handle from CPMCreateQueryOut message identifying the query for which to request completion information.</span></span>

<span data-ttu-id="8457e-3767">**\_ fQuick**: debe establecerse en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8457e-3767">**\_fQuick**: MUST be set to 0x00000001.</span></span> <span data-ttu-id="8457e-3768">No se usa y el servidor debe pasarlo por alto.</span><span class="sxs-lookup"><span data-stu-id="8457e-3768">Unused and MUST be ignored by the server.</span></span>

### <a name="22318-cpmratiofinishedout"></a><span data-ttu-id="8457e-3769">2.2.3.18 CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="8457e-3769">2.2.3.18 CPMRatioFinishedOut</span></span>

<span data-ttu-id="8457e-3770">El mensaje CPMRatioFinishedOut responde a un mensaje CPMRatioFinishedIn con la relación de finalización de una consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3770">The CPMRatioFinishedOut message replies to a CPMRatioFinishedIn message with the completion ratio of a query.</span></span> <span data-ttu-id="8457e-3771">El formato del mensaje CPMRatioFinishedOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-3771">The format of the CPMRatioFinishedOut message that follows the header is:</span></span>



<span data-ttu-id="8457e-3772">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3772">0</span></span>

<span data-ttu-id="8457e-3773">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3773">1</span></span>

<span data-ttu-id="8457e-3774">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3774">2</span></span>

<span data-ttu-id="8457e-3775">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3775">3</span></span>

<span data-ttu-id="8457e-3776">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3776">4</span></span>

<span data-ttu-id="8457e-3777">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3777">5</span></span>

<span data-ttu-id="8457e-3778">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3778">6</span></span>

<span data-ttu-id="8457e-3779">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3779">7</span></span>

<span data-ttu-id="8457e-3780">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3780">8</span></span>

<span data-ttu-id="8457e-3781">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3781">9</span></span>

<span data-ttu-id="8457e-3782">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3782">1</span></span><br/> <span data-ttu-id="8457e-3783">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3783">0</span></span><br/>

<span data-ttu-id="8457e-3784">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3784">1</span></span>

<span data-ttu-id="8457e-3785">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3785">2</span></span>

<span data-ttu-id="8457e-3786">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3786">3</span></span>

<span data-ttu-id="8457e-3787">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3787">4</span></span>

<span data-ttu-id="8457e-3788">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3788">5</span></span>

<span data-ttu-id="8457e-3789">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3789">6</span></span>

<span data-ttu-id="8457e-3790">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3790">7</span></span>

<span data-ttu-id="8457e-3791">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3791">8</span></span>

<span data-ttu-id="8457e-3792">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3792">9</span></span>

<span data-ttu-id="8457e-3793">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3793">2</span></span><br/> <span data-ttu-id="8457e-3794">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3794">0</span></span><br/>

<span data-ttu-id="8457e-3795">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3795">1</span></span>

<span data-ttu-id="8457e-3796">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3796">2</span></span>

<span data-ttu-id="8457e-3797">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3797">3</span></span>

<span data-ttu-id="8457e-3798">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3798">4</span></span>

<span data-ttu-id="8457e-3799">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3799">5</span></span>

<span data-ttu-id="8457e-3800">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3800">6</span></span>

<span data-ttu-id="8457e-3801">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3801">7</span></span>

<span data-ttu-id="8457e-3802">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3802">8</span></span>

<span data-ttu-id="8457e-3803">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3803">9</span></span>

<span data-ttu-id="8457e-3804">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3804">3</span></span><br/> <span data-ttu-id="8457e-3805">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3805">0</span></span><br/>

<span data-ttu-id="8457e-3806">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3806">1</span></span>

<span data-ttu-id="8457e-3807">\_ ulNumerator</span><span class="sxs-lookup"><span data-stu-id="8457e-3807">\_ ulNumerator</span></span>

<span data-ttu-id="8457e-3808">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="8457e-3808">\_ulDenominator</span></span>

<span data-ttu-id="8457e-3809">\_cRows</span><span class="sxs-lookup"><span data-stu-id="8457e-3809">\_cRows</span></span>

<span data-ttu-id="8457e-3810">\_fNewRows</span><span class="sxs-lookup"><span data-stu-id="8457e-3810">\_fNewRows</span></span>



 

<span data-ttu-id="8457e-3811">**\_ ulNumerator**: entero de 32 bits sin signo que indica el numerador de la relación de finalización en términos de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-3811">**\_ulNumerator**: A 32-bit unsigned integer indicating the numerator of the completion ratio in terms of rows.</span></span>

<span data-ttu-id="8457e-3812">**\_ ulDenominator**: entero de 32 bits sin signo que indica el denominador de la relación de finalización en términos de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-3812">**\_ulDenominator**: A 32-bit unsigned integer indicating the denominator of the completion ratio in terms of rows.</span></span> <span data-ttu-id="8457e-3813">DEBE ser mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="8457e-3813">MUST be greater than zero.</span></span>

<span data-ttu-id="8457e-3814">**\_ Crows**: entero de 32 bits sin signo que indica el número total de filas de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3814">**\_cRows**: A 32-bit unsigned integer indicating the total number of rows for the query.</span></span>

<span data-ttu-id="8457e-3815">**\_ fNewRows**: un valor booleano que indica si hay nuevas filas disponibles.</span><span class="sxs-lookup"><span data-stu-id="8457e-3815">**\_fNewRows**: A boolean value indicating if there are new rows available.</span></span> <span data-ttu-id="8457e-3816">Un valor de 0x00000001 indica que las nuevas filas están disponibles en el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-3816">A value of 0x00000001 indicates that new rows are available in the rowset.</span></span> <span data-ttu-id="8457e-3817">Un valor de 0x00000000 indica que el conjunto de filas no contiene ninguna fila nueva.</span><span class="sxs-lookup"><span data-stu-id="8457e-3817">A value of 0x00000000 indicates that the rowset does not contain any new rows.</span></span> <span data-ttu-id="8457e-3818">Este campo no se debe establecer en ningún otro valor.</span><span class="sxs-lookup"><span data-stu-id="8457e-3818">This field MUST NOT be set to any other values.</span></span>

### <a name="22319-cpmfetchvaluein"></a><span data-ttu-id="8457e-3819">2.2.3.19 CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="8457e-3819">2.2.3.19 CPMFetchValueIn</span></span>

<span data-ttu-id="8457e-3820">El mensaje CPMFetchValueIn solicita un valor de propiedad que era demasiado grande para devolver en un conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-3820">The CPMFetchValueIn message requests a property value that was too large to return in a rowset.</span></span> <span data-ttu-id="8457e-3821">Tal y como se especifica en la sección 3.2.4.2.5, este mensaje se envía repetidamente para recuperar todos los bytes de la propiedad, actualizando \_ cbSoFar para cada uno, hasta que el \_ campo fMoreExists del mensaje CPMFetchValueOut se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="8457e-3821">As specified in section 3.2.4.2.5, this message is sent repeatedly to retrieve all bytes of the property, updating \_cbSoFar for each, until the \_fMoreExists field of CPMFetchValueOut message is set to **FALSE**.</span></span>

<span data-ttu-id="8457e-3822">El formato del mensaje CPMFetchValueIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-3822">The format of the CPMFetchValueIn message that follows the header is:</span></span>



<span data-ttu-id="8457e-3823">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3823">0</span></span>

<span data-ttu-id="8457e-3824">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3824">1</span></span>

<span data-ttu-id="8457e-3825">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3825">2</span></span>

<span data-ttu-id="8457e-3826">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3826">3</span></span>

<span data-ttu-id="8457e-3827">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3827">4</span></span>

<span data-ttu-id="8457e-3828">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3828">5</span></span>

<span data-ttu-id="8457e-3829">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3829">6</span></span>

<span data-ttu-id="8457e-3830">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3830">7</span></span>

<span data-ttu-id="8457e-3831">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3831">8</span></span>

<span data-ttu-id="8457e-3832">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3832">9</span></span>

<span data-ttu-id="8457e-3833">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3833">1</span></span><br/> <span data-ttu-id="8457e-3834">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3834">0</span></span><br/>

<span data-ttu-id="8457e-3835">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3835">1</span></span>

<span data-ttu-id="8457e-3836">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3836">2</span></span>

<span data-ttu-id="8457e-3837">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3837">3</span></span>

<span data-ttu-id="8457e-3838">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3838">4</span></span>

<span data-ttu-id="8457e-3839">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3839">5</span></span>

<span data-ttu-id="8457e-3840">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3840">6</span></span>

<span data-ttu-id="8457e-3841">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3841">7</span></span>

<span data-ttu-id="8457e-3842">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3842">8</span></span>

<span data-ttu-id="8457e-3843">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3843">9</span></span>

<span data-ttu-id="8457e-3844">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3844">2</span></span><br/> <span data-ttu-id="8457e-3845">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3845">0</span></span><br/>

<span data-ttu-id="8457e-3846">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3846">1</span></span>

<span data-ttu-id="8457e-3847">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3847">2</span></span>

<span data-ttu-id="8457e-3848">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3848">3</span></span>

<span data-ttu-id="8457e-3849">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3849">4</span></span>

<span data-ttu-id="8457e-3850">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3850">5</span></span>

<span data-ttu-id="8457e-3851">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3851">6</span></span>

<span data-ttu-id="8457e-3852">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3852">7</span></span>

<span data-ttu-id="8457e-3853">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3853">8</span></span>

<span data-ttu-id="8457e-3854">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3854">9</span></span>

<span data-ttu-id="8457e-3855">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3855">3</span></span><br/> <span data-ttu-id="8457e-3856">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3856">0</span></span><br/>

<span data-ttu-id="8457e-3857">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3857">1</span></span>

<span data-ttu-id="8457e-3858">\_WID</span><span class="sxs-lookup"><span data-stu-id="8457e-3858">\_wid</span></span>

<span data-ttu-id="8457e-3859">\_cbSoFar</span><span class="sxs-lookup"><span data-stu-id="8457e-3859">\_cbSoFar</span></span>

<span data-ttu-id="8457e-3860">\_cbPropSpec</span><span class="sxs-lookup"><span data-stu-id="8457e-3860">\_cbPropSpec</span></span>

<span data-ttu-id="8457e-3861">\_cbChunk</span><span class="sxs-lookup"><span data-stu-id="8457e-3861">\_cbChunk</span></span>

<span data-ttu-id="8457e-3862">PropSpec (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-3862">PropSpec (variable)</span></span>

<span data-ttu-id="8457e-3863">...</span><span class="sxs-lookup"><span data-stu-id="8457e-3863">...</span></span>

<span data-ttu-id="8457e-3864">\_padding (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-3864">\_padding (variable)</span></span>



 

<span data-ttu-id="8457e-3865">**\_ WID**: entero de 32 bits sin signo que representa el identificador de documento que identifica el documento para el que se debe capturar una propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-3865">**\_wid**: A 32-bit unsigned integer representing the document ID identifying the document for which a property should be fetched.</span></span>

<span data-ttu-id="8457e-3866">**\_ cbSoFar**: entero de 32 bits sin signo que contiene el número de bytes transferidos previamente para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-3866">**\_cbSoFar**: A 32-bit unsigned integer containing the number of bytes previously transferred for this property.</span></span> <span data-ttu-id="8457e-3867">DEBE establecerse en 0x00000000 en el primer mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-3867">MUST be set to 0x00000000 in the first message.</span></span>

<span data-ttu-id="8457e-3868">**\_ cbPropSpec**: entero de 32 bits sin signo que contiene el tamaño del campo PropSpec, en bytes.</span><span class="sxs-lookup"><span data-stu-id="8457e-3868">**\_cbPropSpec**: A 32-bit unsigned integer containing the size of the PropSpec field, in bytes.</span></span>

<span data-ttu-id="8457e-3869">**\_ cbChunk**: entero de 32 bits sin signo que contiene el número máximo de bytes que el remitente puede aceptar en un mensaje de CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-3869">**\_cbChunk**: A 32-bit unsigned integer containing the maximum number of bytes that the sender can accept in a CPMFetchValueOut message.</span></span>

<span data-ttu-id="8457e-3870">*Comportamiento de Windows: este campo se establece en 0x00004000 para todas las versiones de Windows.*</span><span class="sxs-lookup"><span data-stu-id="8457e-3870">*Windows Behavior: This field is set to 0x00004000 for all versions of Windows.*</span></span>

<span data-ttu-id="8457e-3871">**PropSpec**: estructura CFullPropSpec que especifica la propiedad que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="8457e-3871">**PropSpec**: A CFullPropSpec structure specifying the property to retrieve.</span></span>

<span data-ttu-id="8457e-3872">**\_ padding**: este campo debe tener la longitud necesaria (de 0 a 3 bytes) para rellenar el mensaje hasta un múltiplo de 4 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="8457e-3872">**\_padding**: This field MUST be of the length necessary (0 to 3 bytes) to pad the message out to a multiple of 4 bytes in length.</span></span> <span data-ttu-id="8457e-3873">El valor de los bytes de relleno puede ser cualquier valor arbitrario.</span><span class="sxs-lookup"><span data-stu-id="8457e-3873">The value of the padding bytes can be any arbitrary value.</span></span> <span data-ttu-id="8457e-3874">El receptor debe omitir este campo.</span><span class="sxs-lookup"><span data-stu-id="8457e-3874">This field MUST be ignored by the receiver.</span></span>

### <a name="22320-cpmfetchvalueout"></a><span data-ttu-id="8457e-3875">2.2.3.20 CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="8457e-3875">2.2.3.20 CPMFetchValueOut</span></span>

<span data-ttu-id="8457e-3876">El mensaje CPMFetchValueOut responde a un mensaje CPMFetchValueIn con un valor de propiedad de una consulta anterior.</span><span class="sxs-lookup"><span data-stu-id="8457e-3876">The CPMFetchValueOut message replies to a CPMFetchValueIn message with a property value from a previous query.</span></span> <span data-ttu-id="8457e-3877">Tal y como se especifica en la sección 3.1.5.2.8, este mensaje se envía después de cada mensaje de CPMFetchValueIn hasta que se transfieren todos los bytes de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-3877">As specified in section 3.1.5.2.8, this message is sent after each CPMFetchValueIn message until all bytes of the property are transferred.</span></span>

<span data-ttu-id="8457e-3878">El formato del mensaje CPMFetchValueOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-3878">The format of the CPMFetchValueOut message that follows the header is:</span></span>



<span data-ttu-id="8457e-3879">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3879">0</span></span>

<span data-ttu-id="8457e-3880">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3880">1</span></span>

<span data-ttu-id="8457e-3881">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3881">2</span></span>

<span data-ttu-id="8457e-3882">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3882">3</span></span>

<span data-ttu-id="8457e-3883">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3883">4</span></span>

<span data-ttu-id="8457e-3884">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3884">5</span></span>

<span data-ttu-id="8457e-3885">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3885">6</span></span>

<span data-ttu-id="8457e-3886">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3886">7</span></span>

<span data-ttu-id="8457e-3887">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3887">8</span></span>

<span data-ttu-id="8457e-3888">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3888">9</span></span>

<span data-ttu-id="8457e-3889">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3889">1</span></span><br/> <span data-ttu-id="8457e-3890">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3890">0</span></span><br/>

<span data-ttu-id="8457e-3891">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3891">1</span></span>

<span data-ttu-id="8457e-3892">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3892">2</span></span>

<span data-ttu-id="8457e-3893">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3893">3</span></span>

<span data-ttu-id="8457e-3894">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3894">4</span></span>

<span data-ttu-id="8457e-3895">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3895">5</span></span>

<span data-ttu-id="8457e-3896">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3896">6</span></span>

<span data-ttu-id="8457e-3897">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3897">7</span></span>

<span data-ttu-id="8457e-3898">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3898">8</span></span>

<span data-ttu-id="8457e-3899">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3899">9</span></span>

<span data-ttu-id="8457e-3900">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3900">2</span></span><br/> <span data-ttu-id="8457e-3901">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3901">0</span></span><br/>

<span data-ttu-id="8457e-3902">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3902">1</span></span>

<span data-ttu-id="8457e-3903">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3903">2</span></span>

<span data-ttu-id="8457e-3904">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3904">3</span></span>

<span data-ttu-id="8457e-3905">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3905">4</span></span>

<span data-ttu-id="8457e-3906">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3906">5</span></span>

<span data-ttu-id="8457e-3907">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3907">6</span></span>

<span data-ttu-id="8457e-3908">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3908">7</span></span>

<span data-ttu-id="8457e-3909">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3909">8</span></span>

<span data-ttu-id="8457e-3910">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3910">9</span></span>

<span data-ttu-id="8457e-3911">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3911">3</span></span><br/> <span data-ttu-id="8457e-3912">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3912">0</span></span><br/>

<span data-ttu-id="8457e-3913">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3913">1</span></span>

<span data-ttu-id="8457e-3914">\_cbValue</span><span class="sxs-lookup"><span data-stu-id="8457e-3914">\_cbValue</span></span>

<span data-ttu-id="8457e-3915">\_fMoreExists</span><span class="sxs-lookup"><span data-stu-id="8457e-3915">\_fMoreExists</span></span>

<span data-ttu-id="8457e-3916">\_fValueExists</span><span class="sxs-lookup"><span data-stu-id="8457e-3916">\_fValueExists</span></span>

<span data-ttu-id="8457e-3917">vType</span><span class="sxs-lookup"><span data-stu-id="8457e-3917">vType</span></span>

<span data-ttu-id="8457e-3918">vValue (variable)</span><span class="sxs-lookup"><span data-stu-id="8457e-3918">vValue (variable)</span></span>



 

<span data-ttu-id="8457e-3919">**\_ cbValue**: entero de 32 bits sin signo que contiene el tamaño total, en bytes, en vValue.</span><span class="sxs-lookup"><span data-stu-id="8457e-3919">**\_cbValue**: A 32-bit unsigned integer containing the total size, in bytes in vValue.</span></span>

<span data-ttu-id="8457e-3920">**\_ fMoreExists**: un valor booleano que indica si hay mensajes CPMFetchValueOut adicionales disponibles.</span><span class="sxs-lookup"><span data-stu-id="8457e-3920">**\_fMoreExists**: A boolean value indicating whether there are additional CPMFetchValueOut messages available.</span></span> <span data-ttu-id="8457e-3921">Si se establece en 0x00000001, hay mensajes CPMFetchValueOut adicionales.</span><span class="sxs-lookup"><span data-stu-id="8457e-3921">If set to 0x00000001, then there are additional CPMFetchValueOut messages.</span></span> <span data-ttu-id="8457e-3922">Si se establece en 0x00000000, no hay mensajes CPMFetchValueOut adicionales disponibles.</span><span class="sxs-lookup"><span data-stu-id="8457e-3922">If set to 0x00000000, then there are no additional CPMFetchValueOut messages available.</span></span>

<span data-ttu-id="8457e-3923">**\_ fValueExists**: un valor booleano que indica si hay un valor para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-3923">**\_fValueExists**: A boolean value indicating whether there is a value for the property.</span></span> <span data-ttu-id="8457e-3924">Si se establece en 0x00000001, existe un valor para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-3924">If set to 0x00000001, a value for the property exists.</span></span> <span data-ttu-id="8457e-3925">Si se establece en 0x00000000, no existe un valor para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-3925">If set to 0x00000000, a value for the property does not exist.</span></span>

<span data-ttu-id="8457e-3926">**vType**: un valor de la enumeración VARENUM, vea la sección 2.2.1.1 para obtener más información, que describe el tipo de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-3926">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span></span>

<span data-ttu-id="8457e-3927">**vValue**: una parte de una matriz de bytes que contiene una estructura SERIALIZEDPROPERTYVALUE, tal como se especifica en la sección 2.2.1.32, donde el desplazamiento del principio de la parte es el valor de \_ cbSoFar en CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-3927">**vValue**: A portion of a byte array containing a SERIALIZEDPROPERTYVALUE structure as specified in section 2.2.1.32, where the offset of the beginning of the portion is the value of\_cbSoFar in CPMFetchValueIn.</span></span> <span data-ttu-id="8457e-3928">La longitud de la parte, indicada por el \_ campo cbValue, debe ser igual al valor de \_ CbChunk en CPMFetchValueIn si \_ fMoreExists está establecido en 0x00000001 y debe ser menor o igual que el valor de \_ cbChunk en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8457e-3928">The length of the portion, indicated by the \_cbValue field, MUST be equal to the value of \_cbChunk in CPMFetchValueIn if \_fMoreExists is set to 0x00000001, and MUST be less than or equal to the value of \_cbChunk otherwise.</span></span>

### <a name="22321-cpmgetnotify"></a><span data-ttu-id="8457e-3929">2.2.3.21 CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="8457e-3929">2.2.3.21 CPMGetNotify</span></span>

<span data-ttu-id="8457e-3930">El mensaje CPMGetNotify solicita que el cliente desea recibir una notificación de los cambios del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-3930">The CPMGetNotify message requests that the client wants to be notified of rowset changes.</span></span>

<span data-ttu-id="8457e-3931">El mensaje no debe incluir un cuerpo; solo se enviará el encabezado del mensaje, como se especifica en la sección 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="8457e-3931">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2, is to be sent.</span></span>

### <a name="22322-cpmsendnotifyout"></a><span data-ttu-id="8457e-3932">2.2.3.22 CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="8457e-3932">2.2.3.22 CPMSendNotifyOut</span></span>

<span data-ttu-id="8457e-3933">El mensaje CPMSendNotifyOut notifica al cliente un cambio en los resultados de una consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3933">The CPMSendNotifyOut message notifies the client of a change to the results of a query.</span></span>

<span data-ttu-id="8457e-3934">Este mensaje solo se envía cuando se produce un cambio.</span><span class="sxs-lookup"><span data-stu-id="8457e-3934">This message is only sent when a change occurs.</span></span> <span data-ttu-id="8457e-3935">El formato del mensaje CPMSendNotifyOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-3935">The format of the CPMSendNotifyOut message that follows the header is:</span></span>



<span data-ttu-id="8457e-3936">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3936">0</span></span>

<span data-ttu-id="8457e-3937">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3937">1</span></span>

<span data-ttu-id="8457e-3938">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3938">2</span></span>

<span data-ttu-id="8457e-3939">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3939">3</span></span>

<span data-ttu-id="8457e-3940">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3940">4</span></span>

<span data-ttu-id="8457e-3941">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3941">5</span></span>

<span data-ttu-id="8457e-3942">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3942">6</span></span>

<span data-ttu-id="8457e-3943">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3943">7</span></span>

<span data-ttu-id="8457e-3944">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3944">8</span></span>

<span data-ttu-id="8457e-3945">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3945">9</span></span>

<span data-ttu-id="8457e-3946">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3946">1</span></span><br/> <span data-ttu-id="8457e-3947">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3947">0</span></span><br/>

<span data-ttu-id="8457e-3948">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3948">1</span></span>

<span data-ttu-id="8457e-3949">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3949">2</span></span>

<span data-ttu-id="8457e-3950">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3950">3</span></span>

<span data-ttu-id="8457e-3951">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3951">4</span></span>

<span data-ttu-id="8457e-3952">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3952">5</span></span>

<span data-ttu-id="8457e-3953">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3953">6</span></span>

<span data-ttu-id="8457e-3954">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3954">7</span></span>

<span data-ttu-id="8457e-3955">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3955">8</span></span>

<span data-ttu-id="8457e-3956">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3956">9</span></span>

<span data-ttu-id="8457e-3957">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3957">2</span></span><br/> <span data-ttu-id="8457e-3958">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3958">0</span></span><br/>

<span data-ttu-id="8457e-3959">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3959">1</span></span>

<span data-ttu-id="8457e-3960">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3960">2</span></span>

<span data-ttu-id="8457e-3961">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3961">3</span></span>

<span data-ttu-id="8457e-3962">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3962">4</span></span>

<span data-ttu-id="8457e-3963">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3963">5</span></span>

<span data-ttu-id="8457e-3964">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3964">6</span></span>

<span data-ttu-id="8457e-3965">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3965">7</span></span>

<span data-ttu-id="8457e-3966">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3966">8</span></span>

<span data-ttu-id="8457e-3967">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3967">9</span></span>

<span data-ttu-id="8457e-3968">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3968">3</span></span><br/> <span data-ttu-id="8457e-3969">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3969">0</span></span><br/>

<span data-ttu-id="8457e-3970">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3970">1</span></span>

<span data-ttu-id="8457e-3971">\_watchNotify</span><span class="sxs-lookup"><span data-stu-id="8457e-3971">\_watchNotify</span></span>



 

<span data-ttu-id="8457e-3972">**\_ watchNotify**: el cambio en la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3972">**\_watchNotify**: The change to the query.</span></span> <span data-ttu-id="8457e-3973">DEBE ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="8457e-3973">It MUST be one of the following values:</span></span>



| <span data-ttu-id="8457e-3974">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-3974">Value</span></span>                                     | <span data-ttu-id="8457e-3975">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-3975">Meaning</span></span>                                             |
|-------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="8457e-3976">DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-3976">DBWATCHNOTIFY\_ROWSCHANGED 0x00000001</span></span>     | <span data-ttu-id="8457e-3977">El número de filas del conjunto de filas de consulta ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="8457e-3977">The number of rows in the query rowset has changed.</span></span> |
| <span data-ttu-id="8457e-3978">DBWATCHNOTIFY \_ QUERYDONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8457e-3978">DBWATCHNOTIFY\_QUERYDONE 0x00000002</span></span>       | <span data-ttu-id="8457e-3979">La consulta se ha completado.</span><span class="sxs-lookup"><span data-stu-id="8457e-3979">The query has completed.</span></span>                            |
| <span data-ttu-id="8457e-3980">DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8457e-3980">DBWATCHNOTIFY\_QUERYREEXECUTED 0x00000003</span></span> | <span data-ttu-id="8457e-3981">Se ha vuelto a ejecutar la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-3981">The query has been re-executed.</span></span>                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a><span data-ttu-id="8457e-3982">2.2.3.23 CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="8457e-3982">2.2.3.23 CPMGetApproximatePositionIn</span></span>

<span data-ttu-id="8457e-3983">El mensaje CPMGetApproximatePositionIn solicita la posición aproximada de un marcador en un capítulo.</span><span class="sxs-lookup"><span data-stu-id="8457e-3983">The CPMGetApproximatePositionIn message requests the approximate position of a bookmark in a chapter.</span></span> <span data-ttu-id="8457e-3984">El formato del mensaje CPMGetApproximatePositionIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-3984">The format of the CPMGetApproximatePositionIn message that follows the header is:</span></span>



<span data-ttu-id="8457e-3985">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3985">0</span></span>

<span data-ttu-id="8457e-3986">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3986">1</span></span>

<span data-ttu-id="8457e-3987">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3987">2</span></span>

<span data-ttu-id="8457e-3988">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3988">3</span></span>

<span data-ttu-id="8457e-3989">4</span><span class="sxs-lookup"><span data-stu-id="8457e-3989">4</span></span>

<span data-ttu-id="8457e-3990">5</span><span class="sxs-lookup"><span data-stu-id="8457e-3990">5</span></span>

<span data-ttu-id="8457e-3991">6</span><span class="sxs-lookup"><span data-stu-id="8457e-3991">6</span></span>

<span data-ttu-id="8457e-3992">7</span><span class="sxs-lookup"><span data-stu-id="8457e-3992">7</span></span>

<span data-ttu-id="8457e-3993">8</span><span class="sxs-lookup"><span data-stu-id="8457e-3993">8</span></span>

<span data-ttu-id="8457e-3994">9</span><span class="sxs-lookup"><span data-stu-id="8457e-3994">9</span></span>

<span data-ttu-id="8457e-3995">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3995">1</span></span><br/> <span data-ttu-id="8457e-3996">0</span><span class="sxs-lookup"><span data-stu-id="8457e-3996">0</span></span><br/>

<span data-ttu-id="8457e-3997">1</span><span class="sxs-lookup"><span data-stu-id="8457e-3997">1</span></span>

<span data-ttu-id="8457e-3998">2</span><span class="sxs-lookup"><span data-stu-id="8457e-3998">2</span></span>

<span data-ttu-id="8457e-3999">3</span><span class="sxs-lookup"><span data-stu-id="8457e-3999">3</span></span>

<span data-ttu-id="8457e-4000">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4000">4</span></span>

<span data-ttu-id="8457e-4001">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4001">5</span></span>

<span data-ttu-id="8457e-4002">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4002">6</span></span>

<span data-ttu-id="8457e-4003">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4003">7</span></span>

<span data-ttu-id="8457e-4004">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4004">8</span></span>

<span data-ttu-id="8457e-4005">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4005">9</span></span>

<span data-ttu-id="8457e-4006">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4006">2</span></span><br/> <span data-ttu-id="8457e-4007">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4007">0</span></span><br/>

<span data-ttu-id="8457e-4008">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4008">1</span></span>

<span data-ttu-id="8457e-4009">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4009">2</span></span>

<span data-ttu-id="8457e-4010">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4010">3</span></span>

<span data-ttu-id="8457e-4011">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4011">4</span></span>

<span data-ttu-id="8457e-4012">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4012">5</span></span>

<span data-ttu-id="8457e-4013">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4013">6</span></span>

<span data-ttu-id="8457e-4014">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4014">7</span></span>

<span data-ttu-id="8457e-4015">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4015">8</span></span>

<span data-ttu-id="8457e-4016">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4016">9</span></span>

<span data-ttu-id="8457e-4017">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4017">3</span></span><br/> <span data-ttu-id="8457e-4018">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4018">0</span></span><br/>

<span data-ttu-id="8457e-4019">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4019">1</span></span>

<span data-ttu-id="8457e-4020">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="8457e-4020">\_hCursor</span></span>

<span data-ttu-id="8457e-4021">\_chapt</span><span class="sxs-lookup"><span data-stu-id="8457e-4021">\_chapt</span></span>

<span data-ttu-id="8457e-4022">\_bmk</span><span class="sxs-lookup"><span data-stu-id="8457e-4022">\_bmk</span></span>



 

<span data-ttu-id="8457e-4023">**\_ hCursor**: un valor de 32 bits que representa el cursor de consulta Obtenido de CPMCreateQueryOut para el conjunto de filas que contiene el marcador.</span><span class="sxs-lookup"><span data-stu-id="8457e-4023">**\_hCursor**: A 32-bit value representing the query cursor obtained from CPMCreateQueryOut for the rowset containing the bookmark.</span></span>

<span data-ttu-id="8457e-4024">**\_ chapt**: un valor de 32 bits que representa el identificador del segmento que contiene el marcador.</span><span class="sxs-lookup"><span data-stu-id="8457e-4024">**\_chapt**: A 32-bit value representing the handle to the chapter containing the bookmark.</span></span>

<span data-ttu-id="8457e-4025">**\_ BMK**: un valor de 32 bits que representa el identificador del marcador para el que se va a recuperar la posición aproximada.</span><span class="sxs-lookup"><span data-stu-id="8457e-4025">**\_bmk**: A 32-bit value representing the handle to the bookmark for which to retrieve the approximate position.</span></span>

### <a name="22324-cpmgetapproximatepositionout"></a><span data-ttu-id="8457e-4026">2.2.3.24 CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="8457e-4026">2.2.3.24 CPMGetApproximatePositionOut</span></span>

<span data-ttu-id="8457e-4027">El mensaje CPMGetApproximatePositionOut responde a un mensaje CPMGetApproximatePositionIn que describe la posición aproximada del marcador en el capítulo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4027">The CPMGetApproximatePositionOut message replies to a CPMGetApproximatePositionIn message describing the approximate position of the bookmark in the chapter.</span></span> <span data-ttu-id="8457e-4028">El formato del mensaje CPMGetApproximatePositionOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-4028">The format of the CPMGetApproximatePositionOut message that follows the header is:</span></span>



<span data-ttu-id="8457e-4029">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4029">0</span></span>

<span data-ttu-id="8457e-4030">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4030">1</span></span>

<span data-ttu-id="8457e-4031">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4031">2</span></span>

<span data-ttu-id="8457e-4032">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4032">3</span></span>

<span data-ttu-id="8457e-4033">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4033">4</span></span>

<span data-ttu-id="8457e-4034">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4034">5</span></span>

<span data-ttu-id="8457e-4035">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4035">6</span></span>

<span data-ttu-id="8457e-4036">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4036">7</span></span>

<span data-ttu-id="8457e-4037">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4037">8</span></span>

<span data-ttu-id="8457e-4038">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4038">9</span></span>

<span data-ttu-id="8457e-4039">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4039">1</span></span><br/> <span data-ttu-id="8457e-4040">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4040">0</span></span><br/>

<span data-ttu-id="8457e-4041">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4041">1</span></span>

<span data-ttu-id="8457e-4042">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4042">2</span></span>

<span data-ttu-id="8457e-4043">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4043">3</span></span>

<span data-ttu-id="8457e-4044">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4044">4</span></span>

<span data-ttu-id="8457e-4045">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4045">5</span></span>

<span data-ttu-id="8457e-4046">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4046">6</span></span>

<span data-ttu-id="8457e-4047">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4047">7</span></span>

<span data-ttu-id="8457e-4048">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4048">8</span></span>

<span data-ttu-id="8457e-4049">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4049">9</span></span>

<span data-ttu-id="8457e-4050">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4050">2</span></span><br/> <span data-ttu-id="8457e-4051">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4051">0</span></span><br/>

<span data-ttu-id="8457e-4052">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4052">1</span></span>

<span data-ttu-id="8457e-4053">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4053">2</span></span>

<span data-ttu-id="8457e-4054">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4054">3</span></span>

<span data-ttu-id="8457e-4055">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4055">4</span></span>

<span data-ttu-id="8457e-4056">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4056">5</span></span>

<span data-ttu-id="8457e-4057">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4057">6</span></span>

<span data-ttu-id="8457e-4058">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4058">7</span></span>

<span data-ttu-id="8457e-4059">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4059">8</span></span>

<span data-ttu-id="8457e-4060">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4060">9</span></span>

<span data-ttu-id="8457e-4061">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4061">3</span></span><br/> <span data-ttu-id="8457e-4062">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4062">0</span></span><br/>

<span data-ttu-id="8457e-4063">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4063">1</span></span>

<span data-ttu-id="8457e-4064">\_numerator</span><span class="sxs-lookup"><span data-stu-id="8457e-4064">\_numerator</span></span>

<span data-ttu-id="8457e-4065">\_denominator</span><span class="sxs-lookup"><span data-stu-id="8457e-4065">\_denominator</span></span>



 

<span data-ttu-id="8457e-4066">**\_ numerador**: entero de 32 bits sin signo que contiene el número de fila del marcador en el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-4066">**\_numerator**: A 32-bit unsigned integer containing the row number of the bookmark in the rowset.</span></span> <span data-ttu-id="8457e-4067">Si no hay ninguna fila, este campo debe establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4067">If there are no rows, this field MUST be set to 0x00000000.</span></span>

<span data-ttu-id="8457e-4068">**\_ denominador**: entero de 32 bits sin signo que contiene el número de filas del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-4068">**\_denominator**: A 32-bit unsigned integer containing the number of rows in the rowset.</span></span>

### <a name="22325-cpmcomparebmkin"></a><span data-ttu-id="8457e-4069">2.2.3.25 CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4069">2.2.3.25 CPMCompareBmkIn</span></span>

<span data-ttu-id="8457e-4070">El mensaje CPMCompareBmkIn solicita una comparación de dos marcadores en un capítulo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4070">The CPMCompareBmkIn message requests a comparison of two bookmarks in a chapter.</span></span>

<span data-ttu-id="8457e-4071">El formato del mensaje CPMCompareBmkIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-4071">The format of the CPMCompareBmkIn message that follows the header is:</span></span>



<span data-ttu-id="8457e-4072">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4072">0</span></span>

<span data-ttu-id="8457e-4073">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4073">1</span></span>

<span data-ttu-id="8457e-4074">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4074">2</span></span>

<span data-ttu-id="8457e-4075">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4075">3</span></span>

<span data-ttu-id="8457e-4076">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4076">4</span></span>

<span data-ttu-id="8457e-4077">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4077">5</span></span>

<span data-ttu-id="8457e-4078">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4078">6</span></span>

<span data-ttu-id="8457e-4079">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4079">7</span></span>

<span data-ttu-id="8457e-4080">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4080">8</span></span>

<span data-ttu-id="8457e-4081">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4081">9</span></span>

<span data-ttu-id="8457e-4082">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4082">1</span></span><br/> <span data-ttu-id="8457e-4083">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4083">0</span></span><br/>

<span data-ttu-id="8457e-4084">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4084">1</span></span>

<span data-ttu-id="8457e-4085">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4085">2</span></span>

<span data-ttu-id="8457e-4086">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4086">3</span></span>

<span data-ttu-id="8457e-4087">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4087">4</span></span>

<span data-ttu-id="8457e-4088">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4088">5</span></span>

<span data-ttu-id="8457e-4089">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4089">6</span></span>

<span data-ttu-id="8457e-4090">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4090">7</span></span>

<span data-ttu-id="8457e-4091">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4091">8</span></span>

<span data-ttu-id="8457e-4092">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4092">9</span></span>

<span data-ttu-id="8457e-4093">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4093">2</span></span><br/> <span data-ttu-id="8457e-4094">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4094">0</span></span><br/>

<span data-ttu-id="8457e-4095">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4095">1</span></span>

<span data-ttu-id="8457e-4096">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4096">2</span></span>

<span data-ttu-id="8457e-4097">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4097">3</span></span>

<span data-ttu-id="8457e-4098">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4098">4</span></span>

<span data-ttu-id="8457e-4099">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4099">5</span></span>

<span data-ttu-id="8457e-4100">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4100">6</span></span>

<span data-ttu-id="8457e-4101">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4101">7</span></span>

<span data-ttu-id="8457e-4102">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4102">8</span></span>

<span data-ttu-id="8457e-4103">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4103">9</span></span>

<span data-ttu-id="8457e-4104">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4104">3</span></span><br/> <span data-ttu-id="8457e-4105">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4105">0</span></span><br/>

<span data-ttu-id="8457e-4106">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4106">1</span></span>

<span data-ttu-id="8457e-4107">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="8457e-4107">\_hCursor</span></span>

<span data-ttu-id="8457e-4108">\_chapt</span><span class="sxs-lookup"><span data-stu-id="8457e-4108">\_chapt</span></span>

<span data-ttu-id="8457e-4109">\_bmkFirst</span><span class="sxs-lookup"><span data-stu-id="8457e-4109">\_bmkFirst</span></span>

<span data-ttu-id="8457e-4110">\_bmkSecond</span><span class="sxs-lookup"><span data-stu-id="8457e-4110">\_bmkSecond</span></span>



 

<span data-ttu-id="8457e-4111">\_**hCursor**: un valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut para el conjunto de filas que contiene los marcadores.</span><span class="sxs-lookup"><span data-stu-id="8457e-4111">\_**hCursor**: A 32-bit value representing the handle from CPMCreateQueryOut message for the rowset containing the bookmarks.</span></span>

<span data-ttu-id="8457e-4112">\_**chapt**: un valor de 32 bits que representa el identificador del capítulo que contiene los marcadores que se van a comparar.</span><span class="sxs-lookup"><span data-stu-id="8457e-4112">\_**chapt**: A 32-bit value representing the handle of the chapter containing the bookmarks to compare.</span></span>

<span data-ttu-id="8457e-4113">\_**bmkFirst**: un valor de 32 bits que representa el identificador del primer marcador que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="8457e-4113">\_**bmkFirst**: A 32-bit value representing the handle to the first bookmark to compare.</span></span>

<span data-ttu-id="8457e-4114">\_**bmkSecond**: un valor de 32 bits que representa el identificador del segundo marcador que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="8457e-4114">\_**bmkSecond**: A 32-bit value representing the handle to the second bookmark to compare.</span></span>

### <a name="22326-cpmcomparebmkout"></a><span data-ttu-id="8457e-4115">2.2.3.26 CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="8457e-4115">2.2.3.26 CPMCompareBmkOut</span></span>

<span data-ttu-id="8457e-4116">El mensaje CPMCompareBmkOut responde a un mensaje CPMCompareBmkIn con la comparación de los dos marcadores del capítulo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4116">The CPMCompareBmkOut message replies to a CPMCompareBmkIn message with the comparison of the two bookmarks in the chapter.</span></span> <span data-ttu-id="8457e-4117">El formato del mensaje CPMCompareBmkOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-4117">The format of the CPMCompareBmkOut message that follows the header is:</span></span>



<span data-ttu-id="8457e-4118">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4118">0</span></span>

<span data-ttu-id="8457e-4119">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4119">1</span></span>

<span data-ttu-id="8457e-4120">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4120">2</span></span>

<span data-ttu-id="8457e-4121">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4121">3</span></span>

<span data-ttu-id="8457e-4122">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4122">4</span></span>

<span data-ttu-id="8457e-4123">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4123">5</span></span>

<span data-ttu-id="8457e-4124">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4124">6</span></span>

<span data-ttu-id="8457e-4125">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4125">7</span></span>

<span data-ttu-id="8457e-4126">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4126">8</span></span>

<span data-ttu-id="8457e-4127">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4127">9</span></span>

<span data-ttu-id="8457e-4128">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4128">1</span></span><br/> <span data-ttu-id="8457e-4129">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4129">0</span></span><br/>

<span data-ttu-id="8457e-4130">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4130">1</span></span>

<span data-ttu-id="8457e-4131">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4131">2</span></span>

<span data-ttu-id="8457e-4132">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4132">3</span></span>

<span data-ttu-id="8457e-4133">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4133">4</span></span>

<span data-ttu-id="8457e-4134">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4134">5</span></span>

<span data-ttu-id="8457e-4135">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4135">6</span></span>

<span data-ttu-id="8457e-4136">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4136">7</span></span>

<span data-ttu-id="8457e-4137">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4137">8</span></span>

<span data-ttu-id="8457e-4138">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4138">9</span></span>

<span data-ttu-id="8457e-4139">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4139">2</span></span><br/> <span data-ttu-id="8457e-4140">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4140">0</span></span><br/>

<span data-ttu-id="8457e-4141">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4141">1</span></span>

<span data-ttu-id="8457e-4142">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4142">2</span></span>

<span data-ttu-id="8457e-4143">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4143">3</span></span>

<span data-ttu-id="8457e-4144">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4144">4</span></span>

<span data-ttu-id="8457e-4145">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4145">5</span></span>

<span data-ttu-id="8457e-4146">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4146">6</span></span>

<span data-ttu-id="8457e-4147">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4147">7</span></span>

<span data-ttu-id="8457e-4148">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4148">8</span></span>

<span data-ttu-id="8457e-4149">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4149">9</span></span>

<span data-ttu-id="8457e-4150">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4150">3</span></span><br/> <span data-ttu-id="8457e-4151">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4151">0</span></span><br/>

<span data-ttu-id="8457e-4152">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4152">1</span></span>

<span data-ttu-id="8457e-4153">\_dwComparison</span><span class="sxs-lookup"><span data-stu-id="8457e-4153">\_dwComparison</span></span>



 

<span data-ttu-id="8457e-4154">\_**dwComparison**: uno de los siguientes valores, que indica las posiciones relativas de los dos marcadores del capítulo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4154">\_**dwComparison**: One of the following values, indicating the relative positions of the two bookmarks in the chapter.</span></span>



| <span data-ttu-id="8457e-4155">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-4155">Value</span></span>                               | <span data-ttu-id="8457e-4156">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-4156">Meaning</span></span>                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="8457e-4157">DBCOMPARE \_ lt 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8457e-4157">DBCOMPARE\_LT 0x00000000</span></span>            | <span data-ttu-id="8457e-4158">El primer marcador se coloca antes del segundo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4158">The first bookmark is positioned before the second.</span></span>               |
| <span data-ttu-id="8457e-4159">DBCOMPARE \_ EQ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="8457e-4159">DBCOMPARE\_EQ 0x00000001</span></span>            | <span data-ttu-id="8457e-4160">El primer marcador tiene la misma posición que el segundo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4160">The first bookmark has the same position as the second.</span></span>           |
| <span data-ttu-id="8457e-4161">DBCOMPARE \_ gt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="8457e-4161">DBCOMPARE\_GT 0x00000002</span></span>            | <span data-ttu-id="8457e-4162">El primer marcador se coloca después del segundo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4162">The first bookmark is positioned after the second.</span></span>                |
| <span data-ttu-id="8457e-4163">DBCOMPARE \_ ne 0x00000003</span><span class="sxs-lookup"><span data-stu-id="8457e-4163">DBCOMPARE\_NE 0x00000003</span></span>            | <span data-ttu-id="8457e-4164">El primer marcador no tiene la misma posición que el segundo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4164">The first bookmark does not have the same position as the second.</span></span> |
| <span data-ttu-id="8457e-4165">DBCOMPARE \_ NOTCOMPARABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="8457e-4165">DBCOMPARE\_NOTCOMPARABLE 0x00000004</span></span> | <span data-ttu-id="8457e-4166">El primer marcador no es comparable al segundo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4166">The first bookmark is not comparable to the second.</span></span>               |



 

### <a name="22327-cpmrestartpositionin"></a><span data-ttu-id="8457e-4167">2.2.3.27 CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4167">2.2.3.27 CPMRestartPositionIn</span></span>

<span data-ttu-id="8457e-4168">El mensaje CPMRestartPositionIn mueve la posición de captura de un cursor al principio del capítulo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4168">The CPMRestartPositionIn message moves the fetch position for a cursor to the beginning of the chapter.</span></span> <span data-ttu-id="8457e-4169">Como se especifica en la sección 3.1.5.2.12, el servidor responderá con el mismo mensaje, con los resultados de la solicitud contenidos en el \_ campo status del encabezado CISP.</span><span class="sxs-lookup"><span data-stu-id="8457e-4169">As specified in section 3.1.5.2.12, the server will reply using the same message, with the results of the request contained in the \_status field of the CISP header.</span></span>

<span data-ttu-id="8457e-4170">El formato del mensaje CPMRestartPositionIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-4170">The format of the CPMRestartPositionIn message that follows the header is:</span></span>



<span data-ttu-id="8457e-4171">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4171">0</span></span>

<span data-ttu-id="8457e-4172">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4172">1</span></span>

<span data-ttu-id="8457e-4173">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4173">2</span></span>

<span data-ttu-id="8457e-4174">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4174">3</span></span>

<span data-ttu-id="8457e-4175">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4175">4</span></span>

<span data-ttu-id="8457e-4176">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4176">5</span></span>

<span data-ttu-id="8457e-4177">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4177">6</span></span>

<span data-ttu-id="8457e-4178">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4178">7</span></span>

<span data-ttu-id="8457e-4179">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4179">8</span></span>

<span data-ttu-id="8457e-4180">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4180">9</span></span>

<span data-ttu-id="8457e-4181">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4181">1</span></span><br/> <span data-ttu-id="8457e-4182">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4182">0</span></span><br/>

<span data-ttu-id="8457e-4183">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4183">1</span></span>

<span data-ttu-id="8457e-4184">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4184">2</span></span>

<span data-ttu-id="8457e-4185">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4185">3</span></span>

<span data-ttu-id="8457e-4186">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4186">4</span></span>

<span data-ttu-id="8457e-4187">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4187">5</span></span>

<span data-ttu-id="8457e-4188">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4188">6</span></span>

<span data-ttu-id="8457e-4189">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4189">7</span></span>

<span data-ttu-id="8457e-4190">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4190">8</span></span>

<span data-ttu-id="8457e-4191">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4191">9</span></span>

<span data-ttu-id="8457e-4192">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4192">2</span></span><br/> <span data-ttu-id="8457e-4193">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4193">0</span></span><br/>

<span data-ttu-id="8457e-4194">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4194">1</span></span>

<span data-ttu-id="8457e-4195">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4195">2</span></span>

<span data-ttu-id="8457e-4196">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4196">3</span></span>

<span data-ttu-id="8457e-4197">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4197">4</span></span>

<span data-ttu-id="8457e-4198">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4198">5</span></span>

<span data-ttu-id="8457e-4199">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4199">6</span></span>

<span data-ttu-id="8457e-4200">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4200">7</span></span>

<span data-ttu-id="8457e-4201">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4201">8</span></span>

<span data-ttu-id="8457e-4202">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4202">9</span></span>

<span data-ttu-id="8457e-4203">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4203">3</span></span><br/> <span data-ttu-id="8457e-4204">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4204">0</span></span><br/>

<span data-ttu-id="8457e-4205">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4205">1</span></span>

<span data-ttu-id="8457e-4206">\_hCursor (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-4206">\_hCursor (optional)</span></span>

<span data-ttu-id="8457e-4207">\_chapt (opcional)</span><span class="sxs-lookup"><span data-stu-id="8457e-4207">\_chapt (optional)</span></span>



 

<span data-ttu-id="8457e-4208">**\_ hCursor**: un valor de 32 bits que representa el identificador obtenido a partir de un mensaje CPMCreateQueryOut, que identifica la consulta para la que se va a reiniciar la posición.</span><span class="sxs-lookup"><span data-stu-id="8457e-4208">**\_hCursor**: A 32-bit value representing the handle, obtained from a CPMCreateQueryOut message, which identifies the query for which to restart the position.</span></span> <span data-ttu-id="8457e-4209">Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-4209">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="8457e-4210">**\_ chapt**: valor de 32 bits que representa el identificador de un capítulo del que se van a recuperar filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-4210">**\_chapt**: A 32-bit value representing the handle of a chapter from which to retrieve rows.</span></span> <span data-ttu-id="8457e-4211">Este campo debe estar presente cuando el cliente envía el mensaje y debe estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-4211">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

### <a name="22328-cpmfreecursorin"></a><span data-ttu-id="8457e-4212">2.2.3.28 CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4212">2.2.3.28 CPMFreeCursorIn</span></span>

<span data-ttu-id="8457e-4213">El mensaje CPMFreeCursorIn solicita el lanzamiento de un cursor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4213">The CPMFreeCursorIn message requests the release of a cursor.</span></span> <span data-ttu-id="8457e-4214">El formato del mensaje CPMFreeCursorIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-4214">The format of the CPMFreeCursorIn message that follows the header is:</span></span>



<span data-ttu-id="8457e-4215">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4215">0</span></span>

<span data-ttu-id="8457e-4216">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4216">1</span></span>

<span data-ttu-id="8457e-4217">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4217">2</span></span>

<span data-ttu-id="8457e-4218">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4218">3</span></span>

<span data-ttu-id="8457e-4219">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4219">4</span></span>

<span data-ttu-id="8457e-4220">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4220">5</span></span>

<span data-ttu-id="8457e-4221">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4221">6</span></span>

<span data-ttu-id="8457e-4222">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4222">7</span></span>

<span data-ttu-id="8457e-4223">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4223">8</span></span>

<span data-ttu-id="8457e-4224">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4224">9</span></span>

<span data-ttu-id="8457e-4225">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4225">1</span></span><br/> <span data-ttu-id="8457e-4226">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4226">0</span></span><br/>

<span data-ttu-id="8457e-4227">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4227">1</span></span>

<span data-ttu-id="8457e-4228">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4228">2</span></span>

<span data-ttu-id="8457e-4229">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4229">3</span></span>

<span data-ttu-id="8457e-4230">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4230">4</span></span>

<span data-ttu-id="8457e-4231">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4231">5</span></span>

<span data-ttu-id="8457e-4232">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4232">6</span></span>

<span data-ttu-id="8457e-4233">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4233">7</span></span>

<span data-ttu-id="8457e-4234">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4234">8</span></span>

<span data-ttu-id="8457e-4235">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4235">9</span></span>

<span data-ttu-id="8457e-4236">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4236">2</span></span><br/> <span data-ttu-id="8457e-4237">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4237">0</span></span><br/>

<span data-ttu-id="8457e-4238">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4238">1</span></span>

<span data-ttu-id="8457e-4239">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4239">2</span></span>

<span data-ttu-id="8457e-4240">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4240">3</span></span>

<span data-ttu-id="8457e-4241">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4241">4</span></span>

<span data-ttu-id="8457e-4242">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4242">5</span></span>

<span data-ttu-id="8457e-4243">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4243">6</span></span>

<span data-ttu-id="8457e-4244">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4244">7</span></span>

<span data-ttu-id="8457e-4245">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4245">8</span></span>

<span data-ttu-id="8457e-4246">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4246">9</span></span>

<span data-ttu-id="8457e-4247">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4247">3</span></span><br/> <span data-ttu-id="8457e-4248">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4248">0</span></span><br/>

<span data-ttu-id="8457e-4249">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4249">1</span></span>

<span data-ttu-id="8457e-4250">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="8457e-4250">\_hCursor</span></span>



 

<span data-ttu-id="8457e-4251">**\_ hCursor**: un valor de 32 bits que representa el identificador del cursor del mensaje CPMCreateQueryOut que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="8457e-4251">**\_hCursor**: A 32-bit value representing the handle of the cursor from the CPMCreateQueryOut message to release.</span></span>

### <a name="22329-cpmfreecursorout"></a><span data-ttu-id="8457e-4252">2.2.3.29 CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="8457e-4252">2.2.3.29 CPMFreeCursorOut</span></span>

<span data-ttu-id="8457e-4253">El mensaje CPMFreeCursorOut responde a un mensaje CPMFreeCursorIn con los resultados de liberar un cursor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4253">The CPMFreeCursorOut message replies to a CPMFreeCursorIn message with the results of freeing a cursor.</span></span> <span data-ttu-id="8457e-4254">El formato del mensaje CPMFreeCursorOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="8457e-4254">The format of the CPMFreeCursorOut message that follows the header is:</span></span>



<span data-ttu-id="8457e-4255">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4255">0</span></span>

<span data-ttu-id="8457e-4256">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4256">1</span></span>

<span data-ttu-id="8457e-4257">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4257">2</span></span>

<span data-ttu-id="8457e-4258">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4258">3</span></span>

<span data-ttu-id="8457e-4259">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4259">4</span></span>

<span data-ttu-id="8457e-4260">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4260">5</span></span>

<span data-ttu-id="8457e-4261">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4261">6</span></span>

<span data-ttu-id="8457e-4262">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4262">7</span></span>

<span data-ttu-id="8457e-4263">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4263">8</span></span>

<span data-ttu-id="8457e-4264">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4264">9</span></span>

<span data-ttu-id="8457e-4265">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4265">1</span></span><br/> <span data-ttu-id="8457e-4266">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4266">0</span></span><br/>

<span data-ttu-id="8457e-4267">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4267">1</span></span>

<span data-ttu-id="8457e-4268">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4268">2</span></span>

<span data-ttu-id="8457e-4269">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4269">3</span></span>

<span data-ttu-id="8457e-4270">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4270">4</span></span>

<span data-ttu-id="8457e-4271">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4271">5</span></span>

<span data-ttu-id="8457e-4272">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4272">6</span></span>

<span data-ttu-id="8457e-4273">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4273">7</span></span>

<span data-ttu-id="8457e-4274">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4274">8</span></span>

<span data-ttu-id="8457e-4275">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4275">9</span></span>

<span data-ttu-id="8457e-4276">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4276">2</span></span><br/> <span data-ttu-id="8457e-4277">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4277">0</span></span><br/>

<span data-ttu-id="8457e-4278">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4278">1</span></span>

<span data-ttu-id="8457e-4279">2</span><span class="sxs-lookup"><span data-stu-id="8457e-4279">2</span></span>

<span data-ttu-id="8457e-4280">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4280">3</span></span>

<span data-ttu-id="8457e-4281">4</span><span class="sxs-lookup"><span data-stu-id="8457e-4281">4</span></span>

<span data-ttu-id="8457e-4282">5</span><span class="sxs-lookup"><span data-stu-id="8457e-4282">5</span></span>

<span data-ttu-id="8457e-4283">6</span><span class="sxs-lookup"><span data-stu-id="8457e-4283">6</span></span>

<span data-ttu-id="8457e-4284">7</span><span class="sxs-lookup"><span data-stu-id="8457e-4284">7</span></span>

<span data-ttu-id="8457e-4285">8</span><span class="sxs-lookup"><span data-stu-id="8457e-4285">8</span></span>

<span data-ttu-id="8457e-4286">9</span><span class="sxs-lookup"><span data-stu-id="8457e-4286">9</span></span>

<span data-ttu-id="8457e-4287">3</span><span class="sxs-lookup"><span data-stu-id="8457e-4287">3</span></span><br/> <span data-ttu-id="8457e-4288">0</span><span class="sxs-lookup"><span data-stu-id="8457e-4288">0</span></span><br/>

<span data-ttu-id="8457e-4289">1</span><span class="sxs-lookup"><span data-stu-id="8457e-4289">1</span></span>

<span data-ttu-id="8457e-4290">\_cCursorsRemaining</span><span class="sxs-lookup"><span data-stu-id="8457e-4290">\_cCursorsRemaining</span></span>



 

<span data-ttu-id="8457e-4291">**\_ cCursorsRemaining**: entero de 32 bits sin signo que indica el número de cursores que todavía están en uso para la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-4291">**\_cCursorsRemaining**: A 32-bit unsigned integer indicating the number of cursors still in use for the query.</span></span>

### <a name="22330-cpmdisconnect"></a><span data-ttu-id="8457e-4292">2.2.3.30 CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="8457e-4292">2.2.3.30 CPMDisconnect</span></span>

<span data-ttu-id="8457e-4293">El mensaje CPMDisconnect finaliza la conexión con el servidor</span><span class="sxs-lookup"><span data-stu-id="8457e-4293">The CPMDisconnect message ends the connection with the server</span></span>

<span data-ttu-id="8457e-4294">El mensaje no debe incluir un cuerpo; solo se enviará el encabezado del mensaje, tal como se especifica en la sección 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="8457e-4294">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2 is to be sent.</span></span>

### <a name="224-errors"></a><span data-ttu-id="8457e-4295">2.2.4 errores</span><span class="sxs-lookup"><span data-stu-id="8457e-4295">2.2.4 Errors</span></span>

<span data-ttu-id="8457e-4296">Todos los mensajes de protocolo del servicio de indización de contenido deben devolver 0x00000000 en caso de éxito; de lo contrario, devuelven un código de error distinto de cero 32, que puede ser un valor HRESULT o un valor NTSTATUS (consulte la sección 1,8).</span><span class="sxs-lookup"><span data-stu-id="8457e-4296">All Content Indexing Service Protocol messages MUST return 0x00000000 on success; otherwise, they return a 32-bit nonzero error code which can be either an HRESULT or an NTSTATUS value (see section 1.8).</span></span> <span data-ttu-id="8457e-4297">Si un búfer es demasiado pequeño para ajustarse a un resultado, se debe devolver un código de estado de \_ recursos insuficientes \_ (0xC0000009A) y se debe volver a intentar la operación con un búfer mayor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4297">If a buffer is too small to fit a result, a status code of STATUS\_INSUFFICIENT\_RESOURCES (0xC0000009A) MUST be returned and the failing operation should be retried with a larger buffer.</span></span>

<span data-ttu-id="8457e-4298">El resto de los valores de error deben tratarse de la misma.</span><span class="sxs-lookup"><span data-stu-id="8457e-4298">All other error values MUST be treated the same.</span></span>

<span data-ttu-id="8457e-4299">(Tenga en cuenta que actualmente no se superponen los espacios de numeración de HRESULT y NTSTATUS excepto con valores idénticos, pero incluso si fueran conflictos en el futuro, no produciría ningún problema de protocolo, siempre que el valor de estado \_ Los recursos insuficientes \_ siguen siendo únicos, ya que todos los demás valores de error se tratan igual.)</span><span class="sxs-lookup"><span data-stu-id="8457e-4299">(Note that currently the HRESULT and NTSTATUS numbering spaces do not overlap except with values of identical meaning, but even if they were to be conflicts in the future, it would not cause any protocol issues as long as the value for STATUS\_INSUFFICIENT\_RESOURCES remains unique, since all other error values are treated the same.)</span></span>

## <a name="3-protocol-details"></a><span data-ttu-id="8457e-4300">3 Detalles del protocolo</span><span class="sxs-lookup"><span data-stu-id="8457e-4300">3 Protocol Details</span></span>

-   [<span data-ttu-id="8457e-4301">Detalles del servidor 3,1</span><span class="sxs-lookup"><span data-stu-id="8457e-4301">3.1 Server Details</span></span>](#31-server-details)
-   [<span data-ttu-id="8457e-4302">Detalles del cliente 3,2</span><span class="sxs-lookup"><span data-stu-id="8457e-4302">3.2 Client Details</span></span>](#32-client-details)

<span data-ttu-id="8457e-4303">Las solicitudes de mensajes de CISP para consultar de forma remota los catálogos del servicio de indexación no requieren ninguna secuencia determinada.</span><span class="sxs-lookup"><span data-stu-id="8457e-4303">CISP message requests for remotely querying the indexing service catalogs do not require any particular sequence.</span></span> <span data-ttu-id="8457e-4304">Sin embargo, se recomienda que la capa superior se adhiere a una secuencia de mensajes significativa, como en el caso de los mensajes que se reciben fuera de esta secuencia o con datos no válidos, el servidor responderá con un error.</span><span class="sxs-lookup"><span data-stu-id="8457e-4304">It is advised that the higher layer adhere to a meaningful message sequence though, as for messages that are received out of this sequence or with invalid data, the server will respond with an error.</span></span> <span data-ttu-id="8457e-4305">Algunos mensajes también dependen de la capa superior que proporciona datos válidos que se recibieron en los mensajes anteriores de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8457e-4305">Some messages are also dependent on the higher layer providing valid data that was received in messages earlier in the sequence.</span></span>

<span data-ttu-id="8457e-4306">En el diagrama siguiente se muestra una secuencia de mensajes típica para una consulta simple desde un cliente a un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="8457e-4306">A typical message sequence for a simple query from a client to a remote computer is illustrated in the following diagram.</span></span>

![secuencia de mensajes para consulta simple](images/protocoldetails.jpg)

<span data-ttu-id="8457e-4308">Los mensajes representados en el diagrama anterior representan un subconjunto de todos los mensajes de CISP usados para consultar un catálogo de servicios de indexación remota.</span><span class="sxs-lookup"><span data-stu-id="8457e-4308">The messages represented in the preceding diagram represent a subset of all of the CISP messages used for querying a remote indexing service catalog.</span></span>

### <a name="31-server-details"></a><span data-ttu-id="8457e-4309">Detalles del servidor 3,1</span><span class="sxs-lookup"><span data-stu-id="8457e-4309">3.1 Server Details</span></span>

### <a name="311-abstract-data-model"></a><span data-ttu-id="8457e-4310">3.1.1 Modelo de datos abstracto</span><span class="sxs-lookup"><span data-stu-id="8457e-4310">3.1.1 Abstract Data Model</span></span>

<span data-ttu-id="8457e-4311">En la sección siguiente se especifican los datos y el estado mantenidos por el servidor CISP.</span><span class="sxs-lookup"><span data-stu-id="8457e-4311">The following section specifies data and state maintained by the CISP server.</span></span> <span data-ttu-id="8457e-4312">Los datos que se proporcionan aquí son para facilitar la explicación de cómo se comporta el protocolo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4312">The data provided here is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="8457e-4313">En esta sección no se exige que las implementaciones se adhieren a este modelo, siempre y cuando su comportamiento externo sea coherente con el descrito en este documento.</span><span class="sxs-lookup"><span data-stu-id="8457e-4313">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="8457e-4314">Un servicio de indización que implementa CISP debe mantener los siguientes elementos de datos abstractos:</span><span class="sxs-lookup"><span data-stu-id="8457e-4314">An indexing service implementing the CISP MUST maintain the following abstract data elements:</span></span>

-   <span data-ttu-id="8457e-4315">La lista de clientes conectados al servidor</span><span class="sxs-lookup"><span data-stu-id="8457e-4315">The list of clients connected to the server</span></span>
-   <span data-ttu-id="8457e-4316">Información acerca de cada cliente, que incluye:</span><span class="sxs-lookup"><span data-stu-id="8457e-4316">Information about each client, which includes:</span></span>
-   -   <span data-ttu-id="8457e-4317">Versión del cliente (como se indica en el mensaje CPMConnectIn especificado en la sección 2.2.3.6)</span><span class="sxs-lookup"><span data-stu-id="8457e-4317">Client's version (as indicated in the CPMConnectIn message specified in section 2.2.3.6)</span></span>
    -   <span data-ttu-id="8457e-4318">Catálogo asociado al cliente (mediante un mensaje CPMConnectIn)</span><span class="sxs-lookup"><span data-stu-id="8457e-4318">Catalog associated with the client (by a CPMConnectIn message)</span></span>
    -   <span data-ttu-id="8457e-4319">Propiedades de cliente adicionales como se especifica en la sección 2.2.1.21.1.</span><span class="sxs-lookup"><span data-stu-id="8457e-4319">Additional client properties as specified in section 2.2.1.21.1.</span></span>
    -   <span data-ttu-id="8457e-4320">Consulta de búsqueda del cliente</span><span class="sxs-lookup"><span data-stu-id="8457e-4320">Client's search query</span></span>
    -   <span data-ttu-id="8457e-4321">Lista de identificadores de cursor para la consulta y posición en el conjunto de resultados para cada identificador.</span><span class="sxs-lookup"><span data-stu-id="8457e-4321">List of cursor handles for the query and position in result set for each handle.</span></span>
    -   <span data-ttu-id="8457e-4322">Conjunto actual de enlaces</span><span class="sxs-lookup"><span data-stu-id="8457e-4322">Current set of bindings</span></span>
    -   <span data-ttu-id="8457e-4323">Estado actual de la consulta que incluye (para cada cursor):</span><span class="sxs-lookup"><span data-stu-id="8457e-4323">Current status of the query which includes (for each cursor):</span></span>
    -   -   <span data-ttu-id="8457e-4324">Número de filas en el resultado de la consulta</span><span class="sxs-lookup"><span data-stu-id="8457e-4324">Number of rows in query result</span></span>
        -   <span data-ttu-id="8457e-4325">Numerador y denominador de finalización de consulta</span><span class="sxs-lookup"><span data-stu-id="8457e-4325">Numerator and denominator of query completion</span></span>
        -   <span data-ttu-id="8457e-4326">Último número de filas, indicado por el mensaje CPMRatioFinishedOut más reciente para este cursor</span><span class="sxs-lookup"><span data-stu-id="8457e-4326">Last number of rows, reported by most recent CPMRatioFinishedOut message for this cursor</span></span>
        -   <span data-ttu-id="8457e-4327">Si el servidor supervisa la consulta en busca de cambios en los resultados de la consulta y, si se supervisa, qué ha cambiado en los resultados de la consulta desde la última vez que se comunicó al cliente por CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="8457e-4327">Whether the query is monitored by the server for changes in query results and if it is monitored, what changed in the query results since it was last reported to client by CPMSendNotifyOut</span></span>
        -   <span data-ttu-id="8457e-4328">Lista de identificadores de capítulos, atendidos por esta consulta a un cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4328">List of chapters handles, served by this query to a client.</span></span>
        -   <span data-ttu-id="8457e-4329">Lista de identificadores de marcador para cada cursor, servido por esta consulta a un cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4329">List of bookmark handles for each cursor, served by this query to a client.</span></span>

-   <span data-ttu-id="8457e-4330">Estado actual del servicio de indización, que puede ser "no inicializado", "en ejecución" o "cerrando".</span><span class="sxs-lookup"><span data-stu-id="8457e-4330">The current state of the indexing service, which may be "not initialized", "running", or "shutting down".</span></span> <span data-ttu-id="8457e-4331">Tenga en cuenta que la mayoría del servidor horario está en estado "en ejecución".</span><span class="sxs-lookup"><span data-stu-id="8457e-4331">Note that most of the time server is in "running" state.</span></span> <span data-ttu-id="8457e-4332">A continuación se indica el diagrama de la máquina de Estados para el servidor:</span><span class="sxs-lookup"><span data-stu-id="8457e-4332">Following is the state machine diagram for the server:</span></span>

    ![diagrama de equipo de estado del servidor de servicios de Index Server](images/abstractdatamodel.jpg)

-   <span data-ttu-id="8457e-4334">Información sobre el catálogo: el número de documentos indizados, el tamaño del índice, el número de claves únicas, etc. (consulte la sección 2.2.3.1 para completar la lista), State (que corresponde a los valores de dwNewState de la sección 2.2.3.2).</span><span class="sxs-lookup"><span data-stu-id="8457e-4334">Per-catalog information: number of documents indexed, size of index, number of unique keys, etc (see section 2.2.3.1 for complete list), state (which corresponds to the values of dwNewState in section 2.2.3.2).</span></span>
-   <span data-ttu-id="8457e-4335">Para cada idioma admitido, una base de datos de variaciones de palabras, tal como se describe en la sección 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="8457e-4335">For each language supported, a database of word variations as discussed in section 2.2.1.3.</span></span>

### <a name="312-timers"></a><span data-ttu-id="8457e-4336">3.1.2 Temporizadores</span><span class="sxs-lookup"><span data-stu-id="8457e-4336">3.1.2 Timers</span></span>

<span data-ttu-id="8457e-4337">No se requieren temporizadores de protocolos.</span><span class="sxs-lookup"><span data-stu-id="8457e-4337">No protocol timers are required.</span></span>

### <a name="313-initialization"></a><span data-ttu-id="8457e-4338">3.1.3 Inicialización</span><span class="sxs-lookup"><span data-stu-id="8457e-4338">3.1.3 Initialization</span></span>

<span data-ttu-id="8457e-4339">Tras la inicialización, el servidor debe establecer su estado en "no inicializado" e iniciar la escucha de mensajes en la canalización con nombre especificada en la sección 1,9.</span><span class="sxs-lookup"><span data-stu-id="8457e-4339">Upon initialization, the server MUST set its state to "not initialized" and start listening for messages on the named pipe specified in section 1.9.</span></span> <span data-ttu-id="8457e-4340">Después de realizar cualquier otra inicialización interna, debe pasar al estado "en ejecución".</span><span class="sxs-lookup"><span data-stu-id="8457e-4340">After doing any other internal initialization, it MUST transition to the "running" state.</span></span>

### <a name="314-higher-layer-triggered-events"></a><span data-ttu-id="8457e-4341">3.1.4 Eventos desencadenados al más alto nivel</span><span class="sxs-lookup"><span data-stu-id="8457e-4341">3.1.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="8457e-4342">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8457e-4342">None.</span></span>

### <a name="315-message-processing-and-sequencing-rules"></a><span data-ttu-id="8457e-4343">Reglas de procesamiento y secuenciación de mensajes de 3.1.5</span><span class="sxs-lookup"><span data-stu-id="8457e-4343">3.1.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="8457e-4344">Siempre que se produce un error durante el procesamiento de un mensaje enviado por un cliente, el servidor debe notificar un error al cliente de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4344">Whenever there is an error occurs during processing of a message sent by a client the server MUST report an error back to the client as follows:</span></span>

-   <span data-ttu-id="8457e-4345">Detener el procesamiento del mensaje enviado por el cliente</span><span class="sxs-lookup"><span data-stu-id="8457e-4345">Stop processing the message sent by the client</span></span>
-   <span data-ttu-id="8457e-4346">Responda con el encabezado del mensaje (solo) del mensaje enviado por el cliente, manteniendo el \_ campo MSG intacto.</span><span class="sxs-lookup"><span data-stu-id="8457e-4346">Respond with the message header (only) of the message sent by the client, keeping \_msg field intact.</span></span>
-   <span data-ttu-id="8457e-4347">Establezca el \_ campo Estado en el valor del código de error.</span><span class="sxs-lookup"><span data-stu-id="8457e-4347">Set the \_status field to the error code value.</span></span>

<span data-ttu-id="8457e-4348">Cuando llega un mensaje, el servidor debe comprobar el \_ valor del campo MSG para ver si se trata de un tipo conocido (consulte la sección 2.2.2).</span><span class="sxs-lookup"><span data-stu-id="8457e-4348">When a message arrives, the server MUST check the \_msg field value to see if it is a known type (see section 2.2.2).</span></span> <span data-ttu-id="8457e-4349">Si no se conoce el tipo, debe notificar un \_ error de parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4349">If the type is not known, it MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="8457e-4350">El servidor debe validar el \_ valor del campo ulChecksum si el tipo de mensaje es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="8457e-4350">The server MUST then validate the \_ulChecksum field value if the message type is one of the following:</span></span>

-   <span data-ttu-id="8457e-4351">CPMConnectIn (0x000000C8)</span><span class="sxs-lookup"><span data-stu-id="8457e-4351">CPMConnectIn (0x000000C8)</span></span>
-   <span data-ttu-id="8457e-4352">CPMCreateQueryIn (0x000000CA)</span><span class="sxs-lookup"><span data-stu-id="8457e-4352">CPMCreateQueryIn (0x000000CA)</span></span>
-   <span data-ttu-id="8457e-4353">CPMSetBindingsIn (0x000000D0)</span><span class="sxs-lookup"><span data-stu-id="8457e-4353">CPMSetBindingsIn (0x000000D0)</span></span>
-   <span data-ttu-id="8457e-4354">CPMGetRowsIn (0x000000CC)</span><span class="sxs-lookup"><span data-stu-id="8457e-4354">CPMGetRowsIn (0x000000CC)</span></span>
-   <span data-ttu-id="8457e-4355">CPMFetchValueIn (0x000000E4)</span><span class="sxs-lookup"><span data-stu-id="8457e-4355">CPMFetchValueIn (0x000000E4)</span></span>

<span data-ttu-id="8457e-4356">Para validar el \_ valor del campo ulChecksum, el servidor debe comprobar el valor especificado por el cliente en el \_ campo iClientVersion del mensaje CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-4356">To validate the \_ulChecksum field value, the server MUST check the value the client specified in the \_iClientVersion field in the CPMConnectIn message.</span></span>

<span data-ttu-id="8457e-4357">Si el \_ campo iClientVersion no se establece en 0x00000008 y el \_ campo ulChecksum no se establece en 0x00000000, el servidor debe notificar un \_ error de parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4357">If the \_iClientVersion field is not set to 0x00000008 and the \_ulChecksum field is not set to 0x00000000, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="8457e-4358">El servidor no debe validar el \_ campo ulChecksum para los clientes. establezca el \_ campo iClientVersion en un valor inferior a 0x00000008.</span><span class="sxs-lookup"><span data-stu-id="8457e-4358">Server MUST NOT validate the \_ulChecksum field for clients the set the \_iClientVersion field to a value less than 0x00000008.</span></span>

<span data-ttu-id="8457e-4359">Si el \_ valor del campo iClientVersionfield es 0x00000008 o superior, el servidor debe validar que el \_ campo ulChecksum se calculó como se especifica en la sección 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="8457e-4359">If the \_iClientVersionfield field value is 0x00000008 or greater, the server MUST validate that the \_ulChecksum field was calculated as specified in section 3.2.4.</span></span> <span data-ttu-id="8457e-4360">Si el \_ valor de ulChecksum no es válido, el servidor debe notificar un \_ error de parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4360">If the \_ulChecksum value is invalid, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="8457e-4361">A continuación, el servidor comprueba en qué estado se encuentra.</span><span class="sxs-lookup"><span data-stu-id="8457e-4361">Next, the server checks which state is it in.</span></span> <span data-ttu-id="8457e-4362">Si su estado es "no inicializado", el servidor debe notificar un error de CI \_ E \_ no \_ inicializado (0x8004180B).</span><span class="sxs-lookup"><span data-stu-id="8457e-4362">If its state is "not initialized" the server MUST report a CI\_E\_NOT\_INITIALIZED (0x8004180B) error.</span></span> <span data-ttu-id="8457e-4363">Si el estado es "cerrando", el servidor debe notificar un \_ error de cierre de CI E \_ (0x80041812).</span><span class="sxs-lookup"><span data-stu-id="8457e-4363">If the state is "shutting down" the server MUST report a CI\_E\_SHUTDOWN (0x80041812) error.</span></span>

<span data-ttu-id="8457e-4364">Una vez que se ha determinado que un encabezado es válido y el servidor está en estado "en ejecución", se debe realizar un procesamiento adicional específico del mensaje tal y como se especifica en las subsecciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="8457e-4364">Once a header has been determined to be valid and the server to be in "running" state, further message-specific processing MUST be done as specified in the subsections below.</span></span>

### <a name="3151-remote-indexing-service-catalog-management"></a><span data-ttu-id="8457e-4365">Administración de catálogos del servicio de indexación remota de 3.1.5.1</span><span class="sxs-lookup"><span data-stu-id="8457e-4365">3.1.5.1 Remote Indexing Service Catalog Management</span></span>

### <a name="31511-receiving-a-cpmcistateinout-request"></a><span data-ttu-id="8457e-4366">3.1.5.1.1 recibir una solicitud de CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="8457e-4366">3.1.5.1.1 Receiving a CPMCiStateInOut Request</span></span>

<span data-ttu-id="8457e-4367">Cuando el servidor recibe una solicitud de mensaje de CPMCIStateInOut desde el cliente, el servidor debe comprobar primero si el cliente está en una lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="8457e-4367">When the server receives a CPMCIStateInOut message request from the client, the server MUST first check if the client is in a list of connected clients.</span></span> <span data-ttu-id="8457e-4368">Si el cliente no está en la lista, el servidor debe notificar un \_ error de parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4368">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="8457e-4369">De lo contrario, debe responder al cliente con un mensaje CPMCIStateInOut, rellenándolo con información sobre el catálogo asociado del cliente, tal como se especifica en la sección 2.2.3.1.</span><span class="sxs-lookup"><span data-stu-id="8457e-4369">Otherwise, it MUST respond to the client with a CPMCIStateInOut message, filling it in with information about the client's associated catalog as specified in Section 2.2.3.1.</span></span>

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a><span data-ttu-id="8457e-4370">3.1.5.1.2 recibir una solicitud de CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4370">3.1.5.1.2 Receiving a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="8457e-4371">Cuando el servidor recibe una solicitud de mensaje de CPMSetCatStateIn desde el cliente, el servidor debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4371">When the server receives a CPMSetCatStateIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4372">Compruebe que el cliente tiene acceso administrativo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4372">Check that client has administrative access.</span></span> <span data-ttu-id="8457e-4373">Si el cliente no tiene acceso administrativo, el servidor debe notificar un \_ error de acceso \_ denegado (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="8457e-4373">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="8457e-4374">Si \_ dwNewState no es igual que CiCAT \_ todos \_ abiertos, cambie el estado del catálogo especificado en el campo CatName de acuerdo con lo especificado en el \_ campo dwNewState.</span><span class="sxs-lookup"><span data-stu-id="8457e-4374">If \_dwNewState is not equal to CICAT\_ALL\_OPENED then change the state of the catalog specified in the CatName field as specified by the \_dwNewState field.</span></span> <span data-ttu-id="8457e-4375">Vea la sección 2.2.3.2 para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="8457e-4375">See Section 2.2.3.2 for more details.</span></span> <span data-ttu-id="8457e-4376">Si el servidor no encuentra un catálogo con el nombre especificado en el campo CatName, el servidor debe devolver un error de \_ parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4376">If the server does not locate a catalog with the name specified in the CatName field, the server MUST return a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8457e-4377">Responder al cliente con un mensaje CPMSetCatStateOut, donde \_ DWOLDSTATE debe establecerse en el estado anterior del catálogo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4377">Respond to the client with a CPMSetCatStateOut message, where \_dwOldState MUST be set to the previous state of the catalog.</span></span> <span data-ttu-id="8457e-4378">Si \_ dwNewState es igual a CiCAT \_ todos los \_ abiertos, el servidor debe comprobar el estado de todos los catálogos y, si todos ellos se han iniciado, debe establecer \_ dwOldState en 0x00000001 y, de lo contrario, establecer \_ dwOldState en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4378">If \_dwNewState is equal to CICAT\_ALL\_OPENED the server MUST check the status of all catalogs and if all of them are started it MUST set \_dwOldState to 0x00000001, and otherwise set \_dwOldState to 0x00000000.</span></span>

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="8457e-4379">3.1.5.1.3 recibir una solicitud de CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4379">3.1.5.1.3 Receiving a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="8457e-4380">Cuando el servidor recibe una solicitud de mensaje CPMUpdateDocumentsIn, el servidor debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4380">When the server receives a CPMUpdateDocumentsIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4381">Compruebe si el cliente está en una lista de clientes conectados (que tienen asociado un catálogo).</span><span class="sxs-lookup"><span data-stu-id="8457e-4381">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="8457e-4382">Si el cliente no está en la lista, el servidor debe notificar un \_ error de parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4382">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8457e-4383">Compruebe que el cliente tiene acceso administrativo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4383">Check that client has administrative access.</span></span> <span data-ttu-id="8457e-4384">Si el cliente no tiene acceso administrativo al servidor, el servidor debe notificar un error de \_ acceso \_ denegado (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="8457e-4384">If the client does not have administrative access to the server, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="8457e-4385">Comienza el proceso de indización de la ruta de acceso especificada por el cliente, realizando un examen completo o incremental, en función del valor del \_ campo Flag en el mensaje CPMUpdateDocumentsIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-4385">Begin the process of indexing the path specified by the client, doing a full or incremental scan, depending on value of \_flag field in CPMUpdateDocumentsIn message.</span></span> <span data-ttu-id="8457e-4386">Si la ruta de acceso no se ha indizado previamente, debe agregarse a la colección de ubicaciones indizadas y realizar un examen completo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4386">If the path was not previously indexed, it MUST be added to the collection of indexed locations and a full scan performed.</span></span> <span data-ttu-id="8457e-4387">Si se especifica un valor no válido del \_ campo de marca, el servidor debe actuar como si la \_ marca estuviera establecida en UPD \_ init y realizar un examen completo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4387">If an illegal value of the \_flag field is specified, the server MUST act as if \_flag was set to UPD\_INIT and perform a full scan.</span></span> <span data-ttu-id="8457e-4388">Esta operación debe realizarse en el catálogo asociado al cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4388">This operation MUST be performed in the catalog associated with the client.</span></span>
-   <span data-ttu-id="8457e-4389">Responda al cliente con el encabezado del mensaje de CPMUpdateDocumentsIn y establezca el \_ campo Estado en los resultados de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8457e-4389">Respond to the client with the message header for the CPMUpdateDocumentsIn, and set the \_status field to the results of the request.</span></span>

### <a name="31514-receiving-a-cpmforcemergein-request"></a><span data-ttu-id="8457e-4390">3.1.5.1.4 recibir una solicitud de CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4390">3.1.5.1.4 Receiving a CPMForceMergeIn Request</span></span>

<span data-ttu-id="8457e-4391">Cuando el servidor recibe una solicitud de mensaje CPMForceMergeIn, el servidor debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4391">When the server receives a CPMForceMergeIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4392">Compruebe si el cliente está en una lista de clientes conectados (que tienen asociado un catálogo).</span><span class="sxs-lookup"><span data-stu-id="8457e-4392">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="8457e-4393">Si el cliente no está en la lista, el servidor debe notificar un \_ error de parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4393">If client is not in the list the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8457e-4394">Compruebe que el cliente tiene acceso administrativo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4394">Check that client has administrative access.</span></span> <span data-ttu-id="8457e-4395">Si el cliente no tiene acceso administrativo, el servidor debe notificar un \_ error de acceso \_ denegado (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="8457e-4395">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="8457e-4396">Comience cualquier proceso de mantenimiento necesario para mejorar el rendimiento de las consultas en un catálogo, asociado al cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4396">Begin any process of maintenance necessary to improve query performance on a catalog, associated with the client.</span></span>
-   <span data-ttu-id="8457e-4397">Responda al cliente con un encabezado de mensaje para CPMForceMergeIn y establezca el \_ campo Estado en los resultados de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8457e-4397">Respond to the client with a message header for the CPMForceMergeIn, and set the \_status field to the results of the request.</span></span>

<span data-ttu-id="8457e-4398">Tenga en cuenta que el proceso de mantenimiento es asincrónico y puede continuar después de que el cliente reciba el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8457e-4398">Note that process of maintenance is asynchronous and can continue after client receives the response message.</span></span> <span data-ttu-id="8457e-4399">Este proceso no afecta directamente al Protocolo de ninguna manera (a excepción del tiempo de respuesta).</span><span class="sxs-lookup"><span data-stu-id="8457e-4399">This process does not directly impact the protocol in any way (other than response time).</span></span>

### <a name="3152-remote-indexing-service-querying"></a><span data-ttu-id="8457e-4400">3.1.5.2 consulta de servicio de indexación remota</span><span class="sxs-lookup"><span data-stu-id="8457e-4400">3.1.5.2 Remote Indexing Service Querying</span></span>

### <a name="31521-receiving-a-cpmconnectin-request"></a><span data-ttu-id="8457e-4401">3.1.5.2.1 recibir una solicitud de CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4401">3.1.5.2.1 Receiving a CPMConnectIn Request</span></span>

<span data-ttu-id="8457e-4402">Cuando el servidor recibe una solicitud CPMConnectIn de un cliente, el servidor debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4402">When the server receives a CPMConnectIn request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4403">Compruebe si el cliente está en la lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="8457e-4403">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="8457e-4404">En este caso, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4404">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8457e-4405">Comprueba si el catálogo especificado existe y no está en estado detenido.</span><span class="sxs-lookup"><span data-stu-id="8457e-4405">Checks if the specified catalog exists and not in the stopped state.</span></span> <span data-ttu-id="8457e-4406">Si no es así, el servidor debe tener un error de CI \_ E \_ no \_ Catalog (0x8004181D) de informe.</span><span class="sxs-lookup"><span data-stu-id="8457e-4406">If this is not the case then the server MUST a report CI\_E\_NO\_CATALOG (0x8004181D) error.</span></span>
-   <span data-ttu-id="8457e-4407">Agregue el cliente a la lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="8457e-4407">Add the client to the list of connected clients.</span></span>
-   <span data-ttu-id="8457e-4408">Asocie el catálogo con el cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4408">Associate the catalog with the client.</span></span>
-   <span data-ttu-id="8457e-4409">Almacene la información que se pasa en el mensaje CPMConnectIn (como el nombre del catálogo, la versión del cliente, etc.) en el estado del cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4409">Store the information passed in the CPMConnectIn message (such as catalog name, client version, etc.) in the client state.</span></span>
-   <span data-ttu-id="8457e-4410">Responder al cliente con un mensaje CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4410">Respond to the client with a CPMConnectOut message.</span></span>

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a><span data-ttu-id="8457e-4411">3.1.5.2.2 recibir una solicitud de CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4411">3.1.5.2.2 Receiving a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="8457e-4412">Cuando el servidor recibe una solicitud de mensaje de CPMCreateQueryIn desde un cliente, el servidor debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4412">When the server receives a CPMCreateQueryIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4413">Compruebe si el cliente está en la lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="8457e-4413">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="8457e-4414">Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4414">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8457e-4415">Compruebe si el cliente ya tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="8457e-4415">Check if the client already has a query associated with it.</span></span> <span data-ttu-id="8457e-4416">En este caso, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4416">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8457e-4417">Compruebe si el catálogo asociado al cliente está en el estado que permite procesar la consulta (CICAT \_ ReadOnly o CiCAT \_ grabable).</span><span class="sxs-lookup"><span data-stu-id="8457e-4417">Check if the catalog associated with the client is in state which allows query to be processed (CICAT\_READONLY or CICAT\_WRITABLE).</span></span> <span data-ttu-id="8457e-4418">Si no es así, el servidor debe notificar un error QUERY \_ S \_ no \_ query (0x8004160C).</span><span class="sxs-lookup"><span data-stu-id="8457e-4418">If this is not the case, the server MUST report a QUERY\_S\_NO\_QUERY (0x8004160C) error.</span></span>
-   <span data-ttu-id="8457e-4419">Analiza el conjunto de restricciones, los criterios de ordenación y las agrupaciones especificados en la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-4419">Parse the restriction set, sort orders, and groupings specified in the query.</span></span> <span data-ttu-id="8457e-4420">Si el servidor encuentra un error, debe informar de un error adecuado.</span><span class="sxs-lookup"><span data-stu-id="8457e-4420">If the server encounters an error, it MUST report an appropriate error.</span></span> <span data-ttu-id="8457e-4421">Si se produce un error en este paso por cualquier otro motivo, el servidor debe notificar el error encontrado.</span><span class="sxs-lookup"><span data-stu-id="8457e-4421">If this step fails for any other reason, the server MUST report the error encountered.</span></span> <span data-ttu-id="8457e-4422">Para obtener información acerca de los errores de consulta del servicio de indización, consulte \[ MSDN-QUERYERR \] .</span><span class="sxs-lookup"><span data-stu-id="8457e-4422">For information about indexing service query errors, see \[MSDN-QUERYERR\].</span></span>
-   <span data-ttu-id="8457e-4423">Guarde la consulta de búsqueda en el estado del cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4423">Save the search query in the state for the client.</span></span>
-   <span data-ttu-id="8457e-4424">Realice los preparativos necesarios para servir las filas a un cliente y asocie la consulta con los identificadores de cursor adecuados (dependiendo de la información pasada en el mensaje CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="8457e-4424">Make any preparations needed to serve rows to a client and associate the query with appropriate cursor handles (depending on information passed in CPMCreateQueryIn message).</span></span>
-   <span data-ttu-id="8457e-4425">Agregue esos identificadores a la lista de identificadores de cursor del cliente e inicialice listas de identificadores de capítulo y marcadores.</span><span class="sxs-lookup"><span data-stu-id="8457e-4425">Add those handles to client's list of cursor handles, and initialize lists of chapter handles and bookmarks.</span></span>
-   <span data-ttu-id="8457e-4426">Inicializa la lista de identificadores de capítulo para cada cursor de esta consulta en DB \_ null \_ HCHAPTER</span><span class="sxs-lookup"><span data-stu-id="8457e-4426">Initialize list of chapter handles for every cursor in this query to DB\_NULL\_HCHAPTER</span></span>
-   <span data-ttu-id="8457e-4427">Inicializa la lista de identificadores de marcador para cada cursor de esta consulta en un conjunto de DBBMK \_ First y DBBMK \_ Last.</span><span class="sxs-lookup"><span data-stu-id="8457e-4427">Initialize list of bookmark handles for every cursor in this query to a set of DBBMK\_FIRST and DBBMK\_LAST.</span></span>
-   <span data-ttu-id="8457e-4428">Marque la consulta como no supervisada para los cambios.</span><span class="sxs-lookup"><span data-stu-id="8457e-4428">Mark the query as not monitored for changes.</span></span>
-   <span data-ttu-id="8457e-4429">Inicializa el número de filas en el número calculado actualmente de filas (que puede ser 0 si la consulta no se inició para ejecutar o algún número si la consulta está en un proceso de ejecución) e inicializa el numerador y el denominador de finalización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-4429">Initialize the number of rows to the currently calculated number of rows (which can be 0 if query did not start to execute or some number if query is in a process of execution), and initialize the numerator and denominator of query completion.</span></span>
-   <span data-ttu-id="8457e-4430">Responder al cliente con un mensaje CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4430">Respond to the client with a CPMCreateQueryOut message.</span></span>

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a><span data-ttu-id="8457e-4431">3.1.5.2.3 recibir una solicitud de CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4431">3.1.5.2.3 Receiving a CPMGetQueryStatusIn Request</span></span>

<span data-ttu-id="8457e-4432">Cuando el servidor recibe una solicitud de mensaje de CPMGetQueryStatusIn desde un cliente, el servidor debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4432">When the server receives a CPMGetQueryStatusIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4433">Compruebe si el cliente tiene consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="8457e-4433">Check if the client has query associated with it.</span></span> <span data-ttu-id="8457e-4434">Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4434">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8457e-4435">Compruebe si el identificador de cursor está en una lista de identificadores de cursor del cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4435">Check if the cursor handle is in a list of client's cursor handles.</span></span> <span data-ttu-id="8457e-4436">Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8457e-4436">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8457e-4437">Preparar un mensaje CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4437">Prepare a CPMGetQueryStatusOut message.</span></span> <span data-ttu-id="8457e-4438">El servidor debe recuperar el estado de la consulta actual y establecerlo en el \_ campo QStatus (consulte 2.2.3.11 para ver los valores posibles).</span><span class="sxs-lookup"><span data-stu-id="8457e-4438">The server MUST retrieve the current query status and set it in the \_QStatus field (see 2.2.3.11 for possible values).</span></span> <span data-ttu-id="8457e-4439">Si se produce un error en este paso por cualquier motivo, el servidor debe informar de un error.</span><span class="sxs-lookup"><span data-stu-id="8457e-4439">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="8457e-4440">Responder al cliente con el mensaje CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4440">Respond to the client with the CPMGetQueryStatusOut message.</span></span>

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a><span data-ttu-id="8457e-4441">3.1.5.2.4 recibir una solicitud de CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4441">3.1.5.2.4 Receiving a CPMGetQueryStatusExIn Request</span></span>

<span data-ttu-id="8457e-4442">Cuando el servidor recibe una solicitud de mensaje de CPMGetQueryStatusExIn desde un cliente, el servidor debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4442">When the server receives a CPMGetQueryStatusExIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4443">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="8457e-4443">Check if the client has a query associated with it.</span></span> <span data-ttu-id="8457e-4444">Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4444">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8457e-4445">Compruebe si el identificador de cursor que se ha pasado está en una lista de identificadores de cursor del cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4445">Check if the cursor handle passed is in a list of client's cursor handles.</span></span> <span data-ttu-id="8457e-4446">Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8457e-4446">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8457e-4447">Preparar un mensaje CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4447">Prepare a CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="8457e-4448">El servidor debe recuperar el estado de la consulta actual y el progreso de la consulta y establecer QStatus (vea 2.2.3.11 para ver los valores posibles), \_ dwRatioFinishedDenominator y \_ dwRatioFinishedNumerator, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4448">The server MUST retrieve the current query status and query progress and set QStatus (see 2.2.3.11 for possible values), \_dwRatioFinishedDenominator and \_dwRatioFinishedNumerator respectively.</span></span> <span data-ttu-id="8457e-4449">A continuación, debe establecer el número de filas de los resultados de la consulta en \_ cRowsTotal.</span><span class="sxs-lookup"><span data-stu-id="8457e-4449">It MUST then set the number of rows in the query results to \_cRowsTotal.</span></span> <span data-ttu-id="8457e-4450">Si se produce un error en este paso por cualquier motivo, el servidor debe notificar que se ha detectado un error.</span><span class="sxs-lookup"><span data-stu-id="8457e-4450">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="8457e-4451">Recupere información sobre el catálogo del cliente y rellene \_ cFilteredDocuments y \_ cDocumentsToFilter.</span><span class="sxs-lookup"><span data-stu-id="8457e-4451">Retrieve information about client's catalog and fill in \_cFilteredDocuments and \_cDocumentsToFilter.</span></span> <span data-ttu-id="8457e-4452">Si por algún motivo se produce un error en este paso, el servidor debe notificar que se ha detectado un error.</span><span class="sxs-lookup"><span data-stu-id="8457e-4452">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="8457e-4453">Recupere la posición del marcador indicado por el identificador en el \_ campo BMK y rellene el \_ campo iRowBmk restante en el mensaje CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4453">Retrieve the position of the bookmark indicated by the handle in the \_bmk field, and fill the remaining \_iRowBmk field in the CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="8457e-4454">Si se produce un error en este paso por cualquier motivo, el servidor debe notificar que se ha detectado un error.</span><span class="sxs-lookup"><span data-stu-id="8457e-4454">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="8457e-4455">Responder al cliente con el mensaje CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4455">Respond to the client with the CPMGetQueryStatusExOut message.</span></span>

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a><span data-ttu-id="8457e-4456">3.1.5.2.5 recibir una solicitud de CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4456">3.1.5.2.5 Receiving a CPMRatioFinishedIn Request</span></span>

<span data-ttu-id="8457e-4457">Cuando el servidor recibe una solicitud de mensaje de CPMRatioFinishedIn desde un cliente, el servidor debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4457">When the server receives a CPMRatioFinishedIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4458">Compruebe si el cliente tiene consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="8457e-4458">Check if the client has query associated with it.</span></span> <span data-ttu-id="8457e-4459">Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4459">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8457e-4460">Compruebe si el identificador de cursor que se ha pasado está en la lista de identificadores de cursor del cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4460">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="8457e-4461">Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8457e-4461">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8457e-4462">Preparar un mensaje CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4462">Prepare a CPMRatioFinishedOut message.</span></span> <span data-ttu-id="8457e-4463">El servidor debe recuperar el estado de la consulta del cliente y rellenar los \_ campos ulNumerator, \_ ulDenominator y \_ Crows.</span><span class="sxs-lookup"><span data-stu-id="8457e-4463">The server MUST retrieve the client's query status and fill in \_ulNumerator, \_ulDenominator and \_cRows fields.</span></span> <span data-ttu-id="8457e-4464">Si por algún motivo se produce un error en este paso, el servidor debe notificar que se ha detectado un error.</span><span class="sxs-lookup"><span data-stu-id="8457e-4464">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="8457e-4465">Si \_ Crows es igual al último número de filas del que se ha comunicado esta consulta, establezca \_ fNewRows en 0x00000000; de lo contrario, establézcalo en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8457e-4465">If \_cRows is equal to the last reported number of rows for this query, then set \_fNewRows to 0x00000000, otherwise set it to 0x00000001.</span></span>
-   <span data-ttu-id="8457e-4466">Actualice el último número de filas del que se ha comunicado esta consulta al valor de \_ Crows.</span><span class="sxs-lookup"><span data-stu-id="8457e-4466">Update the last reported number of rows for this query to the value of \_cRows.</span></span>
-   <span data-ttu-id="8457e-4467">Responder al cliente con el mensaje CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4467">Respond to the client with the CPMRatioFinishedOut message.</span></span>

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a><span data-ttu-id="8457e-4468">3.1.5.2.6 recibir una solicitud de CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4468">3.1.5.2.6 Receiving a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="8457e-4469">Cuando el servidor recibe una solicitud de mensaje de CPMSetBindingsIn desde un cliente, el servidor debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4469">When the server receives a CPMSetBindingsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4470">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="8457e-4470">Check if the client has a query associated with it.</span></span> <span data-ttu-id="8457e-4471">Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4471">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8457e-4472">Compruebe si el identificador de cursor que se ha pasado está en la lista de identificadores de cursor del cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4472">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="8457e-4473">Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8457e-4473">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8457e-4474">Compruebe que la información de los enlaces es válida (es decir, la columna especifica el valor, la longitud o el estado que se va a devolver; no se superponen en los enlaces del valor, la longitud o el estado; y el valor, la longitud y el estado caben en el tamaño de fila especificado) y si no se notifica un error de la base de datos \_ \_ BADBINDINFO</span><span class="sxs-lookup"><span data-stu-id="8457e-4474">Verify that bindings information is valid (i.e., column at least specifies value, length or status to be returned; no overlap in bindings for value, length or status; and value, length and status fit in the row size specified) and if not report a DB\_E\_BADBINDINFO (0x80040E08) error.</span></span>
-   <span data-ttu-id="8457e-4475">Guarde la información de enlace asociada a las columnas especificadas en el campo aColumns.</span><span class="sxs-lookup"><span data-stu-id="8457e-4475">Save the binding information associated with the columns specified in the aColumns field.</span></span> <span data-ttu-id="8457e-4476">Si por algún motivo se produce un error en este paso, el servidor debe notificar que se ha detectado un error.</span><span class="sxs-lookup"><span data-stu-id="8457e-4476">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="8457e-4477">Responda al cliente con un encabezado de mensaje (solo) con \_ el mensaje establecido en CPMSetBindingsIn y \_ el estado establecido en los resultados del enlace especificado.</span><span class="sxs-lookup"><span data-stu-id="8457e-4477">Respond to the client with a message header (only) with \_msg set to CPMSetBindingsIn, and \_status set to the results of the specified binding.</span></span>

### <a name="31527-receiving-a-cpmgetrowsin-request"></a><span data-ttu-id="8457e-4478">3.1.5.2.7 recibir una solicitud de CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4478">3.1.5.2.7 Receiving a CPMGetRowsIn Request</span></span>

<span data-ttu-id="8457e-4479">Cuando el servidor recibe una solicitud de mensaje de CPMGetRowsIn desde un cliente, el servidor debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4479">When the server receives a CPMGetRowsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4480">Compruebe si el cliente tiene consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="8457e-4480">Check if the client has query associated with it.</span></span> <span data-ttu-id="8457e-4481">Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4481">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8457e-4482">Compruebe si el identificador de cursor que se pasa está en athelist de los identificadores de cursor del cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4482">Check if the cursor handle passed is in athelist of the client's cursor handles.</span></span> <span data-ttu-id="8457e-4483">Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8457e-4483">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8457e-4484">Compruebe si el cliente tiene un conjunto actual de enlaces.</span><span class="sxs-lookup"><span data-stu-id="8457e-4484">Check if the client has a current set of bindings.</span></span> <span data-ttu-id="8457e-4485">Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8457e-4485">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8457e-4486">Preparar un mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4486">Prepare a CPMGetRowsOut message.</span></span> <span data-ttu-id="8457e-4487">El servidor debe colocar el cursor en los resultados de la consulta como se indica en la descripción de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8457e-4487">The server MUST position the cursor in query results as indicated by the seek description.</span></span> <span data-ttu-id="8457e-4488">Si por algún motivo se produce un error en este paso, el servidor debe notificar que se ha detectado un error.</span><span class="sxs-lookup"><span data-stu-id="8457e-4488">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="8457e-4489">Obtiene tantas filas como quepan en un búfer, cuyo tamaño se indica mediante \_ cbReadBuffer, pero no más de lo indicado por \_ cRowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="8457e-4489">Fetch as many rows as fits in a buffer, the size of which is indicated by \_cbReadBuffer, but not more than indicated by \_cRowsToTransfer.</span></span> <span data-ttu-id="8457e-4490">Al capturar filas, el servidor debe comparar el tipo de valor de propiedad de cada columna seleccionada con el tipo especificado en el conjunto actual de enlaces del cliente (sección 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="8457e-4490">When fetching rows, the server MUST compare each selected column's property value type to the type specified in the Client's current set of bindings (section 3.1.1).</span></span> <span data-ttu-id="8457e-4491">Si el tipo del enlace no es una variante de VT \_ , el servidor debe intentar convertir el valor de la propiedad de la columna a ese tipo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4491">If the type in the binding is not VT\_VARIANT, the server MUST attempt to convert the column's property value to that type.</span></span> <span data-ttu-id="8457e-4492">De lo contrario, si \_ se establece la marca DBPROP USEEXTENDEDDBTYPES en el conjunto de propiedades DBPROPSET QUERYEXT del cliente \_ , o si el valor de la propiedad de la columna no es un \_ tipo de vector VT, el valor de la propiedad se debe devolver en su tipo normal.</span><span class="sxs-lookup"><span data-stu-id="8457e-4492">Otherwise, if the DBPROP\_USEEXTENDEDDBTYPES flag is set in the client's DBPROPSET\_QUERYEXT property set, or if the column's property value is not a VT\_VECTOR type, then the property value MUST be returned in its normal type.</span></span> <span data-ttu-id="8457e-4493">Si ninguno de estos es el caso (es decir, el servidor tiene un \_ tipo de vector VT y el cliente no admite el \_ Vector VT), el servidor debe intentar convertirlo en un \_ tipo de matriz VT de la siguiente manera: los \_ elementos de matriz VT i8, VT \_ UI8, VT \_ FILETIME y VT \_ CLSID no se pueden convertir y se producirá un error en su lugar. Los \_ elementos de matriz VT LPSTR y VT \_ LPWStr deben convertirse en VT \_ BSTR; los elementos de la matriz de todos los demás tipos deben permanecer sin cambios.</span><span class="sxs-lookup"><span data-stu-id="8457e-4493">If none of these are the case (i.e., the server has a VT\_VECTOR type, and the client does not support VT\_VECTOR), then the server MUST attempt to convert it to a VT\_ARRAY type as follows: VT\_I8, VT\_UI8, VT\_FILETIME, and VT\_CLSID array elements cannot be converted and instead fail; VT\_LPSTR and VT\_LPWSTR array elements MUST be converted to VT\_BSTR; array elements of all other types MUST remain unchanged.</span></span> <span data-ttu-id="8457e-4494">Por último, si las columnas de fila contienen identificadores de capítulo o de marcador, el servidor debe actualizar las listas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="8457e-4494">Finally, if row columns contain chapter handles or bookmark handles, the server MUST update the corresponding lists.</span></span> <span data-ttu-id="8457e-4495">Si por algún motivo se produce un error en este paso, el servidor debe notificar que se ha detectado un error.</span><span class="sxs-lookup"><span data-stu-id="8457e-4495">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="8457e-4496">Almacenar el número real de filas capturadas en \_ cRowsReturned.</span><span class="sxs-lookup"><span data-stu-id="8457e-4496">Store the actual number of rows fetched in \_cRowsReturned.</span></span>
-   <span data-ttu-id="8457e-4497">Copie el campo Descripción de búsqueda y capítulo de CPMGetRowsIn en un mensaje de CPMGetRowsOut para enviarlo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4497">Copy the seek description and chapter field from CPMGetRowsIn to a CPMGetRowsOut message to be sent.</span></span>
-   <span data-ttu-id="8457e-4498">Almacene las filas capturadas en el campo Rows (vea la nota sobre el byte de estado siguiente y la sección 2.2.3.16 en la estructura del campo Rows).</span><span class="sxs-lookup"><span data-stu-id="8457e-4498">Store fetched rows in the Rows field (see note on status byte below and section 2.2.3.16 on the structure of the Rows field).</span></span>
-   <span data-ttu-id="8457e-4499">Responder al cliente con el mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4499">Respond to the client with the CPMGetRowsOut message.</span></span>

<span data-ttu-id="8457e-4500">Nota sobre el campo de bytes de estado:</span><span class="sxs-lookup"><span data-stu-id="8457e-4500">Note on status byte field:</span></span>

<span data-ttu-id="8457e-4501">Si StatusUsed se establece en 0x01 en el CTableColumn del mensaje CPMSetBindingIn para la columna, el servidor debe establecer el byte de estado (que se encuentra en StatusOffset desde el inicio de la fila) para esta columna en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="8457e-4501">If StatusUsed is set to 0x01 in the CTableColumn of the CPMSetBindingIn message for the column, then the server MUST set the status byte (which is located at StatusOffset from the start of the row) for this column to one of the following values:</span></span>



| <span data-ttu-id="8457e-4502">Value</span><span class="sxs-lookup"><span data-stu-id="8457e-4502">Value</span></span> | <span data-ttu-id="8457e-4503">Significado</span><span class="sxs-lookup"><span data-stu-id="8457e-4503">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="8457e-4504">0x00</span><span class="sxs-lookup"><span data-stu-id="8457e-4504">0x00</span></span>  | <span data-ttu-id="8457e-4505">StatusOK</span><span class="sxs-lookup"><span data-stu-id="8457e-4505">StatusOK</span></span>       |
| <span data-ttu-id="8457e-4506">0x01</span><span class="sxs-lookup"><span data-stu-id="8457e-4506">0x01</span></span>  | <span data-ttu-id="8457e-4507">StatusDeferred</span><span class="sxs-lookup"><span data-stu-id="8457e-4507">StatusDeferred</span></span> |
| <span data-ttu-id="8457e-4508">0x02</span><span class="sxs-lookup"><span data-stu-id="8457e-4508">0x02</span></span>  | <span data-ttu-id="8457e-4509">StatusNull</span><span class="sxs-lookup"><span data-stu-id="8457e-4509">StatusNull</span></span>     |



 

<span data-ttu-id="8457e-4510">Si el valor de la propiedad no está presente en esta fila, el servidor debe establecer el byte de estado en StatusNull.</span><span class="sxs-lookup"><span data-stu-id="8457e-4510">If the property value is absent for this row, the server MUST set the status byte to StatusNull.</span></span> <span data-ttu-id="8457e-4511">Si el valor es demasiado grande para transferirse en el mensaje CPMGetRowsOut, el servidor debe establecer el byte de estado en StatusDeferred.</span><span class="sxs-lookup"><span data-stu-id="8457e-4511">If the value is too big to be transferred in the CPMGetRowsOut message, the server MUST set the status byte to StatusDeferred.</span></span> <span data-ttu-id="8457e-4512">En caso contrario, el servidor debe establecer el byte de estado en StatusOK.</span><span class="sxs-lookup"><span data-stu-id="8457e-4512">Otherwise the server MUST set the status byte to StatusOK.</span></span>

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a><span data-ttu-id="8457e-4513">3.1.5.2.8 recibir una solicitud de CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4513">3.1.5.2.8 Receiving a CPMFetchValueIn Request</span></span>

<span data-ttu-id="8457e-4514">Cuando el servidor recibe una solicitud de mensaje de CPMFetchValueIn desde un cliente, el servidor debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4514">When the server receives a CPMFetchValueIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4515">Compruebe si el cliente tiene consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="8457e-4515">Check if the client has query associated with it.</span></span> <span data-ttu-id="8457e-4516">Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4516">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8457e-4517">Preparar un mensaje CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4517">Prepare a CPMFetchValueOut message.</span></span> <span data-ttu-id="8457e-4518">Si se produce un error en este paso por cualquier motivo, el servidor debe informar de un error.</span><span class="sxs-lookup"><span data-stu-id="8457e-4518">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="8457e-4519">Busque el documento indicado por el \_ campo WID y compruebe si el identificador de propiedad de este documento (más adelante conocido como ' valor de propiedad ') indicado por la estructura PropSpec está disponible para este cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4519">Find the document indicated by the\_wid field and check if the property ID for this document (later referred to as 'property value') indicated by the PropSpec structure is available for this client.</span></span> <span data-ttu-id="8457e-4520">Si este valor no está disponible, el servidor debe establecer \_ fValueExists en 0x00000000 y, de lo contrario, establecer \_ fValueExists en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8457e-4520">If this value is not available the server MUST set \_fValueExists to 0x00000000, and otherwise set \_fValueExists to 0x00000001.</span></span> <span data-ttu-id="8457e-4521">Si se produce un error en este paso por cualquier motivo, el servidor debe informar de un error.</span><span class="sxs-lookup"><span data-stu-id="8457e-4521">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="8457e-4522">Si \_ fValueExists es igual a 0x00000001, el servidor debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4522">If \_fValueExists is equal to 0x00000001 the server MUST do the following:</span></span>
-   -   <span data-ttu-id="8457e-4523">Serialice el valor de propiedad en una estructura SERIALIZEDPROPERTYVALUE y copie, empezando por el \_ desplazamiento cbSoFar, como máximo \_ cbChunk bytes (pero no más allá del final de la propiedad serializada) al campo vValue.</span><span class="sxs-lookup"><span data-stu-id="8457e-4523">Serialize the property value to a SERIALIZEDPROPERTYVALUE structure and copy, starting from the \_cbSoFar offset, at most \_cbChunk bytes (but not past the end of the serialized property) to vValue field.</span></span> <span data-ttu-id="8457e-4524">Si se produce un error en este paso por cualquier motivo, el servidor debe informar de un error.</span><span class="sxs-lookup"><span data-stu-id="8457e-4524">If this step fails for any reason server MUST report an error.</span></span>
    -   <span data-ttu-id="8457e-4525">Establezca \_ cbValue en el número de bytes copiados en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4525">Set \_cbValue to the number of bytes copied in previous step.</span></span>
    -   <span data-ttu-id="8457e-4526">Establezca vType en el tipo de propiedad del valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-4526">Set vType to the property type of the property value.</span></span>
    -   <span data-ttu-id="8457e-4527">Si la longitud de la propiedad serializada es mayor que \_ cbSoFar se agrega a \_ cbValue, establezca \_ fMoreExists en 0x00000001; de lo contrario, establézcalo en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4527">If the length of serialized property is greater than \_cbSoFar added to \_cbValue, then set \_fMoreExists to 0x00000001, otherwise set it to 0x00000000.</span></span>

-   <span data-ttu-id="8457e-4528">Responder al cliente con el mensaje CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="8457e-4528">Respond to the client with the CPMFetchValueOut message</span></span>

### <a name="31529-receiving-a-cpmgetnotify-request"></a><span data-ttu-id="8457e-4529">3.1.5.2.9 recibir una solicitud de CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="8457e-4529">3.1.5.2.9 Receiving a CPMGetNotify Request</span></span>

<span data-ttu-id="8457e-4530">Cuando el servidor recibe un mensaje CPMGetNotify de un cliente, el servidor debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4530">When the server receives a CPMGetNotify message from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4531">Compruebe si el cliente tiene consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="8457e-4531">Check if the client has query associated with it.</span></span> <span data-ttu-id="8457e-4532">Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4532">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8457e-4533">Si no se ha producido ningún cambio en el conjunto de resultados de la consulta desde el último mensaje CPMSendNotifyOut para este cliente, o si la consulta no está supervisada actualmente para los cambios del conjunto de resultados, el servidor debe responder con el mensaje CPMGetNotify y empezar a supervisar la consulta en busca de cambios en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="8457e-4533">If there were no changes in the query result set since the last CPMSendNotifyOut message for this client, or if the query is not currently monitored for changes in the results set, then the server MUST respond with CPMGetNotify message and start to monitor the query for changes in results set.</span></span> <span data-ttu-id="8457e-4534">Si posteriormente hay un cambio en el conjunto de resultados de la consulta, el servidor debe enviar exactamente un mensaje CPMSendNotifyOut al cliente y debe especificar el cambio en el \_ campo watchNotify.</span><span class="sxs-lookup"><span data-stu-id="8457e-4534">If at a later time there is a change in the query results set then the server MUST send exactly one CPMSendNotifyOut message to the client and MUST specify the change in the \_watchNotify field.</span></span>
-   <span data-ttu-id="8457e-4535">Si hubo cambios en el conjunto de resultados de la consulta desde el último mensaje de CPMSendNotifyOut, el servidor debe responder con CPMSendNotifyOut y debe especificar el cambio en el \_ campo watchNotify.</span><span class="sxs-lookup"><span data-stu-id="8457e-4535">If there were changes to the query result set since the last CPMSendNotifyOut message, the server MUST reply with CPMSendNotifyOut and MUST specify the change in the \_watchNotify field.</span></span> <span data-ttu-id="8457e-4536">Tenga en cuenta que, en el caso de muchos cambios en los resultados de la consulta, DBWATCHNOTIFY \_ ROWSCHANGED tiene prioridad (es decir, si la consulta se ha realizado, se vuelve a ejecutar y, a continuación, se ha cambiado el número de filas y la consulta se ha realizado de nuevo, el evento indicado sería DBWATCHNOTIFY \_ ROWSCHANGED).</span><span class="sxs-lookup"><span data-stu-id="8457e-4536">Note, that in the case of many changes to query results, DBWATCHNOTIFY\_ROWSCHANGED takes priority (i.e., if the query was done, re-executed and then the number of rows changed and the query was done again then the event reported would be DBWATCHNOTIFY\_ROWSCHANGED).</span></span>

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a><span data-ttu-id="8457e-4537">3.1.5.2.10 recibir una solicitud de CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4537">3.1.5.2.10 Receiving a CPMGetApproximatePositionIn Request</span></span>

<span data-ttu-id="8457e-4538">Cuando el servidor recibe una solicitud de mensaje de CPMGetApproximatePositionIn desde el cliente, el servidor debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4538">When the server receives a CPMGetApproximatePositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4539">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="8457e-4539">Check if the client has a query associated with it.</span></span> <span data-ttu-id="8457e-4540">Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4540">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8457e-4541">Compruebe si el identificador de cursor, el identificador de capítulo y el identificador de marcador pasados están en las listas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="8457e-4541">Check if the cursor handle, chapter handle and bookmark handle passed are in corresponding lists.</span></span> <span data-ttu-id="8457e-4542">Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8457e-4542">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8457e-4543">Busque una fila que esté asociada al identificador de marcador en los resultados de la consulta y aproxime la posición de la fila en el conjunto de filas, a la que hace referencia el identificador del capítulo, y determine el numerador y el denominador para la posición.</span><span class="sxs-lookup"><span data-stu-id="8457e-4543">Find a row which is associated with the bookmark handle in the query results and approximate the position of the row in the rowset, referred to by the chapter handle, and determine the numerator and denominator for the position.</span></span> <span data-ttu-id="8457e-4544">Tenga en cuenta que cuando el identificador del capítulo es DB \_ null \_ HCHAPTER, el capítulo correspondiente es el conjunto de filas principal de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-4544">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="8457e-4545">Si se produce un error en este paso por cualquier motivo, el servidor debe informar de un error.</span><span class="sxs-lookup"><span data-stu-id="8457e-4545">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="8457e-4546">Responder al cliente con un mensaje CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4546">Respond to the client with a CPMFetchValueOut message.</span></span>

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a><span data-ttu-id="8457e-4547">3.1.5.2.11 recibir una solicitud de CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4547">3.1.5.2.11 Receiving a CPMCompareBmkIn Request</span></span>

<span data-ttu-id="8457e-4548">Cuando el servidor recibe una solicitud de mensaje de CPMCompareBmkIn desde el cliente, el servidor debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4548">When the server receives a CPMCompareBmkIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4549">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="8457e-4549">Check if the client has a query associated with it.</span></span> <span data-ttu-id="8457e-4550">Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4550">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8457e-4551">Compruebe si el identificador de cursor, el identificador de capítulo y los identificadores de marcador pasados están en las listas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="8457e-4551">Check if the cursor handle, chapter handle and bookmark handles passed are in corresponding lists.</span></span> <span data-ttu-id="8457e-4552">Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8457e-4552">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8457e-4553">Preparar un mensaje CPMCompareBmkOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4553">Prepare a CPMCompareBmkOut message.</span></span>
-   <span data-ttu-id="8457e-4554">Si los identificadores de marcador son iguales, \_ DWCOMPARISON debe estar establecido en DBCOMPARE \_ EQ.</span><span class="sxs-lookup"><span data-stu-id="8457e-4554">If bookmark handles are equal, then \_dwComparison MUST be is set to DBCOMPARE\_EQ.</span></span>
-   <span data-ttu-id="8457e-4555">De lo contrario, si uno de los marcadores se DBBMK \_ primero o DBBMK \_ por último, entonces \_ dwComparison debe establecerse en DBCOMPARE \_ ne.</span><span class="sxs-lookup"><span data-stu-id="8457e-4555">Otherwise, if one of bookmarks handles is DBBMK\_FIRST or DBBMK\_LAST then \_dwComparison MUST be set to DBCOMPARE\_NE.</span></span>
-   <span data-ttu-id="8457e-4556">En caso contrario, el servidor debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4556">Otherwise the server MUST do the following:</span></span>
-   -   <span data-ttu-id="8457e-4557">Buscar filas a las que hace referencia cada identificador de marcador en los resultados de la consulta</span><span class="sxs-lookup"><span data-stu-id="8457e-4557">Find rows which are referred to by each bookmark handle in the query results</span></span>
    -   <span data-ttu-id="8457e-4558">Si alguna de las filas no está en el capítulo indicado por el identificador de capítulo en CPMCompareBmkIn, \_ DWCOMPARISON debe establecerse en DBCOMPARE \_ NOTCOMPARABLE.</span><span class="sxs-lookup"><span data-stu-id="8457e-4558">If any one of the rows is not in the chapter indicated by the chapter handle in CPMCompareBmkIn, then \_dwComparison MUST be set to DBCOMPARE\_NOTCOMPARABLE.</span></span>
    -   <span data-ttu-id="8457e-4559">De lo contrario, cuando ambas filas están en el mismo capítulo, el servidor debe aproximar una posición de las filas del conjunto de filas al que se hace referencia en el identificador de este capítulo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4559">Otherwise, when both rows are in the same chapter, then the server MUST approximate a position of those rows in the rowset referred to by this chapter's handle.</span></span> <span data-ttu-id="8457e-4560">A continuación, debe comparar los valores de posición y establecer \_ dwComparison en DBCOMPARE \_ lt si la posición de la primera fila es menor que la posición de la segunda fila; de lo contrario, \_ dwComparison debe establecerse en DBCOMPARE \_ gt.</span><span class="sxs-lookup"><span data-stu-id="8457e-4560">It MUST then compare position values and set\_dwComparison to DBCOMPARE\_LT if position of first row is smaller than position of the second row; otherwise \_dwComparison MUST be set to DBCOMPARE\_GT.</span></span>

-   <span data-ttu-id="8457e-4561">Responder al cliente con el mensaje CPMCompareBmkOut rellenado.</span><span class="sxs-lookup"><span data-stu-id="8457e-4561">Respond to the client with filled CPMCompareBmkOut message.</span></span>

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a><span data-ttu-id="8457e-4562">3.1.5.2.12 recibir una solicitud de CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4562">3.1.5.2.12 Receiving a CPMRestartPositionIn Request</span></span>

<span data-ttu-id="8457e-4563">Cuando el servidor recibe la solicitud de mensaje CPMRestartPositionIn desde el cliente, el servidor debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4563">When the server receives the CPMRestartPositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4564">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="8457e-4564">Check if the client has a query associated with it.</span></span> <span data-ttu-id="8457e-4565">Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4565">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8457e-4566">Compruebe si el identificador de cursor y el identificador de capítulo pasados están en las listas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="8457e-4566">Check if the cursor handle and chapter handle passed are in corresponding lists.</span></span> <span data-ttu-id="8457e-4567">Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8457e-4567">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8457e-4568">Mueva el cursor al principio del capítulo, identificado por el identificador del capítulo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4568">Move the cursor to the beginning of the chapter, identified by the chapter handle.</span></span> <span data-ttu-id="8457e-4569">Tenga en cuenta que cuando el identificador del capítulo es DB \_ null \_ HCHAPTER, el capítulo correspondiente es el conjunto de filas principal de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-4569">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="8457e-4570">Si se produce un error en este paso por cualquier motivo, el servidor debe informar de un error.</span><span class="sxs-lookup"><span data-stu-id="8457e-4570">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="8457e-4571">Responder al cliente con un mensaje CPMRestartPositionIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-4571">Respond to the client with a CPMRestartPositionIn message.</span></span>

### <a name="315213-receiving-a-cpmfreecursorin-request"></a><span data-ttu-id="8457e-4572">3.1.5.2.13 recibir una solicitud de CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4572">3.1.5.2.13 Receiving a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="8457e-4573">Cuando el servidor recibe una solicitud de mensaje de CPMFreeCursorIn desde el cliente, el servidor debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4573">When the server receives a CPMFreeCursorIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4574">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="8457e-4574">Check if the client has a query associated with it.</span></span> <span data-ttu-id="8457e-4575">Si no es así, el servidor debe notificar un error de \_ parámetro no válido de estado \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="8457e-4575">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="8457e-4576">Compruebe si el identificador de cursor que se ha pasado está en la lista de identificadores de cursor del cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4576">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="8457e-4577">Si no es así, el servidor debe notificar un error de E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="8457e-4577">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="8457e-4578">Libere el cursor y los recursos asociados (consulte la sección 3.1.1 para obtener una lista completa) para este identificador de cursor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4578">Release the cursor and associated resources (see section 3.1.1 for complete list) for this cursor handle.</span></span>
-   <span data-ttu-id="8457e-4579">Quite el cursor de la lista de cursores para ese cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4579">Remove the cursor from the list of cursors for that client.</span></span>
-   <span data-ttu-id="8457e-4580">Responda con un mensaje de CPMFreeCursorOut, estableciendo el \_ campo cCursorsRemaining con el número de cursores restantes.</span><span class="sxs-lookup"><span data-stu-id="8457e-4580">Respond with a CPMFreeCursorOut message, setting the \_cCursorsRemaining field with the number of cursors remaining.</span></span> <span data-ttu-id="8457e-4581">en la lista de este cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4581">in this client's list.</span></span>
-   <span data-ttu-id="8457e-4582">Si no hay más cursores para este cliente, el servidor debe liberar la consulta y los recursos asociados (consulte la sección 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="8457e-4582">If there are no more cursors for this client, the server MUST release the query and associated resources (see section 3.1.1).</span></span>

### <a name="315214-receiving-a-cpmdisconnect-request"></a><span data-ttu-id="8457e-4583">3.1.5.2.14 recibir una solicitud de CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="8457e-4583">3.1.5.2.14 Receiving a CPMDisconnect Request</span></span>

<span data-ttu-id="8457e-4584">Cuando el servidor recibe una solicitud de mensaje de CPMDisconnect desde el cliente, el servidor debe quitar el cliente de la lista de clientes conectados y liberar todos los recursos asociados con el cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4584">When the server receives a CPMDisconnect message request from the client, the server MUST remove the client from the list of connected clients and release all resources associated with the client.</span></span>

### <a name="316-timer-events"></a><span data-ttu-id="8457e-4585">Eventos de temporizador de 3.1.6</span><span class="sxs-lookup"><span data-stu-id="8457e-4585">3.1.6 Timer Events</span></span>

<span data-ttu-id="8457e-4586">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8457e-4586">None.</span></span>

### <a name="317-other-local-events"></a><span data-ttu-id="8457e-4587">3.1.7 otros eventos locales</span><span class="sxs-lookup"><span data-stu-id="8457e-4587">3.1.7 Other Local Events</span></span>

<span data-ttu-id="8457e-4588">Cuando se detiene el servidor, primero debe realizar la transición al estado "cerrando".</span><span class="sxs-lookup"><span data-stu-id="8457e-4588">When the server is stopped, it MUST first transition to the "shutting down" state.</span></span> <span data-ttu-id="8457e-4589">A continuación, debe dejar de escuchar la canalización, realizar cualquier otra tarea de apagado específica de la implementación y, a continuación, pasar al estado "detenido".</span><span class="sxs-lookup"><span data-stu-id="8457e-4589">It MUST then stop listening to the pipe, perform any other implementation-specific shutdown tasks, and then transition into the "stopped" state.</span></span>

### <a name="32-client-details"></a><span data-ttu-id="8457e-4590">Detalles del cliente 3,2</span><span class="sxs-lookup"><span data-stu-id="8457e-4590">3.2 Client Details</span></span>

### <a name="321-abstract-data-model"></a><span data-ttu-id="8457e-4591">3.2.1 modelo de datos abstracto</span><span class="sxs-lookup"><span data-stu-id="8457e-4591">3.2.1 Abstract Data Model</span></span>

<span data-ttu-id="8457e-4592">En la sección siguiente se especifican los datos y el estado que mantiene el cliente del protocolo del servicio de indización de contenido.</span><span class="sxs-lookup"><span data-stu-id="8457e-4592">The following section specifies data and state maintained by the Content Indexing Service Protocol client.</span></span> <span data-ttu-id="8457e-4593">Los datos proporcionados son para facilitar la explicación de cómo se comporta el protocolo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4593">The provided data is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="8457e-4594">En esta sección no se exige que las implementaciones se adhieren a este modelo, siempre y cuando su comportamiento externo sea coherente con el descrito en este documento.</span><span class="sxs-lookup"><span data-stu-id="8457e-4594">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="8457e-4595">Un cliente tiene el siguiente estado abstracto:</span><span class="sxs-lookup"><span data-stu-id="8457e-4595">A client has the following abstract state:</span></span>

-   <span data-ttu-id="8457e-4596">**Último mensaje enviado**: una copia del último mensaje enviado al servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4596">**Last Message Sent**: A copy of the last message sent to the server.</span></span>
-   <span data-ttu-id="8457e-4597">**Valor de propiedad actual**: valor parcial de una propiedad "diferida", que se encuentra en proceso de recuperación.</span><span class="sxs-lookup"><span data-stu-id="8457e-4597">**Current Property Value**: A partial value of a "deferred" property, which is in the process of being retrieved.</span></span>
-   <span data-ttu-id="8457e-4598">**Bytes recibidos actuales**: el número de bytes recibidos para el valor actual de la propiedad hasta ahora.</span><span class="sxs-lookup"><span data-stu-id="8457e-4598">**Current Bytes Received**: The number of bytes received for Current Property Value so far.</span></span>
-   <span data-ttu-id="8457e-4599">**Estado de conexión de canalización con nombre**: conexión al servidor</span><span class="sxs-lookup"><span data-stu-id="8457e-4599">**Named pipe connection state**: A connection to the server</span></span>

### <a name="322-timers"></a><span data-ttu-id="8457e-4600">3.2.2 temporizadores</span><span class="sxs-lookup"><span data-stu-id="8457e-4600">3.2.2 Timers</span></span>

<span data-ttu-id="8457e-4601">No se requieren temporizadores de protocolos.</span><span class="sxs-lookup"><span data-stu-id="8457e-4601">No protocol timers are required.</span></span>

### <a name="323-initialization"></a><span data-ttu-id="8457e-4602">inicialización de 3.2.3</span><span class="sxs-lookup"><span data-stu-id="8457e-4602">3.2.3 Initialization</span></span>

<span data-ttu-id="8457e-4603">No se realiza ninguna acción hasta que se recibe una solicitud de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4603">No actions are taken until a higher layer request is received.</span></span>

### <a name="324-higher-layer-triggered-events"></a><span data-ttu-id="8457e-4604">3.2.4 Higher-Layer eventos desencadenados</span><span class="sxs-lookup"><span data-stu-id="8457e-4604">3.2.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="8457e-4605">Cuando se recibe una solicitud de una capa superior, el cliente debe crear una conexión de canalización con nombre en el servidor, con los detalles especificados en la sección 2,1.</span><span class="sxs-lookup"><span data-stu-id="8457e-4605">When a request is received from a higher layer, the client MUST create a named pipe connection to the server, using the details specified in Section 2.1.</span></span> <span data-ttu-id="8457e-4606">Si no puede hacerlo, debe haber un error en la solicitud de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4606">If it is unable to do so, the higher layer request MUST be failed.</span></span> <span data-ttu-id="8457e-4607">Es decir, en caso de que se produzca un error de conexión, es responsabilidad del nivel superior volver a intentarlo si lo desea.</span><span class="sxs-lookup"><span data-stu-id="8457e-4607">That is, in case of a failure to connect, it is the responsibility of the higher level to retry if desired.</span></span>

<span data-ttu-id="8457e-4608">Un encabezado debe anteponerse al conjunto de campos especificado en la sección 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="8457e-4608">A header MUST be pre-pended with fields set as specified in section 2.2.2.</span></span>

<span data-ttu-id="8457e-4609">En el caso de los mensajes que se especifican como que requieren una suma de comprobación distinto de cero, el \_ valor de ulChecksum se debe calcular de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4609">For messages that are specified as requiring a nonzero checksum, the \_ulChecksum value MUST be calculated as follows:</span></span>

1.  <span data-ttu-id="8457e-4610">El contenido del mensaje después del \_ campo ulReserved2 en el encabezado del mensaje debe interpretarse como una secuencia de enteros de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8457e-4610">The contents of the message after the \_ulReserved2 field in the message header MUST be interpreted as a sequence of 32 bit integers.</span></span> <span data-ttu-id="8457e-4611">El cliente debe calcular la suma de los valores numéricos proporcionados por estos enteros.</span><span class="sxs-lookup"><span data-stu-id="8457e-4611">The client MUST calculate the sum of the numeric values given by these integers.</span></span>
2.  <span data-ttu-id="8457e-4612">Calcula la operación XOR bit a bit de este valor con 0x59533959.</span><span class="sxs-lookup"><span data-stu-id="8457e-4612">Calculate the bitwise XOR of this value with 0x59533959.</span></span>
3.  <span data-ttu-id="8457e-4613">Resta el valor proporcionado por \_ MSG del valor que es el resultado de la operación XOR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="8457e-4613">Subtract the value given by \_msg from the value that results from the bitwise XOR.</span></span>

### <a name="3241-remote-indexing-service-catalog-management"></a><span data-ttu-id="8457e-4614">Administración de catálogos del servicio de indexación remota de 3.2.4.1</span><span class="sxs-lookup"><span data-stu-id="8457e-4614">3.2.4.1 Remote Indexing Service Catalog Management</span></span>

<span data-ttu-id="8457e-4615">Cada mensaje se desencadena mediante una solicitud de la capa superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4615">Each message is triggered by a request from the higher layer.</span></span> <span data-ttu-id="8457e-4616">No hay ninguna secuencia de mensajes impuesta por el cliente para las solicitudes de mensajes CISP para administrar de forma remota los catálogos, pero (con la excepción de un mensaje CPMSetCatStateIn) el servidor solo responderá correctamente si el cliente se conectó anteriormente mediante un mensaje de CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-4616">There is no message sequence enforced by the client for CISP message requests for remotely managing catalogs, but (with the exception of a CPMSetCatStateIn message) the server will only reply with success if the client previously connected by means of a CPMConnectIn message.</span></span>

### <a name="32411-sending-a-cpmcistateinout-request"></a><span data-ttu-id="8457e-4617">3.2.4.1.1 enviar una solicitud de CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="8457e-4617">3.2.4.1.1 Sending a CPMCiStateInOut Request</span></span>

<span data-ttu-id="8457e-4618">Normalmente, el nivel superior solicita al cliente de protocolo que envíe un mensaje de CPMCiStateInOut cuando requiere información sobre los servicios de Index Server en el servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4618">Typically, the higher layer asks the protocol client to send a CPMCiStateInOut message when it requires information about indexing services on the server.</span></span>

<span data-ttu-id="8457e-4619">Cuando se solicita el envío de este mensaje, el cliente debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4619">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4620">Envíe un mensaje CPMCiStateInOut como se especifica en la sección 2.2.3.1 al servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4620">Send a CPMCiStateInOut message as specified in section 2.2.3.1 to the server.</span></span>
-   <span data-ttu-id="8457e-4621">Espere para recibir el mensaje CPMCiStateInOut del servidor, descartando de forma silenciosa el resto de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8457e-4621">Wait to receive CPMCiStateInOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="8457e-4622">Informe del valor del \_ campo de estado de la respuesta y, si fue correcto, la estructura informativa de vuelta a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4622">Report the value of the \_status field of the response and, if it was successful, the informational structure back to the higher layer.</span></span>

### <a name="32412-sending-a-cpmsetcatstatein-request"></a><span data-ttu-id="8457e-4623">3.2.4.1.2 enviar una solicitud de CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4623">3.2.4.1.2 Sending a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="8457e-4624">Normalmente, el nivel superior solicita al cliente de protocolo que envíe un mensaje de CPMSetCatStateIn cuando requiere información sobre un catálogo o todo el catálogo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4624">Typically, the higher layer asks the protocol client to send a CPMSetCatStateIn message when it requires information about a catalog or all catalog.</span></span> <span data-ttu-id="8457e-4625">En este mensaje, la capa más alta debe proporcionar al cliente de protocolo un valor para \_ dwNewState y, si es necesario, el nombre del catálogo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4625">For this message the higher layer needs to provide the protocol client with a value for \_dwNewState and, if required, the name of the catalog.</span></span>

<span data-ttu-id="8457e-4626">Cuando se solicita el envío de este mensaje, el cliente debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4626">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4627">Envíe un mensaje CPMSetCatStateIn como se especifica en 2.2.3.2 al servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4627">Send a CPMSetCatStateIn message as specified in 2.2.3.2 to the server.</span></span>
-   <span data-ttu-id="8457e-4628">Espere a recibir un mensaje CPMSetCatStateOut del servidor, descartando de forma silenciosa el resto de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="8457e-4628">Wait to receive a CPMSetCatStateOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="8457e-4629">Informe del valor del \_ campo de estado de la respuesta y, si fue correcto, dwOldState de \_ nuevo a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4629">Report the value of the \_status field of the response and, if it was successful, the \_dwOldState back to the higher layer.</span></span>

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="8457e-4630">3.2.4.1.3 enviar una solicitud de CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4630">3.2.4.1.3 Sending a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="8457e-4631">Normalmente, el nivel superior solicita que se envíe este mensaje cuando es necesario actualizar documentos en una ruta de acceso existente o agregar una nueva ruta de acceso al índice.</span><span class="sxs-lookup"><span data-stu-id="8457e-4631">The higher layer typically asks to send this message when it needs to either update documents in existing path or add a new file path to the index.</span></span> <span data-ttu-id="8457e-4632">Por lo tanto, la capa superior es proporcionar la ruta de acceso y el tipo de un examen, que se especifica como en la sección 2.2.3.4, donde una actualización incremental o completa está pensada para las rutas de acceso existentes, y la nueva inicialización está destinada a nuevas rutas.</span><span class="sxs-lookup"><span data-stu-id="8457e-4632">Thus the higher layer is to provide the path and type of a scan, which is specified as in section 2.2.3.4 where an incremental or full update is meant for existing paths, and new initialization is meant for new paths.</span></span>

<span data-ttu-id="8457e-4633">Para atender la solicitud de nivel superior, el cliente debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4633">In order to serve the higher layer request, the client MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4634">Envíe un mensaje CPMUpdateDocumentsIn como se especifica en la sección 2.2.3.4 al servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4634">Send a CPMUpdateDocumentsIn message as specified in section 2.2.3.4 to the server.</span></span>
-   <span data-ttu-id="8457e-4635">Espere para recibir el mensaje de CPMUpdateDocumentsIn de vuelta del servidor, descartando de forma silenciosa el resto de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8457e-4635">Wait to receive CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="8457e-4636">Vuelva a informar del valor del \_ campo Estado de la respuesta a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4636">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="32414-sending-a-cpmforcemergein-request"></a><span data-ttu-id="8457e-4637">3.2.4.1.4 enviar una solicitud de CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4637">3.2.4.1.4 Sending a CPMForceMergeIn Request</span></span>

<span data-ttu-id="8457e-4638">Normalmente, el nivel superior solicita que se envíe este mensaje cuando es necesario mejorar el rendimiento de las consultas o forma parte del mantenimiento de los servicios de Index Server programados.</span><span class="sxs-lookup"><span data-stu-id="8457e-4638">Typically, the higher layer requests to send this message when there is a need to improve query performance, or it's a part of scheduled indexing service maintenance.</span></span>

<span data-ttu-id="8457e-4639">Para atender a la capa más alta, el cliente debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4639">In order to serve the higher layer the client MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4640">Envíe el mensaje CPMForceMergeIn como se especifica en la sección 2.2.3.5 al servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4640">Send CPMForceMergeIn message as specified by section 2.2.3.5 to the server.</span></span>
-   <span data-ttu-id="8457e-4641">Espere para recibir un mensaje de CPMUpdateDocumentsIn de vuelta del servidor, descartando de forma silenciosa el resto de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8457e-4641">Wait to receive a CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="8457e-4642">Vuelva a informar del valor del \_ campo Estado de la respuesta a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4642">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="3242-remote-indexing-service-catalog-query-messages"></a><span data-ttu-id="8457e-4643">3.2.4.2 mensajes de consulta del catálogo del servicio de indexación remota</span><span class="sxs-lookup"><span data-stu-id="8457e-4643">3.2.4.2 Remote Indexing Service Catalog Query Messages</span></span>

<span data-ttu-id="8457e-4644">Con la excepción de CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, hay una relación uno a uno entre los mensajes de CISP y las solicitudes de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4644">With the exception of CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, there is a one-to-one relationship between CISP messages and higher layer requests.</span></span> <span data-ttu-id="8457e-4645">En el caso de las dos excepciones mencionadas anteriormente, puede haber varios mensajes generados por el cliente para satisfacer los requisitos de tamaño o para recuperar una propiedad completa.</span><span class="sxs-lookup"><span data-stu-id="8457e-4645">For the two exceptions mentioned above, there can be multiple messages generated by the client to either satisfy size requirements, or to retrieve a complete property.</span></span> <span data-ttu-id="8457e-4646">El nivel superior normalmente realiza un seguimiento de toda la información específica de la consulta (por ejemplo, los identificadores de cursor abiertos, los valores válidos para los identificadores de marcador y de capítulo, los valores de WID para los valores de propiedad aplazados, etc.) y también realiza el seguimiento de si el cliente está en un estado conectado, pero el cliente no lo exige.</span><span class="sxs-lookup"><span data-stu-id="8457e-4646">The higher layer typically keeps track of all query-specific information (such as cursor handles opened, legal values for bookmark and chapter handles, wid values for deferred property values, etc.) and also tracks if the client is in a connected state, but this is not enforced in any way by the client.</span></span>

<span data-ttu-id="8457e-4647">Con fines ilustrativos, la parte del cliente del diagrama de la sección 3 muestra esta secuencia para una consulta de servicio de indexación simple.</span><span class="sxs-lookup"><span data-stu-id="8457e-4647">For illustrative purposes the client portion of the diagram in Section 3 illustrates this sequence for a simple Indexing Service query.</span></span>

### <a name="32421-sending-a-cpmconnectin-request"></a><span data-ttu-id="8457e-4648">3.2.4.2.1 enviar una solicitud de CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4648">3.2.4.2.1 Sending a CPMConnectIn Request</span></span>

<span data-ttu-id="8457e-4649">Este mensaje suele ser la primera solicitud de la capa superior (como si el cliente no está conectado, el servidor producirá un error en la mayoría de los mensajes con la excepción de CPMSetCatStateIn).</span><span class="sxs-lookup"><span data-stu-id="8457e-4649">This message is typically the very first request from the higher layer (as if the client is not connected, the server will fail most of the messages with exception of CPMSetCatStateIn).</span></span> <span data-ttu-id="8457e-4650">El nivel superior proporciona al cliente de protocolo la información necesaria para conectarse.</span><span class="sxs-lookup"><span data-stu-id="8457e-4650">The higher level provides the protocol client with information necessary to connect.</span></span>

<span data-ttu-id="8457e-4651">Para atender el nivel superior, el cliente debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4651">In order to serve the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4652">Rellene el mensaje con la información que el cliente de nivel superior proporcionó (consulte la sección 2.2.3.6) en \_ iClientVersion, MachineName, username, PropertySet1, PropertySet2 y aPropertySet.</span><span class="sxs-lookup"><span data-stu-id="8457e-4652">Fill in the message, using information which the higher layer client provided (see section 2.2.3.6) in \_iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 and aPropertySet.</span></span>
-   <span data-ttu-id="8457e-4653">Establezca \_ fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet y cExtPropSet como se especifica en 2.2.3.6.</span><span class="sxs-lookup"><span data-stu-id="8457e-4653">Set \_fClientIsRemote, \_cbBlob, \_cbBlob2, cPropSet and cExtPropSet as specified in 2.2.3.6.</span></span>
-   <span data-ttu-id="8457e-4654">Establezca la suma de comprobación en el \_ campo ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="8457e-4654">Set the checksum in the \_ulChecksum field.</span></span>
-   <span data-ttu-id="8457e-4655">Envíe el mensaje CPMConnectIn al servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4655">Send the CPMConnectIn message to the server.</span></span>
-   <span data-ttu-id="8457e-4656">Espere para recibir un mensaje de CPMConnectOut de vuelta del servidor, descartando de forma silenciosa el resto de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8457e-4656">Wait to receive a CPMConnectOut message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="8457e-4657">Informe del valor del \_ campo de estado de la respuesta y, si fue correcto, serverVersion de \_ nuevo a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4657">Report the value of the \_status field of the response and, if it was successful, the \_serverVersion back to the higher layer.</span></span>

<span data-ttu-id="8457e-4658">Para fines informativos, se espera que las capas más altas realicen normalmente las siguientes acciones tras una conexión correcta, pero que no las aplique el cliente de CISP:</span><span class="sxs-lookup"><span data-stu-id="8457e-4658">For informative purposes, it is expected that higher layers will typically do the following actions upon successful connection, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="8457e-4659">Usar mensajes de administración de catálogos de servicio de indexación remota para tareas administrativas</span><span class="sxs-lookup"><span data-stu-id="8457e-4659">Use remote indexing service catalog management messages for administrative tasks</span></span>
-   <span data-ttu-id="8457e-4660">Use una solicitud CPMCreateQueryIn para crear una consulta de búsqueda con el fin de recuperar los resultados del catálogo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4660">Use a CPMCreateQueryIn request to create a search query with a purpose of retrieving results from the catalog.</span></span>

### <a name="32422-sending-a-cpmcreatequeryin-request"></a><span data-ttu-id="8457e-4661">3.2.4.2.2 enviar una solicitud de CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4661">3.2.4.2.2 Sending a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="8457e-4662">La capa superior normalmente proporcionará información para la creación de la consulta una vez que el cliente del protocolo esté conectado.</span><span class="sxs-lookup"><span data-stu-id="8457e-4662">The higher layer will typically provide information for the query creation once the protocol client is connected.</span></span> <span data-ttu-id="8457e-4663">La capa superior proporciona al cliente un conjunto de restricciones, conjunto de columnas, reglas de ordenación y conjunto de categorización (se pueden omitir cada una de ellas), propiedades de conjunto de filas y estructura del asignador de IDENTIFICADOres de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8457e-4663">The higher layer provides the client with a restrictions set, columns set, sort order rules and categorization set (each of them can be omitted), rowset properties and property ID mapper structure.</span></span>

<span data-ttu-id="8457e-4664">Cuando se recibe esta solicitud de una capa superior, el cliente debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4664">When this request is received from a higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4665">Prepare un CPMCreateQueryOut como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="8457e-4665">Prepare a CPMCreateQueryOut as follows.</span></span>
-   -   <span data-ttu-id="8457e-4666">Si hay un conjunto de columnas, establezca CColumnsSetPreset en 0x01 y rellene el campo ColumnsSet.</span><span class="sxs-lookup"><span data-stu-id="8457e-4666">If a columns set is present then set CColumnsSetPreset to 0x01 and fill the ColumnsSet field.</span></span>
    -   <span data-ttu-id="8457e-4667">Si hay restricciones, establezca CRestrictionPresent en 0x01 y rellene el campo de restricción.</span><span class="sxs-lookup"><span data-stu-id="8457e-4667">If restrictions are present, set CRestrictionPresent to 0x01 and fill the Restriction field.</span></span>
    -   <span data-ttu-id="8457e-4668">Si hay un conjunto de ordenación, rellene el campo SortSet.</span><span class="sxs-lookup"><span data-stu-id="8457e-4668">If a sort set is present, fill the SortSet field.</span></span>
    -   <span data-ttu-id="8457e-4669">Si hay un conjunto de categorización, establezca CSortSetPresent en 0x01 y rellene el campo CategorizationSet.</span><span class="sxs-lookup"><span data-stu-id="8457e-4669">If a categorization set is present, set CSortSetPresent to 0x01 and fill the CategorizationSet field.</span></span>
    -   <span data-ttu-id="8457e-4670">Establecer el resto de campos tal como se especifica en 2.2.3.8</span><span class="sxs-lookup"><span data-stu-id="8457e-4670">Set the rest of fields as specified in 2.2.3.8</span></span>

-   <span data-ttu-id="8457e-4671">Calcula \_ el campo ulCheckSum en el encabezado.</span><span class="sxs-lookup"><span data-stu-id="8457e-4671">Calculate \_ulCheckSum field in the header.</span></span>
-   <span data-ttu-id="8457e-4672">Envíe el mensaje CPMCreateQueryIn al servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4672">Send the CPMCreateQueryIn message to the server.</span></span>
-   <span data-ttu-id="8457e-4673">Espere para recibir el mensaje CPMCreateQueryOut (vea los detalles en la sección 3.2.5.1.1) y descarte de forma silenciosa el resto de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="8457e-4673">Wait to receive CPMCreateQueryOut message (see details in section 3.2.5.1.1), silently discarding all other messages.</span></span>
-   <span data-ttu-id="8457e-4674">Notifique el valor del \_ campo de estado de la respuesta y, si fue correcto, la matriz de identificadores de cursor y valores booleanos informativos (como se especifica en 2.2.3.9) de nuevo a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4674">Report the value of the \_status field of the response and, if it was successful, the array of cursor handles, and informative Boolean values (as specified in 2.2.3.9) back to the higher layer.</span></span>

### <a name="32423-sending-a-cpmsetbindingsin-request"></a><span data-ttu-id="8457e-4675">3.2.4.2.3 enviar una solicitud de CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4675">3.2.4.2.3 Sending a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="8457e-4676">Normalmente, el nivel superior establecerá enlaces para cada columna que se va a devolver en las filas cuando ya tenga un identificador de cursor válido (después de recibir correctamente CPMCreateQueryOut, vea la sección 3.2.5.1.1).</span><span class="sxs-lookup"><span data-stu-id="8457e-4676">Typically, the higher layer will set bindings for each column to be returned in the rows when it already has valid cursor handle (after successfully receiving CPMCreateQueryOut, see section 3.2.5.1.1).</span></span> <span data-ttu-id="8457e-4677">Se espera que el mayor proporcione una matriz de estructuras CTableColumn, como se especifica en la sección 2.2.4.31, para el campo aColumns y un identificador de cursor válido.</span><span class="sxs-lookup"><span data-stu-id="8457e-4677">The higher is expected to provide an array of CTableColumn structures, as specified in Section 2.2.4.31, for the aColumns field and a valid cursor handle.</span></span>

<span data-ttu-id="8457e-4678">Cuando se recibe esta solicitud desde el nivel superior, el cliente debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4678">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4679">Calcule el número de estructuras CTableColumn en la matriz aColumns y establezca el campo cColumns en este valor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4679">Calculate the number of CTableColumn structures in the aColumns array, and set the cColumns field to this value.</span></span>
-   <span data-ttu-id="8457e-4680">Calcule el tamaño total en bytes de los campos cColumns y aColumns y establezca el \_ campo cbBindingDesc en este valor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4680">Calculate the total size in bytes of the cColumns and aColumns fields, and set the \_cbBindingDesc field to this value.</span></span>
-   <span data-ttu-id="8457e-4681">Establezca los campos especificados en el mensaje CPMSetBindingsIn en los valores proporcionados por el nivel de aplicación superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4681">Set specified fields in CPMSetBindingsIn message to the values provided by the higher application layer.</span></span> <span data-ttu-id="8457e-4682">Establezca el \_ campo ulChecksum en el valor calculado tal y como se especifica en la sección 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="8457e-4682">Set the \_ulChecksum field to the value calculated as specified in Section 3.2.5.</span></span>
-   <span data-ttu-id="8457e-4683">Envíe el mensaje CPMSetBindignsIn completado al servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4683">Send the completed CPMSetBindignsIn message to the server.</span></span>
-   <span data-ttu-id="8457e-4684">Espere para recibir un mensaje de CPMSetBindingsIn del servidor, descartando otros mensajes.</span><span class="sxs-lookup"><span data-stu-id="8457e-4684">Wait to receive a CPMSetBindingsIn message from server, discarding other messages.</span></span>
-   <span data-ttu-id="8457e-4685">Indica el estado del \_ campo de estado de la respuesta a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4685">Indicate the status from \_status field of the response to the higher layer.</span></span>

<span data-ttu-id="8457e-4686">Para fines informativos, se espera que las capas más altas pidan normalmente a un cliente que envíe un mensaje CPMGetRowsIn, pero el protocolo del servicio de indización de contenido no lo exige.</span><span class="sxs-lookup"><span data-stu-id="8457e-4686">For informative purposes, it is expected that higher layers will typically request a client to send a CPMGetRowsIn message, but this is not enforced by the Content Indexing Service Protocol.</span></span>

### <a name="32424-sending-a-cpmgetrowsin-request"></a><span data-ttu-id="8457e-4687">3.2.4.2.4 enviar una solicitud de CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4687">3.2.4.2.4 Sending a CPMGetRowsIn Request</span></span>

<span data-ttu-id="8457e-4688">Cuando el nivel superior está a punto de recibir información de filas, proporcionará al cliente de protocolo un identificador de cursor y de capítulo válido y proporcionará la descripción de búsqueda adecuada.</span><span class="sxs-lookup"><span data-stu-id="8457e-4688">When the higher layer is about to receive rows information it will provide protocol client with valid cursor and chapter handle and give appropriate seek description.</span></span> <span data-ttu-id="8457e-4689">Normalmente, se espera que una capa superior lo haga cuando tiene un cursor o un identificador de capítulo válido y los enlaces se han establecido con el mensaje CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-4689">Typically, a higher layer is expected to do so when it has a valid cursor and/or chapter handle, and the bindings had been set with CPMSetBindingsIn message.</span></span> <span data-ttu-id="8457e-4690">Para tener acceso al conjunto de filas en un capítulo, el nivel superior es usar el identificador de capítulo recibido del servidor en un mensaje CPMGetRowsOut anterior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4690">To access the rowset in a chapter, the higher layer is to use chapter handle received from the server in a previous CPMGetRowsOut message.</span></span>

<span data-ttu-id="8457e-4691">Cuando se recibe esta solicitud desde el nivel superior, el cliente debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4691">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4692">Determine el valor entero sin signo que se va a especificar para el \_ campo cbReadBuffer.</span><span class="sxs-lookup"><span data-stu-id="8457e-4692">Determine what unsigned integer value to specify for the \_cbReadBuffer field.</span></span> <span data-ttu-id="8457e-4693">Para determinar este valor, el cliente debe tomar el valor máximo de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4693">To determine this value, the client MUST take the maximum value from the following:</span></span>
-   -   <span data-ttu-id="8457e-4694">1000 veces el valor del \_ campo RowsToTransfer de c.</span><span class="sxs-lookup"><span data-stu-id="8457e-4694">One thousand times the value of the c\_RowsToTransfer field.</span></span>
    -   <span data-ttu-id="8457e-4695">Valor de \_ cbRowWidth, redondeado al múltiplo de 512 Byte más próximo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4695">Value of \_cbRowWidth, rounded up to the nearest 512 byte multiple.</span></span>
    -   <span data-ttu-id="8457e-4696">Tome el mayor de estos dos valores, hasta el límite de 16 k.</span><span class="sxs-lookup"><span data-stu-id="8457e-4696">Take the higher of these two values, up to the 16K limit.</span></span>
    -   <span data-ttu-id="8457e-4697">En los casos en los que una sola fila es mayor que 16 k, el servidor no puede devolver resultados a esta consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-4697">In cases where a single row is larger than 16K, the server cannot return results to this query.</span></span>

<span data-ttu-id="8457e-4698">Especifique una base de cliente para los datos de fila de tamaño variable en el campo espacio de direcciones de cliente en \_ ulClientBase.</span><span class="sxs-lookup"><span data-stu-id="8457e-4698">Specify a client base for variable-sized row data in client address space in \_ulClientBase field.</span></span>

<span data-ttu-id="8457e-4699">*Comportamiento de Windows: para que un cliente de 32 bits se comunique con un servidor de 32 bits o un cliente de 64 bits hablando con un servidor de 64 bits, este valor se establece en una dirección de memoria del búfer de recepción en el proceso de la aplicación. Esto permite que los punteros, que se reciben en el campo Rows de CPMGetRowsOut sean punteros de memoria correctos en un proceso de aplicación cliente. De lo contrario, se establece en 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="8457e-4699">*Windows Behavior: For a 32-bit client talking to a 32-bit server, or a 64 bit client talking to a 64-bit server this value is set to a memory address of the receiving buffer in application process. This allows for pointers, received in Rows field of CPMGetRowsOut to be correct memory pointers in a client application process. Otherwise it is set to 0x00000000.*</span></span>

-   <span data-ttu-id="8457e-4700">Calcule el tamaño de la descripción de búsqueda y establézcalo en el \_ campo cbSeek.</span><span class="sxs-lookup"><span data-stu-id="8457e-4700">Calculate the size of seek description and set it in the \_cbSeek field.</span></span>
-   <span data-ttu-id="8457e-4701">Establezca el valor de cbReserved (que actuaría como desplazamiento para el inicio de filas) en el valor de \_ cbSeek más 0x14.</span><span class="sxs-lookup"><span data-stu-id="8457e-4701">Set the value of cbReserved (which would act as an offset for Rows start) to the value of \_cbSeek plus 0x14.</span></span>
-   <span data-ttu-id="8457e-4702">Envíe un mensaje CPMConnectIn como se especifica en 2.2.3.15 al servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4702">Send a CPMConnectIn message as specified in 2.2.3.15 to the server.</span></span>

### <a name="32425-sending-a-cpmfetchvaluein-request"></a><span data-ttu-id="8457e-4703">3.2.4.2.5 enviar una solicitud de CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4703">3.2.4.2.5 Sending a CPMFetchValueIn Request</span></span>

<span data-ttu-id="8457e-4704">Si el cliente recibe una respuesta CPMGetRowsOut del servidor con el campo de estado de la columna establecido en StatusDeferred (0x01) significa que el valor de la propiedad no se incluyó en el campo Rows del mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4704">If the client receives a CPMGetRowsOut response from the server with the column's Status field set to StatusDeferred (0x01) it means that the property value was not included in the Rows field of the CPMGetRowsOut message.</span></span> <span data-ttu-id="8457e-4705">En este caso, la capa más alta normalmente solicita al cliente del protocolo que recupere el valor por medio del mensaje CPMFetchValueIn y proporciona el valor PropSpec y \_ WID para una propiedad aplazada, que el cliente de protocolo debe usar en el primer mensaje de CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-4705">In this case the higher layer typically asks the protocol client to retrieve the value by means of CPMFetchValueIn message, and provides the PropSpec and \_wid value for a deferred property, which the protocol client MUST use in the first CPMFetchValueIn message.</span></span>

<span data-ttu-id="8457e-4706">Si éste es el primer mensaje CPMFetchValueIn que el cliente ha enviado para solicitar la propiedad especificada, el cliente debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4706">If this is the first CPMFetchValueIn message the client has sent to request the specified property, the client MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4707">Establezca todos los campos de un mensaje como se especifica en la sección 2.2.3.19.</span><span class="sxs-lookup"><span data-stu-id="8457e-4707">Set all the fields in a message as specified in section 2.2.3.19.</span></span>
-   <span data-ttu-id="8457e-4708">Establezca \_ cbSoFar en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4708">Set \_cbSoFar to 0x00000000.</span></span>
-   <span data-ttu-id="8457e-4709">Establecer bytes actuales recibidos en 0.</span><span class="sxs-lookup"><span data-stu-id="8457e-4709">Set Current Bytes Received to 0.</span></span>
-   <span data-ttu-id="8457e-4710">Envíe el mensaje CPMFetchValueIn al servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4710">Send the CPMFetchValueIn message to the server.</span></span>

### <a name="32426-sending-a-cpmfreecursorin-request"></a><span data-ttu-id="8457e-4711">3.2.4.2.6 enviar una solicitud de CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="8457e-4711">3.2.4.2.6 Sending a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="8457e-4712">Una vez que el nivel superior ya no usa la consulta de búsqueda, puede liberar los recursos en el servidor solicitando al cliente que envíe un mensaje de CPMFreeCursorIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-4712">Once the higher level is no longer using the search query, it can release the resources on the server by asking the client to send a CPMFreeCursorIn message.</span></span>

<span data-ttu-id="8457e-4713">Cuando se recibe esta solicitud, el cliente debe enviar un mensaje CPMFreeCursorIn como se especifica en 2.2.3.28 al servidor, que contiene el identificador especificado por la capa superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4713">When this request is received, the client MUST send a CPMFreeCursorIn message as specified in 2.2.3.28 to the server, containing the handle specified by the upper layer.</span></span>

### <a name="32427-sending-a-cpmdisconnect-message"></a><span data-ttu-id="8457e-4714">3.2.4.2.7 enviar un mensaje de CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="8457e-4714">3.2.4.2.7 Sending a CPMDisconnect Message</span></span>

<span data-ttu-id="8457e-4715">Si el nivel superior no tiene más consultas para el servicio de indexación, para liberar más recursos del servidor, la aplicación puede solicitar que el cliente envíe un mensaje CPMDisconnect al servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4715">If the higher layer has no more queries for the indexing service, to free up more server resources, the application may request that the client send a CPMDisconnect message to the server.</span></span> <span data-ttu-id="8457e-4716">Cuando se recibe esta consulta, el cliente debe enviar simplemente el mensaje como se ha solicitado.</span><span class="sxs-lookup"><span data-stu-id="8457e-4716">When this query is received, the client MUST simply send the message as requested.</span></span> <span data-ttu-id="8457e-4717">No hay ninguna respuesta a este mensaje del servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4717">There is no response to this message from the server.</span></span>

### <a name="325-message-processing-and-sequencing-rules"></a><span data-ttu-id="8457e-4718">Reglas de procesamiento y secuenciación de mensajes 3.2.5</span><span class="sxs-lookup"><span data-stu-id="8457e-4718">3.2.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="8457e-4719">Cuando el cliente recibe una respuesta de mensaje del servidor, el cliente debe utilizar el último mensaje enviado para determinar si el mensaje recibido del servidor es el esperado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4719">When the client receives a message response from the server, the client MUST use the Last Sent Message to determine if the message received from the server is the one expected by the client.</span></span> <span data-ttu-id="8457e-4720">\_Se deben omitir todos los mensajes con el campo MSG diferente del último mensaje de envío.</span><span class="sxs-lookup"><span data-stu-id="8457e-4720">All messages with \_msg field different from the one in Last Send Message MUST be ignored.</span></span>

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a><span data-ttu-id="8457e-4721">3.2.5.1 recibir una respuesta CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="8457e-4721">3.2.5.1 Receiving a CPMCreateQueryOut Response</span></span>

<span data-ttu-id="8457e-4722">Cuando el cliente recibe una respuesta del mensaje CPMCreateQueryOut desde el servidor, el cliente debe devolver el \_ Estado y, si el estado es correcto, los valores de identificador de cursor a una capa superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4722">When the client receives a CPMCreateQueryOut message response from the server, the client MUST return \_status and (if the status is successful) cursor handle values back to higher layer.</span></span> <span data-ttu-id="8457e-4723">Todas las acciones posteriores se encuentran hasta el nivel superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4723">Any further actions are up to the higher layer.</span></span>

<span data-ttu-id="8457e-4724">Como el nivel más alto es consciente de la estructura de la consulta, siempre se espera que se devuelva el número de identificadores de cursor correctos en el mensaje CPMCreateOueryOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4724">As the higher layer is aware of query structure it will always expect correct number of cursor handles to be returned in the CPMCreateOueryOut message.</span></span> <span data-ttu-id="8457e-4725">Los identificadores de cursor se devuelven en el orden siguiente: el primer identificador está en el conjunto de filas sin capítulo, el segundo es el primer conjunto de filas de capítulo (que es la agrupación de los resultados en función de la primera categoría especificada en el campo CategorizationSet del mensaje CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="8457e-4725">The cursor handles are returned in the following order: the first handle is to the unchaptered rowset, the second is to the first chaptered rowset (which is the grouping of results based on the first category specified in the CategorizationSet field of the CPMCreateQueryIn message.)</span></span>

<span data-ttu-id="8457e-4726">Para fines informativos, se espera que las capas superiores puedan realizar las siguientes acciones, pero el cliente de CISP no las aplica:</span><span class="sxs-lookup"><span data-stu-id="8457e-4726">For informative purposes, it is expected that higher layers can do the following actions, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="8457e-4727">Use CPMSetBindingsIn para establecer enlaces para columnas individuales y realizar las siguientes acciones en la ruta de acceso de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-4727">Use CPMSetBindingsIn, to set bindings for individual columns and do any subsequent actions on query path</span></span>
-   <span data-ttu-id="8457e-4728">Use CPMGetQueryStatusIn para comprobar el progreso de la ejecución de una consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-4728">Use CPMGetQueryStatusIn, to check on the execution progress of a query.</span></span>
-   <span data-ttu-id="8457e-4729">Use CPMRatioFinishedIn para solicitar el porcentaje de finalización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-4729">Use CPMRatioFinishedIn, to request the completion percentage of the query.</span></span>

### <a name="3252-receiving-a-cpmgetrowsout-response"></a><span data-ttu-id="8457e-4730">3.2.5.2 recibir una respuesta CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="8457e-4730">3.2.5.2 Receiving a CPMGetRowsOut Response</span></span>

<span data-ttu-id="8457e-4731">Cuando el cliente recibe una respuesta del mensaje CPMGetRowsOut desde el servidor, el cliente debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4731">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4732">Compruebe si el \_ campo de estado del encabezado indica éxito o error.</span><span class="sxs-lookup"><span data-stu-id="8457e-4732">Check if the \_status field in the header indicates success or failure.</span></span>
-   <span data-ttu-id="8457e-4733">Si el \_ valor de estado es \_ búfer de estado \_ demasiado \_ pequeño (0xC0000023), el cliente debe comprobar el último mensaje enviado.</span><span class="sxs-lookup"><span data-stu-id="8457e-4733">If the \_status value is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), the client MUST check the Last Message Sent state.</span></span> <span data-ttu-id="8457e-4734">Si no contiene un mensaje CPMGetRowsIn, el mensaje recibido debe omitirse de forma silenciosa.</span><span class="sxs-lookup"><span data-stu-id="8457e-4734">If it does not contain a CPMGetRowsIn message, the received message MUST be silently ignored.</span></span> <span data-ttu-id="8457e-4735">De lo contrario, el cliente debe enviar al servidor un nuevo mensaje CPMGetRowsIn con todos los campos idénticos al almacenado, con la excepción de que el \_ CBREADBUFFER debe aumentarse en 512 (pero no mayor que 0x4000).</span><span class="sxs-lookup"><span data-stu-id="8457e-4735">Otherwise, the client MUST send to the server a new CPMGetRowsIn message with all fields identical to the stored one, except that the \_cbReadBuffer MUST be increased by 512 (but not greater than 0x4000).</span></span> <span data-ttu-id="8457e-4736">Si el \_ Estado es el búfer de estado \_ \_ demasiado \_ pequeño (0XC0000023) y el último mensaje enviado ya tiene \_ CBREADBUFFER igual a 0x4000 cliente debe notificar el error hasta el nivel superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4736">If \_status is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), and Last Message Sent already has \_cbReadBuffer equal to 0x4000 client MUST report the error up to the higher level.</span></span>
-   <span data-ttu-id="8457e-4737">Si el \_ valor de estado es cualquier otro valor de error, el cliente debe indicar el error hasta el nivel superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4737">If the \_status value is any other error value, the client MUST indicate the failure up to the higher layer.</span></span>
-   <span data-ttu-id="8457e-4738">Si el \_ valor de estado indica que la operación se ha realizado correctamente, los resultados se deben indicar hasta el nivel superior que solicita la información, y las acciones adicionales están en el nivel más alto.</span><span class="sxs-lookup"><span data-stu-id="8457e-4738">If the \_status value indicates success, the results MUST be indicated up to the higher layer requesting the information, and further actions are up to the higher layer.</span></span>

<span data-ttu-id="8457e-4739">Para fines informativos, se espera que las capas superiores realicen normalmente las siguientes acciones, pero el cliente del protocolo del servicio de indización de contenido no las aplica:</span><span class="sxs-lookup"><span data-stu-id="8457e-4739">For informative purposes, it is expected that higher layers will typically do the following actions, but these are not enforced by the Content Indexing Service Protocol client:</span></span>

-   <span data-ttu-id="8457e-4740">Si los valores de las filas representan los identificadores de documento, el capítulo o los marcadores de marcador, el nivel superior normalmente los almacenará para su uso en operaciones posteriores que impliquen identificadores de documento, capítulos o identificadores de marcador válidos.</span><span class="sxs-lookup"><span data-stu-id="8457e-4740">If the values in rows represent the document IDs, chapter or bookmark handles the higher layer will typically store them for use in subsequent operations which involve valid document IDs, chapter or bookmark handles.</span></span>
-   <span data-ttu-id="8457e-4741">El nivel superior normalmente almacenará o mostrará o utilizará los datos de los valores de fila.</span><span class="sxs-lookup"><span data-stu-id="8457e-4741">The higher layer will typically store or display or otherwise use the data from row values.</span></span>
-   <span data-ttu-id="8457e-4742">En el caso de los valores que se marcaron como el nivel más alto aplazado, capturará el valor mediante mensajes CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-4742">For the values which were marked as deferred higher layer will fetch the value using CPMFetchValueIn messages.</span></span>
-   <span data-ttu-id="8457e-4743">La descripción de la búsqueda se devuelve también al nivel superior y puede ser reutilizada o examinada por el nivel superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4743">The seek description is returned back to higher layer as well, and can be reused or examined by the higher layer.</span></span>

<span data-ttu-id="8457e-4744">Para fines informativos, si la capa superior solicitó controladores a capítulos y marcadores que se recibieron en las filas, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4744">For informative purposes, if the higher layer requested handles to chapters and bookmarks which were received in the rows, it may do the following:</span></span>

-   <span data-ttu-id="8457e-4745">Use CPMGetQueryStatusExIn para comprobar el progreso de la ejecución de una consulta, así como información de estado adicional, como el número de documentos filtrados, los documentos que quedan por filtrar, la proporción de documentos procesados por la consulta, el número total de filas de la consulta y la posición del marcador en el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-4745">Use CPMGetQueryStatusExIn, to check on the execution progress of a query, as well as additional status information, such as the number of filtered documents, documents remaining to be filtered, the ratio of documents processed by the query, the total number of rows in the query, and the position of the bookmark in the rowset.</span></span>
-   <span data-ttu-id="8457e-4746">Use CPMGetNotify para solicitar que el servidor notifique al cliente los cambios del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-4746">Use CPMGetNotify, to request that the server notify the client of rowset changes.</span></span>
-   <span data-ttu-id="8457e-4747">Use CPMGetApproximatePositionIn para solicitar la posición aproximada de un marcador en un capítulo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4747">Use CPMGetApproximatePositionIn, to request the approximate position of a bookmark in a chapter.</span></span>
-   <span data-ttu-id="8457e-4748">Use CPMCompareBmkIn para solicitar una comparación de dos marcadores en un capítulo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4748">Use CPMCompareBmkIn, to request a comparison of two bookmarks in a chapter.</span></span>
-   <span data-ttu-id="8457e-4749">Use CPMRestartPositionIn para que el servidor cambie la ubicación del cursor al inicio del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-4749">Use CPMRestartPositionIn, to the server to change the location of the cursor to the start of rowset.</span></span>

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a><span data-ttu-id="8457e-4750">3.2.5.3 recibir una respuesta CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="8457e-4750">3.2.5.3 Receiving a CPMFetchValueOut Response</span></span>

<span data-ttu-id="8457e-4751">Cuando el cliente recibe una respuesta del mensaje CPMGetRowsOut desde el servidor, el cliente debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4751">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="8457e-4752">Compruebe si el \_ campo de estado del encabezado indica éxito o error.</span><span class="sxs-lookup"><span data-stu-id="8457e-4752">Check if the \_status field in the header indicates success or failure.</span></span> <span data-ttu-id="8457e-4753">En caso de error, notifique a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4753">In a case of failure notify the higher layer.</span></span> <span data-ttu-id="8457e-4754">De lo contrario, continúe a continuación.</span><span class="sxs-lookup"><span data-stu-id="8457e-4754">Otherwise, continue below.</span></span>
-   <span data-ttu-id="8457e-4755">Compruebe \_ fValueExist y, si está establecido en 0x00000000, notifique a la capa superior que no se encontró el valor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4755">Check \_fValueExist, and if set to 0x00000000 notify the higher layer that the value was not found.</span></span>
-   <span data-ttu-id="8457e-4756">De lo contrario, anexe \_ cbValue bytes de vValue al valor de propiedad actual.</span><span class="sxs-lookup"><span data-stu-id="8457e-4756">Otherwise append \_ cbValue bytes from vValue to Current Property Value.</span></span>
-   <span data-ttu-id="8457e-4757">Si \_ \_ fMoreExists se establece en 0x00000001, se incrementan los \_ bytes actuales recibidos por \_ cbValue y se envía un mensaje de CPMFetchValueIn al servidor, estableciendo \_ CbSoFar en el valor de bytes actuales recibidos, \_ cbPropSpec en cero y \_ cbChunk en el tamaño de búfer que desea la capa superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4757">If \_\_fMoreExists is set to 0x00000001 then increment \_Current Bytes Received by \_cbValue and send a CPMFetchValueIn message to the server, setting \_cbSoFar to the value of Current Bytes Received, \_cbPropSpec to zero and \_cbChunk to the buffer size desired by the higher layer.</span></span>
-   <span data-ttu-id="8457e-4758">Si \_ fMoreExists se establece en 0x00000000, indique el valor de propiedad del valor de propiedad actual a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4758">If \_fMoreExists is set to 0x00000000 then indicate the property value from Current Property Value to the higher layer.</span></span>

### <a name="3254-receiving-a-cpmfreecursorout-response"></a><span data-ttu-id="8457e-4759">3.2.5.4 recibir una respuesta CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="8457e-4759">3.2.5.4 Receiving a CPMFreeCursorOut Response</span></span>

<span data-ttu-id="8457e-4760">Cuando el cliente recibe una respuesta de mensaje CPMFreeCursorOut correcta del servidor, el cliente debe devolver el \_ valor de cCursorsRemaining a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="8457e-4760">When the client receives a successful CPMFreeCursorOut message response from the server, the client MUST return the \_cCursorsRemaining value to the higher layer.</span></span>

<span data-ttu-id="8457e-4761">La siguiente información se proporciona solo con fines informativos y no la aplica el cliente de CISP.</span><span class="sxs-lookup"><span data-stu-id="8457e-4761">The following information is given for informative purposes only and is not enforced by the CISP client.</span></span> <span data-ttu-id="8457e-4762">Se espera que el nivel superior realice un seguimiento de los identificadores de cursor y no use los que ya se han liberado.</span><span class="sxs-lookup"><span data-stu-id="8457e-4762">The higher layer is expected to keep track of cursor handles and not to use ones which have already been freed.</span></span> <span data-ttu-id="8457e-4763">Una vez que el número de \_ cCursorsRemaining es igual a 0x00000000, el nivel superior puede utilizar la conexión para especificar otra consulta (mediante un mensaje CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="8457e-4763">Once the number of \_cCursorsRemaining is equal to 0x00000000, the higher layer can use the connection to specify another query (using a CPMCreateQueryIn message).</span></span>

### <a name="326-timer-events"></a><span data-ttu-id="8457e-4764">Eventos de temporizador de 3.2.6 procedimientos</span><span class="sxs-lookup"><span data-stu-id="8457e-4764">3.2.6 Timer Events</span></span>

<span data-ttu-id="8457e-4765">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8457e-4765">None.</span></span>

### <a name="327-other-local-events"></a><span data-ttu-id="8457e-4766">3.2.7 otros eventos locales</span><span class="sxs-lookup"><span data-stu-id="8457e-4766">3.2.7 Other Local Events</span></span>

<span data-ttu-id="8457e-4767">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8457e-4767">None.</span></span>

## <a name="4-protocol-examples"></a><span data-ttu-id="8457e-4768">4 Ejemplos de protocolo</span><span class="sxs-lookup"><span data-stu-id="8457e-4768">4 Protocol Examples</span></span>

-   [<span data-ttu-id="8457e-4769">4,1 ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="8457e-4769">4.1 Example 1</span></span>](#41-example-1)
-   [<span data-ttu-id="8457e-4770">ejemplo 2 de 4,2</span><span class="sxs-lookup"><span data-stu-id="8457e-4770">4.2 Example 2</span></span>](#42-example-2)

### <a name="41-example-1"></a><span data-ttu-id="8457e-4771">4,1 ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="8457e-4771">4.1 Example 1</span></span>

<span data-ttu-id="8457e-4772">En el ejemplo siguiente, se considera un escenario en el que el usuario JOHN del equipo A desea obtener los tamaños de los archivos que contienen la palabra "Microsoft" del conjunto de documentos almacenados en el servidor X en el sistema de catálogos.</span><span class="sxs-lookup"><span data-stu-id="8457e-4772">In the following example, we consider a scenario in which the user JOHN on machine A wants to obtain the sizes of files that contain the word "Microsoft" from the set of documents stored on server X in catalog SYSTEM.</span></span> <span data-ttu-id="8457e-4773">Supongamos que el equipo A ejecuta un sistema operativo Windows XP de 32 bits y el equipo X está ejecutando un sistema operativo Windows Server 2003 de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8457e-4773">Let us assume that machine A is running a 32-bit Windows XP operating system and machine X is running a 32-bit Windows Server 2003 operating system.</span></span>

1.  <span data-ttu-id="8457e-4774">El usuario inicia una aplicación de búsqueda y entra en la consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8457e-4774">The user launches a search application and enters the search query.</span></span> <span data-ttu-id="8457e-4775">A su vez, la aplicación pasa la consulta de búsqueda al cliente del protocolo.</span><span class="sxs-lookup"><span data-stu-id="8457e-4775">The application in turn passes the search query to the protocol client.</span></span>
2.  <span data-ttu-id="8457e-4776">El cliente de Protocolo establece una conexión con el servidor de indexación X. El cliente de protocolo usa el \\ elemento de CI de canalización con nombre \\ \_ SKADS para conectarse al servidor X a través de SMB.</span><span class="sxs-lookup"><span data-stu-id="8457e-4776">The protocol client establishes a connection with indexing server X. The protocol client uses the named pipe \\pipe\\CI\_SKADS to connect to the server X over SMB.</span></span>
3.  <span data-ttu-id="8457e-4777">A continuación, el cliente de protocolo prepara un mensaje CPMConnectIn con los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="8457e-4777">The protocol client then prepares a CPMConnectIn message with the following values:</span></span>

    <span data-ttu-id="8457e-4778">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4778">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8457e-4779">**\_ MSG** se establece en 0x000000C8, lo que indica que se trata de un mensaje CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-4779">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectIn message.</span></span>
    -   <span data-ttu-id="8457e-4780">**\_ status** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4780">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="8457e-4781">**\_ ulChecksum** contiene la suma de comprobación, calculada como se especifica en la sección 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="8457e-4781">**\_ulChecksum** contains the checksum, computed as specified in Section 3.2.4.</span></span>
    -   <span data-ttu-id="8457e-4782">**\_ ulReserved2** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4782">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="8457e-4783">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4783">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8457e-4784">**\_ iClientVersion** se establece en 0x00000008, lo que indica que el servidor va a validar el campo de suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="8457e-4784">**\_iClientVersion** is set to 0x00000008, indicating that the server is to validate the checksum field.</span></span>
    -   <span data-ttu-id="8457e-4785">**\_ fClientIsRemote** se establece en 0x00000001, lo que indica que el servidor es un servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="8457e-4785">**\_fClientIsRemote** is set to 0x00000001, indicating that the server is a remote server.</span></span>
    -   <span data-ttu-id="8457e-4786">**\_ cbBlob1** se establece en el tamaño, en bytes, de los campos cPropSet, PropertySet1 y PropertySet2 combinados.</span><span class="sxs-lookup"><span data-stu-id="8457e-4786">**\_cbBlob1** is set to the size, in bytes, of the cPropSet, PropertySet1 and PropertySet2 fields combined.</span></span>
    -   <span data-ttu-id="8457e-4787">**\_ cbBlob2** se establece en 0x00000004 (lo que significa que no hay conjuntos de propiedades adicionales).</span><span class="sxs-lookup"><span data-stu-id="8457e-4787">**\_cbBlob2** is set to 0x00000004 (meaning no extra property sets).</span></span>
    -   <span data-ttu-id="8457e-4788">**MachineName** se establece en.</span><span class="sxs-lookup"><span data-stu-id="8457e-4788">**MachineName** is set to A.</span></span>
    -   <span data-ttu-id="8457e-4789">**Username** se establece en John.</span><span class="sxs-lookup"><span data-stu-id="8457e-4789">**UserName** is set to JOHN.</span></span>
    -   <span data-ttu-id="8457e-4790">**cPropSets** se establece en 0x00000002.</span><span class="sxs-lookup"><span data-stu-id="8457e-4790">**cPropSets** is set to 0x00000002.</span></span>
    -   <span data-ttu-id="8457e-4791">El campo **PropertySet1** es de tipo CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="8457e-4791">**PropertySet1** field is of type CDbPropSet.</span></span> <span data-ttu-id="8457e-4792">La estructura CDbPropSet que consta del campo PropertySet1 se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4792">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>
        -   <span data-ttu-id="8457e-4793">El campo **GuidPropSet** está establecido en A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ ext).</span><span class="sxs-lookup"><span data-stu-id="8457e-4793">**GuidPropSet** field is set to A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET\_FSCIFRMWRK\_EXT).</span></span>
        -   <span data-ttu-id="8457e-4794">el campo **cProperties** se establece en 0x00000004.</span><span class="sxs-lookup"><span data-stu-id="8457e-4794">**cProperties** field is set to 0x00000004.</span></span>
        -   <span data-ttu-id="8457e-4795">el campo **aProps** es una matriz de estructuras CDbProp.</span><span class="sxs-lookup"><span data-stu-id="8457e-4795">**aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="8457e-4796">Para el **elemento \[ aProps \] 0** :</span><span class="sxs-lookup"><span data-stu-id="8457e-4796">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="8457e-4797">**PropId** se establece en 0X00000002 (DBPROP \_ CI \_ Catalog \_ Name).</span><span class="sxs-lookup"><span data-stu-id="8457e-4797">**PropId** is set to 0x00000002 (DBPROP\_CI\_CATALOG\_NAME).</span></span>
            -   <span data-ttu-id="8457e-4798">**DBPROPOPTIONS** se establece en 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4798">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="8457e-4799">**DBPROPSTATUS** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4799">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="8457e-4800">Para el elemento **colid** :</span><span class="sxs-lookup"><span data-stu-id="8457e-4800">For the **ColId** element:</span></span>
                -   <span data-ttu-id="8457e-4801">**eKind** está establecido en 0X00000001 (DBKIND \_ GUID \_ PROPID)</span><span class="sxs-lookup"><span data-stu-id="8457e-4801">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID)</span></span>
                -   <span data-ttu-id="8457e-4802">**GUID** es null (todo ceros), lo que significa que el valor se aplica a la consulta, no solo a una columna.</span><span class="sxs-lookup"><span data-stu-id="8457e-4802">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="8457e-4803">**ulID** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4803">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="8457e-4804">Para el elemento **vValue** :</span><span class="sxs-lookup"><span data-stu-id="8457e-4804">For the **vValue** element:</span></span>
                -   <span data-ttu-id="8457e-4805">**vType** se establece en 0X001F (VT \_ LPWStr).</span><span class="sxs-lookup"><span data-stu-id="8457e-4805">**vType** is set to 0x001F (VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="8457e-4806">**vValue** se establece en "System", el nombre del catálogo deseado.</span><span class="sxs-lookup"><span data-stu-id="8457e-4806">**vValue** is set to "SYSTEM", the name of the desired catalog.</span></span>

            <span data-ttu-id="8457e-4807">Para el **elemento \[ aProps \] 1** :</span><span class="sxs-lookup"><span data-stu-id="8457e-4807">For the **aProps\[1\]** element:</span></span>

            -   <span data-ttu-id="8457e-4808">**PropId** se establece en 0X00000007 (DBPROP \_ CI \_ query \_ Type)</span><span class="sxs-lookup"><span data-stu-id="8457e-4808">**PropId** is set to 0x00000007 (DBPROP\_CI\_QUERY\_TYPE)</span></span>
            -   <span data-ttu-id="8457e-4809">**DBPROPOPTIONS** se establece en 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4809">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="8457e-4810">**DBPROPSTATUS** es Set to0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4810">**DBPROPSTATUS** is set to0x00000000.</span></span>
            -   <span data-ttu-id="8457e-4811">Para el elemento **colid** :</span><span class="sxs-lookup"><span data-stu-id="8457e-4811">For the **ColId** element:</span></span>
                -   <span data-ttu-id="8457e-4812">**eKind** se establece en 0X00000001 (DBKIND \_ GUID \_ PROPID).</span><span class="sxs-lookup"><span data-stu-id="8457e-4812">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="8457e-4813">**GUID** es null (todo ceros), lo que significa que el valor se aplica a la consulta, no solo a una columna.</span><span class="sxs-lookup"><span data-stu-id="8457e-4813">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="8457e-4814">**ulID** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4814">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="8457e-4815">Para el elemento **vValue** :</span><span class="sxs-lookup"><span data-stu-id="8457e-4815">For the **vValue** element:</span></span>
                -   <span data-ttu-id="8457e-4816">**vType** se establece en 0X0003 (VT \_ I4).</span><span class="sxs-lookup"><span data-stu-id="8457e-4816">**vType** is set to 0x0003 (VT\_I4).</span></span>
                -   <span data-ttu-id="8457e-4817">**vValue** se establece en 0X00000000 (CiNormal), lo que significa que es una consulta normal.</span><span class="sxs-lookup"><span data-stu-id="8457e-4817">**vValue** is set to 0x00000000 (CiNormal), meaning it is a regular query.</span></span>

            <span data-ttu-id="8457e-4818">Para el **elemento \[ aProps \] 2** :</span><span class="sxs-lookup"><span data-stu-id="8457e-4818">For the **aProps\[2\]** element:</span></span>

            -   <span data-ttu-id="8457e-4819">**PropId** se establece en 0X00000004 (DBPROP \_ CI \_ Scope \_ Flags).</span><span class="sxs-lookup"><span data-stu-id="8457e-4819">**PropId** is set to 0x00000004 (DBPROP\_CI\_SCOPE\_FLAGS).</span></span>
            -   <span data-ttu-id="8457e-4820">**DBPROPOPTIONS** se establece en 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4820">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="8457e-4821">**DBPROPSTATUS** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4821">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="8457e-4822">Para el elemento **colid** :</span><span class="sxs-lookup"><span data-stu-id="8457e-4822">For the **ColId** element:</span></span>
                -   <span data-ttu-id="8457e-4823">**eKind** se establece en 0X00000001 (DBKIND \_ GUID \_ PROPID).</span><span class="sxs-lookup"><span data-stu-id="8457e-4823">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="8457e-4824">**GUID** es null (todo ceros), lo que significa que el valor se aplica a la consulta, no solo a una columna.</span><span class="sxs-lookup"><span data-stu-id="8457e-4824">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="8457e-4825">**ulID** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4825">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="8457e-4826">Para el elemento **vValue** :</span><span class="sxs-lookup"><span data-stu-id="8457e-4826">For the **vValue** element:</span></span>
                -   <span data-ttu-id="8457e-4827">**vType**: 0X1003 (VT \_ Vector \| VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="8457e-4827">**vType**: 0x1003 (VT\_VECTOR \| VT\_I4)</span></span>
                -   <span data-ttu-id="8457e-4828">**vValue**: 0x00000001/0x00000001 (un elemento con el valor 1), lo que significa que las subcarpetas de búsqueda</span><span class="sxs-lookup"><span data-stu-id="8457e-4828">**vValue**: 0x00000001 / 0x00000001 (one element with value 1), meaning search sub-folders</span></span>

            <span data-ttu-id="8457e-4829">Para el **elemento \[ aProps \] 3** :</span><span class="sxs-lookup"><span data-stu-id="8457e-4829">For the **aProps\[3\]** element:</span></span>

            -   <span data-ttu-id="8457e-4830">**PropId**: 0X00000003 (DBPROP \_ CI \_ incluir \_ ámbitos)</span><span class="sxs-lookup"><span data-stu-id="8457e-4830">**PropId**: 0x00000003 (DBPROP\_CI\_INCLUDE\_SCOPES)</span></span>
            -   <span data-ttu-id="8457e-4831">**DBPROPOPTIONS**: 0x0000000</span><span class="sxs-lookup"><span data-stu-id="8457e-4831">**DBPROPOPTIONS**: 0x0000000</span></span>
            -   <span data-ttu-id="8457e-4832">**DBPROPSTATUS**: 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8457e-4832">**DBPROPSTATUS**: 0x00000000</span></span>
            -   <span data-ttu-id="8457e-4833">Para el elemento **colid** :</span><span class="sxs-lookup"><span data-stu-id="8457e-4833">For the **ColId** element:</span></span>
                -   <span data-ttu-id="8457e-4834">**eKind** se establece en 0X00000001 (DBKIND \_ GUID \_ PROPID).</span><span class="sxs-lookup"><span data-stu-id="8457e-4834">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="8457e-4835">**GUID** es null (todo ceros), lo que significa que el valor se aplica a la consulta, no solo a una columna.</span><span class="sxs-lookup"><span data-stu-id="8457e-4835">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="8457e-4836">**ulID** está establecido en 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8457e-4836">**ulID** is set to 0x00000000</span></span>
            -   <span data-ttu-id="8457e-4837">Para el elemento **vValue** :</span><span class="sxs-lookup"><span data-stu-id="8457e-4837">For the **vValue** element:</span></span>
                -   <span data-ttu-id="8457e-4838">**vType** se establece en 0X101F (VT \_ Vector \| VT \_ LPWStr).</span><span class="sxs-lookup"><span data-stu-id="8457e-4838">**vType** is set to 0x101F (VT\_VECTOR \| VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="8457e-4839">**vValue** se establece en 0x00000001/0x00000002/" \\ " (un elemento con una cadena terminada en NULL de 2 caracteres), es decir, el ámbito raíz.</span><span class="sxs-lookup"><span data-stu-id="8457e-4839">**vValue** is set to 0x00000001 / 0x00000002 / "\\" (one element with a 2 character null-terminated string), meaning the root scope.</span></span>

    -   <span data-ttu-id="8457e-4840">El campo **PropertySet2** es de tipo CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="8457e-4840">The **PropertySet2** field is of type CDbPropSet.</span></span>

        <span data-ttu-id="8457e-4841">La estructura CDbPropSet que consta del campo PropertySet1 se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4841">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>

        -   <span data-ttu-id="8457e-4842">**GuidPropSet** se establece en AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ ext).</span><span class="sxs-lookup"><span data-stu-id="8457e-4842">**GuidPropSet** is set to AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET\_CIFRMWRKCORE\_EXT).</span></span>
        -   <span data-ttu-id="8457e-4843">el campo **cProperties** está establecido en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8457e-4843">**cProperties** field is set to 0x00000001.</span></span>
        -   <span data-ttu-id="8457e-4844">El campo **aProps** es una matriz de estructuras CDbProp.</span><span class="sxs-lookup"><span data-stu-id="8457e-4844">The **aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="8457e-4845">Para el **elemento \[ aProps \] 0** :</span><span class="sxs-lookup"><span data-stu-id="8457e-4845">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="8457e-4846">**PropId** se establece en 0X00000002 (DBPROP \_ Machine).</span><span class="sxs-lookup"><span data-stu-id="8457e-4846">**PropId** is set to 0x00000002 (DBPROP\_MACHINE).</span></span>
            -   <span data-ttu-id="8457e-4847">**DBPROPOPTIONS** se establece en 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4847">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="8457e-4848">**DBPROPSTATUS** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4848">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="8457e-4849">Para el elemento **colid** :</span><span class="sxs-lookup"><span data-stu-id="8457e-4849">For the **ColId** element:</span></span>
                -   <span data-ttu-id="8457e-4850">**eKind** se establece en 0X00000001 (DBKIND \_ GUID \_ PROPID).</span><span class="sxs-lookup"><span data-stu-id="8457e-4850">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID),</span></span>
                -   <span data-ttu-id="8457e-4851">**GUID** es null (todo ceros), lo que significa que el valor se aplica a la consulta, no solo a una columna.</span><span class="sxs-lookup"><span data-stu-id="8457e-4851">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="8457e-4852">**ulID** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4852">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="8457e-4853">Para el elemento **vValue** :</span><span class="sxs-lookup"><span data-stu-id="8457e-4853">For **vValue** element:</span></span>
                -   <span data-ttu-id="8457e-4854">**vType**: 0X0008 (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="8457e-4854">**vType**: 0x0008 (VT\_BSTR)</span></span>
                -   <span data-ttu-id="8457e-4855">**vValue**: 0x04/"x" (4 bytes/cadena Unicode terminada en null), lo que significa "x": el nombre de un servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4855">**vValue**: 0x04 / "X" (4 bytes / null-terminated Unicode string), meaning "X" -name of a server.</span></span>

    -   <span data-ttu-id="8457e-4856">el campo **cExtPropSet** está establecido en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4856">**cExtPropSet** field is set to 0x00000000.</span></span>
    -   <span data-ttu-id="8457e-4857">la matriz **aPropertySets** no existe.</span><span class="sxs-lookup"><span data-stu-id="8457e-4857">**aPropertySets** array does not exist.</span></span>
    -   <span data-ttu-id="8457e-4858">Se rellenan varios campos de relleno según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="8457e-4858">Various padding fields are filled in as needed.</span></span> <span data-ttu-id="8457e-4859">El mensaje se envía al servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4859">The message is sent to the server.</span></span>

4.  <span data-ttu-id="8457e-4860">El servidor comprueba que **\_ ulChecksum** es correcto, comprueba que el usuario está autorizado para hacer esta solicitud y responde con un mensaje CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4860">The server verifies that the **\_ulChecksum** is correct, verifies that the user is authorized to make this request, and responds with a CPMConnectOut message.</span></span>

    <span data-ttu-id="8457e-4861">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4861">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8457e-4862">**\_ MSG** se establece en 0x000000C8, lo que indica que se trata de un mensaje CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4862">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectOut message.</span></span>
    -   <span data-ttu-id="8457e-4863">**\_ status** se establece en 0x0000000, lo que indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4863">**\_status** is set to 0x0000000 indicating SUCCESS.</span></span>
    -   <span data-ttu-id="8457e-4864">**\_ ulChecksum** se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="8457e-4864">**\_ulChecksum** is set to 0.</span></span>
    -   <span data-ttu-id="8457e-4865">**\_ ulReserved2** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4865">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="8457e-4866">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4866">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8457e-4867">el campo **\_ serverVersion** está establecido en 0x00000007 (32 de windows XP o 32 bits Windows Server 2003).</span><span class="sxs-lookup"><span data-stu-id="8457e-4867">**\_serverVersion** field is set to 0x00000007 (32-bit Windows XP or 32-bit Windows Server 2003).</span></span>
    -   <span data-ttu-id="8457e-4868">los campos **\_ reservados** se rellenan con datos arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="8457e-4868">**\_reserved** fields are filled with arbitrary data.</span></span>

5.  <span data-ttu-id="8457e-4869">El cliente prepara un mensaje CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-4869">The client prepares a CPMCreateQueryIn message.</span></span>

    <span data-ttu-id="8457e-4870">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4870">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8457e-4871">**\_ MSG** se establece en 0x000000CA, lo que indica que se trata de un mensaje CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-4871">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryIn message.</span></span>
    -   <span data-ttu-id="8457e-4872">**\_ status** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4872">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="8457e-4873">**\_ ulChecksum** contiene la suma de comprobación, calculada según 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="8457e-4873">**\_ulChecksum** contains the checksum, computed according to 3.2.5.</span></span>
    -   <span data-ttu-id="8457e-4874">**\_ ulReserved2** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4874">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="8457e-4875">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4875">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8457e-4876">El campo **tamaño** se establece en el tamaño del resto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-4876">**Size** field is set to the size of the rest of the message.</span></span>
    -   <span data-ttu-id="8457e-4877">El campo **CColumnSetPresent** se establece en 0x01.</span><span class="sxs-lookup"><span data-stu-id="8457e-4877">**CColumnSetPresent** field is set to 0x01.</span></span>
    -   <span data-ttu-id="8457e-4878">El campo **ColumnSet** es de tipo CColumnSet.</span><span class="sxs-lookup"><span data-stu-id="8457e-4878">**ColumnSet** field is of type CColumnSet.</span></span> <span data-ttu-id="8457e-4879">La estructura CColumnSet que consta de este campo se establece de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="8457e-4879">The CColumnSet structure comprising this field is set as follows:</span></span>
        -   <span data-ttu-id="8457e-4880">el campo **\_ Count** se establece en 0x00000001, lo que indica que se devuelve una columna.</span><span class="sxs-lookup"><span data-stu-id="8457e-4880">**\_count** field is set to 0x00000001 indicating one column is returned.</span></span>
        -   <span data-ttu-id="8457e-4881">la matriz de **índices** es 0x00000000 que indica la primera entrada en \_ aPropSpec.</span><span class="sxs-lookup"><span data-stu-id="8457e-4881">**indexes** array is 0x00000000 indicating the first entry in \_aPropSpec.</span></span>
    -   <span data-ttu-id="8457e-4882">El campo **CRestrictionPresent** se establece en 0x01, lo que indica que el campo **Restriction** está presente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4882">**CRestrictionPresent** field is set to 0x01 indicating the **Restriction** field is present.</span></span>
    -   <span data-ttu-id="8457e-4883">El campo de **restricción** es de tipo CRestriction y está establecido en:</span><span class="sxs-lookup"><span data-stu-id="8457e-4883">**Restriction** field is of type CRestriction and is set to:</span></span>
        -   <span data-ttu-id="8457e-4884">**\_ ulType** se establece en 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="8457e-4884">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
        -   <span data-ttu-id="8457e-4885">**\_ Weight** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4885">**\_weight** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="8457e-4886">El resto del campo contiene una estructura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="8457e-4886">The rest of the field contains a CContentRestriction structure:</span></span>
        -   <span data-ttu-id="8457e-4887">La **\_ propiedad** se establece en GUID B725F130-47EF-101A-A5F1-02608c9eebac/0X00000001 (para PRSPEC \_ PROPID)/0x13 que representa el cuerpo del documento.</span><span class="sxs-lookup"><span data-stu-id="8457e-4887">**\_Property** is set to GUID B725F130-47EF-101A-A5F1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13 which represents the document body.</span></span>
        -   <span data-ttu-id="8457e-4888">**\_ CC** está establecido en 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="8457e-4888">**\_Cc** is set to 0x00000009.</span></span>
        -   <span data-ttu-id="8457e-4889">**\_ pwcsphrase** se establece en la cadena "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="8457e-4889">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
        -   <span data-ttu-id="8457e-4890">**\_ LCID** se establece en 0Xc0a (para inglés).</span><span class="sxs-lookup"><span data-stu-id="8457e-4890">**\_lcid** is set to 0x409 (for English).</span></span>
        -   <span data-ttu-id="8457e-4891">**\_ ulGenerateMethod** se establece en 0x00000000 (coincidencia exacta).</span><span class="sxs-lookup"><span data-stu-id="8457e-4891">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>
    -   <span data-ttu-id="8457e-4892">**CSortPresent** está establecido en 0x00.</span><span class="sxs-lookup"><span data-stu-id="8457e-4892">**CSortPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="8457e-4893">**CCategorizationSetPresent** está establecido en 0x00.</span><span class="sxs-lookup"><span data-stu-id="8457e-4893">**CCategorizationSetPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="8457e-4894">**RowSetProperties** se establece de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4894">**RowSetProperties** is set as follows:</span></span>
        -   <span data-ttu-id="8457e-4895">**\_ uBooleanOptions** se establece en 0x00000001 (secuencial).</span><span class="sxs-lookup"><span data-stu-id="8457e-4895">**\_uBooleanOptions** is set to 0x00000001 (sequential).</span></span>
        -   <span data-ttu-id="8457e-4896">**\_ ulMaxOpenRows** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4896">**\_ulMaxOpenRows** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="8457e-4897">**\_ ulMemoryUsage** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4897">**\_ulMemoryUsage** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="8457e-4898">\_**cMaxResults** se establece en 0x00000100 (devuelve como máximo 256 filas).</span><span class="sxs-lookup"><span data-stu-id="8457e-4898">\_**cMaxResults** is set to 0x00000100 (return at most 256 rows).</span></span>
        -   <span data-ttu-id="8457e-4899">**\_ cCmdTimeOut** se establece en 0x00000000 (nunca se agota el tiempo de espera).</span><span class="sxs-lookup"><span data-stu-id="8457e-4899">**\_cCmdTimeOut** is set to 0x00000000 (never timeout).</span></span>
    -   <span data-ttu-id="8457e-4900">**PidMapper** se establece en:</span><span class="sxs-lookup"><span data-stu-id="8457e-4900">**PidMapper** is set to:</span></span>
        -   <span data-ttu-id="8457e-4901">**\_ Count** se establece en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8457e-4901">**\_count** is set to 0x00000001.</span></span>
        -   <span data-ttu-id="8457e-4902">**\_ aPropSpec** se establece en GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC/0X00000001 (para PRSPEC \_ PROPID)/0x0000000c, que representa la propiedad de tamaño de archivo de Windows.</span><span class="sxs-lookup"><span data-stu-id="8457e-4902">**\_aPropSpec** is set to GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>

6.  <span data-ttu-id="8457e-4903">El servidor lo procesa y responde con un mensaje CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4903">The server processes it and responds with a CPMCreateQueryOut message.</span></span>

    <span data-ttu-id="8457e-4904">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4904">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8457e-4905">**\_ MSG** se establece en 0x000000CA, lo que indica que se trata de un mensaje CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4905">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryOut message.</span></span>
    -   <span data-ttu-id="8457e-4906">**\_ status** se establece en Success.</span><span class="sxs-lookup"><span data-stu-id="8457e-4906">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="8457e-4907">**\_ ulChecksum** se establece en 0x00000000 (o cualquier otro valor arbitrario).</span><span class="sxs-lookup"><span data-stu-id="8457e-4907">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="8457e-4908">**\_ ulReserved2** se establece en 0x00000000 (o cualquier otro valor arbitrario).</span><span class="sxs-lookup"><span data-stu-id="8457e-4908">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="8457e-4909">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4909">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8457e-4910">**\_ fTrueSeqeuntial** se establece en 0x00000000, lo que indica que la consulta puede utilizar un índice.</span><span class="sxs-lookup"><span data-stu-id="8457e-4910">**\_fTrueSeqeuntial** is set to 0x00000000, indicating that the query can use an index.</span></span>
    -   <span data-ttu-id="8457e-4911">**\_ fWorkIdUnique** se establece en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8457e-4911">**\_fWorkIdUnique** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="8457e-4912">La matriz **aCursors** contiene un solo elemento, que representa un identificador de cursor para esta consulta.</span><span class="sxs-lookup"><span data-stu-id="8457e-4912">The **aCursors** array contains only one element, representing a cursor handle to this query.</span></span> <span data-ttu-id="8457e-4913">El valor depende del estado del servidor.</span><span class="sxs-lookup"><span data-stu-id="8457e-4913">The value depends on the state of the server.</span></span> <span data-ttu-id="8457e-4914">Supongamos que el valor devuelto es 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="8457e-4914">Let us assume that the returned value is 0xAAAAAAAA.</span></span>

7.  <span data-ttu-id="8457e-4915">El cliente emite un mensaje de solicitud CPMSetBindingsIn para definir el formato de una fila.</span><span class="sxs-lookup"><span data-stu-id="8457e-4915">The client issues a CPMSetBindingsIn request message to define the format of a row.</span></span>

    <span data-ttu-id="8457e-4916">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4916">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8457e-4917">**\_ MSG** se establece en 0x000000D0, lo que indica que se trata de un mensaje CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-4917">**\_msg** is set to 0x000000D0, indicating that this is a CPMSetBindingsIn message.</span></span>
    -   <span data-ttu-id="8457e-4918">**\_ status** se establece en Success.</span><span class="sxs-lookup"><span data-stu-id="8457e-4918">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="8457e-4919">**\_ ulChecksum** se establece en 0x00000000 (o cualquier otro valor arbitrario).</span><span class="sxs-lookup"><span data-stu-id="8457e-4919">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="8457e-4920">**\_ ulReserved2** se establece en 0x00000000 (o cualquier otro valor arbitrario).</span><span class="sxs-lookup"><span data-stu-id="8457e-4920">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="8457e-4921">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4921">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8457e-4922">**\_ hCursor** se establece en 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="8457e-4922">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="8457e-4923">**\_ cbRow** se establece en 0x10 (lo suficientemente grande como para ajustarse a las columnas).</span><span class="sxs-lookup"><span data-stu-id="8457e-4923">**\_cbRow** is set to 0x10 (big enough to fit columns).</span></span>
    -   <span data-ttu-id="8457e-4924">**\_ cbBindingDesc** se establece en el tamaño de los campos **\_ cColumns** y **\_ aColumns** combinados.</span><span class="sxs-lookup"><span data-stu-id="8457e-4924">**\_cbBindingDesc** is set to the size of the **\_cColumns** and **\_aColumns** fields combined.</span></span>
    -   <span data-ttu-id="8457e-4925">**\_ cColumns** se establece en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8457e-4925">**\_cColumns** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="8457e-4926">la matriz **\_ aColumns** se establece para que contenga una estructura CTableColumn que contenga:</span><span class="sxs-lookup"><span data-stu-id="8457e-4926">**\_aColumns** array is set to contain one CTableColumn structure containing:</span></span>
    -   -   <span data-ttu-id="8457e-4927">**\_ PropSpec** se establece en GUID b725f130-47ef-101A-A5-F1-02608c9eebac/0X00000001 (para PRSPEC \_ PROPID)/0x0000000c, que representa la propiedad de tamaño de archivo de Windows.</span><span class="sxs-lookup"><span data-stu-id="8457e-4927">**\_PropSpec** is set to GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>
        -   <span data-ttu-id="8457e-4928">**\_ vType** se establece en 0x0015 (VT \_ UI8).</span><span class="sxs-lookup"><span data-stu-id="8457e-4928">**\_vType** is set to 0x0015 (VT\_UI8).</span></span>
        -   <span data-ttu-id="8457e-4929">**\_ ValueUsed** se establece en 0x01 (columna transferida en la fila).</span><span class="sxs-lookup"><span data-stu-id="8457e-4929">**\_ValueUsed** is set to 0x01 (column transferred in row).</span></span>
        -   <span data-ttu-id="8457e-4930">**\_ ValueOffset** se establece en 0x0002 (al principio de la fila).</span><span class="sxs-lookup"><span data-stu-id="8457e-4930">**\_ValueOffset** is set to 0x0002 (at beginning of row).</span></span>
        -   <span data-ttu-id="8457e-4931">El **\_ valor** de se establece en 0x08 (tamaño de una \_ UI8 de VT).</span><span class="sxs-lookup"><span data-stu-id="8457e-4931">**\_ValueSize** is set to 0x08 (size of a VT\_UI8).</span></span>
        -   <span data-ttu-id="8457e-4932">**\_ StatusUsed** se establece en 0x01.</span><span class="sxs-lookup"><span data-stu-id="8457e-4932">**\_StatusUsed** is set to 0x01.</span></span>
        -   <span data-ttu-id="8457e-4933">**\_ StatusOffset** está establecido en 0x0A.</span><span class="sxs-lookup"><span data-stu-id="8457e-4933">**\_StatusOffset** is set to 0x0A.</span></span>
        -   <span data-ttu-id="8457e-4934">**\_ LengthUsed** está establecido en 0x00.</span><span class="sxs-lookup"><span data-stu-id="8457e-4934">**\_LengthUsed** is set to 0x00.</span></span>

8.  <span data-ttu-id="8457e-4935">El servidor lo procesa y responde con un mensaje CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-4935">The server processes it and responds with a CPMSetBindingsIn message.</span></span>

    <span data-ttu-id="8457e-4936">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4936">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8457e-4937">**\_ MSG** se establece en 0x000000D0.</span><span class="sxs-lookup"><span data-stu-id="8457e-4937">**\_msg** is set to 0x000000D0.</span></span>
    -   <span data-ttu-id="8457e-4938">**\_ status** se establece en Success.</span><span class="sxs-lookup"><span data-stu-id="8457e-4938">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="8457e-4939">**\_ ulChecksum** se establece en 0x00000000 (o cualquier otro valor arbitrario).</span><span class="sxs-lookup"><span data-stu-id="8457e-4939">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="8457e-4940">**\_ ulReserved2** se establece en 0x00000000 (o cualquier otro valor arbitrario).</span><span class="sxs-lookup"><span data-stu-id="8457e-4940">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

9.  <span data-ttu-id="8457e-4941">El cliente emite un mensaje de solicitud CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-4941">The client issues a CPMGetRowsIn request message.</span></span> <span data-ttu-id="8457e-4942">Supongamos que el cliente está preparado para aceptar 100 filas en este momento y los desea en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4942">Let us assume that the client is prepared to accept 100 rows at this point, and wants them in ascending order.</span></span>

    <span data-ttu-id="8457e-4943">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4943">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8457e-4944">**\_ MSG** se establece en 0x000000CC, lo que indica que se trata de un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="8457e-4944">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsIn message.</span></span>
    -   <span data-ttu-id="8457e-4945">**\_ status** se establece en 0x00000000</span><span class="sxs-lookup"><span data-stu-id="8457e-4945">**\_status** is set to 0x00000000</span></span>
    -   <span data-ttu-id="8457e-4946">**\_ ulChecksum** contiene la suma de comprobación, calculada según la sección 0.</span><span class="sxs-lookup"><span data-stu-id="8457e-4946">**\_ulChecksum** contains the checksum, computed according to Section 0.</span></span>
    -   <span data-ttu-id="8457e-4947">**\_ ulReserved2** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4947">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="8457e-4948">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4948">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8457e-4949">**\_ hCursor** se establece en 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="8457e-4949">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="8457e-4950">**\_ cRowsToTransfer** se establece en 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="8457e-4950">**\_cRowsToTransfer** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="8457e-4951">**\_ cRowWidth** se establece en 0x00000010 (de los enlaces).</span><span class="sxs-lookup"><span data-stu-id="8457e-4951">**\_cRowWidth** is set to 0x00000010 (from bindings).</span></span>
    -   <span data-ttu-id="8457e-4952">**\_ cbSeek** se establece en 0x14, que es el tamaño de los campos ETYPE, \_ chapt y CRowSeekNext combinados.</span><span class="sxs-lookup"><span data-stu-id="8457e-4952">**\_cbSeek** is set to 0x14 which is the size of the eType, \_chapt and CRowSeekNext fields combined.</span></span>
    -   <span data-ttu-id="8457e-4953">**\_ cbReserved** se establece en 0x18 (0x14 más \_ cbSeek).</span><span class="sxs-lookup"><span data-stu-id="8457e-4953">**\_cbReserved** is set to 0x18 (0x14 plus \_cbSeek).</span></span>
    -   <span data-ttu-id="8457e-4954">**\_ cbReadBuffer** se establece en 0x800 (0x64 \* 0x10 redondeado hacia arriba al siguiente múltiplo de 0x200).</span><span class="sxs-lookup"><span data-stu-id="8457e-4954">**\_cbReadBuffer** is set to 0x800 (0x64\*0x10 rounded up to the next multiple of 0x200).</span></span>
    -   <span data-ttu-id="8457e-4955">**\_ ulClientBase** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4955">**\_ulClientBase** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="8457e-4956">**\_ fBwdfetch** se establece en 0x00000000, lo que indica que las filas se van a capturar en orden hacia delante.</span><span class="sxs-lookup"><span data-stu-id="8457e-4956">**\_fBwdfetch** is set to 0x00000000 indicating that the rows are to be fetched in forward order.</span></span>
    -   <span data-ttu-id="8457e-4957">**ETYPE** se establece en 0x0000001, lo que indica que el cliente desea filas siguientes.</span><span class="sxs-lookup"><span data-stu-id="8457e-4957">**eType** is set to 0x0000001 indicating that the client wants next rows.</span></span>
    -   <span data-ttu-id="8457e-4958">**\_ chapt** está establecido en 0 (no es un resultado en el capítulo).</span><span class="sxs-lookup"><span data-stu-id="8457e-4958">**\_chapt** is set to 0 (not a chaptered result).</span></span>
    -   <span data-ttu-id="8457e-4959">**SeekDescription** se establece en CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="8457e-4959">**SeekDescription** is set to CRowSeekNext.</span></span> <span data-ttu-id="8457e-4960">La estructura CRowSeekNext contiene los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="8457e-4960">The CRowSeekNext structure contains the following values:</span></span>
        -   <span data-ttu-id="8457e-4961">**CiTblChapt** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4961">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="8457e-4962">**\_ hRegion** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4962">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="8457e-4963">**\_ cSkip** se establece en 0, lo que indica que el cliente no desea omitir filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-4963">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>

10. <span data-ttu-id="8457e-4964">El servidor lo procesa y responde con un mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4964">The server processes it and responds with a CPMGetRowsOut message.</span></span> <span data-ttu-id="8457e-4965">Supongamos que el servidor encontró 100 documentos que contienen la palabra "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="8457e-4965">Let us assume that the server found 100 documents that contain the word "Microsoft".</span></span>

    <span data-ttu-id="8457e-4966">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4966">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8457e-4967">**\_ MSG** se establece en 0x000000CC, lo que indica que se trata de un mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="8457e-4967">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsOut message.</span></span>
    -   <span data-ttu-id="8457e-4968">**\_ status** se establece en Success.</span><span class="sxs-lookup"><span data-stu-id="8457e-4968">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="8457e-4969">**\_ ulChecksum** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4969">**\_ulChecksum** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="8457e-4970">**\_ ulReserved2** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4970">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="8457e-4971">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4971">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8457e-4972">**\_ CRowsReturned** se establece en 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="8457e-4972">**\_CRowsReturned** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="8457e-4973">**ETYPE** se establece en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="8457e-4973">**eType** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="8457e-4974">**\_ chapt** está establecido en 0x00000000 (no en un resultado en el capítulo).</span><span class="sxs-lookup"><span data-stu-id="8457e-4974">**\_chapt** is set to 0x00000000 (not a chaptered result).</span></span>
    -   <span data-ttu-id="8457e-4975">**SeekDescription** contiene una estructura CRowSeekNext, que se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4975">**SeekDescription** contains a CRowSeekNext structure, populated as follows:</span></span>
        -   <span data-ttu-id="8457e-4976">**CiTblChapt** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4976">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="8457e-4977">**\_ hRegion** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4977">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="8457e-4978">**\_ cSkip** se establece en 0, lo que indica que el cliente no desea omitir filas.</span><span class="sxs-lookup"><span data-stu-id="8457e-4978">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>
    -   <span data-ttu-id="8457e-4979">**Rows** contiene el tamaño de los documentos 100 que contienen la palabra "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="8457e-4979">**Rows** contains the size of the 100 documents that contain the word "Microsoft".</span></span> <span data-ttu-id="8457e-4980">Dado que se trata de datos de tamaño fijo, simplemente está estructurado como una lista de enteros de 8 bytes sin signo de 100.</span><span class="sxs-lookup"><span data-stu-id="8457e-4980">Since this is fixed-sized data, it is simply structured as a list of 100, 8-byte unsigned integers.</span></span>

11. <span data-ttu-id="8457e-4981">El cliente envía un mensaje CPMDisconnect para finalizar la conexión.</span><span class="sxs-lookup"><span data-stu-id="8457e-4981">The client sends a CPMDisconnect message to end the connection.</span></span>

    <span data-ttu-id="8457e-4982">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4982">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="8457e-4983">**\_ MSG** se establece en 0x000000C9, lo que indica que se trata de un mensaje CPMDisconnect.</span><span class="sxs-lookup"><span data-stu-id="8457e-4983">**\_msg** is set to 0x000000C9, indicating that this is a CPMDisconnect message.</span></span>
    -   <span data-ttu-id="8457e-4984">**\_ status** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4984">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="8457e-4985">**\_ ulChecksum** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4985">**\_ulChecksum** is set to 0x00000000.</span></span>

12. <span data-ttu-id="8457e-4986">El servidor procesa el mensaje y quita todo el estado del cliente.</span><span class="sxs-lookup"><span data-stu-id="8457e-4986">The server processes the message and removes all client state.</span></span>

### <a name="42-example-2"></a><span data-ttu-id="8457e-4987">ejemplo 2 de 4,2</span><span class="sxs-lookup"><span data-stu-id="8457e-4987">4.2 Example 2</span></span>

<span data-ttu-id="8457e-4988">En el ejemplo anterior, la consulta era bastante sencilla.</span><span class="sxs-lookup"><span data-stu-id="8457e-4988">In the previous example, the query was quite simple.</span></span> <span data-ttu-id="8457e-4989">Ahora vamos a considerar una consulta ligeramente más compleja.</span><span class="sxs-lookup"><span data-stu-id="8457e-4989">Let us now consider a slightly more complex query.</span></span> <span data-ttu-id="8457e-4990">Supongamos que el usuario desea recuperar el tamaño de los documentos que contienen las siguientes palabras: "Microsoft" y "Office".</span><span class="sxs-lookup"><span data-stu-id="8457e-4990">Let us assume that the user wants to retrieve the size of the documents that contain both the following words: "Microsoft" and "Office".</span></span> <span data-ttu-id="8457e-4991">Esto se especifica cambiando el campo de restricción incluido en el mensaje CPMCreateQueryIn enviado en el paso 5 de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8457e-4991">This is specified by changing the Restriction field contained in the CPMCreateQueryIn message sent in step 5 as follows:</span></span>

<span data-ttu-id="8457e-4992">El campo de **restricción** es de tipo CRestriction y se establece en:</span><span class="sxs-lookup"><span data-stu-id="8457e-4992">The **Restriction** field is of type CRestriction and is set to:</span></span>

-   -   <span data-ttu-id="8457e-4993">**\_ ulType** se establece en 0x00000004 (RTAnd).</span><span class="sxs-lookup"><span data-stu-id="8457e-4993">**\_ulType** is set to 0x00000004 (RTAnd).</span></span>
    -   <span data-ttu-id="8457e-4994">**\_ Weight** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-4994">**\_weight** is set to 0x00000000.</span></span>

<span data-ttu-id="8457e-4995">El resto del campo contiene una estructura CNodeRestriction:</span><span class="sxs-lookup"><span data-stu-id="8457e-4995">The rest of the field contains a CNodeRestriction structure:</span></span>

-   -   <span data-ttu-id="8457e-4996">**\_ cNode** se establece en 0x00000002, lo que indica que hay dos nodos en la matriz de nodos.</span><span class="sxs-lookup"><span data-stu-id="8457e-4996">**\_cNode** is set to 0x00000002, indicating that there are two nodes in the paNode array.</span></span>
    -   <span data-ttu-id="8457e-4997">El campo **\_ panode** es una matriz de dos estructuras CRestriction.</span><span class="sxs-lookup"><span data-stu-id="8457e-4997">The **\_paNode** field is an array of two CRestriction structures.</span></span>

        <span data-ttu-id="8457e-4998">el **\_ nodo \[ 0 \]** contiene:</span><span class="sxs-lookup"><span data-stu-id="8457e-4998">**\_paNode\[0\]** contains:</span></span>

        -   -   <span data-ttu-id="8457e-4999">**\_ ulType** se establece en 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="8457e-4999">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="8457e-5000">**\_ Weight** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-5000">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="8457e-5001">El resto del campo contiene una estructura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="8457e-5001">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="8457e-5002">La **\_ propiedad** se establece en GUID b725f130-47ef-101A-a5f1-02608c9eebac/0X00000001 (para PRSPEC \_ PROPID)/0x13.</span><span class="sxs-lookup"><span data-stu-id="8457e-5002">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="8457e-5003">**\_ CC** está establecido en 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="8457e-5003">**\_Cc** is set to 0x00000009.</span></span>
                -   <span data-ttu-id="8457e-5004">**\_ pwcsphrase** se establece en la cadena "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="8457e-5004">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
                -   <span data-ttu-id="8457e-5005">**\_ LCID** se establece en 0Xc0a (para inglés).</span><span class="sxs-lookup"><span data-stu-id="8457e-5005">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="8457e-5006">**\_ ulGenerateMethod** se establece en 0x00000000 (coincidencia exacta).</span><span class="sxs-lookup"><span data-stu-id="8457e-5006">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

        <span data-ttu-id="8457e-5007">el **\_ nodo \[ 1 \]** contiene:</span><span class="sxs-lookup"><span data-stu-id="8457e-5007">**\_paNode\[1\]** contains:</span></span>

        -   -   <span data-ttu-id="8457e-5008">**\_ ulType** se establece en 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="8457e-5008">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="8457e-5009">**\_ Weight** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="8457e-5009">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="8457e-5010">El resto del campo contiene una estructura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="8457e-5010">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="8457e-5011">La **\_ propiedad** se establece en GUID b725f130-47ef-101A-a5f1-02608c9eebac/0X00000001 (para PRSPEC \_ PROPID)/0x13.</span><span class="sxs-lookup"><span data-stu-id="8457e-5011">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="8457e-5012">**\_ CC** está establecido en 0x00000006.</span><span class="sxs-lookup"><span data-stu-id="8457e-5012">**\_Cc** is set to 0x00000006.</span></span>
                -   <span data-ttu-id="8457e-5013">**\_ pwcsphrase** se establece en la cadena "Office".</span><span class="sxs-lookup"><span data-stu-id="8457e-5013">**\_pwcsphrase** is set to the string "Office".</span></span>
                -   <span data-ttu-id="8457e-5014">**\_ LCID** se establece en 0Xc0a (para inglés).</span><span class="sxs-lookup"><span data-stu-id="8457e-5014">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="8457e-5015">**\_ ulGenerateMethod** se establece en 0x00000000 (coincidencia exacta).</span><span class="sxs-lookup"><span data-stu-id="8457e-5015">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

## <a name="5-security"></a><span data-ttu-id="8457e-5016">5 Seguridad</span><span class="sxs-lookup"><span data-stu-id="8457e-5016">5 Security</span></span>

### <a name="51-security-considerations-for-implementers"></a><span data-ttu-id="8457e-5017">5.1 Consideraciones de seguridad para los implementadores</span><span class="sxs-lookup"><span data-stu-id="8457e-5017">5.1 Security Considerations for Implementers</span></span>

<span data-ttu-id="8457e-5018">Las implementaciones de indexación que indexan contenido seguro deben considerar el uso del contexto de usuario proporcionado por \[ MS SMB MS-SMB \] para recortar los resultados de la búsqueda y devolver solo aquellos accesibles para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="8457e-5018">Indexing implementations which index secure content should consider using the user context provided by SMB \[MS-SMB\] to trim search results and return only those accessible to the caller.</span></span>

### <a name="52-index-of-security-parameters"></a><span data-ttu-id="8457e-5019">5.2 Índice de parámetros de seguridad</span><span class="sxs-lookup"><span data-stu-id="8457e-5019">5.2 Index of Security Parameters</span></span>



| <span data-ttu-id="8457e-5020">Parámetro de seguridad</span><span class="sxs-lookup"><span data-stu-id="8457e-5020">Security Parameter</span></span>  | <span data-ttu-id="8457e-5021">Sección</span><span class="sxs-lookup"><span data-stu-id="8457e-5021">Section</span></span> |
|---------------------|---------|
| <span data-ttu-id="8457e-5022">Nivel de suplantación</span><span class="sxs-lookup"><span data-stu-id="8457e-5022">Impersonation level</span></span> | <span data-ttu-id="8457e-5023">2.1</span><span class="sxs-lookup"><span data-stu-id="8457e-5023">2.1</span></span>     |



 

## <a name="6-index-of-version-specific-behavior"></a><span data-ttu-id="8457e-5024">6 índice de comportamiento específico de la versión</span><span class="sxs-lookup"><span data-stu-id="8457e-5024">6 Index of Version Specific Behavior</span></span>



| <span data-ttu-id="8457e-5025">Comportamiento específico de la versión</span><span class="sxs-lookup"><span data-stu-id="8457e-5025">Version Specific Behavior</span></span>                                                                         | <span data-ttu-id="8457e-5026">Sección</span><span class="sxs-lookup"><span data-stu-id="8457e-5026">Section</span></span>   | <span data-ttu-id="8457e-5027">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8457e-5027">Windows 2000</span></span> | <span data-ttu-id="8457e-5028">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8457e-5028">Windows XP</span></span> | <span data-ttu-id="8457e-5029">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8457e-5029">Windows Server 2003</span></span> |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| <span data-ttu-id="8457e-5030">Este protocolo se implementa en Windows 2000, Windows XP, Windows Server 2003 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8457e-5030">This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span> | <span data-ttu-id="8457e-5031">1.3.2</span><span class="sxs-lookup"><span data-stu-id="8457e-5031">1.3.2</span></span>     | <span data-ttu-id="8457e-5032">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5032">X</span></span>            | <span data-ttu-id="8457e-5033">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5033">X</span></span>          | <span data-ttu-id="8457e-5034">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5034">X</span></span>                   |
| <span data-ttu-id="8457e-5035">Las aplicaciones suelen interactuar con un contenedor de interfaz OLE DB</span><span class="sxs-lookup"><span data-stu-id="8457e-5035">Applications typically interact with an OLE DB interface wrapper</span></span>                                  | <span data-ttu-id="8457e-5036">1.4</span><span class="sxs-lookup"><span data-stu-id="8457e-5036">1.4</span></span>       | <span data-ttu-id="8457e-5037">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5037">X</span></span>            | <span data-ttu-id="8457e-5038">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5038">X</span></span>          | <span data-ttu-id="8457e-5039">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5039">X</span></span>                   |
| <span data-ttu-id="8457e-5040">Valores de NTSTATUS</span><span class="sxs-lookup"><span data-stu-id="8457e-5040">NTSTATUS values</span></span>                                                                                   | <span data-ttu-id="8457e-5041">1.8</span><span class="sxs-lookup"><span data-stu-id="8457e-5041">1.8</span></span>       | <span data-ttu-id="8457e-5042">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5042">X</span></span>            | <span data-ttu-id="8457e-5043">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5043">X</span></span>          | <span data-ttu-id="8457e-5044">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5044">X</span></span>                   |
| <span data-ttu-id="8457e-5045">El cliente establece el \_ campo de estado en cada encabezado de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8457e-5045">The client sets the \_status field in each Message Header.</span></span>                                        | <span data-ttu-id="8457e-5046">2.2.2</span><span class="sxs-lookup"><span data-stu-id="8457e-5046">2.2.2</span></span>     | <span data-ttu-id="8457e-5047">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5047">X</span></span>            | <span data-ttu-id="8457e-5048">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5048">X</span></span>          | <span data-ttu-id="8457e-5049">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5049">X</span></span>                   |
| <span data-ttu-id="8457e-5050">el valor de cPendingScans suele ser cero</span><span class="sxs-lookup"><span data-stu-id="8457e-5050">cPendingScans value is usually zero</span></span>                                                               | <span data-ttu-id="8457e-5051">2.2.3.1</span><span class="sxs-lookup"><span data-stu-id="8457e-5051">2.2.3.1</span></span>   | <span data-ttu-id="8457e-5052">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5052">X</span></span>            | <span data-ttu-id="8457e-5053">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5053">X</span></span>          | <span data-ttu-id="8457e-5054">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5054">X</span></span>                   |
| <span data-ttu-id="8457e-5055">valor iClientVersion</span><span class="sxs-lookup"><span data-stu-id="8457e-5055">iClientVersion value</span></span>                                                                              | <span data-ttu-id="8457e-5056">2.2.3.6</span><span class="sxs-lookup"><span data-stu-id="8457e-5056">2.2.3.6</span></span>   | <span data-ttu-id="8457e-5057">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5057">X</span></span>            | <span data-ttu-id="8457e-5058">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5058">X</span></span>          | <span data-ttu-id="8457e-5059">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5059">X</span></span>                   |
| <span data-ttu-id="8457e-5060">\_valor cbChunk</span><span class="sxs-lookup"><span data-stu-id="8457e-5060">\_cbChunk value</span></span>                                                                                   | <span data-ttu-id="8457e-5061">2.2.3.19</span><span class="sxs-lookup"><span data-stu-id="8457e-5061">2.2.3.19</span></span>  | <span data-ttu-id="8457e-5062">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5062">X</span></span>            | <span data-ttu-id="8457e-5063">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5063">X</span></span>          | <span data-ttu-id="8457e-5064">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5064">X</span></span>                   |
| <span data-ttu-id="8457e-5065">direcciones de memoria de 32 bits y de 64 bits</span><span class="sxs-lookup"><span data-stu-id="8457e-5065">32-bit and 64-bit memory addresses</span></span>                                                                | <span data-ttu-id="8457e-5066">3.2.4.2.4</span><span class="sxs-lookup"><span data-stu-id="8457e-5066">3.2.4.2.4</span></span> | <span data-ttu-id="8457e-5067">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5067">X</span></span>            | <span data-ttu-id="8457e-5068">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5068">X</span></span>          | <span data-ttu-id="8457e-5069">X</span><span class="sxs-lookup"><span data-stu-id="8457e-5069">X</span></span>                   |



 

 

 





