---
title: Protocolo de servicios de indexación de contenido
description: Este documento es una especificación del Protocolo de servicio de indexación de contenido.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5265d9d8c802b278b4349ef4b8248b068dc7edc4
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492297"
---
# <a name="content-indexing-services-protocol"></a><span data-ttu-id="d07fb-103">Protocolo de servicios de indexación de contenido</span><span class="sxs-lookup"><span data-stu-id="d07fb-103">Content Indexing Services Protocol</span></span>

> [!NOTE]
> <span data-ttu-id="d07fb-104">Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d07fb-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d07fb-105">En versiones posteriores, use [Windows Search](../search/-search-3x-wds-overview.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="d07fb-106">Especificación de protocolo, versión 0.12</span><span class="sxs-lookup"><span data-stu-id="d07fb-106">Protocol Specification, Version 0.12</span></span>

-   [<span data-ttu-id="d07fb-107">1 Introducción</span><span class="sxs-lookup"><span data-stu-id="d07fb-107">1 Introduction</span></span>](#1-introduction)
    -   [<span data-ttu-id="d07fb-108">1.1 Glosario</span><span class="sxs-lookup"><span data-stu-id="d07fb-108">1.1 Glossary</span></span>](#11-glossary)
    -   [<span data-ttu-id="d07fb-109">1.2 Referencias</span><span class="sxs-lookup"><span data-stu-id="d07fb-109">1.2 References</span></span>](#12-references)
    -   [<span data-ttu-id="d07fb-110">Introducción al protocolo 1.3 (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="d07fb-110">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
    -   [<span data-ttu-id="d07fb-111">1.4 Relación con otros protocolos</span><span class="sxs-lookup"><span data-stu-id="d07fb-111">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
    -   [<span data-ttu-id="d07fb-112">1.5 Requisitos previos y condiciones previas</span><span class="sxs-lookup"><span data-stu-id="d07fb-112">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
    -   [<span data-ttu-id="d07fb-113">1.6 Declaración de aplicabilidad</span><span class="sxs-lookup"><span data-stu-id="d07fb-113">1.6 Applicability Statement</span></span>](#16-applicability-statement)
    -   [<span data-ttu-id="d07fb-114">1.7 Control de versiones y negociación de funcionalidad</span><span class="sxs-lookup"><span data-stu-id="d07fb-114">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
    -   [<span data-ttu-id="d07fb-115">1.8 Campos extensibles por el proveedor</span><span class="sxs-lookup"><span data-stu-id="d07fb-115">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
    -   [<span data-ttu-id="d07fb-116">1.9 Asignaciones de estándares</span><span class="sxs-lookup"><span data-stu-id="d07fb-116">1.9 Standards Assignments</span></span>](#19-standards-assignments)
-   [<span data-ttu-id="d07fb-117">2 Mensajes</span><span class="sxs-lookup"><span data-stu-id="d07fb-117">2 Messages</span></span>](#2-messages)
    -   [<span data-ttu-id="d07fb-118">2.1 Transporte</span><span class="sxs-lookup"><span data-stu-id="d07fb-118">2.1 Transport</span></span>](#21-transport)
    -   [<span data-ttu-id="d07fb-119">2.2 Sintaxis de mensajes</span><span class="sxs-lookup"><span data-stu-id="d07fb-119">2.2 Message Syntax</span></span>](#22-message-syntax)
-   [<span data-ttu-id="d07fb-120">3 Detalles del protocolo</span><span class="sxs-lookup"><span data-stu-id="d07fb-120">3 Protocol Details</span></span>](#3-protocol-details)
    -   [<span data-ttu-id="d07fb-121">3.1 Detalles del servidor</span><span class="sxs-lookup"><span data-stu-id="d07fb-121">3.1 Server Details</span></span>](#31-server-details)
    -   [<span data-ttu-id="d07fb-122">3.2 Detalles del cliente</span><span class="sxs-lookup"><span data-stu-id="d07fb-122">3.2 Client Details</span></span>](#32-client-details)
-   [<span data-ttu-id="d07fb-123">4 Ejemplos de protocolo</span><span class="sxs-lookup"><span data-stu-id="d07fb-123">4 Protocol Examples</span></span>](#4-protocol-examples)
    -   [<span data-ttu-id="d07fb-124">4.1 Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="d07fb-124">4.1 Example 1</span></span>](#41-example-1)
    -   [<span data-ttu-id="d07fb-125">4.2 Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="d07fb-125">4.2 Example 2</span></span>](#42-example-2)
-   [<span data-ttu-id="d07fb-126">5 Seguridad</span><span class="sxs-lookup"><span data-stu-id="d07fb-126">5 Security</span></span>](#5-security)
    -   [<span data-ttu-id="d07fb-127">5.1 Consideraciones de seguridad para los implementadores</span><span class="sxs-lookup"><span data-stu-id="d07fb-127">5.1 Security Considerations for Implementers</span></span>](#51-security-considerations-for-implementers)
    -   [<span data-ttu-id="d07fb-128">5.2 Índice de parámetros de seguridad</span><span class="sxs-lookup"><span data-stu-id="d07fb-128">5.2 Index of Security Parameters</span></span>](#52-index-of-security-parameters)
-   [<span data-ttu-id="d07fb-129">6 Índice del comportamiento específico de la versión</span><span class="sxs-lookup"><span data-stu-id="d07fb-129">6 Index of Version Specific Behavior</span></span>](#6-index-of-version-specific-behavior)

<span data-ttu-id="d07fb-130">Este documento es una especificación del Protocolo de servicio de indexación de contenido.</span><span class="sxs-lookup"><span data-stu-id="d07fb-130">This document is a specification of the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="d07fb-131">La documentación del Programa de protocolo de servidor de grupo de trabajo (WSPP) está pensada para usarse junto con la documentación de estándares públicos, el arte de programación de red y los conceptos de sistemas distribuidos del grupo de trabajo de Windows, y supone que el lector está familiarizado con el material mencionado anteriormente o tiene acceso inmediato a él.</span><span class="sxs-lookup"><span data-stu-id="d07fb-131">The Workgroup Server Protocol Program (WSPP) documentation is intended for use in conjunction with public standards documentation, network programming art, and Windows workgroup distributed systems concepts, and assumes that the reader either is familiar with the aforementioned material or has immediate access to it.</span></span>

<span data-ttu-id="d07fb-132">Una especificación del protocolo WSPP no requiere el uso de herramientas de programación o entornos de programación de Microsoft para que un licenciado desarrolle una implementación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-132">A WSPP protocol specification does not require the use of Microsoft programming tools or programming environments in order for a Licensee to develop an implementation.</span></span> <span data-ttu-id="d07fb-133">Los licencias que tienen acceso a entornos y herramientas de programación de Microsoft pueden aprovecharse de ellos de forma gratuita.</span><span class="sxs-lookup"><span data-stu-id="d07fb-133">Licensees who have access to Microsoft programming tools and environments are free to take advantage of them.</span></span>

## <a name="1-introduction"></a><span data-ttu-id="d07fb-134">1 Introducción</span><span class="sxs-lookup"><span data-stu-id="d07fb-134">1 Introduction</span></span>

-   [<span data-ttu-id="d07fb-135">1.1 Glosario</span><span class="sxs-lookup"><span data-stu-id="d07fb-135">1.1 Glossary</span></span>](#11-glossary)
-   [<span data-ttu-id="d07fb-136">1.2 Referencias</span><span class="sxs-lookup"><span data-stu-id="d07fb-136">1.2 References</span></span>](#12-references)
-   [<span data-ttu-id="d07fb-137">Introducción al protocolo 1.3 (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="d07fb-137">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
-   [<span data-ttu-id="d07fb-138">1.4 Relación con otros protocolos</span><span class="sxs-lookup"><span data-stu-id="d07fb-138">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
-   [<span data-ttu-id="d07fb-139">1.5 Requisitos previos y condiciones previas</span><span class="sxs-lookup"><span data-stu-id="d07fb-139">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
-   [<span data-ttu-id="d07fb-140">1.6 Declaración de aplicabilidad</span><span class="sxs-lookup"><span data-stu-id="d07fb-140">1.6 Applicability Statement</span></span>](#16-applicability-statement)
-   [<span data-ttu-id="d07fb-141">1.7 Control de versiones y negociación de funcionalidad</span><span class="sxs-lookup"><span data-stu-id="d07fb-141">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
-   [<span data-ttu-id="d07fb-142">1.8 Campos extensibles por el proveedor</span><span class="sxs-lookup"><span data-stu-id="d07fb-142">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
-   [<span data-ttu-id="d07fb-143">1.9 Asignaciones de estándares</span><span class="sxs-lookup"><span data-stu-id="d07fb-143">1.9 Standards Assignments</span></span>](#19-standards-assignments)

### <a name="11-glossary"></a><span data-ttu-id="d07fb-144">1.1 Glosario</span><span class="sxs-lookup"><span data-stu-id="d07fb-144">1.1 Glossary</span></span>

> [!Note]  
> <span data-ttu-id="d07fb-145">Los términos siguientes se definen en la sección Glosario de \[ MS-SYS \] :</span><span class="sxs-lookup"><span data-stu-id="d07fb-145">The following terms are defined in the Glossary section of \[MS-SYS\]:</span></span>
>
> -   <span data-ttu-id="d07fb-146">GUID</span><span class="sxs-lookup"><span data-stu-id="d07fb-146">GUID</span></span>
> -   <span data-ttu-id="d07fb-147">Little Endian</span><span class="sxs-lookup"><span data-stu-id="d07fb-147">Little Endian</span></span>
> -   <span data-ttu-id="d07fb-148">Canalización con nombre</span><span class="sxs-lookup"><span data-stu-id="d07fb-148">Named Pipe</span></span>
> -   <span data-ttu-id="d07fb-149">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="d07fb-149">Path</span></span>

 

<span data-ttu-id="d07fb-150">**Enlace:** solicitud para incluir una columna determinada **en** un conjunto de **filas devuelto.**</span><span class="sxs-lookup"><span data-stu-id="d07fb-150">**Binding**: A request to include a particular **column** in a returned **rowset** .</span></span> <span data-ttu-id="d07fb-151">El **enlace** especifica una propiedad que se va a incluir en los resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d07fb-151">The **binding** specifies a property to be included in the search results.</span></span>

<span data-ttu-id="d07fb-152">**Marcador:** marcador que identifica de forma única una fila dentro de un conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-152">**Bookmark**: A marker that uniquely identifies a row within a set of rows.</span></span>

<span data-ttu-id="d07fb-153">**Catálogo:** unidad de nivel superior de la organización en el servicio de indexación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-153">**Catalog**: The highest-level unit of organization in the indexing service.</span></span> <span data-ttu-id="d07fb-154">Representa un conjunto de documentos indexados en los que se pueden ejecutar consultas mediante el protocolo content indexing Service.</span><span class="sxs-lookup"><span data-stu-id="d07fb-154">It represents a set of indexed documents against which queries can be executed using the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="d07fb-155">**Categoría:** una agrupación jerárquica de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-155">**Category**: A hierarchical grouping of rows.</span></span> <span data-ttu-id="d07fb-156">Por ejemplo, un resultado de consulta que contiene columnas de autor y título se puede clasificar en función del autor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-156">For example, a query result containing author and title columns can be categorized based on author.</span></span> <span data-ttu-id="d07fb-157">Cada grupo de filas que contiene el mismo valor para author constituiría una categoría.</span><span class="sxs-lookup"><span data-stu-id="d07fb-157">Each group of rows containing the same value for author would constitute a category.</span></span>

<span data-ttu-id="d07fb-158">**Capítulo:** intervalo de **filas dentro** de un conjunto de **filas** .</span><span class="sxs-lookup"><span data-stu-id="d07fb-158">**Chapter** : A range of **rows** within a set of **rows** .</span></span>

<span data-ttu-id="d07fb-159">**Columna**: contenedor de un único tipo de información de una **fila.**</span><span class="sxs-lookup"><span data-stu-id="d07fb-159">**Column**: The container for a single type of information in a **row** .</span></span> <span data-ttu-id="d07fb-160">Las columnas se asignan a nombres de propiedad y  especifican qué propiedades se usan para los elementos del árbol de comandos de la consulta **de** búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d07fb-160">Columns map to property names, and specify which properties are used for the search query's **command** **tree** elements.</span></span>

<span data-ttu-id="d07fb-161">**Árbol de comandos:** combinación de **restricciones,** **categorías** **y** criterios de ordenación especificados para la consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d07fb-161">**Command Tree**: A combination of **restrictions** , **categories** , and **sort orders** specified for the search query.</span></span>

<span data-ttu-id="d07fb-162">**Cursor:** entidad que se usa como mecanismo  para trabajar con  una fila o un pequeño bloque de filas a la vez en un conjunto de datos devuelto en un conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-162">**Cursor**: An entity that is used as a mechanism to work with one **row** or a small block of **rows** at a time in a set of data returned in a result set.</span></span> <span data-ttu-id="d07fb-163">Un **cursor** se coloca en una sola **fila dentro** del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-163">A **cursor** is positioned on a single **row** within the result set.</span></span> <span data-ttu-id="d07fb-164">Una vez **que el cursor** se coloca en una fila, se pueden realizar operaciones en esa fila o en un bloque de filas a partir de esa posición.  </span><span class="sxs-lookup"><span data-stu-id="d07fb-164">After the **cursor** is positioned on a row, operations can be performed on that **row** , or on a block of **rows** starting at that position.</span></span>

<span data-ttu-id="d07fb-165">**Identificador:** token que se puede usar para identificar y acceder a **cursores,** **capítulos** y **marcadores.**</span><span class="sxs-lookup"><span data-stu-id="d07fb-165">**Handle**: A token that can be used to identify and access **cursors** , **chapters** , and **bookmarks** .</span></span>

<span data-ttu-id="d07fb-166">**Índice:** estructura persistente que contiene el contenido de texto que un servicio de indexación extrayó de **los archivos.**</span><span class="sxs-lookup"><span data-stu-id="d07fb-166">**Index**: A persistent structure that contains the text content pulled out of files by an **indexing service** .</span></span> <span data-ttu-id="d07fb-167">Esto incluye la lista de palabras, que se almacenan junto con el nombre de archivo que contiene, la ubicación de la palabra y **la configuración regional.**</span><span class="sxs-lookup"><span data-stu-id="d07fb-167">This includes the list of words, which are stored along with the containing file name, word location, and **locale** .</span></span>

<span data-ttu-id="d07fb-168">**Indexación:** proceso de extracción de texto y propiedades de archivos y almacenamiento de los valores extraídos en los índices **(para** texto) y la caché de propiedades **(para** propiedades).</span><span class="sxs-lookup"><span data-stu-id="d07fb-168">**Indexing**: The process of extracting text and properties from files and storing the extracted values into the **indexes** (for text), and the **property cache** (for properties).</span></span>

<span data-ttu-id="d07fb-169">**Servicio de indexación:** servicio que crea **catálogos indexados** para el contenido y las propiedades de los sistemas de archivos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-169">**Indexing Service**: A service that creates indexed **catalogs** for the contents and properties of file systems.</span></span> <span data-ttu-id="d07fb-170">Las aplicaciones pueden buscar en los catálogos información de los archivos del sistema de archivos indexado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-170">Applications can search the catalogs for information from the files on the indexed file system.</span></span>

<span data-ttu-id="d07fb-171">**Configuración regional:** identificador, como se especifica en el Apéndice A de MS-GPSI, que especifica las \[ \] preferencias relacionadas con el idioma.</span><span class="sxs-lookup"><span data-stu-id="d07fb-171">**Locale**: An identifier, as specified in \[MS-GPSI\] Appendix A, that specifies preferences related to language.</span></span> <span data-ttu-id="d07fb-172">Estas preferencias indican cómo se va a dar formato a las fechas y horas, los elementos se ordenan alfabéticamente, las cadenas se comparan, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-172">These preferences indicate how dates and times are to be formatted, items are to be sorted alphabetically, strings are to be compared, and so on.</span></span>

<span data-ttu-id="d07fb-173">**Consulta en lenguaje natural:** consulta construida con lenguaje humano en lugar de sintaxis de consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-173">**Natural Language Query**: A query constructed using human language instead of query syntax.</span></span>

<span data-ttu-id="d07fb-174">**Palabra ruido:** palabra que el servicio de indexación omite cuando está presente en las **restricciones especificadas** para la consulta de búsqueda porque tiene poco valor discriminador.</span><span class="sxs-lookup"><span data-stu-id="d07fb-174">**Noise word**: A word that is ignored by the indexing service when present in the **restrictions** specified for the search query because it has little discriminatory value.</span></span> <span data-ttu-id="d07fb-175">Entre los ejemplos en inglés se incluyen "a", "and" y "the".</span><span class="sxs-lookup"><span data-stu-id="d07fb-175">English examples include "a", "and" and "the".</span></span>

<span data-ttu-id="d07fb-176">**Caché de propiedades:** caché de propiedades de archivo extraídas por un **servicio de indexación.**</span><span class="sxs-lookup"><span data-stu-id="d07fb-176">**Property Cache**: A cache of file properties extracted by an **indexing service** .</span></span>

<span data-ttu-id="d07fb-177">**Indexación de propiedades:** proceso  de  creación de un índice de propiedades de tipo de valor de un documento, incluidos el autor, el asunto, el tipo, el recuento de palabras, el recuento de páginas impresas y cualquier otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-177">**Property Indexing**: The process of creating an **index** of **value-type properties** of a document, including author, subject, type, word count, printed page count, and any other properties.</span></span>

<span data-ttu-id="d07fb-178">**Restricción:** conjunto de condiciones que un archivo debe cumplir para incluirse en los resultados de búsqueda devueltos por el **servicio de indexación** en respuesta a una consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d07fb-178">**Restriction**: A set of conditions that a file must meet to be included in the search results returned by the **indexing service** in response to a search query.</span></span> <span data-ttu-id="d07fb-179">Una **restricción** limita el foco de una consulta de búsqueda, limitando los archivos que el servicio de **indexación** incluirá en los resultados de la búsqueda a solo aquellos que coincidan con las condiciones.</span><span class="sxs-lookup"><span data-stu-id="d07fb-179">A **restriction** narrows the focus of a search query, limiting the files that the **indexing service** will include in the search results to only those that match the conditions.</span></span>

<span data-ttu-id="d07fb-180">**Fila:** colección de columnas **que** contiene los valores de propiedad que describen un único archivo del conjunto de archivos que coincidieron con las **restricciones especificadas** en la consulta de búsqueda enviada al servicio **de indexación** .</span><span class="sxs-lookup"><span data-stu-id="d07fb-180">**Row**: The collection of **columns** , containing the property values that describe a single file from the set of files that matched the **restrictions** specified in the search query submitted to the **indexing service** .</span></span>

<span data-ttu-id="d07fb-181">**Conjunto de filas:** conjunto de **filas devuelto en** los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d07fb-181">**Rowset**: A set of **rows** returned in the search results.</span></span>

<span data-ttu-id="d07fb-182">**Criterio de** ordenación: el conjunto de reglas de una consulta de búsqueda que definen el orden de las filas en el resultado de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d07fb-182">**Sort Order**: The set of rules in a search query that define the ordering of rows in the search result.</span></span> <span data-ttu-id="d07fb-183">Cada regla consta de una propiedad (nombre, tamaño, etc.) y una dirección para la ordenación (ascendente o descendente).</span><span class="sxs-lookup"><span data-stu-id="d07fb-183">Each rule consists of a property (name, size, etc.) and a direction for the ordering (ascending or descending).</span></span> <span data-ttu-id="d07fb-184">Varias reglas se aplican secuencialmente</span><span class="sxs-lookup"><span data-stu-id="d07fb-184">Multiple rules are applied sequentially</span></span>

<span data-ttu-id="d07fb-185">**Propiedad de tipo de texto:** propiedad que describe el contenido de un documento y solo tiene texto sin formato asociado a su nombre.</span><span class="sxs-lookup"><span data-stu-id="d07fb-185">**Text-type Property**: A property that describes the content of a document and has only unformatted text associated with its name.</span></span>

<span data-ttu-id="d07fb-186">**Propiedad de tipo de valor:** propiedad que describe un único atributo de un documento completo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-186">**Value-type Property**: A property that describes a single attribute of an entire document.</span></span> <span data-ttu-id="d07fb-187">Una propiedad de tipo de valor tiene un identificador de tipo de datos y un valor de ese tipo de datos asociado a su nombre.</span><span class="sxs-lookup"><span data-stu-id="d07fb-187">A value-type property has a data type ID and a value of that data type associated with its name.</span></span>

<span data-ttu-id="d07fb-188">**Raíz virtual:** ruta de acceso alternativa a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-188">**Virtual Root**: An alternate path to a folder.</span></span> <span data-ttu-id="d07fb-189">Una carpeta física puede tener cero o más raíces virtuales.</span><span class="sxs-lookup"><span data-stu-id="d07fb-189">A physical folder can have zero or more virtual roots.</span></span> <span data-ttu-id="d07fb-190">Las rutas de acceso que comienzan por una raíz virtual se denominan rutas de acceso virtuales.</span><span class="sxs-lookup"><span data-stu-id="d07fb-190">Paths beginning with a virtual root are called virtual paths.</span></span> <span data-ttu-id="d07fb-191">Por ejemplo, /server/vanityroot podría ser una raíz virtual de C: \\ carpeta \\ web de \\ IIS1.</span><span class="sxs-lookup"><span data-stu-id="d07fb-191">For example, /server/vanityroot might be a virtual root of C:\\IIS\\web\\folder1.</span></span> <span data-ttu-id="d07fb-192">A continuación, el archivo C: carpeta web de IIS1default.htm una ruta de acceso \\ \\ virtual de \\ \\ /server/vanityroot/default.htm.</span><span class="sxs-lookup"><span data-stu-id="d07fb-192">Then the file C:\\IIS\\web\\folder1\\default.htm would have a virtual path of /server/vanityroot/default.htm.</span></span>

<span data-ttu-id="d07fb-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT:** estos términos (en todos los límites) se usan como se describe en \[ RFC2119 \] .</span><span class="sxs-lookup"><span data-stu-id="d07fb-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT**: These terms (in all caps) are used as described in \[RFC2119\].</span></span> <span data-ttu-id="d07fb-194">Todas las instrucciones de comportamiento opcional utilizan MAY, SHOULD o SHOULD NOT.</span><span class="sxs-lookup"><span data-stu-id="d07fb-194">All statements of optional behavior use either MAY, SHOULD, or SHOULD NOT.</span></span>

### <a name="12-references"></a><span data-ttu-id="d07fb-195">1.2 Referencias</span><span class="sxs-lookup"><span data-stu-id="d07fb-195">1.2 References</span></span>

### <a name="121-normative-references"></a><span data-ttu-id="d07fb-196">1.2.1 Referencias de normativa</span><span class="sxs-lookup"><span data-stu-id="d07fb-196">1.2.1 Normative References</span></span>

<span data-ttu-id="d07fb-197">\[IEEE754 \] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, octubre de 1985, https://standards.ieee.org/standard/754-1985.html</span><span class="sxs-lookup"><span data-stu-id="d07fb-197">\[IEEE754\] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span></span>

<span data-ttu-id="d07fb-198">\[MS-DCOM \] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", junio de 2006.</span><span class="sxs-lookup"><span data-stu-id="d07fb-198">\[MS-DCOM\] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", June 2006.</span></span>

<span data-ttu-id="d07fb-199">\[MS-GPSI \] Microsoft Corporation, "Directiva de grupo de Instalación de software Extension", junio de 2006.</span><span class="sxs-lookup"><span data-stu-id="d07fb-199">\[MS-GPSI\] Microsoft Corporation, "Group Policy Software Installation Extension", June 2006.</span></span>

<span data-ttu-id="d07fb-200">\[MS-SMB \] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions", mayo de 2006.</span><span class="sxs-lookup"><span data-stu-id="d07fb-200">\[MS-SMB\] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions," May 2006.</span></span>

<span data-ttu-id="d07fb-201">\[MS-SYS \] Microsoft Corporation, "System Overview v4", julio de 2006.</span><span class="sxs-lookup"><span data-stu-id="d07fb-201">\[MS-SYS\] Microsoft Corporation, "System Overview v4", July 2006.</span></span>

<span data-ttu-id="d07fb-202">\[SALTON \] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span><span class="sxs-lookup"><span data-stu-id="d07fb-202">\[SALTON\] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span></span>

<span data-ttu-id="d07fb-203">\[UNICODE \] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span><span class="sxs-lookup"><span data-stu-id="d07fb-203">\[UNICODE\] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span></span>

### <a name="122-informative-references"></a><span data-ttu-id="d07fb-204">1.2.2 Referencias informativas</span><span class="sxs-lookup"><span data-stu-id="d07fb-204">1.2.2 Informative References</span></span>

<span data-ttu-id="d07fb-205">\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .</span><span class="sxs-lookup"><span data-stu-id="d07fb-205">\[MSDN-OLEDB\] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp.</span></span>

<span data-ttu-id="d07fb-206">\[MSDN-QUERYERR \] Microsoft Corporation, Query-Execution, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span><span class="sxs-lookup"><span data-stu-id="d07fb-206">\[MSDN-QUERYERR\] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span></span>

### <a name="13-protocol-overview-synopsis"></a><span data-ttu-id="d07fb-207">Introducción al protocolo 1.3 (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="d07fb-207">1.3 Protocol Overview (Synopsis)</span></span>

<span data-ttu-id="d07fb-208">Un servicio **de indexación de contenido** ayuda a organizar de forma eficaz las características extraídas de una colección de documentos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-208">A content **indexing service** helps efficiently organize the extracted features of a collection of documents.</span></span> <span data-ttu-id="d07fb-209">El Protocolo de servicio de indexación de contenido (CISP) permite a un cliente comunicarse con un servidor que hospeda un servicio de indexación para emitir consultas y permitir que un administrador administre el servidor de indexación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-209">The Content Indexing Service Protocol (CISP) allows a client to communicate with a server hosting an indexing service to issue queries and to allow an administrator to manage the indexing server.</span></span>

<span data-ttu-id="d07fb-210">Al procesar archivos, un servicio de indexación analiza un conjunto de documentos  y reorganiza su contenido de forma que las propiedades de esos documentos se puedan devolver de forma eficaz en respuesta a las consultas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-210">When processing files, an indexing service analyzes a set of documents and reorganizes their content in such a way that **properties** of those documents can be efficiently returned in response to queries.</span></span> <span data-ttu-id="d07fb-211">Una colección de documentos que se pueden consultar consta de un **catálogo .**</span><span class="sxs-lookup"><span data-stu-id="d07fb-211">A collection of documents that can be queried comprises a **catalog** .</span></span> <span data-ttu-id="d07fb-212">Un catálogo puede contener un **índice (para** referencia rápida al texto) y una caché de **propiedades** (para la recuperación rápida de valores de propiedad).</span><span class="sxs-lookup"><span data-stu-id="d07fb-212">A catalog may contain an **index** (for quick reference to text) and a **property cache** (for quick retrieval of property values).</span></span>

<span data-ttu-id="d07fb-213">Conceptualmente, un catálogo consta de una "tabla" lógica de propiedades con el texto o el valor y la configuración regional correspondiente almacenada en **columnas** de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d07fb-213">Conceptually, a catalog consists of a logical "table" of properties with the text or value and corresponding locale stored in **columns** of the table.</span></span> <span data-ttu-id="d07fb-214">Cada "fila" de la tabla corresponde a un documento independiente en el ámbito del catálogo y cada "columna" de la tabla corresponde a una propiedad .</span><span class="sxs-lookup"><span data-stu-id="d07fb-214">Each "row" of the table corresponds to a separate document in the scope of the catalog and each "column" of the table corresponds to a property.</span></span>

<span data-ttu-id="d07fb-215">Las tareas específicas realizadas por CISP se agrupan en dos áreas funcionales:</span><span class="sxs-lookup"><span data-stu-id="d07fb-215">The specific tasks performed by CISP are grouped into two functional areas:</span></span>

-   <span data-ttu-id="d07fb-216">Administración remota de catálogos de servicios de indexación,</span><span class="sxs-lookup"><span data-stu-id="d07fb-216">Remote administration of indexing service catalogs,</span></span>
-   <span data-ttu-id="d07fb-217">Consulta remota de catálogos de servicios de indexación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-217">Remote querying of indexing service catalogs.</span></span>

### <a name="131-remote-administration-tasks"></a><span data-ttu-id="d07fb-218">1.3.1 Tareas de administración remota</span><span class="sxs-lookup"><span data-stu-id="d07fb-218">1.3.1 Remote Administration Tasks</span></span>

<span data-ttu-id="d07fb-219">CISP habilita las siguientes tareas de administración del catálogo de servicios de indexación desde un cliente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-219">CISP enables the following indexing service catalog management tasks from a client:</span></span>

-   <span data-ttu-id="d07fb-220">Consulte el estado actual de un catálogo de servicios de indexación en el servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-220">Query the current state of an indexing service catalog on the server.</span></span>
-   <span data-ttu-id="d07fb-221">Actualice el estado de un catálogo de servicios de indexación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-221">Update the state of an indexing service catalog.</span></span>
-   <span data-ttu-id="d07fb-222">Inicie el proceso de indexación para un conjunto determinado de archivos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-222">Launch the indexing process for a particular set of files.</span></span>
-   <span data-ttu-id="d07fb-223">Inicie la optimización de un índice para mejorar el rendimiento de las consultas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-223">Initiate optimization of an index in order to improve query performance.</span></span>

<span data-ttu-id="d07fb-224">Todas las tareas de administración remota siguen un modelo sencillo de solicitud/respuesta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-224">All remote administration tasks follow a simple request/response model.</span></span> <span data-ttu-id="d07fb-225">No se mantiene ningún estado en el cliente para ninguna llamada de administración y se pueden realizar llamadas administrativas en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="d07fb-225">No state is maintained on the client for any administration call and administrative calls can be made in any order.</span></span>

### <a name="132-remote-querying"></a><span data-ttu-id="d07fb-226">1.3.2 Consulta remota</span><span class="sxs-lookup"><span data-stu-id="d07fb-226">1.3.2 Remote Querying</span></span>

<span data-ttu-id="d07fb-227">CISP permite a los clientes realizar consultas de búsqueda en un servidor remoto que hospeda un servicio de indexación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-227">CISP enables clients to perform search queries against a remote server hosting an indexing service.</span></span>

<span data-ttu-id="d07fb-228">El envío de una consulta de búsqueda es un proceso de varios pasos iniciado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-228">Sending a search query is a multi-step process initiated by the client.</span></span> <span data-ttu-id="d07fb-229">Los pasos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d07fb-229">The steps are as follows:</span></span>

1.  <span data-ttu-id="d07fb-230">El cliente solicita una conexión a un servidor que hospeda un servicio de indexación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-230">The client requests a connection to a server hosting an indexing service.</span></span>
2.  <span data-ttu-id="d07fb-231">El cliente envía los parámetros para la consulta de búsqueda, que incluyen:</span><span class="sxs-lookup"><span data-stu-id="d07fb-231">The client sends the parameters for the search query, which include:</span></span>
    -   <span data-ttu-id="d07fb-232">Restricciones para especificar qué documentos se van a incluir o excluir de los **resultados** de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d07fb-232">The **restrictions** to specify which documents are to be included and/or excluded from the search results.</span></span>
    -   <span data-ttu-id="d07fb-233">Orden en el que se van a devolver los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d07fb-233">The order in which the search results are to be returned.</span></span>
    -   <span data-ttu-id="d07fb-234">Columnas que se devolverán en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-234">The columns to be returned in the result set.</span></span>
    -   <span data-ttu-id="d07fb-235">Número máximo de **filas que** se deben devolver para la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-235">The maximum number of **rows** that should be returned for the query.</span></span>
    -   <span data-ttu-id="d07fb-236">Tiempo máximo para la ejecución de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-236">The maximum time for query execution.</span></span>

        <span data-ttu-id="d07fb-237">Una vez que el servidor ha reconocido la solicitud del cliente para iniciar la consulta, el cliente puede solicitar información de estado sobre la consulta, pero este no es un paso necesario.</span><span class="sxs-lookup"><span data-stu-id="d07fb-237">Once the server has acknowledged the client's request to initiate the query, the client can request status information about the query, but this is not a required step.</span></span>

3.  <span data-ttu-id="d07fb-238">A continuación, el cliente especifica qué propiedades debe incluir el servidor en los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d07fb-238">The client then specifies which properties the server should include in the search results.</span></span>
4.  <span data-ttu-id="d07fb-239">El cliente solicita un conjunto de resultados del servidor y el servidor responde enviando al cliente los valores de propiedad de los archivos incluidos en los resultados de la consulta de búsqueda del cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-239">The client requests a result set from the server, and the server responds by sending the client the property values for files that were included in the results for the client's search query.</span></span> <span data-ttu-id="d07fb-240">Si el valor de una propiedad es demasiado grande para caber en un búfer de respuesta único, el servidor no enviará la propiedad, sino que establecerá el estado de la propiedad en diferido.</span><span class="sxs-lookup"><span data-stu-id="d07fb-240">If the value of a property is too large to fit in a single response buffer the server will not send the property but instead will set the property status to deferred.</span></span> <span data-ttu-id="d07fb-241">A continuación, el cliente solicita el valor de propiedad por separado mediante una serie de solicitudes para fragmentos sucesivos del valor y, a continuación, reanuda la solicitud de otros valores.</span><span class="sxs-lookup"><span data-stu-id="d07fb-241">The client then requests the property value separately using a series of requests for successive chunks of the value, and then resumes requesting other values.</span></span>
5.  <span data-ttu-id="d07fb-242">Una vez que el cliente ha terminado con la consulta de búsqueda y ya no requiere resultados adicionales, el cliente se pone en contacto con el servidor para liberar la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-242">Once the client is finished with the search query and no longer requires additional results, the client contacts the server to release the query.</span></span>
6.  <span data-ttu-id="d07fb-243">Una vez que el servidor ha publicado la consulta, el cliente puede enviar una solicitud para desconectarse del servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-243">Once the server has released the query, the client may send a request to disconnect from the server.</span></span> <span data-ttu-id="d07fb-244">A continuación, se cierra la conexión.</span><span class="sxs-lookup"><span data-stu-id="d07fb-244">The connection is then closed.</span></span> <span data-ttu-id="d07fb-245">Como alternativa, el cliente puede emitir otra consulta y repetir la secuencia del paso 2.</span><span class="sxs-lookup"><span data-stu-id="d07fb-245">Alternatively, the client may issue another query and repeat the sequence from the step 2.</span></span>

<span data-ttu-id="d07fb-246">Comportamiento de Windows: este protocolo se implementa en Windows 2000, Windows XP, Windows Server 2003 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d07fb-246">Windows Behavior: This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span>

### <a name="14-relationship-to-other-protocols"></a><span data-ttu-id="d07fb-247">1.4 Relación con otros protocolos</span><span class="sxs-lookup"><span data-stu-id="d07fb-247">1.4 Relationship to Other Protocols</span></span>

<span data-ttu-id="d07fb-248">CISP se basa en el protocolo \[ SMB MS-SMB \] para el transporte de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-248">The CISP relies on the SMB \[MS-SMB\] protocol for message transport.</span></span> <span data-ttu-id="d07fb-249">Ningún otro protocolo depende directamente del protocolo del servicio de indexación de contenido.</span><span class="sxs-lookup"><span data-stu-id="d07fb-249">No other protocol depends directly on the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="d07fb-250">*Comportamiento de Windows: las aplicaciones suelen interactuar con un contenedor de interfaz OLE DB \[ MSDN-OLEDB (por ejemplo, un cliente de protocolo) y no \] directamente con el protocolo.*</span><span class="sxs-lookup"><span data-stu-id="d07fb-250">*Windows Behavior: Applications typically interact with an OLE DB interface wrapper \[MSDN-OLEDB\] (e.g., a protocol client) and not directly with the protocol.*</span></span>

### <a name="15-prerequisites-and-preconditions"></a><span data-ttu-id="d07fb-251">1.5 Requisitos previos y condiciones previas</span><span class="sxs-lookup"><span data-stu-id="d07fb-251">1.5 Prerequisites and Preconditions</span></span>

<span data-ttu-id="d07fb-252">Se supone que el cliente ha obtenido el nombre del servidor y un nombre de catálogo antes de invocar este protocolo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-252">It is assumed that the client has obtained the name of the server and a catalog name before this protocol is invoked.</span></span> <span data-ttu-id="d07fb-253">La forma en que un cliente lo hace está fuera del ámbito de esta especificación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-253">How a client does this is outside of the scope of this specification.</span></span>

<span data-ttu-id="d07fb-254">También se supone que el cliente y el servidor tienen una asociación de seguridad que se puede usar con canalizaciones \[ con nombre MS-SMB. \]</span><span class="sxs-lookup"><span data-stu-id="d07fb-254">It is also assumed that the client and server have a security association usable with named pipes \[MS-SMB\].</span></span>

### <a name="16-applicability-statement"></a><span data-ttu-id="d07fb-255">1.6 Declaración de aplicabilidad</span><span class="sxs-lookup"><span data-stu-id="d07fb-255">1.6 Applicability Statement</span></span>

<span data-ttu-id="d07fb-256">CISP está diseñado para consultar y administrar catálogos en un servidor remoto desde un cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-256">CISP is designed for querying and managing catalogs on a remote server from a client.</span></span> <span data-ttu-id="d07fb-257">CISP está en desuso en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d07fb-257">CISP is deprecated on Windows Vista.</span></span>

### <a name="17-versioning-and-capability-negotiation"></a><span data-ttu-id="d07fb-258">1.7 Control de versiones y negociación de funcionalidad</span><span class="sxs-lookup"><span data-stu-id="d07fb-258">1.7 Versioning and Capability Negotiation</span></span>

<span data-ttu-id="d07fb-259">Este protocolo no tiene mecanismos de control de versiones ni de negociación de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="d07fb-259">This protocol has no versioning or capability negotiation mechanisms.</span></span>

### <a name="18-vendor-extensible-fields"></a><span data-ttu-id="d07fb-260">1.8 Campos extensibles por el proveedor</span><span class="sxs-lookup"><span data-stu-id="d07fb-260">1.8 Vendor-Extensible Fields</span></span>

<span data-ttu-id="d07fb-261">Este protocolo usa HULT que son extensibles por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-261">This protocol uses HRESULTs which are vendor-extensible.</span></span> <span data-ttu-id="d07fb-262">Los proveedores pueden elegir sus propios valores para este campo, siempre que el bit C (0x20000000) se establezca como se especifica en la sección 4.1.1 de MS-SYS, lo que indica que es un código de \[ \] cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-262">Vendors are free to choose their own values for this field, as long as the C bit (0x20000000) is set as specified in Section 4.1.1 of \[MS-SYS\], indicating it is a customer code.</span></span>

<span data-ttu-id="d07fb-263">Este protocolo también usa valores NTSTATUS tomados del espacio numérico NTSTATUS definido en \[ MS-SYS \] .</span><span class="sxs-lookup"><span data-stu-id="d07fb-263">This protocol also uses NTSTATUS values taken from the NTSTATUS number space defined in \[MS-SYS\].</span></span> <span data-ttu-id="d07fb-264">Los proveedores DEBEN reutilizar esos valores con su significado indicado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-264">Vendors SHOULD reuse those values with their indicated meaning.</span></span> <span data-ttu-id="d07fb-265">La elección de cualquier otro valor corre el riesgo de colisión en el futuro.</span><span class="sxs-lookup"><span data-stu-id="d07fb-265">Choosing any other value runs the risk of a collision in the future.</span></span>

<span data-ttu-id="d07fb-266">*Comportamiento de Windows: Windows solo usa los valores especificados en la sección 4.1.3 \[ de MS-SYS. \]*</span><span class="sxs-lookup"><span data-stu-id="d07fb-266">*Windows Behavior: Windows only uses the values specified in Section 4.1.3 of \[MS-SYS\].*</span></span>

### <a name="181-property-ids"></a><span data-ttu-id="d07fb-267">1.8.1 IDs de propiedad</span><span class="sxs-lookup"><span data-stu-id="d07fb-267">1.8.1 Property IDs</span></span>

<span data-ttu-id="d07fb-268">Las propiedades se representan mediante los ID conocidos como los de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-268">Properties are represented by IDs known as Property IDs.</span></span> <span data-ttu-id="d07fb-269">Cada propiedad debe tener un identificador único global.</span><span class="sxs-lookup"><span data-stu-id="d07fb-269">Each property must have a globally unique identifier.</span></span> <span data-ttu-id="d07fb-270">Este identificador consta de un **GUID** que representa una colección de propiedades denominada conjunto de propiedades más una cadena o un entero de 32 bits para identificar la propiedad dentro del conjunto.</span><span class="sxs-lookup"><span data-stu-id="d07fb-270">This identifier consists of a **GUID** representing a collection of properties called a property set plus either a string or 32-bit integer to identify the property within the set.</span></span> <span data-ttu-id="d07fb-271">Si se usa el formato entero de id., los valores 0x00000000, 0xFFFFFFFF y 0xFFFFFFFE se consideran no válidos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-271">If the integer form of ID is used, then the values 0x00000000, 0xFFFFFFFF and 0xFFFFFFFE are considered invalid.</span></span>

<span data-ttu-id="d07fb-272">Los proveedores pueden garantizar que sus propiedades se definen de forma única al colocarlas en un conjunto de propiedades definido por su propio GUID.</span><span class="sxs-lookup"><span data-stu-id="d07fb-272">Vendors can guarantee their properties are uniquely defined by placing them in a property set defined by their own GUID.</span></span>

### <a name="19-standards-assignments"></a><span data-ttu-id="d07fb-273">1.9 Asignaciones de estándares</span><span class="sxs-lookup"><span data-stu-id="d07fb-273">1.9 Standards Assignments</span></span>

<span data-ttu-id="d07fb-274">Este protocolo no tiene asignaciones de estándares, solo asignaciones privadas realizadas por Microsoft mediante procedimientos de asignación especificados en otros protocolos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-274">This protocol has no standards assignments, only private assignments made by Microsoft using allocation procedures specified in other protocols.</span></span>

<span data-ttu-id="d07fb-275">Microsoft ha asignado a este protocolo una canalización con nombre como se especifica en \[ MS-SMB. \]</span><span class="sxs-lookup"><span data-stu-id="d07fb-275">Microsoft has allocated this protocol a named pipe as specified in \[MS-SMB\].</span></span> <span data-ttu-id="d07fb-276">La asignación es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-276">The assignment is:</span></span>



| <span data-ttu-id="d07fb-277">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d07fb-277">Parameter</span></span> | <span data-ttu-id="d07fb-278">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-278">Value</span></span>             | <span data-ttu-id="d07fb-279">Referencia</span><span class="sxs-lookup"><span data-stu-id="d07fb-279">Reference</span></span>  |
|-----------|-------------------|------------|
| <span data-ttu-id="d07fb-280">Nombre de canalización</span><span class="sxs-lookup"><span data-stu-id="d07fb-280">Pipe name</span></span> | <span data-ttu-id="d07fb-281">\\pipe \\ CI \_ PIPEDS</span><span class="sxs-lookup"><span data-stu-id="d07fb-281">\\pipe\\CI\_SKADS</span></span> | <span data-ttu-id="d07fb-282">\[MS-SMB\]</span><span class="sxs-lookup"><span data-stu-id="d07fb-282">\[MS-SMB\]</span></span> |



 

## <a name="2-messages"></a><span data-ttu-id="d07fb-283">2 Mensajes</span><span class="sxs-lookup"><span data-stu-id="d07fb-283">2 Messages</span></span>

-   [<span data-ttu-id="d07fb-284">2.1 Transporte</span><span class="sxs-lookup"><span data-stu-id="d07fb-284">2.1 Transport</span></span>](#21-transport)
-   [<span data-ttu-id="d07fb-285">2.2 Sintaxis de mensajes</span><span class="sxs-lookup"><span data-stu-id="d07fb-285">2.2 Message Syntax</span></span>](#22-message-syntax)

### <a name="21-transport"></a><span data-ttu-id="d07fb-286">2.1 Transporte</span><span class="sxs-lookup"><span data-stu-id="d07fb-286">2.1 Transport</span></span>

<span data-ttu-id="d07fb-287">Todos los mensajes DEBEN transportarse mediante una canalización con nombre, como se especifica en \[ MS-SMB. \]</span><span class="sxs-lookup"><span data-stu-id="d07fb-287">All messages MUST be transported using a named pipe, as specified in \[MS-SMB\].</span></span> <span data-ttu-id="d07fb-288">Se usa el siguiente nombre de canalización:</span><span class="sxs-lookup"><span data-stu-id="d07fb-288">The following pipe name is used:</span></span>

-   <span data-ttu-id="d07fb-289">\\pipe \\ CI \_ PIPEDS</span><span class="sxs-lookup"><span data-stu-id="d07fb-289">\\pipe\\CI\_SKADS</span></span>

<span data-ttu-id="d07fb-290">Este protocolo usa el protocolo de canalización con nombre SMB subyacente para recuperar la identidad del autor de la llamada que realizó la conexión como se especifica en la sección 2.2.8 de MS-SMB; el cliente DEBE establecer SECURITY IDENTIFICATION como \[ \] ImpersonationLevel en la solicitud para abrir la canalización con \_ nombre.</span><span class="sxs-lookup"><span data-stu-id="d07fb-290">This protocol uses the underlying SMB named pipe protocol to retrieve the identity of the caller that made the connection as specified in Section 2.2.8 of \[MS-SMB\]; the client MUST set SECURITY\_IDENTIFICATION as the ImpersonationLevel in the request to open the named pipe.</span></span>

### <a name="22-message-syntax"></a><span data-ttu-id="d07fb-291">2.2 Sintaxis de mensajes</span><span class="sxs-lookup"><span data-stu-id="d07fb-291">2.2 Message Syntax</span></span>

<span data-ttu-id="d07fb-292">Varias estructuras y mensajes de las secciones siguientes hacen referencia a los identificadores de capítulo o marcador.</span><span class="sxs-lookup"><span data-stu-id="d07fb-292">Several structures and messages in the following sections refer to chapter or bookmark handles.</span></span> <span data-ttu-id="d07fb-293">Un identificador es una estructura opaca de 32 bits de longitud que identifica de forma única un capítulo o marcador.</span><span class="sxs-lookup"><span data-stu-id="d07fb-293">A handle is a 32-bit long opaque structure which uniquely identifies a chapter or bookmark.</span></span> <span data-ttu-id="d07fb-294">Normalmente, las aplicaciones cliente reciben valores de identificador a través de llamadas a métodos; sin embargo, hay varios valores conocidos que no se deben obtener de un servidor, cuyo significado se especifica en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-294">Typically, client applications receive handle values via method calls; however there are several well known values which need not be obtained from a server, the meaning of which is specified in the following table:</span></span>



| <span data-ttu-id="d07fb-295">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-295">Value</span></span>                         | <span data-ttu-id="d07fb-296">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-296">Meaning</span></span>                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-297">Db \_ NULL \_ HCHAPTER 0x00000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-297">DB\_NULL\_HCHAPTER 0x00000000</span></span> | <span data-ttu-id="d07fb-298">Identificador de capítulo para el conjunto de filas sin cadena, que contiene todos los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-298">A chapter handle to the unchaptered rowset, containing all query results.</span></span>    |
| <span data-ttu-id="d07fb-299">DBBMK \_ FIRST 0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-299">DBBMK\_FIRST 0x00000001</span></span>       | <span data-ttu-id="d07fb-300">Identificador de marcador para un marcador que identifica la primera fila del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-300">A bookmark handle to a bookmark that identifies the first row in the rowset.</span></span> |
| <span data-ttu-id="d07fb-301">DBBMK \_ LAST 0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-301">DBBMK\_LAST 0x00000002</span></span>        | <span data-ttu-id="d07fb-302">Identificador de marcador de un marcador que identifica la última fila del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-302">A bookmark handle to a bookmark that identifies the last row in the rowset.</span></span>  |



 

### <a name="221-structures"></a><span data-ttu-id="d07fb-303">2.2.1 Estructuras</span><span class="sxs-lookup"><span data-stu-id="d07fb-303">2.2.1 Structures</span></span>

<span data-ttu-id="d07fb-304">En esta sección se detallan las estructuras de datos definidas y usadas por CISP.</span><span class="sxs-lookup"><span data-stu-id="d07fb-304">This section details data structures that are defined and used by CISP.</span></span>

<span data-ttu-id="d07fb-305">Todos los enteros de 2, 4 y 8 bytes con signo y sin signo de las estructuras siguientes DEBEN transferirse en orden de bytes little-endian.</span><span class="sxs-lookup"><span data-stu-id="d07fb-305">All 2-, 4- and 8-byte signed and unsigned integers in the following structures MUST be transferred in little-endian byte order.</span></span>

<span data-ttu-id="d07fb-306">En la tabla siguiente se resumen las estructuras de datos definidas en esta sección.</span><span class="sxs-lookup"><span data-stu-id="d07fb-306">The following table summarizes the data structures defined in this section.</span></span>



| <span data-ttu-id="d07fb-307">Estructura</span><span class="sxs-lookup"><span data-stu-id="d07fb-307">Structure</span></span>                    | <span data-ttu-id="d07fb-308">Descripción</span><span class="sxs-lookup"><span data-stu-id="d07fb-308">Description</span></span>                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-309">CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="d07fb-309">CBaseStorageVariant</span></span>          | <span data-ttu-id="d07fb-310">Contiene el valor en el que se va a realizar una operación de coincidencia para una propiedad especificada en una estructura CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="d07fb-310">Contains the value on which to perform a match operation for a property specified in a CPropertyRestriction structure.</span></span> |
| <span data-ttu-id="d07fb-311">SAFEARRAY, SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="d07fb-311">SAFEARRAY, SAFEARRAY2</span></span>        | <span data-ttu-id="d07fb-312">Contiene una matriz multidimensional.</span><span class="sxs-lookup"><span data-stu-id="d07fb-312">Contains a multidimensional array.</span></span>                                                                                     |
| <span data-ttu-id="d07fb-313">SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="d07fb-313">SAFEARRAYBOUND</span></span>               | <span data-ttu-id="d07fb-314">Representa los límites de una dimensión de una matriz especificada en una estructura SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="d07fb-314">Represents the bounds for a dimension of an array specified in a SAFEARRAY structure.</span></span>                                  |
| <span data-ttu-id="d07fb-315">CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="d07fb-315">CFullPropSpec</span></span>                | <span data-ttu-id="d07fb-316">Contiene una especificación de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-316">Contains a property specification.</span></span>                                                                                     |
| <span data-ttu-id="d07fb-317">CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-317">CContentRestriction</span></span>          | <span data-ttu-id="d07fb-318">Contiene una cadena que debe coincidir con un valor de propiedad en la caché de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d07fb-318">Contains a string to match for a property value in the property cache.</span></span>                                                 |
| <span data-ttu-id="d07fb-319">CKey</span><span class="sxs-lookup"><span data-stu-id="d07fb-319">CKey</span></span>                         | <span data-ttu-id="d07fb-320">Contiene un valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-320">Contains a property value.</span></span>                                                                                             |
| <span data-ttu-id="d07fb-321">CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-321">CInternalPropertyRestriction</span></span> | <span data-ttu-id="d07fb-322">Contiene un valor de propiedad que debe coincidir con una operación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-322">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="d07fb-323">CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-323">CNatLanguageRestriction</span></span>      | <span data-ttu-id="d07fb-324">Contiene una coincidencia de consulta de lenguaje natural para una propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-324">Contains a natural language query match for a property.</span></span>                                                                |
| <span data-ttu-id="d07fb-325">CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-325">CNodeRestriction</span></span>             | <span data-ttu-id="d07fb-326">Contiene una matriz de nodos de árbol de comandos que especifican las restricciones de una consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-326">Contains an array of command tree nodes specifying the restrictions for a query.</span></span>                                       |
| <span data-ttu-id="d07fb-327">COccRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-327">COccRestriction</span></span>              | <span data-ttu-id="d07fb-328">Contiene la ubicación de una palabra en una frase.</span><span class="sxs-lookup"><span data-stu-id="d07fb-328">Contains the location of a word in a phrase.</span></span>                                                                           |
| <span data-ttu-id="d07fb-329">CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-329">CPropertyRestriction</span></span>         | <span data-ttu-id="d07fb-330">Contiene un valor de propiedad que debe coincidir con una operación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-330">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="d07fb-331">CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-331">CRangeRestriction</span></span>            | <span data-ttu-id="d07fb-332">Contiene una restricción en un intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="d07fb-332">Contains a restriction on a range of values.</span></span>                                                                           |
| <span data-ttu-id="d07fb-333">CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-333">CScopeRestriction</span></span>            | <span data-ttu-id="d07fb-334">Contiene una restricción en los archivos en los que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-334">Contains a restriction on the files to be searched.</span></span>                                                                    |
| <span data-ttu-id="d07fb-335">CSort</span><span class="sxs-lookup"><span data-stu-id="d07fb-335">CSort</span></span>                        | <span data-ttu-id="d07fb-336">Identifica una columna que se ordenará.</span><span class="sxs-lookup"><span data-stu-id="d07fb-336">Identifies a column to sort.</span></span>                                                                                           |
| <span data-ttu-id="d07fb-337">CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-337">CSynRestriction</span></span>              | <span data-ttu-id="d07fb-338">Contiene una palabra o sus sinónimos para una frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-338">Contains a word or its synonyms for a query phrase.</span></span>                                                                    |
| <span data-ttu-id="d07fb-339">CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-339">CVectorRestriction</span></span>           | <span data-ttu-id="d07fb-340">Contiene una operación OR ponderada en un nodo de árbol de comandos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-340">Contains a weighted OR operation on a command tree node.</span></span>                                                               |
| <span data-ttu-id="d07fb-341">CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-341">CWordRestriction</span></span>             | <span data-ttu-id="d07fb-342">Contiene una palabra para una frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-342">Contains a word for a query phrase.</span></span>                                                                                    |
| <span data-ttu-id="d07fb-343">CRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-343">CRestriction</span></span>                 | <span data-ttu-id="d07fb-344">Contiene un nodo de un árbol de comandos de consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-344">Contains a node of a query command tree.</span></span>                                                                               |
| <span data-ttu-id="d07fb-345">CColumnSet</span><span class="sxs-lookup"><span data-stu-id="d07fb-345">CColumnSet</span></span>                   | <span data-ttu-id="d07fb-346">Indica el número de columnas que se devolverán.</span><span class="sxs-lookup"><span data-stu-id="d07fb-346">Indicates the number of columns to return.</span></span>                                                                             |
| <span data-ttu-id="d07fb-347">CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="d07fb-347">CCategorizationSet</span></span>           | <span data-ttu-id="d07fb-348">Contiene información sobre la agrupación de un conjunto de resultados de consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-348">Contains information about the grouping of a set of query results.</span></span>                                                     |
| <span data-ttu-id="d07fb-349">CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="d07fb-349">CCategorizationSpec</span></span>          | <span data-ttu-id="d07fb-350">Contiene una definición de categorías en las que se clasificarán los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-350">Contains a definition of categories into which query results will be categorized.</span></span>                                      |
| <span data-ttu-id="d07fb-351">CDbColId</span><span class="sxs-lookup"><span data-stu-id="d07fb-351">CDbColId</span></span>                     | <span data-ttu-id="d07fb-352">Contiene una columna.</span><span class="sxs-lookup"><span data-stu-id="d07fb-352">Contains a column.</span></span>                                                                                                     |
| <span data-ttu-id="d07fb-353">CDbProp</span><span class="sxs-lookup"><span data-stu-id="d07fb-353">CDbProp</span></span>                      | <span data-ttu-id="d07fb-354">Contiene una propiedad .</span><span class="sxs-lookup"><span data-stu-id="d07fb-354">Contains a property.</span></span>                                                                                                   |
| <span data-ttu-id="d07fb-355">CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="d07fb-355">CDbPropSet</span></span>                   | <span data-ttu-id="d07fb-356">Contiene un conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d07fb-356">Contains a set of properties.</span></span>                                                                                          |
| <span data-ttu-id="d07fb-357">CPidMapper</span><span class="sxs-lookup"><span data-stu-id="d07fb-357">CPidMapper</span></span>                   | <span data-ttu-id="d07fb-358">Contiene una matriz de los nombres de propiedad que especifican las propiedades que se devolverán en un conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-358">Contains an array of property IDs specifying the properties to return in a rowset.</span></span>                                     |
| <span data-ttu-id="d07fb-359">CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="d07fb-359">CRowSeekAt</span></span>                   | <span data-ttu-id="d07fb-360">Contiene el desplazamiento en el que se van a recuperar las filas de un mensaje CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-360">Contains the offset at which to retrieve rows in a CPMGetRowsIn message</span></span>                                                |
| <span data-ttu-id="d07fb-361">CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="d07fb-361">CRowSeekAtRatio</span></span>              | <span data-ttu-id="d07fb-362">Identifica el punto en el que se va a iniciar la recuperación de un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-362">Identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>                                           |
| <span data-ttu-id="d07fb-363">CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="d07fb-363">CRowSeekByBookmark</span></span>           | <span data-ttu-id="d07fb-364">Identifica los marcadores de los que se van a recuperar las filas de un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-364">Identifies the bookmarks from which to retrieve rows for a CPMGetRowsIn message.</span></span>                                       |
| <span data-ttu-id="d07fb-365">CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="d07fb-365">CRowSeekNext</span></span>                 | <span data-ttu-id="d07fb-366">Contiene el número de filas que se omitirán en un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-366">Contains the number of rows to skip in a CPMGetRowsIn message.</span></span>                                                         |
| <span data-ttu-id="d07fb-367">CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="d07fb-367">CRowsetProperties</span></span>            | <span data-ttu-id="d07fb-368">Contiene la información de configuración de una consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-368">Contains the configuration information for a query.</span></span>                                                                    |
| <span data-ttu-id="d07fb-369">CSortSet</span><span class="sxs-lookup"><span data-stu-id="d07fb-369">CSortSet</span></span>                     | <span data-ttu-id="d07fb-370">Contiene el criterio de ordenación de una consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-370">Contains the sort order for a query.</span></span>                                                                                   |
| <span data-ttu-id="d07fb-371">CTableColumn</span><span class="sxs-lookup"><span data-stu-id="d07fb-371">CTableColumn</span></span>                 | <span data-ttu-id="d07fb-372">Contiene una columna para el mensaje CPMSetBindings.</span><span class="sxs-lookup"><span data-stu-id="d07fb-372">Contains a column for the CPMSetBindings message.</span></span>                                                                      |
| <span data-ttu-id="d07fb-373">SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="d07fb-373">SERIALIZEDPROPERTYVALUE</span></span>      | <span data-ttu-id="d07fb-374">Contiene un valor serializado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-374">Contains a serialized value.</span></span>                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a><span data-ttu-id="d07fb-375">2.2.1.1 CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="d07fb-375">2.2.1.1 CBaseStorageVariant</span></span>

<span data-ttu-id="d07fb-376">La estructura CBaseStorageVariant contiene el valor en el que se va a realizar una operación de coincidencia para una propiedad especificada en la estructura CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="d07fb-376">The CBaseStorageVariant structure contains the value on which to perform a match operation for a property specified in the CPropertyRestriction structure.</span></span>



<span data-ttu-id="d07fb-377">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-377">0</span></span>

<span data-ttu-id="d07fb-378">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-378">1</span></span>

<span data-ttu-id="d07fb-379">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-379">2</span></span>

<span data-ttu-id="d07fb-380">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-380">3</span></span>

<span data-ttu-id="d07fb-381">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-381">4</span></span>

<span data-ttu-id="d07fb-382">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-382">5</span></span>

<span data-ttu-id="d07fb-383">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-383">6</span></span>

<span data-ttu-id="d07fb-384">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-384">7</span></span>

<span data-ttu-id="d07fb-385">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-385">8</span></span>

<span data-ttu-id="d07fb-386">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-386">9</span></span>

<span data-ttu-id="d07fb-387">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-387">1</span></span><br/> <span data-ttu-id="d07fb-388">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-388">0</span></span><br/>

<span data-ttu-id="d07fb-389">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-389">1</span></span>

<span data-ttu-id="d07fb-390">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-390">2</span></span>

<span data-ttu-id="d07fb-391">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-391">3</span></span>

<span data-ttu-id="d07fb-392">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-392">4</span></span>

<span data-ttu-id="d07fb-393">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-393">5</span></span>

<span data-ttu-id="d07fb-394">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-394">6</span></span>

<span data-ttu-id="d07fb-395">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-395">7</span></span>

<span data-ttu-id="d07fb-396">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-396">8</span></span>

<span data-ttu-id="d07fb-397">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-397">9</span></span>

<span data-ttu-id="d07fb-398">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-398">2</span></span><br/> <span data-ttu-id="d07fb-399">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-399">0</span></span><br/>

<span data-ttu-id="d07fb-400">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-400">1</span></span>

<span data-ttu-id="d07fb-401">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-401">2</span></span>

<span data-ttu-id="d07fb-402">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-402">3</span></span>

<span data-ttu-id="d07fb-403">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-403">4</span></span>

<span data-ttu-id="d07fb-404">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-404">5</span></span>

<span data-ttu-id="d07fb-405">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-405">6</span></span>

<span data-ttu-id="d07fb-406">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-406">7</span></span>

<span data-ttu-id="d07fb-407">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-407">8</span></span>

<span data-ttu-id="d07fb-408">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-408">9</span></span>

<span data-ttu-id="d07fb-409">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-409">3</span></span><br/> <span data-ttu-id="d07fb-410">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-410">0</span></span><br/>

<span data-ttu-id="d07fb-411">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-411">1</span></span>

<span data-ttu-id="d07fb-412">vType</span><span class="sxs-lookup"><span data-stu-id="d07fb-412">vType</span></span>

<span data-ttu-id="d07fb-413">vData1</span><span class="sxs-lookup"><span data-stu-id="d07fb-413">vData1</span></span>

<span data-ttu-id="d07fb-414">vData2</span><span class="sxs-lookup"><span data-stu-id="d07fb-414">vData2</span></span>

<span data-ttu-id="d07fb-415">vValue (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-415">vValue (variable)</span></span>



 

<span data-ttu-id="d07fb-416">**vType:** un indicador de tipo que indica el tipo de vValue.</span><span class="sxs-lookup"><span data-stu-id="d07fb-416">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="d07fb-417">DEBE ser uno de los valores VARENUM especificados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-417">It MUST be one of the VARENUM values specified in the following table.</span></span>



| <span data-ttu-id="d07fb-418">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-418">Value</span></span>                 | <span data-ttu-id="d07fb-419">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-419">Meaning</span></span>                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-420">VT \_ EMPTY (0x0000)</span><span class="sxs-lookup"><span data-stu-id="d07fb-420">VT\_EMPTY (0x0000)</span></span>    | <span data-ttu-id="d07fb-421">vValue no está presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-421">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="d07fb-422">VT \_ NULL (0x0001)</span><span class="sxs-lookup"><span data-stu-id="d07fb-422">VT\_NULL (0x0001)</span></span>     | <span data-ttu-id="d07fb-423">vValue no está presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-423">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="d07fb-424">VT \_ I1 (0x0010)</span><span class="sxs-lookup"><span data-stu-id="d07fb-424">VT\_I1 (0x0010)</span></span>       | <span data-ttu-id="d07fb-425">Entero de 1 byte con signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-425">A 1-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="d07fb-426">VT \_ UI1 (0x0011)</span><span class="sxs-lookup"><span data-stu-id="d07fb-426">VT\_UI1 (0x0011)</span></span>      | <span data-ttu-id="d07fb-427">Entero de 1 byte sin signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-427">A 1-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="d07fb-428">VT \_ I2 (0x0002)</span><span class="sxs-lookup"><span data-stu-id="d07fb-428">VT\_I2 (0x0002)</span></span>       | <span data-ttu-id="d07fb-429">Entero de 2 bytes con signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-429">A 2-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="d07fb-430">VT \_ UI2 (0x0012)</span><span class="sxs-lookup"><span data-stu-id="d07fb-430">VT\_UI2 (0x0012)</span></span>      | <span data-ttu-id="d07fb-431">Entero de 2 bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-431">A 2-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="d07fb-432">VT \_ BOOL (0x000B)</span><span class="sxs-lookup"><span data-stu-id="d07fb-432">VT\_BOOL (0x000B)</span></span>     | <span data-ttu-id="d07fb-433">Valor booleano; entero de 2 bytes que contiene 0x0000 (FALSE) o 0xFFFF (TRUE).</span><span class="sxs-lookup"><span data-stu-id="d07fb-433">A boolean value; a 2-byte integer containing 0x0000 (FALSE) or 0xFFFF (TRUE).</span></span>                                                        |
| <span data-ttu-id="d07fb-434">VT \_ I4 (0x0003)</span><span class="sxs-lookup"><span data-stu-id="d07fb-434">VT\_I4 (0x0003)</span></span>       | <span data-ttu-id="d07fb-435">Entero de 4 bytes con signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-435">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="d07fb-436">VT \_ UI4 (0x0013)</span><span class="sxs-lookup"><span data-stu-id="d07fb-436">VT\_UI4 (0x0013)</span></span>      | <span data-ttu-id="d07fb-437">Entero de 4 bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-437">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="d07fb-438">VT \_ R4 (0x0004)</span><span class="sxs-lookup"><span data-stu-id="d07fb-438">VT\_R4 (0x0004)</span></span>       | <span data-ttu-id="d07fb-439">Número de punto flotante ieee de 32 bits, tal como se define en \[ IEEE754. \]</span><span class="sxs-lookup"><span data-stu-id="d07fb-439">An IEEE 32-bit floating-point number, as defined in \[IEEE754\].</span></span>                                                                     |
| <span data-ttu-id="d07fb-440">VT \_ INT (0x0016)</span><span class="sxs-lookup"><span data-stu-id="d07fb-440">VT\_INT (0x0016)</span></span>      | <span data-ttu-id="d07fb-441">Entero de 4 bytes con signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-441">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="d07fb-442">VT \_ UINT (0x0017)</span><span class="sxs-lookup"><span data-stu-id="d07fb-442">VT\_UINT (0x0017)</span></span>     | <span data-ttu-id="d07fb-443">Entero de 4 bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-443">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="d07fb-444">\_ERROR DE VT (0x000A)</span><span class="sxs-lookup"><span data-stu-id="d07fb-444">VT\_ERROR (0x000A)</span></span>    | <span data-ttu-id="d07fb-445">Entero de 4 bytes sin signo que contiene un valor HRESULT, tal y como se especifica en \[ MS-SYS \] .</span><span class="sxs-lookup"><span data-stu-id="d07fb-445">A 4-byte unsigned integer containing an HRESULT, as specified in \[MS-SYS\].</span></span>                                                         |
| <span data-ttu-id="d07fb-446">VT \_ I8 (0x0014)</span><span class="sxs-lookup"><span data-stu-id="d07fb-446">VT\_I8 (0x0014)</span></span>       | <span data-ttu-id="d07fb-447">Entero de 8 bytes con signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-447">An 8 byte signed integer.</span></span>                                                                                                            |
| <span data-ttu-id="d07fb-448">VT \_ UI8 (0x0015)</span><span class="sxs-lookup"><span data-stu-id="d07fb-448">VT\_UI8 (0x0015)</span></span>      | <span data-ttu-id="d07fb-449">Entero de 8 bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-449">An 8-byte unsigned integer.</span></span>                                                                                                          |
| <span data-ttu-id="d07fb-450">VT \_ R8 (0x0005)</span><span class="sxs-lookup"><span data-stu-id="d07fb-450">VT\_R8 (0x0005)</span></span>       | <span data-ttu-id="d07fb-451">Número de punto flotante ieee de 64 bits definido en \[ IEEE754. \]</span><span class="sxs-lookup"><span data-stu-id="d07fb-451">An IEEE 64-bit floating-point number as defined in \[IEEE754\].</span></span>                                                                      |
| <span data-ttu-id="d07fb-452">VT \_ CY (0x0006)</span><span class="sxs-lookup"><span data-stu-id="d07fb-452">VT\_CY (0x0006)</span></span>       | <span data-ttu-id="d07fb-453">Entero de complemento de dos de 8 bytes (escalado en 10 000).</span><span class="sxs-lookup"><span data-stu-id="d07fb-453">An 8-byte two's complement integer (scaled by 10,000).</span></span>                                                                               |
| <span data-ttu-id="d07fb-454">VT \_ DATE (0x0007)</span><span class="sxs-lookup"><span data-stu-id="d07fb-454">VT\_DATE (0x0007)</span></span>     | <span data-ttu-id="d07fb-455">Número de punto flotante de 64 bits que representa el número de días desde las 00:00:00 del 31 de diciembre de 1899 (hora universal coordinada).</span><span class="sxs-lookup"><span data-stu-id="d07fb-455">A 64-bit floating-point number representing the number of days since 00:00:00 on December 31, 1899 (Coordinated Universal Time).</span></span>     |
| <span data-ttu-id="d07fb-456">VT \_ FILETIME (0x0040)</span><span class="sxs-lookup"><span data-stu-id="d07fb-456">VT\_FILETIME (0x0040)</span></span> | <span data-ttu-id="d07fb-457">Entero de 64 bits que representa el número de intervalos de 100 nanosegundos desde las 00:00:00 del 1 de enero de 1601 (hora universal coordinada).</span><span class="sxs-lookup"><span data-stu-id="d07fb-457">A 64-bit integer representing the number of 100-nanosecond intervals since 00:00:00 on January 1, 1601 (Coordinated Universal Time).</span></span> |
| <span data-ttu-id="d07fb-458">\_VT DECIMAL (0x000E)</span><span class="sxs-lookup"><span data-stu-id="d07fb-458">VT\_DECIMAL (0x000E)</span></span>  | <span data-ttu-id="d07fb-459">Estructura DECIMAL especificada en la sección 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="d07fb-459">A DECIMAL structure as specified in section 2.2.1.1.1.1.</span></span>                                                                             |
| <span data-ttu-id="d07fb-460">VT \_ CLSID (0x0048)</span><span class="sxs-lookup"><span data-stu-id="d07fb-460">VT\_CLSID (0x0048)</span></span>    | <span data-ttu-id="d07fb-461">Valor binario de 16 bytes que contiene un GUID.</span><span class="sxs-lookup"><span data-stu-id="d07fb-461">A 16-byte binary value containing a GUID.</span></span>                                                                                            |
| <span data-ttu-id="d07fb-462">\_VT BLOB (0x0041)</span><span class="sxs-lookup"><span data-stu-id="d07fb-462">VT\_BLOB (0x0041)</span></span>     | <span data-ttu-id="d07fb-463">Un número entero de 4 bytes sin signo de bytes en el blob, seguido de tantos bytes de datos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-463">A 4-byte unsigned integer count of bytes in the blob, followed by that many bytes of data.</span></span>                                           |
| <span data-ttu-id="d07fb-464">VT \_ BSTR (0x0008)</span><span class="sxs-lookup"><span data-stu-id="d07fb-464">VT\_BSTR (0x0008)</span></span>     | <span data-ttu-id="d07fb-465">Un número entero de 4 bytes sin signo de bytes en la cadena, seguido de una cadena, como se especifica a continuación en vValue.</span><span class="sxs-lookup"><span data-stu-id="d07fb-465">A 4-byte unsigned integer count of bytes in the string, followed by a string, as specified below under vValue.</span></span>                       |
| <span data-ttu-id="d07fb-466">VT \_ LPSTR (0x001E)</span><span class="sxs-lookup"><span data-stu-id="d07fb-466">VT\_LPSTR (0x001E)</span></span>    | <span data-ttu-id="d07fb-467">Cadena ANSI terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="d07fb-467">A null-terminated ANSI string.</span></span>                                                                                                       |
| <span data-ttu-id="d07fb-468">VT \_ LPWSTR (0x001F)</span><span class="sxs-lookup"><span data-stu-id="d07fb-468">VT\_LPWSTR (0x001F)</span></span>   | <span data-ttu-id="d07fb-469">Cadena Unicode terminada en \[ \] NULL.</span><span class="sxs-lookup"><span data-stu-id="d07fb-469">A null-terminated Unicode \[UNICODE\] string.</span></span>                                                                                        |
| <span data-ttu-id="d07fb-470">VT \_ VARIANT (0x000C)</span><span class="sxs-lookup"><span data-stu-id="d07fb-470">VT\_VARIANT (0x000C)</span></span>  | <span data-ttu-id="d07fb-471">CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="d07fb-471">CBaseStorageVariant.</span></span> <span data-ttu-id="d07fb-472">DEBE combinarse con un modificador de tipo de VT \_ ARRAY o VT \_ VECTOR.</span><span class="sxs-lookup"><span data-stu-id="d07fb-472">MUST be combined with a type modifier of VT\_ARRAY or VT\_VECTOR.</span></span>                                               |



 

<span data-ttu-id="d07fb-473">En la tabla siguiente se especifican los modificadores de tipo para vType.</span><span class="sxs-lookup"><span data-stu-id="d07fb-473">The following table specifies the type modifiers for vType.</span></span> <span data-ttu-id="d07fb-474">Los modificadores de tipo pueden ser binarios ORed con vType, para cambiar el significado de vValue para indicar que es uno de los dos tipos de matriz posibles.</span><span class="sxs-lookup"><span data-stu-id="d07fb-474">Type modifiers can be binary ORed with vType, to change the meaning of vValue to indicate it is one of two possible array types.</span></span>



| <span data-ttu-id="d07fb-475">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-475">Value</span></span>               | <span data-ttu-id="d07fb-476">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-476">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-477">VT \_ VECTOR (0x1000)</span><span class="sxs-lookup"><span data-stu-id="d07fb-477">VT\_VECTOR (0x1000)</span></span> | <span data-ttu-id="d07fb-478">Si el indicador de tipo se combina con VT VECTOR mediante un operador OR, vValue es una matriz de valores con recuento \_ del tipo indicado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-478">If the type indicator is combined with VT\_VECTOR by using an OR operator, vValue is a counted array of values of the indicated type.</span></span> <span data-ttu-id="d07fb-479">Consulte la sección 2.2.1.1.1.2 para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="d07fb-479">See section 2.2.1.1.1.2 for details.</span></span> <br/> <span data-ttu-id="d07fb-480">Este modificador de tipo NO DEBE combinarse con los siguientes tipos: VT \_ INT, VT \_ UINT, VT \_ DECIMAL, VT \_ BLOB, VT \_ BLOB \_ OBJECT.</span><span class="sxs-lookup"><span data-stu-id="d07fb-480">This type modifier MUST NOT be combined with the following types: VT\_INT, VT\_UINT, VT\_DECIMAL, VT\_BLOB, VT\_BLOB\_OBJECT.</span></span><br/>                                    |
| <span data-ttu-id="d07fb-481">VT \_ ARRAY (0x2000)</span><span class="sxs-lookup"><span data-stu-id="d07fb-481">VT\_ARRAY (0x2000)</span></span>  | <span data-ttu-id="d07fb-482">Si un operador OR combina el indicador de tipo con VT ARRAY, el valor es SAFEARRAY (como se especifica en la sección \_ 2.2.1.1.1.3) que contiene valores del tipo indicado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-482">If the type indicator is combined with VT\_ARRAY by an OR operator, the value is a SAFEARRAY (as specified in section 2.2.1.1.1.3) containing values of the indicated type.</span></span> <br/> <span data-ttu-id="d07fb-483">Este modificador de tipo NO DEBE combinarse con los siguientes tipos: VT \_ I8, VT \_ UI8, VT \_ FILETIME, VT \_ CLSID, VT \_ BLOB, VT \_ BLOB \_ OBJECT, VT \_ LPSTR, VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="d07fb-483">This type modifier MUST NOT be combined with the following types: VT\_I8, VT\_UI8, VT\_FILETIME, VT\_CLSID, VT\_BLOB, VT\_BLOB\_OBJECT, VT\_LPSTR, VT\_LPWSTR.</span></span> <br/> |



 

<span data-ttu-id="d07fb-484">**vData1:** cuando vType es VT DECIMAL, el valor de este campo se especifica como el campo Escala en la sección \_ 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="d07fb-484">**vData1**: When vType is VT\_DECIMAL, the value of this field is specified as the Scale field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="d07fb-485">Para todos los demás vTypes, el valor DEBE establecerse en 0x00.</span><span class="sxs-lookup"><span data-stu-id="d07fb-485">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="d07fb-486">**vData2:** cuando vType es VT DECIMAL, el valor de este campo se especifica como el campo Sign en la sección \_ 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="d07fb-486">**vData2**: When vType is VT\_DECIMAL, the value of this field is specified as the Sign field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="d07fb-487">Para todos los demás vTypes, el valor DEBE establecerse en 0x00.</span><span class="sxs-lookup"><span data-stu-id="d07fb-487">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="d07fb-488">**vValue:** el valor de la operación de coincidencia.</span><span class="sxs-lookup"><span data-stu-id="d07fb-488">**vValue**: The value for the match operation.</span></span> <span data-ttu-id="d07fb-489">La sintaxis DEBE ser como se indica en el campo vType.</span><span class="sxs-lookup"><span data-stu-id="d07fb-489">The syntax MUST be as indicated in the vType field.</span></span>

<span data-ttu-id="d07fb-490">En la tabla siguiente se resumen los tamaños del campo vValue, en función del campo vType para los tipos de datos de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="d07fb-490">The following table summarizes sizes for the vValue field, dependent upon the vType field for fixed-length data types.</span></span> <span data-ttu-id="d07fb-491">El tamaño es en bytes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-491">The size is in bytes.</span></span>



| <span data-ttu-id="d07fb-492">vType</span><span class="sxs-lookup"><span data-stu-id="d07fb-492">vType</span></span>                                                   | <span data-ttu-id="d07fb-493">Size</span><span class="sxs-lookup"><span data-stu-id="d07fb-493">Size</span></span> |
|---------------------------------------------------------|------|
| <span data-ttu-id="d07fb-494">VT \_ I1, VT, \_ UI1</span><span class="sxs-lookup"><span data-stu-id="d07fb-494">VT\_I1, VT,\_UI1</span></span>                                        | <span data-ttu-id="d07fb-495">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-495">1</span></span>    |
| <span data-ttu-id="d07fb-496">VT \_ I2, VT \_ UI2, VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="d07fb-496">VT\_I2, VT\_UI2, VT\_BOOL</span></span>                               | <span data-ttu-id="d07fb-497">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-497">2</span></span>    |
| <span data-ttu-id="d07fb-498">VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ INT, VT \_ UINT, VT \_ ERROR</span><span class="sxs-lookup"><span data-stu-id="d07fb-498">VT\_I4, VT\_UI4, VT\_R4, VT\_INT, VT\_UINT, VT\_ERROR</span></span>   | <span data-ttu-id="d07fb-499">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-499">4</span></span>    |
| <span data-ttu-id="d07fb-500">VT \_ I8, VT \_ UI8, VT \_ R8, VT \_ CY, VT \_ DATE, VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="d07fb-500">VT\_I8, VT\_UI8, VT\_R8, VT\_CY, VT\_DATE, VT\_FILETIME</span></span> | <span data-ttu-id="d07fb-501">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-501">8</span></span>    |
| <span data-ttu-id="d07fb-502">VT \_ DECIMAL, VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="d07fb-502">VT\_DECIMAL, VT\_CLSID</span></span>                                  | <span data-ttu-id="d07fb-503">16</span><span class="sxs-lookup"><span data-stu-id="d07fb-503">16</span></span>   |



 

<span data-ttu-id="d07fb-504">Si vType se establece en \_ VT BLOB, VT BSTR o VT LPSTR, la estructura de vValue se \_ especifica en el diagrama \_ siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-504">If vType is set to VT\_BLOB, VT\_BSTR or VT\_LPSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="d07fb-505">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-505">0</span></span>

<span data-ttu-id="d07fb-506">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-506">1</span></span>

<span data-ttu-id="d07fb-507">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-507">2</span></span>

<span data-ttu-id="d07fb-508">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-508">3</span></span>

<span data-ttu-id="d07fb-509">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-509">4</span></span>

<span data-ttu-id="d07fb-510">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-510">5</span></span>

<span data-ttu-id="d07fb-511">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-511">6</span></span>

<span data-ttu-id="d07fb-512">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-512">7</span></span>

<span data-ttu-id="d07fb-513">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-513">8</span></span>

<span data-ttu-id="d07fb-514">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-514">9</span></span>

<span data-ttu-id="d07fb-515">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-515">1</span></span><br/> <span data-ttu-id="d07fb-516">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-516">0</span></span><br/>

<span data-ttu-id="d07fb-517">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-517">1</span></span>

<span data-ttu-id="d07fb-518">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-518">2</span></span>

<span data-ttu-id="d07fb-519">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-519">3</span></span>

<span data-ttu-id="d07fb-520">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-520">4</span></span>

<span data-ttu-id="d07fb-521">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-521">5</span></span>

<span data-ttu-id="d07fb-522">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-522">6</span></span>

<span data-ttu-id="d07fb-523">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-523">7</span></span>

<span data-ttu-id="d07fb-524">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-524">8</span></span>

<span data-ttu-id="d07fb-525">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-525">9</span></span>

<span data-ttu-id="d07fb-526">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-526">2</span></span><br/> <span data-ttu-id="d07fb-527">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-527">0</span></span><br/>

<span data-ttu-id="d07fb-528">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-528">1</span></span>

<span data-ttu-id="d07fb-529">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-529">2</span></span>

<span data-ttu-id="d07fb-530">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-530">3</span></span>

<span data-ttu-id="d07fb-531">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-531">4</span></span>

<span data-ttu-id="d07fb-532">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-532">5</span></span>

<span data-ttu-id="d07fb-533">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-533">6</span></span>

<span data-ttu-id="d07fb-534">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-534">7</span></span>

<span data-ttu-id="d07fb-535">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-535">8</span></span>

<span data-ttu-id="d07fb-536">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-536">9</span></span>

<span data-ttu-id="d07fb-537">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-537">3</span></span><br/> <span data-ttu-id="d07fb-538">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-538">0</span></span><br/>

<span data-ttu-id="d07fb-539">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-539">1</span></span>

<span data-ttu-id="d07fb-540">cbSize</span><span class="sxs-lookup"><span data-stu-id="d07fb-540">cbSize</span></span>

<span data-ttu-id="d07fb-541">blobData (variable, opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-541">blobData (variable, optional)</span></span>



 

<span data-ttu-id="d07fb-542">**cbSize:** entero de 32 bits sin signo, que indica el tamaño del campo blobData en bytes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-542">**cbSize**: Unsigned 32-bit integer, indicating the size of the blobData field in bytes.</span></span> <span data-ttu-id="d07fb-543">Si vType se establece en VT BSTR o \_ VT LPSTR, cbSize DEBE establecerse en 0x00000000 cuando la cadena representada \_ es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="d07fb-543">If vType is set to VT\_BSTR or VT\_LPSTR, cbSize MUST be set to 0x00000000 when the string represented is an empty string.</span></span>

<span data-ttu-id="d07fb-544">**blobData:** DEBE tener la longitud cbSize en bytes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-544">**blobData**: MUST be of length cbSize in bytes.</span></span>

<span data-ttu-id="d07fb-545">Para vType establecido en VT \_ BLOB, este campo son datos de blob binario opacos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-545">For vType set to VT\_BLOB, this field is opaque binary blob data.</span></span>

<span data-ttu-id="d07fb-546">Para vType establecido en VT BSTR, este campo es un conjunto de caracteres en un juego de caracteres \_ seleccionado por OEM.</span><span class="sxs-lookup"><span data-stu-id="d07fb-546">For vType set to VT\_BSTR, this field is a set of characters in an OEM selected character set.</span></span> <span data-ttu-id="d07fb-547">El cliente y el servidor DEBEN configurarse para tener conjuntos de caracteres interoperables (fuera de banda del protocolo).</span><span class="sxs-lookup"><span data-stu-id="d07fb-547">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span> <span data-ttu-id="d07fb-548">No es necesario que se termine en null.</span><span class="sxs-lookup"><span data-stu-id="d07fb-548">There is no requirement that it be null-terminated.</span></span>

<span data-ttu-id="d07fb-549">Para vType establecido en VT LPSTR, este campo es una cadena de caracteres terminada en NULL en un \_ juego de caracteres seleccionado por OEM.</span><span class="sxs-lookup"><span data-stu-id="d07fb-549">For vType set to VT\_LPSTR this field is a null-terminated character string in an OEM selected character set.</span></span> <span data-ttu-id="d07fb-550">El cliente y el servidor DEBEN configurarse para tener conjuntos de caracteres interoperables (fuera de banda del protocolo).</span><span class="sxs-lookup"><span data-stu-id="d07fb-550">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span>

<span data-ttu-id="d07fb-551">Si vType se establece en VT \_ LPWSTR, la estructura de vValue se especifica en el diagrama siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-551">If vType is set to VT\_LPWSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="d07fb-552">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-552">0</span></span>

<span data-ttu-id="d07fb-553">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-553">1</span></span>

<span data-ttu-id="d07fb-554">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-554">2</span></span>

<span data-ttu-id="d07fb-555">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-555">3</span></span>

<span data-ttu-id="d07fb-556">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-556">4</span></span>

<span data-ttu-id="d07fb-557">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-557">5</span></span>

<span data-ttu-id="d07fb-558">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-558">6</span></span>

<span data-ttu-id="d07fb-559">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-559">7</span></span>

<span data-ttu-id="d07fb-560">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-560">8</span></span>

<span data-ttu-id="d07fb-561">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-561">9</span></span>

<span data-ttu-id="d07fb-562">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-562">1</span></span><br/> <span data-ttu-id="d07fb-563">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-563">0</span></span><br/>

<span data-ttu-id="d07fb-564">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-564">1</span></span>

<span data-ttu-id="d07fb-565">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-565">2</span></span>

<span data-ttu-id="d07fb-566">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-566">3</span></span>

<span data-ttu-id="d07fb-567">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-567">4</span></span>

<span data-ttu-id="d07fb-568">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-568">5</span></span>

<span data-ttu-id="d07fb-569">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-569">6</span></span>

<span data-ttu-id="d07fb-570">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-570">7</span></span>

<span data-ttu-id="d07fb-571">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-571">8</span></span>

<span data-ttu-id="d07fb-572">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-572">9</span></span>

<span data-ttu-id="d07fb-573">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-573">2</span></span><br/> <span data-ttu-id="d07fb-574">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-574">0</span></span><br/>

<span data-ttu-id="d07fb-575">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-575">1</span></span>

<span data-ttu-id="d07fb-576">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-576">2</span></span>

<span data-ttu-id="d07fb-577">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-577">3</span></span>

<span data-ttu-id="d07fb-578">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-578">4</span></span>

<span data-ttu-id="d07fb-579">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-579">5</span></span>

<span data-ttu-id="d07fb-580">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-580">6</span></span>

<span data-ttu-id="d07fb-581">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-581">7</span></span>

<span data-ttu-id="d07fb-582">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-582">8</span></span>

<span data-ttu-id="d07fb-583">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-583">9</span></span>

<span data-ttu-id="d07fb-584">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-584">3</span></span><br/> <span data-ttu-id="d07fb-585">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-585">0</span></span><br/>

<span data-ttu-id="d07fb-586">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-586">1</span></span>

<span data-ttu-id="d07fb-587">ccLen</span><span class="sxs-lookup"><span data-stu-id="d07fb-587">ccLen</span></span>

<span data-ttu-id="d07fb-588">string (variable, opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-588">string (variable, optional)</span></span>



 

<span data-ttu-id="d07fb-589">**ccLen:** entero de 32 bits sin signo, que indica el tamaño del campo de cadena en caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="d07fb-589">**ccLen**: Unsigned 32-bit integer, indicating the size of the string field in Unicode characters.</span></span> <span data-ttu-id="d07fb-590">DEBE establecerse en 0x00000000 para una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="d07fb-590">MUST be set to 0x00000000 for an empty string.</span></span>

<span data-ttu-id="d07fb-591">**string:** cadena Unicode terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="d07fb-591">**string**: Null-terminated Unicode string.</span></span>

### <a name="22111-cbasestoragevariant-structures"></a><span data-ttu-id="d07fb-592">2.2.1.1.1 CBaseStorageVariant Structures</span><span class="sxs-lookup"><span data-stu-id="d07fb-592">2.2.1.1.1 CBaseStorageVariant Structures</span></span>

<span data-ttu-id="d07fb-593">Las estructuras siguientes se usan en la estructura CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="d07fb-593">The following structures are used in the CBaseStorageVariant structure.</span></span>

### <a name="221111-decimal"></a><span data-ttu-id="d07fb-594">2.2.1.1.1.1 DECIMAL</span><span class="sxs-lookup"><span data-stu-id="d07fb-594">2.2.1.1.1.1 DECIMAL</span></span>

<span data-ttu-id="d07fb-595">DECIMAL se usa para representar un valor numérico exacto con una precisión fija y una escala fija.</span><span class="sxs-lookup"><span data-stu-id="d07fb-595">DECIMAL is used to represent an exact numeric value with a fixed precision and fixed scale.</span></span>

<span data-ttu-id="d07fb-596">Cuando vType se establece en VT DECIMAL (0x0000E), los campos vData1 y vData2 de CBaseStorageVariant DEBEN interpretarse de \_ la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-596">When vType is set to VT\_DECIMAL (0x0000E), the vData1 and vData2 fields of CBaseStorageVariant MUST be interpreted as follows:</span></span>

<span data-ttu-id="d07fb-597">**vData1:** número de dígitos a la derecha del separador decimal.</span><span class="sxs-lookup"><span data-stu-id="d07fb-597">**vData1**: The number of digits to the right of the decimal point.</span></span> <span data-ttu-id="d07fb-598">DEBE estar en el intervalo de 0 a 28.</span><span class="sxs-lookup"><span data-stu-id="d07fb-598">MUST be in the range 0 to 28.</span></span>

<span data-ttu-id="d07fb-599">**vData2:** signo del valor numérico.</span><span class="sxs-lookup"><span data-stu-id="d07fb-599">**vData2**: The sign of the numeric value.</span></span> <span data-ttu-id="d07fb-600">Establezca en 0x00 si es positivo, 0x80 si es negativo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-600">Set to 0x00 if positive, 0x80 if negative.</span></span>

<span data-ttu-id="d07fb-601">El formato del campo vValue es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-601">The format of the vValue field is:</span></span>



<span data-ttu-id="d07fb-602">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-602">0</span></span>

<span data-ttu-id="d07fb-603">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-603">1</span></span>

<span data-ttu-id="d07fb-604">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-604">2</span></span>

<span data-ttu-id="d07fb-605">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-605">3</span></span>

<span data-ttu-id="d07fb-606">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-606">4</span></span>

<span data-ttu-id="d07fb-607">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-607">5</span></span>

<span data-ttu-id="d07fb-608">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-608">6</span></span>

<span data-ttu-id="d07fb-609">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-609">7</span></span>

<span data-ttu-id="d07fb-610">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-610">8</span></span>

<span data-ttu-id="d07fb-611">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-611">9</span></span>

<span data-ttu-id="d07fb-612">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-612">1</span></span><br/> <span data-ttu-id="d07fb-613">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-613">0</span></span><br/>

<span data-ttu-id="d07fb-614">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-614">1</span></span>

<span data-ttu-id="d07fb-615">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-615">2</span></span>

<span data-ttu-id="d07fb-616">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-616">3</span></span>

<span data-ttu-id="d07fb-617">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-617">4</span></span>

<span data-ttu-id="d07fb-618">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-618">5</span></span>

<span data-ttu-id="d07fb-619">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-619">6</span></span>

<span data-ttu-id="d07fb-620">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-620">7</span></span>

<span data-ttu-id="d07fb-621">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-621">8</span></span>

<span data-ttu-id="d07fb-622">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-622">9</span></span>

<span data-ttu-id="d07fb-623">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-623">2</span></span><br/> <span data-ttu-id="d07fb-624">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-624">0</span></span><br/>

<span data-ttu-id="d07fb-625">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-625">1</span></span>

<span data-ttu-id="d07fb-626">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-626">2</span></span>

<span data-ttu-id="d07fb-627">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-627">3</span></span>

<span data-ttu-id="d07fb-628">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-628">4</span></span>

<span data-ttu-id="d07fb-629">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-629">5</span></span>

<span data-ttu-id="d07fb-630">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-630">6</span></span>

<span data-ttu-id="d07fb-631">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-631">7</span></span>

<span data-ttu-id="d07fb-632">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-632">8</span></span>

<span data-ttu-id="d07fb-633">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-633">9</span></span>

<span data-ttu-id="d07fb-634">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-634">3</span></span><br/> <span data-ttu-id="d07fb-635">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-635">0</span></span><br/>

<span data-ttu-id="d07fb-636">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-636">1</span></span>

<span data-ttu-id="d07fb-637">Hi32</span><span class="sxs-lookup"><span data-stu-id="d07fb-637">Hi32</span></span>

<span data-ttu-id="d07fb-638">Lo32</span><span class="sxs-lookup"><span data-stu-id="d07fb-638">Lo32</span></span>

<span data-ttu-id="d07fb-639">Mid32</span><span class="sxs-lookup"><span data-stu-id="d07fb-639">Mid32</span></span>



 

<span data-ttu-id="d07fb-640">**Hi32:** los 32 bits más altos del entero de 96 bits.</span><span class="sxs-lookup"><span data-stu-id="d07fb-640">**Hi32**: The highest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="d07fb-641">**Lo32:** los 32 bits más bajos del entero de 96 bits.</span><span class="sxs-lookup"><span data-stu-id="d07fb-641">**Lo32**: The lowest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="d07fb-642">**Mid32:** los 32 bits centrales del entero de 96 bits.</span><span class="sxs-lookup"><span data-stu-id="d07fb-642">**Mid32**: The middle 32 bits of the 96 bit integer.</span></span>

### <a name="221112-vt_vector"></a><span data-ttu-id="d07fb-643">2.2.1.1.1.2 VT \_ VECTOR</span><span class="sxs-lookup"><span data-stu-id="d07fb-643">2.2.1.1.1.2 VT\_VECTOR</span></span>

<span data-ttu-id="d07fb-644">Vt \_ Vector se usa para pasar matrices unidimensionales.</span><span class="sxs-lookup"><span data-stu-id="d07fb-644">VT\_Vector is used to pass one-dimensional arrays.</span></span>



<span data-ttu-id="d07fb-645">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-645">0</span></span>

<span data-ttu-id="d07fb-646">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-646">1</span></span>

<span data-ttu-id="d07fb-647">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-647">2</span></span>

<span data-ttu-id="d07fb-648">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-648">3</span></span>

<span data-ttu-id="d07fb-649">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-649">4</span></span>

<span data-ttu-id="d07fb-650">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-650">5</span></span>

<span data-ttu-id="d07fb-651">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-651">6</span></span>

<span data-ttu-id="d07fb-652">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-652">7</span></span>

<span data-ttu-id="d07fb-653">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-653">8</span></span>

<span data-ttu-id="d07fb-654">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-654">9</span></span>

<span data-ttu-id="d07fb-655">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-655">1</span></span><br/> <span data-ttu-id="d07fb-656">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-656">0</span></span><br/>

<span data-ttu-id="d07fb-657">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-657">1</span></span>

<span data-ttu-id="d07fb-658">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-658">2</span></span>

<span data-ttu-id="d07fb-659">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-659">3</span></span>

<span data-ttu-id="d07fb-660">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-660">4</span></span>

<span data-ttu-id="d07fb-661">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-661">5</span></span>

<span data-ttu-id="d07fb-662">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-662">6</span></span>

<span data-ttu-id="d07fb-663">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-663">7</span></span>

<span data-ttu-id="d07fb-664">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-664">8</span></span>

<span data-ttu-id="d07fb-665">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-665">9</span></span>

<span data-ttu-id="d07fb-666">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-666">2</span></span><br/> <span data-ttu-id="d07fb-667">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-667">0</span></span><br/>

<span data-ttu-id="d07fb-668">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-668">1</span></span>

<span data-ttu-id="d07fb-669">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-669">2</span></span>

<span data-ttu-id="d07fb-670">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-670">3</span></span>

<span data-ttu-id="d07fb-671">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-671">4</span></span>

<span data-ttu-id="d07fb-672">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-672">5</span></span>

<span data-ttu-id="d07fb-673">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-673">6</span></span>

<span data-ttu-id="d07fb-674">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-674">7</span></span>

<span data-ttu-id="d07fb-675">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-675">8</span></span>

<span data-ttu-id="d07fb-676">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-676">9</span></span>

<span data-ttu-id="d07fb-677">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-677">3</span></span><br/> <span data-ttu-id="d07fb-678">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-678">0</span></span><br/>

<span data-ttu-id="d07fb-679">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-679">1</span></span>

<span data-ttu-id="d07fb-680">vVectorElements</span><span class="sxs-lookup"><span data-stu-id="d07fb-680">vVectorElements</span></span>

<span data-ttu-id="d07fb-681">vVectorData</span><span class="sxs-lookup"><span data-stu-id="d07fb-681">vVectorData</span></span>



 

<span data-ttu-id="d07fb-682">**vVectorElements:** entero de 32 bits sin signo, que indica el número de elementos del campo vVectorData.</span><span class="sxs-lookup"><span data-stu-id="d07fb-682">**vVectorElements**: Unsigned 32-bit integer, indicating the number of elements in the vVectorData field.</span></span>

<span data-ttu-id="d07fb-683">**vVectorData:** matriz de elementos que tienen un tipo indicado por vType con el 0x1000 de bits desactivado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-683">**vVectorData**: An array of items which have a type indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="d07fb-684">El tamaño de un elemento de longitud fija individual se puede obtener de la tabla de tipo de datos de longitud fija, como se especifica en la sección 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="d07fb-684">The size of an individual fixed-length item can be obtained from the fixed-length data type table, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="d07fb-685">La longitud de este campo, en bytes, se puede calcular multiplicando vVectorElements por el tamaño de un elemento individual.</span><span class="sxs-lookup"><span data-stu-id="d07fb-685">The length of this field, in bytes, can be calculated by multiplying vVectorElements by the size of individual item.</span></span>

<span data-ttu-id="d07fb-686">En el caso de los tipos de datos de longitud variable, vVectorData contiene una secuencia de tipos simples serializados consecutivamente donde el tipo se indica mediante vType con el 0x1000 bits desactivado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-686">For variable-length data types vVectorData contains a sequence of consecutively marshaled simple types where the type is indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="d07fb-687">Esto incluye un caso especial indicado por vType VT \_ ARRAY \| VT VARIANT \_ (es decir, 0x100C).</span><span class="sxs-lookup"><span data-stu-id="d07fb-687">This includes a special case indicated by vType VT\_ARRAY \| VT\_VARIANT (i.e., 0x100C).</span></span>

<span data-ttu-id="d07fb-688">Los elementos del campo vVectorData DEBEN estar separados por 0 a 3 bytes de relleno, de forma que cada elemento comience en un desplazamiento que sea un múltiplo de 4 bytes desde el principio del mensaje que contiene esta matriz.</span><span class="sxs-lookup"><span data-stu-id="d07fb-688">The elements in the vVectorData field MUST be separated by 0 to 3 padding bytes such that each element begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="d07fb-689">Si hay bytes de relleno, el valor que contienen es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="d07fb-689">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="d07fb-690">El receptor DEBE omitir el contenido de los bytes de relleno.</span><span class="sxs-lookup"><span data-stu-id="d07fb-690">The content of the padding bytes MUST be ignored by the receiver.</span></span>

<span data-ttu-id="d07fb-691">Para un vType establecido en VT ARRAY VT VARIANT, el tipo de los elementos de esta \_ \| secuencia es \_ CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="d07fb-691">For a vType set to VT\_ARRAY \| VT\_VARIANT, the type for items in this sequence is CBaseStorageVariant.</span></span>

### <a name="221113-safearray"></a><span data-ttu-id="d07fb-692">2.2.1.1.1.3 SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="d07fb-692">2.2.1.1.1.3 SAFEARRAY</span></span>

<span data-ttu-id="d07fb-693">SAFEARRAY se usa para pasar matrices multidimensionales.</span><span class="sxs-lookup"><span data-stu-id="d07fb-693">SAFEARRAY is used to pass multidimensional arrays.</span></span> <span data-ttu-id="d07fb-694">La estructura contiene información de tamaño de matriz, así como los datos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="d07fb-694">The structure contains array size information as well as the data in the array.</span></span>



<span data-ttu-id="d07fb-695">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-695">0</span></span>

<span data-ttu-id="d07fb-696">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-696">1</span></span>

<span data-ttu-id="d07fb-697">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-697">2</span></span>

<span data-ttu-id="d07fb-698">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-698">3</span></span>

<span data-ttu-id="d07fb-699">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-699">4</span></span>

<span data-ttu-id="d07fb-700">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-700">5</span></span>

<span data-ttu-id="d07fb-701">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-701">6</span></span>

<span data-ttu-id="d07fb-702">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-702">7</span></span>

<span data-ttu-id="d07fb-703">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-703">8</span></span>

<span data-ttu-id="d07fb-704">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-704">9</span></span>

<span data-ttu-id="d07fb-705">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-705">1</span></span><br/> <span data-ttu-id="d07fb-706">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-706">0</span></span><br/>

<span data-ttu-id="d07fb-707">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-707">1</span></span>

<span data-ttu-id="d07fb-708">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-708">2</span></span>

<span data-ttu-id="d07fb-709">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-709">3</span></span>

<span data-ttu-id="d07fb-710">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-710">4</span></span>

<span data-ttu-id="d07fb-711">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-711">5</span></span>

<span data-ttu-id="d07fb-712">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-712">6</span></span>

<span data-ttu-id="d07fb-713">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-713">7</span></span>

<span data-ttu-id="d07fb-714">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-714">8</span></span>

<span data-ttu-id="d07fb-715">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-715">9</span></span>

<span data-ttu-id="d07fb-716">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-716">2</span></span><br/> <span data-ttu-id="d07fb-717">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-717">0</span></span><br/>

<span data-ttu-id="d07fb-718">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-718">1</span></span>

<span data-ttu-id="d07fb-719">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-719">2</span></span>

<span data-ttu-id="d07fb-720">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-720">3</span></span>

<span data-ttu-id="d07fb-721">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-721">4</span></span>

<span data-ttu-id="d07fb-722">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-722">5</span></span>

<span data-ttu-id="d07fb-723">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-723">6</span></span>

<span data-ttu-id="d07fb-724">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-724">7</span></span>

<span data-ttu-id="d07fb-725">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-725">8</span></span>

<span data-ttu-id="d07fb-726">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-726">9</span></span>

<span data-ttu-id="d07fb-727">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-727">3</span></span><br/> <span data-ttu-id="d07fb-728">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-728">0</span></span><br/>

<span data-ttu-id="d07fb-729">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-729">1</span></span>

<span data-ttu-id="d07fb-730">cDims</span><span class="sxs-lookup"><span data-stu-id="d07fb-730">cDims</span></span>

<span data-ttu-id="d07fb-731">fFeatures</span><span class="sxs-lookup"><span data-stu-id="d07fb-731">fFeatures</span></span>

<span data-ttu-id="d07fb-732">cbElements</span><span class="sxs-lookup"><span data-stu-id="d07fb-732">cbElements</span></span>

<span data-ttu-id="d07fb-733">Rgsabound (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-733">Rgsabound (variable)</span></span>

<span data-ttu-id="d07fb-734">vData (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-734">vData (variable)</span></span>



 

<span data-ttu-id="d07fb-735">**cDims:** entero de 16 bits sin signo, que indica el número de dimensiones de la matriz multidimensional.</span><span class="sxs-lookup"><span data-stu-id="d07fb-735">**cDims**: Unsigned 16-bit integer, indicating the number of dimensions of the multidimensional array.</span></span>

<span data-ttu-id="d07fb-736">**fFeatures:** campo de bits de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d07fb-736">**fFeatures**: A 16-bit bitfield.</span></span> <span data-ttu-id="d07fb-737">Los valores representan características, definidas por aplicaciones de capa superior y DEBEN omitirse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-737">The values represent features, defined by upper layer applications and MUST be ignored.</span></span>

<span data-ttu-id="d07fb-738">**cbElements:** entero de 32 bits sin signo que especifica el tamaño de cada elemento de la matriz.</span><span class="sxs-lookup"><span data-stu-id="d07fb-738">**cbElements**: A 32-bit unsigned integer specifying the size of each element of the array.</span></span>

<span data-ttu-id="d07fb-739">**Rgsabound:** matriz que contiene una estructura SAFEARRAYBOUND, como se especifica en la sección 2.2.1.1.1.4, por dimensión en SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="d07fb-739">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4, per dimension in the SAFEARRAY.</span></span> <span data-ttu-id="d07fb-740">Esta matriz tiene la dimensión más a la izquierda en primer lugar y la dimensión más a la derecha en último lugar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-740">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="d07fb-741">**vData:** vector de elementos serializados de un tipo determinado, indicado por el vType del elemento que contiene CBaseStorageVariant, con el bit 0x2000 borrado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-741">**vData**: A vector of marshaled items of a particular type, indicated by the vType of the containing CBaseStorageVariant, with the bit 0x2000 cleared.</span></span>

<span data-ttu-id="d07fb-742">vData se serializa de forma similar a VT VECTOR, como se especifica en la sección 2.2.1.1.1.2, con la diferencia de que el número de elementos no se almacena delante del \_ vector.</span><span class="sxs-lookup"><span data-stu-id="d07fb-742">vData is marshaled similarly to VT\_VECTOR, as specified in Section 2.2.1.1.1.2, with the difference that the number of items is not stored in front of the vector.</span></span> <span data-ttu-id="d07fb-743">En su lugar, el número de elementos se calcula multiplicando el valor cElements por todos los límites de matriz seguros especificados en el campo Rgsabound.</span><span class="sxs-lookup"><span data-stu-id="d07fb-743">Rather the number of items is calculated by multiplying the cElements value with all safe array bounds given in the Rgsabound field.</span></span> <span data-ttu-id="d07fb-744">Los elementos se almacenan en un vector en orden de dimensiones, iterando a partir de la dimensión más a la derecha.</span><span class="sxs-lookup"><span data-stu-id="d07fb-744">Elements are stored in a vector in order of dimensions, iterating beginning with the right-most dimension.</span></span>

<span data-ttu-id="d07fb-745">El diagrama siguiente representa visualmente una matriz bidimensional de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-745">The following diagram visually represents a sample two-dimensional array.</span></span> <span data-ttu-id="d07fb-746">La primera dimensión tiene cElements igual a 4 (representado horizontalmente) y lLbound igual a 0, y la segunda dimensión tiene cElements igual a 2 (representado verticalmente) y lLbound igual a 0.</span><span class="sxs-lookup"><span data-stu-id="d07fb-746">The first dimension has cElements equal to 4 (represented horizontally) and lLbound equal to 0, and the second dimension has cElements equal to 2 (represented vertically) and lLbound equal to 0.</span></span>



|            |            |            |            |
|------------|------------|------------|------------|
| <span data-ttu-id="d07fb-747">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-747">0x00000001</span></span> | <span data-ttu-id="d07fb-748">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-748">0x00000002</span></span> | <span data-ttu-id="d07fb-749">0x00000003</span><span class="sxs-lookup"><span data-stu-id="d07fb-749">0x00000003</span></span> | <span data-ttu-id="d07fb-750">0x00000005</span><span class="sxs-lookup"><span data-stu-id="d07fb-750">0x00000005</span></span> |
| <span data-ttu-id="d07fb-751">0x00000007</span><span class="sxs-lookup"><span data-stu-id="d07fb-751">0x00000007</span></span> | <span data-ttu-id="d07fb-752">0x00000011</span><span class="sxs-lookup"><span data-stu-id="d07fb-752">0x00000011</span></span> | <span data-ttu-id="d07fb-753">0x00000013</span><span class="sxs-lookup"><span data-stu-id="d07fb-753">0x00000013</span></span> | <span data-ttu-id="d07fb-754">0x00000017</span><span class="sxs-lookup"><span data-stu-id="d07fb-754">0x00000017</span></span> |



 

<span data-ttu-id="d07fb-755">Con el diagrama anterior, vData contendrá la siguiente secuencia: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterando primero por la dimensión situada más a la derecha y, a continuación, incrementando la dimensión siguiente).</span><span class="sxs-lookup"><span data-stu-id="d07fb-755">Using the diagram above, vData will contain the following sequence: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterating through the rightmost dimension first, then incrementing the next dimension).</span></span> <span data-ttu-id="d07fb-756">El Rgsabound anterior (que registra cElements y Lbound) sería: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-756">The preceding Rgsabound (which records cElements and Lbound) would be: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span></span>

### <a name="221114-safearraybound"></a><span data-ttu-id="d07fb-757">2.2.1.1.1.4 SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="d07fb-757">2.2.1.1.1.4 SAFEARRAYBOUND</span></span>

<span data-ttu-id="d07fb-758">La estructura SAFEARRAYBOUND representa los límites de una dimensión de SAFEARRAY o SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="d07fb-758">The SAFEARRAYBOUND structure represents the bounds of one dimension of a SAFEARRAY or SAFEARRAY2.</span></span> <span data-ttu-id="d07fb-759">Su formato es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-759">Its format is:</span></span>



<span data-ttu-id="d07fb-760">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-760">0</span></span>

<span data-ttu-id="d07fb-761">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-761">1</span></span>

<span data-ttu-id="d07fb-762">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-762">2</span></span>

<span data-ttu-id="d07fb-763">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-763">3</span></span>

<span data-ttu-id="d07fb-764">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-764">4</span></span>

<span data-ttu-id="d07fb-765">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-765">5</span></span>

<span data-ttu-id="d07fb-766">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-766">6</span></span>

<span data-ttu-id="d07fb-767">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-767">7</span></span>

<span data-ttu-id="d07fb-768">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-768">8</span></span>

<span data-ttu-id="d07fb-769">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-769">9</span></span>

<span data-ttu-id="d07fb-770">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-770">1</span></span><br/> <span data-ttu-id="d07fb-771">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-771">0</span></span><br/>

<span data-ttu-id="d07fb-772">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-772">1</span></span>

<span data-ttu-id="d07fb-773">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-773">2</span></span>

<span data-ttu-id="d07fb-774">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-774">3</span></span>

<span data-ttu-id="d07fb-775">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-775">4</span></span>

<span data-ttu-id="d07fb-776">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-776">5</span></span>

<span data-ttu-id="d07fb-777">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-777">6</span></span>

<span data-ttu-id="d07fb-778">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-778">7</span></span>

<span data-ttu-id="d07fb-779">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-779">8</span></span>

<span data-ttu-id="d07fb-780">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-780">9</span></span>

<span data-ttu-id="d07fb-781">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-781">2</span></span><br/> <span data-ttu-id="d07fb-782">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-782">0</span></span><br/>

<span data-ttu-id="d07fb-783">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-783">1</span></span>

<span data-ttu-id="d07fb-784">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-784">2</span></span>

<span data-ttu-id="d07fb-785">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-785">3</span></span>

<span data-ttu-id="d07fb-786">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-786">4</span></span>

<span data-ttu-id="d07fb-787">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-787">5</span></span>

<span data-ttu-id="d07fb-788">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-788">6</span></span>

<span data-ttu-id="d07fb-789">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-789">7</span></span>

<span data-ttu-id="d07fb-790">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-790">8</span></span>

<span data-ttu-id="d07fb-791">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-791">9</span></span>

<span data-ttu-id="d07fb-792">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-792">3</span></span><br/> <span data-ttu-id="d07fb-793">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-793">0</span></span><br/>

<span data-ttu-id="d07fb-794">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-794">1</span></span>

<span data-ttu-id="d07fb-795">cElements</span><span class="sxs-lookup"><span data-stu-id="d07fb-795">cElements</span></span>

<span data-ttu-id="d07fb-796">lLbound</span><span class="sxs-lookup"><span data-stu-id="d07fb-796">lLbound</span></span>



 

<span data-ttu-id="d07fb-797">**cElements:** entero de 32 bits sin signo que especifica el número de elementos de la dimensión.</span><span class="sxs-lookup"><span data-stu-id="d07fb-797">**cElements**: A 32-bit unsigned integer, specifying the number of elements in the dimension.</span></span>

<span data-ttu-id="d07fb-798">**lLbound:** entero de 32 bits sin signo que especifica el límite inferior de la dimensión.</span><span class="sxs-lookup"><span data-stu-id="d07fb-798">**lLbound**: A 32-bit unsigned integer, specifying the lower bound of the dimension.</span></span>

### <a name="221115-safearray2"></a><span data-ttu-id="d07fb-799">2.2.1.1.1.5 SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="d07fb-799">2.2.1.1.1.5 SAFEARRAY2</span></span>

<span data-ttu-id="d07fb-800">SAFEARRAY2 se usa para pasar matrices multidimensionales en SERIALIZEDPROPERTYVALUE.</span><span class="sxs-lookup"><span data-stu-id="d07fb-800">SAFEARRAY2 is used to pass multidimensional arrays in SERIALIZEDPROPERTYVALUE.</span></span> <span data-ttu-id="d07fb-801">La estructura contiene información de límites, así como los datos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-801">The structure contains boundary information as well as the data.</span></span>



<span data-ttu-id="d07fb-802">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-802">0</span></span>

<span data-ttu-id="d07fb-803">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-803">1</span></span>

<span data-ttu-id="d07fb-804">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-804">2</span></span>

<span data-ttu-id="d07fb-805">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-805">3</span></span>

<span data-ttu-id="d07fb-806">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-806">4</span></span>

<span data-ttu-id="d07fb-807">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-807">5</span></span>

<span data-ttu-id="d07fb-808">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-808">6</span></span>

<span data-ttu-id="d07fb-809">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-809">7</span></span>

<span data-ttu-id="d07fb-810">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-810">8</span></span>

<span data-ttu-id="d07fb-811">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-811">9</span></span>

<span data-ttu-id="d07fb-812">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-812">1</span></span><br/> <span data-ttu-id="d07fb-813">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-813">0</span></span><br/>

<span data-ttu-id="d07fb-814">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-814">1</span></span>

<span data-ttu-id="d07fb-815">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-815">2</span></span>

<span data-ttu-id="d07fb-816">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-816">3</span></span>

<span data-ttu-id="d07fb-817">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-817">4</span></span>

<span data-ttu-id="d07fb-818">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-818">5</span></span>

<span data-ttu-id="d07fb-819">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-819">6</span></span>

<span data-ttu-id="d07fb-820">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-820">7</span></span>

<span data-ttu-id="d07fb-821">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-821">8</span></span>

<span data-ttu-id="d07fb-822">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-822">9</span></span>

<span data-ttu-id="d07fb-823">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-823">2</span></span><br/> <span data-ttu-id="d07fb-824">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-824">0</span></span><br/>

<span data-ttu-id="d07fb-825">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-825">1</span></span>

<span data-ttu-id="d07fb-826">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-826">2</span></span>

<span data-ttu-id="d07fb-827">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-827">3</span></span>

<span data-ttu-id="d07fb-828">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-828">4</span></span>

<span data-ttu-id="d07fb-829">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-829">5</span></span>

<span data-ttu-id="d07fb-830">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-830">6</span></span>

<span data-ttu-id="d07fb-831">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-831">7</span></span>

<span data-ttu-id="d07fb-832">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-832">8</span></span>

<span data-ttu-id="d07fb-833">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-833">9</span></span>

<span data-ttu-id="d07fb-834">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-834">3</span></span><br/> <span data-ttu-id="d07fb-835">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-835">0</span></span><br/>

<span data-ttu-id="d07fb-836">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-836">1</span></span>

<span data-ttu-id="d07fb-837">cDims</span><span class="sxs-lookup"><span data-stu-id="d07fb-837">cDims</span></span>

<span data-ttu-id="d07fb-838">Rgsabound (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-838">Rgsabound (variable)</span></span>

<span data-ttu-id="d07fb-839">vData (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-839">vData (variable)</span></span>



 

<span data-ttu-id="d07fb-840">**cDims:** entero de 32 bits sin signo, que indica el número de dimensiones de SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="d07fb-840">**cDims**: Unsigned 32-bit integer, indicating the number of dimensions of the SAFEARRAY2.</span></span>

<span data-ttu-id="d07fb-841">**Rgsabound:** matriz que contiene una estructura SAFEARRAYBOUND, como se especifica en la sección 2.2.1.1.1.4 por dimensión de SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="d07fb-841">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4 per dimension in the SAFEARRAY2.</span></span> <span data-ttu-id="d07fb-842">Esta matriz tiene la dimensión más a la izquierda en primer lugar y la última dimensión más a la derecha.</span><span class="sxs-lookup"><span data-stu-id="d07fb-842">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="d07fb-843">**vData:** vector de elementos serializados de un tipo determinado, indicados por dwType de la clase SERIALIZEDPROPERTYVALUE que contiene, con valores de 0x2000 borrados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-843">**vData**: A vector of marshaled items of a particular type, indicated by the dwType of the containing SERIALIZEDPROPERTYVALUE, with bit 0x2000 cleared.</span></span> <span data-ttu-id="d07fb-844">El formato de vData es el mismo que el especificado para el campo vData de SAFEARRAY en la sección 2.2.1.1.1.3.</span><span class="sxs-lookup"><span data-stu-id="d07fb-844">The format of vData the same as that specified for the vData field of SAFEARRAY in Section 2.2.1.1.1.3.</span></span>

### <a name="2212-cfullpropspec"></a><span data-ttu-id="d07fb-845">2.2.1.2 CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="d07fb-845">2.2.1.2 CFullPropSpec</span></span>

<span data-ttu-id="d07fb-846">La estructura CFullPropSpec contiene un GUID del conjunto de propiedades y un identificador de propiedad para identificar de forma única la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-846">The CFullPropSpec structure contains a property set GUID and a property identifier to uniquely identify property.</span></span>



<span data-ttu-id="d07fb-847">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-847">0</span></span>

<span data-ttu-id="d07fb-848">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-848">1</span></span>

<span data-ttu-id="d07fb-849">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-849">2</span></span>

<span data-ttu-id="d07fb-850">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-850">3</span></span>

<span data-ttu-id="d07fb-851">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-851">4</span></span>

<span data-ttu-id="d07fb-852">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-852">5</span></span>

<span data-ttu-id="d07fb-853">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-853">6</span></span>

<span data-ttu-id="d07fb-854">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-854">7</span></span>

<span data-ttu-id="d07fb-855">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-855">8</span></span>

<span data-ttu-id="d07fb-856">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-856">9</span></span>

<span data-ttu-id="d07fb-857">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-857">1</span></span><br/> <span data-ttu-id="d07fb-858">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-858">0</span></span><br/>

<span data-ttu-id="d07fb-859">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-859">1</span></span>

<span data-ttu-id="d07fb-860">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-860">2</span></span>

<span data-ttu-id="d07fb-861">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-861">3</span></span>

<span data-ttu-id="d07fb-862">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-862">4</span></span>

<span data-ttu-id="d07fb-863">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-863">5</span></span>

<span data-ttu-id="d07fb-864">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-864">6</span></span>

<span data-ttu-id="d07fb-865">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-865">7</span></span>

<span data-ttu-id="d07fb-866">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-866">8</span></span>

<span data-ttu-id="d07fb-867">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-867">9</span></span>

<span data-ttu-id="d07fb-868">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-868">2</span></span><br/> <span data-ttu-id="d07fb-869">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-869">0</span></span><br/>

<span data-ttu-id="d07fb-870">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-870">1</span></span>

<span data-ttu-id="d07fb-871">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-871">2</span></span>

<span data-ttu-id="d07fb-872">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-872">3</span></span>

<span data-ttu-id="d07fb-873">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-873">4</span></span>

<span data-ttu-id="d07fb-874">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-874">5</span></span>

<span data-ttu-id="d07fb-875">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-875">6</span></span>

<span data-ttu-id="d07fb-876">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-876">7</span></span>

<span data-ttu-id="d07fb-877">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-877">8</span></span>

<span data-ttu-id="d07fb-878">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-878">9</span></span>

<span data-ttu-id="d07fb-879">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-879">3</span></span><br/> <span data-ttu-id="d07fb-880">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-880">0</span></span><br/>

<span data-ttu-id="d07fb-881">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-881">1</span></span>

<span data-ttu-id="d07fb-882">\_guidPropSet</span><span class="sxs-lookup"><span data-stu-id="d07fb-882">\_guidPropSet</span></span>

<span data-ttu-id="d07fb-883">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-883">...</span></span>

<span data-ttu-id="d07fb-884">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-884">...</span></span>

<span data-ttu-id="d07fb-885">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-885">...</span></span>

<span data-ttu-id="d07fb-886">ulKind</span><span class="sxs-lookup"><span data-stu-id="d07fb-886">ulKind</span></span>

<span data-ttu-id="d07fb-887">PrSpec</span><span class="sxs-lookup"><span data-stu-id="d07fb-887">PrSpec</span></span>

<span data-ttu-id="d07fb-888">Nombre de propiedad (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-888">Property name (variable)</span></span>



 

<span data-ttu-id="d07fb-889">**\_ guidPropSet:** GUID del conjunto de propiedades al que pertenece la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-889">**\_guidPropSet**: The GUID of the property set to which the property belongs.</span></span>

<span data-ttu-id="d07fb-890">**ulKind:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-890">**ulKind**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="d07fb-891">Uno de los siguientes valores, que indica el contenido de PrSpec.</span><span class="sxs-lookup"><span data-stu-id="d07fb-891">One of the following values below, that indicates the contents of PrSpec.</span></span>



| <span data-ttu-id="d07fb-892">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-892">Value</span></span>                                            | <span data-ttu-id="d07fb-893">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-893">Meaning</span></span>                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-894">PRSPEC \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="d07fb-894">PRSPEC\_ LPWSTR</span></span><br/> <span data-ttu-id="d07fb-895">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-895">0x00000000</span></span><br/> | <span data-ttu-id="d07fb-896">El campo PrSpec especifica el número de caracteres que no son NULL en el campo Nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-896">The PrSpec field specifies the number of non-NULL characters in the Property name field.</span></span> |
| <span data-ttu-id="d07fb-897">PRSPEC \_ PROPID</span><span class="sxs-lookup"><span data-stu-id="d07fb-897">PRSPEC\_PROPID</span></span><br/> <span data-ttu-id="d07fb-898">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-898">0x00000001</span></span><br/>  | <span data-ttu-id="d07fb-899">El campo PrSpec especifica el identificador de propiedad (PROPID).</span><span class="sxs-lookup"><span data-stu-id="d07fb-899">The PrSpec field specifies the property ID (PROPID).</span></span>                                     |



 

<span data-ttu-id="d07fb-900">**PrSpec:** entero de 32 bits sin signo con un significado indicado por el campo ulKind.</span><span class="sxs-lookup"><span data-stu-id="d07fb-900">**PrSpec**: A 32-bit unsigned integer with a meaning as indicated by the ulKind field.</span></span>

<span data-ttu-id="d07fb-901">**Nombre de** propiedad: si ulKind se establece en PRSPEC \_ PROPID, este campo NO DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-901">**Property name**: If ulKind is set to PRSPEC\_PROPID, this field MUST NOT be present.</span></span> <span data-ttu-id="d07fb-902">Si ulKind se establece en PRSPEC LPWSTR, este campo DEBE contener una matriz sin mayúsculas y minúsculas de caracteres Unicode no NULL prSpec, que contiene el nombre de la \_ propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-902">If ulKind is set to PRSPEC\_LPWSTR, then this field MUST contain a case-insensitive array of PrSpec non-null Unicode characters, containing the name of the property.</span></span>

### <a name="2213-ccontentrestriction"></a><span data-ttu-id="d07fb-903">2.2.1.3 CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-903">2.2.1.3 CContentRestriction</span></span>

<span data-ttu-id="d07fb-904">La estructura CContentRestriction contiene una cadena que debe coincidir con una propiedad de la caché de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d07fb-904">The CContentRestriction structure contains a string to match for a property in the property cache.</span></span>



<span data-ttu-id="d07fb-905">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-905">0</span></span>

<span data-ttu-id="d07fb-906">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-906">1</span></span>

<span data-ttu-id="d07fb-907">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-907">2</span></span>

<span data-ttu-id="d07fb-908">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-908">3</span></span>

<span data-ttu-id="d07fb-909">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-909">4</span></span>

<span data-ttu-id="d07fb-910">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-910">5</span></span>

<span data-ttu-id="d07fb-911">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-911">6</span></span>

<span data-ttu-id="d07fb-912">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-912">7</span></span>

<span data-ttu-id="d07fb-913">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-913">8</span></span>

<span data-ttu-id="d07fb-914">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-914">9</span></span>

<span data-ttu-id="d07fb-915">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-915">1</span></span><br/> <span data-ttu-id="d07fb-916">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-916">0</span></span><br/>

<span data-ttu-id="d07fb-917">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-917">1</span></span>

<span data-ttu-id="d07fb-918">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-918">2</span></span>

<span data-ttu-id="d07fb-919">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-919">3</span></span>

<span data-ttu-id="d07fb-920">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-920">4</span></span>

<span data-ttu-id="d07fb-921">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-921">5</span></span>

<span data-ttu-id="d07fb-922">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-922">6</span></span>

<span data-ttu-id="d07fb-923">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-923">7</span></span>

<span data-ttu-id="d07fb-924">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-924">8</span></span>

<span data-ttu-id="d07fb-925">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-925">9</span></span>

<span data-ttu-id="d07fb-926">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-926">2</span></span><br/> <span data-ttu-id="d07fb-927">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-927">0</span></span><br/>

<span data-ttu-id="d07fb-928">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-928">1</span></span>

<span data-ttu-id="d07fb-929">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-929">2</span></span>

<span data-ttu-id="d07fb-930">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-930">3</span></span>

<span data-ttu-id="d07fb-931">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-931">4</span></span>

<span data-ttu-id="d07fb-932">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-932">5</span></span>

<span data-ttu-id="d07fb-933">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-933">6</span></span>

<span data-ttu-id="d07fb-934">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-934">7</span></span>

<span data-ttu-id="d07fb-935">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-935">8</span></span>

<span data-ttu-id="d07fb-936">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-936">9</span></span>

<span data-ttu-id="d07fb-937">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-937">3</span></span><br/> <span data-ttu-id="d07fb-938">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-938">0</span></span><br/>

<span data-ttu-id="d07fb-939">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-939">1</span></span>

<span data-ttu-id="d07fb-940">\_Propiedad (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-940">\_Property (variable)</span></span>

<span data-ttu-id="d07fb-941">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-941">...</span></span>

<span data-ttu-id="d07fb-942">Padding1 (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-942">Padding1 (variable)</span></span>

<span data-ttu-id="d07fb-943">CC</span><span class="sxs-lookup"><span data-stu-id="d07fb-943">Cc</span></span>

<span data-ttu-id="d07fb-944">\_pwcsPhrase (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-944">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="d07fb-945">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-945">...</span></span>

<span data-ttu-id="d07fb-946">Padding2 (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-946">Padding2 (variable)</span></span>

<span data-ttu-id="d07fb-947">lcid</span><span class="sxs-lookup"><span data-stu-id="d07fb-947">lcid</span></span>

<span data-ttu-id="d07fb-948">\_ulGenerateMethod</span><span class="sxs-lookup"><span data-stu-id="d07fb-948">\_ulGenerateMethod</span></span>



 

<span data-ttu-id="d07fb-949">**\_ Propiedad**: estructura CFullPropSpec, como se especifica en la sección 2.2.1.2.</span><span class="sxs-lookup"><span data-stu-id="d07fb-949">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2.</span></span> <span data-ttu-id="d07fb-950">Este campo indica la propiedad en la que se va a realizar una operación de coincidencia.</span><span class="sxs-lookup"><span data-stu-id="d07fb-950">This field indicates the property on which to perform a match operation.</span></span>

<span data-ttu-id="d07fb-951">**Padding1:** este campo DEBE tener una longitud de 0 a 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-951">**Padding1**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="d07fb-952">La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="d07fb-952">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="d07fb-953">Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="d07fb-953">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="d07fb-954">El receptor DEBE omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-954">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="d07fb-955">**Cc:** entero de 32 bits sin signo que especifica el número de caracteres en el \_ campo pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="d07fb-955">**Cc**: A 32-bit unsigned integer, specifying the number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="d07fb-956">**\_ pwcsPhrase:** cadena Unicode no terminada en NULL que representa la palabra o frase que se debe coincidir con la propiedad .</span><span class="sxs-lookup"><span data-stu-id="d07fb-956">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="d07fb-957">Este campo NO DEBE estar vacío.</span><span class="sxs-lookup"><span data-stu-id="d07fb-957">This field MUST NOT be empty.</span></span> <span data-ttu-id="d07fb-958">El campo Cc contiene la longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="d07fb-958">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="d07fb-959">**Padding2:** este campo DEBE tener una longitud de 0 a 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-959">**Padding2**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="d07fb-960">La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="d07fb-960">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="d07fb-961">Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="d07fb-961">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="d07fb-962">El receptor DEBE omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-962">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="d07fb-963">**Lcid:** entero de 32 bits sin signo, que indica la configuración regional de pwcsPhrase, como se especifica en el Apéndice A de \_ \[ MS-GPSI. \]</span><span class="sxs-lookup"><span data-stu-id="d07fb-963">**Lcid**: A 32-bit unsigned integer, indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

<span data-ttu-id="d07fb-964">**\_ ulGenerateMethod:** entero de 32 bits sin signo que especifica el método que se usará al generar formularios de palabras alternativos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-964">**\_ulGenerateMethod**: A 32-bit unsigned integer, specifying the method to use when generating alternate word forms</span></span>



| <span data-ttu-id="d07fb-965">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-965">Value</span></span>                                                       | <span data-ttu-id="d07fb-966">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-966">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-967">GENERATE \_ METHOD \_ EXACT</span><span class="sxs-lookup"><span data-stu-id="d07fb-967">GENERATE\_METHOD\_EXACT</span></span><br/> <span data-ttu-id="d07fb-968">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-968">0x00000000</span></span><br/>    | <span data-ttu-id="d07fb-969">Coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-969">Exact match.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d07fb-970">GENERAR \_ PREFIJO DE \_ MÉTODO</span><span class="sxs-lookup"><span data-stu-id="d07fb-970">GENERATE\_METHOD\_PREFIX</span></span><br/> <span data-ttu-id="d07fb-971">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-971">0x00000001</span></span> <br/>  | <span data-ttu-id="d07fb-972">Coincidencia de prefijo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-972">Prefix match.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="d07fb-973">GENERATE \_ METHOD \_ INFLECT</span><span class="sxs-lookup"><span data-stu-id="d07fb-973">GENERATE\_METHOD\_INFLECT</span></span> <br/> <span data-ttu-id="d07fb-974">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-974">0x00000002</span></span><br/> | <span data-ttu-id="d07fb-975">Coincide con las inflexiones de una palabra.</span><span class="sxs-lookup"><span data-stu-id="d07fb-975">Matches inflections of a word.</span></span> <span data-ttu-id="d07fb-976">Una inflexión de una palabra es una variante de la palabra raíz en la misma parte de la voz que se ha modificado según las reglas lingüísticas de un idioma determinado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-976">An inflection of a word is a variant of the root word in the same part of speech that has been modified according to linguistic rules of a given language.</span></span> <span data-ttu-id="d07fb-977">Por ejemplo, las inflexiones del verbo "nado" en inglés incluyen "nada", "nada", "bañón" y "nada".</span><span class="sxs-lookup"><span data-stu-id="d07fb-977">For example, inflections of the verb "swim" in English include "swim", "swims", "swimming", and "swam".</span></span> |



 

### <a name="2214-ckey"></a><span data-ttu-id="d07fb-978">2.2.1.4 CKey</span><span class="sxs-lookup"><span data-stu-id="d07fb-978">2.2.1.4 CKey</span></span>

<span data-ttu-id="d07fb-979">La estructura CKey contiene un valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-979">The CKey structure contains a property value.</span></span>



<span data-ttu-id="d07fb-980">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-980">0</span></span>

<span data-ttu-id="d07fb-981">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-981">1</span></span>

<span data-ttu-id="d07fb-982">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-982">2</span></span>

<span data-ttu-id="d07fb-983">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-983">3</span></span>

<span data-ttu-id="d07fb-984">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-984">4</span></span>

<span data-ttu-id="d07fb-985">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-985">5</span></span>

<span data-ttu-id="d07fb-986">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-986">6</span></span>

<span data-ttu-id="d07fb-987">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-987">7</span></span>

<span data-ttu-id="d07fb-988">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-988">8</span></span>

<span data-ttu-id="d07fb-989">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-989">9</span></span>

<span data-ttu-id="d07fb-990">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-990">1</span></span><br/> <span data-ttu-id="d07fb-991">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-991">0</span></span><br/>

<span data-ttu-id="d07fb-992">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-992">1</span></span>

<span data-ttu-id="d07fb-993">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-993">2</span></span>

<span data-ttu-id="d07fb-994">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-994">3</span></span>

<span data-ttu-id="d07fb-995">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-995">4</span></span>

<span data-ttu-id="d07fb-996">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-996">5</span></span>

<span data-ttu-id="d07fb-997">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-997">6</span></span>

<span data-ttu-id="d07fb-998">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-998">7</span></span>

<span data-ttu-id="d07fb-999">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-999">8</span></span>

<span data-ttu-id="d07fb-1000">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1000">9</span></span>

<span data-ttu-id="d07fb-1001">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1001">2</span></span><br/> <span data-ttu-id="d07fb-1002">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1002">0</span></span><br/>

<span data-ttu-id="d07fb-1003">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1003">1</span></span>

<span data-ttu-id="d07fb-1004">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1004">2</span></span>

<span data-ttu-id="d07fb-1005">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1005">3</span></span>

<span data-ttu-id="d07fb-1006">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1006">4</span></span>

<span data-ttu-id="d07fb-1007">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1007">5</span></span>

<span data-ttu-id="d07fb-1008">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1008">6</span></span>

<span data-ttu-id="d07fb-1009">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1009">7</span></span>

<span data-ttu-id="d07fb-1010">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1010">8</span></span>

<span data-ttu-id="d07fb-1011">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1011">9</span></span>

<span data-ttu-id="d07fb-1012">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1012">3</span></span><br/> <span data-ttu-id="d07fb-1013">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1013">0</span></span><br/>

<span data-ttu-id="d07fb-1014">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1014">1</span></span>

<span data-ttu-id="d07fb-1015">PROPID</span><span class="sxs-lookup"><span data-stu-id="d07fb-1015">PROPID</span></span>

<span data-ttu-id="d07fb-1016">Cb</span><span class="sxs-lookup"><span data-stu-id="d07fb-1016">Cb</span></span>

<span data-ttu-id="d07fb-1017">buf (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1017">buf (variable)</span></span>



 

<span data-ttu-id="d07fb-1018">**PROPID:** entero de 32 bits sin signo que representa el identificador de propiedad como se describe en la sección 1.8.1.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1018">**PROPID**: A 32-bit unsigned integer, representing the property ID as discussed in section 1.8.1.</span></span> <span data-ttu-id="d07fb-1019">Los valores conocidos son:</span><span class="sxs-lookup"><span data-stu-id="d07fb-1019">Well-known values are:</span></span>



| <span data-ttu-id="d07fb-1020">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-1020">Value</span></span>      | <span data-ttu-id="d07fb-1021">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-1021">Meaning</span></span>                                                 |
|------------|---------------------------------------------------------|
| <span data-ttu-id="d07fb-1022">0xffffffff</span><span class="sxs-lookup"><span data-stu-id="d07fb-1022">0xFFFFFFFF</span></span> | <span data-ttu-id="d07fb-1023">Representa un identificador de propiedad no válido y NO SE DEBE usar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1023">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="d07fb-1024">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="d07fb-1024">0xFFFFFFFE</span></span> | <span data-ttu-id="d07fb-1025">Representa un identificador de propiedad no válido y NO SE DEBE usar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1025">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="d07fb-1026">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-1026">0x00000000</span></span> | <span data-ttu-id="d07fb-1027">Representa cualquier identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1027">Represents any property ID.</span></span>                             |



 

<span data-ttu-id="d07fb-1028">**Cb:** entero de 32 bits sin signo que contiene la longitud de buf, en bytes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1028">**Cb**: A 32-bit unsigned integer containing the length of buf, in bytes.</span></span>

<span data-ttu-id="d07fb-1029">**buf:** secuencia de bytes que representa el valor de la propiedad .</span><span class="sxs-lookup"><span data-stu-id="d07fb-1029">**buf**: A sequence of bytes representing the value of the property.</span></span>

### <a name="2215-cinternalpropertyrestriction"></a><span data-ttu-id="d07fb-1030">2.2.1.5 CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-1030">2.2.1.5 CInternalPropertyRestriction</span></span>

<span data-ttu-id="d07fb-1031">La estructura CInternalPropertyRestriction contiene un valor de propiedad que debe coincidir con una operación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1031">The CInternalPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="d07fb-1032">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1032">0</span></span>

<span data-ttu-id="d07fb-1033">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1033">1</span></span>

<span data-ttu-id="d07fb-1034">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1034">2</span></span>

<span data-ttu-id="d07fb-1035">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1035">3</span></span>

<span data-ttu-id="d07fb-1036">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1036">4</span></span>

<span data-ttu-id="d07fb-1037">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1037">5</span></span>

<span data-ttu-id="d07fb-1038">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1038">6</span></span>

<span data-ttu-id="d07fb-1039">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1039">7</span></span>

<span data-ttu-id="d07fb-1040">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1040">8</span></span>

<span data-ttu-id="d07fb-1041">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1041">9</span></span>

<span data-ttu-id="d07fb-1042">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1042">1</span></span><br/> <span data-ttu-id="d07fb-1043">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1043">0</span></span><br/>

<span data-ttu-id="d07fb-1044">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1044">1</span></span>

<span data-ttu-id="d07fb-1045">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1045">2</span></span>

<span data-ttu-id="d07fb-1046">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1046">3</span></span>

<span data-ttu-id="d07fb-1047">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1047">4</span></span>

<span data-ttu-id="d07fb-1048">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1048">5</span></span>

<span data-ttu-id="d07fb-1049">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1049">6</span></span>

<span data-ttu-id="d07fb-1050">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1050">7</span></span>

<span data-ttu-id="d07fb-1051">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1051">8</span></span>

<span data-ttu-id="d07fb-1052">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1052">9</span></span>

<span data-ttu-id="d07fb-1053">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1053">2</span></span><br/> <span data-ttu-id="d07fb-1054">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1054">0</span></span><br/>

<span data-ttu-id="d07fb-1055">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1055">1</span></span>

<span data-ttu-id="d07fb-1056">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1056">2</span></span>

<span data-ttu-id="d07fb-1057">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1057">3</span></span>

<span data-ttu-id="d07fb-1058">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1058">4</span></span>

<span data-ttu-id="d07fb-1059">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1059">5</span></span>

<span data-ttu-id="d07fb-1060">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1060">6</span></span>

<span data-ttu-id="d07fb-1061">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1061">7</span></span>

<span data-ttu-id="d07fb-1062">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1062">8</span></span>

<span data-ttu-id="d07fb-1063">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1063">9</span></span>

<span data-ttu-id="d07fb-1064">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1064">3</span></span><br/> <span data-ttu-id="d07fb-1065">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1065">0</span></span><br/>

<span data-ttu-id="d07fb-1066">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1066">1</span></span>

<span data-ttu-id="d07fb-1067">\_volver a reestechar</span><span class="sxs-lookup"><span data-stu-id="d07fb-1067">\_relop</span></span>

<span data-ttu-id="d07fb-1068">\_Pid</span><span class="sxs-lookup"><span data-stu-id="d07fb-1068">\_pid</span></span>

<span data-ttu-id="d07fb-1069">\_prval (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1069">\_prval (variable)</span></span>

<span data-ttu-id="d07fb-1070">restrictionPresent</span><span class="sxs-lookup"><span data-stu-id="d07fb-1070">restrictionPresent</span></span>

<span data-ttu-id="d07fb-1071">nextRestriction (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1071">nextRestriction (variable)</span></span>



 

<span data-ttu-id="d07fb-1072">**\_ rehard:** entero de 32 bits que especifica la relación que se va a realizar en la propiedad .</span><span class="sxs-lookup"><span data-stu-id="d07fb-1072">**\_relop**: A 32-bit integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="d07fb-1073">DEBE ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="d07fb-1073">MUST be one of the following values:</span></span>



| <span data-ttu-id="d07fb-1074">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-1074">Value</span></span>                 | <span data-ttu-id="d07fb-1075">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-1075">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-1076">PRLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-1076">PRLT 0x00000000</span></span>       | <span data-ttu-id="d07fb-1077">Una comparación menor que.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1077">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="d07fb-1078">Prle 0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-1078">PRLE 0x00000001</span></span>       | <span data-ttu-id="d07fb-1079">Una comparación menor o igual que.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1079">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="d07fb-1080">PrGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-1080">PRGT 0x00000002</span></span>       | <span data-ttu-id="d07fb-1081">Una comparación mayor que.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1081">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="d07fb-1082">PRGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="d07fb-1082">PRGE 0x00000003</span></span>       | <span data-ttu-id="d07fb-1083">Una comparación mayor o igual que.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1083">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="d07fb-1084">Requisitos previos 0x00000004</span><span class="sxs-lookup"><span data-stu-id="d07fb-1084">PREQ 0x00000004</span></span>       | <span data-ttu-id="d07fb-1085">Comparación de igualdad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1085">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="d07fb-1086">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="d07fb-1086">PRNE 0x00000005</span></span>       | <span data-ttu-id="d07fb-1087">Comparación no igual.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1087">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="d07fb-1088">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="d07fb-1088">PRRE 0x00000006</span></span>       | <span data-ttu-id="d07fb-1089">Comparación de expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1089">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="d07fb-1090">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="d07fb-1090">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="d07fb-1091">AND bit a bit que devuelve el operando derecho.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1091">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="d07fb-1092">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="d07fb-1092">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="d07fb-1093">AND bit a bit que devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1093">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="d07fb-1094">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="d07fb-1094">PRAll 0x00000100</span></span>      | <span data-ttu-id="d07fb-1095">La operación se va a realizar en una columna de un conjunto de filas y solo es true si la operación es verdadera para todas las filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1095">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="d07fb-1096">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="d07fb-1096">PRAny 0x00000200</span></span>      | <span data-ttu-id="d07fb-1097">La operación se va a realizar en una columna de un conjunto de filas y es true si la operación es verdadera para cualquier fila.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1097">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="d07fb-1098">**\_ pid:** entero de 32 bits sin signo que representa el identificador de propiedad (vea PROPID en la sección 2.2.1.4).</span><span class="sxs-lookup"><span data-stu-id="d07fb-1098">**\_pid**: A 32-bit unsigned integer, representing the property ID (see PROPID in section 2.2.1.4).</span></span>

<span data-ttu-id="d07fb-1099">**\_ prval:** CBaseStorageVariant que contiene el valor que se relaciona con la propiedad .</span><span class="sxs-lookup"><span data-stu-id="d07fb-1099">**\_prval**: A CBaseStorageVariant containing the value to relate to the property.</span></span>

<span data-ttu-id="d07fb-1100">**restrictionPresent:** valor de byte que indica si el campo nextRestriction está presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1100">**restrictionPresent**: A byte value indicating if the nextRestriction field is present.</span></span> <span data-ttu-id="d07fb-1101">DEBE establecerse en 0x00 o 0x01.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1101">MUST be set to either 0x00 or 0x01.</span></span> <span data-ttu-id="d07fb-1102">Si se establece en 0x01, restrictionPresent indica que el campo nextRestriction está presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1102">If set to 0x01, restrictionPresent indicates that the nextRestriction field is present.</span></span> <span data-ttu-id="d07fb-1103">Si se establece en 0x00, restrictionPresent indica que el campo nextRestriction no está presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1103">If set to 0x00, restrictionPresent indicates that the nextRestriction field is not present.</span></span>

<span data-ttu-id="d07fb-1104">**nextRestriction:** una estructura CRestriction, como se especifica en la sección 2.2.1.16, especificando una restricción adicional.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1104">**nextRestriction**: A CRestriction structure, as specified in section 2.2.1.16, specifying a further restriction.</span></span>

### <a name="2216-cnatlanguagerestriction"></a><span data-ttu-id="d07fb-1105">2.2.1.6 CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-1105">2.2.1.6 CNatLanguageRestriction</span></span>

<span data-ttu-id="d07fb-1106">La estructura CNatLanguageRestriction contiene una coincidencia de consulta **en lenguaje natural** para una propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1106">The CNatLanguageRestriction structure contains a **natural language query** match for a property.</span></span>



<span data-ttu-id="d07fb-1107">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1107">0</span></span>

<span data-ttu-id="d07fb-1108">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1108">1</span></span>

<span data-ttu-id="d07fb-1109">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1109">2</span></span>

<span data-ttu-id="d07fb-1110">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1110">3</span></span>

<span data-ttu-id="d07fb-1111">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1111">4</span></span>

<span data-ttu-id="d07fb-1112">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1112">5</span></span>

<span data-ttu-id="d07fb-1113">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1113">6</span></span>

<span data-ttu-id="d07fb-1114">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1114">7</span></span>

<span data-ttu-id="d07fb-1115">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1115">8</span></span>

<span data-ttu-id="d07fb-1116">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1116">9</span></span>

<span data-ttu-id="d07fb-1117">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1117">1</span></span><br/> <span data-ttu-id="d07fb-1118">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1118">0</span></span><br/>

<span data-ttu-id="d07fb-1119">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1119">1</span></span>

<span data-ttu-id="d07fb-1120">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1120">2</span></span>

<span data-ttu-id="d07fb-1121">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1121">3</span></span>

<span data-ttu-id="d07fb-1122">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1122">4</span></span>

<span data-ttu-id="d07fb-1123">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1123">5</span></span>

<span data-ttu-id="d07fb-1124">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1124">6</span></span>

<span data-ttu-id="d07fb-1125">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1125">7</span></span>

<span data-ttu-id="d07fb-1126">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1126">8</span></span>

<span data-ttu-id="d07fb-1127">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1127">9</span></span>

<span data-ttu-id="d07fb-1128">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1128">2</span></span><br/> <span data-ttu-id="d07fb-1129">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1129">0</span></span><br/>

<span data-ttu-id="d07fb-1130">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1130">1</span></span>

<span data-ttu-id="d07fb-1131">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1131">2</span></span>

<span data-ttu-id="d07fb-1132">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1132">3</span></span>

<span data-ttu-id="d07fb-1133">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1133">4</span></span>

<span data-ttu-id="d07fb-1134">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1134">5</span></span>

<span data-ttu-id="d07fb-1135">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1135">6</span></span>

<span data-ttu-id="d07fb-1136">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1136">7</span></span>

<span data-ttu-id="d07fb-1137">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1137">8</span></span>

<span data-ttu-id="d07fb-1138">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1138">9</span></span>

<span data-ttu-id="d07fb-1139">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1139">3</span></span><br/> <span data-ttu-id="d07fb-1140">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1140">0</span></span><br/>

<span data-ttu-id="d07fb-1141">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1141">1</span></span>

<span data-ttu-id="d07fb-1142">\_Propiedad (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1142">\_Property (variable)</span></span>

<span data-ttu-id="d07fb-1143">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-1143">...</span></span>

<span data-ttu-id="d07fb-1144">\_padding \_ cc (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1144">\_padding\_cc (variable)</span></span>

<span data-ttu-id="d07fb-1145">CC</span><span class="sxs-lookup"><span data-stu-id="d07fb-1145">Cc</span></span>

<span data-ttu-id="d07fb-1146">\_pwcsPhrase (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1146">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="d07fb-1147">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-1147">...</span></span>

<span data-ttu-id="d07fb-1148">\_padding \_ lcid (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1148">\_padding\_lcid (variable)</span></span>

<span data-ttu-id="d07fb-1149">Lcid</span><span class="sxs-lookup"><span data-stu-id="d07fb-1149">Lcid</span></span>



 

<span data-ttu-id="d07fb-1150">**\_ Propiedad**: estructura CFullPropSpec, como se especifica en la sección 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1150">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.3.</span></span> <span data-ttu-id="d07fb-1151">Este campo indica la propiedad en la que se va a realizar la operación de coincidencia.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1151">This field indicates the property on which to perform the match operation.</span></span>

<span data-ttu-id="d07fb-1152">**\_ padding \_ cc:** este campo DEBE tener una longitud de 0 a 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1152">**\_padding\_cc**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="d07fb-1153">La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1153">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="d07fb-1154">Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1154">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="d07fb-1155">El receptor DEBE omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1155">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="d07fb-1156">**Cc:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1156">**Cc**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="d07fb-1157">Número de caracteres del campo \_ pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1157">The number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="d07fb-1158">**\_ pwcsPhrase:** cadena Unicode no terminada en NULL que representa la palabra o frase que se debe coincidir con la propiedad .</span><span class="sxs-lookup"><span data-stu-id="d07fb-1158">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="d07fb-1159">NO DEBE estar vacío.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1159">MUST NOT be empty.</span></span> <span data-ttu-id="d07fb-1160">El campo Cc contiene la longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1160">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="d07fb-1161">**\_ padding \_ lcid:** este campo DEBE tener entre 0 y 3 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1161">**\_padding\_lcid**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="d07fb-1162">La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1162">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="d07fb-1163">Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1163">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="d07fb-1164">El receptor DEBE omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1164">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="d07fb-1165">**Lcid:** entero de 32 bits sin signo que indica la configuración regional de pwcsPhrase, como se especifica en el Apéndice A de \_ \[ MS-GPSI. \]</span><span class="sxs-lookup"><span data-stu-id="d07fb-1165">**Lcid**: A 32-bit unsigned integer indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

### <a name="2217-cnoderestriction"></a><span data-ttu-id="d07fb-1166">2.2.1.7 CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-1166">2.2.1.7 CNodeRestriction</span></span>

<span data-ttu-id="d07fb-1167">La estructura CNodeRestriction contiene una matriz de **nodos de árbol** de comandos que especifican las restricciones para la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1167">The CNodeRestriction structure contains an array of **command tree** nodes that specify the restrictions for the query.</span></span>



<span data-ttu-id="d07fb-1168">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1168">0</span></span>

<span data-ttu-id="d07fb-1169">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1169">1</span></span>

<span data-ttu-id="d07fb-1170">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1170">2</span></span>

<span data-ttu-id="d07fb-1171">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1171">3</span></span>

<span data-ttu-id="d07fb-1172">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1172">4</span></span>

<span data-ttu-id="d07fb-1173">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1173">5</span></span>

<span data-ttu-id="d07fb-1174">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1174">6</span></span>

<span data-ttu-id="d07fb-1175">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1175">7</span></span>

<span data-ttu-id="d07fb-1176">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1176">8</span></span>

<span data-ttu-id="d07fb-1177">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1177">9</span></span>

<span data-ttu-id="d07fb-1178">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1178">1</span></span><br/> <span data-ttu-id="d07fb-1179">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1179">0</span></span><br/>

<span data-ttu-id="d07fb-1180">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1180">1</span></span>

<span data-ttu-id="d07fb-1181">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1181">2</span></span>

<span data-ttu-id="d07fb-1182">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1182">3</span></span>

<span data-ttu-id="d07fb-1183">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1183">4</span></span>

<span data-ttu-id="d07fb-1184">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1184">5</span></span>

<span data-ttu-id="d07fb-1185">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1185">6</span></span>

<span data-ttu-id="d07fb-1186">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1186">7</span></span>

<span data-ttu-id="d07fb-1187">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1187">8</span></span>

<span data-ttu-id="d07fb-1188">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1188">9</span></span>

<span data-ttu-id="d07fb-1189">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1189">2</span></span><br/> <span data-ttu-id="d07fb-1190">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1190">0</span></span><br/>

<span data-ttu-id="d07fb-1191">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1191">1</span></span>

<span data-ttu-id="d07fb-1192">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1192">2</span></span>

<span data-ttu-id="d07fb-1193">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1193">3</span></span>

<span data-ttu-id="d07fb-1194">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1194">4</span></span>

<span data-ttu-id="d07fb-1195">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1195">5</span></span>

<span data-ttu-id="d07fb-1196">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1196">6</span></span>

<span data-ttu-id="d07fb-1197">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1197">7</span></span>

<span data-ttu-id="d07fb-1198">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1198">8</span></span>

<span data-ttu-id="d07fb-1199">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1199">9</span></span>

<span data-ttu-id="d07fb-1200">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1200">3</span></span><br/> <span data-ttu-id="d07fb-1201">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1201">0</span></span><br/>

<span data-ttu-id="d07fb-1202">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1202">1</span></span>

<span data-ttu-id="d07fb-1203">\_cNode</span><span class="sxs-lookup"><span data-stu-id="d07fb-1203">\_cNode</span></span>

<span data-ttu-id="d07fb-1204">\_paNode (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1204">\_paNode (variable)</span></span>



 

<span data-ttu-id="d07fb-1205">**\_ cNode:** entero de 32 bits sin signo que especifica el número de estructuras de CRestriction contenidas en el \_ campo paNode.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1205">**\_cNode**: A 32-bit unsigned integer specifying the number of CRestriction structures contained in the \_paNode field.</span></span>

<span data-ttu-id="d07fb-1206">**\_ paNode:** una matriz de estructuras de CRestriction.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1206">**\_paNode**: An array of CRestriction structures.</span></span> <span data-ttu-id="d07fb-1207">Las estructuras de la matriz DEBEN estar separadas por 0 a 3 bytes de relleno, de forma que cada estructura comience en un desplazamiento que sea un múltiplo de 4 bytes desde el principio del mensaje que contiene esta matriz.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1207">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="d07fb-1208">Si hay bytes de relleno, el valor que contienen es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1208">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="d07fb-1209">El receptor DEBE omitir el contenido de los bytes de relleno.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1209">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="2218-coccrestriction"></a><span data-ttu-id="d07fb-1210">2.2.1.8 COccRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-1210">2.2.1.8 COccRestriction</span></span>

<span data-ttu-id="d07fb-1211">La estructura COccRestriction contiene la ubicación de una palabra en una frase.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1211">The COccRestriction structure contains the location of a word in a phrase.</span></span>



<span data-ttu-id="d07fb-1212">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1212">0</span></span>

<span data-ttu-id="d07fb-1213">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1213">1</span></span>

<span data-ttu-id="d07fb-1214">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1214">2</span></span>

<span data-ttu-id="d07fb-1215">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1215">3</span></span>

<span data-ttu-id="d07fb-1216">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1216">4</span></span>

<span data-ttu-id="d07fb-1217">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1217">5</span></span>

<span data-ttu-id="d07fb-1218">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1218">6</span></span>

<span data-ttu-id="d07fb-1219">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1219">7</span></span>

<span data-ttu-id="d07fb-1220">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1220">8</span></span>

<span data-ttu-id="d07fb-1221">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1221">9</span></span>

<span data-ttu-id="d07fb-1222">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1222">1</span></span><br/> <span data-ttu-id="d07fb-1223">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1223">0</span></span><br/>

<span data-ttu-id="d07fb-1224">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1224">1</span></span>

<span data-ttu-id="d07fb-1225">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1225">2</span></span>

<span data-ttu-id="d07fb-1226">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1226">3</span></span>

<span data-ttu-id="d07fb-1227">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1227">4</span></span>

<span data-ttu-id="d07fb-1228">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1228">5</span></span>

<span data-ttu-id="d07fb-1229">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1229">6</span></span>

<span data-ttu-id="d07fb-1230">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1230">7</span></span>

<span data-ttu-id="d07fb-1231">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1231">8</span></span>

<span data-ttu-id="d07fb-1232">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1232">9</span></span>

<span data-ttu-id="d07fb-1233">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1233">2</span></span><br/> <span data-ttu-id="d07fb-1234">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1234">0</span></span><br/>

<span data-ttu-id="d07fb-1235">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1235">1</span></span>

<span data-ttu-id="d07fb-1236">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1236">2</span></span>

<span data-ttu-id="d07fb-1237">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1237">3</span></span>

<span data-ttu-id="d07fb-1238">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1238">4</span></span>

<span data-ttu-id="d07fb-1239">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1239">5</span></span>

<span data-ttu-id="d07fb-1240">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1240">6</span></span>

<span data-ttu-id="d07fb-1241">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1241">7</span></span>

<span data-ttu-id="d07fb-1242">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1242">8</span></span>

<span data-ttu-id="d07fb-1243">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1243">9</span></span>

<span data-ttu-id="d07fb-1244">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1244">3</span></span><br/> <span data-ttu-id="d07fb-1245">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1245">0</span></span><br/>

<span data-ttu-id="d07fb-1246">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1246">1</span></span>

<span data-ttu-id="d07fb-1247">\_Occ</span><span class="sxs-lookup"><span data-stu-id="d07fb-1247">\_occ</span></span>

<span data-ttu-id="d07fb-1248">\_cPrevNoiseWords</span><span class="sxs-lookup"><span data-stu-id="d07fb-1248">\_cPrevNoiseWords</span></span>

<span data-ttu-id="d07fb-1249">\_cNextNoiseWords</span><span class="sxs-lookup"><span data-stu-id="d07fb-1249">\_cNextNoiseWords</span></span>



 

<span data-ttu-id="d07fb-1250">**\_ occ:** entero de 32 bits sin signo que especifica el desplazamiento de la palabra en una cadena de consulta, en unidades de palabras.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1250">**\_occ**: A 32-bit unsigned integer specifying the offset of the word in a query string, in units of words.</span></span> <span data-ttu-id="d07fb-1251">Una palabra, como se usa en esta especificación, es una unidad de idioma en cualquier configuración regional que lleva significado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1251">A word, as used in this specification, is a unit of language in any locale that carries meaning.</span></span>

<span data-ttu-id="d07fb-1252">**\_ cPrevNoiseWords:** entero de 32 bits sin signo  que contiene el número de palabras que se producen entre esta palabra y la palabra anterior de la frase.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1252">**\_cPrevNoiseWords**: A 32-bit unsigned integer containing the number of **noise words** that occur between this word and the previous word in the phrase.</span></span>

<span data-ttu-id="d07fb-1253">**\_ cNextNoiseWords:** entero de 32 bits sin signo que contiene el número de palabras que se producen entre esta palabra y la siguiente palabra de la frase.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1253">**\_cNextNoiseWords**: A 32-bit unsigned integer containing the number of noise words that occur between this word and the next word in the phrase.</span></span>

### <a name="2219-cpropertyrestriction"></a><span data-ttu-id="d07fb-1254">2.2.1.9 CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-1254">2.2.1.9 CPropertyRestriction</span></span>

<span data-ttu-id="d07fb-1255">La estructura CPropertyRestriction contiene un valor de propiedad que debe coincidir con una operación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1255">The CPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="d07fb-1256">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1256">0</span></span>

<span data-ttu-id="d07fb-1257">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1257">1</span></span>

<span data-ttu-id="d07fb-1258">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1258">2</span></span>

<span data-ttu-id="d07fb-1259">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1259">3</span></span>

<span data-ttu-id="d07fb-1260">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1260">4</span></span>

<span data-ttu-id="d07fb-1261">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1261">5</span></span>

<span data-ttu-id="d07fb-1262">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1262">6</span></span>

<span data-ttu-id="d07fb-1263">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1263">7</span></span>

<span data-ttu-id="d07fb-1264">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1264">8</span></span>

<span data-ttu-id="d07fb-1265">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1265">9</span></span>

<span data-ttu-id="d07fb-1266">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1266">1</span></span><br/> <span data-ttu-id="d07fb-1267">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1267">0</span></span><br/>

<span data-ttu-id="d07fb-1268">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1268">1</span></span>

<span data-ttu-id="d07fb-1269">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1269">2</span></span>

<span data-ttu-id="d07fb-1270">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1270">3</span></span>

<span data-ttu-id="d07fb-1271">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1271">4</span></span>

<span data-ttu-id="d07fb-1272">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1272">5</span></span>

<span data-ttu-id="d07fb-1273">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1273">6</span></span>

<span data-ttu-id="d07fb-1274">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1274">7</span></span>

<span data-ttu-id="d07fb-1275">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1275">8</span></span>

<span data-ttu-id="d07fb-1276">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1276">9</span></span>

<span data-ttu-id="d07fb-1277">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1277">2</span></span><br/> <span data-ttu-id="d07fb-1278">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1278">0</span></span><br/>

<span data-ttu-id="d07fb-1279">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1279">1</span></span>

<span data-ttu-id="d07fb-1280">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1280">2</span></span>

<span data-ttu-id="d07fb-1281">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1281">3</span></span>

<span data-ttu-id="d07fb-1282">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1282">4</span></span>

<span data-ttu-id="d07fb-1283">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1283">5</span></span>

<span data-ttu-id="d07fb-1284">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1284">6</span></span>

<span data-ttu-id="d07fb-1285">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1285">7</span></span>

<span data-ttu-id="d07fb-1286">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1286">8</span></span>

<span data-ttu-id="d07fb-1287">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1287">9</span></span>

<span data-ttu-id="d07fb-1288">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1288">3</span></span><br/> <span data-ttu-id="d07fb-1289">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1289">0</span></span><br/>

<span data-ttu-id="d07fb-1290">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1290">1</span></span>

<span data-ttu-id="d07fb-1291">\_volver a reestechar</span><span class="sxs-lookup"><span data-stu-id="d07fb-1291">\_relop</span></span>

<span data-ttu-id="d07fb-1292">\_Propiedad (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1292">\_Property (variable)</span></span>

<span data-ttu-id="d07fb-1293">\_prval (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1293">\_prval (variable)</span></span>



 

<span data-ttu-id="d07fb-1294">**\_ rehard:** entero de 32 bits sin signo que especifica la relación que se va a realizar en la propiedad .</span><span class="sxs-lookup"><span data-stu-id="d07fb-1294">**\_relop**: A 32-bit unsigned integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="d07fb-1295">DEBE ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1295">MUST be one of the following values.</span></span>



| <span data-ttu-id="d07fb-1296">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-1296">Value</span></span>                 | <span data-ttu-id="d07fb-1297">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-1297">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-1298">PRLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-1298">PRLT 0x00000000</span></span>       | <span data-ttu-id="d07fb-1299">Una comparación menor que.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1299">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="d07fb-1300">Prle 0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-1300">PRLE 0x00000001</span></span>       | <span data-ttu-id="d07fb-1301">Una comparación menor o igual que.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1301">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="d07fb-1302">PrGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-1302">PRGT 0x00000002</span></span>       | <span data-ttu-id="d07fb-1303">Una comparación mayor que.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1303">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="d07fb-1304">PRGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="d07fb-1304">PRGE 0x00000003</span></span>       | <span data-ttu-id="d07fb-1305">Una comparación mayor o igual que.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1305">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="d07fb-1306">Requisitos previos 0x00000004</span><span class="sxs-lookup"><span data-stu-id="d07fb-1306">PREQ 0x00000004</span></span>       | <span data-ttu-id="d07fb-1307">Comparación de igualdad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1307">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="d07fb-1308">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="d07fb-1308">PRNE 0x00000005</span></span>       | <span data-ttu-id="d07fb-1309">Comparación no igual.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1309">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="d07fb-1310">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="d07fb-1310">PRRE 0x00000006</span></span>       | <span data-ttu-id="d07fb-1311">Comparación de expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1311">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="d07fb-1312">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="d07fb-1312">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="d07fb-1313">AND bit a bit que devuelve el operando derecho.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1313">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="d07fb-1314">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="d07fb-1314">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="d07fb-1315">AND bit a bit que devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1315">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="d07fb-1316">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="d07fb-1316">PRAll 0x00000100</span></span>      | <span data-ttu-id="d07fb-1317">La operación se va a realizar en una columna de un conjunto de filas y solo es true si la operación es verdadera para todas las filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1317">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="d07fb-1318">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="d07fb-1318">PRAny 0x00000200</span></span>      | <span data-ttu-id="d07fb-1319">La operación se va a realizar en una columna de un conjunto de filas y es true si la operación es verdadera para cualquier fila.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1319">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="d07fb-1320">**\_ Propiedad**: estructura CFullPropSpec, como se especifica en la sección 2.2.1.2, que indica la propiedad en la que se va a realizar una operación de coincidencia.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1320">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2, indicating the property on which to perform a match operation.</span></span>

<span data-ttu-id="d07fb-1321">**\_ prval:** una estructura CBaseStorageVariant, como se especifica en la sección 2.2.1.1, que contiene el valor que se relaciona con la propiedad .</span><span class="sxs-lookup"><span data-stu-id="d07fb-1321">**\_prval**: A CBaseStorageVariant structure, as specified in Section 2.2.1.1, containing the value to relate to the property.</span></span>

### <a name="22110-crangerestriction"></a><span data-ttu-id="d07fb-1322">2.2.1.10 CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-1322">2.2.1.10 CRangeRestriction</span></span>

<span data-ttu-id="d07fb-1323">La estructura CRangeRestriction contiene una restricción en un intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1323">The CRangeRestriction structure contains a restriction on a range of values.</span></span>



<span data-ttu-id="d07fb-1324">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1324">0</span></span>

<span data-ttu-id="d07fb-1325">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1325">1</span></span>

<span data-ttu-id="d07fb-1326">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1326">2</span></span>

<span data-ttu-id="d07fb-1327">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1327">3</span></span>

<span data-ttu-id="d07fb-1328">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1328">4</span></span>

<span data-ttu-id="d07fb-1329">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1329">5</span></span>

<span data-ttu-id="d07fb-1330">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1330">6</span></span>

<span data-ttu-id="d07fb-1331">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1331">7</span></span>

<span data-ttu-id="d07fb-1332">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1332">8</span></span>

<span data-ttu-id="d07fb-1333">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1333">9</span></span>

<span data-ttu-id="d07fb-1334">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1334">1</span></span><br/> <span data-ttu-id="d07fb-1335">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1335">0</span></span><br/>

<span data-ttu-id="d07fb-1336">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1336">1</span></span>

<span data-ttu-id="d07fb-1337">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1337">2</span></span>

<span data-ttu-id="d07fb-1338">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1338">3</span></span>

<span data-ttu-id="d07fb-1339">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1339">4</span></span>

<span data-ttu-id="d07fb-1340">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1340">5</span></span>

<span data-ttu-id="d07fb-1341">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1341">6</span></span>

<span data-ttu-id="d07fb-1342">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1342">7</span></span>

<span data-ttu-id="d07fb-1343">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1343">8</span></span>

<span data-ttu-id="d07fb-1344">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1344">9</span></span>

<span data-ttu-id="d07fb-1345">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1345">2</span></span><br/> <span data-ttu-id="d07fb-1346">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1346">0</span></span><br/>

<span data-ttu-id="d07fb-1347">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1347">1</span></span>

<span data-ttu-id="d07fb-1348">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1348">2</span></span>

<span data-ttu-id="d07fb-1349">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1349">3</span></span>

<span data-ttu-id="d07fb-1350">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1350">4</span></span>

<span data-ttu-id="d07fb-1351">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1351">5</span></span>

<span data-ttu-id="d07fb-1352">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1352">6</span></span>

<span data-ttu-id="d07fb-1353">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1353">7</span></span>

<span data-ttu-id="d07fb-1354">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1354">8</span></span>

<span data-ttu-id="d07fb-1355">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1355">9</span></span>

<span data-ttu-id="d07fb-1356">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1356">3</span></span><br/> <span data-ttu-id="d07fb-1357">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1357">0</span></span><br/>

<span data-ttu-id="d07fb-1358">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1358">1</span></span>

<span data-ttu-id="d07fb-1359">\_keyStart (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1359">\_keyStart (variable)</span></span>

<span data-ttu-id="d07fb-1360">\_keyEnd (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1360">\_keyEnd (variable)</span></span>



 

<span data-ttu-id="d07fb-1361">**\_ keyStart:** estructura CKey, como se especifica en la sección 2.2.1.4, que contiene el principio del intervalo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1361">**\_keyStart**: A CKey structure, as specified in section 2.2.1.4, containing the beginning of the range.</span></span>

<span data-ttu-id="d07fb-1362">**\_ keyEnd:** estructura CKey que contiene el final del intervalo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1362">**\_keyEnd**: A CKey structure containing the end of the range.</span></span>

### <a name="22111-cscoperestriction"></a><span data-ttu-id="d07fb-1363">2.2.1.11 CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-1363">2.2.1.11 CScopeRestriction</span></span>

<span data-ttu-id="d07fb-1364">La estructura CScopeRestriction contiene una restricción en los archivos que se buscarán.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1364">The CScopeRestriction structure contains a restriction on the files to be searched</span></span>



<span data-ttu-id="d07fb-1365">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1365">0</span></span>

<span data-ttu-id="d07fb-1366">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1366">1</span></span>

<span data-ttu-id="d07fb-1367">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1367">2</span></span>

<span data-ttu-id="d07fb-1368">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1368">3</span></span>

<span data-ttu-id="d07fb-1369">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1369">4</span></span>

<span data-ttu-id="d07fb-1370">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1370">5</span></span>

<span data-ttu-id="d07fb-1371">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1371">6</span></span>

<span data-ttu-id="d07fb-1372">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1372">7</span></span>

<span data-ttu-id="d07fb-1373">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1373">8</span></span>

<span data-ttu-id="d07fb-1374">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1374">9</span></span>

<span data-ttu-id="d07fb-1375">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1375">1</span></span><br/> <span data-ttu-id="d07fb-1376">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1376">0</span></span><br/>

<span data-ttu-id="d07fb-1377">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1377">1</span></span>

<span data-ttu-id="d07fb-1378">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1378">2</span></span>

<span data-ttu-id="d07fb-1379">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1379">3</span></span>

<span data-ttu-id="d07fb-1380">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1380">4</span></span>

<span data-ttu-id="d07fb-1381">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1381">5</span></span>

<span data-ttu-id="d07fb-1382">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1382">6</span></span>

<span data-ttu-id="d07fb-1383">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1383">7</span></span>

<span data-ttu-id="d07fb-1384">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1384">8</span></span>

<span data-ttu-id="d07fb-1385">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1385">9</span></span>

<span data-ttu-id="d07fb-1386">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1386">2</span></span><br/> <span data-ttu-id="d07fb-1387">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1387">0</span></span><br/>

<span data-ttu-id="d07fb-1388">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1388">1</span></span>

<span data-ttu-id="d07fb-1389">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1389">2</span></span>

<span data-ttu-id="d07fb-1390">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1390">3</span></span>

<span data-ttu-id="d07fb-1391">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1391">4</span></span>

<span data-ttu-id="d07fb-1392">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1392">5</span></span>

<span data-ttu-id="d07fb-1393">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1393">6</span></span>

<span data-ttu-id="d07fb-1394">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1394">7</span></span>

<span data-ttu-id="d07fb-1395">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1395">8</span></span>

<span data-ttu-id="d07fb-1396">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1396">9</span></span>

<span data-ttu-id="d07fb-1397">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1397">3</span></span><br/> <span data-ttu-id="d07fb-1398">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1398">0</span></span><br/>

<span data-ttu-id="d07fb-1399">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1399">1</span></span>

<span data-ttu-id="d07fb-1400">CcLowerPath</span><span class="sxs-lookup"><span data-stu-id="d07fb-1400">CcLowerPath</span></span>

<span data-ttu-id="d07fb-1401">\_lowerPath (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1401">\_lowerPath (variable)</span></span>

<span data-ttu-id="d07fb-1402">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-1402">...</span></span>

<span data-ttu-id="d07fb-1403">\_padding (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1403">\_padding ( variable)</span></span>

<span data-ttu-id="d07fb-1404">\_Longitud</span><span class="sxs-lookup"><span data-stu-id="d07fb-1404">\_length</span></span>

<span data-ttu-id="d07fb-1405">\_fRecursive</span><span class="sxs-lookup"><span data-stu-id="d07fb-1405">\_fRecursive</span></span>

<span data-ttu-id="d07fb-1406">\_fVirtual</span><span class="sxs-lookup"><span data-stu-id="d07fb-1406">\_fVirtual</span></span>



 

<span data-ttu-id="d07fb-1407">**CcLowerPath:** entero de 32 bits sin signo que contiene el número de caracteres Unicode en el \_ campo lowerPath.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1407">**CcLowerPath**: A 32-bit unsigned integer containing the number of Unicode characters in the \_lowerPath field.</span></span>

<span data-ttu-id="d07fb-1408">**\_ lowerPath:** cadena Unicode no terminada en NULL que **representa** la ruta de acceso a la que se debe restringir la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1408">**\_lowerPath**: A non null-terminated Unicode string representing the **path** to which the query should be restricted.</span></span> <span data-ttu-id="d07fb-1409">El campo CcLowerPath contiene la longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1409">The CcLowerPath field contains the length of the string.</span></span>

<span data-ttu-id="d07fb-1410">**\_ padding:** este campo DEBE tener una longitud de 0 a 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1410">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="d07fb-1411">La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1411">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="d07fb-1412">Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1412">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="d07fb-1413">El receptor DEBE omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1413">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="d07fb-1414">**\_ length:** entero de 32 bits sin signo que contiene la longitud \_ de lowerPath, en caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1414">**\_length**: A 32-bit unsigned integer containing the length of \_lowerPath, in Unicode characters.</span></span> <span data-ttu-id="d07fb-1415">Debe ser el mismo valor que CcLowerPath.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1415">This MUST be the same value as CcLowerPath.</span></span>

<span data-ttu-id="d07fb-1416">**\_ fRecursive:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1416">**\_fRecursive**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="d07fb-1417">DEBE establecerse en 0x00000001 o 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1417">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="d07fb-1418">Si se establece en 0x00000001, el servidor examinará de forma recursiva todos los subdirectorios de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1418">If set to 0x00000001, the server is to recursively examine all subdirectories of the path.</span></span> <span data-ttu-id="d07fb-1419">Si se establece en 0x00000000, el servidor no examinará ningún subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1419">If set to 0x00000000, the server is to not examine any subdirectories.</span></span>

<span data-ttu-id="d07fb-1420">**\_ fVirtual:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1420">**\_fVirtual**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="d07fb-1421">DEBE establecerse en 0x00000001 o 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1421">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="d07fb-1422">Si se establece en 0x00000001, lowerPath es una ruta de acceso virtual (el localizador uniforme de recursos (URL) asociado a un directorio físico en el sistema de \_ archivos) para un sitio web.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1422">If set to 0x00000001, \_lowerPath is a virtual path (the Uniform Resource Locator (URL) associated with a physical directory on the file system) for a web site.</span></span> <span data-ttu-id="d07fb-1423">Si se establece en 0x00000000, \_ lowerPath es una ruta de acceso del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1423">If set to 0x00000000, \_lowerPath is a file system path.</span></span>

### <a name="22112-csort"></a><span data-ttu-id="d07fb-1424">2.2.1.12 CSort</span><span class="sxs-lookup"><span data-stu-id="d07fb-1424">2.2.1.12 CSort</span></span>

<span data-ttu-id="d07fb-1425">La estructura CSort identifica una columna que se debe ordenar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1425">The CSort structure identifies a column to sort.</span></span>



<span data-ttu-id="d07fb-1426">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1426">0</span></span>

<span data-ttu-id="d07fb-1427">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1427">1</span></span>

<span data-ttu-id="d07fb-1428">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1428">2</span></span>

<span data-ttu-id="d07fb-1429">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1429">3</span></span>

<span data-ttu-id="d07fb-1430">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1430">4</span></span>

<span data-ttu-id="d07fb-1431">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1431">5</span></span>

<span data-ttu-id="d07fb-1432">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1432">6</span></span>

<span data-ttu-id="d07fb-1433">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1433">7</span></span>

<span data-ttu-id="d07fb-1434">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1434">8</span></span>

<span data-ttu-id="d07fb-1435">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1435">9</span></span>

<span data-ttu-id="d07fb-1436">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1436">1</span></span><br/> <span data-ttu-id="d07fb-1437">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1437">0</span></span><br/>

<span data-ttu-id="d07fb-1438">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1438">1</span></span>

<span data-ttu-id="d07fb-1439">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1439">2</span></span>

<span data-ttu-id="d07fb-1440">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1440">3</span></span>

<span data-ttu-id="d07fb-1441">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1441">4</span></span>

<span data-ttu-id="d07fb-1442">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1442">5</span></span>

<span data-ttu-id="d07fb-1443">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1443">6</span></span>

<span data-ttu-id="d07fb-1444">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1444">7</span></span>

<span data-ttu-id="d07fb-1445">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1445">8</span></span>

<span data-ttu-id="d07fb-1446">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1446">9</span></span>

<span data-ttu-id="d07fb-1447">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1447">2</span></span><br/> <span data-ttu-id="d07fb-1448">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1448">0</span></span><br/>

<span data-ttu-id="d07fb-1449">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1449">1</span></span>

<span data-ttu-id="d07fb-1450">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1450">2</span></span>

<span data-ttu-id="d07fb-1451">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1451">3</span></span>

<span data-ttu-id="d07fb-1452">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1452">4</span></span>

<span data-ttu-id="d07fb-1453">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1453">5</span></span>

<span data-ttu-id="d07fb-1454">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1454">6</span></span>

<span data-ttu-id="d07fb-1455">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1455">7</span></span>

<span data-ttu-id="d07fb-1456">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1456">8</span></span>

<span data-ttu-id="d07fb-1457">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1457">9</span></span>

<span data-ttu-id="d07fb-1458">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1458">3</span></span><br/> <span data-ttu-id="d07fb-1459">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1459">0</span></span><br/>

<span data-ttu-id="d07fb-1460">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1460">1</span></span>

<span data-ttu-id="d07fb-1461">pidColumn</span><span class="sxs-lookup"><span data-stu-id="d07fb-1461">pidColumn</span></span>

<span data-ttu-id="d07fb-1462">dwOrder</span><span class="sxs-lookup"><span data-stu-id="d07fb-1462">dwOrder</span></span>

<span data-ttu-id="d07fb-1463">locale</span><span class="sxs-lookup"><span data-stu-id="d07fb-1463">locale</span></span>



 

<span data-ttu-id="d07fb-1464">**pidColumn:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1464">**pidColumn**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="d07fb-1465">Número de la columna por la que se ordenará.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1465">The number of the column to sort by.</span></span>

<span data-ttu-id="d07fb-1466">**dwOrder:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1466">**dwOrder**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="d07fb-1467">DEBE ser uno de los siguientes valores, especificando cómo ordenar en función de la columna.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1467">MUST be one of the following values, specifying how to sort based on the column.</span></span>



| <span data-ttu-id="d07fb-1468">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-1468">Value</span></span>                        | <span data-ttu-id="d07fb-1469">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-1469">Meaning</span></span>                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-1470">Query \_ SORTASCEND 0x00000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-1470">QUERY\_SORTASCEND 0x00000000</span></span> | <span data-ttu-id="d07fb-1471">Las filas deben ordenarse en orden ascendente en función de los valores de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1471">The rows are to be sorted in ascending order based on the values in the column specified.</span></span>  |
| <span data-ttu-id="d07fb-1472">Query \_ DESCEND 0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-1472">QUERY\_DESCEND 0x00000001</span></span>    | <span data-ttu-id="d07fb-1473">Las filas deben ordenarse en orden descendente en función de los valores de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1473">The rows are to be sorted in descending order based on the values in the column specified.</span></span> |



 

<span data-ttu-id="d07fb-1474">**configuración regional:** entero de 32 bits sin signo que indica la configuración regional, como se especifica en el apéndice A de \[ MS-GPSI, \] de la columna.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1474">**locale**: A 32-bit unsigned integer indicating the locale, as specified in \[MS-GPSI\] Appendix A, of the column.</span></span>

### <a name="22113-csynrestriction"></a><span data-ttu-id="d07fb-1475">2.2.1.13 CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-1475">2.2.1.13 CSynRestriction</span></span>

<span data-ttu-id="d07fb-1476">La estructura CSynRestriction contiene una palabra o sus sinónimos para una frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1476">The CSynRestriction structure contains a word or its synonyms for a query phrase.</span></span>



<span data-ttu-id="d07fb-1477">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1477">0</span></span>

<span data-ttu-id="d07fb-1478">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1478">1</span></span>

<span data-ttu-id="d07fb-1479">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1479">2</span></span>

<span data-ttu-id="d07fb-1480">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1480">3</span></span>

<span data-ttu-id="d07fb-1481">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1481">4</span></span>

<span data-ttu-id="d07fb-1482">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1482">5</span></span>

<span data-ttu-id="d07fb-1483">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1483">6</span></span>

<span data-ttu-id="d07fb-1484">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1484">7</span></span>

<span data-ttu-id="d07fb-1485">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1485">8</span></span>

<span data-ttu-id="d07fb-1486">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1486">9</span></span>

<span data-ttu-id="d07fb-1487">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1487">1</span></span><br/> <span data-ttu-id="d07fb-1488">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1488">0</span></span><br/>

<span data-ttu-id="d07fb-1489">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1489">1</span></span>

<span data-ttu-id="d07fb-1490">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1490">2</span></span>

<span data-ttu-id="d07fb-1491">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1491">3</span></span>

<span data-ttu-id="d07fb-1492">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1492">4</span></span>

<span data-ttu-id="d07fb-1493">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1493">5</span></span>

<span data-ttu-id="d07fb-1494">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1494">6</span></span>

<span data-ttu-id="d07fb-1495">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1495">7</span></span>

<span data-ttu-id="d07fb-1496">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1496">8</span></span>

<span data-ttu-id="d07fb-1497">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1497">9</span></span>

<span data-ttu-id="d07fb-1498">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1498">2</span></span><br/> <span data-ttu-id="d07fb-1499">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1499">0</span></span><br/>

<span data-ttu-id="d07fb-1500">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1500">1</span></span>

<span data-ttu-id="d07fb-1501">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1501">2</span></span>

<span data-ttu-id="d07fb-1502">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1502">3</span></span>

<span data-ttu-id="d07fb-1503">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1503">4</span></span>

<span data-ttu-id="d07fb-1504">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1504">5</span></span>

<span data-ttu-id="d07fb-1505">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1505">6</span></span>

<span data-ttu-id="d07fb-1506">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1506">7</span></span>

<span data-ttu-id="d07fb-1507">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1507">8</span></span>

<span data-ttu-id="d07fb-1508">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1508">9</span></span>

<span data-ttu-id="d07fb-1509">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1509">3</span></span><br/> <span data-ttu-id="d07fb-1510">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1510">0</span></span><br/>

<span data-ttu-id="d07fb-1511">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1511">1</span></span>

<span data-ttu-id="d07fb-1512">Restricción</span><span class="sxs-lookup"><span data-stu-id="d07fb-1512">Restriction</span></span>

<span data-ttu-id="d07fb-1513">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-1513">...</span></span>

<span data-ttu-id="d07fb-1514">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-1514">...</span></span>

<span data-ttu-id="d07fb-1515">cKey</span><span class="sxs-lookup"><span data-stu-id="d07fb-1515">cKey</span></span>

<span data-ttu-id="d07fb-1516">\_keyArray (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1516">\_keyArray (variable)</span></span>

<span data-ttu-id="d07fb-1517">\_isRange</span><span class="sxs-lookup"><span data-stu-id="d07fb-1517">\_isRange</span></span>



 

<span data-ttu-id="d07fb-1518">**Restricción:** estructura COccRestriction que especifica la ubicación de la palabra.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1518">**Restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="d07fb-1519">**cKey:** entero de 32 bits sin signo que especifica el número de elementos de la \_ matriz keyArray.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1519">**cKey**: A 32-bit unsigned integer specifying the number of elements in the \_keyArray array.</span></span>

<span data-ttu-id="d07fb-1520">**\_ keyArray:** matriz de estructuras CKey que especifican una palabra y sus sinónimos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1520">**\_keyArray**: An array of CKey structures specifying a word and its synonyms.</span></span>

<span data-ttu-id="d07fb-1521">**\_ isRange:** si se establece en 0x01, las claves son prefijos para coincidir.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1521">**\_isRange**: If set to 0x01, the keys are prefixes to match.</span></span> <span data-ttu-id="d07fb-1522">Si se establece en 0x00, las claves son valores exactos que se van a coincidir.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1522">If set to 0x00, the keys are exact values to match.</span></span> <span data-ttu-id="d07fb-1523">\_isRange NO DEBE establecerse en ningún otro valor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1523">\_isRange MUST NOT be set to any other values.</span></span>

### <a name="22114-cvectorrestriction"></a><span data-ttu-id="d07fb-1524">2.2.1.14 CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-1524">2.2.1.14 CVectorRestriction</span></span>

<span data-ttu-id="d07fb-1525">La estructura CVectorRestriction contiene una operación OR ponderada en un nodo de árbol de comandos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1525">The CVectorRestriction structure contains a weighted OR operation on a command tree node.</span></span>



<span data-ttu-id="d07fb-1526">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1526">0</span></span>

<span data-ttu-id="d07fb-1527">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1527">1</span></span>

<span data-ttu-id="d07fb-1528">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1528">2</span></span>

<span data-ttu-id="d07fb-1529">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1529">3</span></span>

<span data-ttu-id="d07fb-1530">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1530">4</span></span>

<span data-ttu-id="d07fb-1531">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1531">5</span></span>

<span data-ttu-id="d07fb-1532">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1532">6</span></span>

<span data-ttu-id="d07fb-1533">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1533">7</span></span>

<span data-ttu-id="d07fb-1534">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1534">8</span></span>

<span data-ttu-id="d07fb-1535">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1535">9</span></span>

<span data-ttu-id="d07fb-1536">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1536">1</span></span><br/> <span data-ttu-id="d07fb-1537">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1537">0</span></span><br/>

<span data-ttu-id="d07fb-1538">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1538">1</span></span>

<span data-ttu-id="d07fb-1539">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1539">2</span></span>

<span data-ttu-id="d07fb-1540">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1540">3</span></span>

<span data-ttu-id="d07fb-1541">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1541">4</span></span>

<span data-ttu-id="d07fb-1542">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1542">5</span></span>

<span data-ttu-id="d07fb-1543">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1543">6</span></span>

<span data-ttu-id="d07fb-1544">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1544">7</span></span>

<span data-ttu-id="d07fb-1545">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1545">8</span></span>

<span data-ttu-id="d07fb-1546">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1546">9</span></span>

<span data-ttu-id="d07fb-1547">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1547">2</span></span><br/> <span data-ttu-id="d07fb-1548">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1548">0</span></span><br/>

<span data-ttu-id="d07fb-1549">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1549">1</span></span>

<span data-ttu-id="d07fb-1550">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1550">2</span></span>

<span data-ttu-id="d07fb-1551">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1551">3</span></span>

<span data-ttu-id="d07fb-1552">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1552">4</span></span>

<span data-ttu-id="d07fb-1553">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1553">5</span></span>

<span data-ttu-id="d07fb-1554">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1554">6</span></span>

<span data-ttu-id="d07fb-1555">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1555">7</span></span>

<span data-ttu-id="d07fb-1556">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1556">8</span></span>

<span data-ttu-id="d07fb-1557">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1557">9</span></span>

<span data-ttu-id="d07fb-1558">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1558">3</span></span><br/> <span data-ttu-id="d07fb-1559">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1559">0</span></span><br/>

<span data-ttu-id="d07fb-1560">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1560">1</span></span>

<span data-ttu-id="d07fb-1561">\_pres (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1561">\_pres (variable)</span></span>

<span data-ttu-id="d07fb-1562">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-1562">...</span></span>

<span data-ttu-id="d07fb-1563">\_padding (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1563">\_padding (variable)</span></span>

<span data-ttu-id="d07fb-1564">\_ulRankMethod</span><span class="sxs-lookup"><span data-stu-id="d07fb-1564">\_ulRankMethod</span></span>



 

<span data-ttu-id="d07fb-1565">**\_ pres:** árbol de comandos CNodeRestriction en el que se va a realizar una operación OR clasificada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1565">**\_pres**: A CNodeRestriction command tree upon which a ranked OR operation is to be performed.</span></span>

<span data-ttu-id="d07fb-1566">**\_ padding:** este campo DEBE tener una longitud de 0 a 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1566">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="d07fb-1567">La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1567">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="d07fb-1568">Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1568">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="d07fb-1569">El receptor DEBE omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1569">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="d07fb-1570">**\_ ulRankMethod:** entero de 32 bits sin signo que especifica un algoritmo de clasificación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1570">**\_ulRankMethod**: A 32-bit unsigned integer specifying a ranking algorithm.</span></span> <span data-ttu-id="d07fb-1571">DEBE establecerse en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1571">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="d07fb-1572">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-1572">Value</span></span>                            | <span data-ttu-id="d07fb-1573">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-1573">Meaning</span></span>                                       |
|----------------------------------|-----------------------------------------------|
| <span data-ttu-id="d07fb-1574">VECTOR \_ RANK \_ MIN 0x00000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-1574">VECTOR\_RANK\_MIN 0x00000000</span></span>     | <span data-ttu-id="d07fb-1575">Use el algoritmo \[ mínimo SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="d07fb-1575">Use minimum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="d07fb-1576">VECTOR \_ RANK \_ MAX 0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-1576">VECTOR\_RANK\_MAX 0x00000001</span></span>     | <span data-ttu-id="d07fb-1577">Use el algoritmo \[ máximo SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="d07fb-1577">Use maximum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="d07fb-1578">VECTOR \_ RANK \_ INNER 0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-1578">VECTOR\_RANK\_INNER 0x00000002</span></span>   | <span data-ttu-id="d07fb-1579">Use el algoritmo de producto \[ interno SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="d07fb-1579">Use inner product algorithm \[SALTON\].</span></span>       |
| <span data-ttu-id="d07fb-1580">Vector \_ RANK \_ DICE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="d07fb-1580">VECTOR\_RANK\_DICE 0x00000003</span></span>    | <span data-ttu-id="d07fb-1581">Use el algoritmo de coeficiente de \[ dados SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="d07fb-1581">Use Dice coefficient algorithm \[SALTON\].</span></span>    |
| <span data-ttu-id="d07fb-1582">Vector \_ RANK \_ 0X00000004</span><span class="sxs-lookup"><span data-stu-id="d07fb-1582">VECTOR\_RANK\_JACCARD 0x00000004</span></span> | <span data-ttu-id="d07fb-1583">Use el algoritmo de coeficiente deCard \[ SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="d07fb-1583">Use Jaccard coefficient algorithm \[SALTON\].</span></span> |



 

### <a name="22115-cwordrestriction"></a><span data-ttu-id="d07fb-1584">2.2.1.15 CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-1584">2.2.1.15 CWordRestriction</span></span>

<span data-ttu-id="d07fb-1585">La estructura CWordRestriction contiene una palabra para una frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1585">The CWordRestriction structure contains a word for a query phrase.</span></span>



<span data-ttu-id="d07fb-1586">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1586">0</span></span>

<span data-ttu-id="d07fb-1587">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1587">1</span></span>

<span data-ttu-id="d07fb-1588">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1588">2</span></span>

<span data-ttu-id="d07fb-1589">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1589">3</span></span>

<span data-ttu-id="d07fb-1590">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1590">4</span></span>

<span data-ttu-id="d07fb-1591">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1591">5</span></span>

<span data-ttu-id="d07fb-1592">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1592">6</span></span>

<span data-ttu-id="d07fb-1593">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1593">7</span></span>

<span data-ttu-id="d07fb-1594">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1594">8</span></span>

<span data-ttu-id="d07fb-1595">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1595">9</span></span>

<span data-ttu-id="d07fb-1596">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1596">1</span></span><br/> <span data-ttu-id="d07fb-1597">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1597">0</span></span><br/>

<span data-ttu-id="d07fb-1598">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1598">1</span></span>

<span data-ttu-id="d07fb-1599">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1599">2</span></span>

<span data-ttu-id="d07fb-1600">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1600">3</span></span>

<span data-ttu-id="d07fb-1601">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1601">4</span></span>

<span data-ttu-id="d07fb-1602">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1602">5</span></span>

<span data-ttu-id="d07fb-1603">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1603">6</span></span>

<span data-ttu-id="d07fb-1604">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1604">7</span></span>

<span data-ttu-id="d07fb-1605">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1605">8</span></span>

<span data-ttu-id="d07fb-1606">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1606">9</span></span>

<span data-ttu-id="d07fb-1607">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1607">2</span></span><br/> <span data-ttu-id="d07fb-1608">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1608">0</span></span><br/>

<span data-ttu-id="d07fb-1609">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1609">1</span></span>

<span data-ttu-id="d07fb-1610">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1610">2</span></span>

<span data-ttu-id="d07fb-1611">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1611">3</span></span>

<span data-ttu-id="d07fb-1612">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1612">4</span></span>

<span data-ttu-id="d07fb-1613">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1613">5</span></span>

<span data-ttu-id="d07fb-1614">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1614">6</span></span>

<span data-ttu-id="d07fb-1615">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1615">7</span></span>

<span data-ttu-id="d07fb-1616">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1616">8</span></span>

<span data-ttu-id="d07fb-1617">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1617">9</span></span>

<span data-ttu-id="d07fb-1618">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1618">3</span></span><br/> <span data-ttu-id="d07fb-1619">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1619">0</span></span><br/>

<span data-ttu-id="d07fb-1620">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1620">1</span></span>

<span data-ttu-id="d07fb-1621">restricción</span><span class="sxs-lookup"><span data-stu-id="d07fb-1621">restriction</span></span>

<span data-ttu-id="d07fb-1622">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-1622">...</span></span>

<span data-ttu-id="d07fb-1623">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-1623">...</span></span>

<span data-ttu-id="d07fb-1624">\_key (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1624">\_key (variable)</span></span>

<span data-ttu-id="d07fb-1625">\_isRange</span><span class="sxs-lookup"><span data-stu-id="d07fb-1625">\_isRange</span></span>



 

<span data-ttu-id="d07fb-1626">**restriction:** estructura COccRestriction que especifica la ubicación de la palabra.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1626">**restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="d07fb-1627">**\_ key:** estructura CKey que especifica una palabra.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1627">**\_key**: A CKey structure specifying a word.</span></span>

<span data-ttu-id="d07fb-1628">**\_ isRange:** si se establece en 0x01, la clave es un prefijo que debe coincidir.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1628">**\_isRange**: If set to 0x01, the key is a prefix to match.</span></span> <span data-ttu-id="d07fb-1629">Si se establece en 0x00, la clave es un valor exacto que debe coincidir.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1629">If set to 0x00, the key is an exact value to match.</span></span> <span data-ttu-id="d07fb-1630">\_isRange NO DEBE establecerse en ningún otro valor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1630">\_isRange MUST NOT be set to any other value.</span></span>

### <a name="22116-crestriction"></a><span data-ttu-id="d07fb-1631">2.2.1.16 CRestriction</span><span class="sxs-lookup"><span data-stu-id="d07fb-1631">2.2.1.16 CRestriction</span></span>

<span data-ttu-id="d07fb-1632">La estructura CRestriction contiene un nodo de un árbol de comandos de consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1632">The CRestriction structure contains a node of a query command tree.</span></span>



<span data-ttu-id="d07fb-1633">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1633">0</span></span>

<span data-ttu-id="d07fb-1634">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1634">1</span></span>

<span data-ttu-id="d07fb-1635">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1635">2</span></span>

<span data-ttu-id="d07fb-1636">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1636">3</span></span>

<span data-ttu-id="d07fb-1637">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1637">4</span></span>

<span data-ttu-id="d07fb-1638">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1638">5</span></span>

<span data-ttu-id="d07fb-1639">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1639">6</span></span>

<span data-ttu-id="d07fb-1640">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1640">7</span></span>

<span data-ttu-id="d07fb-1641">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1641">8</span></span>

<span data-ttu-id="d07fb-1642">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1642">9</span></span>

<span data-ttu-id="d07fb-1643">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1643">1</span></span><br/> <span data-ttu-id="d07fb-1644">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1644">0</span></span><br/>

<span data-ttu-id="d07fb-1645">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1645">1</span></span>

<span data-ttu-id="d07fb-1646">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1646">2</span></span>

<span data-ttu-id="d07fb-1647">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1647">3</span></span>

<span data-ttu-id="d07fb-1648">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1648">4</span></span>

<span data-ttu-id="d07fb-1649">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1649">5</span></span>

<span data-ttu-id="d07fb-1650">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1650">6</span></span>

<span data-ttu-id="d07fb-1651">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1651">7</span></span>

<span data-ttu-id="d07fb-1652">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1652">8</span></span>

<span data-ttu-id="d07fb-1653">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1653">9</span></span>

<span data-ttu-id="d07fb-1654">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1654">2</span></span><br/> <span data-ttu-id="d07fb-1655">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1655">0</span></span><br/>

<span data-ttu-id="d07fb-1656">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1656">1</span></span>

<span data-ttu-id="d07fb-1657">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1657">2</span></span>

<span data-ttu-id="d07fb-1658">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1658">3</span></span>

<span data-ttu-id="d07fb-1659">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1659">4</span></span>

<span data-ttu-id="d07fb-1660">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1660">5</span></span>

<span data-ttu-id="d07fb-1661">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1661">6</span></span>

<span data-ttu-id="d07fb-1662">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1662">7</span></span>

<span data-ttu-id="d07fb-1663">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1663">8</span></span>

<span data-ttu-id="d07fb-1664">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1664">9</span></span>

<span data-ttu-id="d07fb-1665">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1665">3</span></span><br/> <span data-ttu-id="d07fb-1666">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1666">0</span></span><br/>

<span data-ttu-id="d07fb-1667">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1667">1</span></span>

<span data-ttu-id="d07fb-1668">\_ulType</span><span class="sxs-lookup"><span data-stu-id="d07fb-1668">\_ulType</span></span>

<span data-ttu-id="d07fb-1669">Peso</span><span class="sxs-lookup"><span data-stu-id="d07fb-1669">Weight</span></span>

<span data-ttu-id="d07fb-1670">Restricción</span><span class="sxs-lookup"><span data-stu-id="d07fb-1670">Restriction</span></span>



 

<span data-ttu-id="d07fb-1671">**\_ ulType:** entero de 32 bits sin signo que indica el tipo de restricción utilizado para el nodo de árbol de comandos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1671">**\_ulType**: A 32-bit unsigned integer indicating the restriction type used for the command tree node.</span></span> <span data-ttu-id="d07fb-1672">DEBE establecerse en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1672">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="d07fb-1673">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-1673">Value</span></span>                    | <span data-ttu-id="d07fb-1674">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-1674">Meaning</span></span>                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-1675">RTNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-1675">RTNone 0x00000000</span></span>        | <span data-ttu-id="d07fb-1676">El nodo representa una palabra ruidosa en una consulta vectorial.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1676">The node represents a noise word in a vector query.</span></span>                                         |
| <span data-ttu-id="d07fb-1677">RTAnd 0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-1677">RTAnd 0x00000001</span></span>         | <span data-ttu-id="d07fb-1678">El nodo contiene una CNodeRestriction en la que se va a realizar una operación AND lógica.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1678">The node contains a CNodeRestriction upon which a logical AND operation it to be performed.</span></span> |
| <span data-ttu-id="d07fb-1679">RTOr 0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-1679">RTOr 0x00000002</span></span>          | <span data-ttu-id="d07fb-1680">El nodo contiene una CNodeRestriction en la que se va a realizar una operación OR lógica.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1680">The node contains a CNodeRestriction upon which a logical OR operation is to be performed.</span></span>  |
| <span data-ttu-id="d07fb-1681">RTNot 0x00000003</span><span class="sxs-lookup"><span data-stu-id="d07fb-1681">RTNot 0x00000003</span></span>         | <span data-ttu-id="d07fb-1682">El nodo contiene una CRestriction en la que se va a realizar una operación NOT.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1682">The node contains a CRestriction upon which a NOT operation is to be performed.</span></span>             |
| <span data-ttu-id="d07fb-1683">RTContent 0x00000004</span><span class="sxs-lookup"><span data-stu-id="d07fb-1683">RTContent 0x00000004</span></span>     | <span data-ttu-id="d07fb-1684">El nodo contiene una CContentRestriction.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1684">The node contains a CContentRestriction.</span></span>                                                    |
| <span data-ttu-id="d07fb-1685">RtProperty 0x00000005</span><span class="sxs-lookup"><span data-stu-id="d07fb-1685">RTProperty 0x00000005</span></span>    | <span data-ttu-id="d07fb-1686">El nodo contiene una CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1686">The node contains a CPropertyRestriction.</span></span>                                                   |
| <span data-ttu-id="d07fb-1687">RTProximity 0x00000006</span><span class="sxs-lookup"><span data-stu-id="d07fb-1687">RTProximity 0x00000006</span></span>   | <span data-ttu-id="d07fb-1688">El nodo contiene una CNodeRestriction en la que se va a realizar una clasificación de proximidad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1688">The node contains a CNodeRestriction upon which a proximity ranking is to be performed,</span></span>     |
| <span data-ttu-id="d07fb-1689">RTVector 0x00000007</span><span class="sxs-lookup"><span data-stu-id="d07fb-1689">RTVector 0x00000007</span></span>      | <span data-ttu-id="d07fb-1690">El nodo contiene una CVectorRestriction.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1690">The node contains a CVectorRestriction.</span></span>                                                     |
| <span data-ttu-id="d07fb-1691">RTNatLanguage 0x00000008</span><span class="sxs-lookup"><span data-stu-id="d07fb-1691">RTNatLanguage 0x00000008</span></span> | <span data-ttu-id="d07fb-1692">El nodo contiene una CNatLanguageRestriction.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1692">The node contains a CNatLanguageRestriction.</span></span>                                                |
| <span data-ttu-id="d07fb-1693">RtScope 0x00000009</span><span class="sxs-lookup"><span data-stu-id="d07fb-1693">RTScope 0x00000009</span></span>       | <span data-ttu-id="d07fb-1694">El nodo contiene una CScopeRestriction.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1694">The node contains a CScopeRestriction.</span></span>                                                      |
| <span data-ttu-id="d07fb-1695">PRAny 0xFFFFFFFA</span><span class="sxs-lookup"><span data-stu-id="d07fb-1695">PRAny 0xFFFFFFFA</span></span>         | <span data-ttu-id="d07fb-1696">El nodo contiene un objeto CInternalPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1696">The node contains a CInternalPropertyRestriction.</span></span>                                           |
| <span data-ttu-id="d07fb-1697">RtRange 0xFFFFFFFC</span><span class="sxs-lookup"><span data-stu-id="d07fb-1697">RTRange 0xFFFFFFFC</span></span>       | <span data-ttu-id="d07fb-1698">El nodo contiene una CRangeRestriction.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1698">The node contains a CRangeRestriction.</span></span>                                                      |
| <span data-ttu-id="d07fb-1699">RTPhrase 0xFFFFFFFD</span><span class="sxs-lookup"><span data-stu-id="d07fb-1699">RTPhrase 0xFFFFFFFD</span></span>      | <span data-ttu-id="d07fb-1700">El nodo contiene una CNodeRestriction en la que se va a realizar una coincidencia de frases.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1700">The node contains a CNodeRestriction upon which a phrase match is to be performed.</span></span>          |
| <span data-ttu-id="d07fb-1701">RTSynonym 0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="d07fb-1701">RTSynonym 0xFFFFFFFE</span></span>     | <span data-ttu-id="d07fb-1702">El nodo contiene una CSynRestriction.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1702">The node contains a CSynRestriction.</span></span>                                                        |
| <span data-ttu-id="d07fb-1703">RtWord 0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="d07fb-1703">RTWord 0xFFFFFFFF</span></span>        | <span data-ttu-id="d07fb-1704">El nodo contiene una CWordRestriction.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1704">The node contains a CWordRestriction.</span></span>                                                       |



 

<span data-ttu-id="d07fb-1705">**Peso:** entero de 32 bits sin signo que representa el peso del nodo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1705">**Weight**: A 32-bit unsigned integer representing the weight of the node.</span></span> <span data-ttu-id="d07fb-1706">Peso indica la importancia del nodo con respecto a otros nodos del árbol de comandos de consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1706">Weight indicates the node's importance relative to other nodes in the query command tree.</span></span> <span data-ttu-id="d07fb-1707">Los valores de peso más altos son más importantes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1707">Higher weight values are more important.</span></span>

<span data-ttu-id="d07fb-1708">**Restricción:** tipo de restricción para el nodo de árbol de comandos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1708">**Restriction**: The restriction type for the command tree node.</span></span> <span data-ttu-id="d07fb-1709">La sintaxis DEBE ser tal como se indica en \_ el campo ulType.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1709">The syntax MUST be as indicated by the \_ulType field.</span></span>

### <a name="22117-ccolumnset"></a><span data-ttu-id="d07fb-1710">2.2.1.17 CColumnSet</span><span class="sxs-lookup"><span data-stu-id="d07fb-1710">2.2.1.17 CColumnSet</span></span>

<span data-ttu-id="d07fb-1711">La estructura CColumnSet especifica los números de columna que se devolverán.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1711">The CColumnSet structure specifies the column numbers to be returned.</span></span> <span data-ttu-id="d07fb-1712">Esta estructura siempre se usa en referencia a una estructura CPidMapper específica (sección 2.2.1.23).</span><span class="sxs-lookup"><span data-stu-id="d07fb-1712">This structure is always used in reference to a specific CPidMapper structure (section 2.2.1.23).</span></span>



<span data-ttu-id="d07fb-1713">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1713">0</span></span>

<span data-ttu-id="d07fb-1714">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1714">1</span></span>

<span data-ttu-id="d07fb-1715">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1715">2</span></span>

<span data-ttu-id="d07fb-1716">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1716">3</span></span>

<span data-ttu-id="d07fb-1717">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1717">4</span></span>

<span data-ttu-id="d07fb-1718">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1718">5</span></span>

<span data-ttu-id="d07fb-1719">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1719">6</span></span>

<span data-ttu-id="d07fb-1720">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1720">7</span></span>

<span data-ttu-id="d07fb-1721">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1721">8</span></span>

<span data-ttu-id="d07fb-1722">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1722">9</span></span>

<span data-ttu-id="d07fb-1723">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1723">1</span></span><br/> <span data-ttu-id="d07fb-1724">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1724">0</span></span><br/>

<span data-ttu-id="d07fb-1725">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1725">1</span></span>

<span data-ttu-id="d07fb-1726">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1726">2</span></span>

<span data-ttu-id="d07fb-1727">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1727">3</span></span>

<span data-ttu-id="d07fb-1728">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1728">4</span></span>

<span data-ttu-id="d07fb-1729">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1729">5</span></span>

<span data-ttu-id="d07fb-1730">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1730">6</span></span>

<span data-ttu-id="d07fb-1731">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1731">7</span></span>

<span data-ttu-id="d07fb-1732">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1732">8</span></span>

<span data-ttu-id="d07fb-1733">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1733">9</span></span>

<span data-ttu-id="d07fb-1734">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1734">2</span></span><br/> <span data-ttu-id="d07fb-1735">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1735">0</span></span><br/>

<span data-ttu-id="d07fb-1736">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1736">1</span></span>

<span data-ttu-id="d07fb-1737">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1737">2</span></span>

<span data-ttu-id="d07fb-1738">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1738">3</span></span>

<span data-ttu-id="d07fb-1739">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1739">4</span></span>

<span data-ttu-id="d07fb-1740">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1740">5</span></span>

<span data-ttu-id="d07fb-1741">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1741">6</span></span>

<span data-ttu-id="d07fb-1742">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1742">7</span></span>

<span data-ttu-id="d07fb-1743">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1743">8</span></span>

<span data-ttu-id="d07fb-1744">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1744">9</span></span>

<span data-ttu-id="d07fb-1745">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1745">3</span></span><br/> <span data-ttu-id="d07fb-1746">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1746">0</span></span><br/>

<span data-ttu-id="d07fb-1747">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1747">1</span></span>

<span data-ttu-id="d07fb-1748">count</span><span class="sxs-lookup"><span data-stu-id="d07fb-1748">count</span></span>

<span data-ttu-id="d07fb-1749">índices (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1749">indexes (variable)</span></span>



 

<span data-ttu-id="d07fb-1750">**count:** entero de 32 bits sin signo que especifica el número de elementos de la matriz de índices.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1750">**count**: A 32-bit unsigned integer specifying the number of elements in the indexes array.</span></span>

<span data-ttu-id="d07fb-1751">**indexes:** matriz de enteros sin signo de 4 bytes que representan índices de base cero en la matriz aPropSpec de la estructura CPidMapper correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1751">**indexes**: Array of 4-byte unsigned integers representing zero-based indexes into the aPropSpec array in the corresponding CPidMapper structure.</span></span>

### <a name="22118-ccategorizationset"></a><span data-ttu-id="d07fb-1752">2.2.1.18 CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="d07fb-1752">2.2.1.18 CCategorizationSet</span></span>

<span data-ttu-id="d07fb-1753">La estructura CCategorizationSet contiene información sobre la agrupación de un conjunto de resultados de consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1753">The CCategorizationSet structure contains information about the grouping of a query result set.</span></span>



<span data-ttu-id="d07fb-1754">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1754">0</span></span>

<span data-ttu-id="d07fb-1755">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1755">1</span></span>

<span data-ttu-id="d07fb-1756">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1756">2</span></span>

<span data-ttu-id="d07fb-1757">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1757">3</span></span>

<span data-ttu-id="d07fb-1758">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1758">4</span></span>

<span data-ttu-id="d07fb-1759">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1759">5</span></span>

<span data-ttu-id="d07fb-1760">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1760">6</span></span>

<span data-ttu-id="d07fb-1761">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1761">7</span></span>

<span data-ttu-id="d07fb-1762">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1762">8</span></span>

<span data-ttu-id="d07fb-1763">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1763">9</span></span>

<span data-ttu-id="d07fb-1764">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1764">1</span></span><br/> <span data-ttu-id="d07fb-1765">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1765">0</span></span><br/>

<span data-ttu-id="d07fb-1766">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1766">1</span></span>

<span data-ttu-id="d07fb-1767">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1767">2</span></span>

<span data-ttu-id="d07fb-1768">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1768">3</span></span>

<span data-ttu-id="d07fb-1769">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1769">4</span></span>

<span data-ttu-id="d07fb-1770">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1770">5</span></span>

<span data-ttu-id="d07fb-1771">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1771">6</span></span>

<span data-ttu-id="d07fb-1772">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1772">7</span></span>

<span data-ttu-id="d07fb-1773">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1773">8</span></span>

<span data-ttu-id="d07fb-1774">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1774">9</span></span>

<span data-ttu-id="d07fb-1775">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1775">2</span></span><br/> <span data-ttu-id="d07fb-1776">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1776">0</span></span><br/>

<span data-ttu-id="d07fb-1777">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1777">1</span></span>

<span data-ttu-id="d07fb-1778">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1778">2</span></span>

<span data-ttu-id="d07fb-1779">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1779">3</span></span>

<span data-ttu-id="d07fb-1780">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1780">4</span></span>

<span data-ttu-id="d07fb-1781">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1781">5</span></span>

<span data-ttu-id="d07fb-1782">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1782">6</span></span>

<span data-ttu-id="d07fb-1783">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1783">7</span></span>

<span data-ttu-id="d07fb-1784">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1784">8</span></span>

<span data-ttu-id="d07fb-1785">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1785">9</span></span>

<span data-ttu-id="d07fb-1786">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1786">3</span></span><br/> <span data-ttu-id="d07fb-1787">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1787">0</span></span><br/>

<span data-ttu-id="d07fb-1788">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1788">1</span></span>

<span data-ttu-id="d07fb-1789">count</span><span class="sxs-lookup"><span data-stu-id="d07fb-1789">count</span></span>

<span data-ttu-id="d07fb-1790">categories (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1790">categories (variable)</span></span>



 

<span data-ttu-id="d07fb-1791">**count:** entero de 32 bits sin signo que contiene el número de elementos de la matriz categories.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1791">**count**: A 32-bit unsigned integer containing the number of elements in the categories array.</span></span>

<span data-ttu-id="d07fb-1792">**categories**: matriz de estructuras CCategorizationSpec que especifican la agrupación de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1792">**categories**: Array of CCategorizationSpec structures specifying the grouping of the query.</span></span>

### <a name="22119-ccategorizationspec"></a><span data-ttu-id="d07fb-1793">2.2.1.19 CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="d07fb-1793">2.2.1.19 CCategorizationSpec</span></span>

<span data-ttu-id="d07fb-1794">La estructura CCategorizationSpec contiene una agrupación para un conjunto de resultados de consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1794">The CCategorizationSpec structure contains a grouping for a query result set.</span></span>



<span data-ttu-id="d07fb-1795">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1795">0</span></span>

<span data-ttu-id="d07fb-1796">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1796">1</span></span>

<span data-ttu-id="d07fb-1797">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1797">2</span></span>

<span data-ttu-id="d07fb-1798">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1798">3</span></span>

<span data-ttu-id="d07fb-1799">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1799">4</span></span>

<span data-ttu-id="d07fb-1800">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1800">5</span></span>

<span data-ttu-id="d07fb-1801">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1801">6</span></span>

<span data-ttu-id="d07fb-1802">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1802">7</span></span>

<span data-ttu-id="d07fb-1803">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1803">8</span></span>

<span data-ttu-id="d07fb-1804">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1804">9</span></span>

<span data-ttu-id="d07fb-1805">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1805">1</span></span><br/> <span data-ttu-id="d07fb-1806">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1806">0</span></span><br/>

<span data-ttu-id="d07fb-1807">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1807">1</span></span>

<span data-ttu-id="d07fb-1808">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1808">2</span></span>

<span data-ttu-id="d07fb-1809">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1809">3</span></span>

<span data-ttu-id="d07fb-1810">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1810">4</span></span>

<span data-ttu-id="d07fb-1811">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1811">5</span></span>

<span data-ttu-id="d07fb-1812">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1812">6</span></span>

<span data-ttu-id="d07fb-1813">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1813">7</span></span>

<span data-ttu-id="d07fb-1814">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1814">8</span></span>

<span data-ttu-id="d07fb-1815">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1815">9</span></span>

<span data-ttu-id="d07fb-1816">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1816">2</span></span><br/> <span data-ttu-id="d07fb-1817">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1817">0</span></span><br/>

<span data-ttu-id="d07fb-1818">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1818">1</span></span>

<span data-ttu-id="d07fb-1819">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1819">2</span></span>

<span data-ttu-id="d07fb-1820">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1820">3</span></span>

<span data-ttu-id="d07fb-1821">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1821">4</span></span>

<span data-ttu-id="d07fb-1822">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1822">5</span></span>

<span data-ttu-id="d07fb-1823">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1823">6</span></span>

<span data-ttu-id="d07fb-1824">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1824">7</span></span>

<span data-ttu-id="d07fb-1825">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1825">8</span></span>

<span data-ttu-id="d07fb-1826">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1826">9</span></span>

<span data-ttu-id="d07fb-1827">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1827">3</span></span><br/> <span data-ttu-id="d07fb-1828">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1828">0</span></span><br/>

<span data-ttu-id="d07fb-1829">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1829">1</span></span>

<span data-ttu-id="d07fb-1830">\_csColumns (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1830">\_csColumns (variable)</span></span>

<span data-ttu-id="d07fb-1831">\_ulCategType</span><span class="sxs-lookup"><span data-stu-id="d07fb-1831">\_ulCategType</span></span>



 

<span data-ttu-id="d07fb-1832">**\_ csColumns:** estructura CColumnSet que indica las columnas por las que se va a agrupar la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1832">**\_csColumns**: A CColumnSet structure indicating the columns by which to group the query.</span></span>

<span data-ttu-id="d07fb-1833">**\_ ulCategType:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1833">**\_ulCategType**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="d07fb-1834">DEBE establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1834">MUST be set to 0x00000000.</span></span>

### <a name="22120-cdbcolid"></a><span data-ttu-id="d07fb-1835">2.2.1.20 CDbColId</span><span class="sxs-lookup"><span data-stu-id="d07fb-1835">2.2.1.20 CDbColId</span></span>

<span data-ttu-id="d07fb-1836">La estructura CDbColId contiene una columna.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1836">The CDbColId structure contains a column.</span></span>



<span data-ttu-id="d07fb-1837">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1837">0</span></span>

<span data-ttu-id="d07fb-1838">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1838">1</span></span>

<span data-ttu-id="d07fb-1839">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1839">2</span></span>

<span data-ttu-id="d07fb-1840">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1840">3</span></span>

<span data-ttu-id="d07fb-1841">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1841">4</span></span>

<span data-ttu-id="d07fb-1842">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1842">5</span></span>

<span data-ttu-id="d07fb-1843">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1843">6</span></span>

<span data-ttu-id="d07fb-1844">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1844">7</span></span>

<span data-ttu-id="d07fb-1845">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1845">8</span></span>

<span data-ttu-id="d07fb-1846">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1846">9</span></span>

<span data-ttu-id="d07fb-1847">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1847">1</span></span><br/> <span data-ttu-id="d07fb-1848">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1848">0</span></span><br/>

<span data-ttu-id="d07fb-1849">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1849">1</span></span>

<span data-ttu-id="d07fb-1850">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1850">2</span></span>

<span data-ttu-id="d07fb-1851">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1851">3</span></span>

<span data-ttu-id="d07fb-1852">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1852">4</span></span>

<span data-ttu-id="d07fb-1853">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1853">5</span></span>

<span data-ttu-id="d07fb-1854">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1854">6</span></span>

<span data-ttu-id="d07fb-1855">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1855">7</span></span>

<span data-ttu-id="d07fb-1856">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1856">8</span></span>

<span data-ttu-id="d07fb-1857">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1857">9</span></span>

<span data-ttu-id="d07fb-1858">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1858">2</span></span><br/> <span data-ttu-id="d07fb-1859">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1859">0</span></span><br/>

<span data-ttu-id="d07fb-1860">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1860">1</span></span>

<span data-ttu-id="d07fb-1861">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1861">2</span></span>

<span data-ttu-id="d07fb-1862">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1862">3</span></span>

<span data-ttu-id="d07fb-1863">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1863">4</span></span>

<span data-ttu-id="d07fb-1864">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1864">5</span></span>

<span data-ttu-id="d07fb-1865">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1865">6</span></span>

<span data-ttu-id="d07fb-1866">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1866">7</span></span>

<span data-ttu-id="d07fb-1867">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1867">8</span></span>

<span data-ttu-id="d07fb-1868">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1868">9</span></span>

<span data-ttu-id="d07fb-1869">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1869">3</span></span><br/> <span data-ttu-id="d07fb-1870">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1870">0</span></span><br/>

<span data-ttu-id="d07fb-1871">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1871">1</span></span>

<span data-ttu-id="d07fb-1872">eKind</span><span class="sxs-lookup"><span data-stu-id="d07fb-1872">eKind</span></span>

<span data-ttu-id="d07fb-1873">GUID</span><span class="sxs-lookup"><span data-stu-id="d07fb-1873">GUID</span></span>

<span data-ttu-id="d07fb-1874">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-1874">...</span></span>

<span data-ttu-id="d07fb-1875">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-1875">...</span></span>

<span data-ttu-id="d07fb-1876">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-1876">...</span></span>

<span data-ttu-id="d07fb-1877">ulId</span><span class="sxs-lookup"><span data-stu-id="d07fb-1877">ulId</span></span>

<span data-ttu-id="d07fb-1878">vString (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1878">vString (variable)</span></span>



 

<span data-ttu-id="d07fb-1879">**eKind:** debe establecerse en uno de los valores siguientes que indica el contenido de GUID y vValue.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1879">**eKind**: MUST be set to one of the values below that indicates the contents of GUID and vValue.</span></span>



| <span data-ttu-id="d07fb-1880">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-1880">Value</span></span>                            | <span data-ttu-id="d07fb-1881">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-1881">Meaning</span></span>                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-1882">Nombre del GUID de DBKIND \_ \_ 0x00000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-1882">DBKIND\_GUID\_NAME 0x00000000</span></span>    | <span data-ttu-id="d07fb-1883">vString contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1883">vString contains a property name.</span></span>                                                                               |
| <span data-ttu-id="d07fb-1884">DBKIND \_ GUID \_ PROPID 0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-1884">DBKIND\_GUID\_PROPID 0x00000001</span></span>  | <span data-ttu-id="d07fb-1885">ulId contiene un entero de 4 bytes que indica el identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1885">ulId contains a 4-byte integer indicating the property ID.</span></span>                                                      |
| <span data-ttu-id="d07fb-1886">Nombre \_ de PGUID de DBKIND \_ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="d07fb-1886">DBKIND\_PGUID\_NAME 0x00000003</span></span>   | <span data-ttu-id="d07fb-1887">vString contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1887">vString contains a property name.</span></span> <span data-ttu-id="d07fb-1888">Este valor DEBE tratarse igual que DBKIND \_ GUID \_ NAME.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1888">This value MUST be treated the same as DBKIND\_GUID\_NAME.</span></span>                    |
| <span data-ttu-id="d07fb-1889">DBKIND \_ PGUID \_ PROPID 0x00000004</span><span class="sxs-lookup"><span data-stu-id="d07fb-1889">DBKIND\_PGUID\_PROPID 0x00000004</span></span> | <span data-ttu-id="d07fb-1890">ulId contiene un entero de 4 bytes que indica el identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1890">ulId contains a 4-byte integer indicating the property ID.</span></span> <span data-ttu-id="d07fb-1891">Este valor DEBE ser el mismo que DBKIND \_ GUID \_ PROPID.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1891">This value MUST be the same as DBKIND\_GUID\_PROPID.</span></span> |



 

<span data-ttu-id="d07fb-1892">**GUID:** GUID de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1892">**GUID**: The property GUID.</span></span>

<span data-ttu-id="d07fb-1893">**ulId:** si eKind es DBKIND GUID PROPID o \_ \_ DBKIND \_ PGUID PROPID, este campo contiene un entero sin signo y especifica el identificador \_ de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1893">**ulId**: If eKind is DBKIND\_GUID\_PROPID or DBKIND\_PGUID\_PROPID, this field contains an unsigned integer, specifying the property ID.</span></span> <span data-ttu-id="d07fb-1894">Si eKind es DBKIND GUID NAME o \_ \_ DBKIND PGUID NAME, este campo contiene un entero sin signo que especifica el número de caracteres Unicode contenidos en el \_ \_ campo vString.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1894">If eKind is DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME, this field contains an unsigned integer specifying the number of Unicode characters contained in the vString field.</span></span>

<span data-ttu-id="d07fb-1895">**vString:** cadena Unicode no terminada en NULL que representa el nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1895">**vString**: A non null-terminated Unicode string representing the property name.</span></span> <span data-ttu-id="d07fb-1896">Debe omitirse a menos que el campo eKind esté establecido en DBKIND \_ GUID \_ NAME o DBKIND \_ PGUID \_ NAME.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1896">It MUST be omitted unless the eKind field is set to DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME.</span></span>

### <a name="22121-cdbprop"></a><span data-ttu-id="d07fb-1897">2.2.1.21 CDbProp</span><span class="sxs-lookup"><span data-stu-id="d07fb-1897">2.2.1.21 CDbProp</span></span>

<span data-ttu-id="d07fb-1898">La estructura CDbProp contiene una propiedad .</span><span class="sxs-lookup"><span data-stu-id="d07fb-1898">The CDbProp structure contains a property.</span></span>



<span data-ttu-id="d07fb-1899">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1899">0</span></span>

<span data-ttu-id="d07fb-1900">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1900">1</span></span>

<span data-ttu-id="d07fb-1901">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1901">2</span></span>

<span data-ttu-id="d07fb-1902">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1902">3</span></span>

<span data-ttu-id="d07fb-1903">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1903">4</span></span>

<span data-ttu-id="d07fb-1904">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1904">5</span></span>

<span data-ttu-id="d07fb-1905">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1905">6</span></span>

<span data-ttu-id="d07fb-1906">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1906">7</span></span>

<span data-ttu-id="d07fb-1907">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1907">8</span></span>

<span data-ttu-id="d07fb-1908">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1908">9</span></span>

<span data-ttu-id="d07fb-1909">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1909">1</span></span><br/> <span data-ttu-id="d07fb-1910">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1910">0</span></span><br/>

<span data-ttu-id="d07fb-1911">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1911">1</span></span>

<span data-ttu-id="d07fb-1912">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1912">2</span></span>

<span data-ttu-id="d07fb-1913">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1913">3</span></span>

<span data-ttu-id="d07fb-1914">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1914">4</span></span>

<span data-ttu-id="d07fb-1915">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1915">5</span></span>

<span data-ttu-id="d07fb-1916">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1916">6</span></span>

<span data-ttu-id="d07fb-1917">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1917">7</span></span>

<span data-ttu-id="d07fb-1918">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1918">8</span></span>

<span data-ttu-id="d07fb-1919">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1919">9</span></span>

<span data-ttu-id="d07fb-1920">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1920">2</span></span><br/> <span data-ttu-id="d07fb-1921">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1921">0</span></span><br/>

<span data-ttu-id="d07fb-1922">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1922">1</span></span>

<span data-ttu-id="d07fb-1923">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-1923">2</span></span>

<span data-ttu-id="d07fb-1924">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1924">3</span></span>

<span data-ttu-id="d07fb-1925">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-1925">4</span></span>

<span data-ttu-id="d07fb-1926">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-1926">5</span></span>

<span data-ttu-id="d07fb-1927">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-1927">6</span></span>

<span data-ttu-id="d07fb-1928">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-1928">7</span></span>

<span data-ttu-id="d07fb-1929">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-1929">8</span></span>

<span data-ttu-id="d07fb-1930">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-1930">9</span></span>

<span data-ttu-id="d07fb-1931">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-1931">3</span></span><br/> <span data-ttu-id="d07fb-1932">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-1932">0</span></span><br/>

<span data-ttu-id="d07fb-1933">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-1933">1</span></span>

<span data-ttu-id="d07fb-1934">DBPROPID</span><span class="sxs-lookup"><span data-stu-id="d07fb-1934">DBPROPID</span></span>

<span data-ttu-id="d07fb-1935">DBPROPOPTIONS</span><span class="sxs-lookup"><span data-stu-id="d07fb-1935">DBPROPOPTIONS</span></span>

<span data-ttu-id="d07fb-1936">DBPROPSTATUS</span><span class="sxs-lookup"><span data-stu-id="d07fb-1936">DBPROPSTATUS</span></span>

<span data-ttu-id="d07fb-1937">yd (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1937">colid (variable)</span></span>

<span data-ttu-id="d07fb-1938">vValue (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-1938">vValue (variable)</span></span>



 

<span data-ttu-id="d07fb-1939">**DBPROPID:** entero de 32 bits sin signo que indica el identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1939">**DBPROPID**: A 32-bit unsigned integer, indicating the property ID.</span></span>

<span data-ttu-id="d07fb-1940">**DBPROPOPTIONS:** DEBE establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1940">**DBPROPOPTIONS** : MUST be set to 0x00000000.</span></span>

<span data-ttu-id="d07fb-1941">**DBPROPSTATUS:** DEBE establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1941">**DBPROPSTATUS**: MUST be set to 0x00000000.</span></span>

<span data-ttu-id="d07fb-1942">**: estructura** CDbColId, como se especifica en la sección 2.2.1.20, que indica la columna a la que se aplica la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1942">**colid**: A CDbColId structure, as specified in section 2.2.1.20, indicating the column to which the property applies.</span></span>

<span data-ttu-id="d07fb-1943">**vValue:** CBaseStorageVariant que contiene el valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1943">**vValue**: A CBaseStorageVariant containing the property value.</span></span>

### <a name="221211-properties"></a><span data-ttu-id="d07fb-1944">2.2.1.21.1 Propiedades</span><span class="sxs-lookup"><span data-stu-id="d07fb-1944">2.2.1.21.1 Properties</span></span>

<span data-ttu-id="d07fb-1945">En esta sección se detallan las propiedades que usa CISP.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1945">This section details the properties that are used by CISP.</span></span> <span data-ttu-id="d07fb-1946">Estas propiedades se agrupan en tres conjuntos de propiedades, ident2.2.1.21.1, en el campo guidPropertySet de la estructura CDbPropSet (sección 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="d07fb-1946">These properties are grouped into three property sets, ident2.2.1.21.1 ified in the guidPropertySet field of the CDbPropSet structure (Section 2.2.1.22).</span></span>

<span data-ttu-id="d07fb-1947">En la tabla siguiente se enumeran las propiedades que forman parte del conjunto de propiedades DBPROPSET \_ FSCIFRMWRK \_ EXT.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1947">The following table lists the properties that are part of the DBPROPSET\_FSCIFRMWRK\_EXT property set.</span></span>



| <span data-ttu-id="d07fb-1948">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-1948">Value</span></span>                                  | <span data-ttu-id="d07fb-1949">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-1949">Meaning</span></span>                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-1950">NOMBRE DEL CATÁLOGO DE CI de DBPROP \_ \_ \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-1950">DBPROP\_CI\_CATALOG\_NAME 0x00000002</span></span>   | <span data-ttu-id="d07fb-1951">Especifica el nombre del catálogo o catálogos que se consultan.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1951">Specifies the name of the catalog or catalogs to query.</span></span> <span data-ttu-id="d07fb-1952">El valor DEBE ser VT \_ LPWSTR o VT \_ VECTOR \| VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1952">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR</span></span>                                   |
| <span data-ttu-id="d07fb-1953">ÁMBITOS \_ DE INCLUIR DE DBPROP CI \_ \_ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="d07fb-1953">DBPROP\_CI\_INCLUDE\_SCOPES 0x00000003</span></span> | <span data-ttu-id="d07fb-1954">Especifica una o varias rutas de acceso que se incluirán en la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1954">Specifies one or more paths to be included in the query.</span></span> <span data-ttu-id="d07fb-1955">El valor DEBE ser VT \_ LPWSTR o VT \_ VECTOR \| VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1955">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR.</span></span>                                 |
| <span data-ttu-id="d07fb-1956">MARCAS DE ÁMBITO DE CI DE DBPROP \_ \_ \_ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="d07fb-1956">DBPROP\_CI\_SCOPE\_FLAGS 0x00000004</span></span>    | <span data-ttu-id="d07fb-1957">Especifica cómo se van a tratar las rutas de acceso especificadas por la propiedad \_ DBPROP CI \_ INCLUDE \_ SCOPES.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1957">Specifies how the paths specified by the DBPROP\_CI\_INCLUDE\_SCOPES property are to be treated.</span></span> <span data-ttu-id="d07fb-1958">El valor DEBE ser VT \_ I4 o VT \_ VECTOR VT \| \_ I4.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1958">Value MUST be a VT\_I4 or a VT\_VECTOR \| VT\_I4.</span></span> |
| <span data-ttu-id="d07fb-1959">TIPO DE \_ CONSULTA CI \_ DBPROP \_ 0x00000007</span><span class="sxs-lookup"><span data-stu-id="d07fb-1959">DBPROP\_CI\_QUERY\_TYPE 0x00000007</span></span>     | <span data-ttu-id="d07fb-1960">Especifica el tipo de consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1960">Specifies the type of query.</span></span> <span data-ttu-id="d07fb-1961">CDbColId DEBE establecerse en NULLID de base \_ de datos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1961">The CDbColId MUST be set to DB\_NULLID.</span></span>                                                                               |



 

<span data-ttu-id="d07fb-1962">En la tabla siguiente se enumeran las marcas de la propiedad DBPROP \_ CI \_ SCOPE \_ FLAGS:</span><span class="sxs-lookup"><span data-stu-id="d07fb-1962">The following table lists the flags for the DBPROP\_CI\_SCOPE\_FLAGS property:</span></span>



| <span data-ttu-id="d07fb-1963">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-1963">Value</span></span>                     | <span data-ttu-id="d07fb-1964">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-1964">Meaning</span></span>                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-1965">Consulta \_ en profundidad 0x01</span><span class="sxs-lookup"><span data-stu-id="d07fb-1965">QUERY\_DEEP 0x01</span></span>          | <span data-ttu-id="d07fb-1966">Si se establece, indica que los archivos del directorio de ámbito y todos los subdirectorios se incluyen en los resultados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1966">If set, indicates that files in the scope directory and all subdirectories are included in the results.</span></span> <span data-ttu-id="d07fb-1967">Si está claro, solo los archivos del directorio de ámbito se incluyen en los resultados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1967">If clear, only files in the scope directory are included in the results.</span></span> <span data-ttu-id="d07fb-1968">NO SE DEBE combinar con QUERY \_ DEEP.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1968">MUST NOT be combined with QUERY\_DEEP.</span></span> |
| <span data-ttu-id="d07fb-1969">RUTA \_ DE ACCESO VIRTUAL DE CONSULTA \_ 0x02</span><span class="sxs-lookup"><span data-stu-id="d07fb-1969">QUERY\_VIRTUAL\_PATH 0x02</span></span> | <span data-ttu-id="d07fb-1970">Si se establece, indica que el ámbito es una ruta de acceso virtual.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1970">If set, indicates that the scope is a virtual path.</span></span> <span data-ttu-id="d07fb-1971">Si está claro, indica que el ámbito es un directorio físico.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1971">If clear, indicates that the scope is a physical directory.</span></span>                                                                                                         |



 

<span data-ttu-id="d07fb-1972">En la tabla siguiente se enumeran los tipos de consulta para la propiedad DBPROP \_ CI \_ QUERY \_ TYPE:</span><span class="sxs-lookup"><span data-stu-id="d07fb-1972">The following table lists the query types for the DBPROP\_CI\_QUERY\_TYPE property:</span></span>



| <span data-ttu-id="d07fb-1973">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-1973">Value</span></span>                     | <span data-ttu-id="d07fb-1974">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-1974">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-1975">CiNormal 0x00000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-1975">CiNormal 0x00000000</span></span>       | <span data-ttu-id="d07fb-1976">Una consulta normal.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1976">A regular query.</span></span>                                                                                                   |
| <span data-ttu-id="d07fb-1977">CiVirtualRoots 0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-1977">CiVirtualRoots 0x00000001</span></span> | <span data-ttu-id="d07fb-1978">La consulta solicita una lista de las raíces virtuales del catálogo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1978">The query is requesting a list of the virtual roots of the catalog.</span></span> <span data-ttu-id="d07fb-1979">Este valor requiere privilegios administrativos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1979">This value requires administrative privileges.</span></span> |
| <span data-ttu-id="d07fb-1980">CiProperties 0x00000003</span><span class="sxs-lookup"><span data-stu-id="d07fb-1980">CiProperties 0x00000003</span></span>   | <span data-ttu-id="d07fb-1981">La consulta solicita una lista de todas las propiedades admitidas por el servicio de indexación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1981">The query is requesting a list of all the properties supported by the indexing service.</span></span>                            |
| <span data-ttu-id="d07fb-1982">CiAdminOp 0x00000004</span><span class="sxs-lookup"><span data-stu-id="d07fb-1982">CiAdminOp 0x00000004</span></span>      | <span data-ttu-id="d07fb-1983">La consulta es una operación administrativa.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1983">The query is an administrative operation.</span></span> <span data-ttu-id="d07fb-1984">Este valor requiere privilegios administrativos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1984">This value requires administrative privileges.</span></span>                           |



 

<span data-ttu-id="d07fb-1985">En la tabla siguiente se enumeran las propiedades que forman parte del conjunto de propiedades DBPROPSET \_ QUERYEXT.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1985">The following table lists the properties that are part of the DBPROPSET\_QUERYEXT property set.</span></span>



| <span data-ttu-id="d07fb-1986">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-1986">Value</span></span>                                      | <span data-ttu-id="d07fb-1987">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-1987">Meaning</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-1988">DBPROP \_ USECONTENTINDEX 0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-1988">DBPROP\_USECONTENTINDEX 0x00000002</span></span>         | <span data-ttu-id="d07fb-1989">Especifica cómo el servicio de indexación debe controlar consultas lentas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1989">Specifies how the indexing service is to handle slow queries.</span></span> <span data-ttu-id="d07fb-1990">El valor DEBE ser un \_ VT BOOL.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1990">Value MUST be a VT\_BOOL.</span></span> <span data-ttu-id="d07fb-1991">Si es TRUE, el servidor puede producir un error en estas consultas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1991">If TRUE, the server is allowed to fail these queries.</span></span>                                                                                    |
| <span data-ttu-id="d07fb-1992">DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003</span><span class="sxs-lookup"><span data-stu-id="d07fb-1992">DBPROP\_DEFERNONINDEXEDTRIMMING 0x00000003</span></span> | <span data-ttu-id="d07fb-1993">Indica si el servicio de indexación va a realizar el recorte de resultados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1993">Indicates whether the indexing service is to perform results trimming.</span></span> <span data-ttu-id="d07fb-1994">Si es TRUE, el servidor debe considerar la posibilidad de realizar el recorte de resultados de una manera que optimice el tiempo de respuesta al cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1994">If TRUE, the server is to consider performing results trimming in a way that optimizes response time to the client.</span></span> <span data-ttu-id="d07fb-1995">El valor DEBE ser un \_ VT BOOL.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1995">Value MUST be a VT\_BOOL.</span></span>             |
| <span data-ttu-id="d07fb-1996">DBPROP \_ USEEXTENDEDDBTYPES 0x00000004</span><span class="sxs-lookup"><span data-stu-id="d07fb-1996">DBPROP\_USEEXTENDEDDBTYPES 0x00000004</span></span>      | <span data-ttu-id="d07fb-1997">Indica si el cliente admite tipos de datos VT \_ VECTOR.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1997">Indicates whether the client supports VT\_VECTOR data types.</span></span> <span data-ttu-id="d07fb-1998">Si es TRUE, el cliente admite VT VECTOR; si es FALSE, el servidor va a convertir tipos de datos VT VECTOR en tipos de datos \_ \_ VT \_ ARRAY.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1998">If TRUE, then the client supports VT\_VECTOR; if FALSE, then the server is to convert VT\_VECTOR data types to VT\_ARRAY data types.</span></span>  <span data-ttu-id="d07fb-1999">El valor DEBE ser un \_ VT BOOL.</span><span class="sxs-lookup"><span data-stu-id="d07fb-1999">The value MUST be a VT\_BOOL.</span></span> |
| <span data-ttu-id="d07fb-2000">DBPROP \_ FIRSTROWS 0x00000007</span><span class="sxs-lookup"><span data-stu-id="d07fb-2000">DBPROP\_FIRSTROWS 0x00000007</span></span>               | <span data-ttu-id="d07fb-2001">Indica las coincidencias de fila que se devolverán.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2001">Indicates the row matches to return.</span></span> <span data-ttu-id="d07fb-2002">Si es TRUE, el servidor devolverá el primer conjunto de filas coincidentes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2002">If TRUE, the server is to return the first set of matching rows.</span></span> <span data-ttu-id="d07fb-2003">Si es FALSE, se deben devolver las mejores filas coincidentes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2003">If FALSE, the best matching rows should be returned.</span></span> <span data-ttu-id="d07fb-2004">El valor DEBE ser un \_ VT BOOL.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2004">Value MUST be a VT\_BOOL.</span></span>                                             |



 

<span data-ttu-id="d07fb-2005">En la tabla siguiente se enumeran las propiedades que forman parte del conjunto de propiedades DBPROPSET \_ CIFRMWRKCORE \_ EXT.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2005">The following table lists the properties that are part of the DBPROPSET\_CIFRMWRKCORE\_EXT property set.</span></span>



| <span data-ttu-id="d07fb-2006">Valor/DBPROPID</span><span class="sxs-lookup"><span data-stu-id="d07fb-2006">Value / DBPROPID</span></span>                 | <span data-ttu-id="d07fb-2007">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-2007">Meaning</span></span>                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-2008">DbPROP \_ MACHINE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-2008">DBPROP\_MACHINE 0x00000002</span></span>       | <span data-ttu-id="d07fb-2009">Especifica los nombres de los equipos en los que se va a procesar una consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2009">Specifies the names of the computer(s) on which a query is to be processed.</span></span> <span data-ttu-id="d07fb-2010">El valor DEBE ser VT \_ BSTR o VT \_ ARRAY VT \| \_ BSTR.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2010">The value MUST be either VT\_BSTR or VT\_ARRAY \| VT\_BSTR.</span></span> |
| <span data-ttu-id="d07fb-2011">DBPROP \_ CLIENT \_ CLSID 0x00000003</span><span class="sxs-lookup"><span data-stu-id="d07fb-2011">DBPROP\_CLIENT\_CLSID 0x00000003</span></span> | <span data-ttu-id="d07fb-2012">Especifica una constante de conexión para el servicio de indexación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2012">Specifies a connection constant for the indexing service.</span></span> <span data-ttu-id="d07fb-2013">El valor DEBE ser un \_ CLSID VT que contenga 0x2A4880706FD911D0A80800A0C906241A.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2013">The value MUST be a VT\_CLSID containing 0x2A4880706FD911D0A80800A0C906241A.</span></span>  |



 

### <a name="22122-cdbpropset"></a><span data-ttu-id="d07fb-2014">2.2.1.22 CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="d07fb-2014">2.2.1.22 CDbPropSet</span></span>

<span data-ttu-id="d07fb-2015">La estructura CDbPropSet contiene un conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2015">The CDbPropSet structure contains a set of properties.</span></span> <span data-ttu-id="d07fb-2016">Tenga en cuenta que el primer campo es de tamaño fijo, pero puede que no se alinee en un desplazamiento que sea un múltiplo de 4 bytes desde el inicio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2016">Note that the first field is fixed-size, but may not be aligned at an offset that is a 4-byte multiple from the start of the message containing this structure.</span></span> <span data-ttu-id="d07fb-2017">Sin embargo, el campo cProperties está alineado como tal y, por lo tanto, el formato se representa de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-2017">However, the cProperties field is aligned as such, and hence the format is depicted as follows:</span></span>



<span data-ttu-id="d07fb-2018">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2018">0</span></span>

<span data-ttu-id="d07fb-2019">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2019">1</span></span>

<span data-ttu-id="d07fb-2020">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2020">2</span></span>

<span data-ttu-id="d07fb-2021">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2021">3</span></span>

<span data-ttu-id="d07fb-2022">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2022">4</span></span>

<span data-ttu-id="d07fb-2023">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2023">5</span></span>

<span data-ttu-id="d07fb-2024">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2024">6</span></span>

<span data-ttu-id="d07fb-2025">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2025">7</span></span>

<span data-ttu-id="d07fb-2026">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2026">8</span></span>

<span data-ttu-id="d07fb-2027">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2027">9</span></span>

<span data-ttu-id="d07fb-2028">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2028">1</span></span><br/> <span data-ttu-id="d07fb-2029">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2029">0</span></span><br/>

<span data-ttu-id="d07fb-2030">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2030">1</span></span>

<span data-ttu-id="d07fb-2031">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2031">2</span></span>

<span data-ttu-id="d07fb-2032">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2032">3</span></span>

<span data-ttu-id="d07fb-2033">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2033">4</span></span>

<span data-ttu-id="d07fb-2034">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2034">5</span></span>

<span data-ttu-id="d07fb-2035">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2035">6</span></span>

<span data-ttu-id="d07fb-2036">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2036">7</span></span>

<span data-ttu-id="d07fb-2037">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2037">8</span></span>

<span data-ttu-id="d07fb-2038">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2038">9</span></span>

<span data-ttu-id="d07fb-2039">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2039">2</span></span><br/> <span data-ttu-id="d07fb-2040">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2040">0</span></span><br/>

<span data-ttu-id="d07fb-2041">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2041">1</span></span>

<span data-ttu-id="d07fb-2042">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2042">2</span></span>

<span data-ttu-id="d07fb-2043">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2043">3</span></span>

<span data-ttu-id="d07fb-2044">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2044">4</span></span>

<span data-ttu-id="d07fb-2045">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2045">5</span></span>

<span data-ttu-id="d07fb-2046">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2046">6</span></span>

<span data-ttu-id="d07fb-2047">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2047">7</span></span>

<span data-ttu-id="d07fb-2048">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2048">8</span></span>

<span data-ttu-id="d07fb-2049">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2049">9</span></span>

<span data-ttu-id="d07fb-2050">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2050">3</span></span><br/> <span data-ttu-id="d07fb-2051">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2051">0</span></span><br/>

<span data-ttu-id="d07fb-2052">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2052">1</span></span>

<span data-ttu-id="d07fb-2053">guidPropertySet</span><span class="sxs-lookup"><span data-stu-id="d07fb-2053">guidPropertySet</span></span>

<span data-ttu-id="d07fb-2054">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-2054">...</span></span>

<span data-ttu-id="d07fb-2055">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-2055">...</span></span>

<span data-ttu-id="d07fb-2056">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-2056">...</span></span>

<span data-ttu-id="d07fb-2057">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-2057">...</span></span>

<span data-ttu-id="d07fb-2058">\_padding (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2058">\_padding (variable)</span></span>

<span data-ttu-id="d07fb-2059">cProperties</span><span class="sxs-lookup"><span data-stu-id="d07fb-2059">cProperties</span></span>

<span data-ttu-id="d07fb-2060">aProps (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2060">aProps (variable)</span></span>



 

<span data-ttu-id="d07fb-2061">**guidPropertySet:** GUID que identifica el conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2061">**guidPropertySet**: A GUID identifying the property set.</span></span> <span data-ttu-id="d07fb-2062">DEBE establecerse en el formulario binario correspondiente a uno de los siguientes valores (que se muestra en el formulario de representación de cadena), identificando el conjunto de propiedades de las propiedades contenidas en el campo aProps.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2062">MUST be set to the binary form corresponding to one of the following values (shown in string representation form), identifying the property set of the properties contained in the aProps field.</span></span>



| <span data-ttu-id="d07fb-2063">Valor/GUID</span><span class="sxs-lookup"><span data-stu-id="d07fb-2063">Value / GUID</span></span>                                                                              | <span data-ttu-id="d07fb-2064">Nombre</span><span class="sxs-lookup"><span data-stu-id="d07fb-2064">Name</span></span>                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="d07fb-2065">DBPROPSET \_ FSCIFRMWRK \_ EXT</span><span class="sxs-lookup"><span data-stu-id="d07fb-2065">DBPROPSET\_FSCIFRMWRK\_EXT</span></span><br/> <span data-ttu-id="d07fb-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span><span class="sxs-lookup"><span data-stu-id="d07fb-2066">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span></span><br/>   | <span data-ttu-id="d07fb-2067">Conjunto de propiedades del marco de índice de contenido del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="d07fb-2067">File System Content Index Framework Property Set</span></span> |
| <span data-ttu-id="d07fb-2068">DBPROPSET \_ QUERYEXT</span><span class="sxs-lookup"><span data-stu-id="d07fb-2068">DBPROPSET\_QUERYEXT</span></span><br/> <span data-ttu-id="d07fb-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span><span class="sxs-lookup"><span data-stu-id="d07fb-2069">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span></span><br/>          | <span data-ttu-id="d07fb-2070">Conjunto de propiedades de extensión de consulta</span><span class="sxs-lookup"><span data-stu-id="d07fb-2070">Query Extension Property Set</span></span>                     |
| <span data-ttu-id="d07fb-2071">DBPROPSET \_ CIFRMWRKCORE \_ EXT</span><span class="sxs-lookup"><span data-stu-id="d07fb-2071">DBPROPSET\_CIFRMWRKCORE\_EXT</span></span><br/> <span data-ttu-id="d07fb-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span><span class="sxs-lookup"><span data-stu-id="d07fb-2072">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span></span><br/> | <span data-ttu-id="d07fb-2073">Conjunto de propiedades de Content Index Framework Core</span><span class="sxs-lookup"><span data-stu-id="d07fb-2073">Content Index Framework Core Property Set</span></span>        |



 

<span data-ttu-id="d07fb-2074">**\_ padding:** este campo DEBE tener una longitud de 0 a 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2074">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="d07fb-2075">La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2075">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="d07fb-2076">Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2076">If this field is present (i.e., length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="d07fb-2077">El receptor DEBE omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2077">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="d07fb-2078">**cProperties:** entero de 32 bits sin signo que contiene el número de elementos de la matriz aProps.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2078">**cProperties**: A 32-bit unsigned integer containing the number of elements in the aProps array.</span></span>

<span data-ttu-id="d07fb-2079">**aProps:** una matriz de estructuras CDbProp, como se especifica en la sección 0, que contiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2079">**aProps**: An array of CDbProp structures, as specified in section 0, containing properties.</span></span> <span data-ttu-id="d07fb-2080">Las estructuras de la matriz DEBEN estar separadas por 0 a 3 bytes de relleno, de forma que cada estructura comience en un desplazamiento que sea un múltiplo de 4 bytes desde el principio del mensaje que contiene esta matriz.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2080">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="d07fb-2081">Si hay bytes de relleno, el valor que contienen es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2081">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="d07fb-2082">El receptor DEBE omitir el contenido de los bytes de relleno.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2082">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="22123-cpidmapper"></a><span data-ttu-id="d07fb-2083">2.2.1.23 CPidMapper</span><span class="sxs-lookup"><span data-stu-id="d07fb-2083">2.2.1.23 CPidMapper</span></span>

<span data-ttu-id="d07fb-2084">La estructura CPidMapper contiene una matriz de los IDs de propiedad que especifican las propiedades que se devolverán en un conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2084">The CPidMapper structure contains an array of property IDs specifying the properties to return in a rowset.</span></span>



<span data-ttu-id="d07fb-2085">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2085">0</span></span>

<span data-ttu-id="d07fb-2086">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2086">1</span></span>

<span data-ttu-id="d07fb-2087">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2087">2</span></span>

<span data-ttu-id="d07fb-2088">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2088">3</span></span>

<span data-ttu-id="d07fb-2089">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2089">4</span></span>

<span data-ttu-id="d07fb-2090">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2090">5</span></span>

<span data-ttu-id="d07fb-2091">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2091">6</span></span>

<span data-ttu-id="d07fb-2092">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2092">7</span></span>

<span data-ttu-id="d07fb-2093">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2093">8</span></span>

<span data-ttu-id="d07fb-2094">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2094">9</span></span>

<span data-ttu-id="d07fb-2095">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2095">1</span></span><br/> <span data-ttu-id="d07fb-2096">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2096">0</span></span><br/>

<span data-ttu-id="d07fb-2097">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2097">1</span></span>

<span data-ttu-id="d07fb-2098">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2098">2</span></span>

<span data-ttu-id="d07fb-2099">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2099">3</span></span>

<span data-ttu-id="d07fb-2100">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2100">4</span></span>

<span data-ttu-id="d07fb-2101">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2101">5</span></span>

<span data-ttu-id="d07fb-2102">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2102">6</span></span>

<span data-ttu-id="d07fb-2103">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2103">7</span></span>

<span data-ttu-id="d07fb-2104">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2104">8</span></span>

<span data-ttu-id="d07fb-2105">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2105">9</span></span>

<span data-ttu-id="d07fb-2106">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2106">2</span></span><br/> <span data-ttu-id="d07fb-2107">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2107">0</span></span><br/>

<span data-ttu-id="d07fb-2108">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2108">1</span></span>

<span data-ttu-id="d07fb-2109">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2109">2</span></span>

<span data-ttu-id="d07fb-2110">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2110">3</span></span>

<span data-ttu-id="d07fb-2111">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2111">4</span></span>

<span data-ttu-id="d07fb-2112">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2112">5</span></span>

<span data-ttu-id="d07fb-2113">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2113">6</span></span>

<span data-ttu-id="d07fb-2114">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2114">7</span></span>

<span data-ttu-id="d07fb-2115">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2115">8</span></span>

<span data-ttu-id="d07fb-2116">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2116">9</span></span>

<span data-ttu-id="d07fb-2117">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2117">3</span></span><br/> <span data-ttu-id="d07fb-2118">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2118">0</span></span><br/>

<span data-ttu-id="d07fb-2119">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2119">1</span></span>

<span data-ttu-id="d07fb-2120">count</span><span class="sxs-lookup"><span data-stu-id="d07fb-2120">count</span></span>

<span data-ttu-id="d07fb-2121">aPropSpec</span><span class="sxs-lookup"><span data-stu-id="d07fb-2121">aPropSpec</span></span>

<span data-ttu-id="d07fb-2122">... (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2122">... (variable)</span></span>



 

<span data-ttu-id="d07fb-2123">**count:** entero de 32 bits sin signo que contiene el número de elementos de la matriz aPropSpec.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2123">**count**: A 32-bit unsigned integer containing the number of elements in the aPropSpec array.</span></span>

<span data-ttu-id="d07fb-2124">**aPropSpec:** matriz de estructuras CFullPropSpec que indican las propiedades que se devolverán.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2124">**aPropSpec**: Array of CFullPropSpec structures indicating the properties to return.</span></span> <span data-ttu-id="d07fb-2125">Las estructuras de la matriz DEBEN estar separadas por 0 a 3 bytes de relleno, de forma que cada estructura tenga una alineación de 4 bytes desde el principio de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2125">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="d07fb-2126">Estos bytes de relleno pueden ser cualquier valor arbitrario y DEBEN omitirse al recibirse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2126">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22124-crowseekat"></a><span data-ttu-id="d07fb-2127">2.2.1.24 CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="d07fb-2127">2.2.1.24 CRowSeekAt</span></span>

<span data-ttu-id="d07fb-2128">La estructura CRowSeekAt contiene el desplazamiento en el que se van a recuperar filas en un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2128">The CRowSeekAt structure contains the offset at which to retrieve rows in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="d07fb-2129">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2129">0</span></span>

<span data-ttu-id="d07fb-2130">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2130">1</span></span>

<span data-ttu-id="d07fb-2131">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2131">2</span></span>

<span data-ttu-id="d07fb-2132">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2132">3</span></span>

<span data-ttu-id="d07fb-2133">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2133">4</span></span>

<span data-ttu-id="d07fb-2134">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2134">5</span></span>

<span data-ttu-id="d07fb-2135">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2135">6</span></span>

<span data-ttu-id="d07fb-2136">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2136">7</span></span>

<span data-ttu-id="d07fb-2137">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2137">8</span></span>

<span data-ttu-id="d07fb-2138">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2138">9</span></span>

<span data-ttu-id="d07fb-2139">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2139">1</span></span><br/> <span data-ttu-id="d07fb-2140">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2140">0</span></span><br/>

<span data-ttu-id="d07fb-2141">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2141">1</span></span>

<span data-ttu-id="d07fb-2142">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2142">2</span></span>

<span data-ttu-id="d07fb-2143">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2143">3</span></span>

<span data-ttu-id="d07fb-2144">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2144">4</span></span>

<span data-ttu-id="d07fb-2145">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2145">5</span></span>

<span data-ttu-id="d07fb-2146">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2146">6</span></span>

<span data-ttu-id="d07fb-2147">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2147">7</span></span>

<span data-ttu-id="d07fb-2148">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2148">8</span></span>

<span data-ttu-id="d07fb-2149">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2149">9</span></span>

<span data-ttu-id="d07fb-2150">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2150">2</span></span><br/> <span data-ttu-id="d07fb-2151">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2151">0</span></span><br/>

<span data-ttu-id="d07fb-2152">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2152">1</span></span>

<span data-ttu-id="d07fb-2153">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2153">2</span></span>

<span data-ttu-id="d07fb-2154">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2154">3</span></span>

<span data-ttu-id="d07fb-2155">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2155">4</span></span>

<span data-ttu-id="d07fb-2156">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2156">5</span></span>

<span data-ttu-id="d07fb-2157">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2157">6</span></span>

<span data-ttu-id="d07fb-2158">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2158">7</span></span>

<span data-ttu-id="d07fb-2159">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2159">8</span></span>

<span data-ttu-id="d07fb-2160">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2160">9</span></span>

<span data-ttu-id="d07fb-2161">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2161">3</span></span><br/> <span data-ttu-id="d07fb-2162">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2162">0</span></span><br/>

<span data-ttu-id="d07fb-2163">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2163">1</span></span>

<span data-ttu-id="d07fb-2164">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="d07fb-2164">\_hRegion</span></span>

<span data-ttu-id="d07fb-2165">\_cskip</span><span class="sxs-lookup"><span data-stu-id="d07fb-2165">\_cskip</span></span>

<span data-ttu-id="d07fb-2166">\_bmkOffset</span><span class="sxs-lookup"><span data-stu-id="d07fb-2166">\_bmkOffset</span></span>



 

<span data-ttu-id="d07fb-2167">**\_ hRegion:** DEBE establecerse en 0x00000000 y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2167">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="d07fb-2168">**\_ cskip:** entero de 32 bits sin signo que contiene el número de filas que se omitirán en el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2168">**\_cskip**: A 32-bit unsigned integer containing the number of rows to skip in the rowset.</span></span>

<span data-ttu-id="d07fb-2169">**\_ bmkOffset:** valor de 32 bits que  representa el identificador del marcador que indica la posición inicial desde la que se omite el número de filas especificadas en cskip, antes de comenzar la \_ recuperación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2169">**\_bmkOffset**: A 32-bit value representing the handle of the **bookmark** indicating the starting position from which to skip the number of rows specified in \_cskip, before beginning retrieval.</span></span>

### <a name="22125-crowseekatratio"></a><span data-ttu-id="d07fb-2170">2.2.1.25 CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="d07fb-2170">2.2.1.25 CRowSeekAtRatio</span></span>

<span data-ttu-id="d07fb-2171">La estructura CRowSeekAtRatio identifica el punto en el que se va a iniciar la recuperación de un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2171">The CRowSeekAtRatio structure identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="d07fb-2172">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2172">0</span></span>

<span data-ttu-id="d07fb-2173">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2173">1</span></span>

<span data-ttu-id="d07fb-2174">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2174">2</span></span>

<span data-ttu-id="d07fb-2175">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2175">3</span></span>

<span data-ttu-id="d07fb-2176">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2176">4</span></span>

<span data-ttu-id="d07fb-2177">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2177">5</span></span>

<span data-ttu-id="d07fb-2178">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2178">6</span></span>

<span data-ttu-id="d07fb-2179">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2179">7</span></span>

<span data-ttu-id="d07fb-2180">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2180">8</span></span>

<span data-ttu-id="d07fb-2181">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2181">9</span></span>

<span data-ttu-id="d07fb-2182">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2182">1</span></span><br/> <span data-ttu-id="d07fb-2183">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2183">0</span></span><br/>

<span data-ttu-id="d07fb-2184">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2184">1</span></span>

<span data-ttu-id="d07fb-2185">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2185">2</span></span>

<span data-ttu-id="d07fb-2186">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2186">3</span></span>

<span data-ttu-id="d07fb-2187">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2187">4</span></span>

<span data-ttu-id="d07fb-2188">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2188">5</span></span>

<span data-ttu-id="d07fb-2189">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2189">6</span></span>

<span data-ttu-id="d07fb-2190">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2190">7</span></span>

<span data-ttu-id="d07fb-2191">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2191">8</span></span>

<span data-ttu-id="d07fb-2192">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2192">9</span></span>

<span data-ttu-id="d07fb-2193">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2193">2</span></span><br/> <span data-ttu-id="d07fb-2194">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2194">0</span></span><br/>

<span data-ttu-id="d07fb-2195">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2195">1</span></span>

<span data-ttu-id="d07fb-2196">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2196">2</span></span>

<span data-ttu-id="d07fb-2197">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2197">3</span></span>

<span data-ttu-id="d07fb-2198">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2198">4</span></span>

<span data-ttu-id="d07fb-2199">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2199">5</span></span>

<span data-ttu-id="d07fb-2200">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2200">6</span></span>

<span data-ttu-id="d07fb-2201">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2201">7</span></span>

<span data-ttu-id="d07fb-2202">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2202">8</span></span>

<span data-ttu-id="d07fb-2203">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2203">9</span></span>

<span data-ttu-id="d07fb-2204">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2204">3</span></span><br/> <span data-ttu-id="d07fb-2205">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2205">0</span></span><br/>

<span data-ttu-id="d07fb-2206">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2206">1</span></span>

<span data-ttu-id="d07fb-2207">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="d07fb-2207">CiTblChapt</span></span>

<span data-ttu-id="d07fb-2208">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="d07fb-2208">\_hRegion</span></span>

<span data-ttu-id="d07fb-2209">\_ulNumerator</span><span class="sxs-lookup"><span data-stu-id="d07fb-2209">\_ulNumerator</span></span>

<span data-ttu-id="d07fb-2210">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="d07fb-2210">\_ulDenominator</span></span>



 

<span data-ttu-id="d07fb-2211">**CiTblChapt:** entero de 32 bits sin signo que indica el capítulo del conjunto de filas del que se recuperarán las filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2211">**CiTblChapt**: A 32-bit unsigned integer indicating the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="d07fb-2212">**\_ hRegion:** DEBE establecerse en 0x00000000 y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2212">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="d07fb-2213">**\_ ulNumerator:** entero de 32 bits sin signo que representa el numerador de la proporción de filas del capítulo en el que se va a comenzar la recuperación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2213">**\_ulNumerator**: Unsigned 32-bit integer representing the numerator of the ratio of rows in the chapter at which to begin retrieval.</span></span>

<span data-ttu-id="d07fb-2214">**\_ ulDenominator:** entero de 32 bits sin signo que representa el denominador de la proporción de filas del capítulo en el que se va a comenzar la recuperación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2214">**\_ulDenominator**: Unsigned 32-bit integer representing the denominator of the ratio of rows in the chapter at which to begin retrieval.</span></span> <span data-ttu-id="d07fb-2215">DEBE ser mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2215">MUST be greater than zero.</span></span>

### <a name="22126-crowseekbybookmark"></a><span data-ttu-id="d07fb-2216">2.2.1.26 CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="d07fb-2216">2.2.1.26 CRowSeekByBookmark</span></span>

<span data-ttu-id="d07fb-2217">La estructura CRowSeekByBookmark identifica los marcadores desde los que empezar a recuperar filas para un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2217">The CRowSeekByBookmark structure identifies the bookmarks from which to begin retrieving rows for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="d07fb-2218">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2218">0</span></span>

<span data-ttu-id="d07fb-2219">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2219">1</span></span>

<span data-ttu-id="d07fb-2220">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2220">2</span></span>

<span data-ttu-id="d07fb-2221">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2221">3</span></span>

<span data-ttu-id="d07fb-2222">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2222">4</span></span>

<span data-ttu-id="d07fb-2223">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2223">5</span></span>

<span data-ttu-id="d07fb-2224">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2224">6</span></span>

<span data-ttu-id="d07fb-2225">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2225">7</span></span>

<span data-ttu-id="d07fb-2226">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2226">8</span></span>

<span data-ttu-id="d07fb-2227">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2227">9</span></span>

<span data-ttu-id="d07fb-2228">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2228">1</span></span><br/> <span data-ttu-id="d07fb-2229">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2229">0</span></span><br/>

<span data-ttu-id="d07fb-2230">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2230">1</span></span>

<span data-ttu-id="d07fb-2231">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2231">2</span></span>

<span data-ttu-id="d07fb-2232">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2232">3</span></span>

<span data-ttu-id="d07fb-2233">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2233">4</span></span>

<span data-ttu-id="d07fb-2234">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2234">5</span></span>

<span data-ttu-id="d07fb-2235">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2235">6</span></span>

<span data-ttu-id="d07fb-2236">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2236">7</span></span>

<span data-ttu-id="d07fb-2237">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2237">8</span></span>

<span data-ttu-id="d07fb-2238">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2238">9</span></span>

<span data-ttu-id="d07fb-2239">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2239">2</span></span><br/> <span data-ttu-id="d07fb-2240">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2240">0</span></span><br/>

<span data-ttu-id="d07fb-2241">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2241">1</span></span>

<span data-ttu-id="d07fb-2242">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2242">2</span></span>

<span data-ttu-id="d07fb-2243">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2243">3</span></span>

<span data-ttu-id="d07fb-2244">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2244">4</span></span>

<span data-ttu-id="d07fb-2245">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2245">5</span></span>

<span data-ttu-id="d07fb-2246">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2246">6</span></span>

<span data-ttu-id="d07fb-2247">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2247">7</span></span>

<span data-ttu-id="d07fb-2248">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2248">8</span></span>

<span data-ttu-id="d07fb-2249">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2249">9</span></span>

<span data-ttu-id="d07fb-2250">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2250">3</span></span><br/> <span data-ttu-id="d07fb-2251">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2251">0</span></span><br/>

<span data-ttu-id="d07fb-2252">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2252">1</span></span>

<span data-ttu-id="d07fb-2253">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="d07fb-2253">\_hRegion</span></span>

<span data-ttu-id="d07fb-2254">\_cBookmarks</span><span class="sxs-lookup"><span data-stu-id="d07fb-2254">\_cBookmarks</span></span>

<span data-ttu-id="d07fb-2255">\_maxRet</span><span class="sxs-lookup"><span data-stu-id="d07fb-2255">\_maxRet</span></span>

<span data-ttu-id="d07fb-2256">\_cValidRet</span><span class="sxs-lookup"><span data-stu-id="d07fb-2256">\_cValidRet</span></span>

<span data-ttu-id="d07fb-2257">\_aBookmarks (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2257">\_aBookmarks (variable)</span></span>

<span data-ttu-id="d07fb-2258">\_ascRet (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2258">\_ascRet (variable)</span></span>



 

<span data-ttu-id="d07fb-2259">**\_ hRegion**: DEBE establecerse en 0x00000000 y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2259">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="d07fb-2260">**\_ cBookmarks:** entero de 32 bits sin signo que representa el número de elementos de \_ una matriz de aBookmarks.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2260">**\_cBookmarks**: Unsigned 32-bit integer representing the number of elements in \_aBookmarks array.</span></span>

<span data-ttu-id="d07fb-2261">**\_ maxRet:** entero de 32 bits sin signo que representa el número de elementos de la matriz \_ ascRet.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2261">**\_maxRet**: Unsigned 32-bit integer representing the number of elements in \_ascRet array.</span></span>

<span data-ttu-id="d07fb-2262">**\_ cValidRet:** entero de 32 bits sin signo que representa el número de elementos de la matriz \_ ascRet que son válidos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2262">**\_cValidRet**: Unsigned 32-bit integer representing the number of elements in the \_ascRet array which are valid.</span></span> <span data-ttu-id="d07fb-2263">Se han definido elementos válidos en la matriz, mientras que los elementos no válidos no están definidos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2263">Valid elements have been defined in the array, while invalid elements are undefined.</span></span>

<span data-ttu-id="d07fb-2264">**\_ aBookmarks:** matriz de identificadores de marcador (cada uno representado por 4 bytes), como se obtiene de un mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2264">**\_aBookmarks**: An array of bookmark handles (each represented by 4 bytes), as obtained from a CPMGetRowsOut message.</span></span>

<span data-ttu-id="d07fb-2265">**\_ ascRet:** matriz de valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2265">**\_ascRet**: An array of HRESULT values.</span></span> <span data-ttu-id="d07fb-2266">Cuando se envía CRowSeekByBookMark como parte de la solicitud CPMGetRowsIn, el número de entradas de la matriz DEBE ser igual a \_ cBookMarks.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2266">When the CRowSeekByBookMark is sent as part of the CPMGetRowsIn request, the number of entries in the array MUST be equal to \_cBookMarks.</span></span> <span data-ttu-id="d07fb-2267">Cuando el cliente los envía, los valores DEBEN establecerse en cero y el servidor DEBE omitir el contenido de la matriz.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2267">When sent by the client, the values MUST be set zero, and the server MUST ignore the contents of the array.</span></span> <span data-ttu-id="d07fb-2268">Cuando el servidor lo envía (como parte del mensaje CPMGetRowsOut), los valores de la matriz indican el estado del resultado de cada recuperación de fila.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2268">When sent by the server (as part of the CPMGetRowsOut message), the values in the array indicate the result status for each row retrieval.</span></span>

### <a name="22127-crowseeknext"></a><span data-ttu-id="d07fb-2269">2.2.1.27 CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="d07fb-2269">2.2.1.27 CRowSeekNext</span></span>

<span data-ttu-id="d07fb-2270">La estructura CRowSeekNext contiene el número de filas que se omitirán en un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2270">The CRowSeekNext structure contains the number of rows to skip in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="d07fb-2271">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2271">0</span></span>

<span data-ttu-id="d07fb-2272">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2272">1</span></span>

<span data-ttu-id="d07fb-2273">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2273">2</span></span>

<span data-ttu-id="d07fb-2274">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2274">3</span></span>

<span data-ttu-id="d07fb-2275">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2275">4</span></span>

<span data-ttu-id="d07fb-2276">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2276">5</span></span>

<span data-ttu-id="d07fb-2277">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2277">6</span></span>

<span data-ttu-id="d07fb-2278">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2278">7</span></span>

<span data-ttu-id="d07fb-2279">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2279">8</span></span>

<span data-ttu-id="d07fb-2280">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2280">9</span></span>

<span data-ttu-id="d07fb-2281">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2281">1</span></span><br/> <span data-ttu-id="d07fb-2282">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2282">0</span></span><br/>

<span data-ttu-id="d07fb-2283">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2283">1</span></span>

<span data-ttu-id="d07fb-2284">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2284">2</span></span>

<span data-ttu-id="d07fb-2285">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2285">3</span></span>

<span data-ttu-id="d07fb-2286">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2286">4</span></span>

<span data-ttu-id="d07fb-2287">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2287">5</span></span>

<span data-ttu-id="d07fb-2288">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2288">6</span></span>

<span data-ttu-id="d07fb-2289">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2289">7</span></span>

<span data-ttu-id="d07fb-2290">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2290">8</span></span>

<span data-ttu-id="d07fb-2291">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2291">9</span></span>

<span data-ttu-id="d07fb-2292">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2292">2</span></span><br/> <span data-ttu-id="d07fb-2293">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2293">0</span></span><br/>

<span data-ttu-id="d07fb-2294">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2294">1</span></span>

<span data-ttu-id="d07fb-2295">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2295">2</span></span>

<span data-ttu-id="d07fb-2296">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2296">3</span></span>

<span data-ttu-id="d07fb-2297">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2297">4</span></span>

<span data-ttu-id="d07fb-2298">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2298">5</span></span>

<span data-ttu-id="d07fb-2299">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2299">6</span></span>

<span data-ttu-id="d07fb-2300">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2300">7</span></span>

<span data-ttu-id="d07fb-2301">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2301">8</span></span>

<span data-ttu-id="d07fb-2302">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2302">9</span></span>

<span data-ttu-id="d07fb-2303">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2303">3</span></span><br/> <span data-ttu-id="d07fb-2304">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2304">0</span></span><br/>

<span data-ttu-id="d07fb-2305">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2305">1</span></span>

<span data-ttu-id="d07fb-2306">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="d07fb-2306">CiTblChapt</span></span>

<span data-ttu-id="d07fb-2307">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="d07fb-2307">\_hRegion</span></span>

<span data-ttu-id="d07fb-2308">\_cskip</span><span class="sxs-lookup"><span data-stu-id="d07fb-2308">\_cskip</span></span>



 

<span data-ttu-id="d07fb-2309">**CiTblChapt:** entero de 32 bits sin signo que especifica el capítulo del conjunto de filas del que se recuperarán las filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2309">**CiTblChapt**: Unsigned 32-bit integer specifying the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="d07fb-2310">**\_ hRegion:** DEBE establecerse en 0x00000000 y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2310">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="d07fb-2311">**\_ cskip:** entero de 32 bits sin signo que representa el número de filas que se omitirán en el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2311">**\_cskip**: Unsigned 32-bit integer representing the number of rows to skip in the rowset.</span></span>

### <a name="22128-crowsetproperties"></a><span data-ttu-id="d07fb-2312">2.2.1.28 CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="d07fb-2312">2.2.1.28 CRowsetProperties</span></span>

<span data-ttu-id="d07fb-2313">La estructura CRowsetProperties contiene información de configuración para una consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2313">The CRowsetProperties structure contains configuration information for a query.</span></span>



<span data-ttu-id="d07fb-2314">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2314">0</span></span>

<span data-ttu-id="d07fb-2315">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2315">1</span></span>

<span data-ttu-id="d07fb-2316">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2316">2</span></span>

<span data-ttu-id="d07fb-2317">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2317">3</span></span>

<span data-ttu-id="d07fb-2318">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2318">4</span></span>

<span data-ttu-id="d07fb-2319">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2319">5</span></span>

<span data-ttu-id="d07fb-2320">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2320">6</span></span>

<span data-ttu-id="d07fb-2321">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2321">7</span></span>

<span data-ttu-id="d07fb-2322">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2322">8</span></span>

<span data-ttu-id="d07fb-2323">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2323">9</span></span>

<span data-ttu-id="d07fb-2324">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2324">1</span></span><br/> <span data-ttu-id="d07fb-2325">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2325">0</span></span><br/>

<span data-ttu-id="d07fb-2326">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2326">1</span></span>

<span data-ttu-id="d07fb-2327">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2327">2</span></span>

<span data-ttu-id="d07fb-2328">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2328">3</span></span>

<span data-ttu-id="d07fb-2329">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2329">4</span></span>

<span data-ttu-id="d07fb-2330">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2330">5</span></span>

<span data-ttu-id="d07fb-2331">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2331">6</span></span>

<span data-ttu-id="d07fb-2332">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2332">7</span></span>

<span data-ttu-id="d07fb-2333">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2333">8</span></span>

<span data-ttu-id="d07fb-2334">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2334">9</span></span>

<span data-ttu-id="d07fb-2335">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2335">2</span></span><br/> <span data-ttu-id="d07fb-2336">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2336">0</span></span><br/>

<span data-ttu-id="d07fb-2337">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2337">1</span></span>

<span data-ttu-id="d07fb-2338">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2338">2</span></span>

<span data-ttu-id="d07fb-2339">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2339">3</span></span>

<span data-ttu-id="d07fb-2340">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2340">4</span></span>

<span data-ttu-id="d07fb-2341">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2341">5</span></span>

<span data-ttu-id="d07fb-2342">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2342">6</span></span>

<span data-ttu-id="d07fb-2343">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2343">7</span></span>

<span data-ttu-id="d07fb-2344">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2344">8</span></span>

<span data-ttu-id="d07fb-2345">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2345">9</span></span>

<span data-ttu-id="d07fb-2346">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2346">3</span></span><br/> <span data-ttu-id="d07fb-2347">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2347">0</span></span><br/>

<span data-ttu-id="d07fb-2348">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2348">1</span></span>

<span data-ttu-id="d07fb-2349">\_uBooleanOptions</span><span class="sxs-lookup"><span data-stu-id="d07fb-2349">\_uBooleanOptions</span></span>

<span data-ttu-id="d07fb-2350">\_ulMaxOpenRows</span><span class="sxs-lookup"><span data-stu-id="d07fb-2350">\_ulMaxOpenRows</span></span>

<span data-ttu-id="d07fb-2351">\_ulMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="d07fb-2351">\_ulMemoryUsage</span></span>

<span data-ttu-id="d07fb-2352">\_cMaxResults</span><span class="sxs-lookup"><span data-stu-id="d07fb-2352">\_cMaxResults</span></span>

<span data-ttu-id="d07fb-2353">\_cCmdTimeout</span><span class="sxs-lookup"><span data-stu-id="d07fb-2353">\_cCmdTimeout</span></span>



 

<span data-ttu-id="d07fb-2354">**\_ uBooleanOptions:** los 3 bits menos significativos de este campo DEBEN contener uno de los tres valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="d07fb-2354">**\_uBooleanOptions**: The least significant 3 bits of this field MUST contain one of the following three values:</span></span>



| <span data-ttu-id="d07fb-2355">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-2355">Value</span></span>                  | <span data-ttu-id="d07fb-2356">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-2356">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d07fb-2357">eSequential 0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-2357">eSequential 0x00000001</span></span> | <span data-ttu-id="d07fb-2358">El cursor solo se puede mover hacia delante.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2358">The cursor can only be moved forwards.</span></span>                              |
| <span data-ttu-id="d07fb-2359">eLocatable 0x00000003</span><span class="sxs-lookup"><span data-stu-id="d07fb-2359">eLocatable 0x00000003</span></span>  | <span data-ttu-id="d07fb-2360">El cursor se puede mover a cualquier posición.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2360">The cursor can be moved to any position.</span></span>                            |
| <span data-ttu-id="d07fb-2361">eScrollable 0x00000007</span><span class="sxs-lookup"><span data-stu-id="d07fb-2361">eScrollable 0x00000007</span></span> | <span data-ttu-id="d07fb-2362">El cursor se puede mover a cualquier posición y capturar en cualquier dirección.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2362">The cursor can be moved to any position and fetch in any direction.</span></span> |



 

<span data-ttu-id="d07fb-2363">Los bits restantes pueden ser claros o establecerse en cualquier combinación de los siguientes valores de forma lógica o conjunta:</span><span class="sxs-lookup"><span data-stu-id="d07fb-2363">The remaining bits may either be clear, or set to any combination of the following values logically OR'd together:</span></span>



| <span data-ttu-id="d07fb-2364">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-2364">Value</span></span>                     | <span data-ttu-id="d07fb-2365">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-2365">Meaning</span></span>                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-2366">eAsynchronous 0x00000008</span><span class="sxs-lookup"><span data-stu-id="d07fb-2366">eAsynchronous 0x00000008</span></span>  | <span data-ttu-id="d07fb-2367">El cliente no esperará a que finalice la ejecución.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2367">The client will not wait for execution completion.</span></span>                                                          |
| <span data-ttu-id="d07fb-2368">eFirstRows 0x00000080</span><span class="sxs-lookup"><span data-stu-id="d07fb-2368">eFirstRows 0x00000080</span></span>     | <span data-ttu-id="d07fb-2369">Devuelve las primeras filas encontradas, no las mejores coincidencias.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2369">Return the first rows encountered, not the best matches.</span></span>                                                    |
| <span data-ttu-id="d07fb-2370">eHoldRows 0x00000200</span><span class="sxs-lookup"><span data-stu-id="d07fb-2370">eHoldRows 0x00000200</span></span>      | <span data-ttu-id="d07fb-2371">El servidor NO DEBE descartar filas hasta que el cliente se realiza con una consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2371">The server MUST NOT discard rows until the client is done with a query.</span></span>                                     |
| <span data-ttu-id="d07fb-2372">eChaptered 0x00000800</span><span class="sxs-lookup"><span data-stu-id="d07fb-2372">eChaptered 0x00000800</span></span>     | <span data-ttu-id="d07fb-2373">El conjunto de filas admite capítulos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2373">The rowset supports chapters.</span></span>                                                                               |
| <span data-ttu-id="d07fb-2374">eUseCI 0x00001000</span><span class="sxs-lookup"><span data-stu-id="d07fb-2374">eUseCI 0x00001000</span></span>         | <span data-ttu-id="d07fb-2375">Responda solo a la consulta desde el índice, no desde el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2375">Only answer the query from the index, not the file system.</span></span>                                                  |
| <span data-ttu-id="d07fb-2376">eDeferTrimming 0x00002000</span><span class="sxs-lookup"><span data-stu-id="d07fb-2376">eDeferTrimming 0x00002000</span></span> | <span data-ttu-id="d07fb-2377">El servicio de indexación debe considerar la posibilidad de optimizar el tiempo de respuesta al cliente al realizar la eliminación de resultados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2377">The indexing service is to consider optimizing response time to the client when performing results removal.</span></span> |



 

<span data-ttu-id="d07fb-2378">**\_ ulMaxOpenRows:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2378">**\_ulMaxOpenRows**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="d07fb-2379">Debe establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2379">Must be set to 0x00000000.</span></span> <span data-ttu-id="d07fb-2380">No se usa y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2380">Not used and MUST be ignored.</span></span>

<span data-ttu-id="d07fb-2381">**\_ ulMemoryUsage:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2381">**\_ulMemoryUsage**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="d07fb-2382">Debe establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2382">Must be set to 0x00000000.</span></span> <span data-ttu-id="d07fb-2383">No se usa y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2383">Not used and MUST be ignored.</span></span>

<span data-ttu-id="d07fb-2384">**\_ cMaxResults:** entero de 32 bits sin signo que especifica el número máximo de filas que se van a devolver para la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2384">**\_cMaxResults**: A 32-bit unsigned integer specifying the maximum number of rows that are to be returned for the query.</span></span>

<span data-ttu-id="d07fb-2385">**\_ cCmdTimeout:** entero de 32 bits sin signo, que especifica el número de segundos en los que una consulta debe finalizar automáticamente y el tiempo de espera, contando desde el momento en que la consulta comienza a ejecutarse en el servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2385">**\_cCmdTimeout**: A 32-bit unsigned integer, specifying the number of seconds at which a query is to time out and automatically terminate, counting from the time the query starts executing on the server.</span></span> <span data-ttu-id="d07fb-2386">Un valor de 0x00000000 significa que no se debe hacer el tiempo de espera de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2386">A value of 0x00000000 means that the query is not to time out.</span></span>

### <a name="22129-crowvariant"></a><span data-ttu-id="d07fb-2387">2.2.1.29 CRowVariant</span><span class="sxs-lookup"><span data-stu-id="d07fb-2387">2.2.1.29 CRowVariant</span></span>

<span data-ttu-id="d07fb-2388">La estructura CRowVariant contiene la parte de tamaño fijo de un tipo de datos de longitud variable almacenado en el mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2388">The CRowVariant structure contains the fixed-size portion of a variable length data type stored in the CPMGetRowsOut message.</span></span>



<span data-ttu-id="d07fb-2389">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2389">0</span></span>

<span data-ttu-id="d07fb-2390">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2390">1</span></span>

<span data-ttu-id="d07fb-2391">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2391">2</span></span>

<span data-ttu-id="d07fb-2392">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2392">3</span></span>

<span data-ttu-id="d07fb-2393">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2393">4</span></span>

<span data-ttu-id="d07fb-2394">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2394">5</span></span>

<span data-ttu-id="d07fb-2395">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2395">6</span></span>

<span data-ttu-id="d07fb-2396">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2396">7</span></span>

<span data-ttu-id="d07fb-2397">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2397">8</span></span>

<span data-ttu-id="d07fb-2398">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2398">9</span></span>

<span data-ttu-id="d07fb-2399">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2399">1</span></span><br/> <span data-ttu-id="d07fb-2400">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2400">0</span></span><br/>

<span data-ttu-id="d07fb-2401">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2401">1</span></span>

<span data-ttu-id="d07fb-2402">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2402">2</span></span>

<span data-ttu-id="d07fb-2403">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2403">3</span></span>

<span data-ttu-id="d07fb-2404">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2404">4</span></span>

<span data-ttu-id="d07fb-2405">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2405">5</span></span>

<span data-ttu-id="d07fb-2406">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2406">6</span></span>

<span data-ttu-id="d07fb-2407">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2407">7</span></span>

<span data-ttu-id="d07fb-2408">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2408">8</span></span>

<span data-ttu-id="d07fb-2409">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2409">9</span></span>

<span data-ttu-id="d07fb-2410">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2410">2</span></span><br/> <span data-ttu-id="d07fb-2411">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2411">0</span></span><br/>

<span data-ttu-id="d07fb-2412">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2412">1</span></span>

<span data-ttu-id="d07fb-2413">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2413">2</span></span>

<span data-ttu-id="d07fb-2414">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2414">3</span></span>

<span data-ttu-id="d07fb-2415">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2415">4</span></span>

<span data-ttu-id="d07fb-2416">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2416">5</span></span>

<span data-ttu-id="d07fb-2417">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2417">6</span></span>

<span data-ttu-id="d07fb-2418">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2418">7</span></span>

<span data-ttu-id="d07fb-2419">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2419">8</span></span>

<span data-ttu-id="d07fb-2420">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2420">9</span></span>

<span data-ttu-id="d07fb-2421">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2421">3</span></span><br/> <span data-ttu-id="d07fb-2422">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2422">0</span></span><br/>

<span data-ttu-id="d07fb-2423">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2423">1</span></span>

<span data-ttu-id="d07fb-2424">vType</span><span class="sxs-lookup"><span data-stu-id="d07fb-2424">vType</span></span>

<span data-ttu-id="d07fb-2425">reserved1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2425">reserved1</span></span>

<span data-ttu-id="d07fb-2426">reserved2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2426">reserved2</span></span>

<span data-ttu-id="d07fb-2427">Desplazamiento (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2427">Offset (optional)</span></span>



 

<span data-ttu-id="d07fb-2428">**vType:** un indicador de tipo que indica el tipo de vValue.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2428">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="d07fb-2429">DEBE ser uno de los valores VARENUM especificados en la sección 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2429">It MUST be one of the VARENUM values specified in section 2.2.1.1.</span></span>

<span data-ttu-id="d07fb-2430">**reserved1:** no se usa.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2430">**reserved1**: Not used.</span></span> <span data-ttu-id="d07fb-2431">El valor se puede establecer en cualquier valor arbitrario y DEBE omitirse al recibirse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2431">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="d07fb-2432">**reserved2:** no se usa.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2432">**reserved2**: Not used.</span></span> <span data-ttu-id="d07fb-2433">El valor se puede establecer en cualquier valor arbitrario y DEBE omitirse al recibirse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2433">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="d07fb-2434">**Offset:** desplazamiento a datos de longitud variable (por ejemplo, una cadena).</span><span class="sxs-lookup"><span data-stu-id="d07fb-2434">**Offset**: An offset to variable length data (e.g. a string).</span></span>  <span data-ttu-id="d07fb-2435">Debe ser un valor de 32 bits (4 bytes de longitud) si se usan desplazamientos de 32 bits (según las reglas de la sección 2.2.3.16) o un valor de 64 bytes (8 bytes de longitud) si se usan desplazamientos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2435">This MUST be a 32-bit value (4 bytes long) if 32-bit offsets are being used (per the rules in section 2.2.3.16), or a 64-byte value (8 bytes long) if 64-bit offsets are being used.</span></span>

### <a name="22130-csortset"></a><span data-ttu-id="d07fb-2436">2.2.1.30 CSortSet</span><span class="sxs-lookup"><span data-stu-id="d07fb-2436">2.2.1.30 CSortSet</span></span>

<span data-ttu-id="d07fb-2437">La estructura CSortSet contiene el criterio de ordenación de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2437">The CSortSet structure contains the sort order of the query.</span></span>



<span data-ttu-id="d07fb-2438">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2438">0</span></span>

<span data-ttu-id="d07fb-2439">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2439">1</span></span>

<span data-ttu-id="d07fb-2440">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2440">2</span></span>

<span data-ttu-id="d07fb-2441">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2441">3</span></span>

<span data-ttu-id="d07fb-2442">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2442">4</span></span>

<span data-ttu-id="d07fb-2443">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2443">5</span></span>

<span data-ttu-id="d07fb-2444">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2444">6</span></span>

<span data-ttu-id="d07fb-2445">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2445">7</span></span>

<span data-ttu-id="d07fb-2446">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2446">8</span></span>

<span data-ttu-id="d07fb-2447">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2447">9</span></span>

<span data-ttu-id="d07fb-2448">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2448">1</span></span><br/> <span data-ttu-id="d07fb-2449">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2449">0</span></span><br/>

<span data-ttu-id="d07fb-2450">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2450">1</span></span>

<span data-ttu-id="d07fb-2451">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2451">2</span></span>

<span data-ttu-id="d07fb-2452">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2452">3</span></span>

<span data-ttu-id="d07fb-2453">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2453">4</span></span>

<span data-ttu-id="d07fb-2454">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2454">5</span></span>

<span data-ttu-id="d07fb-2455">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2455">6</span></span>

<span data-ttu-id="d07fb-2456">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2456">7</span></span>

<span data-ttu-id="d07fb-2457">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2457">8</span></span>

<span data-ttu-id="d07fb-2458">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2458">9</span></span>

<span data-ttu-id="d07fb-2459">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2459">2</span></span><br/> <span data-ttu-id="d07fb-2460">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2460">0</span></span><br/>

<span data-ttu-id="d07fb-2461">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2461">1</span></span>

<span data-ttu-id="d07fb-2462">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2462">2</span></span>

<span data-ttu-id="d07fb-2463">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2463">3</span></span>

<span data-ttu-id="d07fb-2464">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2464">4</span></span>

<span data-ttu-id="d07fb-2465">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2465">5</span></span>

<span data-ttu-id="d07fb-2466">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2466">6</span></span>

<span data-ttu-id="d07fb-2467">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2467">7</span></span>

<span data-ttu-id="d07fb-2468">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2468">8</span></span>

<span data-ttu-id="d07fb-2469">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2469">9</span></span>

<span data-ttu-id="d07fb-2470">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2470">3</span></span><br/> <span data-ttu-id="d07fb-2471">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2471">0</span></span><br/>

<span data-ttu-id="d07fb-2472">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2472">1</span></span>

<span data-ttu-id="d07fb-2473">Count</span><span class="sxs-lookup"><span data-stu-id="d07fb-2473">Count</span></span>

<span data-ttu-id="d07fb-2474">sortArray (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2474">sortArray (variable)</span></span>



 

<span data-ttu-id="d07fb-2475">**count:** entero de 32 bits sin signo que especifica el número de elementos en sortArray.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2475">**count**: A 32-bit unsigned integer specifying number of elements in sortArray.</span></span>

<span data-ttu-id="d07fb-2476">**sortArray:** matriz de estructuras de CSort que describen el orden en el que se ordenan los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2476">**sortArray**: An array of CSort structures describing the order in which to sort the results of the query.</span></span> <span data-ttu-id="d07fb-2477">Las estructuras de la matriz DEBEN estar separadas por 0 a 3 bytes de relleno, de forma que cada estructura tenga una alineación de 4 bytes desde el principio de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2477">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="d07fb-2478">Estos bytes de relleno pueden ser cualquier valor arbitrario y DEBEN omitirse al recibirse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2478">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22131-ctablecolumn"></a><span data-ttu-id="d07fb-2479">2.2.1.31 CTableColumn</span><span class="sxs-lookup"><span data-stu-id="d07fb-2479">2.2.1.31 CTableColumn</span></span>

<span data-ttu-id="d07fb-2480">La estructura CTableColumn contiene una columna de un mensaje CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-2480">The CTableColumn structure contains a column of a CPMSetBindingsIn message</span></span>



<span data-ttu-id="d07fb-2481">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2481">0</span></span>

<span data-ttu-id="d07fb-2482">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2482">1</span></span>

<span data-ttu-id="d07fb-2483">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2483">2</span></span>

<span data-ttu-id="d07fb-2484">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2484">3</span></span>

<span data-ttu-id="d07fb-2485">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2485">4</span></span>

<span data-ttu-id="d07fb-2486">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2486">5</span></span>

<span data-ttu-id="d07fb-2487">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2487">6</span></span>

<span data-ttu-id="d07fb-2488">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2488">7</span></span>

<span data-ttu-id="d07fb-2489">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2489">8</span></span>

<span data-ttu-id="d07fb-2490">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2490">9</span></span>

<span data-ttu-id="d07fb-2491">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2491">1</span></span><br/> <span data-ttu-id="d07fb-2492">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2492">0</span></span><br/>

<span data-ttu-id="d07fb-2493">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2493">1</span></span>

<span data-ttu-id="d07fb-2494">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2494">2</span></span>

<span data-ttu-id="d07fb-2495">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2495">3</span></span>

<span data-ttu-id="d07fb-2496">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2496">4</span></span>

<span data-ttu-id="d07fb-2497">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2497">5</span></span>

<span data-ttu-id="d07fb-2498">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2498">6</span></span>

<span data-ttu-id="d07fb-2499">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2499">7</span></span>

<span data-ttu-id="d07fb-2500">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2500">8</span></span>

<span data-ttu-id="d07fb-2501">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2501">9</span></span>

<span data-ttu-id="d07fb-2502">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2502">2</span></span><br/> <span data-ttu-id="d07fb-2503">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2503">0</span></span><br/>

<span data-ttu-id="d07fb-2504">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2504">1</span></span>

<span data-ttu-id="d07fb-2505">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2505">2</span></span>

<span data-ttu-id="d07fb-2506">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2506">3</span></span>

<span data-ttu-id="d07fb-2507">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2507">4</span></span>

<span data-ttu-id="d07fb-2508">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2508">5</span></span>

<span data-ttu-id="d07fb-2509">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2509">6</span></span>

<span data-ttu-id="d07fb-2510">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2510">7</span></span>

<span data-ttu-id="d07fb-2511">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2511">8</span></span>

<span data-ttu-id="d07fb-2512">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2512">9</span></span>

<span data-ttu-id="d07fb-2513">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2513">3</span></span><br/> <span data-ttu-id="d07fb-2514">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2514">0</span></span><br/>

<span data-ttu-id="d07fb-2515">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2515">1</span></span>

<span data-ttu-id="d07fb-2516">PropSpec</span><span class="sxs-lookup"><span data-stu-id="d07fb-2516">PropSpec</span></span>

<span data-ttu-id="d07fb-2517">... (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2517">...(variable)</span></span>

<span data-ttu-id="d07fb-2518">vType</span><span class="sxs-lookup"><span data-stu-id="d07fb-2518">vType</span></span>

<span data-ttu-id="d07fb-2519">ValueUsed</span><span class="sxs-lookup"><span data-stu-id="d07fb-2519">ValueUsed</span></span>

<span data-ttu-id="d07fb-2520">\_padding1 (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2520">\_padding1 (optional)</span></span>

<span data-ttu-id="d07fb-2521">ValueOffset (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2521">ValueOffset (optional)</span></span>

<span data-ttu-id="d07fb-2522">ValueSize (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2522">ValueSize (optional)</span></span>

<span data-ttu-id="d07fb-2523">StatusUsed</span><span class="sxs-lookup"><span data-stu-id="d07fb-2523">StatusUsed</span></span>

<span data-ttu-id="d07fb-2524">\_padding2 (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2524">\_padding2 (optional)</span></span>

<span data-ttu-id="d07fb-2525">StatusOffset (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2525">StatusOffset (optional)</span></span>

<span data-ttu-id="d07fb-2526">LengthUsed</span><span class="sxs-lookup"><span data-stu-id="d07fb-2526">LengthUsed</span></span>

<span data-ttu-id="d07fb-2527">\_padding3 (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2527">\_padding3 (optional)</span></span>

<span data-ttu-id="d07fb-2528">LengthOffset (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2528">LengthOffset (optional)</span></span>



 

<span data-ttu-id="d07fb-2529">**PropSpec:** una estructura CFullPropSpec como se especifica en la sección 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2529">**PropSpec**: A CFullPropSpec structure as specified in Section 2.2.1.3.</span></span>

<span data-ttu-id="d07fb-2530">**vType:** especifica el tipo de valor de datos contenido en la columna.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2530">**vType**: Specifies the type of data value contained in the column.</span></span> <span data-ttu-id="d07fb-2531">Consulte el campo vType de la sección 2.2.1.1 para obtener la lista de valores de este campo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2531">See the vType field in Section 2.2.1.1 for the list of values for this field.</span></span>

<span data-ttu-id="d07fb-2532">**ValueUsed:** campo de un byte que DEBE establecerse en 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2532">**ValueUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="d07fb-2533">Si se establece en 0x01, la columna se transfiere dentro de la fila de tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2533">If set to 0x01, the column is transferred within the fixed size row.</span></span> <span data-ttu-id="d07fb-2534">Si se establece en 0x00, el valor de la columna se transfiere en la sección de longitud variable al final del búfer.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2534">If set to 0x00, the value of the column is transferred in the variable-length section at the end of the buffer.</span></span>

<span data-ttu-id="d07fb-2535">**\_ padding1:** campo de un byte que SE DEBE insertar antes de ValueOffset si, sin él, ValueOffset no comenzaría con un desplazamiento par desde el principio del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2535">**\_padding1**: A one byte field that MUST be inserted before ValueOffset if, without it, ValueOffset would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="d07fb-2536">El valor de este byte es arbitrario y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2536">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="d07fb-2537">Si ValueUsed está establecido en 0x00, este campo NO DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2537">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="d07fb-2538">**ValueOffset:** entero de 2 bytes sin signo que especifica el desplazamiento del valor de columna de la fila.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2538">**ValueOffset**: An unsigned 2-byte integer specifying the offset of the column value in the row.</span></span> <span data-ttu-id="d07fb-2539">Si ValueUsed está establecido en 0x00, este campo NO DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2539">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="d07fb-2540">**ValueSize:** entero de 2 bytes sin signo que especifica el tamaño del valor de columna en bytes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2540">**ValueSize**: An unsigned 2-byte integer specifying the size of the column value in bytes.</span></span> <span data-ttu-id="d07fb-2541">Si ValueUsed está establecido en 0x00, este campo NO DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2541">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="d07fb-2542">**StatusUsed:** campo de un byte que DEBE establecerse en 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2542">**StatusUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="d07fb-2543">Si se establece en 0x01, el estado de la columna se transfiere dentro de la fila.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2543">If set to 0x01, the status of the column is transferred within the row.</span></span> <span data-ttu-id="d07fb-2544">Si 0x00, el estado de la columna no se transfiere dentro de la fila.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2544">If 0x00, the status of the column is not transferred within the row.</span></span>

<span data-ttu-id="d07fb-2545">**\_ padding2:** campo de un byte que SE DEBE insertar antes de StatusOffset si, sin él, el campo StatusOffset no comenzaría con un desplazamiento par desde el principio del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2545">**\_padding2**: A one byte field that MUST be inserted before StatusOffset if, without it,the StatusOffset field would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="d07fb-2546">El valor de este byte es arbitrario y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2546">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="d07fb-2547">Si StatusUsed está establecido en 0x00, este campo NO DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2547">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="d07fb-2548">**StatusOffset:** entero de 2 bytes sin signo que especifica el desplazamiento del estado de la columna en la fila.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2548">**StatusOffset**: An unsigned 2-byte integer specifying the offset of the column status in the row.</span></span> <span data-ttu-id="d07fb-2549">Si StatusUsed está establecido en 0x00, este campo NO DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2549">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="d07fb-2550">**LengthUsed:** campo de un byte que DEBE establecerse en 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2550">**LengthUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="d07fb-2551">Si se establece en 0x01, la longitud de la columna se transfiere dentro de la fila.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2551">If set to 0x01, the length of the column is transferred within the row.</span></span> <span data-ttu-id="d07fb-2552">Si 0x00, la longitud de la columna NO SE DEBE transferir dentro de la fila.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2552">If 0x00, the length of the column MUST NOT be transferred within the row.</span></span>

<span data-ttu-id="d07fb-2553">**\_ padding3:** campo de un byte que SE DEBE insertar antes de LengthOffset si, sin él, LengthOffset no comenzaría en un desplazamiento par desde el principio de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2553">**\_padding3**: A one byte field which MUST be inserted before LengthOffset if, without it, LengthOffset would not begin at an even offset from the beginning of a message.</span></span> <span data-ttu-id="d07fb-2554">El valor de este byte es arbitrario y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2554">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="d07fb-2555">Si LengthUsed está establecido en 0x00, este campo NO DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2555">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="d07fb-2556">**LengthOffset:** entero de 2 bytes sin signo que especifica el desplazamiento de la longitud de columna de la fila.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2556">**LengthOffset**: An unsigned 2-byte integer specifying the offset of the column length in the row.</span></span> <span data-ttu-id="d07fb-2557">Si LengthUsed está establecido en 0x00, este campo NO DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2557">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

### <a name="22132-serializedpropertyvalue"></a><span data-ttu-id="d07fb-2558">2.2.1.32 SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="d07fb-2558">2.2.1.32 SERIALIZEDPROPERTYVALUE</span></span>

<span data-ttu-id="d07fb-2559">La estructura SERIALIZEDPROPERTYVALUE contiene un valor serializado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2559">The SERIALIZEDPROPERTYVALUE structure contains a serialized value.</span></span>



<span data-ttu-id="d07fb-2560">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2560">0</span></span>

<span data-ttu-id="d07fb-2561">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2561">1</span></span>

<span data-ttu-id="d07fb-2562">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2562">2</span></span>

<span data-ttu-id="d07fb-2563">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2563">3</span></span>

<span data-ttu-id="d07fb-2564">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2564">4</span></span>

<span data-ttu-id="d07fb-2565">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2565">5</span></span>

<span data-ttu-id="d07fb-2566">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2566">6</span></span>

<span data-ttu-id="d07fb-2567">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2567">7</span></span>

<span data-ttu-id="d07fb-2568">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2568">8</span></span>

<span data-ttu-id="d07fb-2569">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2569">9</span></span>

<span data-ttu-id="d07fb-2570">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2570">1</span></span><br/> <span data-ttu-id="d07fb-2571">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2571">0</span></span><br/>

<span data-ttu-id="d07fb-2572">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2572">1</span></span>

<span data-ttu-id="d07fb-2573">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2573">2</span></span>

<span data-ttu-id="d07fb-2574">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2574">3</span></span>

<span data-ttu-id="d07fb-2575">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2575">4</span></span>

<span data-ttu-id="d07fb-2576">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2576">5</span></span>

<span data-ttu-id="d07fb-2577">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2577">6</span></span>

<span data-ttu-id="d07fb-2578">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2578">7</span></span>

<span data-ttu-id="d07fb-2579">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2579">8</span></span>

<span data-ttu-id="d07fb-2580">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2580">9</span></span>

<span data-ttu-id="d07fb-2581">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2581">2</span></span><br/> <span data-ttu-id="d07fb-2582">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2582">0</span></span><br/>

<span data-ttu-id="d07fb-2583">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2583">1</span></span>

<span data-ttu-id="d07fb-2584">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2584">2</span></span>

<span data-ttu-id="d07fb-2585">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2585">3</span></span>

<span data-ttu-id="d07fb-2586">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2586">4</span></span>

<span data-ttu-id="d07fb-2587">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2587">5</span></span>

<span data-ttu-id="d07fb-2588">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2588">6</span></span>

<span data-ttu-id="d07fb-2589">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2589">7</span></span>

<span data-ttu-id="d07fb-2590">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2590">8</span></span>

<span data-ttu-id="d07fb-2591">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2591">9</span></span>

<span data-ttu-id="d07fb-2592">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2592">3</span></span><br/> <span data-ttu-id="d07fb-2593">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2593">0</span></span><br/>

<span data-ttu-id="d07fb-2594">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2594">1</span></span>

<span data-ttu-id="d07fb-2595">dwType</span><span class="sxs-lookup"><span data-stu-id="d07fb-2595">dwType</span></span>

<span data-ttu-id="d07fb-2596">rgb (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2596">rgb (variable)</span></span>



 

<span data-ttu-id="d07fb-2597">**dwType:** uno de los tipos de variante, definidos en la sección 2.2.1.1, que se puede combinar con modificadores de tipo variante.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2597">**dwType**: One of the variant types, defined in section 2.2.1.1, which can be combined with variant type modifiers.</span></span> <span data-ttu-id="d07fb-2598">Para todos los tipos de variantes, excepto los combinados con VT ARRAY, SERIALIZEDPROPERTYVALUE tiene el mismo diseño que CBaseStorageVariant, como se especifica en la sección \_ 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2598">For all variant types, except those combined with VT\_ARRAY, SERIALIZEDPROPERTYVALUE has the same layout as CBaseStorageVariant, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="d07fb-2599">Si el tipo de variante se combina con el modificador de tipo VT ARRAY, se usa SAFEARRAY2, especificado en la sección \_ 2.2.1.2.1.1, en lugar de SAFEARRAY en el campo vValue de CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2599">If the variant type is combined with the VT\_ARRAY type modifier, then SAFEARRAY2, specified in Section 2.2.1.2.1.1, is used instead of SAFEARRAY in CBaseStorageVariant's vValue field.</span></span>

<span data-ttu-id="d07fb-2600">**rgb:** valor serializado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2600">**rgb**: Serialized value.</span></span> <span data-ttu-id="d07fb-2601">Vea los detalles de serialización de vValue en 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2601">See details of serialization for vValue in 2.2.1.1.</span></span>

### <a name="222-message-headers"></a><span data-ttu-id="d07fb-2602">2.2.2 Encabezados de mensaje</span><span class="sxs-lookup"><span data-stu-id="d07fb-2602">2.2.2 Message Headers</span></span>

<span data-ttu-id="d07fb-2603">Todos los mensajes del Protocolo de servicio de indexación de contenido tienen un encabezado de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2603">All Content Indexing Service Protocol messages have a 16 byte header.</span></span>

<span data-ttu-id="d07fb-2604">A continuación se muestra un diagrama que muestra el formato de encabezado de mensaje del protocolo content indexing Service.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2604">Below is a diagram showing the Content Indexing Service Protocol message header format.</span></span>



<span data-ttu-id="d07fb-2605">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2605">0</span></span>

<span data-ttu-id="d07fb-2606">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2606">1</span></span>

<span data-ttu-id="d07fb-2607">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2607">2</span></span>

<span data-ttu-id="d07fb-2608">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2608">3</span></span>

<span data-ttu-id="d07fb-2609">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2609">4</span></span>

<span data-ttu-id="d07fb-2610">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2610">5</span></span>

<span data-ttu-id="d07fb-2611">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2611">6</span></span>

<span data-ttu-id="d07fb-2612">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2612">7</span></span>

<span data-ttu-id="d07fb-2613">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2613">8</span></span>

<span data-ttu-id="d07fb-2614">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2614">9</span></span>

<span data-ttu-id="d07fb-2615">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2615">1</span></span><br/> <span data-ttu-id="d07fb-2616">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2616">0</span></span><br/>

<span data-ttu-id="d07fb-2617">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2617">1</span></span>

<span data-ttu-id="d07fb-2618">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2618">2</span></span>

<span data-ttu-id="d07fb-2619">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2619">3</span></span>

<span data-ttu-id="d07fb-2620">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2620">4</span></span>

<span data-ttu-id="d07fb-2621">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2621">5</span></span>

<span data-ttu-id="d07fb-2622">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2622">6</span></span>

<span data-ttu-id="d07fb-2623">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2623">7</span></span>

<span data-ttu-id="d07fb-2624">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2624">8</span></span>

<span data-ttu-id="d07fb-2625">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2625">9</span></span>

<span data-ttu-id="d07fb-2626">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2626">2</span></span><br/> <span data-ttu-id="d07fb-2627">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2627">0</span></span><br/>

<span data-ttu-id="d07fb-2628">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2628">1</span></span>

<span data-ttu-id="d07fb-2629">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2629">2</span></span>

<span data-ttu-id="d07fb-2630">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2630">3</span></span>

<span data-ttu-id="d07fb-2631">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2631">4</span></span>

<span data-ttu-id="d07fb-2632">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2632">5</span></span>

<span data-ttu-id="d07fb-2633">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2633">6</span></span>

<span data-ttu-id="d07fb-2634">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2634">7</span></span>

<span data-ttu-id="d07fb-2635">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2635">8</span></span>

<span data-ttu-id="d07fb-2636">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2636">9</span></span>

<span data-ttu-id="d07fb-2637">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2637">3</span></span><br/> <span data-ttu-id="d07fb-2638">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2638">0</span></span><br/>

<span data-ttu-id="d07fb-2639">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2639">1</span></span>

<span data-ttu-id="d07fb-2640">\_Msg</span><span class="sxs-lookup"><span data-stu-id="d07fb-2640">\_msg</span></span>

<span data-ttu-id="d07fb-2641">\_Estado</span><span class="sxs-lookup"><span data-stu-id="d07fb-2641">\_status</span></span>

<span data-ttu-id="d07fb-2642">\_ulChecksum</span><span class="sxs-lookup"><span data-stu-id="d07fb-2642">\_ulChecksum</span></span>

<span data-ttu-id="d07fb-2643">\_ulReserved2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2643">\_ulReserved2</span></span>



 

<span data-ttu-id="d07fb-2644">\_**msg:** entero de 32 bits que identifica el tipo de mensaje que sigue al encabezado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2644">\_**msg**: A 32 bit integer that identifies the type of message following the header.</span></span> <span data-ttu-id="d07fb-2645">En la tabla siguiente se enumeran los mensajes del Protocolo de servicio de indexación de contenido y los valores enteros especificados para cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2645">The following table lists the Content Indexing Service Protocol messages and the integer values specified for each message.</span></span> <span data-ttu-id="d07fb-2646">Como se muestra en la tabla, algunos valores identifican dos mensajes en la tabla.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2646">As shown in the table, some values identify 2 messages in the table.</span></span> <span data-ttu-id="d07fb-2647">En esos casos, el mensaje que sigue al encabezado se puede identificar por la dirección del flujo de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2647">In those instances the message following the header can be identified by the direction of the message flow.</span></span> <span data-ttu-id="d07fb-2648">Si la dirección es cliente a servidor, se indica el mensaje con "In" anexado al nombre del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2648">If the direction is client to server, the message with "In" appended to the message name is indicated.</span></span> <span data-ttu-id="d07fb-2649">Si la dirección es de servidor a cliente, se indica el mensaje con "Out" anexado al nombre del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2649">If the direction is server to client, the message with "Out" appended to the message name is indicated.</span></span>



| <span data-ttu-id="d07fb-2650">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-2650">Value</span></span>      | <span data-ttu-id="d07fb-2651">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-2651">Meaning</span></span>                                                     |
|------------|-------------------------------------------------------------|
| <span data-ttu-id="d07fb-2652">0x000000C8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2652">0x000000C8</span></span> | <span data-ttu-id="d07fb-2653">CPMConnectIn o CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-2653">CPMConnectIn or CPMConnectOut</span></span>                               |
| <span data-ttu-id="d07fb-2654">0x000000C9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2654">0x000000C9</span></span> | <span data-ttu-id="d07fb-2655">CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="d07fb-2655">CPMDisconnect</span></span>                                               |
| <span data-ttu-id="d07fb-2656">0x000000CA</span><span class="sxs-lookup"><span data-stu-id="d07fb-2656">0x000000CA</span></span> | <span data-ttu-id="d07fb-2657">CPMCreateQueryIn o CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-2657">CPMCreateQueryIn or CPMCreateQueryOut</span></span>                       |
| <span data-ttu-id="d07fb-2658">0x000000CB</span><span class="sxs-lookup"><span data-stu-id="d07fb-2658">0x000000CB</span></span> | <span data-ttu-id="d07fb-2659">CPMFreeCursorIn o CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-2659">CPMFreeCursorIn or CPMFreeCursorOut</span></span>                         |
| <span data-ttu-id="d07fb-2660">0x000000CC</span><span class="sxs-lookup"><span data-stu-id="d07fb-2660">0x000000CC</span></span> | <span data-ttu-id="d07fb-2661">CPMGetRowsIn o CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-2661">CPMGetRowsIn or CPMGetRowsOut</span></span>                               |
| <span data-ttu-id="d07fb-2662">0x000000CD</span><span class="sxs-lookup"><span data-stu-id="d07fb-2662">0x000000CD</span></span> | <span data-ttu-id="d07fb-2663">CPMRatioFinishedIn o CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-2663">CPMRatioFinishedIn or CPMRatioFinishedOut</span></span>                   |
| <span data-ttu-id="d07fb-2664">0x000000CE</span><span class="sxs-lookup"><span data-stu-id="d07fb-2664">0x000000CE</span></span> | <span data-ttu-id="d07fb-2665">CPMCompareBmkIn o CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-2665">CPMCompareBmkIn or CPMCompareBmkOut</span></span>                         |
| <span data-ttu-id="d07fb-2666">0x000000CF</span><span class="sxs-lookup"><span data-stu-id="d07fb-2666">0x000000CF</span></span> | <span data-ttu-id="d07fb-2667">CPMGetApproximatePositionIn o CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-2667">CPMGetApproximatePositionIn or CPMGetApproximatePositionOut</span></span> |
| <span data-ttu-id="d07fb-2668">0x000000D0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2668">0x000000D0</span></span> | <span data-ttu-id="d07fb-2669">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-2669">CPMSetBindingsIn</span></span>                                            |
| <span data-ttu-id="d07fb-2670">0x000000D1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2670">0x000000D1</span></span> | <span data-ttu-id="d07fb-2671">CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="d07fb-2671">CPMGetNotify</span></span>                                                |
| <span data-ttu-id="d07fb-2672">0x000000D2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2672">0x000000D2</span></span> | <span data-ttu-id="d07fb-2673">CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-2673">CPMSendNotifyOut</span></span>                                            |
| <span data-ttu-id="d07fb-2674">0x000000D7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2674">0x000000D7</span></span> | <span data-ttu-id="d07fb-2675">CPMGetQueryStatusIn o CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-2675">CPMGetQueryStatusIn or CPMGetQueryStatusOut</span></span>                 |
| <span data-ttu-id="d07fb-2676">0x000000D9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2676">0x000000D9</span></span> | <span data-ttu-id="d07fb-2677">CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-2677">CPMCiStateInOut</span></span>                                             |
| <span data-ttu-id="d07fb-2678">0x000000E1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2678">0x000000E1</span></span> | <span data-ttu-id="d07fb-2679">CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-2679">CPMForceMergeIn</span></span>                                             |
| <span data-ttu-id="d07fb-2680">0x000000E4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2680">0x000000E4</span></span> | <span data-ttu-id="d07fb-2681">CPMFetchValueIn o CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-2681">CPMFetchValueIn or CPMFetchValueOut</span></span>                         |
| <span data-ttu-id="d07fb-2682">0x000000E6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2682">0x000000E6</span></span> | <span data-ttu-id="d07fb-2683">CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-2683">CPMUpdateDocumentsIn</span></span>                                        |
| <span data-ttu-id="d07fb-2684">0x000000E7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2684">0x000000E7</span></span> | <span data-ttu-id="d07fb-2685">CPMGetQueryStatusExIn o PMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-2685">CPMGetQueryStatusExIn or PMGetQueryStatusExOut</span></span>              |
| <span data-ttu-id="d07fb-2686">0x000000E8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2686">0x000000E8</span></span> | <span data-ttu-id="d07fb-2687">CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-2687">CPMRestartPositionIn</span></span>                                        |
| <span data-ttu-id="d07fb-2688">0x000000E9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2688">0x000000E9</span></span> | <span data-ttu-id="d07fb-2689">CPMStopAsynchIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-2689">CPMStopAsynchIn</span></span>                                             |
| <span data-ttu-id="d07fb-2690">0x000000EC</span><span class="sxs-lookup"><span data-stu-id="d07fb-2690">0x000000EC</span></span> | <span data-ttu-id="d07fb-2691">CPMSetCatStateIn o CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-2691">CPMSetCatStateIn or CPMSetCatStateOut</span></span>                       |



 

<span data-ttu-id="d07fb-2692">\_**status:** HRESULT \[ MS-SYS \] , que indica el estado de la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2692">\_**status**: An HRESULT \[MS-SYS\], indicating the status of the requested operation.</span></span>

\* *

<span data-ttu-id="d07fb-2693">*Comportamiento de Windows: el cliente siempre establece el \_ campo de estado en 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="d07fb-2693">*Windows Behavior: The client always sets the \_status field to 0x00000000.*</span></span>

<span data-ttu-id="d07fb-2694">**\_ ulChecksum:** ulChecksum DEBE calcularse según lo especificado en la sección \_ 3.2.4 para los mensajes siguientes:</span><span class="sxs-lookup"><span data-stu-id="d07fb-2694">**\_ulChecksum**: The \_ulChecksum MUST be calculated as specified in Section 3.2.4 for the following messages:</span></span>

-   <span data-ttu-id="d07fb-2695">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-2695">CPMConnectIn</span></span>
-   <span data-ttu-id="d07fb-2696">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-2696">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="d07fb-2697">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-2697">CPMSetBindingsIn</span></span>
-   <span data-ttu-id="d07fb-2698">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-2698">CPMGetRowsIn</span></span>
-   <span data-ttu-id="d07fb-2699">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-2699">CPMFetchValueIn</span></span>

<span data-ttu-id="d07fb-2700">Para todos los demás mensajes, \_ ulChecksum DEBE establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2700">For all other messages, \_ulChecksum MUST be set to 0x00000000.</span></span> <span data-ttu-id="d07fb-2701">Un cliente DEBE omitir el \_ campo ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2701">A client MUST ignore the\_ulChecksum field.</span></span>

<span data-ttu-id="d07fb-2702">**\_ ulReserved2:** DEBE establecerse en 0 y el receptor debe omitirlo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2702">**\_ulReserved2**: MUST be set to 0, and ignored by the receiver.</span></span>

### <a name="223-messages"></a><span data-ttu-id="d07fb-2703">2.2.3 Mensajes</span><span class="sxs-lookup"><span data-stu-id="d07fb-2703">2.2.3 Messages</span></span>

### <a name="2231-cpmcistateinout"></a><span data-ttu-id="d07fb-2704">2.2.3.1 CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-2704">2.2.3.1 CPMCiStateInOut</span></span>

<span data-ttu-id="d07fb-2705">El mensaje CPMCiStateInOut contiene información sobre el estado del servicio de indexación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2705">The CPMCiStateInOut message contains information about the state of the indexing service.</span></span> <span data-ttu-id="d07fb-2706">El formato del mensaje CPMCiStateInOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-2706">The format of the CPMCiStateInOut message that follows the header is:</span></span>



<span data-ttu-id="d07fb-2707">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2707">0</span></span>

<span data-ttu-id="d07fb-2708">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2708">1</span></span>

<span data-ttu-id="d07fb-2709">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2709">2</span></span>

<span data-ttu-id="d07fb-2710">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2710">3</span></span>

<span data-ttu-id="d07fb-2711">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2711">4</span></span>

<span data-ttu-id="d07fb-2712">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2712">5</span></span>

<span data-ttu-id="d07fb-2713">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2713">6</span></span>

<span data-ttu-id="d07fb-2714">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2714">7</span></span>

<span data-ttu-id="d07fb-2715">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2715">8</span></span>

<span data-ttu-id="d07fb-2716">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2716">9</span></span>

<span data-ttu-id="d07fb-2717">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2717">1</span></span><br/> <span data-ttu-id="d07fb-2718">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2718">0</span></span><br/>

<span data-ttu-id="d07fb-2719">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2719">1</span></span>

<span data-ttu-id="d07fb-2720">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2720">2</span></span>

<span data-ttu-id="d07fb-2721">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2721">3</span></span>

<span data-ttu-id="d07fb-2722">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2722">4</span></span>

<span data-ttu-id="d07fb-2723">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2723">5</span></span>

<span data-ttu-id="d07fb-2724">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2724">6</span></span>

<span data-ttu-id="d07fb-2725">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2725">7</span></span>

<span data-ttu-id="d07fb-2726">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2726">8</span></span>

<span data-ttu-id="d07fb-2727">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2727">9</span></span>

<span data-ttu-id="d07fb-2728">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2728">2</span></span><br/> <span data-ttu-id="d07fb-2729">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2729">0</span></span><br/>

<span data-ttu-id="d07fb-2730">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2730">1</span></span>

<span data-ttu-id="d07fb-2731">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2731">2</span></span>

<span data-ttu-id="d07fb-2732">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2732">3</span></span>

<span data-ttu-id="d07fb-2733">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2733">4</span></span>

<span data-ttu-id="d07fb-2734">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2734">5</span></span>

<span data-ttu-id="d07fb-2735">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2735">6</span></span>

<span data-ttu-id="d07fb-2736">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2736">7</span></span>

<span data-ttu-id="d07fb-2737">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2737">8</span></span>

<span data-ttu-id="d07fb-2738">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2738">9</span></span>

<span data-ttu-id="d07fb-2739">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2739">3</span></span><br/> <span data-ttu-id="d07fb-2740">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2740">0</span></span><br/>

<span data-ttu-id="d07fb-2741">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2741">1</span></span>

<span data-ttu-id="d07fb-2742">cbStruct</span><span class="sxs-lookup"><span data-stu-id="d07fb-2742">cbStruct</span></span>

<span data-ttu-id="d07fb-2743">cWordList</span><span class="sxs-lookup"><span data-stu-id="d07fb-2743">cWordList</span></span>

<span data-ttu-id="d07fb-2744">cPersistentIndex</span><span class="sxs-lookup"><span data-stu-id="d07fb-2744">cPersistentIndex</span></span>

<span data-ttu-id="d07fb-2745">cQueries</span><span class="sxs-lookup"><span data-stu-id="d07fb-2745">cQueries</span></span>

<span data-ttu-id="d07fb-2746">cDocuments</span><span class="sxs-lookup"><span data-stu-id="d07fb-2746">cDocuments</span></span>

<span data-ttu-id="d07fb-2747">cFreshTest</span><span class="sxs-lookup"><span data-stu-id="d07fb-2747">cFreshTest</span></span>

<span data-ttu-id="d07fb-2748">dwMergeProgress</span><span class="sxs-lookup"><span data-stu-id="d07fb-2748">dwMergeProgress</span></span>

<span data-ttu-id="d07fb-2749">eState</span><span class="sxs-lookup"><span data-stu-id="d07fb-2749">eState</span></span>

<span data-ttu-id="d07fb-2750">cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="d07fb-2750">cFilteredDocuments</span></span>

<span data-ttu-id="d07fb-2751">cTotalDocuments</span><span class="sxs-lookup"><span data-stu-id="d07fb-2751">cTotalDocuments</span></span>

<span data-ttu-id="d07fb-2752">cPendingScans</span><span class="sxs-lookup"><span data-stu-id="d07fb-2752">cPendingScans</span></span>

<span data-ttu-id="d07fb-2753">dwIndexSize</span><span class="sxs-lookup"><span data-stu-id="d07fb-2753">dwIndexSize</span></span>

<span data-ttu-id="d07fb-2754">cUniqueKeys</span><span class="sxs-lookup"><span data-stu-id="d07fb-2754">cUniqueKeys</span></span>

<span data-ttu-id="d07fb-2755">cSecQDocuments</span><span class="sxs-lookup"><span data-stu-id="d07fb-2755">cSecQDocuments</span></span>

<span data-ttu-id="d07fb-2756">dwPropCacheSize</span><span class="sxs-lookup"><span data-stu-id="d07fb-2756">dwPropCacheSize</span></span>



 

<span data-ttu-id="d07fb-2757">**cbStruct:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2757">**cbStruct**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="d07fb-2758">Tamaño en bytes de este mensaje (excepto el encabezado común).</span><span class="sxs-lookup"><span data-stu-id="d07fb-2758">The size in bytes of this message (excluding the common header).</span></span> <span data-ttu-id="d07fb-2759">DEBE establecerse en 0x0000003C.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2759">MUST be set to 0x0000003C.</span></span>

<span data-ttu-id="d07fb-2760">**cWordList:** entero de 32 bits sin signo que indica el recuento de índices iniciales creados para documentos indexados recientemente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2760">**cWordList**: A 32-bit unsigned integer indicating the count of initial indexes created for recently indexed documents.</span></span>

<span data-ttu-id="d07fb-2761">**cPersistentIndex:** entero de 32 bits sin signo que indica el recuento de índices persistentes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2761">**cPersistentIndex**: A 32-bit unsigned integer indicating the count of persistent indexes.</span></span>

<span data-ttu-id="d07fb-2762">**cQueries:** entero de 32 bits sin signo que indica un número de consultas que se ejecutan activamente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2762">**cQueries**: A 32-bit unsigned integer indicating a number of actively running queries.</span></span>

<span data-ttu-id="d07fb-2763">**cDocuments:** entero de 32 bits sin signo que indica el número total de documentos que esperan ser indexados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2763">**cDocuments**: A 32-bit unsigned integer indicating the total number of documents waiting to be indexed.</span></span>

<span data-ttu-id="d07fb-2764">**cFreshTest:** entero de 32 bits sin signo que indica el número de documentos únicos con información en índices que no están totalmente optimizados para el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2764">**cFreshTest**: A 32-bit unsigned integer indicating the number of unique documents with information in indexes that are not fully optimized for performance.</span></span>

<span data-ttu-id="d07fb-2765">**dwMergeProgress:** entero de 32 bits sin signo que especifica el porcentaje de finalización de la optimización completa actual de índices, si la optimización está actualmente en curso.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2765">**dwMergeProgress**: Unsigned 32-bit integer specifying the completion percentage of current full optimization of indexes, if optimization is currently in progress.</span></span> <span data-ttu-id="d07fb-2766">DEBE ser menor o igual que 100.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2766">MUST be less than or equal to 100.</span></span>

<span data-ttu-id="d07fb-2767">**eState:** estado de la indexación de contenido según lo especificado por una o varias de las constantes DE ESTADO DE \_ \_ \* CI, definidas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2767">**eState**: State of content indexing as given by one or more of the CI\_STATE\_\* constants, defined in the table below.</span></span>



| <span data-ttu-id="d07fb-2768">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-2768">Value</span></span>                                         | <span data-ttu-id="d07fb-2769">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-2769">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-2770">COMBINACIÓN \_ DE \_ \_ SOMBRAS DE ESTADO DE CI 0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-2770">CI\_STATE\_SHADOW\_MERGE 0x00000001</span></span>           | <span data-ttu-id="d07fb-2771">El servicio de indexación está en proceso de optimizar algunos de los índices para reducir el uso de memoria y mejorar el rendimiento de las consultas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2771">The indexing service is in the process of optimizing some of the indexes to reduce memory usage and improve query performance.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="d07fb-2772">Ci \_ STATE MASTER MERGE \_ \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-2772">CI\_STATE\_MASTER\_MERGE 0x00000002</span></span>           | <span data-ttu-id="d07fb-2773">El servicio de indexación está en proceso de optimización completa para todos los índices.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2773">The indexing service is in the process of full optimization for all indexes.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d07fb-2774">EXAMEN \_ DE CONTENIDO DE ESTADO DE CI \_ \_ \_ 0X00000004</span><span class="sxs-lookup"><span data-stu-id="d07fb-2774">CI\_STATE\_CONTENT\_SCAN\_REQUIRED 0x00000004</span></span> | <span data-ttu-id="d07fb-2775">Algunos documentos del índice han cambiado y el servicio de indexación debe determinar cuáles se han agregado, modificado o eliminado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2775">Some documents in the index have changed and the indexing service needs to determine which have been added, changed, or deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d07fb-2776">CI \_ STATE \_ RECOCIDO \_ MERGE 0x00000008</span><span class="sxs-lookup"><span data-stu-id="d07fb-2776">CI\_STATE\_ANNEALING\_MERGE 0x00000008</span></span>        | <span data-ttu-id="d07fb-2777">El servicio de indexación está en proceso de optimizar los índices para reducir el uso de memoria y mejorar el rendimiento de las consultas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2777">The indexing service is in the process of optimizing indexes to reduce memory usage and improve query performance.</span></span> <span data-ttu-id="d07fb-2778">Este proceso es más completo que el identificado por el valor CI STATE SHADOW MERGE, pero no es tan completo como se especifica en el valor \_ DE CI STATE MASTER \_ \_ \_ \_ \_ MERGE.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2778">This process is more comprehensive than the one identified by the CI\_STATE\_SHADOW\_MERGE value, but it is not as comprehensive as specified by the CI\_STATE\_MASTER\_MERGE value.</span></span> <span data-ttu-id="d07fb-2779">Estas optimizaciones son específicas de la implementación, ya que dependen de la forma en que los datos se almacenan internamente. las optimizaciones no afectan al protocolo de ninguna manera que no sea el tiempo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2779">Such optimizations are implementation-specific as they depend on the way data is stored internally; the optimizations do not affect the protocol in any way other than response time.</span></span> |
| <span data-ttu-id="d07fb-2780">Análisis \_ de ESTADO DE CI \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="d07fb-2780">CI\_STATE\_SCANNING 0x00000010</span></span>                | <span data-ttu-id="d07fb-2781">El servicio de indexación está examinando un directorio o un conjunto de directorios para ver si se ha agregado, eliminado o actualizado algún archivo desde la última vez que se indexó el directorio.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2781">The indexing service is examining a directory or a set of directories to see if any files have been added, deleted, or updated since the last time the directory was indexed.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="d07fb-2782">RECUPERACIÓN \_ DE ESTADO DE CI \_ 0x00000020</span><span class="sxs-lookup"><span data-stu-id="d07fb-2782">CI\_STATE\_RECOVERING 0x00000020</span></span>              | <span data-ttu-id="d07fb-2783">El servicio se inicia desde el último estado guardado y está en proceso de recuperación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2783">The service is starting from the last saved state and is in the process of recovering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d07fb-2784">ESTADO \_ DE CI MEMORIA BAJA \_ \_ 0x00000080</span><span class="sxs-lookup"><span data-stu-id="d07fb-2784">CI\_STATE\_LOW\_MEMORY 0x00000080</span></span>             | <span data-ttu-id="d07fb-2785">La mayor parte de la memoria virtual del servidor está en uso.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2785">Most of the virtual memory of the server is in use.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="d07fb-2786">CI \_ STATE HIGH IO \_ \_ 0x00000100</span><span class="sxs-lookup"><span data-stu-id="d07fb-2786">CI\_STATE\_HIGH\_IO 0x00000100</span></span>                | <span data-ttu-id="d07fb-2787">El nivel de actividad de entrada/salida (E/S) en el servidor es relativamente alto.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2787">The level of input/output (I/O) activity on the server is relatively high.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="d07fb-2788">COMBINACIÓN \_ MAESTRA DE ESTADO DE CI EN PAUSA \_ \_ \_ 0x00000200</span><span class="sxs-lookup"><span data-stu-id="d07fb-2788">CI\_STATE\_MASTER\_MERGE\_PAUSED 0x00000200</span></span>   | <span data-ttu-id="d07fb-2789">Se ha pausado el proceso de optimización completa para todos los índices que se encontraban en curso.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2789">The process of full optimization for all indexes that was in progress has been paused.</span></span> <span data-ttu-id="d07fb-2790">Esto se proporciona solo con fines informativos y no afecta a CISP.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2790">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d07fb-2791">Ci \_ STATE READ ONLY \_ \_ 0x00000400</span><span class="sxs-lookup"><span data-stu-id="d07fb-2791">CI\_STATE\_READ\_ONLY 0x00000400</span></span>              | <span data-ttu-id="d07fb-2792">Se ha pausado la parte del servicio de indexación que recoge nuevos documentos para indexar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2792">The portion of the indexing service that picks up new documents to index has been paused.</span></span> <span data-ttu-id="d07fb-2793">Esto se proporciona solo con fines informativos y no afecta a CISP.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2793">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="d07fb-2794">Ci \_ STATE BATTERY POWER \_ \_ 0x00000800</span><span class="sxs-lookup"><span data-stu-id="d07fb-2794">CI\_STATE\_BATTERY\_POWER 0x00000800</span></span>          | <span data-ttu-id="d07fb-2795">La parte del servicio de indexación que recoge nuevos documentos para indexar se ha pausado para conservar la duración de la batería, pero sigue respondiendo a las consultas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2795">The portion of the indexing service that picks up new documents to index has been paused to conserve battery lifetime but still replies to the queries.</span></span> <span data-ttu-id="d07fb-2796">Esto se proporciona solo con fines informativos y no afecta a CISP.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2796">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="d07fb-2797">USUARIO \_ DE ESTADO DE CI activo \_ \_ 0x00001000</span><span class="sxs-lookup"><span data-stu-id="d07fb-2797">CI\_STATE\_USER\_ACTIVE 0x00001000</span></span>            | <span data-ttu-id="d07fb-2798">La parte del servicio de indexación que recoge nuevos documentos para indexar se ha pausado debido a la alta actividad del usuario (teclado o mouse), pero sigue respondiendo a las consultas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2798">The portion of the indexing service that picks up new documents to index has been paused due to high activity by the user (keyboard or mouse) but still replies to the queries.</span></span> <span data-ttu-id="d07fb-2799">Esto se proporciona solo con fines informativos y no afecta a CISP.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2799">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="d07fb-2800">CI \_ STATE \_ STARTING 0x00002000</span><span class="sxs-lookup"><span data-stu-id="d07fb-2800">CI\_STATE\_STARTING 0x00002000</span></span>                | <span data-ttu-id="d07fb-2801">El servicio está iniciándose.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2801">The service is starting.</span></span> <span data-ttu-id="d07fb-2802">Las consultas se pueden ejecutar, pero el examen y la notificación aún no se han habilitado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2802">Queries can be run, but scanning and notification have not been enabled yet.</span></span> <span data-ttu-id="d07fb-2803">Esto se proporciona solo con fines informativos y no afecta a CISP.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2803">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="d07fb-2804">ESTADO \_ DE CI QUE LEE \_ \_ USNS 0x00004000</span><span class="sxs-lookup"><span data-stu-id="d07fb-2804">CI\_STATE\_READING\_USNS 0x00004000</span></span>           | <span data-ttu-id="d07fb-2805">El servicio no ha leído el registro que mantiene el sistema de archivos para realizar un seguimiento de los cambios en los archivos o directorios de un volumen, por lo que es posible que el índice no esté actualizado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2805">The service has not read the log kept by the file system to keep track of changes to files or directories in a volume, so the index might not be up to date.</span></span>                                                                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="d07fb-2806">**cFilteredDocuments:** entero de 32 bits sin signo que indica el número de documentos indexados desde que se inició la indexación de contenido.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2806">**cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents indexed since content indexing was begun.</span></span>

<span data-ttu-id="d07fb-2807">**cTotalDocuments:** entero de 32 bits sin signo que indica el número total de documentos del sistema.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2807">**cTotalDocuments**: A 32-bit unsigned integer indicating the total number of documents in the system.</span></span>

<span data-ttu-id="d07fb-2808">**cPendingScans:** entero de 32 bits sin signo que indica el número de operaciones de indexación de alto nivel pendientes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2808">**cPendingScans**: A 32-bit unsigned integer indicating the number of pending high level indexing operations.</span></span> <span data-ttu-id="d07fb-2809">El significado de este valor es específico del proveedor, pero se espera que números mayores indiquen que queda más indexación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2809">The meaning of this value is provider-specific but larger numbers are expected to indicate more indexing remains.</span></span>

<span data-ttu-id="d07fb-2810">*Comportamiento de Windows:* este valor suele ser cero, excepto inmediatamente después de que se haya iniciado la indexación o después de que se desborda una cola de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2810">*Windows Behavior*: This value is usually zero, except immediately after indexing has been started or after a notification queue overflows.</span></span>

<span data-ttu-id="d07fb-2811">**dwIndexSize:** entero de 32 bits sin signo que indica el tamaño, en megabytes, del índice (excepto la caché de propiedades).</span><span class="sxs-lookup"><span data-stu-id="d07fb-2811">**dwIndexSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the index (excluding the property cache).</span></span>

<span data-ttu-id="d07fb-2812">**cUniqueKeys:** entero de 32 bits sin signo que indica el número aproximado de claves únicas del catálogo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2812">**cUniqueKeys**: A 32-bit unsigned integer indicating the approximate number of unique keys in the catalog.</span></span>

<span data-ttu-id="d07fb-2813">**cSecQDocuments:** entero de 32 bits sin signo que indica el número de documentos que el servicio de indexación volverá a intentar indexar debido a un error durante el intento de indexación inicial.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2813">**cSecQDocuments**: A 32-bit unsigned integer indicating the number of documents that the indexing service will re-attempt to index because of a failure during the initial indexing attempt.</span></span>

<span data-ttu-id="d07fb-2814">**dwPropCacheSize:** entero de 32 bits sin signo que indica el tamaño, en megabytes, de la caché de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2814">**dwPropCacheSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the property cache.</span></span>

### <a name="2232-cpmsetcatstatein"></a><span data-ttu-id="d07fb-2815">2.2.3.2 CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-2815">2.2.3.2 CPMSetCatStateIn</span></span>

<span data-ttu-id="d07fb-2816">El mensaje CPMSetCatStateIn establece el estado de un catálogo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2816">The CPMSetCatStateIn message sets the state of a catalog.</span></span> <span data-ttu-id="d07fb-2817">El formato del mensaje CPMSetCatStateIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-2817">The format of the CPMSetCatStateIn message that follows the header is:</span></span>



<span data-ttu-id="d07fb-2818">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2818">0</span></span>

<span data-ttu-id="d07fb-2819">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2819">1</span></span>

<span data-ttu-id="d07fb-2820">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2820">2</span></span>

<span data-ttu-id="d07fb-2821">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2821">3</span></span>

<span data-ttu-id="d07fb-2822">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2822">4</span></span>

<span data-ttu-id="d07fb-2823">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2823">5</span></span>

<span data-ttu-id="d07fb-2824">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2824">6</span></span>

<span data-ttu-id="d07fb-2825">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2825">7</span></span>

<span data-ttu-id="d07fb-2826">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2826">8</span></span>

<span data-ttu-id="d07fb-2827">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2827">9</span></span>

<span data-ttu-id="d07fb-2828">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2828">1</span></span><br/> <span data-ttu-id="d07fb-2829">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2829">0</span></span><br/>

<span data-ttu-id="d07fb-2830">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2830">1</span></span>

<span data-ttu-id="d07fb-2831">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2831">2</span></span>

<span data-ttu-id="d07fb-2832">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2832">3</span></span>

<span data-ttu-id="d07fb-2833">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2833">4</span></span>

<span data-ttu-id="d07fb-2834">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2834">5</span></span>

<span data-ttu-id="d07fb-2835">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2835">6</span></span>

<span data-ttu-id="d07fb-2836">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2836">7</span></span>

<span data-ttu-id="d07fb-2837">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2837">8</span></span>

<span data-ttu-id="d07fb-2838">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2838">9</span></span>

<span data-ttu-id="d07fb-2839">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2839">2</span></span><br/> <span data-ttu-id="d07fb-2840">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2840">0</span></span><br/>

<span data-ttu-id="d07fb-2841">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2841">1</span></span>

<span data-ttu-id="d07fb-2842">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2842">2</span></span>

<span data-ttu-id="d07fb-2843">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2843">3</span></span>

<span data-ttu-id="d07fb-2844">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2844">4</span></span>

<span data-ttu-id="d07fb-2845">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2845">5</span></span>

<span data-ttu-id="d07fb-2846">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2846">6</span></span>

<span data-ttu-id="d07fb-2847">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2847">7</span></span>

<span data-ttu-id="d07fb-2848">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2848">8</span></span>

<span data-ttu-id="d07fb-2849">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2849">9</span></span>

<span data-ttu-id="d07fb-2850">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2850">3</span></span><br/> <span data-ttu-id="d07fb-2851">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2851">0</span></span><br/>

<span data-ttu-id="d07fb-2852">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2852">1</span></span>

<span data-ttu-id="d07fb-2853">\_partID</span><span class="sxs-lookup"><span data-stu-id="d07fb-2853">\_partID</span></span>

<span data-ttu-id="d07fb-2854">\_dwNewState</span><span class="sxs-lookup"><span data-stu-id="d07fb-2854">\_dwNewState</span></span>

<span data-ttu-id="d07fb-2855">\_CatName (variable, opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2855">\_CatName (variable, optional)</span></span>



 

<span data-ttu-id="d07fb-2856">**\_ partID:** DEBE establecerse en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2856">**\_partID**: MUST be set to 0x00000001.</span></span>

<span data-ttu-id="d07fb-2857">**\_ dwNewState**: debe establecerse en uno de los valores siguientes, lo que indica el nuevo estado del catálogo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2857">**\_dwNewState**: MUST be set to one of the following values, indicating the new state of the catalog.</span></span>



| <span data-ttu-id="d07fb-2858">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-2858">Value</span></span>                         | <span data-ttu-id="d07fb-2859">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-2859">Meaning</span></span>                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-2860">CICAT \_ STOPPED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-2860">CICAT\_STOPPED 0x00000001</span></span>     | <span data-ttu-id="d07fb-2861">El catálogo se detiene.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2861">The catalog is stopped.</span></span> <span data-ttu-id="d07fb-2862">Este estado significa que no se van a indexar nuevos archivos y que no se van a procesar consultas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2862">This state means no new files are to be indexed, and no search queries are to be processed.</span></span>                                                     |
| <span data-ttu-id="d07fb-2863">CICAT \_ READONLY 0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-2863">CICAT\_READONLY 0x00000002</span></span>    | <span data-ttu-id="d07fb-2864">El catálogo es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2864">The catalog is read-only.</span></span> <span data-ttu-id="d07fb-2865">No se van a indexar nuevos archivos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2865">No new files are to be indexed.</span></span>                                                                                                               |
| <span data-ttu-id="d07fb-2866">CICAT \_ WRITABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="d07fb-2866">CICAT\_WRITABLE 0x00000004</span></span>    | <span data-ttu-id="d07fb-2867">El catálogo se puede escribir.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2867">The catalog is writable.</span></span> <span data-ttu-id="d07fb-2868">Se pueden indexar nuevos archivos y se van a procesar las consultas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2868">New files can be indexed, and search queries are to be processed.</span></span>                                                                              |
| <span data-ttu-id="d07fb-2869">CICAT \_ NO \_ QUERY 0x00000008</span><span class="sxs-lookup"><span data-stu-id="d07fb-2869">CICAT\_NO\_QUERY 0x00000008</span></span>   | <span data-ttu-id="d07fb-2870">El catálogo no está disponible para realizar consultas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2870">The catalog is not available for querying.</span></span>                                                                                                                              |
| <span data-ttu-id="d07fb-2871">CICAT \_ GET \_ STATE 0x00000010</span><span class="sxs-lookup"><span data-stu-id="d07fb-2871">CICAT\_GET\_STATE 0x00000010</span></span>  | <span data-ttu-id="d07fb-2872">El estado del catálogo no se va a cambiar, solo se recupera.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2872">The state of the catalog is not to be changed, only retrieved.</span></span>                                                                                                          |
| <span data-ttu-id="d07fb-2873">CICAT \_ ALL \_ OPENED 0x00000020</span><span class="sxs-lookup"><span data-stu-id="d07fb-2873">CICAT\_ALL\_OPENED 0x00000020</span></span> | <span data-ttu-id="d07fb-2874">Una comprobación para ver si se han iniciado todos los catálogos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2874">A check to see if all of the catalogs have been started.</span></span> <span data-ttu-id="d07fb-2875">Si es así, el campo dwOldState enviado en la respuesta CPMSetCatStateOut a este mensaje se notifica \_ como distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2875">If so, the \_dwOldState field sent in the CPMSetCatStateOut reply to this message will be reported as nonzero.</span></span> |



 

<span data-ttu-id="d07fb-2876">**\_ CatName:** el nombre del catálogo que debe modificar su estado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2876">**\_CatName**: The name of the catalog which is to have its state modified.</span></span> <span data-ttu-id="d07fb-2877">El nombre DEBE ser una cadena Unicode terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2877">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="d07fb-2878">Este campo DEBE omitirse si \_ dwNewState está establecido en CICAT \_ ALL \_ OPENED.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2878">This field MUST be omitted if \_dwNewState is set to CICAT\_ALL\_OPENED.</span></span>

### <a name="2233-cpmsetcatstateout"></a><span data-ttu-id="d07fb-2879">2.2.3.3 CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-2879">2.2.3.3 CPMSetCatStateOut</span></span>

<span data-ttu-id="d07fb-2880">El mensaje CPMSetCatStateOut es una respuesta a un mensaje CPMSetCatStateIn con el estado anterior del catálogo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2880">The CPMSetCatStateOut message is a reply to a CPMSetCatStateIn message with the old state of the catalog.</span></span> <span data-ttu-id="d07fb-2881">El formato del mensaje CPMSetCatStateOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-2881">The format of the CPMSetCatStateOut message that follows the header is:</span></span>



<span data-ttu-id="d07fb-2882">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2882">0</span></span>

<span data-ttu-id="d07fb-2883">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2883">1</span></span>

<span data-ttu-id="d07fb-2884">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2884">2</span></span>

<span data-ttu-id="d07fb-2885">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2885">3</span></span>

<span data-ttu-id="d07fb-2886">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2886">4</span></span>

<span data-ttu-id="d07fb-2887">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2887">5</span></span>

<span data-ttu-id="d07fb-2888">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2888">6</span></span>

<span data-ttu-id="d07fb-2889">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2889">7</span></span>

<span data-ttu-id="d07fb-2890">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2890">8</span></span>

<span data-ttu-id="d07fb-2891">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2891">9</span></span>

<span data-ttu-id="d07fb-2892">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2892">1</span></span><br/> <span data-ttu-id="d07fb-2893">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2893">0</span></span><br/>

<span data-ttu-id="d07fb-2894">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2894">1</span></span>

<span data-ttu-id="d07fb-2895">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2895">2</span></span>

<span data-ttu-id="d07fb-2896">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2896">3</span></span>

<span data-ttu-id="d07fb-2897">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2897">4</span></span>

<span data-ttu-id="d07fb-2898">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2898">5</span></span>

<span data-ttu-id="d07fb-2899">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2899">6</span></span>

<span data-ttu-id="d07fb-2900">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2900">7</span></span>

<span data-ttu-id="d07fb-2901">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2901">8</span></span>

<span data-ttu-id="d07fb-2902">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2902">9</span></span>

<span data-ttu-id="d07fb-2903">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2903">2</span></span><br/> <span data-ttu-id="d07fb-2904">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2904">0</span></span><br/>

<span data-ttu-id="d07fb-2905">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2905">1</span></span>

<span data-ttu-id="d07fb-2906">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2906">2</span></span>

<span data-ttu-id="d07fb-2907">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2907">3</span></span>

<span data-ttu-id="d07fb-2908">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2908">4</span></span>

<span data-ttu-id="d07fb-2909">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2909">5</span></span>

<span data-ttu-id="d07fb-2910">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2910">6</span></span>

<span data-ttu-id="d07fb-2911">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2911">7</span></span>

<span data-ttu-id="d07fb-2912">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2912">8</span></span>

<span data-ttu-id="d07fb-2913">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2913">9</span></span>

<span data-ttu-id="d07fb-2914">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2914">3</span></span><br/> <span data-ttu-id="d07fb-2915">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2915">0</span></span><br/>

<span data-ttu-id="d07fb-2916">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2916">1</span></span>

<span data-ttu-id="d07fb-2917">\_dwOldState</span><span class="sxs-lookup"><span data-stu-id="d07fb-2917">\_dwOldState</span></span>



 

<span data-ttu-id="d07fb-2918">**\_ dwOldState:** uno de los valores siguientes, que indica el estado anterior del catálogo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2918">**\_dwOldState**: One of the following values, indicating the old state of the catalog.</span></span>



| <span data-ttu-id="d07fb-2919">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-2919">Value</span></span>                       | <span data-ttu-id="d07fb-2920">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-2920">Meaning</span></span>                                    |
|-----------------------------|--------------------------------------------|
| <span data-ttu-id="d07fb-2921">CICAT \_ STOPPED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-2921">CICAT\_STOPPED 0x00000001</span></span>   | <span data-ttu-id="d07fb-2922">El catálogo se detiene.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2922">The catalog is stopped.</span></span>                    |
| <span data-ttu-id="d07fb-2923">CICAT \_ READONLY 0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-2923">CICAT\_READONLY 0x00000002</span></span>  | <span data-ttu-id="d07fb-2924">El catálogo es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2924">The catalog is read-only.</span></span>                  |
| <span data-ttu-id="d07fb-2925">CICAT \_ WRITABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="d07fb-2925">CICAT\_WRITABLE 0x00000004</span></span>  | <span data-ttu-id="d07fb-2926">El catálogo se puede escribir.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2926">The catalog is writable.</span></span>                   |
| <span data-ttu-id="d07fb-2927">CICAT \_ NO \_ QUERY 0x00000008</span><span class="sxs-lookup"><span data-stu-id="d07fb-2927">CICAT\_NO\_QUERY 0x00000008</span></span> | <span data-ttu-id="d07fb-2928">El catálogo no está disponible para realizar consultas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2928">The catalog is not available for querying.</span></span> |



 

### <a name="2234-cpmupdatedocumentsin"></a><span data-ttu-id="d07fb-2929">2.2.3.4 CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-2929">2.2.3.4 CPMUpdateDocumentsIn</span></span>

<span data-ttu-id="d07fb-2930">El mensaje CPMUpdateDocumentsIn indica al servidor que indexe la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2930">The CPMUpdateDocumentsIn message directs the server to index the specified path.</span></span>

<span data-ttu-id="d07fb-2931">El servidor responderá con el encabezado del mensaje CPMUpdateDocumentsOut, con los resultados de la solicitud contenida en el campo de estado del \_ encabezado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2931">The server will reply with the message header of the CPMUpdateDocumentsOut message, with the results of the request contained in the \_status field of the message header.</span></span>

<span data-ttu-id="d07fb-2932">El formato del mensaje CPMUpdateDocumentsIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-2932">The format of the CPMUpdateDocumentsIn message that follows the header is:</span></span>



<span data-ttu-id="d07fb-2933">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2933">0</span></span>

<span data-ttu-id="d07fb-2934">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2934">1</span></span>

<span data-ttu-id="d07fb-2935">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2935">2</span></span>

<span data-ttu-id="d07fb-2936">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2936">3</span></span>

<span data-ttu-id="d07fb-2937">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2937">4</span></span>

<span data-ttu-id="d07fb-2938">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2938">5</span></span>

<span data-ttu-id="d07fb-2939">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2939">6</span></span>

<span data-ttu-id="d07fb-2940">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2940">7</span></span>

<span data-ttu-id="d07fb-2941">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2941">8</span></span>

<span data-ttu-id="d07fb-2942">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2942">9</span></span>

<span data-ttu-id="d07fb-2943">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2943">1</span></span><br/> <span data-ttu-id="d07fb-2944">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2944">0</span></span><br/>

<span data-ttu-id="d07fb-2945">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2945">1</span></span>

<span data-ttu-id="d07fb-2946">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2946">2</span></span>

<span data-ttu-id="d07fb-2947">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2947">3</span></span>

<span data-ttu-id="d07fb-2948">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2948">4</span></span>

<span data-ttu-id="d07fb-2949">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2949">5</span></span>

<span data-ttu-id="d07fb-2950">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2950">6</span></span>

<span data-ttu-id="d07fb-2951">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2951">7</span></span>

<span data-ttu-id="d07fb-2952">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2952">8</span></span>

<span data-ttu-id="d07fb-2953">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2953">9</span></span>

<span data-ttu-id="d07fb-2954">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2954">2</span></span><br/> <span data-ttu-id="d07fb-2955">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2955">0</span></span><br/>

<span data-ttu-id="d07fb-2956">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2956">1</span></span>

<span data-ttu-id="d07fb-2957">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2957">2</span></span>

<span data-ttu-id="d07fb-2958">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2958">3</span></span>

<span data-ttu-id="d07fb-2959">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2959">4</span></span>

<span data-ttu-id="d07fb-2960">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-2960">5</span></span>

<span data-ttu-id="d07fb-2961">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-2961">6</span></span>

<span data-ttu-id="d07fb-2962">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-2962">7</span></span>

<span data-ttu-id="d07fb-2963">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-2963">8</span></span>

<span data-ttu-id="d07fb-2964">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-2964">9</span></span>

<span data-ttu-id="d07fb-2965">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2965">3</span></span><br/> <span data-ttu-id="d07fb-2966">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2966">0</span></span><br/>

<span data-ttu-id="d07fb-2967">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2967">1</span></span>

<span data-ttu-id="d07fb-2968">\_flag (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2968">\_flag (optional)</span></span>

<span data-ttu-id="d07fb-2969">\_fRootPath (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2969">\_fRootPath (optional)</span></span>

<span data-ttu-id="d07fb-2970">RootPath (variable, opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-2970">RootPath (variable, optional)</span></span>



 

<span data-ttu-id="d07fb-2971">**\_ flag**: tipo de actualización que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2971">**\_flag**: The type of update to be performed.</span></span> <span data-ttu-id="d07fb-2972">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2972">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="d07fb-2973">Este campo DEBE establecerse en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="d07fb-2973">This field MUST be set to one of the following values:</span></span>



| <span data-ttu-id="d07fb-2974">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-2974">Value</span></span>                  | <span data-ttu-id="d07fb-2975">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-2975">Meaning</span></span>                                   |
|------------------------|-------------------------------------------|
| <span data-ttu-id="d07fb-2976">UPD \_ INCREM 0x00000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-2976">UPD\_INCREM 0x00000000</span></span> | <span data-ttu-id="d07fb-2977">Se va a realizar una actualización incremental.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2977">An incremental update is to be performed.</span></span> |
| <span data-ttu-id="d07fb-2978">UPD \_ FULL 0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-2978">UPD\_FULL 0x00000001</span></span>   | <span data-ttu-id="d07fb-2979">Se va a realizar una actualización completa.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2979">A full update is to be performed.</span></span>         |
| <span data-ttu-id="d07fb-2980">Upd \_ INIT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-2980">UPD\_INIT 0x00000002</span></span>   | <span data-ttu-id="d07fb-2981">Se va a realizar una nueva inicialización.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2981">A new initialization is to be performed.</span></span>  |



 

<span data-ttu-id="d07fb-2982">**\_ fRootPath:** valor booleano que indica si el campo RootPath especifica una ruta de acceso en la que realizar la actualización.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2982">**\_fRootPath**: A boolean value indicating if the RootPath field specifies a path on which to perform the update.</span></span> <span data-ttu-id="d07fb-2983">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2983">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="d07fb-2984">Este campo DEBE establecerse en 0x00000001 o 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2984">This field MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="d07fb-2985">Si se establece en 0x00000001, se incluye una ruta de acceso en la que realizar la actualización en RootPath.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2985">If set to 0x00000001, then a path on which to perform the update is included in RootPath.</span></span> <span data-ttu-id="d07fb-2986">Si se establece en 0x00000000, la actualización se realizará en todas las rutas de acceso indexadas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2986">If set to 0x00000000, then the update is to be performed on all indexed paths.</span></span>

<span data-ttu-id="d07fb-2987">**RootPath:** nombre de la ruta de acceso que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2987">**RootPath**: The name of the path to be updated.</span></span> <span data-ttu-id="d07fb-2988">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2988">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="d07fb-2989">El nombre DEBE ser una cadena Unicode terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2989">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="d07fb-2990">Este campo DEBE omitirse si \_ fRootPath está establecido en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2990">This field MUST be omitted if \_fRootPath is set to 0x00000000.</span></span>

### <a name="2235-cpmforcemergein"></a><span data-ttu-id="d07fb-2991">2.2.3.5 CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-2991">2.2.3.5 CPMForceMergeIn</span></span>

<span data-ttu-id="d07fb-2992">El mensaje CPMForceMergeIn solicita a un servidor que realice el mantenimiento necesario para mejorar el rendimiento de las consultas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2992">The CPMForceMergeIn message requests a server to perform any maintenance necessary to improve query performance.</span></span> <span data-ttu-id="d07fb-2993">El servidor responderá con el encabezado del mensaje CPMForceMergeIn, con los resultados de la solicitud contenida en el \_ campo de estado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-2993">The server will reply with the message header of the CPMForceMergeIn message, with the results of the request contained in the \_status field.</span></span>

<span data-ttu-id="d07fb-2994">El formato del mensaje CPMForceMergeIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-2994">The format of the CPMForceMergeIn message that follows the header is:</span></span>



<span data-ttu-id="d07fb-2995">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-2995">0</span></span>

<span data-ttu-id="d07fb-2996">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-2996">1</span></span>

<span data-ttu-id="d07fb-2997">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-2997">2</span></span>

<span data-ttu-id="d07fb-2998">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-2998">3</span></span>

<span data-ttu-id="d07fb-2999">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-2999">4</span></span>

<span data-ttu-id="d07fb-3000">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3000">5</span></span>

<span data-ttu-id="d07fb-3001">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3001">6</span></span>

<span data-ttu-id="d07fb-3002">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3002">7</span></span>

<span data-ttu-id="d07fb-3003">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3003">8</span></span>

<span data-ttu-id="d07fb-3004">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3004">9</span></span>

<span data-ttu-id="d07fb-3005">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3005">1</span></span><br/> <span data-ttu-id="d07fb-3006">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3006">0</span></span><br/>

<span data-ttu-id="d07fb-3007">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3007">1</span></span>

<span data-ttu-id="d07fb-3008">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3008">2</span></span>

<span data-ttu-id="d07fb-3009">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3009">3</span></span>

<span data-ttu-id="d07fb-3010">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3010">4</span></span>

<span data-ttu-id="d07fb-3011">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3011">5</span></span>

<span data-ttu-id="d07fb-3012">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3012">6</span></span>

<span data-ttu-id="d07fb-3013">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3013">7</span></span>

<span data-ttu-id="d07fb-3014">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3014">8</span></span>

<span data-ttu-id="d07fb-3015">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3015">9</span></span>

<span data-ttu-id="d07fb-3016">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3016">2</span></span><br/> <span data-ttu-id="d07fb-3017">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3017">0</span></span><br/>

<span data-ttu-id="d07fb-3018">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3018">1</span></span>

<span data-ttu-id="d07fb-3019">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3019">2</span></span>

<span data-ttu-id="d07fb-3020">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3020">3</span></span>

<span data-ttu-id="d07fb-3021">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3021">4</span></span>

<span data-ttu-id="d07fb-3022">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3022">5</span></span>

<span data-ttu-id="d07fb-3023">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3023">6</span></span>

<span data-ttu-id="d07fb-3024">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3024">7</span></span>

<span data-ttu-id="d07fb-3025">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3025">8</span></span>

<span data-ttu-id="d07fb-3026">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3026">9</span></span>

<span data-ttu-id="d07fb-3027">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3027">3</span></span><br/> <span data-ttu-id="d07fb-3028">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3028">0</span></span><br/>

<span data-ttu-id="d07fb-3029">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3029">1</span></span>

<span data-ttu-id="d07fb-3030">\_partID (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3030">\_partID (optional)</span></span>



 

<span data-ttu-id="d07fb-3031">**\_ partID:** este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3031">**\_partID**: This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="d07fb-3032">Cuando este campo está presente, debe establecerse en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3032">When this field is present, it MUST be set to 0x00000001.</span></span>

### <a name="2236-cpmconnectin"></a><span data-ttu-id="d07fb-3033">2.2.3.6 CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-3033">2.2.3.6 CPMConnectIn</span></span>

<span data-ttu-id="d07fb-3034">El mensaje CPMConnectIn inicia una sesión entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3034">The CPMConnectIn message begins a session between the client and server.</span></span>

<span data-ttu-id="d07fb-3035">El formato del mensaje CPMConnectIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3035">The format of the CPMConnectIn message that follows the header is:</span></span>



<span data-ttu-id="d07fb-3036">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3036">0</span></span>

<span data-ttu-id="d07fb-3037">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3037">1</span></span>

<span data-ttu-id="d07fb-3038">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3038">2</span></span>

<span data-ttu-id="d07fb-3039">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3039">3</span></span>

<span data-ttu-id="d07fb-3040">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3040">4</span></span>

<span data-ttu-id="d07fb-3041">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3041">5</span></span>

<span data-ttu-id="d07fb-3042">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3042">6</span></span>

<span data-ttu-id="d07fb-3043">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3043">7</span></span>

<span data-ttu-id="d07fb-3044">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3044">8</span></span>

<span data-ttu-id="d07fb-3045">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3045">9</span></span>

<span data-ttu-id="d07fb-3046">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3046">1</span></span><br/> <span data-ttu-id="d07fb-3047">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3047">0</span></span><br/>

<span data-ttu-id="d07fb-3048">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3048">1</span></span>

<span data-ttu-id="d07fb-3049">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3049">2</span></span>

<span data-ttu-id="d07fb-3050">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3050">3</span></span>

<span data-ttu-id="d07fb-3051">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3051">4</span></span>

<span data-ttu-id="d07fb-3052">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3052">5</span></span>

<span data-ttu-id="d07fb-3053">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3053">6</span></span>

<span data-ttu-id="d07fb-3054">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3054">7</span></span>

<span data-ttu-id="d07fb-3055">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3055">8</span></span>

<span data-ttu-id="d07fb-3056">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3056">9</span></span>

<span data-ttu-id="d07fb-3057">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3057">2</span></span><br/> <span data-ttu-id="d07fb-3058">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3058">0</span></span><br/>

<span data-ttu-id="d07fb-3059">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3059">1</span></span>

<span data-ttu-id="d07fb-3060">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3060">2</span></span>

<span data-ttu-id="d07fb-3061">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3061">3</span></span>

<span data-ttu-id="d07fb-3062">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3062">4</span></span>

<span data-ttu-id="d07fb-3063">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3063">5</span></span>

<span data-ttu-id="d07fb-3064">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3064">6</span></span>

<span data-ttu-id="d07fb-3065">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3065">7</span></span>

<span data-ttu-id="d07fb-3066">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3066">8</span></span>

<span data-ttu-id="d07fb-3067">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3067">9</span></span>

<span data-ttu-id="d07fb-3068">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3068">3</span></span><br/> <span data-ttu-id="d07fb-3069">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3069">0</span></span><br/>

<span data-ttu-id="d07fb-3070">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3070">1</span></span>

<span data-ttu-id="d07fb-3071">\_iClientVersion</span><span class="sxs-lookup"><span data-stu-id="d07fb-3071">\_iClientVersion</span></span>

<span data-ttu-id="d07fb-3072">\_fClientIsRemote</span><span class="sxs-lookup"><span data-stu-id="d07fb-3072">\_fClientIsRemote</span></span>

<span data-ttu-id="d07fb-3073">\_cbBlob1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3073">\_cbBlob1</span></span>

<span data-ttu-id="d07fb-3074">\_cbBlob2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3074">\_cbBlob2</span></span>

<span data-ttu-id="d07fb-3075">\_Acolchado</span><span class="sxs-lookup"><span data-stu-id="d07fb-3075">\_padding</span></span>

<span data-ttu-id="d07fb-3076">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-3076">...</span></span>

<span data-ttu-id="d07fb-3077">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-3077">...</span></span>

<span data-ttu-id="d07fb-3078">MachineName</span><span class="sxs-lookup"><span data-stu-id="d07fb-3078">MachineName</span></span>

<span data-ttu-id="d07fb-3079">... (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3079">... (variable)</span></span>

<span data-ttu-id="d07fb-3080">UserName</span><span class="sxs-lookup"><span data-stu-id="d07fb-3080">UserName</span></span>

<span data-ttu-id="d07fb-3081">... (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3081">... (variable)</span></span>

<span data-ttu-id="d07fb-3082">\_paddingcPropSets (opcional, variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3082">\_paddingcPropSets (optional, variable)</span></span>

<span data-ttu-id="d07fb-3083">cPropSets</span><span class="sxs-lookup"><span data-stu-id="d07fb-3083">cPropSets</span></span>

<span data-ttu-id="d07fb-3084">PropertySet1 (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3084">PropertySet1 (variable)</span></span>

<span data-ttu-id="d07fb-3085">PropertySet2 (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3085">PropertySet2 (variable)</span></span>

<span data-ttu-id="d07fb-3086">\_paddingExtPropset (opcional, variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3086">\_paddingExtPropset (optional, variable)</span></span>

<span data-ttu-id="d07fb-3087">cExtPropSet</span><span class="sxs-lookup"><span data-stu-id="d07fb-3087">cExtPropSet</span></span>

<span data-ttu-id="d07fb-3088">aPropertySets (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3088">aPropertySets (variable)</span></span>



 

<span data-ttu-id="d07fb-3089">**\_ iClientVersion:** entero de 32 bits que indica si el servidor va a validar el valor de suma de comprobación especificado en el campo ulChecksum de los encabezados de mensaje para los mensajes enviados por el \_ cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3089">**\_iClientVersion**: A 32-bit integer indicating whether the server is to validate the checksum value specified in the \_ulChecksum field of the message headers for messages sent by the client.</span></span> <span data-ttu-id="d07fb-3090">Si el campo iClientVersion está establecido en 0x00000008 o superior, el servidor DEBE validar el valor del campo \_ \_ ulChecksum para los mensajes siguientes:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3090">If the \_iClientVersion field is set to 0x00000008 or greater, the server MUST validate the \_ulChecksum field value for the following messages:</span></span>

-   <span data-ttu-id="d07fb-3091">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-3091">CPMConnectIn</span></span>
-   <span data-ttu-id="d07fb-3092">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-3092">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="d07fb-3093">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-3093">CPMFetchValueIn</span></span>
-   <span data-ttu-id="d07fb-3094">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-3094">CPMGetRowsIn</span></span>
-   <span data-ttu-id="d07fb-3095">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-3095">CPMSetBindingsIn</span></span>

<span data-ttu-id="d07fb-3096">Para obtener más información sobre cómo el servidor valida el valor especificado por el cliente en el campo ulChecksum para los mensajes enumerados anteriormente, consulte la sección 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3096">For details about how the server validates the value specified by the client in the ulChecksum field for the messages listed above, see Section 3.2.5.</span></span>

<span data-ttu-id="d07fb-3097">Si el valor es mayor que 0x00000008, se supone que el cliente es capaz de controlar desplazamientos de 64 bits en mensajes CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3097">If the value is greater than 0x00000008 then the client is assumed capable of handling 64-bit offsets in CPMGetRowsOut messages.</span></span> <span data-ttu-id="d07fb-3098">Consulte la sección 2.2.3.16 para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3098">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="d07fb-3099">*Comportamiento de Windows: en los clientes windows, iClientVersion se establece de la siguiente manera:*</span><span class="sxs-lookup"><span data-stu-id="d07fb-3099">*Windows Behavior: On Windows clients, the iClientVersion is set as follows*:</span></span>



| <span data-ttu-id="d07fb-3100">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-3100">Value</span></span>      | <span data-ttu-id="d07fb-3101">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-3101">Meaning</span></span>                                                              |
|------------|----------------------------------------------------------------------|
| <span data-ttu-id="d07fb-3102">0x00000005</span><span class="sxs-lookup"><span data-stu-id="d07fb-3102">0x00000005</span></span> | <span data-ttu-id="d07fb-3103">El sistema operativo cliente es Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3103">Client OS is Windows 2000.</span></span>                                           |
| <span data-ttu-id="d07fb-3104">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d07fb-3104">0x00000008</span></span> | <span data-ttu-id="d07fb-3105">El sistema operativo cliente es Windows XP de 32 bits o Windows Server 2003 de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3105">Client OS is either 32-bit Windows XP or 32-bit Windows Server 2003.</span></span> |
| <span data-ttu-id="d07fb-3106">0x00010008</span><span class="sxs-lookup"><span data-stu-id="d07fb-3106">0x00010008</span></span> | <span data-ttu-id="d07fb-3107">El sistema operativo cliente es Windows XP de 64 bits o Windows Server 2003 de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3107">Client OS is either 64-bit Windows XP or 64-bit Windows Server 2003.</span></span> |



 

<span data-ttu-id="d07fb-3108">\_**fClientIsRemote:** valor booleano que indica si el cliente se ejecuta en un equipo diferente al servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3108">\_**fClientIsRemote**: A boolean value indicating whether the client is running on a different machine than the server.</span></span> <span data-ttu-id="d07fb-3109">DEBE establecerse en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3109">MUST be set to 0x00000001.</span></span>

<span data-ttu-id="d07fb-3110">\_**cbBlob1:** entero de 32 bits sin signo que indica el tamaño en bytes de los campos cPropSet, PropertySet1 y PropertySet2 combinados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3110">\_**cbBlob1**: A 32-bit unsigned integer indicating the size in bytes of cPropSet, PropertySet1, and PropertySet2 fields, combined.</span></span>

<span data-ttu-id="d07fb-3111">\_**cbBlob2:** entero de 32 bits sin signo que indica el tamaño en bytes de los campos cExPropSet y aPropertySet, combinados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3111">\_**cbBlob2**: A 32-bit unsigned integer indicating the size in bytes of cExPropSet and aPropertySet fields, combined.</span></span>

<span data-ttu-id="d07fb-3112">\_**padding:** 12 bytes de relleno que puede contener valores arbitrarios y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3112">\_**padding**: 12 bytes of padding which can contain arbitrary values and MUST be ignored.</span></span>

<span data-ttu-id="d07fb-3113">**MachineName:** el nombre del equipo del cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3113">**MachineName**: The machine name of the client.</span></span> <span data-ttu-id="d07fb-3114">La cadena de nombre DEBE ser una matriz terminada en NULL de menos de 512 caracteres Unicode, incluido el terminador NULL.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3114">The name string MUST be a null-terminated array of less than 512 Unicode characters, including the NULL terminator.</span></span>

<span data-ttu-id="d07fb-3115">**UserName:** cadena que representa el nombre de usuario de la persona que ejecuta la aplicación que invocó este protocolo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3115">**UserName**: A string that represents the user name of the person who is running the application that invoked this protocol.</span></span> <span data-ttu-id="d07fb-3116">La cadena de nombre DEBE ser una matriz terminada en NULL de menos de 512 caracteres Unicode cuando se concatena con MachineName.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3116">The name string MUST be a null-terminated array of less than 512 Unicode characters when concatenated with MachineName.</span></span>

<span data-ttu-id="d07fb-3117">**\_ paddingcPropSets:** este campo DEBE tener entre 0 y 7 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3117">**\_paddingcPropSets**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="d07fb-3118">El número de bytes DEBE ser el número necesario para realizar el desplazamiento de bytes del campo cPropSets desde el principio del mensaje que contiene esta estructura, que es un múltiplo de 8.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3118">The number of bytes MUST be the number required to make the byte offset of the cPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="d07fb-3119">El valor de los bytes puede ser cualquier valor arbitrario y EL receptor DEBE omitirlo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3119">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="d07fb-3120">**cPropSets:** entero de 32 bits sin signo que indica el número de estructuras CDbPropSet que sigue a este campo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3120">**cPropSets**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span> <span data-ttu-id="d07fb-3121">Este valor DEBE establecerse en 0x0000002.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3121">This value MUST be set to 0x0000002.</span></span>

<span data-ttu-id="d07fb-3122">**PropertySet1:** una estructura CDbPropSet con guidPropertySet que contiene DBPROPSET \_ FSCIFRMWRK EXT (consulte la sección \_ 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="d07fb-3122">**PropertySet1**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_FSCIFRMWRK\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="d07fb-3123">**PropertySet2:** una estructura CDbPropSet con guidPropertySet que contiene DBPROPSET \_ CIFRMWRKCORE EXT (consulte la sección \_ 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="d07fb-3123">**PropertySet2**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_CIFRMWRKCORE\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="d07fb-3124">\_**PaddingExtPropset:** este campo DEBE tener entre 0 y 7 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3124">\_**PaddingExtPropset**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="d07fb-3125">El número de bytes DEBE ser el número necesario para que el desplazamiento de bytes del campo cExtPropSets desde el principio del mensaje que contiene esta estructura sea un múltiplo de 8.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3125">The number of bytes MUST be the number required to make the byte offset of the cExtPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="d07fb-3126">El valor de los bytes puede ser cualquier valor arbitrario y EL receptor DEBE omitirlo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3126">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="d07fb-3127">**cExtPropSet:** entero de 32 bits sin signo que indica el número de estructuras CDbPropSet que sigue a este campo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3127">**cExtPropSet**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span>

<span data-ttu-id="d07fb-3128">**aPropertySets:** matriz de estructuras CDbPropSet que especifican otras propiedades.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3128">**aPropertySets**: An array of CDbPropSet structures specifying other properties.</span></span> <span data-ttu-id="d07fb-3129">El número de elementos de esta matriz DEBE ser igual a cExtPropSet.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3129">The number of elements in this array MUST be equal to cExtPropSet.</span></span>

### <a name="2237-cpmconnectout"></a><span data-ttu-id="d07fb-3130">2.2.3.7 CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-3130">2.2.3.7 CPMConnectOut</span></span>

<span data-ttu-id="d07fb-3131">El mensaje CPMConnectOut contiene una respuesta a un mensaje CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3131">The CPMConnectOut message contains a response to a CPMConnectIn message.</span></span>

<span data-ttu-id="d07fb-3132">El formato del mensaje CPMConnectOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3132">The format of the CPMConnectOut message that follows the header is:</span></span>



<span data-ttu-id="d07fb-3133">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3133">0</span></span>

<span data-ttu-id="d07fb-3134">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3134">1</span></span>

<span data-ttu-id="d07fb-3135">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3135">2</span></span>

<span data-ttu-id="d07fb-3136">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3136">3</span></span>

<span data-ttu-id="d07fb-3137">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3137">4</span></span>

<span data-ttu-id="d07fb-3138">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3138">5</span></span>

<span data-ttu-id="d07fb-3139">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3139">6</span></span>

<span data-ttu-id="d07fb-3140">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3140">7</span></span>

<span data-ttu-id="d07fb-3141">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3141">8</span></span>

<span data-ttu-id="d07fb-3142">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3142">9</span></span>

<span data-ttu-id="d07fb-3143">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3143">1</span></span><br/> <span data-ttu-id="d07fb-3144">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3144">0</span></span><br/>

<span data-ttu-id="d07fb-3145">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3145">1</span></span>

<span data-ttu-id="d07fb-3146">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3146">2</span></span>

<span data-ttu-id="d07fb-3147">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3147">3</span></span>

<span data-ttu-id="d07fb-3148">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3148">4</span></span>

<span data-ttu-id="d07fb-3149">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3149">5</span></span>

<span data-ttu-id="d07fb-3150">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3150">6</span></span>

<span data-ttu-id="d07fb-3151">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3151">7</span></span>

<span data-ttu-id="d07fb-3152">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3152">8</span></span>

<span data-ttu-id="d07fb-3153">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3153">9</span></span>

<span data-ttu-id="d07fb-3154">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3154">2</span></span><br/> <span data-ttu-id="d07fb-3155">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3155">0</span></span><br/>

<span data-ttu-id="d07fb-3156">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3156">1</span></span>

<span data-ttu-id="d07fb-3157">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3157">2</span></span>

<span data-ttu-id="d07fb-3158">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3158">3</span></span>

<span data-ttu-id="d07fb-3159">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3159">4</span></span>

<span data-ttu-id="d07fb-3160">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3160">5</span></span>

<span data-ttu-id="d07fb-3161">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3161">6</span></span>

<span data-ttu-id="d07fb-3162">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3162">7</span></span>

<span data-ttu-id="d07fb-3163">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3163">8</span></span>

<span data-ttu-id="d07fb-3164">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3164">9</span></span>

<span data-ttu-id="d07fb-3165">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3165">3</span></span><br/> <span data-ttu-id="d07fb-3166">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3166">0</span></span><br/>

<span data-ttu-id="d07fb-3167">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3167">1</span></span>

<span data-ttu-id="d07fb-3168">\_serverVersion</span><span class="sxs-lookup"><span data-stu-id="d07fb-3168">\_serverVersion</span></span>

<span data-ttu-id="d07fb-3169">\_reserved (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3169">\_reserved (variable)</span></span>



 

<span data-ttu-id="d07fb-3170">**\_ serverVersion**:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3170">**\_serverVersion**:</span></span>

<span data-ttu-id="d07fb-3171">Entero de 32 bits que indica si el servidor puede admitir desplazamientos de 64 *bits.*</span><span class="sxs-lookup"><span data-stu-id="d07fb-3171">A 32-bit integer, indicating whether the server can support 64-bit offsets *.*</span></span> <span data-ttu-id="d07fb-3172">Consulte la sección 2.2.3.16 para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3172">See section 2.2.3.16 for details.</span></span>



| <span data-ttu-id="d07fb-3173">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-3173">Value</span></span>      | <span data-ttu-id="d07fb-3174">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-3174">Meaning</span></span>                                 |
|------------|-----------------------------------------|
| <span data-ttu-id="d07fb-3175">0x00000007</span><span class="sxs-lookup"><span data-stu-id="d07fb-3175">0x00000007</span></span> | <span data-ttu-id="d07fb-3176">El servidor solo puede enviar desplazamientos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3176">Server is can only send 32-bit offsets.</span></span> |
| <span data-ttu-id="d07fb-3177">0x00010007</span><span class="sxs-lookup"><span data-stu-id="d07fb-3177">0x00010007</span></span> | <span data-ttu-id="d07fb-3178">El servidor puede enviar desplazamientos de 32 o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3178">Server can send 32 or 64-bit offsets.</span></span>   |



 

<span data-ttu-id="d07fb-3179">**\_ reserved:** reservado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3179">**\_reserved**: Reserved.</span></span> <span data-ttu-id="d07fb-3180">El servidor PUEDE enviar un número arbitrario de valores arbitrarios y el cliente DEBE omitir estos valores si están presentes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3180">The server MAY send an arbitrary number of arbitrary values and the client MUST ignore these values if present.</span></span>

### <a name="2238-cpmcreatequeryin"></a><span data-ttu-id="d07fb-3181">2.2.3.8 CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-3181">2.2.3.8 CPMCreateQueryIn</span></span>

<span data-ttu-id="d07fb-3182">El mensaje CPMCreateQueryIn crea una nueva consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3182">The CPMCreateQueryIn message creates a new query.</span></span> <span data-ttu-id="d07fb-3183">El formato del mensaje CPMCreateQueryIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3183">The format of the CPMCreateQueryIn message that follows the header is:</span></span>



<span data-ttu-id="d07fb-3184">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3184">0</span></span>

<span data-ttu-id="d07fb-3185">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3185">1</span></span>

<span data-ttu-id="d07fb-3186">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3186">2</span></span>

<span data-ttu-id="d07fb-3187">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3187">3</span></span>

<span data-ttu-id="d07fb-3188">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3188">4</span></span>

<span data-ttu-id="d07fb-3189">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3189">5</span></span>

<span data-ttu-id="d07fb-3190">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3190">6</span></span>

<span data-ttu-id="d07fb-3191">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3191">7</span></span>

<span data-ttu-id="d07fb-3192">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3192">8</span></span>

<span data-ttu-id="d07fb-3193">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3193">9</span></span>

<span data-ttu-id="d07fb-3194">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3194">1</span></span><br/> <span data-ttu-id="d07fb-3195">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3195">0</span></span><br/>

<span data-ttu-id="d07fb-3196">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3196">1</span></span>

<span data-ttu-id="d07fb-3197">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3197">2</span></span>

<span data-ttu-id="d07fb-3198">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3198">3</span></span>

<span data-ttu-id="d07fb-3199">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3199">4</span></span>

<span data-ttu-id="d07fb-3200">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3200">5</span></span>

<span data-ttu-id="d07fb-3201">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3201">6</span></span>

<span data-ttu-id="d07fb-3202">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3202">7</span></span>

<span data-ttu-id="d07fb-3203">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3203">8</span></span>

<span data-ttu-id="d07fb-3204">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3204">9</span></span>

<span data-ttu-id="d07fb-3205">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3205">2</span></span><br/> <span data-ttu-id="d07fb-3206">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3206">0</span></span><br/>

<span data-ttu-id="d07fb-3207">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3207">1</span></span>

<span data-ttu-id="d07fb-3208">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3208">2</span></span>

<span data-ttu-id="d07fb-3209">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3209">3</span></span>

<span data-ttu-id="d07fb-3210">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3210">4</span></span>

<span data-ttu-id="d07fb-3211">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3211">5</span></span>

<span data-ttu-id="d07fb-3212">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3212">6</span></span>

<span data-ttu-id="d07fb-3213">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3213">7</span></span>

<span data-ttu-id="d07fb-3214">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3214">8</span></span>

<span data-ttu-id="d07fb-3215">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3215">9</span></span>

<span data-ttu-id="d07fb-3216">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3216">3</span></span><br/> <span data-ttu-id="d07fb-3217">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3217">0</span></span><br/>

<span data-ttu-id="d07fb-3218">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3218">1</span></span>

<span data-ttu-id="d07fb-3219">Size</span><span class="sxs-lookup"><span data-stu-id="d07fb-3219">Size</span></span>

<span data-ttu-id="d07fb-3220">CColumnSetPresent</span><span class="sxs-lookup"><span data-stu-id="d07fb-3220">CColumnSetPresent</span></span>

<span data-ttu-id="d07fb-3221">ColumnSet (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3221">ColumnSet (optional)</span></span>

<span data-ttu-id="d07fb-3222">... (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3222">... (variable)</span></span>

<span data-ttu-id="d07fb-3223">CRestrictionPresent.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3223">CRestrictionPresent.</span></span>

<span data-ttu-id="d07fb-3224">Restricción (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3224">Restriction (optional)</span></span>

<span data-ttu-id="d07fb-3225">... (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3225">... (variable)</span></span>

<span data-ttu-id="d07fb-3226">CSortSetPresent</span><span class="sxs-lookup"><span data-stu-id="d07fb-3226">CSortSetPresent</span></span>

<span data-ttu-id="d07fb-3227">SortSet (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3227">SortSet (optional)</span></span>

<span data-ttu-id="d07fb-3228">... (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3228">... (variable)</span></span>

<span data-ttu-id="d07fb-3229">CCategorizationSetPresent</span><span class="sxs-lookup"><span data-stu-id="d07fb-3229">CCategorizationSetPresent</span></span>

<span data-ttu-id="d07fb-3230">CategorizationSet (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3230">CategorizationSet (optional)</span></span>

<span data-ttu-id="d07fb-3231">... (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3231">... (variable)</span></span>

<span data-ttu-id="d07fb-3232">RowSetProperties</span><span class="sxs-lookup"><span data-stu-id="d07fb-3232">RowSetProperties</span></span>

<span data-ttu-id="d07fb-3233">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-3233">...</span></span>

<span data-ttu-id="d07fb-3234">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-3234">...</span></span>

<span data-ttu-id="d07fb-3235">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-3235">...</span></span>

<span data-ttu-id="d07fb-3236">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-3236">...</span></span>

<span data-ttu-id="d07fb-3237">PidMapper (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3237">PidMapper (variable)</span></span>



 

<span data-ttu-id="d07fb-3238">**Tamaño:** entero de 32 bits sin signo que indica el número de bytes desde el principio de este campo hasta el final del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3238">**Size**: A 32-bit unsigned integer indicating the number of bytes from the beginning of this field to the end of the message.</span></span>

<span data-ttu-id="d07fb-3239">**CColumnSetPresent:** campo de bytes que indica si el campo ColumnSet está presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3239">**CColumnSetPresent**: A byte field indicating if the ColumnSet field is present.</span></span> <span data-ttu-id="d07fb-3240">Este campo DEBE establecerse en 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3240">This field MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="d07fb-3241">Si se establece 0x01 el campo CColumnSet DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3241">If set to 0x01 the CColumnSet field MUST be present.</span></span> <span data-ttu-id="d07fb-3242">Si se establece en 0x00, DEBE estar ausente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3242">If set to 0x00, it MUST be absent.</span></span>

<span data-ttu-id="d07fb-3243">**ColumnSet:** estructura CColumnSet que contiene los números de columna en los que se devolverán las propiedades de CPidMapper.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3243">**ColumnSet**: A CColumnSet structure containing the column numbers in which the properties of CPidMapper is to be returned.</span></span>

<span data-ttu-id="d07fb-3244">**CRestrictionPresent:** campo de bytes que indica si el campo Restricción está presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3244">**CRestrictionPresent**: A byte field indicating if the Restriction field is present.</span></span> <span data-ttu-id="d07fb-3245">Si se establece en cualquier valor distinto de cero, el campo Restricción DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3245">If set to any nonzero value, the Restriction field MUST be present.</span></span> <span data-ttu-id="d07fb-3246">Si se establece en 0x00, la restricción DEBE estar ausente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3246">If set to 0x00, Restriction MUST be absent.</span></span>

<span data-ttu-id="d07fb-3247">**Restricción:** estructura CRestriction que contiene el árbol de comandos de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3247">**Restriction**: A CRestriction structure containing the command tree of the query.</span></span>

<span data-ttu-id="d07fb-3248">**CSortSetPresent:** campo de bytes que indica si el campo SortSet está presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3248">**CSortSetPresent**: A byte field indicating if the SortSet field is present.</span></span> <span data-ttu-id="d07fb-3249">Si se establece en cualquier valor distinto de cero, el campo SortSet DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3249">If set to any nonzero value, the SortSet field MUST be present.</span></span> <span data-ttu-id="d07fb-3250">Si se establece en 0x00, SortSet DEBE estar ausente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3250">If set to 0x00, SortSet MUST be absent.</span></span>

<span data-ttu-id="d07fb-3251">**SortSet:** una estructura CSortSet que indica el criterio de ordenación de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3251">**SortSet**: A CSortSet structure indicating the sort order of the query.</span></span>

<span data-ttu-id="d07fb-3252">**CCategorizationSetPresent:** campo de bytes que indica si el campo CCategorizationSet está presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3252">**CCategorizationSetPresent**: A byte field indicating if the CCategorizationSet field is present.</span></span> <span data-ttu-id="d07fb-3253">Si se establece en cualquier valor distinto de cero, el campo CCategorizationSet DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3253">If set to any nonzero value, the CCategorizationSet field MUST be present.</span></span> <span data-ttu-id="d07fb-3254">Si se establece en 0x00, CCategorizationSet DEBE estar ausente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3254">If set to 0x00, CCategorizationSet MUST be absent.</span></span>

<span data-ttu-id="d07fb-3255">**CCategorizationSet:** estructura CCategorizationSet que contiene los grupos de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3255">**CCategorizationSet**: A CCategorizationSet structure that contains the groups for the query.</span></span>

<span data-ttu-id="d07fb-3256">**RowSetProperties:** estructura CRowsetProperties que proporciona información de configuración para la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3256">**RowSetProperties**: A CRowsetProperties structure providing configuration information for the query.</span></span>

<span data-ttu-id="d07fb-3257">**PidMapper:** una estructura CPidMapper que contiene las propiedades que se devuelven en un conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3257">**PidMapper**: A CPidMapper structure containing properties to return in a rowset.</span></span>

### <a name="2239-cpmcreatequeryout"></a><span data-ttu-id="d07fb-3258">2.2.3.9 CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-3258">2.2.3.9 CPMCreateQueryOut</span></span>

<span data-ttu-id="d07fb-3259">El mensaje CPMCreateQueryOut contiene una respuesta a un mensaje CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3259">The CPMCreateQueryOut message contains a response to a CPMCreateQueryIn message.</span></span>

<span data-ttu-id="d07fb-3260">El formato del mensaje CPMCreateQueryOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3260">The format of the CPMCreateQueryOut message that follows the header is:</span></span>



<span data-ttu-id="d07fb-3261">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3261">0</span></span>

<span data-ttu-id="d07fb-3262">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3262">1</span></span>

<span data-ttu-id="d07fb-3263">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3263">2</span></span>

<span data-ttu-id="d07fb-3264">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3264">3</span></span>

<span data-ttu-id="d07fb-3265">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3265">4</span></span>

<span data-ttu-id="d07fb-3266">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3266">5</span></span>

<span data-ttu-id="d07fb-3267">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3267">6</span></span>

<span data-ttu-id="d07fb-3268">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3268">7</span></span>

<span data-ttu-id="d07fb-3269">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3269">8</span></span>

<span data-ttu-id="d07fb-3270">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3270">9</span></span>

<span data-ttu-id="d07fb-3271">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3271">1</span></span><br/> <span data-ttu-id="d07fb-3272">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3272">0</span></span><br/>

<span data-ttu-id="d07fb-3273">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3273">1</span></span>

<span data-ttu-id="d07fb-3274">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3274">2</span></span>

<span data-ttu-id="d07fb-3275">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3275">3</span></span>

<span data-ttu-id="d07fb-3276">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3276">4</span></span>

<span data-ttu-id="d07fb-3277">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3277">5</span></span>

<span data-ttu-id="d07fb-3278">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3278">6</span></span>

<span data-ttu-id="d07fb-3279">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3279">7</span></span>

<span data-ttu-id="d07fb-3280">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3280">8</span></span>

<span data-ttu-id="d07fb-3281">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3281">9</span></span>

<span data-ttu-id="d07fb-3282">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3282">2</span></span><br/> <span data-ttu-id="d07fb-3283">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3283">0</span></span><br/>

<span data-ttu-id="d07fb-3284">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3284">1</span></span>

<span data-ttu-id="d07fb-3285">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3285">2</span></span>

<span data-ttu-id="d07fb-3286">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3286">3</span></span>

<span data-ttu-id="d07fb-3287">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3287">4</span></span>

<span data-ttu-id="d07fb-3288">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3288">5</span></span>

<span data-ttu-id="d07fb-3289">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3289">6</span></span>

<span data-ttu-id="d07fb-3290">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3290">7</span></span>

<span data-ttu-id="d07fb-3291">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3291">8</span></span>

<span data-ttu-id="d07fb-3292">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3292">9</span></span>

<span data-ttu-id="d07fb-3293">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3293">3</span></span><br/> <span data-ttu-id="d07fb-3294">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3294">0</span></span><br/>

<span data-ttu-id="d07fb-3295">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3295">1</span></span>

<span data-ttu-id="d07fb-3296">\_fTrueSequential</span><span class="sxs-lookup"><span data-stu-id="d07fb-3296">\_fTrueSequential</span></span>

<span data-ttu-id="d07fb-3297">\_fWorkIdUnique</span><span class="sxs-lookup"><span data-stu-id="d07fb-3297">\_fWorkIdUnique</span></span>

<span data-ttu-id="d07fb-3298">aCursors</span><span class="sxs-lookup"><span data-stu-id="d07fb-3298">aCursors</span></span>



 

<span data-ttu-id="d07fb-3299">**\_ fTrueSequential:** un valor booleano informativo que indica si se puede esperar que la consulta proporcione resultados más rápido.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3299">**\_fTrueSequential**: An informative boolean value indicating if the query can be expected to provide results faster.</span></span> <span data-ttu-id="d07fb-3300">Cuando se establece en 0x00000001 para la consulta proporcionada en CPMCreateQueryIn, el servidor puede usar el índice de forma que los resultados de la consulta probablemente se entreguen más rápido.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3300">When set to 0x00000001 for the query provided in CPMCreateQueryIn, the server can use the index in such a way that query results will likely be delivered faster.</span></span> <span data-ttu-id="d07fb-3301">Cuando se establece en 0x00000000, habría una latencia mayor en la entrega de los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3301">When set to 0x00000000, there would be a bigger latency in delivering query results.</span></span> <span data-ttu-id="d07fb-3302">NO DEBE establecerse en ningún otro valor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3302">MUST not be set to any other value.</span></span>

<span data-ttu-id="d07fb-3303">**\_ fWorkIdUnique:** valor booleano que indica si los identificadores de documento a los que apuntan los cursores son únicos a lo largo de los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3303">**\_fWorkIdUnique**: A boolean value indicating if the document identifiers pointed by the cursors are unique throughout query results.</span></span> <span data-ttu-id="d07fb-3304">Si se establece en 0x00000001, los identificadores son únicos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3304">If set to 0x00000001, the identifiers are unique.</span></span> <span data-ttu-id="d07fb-3305">Si se establece en 0x00000000, solo son únicos en todo el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3305">If set to 0x00000000, they are unique only throughout the rowset.</span></span>

<span data-ttu-id="d07fb-3306">**aCursors:** matriz de enteros de 32 bits sin signo que representan los identificadores de los cursores, con el número de elementos igual al número de categorías del campo CategorizationSet del mensaje CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3306">**aCursors**: An array of 32-bit unsigned integers representing the handles to cursors, with the number of elements equal to the number of categories in the CategorizationSet field of CPMCreateQueryIn message.</span></span>

### <a name="22310-cpmgetquerystatusin"></a><span data-ttu-id="d07fb-3307">2.2.3.10 CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-3307">2.2.3.10 CPMGetQueryStatusIn</span></span>

<span data-ttu-id="d07fb-3308">El mensaje CPMGetQueryStatusIn solicita el estado de una consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3308">The CPMGetQueryStatusIn message requests the status of a query.</span></span> <span data-ttu-id="d07fb-3309">El formato del mensaje CPMGetQueryStatusIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3309">The format of the CPMGetQueryStatusIn message that follows the header is:</span></span>



<span data-ttu-id="d07fb-3310">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3310">0</span></span>

<span data-ttu-id="d07fb-3311">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3311">1</span></span>

<span data-ttu-id="d07fb-3312">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3312">2</span></span>

<span data-ttu-id="d07fb-3313">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3313">3</span></span>

<span data-ttu-id="d07fb-3314">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3314">4</span></span>

<span data-ttu-id="d07fb-3315">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3315">5</span></span>

<span data-ttu-id="d07fb-3316">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3316">6</span></span>

<span data-ttu-id="d07fb-3317">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3317">7</span></span>

<span data-ttu-id="d07fb-3318">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3318">8</span></span>

<span data-ttu-id="d07fb-3319">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3319">9</span></span>

<span data-ttu-id="d07fb-3320">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3320">1</span></span><br/> <span data-ttu-id="d07fb-3321">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3321">0</span></span><br/>

<span data-ttu-id="d07fb-3322">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3322">1</span></span>

<span data-ttu-id="d07fb-3323">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3323">2</span></span>

<span data-ttu-id="d07fb-3324">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3324">3</span></span>

<span data-ttu-id="d07fb-3325">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3325">4</span></span>

<span data-ttu-id="d07fb-3326">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3326">5</span></span>

<span data-ttu-id="d07fb-3327">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3327">6</span></span>

<span data-ttu-id="d07fb-3328">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3328">7</span></span>

<span data-ttu-id="d07fb-3329">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3329">8</span></span>

<span data-ttu-id="d07fb-3330">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3330">9</span></span>

<span data-ttu-id="d07fb-3331">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3331">2</span></span><br/> <span data-ttu-id="d07fb-3332">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3332">0</span></span><br/>

<span data-ttu-id="d07fb-3333">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3333">1</span></span>

<span data-ttu-id="d07fb-3334">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3334">2</span></span>

<span data-ttu-id="d07fb-3335">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3335">3</span></span>

<span data-ttu-id="d07fb-3336">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3336">4</span></span>

<span data-ttu-id="d07fb-3337">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3337">5</span></span>

<span data-ttu-id="d07fb-3338">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3338">6</span></span>

<span data-ttu-id="d07fb-3339">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3339">7</span></span>

<span data-ttu-id="d07fb-3340">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3340">8</span></span>

<span data-ttu-id="d07fb-3341">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3341">9</span></span>

<span data-ttu-id="d07fb-3342">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3342">3</span></span><br/> <span data-ttu-id="d07fb-3343">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3343">0</span></span><br/>

<span data-ttu-id="d07fb-3344">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3344">1</span></span>

<span data-ttu-id="d07fb-3345">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="d07fb-3345">\_hCursor</span></span>



 

<span data-ttu-id="d07fb-3346">**\_ hCursor:** entero de 32 bits sin signo que representa el identificador del mensaje CPMCreateQueryOut que identifica la consulta para la que se va a recuperar información de estado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3346">**\_hCursor**: A 32-bit unsigned integer representing the handle from CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

### <a name="22311-cpmgetquerystatusout"></a><span data-ttu-id="d07fb-3347">2.2.3.11 CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-3347">2.2.3.11 CPMGetQueryStatusOut</span></span>

<span data-ttu-id="d07fb-3348">El mensaje CPMGetQueryStatusOut responde a un mensaje CPMGetQueryStatusIn con el estado de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3348">The CPMGetQueryStatusOut message replies to a CPMGetQueryStatusIn message with the status of the query.</span></span> <span data-ttu-id="d07fb-3349">El formato del mensaje CPMGetQueryStatusOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3349">The format of the CPMGetQueryStatusOut message that follows the header is:</span></span>



<span data-ttu-id="d07fb-3350">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3350">0</span></span>

<span data-ttu-id="d07fb-3351">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3351">1</span></span>

<span data-ttu-id="d07fb-3352">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3352">2</span></span>

<span data-ttu-id="d07fb-3353">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3353">3</span></span>

<span data-ttu-id="d07fb-3354">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3354">4</span></span>

<span data-ttu-id="d07fb-3355">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3355">5</span></span>

<span data-ttu-id="d07fb-3356">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3356">6</span></span>

<span data-ttu-id="d07fb-3357">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3357">7</span></span>

<span data-ttu-id="d07fb-3358">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3358">8</span></span>

<span data-ttu-id="d07fb-3359">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3359">9</span></span>

<span data-ttu-id="d07fb-3360">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3360">1</span></span><br/> <span data-ttu-id="d07fb-3361">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3361">0</span></span><br/>

<span data-ttu-id="d07fb-3362">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3362">1</span></span>

<span data-ttu-id="d07fb-3363">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3363">2</span></span>

<span data-ttu-id="d07fb-3364">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3364">3</span></span>

<span data-ttu-id="d07fb-3365">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3365">4</span></span>

<span data-ttu-id="d07fb-3366">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3366">5</span></span>

<span data-ttu-id="d07fb-3367">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3367">6</span></span>

<span data-ttu-id="d07fb-3368">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3368">7</span></span>

<span data-ttu-id="d07fb-3369">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3369">8</span></span>

<span data-ttu-id="d07fb-3370">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3370">9</span></span>

<span data-ttu-id="d07fb-3371">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3371">2</span></span><br/> <span data-ttu-id="d07fb-3372">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3372">0</span></span><br/>

<span data-ttu-id="d07fb-3373">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3373">1</span></span>

<span data-ttu-id="d07fb-3374">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3374">2</span></span>

<span data-ttu-id="d07fb-3375">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3375">3</span></span>

<span data-ttu-id="d07fb-3376">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3376">4</span></span>

<span data-ttu-id="d07fb-3377">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3377">5</span></span>

<span data-ttu-id="d07fb-3378">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3378">6</span></span>

<span data-ttu-id="d07fb-3379">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3379">7</span></span>

<span data-ttu-id="d07fb-3380">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3380">8</span></span>

<span data-ttu-id="d07fb-3381">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3381">9</span></span>

<span data-ttu-id="d07fb-3382">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3382">3</span></span><br/> <span data-ttu-id="d07fb-3383">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3383">0</span></span><br/>

<span data-ttu-id="d07fb-3384">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3384">1</span></span>

<span data-ttu-id="d07fb-3385">\_Estado</span><span class="sxs-lookup"><span data-stu-id="d07fb-3385">\_Status</span></span>



 

<span data-ttu-id="d07fb-3386">**\_ Estado:** máscara de bits de valores definidos en las tablas siguientes, que describe la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3386">**\_Status**: A bitmask of values defined in the tables below, that describes the query.</span></span>

<span data-ttu-id="d07fb-3387">En la tabla siguiente se enumeran los valores STAT obtenidos mediante la realización de una operación AND bit a bit \_ \* en Status con \_ 0x00000007.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3387">The following table lists STAT\_\* values obtained by performing a bitwise AND operation on \_Status with 0x00000007.</span></span> <span data-ttu-id="d07fb-3388">El resultado DEBE ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3388">The result MUST be one of the following:</span></span>



| <span data-ttu-id="d07fb-3389">Constante</span><span class="sxs-lookup"><span data-stu-id="d07fb-3389">Constant</span></span>                 | <span data-ttu-id="d07fb-3390">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-3390">Meaning</span></span>                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-3391">Stat \_ BUSY 0x00000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-3391">STAT\_BUSY 0x00000000</span></span>    | <span data-ttu-id="d07fb-3392">La consulta asincrónica todavía se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3392">The asynchronous query is still running.</span></span>                                          |
| <span data-ttu-id="d07fb-3393">ERROR \_ DE STAT 0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-3393">STAT\_ERROR 0x00000001</span></span>   | <span data-ttu-id="d07fb-3394">La consulta está en estado de error.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3394">The query is in an error state.</span></span>                                                   |
| <span data-ttu-id="d07fb-3395">STAT \_ DONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-3395">STAT\_DONE 0x00000002</span></span>    | <span data-ttu-id="d07fb-3396">La consulta se ha completado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3396">The query is complete.</span></span>                                                            |
| <span data-ttu-id="d07fb-3397">Actualización \_ de estadísticas 0x00000003</span><span class="sxs-lookup"><span data-stu-id="d07fb-3397">STAT\_REFRESH 0x00000003</span></span> | <span data-ttu-id="d07fb-3398">La consulta está completa, pero las actualizaciones están generando cálculos de consulta adicionales.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3398">The query is complete, but updates are resulting in additional query computation.</span></span> |



 

<span data-ttu-id="d07fb-3399">En la tabla siguiente se enumeran los bits STAT \_ \* adicionales que se pueden establecer de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3399">The following table lists additional STAT\_\* bits that can be set independently.</span></span>



| <span data-ttu-id="d07fb-3400">Constante</span><span class="sxs-lookup"><span data-stu-id="d07fb-3400">Constant</span></span>                                    | <span data-ttu-id="d07fb-3401">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-3401">Meaning</span></span>                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07fb-3402">PALABRAS \_ DE RUIDO DE \_ ESTADÍSTICAS 0x00000010</span><span class="sxs-lookup"><span data-stu-id="d07fb-3402">STAT\_NOISE\_WORDS 0x00000010</span></span>               | <span data-ttu-id="d07fb-3403">Las palabras ruido se reemplazaron por caracteres comodín en la consulta de contenido.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3403">Noise words were replaced by wildcard characters in the content query.</span></span>                                                              |
| <span data-ttu-id="d07fb-3404">CONTENIDO \_ DE \_ \_ ESTADÍSTICAS NO ACTUALIZADO \_ 0X00000020</span><span class="sxs-lookup"><span data-stu-id="d07fb-3404">STAT\_CONTENT\_OUT\_OF\_DATE 0x00000020</span></span>     | <span data-ttu-id="d07fb-3405">Los resultados de la consulta podrían ser incorrectos porque la consulta implicaba archivos modificados, pero sin indexar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3405">The results of the query might be incorrect because the query involved modified, but un-indexed, files.</span></span>                             |
| <span data-ttu-id="d07fb-3406">Actualización \_ de \_ estadísticas incompleta 0x00000040</span><span class="sxs-lookup"><span data-stu-id="d07fb-3406">STAT\_REFRESH\_INCOMPLETE 0x00000040</span></span>        | <span data-ttu-id="d07fb-3407">Los resultados de la consulta podrían ser incorrectos porque la consulta implicaba archivos modificados y re indexados cuyo contenido no se incluyó.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3407">The results of the query might be incorrect because the query involved modified and re-indexed files whose content wasn't included.</span></span> |
| <span data-ttu-id="d07fb-3408">STAT \_ CONTENT QUERY INCOMPLETE \_ \_ 0x00000080</span><span class="sxs-lookup"><span data-stu-id="d07fb-3408">STAT\_CONTENT\_QUERY\_INCOMPLETE 0x00000080</span></span> | <span data-ttu-id="d07fb-3409">La consulta de contenido era demasiado compleja para completarse o para la enumeración necesaria en lugar de usar el índice de contenido.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3409">The content query was too complex to complete or required enumeration instead of use of the content index.</span></span>                          |
| <span data-ttu-id="d07fb-3410">SE \_ HA SUPERADO EL LÍMITE DE TIEMPO DE \_ \_ 0X00000100</span><span class="sxs-lookup"><span data-stu-id="d07fb-3410">STAT\_TIME\_LIMIT\_EXCEEDED 0x00000100</span></span>      | <span data-ttu-id="d07fb-3411">Los resultados de la consulta pueden ser incorrectos porque el tiempo de ejecución de la consulta alcanzó el tiempo máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3411">The results of the query might be incorrect because the query execution time reached the maximum allowable time.</span></span>                    |



 

### <a name="22312-cpmgetquerystatusexin"></a><span data-ttu-id="d07fb-3412">2.2.3.12 CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-3412">2.2.3.12 CPMGetQueryStatusExIn</span></span>

<span data-ttu-id="d07fb-3413">El mensaje CPMGetQueryStatusExIn solicita el estado de una consulta e información adicional, como el número de documentos que se han indexado, el número de documentos que quedan por indexar, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3413">The CPMGetQueryStatusExIn message requests the status of a query and additional information, such as the number of documents that have been indexed, the number of documents remaining to be indexed, and so on.</span></span> <span data-ttu-id="d07fb-3414">El formato del mensaje CPMGetQueryStatusExIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3414">The format of the CPMGetQueryStatusExIn message that follows the header is:</span></span>



<span data-ttu-id="d07fb-3415">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3415">0</span></span>

<span data-ttu-id="d07fb-3416">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3416">1</span></span>

<span data-ttu-id="d07fb-3417">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3417">2</span></span>

<span data-ttu-id="d07fb-3418">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3418">3</span></span>

<span data-ttu-id="d07fb-3419">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3419">4</span></span>

<span data-ttu-id="d07fb-3420">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3420">5</span></span>

<span data-ttu-id="d07fb-3421">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3421">6</span></span>

<span data-ttu-id="d07fb-3422">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3422">7</span></span>

<span data-ttu-id="d07fb-3423">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3423">8</span></span>

<span data-ttu-id="d07fb-3424">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3424">9</span></span>

<span data-ttu-id="d07fb-3425">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3425">1</span></span><br/> <span data-ttu-id="d07fb-3426">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3426">0</span></span><br/>

<span data-ttu-id="d07fb-3427">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3427">1</span></span>

<span data-ttu-id="d07fb-3428">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3428">2</span></span>

<span data-ttu-id="d07fb-3429">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3429">3</span></span>

<span data-ttu-id="d07fb-3430">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3430">4</span></span>

<span data-ttu-id="d07fb-3431">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3431">5</span></span>

<span data-ttu-id="d07fb-3432">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3432">6</span></span>

<span data-ttu-id="d07fb-3433">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3433">7</span></span>

<span data-ttu-id="d07fb-3434">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3434">8</span></span>

<span data-ttu-id="d07fb-3435">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3435">9</span></span>

<span data-ttu-id="d07fb-3436">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3436">2</span></span><br/> <span data-ttu-id="d07fb-3437">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3437">0</span></span><br/>

<span data-ttu-id="d07fb-3438">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3438">1</span></span>

<span data-ttu-id="d07fb-3439">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3439">2</span></span>

<span data-ttu-id="d07fb-3440">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3440">3</span></span>

<span data-ttu-id="d07fb-3441">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3441">4</span></span>

<span data-ttu-id="d07fb-3442">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3442">5</span></span>

<span data-ttu-id="d07fb-3443">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3443">6</span></span>

<span data-ttu-id="d07fb-3444">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3444">7</span></span>

<span data-ttu-id="d07fb-3445">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3445">8</span></span>

<span data-ttu-id="d07fb-3446">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3446">9</span></span>

<span data-ttu-id="d07fb-3447">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3447">3</span></span><br/> <span data-ttu-id="d07fb-3448">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3448">0</span></span><br/>

<span data-ttu-id="d07fb-3449">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3449">1</span></span>

<span data-ttu-id="d07fb-3450">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="d07fb-3450">\_hCursor</span></span>

<span data-ttu-id="d07fb-3451">\_Bmk</span><span class="sxs-lookup"><span data-stu-id="d07fb-3451">\_bmk</span></span>



 

<span data-ttu-id="d07fb-3452">**\_ hCursor:** valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut que identifica la consulta para la que se va a recuperar información de estado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3452">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

<span data-ttu-id="d07fb-3453">**\_ bmk:** valor de 32 bits que indica el identificador de un marcador cuya posición se debe recuperar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3453">**\_bmk**: A 32-bit value indicating the handle of a bookmark whose position should be retrieved.</span></span>

### <a name="22313-cpmgetquerystatusexout"></a><span data-ttu-id="d07fb-3454">2.2.3.13 CPMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-3454">2.2.3.13 CPMGetQueryStatusExOut</span></span>

<span data-ttu-id="d07fb-3455">El mensaje CPMGetQueryStatusExOut responde a un mensaje CPMGetQueryStatusExIn con el estado de la consulta y otra información de estado, como se describe en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3455">The CPMGetQueryStatusExOut message replies to a CPMGetQueryStatusExIn message with both the status of the query and other status information, as outlined in the diagram below.</span></span> <span data-ttu-id="d07fb-3456">El formato del mensaje CPMGetQueryStatusExOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3456">The format of the CPMGetQueryStatusExOut message that follows the header is:</span></span>



<span data-ttu-id="d07fb-3457">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3457">0</span></span>

<span data-ttu-id="d07fb-3458">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3458">1</span></span>

<span data-ttu-id="d07fb-3459">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3459">2</span></span>

<span data-ttu-id="d07fb-3460">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3460">3</span></span>

<span data-ttu-id="d07fb-3461">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3461">4</span></span>

<span data-ttu-id="d07fb-3462">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3462">5</span></span>

<span data-ttu-id="d07fb-3463">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3463">6</span></span>

<span data-ttu-id="d07fb-3464">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3464">7</span></span>

<span data-ttu-id="d07fb-3465">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3465">8</span></span>

<span data-ttu-id="d07fb-3466">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3466">9</span></span>

<span data-ttu-id="d07fb-3467">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3467">1</span></span><br/> <span data-ttu-id="d07fb-3468">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3468">0</span></span><br/>

<span data-ttu-id="d07fb-3469">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3469">1</span></span>

<span data-ttu-id="d07fb-3470">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3470">2</span></span>

<span data-ttu-id="d07fb-3471">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3471">3</span></span>

<span data-ttu-id="d07fb-3472">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3472">4</span></span>

<span data-ttu-id="d07fb-3473">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3473">5</span></span>

<span data-ttu-id="d07fb-3474">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3474">6</span></span>

<span data-ttu-id="d07fb-3475">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3475">7</span></span>

<span data-ttu-id="d07fb-3476">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3476">8</span></span>

<span data-ttu-id="d07fb-3477">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3477">9</span></span>

<span data-ttu-id="d07fb-3478">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3478">2</span></span><br/> <span data-ttu-id="d07fb-3479">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3479">0</span></span><br/>

<span data-ttu-id="d07fb-3480">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3480">1</span></span>

<span data-ttu-id="d07fb-3481">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3481">2</span></span>

<span data-ttu-id="d07fb-3482">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3482">3</span></span>

<span data-ttu-id="d07fb-3483">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3483">4</span></span>

<span data-ttu-id="d07fb-3484">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3484">5</span></span>

<span data-ttu-id="d07fb-3485">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3485">6</span></span>

<span data-ttu-id="d07fb-3486">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3486">7</span></span>

<span data-ttu-id="d07fb-3487">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3487">8</span></span>

<span data-ttu-id="d07fb-3488">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3488">9</span></span>

<span data-ttu-id="d07fb-3489">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3489">3</span></span><br/> <span data-ttu-id="d07fb-3490">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3490">0</span></span><br/>

<span data-ttu-id="d07fb-3491">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3491">1</span></span>

<span data-ttu-id="d07fb-3492">\_Estado</span><span class="sxs-lookup"><span data-stu-id="d07fb-3492">\_Status</span></span>

<span data-ttu-id="d07fb-3493">\_cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="d07fb-3493">\_cFilteredDocuments</span></span>

<span data-ttu-id="d07fb-3494">\_cDocumentsToFilter</span><span class="sxs-lookup"><span data-stu-id="d07fb-3494">\_cDocumentsToFilter</span></span>

<span data-ttu-id="d07fb-3495">\_dwRatioFinishedDenominator</span><span class="sxs-lookup"><span data-stu-id="d07fb-3495">\_dwRatioFinishedDenominator</span></span>

<span data-ttu-id="d07fb-3496">\_dwRatioFinishedNumerator</span><span class="sxs-lookup"><span data-stu-id="d07fb-3496">\_dwRatioFinishedNumerator</span></span>

<span data-ttu-id="d07fb-3497">\_iRowBmk</span><span class="sxs-lookup"><span data-stu-id="d07fb-3497">\_iRowBmk</span></span>

<span data-ttu-id="d07fb-3498">\_cRowsTotal</span><span class="sxs-lookup"><span data-stu-id="d07fb-3498">\_cRowsTotal</span></span>



 

<span data-ttu-id="d07fb-3499">**\_ Estado:** una de las estadísticas \_ \* valores especificados en la sección 2.2.3.11.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3499">**\_Status**: One of the STAT\_\* values specified in Section 2.2.3.11.</span></span>

<span data-ttu-id="d07fb-3500">**\_ cFilteredDocuments:** entero de 32 bits sin signo que indica el número de documentos que se han indexado</span><span class="sxs-lookup"><span data-stu-id="d07fb-3500">**\_cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents that have been indexed</span></span>

<span data-ttu-id="d07fb-3501">**\_ cDocumentsToFilter:** entero de 32 bits sin signo que indica el número de documentos que quedan por indexar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3501">**\_cDocumentsToFilter**: A 32-bit unsigned integer indicating the number of documents that still remain to be indexed.</span></span>

<span data-ttu-id="d07fb-3502">**\_ dwRatioFinishedDenominator:** entero de 32 bits sin signo que indica el denominador de la proporción de documentos que la consulta ha terminado de procesar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3502">**\_dwRatioFinishedDenominator**: A 32-bit unsigned integer indicating the denominator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="d07fb-3503">**\_ dwRatioFinishedNumerator:** entero de 32 bits sin signo que indica el numerador de la proporción de documentos que la consulta ha terminado de procesar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3503">**\_dwRatioFinishedNumerator**: A 32-bit unsigned integer indicating the numerator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="d07fb-3504">**\_ iRowBmk:** entero de 32 bits sin signo que indica la posición aproximada del marcador en el conjunto de filas en términos de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3504">**\_iRowBmk**: A 32-bit unsigned integer indicating the approximate position of the bookmark in the rowset in terms of rows.</span></span>

<span data-ttu-id="d07fb-3505">**\_ cRowsTotal:** entero de 32 bits sin signo que especifica el número total de filas del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3505">**\_cRowsTotal**: A 32-bit unsigned integer specifying the total number of rows in the rowset.</span></span>

### <a name="22314-cpmsetbindingsin"></a><span data-ttu-id="d07fb-3506">2.2.3.14 CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-3506">2.2.3.14 CPMSetBindingsIn</span></span>

<span data-ttu-id="d07fb-3507">El mensaje CPMSetBindingsIn solicita el enlace de columnas a un conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3507">The CPMSetBindingsIn message requests the binding of columns to a rowset.</span></span> <span data-ttu-id="d07fb-3508">El servidor responderá al mensaje de solicitud CPMSetBindingsIn mediante la sección de encabezado del mensaje CPMBindingsIn con los resultados de la solicitud contenida en el campo \_ de estado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3508">The server will reply to the CPMSetBindingsIn request message using the header section of the CPMBindingsIn message with the results of the request contained in the \_status field.</span></span> <span data-ttu-id="d07fb-3509">El formato del mensaje CPMSetBindingsIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3509">The format of the CPMSetBindingsIn message that follows the header is:</span></span>



<span data-ttu-id="d07fb-3510">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3510">0</span></span>

<span data-ttu-id="d07fb-3511">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3511">1</span></span>

<span data-ttu-id="d07fb-3512">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3512">2</span></span>

<span data-ttu-id="d07fb-3513">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3513">3</span></span>

<span data-ttu-id="d07fb-3514">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3514">4</span></span>

<span data-ttu-id="d07fb-3515">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3515">5</span></span>

<span data-ttu-id="d07fb-3516">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3516">6</span></span>

<span data-ttu-id="d07fb-3517">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3517">7</span></span>

<span data-ttu-id="d07fb-3518">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3518">8</span></span>

<span data-ttu-id="d07fb-3519">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3519">9</span></span>

<span data-ttu-id="d07fb-3520">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3520">1</span></span><br/> <span data-ttu-id="d07fb-3521">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3521">0</span></span><br/>

<span data-ttu-id="d07fb-3522">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3522">1</span></span>

<span data-ttu-id="d07fb-3523">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3523">2</span></span>

<span data-ttu-id="d07fb-3524">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3524">3</span></span>

<span data-ttu-id="d07fb-3525">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3525">4</span></span>

<span data-ttu-id="d07fb-3526">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3526">5</span></span>

<span data-ttu-id="d07fb-3527">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3527">6</span></span>

<span data-ttu-id="d07fb-3528">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3528">7</span></span>

<span data-ttu-id="d07fb-3529">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3529">8</span></span>

<span data-ttu-id="d07fb-3530">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3530">9</span></span>

<span data-ttu-id="d07fb-3531">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3531">2</span></span><br/> <span data-ttu-id="d07fb-3532">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3532">0</span></span><br/>

<span data-ttu-id="d07fb-3533">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3533">1</span></span>

<span data-ttu-id="d07fb-3534">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3534">2</span></span>

<span data-ttu-id="d07fb-3535">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3535">3</span></span>

<span data-ttu-id="d07fb-3536">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3536">4</span></span>

<span data-ttu-id="d07fb-3537">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3537">5</span></span>

<span data-ttu-id="d07fb-3538">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3538">6</span></span>

<span data-ttu-id="d07fb-3539">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3539">7</span></span>

<span data-ttu-id="d07fb-3540">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3540">8</span></span>

<span data-ttu-id="d07fb-3541">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3541">9</span></span>

<span data-ttu-id="d07fb-3542">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3542">3</span></span><br/> <span data-ttu-id="d07fb-3543">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3543">0</span></span><br/>

<span data-ttu-id="d07fb-3544">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3544">1</span></span>

<span data-ttu-id="d07fb-3545">\_hCursor (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3545">\_hCursor (optional)</span></span>

<span data-ttu-id="d07fb-3546">\_cbRow (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3546">\_cbRow (optional)</span></span>

<span data-ttu-id="d07fb-3547">\_cbBindingDesc (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3547">\_cbBindingDesc (optional)</span></span>

<span data-ttu-id="d07fb-3548">\_dummy (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3548">\_dummy (optional)</span></span>

<span data-ttu-id="d07fb-3549">cColumns (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3549">cColumns (optional)</span></span>

<span data-ttu-id="d07fb-3550">aColumns (variable, opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3550">aColumns (variable, optional)</span></span>



 

<span data-ttu-id="d07fb-3551">**\_ hCursor:** valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut que identifica la fila para la que se establecen los enlaces.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3551">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message that identifies the row for which to set bindings.</span></span> <span data-ttu-id="d07fb-3552">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3552">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="d07fb-3553">**\_ cbRow:** entero de 32 bits sin signo que indica el tamaño, en bytes, de una fila.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3553">**\_cbRow**: A 32-bit unsigned integer indicating the size, in bytes, of a row.</span></span> <span data-ttu-id="d07fb-3554">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3554">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="d07fb-3555">**\_ cbBindingDesc:** entero de 32 bits sin signo que indica la longitud, en bytes, de los campos que sigue al \_ campo ficticio.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3555">**\_cbBindingDesc**: A 32-bit unsigned integer indicating the length, in bytes, of the fields following the \_dummy field.</span></span> <span data-ttu-id="d07fb-3556">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3556">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="d07fb-3557">**\_ dummy:** este campo no se usa y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3557">**\_dummy**: This field is unused and MUST be ignored.</span></span> <span data-ttu-id="d07fb-3558">Se puede establecer en cualquier valor arbitrario.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3558">It can be set to any arbitrary value.</span></span> <span data-ttu-id="d07fb-3559">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3559">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="d07fb-3560">**cColumns:** entero de 32 bits sin signo que indica el número de elementos de la matriz aColumns.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3560">**cColumns**: A 32-bit unsigned integer indicating the number of elements in the aColumns array.</span></span> <span data-ttu-id="d07fb-3561">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3561">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="d07fb-3562">**aColumns:** matriz de las estructuras CTableColumn que describen las columnas de una fila del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3562">**aColumns**: An array of the CTableColumn structures describing the columns of a row in the rowset.</span></span> <span data-ttu-id="d07fb-3563">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3563">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="d07fb-3564">Las estructuras de la matriz DEBEN estar separadas por 0 a 3 bytes de relleno, de forma que cada estructura tenga una alineación de 4 bytes desde el principio de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3564">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="d07fb-3565">Estos bytes de relleno pueden ser cualquier valor arbitrario y DEBEN omitirse al recibirse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3565">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22315-cpmgetrowsin"></a><span data-ttu-id="d07fb-3566">2.2.3.15 CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-3566">2.2.3.15 CPMGetRowsIn</span></span>

<span data-ttu-id="d07fb-3567">El mensaje CPMGetRowsIn solicita filas de una consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3567">The CPMGetRowsIn message requests rows from a query.</span></span> <span data-ttu-id="d07fb-3568">El formato del mensaje CPMGetRowsIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3568">The format of the CPMGetRowsIn message that follows the header is:</span></span>



<span data-ttu-id="d07fb-3569">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3569">0</span></span>

<span data-ttu-id="d07fb-3570">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3570">1</span></span>

<span data-ttu-id="d07fb-3571">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3571">2</span></span>

<span data-ttu-id="d07fb-3572">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3572">3</span></span>

<span data-ttu-id="d07fb-3573">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3573">4</span></span>

<span data-ttu-id="d07fb-3574">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3574">5</span></span>

<span data-ttu-id="d07fb-3575">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3575">6</span></span>

<span data-ttu-id="d07fb-3576">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3576">7</span></span>

<span data-ttu-id="d07fb-3577">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3577">8</span></span>

<span data-ttu-id="d07fb-3578">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3578">9</span></span>

<span data-ttu-id="d07fb-3579">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3579">1</span></span><br/> <span data-ttu-id="d07fb-3580">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3580">0</span></span><br/>

<span data-ttu-id="d07fb-3581">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3581">1</span></span>

<span data-ttu-id="d07fb-3582">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3582">2</span></span>

<span data-ttu-id="d07fb-3583">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3583">3</span></span>

<span data-ttu-id="d07fb-3584">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3584">4</span></span>

<span data-ttu-id="d07fb-3585">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3585">5</span></span>

<span data-ttu-id="d07fb-3586">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3586">6</span></span>

<span data-ttu-id="d07fb-3587">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3587">7</span></span>

<span data-ttu-id="d07fb-3588">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3588">8</span></span>

<span data-ttu-id="d07fb-3589">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3589">9</span></span>

<span data-ttu-id="d07fb-3590">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3590">2</span></span><br/> <span data-ttu-id="d07fb-3591">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3591">0</span></span><br/>

<span data-ttu-id="d07fb-3592">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3592">1</span></span>

<span data-ttu-id="d07fb-3593">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3593">2</span></span>

<span data-ttu-id="d07fb-3594">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3594">3</span></span>

<span data-ttu-id="d07fb-3595">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3595">4</span></span>

<span data-ttu-id="d07fb-3596">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3596">5</span></span>

<span data-ttu-id="d07fb-3597">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3597">6</span></span>

<span data-ttu-id="d07fb-3598">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3598">7</span></span>

<span data-ttu-id="d07fb-3599">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3599">8</span></span>

<span data-ttu-id="d07fb-3600">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3600">9</span></span>

<span data-ttu-id="d07fb-3601">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3601">3</span></span><br/> <span data-ttu-id="d07fb-3602">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3602">0</span></span><br/>

<span data-ttu-id="d07fb-3603">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3603">1</span></span>

<span data-ttu-id="d07fb-3604">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="d07fb-3604">\_hCursor</span></span>

<span data-ttu-id="d07fb-3605">\_cRowsToTransfer</span><span class="sxs-lookup"><span data-stu-id="d07fb-3605">\_cRowsToTransfer</span></span>

<span data-ttu-id="d07fb-3606">\_cbRowWidth</span><span class="sxs-lookup"><span data-stu-id="d07fb-3606">\_cbRowWidth</span></span>

<span data-ttu-id="d07fb-3607">\_cbSeek</span><span class="sxs-lookup"><span data-stu-id="d07fb-3607">\_cbSeek</span></span>

<span data-ttu-id="d07fb-3608">\_cbReserved</span><span class="sxs-lookup"><span data-stu-id="d07fb-3608">\_cbReserved</span></span>

<span data-ttu-id="d07fb-3609">\_cbReadBuffer</span><span class="sxs-lookup"><span data-stu-id="d07fb-3609">\_cbReadBuffer</span></span>

<span data-ttu-id="d07fb-3610">\_ulClientBase</span><span class="sxs-lookup"><span data-stu-id="d07fb-3610">\_ulClientBase</span></span>

<span data-ttu-id="d07fb-3611">\_fBwdFetch</span><span class="sxs-lookup"><span data-stu-id="d07fb-3611">\_fBwdFetch</span></span>

<span data-ttu-id="d07fb-3612">eType</span><span class="sxs-lookup"><span data-stu-id="d07fb-3612">eType</span></span>

<span data-ttu-id="d07fb-3613">\_chapt</span><span class="sxs-lookup"><span data-stu-id="d07fb-3613">\_chapt</span></span>

<span data-ttu-id="d07fb-3614">SeekDescription</span><span class="sxs-lookup"><span data-stu-id="d07fb-3614">SeekDescription</span></span>

<span data-ttu-id="d07fb-3615">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-3615">...</span></span>

<span data-ttu-id="d07fb-3616">... (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3616">... (variable)</span></span>



 

<span data-ttu-id="d07fb-3617">**\_ hCursor:** valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut que identifica la consulta para la que se recuperan filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3617">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve rows.</span></span>

<span data-ttu-id="d07fb-3618">**\_ cRowsToTransfer:** entero de 32 bits sin signo que indica el número máximo de filas que el cliente desea recibir en respuesta a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3618">**\_cRowsToTransfer**: A 32-bit unsigned integer indicating the maximum number of rows the client wishes to receive in response to this message.</span></span>

<span data-ttu-id="d07fb-3619">**\_ cbRowWidth:** entero de 32 bits sin signo que indica la longitud de una fila, en bytes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3619">**\_cbRowWidth**: A 32-bit unsigned integer indicating the length of a row, in bytes.</span></span>

<span data-ttu-id="d07fb-3620">**\_ cbSeek:** entero de 32 bits sin signo que indica el tamaño del mensaje que comienza por eType.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3620">**\_cbSeek**: A 32-bit unsigned integer indicating the size of the message beginning with eType.</span></span>

<span data-ttu-id="d07fb-3621">**\_ cbReserved:** entero de 32 bits sin signo que indica el tamaño, en bytes, de un mensaje CPMGetRowsOut (sin los campos Rows y SeekDescriptions).</span><span class="sxs-lookup"><span data-stu-id="d07fb-3621">**\_cbReserved**: A 32-bit unsigned integer indicating the size, in bytes, of a CPMGetRowsOut message (without the Rows and SeekDescriptions fields).</span></span> <span data-ttu-id="d07fb-3622">Este valor de este campo se agrega al valor del campo cbSeek y, a continuación, se va a usar para calcular el desplazamiento del campo Rows en el mensaje \_ CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3622">This value in this field is added to the value of the \_cbSeek field, and then is to be used to calculate the offset of Rows field in CPMGetRowsOut message.</span></span>

<span data-ttu-id="d07fb-3623">**\_ cbReadBuffer:** entero de 32 bits sin signo que DEBE establecerse en el máximo del valor de cbRowWidth o 1000 veces el valor de \_ cRowsToTransfer, redondeado al múltiplo de \_ 512 bytes más cercano.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3623">**\_cbReadBuffer**: A 32-bit unsigned integer which MUST be set to the maximum of the value of \_cbRowWidth or 1000 times the value of \_cRowsToTransfer, rounded up to the nearest 512 byte multiple.</span></span> <span data-ttu-id="d07fb-3624">El valor NO DEBE superar 0x00004000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3624">The value MUST NOT exceed 0x00004000.</span></span>

<span data-ttu-id="d07fb-3625">**\_ ulClientBase:** entero de 32 bits sin signo que indica el valor base que se usará para los cálculos de puntero en el búfer de fila.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3625">**\_ulClientBase**: A 32-bit unsigned integer indicating the base value to use for pointer calculations in the row buffer.</span></span> <span data-ttu-id="d07fb-3626">Si se usan desplazamientos de 64 bits, el campo reserved2 del encabezado del mensaje se usa como los 32 bits superiores y ulClientBase como los 32 bits inferiores de un valor de \_ 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3626">If 64-bit offsets are being used, then the reserved2 field of the message header is used as the upper 32-bits and \_ulClientBase as the lower 32-bits of a 64-bit value.</span></span> <span data-ttu-id="d07fb-3627">Consulte la sección 2.2.3.16 para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3627">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="d07fb-3628">**\_ fBwdFetch:** entero de 32 bits sin signo que indica el orden en el que se capturan las filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3628">**\_fBwdFetch**: A 32-bit unsigned integer indicating the order in which to fetch the rows.</span></span> <span data-ttu-id="d07fb-3629">Si se establece en 0x00000001, las filas se capturarán en orden inverso.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3629">If set to 0x00000001, the rows are to be fetched in reverse order.</span></span> <span data-ttu-id="d07fb-3630">Si se establece en 0x00000000, las filas se capturarán en orden de reenvío.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3630">If set to 0x00000000, the rows are to be fetched in forward order.</span></span> <span data-ttu-id="d07fb-3631">NO DEBE establecerse en ningún otro valor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3631">MUST NOT be set to any other values.</span></span>

<span data-ttu-id="d07fb-3632">**eType:** entero de 32 bits sin signo que contiene uno de los valores siguientes para indicar el tipo de operación que se debe realizar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3632">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of operation to perform.</span></span>



| <span data-ttu-id="d07fb-3633">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-3633">Value</span></span>                         | <span data-ttu-id="d07fb-3634">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-3634">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="d07fb-3635">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-3635">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="d07fb-3636">SeekDescription contiene una estructura CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3636">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="d07fb-3637">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-3637">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="d07fb-3638">SeekDescription contiene una estructura CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3638">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="d07fb-3639">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="d07fb-3639">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="d07fb-3640">SeekDescription contiene una estructura CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3640">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="d07fb-3641">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="d07fb-3641">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="d07fb-3642">SeekDescription contiene una estructura CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3642">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="d07fb-3643">**\_ chapt:** valor de 32 bits que representa el identificador del capítulo del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3643">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="d07fb-3644">**SeekDescription:** este campo DEBE contener una estructura del tipo indicado por el valor eType.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3644">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType value.</span></span>

### <a name="22316-cpmgetrowsout"></a><span data-ttu-id="d07fb-3645">2.2.3.16 CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-3645">2.2.3.16 CPMGetRowsOut</span></span>

<span data-ttu-id="d07fb-3646">El mensaje CPMGetRowsOut responde a un mensaje CPMGetRowsIn con las filas de una consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3646">The CPMGetRowsOut message replies to a CPMGetRowsIn message with the rows of a query.</span></span> <span data-ttu-id="d07fb-3647">Los servidores DEBEN dar formato a los desplazamientos a los tipos de datos de longitud variable en el campo Filas de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3647">Servers MUST format offsets to variable length data types in the Rows field as follows:</span></span>

-   <span data-ttu-id="d07fb-3648">El cliente indicó que era un sistema de 32 bits (0x00000008 o menos en el campo iClientVersion de CPMConnectIn): los desplazamientos son enteros de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3648">Client indicated it was a 32-bit system (0x00000008 or less in the iClientVersion field of CPMConnectIn): Offsets are 32-bit integers.</span></span>
-   <span data-ttu-id="d07fb-3649">El cliente indicó que era un sistema de 64 bits (iClientVersion > 0x00000008 en CPMConnectIn) y Server indicó que era un sistema de 32 bits (serverVersion establecido en \_ \_ 0x00000007 en CPMConnectOut): los desplazamientos son enteros de 32 bits</span><span class="sxs-lookup"><span data-stu-id="d07fb-3649">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 32-bit system (\_serverVersion set to 0x00000007 in CPMConnectOut): Offsets are 32-bit integers</span></span>
-   <span data-ttu-id="d07fb-3650">El cliente indicó que era un sistema de 64 bits (iClientVersion > 0x00000008 en CPMConnectIn) y Server indicó que era un sistema de 64 bits (serverVersion establecido en \_ \_ 0x00010007 en CPMConnectOut): los desplazamientos son enteros de 64 bits</span><span class="sxs-lookup"><span data-stu-id="d07fb-3650">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 64-bit system (\_serverVersion set to 0x00010007 in CPMConnectOut): Offsets are 64-bit integers</span></span>

<span data-ttu-id="d07fb-3651">El formato del mensaje CPMGetRowsOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3651">The format of the CPMGetRowsOut message that follows the header is:</span></span>



<span data-ttu-id="d07fb-3652">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3652">0</span></span>

<span data-ttu-id="d07fb-3653">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3653">1</span></span>

<span data-ttu-id="d07fb-3654">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3654">2</span></span>

<span data-ttu-id="d07fb-3655">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3655">3</span></span>

<span data-ttu-id="d07fb-3656">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3656">4</span></span>

<span data-ttu-id="d07fb-3657">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3657">5</span></span>

<span data-ttu-id="d07fb-3658">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3658">6</span></span>

<span data-ttu-id="d07fb-3659">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3659">7</span></span>

<span data-ttu-id="d07fb-3660">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3660">8</span></span>

<span data-ttu-id="d07fb-3661">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3661">9</span></span>

<span data-ttu-id="d07fb-3662">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3662">1</span></span><br/> <span data-ttu-id="d07fb-3663">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3663">0</span></span><br/>

<span data-ttu-id="d07fb-3664">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3664">1</span></span>

<span data-ttu-id="d07fb-3665">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3665">2</span></span>

<span data-ttu-id="d07fb-3666">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3666">3</span></span>

<span data-ttu-id="d07fb-3667">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3667">4</span></span>

<span data-ttu-id="d07fb-3668">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3668">5</span></span>

<span data-ttu-id="d07fb-3669">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3669">6</span></span>

<span data-ttu-id="d07fb-3670">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3670">7</span></span>

<span data-ttu-id="d07fb-3671">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3671">8</span></span>

<span data-ttu-id="d07fb-3672">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3672">9</span></span>

<span data-ttu-id="d07fb-3673">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3673">2</span></span><br/> <span data-ttu-id="d07fb-3674">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3674">0</span></span><br/>

<span data-ttu-id="d07fb-3675">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3675">1</span></span>

<span data-ttu-id="d07fb-3676">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3676">2</span></span>

<span data-ttu-id="d07fb-3677">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3677">3</span></span>

<span data-ttu-id="d07fb-3678">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3678">4</span></span>

<span data-ttu-id="d07fb-3679">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3679">5</span></span>

<span data-ttu-id="d07fb-3680">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3680">6</span></span>

<span data-ttu-id="d07fb-3681">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3681">7</span></span>

<span data-ttu-id="d07fb-3682">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3682">8</span></span>

<span data-ttu-id="d07fb-3683">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3683">9</span></span>

<span data-ttu-id="d07fb-3684">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3684">3</span></span><br/> <span data-ttu-id="d07fb-3685">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3685">0</span></span><br/>

<span data-ttu-id="d07fb-3686">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3686">1</span></span>

<span data-ttu-id="d07fb-3687">\_cRowsReturned</span><span class="sxs-lookup"><span data-stu-id="d07fb-3687">\_cRowsReturned</span></span>

<span data-ttu-id="d07fb-3688">eType</span><span class="sxs-lookup"><span data-stu-id="d07fb-3688">eType</span></span>

<span data-ttu-id="d07fb-3689">\_chapt</span><span class="sxs-lookup"><span data-stu-id="d07fb-3689">\_chapt</span></span>

<span data-ttu-id="d07fb-3690">SeekDescription (opcional, variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3690">SeekDescription (optional, variable)</span></span>

<span data-ttu-id="d07fb-3691">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-3691">...</span></span>

<span data-ttu-id="d07fb-3692">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-3692">...</span></span>

<span data-ttu-id="d07fb-3693">paddingRows (opcional, variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3693">paddingRows (optional, variable)</span></span>

<span data-ttu-id="d07fb-3694">Filas</span><span class="sxs-lookup"><span data-stu-id="d07fb-3694">Rows</span></span>



 

<span data-ttu-id="d07fb-3695">**\_ cRowsReturned:** entero de 32 bits sin signo que indica el número de filas devueltas en Filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3695">**\_cRowsReturned**: A 32-bit unsigned integer indicating the number of rows returned in Rows.</span></span>

<span data-ttu-id="d07fb-3696">**eType:** entero de 32 bits sin signo que contiene uno de los valores siguientes para indicar el tipo de operación rowseek que se debe realizar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3696">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of rowseek operation to perform</span></span>



| <span data-ttu-id="d07fb-3697">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-3697">Value</span></span>                         | <span data-ttu-id="d07fb-3698">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-3698">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="d07fb-3699">eRowsSeekNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-3699">eRowsSeekNone 0x00000000</span></span>      | <span data-ttu-id="d07fb-3700">Sin SeekDescription, o bien ignore el campo SeekDescription.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3700">No SeekDescription, ignore SeekDescription field.</span></span>        |
| <span data-ttu-id="d07fb-3701">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-3701">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="d07fb-3702">SeekDescription contiene una estructura CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3702">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="d07fb-3703">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-3703">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="d07fb-3704">SeekDescription contiene una estructura CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3704">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="d07fb-3705">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="d07fb-3705">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="d07fb-3706">SeekDescription contiene una estructura CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3706">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="d07fb-3707">eRowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="d07fb-3707">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="d07fb-3708">SeekDescription contiene una estructura CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3708">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="d07fb-3709">**\_ chapt:** valor de 32 bits que representa el identificador del capítulo del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3709">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="d07fb-3710">**SeekDescription:** este campo DEBE contener una estructura del tipo indicado por el campo eType.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3710">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType field.</span></span>

<span data-ttu-id="d07fb-3711">**paddingRows:** este campo DEBE tener una longitud suficiente (de 0 a cbReserved-1 bytes) para rellenar el campo Rows hasta el desplazamiento cbReserved desde el principio de un mensaje, donde cbReserved es el valor del mensaje \_ \_ \_ CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3711">**paddingRows**: This field MUST be of sufficient length (0 to \_cbReserved-1 bytes) to pad the Rows field to \_cbReserved offset from the beginning of a message, where \_cbReserved is the value in the CPMGetRowsIn message.</span></span> <span data-ttu-id="d07fb-3712">Los bytes de relleno utilizados en este campo pueden ser cualquier valor arbitrario.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3712">Padding bytes used in this field can be any arbitrary value.</span></span> <span data-ttu-id="d07fb-3713">El receptor DEBE omitir este campo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3713">This field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="d07fb-3714">**Filas:** los datos de fila tienen el formato indicado por la información de columna en el mensaje CPMSetBindingsIn más reciente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3714">**Rows**: Row data, is formatted as prescribed by column information in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="d07fb-3715">Las filas DEBEN almacenarse en orden de reenvío (por ejemplo, la fila 1 antes de la fila 2).</span><span class="sxs-lookup"><span data-stu-id="d07fb-3715">Rows MUST be stored in forward order (e.g. row 1 before row 2).</span></span>

<span data-ttu-id="d07fb-3716">Las columnas de tamaño fijo DEBEN almacenarse en los desplazamientos especificados por el mensaje CPMSetBindingsIn más reciente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3716">Fixed-sized columns MUST be stored at the offsets specified by the most recent CPMSetBindingsIn message.</span></span>

<span data-ttu-id="d07fb-3717">Las columnas de tamaño variable (por ejemplo, cadenas) DEBEN almacenarse de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3717">Variable-sized columns (e.g., strings) MUST be stored as follows:</span></span>

-   <span data-ttu-id="d07fb-3718">Los propios datos de la variable (por ejemplo, la cadena) se almacenan cerca del final del búfer en orden descendente (por ejemplo, la colección de todos los datos de variables para la fila 1 está al final, la fila 2 siguiente más cercana, etc.).</span><span class="sxs-lookup"><span data-stu-id="d07fb-3718">The variable data itself (e.g. the string) is stored near the end of the buffer in descending order (e.g. the collection of all variable data for row 1 is at the end, row 2 next closest, etc.).</span></span>
-   <span data-ttu-id="d07fb-3719">El área de tamaño fijo (al principio del búfer de fila) DEBE contener un CRowVariant para cada columna, almacenado en el desplazamiento especificado en el mensaje CPMSetBindingsIn más reciente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3719">The fixed sized area (at the beginning of the row buffer) MUST contain a CRowVariant for each column, stored at the offset specified in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="d07fb-3720">vType DEBE contener el tipo de datos (por ejemplo, VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="d07fb-3720">vType MUST contain the data type (ex: VT\_LPWSTR).</span></span> <span data-ttu-id="d07fb-3721">Si, según lo determinado por las reglas al principio de la sección de esta sección, se usan desplazamientos de 32 bits, el campo Offset de CRowVariant DEBE contener un valor de 32 bits que sea el desplazamiento de los datos de variable desde el principio del mensaje CPMGetRowsOut, más el valor de ulClientBase especificado en el mensaje \_ CPMGetRowsIn más reciente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3721">If, as determined by the rules at the beginning of section this section, 32-bit offsets are being used then the Offset field in CRowVariant MUST contain a 32-bit value that is the offset of the variable data from the beginning of the CPMGetRowsOut message, plus the value of \_ulClientBase specified in the most recent CPMGetRowsIn message.</span></span> <span data-ttu-id="d07fb-3722">Si se usan desplazamientos de 64 bits, el campo Offset de CRowVariant DEBE contener un valor de 64 bits que sea el desplazamiento desde el principio del mensaje CPMGetRowsOut, agregado a un valor de 64 bits compuesto por el uso de ulClientBase como los 32 bits inferiores y \_ \_ ulReserved2 como los 32 bits altos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3722">If 64-bit offsets are being used then the Offset field in CRowVariant MUST contain a 64-bit value that is the offset from the beginning of the CPMGetRowsOut message, added to a 64-bit value composed by using \_ulClientBase as the low 32-bits and \_ulReserved2 as the high 32-bits.</span></span>

<span data-ttu-id="d07fb-3723">Por ejemplo, si el mensaje CPMSetBindingsIn especificaba dos columnas -Size (VT \_ I4) y Title \_ (VT LPWSTR)-y ulClientBase de CPMGetRowsIn era 0x10000 dos filas aparecerán como \_ sigue.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3723">For example, if the CPMSetBindingsIn message specified two columns-Size (VT\_I4) and Title (VT\_LPWSTR)-and \_ulClientBase from CPMGetRowsIn was 0x10000 then two rows would appear as follows.</span></span> <span data-ttu-id="d07fb-3724">La sección marcada en gris es la parte de longitud fija del búfer.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3724">The section marked in grey is the fixed-length part of the buffer.</span></span>

![Ejemplo de mensaje cpmsetbindingsin](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a><span data-ttu-id="d07fb-3726">2.2.3.17 CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-3726">2.2.3.17 CPMRatioFinishedIn</span></span>

<span data-ttu-id="d07fb-3727">El mensaje CPMRatioFinishedIn solicita el porcentaje de finalización de una consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3727">The CPMRatioFinishedIn message requests the completion percentage of a query.</span></span> <span data-ttu-id="d07fb-3728">El formato del mensaje CPMRatioFinishedIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3728">The format of the CPMRatioFinishedIn message that follows the header is:</span></span>



<span data-ttu-id="d07fb-3729">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3729">0</span></span>

<span data-ttu-id="d07fb-3730">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3730">1</span></span>

<span data-ttu-id="d07fb-3731">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3731">2</span></span>

<span data-ttu-id="d07fb-3732">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3732">3</span></span>

<span data-ttu-id="d07fb-3733">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3733">4</span></span>

<span data-ttu-id="d07fb-3734">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3734">5</span></span>

<span data-ttu-id="d07fb-3735">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3735">6</span></span>

<span data-ttu-id="d07fb-3736">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3736">7</span></span>

<span data-ttu-id="d07fb-3737">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3737">8</span></span>

<span data-ttu-id="d07fb-3738">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3738">9</span></span>

<span data-ttu-id="d07fb-3739">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3739">1</span></span><br/> <span data-ttu-id="d07fb-3740">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3740">0</span></span><br/>

<span data-ttu-id="d07fb-3741">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3741">1</span></span>

<span data-ttu-id="d07fb-3742">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3742">2</span></span>

<span data-ttu-id="d07fb-3743">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3743">3</span></span>

<span data-ttu-id="d07fb-3744">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3744">4</span></span>

<span data-ttu-id="d07fb-3745">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3745">5</span></span>

<span data-ttu-id="d07fb-3746">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3746">6</span></span>

<span data-ttu-id="d07fb-3747">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3747">7</span></span>

<span data-ttu-id="d07fb-3748">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3748">8</span></span>

<span data-ttu-id="d07fb-3749">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3749">9</span></span>

<span data-ttu-id="d07fb-3750">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3750">2</span></span><br/> <span data-ttu-id="d07fb-3751">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3751">0</span></span><br/>

<span data-ttu-id="d07fb-3752">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3752">1</span></span>

<span data-ttu-id="d07fb-3753">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3753">2</span></span>

<span data-ttu-id="d07fb-3754">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3754">3</span></span>

<span data-ttu-id="d07fb-3755">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3755">4</span></span>

<span data-ttu-id="d07fb-3756">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3756">5</span></span>

<span data-ttu-id="d07fb-3757">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3757">6</span></span>

<span data-ttu-id="d07fb-3758">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3758">7</span></span>

<span data-ttu-id="d07fb-3759">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3759">8</span></span>

<span data-ttu-id="d07fb-3760">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3760">9</span></span>

<span data-ttu-id="d07fb-3761">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3761">3</span></span><br/> <span data-ttu-id="d07fb-3762">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3762">0</span></span><br/>

<span data-ttu-id="d07fb-3763">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3763">1</span></span>

<span data-ttu-id="d07fb-3764">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="d07fb-3764">\_hCursor</span></span>

<span data-ttu-id="d07fb-3765">\_fQuick</span><span class="sxs-lookup"><span data-stu-id="d07fb-3765">\_fQuick</span></span>



 

<span data-ttu-id="d07fb-3766">**\_ hCursor: identificador** del mensaje CPMCreateQueryOut que identifica la consulta para la que se va a solicitar información de finalización.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3766">**\_hCursor**: The handle from CPMCreateQueryOut message identifying the query for which to request completion information.</span></span>

<span data-ttu-id="d07fb-3767">**\_ fQuick:** DEBE establecerse en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3767">**\_fQuick**: MUST be set to 0x00000001.</span></span> <span data-ttu-id="d07fb-3768">El servidor no usa y DEBE omitirlo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3768">Unused and MUST be ignored by the server.</span></span>

### <a name="22318-cpmratiofinishedout"></a><span data-ttu-id="d07fb-3769">2.2.3.18 CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-3769">2.2.3.18 CPMRatioFinishedOut</span></span>

<span data-ttu-id="d07fb-3770">El mensaje CPMRatioFinishedOut responde a un mensaje CPMRatioFinishedIn con la proporción de finalización de una consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3770">The CPMRatioFinishedOut message replies to a CPMRatioFinishedIn message with the completion ratio of a query.</span></span> <span data-ttu-id="d07fb-3771">El formato del mensaje CPMRatioFinishedOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3771">The format of the CPMRatioFinishedOut message that follows the header is:</span></span>



<span data-ttu-id="d07fb-3772">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3772">0</span></span>

<span data-ttu-id="d07fb-3773">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3773">1</span></span>

<span data-ttu-id="d07fb-3774">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3774">2</span></span>

<span data-ttu-id="d07fb-3775">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3775">3</span></span>

<span data-ttu-id="d07fb-3776">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3776">4</span></span>

<span data-ttu-id="d07fb-3777">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3777">5</span></span>

<span data-ttu-id="d07fb-3778">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3778">6</span></span>

<span data-ttu-id="d07fb-3779">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3779">7</span></span>

<span data-ttu-id="d07fb-3780">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3780">8</span></span>

<span data-ttu-id="d07fb-3781">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3781">9</span></span>

<span data-ttu-id="d07fb-3782">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3782">1</span></span><br/> <span data-ttu-id="d07fb-3783">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3783">0</span></span><br/>

<span data-ttu-id="d07fb-3784">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3784">1</span></span>

<span data-ttu-id="d07fb-3785">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3785">2</span></span>

<span data-ttu-id="d07fb-3786">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3786">3</span></span>

<span data-ttu-id="d07fb-3787">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3787">4</span></span>

<span data-ttu-id="d07fb-3788">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3788">5</span></span>

<span data-ttu-id="d07fb-3789">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3789">6</span></span>

<span data-ttu-id="d07fb-3790">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3790">7</span></span>

<span data-ttu-id="d07fb-3791">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3791">8</span></span>

<span data-ttu-id="d07fb-3792">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3792">9</span></span>

<span data-ttu-id="d07fb-3793">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3793">2</span></span><br/> <span data-ttu-id="d07fb-3794">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3794">0</span></span><br/>

<span data-ttu-id="d07fb-3795">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3795">1</span></span>

<span data-ttu-id="d07fb-3796">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3796">2</span></span>

<span data-ttu-id="d07fb-3797">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3797">3</span></span>

<span data-ttu-id="d07fb-3798">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3798">4</span></span>

<span data-ttu-id="d07fb-3799">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3799">5</span></span>

<span data-ttu-id="d07fb-3800">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3800">6</span></span>

<span data-ttu-id="d07fb-3801">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3801">7</span></span>

<span data-ttu-id="d07fb-3802">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3802">8</span></span>

<span data-ttu-id="d07fb-3803">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3803">9</span></span>

<span data-ttu-id="d07fb-3804">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3804">3</span></span><br/> <span data-ttu-id="d07fb-3805">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3805">0</span></span><br/>

<span data-ttu-id="d07fb-3806">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3806">1</span></span>

<span data-ttu-id="d07fb-3807">\_ ulNumerator</span><span class="sxs-lookup"><span data-stu-id="d07fb-3807">\_ ulNumerator</span></span>

<span data-ttu-id="d07fb-3808">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="d07fb-3808">\_ulDenominator</span></span>

<span data-ttu-id="d07fb-3809">\_Cuervos</span><span class="sxs-lookup"><span data-stu-id="d07fb-3809">\_cRows</span></span>

<span data-ttu-id="d07fb-3810">\_fNewRows</span><span class="sxs-lookup"><span data-stu-id="d07fb-3810">\_fNewRows</span></span>



 

<span data-ttu-id="d07fb-3811">**\_ ulNumerator:** entero de 32 bits sin signo que indica el numerador de la proporción de finalización en términos de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3811">**\_ulNumerator**: A 32-bit unsigned integer indicating the numerator of the completion ratio in terms of rows.</span></span>

<span data-ttu-id="d07fb-3812">**\_ ulDenominator:** entero de 32 bits sin signo que indica el denominador de la proporción de finalización en términos de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3812">**\_ulDenominator**: A 32-bit unsigned integer indicating the denominator of the completion ratio in terms of rows.</span></span> <span data-ttu-id="d07fb-3813">DEBE ser mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3813">MUST be greater than zero.</span></span>

<span data-ttu-id="d07fb-3814">**\_ cRows:** entero de 32 bits sin signo que indica el número total de filas de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3814">**\_cRows**: A 32-bit unsigned integer indicating the total number of rows for the query.</span></span>

<span data-ttu-id="d07fb-3815">**\_ fNewRows:** valor booleano que indica si hay nuevas filas disponibles.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3815">**\_fNewRows**: A boolean value indicating if there are new rows available.</span></span> <span data-ttu-id="d07fb-3816">Un valor de 0x00000001 indica que hay nuevas filas disponibles en el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3816">A value of 0x00000001 indicates that new rows are available in the rowset.</span></span> <span data-ttu-id="d07fb-3817">Un valor de 0x00000000 indica que el conjunto de filas no contiene ninguna fila nueva.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3817">A value of 0x00000000 indicates that the rowset does not contain any new rows.</span></span> <span data-ttu-id="d07fb-3818">Este campo NO DEBE establecerse en ningún otro valor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3818">This field MUST NOT be set to any other values.</span></span>

### <a name="22319-cpmfetchvaluein"></a><span data-ttu-id="d07fb-3819">2.2.3.19 CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-3819">2.2.3.19 CPMFetchValueIn</span></span>

<span data-ttu-id="d07fb-3820">El mensaje CPMFetchValueIn solicita un valor de propiedad demasiado grande para devolverlo en un conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3820">The CPMFetchValueIn message requests a property value that was too large to return in a rowset.</span></span> <span data-ttu-id="d07fb-3821">Como se especifica en la sección 3.2.4.2.5, este mensaje se envía repetidamente para recuperar todos los bytes de la propiedad, actualizando cbSoFar para cada uno, hasta que el campo fMoreExists del mensaje \_ \_ CPMFetchValueOut se establece en **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="d07fb-3821">As specified in section 3.2.4.2.5, this message is sent repeatedly to retrieve all bytes of the property, updating \_cbSoFar for each, until the \_fMoreExists field of CPMFetchValueOut message is set to **FALSE**.</span></span>

<span data-ttu-id="d07fb-3822">El formato del mensaje CPMFetchValueIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3822">The format of the CPMFetchValueIn message that follows the header is:</span></span>



<span data-ttu-id="d07fb-3823">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3823">0</span></span>

<span data-ttu-id="d07fb-3824">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3824">1</span></span>

<span data-ttu-id="d07fb-3825">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3825">2</span></span>

<span data-ttu-id="d07fb-3826">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3826">3</span></span>

<span data-ttu-id="d07fb-3827">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3827">4</span></span>

<span data-ttu-id="d07fb-3828">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3828">5</span></span>

<span data-ttu-id="d07fb-3829">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3829">6</span></span>

<span data-ttu-id="d07fb-3830">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3830">7</span></span>

<span data-ttu-id="d07fb-3831">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3831">8</span></span>

<span data-ttu-id="d07fb-3832">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3832">9</span></span>

<span data-ttu-id="d07fb-3833">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3833">1</span></span><br/> <span data-ttu-id="d07fb-3834">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3834">0</span></span><br/>

<span data-ttu-id="d07fb-3835">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3835">1</span></span>

<span data-ttu-id="d07fb-3836">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3836">2</span></span>

<span data-ttu-id="d07fb-3837">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3837">3</span></span>

<span data-ttu-id="d07fb-3838">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3838">4</span></span>

<span data-ttu-id="d07fb-3839">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3839">5</span></span>

<span data-ttu-id="d07fb-3840">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3840">6</span></span>

<span data-ttu-id="d07fb-3841">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3841">7</span></span>

<span data-ttu-id="d07fb-3842">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3842">8</span></span>

<span data-ttu-id="d07fb-3843">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3843">9</span></span>

<span data-ttu-id="d07fb-3844">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3844">2</span></span><br/> <span data-ttu-id="d07fb-3845">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3845">0</span></span><br/>

<span data-ttu-id="d07fb-3846">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3846">1</span></span>

<span data-ttu-id="d07fb-3847">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3847">2</span></span>

<span data-ttu-id="d07fb-3848">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3848">3</span></span>

<span data-ttu-id="d07fb-3849">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3849">4</span></span>

<span data-ttu-id="d07fb-3850">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3850">5</span></span>

<span data-ttu-id="d07fb-3851">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3851">6</span></span>

<span data-ttu-id="d07fb-3852">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3852">7</span></span>

<span data-ttu-id="d07fb-3853">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3853">8</span></span>

<span data-ttu-id="d07fb-3854">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3854">9</span></span>

<span data-ttu-id="d07fb-3855">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3855">3</span></span><br/> <span data-ttu-id="d07fb-3856">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3856">0</span></span><br/>

<span data-ttu-id="d07fb-3857">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3857">1</span></span>

<span data-ttu-id="d07fb-3858">\_Wid</span><span class="sxs-lookup"><span data-stu-id="d07fb-3858">\_wid</span></span>

<span data-ttu-id="d07fb-3859">\_cbSoFar</span><span class="sxs-lookup"><span data-stu-id="d07fb-3859">\_cbSoFar</span></span>

<span data-ttu-id="d07fb-3860">\_cbPropSpec</span><span class="sxs-lookup"><span data-stu-id="d07fb-3860">\_cbPropSpec</span></span>

<span data-ttu-id="d07fb-3861">\_cbChunk</span><span class="sxs-lookup"><span data-stu-id="d07fb-3861">\_cbChunk</span></span>

<span data-ttu-id="d07fb-3862">PropSpec (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3862">PropSpec (variable)</span></span>

<span data-ttu-id="d07fb-3863">...</span><span class="sxs-lookup"><span data-stu-id="d07fb-3863">...</span></span>

<span data-ttu-id="d07fb-3864">\_padding (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3864">\_padding (variable)</span></span>



 

<span data-ttu-id="d07fb-3865">**\_ wid:** entero de 32 bits sin signo que contiene información sobre el identificador de documento que identifica el documento para el que se debe capturar una propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3865">**\_wid**: A 32-bit unsigned integer containing information about the document ID identifying the document for which a property should be fetched.</span></span>

<span data-ttu-id="d07fb-3866">**\_ cbSoFar:** entero de 32 bits sin signo que contiene el número de bytes transferidos previamente para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3866">**\_cbSoFar**: A 32-bit unsigned integer containing the number of bytes previously transferred for this property.</span></span> <span data-ttu-id="d07fb-3867">DEBE establecerse en 0x00000000 en el primer mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3867">MUST be set to 0x00000000 in the first message.</span></span>

<span data-ttu-id="d07fb-3868">**\_ cbPropSpec:** entero de 32 bits sin signo que contiene el tamaño del campo PropSpec, en bytes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3868">**\_cbPropSpec**: A 32-bit unsigned integer containing the size of the PropSpec field, in bytes.</span></span>

<span data-ttu-id="d07fb-3869">**\_ cbChunk:** entero de 32 bits sin signo que contiene el número máximo de bytes que el remitente puede aceptar en un mensaje CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3869">**\_cbChunk**: A 32-bit unsigned integer containing the maximum number of bytes that the sender can accept in a CPMFetchValueOut message.</span></span>

<span data-ttu-id="d07fb-3870">*Comportamiento de Windows: este campo se establece en 0x00004000 para todas las versiones de Windows.*</span><span class="sxs-lookup"><span data-stu-id="d07fb-3870">*Windows Behavior: This field is set to 0x00004000 for all versions of Windows.*</span></span>

<span data-ttu-id="d07fb-3871">**PropSpec:** estructura CFullPropSpec que especifica la propiedad que se recuperará.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3871">**PropSpec**: A CFullPropSpec structure specifying the property to retrieve.</span></span>

<span data-ttu-id="d07fb-3872">**\_ padding:** este campo DEBE tener la longitud necesaria (de 0 a 3 bytes) para rellenar el mensaje hasta un múltiplo de 4 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3872">**\_padding**: This field MUST be of the length necessary (0 to 3 bytes) to pad the message out to a multiple of 4 bytes in length.</span></span> <span data-ttu-id="d07fb-3873">El valor de los bytes de relleno puede ser cualquier valor arbitrario.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3873">The value of the padding bytes can be any arbitrary value.</span></span> <span data-ttu-id="d07fb-3874">El receptor DEBE omitir este campo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3874">This field MUST be ignored by the receiver.</span></span>

### <a name="22320-cpmfetchvalueout"></a><span data-ttu-id="d07fb-3875">2.2.3.20 CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-3875">2.2.3.20 CPMFetchValueOut</span></span>

<span data-ttu-id="d07fb-3876">El mensaje CPMFetchValueOut responde a un mensaje CPMFetchValueIn con un valor de propiedad de una consulta anterior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3876">The CPMFetchValueOut message replies to a CPMFetchValueIn message with a property value from a previous query.</span></span> <span data-ttu-id="d07fb-3877">Como se especifica en la sección 3.1.5.2.8, este mensaje se envía después de cada mensaje CPMFetchValueIn hasta que se transfieren todos los bytes de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3877">As specified in section 3.1.5.2.8, this message is sent after each CPMFetchValueIn message until all bytes of the property are transferred.</span></span>

<span data-ttu-id="d07fb-3878">El formato del mensaje CPMFetchValueOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3878">The format of the CPMFetchValueOut message that follows the header is:</span></span>



<span data-ttu-id="d07fb-3879">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3879">0</span></span>

<span data-ttu-id="d07fb-3880">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3880">1</span></span>

<span data-ttu-id="d07fb-3881">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3881">2</span></span>

<span data-ttu-id="d07fb-3882">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3882">3</span></span>

<span data-ttu-id="d07fb-3883">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3883">4</span></span>

<span data-ttu-id="d07fb-3884">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3884">5</span></span>

<span data-ttu-id="d07fb-3885">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3885">6</span></span>

<span data-ttu-id="d07fb-3886">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3886">7</span></span>

<span data-ttu-id="d07fb-3887">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3887">8</span></span>

<span data-ttu-id="d07fb-3888">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3888">9</span></span>

<span data-ttu-id="d07fb-3889">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3889">1</span></span><br/> <span data-ttu-id="d07fb-3890">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3890">0</span></span><br/>

<span data-ttu-id="d07fb-3891">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3891">1</span></span>

<span data-ttu-id="d07fb-3892">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3892">2</span></span>

<span data-ttu-id="d07fb-3893">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3893">3</span></span>

<span data-ttu-id="d07fb-3894">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3894">4</span></span>

<span data-ttu-id="d07fb-3895">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3895">5</span></span>

<span data-ttu-id="d07fb-3896">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3896">6</span></span>

<span data-ttu-id="d07fb-3897">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3897">7</span></span>

<span data-ttu-id="d07fb-3898">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3898">8</span></span>

<span data-ttu-id="d07fb-3899">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3899">9</span></span>

<span data-ttu-id="d07fb-3900">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3900">2</span></span><br/> <span data-ttu-id="d07fb-3901">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3901">0</span></span><br/>

<span data-ttu-id="d07fb-3902">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3902">1</span></span>

<span data-ttu-id="d07fb-3903">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3903">2</span></span>

<span data-ttu-id="d07fb-3904">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3904">3</span></span>

<span data-ttu-id="d07fb-3905">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3905">4</span></span>

<span data-ttu-id="d07fb-3906">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3906">5</span></span>

<span data-ttu-id="d07fb-3907">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3907">6</span></span>

<span data-ttu-id="d07fb-3908">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3908">7</span></span>

<span data-ttu-id="d07fb-3909">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3909">8</span></span>

<span data-ttu-id="d07fb-3910">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3910">9</span></span>

<span data-ttu-id="d07fb-3911">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3911">3</span></span><br/> <span data-ttu-id="d07fb-3912">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3912">0</span></span><br/>

<span data-ttu-id="d07fb-3913">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3913">1</span></span>

<span data-ttu-id="d07fb-3914">\_cbValue</span><span class="sxs-lookup"><span data-stu-id="d07fb-3914">\_cbValue</span></span>

<span data-ttu-id="d07fb-3915">\_fMoreExists</span><span class="sxs-lookup"><span data-stu-id="d07fb-3915">\_fMoreExists</span></span>

<span data-ttu-id="d07fb-3916">\_fValueExists</span><span class="sxs-lookup"><span data-stu-id="d07fb-3916">\_fValueExists</span></span>

<span data-ttu-id="d07fb-3917">vType</span><span class="sxs-lookup"><span data-stu-id="d07fb-3917">vType</span></span>

<span data-ttu-id="d07fb-3918">vValue (variable)</span><span class="sxs-lookup"><span data-stu-id="d07fb-3918">vValue (variable)</span></span>



 

<span data-ttu-id="d07fb-3919">**\_ cbValue:** entero de 32 bits sin signo que contiene el tamaño total, en bytes en vValue.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3919">**\_cbValue**: A 32-bit unsigned integer containing the total size, in bytes in vValue.</span></span>

<span data-ttu-id="d07fb-3920">**\_ fMoreExists:** valor booleano que indica si hay mensajes CPMFetchValueOut adicionales disponibles.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3920">**\_fMoreExists**: A boolean value indicating whether there are additional CPMFetchValueOut messages available.</span></span> <span data-ttu-id="d07fb-3921">Si se establece en 0x00000001, hay mensajes CPMFetchValueOut adicionales.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3921">If set to 0x00000001, then there are additional CPMFetchValueOut messages.</span></span> <span data-ttu-id="d07fb-3922">Si se establece en 0x00000000, no hay mensajes CPMFetchValueOut adicionales disponibles.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3922">If set to 0x00000000, then there are no additional CPMFetchValueOut messages available.</span></span>

<span data-ttu-id="d07fb-3923">**\_ fValueExists:** valor booleano que indica si hay un valor para la propiedad .</span><span class="sxs-lookup"><span data-stu-id="d07fb-3923">**\_fValueExists**: A boolean value indicating whether there is a value for the property.</span></span> <span data-ttu-id="d07fb-3924">Si se establece en 0x00000001, existe un valor para la propiedad .</span><span class="sxs-lookup"><span data-stu-id="d07fb-3924">If set to 0x00000001, a value for the property exists.</span></span> <span data-ttu-id="d07fb-3925">Si se establece en 0x00000000, no existe un valor para la propiedad .</span><span class="sxs-lookup"><span data-stu-id="d07fb-3925">If set to 0x00000000, a value for the property does not exist.</span></span>

<span data-ttu-id="d07fb-3926">**vType:** un valor de la enumeración VARENUM, consulte la sección 2.2.1.1 para obtener más información y describir el tipo de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3926">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span></span>

<span data-ttu-id="d07fb-3927">**vValue:** una parte de una matriz de bytes que contiene una estructura SERIALIZEDPROPERTYVALUE como se especifica en la sección 2.2.1.32, donde el desplazamiento del principio de la parte es el valor \_ de cbSoFar en CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3927">**vValue**: A portion of a byte array containing a SERIALIZEDPROPERTYVALUE structure as specified in section 2.2.1.32, where the offset of the beginning of the portion is the value of\_cbSoFar in CPMFetchValueIn.</span></span> <span data-ttu-id="d07fb-3928">La longitud de la parte, indicada por el campo cbValue, DEBE ser igual al valor de \_ \_ cbChunk en CPMFetchValueIn si \_ fMoreExists se establece en 0x00000001 y DEBE ser menor o igual que el valor de cbChunk en caso \_ contrario.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3928">The length of the portion, indicated by the \_cbValue field, MUST be equal to the value of \_cbChunk in CPMFetchValueIn if \_fMoreExists is set to 0x00000001, and MUST be less than or equal to the value of \_cbChunk otherwise.</span></span>

### <a name="22321-cpmgetnotify"></a><span data-ttu-id="d07fb-3929">2.2.3.21 CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="d07fb-3929">2.2.3.21 CPMGetNotify</span></span>

<span data-ttu-id="d07fb-3930">El mensaje CPMGetNotify solicita que el cliente quiera recibir una notificación de los cambios en el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3930">The CPMGetNotify message requests that the client wants to be notified of rowset changes.</span></span>

<span data-ttu-id="d07fb-3931">El mensaje NO DEBE incluir un cuerpo; solo se enviará el encabezado del mensaje, tal como se especifica en la sección 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3931">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2, is to be sent.</span></span>

### <a name="22322-cpmsendnotifyout"></a><span data-ttu-id="d07fb-3932">2.2.3.22 CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-3932">2.2.3.22 CPMSendNotifyOut</span></span>

<span data-ttu-id="d07fb-3933">El mensaje CPMSendNotifyOut notifica al cliente un cambio en los resultados de una consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3933">The CPMSendNotifyOut message notifies the client of a change to the results of a query.</span></span>

<span data-ttu-id="d07fb-3934">Este mensaje solo se envía cuando se produce un cambio.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3934">This message is only sent when a change occurs.</span></span> <span data-ttu-id="d07fb-3935">El formato del mensaje CPMSendNotifyOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3935">The format of the CPMSendNotifyOut message that follows the header is:</span></span>



<span data-ttu-id="d07fb-3936">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3936">0</span></span>

<span data-ttu-id="d07fb-3937">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3937">1</span></span>

<span data-ttu-id="d07fb-3938">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3938">2</span></span>

<span data-ttu-id="d07fb-3939">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3939">3</span></span>

<span data-ttu-id="d07fb-3940">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3940">4</span></span>

<span data-ttu-id="d07fb-3941">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3941">5</span></span>

<span data-ttu-id="d07fb-3942">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3942">6</span></span>

<span data-ttu-id="d07fb-3943">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3943">7</span></span>

<span data-ttu-id="d07fb-3944">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3944">8</span></span>

<span data-ttu-id="d07fb-3945">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3945">9</span></span>

<span data-ttu-id="d07fb-3946">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3946">1</span></span><br/> <span data-ttu-id="d07fb-3947">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3947">0</span></span><br/>

<span data-ttu-id="d07fb-3948">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3948">1</span></span>

<span data-ttu-id="d07fb-3949">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3949">2</span></span>

<span data-ttu-id="d07fb-3950">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3950">3</span></span>

<span data-ttu-id="d07fb-3951">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3951">4</span></span>

<span data-ttu-id="d07fb-3952">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3952">5</span></span>

<span data-ttu-id="d07fb-3953">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3953">6</span></span>

<span data-ttu-id="d07fb-3954">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3954">7</span></span>

<span data-ttu-id="d07fb-3955">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3955">8</span></span>

<span data-ttu-id="d07fb-3956">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3956">9</span></span>

<span data-ttu-id="d07fb-3957">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3957">2</span></span><br/> <span data-ttu-id="d07fb-3958">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3958">0</span></span><br/>

<span data-ttu-id="d07fb-3959">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3959">1</span></span>

<span data-ttu-id="d07fb-3960">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3960">2</span></span>

<span data-ttu-id="d07fb-3961">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3961">3</span></span>

<span data-ttu-id="d07fb-3962">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3962">4</span></span>

<span data-ttu-id="d07fb-3963">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3963">5</span></span>

<span data-ttu-id="d07fb-3964">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3964">6</span></span>

<span data-ttu-id="d07fb-3965">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3965">7</span></span>

<span data-ttu-id="d07fb-3966">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3966">8</span></span>

<span data-ttu-id="d07fb-3967">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3967">9</span></span>

<span data-ttu-id="d07fb-3968">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3968">3</span></span><br/> <span data-ttu-id="d07fb-3969">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3969">0</span></span><br/>

<span data-ttu-id="d07fb-3970">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3970">1</span></span>

<span data-ttu-id="d07fb-3971">\_watchNotify</span><span class="sxs-lookup"><span data-stu-id="d07fb-3971">\_watchNotify</span></span>



 

<span data-ttu-id="d07fb-3972">**\_ watchNotify:** el cambio en la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3972">**\_watchNotify**: The change to the query.</span></span> <span data-ttu-id="d07fb-3973">DEBE ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3973">It MUST be one of the following values:</span></span>



| <span data-ttu-id="d07fb-3974">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-3974">Value</span></span>                                     | <span data-ttu-id="d07fb-3975">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-3975">Meaning</span></span>                                             |
|-------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="d07fb-3976">DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-3976">DBWATCHNOTIFY\_ROWSCHANGED 0x00000001</span></span>     | <span data-ttu-id="d07fb-3977">El número de filas del conjunto de filas de consulta ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3977">The number of rows in the query rowset has changed.</span></span> |
| <span data-ttu-id="d07fb-3978">DBWATCHNOTIFY \_ QUERYDONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-3978">DBWATCHNOTIFY\_QUERYDONE 0x00000002</span></span>       | <span data-ttu-id="d07fb-3979">La consulta se ha completado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3979">The query has completed.</span></span>                            |
| <span data-ttu-id="d07fb-3980">DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003</span><span class="sxs-lookup"><span data-stu-id="d07fb-3980">DBWATCHNOTIFY\_QUERYREEXECUTED 0x00000003</span></span> | <span data-ttu-id="d07fb-3981">La consulta se ha re-ejecutado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3981">The query has been re-executed.</span></span>                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a><span data-ttu-id="d07fb-3982">2.2.3.23 CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-3982">2.2.3.23 CPMGetApproximatePositionIn</span></span>

<span data-ttu-id="d07fb-3983">El mensaje CPMGetApproximatePositionIn solicita la posición aproximada de un marcador en un capítulo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-3983">The CPMGetApproximatePositionIn message requests the approximate position of a bookmark in a chapter.</span></span> <span data-ttu-id="d07fb-3984">El formato del mensaje CPMGetApproximatePositionIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-3984">The format of the CPMGetApproximatePositionIn message that follows the header is:</span></span>



<span data-ttu-id="d07fb-3985">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3985">0</span></span>

<span data-ttu-id="d07fb-3986">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3986">1</span></span>

<span data-ttu-id="d07fb-3987">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3987">2</span></span>

<span data-ttu-id="d07fb-3988">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3988">3</span></span>

<span data-ttu-id="d07fb-3989">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-3989">4</span></span>

<span data-ttu-id="d07fb-3990">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-3990">5</span></span>

<span data-ttu-id="d07fb-3991">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-3991">6</span></span>

<span data-ttu-id="d07fb-3992">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-3992">7</span></span>

<span data-ttu-id="d07fb-3993">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-3993">8</span></span>

<span data-ttu-id="d07fb-3994">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-3994">9</span></span>

<span data-ttu-id="d07fb-3995">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3995">1</span></span><br/> <span data-ttu-id="d07fb-3996">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-3996">0</span></span><br/>

<span data-ttu-id="d07fb-3997">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-3997">1</span></span>

<span data-ttu-id="d07fb-3998">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-3998">2</span></span>

<span data-ttu-id="d07fb-3999">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-3999">3</span></span>

<span data-ttu-id="d07fb-4000">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4000">4</span></span>

<span data-ttu-id="d07fb-4001">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4001">5</span></span>

<span data-ttu-id="d07fb-4002">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4002">6</span></span>

<span data-ttu-id="d07fb-4003">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4003">7</span></span>

<span data-ttu-id="d07fb-4004">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4004">8</span></span>

<span data-ttu-id="d07fb-4005">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4005">9</span></span>

<span data-ttu-id="d07fb-4006">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4006">2</span></span><br/> <span data-ttu-id="d07fb-4007">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4007">0</span></span><br/>

<span data-ttu-id="d07fb-4008">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4008">1</span></span>

<span data-ttu-id="d07fb-4009">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4009">2</span></span>

<span data-ttu-id="d07fb-4010">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4010">3</span></span>

<span data-ttu-id="d07fb-4011">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4011">4</span></span>

<span data-ttu-id="d07fb-4012">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4012">5</span></span>

<span data-ttu-id="d07fb-4013">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4013">6</span></span>

<span data-ttu-id="d07fb-4014">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4014">7</span></span>

<span data-ttu-id="d07fb-4015">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4015">8</span></span>

<span data-ttu-id="d07fb-4016">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4016">9</span></span>

<span data-ttu-id="d07fb-4017">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4017">3</span></span><br/> <span data-ttu-id="d07fb-4018">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4018">0</span></span><br/>

<span data-ttu-id="d07fb-4019">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4019">1</span></span>

<span data-ttu-id="d07fb-4020">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="d07fb-4020">\_hCursor</span></span>

<span data-ttu-id="d07fb-4021">\_chapt</span><span class="sxs-lookup"><span data-stu-id="d07fb-4021">\_chapt</span></span>

<span data-ttu-id="d07fb-4022">\_Bmk</span><span class="sxs-lookup"><span data-stu-id="d07fb-4022">\_bmk</span></span>



 

<span data-ttu-id="d07fb-4023">**\_ hCursor:** valor de 32 bits que representa el cursor de consulta obtenido de CPMCreateQueryOut para el conjunto de filas que contiene el marcador.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4023">**\_hCursor**: A 32-bit value representing the query cursor obtained from CPMCreateQueryOut for the rowset containing the bookmark.</span></span>

<span data-ttu-id="d07fb-4024">**\_ chapt:** valor de 32 bits que representa el identificador del capítulo que contiene el marcador.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4024">**\_chapt**: A 32-bit value representing the handle to the chapter containing the bookmark.</span></span>

<span data-ttu-id="d07fb-4025">**\_ bmk:** valor de 32 bits que representa el identificador del marcador para el que se va a recuperar la posición aproximada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4025">**\_bmk**: A 32-bit value representing the handle to the bookmark for which to retrieve the approximate position.</span></span>

### <a name="22324-cpmgetapproximatepositionout"></a><span data-ttu-id="d07fb-4026">2.2.3.24 CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-4026">2.2.3.24 CPMGetApproximatePositionOut</span></span>

<span data-ttu-id="d07fb-4027">El mensaje CPMGetApproximatePositionOut responde a un mensaje CPMGetApproximatePositionIn que describe la posición aproximada del marcador en el capítulo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4027">The CPMGetApproximatePositionOut message replies to a CPMGetApproximatePositionIn message describing the approximate position of the bookmark in the chapter.</span></span> <span data-ttu-id="d07fb-4028">El formato del mensaje CPMGetApproximatePositionOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4028">The format of the CPMGetApproximatePositionOut message that follows the header is:</span></span>



<span data-ttu-id="d07fb-4029">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4029">0</span></span>

<span data-ttu-id="d07fb-4030">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4030">1</span></span>

<span data-ttu-id="d07fb-4031">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4031">2</span></span>

<span data-ttu-id="d07fb-4032">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4032">3</span></span>

<span data-ttu-id="d07fb-4033">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4033">4</span></span>

<span data-ttu-id="d07fb-4034">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4034">5</span></span>

<span data-ttu-id="d07fb-4035">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4035">6</span></span>

<span data-ttu-id="d07fb-4036">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4036">7</span></span>

<span data-ttu-id="d07fb-4037">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4037">8</span></span>

<span data-ttu-id="d07fb-4038">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4038">9</span></span>

<span data-ttu-id="d07fb-4039">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4039">1</span></span><br/> <span data-ttu-id="d07fb-4040">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4040">0</span></span><br/>

<span data-ttu-id="d07fb-4041">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4041">1</span></span>

<span data-ttu-id="d07fb-4042">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4042">2</span></span>

<span data-ttu-id="d07fb-4043">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4043">3</span></span>

<span data-ttu-id="d07fb-4044">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4044">4</span></span>

<span data-ttu-id="d07fb-4045">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4045">5</span></span>

<span data-ttu-id="d07fb-4046">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4046">6</span></span>

<span data-ttu-id="d07fb-4047">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4047">7</span></span>

<span data-ttu-id="d07fb-4048">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4048">8</span></span>

<span data-ttu-id="d07fb-4049">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4049">9</span></span>

<span data-ttu-id="d07fb-4050">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4050">2</span></span><br/> <span data-ttu-id="d07fb-4051">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4051">0</span></span><br/>

<span data-ttu-id="d07fb-4052">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4052">1</span></span>

<span data-ttu-id="d07fb-4053">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4053">2</span></span>

<span data-ttu-id="d07fb-4054">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4054">3</span></span>

<span data-ttu-id="d07fb-4055">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4055">4</span></span>

<span data-ttu-id="d07fb-4056">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4056">5</span></span>

<span data-ttu-id="d07fb-4057">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4057">6</span></span>

<span data-ttu-id="d07fb-4058">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4058">7</span></span>

<span data-ttu-id="d07fb-4059">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4059">8</span></span>

<span data-ttu-id="d07fb-4060">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4060">9</span></span>

<span data-ttu-id="d07fb-4061">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4061">3</span></span><br/> <span data-ttu-id="d07fb-4062">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4062">0</span></span><br/>

<span data-ttu-id="d07fb-4063">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4063">1</span></span>

<span data-ttu-id="d07fb-4064">\_numerator</span><span class="sxs-lookup"><span data-stu-id="d07fb-4064">\_numerator</span></span>

<span data-ttu-id="d07fb-4065">\_denominator</span><span class="sxs-lookup"><span data-stu-id="d07fb-4065">\_denominator</span></span>



 

<span data-ttu-id="d07fb-4066">**\_ numerador:** entero de 32 bits sin signo que contiene el número de fila del marcador en el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4066">**\_numerator**: A 32-bit unsigned integer containing the row number of the bookmark in the rowset.</span></span> <span data-ttu-id="d07fb-4067">Si no hay filas, este campo DEBE establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4067">If there are no rows, this field MUST be set to 0x00000000.</span></span>

<span data-ttu-id="d07fb-4068">**\_ denominador:** entero de 32 bits sin signo que contiene el número de filas del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4068">**\_denominator**: A 32-bit unsigned integer containing the number of rows in the rowset.</span></span>

### <a name="22325-cpmcomparebmkin"></a><span data-ttu-id="d07fb-4069">2.2.3.25 CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4069">2.2.3.25 CPMCompareBmkIn</span></span>

<span data-ttu-id="d07fb-4070">El mensaje CPMCompareBmkIn solicita una comparación de dos marcadores en un capítulo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4070">The CPMCompareBmkIn message requests a comparison of two bookmarks in a chapter.</span></span>

<span data-ttu-id="d07fb-4071">El formato del mensaje CPMCompareBmkIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4071">The format of the CPMCompareBmkIn message that follows the header is:</span></span>



<span data-ttu-id="d07fb-4072">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4072">0</span></span>

<span data-ttu-id="d07fb-4073">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4073">1</span></span>

<span data-ttu-id="d07fb-4074">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4074">2</span></span>

<span data-ttu-id="d07fb-4075">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4075">3</span></span>

<span data-ttu-id="d07fb-4076">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4076">4</span></span>

<span data-ttu-id="d07fb-4077">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4077">5</span></span>

<span data-ttu-id="d07fb-4078">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4078">6</span></span>

<span data-ttu-id="d07fb-4079">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4079">7</span></span>

<span data-ttu-id="d07fb-4080">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4080">8</span></span>

<span data-ttu-id="d07fb-4081">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4081">9</span></span>

<span data-ttu-id="d07fb-4082">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4082">1</span></span><br/> <span data-ttu-id="d07fb-4083">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4083">0</span></span><br/>

<span data-ttu-id="d07fb-4084">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4084">1</span></span>

<span data-ttu-id="d07fb-4085">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4085">2</span></span>

<span data-ttu-id="d07fb-4086">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4086">3</span></span>

<span data-ttu-id="d07fb-4087">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4087">4</span></span>

<span data-ttu-id="d07fb-4088">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4088">5</span></span>

<span data-ttu-id="d07fb-4089">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4089">6</span></span>

<span data-ttu-id="d07fb-4090">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4090">7</span></span>

<span data-ttu-id="d07fb-4091">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4091">8</span></span>

<span data-ttu-id="d07fb-4092">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4092">9</span></span>

<span data-ttu-id="d07fb-4093">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4093">2</span></span><br/> <span data-ttu-id="d07fb-4094">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4094">0</span></span><br/>

<span data-ttu-id="d07fb-4095">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4095">1</span></span>

<span data-ttu-id="d07fb-4096">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4096">2</span></span>

<span data-ttu-id="d07fb-4097">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4097">3</span></span>

<span data-ttu-id="d07fb-4098">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4098">4</span></span>

<span data-ttu-id="d07fb-4099">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4099">5</span></span>

<span data-ttu-id="d07fb-4100">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4100">6</span></span>

<span data-ttu-id="d07fb-4101">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4101">7</span></span>

<span data-ttu-id="d07fb-4102">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4102">8</span></span>

<span data-ttu-id="d07fb-4103">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4103">9</span></span>

<span data-ttu-id="d07fb-4104">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4104">3</span></span><br/> <span data-ttu-id="d07fb-4105">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4105">0</span></span><br/>

<span data-ttu-id="d07fb-4106">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4106">1</span></span>

<span data-ttu-id="d07fb-4107">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="d07fb-4107">\_hCursor</span></span>

<span data-ttu-id="d07fb-4108">\_chapt</span><span class="sxs-lookup"><span data-stu-id="d07fb-4108">\_chapt</span></span>

<span data-ttu-id="d07fb-4109">\_bmkFirst</span><span class="sxs-lookup"><span data-stu-id="d07fb-4109">\_bmkFirst</span></span>

<span data-ttu-id="d07fb-4110">\_bmkSecond</span><span class="sxs-lookup"><span data-stu-id="d07fb-4110">\_bmkSecond</span></span>



 

<span data-ttu-id="d07fb-4111">\_**hCursor:** valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut para el conjunto de filas que contiene los marcadores.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4111">\_**hCursor**: A 32-bit value representing the handle from CPMCreateQueryOut message for the rowset containing the bookmarks.</span></span>

<span data-ttu-id="d07fb-4112">\_**chapt:** valor de 32 bits que representa el identificador del capítulo que contiene los marcadores que se compararán.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4112">\_**chapt**: A 32-bit value representing the handle of the chapter containing the bookmarks to compare.</span></span>

<span data-ttu-id="d07fb-4113">\_**bmkFirst:** valor de 32 bits que representa el identificador del primer marcador que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4113">\_**bmkFirst**: A 32-bit value representing the handle to the first bookmark to compare.</span></span>

<span data-ttu-id="d07fb-4114">\_**bmkSecond:** valor de 32 bits que representa el identificador del segundo marcador que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4114">\_**bmkSecond**: A 32-bit value representing the handle to the second bookmark to compare.</span></span>

### <a name="22326-cpmcomparebmkout"></a><span data-ttu-id="d07fb-4115">2.2.3.26 CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-4115">2.2.3.26 CPMCompareBmkOut</span></span>

<span data-ttu-id="d07fb-4116">El mensaje CPMCompareBmkOut responde a un mensaje CPMCompareBmkIn con la comparación de los dos marcadores del capítulo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4116">The CPMCompareBmkOut message replies to a CPMCompareBmkIn message with the comparison of the two bookmarks in the chapter.</span></span> <span data-ttu-id="d07fb-4117">El formato del mensaje CPMCompareBmkOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4117">The format of the CPMCompareBmkOut message that follows the header is:</span></span>



<span data-ttu-id="d07fb-4118">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4118">0</span></span>

<span data-ttu-id="d07fb-4119">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4119">1</span></span>

<span data-ttu-id="d07fb-4120">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4120">2</span></span>

<span data-ttu-id="d07fb-4121">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4121">3</span></span>

<span data-ttu-id="d07fb-4122">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4122">4</span></span>

<span data-ttu-id="d07fb-4123">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4123">5</span></span>

<span data-ttu-id="d07fb-4124">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4124">6</span></span>

<span data-ttu-id="d07fb-4125">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4125">7</span></span>

<span data-ttu-id="d07fb-4126">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4126">8</span></span>

<span data-ttu-id="d07fb-4127">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4127">9</span></span>

<span data-ttu-id="d07fb-4128">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4128">1</span></span><br/> <span data-ttu-id="d07fb-4129">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4129">0</span></span><br/>

<span data-ttu-id="d07fb-4130">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4130">1</span></span>

<span data-ttu-id="d07fb-4131">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4131">2</span></span>

<span data-ttu-id="d07fb-4132">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4132">3</span></span>

<span data-ttu-id="d07fb-4133">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4133">4</span></span>

<span data-ttu-id="d07fb-4134">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4134">5</span></span>

<span data-ttu-id="d07fb-4135">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4135">6</span></span>

<span data-ttu-id="d07fb-4136">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4136">7</span></span>

<span data-ttu-id="d07fb-4137">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4137">8</span></span>

<span data-ttu-id="d07fb-4138">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4138">9</span></span>

<span data-ttu-id="d07fb-4139">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4139">2</span></span><br/> <span data-ttu-id="d07fb-4140">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4140">0</span></span><br/>

<span data-ttu-id="d07fb-4141">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4141">1</span></span>

<span data-ttu-id="d07fb-4142">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4142">2</span></span>

<span data-ttu-id="d07fb-4143">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4143">3</span></span>

<span data-ttu-id="d07fb-4144">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4144">4</span></span>

<span data-ttu-id="d07fb-4145">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4145">5</span></span>

<span data-ttu-id="d07fb-4146">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4146">6</span></span>

<span data-ttu-id="d07fb-4147">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4147">7</span></span>

<span data-ttu-id="d07fb-4148">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4148">8</span></span>

<span data-ttu-id="d07fb-4149">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4149">9</span></span>

<span data-ttu-id="d07fb-4150">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4150">3</span></span><br/> <span data-ttu-id="d07fb-4151">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4151">0</span></span><br/>

<span data-ttu-id="d07fb-4152">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4152">1</span></span>

<span data-ttu-id="d07fb-4153">\_dwComparison</span><span class="sxs-lookup"><span data-stu-id="d07fb-4153">\_dwComparison</span></span>



 

<span data-ttu-id="d07fb-4154">\_**dwComparison:** uno de los siguientes valores, que indican las posiciones relativas de los dos marcadores del capítulo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4154">\_**dwComparison**: One of the following values, indicating the relative positions of the two bookmarks in the chapter.</span></span>



| <span data-ttu-id="d07fb-4155">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-4155">Value</span></span>                               | <span data-ttu-id="d07fb-4156">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-4156">Meaning</span></span>                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="d07fb-4157">DBCOMPARE \_ LT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-4157">DBCOMPARE\_LT 0x00000000</span></span>            | <span data-ttu-id="d07fb-4158">El primer marcador se coloca delante del segundo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4158">The first bookmark is positioned before the second.</span></span>               |
| <span data-ttu-id="d07fb-4159">DBCOMPARE \_ EQ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="d07fb-4159">DBCOMPARE\_EQ 0x00000001</span></span>            | <span data-ttu-id="d07fb-4160">El primer marcador tiene la misma posición que el segundo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4160">The first bookmark has the same position as the second.</span></span>           |
| <span data-ttu-id="d07fb-4161">DBCOMPARE \_ GT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="d07fb-4161">DBCOMPARE\_GT 0x00000002</span></span>            | <span data-ttu-id="d07fb-4162">El primer marcador se coloca después del segundo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4162">The first bookmark is positioned after the second.</span></span>                |
| <span data-ttu-id="d07fb-4163">DBCOMPARE \_ NE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="d07fb-4163">DBCOMPARE\_NE 0x00000003</span></span>            | <span data-ttu-id="d07fb-4164">El primer marcador no tiene la misma posición que el segundo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4164">The first bookmark does not have the same position as the second.</span></span> |
| <span data-ttu-id="d07fb-4165">DBCOMPARE \_ NOTCOMPARABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="d07fb-4165">DBCOMPARE\_NOTCOMPARABLE 0x00000004</span></span> | <span data-ttu-id="d07fb-4166">El primer marcador no es comparable al segundo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4166">The first bookmark is not comparable to the second.</span></span>               |



 

### <a name="22327-cpmrestartpositionin"></a><span data-ttu-id="d07fb-4167">2.2.3.27 CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4167">2.2.3.27 CPMRestartPositionIn</span></span>

<span data-ttu-id="d07fb-4168">El mensaje CPMRestartPositionIn mueve la posición de captura de un cursor al principio del capítulo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4168">The CPMRestartPositionIn message moves the fetch position for a cursor to the beginning of the chapter.</span></span> <span data-ttu-id="d07fb-4169">Como se especifica en la sección 3.1.5.2.12, el servidor responderá con el mismo mensaje, con los resultados de la solicitud contenida en el campo de estado del \_ encabezado CISP.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4169">As specified in section 3.1.5.2.12, the server will reply using the same message, with the results of the request contained in the \_status field of the CISP header.</span></span>

<span data-ttu-id="d07fb-4170">El formato del mensaje CPMRestartPositionIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4170">The format of the CPMRestartPositionIn message that follows the header is:</span></span>



<span data-ttu-id="d07fb-4171">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4171">0</span></span>

<span data-ttu-id="d07fb-4172">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4172">1</span></span>

<span data-ttu-id="d07fb-4173">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4173">2</span></span>

<span data-ttu-id="d07fb-4174">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4174">3</span></span>

<span data-ttu-id="d07fb-4175">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4175">4</span></span>

<span data-ttu-id="d07fb-4176">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4176">5</span></span>

<span data-ttu-id="d07fb-4177">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4177">6</span></span>

<span data-ttu-id="d07fb-4178">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4178">7</span></span>

<span data-ttu-id="d07fb-4179">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4179">8</span></span>

<span data-ttu-id="d07fb-4180">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4180">9</span></span>

<span data-ttu-id="d07fb-4181">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4181">1</span></span><br/> <span data-ttu-id="d07fb-4182">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4182">0</span></span><br/>

<span data-ttu-id="d07fb-4183">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4183">1</span></span>

<span data-ttu-id="d07fb-4184">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4184">2</span></span>

<span data-ttu-id="d07fb-4185">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4185">3</span></span>

<span data-ttu-id="d07fb-4186">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4186">4</span></span>

<span data-ttu-id="d07fb-4187">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4187">5</span></span>

<span data-ttu-id="d07fb-4188">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4188">6</span></span>

<span data-ttu-id="d07fb-4189">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4189">7</span></span>

<span data-ttu-id="d07fb-4190">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4190">8</span></span>

<span data-ttu-id="d07fb-4191">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4191">9</span></span>

<span data-ttu-id="d07fb-4192">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4192">2</span></span><br/> <span data-ttu-id="d07fb-4193">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4193">0</span></span><br/>

<span data-ttu-id="d07fb-4194">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4194">1</span></span>

<span data-ttu-id="d07fb-4195">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4195">2</span></span>

<span data-ttu-id="d07fb-4196">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4196">3</span></span>

<span data-ttu-id="d07fb-4197">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4197">4</span></span>

<span data-ttu-id="d07fb-4198">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4198">5</span></span>

<span data-ttu-id="d07fb-4199">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4199">6</span></span>

<span data-ttu-id="d07fb-4200">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4200">7</span></span>

<span data-ttu-id="d07fb-4201">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4201">8</span></span>

<span data-ttu-id="d07fb-4202">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4202">9</span></span>

<span data-ttu-id="d07fb-4203">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4203">3</span></span><br/> <span data-ttu-id="d07fb-4204">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4204">0</span></span><br/>

<span data-ttu-id="d07fb-4205">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4205">1</span></span>

<span data-ttu-id="d07fb-4206">\_hCursor (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-4206">\_hCursor (optional)</span></span>

<span data-ttu-id="d07fb-4207">\_chapt (opcional)</span><span class="sxs-lookup"><span data-stu-id="d07fb-4207">\_chapt (optional)</span></span>



 

<span data-ttu-id="d07fb-4208">**\_ hCursor:** valor de 32 bits que representa el identificador, obtenido de un mensaje CPMCreateQueryOut, que identifica la consulta para la que se debe reiniciar la posición.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4208">**\_hCursor**: A 32-bit value representing the handle, obtained from a CPMCreateQueryOut message, which identifies the query for which to restart the position.</span></span> <span data-ttu-id="d07fb-4209">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4209">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="d07fb-4210">**\_ chapt:** valor de 32 bits que representa el identificador de un capítulo del que se recuperan filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4210">**\_chapt**: A 32-bit value representing the handle of a chapter from which to retrieve rows.</span></span> <span data-ttu-id="d07fb-4211">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4211">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

### <a name="22328-cpmfreecursorin"></a><span data-ttu-id="d07fb-4212">2.2.3.28 CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4212">2.2.3.28 CPMFreeCursorIn</span></span>

<span data-ttu-id="d07fb-4213">El mensaje CPMFreeCursorIn solicita la liberación de un cursor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4213">The CPMFreeCursorIn message requests the release of a cursor.</span></span> <span data-ttu-id="d07fb-4214">El formato del mensaje CPMFreeCursorIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4214">The format of the CPMFreeCursorIn message that follows the header is:</span></span>



<span data-ttu-id="d07fb-4215">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4215">0</span></span>

<span data-ttu-id="d07fb-4216">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4216">1</span></span>

<span data-ttu-id="d07fb-4217">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4217">2</span></span>

<span data-ttu-id="d07fb-4218">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4218">3</span></span>

<span data-ttu-id="d07fb-4219">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4219">4</span></span>

<span data-ttu-id="d07fb-4220">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4220">5</span></span>

<span data-ttu-id="d07fb-4221">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4221">6</span></span>

<span data-ttu-id="d07fb-4222">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4222">7</span></span>

<span data-ttu-id="d07fb-4223">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4223">8</span></span>

<span data-ttu-id="d07fb-4224">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4224">9</span></span>

<span data-ttu-id="d07fb-4225">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4225">1</span></span><br/> <span data-ttu-id="d07fb-4226">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4226">0</span></span><br/>

<span data-ttu-id="d07fb-4227">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4227">1</span></span>

<span data-ttu-id="d07fb-4228">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4228">2</span></span>

<span data-ttu-id="d07fb-4229">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4229">3</span></span>

<span data-ttu-id="d07fb-4230">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4230">4</span></span>

<span data-ttu-id="d07fb-4231">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4231">5</span></span>

<span data-ttu-id="d07fb-4232">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4232">6</span></span>

<span data-ttu-id="d07fb-4233">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4233">7</span></span>

<span data-ttu-id="d07fb-4234">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4234">8</span></span>

<span data-ttu-id="d07fb-4235">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4235">9</span></span>

<span data-ttu-id="d07fb-4236">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4236">2</span></span><br/> <span data-ttu-id="d07fb-4237">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4237">0</span></span><br/>

<span data-ttu-id="d07fb-4238">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4238">1</span></span>

<span data-ttu-id="d07fb-4239">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4239">2</span></span>

<span data-ttu-id="d07fb-4240">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4240">3</span></span>

<span data-ttu-id="d07fb-4241">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4241">4</span></span>

<span data-ttu-id="d07fb-4242">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4242">5</span></span>

<span data-ttu-id="d07fb-4243">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4243">6</span></span>

<span data-ttu-id="d07fb-4244">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4244">7</span></span>

<span data-ttu-id="d07fb-4245">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4245">8</span></span>

<span data-ttu-id="d07fb-4246">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4246">9</span></span>

<span data-ttu-id="d07fb-4247">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4247">3</span></span><br/> <span data-ttu-id="d07fb-4248">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4248">0</span></span><br/>

<span data-ttu-id="d07fb-4249">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4249">1</span></span>

<span data-ttu-id="d07fb-4250">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="d07fb-4250">\_hCursor</span></span>



 

<span data-ttu-id="d07fb-4251">**\_ hCursor:** valor de 32 bits que representa el identificador del cursor del mensaje CPMCreateQueryOut que se debe liberar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4251">**\_hCursor**: A 32-bit value representing the handle of the cursor from the CPMCreateQueryOut message to release.</span></span>

### <a name="22329-cpmfreecursorout"></a><span data-ttu-id="d07fb-4252">2.2.3.29 CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-4252">2.2.3.29 CPMFreeCursorOut</span></span>

<span data-ttu-id="d07fb-4253">El mensaje CPMFreeCursorOut responde a un mensaje CPMFreeCursorIn con los resultados de liberar un cursor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4253">The CPMFreeCursorOut message replies to a CPMFreeCursorIn message with the results of freeing a cursor.</span></span> <span data-ttu-id="d07fb-4254">El formato del mensaje CPMFreeCursorOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4254">The format of the CPMFreeCursorOut message that follows the header is:</span></span>



<span data-ttu-id="d07fb-4255">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4255">0</span></span>

<span data-ttu-id="d07fb-4256">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4256">1</span></span>

<span data-ttu-id="d07fb-4257">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4257">2</span></span>

<span data-ttu-id="d07fb-4258">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4258">3</span></span>

<span data-ttu-id="d07fb-4259">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4259">4</span></span>

<span data-ttu-id="d07fb-4260">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4260">5</span></span>

<span data-ttu-id="d07fb-4261">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4261">6</span></span>

<span data-ttu-id="d07fb-4262">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4262">7</span></span>

<span data-ttu-id="d07fb-4263">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4263">8</span></span>

<span data-ttu-id="d07fb-4264">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4264">9</span></span>

<span data-ttu-id="d07fb-4265">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4265">1</span></span><br/> <span data-ttu-id="d07fb-4266">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4266">0</span></span><br/>

<span data-ttu-id="d07fb-4267">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4267">1</span></span>

<span data-ttu-id="d07fb-4268">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4268">2</span></span>

<span data-ttu-id="d07fb-4269">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4269">3</span></span>

<span data-ttu-id="d07fb-4270">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4270">4</span></span>

<span data-ttu-id="d07fb-4271">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4271">5</span></span>

<span data-ttu-id="d07fb-4272">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4272">6</span></span>

<span data-ttu-id="d07fb-4273">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4273">7</span></span>

<span data-ttu-id="d07fb-4274">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4274">8</span></span>

<span data-ttu-id="d07fb-4275">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4275">9</span></span>

<span data-ttu-id="d07fb-4276">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4276">2</span></span><br/> <span data-ttu-id="d07fb-4277">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4277">0</span></span><br/>

<span data-ttu-id="d07fb-4278">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4278">1</span></span>

<span data-ttu-id="d07fb-4279">2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4279">2</span></span>

<span data-ttu-id="d07fb-4280">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4280">3</span></span>

<span data-ttu-id="d07fb-4281">4</span><span class="sxs-lookup"><span data-stu-id="d07fb-4281">4</span></span>

<span data-ttu-id="d07fb-4282">5</span><span class="sxs-lookup"><span data-stu-id="d07fb-4282">5</span></span>

<span data-ttu-id="d07fb-4283">6</span><span class="sxs-lookup"><span data-stu-id="d07fb-4283">6</span></span>

<span data-ttu-id="d07fb-4284">7</span><span class="sxs-lookup"><span data-stu-id="d07fb-4284">7</span></span>

<span data-ttu-id="d07fb-4285">8</span><span class="sxs-lookup"><span data-stu-id="d07fb-4285">8</span></span>

<span data-ttu-id="d07fb-4286">9</span><span class="sxs-lookup"><span data-stu-id="d07fb-4286">9</span></span>

<span data-ttu-id="d07fb-4287">3</span><span class="sxs-lookup"><span data-stu-id="d07fb-4287">3</span></span><br/> <span data-ttu-id="d07fb-4288">0</span><span class="sxs-lookup"><span data-stu-id="d07fb-4288">0</span></span><br/>

<span data-ttu-id="d07fb-4289">1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4289">1</span></span>

<span data-ttu-id="d07fb-4290">\_cCursorsRemaining</span><span class="sxs-lookup"><span data-stu-id="d07fb-4290">\_cCursorsRemaining</span></span>



 

<span data-ttu-id="d07fb-4291">**\_ cCursorsRemaining:** entero de 32 bits sin signo que indica el número de cursores que siguen en uso para la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4291">**\_cCursorsRemaining**: A 32-bit unsigned integer indicating the number of cursors still in use for the query.</span></span>

### <a name="22330-cpmdisconnect"></a><span data-ttu-id="d07fb-4292">2.2.3.30 CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="d07fb-4292">2.2.3.30 CPMDisconnect</span></span>

<span data-ttu-id="d07fb-4293">El mensaje CPMDisconnect finaliza la conexión con el servidor</span><span class="sxs-lookup"><span data-stu-id="d07fb-4293">The CPMDisconnect message ends the connection with the server</span></span>

<span data-ttu-id="d07fb-4294">El mensaje NO DEBE incluir un cuerpo; solo se enviará el encabezado del mensaje, tal como se especifica en la sección 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4294">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2 is to be sent.</span></span>

### <a name="224-errors"></a><span data-ttu-id="d07fb-4295">2.2.4 Errores</span><span class="sxs-lookup"><span data-stu-id="d07fb-4295">2.2.4 Errors</span></span>

<span data-ttu-id="d07fb-4296">Todos los mensajes de Content Indexing Service Protocol DEBEN devolver 0x00000000 correcto; De lo contrario, devuelven un código de error distinto de cero de 32 bits que puede ser un valor HRESULT o NTSTATUS (consulte la sección 1.8).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4296">All Content Indexing Service Protocol messages MUST return 0x00000000 on success; otherwise, they return a 32-bit nonzero error code which can be either an HRESULT or an NTSTATUS value (see section 1.8).</span></span> <span data-ttu-id="d07fb-4297">Si un búfer es demasiado pequeño para ajustarse a un resultado, se debe devolver un código de estado de STATUS \_ INSUFFICIENT RESOURCES (0xC0000009A) y la operación con errores debe reinterse con un búfer \_ mayor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4297">If a buffer is too small to fit a result, a status code of STATUS\_INSUFFICIENT\_RESOURCES (0xC0000009A) MUST be returned and the failing operation should be retried with a larger buffer.</span></span>

<span data-ttu-id="d07fb-4298">Todos los demás valores de error DEBEN tratarse igual.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4298">All other error values MUST be treated the same.</span></span>

<span data-ttu-id="d07fb-4299">(Tenga en cuenta que actualmente los espacios de numeración HRESULT y NTSTATUS no se superponen excepto con valores de significado idéntico, pero incluso si estuvieran en conflicto en el futuro, no produciría ningún problema de protocolo siempre que el valor de STATUS \_ INSUFFICIENT \_ RESOURCES sigue siendo único, ya que todos los demás valores de error se tratan igual).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4299">(Note that currently the HRESULT and NTSTATUS numbering spaces do not overlap except with values of identical meaning, but even if they were to be conflicts in the future, it would not cause any protocol issues as long as the value for STATUS\_INSUFFICIENT\_RESOURCES remains unique, since all other error values are treated the same.)</span></span>

## <a name="3-protocol-details"></a><span data-ttu-id="d07fb-4300">3 Detalles del protocolo</span><span class="sxs-lookup"><span data-stu-id="d07fb-4300">3 Protocol Details</span></span>

-   [<span data-ttu-id="d07fb-4301">3.1 Detalles del servidor</span><span class="sxs-lookup"><span data-stu-id="d07fb-4301">3.1 Server Details</span></span>](#31-server-details)
-   [<span data-ttu-id="d07fb-4302">3.2 Detalles del cliente</span><span class="sxs-lookup"><span data-stu-id="d07fb-4302">3.2 Client Details</span></span>](#32-client-details)

<span data-ttu-id="d07fb-4303">Las solicitudes de mensajes CISP para consultar de forma remota los catálogos del servicio de indexación no requieren ninguna secuencia determinada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4303">CISP message requests for remotely querying the indexing service catalogs do not require any particular sequence.</span></span> <span data-ttu-id="d07fb-4304">Sin embargo, se recomienda que la capa superior se ajuste a una secuencia de mensajes significativa, como en el caso de los mensajes que se reciben fuera de esta secuencia o con datos no válidos, el servidor responderá con un error.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4304">It is advised that the higher layer adhere to a meaningful message sequence though, as for messages that are received out of this sequence or with invalid data, the server will respond with an error.</span></span> <span data-ttu-id="d07fb-4305">Algunos mensajes también dependen de la capa superior que proporciona datos válidos que se recibieron en los mensajes anteriores de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4305">Some messages are also dependent on the higher layer providing valid data that was received in messages earlier in the sequence.</span></span>

<span data-ttu-id="d07fb-4306">En el diagrama siguiente se muestra una secuencia de mensajes típica para una consulta simple desde un cliente a un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4306">A typical message sequence for a simple query from a client to a remote computer is illustrated in the following diagram.</span></span>

![secuencia de mensajes para una consulta simple](images/protocoldetails.jpg)

<span data-ttu-id="d07fb-4308">Los mensajes representados en el diagrama anterior representan un subconjunto de todos los mensajes CISP usados para consultar un catálogo de servicios de indexación remoto.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4308">The messages represented in the preceding diagram represent a subset of all of the CISP messages used for querying a remote indexing service catalog.</span></span>

### <a name="31-server-details"></a><span data-ttu-id="d07fb-4309">3.1 Detalles del servidor</span><span class="sxs-lookup"><span data-stu-id="d07fb-4309">3.1 Server Details</span></span>

### <a name="311-abstract-data-model"></a><span data-ttu-id="d07fb-4310">3.1.1 Modelo de datos abstracto</span><span class="sxs-lookup"><span data-stu-id="d07fb-4310">3.1.1 Abstract Data Model</span></span>

<span data-ttu-id="d07fb-4311">En la sección siguiente se especifican los datos y el estado que mantiene el servidor CISP.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4311">The following section specifies data and state maintained by the CISP server.</span></span> <span data-ttu-id="d07fb-4312">Los datos que se proporcionan aquí son para facilitar la explicación de cómo se comporta el protocolo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4312">The data provided here is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="d07fb-4313">Esta sección no exige que las implementaciones cumplan este modelo siempre y cuando su comportamiento externo sea coherente con el descrito en este documento.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4313">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="d07fb-4314">Un servicio de indexación que implementa CISP DEBE mantener los siguientes elementos de datos abstractos:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4314">An indexing service implementing the CISP MUST maintain the following abstract data elements:</span></span>

-   <span data-ttu-id="d07fb-4315">Lista de clientes conectados al servidor</span><span class="sxs-lookup"><span data-stu-id="d07fb-4315">The list of clients connected to the server</span></span>
-   <span data-ttu-id="d07fb-4316">Información sobre cada cliente, que incluye:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4316">Information about each client, which includes:</span></span>
-   -   <span data-ttu-id="d07fb-4317">Versión del cliente (como se indica en el mensaje CPMConnectIn especificado en la sección 2.2.3.6)</span><span class="sxs-lookup"><span data-stu-id="d07fb-4317">Client's version (as indicated in the CPMConnectIn message specified in section 2.2.3.6)</span></span>
    -   <span data-ttu-id="d07fb-4318">Catálogo asociado al cliente (por un mensaje CPMConnectIn)</span><span class="sxs-lookup"><span data-stu-id="d07fb-4318">Catalog associated with the client (by a CPMConnectIn message)</span></span>
    -   <span data-ttu-id="d07fb-4319">Propiedades de cliente adicionales, como se especifica en la sección 2.2.1.21.1.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4319">Additional client properties as specified in section 2.2.1.21.1.</span></span>
    -   <span data-ttu-id="d07fb-4320">Consulta de búsqueda del cliente</span><span class="sxs-lookup"><span data-stu-id="d07fb-4320">Client's search query</span></span>
    -   <span data-ttu-id="d07fb-4321">Lista de identificadores de cursor para la consulta y la posición en el conjunto de resultados para cada identificador.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4321">List of cursor handles for the query and position in result set for each handle.</span></span>
    -   <span data-ttu-id="d07fb-4322">Conjunto actual de enlaces</span><span class="sxs-lookup"><span data-stu-id="d07fb-4322">Current set of bindings</span></span>
    -   <span data-ttu-id="d07fb-4323">Estado actual de la consulta que incluye (para cada cursor):</span><span class="sxs-lookup"><span data-stu-id="d07fb-4323">Current status of the query which includes (for each cursor):</span></span>
    -   -   <span data-ttu-id="d07fb-4324">Número de filas en el resultado de la consulta</span><span class="sxs-lookup"><span data-stu-id="d07fb-4324">Number of rows in query result</span></span>
        -   <span data-ttu-id="d07fb-4325">Numerador y denominador de finalización de consultas</span><span class="sxs-lookup"><span data-stu-id="d07fb-4325">Numerator and denominator of query completion</span></span>
        -   <span data-ttu-id="d07fb-4326">Último número de filas, notificado por el mensaje CPMRatioFinishedOut más reciente para este cursor</span><span class="sxs-lookup"><span data-stu-id="d07fb-4326">Last number of rows, reported by most recent CPMRatioFinishedOut message for this cursor</span></span>
        -   <span data-ttu-id="d07fb-4327">Si el servidor supervisa la consulta en busca de cambios en los resultados de la consulta y si se supervisa, qué ha cambiado en los resultados de la consulta desde que CPMSendNotifyOut la informó por última vez al cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4327">Whether the query is monitored by the server for changes in query results and if it is monitored, what changed in the query results since it was last reported to client by CPMSendNotifyOut</span></span>
        -   <span data-ttu-id="d07fb-4328">Lista de identificadores de capítulos que sirve esta consulta a un cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4328">List of chapters handles, served by this query to a client.</span></span>
        -   <span data-ttu-id="d07fb-4329">Lista de identificadores de marcador para cada cursor, que sirve esta consulta a un cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4329">List of bookmark handles for each cursor, served by this query to a client.</span></span>

-   <span data-ttu-id="d07fb-4330">Estado actual del servicio de indexación, que puede ser "no inicializado", "en ejecución" o "apagado".</span><span class="sxs-lookup"><span data-stu-id="d07fb-4330">The current state of the indexing service, which may be "not initialized", "running", or "shutting down".</span></span> <span data-ttu-id="d07fb-4331">Tenga en cuenta que la mayoría de las veces el servidor está en estado "en ejecución".</span><span class="sxs-lookup"><span data-stu-id="d07fb-4331">Note that most of the time server is in "running" state.</span></span> <span data-ttu-id="d07fb-4332">A continuación se muestra el diagrama de la máquina de estado para el servidor:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4332">Following is the state machine diagram for the server:</span></span>

    ![diagrama de máquina de estado del servidor de servicio de indexación](images/abstractdatamodel.jpg)

-   <span data-ttu-id="d07fb-4334">Información por catálogo: número de documentos indexados, tamaño del índice, número de claves únicas, etc. (consulte la sección 2.2.3.1 para obtener una lista completa), estado (que corresponde a los valores de dwNewState de la sección 2.2.3.2).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4334">Per-catalog information: number of documents indexed, size of index, number of unique keys, etc (see section 2.2.3.1 for complete list), state (which corresponds to the values of dwNewState in section 2.2.3.2).</span></span>
-   <span data-ttu-id="d07fb-4335">Para cada idioma admitido, una base de datos de variaciones de palabras como se describe en la sección 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4335">For each language supported, a database of word variations as discussed in section 2.2.1.3.</span></span>

### <a name="312-timers"></a><span data-ttu-id="d07fb-4336">3.1.2 Temporizadores</span><span class="sxs-lookup"><span data-stu-id="d07fb-4336">3.1.2 Timers</span></span>

<span data-ttu-id="d07fb-4337">No se requiere ningún temporizador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4337">No protocol timers are required.</span></span>

### <a name="313-initialization"></a><span data-ttu-id="d07fb-4338">3.1.3 Inicialización</span><span class="sxs-lookup"><span data-stu-id="d07fb-4338">3.1.3 Initialization</span></span>

<span data-ttu-id="d07fb-4339">Tras la inicialización, el servidor DEBE establecer su estado en "no inicializado" y empezar a escuchar mensajes en la canalización con nombre especificada en la sección 1.9.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4339">Upon initialization, the server MUST set its state to "not initialized" and start listening for messages on the named pipe specified in section 1.9.</span></span> <span data-ttu-id="d07fb-4340">Después de realizar cualquier otra inicialización interna, DEBE pasar al estado "en ejecución".</span><span class="sxs-lookup"><span data-stu-id="d07fb-4340">After doing any other internal initialization, it MUST transition to the "running" state.</span></span>

### <a name="314-higher-layer-triggered-events"></a><span data-ttu-id="d07fb-4341">3.1.4 Eventos desencadenados al más alto nivel</span><span class="sxs-lookup"><span data-stu-id="d07fb-4341">3.1.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="d07fb-4342">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4342">None.</span></span>

### <a name="315-message-processing-and-sequencing-rules"></a><span data-ttu-id="d07fb-4343">3.1.5 Reglas de procesamiento y secuenciación de mensajes</span><span class="sxs-lookup"><span data-stu-id="d07fb-4343">3.1.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="d07fb-4344">Cada vez que se produce un error durante el procesamiento de un mensaje enviado por un cliente, el servidor DEBE notificar un error al cliente como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4344">Whenever there is an error occurs during processing of a message sent by a client the server MUST report an error back to the client as follows:</span></span>

-   <span data-ttu-id="d07fb-4345">Detener el procesamiento del mensaje enviado por el cliente</span><span class="sxs-lookup"><span data-stu-id="d07fb-4345">Stop processing the message sent by the client</span></span>
-   <span data-ttu-id="d07fb-4346">Responda con el encabezado de mensaje (solo) del mensaje enviado por el cliente, manteniendo \_ intacto el campo msg.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4346">Respond with the message header (only) of the message sent by the client, keeping \_msg field intact.</span></span>
-   <span data-ttu-id="d07fb-4347">Establezca el \_ campo de estado en el valor del código de error.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4347">Set the \_status field to the error code value.</span></span>

<span data-ttu-id="d07fb-4348">Cuando llega un mensaje, el servidor DEBE comprobar el valor del campo msg para ver si es un tipo conocido (consulte la \_ sección 2.2.2).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4348">When a message arrives, the server MUST check the \_msg field value to see if it is a known type (see section 2.2.2).</span></span> <span data-ttu-id="d07fb-4349">Si no se conoce el tipo, DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4349">If the type is not known, it MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="d07fb-4350">A continuación, el servidor DEBE validar el valor del campo \_ ulChecksum si el tipo de mensaje es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4350">The server MUST then validate the \_ulChecksum field value if the message type is one of the following:</span></span>

-   <span data-ttu-id="d07fb-4351">CPMConnectIn (0x000000C8)</span><span class="sxs-lookup"><span data-stu-id="d07fb-4351">CPMConnectIn (0x000000C8)</span></span>
-   <span data-ttu-id="d07fb-4352">CPMCreateQueryIn (0x000000CA)</span><span class="sxs-lookup"><span data-stu-id="d07fb-4352">CPMCreateQueryIn (0x000000CA)</span></span>
-   <span data-ttu-id="d07fb-4353">CPMSetBindingsIn (0x000000D0)</span><span class="sxs-lookup"><span data-stu-id="d07fb-4353">CPMSetBindingsIn (0x000000D0)</span></span>
-   <span data-ttu-id="d07fb-4354">CPMGetRowsIn (0x000000CC)</span><span class="sxs-lookup"><span data-stu-id="d07fb-4354">CPMGetRowsIn (0x000000CC)</span></span>
-   <span data-ttu-id="d07fb-4355">CPMFetchValueIn (0x000000E4)</span><span class="sxs-lookup"><span data-stu-id="d07fb-4355">CPMFetchValueIn (0x000000E4)</span></span>

<span data-ttu-id="d07fb-4356">Para validar el valor del campo ulChecksum, el servidor DEBE comprobar el valor que el cliente especificó en el campo iClientVersion en el \_ \_ mensaje CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4356">To validate the \_ulChecksum field value, the server MUST check the value the client specified in the \_iClientVersion field in the CPMConnectIn message.</span></span>

<span data-ttu-id="d07fb-4357">Si el campo iClientVersion no está establecido en 0x00000008 y el campo ulChecksum no está establecido en 0x00000000, el servidor DEBE notificar un \_ error STATUS INVALID PARAMETER \_ \_ \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4357">If the \_iClientVersion field is not set to 0x00000008 and the \_ulChecksum field is not set to 0x00000000, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="d07fb-4358">El servidor NO DEBE validar el campo ulChecksum para los clientes y establecer el campo iClientVersion en un \_ \_ valor menor que 0x00000008.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4358">Server MUST NOT validate the \_ulChecksum field for clients the set the \_iClientVersion field to a value less than 0x00000008.</span></span>

<span data-ttu-id="d07fb-4359">Si el valor del campo iClientVersionfield es 0x00000008 o superior, el servidor DEBE validar que el campo ulChecksum se calculó como se especifica en la sección \_ \_ 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4359">If the \_iClientVersionfield field value is 0x00000008 or greater, the server MUST validate that the \_ulChecksum field was calculated as specified in section 3.2.4.</span></span> <span data-ttu-id="d07fb-4360">Si el \_ valor ulChecksum no es válido, el servidor DEBE notificar un error STATUS \_ INVALID PARAMETER \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4360">If the \_ulChecksum value is invalid, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="d07fb-4361">A continuación, el servidor comprueba en qué estado se encuentra.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4361">Next, the server checks which state is it in.</span></span> <span data-ttu-id="d07fb-4362">Si su estado es "no inicializado", el servidor DEBE notificar un error CI \_ E \_ NOT \_ INITIALIZED (0x8004180B).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4362">If its state is "not initialized" the server MUST report a CI\_E\_NOT\_INITIALIZED (0x8004180B) error.</span></span> <span data-ttu-id="d07fb-4363">Si el estado es "apagar", el servidor DEBE notificar un error CI \_ E \_ SHUTDOWN (0x80041812).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4363">If the state is "shutting down" the server MUST report a CI\_E\_SHUTDOWN (0x80041812) error.</span></span>

<span data-ttu-id="d07fb-4364">Una vez que se ha determinado que un encabezado es válido y que el servidor está en estado "en ejecución", se DEBE realizar un procesamiento más específico del mensaje tal como se especifica en las subsecciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4364">Once a header has been determined to be valid and the server to be in "running" state, further message-specific processing MUST be done as specified in the subsections below.</span></span>

### <a name="3151-remote-indexing-service-catalog-management"></a><span data-ttu-id="d07fb-4365">3.1.5.1 Remote Indexing Service Catalog Management</span><span class="sxs-lookup"><span data-stu-id="d07fb-4365">3.1.5.1 Remote Indexing Service Catalog Management</span></span>

### <a name="31511-receiving-a-cpmcistateinout-request"></a><span data-ttu-id="d07fb-4366">3.1.5.1.1 Recepción de una solicitud CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-4366">3.1.5.1.1 Receiving a CPMCiStateInOut Request</span></span>

<span data-ttu-id="d07fb-4367">Cuando el servidor recibe una solicitud de mensaje CPMCIStateInOut del cliente, el servidor debe comprobar primero si el cliente está en una lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4367">When the server receives a CPMCIStateInOut message request from the client, the server MUST first check if the client is in a list of connected clients.</span></span> <span data-ttu-id="d07fb-4368">Si el cliente no está en la lista, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4368">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="d07fb-4369">De lo contrario, DEBE responder al cliente con un mensaje CPMCIStateInOut, rellenando con información sobre el catálogo asociado del cliente, tal como se especifica en la sección 2.2.3.1.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4369">Otherwise, it MUST respond to the client with a CPMCIStateInOut message, filling it in with information about the client's associated catalog as specified in Section 2.2.3.1.</span></span>

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a><span data-ttu-id="d07fb-4370">3.1.5.1.2 Recepción de una solicitud CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4370">3.1.5.1.2 Receiving a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="d07fb-4371">Cuando el servidor recibe una solicitud de mensaje CPMSetCatStateIn del cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4371">When the server receives a CPMSetCatStateIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4372">Compruebe que el cliente tiene acceso administrativo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4372">Check that client has administrative access.</span></span> <span data-ttu-id="d07fb-4373">Si el cliente no tiene acceso administrativo, el servidor DEBE notificar un error STATUS \_ ACCESS \_ DENIED (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4373">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="d07fb-4374">Si dwNewState no es igual a CICAT ALL OPENED, cambie el estado del catálogo especificado en el campo CatName según lo especificado por el \_ \_ campo \_ \_ dwNewState.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4374">If \_dwNewState is not equal to CICAT\_ALL\_OPENED then change the state of the catalog specified in the CatName field as specified by the \_dwNewState field.</span></span> <span data-ttu-id="d07fb-4375">Consulte la sección 2.2.3.2 para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4375">See Section 2.2.3.2 for more details.</span></span> <span data-ttu-id="d07fb-4376">Si el servidor no encuentra un catálogo con el nombre especificado en el campo CatName, el servidor DEBE devolver un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4376">If the server does not locate a catalog with the name specified in the CatName field, the server MUST return a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="d07fb-4377">Responda al cliente con un mensaje CPMSetCatStateOut, donde dwOldState DEBE establecerse en \_ el estado anterior del catálogo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4377">Respond to the client with a CPMSetCatStateOut message, where \_dwOldState MUST be set to the previous state of the catalog.</span></span> <span data-ttu-id="d07fb-4378">Si dwNewState es igual a CICAT ALL OPENED, el servidor DEBE comprobar el estado de todos los catálogos y, si se inician todos ellos, debe establecer dwOldState en 0x00000001 y, de lo \_ \_ \_ \_ contrario, \_ establecer dwOldState en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4378">If \_dwNewState is equal to CICAT\_ALL\_OPENED the server MUST check the status of all catalogs and if all of them are started it MUST set \_dwOldState to 0x00000001, and otherwise set \_dwOldState to 0x00000000.</span></span>

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="d07fb-4379">3.1.5.1.3 Recibir una solicitud CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4379">3.1.5.1.3 Receiving a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="d07fb-4380">Cuando el servidor recibe una solicitud de mensaje CPMUpdateDocumentsIn, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4380">When the server receives a CPMUpdateDocumentsIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4381">Compruebe si el cliente está en una lista de clientes conectados (que tienen un catálogo asociado).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4381">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="d07fb-4382">Si el cliente no está en la lista, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4382">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="d07fb-4383">Compruebe que el cliente tiene acceso administrativo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4383">Check that client has administrative access.</span></span> <span data-ttu-id="d07fb-4384">Si el cliente no tiene acceso administrativo al servidor, el servidor DEBE notificar un error STATUS \_ ACCESS \_ DENIED (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4384">If the client does not have administrative access to the server, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="d07fb-4385">Comience el proceso de indexación de la ruta de acceso especificada por el cliente, realizando un examen completo o incremental, en función del valor del campo de marca en el mensaje \_ CPMUpdateDocumentsIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4385">Begin the process of indexing the path specified by the client, doing a full or incremental scan, depending on value of \_flag field in CPMUpdateDocumentsIn message.</span></span> <span data-ttu-id="d07fb-4386">Si la ruta de acceso no se indexó previamente, DEBE agregarse a la colección de ubicaciones indizadas y realizar un examen completo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4386">If the path was not previously indexed, it MUST be added to the collection of indexed locations and a full scan performed.</span></span> <span data-ttu-id="d07fb-4387">Si se especifica un valor no válido del campo de marca, el servidor DEBE actuar como si la marca se hubiera establecido en UPD INIT y realizar \_ \_ un examen \_ completo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4387">If an illegal value of the \_flag field is specified, the server MUST act as if \_flag was set to UPD\_INIT and perform a full scan.</span></span> <span data-ttu-id="d07fb-4388">Esta operación DEBE realizarse en el catálogo asociado al cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4388">This operation MUST be performed in the catalog associated with the client.</span></span>
-   <span data-ttu-id="d07fb-4389">Responda al cliente con el encabezado de mensaje para CPMUpdateDocumentsIn y establezca el campo de estado en los resultados \_ de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4389">Respond to the client with the message header for the CPMUpdateDocumentsIn, and set the \_status field to the results of the request.</span></span>

### <a name="31514-receiving-a-cpmforcemergein-request"></a><span data-ttu-id="d07fb-4390">3.1.5.1.4 Recepción de una solicitud CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4390">3.1.5.1.4 Receiving a CPMForceMergeIn Request</span></span>

<span data-ttu-id="d07fb-4391">Cuando el servidor recibe una solicitud de mensaje CPMForceMergeIn, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4391">When the server receives a CPMForceMergeIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4392">Compruebe si el cliente está en una lista de clientes conectados (que tienen un catálogo asociado).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4392">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="d07fb-4393">Si el cliente no está en la lista, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4393">If client is not in the list the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="d07fb-4394">Compruebe que el cliente tiene acceso administrativo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4394">Check that client has administrative access.</span></span> <span data-ttu-id="d07fb-4395">Si el cliente no tiene acceso administrativo, el servidor DEBE notificar un error STATUS \_ ACCESS \_ DENIED (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4395">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="d07fb-4396">Comience cualquier proceso de mantenimiento necesario para mejorar el rendimiento de las consultas en un catálogo, asociado al cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4396">Begin any process of maintenance necessary to improve query performance on a catalog, associated with the client.</span></span>
-   <span data-ttu-id="d07fb-4397">Responda al cliente con un encabezado de mensaje para CPMForceMergeIn y establezca el campo de estado en los \_ resultados de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4397">Respond to the client with a message header for the CPMForceMergeIn, and set the \_status field to the results of the request.</span></span>

<span data-ttu-id="d07fb-4398">Tenga en cuenta que el proceso de mantenimiento es asincrónico y puede continuar después de que el cliente reciba el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4398">Note that process of maintenance is asynchronous and can continue after client receives the response message.</span></span> <span data-ttu-id="d07fb-4399">Este proceso no afecta directamente al protocolo de ninguna manera (aparte del tiempo de respuesta).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4399">This process does not directly impact the protocol in any way (other than response time).</span></span>

### <a name="3152-remote-indexing-service-querying"></a><span data-ttu-id="d07fb-4400">3.1.5.2 Consultas remotas del servicio de indexación</span><span class="sxs-lookup"><span data-stu-id="d07fb-4400">3.1.5.2 Remote Indexing Service Querying</span></span>

### <a name="31521-receiving-a-cpmconnectin-request"></a><span data-ttu-id="d07fb-4401">3.1.5.2.1 Recepción de una solicitud CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4401">3.1.5.2.1 Receiving a CPMConnectIn Request</span></span>

<span data-ttu-id="d07fb-4402">Cuando el servidor recibe una solicitud CPMConnectIn de un cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4402">When the server receives a CPMConnectIn request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4403">Compruebe si el cliente está en la lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4403">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="d07fb-4404">Si este es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4404">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="d07fb-4405">Comprueba si el catálogo especificado existe y no está en estado detenido.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4405">Checks if the specified catalog exists and not in the stopped state.</span></span> <span data-ttu-id="d07fb-4406">Si este no es el caso, el servidor DEBE notificar un error CI \_ E \_ NO CATALOG \_ (0x8004181D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4406">If this is not the case then the server MUST a report CI\_E\_NO\_CATALOG (0x8004181D) error.</span></span>
-   <span data-ttu-id="d07fb-4407">Agregue el cliente a la lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4407">Add the client to the list of connected clients.</span></span>
-   <span data-ttu-id="d07fb-4408">Asocie el catálogo al cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4408">Associate the catalog with the client.</span></span>
-   <span data-ttu-id="d07fb-4409">Almacene la información pasada en el mensaje CPMConnectIn (por ejemplo, el nombre del catálogo, la versión del cliente, etc.) en el estado del cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4409">Store the information passed in the CPMConnectIn message (such as catalog name, client version, etc.) in the client state.</span></span>
-   <span data-ttu-id="d07fb-4410">Responda al cliente con un mensaje CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4410">Respond to the client with a CPMConnectOut message.</span></span>

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a><span data-ttu-id="d07fb-4411">3.1.5.2.2 Recibir una solicitud CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4411">3.1.5.2.2 Receiving a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="d07fb-4412">Cuando el servidor recibe una solicitud de mensaje CPMCreateQueryIn de un cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4412">When the server receives a CPMCreateQueryIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4413">Compruebe si el cliente está en la lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4413">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="d07fb-4414">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4414">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="d07fb-4415">Compruebe si el cliente ya tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4415">Check if the client already has a query associated with it.</span></span> <span data-ttu-id="d07fb-4416">Si este es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4416">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="d07fb-4417">Compruebe si el catálogo asociado al cliente está en estado que permite procesar la consulta (CICAT \_ READONLY o CICAT \_ WRITABLE).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4417">Check if the catalog associated with the client is in state which allows query to be processed (CICAT\_READONLY or CICAT\_WRITABLE).</span></span> <span data-ttu-id="d07fb-4418">Si este no es el caso, el servidor DEBE notificar un error QUERY \_ S \_ NO QUERY \_ (0x8004160C).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4418">If this is not the case, the server MUST report a QUERY\_S\_NO\_QUERY (0x8004160C) error.</span></span>
-   <span data-ttu-id="d07fb-4419">Analice el conjunto de restricciones, los criterios de ordenación y las agrupaciones especificados en la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4419">Parse the restriction set, sort orders, and groupings specified in the query.</span></span> <span data-ttu-id="d07fb-4420">Si el servidor encuentra un error, DEBE notificar un error adecuado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4420">If the server encounters an error, it MUST report an appropriate error.</span></span> <span data-ttu-id="d07fb-4421">Si se produce un error en este paso por cualquier otro motivo, el servidor DEBE notificar el error encontrado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4421">If this step fails for any other reason, the server MUST report the error encountered.</span></span> <span data-ttu-id="d07fb-4422">Para obtener información sobre los errores de consulta del servicio de indexación, \[ vea MSDN-QUERYERR \] .</span><span class="sxs-lookup"><span data-stu-id="d07fb-4422">For information about indexing service query errors, see \[MSDN-QUERYERR\].</span></span>
-   <span data-ttu-id="d07fb-4423">Guarde la consulta de búsqueda en el estado del cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4423">Save the search query in the state for the client.</span></span>
-   <span data-ttu-id="d07fb-4424">Realice los preparativos necesarios para atender filas a un cliente y asocie la consulta con los identificadores de cursor adecuados (en función de la información que se pase en el mensaje CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4424">Make any preparations needed to serve rows to a client and associate the query with appropriate cursor handles (depending on information passed in CPMCreateQueryIn message).</span></span>
-   <span data-ttu-id="d07fb-4425">Agregue esos identificadores a la lista de identificadores de cursor del cliente e inicialice listas de identificadores de capítulos y marcadores.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4425">Add those handles to client's list of cursor handles, and initialize lists of chapter handles and bookmarks.</span></span>
-   <span data-ttu-id="d07fb-4426">Inicializar una lista de identificadores de capítulo para cada cursor de esta consulta en DB \_ NULL \_ HCHAPTER</span><span class="sxs-lookup"><span data-stu-id="d07fb-4426">Initialize list of chapter handles for every cursor in this query to DB\_NULL\_HCHAPTER</span></span>
-   <span data-ttu-id="d07fb-4427">Inicialice la lista de identificadores de marcador para cada cursor de esta consulta en un conjunto de DBBMK \_ FIRST y DBBMK \_ LAST.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4427">Initialize list of bookmark handles for every cursor in this query to a set of DBBMK\_FIRST and DBBMK\_LAST.</span></span>
-   <span data-ttu-id="d07fb-4428">Marque la consulta como no supervisada para los cambios.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4428">Mark the query as not monitored for changes.</span></span>
-   <span data-ttu-id="d07fb-4429">Inicialice el número de filas en el número calculado actualmente de filas (que puede ser 0 si la consulta no comenzó a ejecutarse o algún número si la consulta está en un proceso de ejecución) e inicialice el numerador y el denominador de finalización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4429">Initialize the number of rows to the currently calculated number of rows (which can be 0 if query did not start to execute or some number if query is in a process of execution), and initialize the numerator and denominator of query completion.</span></span>
-   <span data-ttu-id="d07fb-4430">Responda al cliente con un mensaje CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4430">Respond to the client with a CPMCreateQueryOut message.</span></span>

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a><span data-ttu-id="d07fb-4431">3.1.5.2.3 Recepción de una solicitud CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4431">3.1.5.2.3 Receiving a CPMGetQueryStatusIn Request</span></span>

<span data-ttu-id="d07fb-4432">Cuando el servidor recibe una solicitud de mensaje CPMGetQueryStatusIn de un cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4432">When the server receives a CPMGetQueryStatusIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4433">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4433">Check if the client has query associated with it.</span></span> <span data-ttu-id="d07fb-4434">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4434">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="d07fb-4435">Compruebe si el identificador del cursor está en una lista de identificadores de cursor del cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4435">Check if the cursor handle is in a list of client's cursor handles.</span></span> <span data-ttu-id="d07fb-4436">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4436">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="d07fb-4437">Prepare un mensaje CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4437">Prepare a CPMGetQueryStatusOut message.</span></span> <span data-ttu-id="d07fb-4438">El servidor DEBE recuperar el estado de consulta actual y establecerlo en el campo \_ QStatus (vea 2.2.3.11 para ver los valores posibles).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4438">The server MUST retrieve the current query status and set it in the \_QStatus field (see 2.2.3.11 for possible values).</span></span> <span data-ttu-id="d07fb-4439">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar un error.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4439">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="d07fb-4440">Responda al cliente con el mensaje CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4440">Respond to the client with the CPMGetQueryStatusOut message.</span></span>

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a><span data-ttu-id="d07fb-4441">3.1.5.2.4 Recepción de una solicitud CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4441">3.1.5.2.4 Receiving a CPMGetQueryStatusExIn Request</span></span>

<span data-ttu-id="d07fb-4442">Cuando el servidor recibe una solicitud de mensaje CPMGetQueryStatusExIn de un cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4442">When the server receives a CPMGetQueryStatusExIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4443">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4443">Check if the client has a query associated with it.</span></span> <span data-ttu-id="d07fb-4444">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4444">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="d07fb-4445">Compruebe si el identificador de cursor pasado está en una lista de identificadores de cursor del cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4445">Check if the cursor handle passed is in a list of client's cursor handles.</span></span> <span data-ttu-id="d07fb-4446">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4446">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="d07fb-4447">Prepare un mensaje CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4447">Prepare a CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="d07fb-4448">El servidor DEBE recuperar el estado de consulta actual y el progreso de la consulta y establecer QStatus (vea 2.2.3.11 para ver los valores posibles), \_ dwRatioFinishedDenominator y \_ dwRatioFinishedNumerator, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4448">The server MUST retrieve the current query status and query progress and set QStatus (see 2.2.3.11 for possible values), \_dwRatioFinishedDenominator and \_dwRatioFinishedNumerator respectively.</span></span> <span data-ttu-id="d07fb-4449">A continuación, DEBE establecer el número de filas de los resultados de la consulta \_ en cRowsTotal.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4449">It MUST then set the number of rows in the query results to \_cRowsTotal.</span></span> <span data-ttu-id="d07fb-4450">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar que se ha encontrado un error.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4450">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="d07fb-4451">Recupere información sobre el catálogo del cliente y rellene \_ cFilteredDocuments y \_ cDocumentsToFilter.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4451">Retrieve information about client's catalog and fill in \_cFilteredDocuments and \_cDocumentsToFilter.</span></span> <span data-ttu-id="d07fb-4452">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar que se ha encontrado un error.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4452">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="d07fb-4453">Recupere la posición del marcador indicado por el identificador en el campo bmk y rellene el campo iRowBmk restante en el mensaje \_ \_ CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4453">Retrieve the position of the bookmark indicated by the handle in the \_bmk field, and fill the remaining \_iRowBmk field in the CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="d07fb-4454">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar que se ha encontrado un error.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4454">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="d07fb-4455">Responda al cliente con el mensaje CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4455">Respond to the client with the CPMGetQueryStatusExOut message.</span></span>

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a><span data-ttu-id="d07fb-4456">3.1.5.2.5 Recepción de una solicitud CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4456">3.1.5.2.5 Receiving a CPMRatioFinishedIn Request</span></span>

<span data-ttu-id="d07fb-4457">Cuando el servidor recibe una solicitud de mensaje CPMRatioFinishedIn de un cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4457">When the server receives a CPMRatioFinishedIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4458">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4458">Check if the client has query associated with it.</span></span> <span data-ttu-id="d07fb-4459">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4459">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="d07fb-4460">Compruebe si el identificador de cursor pasado está en la lista de identificadores de cursor del cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4460">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="d07fb-4461">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4461">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="d07fb-4462">Prepare un mensaje CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4462">Prepare a CPMRatioFinishedOut message.</span></span> <span data-ttu-id="d07fb-4463">El servidor DEBE recuperar el estado de consulta del cliente y rellenar los campos \_ ulNumerator, \_ ulDenominator \_ y cRows.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4463">The server MUST retrieve the client's query status and fill in \_ulNumerator, \_ulDenominator and \_cRows fields.</span></span> <span data-ttu-id="d07fb-4464">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar que se ha encontrado un error.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4464">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="d07fb-4465">Si cRows es igual al último número notificado de filas para esta consulta, establezca \_ \_ fNewRows en 0x00000000; de lo contrario, estafórelo en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4465">If \_cRows is equal to the last reported number of rows for this query, then set \_fNewRows to 0x00000000, otherwise set it to 0x00000001.</span></span>
-   <span data-ttu-id="d07fb-4466">Actualice el último número notificado de filas de esta consulta al valor \_ de cRows.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4466">Update the last reported number of rows for this query to the value of \_cRows.</span></span>
-   <span data-ttu-id="d07fb-4467">Responda al cliente con el mensaje CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4467">Respond to the client with the CPMRatioFinishedOut message.</span></span>

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a><span data-ttu-id="d07fb-4468">3.1.5.2.6 Recepción de una solicitud CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4468">3.1.5.2.6 Receiving a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="d07fb-4469">Cuando el servidor recibe una solicitud de mensaje CPMSetBindingsIn de un cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4469">When the server receives a CPMSetBindingsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4470">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4470">Check if the client has a query associated with it.</span></span> <span data-ttu-id="d07fb-4471">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4471">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="d07fb-4472">Compruebe si el identificador de cursor pasado está en la lista de identificadores de cursor del cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4472">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="d07fb-4473">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4473">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="d07fb-4474">Compruebe que la información de enlaces es válida (es decir, la columna al menos especifica el valor, la longitud o el estado que se va a devolver; no hay superposición en los enlaces para el valor, la longitud o el estado; y el valor, la longitud y el estado caben en el tamaño de fila especificado) y si no se informa de un \_ error BADBINDINFO (0x80040E08) de la base \_ de datos.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4474">Verify that bindings information is valid (i.e., column at least specifies value, length or status to be returned; no overlap in bindings for value, length or status; and value, length and status fit in the row size specified) and if not report a DB\_E\_BADBINDINFO (0x80040E08) error.</span></span>
-   <span data-ttu-id="d07fb-4475">Guarde la información de enlace asociada a las columnas especificadas en el campo aColumns.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4475">Save the binding information associated with the columns specified in the aColumns field.</span></span> <span data-ttu-id="d07fb-4476">Si se produce un error en este paso por cualquier motivo, el servidor DEBE informar de que se ha encontrado un error.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4476">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="d07fb-4477">Responda al cliente con un encabezado de mensaje (solo) con msg establecido en CPMSetBindingsIn y el estado establecido en los resultados \_ \_ del enlace especificado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4477">Respond to the client with a message header (only) with \_msg set to CPMSetBindingsIn, and \_status set to the results of the specified binding.</span></span>

### <a name="31527-receiving-a-cpmgetrowsin-request"></a><span data-ttu-id="d07fb-4478">3.1.5.2.7 Recepción de una solicitud CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4478">3.1.5.2.7 Receiving a CPMGetRowsIn Request</span></span>

<span data-ttu-id="d07fb-4479">Cuando el servidor recibe una solicitud de mensaje CPMGetRowsIn de un cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4479">When the server receives a CPMGetRowsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4480">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4480">Check if the client has query associated with it.</span></span> <span data-ttu-id="d07fb-4481">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4481">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="d07fb-4482">Compruebe si el identificador de cursor pasado está en una lista de identificadores de cursor del cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4482">Check if the cursor handle passed is in athelist of the client's cursor handles.</span></span> <span data-ttu-id="d07fb-4483">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4483">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="d07fb-4484">Compruebe si el cliente tiene un conjunto actual de enlaces.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4484">Check if the client has a current set of bindings.</span></span> <span data-ttu-id="d07fb-4485">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4485">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="d07fb-4486">Prepare un mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4486">Prepare a CPMGetRowsOut message.</span></span> <span data-ttu-id="d07fb-4487">El servidor DEBE colocar el cursor en los resultados de la consulta como se indica en la descripción de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4487">The server MUST position the cursor in query results as indicated by the seek description.</span></span> <span data-ttu-id="d07fb-4488">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar que se ha encontrado un error.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4488">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="d07fb-4489">Capture tantas filas como quepa en un búfer, cuyo tamaño se indica mediante cbReadBuffer, pero no más de lo indicado por \_ \_ cRowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4489">Fetch as many rows as fits in a buffer, the size of which is indicated by \_cbReadBuffer, but not more than indicated by \_cRowsToTransfer.</span></span> <span data-ttu-id="d07fb-4490">Al capturar filas, el servidor DEBE comparar el tipo de valor de propiedad de cada columna seleccionada con el tipo especificado en el conjunto actual de enlaces del cliente (sección 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4490">When fetching rows, the server MUST compare each selected column's property value type to the type specified in the Client's current set of bindings (section 3.1.1).</span></span> <span data-ttu-id="d07fb-4491">Si el tipo del enlace no es VT VARIANT, el servidor DEBE intentar convertir el valor de propiedad de la columna \_ en ese tipo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4491">If the type in the binding is not VT\_VARIANT, the server MUST attempt to convert the column's property value to that type.</span></span> <span data-ttu-id="d07fb-4492">De lo contrario, si la marca DBPROP USEEXTENDEDDBTYPES está establecida en el conjunto de propiedades \_ DBPROPSET QUERYEXT del cliente, o si el valor de propiedad de la columna no es un tipo VT VECTOR, el valor de propiedad DEBE devolverse en su \_ \_ tipo normal.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4492">Otherwise, if the DBPROP\_USEEXTENDEDDBTYPES flag is set in the client's DBPROPSET\_QUERYEXT property set, or if the column's property value is not a VT\_VECTOR type, then the property value MUST be returned in its normal type.</span></span> <span data-ttu-id="d07fb-4493">Si ninguno de estos casos es el caso (es decir, el servidor tiene un tipo VT VECTOR y el cliente no admite VT VECTOR), el servidor DEBE intentar convertirlo a un tipo VT ARRAY como se muestra a continuación: los elementos de la matriz VT \_ \_ \_ \_ I8, VT \_ UI8, VT FILETIME y \_ VT \_ CLSID no se pueden convertir y, en su lugar, producir un error; Los elementos de la matriz VT LPSTR y VT LPWSTR DEBEN convertirse en \_ VT BSTR; los elementos de matriz de todos los demás tipos \_ DEBEN permanecer sin \_ cambios.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4493">If none of these are the case (i.e., the server has a VT\_VECTOR type, and the client does not support VT\_VECTOR), then the server MUST attempt to convert it to a VT\_ARRAY type as follows: VT\_I8, VT\_UI8, VT\_FILETIME, and VT\_CLSID array elements cannot be converted and instead fail; VT\_LPSTR and VT\_LPWSTR array elements MUST be converted to VT\_BSTR; array elements of all other types MUST remain unchanged.</span></span> <span data-ttu-id="d07fb-4494">Por último, si las columnas de fila contienen identificadores de capítulo o identificadores de marcador, el servidor DEBE actualizar las listas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4494">Finally, if row columns contain chapter handles or bookmark handles, the server MUST update the corresponding lists.</span></span> <span data-ttu-id="d07fb-4495">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar que se ha encontrado un error.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4495">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="d07fb-4496">Almacene el número real de filas capturadas en \_ cRowsReturned.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4496">Store the actual number of rows fetched in \_cRowsReturned.</span></span>
-   <span data-ttu-id="d07fb-4497">Copie la descripción de la búsqueda y el campo de capítulo de CPMGetRowsIn en un mensaje CPMGetRowsOut que se va a enviar.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4497">Copy the seek description and chapter field from CPMGetRowsIn to a CPMGetRowsOut message to be sent.</span></span>
-   <span data-ttu-id="d07fb-4498">Almacene las filas capturadas en el campo Filas (vea la nota sobre el byte de estado siguiente y la sección 2.2.3.16 en la estructura del campo Filas).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4498">Store fetched rows in the Rows field (see note on status byte below and section 2.2.3.16 on the structure of the Rows field).</span></span>
-   <span data-ttu-id="d07fb-4499">Responda al cliente con el mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4499">Respond to the client with the CPMGetRowsOut message.</span></span>

<span data-ttu-id="d07fb-4500">Nota sobre el campo de bytes de estado:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4500">Note on status byte field:</span></span>

<span data-ttu-id="d07fb-4501">Si StatusUsed está establecido en 0x01 en el CTableColumn del mensaje CPMSetBindingIn de la columna, el servidor DEBE establecer el byte de estado (que se encuentra en StatusOffset desde el principio de la fila) para esta columna en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4501">If StatusUsed is set to 0x01 in the CTableColumn of the CPMSetBindingIn message for the column, then the server MUST set the status byte (which is located at StatusOffset from the start of the row) for this column to one of the following values:</span></span>



| <span data-ttu-id="d07fb-4502">Value</span><span class="sxs-lookup"><span data-stu-id="d07fb-4502">Value</span></span> | <span data-ttu-id="d07fb-4503">Significado</span><span class="sxs-lookup"><span data-stu-id="d07fb-4503">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="d07fb-4504">0x00</span><span class="sxs-lookup"><span data-stu-id="d07fb-4504">0x00</span></span>  | <span data-ttu-id="d07fb-4505">StatusOK</span><span class="sxs-lookup"><span data-stu-id="d07fb-4505">StatusOK</span></span>       |
| <span data-ttu-id="d07fb-4506">0x01</span><span class="sxs-lookup"><span data-stu-id="d07fb-4506">0x01</span></span>  | <span data-ttu-id="d07fb-4507">StatusDeferred</span><span class="sxs-lookup"><span data-stu-id="d07fb-4507">StatusDeferred</span></span> |
| <span data-ttu-id="d07fb-4508">0x02</span><span class="sxs-lookup"><span data-stu-id="d07fb-4508">0x02</span></span>  | <span data-ttu-id="d07fb-4509">StatusNull</span><span class="sxs-lookup"><span data-stu-id="d07fb-4509">StatusNull</span></span>     |



 

<span data-ttu-id="d07fb-4510">Si el valor de propiedad no está presente para esta fila, el servidor DEBE establecer el byte de estado en StatusNull.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4510">If the property value is absent for this row, the server MUST set the status byte to StatusNull.</span></span> <span data-ttu-id="d07fb-4511">Si el valor es demasiado grande para transferirse en el mensaje CPMGetRowsOut, el servidor DEBE establecer el byte de estado en StatusDeferred.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4511">If the value is too big to be transferred in the CPMGetRowsOut message, the server MUST set the status byte to StatusDeferred.</span></span> <span data-ttu-id="d07fb-4512">De lo contrario, el servidor DEBE establecer el byte de estado en StatusOK.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4512">Otherwise the server MUST set the status byte to StatusOK.</span></span>

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a><span data-ttu-id="d07fb-4513">3.1.5.2.8 Recepción de una solicitud CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4513">3.1.5.2.8 Receiving a CPMFetchValueIn Request</span></span>

<span data-ttu-id="d07fb-4514">Cuando el servidor recibe una solicitud de mensaje CPMFetchValueIn de un cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4514">When the server receives a CPMFetchValueIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4515">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4515">Check if the client has query associated with it.</span></span> <span data-ttu-id="d07fb-4516">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4516">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="d07fb-4517">Prepare un mensaje CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4517">Prepare a CPMFetchValueOut message.</span></span> <span data-ttu-id="d07fb-4518">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar un error.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4518">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="d07fb-4519">Busque el documento indicado por el campo wid y compruebe si el identificador de propiedad de este documento (más adelante denominado "valor de propiedad") indicado por la estructura PropSpec está \_ disponible para este cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4519">Find the document indicated by the\_wid field and check if the property ID for this document (later referred to as 'property value') indicated by the PropSpec structure is available for this client.</span></span> <span data-ttu-id="d07fb-4520">Si este valor no está disponible, el servidor DEBE establecer fValueExists en 0x00000000 y, de lo \_ contrario, \_ establecer fValueExists en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4520">If this value is not available the server MUST set \_fValueExists to 0x00000000, and otherwise set \_fValueExists to 0x00000001.</span></span> <span data-ttu-id="d07fb-4521">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar un error.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4521">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="d07fb-4522">Si \_ fValueExists es igual a 0x00000001 el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4522">If \_fValueExists is equal to 0x00000001 the server MUST do the following:</span></span>
-   -   <span data-ttu-id="d07fb-4523">Serialice el valor de propiedad en una estructura SERIALIZEDPROPERTYVALUE y copie, a partir del desplazamiento \_ cbSoFar, como máximo los bytes cbChunk (pero no más allá del final de la propiedad serializada) en el \_ campo vValue.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4523">Serialize the property value to a SERIALIZEDPROPERTYVALUE structure and copy, starting from the \_cbSoFar offset, at most \_cbChunk bytes (but not past the end of the serialized property) to vValue field.</span></span> <span data-ttu-id="d07fb-4524">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar un error.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4524">If this step fails for any reason server MUST report an error.</span></span>
    -   <span data-ttu-id="d07fb-4525">Establezca \_ cbValue en el número de bytes copiados en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4525">Set \_cbValue to the number of bytes copied in previous step.</span></span>
    -   <span data-ttu-id="d07fb-4526">Establezca vType en el tipo de propiedad del valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4526">Set vType to the property type of the property value.</span></span>
    -   <span data-ttu-id="d07fb-4527">Si la longitud de la propiedad serializada es mayor que cbSoFar agregada a \_ \_ cbValue, establezca fMoreExists en 0x00000001; de lo contrario, estafrála \_ en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4527">If the length of serialized property is greater than \_cbSoFar added to \_cbValue, then set \_fMoreExists to 0x00000001, otherwise set it to 0x00000000.</span></span>

-   <span data-ttu-id="d07fb-4528">Respuesta al cliente con el mensaje CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-4528">Respond to the client with the CPMFetchValueOut message</span></span>

### <a name="31529-receiving-a-cpmgetnotify-request"></a><span data-ttu-id="d07fb-4529">3.1.5.2.9 Recibir una solicitud CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="d07fb-4529">3.1.5.2.9 Receiving a CPMGetNotify Request</span></span>

<span data-ttu-id="d07fb-4530">Cuando el servidor recibe un mensaje CPMGetNotify de un cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4530">When the server receives a CPMGetNotify message from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4531">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4531">Check if the client has query associated with it.</span></span> <span data-ttu-id="d07fb-4532">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4532">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="d07fb-4533">Si no se ha realizado ningún cambio en el conjunto de resultados de la consulta desde el último mensaje CPMSendNotifyOut para este cliente, o si la consulta no está supervisada actualmente para los cambios en el conjunto de resultados, el servidor DEBE responder con el mensaje CPMGetNotify y empezar a supervisar la consulta en busca de cambios en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4533">If there were no changes in the query result set since the last CPMSendNotifyOut message for this client, or if the query is not currently monitored for changes in the results set, then the server MUST respond with CPMGetNotify message and start to monitor the query for changes in results set.</span></span> <span data-ttu-id="d07fb-4534">Si más adelante se produce un cambio en el conjunto de resultados de la consulta, el servidor DEBE enviar exactamente un mensaje CPMSendNotifyOut al cliente y DEBE especificar el cambio en el \_ campo watchNotify.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4534">If at a later time there is a change in the query results set then the server MUST send exactly one CPMSendNotifyOut message to the client and MUST specify the change in the \_watchNotify field.</span></span>
-   <span data-ttu-id="d07fb-4535">Si hubo cambios en el conjunto de resultados de la consulta desde el último mensaje CPMSendNotifyOut, el servidor DEBE responder con CPMSendNotifyOut y DEBE especificar el cambio en el \_ campo watchNotify.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4535">If there were changes to the query result set since the last CPMSendNotifyOut message, the server MUST reply with CPMSendNotifyOut and MUST specify the change in the \_watchNotify field.</span></span> <span data-ttu-id="d07fb-4536">Tenga en cuenta que, en el caso de muchos cambios en los resultados de la consulta, DBWATCHNOTIFY ROWSCHANGED tiene prioridad (es decir, si la consulta se ha realizado, se vuelve a ejecutar y, a continuación, el número de filas ha cambiado y la consulta se ha realizado de nuevo, el evento notificado sería \_ DBWATCHNOTIFY \_ ROWSCHANGED).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4536">Note, that in the case of many changes to query results, DBWATCHNOTIFY\_ROWSCHANGED takes priority (i.e., if the query was done, re-executed and then the number of rows changed and the query was done again then the event reported would be DBWATCHNOTIFY\_ROWSCHANGED).</span></span>

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a><span data-ttu-id="d07fb-4537">3.1.5.2.10 Recibir una solicitud CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4537">3.1.5.2.10 Receiving a CPMGetApproximatePositionIn Request</span></span>

<span data-ttu-id="d07fb-4538">Cuando el servidor recibe una solicitud de mensaje CPMGetApproximatePositionIn del cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4538">When the server receives a CPMGetApproximatePositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4539">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4539">Check if the client has a query associated with it.</span></span> <span data-ttu-id="d07fb-4540">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4540">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="d07fb-4541">Compruebe si el identificador del cursor, el identificador de capítulo y el identificador de marcador pasados están en las listas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4541">Check if the cursor handle, chapter handle and bookmark handle passed are in corresponding lists.</span></span> <span data-ttu-id="d07fb-4542">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4542">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="d07fb-4543">Busque una fila asociada al identificador de marcador en los resultados de la consulta y aproxime la posición de la fila en el conjunto de filas, a la que hace referencia el identificador de capítulo, y determine el numerador y el denominador de la posición.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4543">Find a row which is associated with the bookmark handle in the query results and approximate the position of the row in the rowset, referred to by the chapter handle, and determine the numerator and denominator for the position.</span></span> <span data-ttu-id="d07fb-4544">Tenga en cuenta que cuando el identificador del capítulo es DB \_ NULL HCHAPTER, el capítulo correspondiente es el conjunto de filas \_ principal de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4544">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="d07fb-4545">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar un error.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4545">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="d07fb-4546">Responda al cliente con un mensaje CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4546">Respond to the client with a CPMFetchValueOut message.</span></span>

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a><span data-ttu-id="d07fb-4547">3.1.5.2.11 Recepción de una solicitud CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4547">3.1.5.2.11 Receiving a CPMCompareBmkIn Request</span></span>

<span data-ttu-id="d07fb-4548">Cuando el servidor recibe una solicitud de mensaje CPMCompareBmkIn del cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4548">When the server receives a CPMCompareBmkIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4549">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4549">Check if the client has a query associated with it.</span></span> <span data-ttu-id="d07fb-4550">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4550">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="d07fb-4551">Compruebe si el identificador del cursor, el identificador de capítulo y los identificadores de marcador pasados están en las listas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4551">Check if the cursor handle, chapter handle and bookmark handles passed are in corresponding lists.</span></span> <span data-ttu-id="d07fb-4552">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4552">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="d07fb-4553">Prepare un mensaje CPMCompareBmkOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4553">Prepare a CPMCompareBmkOut message.</span></span>
-   <span data-ttu-id="d07fb-4554">Si los identificadores de marcador son iguales, \_ dwComparison DEBE estar establecido en DBCOMPARE \_ EQ.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4554">If bookmark handles are equal, then \_dwComparison MUST be is set to DBCOMPARE\_EQ.</span></span>
-   <span data-ttu-id="d07fb-4555">De lo contrario, si uno de los identificadores de marcador es DBBMK FIRST o \_ DBBMK \_ LAST, \_ dwComparison DEBE establecerse en DBCOMPARE \_ NE.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4555">Otherwise, if one of bookmarks handles is DBBMK\_FIRST or DBBMK\_LAST then \_dwComparison MUST be set to DBCOMPARE\_NE.</span></span>
-   <span data-ttu-id="d07fb-4556">De lo contrario, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4556">Otherwise the server MUST do the following:</span></span>
-   -   <span data-ttu-id="d07fb-4557">Buscar filas a las que hace referencia cada identificador de marcador en los resultados de la consulta</span><span class="sxs-lookup"><span data-stu-id="d07fb-4557">Find rows which are referred to by each bookmark handle in the query results</span></span>
    -   <span data-ttu-id="d07fb-4558">Si alguna de las filas no está en el capítulo indicado por el identificador del capítulo en CPMCompareBmkIn, dwComparison DEBE establecerse en \_ DBCOMPARE \_ NOTCOMPARABLE.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4558">If any one of the rows is not in the chapter indicated by the chapter handle in CPMCompareBmkIn, then \_dwComparison MUST be set to DBCOMPARE\_NOTCOMPARABLE.</span></span>
    -   <span data-ttu-id="d07fb-4559">De lo contrario, cuando ambas filas están en el mismo capítulo, el servidor DEBE aproximarse a una posición de esas filas en el conjunto de filas al que hace referencia el identificador de este capítulo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4559">Otherwise, when both rows are in the same chapter, then the server MUST approximate a position of those rows in the rowset referred to by this chapter's handle.</span></span> <span data-ttu-id="d07fb-4560">A continuación, DEBE comparar los valores de posición y establecer dwComparison en DBCOMPARE LT si la posición de la primera fila es menor que la posición de la segunda fila; de lo contrario, dwComparison DEBE establecerse en \_ \_ \_ DBCOMPARE \_ GT.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4560">It MUST then compare position values and set\_dwComparison to DBCOMPARE\_LT if position of first row is smaller than position of the second row; otherwise \_dwComparison MUST be set to DBCOMPARE\_GT.</span></span>

-   <span data-ttu-id="d07fb-4561">Responda al cliente con el mensaje CPMCompareBmkOut rellenado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4561">Respond to the client with filled CPMCompareBmkOut message.</span></span>

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a><span data-ttu-id="d07fb-4562">3.1.5.2.12 Recibir una solicitud CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4562">3.1.5.2.12 Receiving a CPMRestartPositionIn Request</span></span>

<span data-ttu-id="d07fb-4563">Cuando el servidor recibe la solicitud de mensaje CPMRestartPositionIn del cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4563">When the server receives the CPMRestartPositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4564">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4564">Check if the client has a query associated with it.</span></span> <span data-ttu-id="d07fb-4565">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4565">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="d07fb-4566">Compruebe si el identificador del cursor y el identificador de capítulo pasados están en las listas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4566">Check if the cursor handle and chapter handle passed are in corresponding lists.</span></span> <span data-ttu-id="d07fb-4567">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4567">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="d07fb-4568">Mueva el cursor al principio del capítulo, identificado por el identificador del capítulo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4568">Move the cursor to the beginning of the chapter, identified by the chapter handle.</span></span> <span data-ttu-id="d07fb-4569">Tenga en cuenta que cuando el identificador de capítulo es DB \_ NULL HCHAPTER, el capítulo correspondiente es el conjunto de filas \_ principal de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4569">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="d07fb-4570">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar un error.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4570">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="d07fb-4571">Responda al cliente con un mensaje CPMRestartPositionIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4571">Respond to the client with a CPMRestartPositionIn message.</span></span>

### <a name="315213-receiving-a-cpmfreecursorin-request"></a><span data-ttu-id="d07fb-4572">3.1.5.2.13 Recibir una solicitud CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4572">3.1.5.2.13 Receiving a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="d07fb-4573">Cuando el servidor recibe una solicitud de mensaje CPMFreeCursorIn del cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4573">When the server receives a CPMFreeCursorIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4574">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4574">Check if the client has a query associated with it.</span></span> <span data-ttu-id="d07fb-4575">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4575">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="d07fb-4576">Compruebe si el identificador de cursor pasado está en la lista de identificadores de cursor del cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4576">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="d07fb-4577">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4577">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="d07fb-4578">Libere el cursor y los recursos asociados (consulte la sección 3.1.1 para obtener una lista completa) para este identificador de cursor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4578">Release the cursor and associated resources (see section 3.1.1 for complete list) for this cursor handle.</span></span>
-   <span data-ttu-id="d07fb-4579">Quite el cursor de la lista de cursores para ese cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4579">Remove the cursor from the list of cursors for that client.</span></span>
-   <span data-ttu-id="d07fb-4580">Responda con un mensaje CPMFreeCursorOut, estableciendo el campo \_ cCursorsRemaining con el número de cursores restantes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4580">Respond with a CPMFreeCursorOut message, setting the \_cCursorsRemaining field with the number of cursors remaining.</span></span> <span data-ttu-id="d07fb-4581">en la lista de este cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4581">in this client's list.</span></span>
-   <span data-ttu-id="d07fb-4582">Si no hay más cursores para este cliente, el servidor DEBE liberar la consulta y los recursos asociados (consulte la sección 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4582">If there are no more cursors for this client, the server MUST release the query and associated resources (see section 3.1.1).</span></span>

### <a name="315214-receiving-a-cpmdisconnect-request"></a><span data-ttu-id="d07fb-4583">3.1.5.2.14 Recepción de una solicitud CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="d07fb-4583">3.1.5.2.14 Receiving a CPMDisconnect Request</span></span>

<span data-ttu-id="d07fb-4584">Cuando el servidor recibe una solicitud de mensaje CPMDisconnect del cliente, el servidor DEBE quitar el cliente de la lista de clientes conectados y liberar todos los recursos asociados al cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4584">When the server receives a CPMDisconnect message request from the client, the server MUST remove the client from the list of connected clients and release all resources associated with the client.</span></span>

### <a name="316-timer-events"></a><span data-ttu-id="d07fb-4585">3.1.6 Eventos de temporizador</span><span class="sxs-lookup"><span data-stu-id="d07fb-4585">3.1.6 Timer Events</span></span>

<span data-ttu-id="d07fb-4586">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4586">None.</span></span>

### <a name="317-other-local-events"></a><span data-ttu-id="d07fb-4587">3.1.7 Otros eventos locales</span><span class="sxs-lookup"><span data-stu-id="d07fb-4587">3.1.7 Other Local Events</span></span>

<span data-ttu-id="d07fb-4588">Cuando se detiene el servidor, debe pasar primero al estado de "apagado".</span><span class="sxs-lookup"><span data-stu-id="d07fb-4588">When the server is stopped, it MUST first transition to the "shutting down" state.</span></span> <span data-ttu-id="d07fb-4589">A continuación, DEBE dejar de escuchar la canalización, realizar cualquier otra tarea de apagado específica de la implementación y, a continuación, realizar la transición al estado "detenido".</span><span class="sxs-lookup"><span data-stu-id="d07fb-4589">It MUST then stop listening to the pipe, perform any other implementation-specific shutdown tasks, and then transition into the "stopped" state.</span></span>

### <a name="32-client-details"></a><span data-ttu-id="d07fb-4590">3.2 Detalles del cliente</span><span class="sxs-lookup"><span data-stu-id="d07fb-4590">3.2 Client Details</span></span>

### <a name="321-abstract-data-model"></a><span data-ttu-id="d07fb-4591">3.2.1 Modelo de datos abstractos</span><span class="sxs-lookup"><span data-stu-id="d07fb-4591">3.2.1 Abstract Data Model</span></span>

<span data-ttu-id="d07fb-4592">En la sección siguiente se especifican los datos y el estado que mantiene el cliente del protocolo content indexing Service.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4592">The following section specifies data and state maintained by the Content Indexing Service Protocol client.</span></span> <span data-ttu-id="d07fb-4593">Los datos proporcionados son para facilitar la explicación de cómo se comporta el protocolo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4593">The provided data is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="d07fb-4594">Esta sección no exige que las implementaciones cumplan este modelo siempre y cuando su comportamiento externo sea coherente con el descrito en este documento.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4594">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="d07fb-4595">Un cliente tiene el siguiente estado abstracto:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4595">A client has the following abstract state:</span></span>

-   <span data-ttu-id="d07fb-4596">**Último mensaje enviado:** copia del último mensaje enviado al servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4596">**Last Message Sent**: A copy of the last message sent to the server.</span></span>
-   <span data-ttu-id="d07fb-4597">**Valor de propiedad actual:** valor parcial de una propiedad "diferida", que está en proceso de recuperación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4597">**Current Property Value**: A partial value of a "deferred" property, which is in the process of being retrieved.</span></span>
-   <span data-ttu-id="d07fb-4598">**Bytes actuales recibidos:** el número de bytes recibidos para el valor de propiedad actual hasta ahora.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4598">**Current Bytes Received**: The number of bytes received for Current Property Value so far.</span></span>
-   <span data-ttu-id="d07fb-4599">**Estado de conexión de canalización con nombre:** una conexión al servidor</span><span class="sxs-lookup"><span data-stu-id="d07fb-4599">**Named pipe connection state**: A connection to the server</span></span>

### <a name="322-timers"></a><span data-ttu-id="d07fb-4600">3.2.2 Temporizadores</span><span class="sxs-lookup"><span data-stu-id="d07fb-4600">3.2.2 Timers</span></span>

<span data-ttu-id="d07fb-4601">No se requiere ningún temporizador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4601">No protocol timers are required.</span></span>

### <a name="323-initialization"></a><span data-ttu-id="d07fb-4602">3.2.3 Inicialización</span><span class="sxs-lookup"><span data-stu-id="d07fb-4602">3.2.3 Initialization</span></span>

<span data-ttu-id="d07fb-4603">No se realizarán acciones hasta que se reciba una solicitud de capa superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4603">No actions are taken until a higher layer request is received.</span></span>

### <a name="324-higher-layer-triggered-events"></a><span data-ttu-id="d07fb-4604">3.2.4 eventos Higher-Layer desencadenados</span><span class="sxs-lookup"><span data-stu-id="d07fb-4604">3.2.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="d07fb-4605">Cuando se recibe una solicitud de una capa superior, el cliente DEBE crear una conexión de canalización con nombre al servidor con los detalles especificados en la sección 2.1.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4605">When a request is received from a higher layer, the client MUST create a named pipe connection to the server, using the details specified in Section 2.1.</span></span> <span data-ttu-id="d07fb-4606">Si no puede hacerlo, se DEBE dar error a la solicitud de capa superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4606">If it is unable to do so, the higher layer request MUST be failed.</span></span> <span data-ttu-id="d07fb-4607">Es decir, en caso de error de conexión, es responsabilidad del nivel superior reintentar si lo desea.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4607">That is, in case of a failure to connect, it is the responsibility of the higher level to retry if desired.</span></span>

<span data-ttu-id="d07fb-4608">Un encabezado DEBE incluirse previamente con campos establecidos como se especifica en la sección 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4608">A header MUST be pre-pended with fields set as specified in section 2.2.2.</span></span>

<span data-ttu-id="d07fb-4609">Para los mensajes que se especifican como que requieren una suma de comprobación distinta de cero, el \_ valor ulChecksum DEBE calcularse de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4609">For messages that are specified as requiring a nonzero checksum, the \_ulChecksum value MUST be calculated as follows:</span></span>

1.  <span data-ttu-id="d07fb-4610">El contenido del mensaje después del campo ulReserved2 en el encabezado del mensaje DEBE interpretarse como una secuencia de enteros de \_ 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4610">The contents of the message after the \_ulReserved2 field in the message header MUST be interpreted as a sequence of 32 bit integers.</span></span> <span data-ttu-id="d07fb-4611">El cliente DEBE calcular la suma de los valores numéricos especificados por estos enteros.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4611">The client MUST calculate the sum of the numeric values given by these integers.</span></span>
2.  <span data-ttu-id="d07fb-4612">Calcule el XOR bit a bit de este valor con 0x59533959.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4612">Calculate the bitwise XOR of this value with 0x59533959.</span></span>
3.  <span data-ttu-id="d07fb-4613">Resta el valor especificado por \_ msg del valor que resulta del XOR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4613">Subtract the value given by \_msg from the value that results from the bitwise XOR.</span></span>

### <a name="3241-remote-indexing-service-catalog-management"></a><span data-ttu-id="d07fb-4614">3.2.4.1 Remote Indexing Service Catalog Management</span><span class="sxs-lookup"><span data-stu-id="d07fb-4614">3.2.4.1 Remote Indexing Service Catalog Management</span></span>

<span data-ttu-id="d07fb-4615">Cada mensaje se desencadena mediante una solicitud de la capa superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4615">Each message is triggered by a request from the higher layer.</span></span> <span data-ttu-id="d07fb-4616">No hay ninguna secuencia de mensajes aplicada por el cliente para las solicitudes de mensajes CISP para administrar catálogos de forma remota, pero (a excepción de un mensaje CPMSetCatStateIn), el servidor solo responderá correctamente si el cliente se conectó previamente mediante un mensaje CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4616">There is no message sequence enforced by the client for CISP message requests for remotely managing catalogs, but (with the exception of a CPMSetCatStateIn message) the server will only reply with success if the client previously connected by means of a CPMConnectIn message.</span></span>

### <a name="32411-sending-a-cpmcistateinout-request"></a><span data-ttu-id="d07fb-4617">3.2.4.1.1 Envío de una solicitud CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-4617">3.2.4.1.1 Sending a CPMCiStateInOut Request</span></span>

<span data-ttu-id="d07fb-4618">Normalmente, la capa superior pide al cliente de protocolo que envíe un mensaje CPMCiStateInOut cuando requiera información sobre los servicios de indexación en el servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4618">Typically, the higher layer asks the protocol client to send a CPMCiStateInOut message when it requires information about indexing services on the server.</span></span>

<span data-ttu-id="d07fb-4619">Cuando se le solicite que envíe este mensaje, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4619">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4620">Envíe un mensaje CPMCiStateInOut como se especifica en la sección 2.2.3.1 al servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4620">Send a CPMCiStateInOut message as specified in section 2.2.3.1 to the server.</span></span>
-   <span data-ttu-id="d07fb-4621">Espere a recibir el mensaje CPMCiStateInOut del servidor, descartando de forma silenciosa todos los demás mensajes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4621">Wait to receive CPMCiStateInOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="d07fb-4622">Informe del valor del campo de estado de la respuesta y, si se ha realizado correctamente, la estructura de información vuelve \_ a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4622">Report the value of the \_status field of the response and, if it was successful, the informational structure back to the higher layer.</span></span>

### <a name="32412-sending-a-cpmsetcatstatein-request"></a><span data-ttu-id="d07fb-4623">3.2.4.1.2 Envío de una solicitud CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4623">3.2.4.1.2 Sending a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="d07fb-4624">Normalmente, la capa superior solicita al cliente de protocolo que envíe un mensaje CPMSetCatStateIn cuando requiera información sobre un catálogo o todo el catálogo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4624">Typically, the higher layer asks the protocol client to send a CPMSetCatStateIn message when it requires information about a catalog or all catalog.</span></span> <span data-ttu-id="d07fb-4625">Para este mensaje, la capa superior debe proporcionar al cliente de protocolo un valor para dwNewState y, si es necesario, el \_ nombre del catálogo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4625">For this message the higher layer needs to provide the protocol client with a value for \_dwNewState and, if required, the name of the catalog.</span></span>

<span data-ttu-id="d07fb-4626">Cuando se le solicite que envíe este mensaje, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4626">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4627">Envíe un mensaje CPMSetCatStateIn como se especifica en 2.2.3.2 al servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4627">Send a CPMSetCatStateIn message as specified in 2.2.3.2 to the server.</span></span>
-   <span data-ttu-id="d07fb-4628">Espere a recibir un mensaje CPMSetCatStateOut del servidor, descartando de forma silenciosa todos los demás mensajes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4628">Wait to receive a CPMSetCatStateOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="d07fb-4629">Informe del valor del campo de estado de la respuesta y, si se ha realizado \_ correctamente, \_ dwOldState de vuelta a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4629">Report the value of the \_status field of the response and, if it was successful, the \_dwOldState back to the higher layer.</span></span>

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="d07fb-4630">3.2.4.1.3 Envío de una solicitud CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4630">3.2.4.1.3 Sending a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="d07fb-4631">La capa superior normalmente solicita que envíe este mensaje cuando necesite actualizar documentos en la ruta de acceso existente o agregar una nueva ruta de acceso de archivo al índice.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4631">The higher layer typically asks to send this message when it needs to either update documents in existing path or add a new file path to the index.</span></span> <span data-ttu-id="d07fb-4632">Por lo tanto, la capa superior es proporcionar la ruta de acceso y el tipo de un examen, que se especifica como en la sección 2.2.3.4, donde una actualización incremental o completa está pensada para las rutas de acceso existentes, y la nueva inicialización está pensada para nuevas rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4632">Thus the higher layer is to provide the path and type of a scan, which is specified as in section 2.2.3.4 where an incremental or full update is meant for existing paths, and new initialization is meant for new paths.</span></span>

<span data-ttu-id="d07fb-4633">Para atender la solicitud de capa superior, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4633">In order to serve the higher layer request, the client MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4634">Envíe un mensaje CPMUpdateDocumentsIn como se especifica en la sección 2.2.3.4 al servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4634">Send a CPMUpdateDocumentsIn message as specified in section 2.2.3.4 to the server.</span></span>
-   <span data-ttu-id="d07fb-4635">Espere a recibir el mensaje CPMUpdateDocumentsIn del servidor, descartando de forma silenciosa todos los demás mensajes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4635">Wait to receive CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="d07fb-4636">Informe el valor del campo \_ de estado de la respuesta a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4636">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="32414-sending-a-cpmforcemergein-request"></a><span data-ttu-id="d07fb-4637">3.2.4.1.4 Envío de una solicitud CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4637">3.2.4.1.4 Sending a CPMForceMergeIn Request</span></span>

<span data-ttu-id="d07fb-4638">Normalmente, la capa superior solicita enviar este mensaje cuando es necesario mejorar el rendimiento de las consultas o forma parte del mantenimiento programado del servicio de indexación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4638">Typically, the higher layer requests to send this message when there is a need to improve query performance, or it's a part of scheduled indexing service maintenance.</span></span>

<span data-ttu-id="d07fb-4639">Para atender la capa superior, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4639">In order to serve the higher layer the client MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4640">Envíe el mensaje CPMForceMergeIn tal como se especifica en la sección 2.2.3.5 al servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4640">Send CPMForceMergeIn message as specified by section 2.2.3.5 to the server.</span></span>
-   <span data-ttu-id="d07fb-4641">Espere a recibir un mensaje CPMUpdateDocumentsIn del servidor, descartando de forma silenciosa todos los demás mensajes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4641">Wait to receive a CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="d07fb-4642">Informe del valor del campo \_ de estado de la respuesta a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4642">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="3242-remote-indexing-service-catalog-query-messages"></a><span data-ttu-id="d07fb-4643">3.2.4.2 Mensajes de consulta del catálogo del servicio de indexación remota</span><span class="sxs-lookup"><span data-stu-id="d07fb-4643">3.2.4.2 Remote Indexing Service Catalog Query Messages</span></span>

<span data-ttu-id="d07fb-4644">A excepción de CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, hay una relación uno a uno entre los mensajes CISP y las solicitudes de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4644">With the exception of CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, there is a one-to-one relationship between CISP messages and higher layer requests.</span></span> <span data-ttu-id="d07fb-4645">Para las dos excepciones mencionadas anteriormente, puede haber varios mensajes generados por el cliente para satisfacer los requisitos de tamaño o para recuperar una propiedad completa.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4645">For the two exceptions mentioned above, there can be multiple messages generated by the client to either satisfy size requirements, or to retrieve a complete property.</span></span> <span data-ttu-id="d07fb-4646">La capa superior suele realizar un seguimiento de toda la información específica de la consulta (por ejemplo, los identificadores de cursor abiertos, los valores legales para los identificadores de marcador y capítulo, los valores de wid para los valores de propiedad diferidos, etc.) y también realiza un seguimiento de si el cliente está en un estado conectado, pero el cliente no lo aplica de ninguna manera.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4646">The higher layer typically keeps track of all query-specific information (such as cursor handles opened, legal values for bookmark and chapter handles, wid values for deferred property values, etc.) and also tracks if the client is in a connected state, but this is not enforced in any way by the client.</span></span>

<span data-ttu-id="d07fb-4647">Con fines ilustrativos, la parte del cliente del diagrama de la sección 3 ilustra esta secuencia para una consulta sencilla de Indexing Service.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4647">For illustrative purposes the client portion of the diagram in Section 3 illustrates this sequence for a simple Indexing Service query.</span></span>

### <a name="32421-sending-a-cpmconnectin-request"></a><span data-ttu-id="d07fb-4648">3.2.4.2.1 Envío de una solicitud CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4648">3.2.4.2.1 Sending a CPMConnectIn Request</span></span>

<span data-ttu-id="d07fb-4649">Este mensaje suele ser la primera solicitud de la capa superior (como si el cliente no está conectado, el servidor producirá un error en la mayoría de los mensajes con la excepción de CPMSetCatStateIn).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4649">This message is typically the very first request from the higher layer (as if the client is not connected, the server will fail most of the messages with exception of CPMSetCatStateIn).</span></span> <span data-ttu-id="d07fb-4650">El nivel superior proporciona al cliente de protocolo la información necesaria para conectarse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4650">The higher level provides the protocol client with information necessary to connect.</span></span>

<span data-ttu-id="d07fb-4651">Para atender la capa superior, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4651">In order to serve the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4652">Rellene el mensaje con la información proporcionada por el cliente de capa superior (consulte la sección 2.2.3.6) en \_ iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 y aPropertySet.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4652">Fill in the message, using information which the higher layer client provided (see section 2.2.3.6) in \_iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 and aPropertySet.</span></span>
-   <span data-ttu-id="d07fb-4653">Establezca \_ fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet y cExtPropSet como se especifica en 2.2.3.6.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4653">Set \_fClientIsRemote, \_cbBlob, \_cbBlob2, cPropSet and cExtPropSet as specified in 2.2.3.6.</span></span>
-   <span data-ttu-id="d07fb-4654">Establezca la suma de comprobación en \_ el campo ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4654">Set the checksum in the \_ulChecksum field.</span></span>
-   <span data-ttu-id="d07fb-4655">Envíe el mensaje CPMConnectIn al servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4655">Send the CPMConnectIn message to the server.</span></span>
-   <span data-ttu-id="d07fb-4656">Espere a recibir un mensaje CPMConnectOut del servidor, descartando silenciosamente todos los demás mensajes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4656">Wait to receive a CPMConnectOut message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="d07fb-4657">Informe del valor del campo de estado de la respuesta y, si se ha realizado correctamente, serverVersion vuelve \_ a la capa \_ superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4657">Report the value of the \_status field of the response and, if it was successful, the \_serverVersion back to the higher layer.</span></span>

<span data-ttu-id="d07fb-4658">Para fines informativos, se espera que las capas superiores realicen normalmente las siguientes acciones tras una conexión correcta, pero el cliente CISP no las aplica:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4658">For informative purposes, it is expected that higher layers will typically do the following actions upon successful connection, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="d07fb-4659">Uso de mensajes de administración remota del catálogo de servicios de indexación para tareas administrativas</span><span class="sxs-lookup"><span data-stu-id="d07fb-4659">Use remote indexing service catalog management messages for administrative tasks</span></span>
-   <span data-ttu-id="d07fb-4660">Use una solicitud CPMCreateQueryIn para crear una consulta de búsqueda con el fin de recuperar los resultados del catálogo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4660">Use a CPMCreateQueryIn request to create a search query with a purpose of retrieving results from the catalog.</span></span>

### <a name="32422-sending-a-cpmcreatequeryin-request"></a><span data-ttu-id="d07fb-4661">3.2.4.2.2 Envío de una solicitud CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4661">3.2.4.2.2 Sending a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="d07fb-4662">La capa superior normalmente proporcionará información para la creación de consultas una vez conectado el cliente de protocolo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4662">The higher layer will typically provide information for the query creation once the protocol client is connected.</span></span> <span data-ttu-id="d07fb-4663">La capa superior proporciona al cliente un conjunto de restricciones, un conjunto de columnas, reglas de criterio de ordenación y un conjunto de categorización (cada uno de ellos se puede omitir), propiedades de conjunto de filas y estructura del asignador de identificadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4663">The higher layer provides the client with a restrictions set, columns set, sort order rules and categorization set (each of them can be omitted), rowset properties and property ID mapper structure.</span></span>

<span data-ttu-id="d07fb-4664">Cuando esta solicitud se recibe de una capa superior, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4664">When this request is received from a higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4665">Prepare CPMCreateQueryOut como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4665">Prepare a CPMCreateQueryOut as follows.</span></span>
-   -   <span data-ttu-id="d07fb-4666">Si hay un conjunto de columnas, establezca CColumnsSetPreset en 0x01 y rellene el campo ColumnsSet.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4666">If a columns set is present then set CColumnsSetPreset to 0x01 and fill the ColumnsSet field.</span></span>
    -   <span data-ttu-id="d07fb-4667">Si existen restricciones, establezca CRestrictionPresent en 0x01 y rellene el campo Restricción.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4667">If restrictions are present, set CRestrictionPresent to 0x01 and fill the Restriction field.</span></span>
    -   <span data-ttu-id="d07fb-4668">Si hay un conjunto de ordenación, rellene el campo SortSet.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4668">If a sort set is present, fill the SortSet field.</span></span>
    -   <span data-ttu-id="d07fb-4669">Si hay un conjunto de categorización, establezca CSortSetPresent en 0x01 y rellene el campo CategorizationSet.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4669">If a categorization set is present, set CSortSetPresent to 0x01 and fill the CategorizationSet field.</span></span>
    -   <span data-ttu-id="d07fb-4670">Establezca el resto de campos como se especifica en 2.2.3.8.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4670">Set the rest of fields as specified in 2.2.3.8</span></span>

-   <span data-ttu-id="d07fb-4671">Calcule \_ el campo ulCheckSum en el encabezado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4671">Calculate \_ulCheckSum field in the header.</span></span>
-   <span data-ttu-id="d07fb-4672">Envíe el mensaje CPMCreateQueryIn al servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4672">Send the CPMCreateQueryIn message to the server.</span></span>
-   <span data-ttu-id="d07fb-4673">Espere a recibir el mensaje CPMCreateQueryOut (consulte los detalles de la sección 3.2.5.1.1), descartando en modo silencioso todos los demás mensajes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4673">Wait to receive CPMCreateQueryOut message (see details in section 3.2.5.1.1), silently discarding all other messages.</span></span>
-   <span data-ttu-id="d07fb-4674">Informe del valor del campo de estado de la respuesta y, si se ha realizado correctamente, la matriz de identificadores de cursor y los valores booleanos informativos (como se especifica en \_ 2.2.3.9) de vuelta a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4674">Report the value of the \_status field of the response and, if it was successful, the array of cursor handles, and informative Boolean values (as specified in 2.2.3.9) back to the higher layer.</span></span>

### <a name="32423-sending-a-cpmsetbindingsin-request"></a><span data-ttu-id="d07fb-4675">3.2.4.2.3 Envío de una solicitud CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4675">3.2.4.2.3 Sending a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="d07fb-4676">Normalmente, la capa superior establecerá enlaces para cada columna que se devolverá en las filas cuando ya tenga un identificador de cursor válido (después de recibir correctamente CPMCreateQueryOut, vea la sección 3.2.5.1.1).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4676">Typically, the higher layer will set bindings for each column to be returned in the rows when it already has valid cursor handle (after successfully receiving CPMCreateQueryOut, see section 3.2.5.1.1).</span></span> <span data-ttu-id="d07fb-4677">Se espera que el valor superior proporcione una matriz de estructuras CTableColumn, como se especifica en la sección 2.2.4.31, para el campo aColumns y un identificador de cursor válido.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4677">The higher is expected to provide an array of CTableColumn structures, as specified in Section 2.2.4.31, for the aColumns field and a valid cursor handle.</span></span>

<span data-ttu-id="d07fb-4678">Cuando esta solicitud se recibe de la capa superior, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4678">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4679">Calcule el número de estructuras CTableColumn de la matriz aColumns y establezca el campo cColumns en este valor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4679">Calculate the number of CTableColumn structures in the aColumns array, and set the cColumns field to this value.</span></span>
-   <span data-ttu-id="d07fb-4680">Calcule el tamaño total en bytes de los campos cColumns y aColumns y establezca el \_ campo cbBindingDesc en este valor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4680">Calculate the total size in bytes of the cColumns and aColumns fields, and set the \_cbBindingDesc field to this value.</span></span>
-   <span data-ttu-id="d07fb-4681">Establezca los campos especificados en el mensaje CPMSetBindingsIn en los valores proporcionados por la capa de aplicación superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4681">Set specified fields in CPMSetBindingsIn message to the values provided by the higher application layer.</span></span> <span data-ttu-id="d07fb-4682">Establezca el \_ campo ulChecksum en el valor calculado como se especifica en la sección 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4682">Set the \_ulChecksum field to the value calculated as specified in Section 3.2.5.</span></span>
-   <span data-ttu-id="d07fb-4683">Envíe el mensaje CPMSetBindignsIn completado al servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4683">Send the completed CPMSetBindignsIn message to the server.</span></span>
-   <span data-ttu-id="d07fb-4684">Espere a recibir un mensaje CPMSetBindingsIn del servidor, descartando otros mensajes.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4684">Wait to receive a CPMSetBindingsIn message from server, discarding other messages.</span></span>
-   <span data-ttu-id="d07fb-4685">Indique el estado del \_ campo de estado de la respuesta a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4685">Indicate the status from \_status field of the response to the higher layer.</span></span>

<span data-ttu-id="d07fb-4686">Con fines informativos, se espera que las capas superiores soliciten normalmente a un cliente que envíe un mensaje CPMGetRowsIn, pero el Protocolo de servicio de indexación de contenido no lo exige.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4686">For informative purposes, it is expected that higher layers will typically request a client to send a CPMGetRowsIn message, but this is not enforced by the Content Indexing Service Protocol.</span></span>

### <a name="32424-sending-a-cpmgetrowsin-request"></a><span data-ttu-id="d07fb-4687">3.2.4.2.4 Envío de una solicitud CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4687">3.2.4.2.4 Sending a CPMGetRowsIn Request</span></span>

<span data-ttu-id="d07fb-4688">Cuando la capa superior está a punto de recibir información de filas, proporcionará al cliente de protocolo un identificador de cursor y capítulo válido y proporcionará la descripción de la búsqueda adecuada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4688">When the higher layer is about to receive rows information it will provide protocol client with valid cursor and chapter handle and give appropriate seek description.</span></span> <span data-ttu-id="d07fb-4689">Normalmente, se espera que una capa superior lo haga cuando tenga un identificador de cursor o capítulo válido y los enlaces se hayan establecido con el mensaje CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4689">Typically, a higher layer is expected to do so when it has a valid cursor and/or chapter handle, and the bindings had been set with CPMSetBindingsIn message.</span></span> <span data-ttu-id="d07fb-4690">Para acceder al conjunto de filas de un capítulo, la capa superior es usar el identificador de capítulo recibido del servidor en un mensaje CPMGetRowsOut anterior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4690">To access the rowset in a chapter, the higher layer is to use chapter handle received from the server in a previous CPMGetRowsOut message.</span></span>

<span data-ttu-id="d07fb-4691">Cuando se recibe esta solicitud de la capa superior, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4691">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4692">Determine qué valor entero sin signo se va a especificar para el \_ campo cbReadBuffer.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4692">Determine what unsigned integer value to specify for the \_cbReadBuffer field.</span></span> <span data-ttu-id="d07fb-4693">Para determinar este valor, el cliente DEBE tomar el valor máximo de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4693">To determine this value, the client MUST take the maximum value from the following:</span></span>
-   -   <span data-ttu-id="d07fb-4694">Mil veces el valor del campo \_ RowsToTransfer de c.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4694">One thousand times the value of the c\_RowsToTransfer field.</span></span>
    -   <span data-ttu-id="d07fb-4695">Valor de cbRowWidth, redondeado al múltiplo \_ de 512 bytes más cercano.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4695">Value of \_cbRowWidth, rounded up to the nearest 512 byte multiple.</span></span>
    -   <span data-ttu-id="d07fb-4696">Tome el valor más alto de estos dos valores, hasta el límite de 16 000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4696">Take the higher of these two values, up to the 16K limit.</span></span>
    -   <span data-ttu-id="d07fb-4697">En los casos en los que una sola fila es mayor que 16 000, el servidor no puede devolver resultados a esta consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4697">In cases where a single row is larger than 16K, the server cannot return results to this query.</span></span>

<span data-ttu-id="d07fb-4698">Especifique una base de cliente para los datos de fila de tamaño variable en el espacio de direcciones del cliente \_ en el campo ulClientBase.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4698">Specify a client base for variable-sized row data in client address space in \_ulClientBase field.</span></span>

<span data-ttu-id="d07fb-4699">*Comportamiento de Windows: para un cliente de 32 bits que habla con un servidor de 32 bits o un cliente de 64 bits que habla con un servidor de 64 bits, este valor se establece en una dirección de memoria del búfer receptor en el proceso de aplicación. Esto permite que los punteros recibidos en el campo Filas de CPMGetRowsOut sean punteros de memoria correctos en un proceso de aplicación cliente. De lo contrario, se establece en 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="d07fb-4699">*Windows Behavior: For a 32-bit client talking to a 32-bit server, or a 64 bit client talking to a 64-bit server this value is set to a memory address of the receiving buffer in application process. This allows for pointers, received in Rows field of CPMGetRowsOut to be correct memory pointers in a client application process. Otherwise it is set to 0x00000000.*</span></span>

-   <span data-ttu-id="d07fb-4700">Calcule el tamaño de la descripción de la búsqueda y estapóla en el \_ campo cbSeek.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4700">Calculate the size of seek description and set it in the \_cbSeek field.</span></span>
-   <span data-ttu-id="d07fb-4701">Establezca el valor de cbReserved (que actuaría como desplazamiento para El inicio de filas) en el valor \_ de cbSeek más 0x14.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4701">Set the value of cbReserved (which would act as an offset for Rows start) to the value of \_cbSeek plus 0x14.</span></span>
-   <span data-ttu-id="d07fb-4702">Envíe un mensaje de CPMConnectIn como se especifica en 2.2.3.15 al servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4702">Send a CPMConnectIn message as specified in 2.2.3.15 to the server.</span></span>

### <a name="32425-sending-a-cpmfetchvaluein-request"></a><span data-ttu-id="d07fb-4703">3.2.4.2.5 Envío de una solicitud CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4703">3.2.4.2.5 Sending a CPMFetchValueIn Request</span></span>

<span data-ttu-id="d07fb-4704">Si el cliente recibe una respuesta CPMGetRowsOut del servidor con el campo Status de la columna establecido en StatusDeferred (0x01), significa que el valor de propiedad no se incluyó en el campo Rows del mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4704">If the client receives a CPMGetRowsOut response from the server with the column's Status field set to StatusDeferred (0x01) it means that the property value was not included in the Rows field of the CPMGetRowsOut message.</span></span> <span data-ttu-id="d07fb-4705">En este caso, la capa superior normalmente solicita al cliente de protocolo que recupere el valor por medio del mensaje CPMFetchValueIn y proporciona el valor PropSpec y wid para una propiedad diferida, que el cliente de protocolo DEBE usar en el primer mensaje \_ CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4705">In this case the higher layer typically asks the protocol client to retrieve the value by means of CPMFetchValueIn message, and provides the PropSpec and \_wid value for a deferred property, which the protocol client MUST use in the first CPMFetchValueIn message.</span></span>

<span data-ttu-id="d07fb-4706">Si este es el primer mensaje CPMFetchValueIn que el cliente ha enviado para solicitar la propiedad especificada, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4706">If this is the first CPMFetchValueIn message the client has sent to request the specified property, the client MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4707">Establezca todos los campos de un mensaje como se especifica en la sección 2.2.3.19.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4707">Set all the fields in a message as specified in section 2.2.3.19.</span></span>
-   <span data-ttu-id="d07fb-4708">Establezca \_ cbSoFar en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4708">Set \_cbSoFar to 0x00000000.</span></span>
-   <span data-ttu-id="d07fb-4709">Establezca Bytes actuales recibidos en 0.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4709">Set Current Bytes Received to 0.</span></span>
-   <span data-ttu-id="d07fb-4710">Envíe el mensaje CPMFetchValueIn al servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4710">Send the CPMFetchValueIn message to the server.</span></span>

### <a name="32426-sending-a-cpmfreecursorin-request"></a><span data-ttu-id="d07fb-4711">3.2.4.2.6 Envío de una solicitud CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="d07fb-4711">3.2.4.2.6 Sending a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="d07fb-4712">Una vez que el nivel superior ya no usa la consulta de búsqueda, puede liberar los recursos en el servidor solicitando al cliente que envíe un mensaje CPMFreeCursorIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4712">Once the higher level is no longer using the search query, it can release the resources on the server by asking the client to send a CPMFreeCursorIn message.</span></span>

<span data-ttu-id="d07fb-4713">Cuando se recibe esta solicitud, el cliente DEBE enviar un mensaje CPMFreeCursorIn como se especifica en 2.2.3.28 al servidor, que contiene el identificador especificado por la capa superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4713">When this request is received, the client MUST send a CPMFreeCursorIn message as specified in 2.2.3.28 to the server, containing the handle specified by the upper layer.</span></span>

### <a name="32427-sending-a-cpmdisconnect-message"></a><span data-ttu-id="d07fb-4714">3.2.4.2.7 Envío de un mensaje CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="d07fb-4714">3.2.4.2.7 Sending a CPMDisconnect Message</span></span>

<span data-ttu-id="d07fb-4715">Si la capa superior no tiene más consultas para el servicio de indexación, para liberar más recursos de servidor, la aplicación puede solicitar que el cliente envíe un mensaje CPMDisconnect al servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4715">If the higher layer has no more queries for the indexing service, to free up more server resources, the application may request that the client send a CPMDisconnect message to the server.</span></span> <span data-ttu-id="d07fb-4716">Cuando se recibe esta consulta, el cliente DEBE enviar simplemente el mensaje como se solicitó.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4716">When this query is received, the client MUST simply send the message as requested.</span></span> <span data-ttu-id="d07fb-4717">No hay ninguna respuesta a este mensaje desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4717">There is no response to this message from the server.</span></span>

### <a name="325-message-processing-and-sequencing-rules"></a><span data-ttu-id="d07fb-4718">3.2.5 Reglas de procesamiento y secuenciación de mensajes</span><span class="sxs-lookup"><span data-stu-id="d07fb-4718">3.2.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="d07fb-4719">Cuando el cliente recibe una respuesta de mensaje del servidor, el cliente DEBE usar el último mensaje enviado para determinar si el mensaje recibido del servidor es el esperado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4719">When the client receives a message response from the server, the client MUST use the Last Sent Message to determine if the message received from the server is the one expected by the client.</span></span> <span data-ttu-id="d07fb-4720">Todos los mensajes \_ con el campo msg distinto del de Last Send Message DEBEN omitirse.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4720">All messages with \_msg field different from the one in Last Send Message MUST be ignored.</span></span>

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a><span data-ttu-id="d07fb-4721">3.2.5.1 Recibir una respuesta CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-4721">3.2.5.1 Receiving a CPMCreateQueryOut Response</span></span>

<span data-ttu-id="d07fb-4722">Cuando el cliente recibe una respuesta de mensaje CPMCreateQueryOut del servidor, el cliente DEBE devolver el estado y (si el estado es correcto) controlar los valores del cursor a una \_ capa superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4722">When the client receives a CPMCreateQueryOut message response from the server, the client MUST return \_status and (if the status is successful) cursor handle values back to higher layer.</span></span> <span data-ttu-id="d07fb-4723">Las acciones adicionales están hasta la capa superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4723">Any further actions are up to the higher layer.</span></span>

<span data-ttu-id="d07fb-4724">Como la capa superior es consciente de la estructura de consulta, siempre esperará que se devuelva el número correcto de identificadores de cursor en el mensaje CPMCreateOueryOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4724">As the higher layer is aware of query structure it will always expect correct number of cursor handles to be returned in the CPMCreateOueryOut message.</span></span> <span data-ttu-id="d07fb-4725">Los identificadores de cursor se devuelven en el orden siguiente: el primer identificador es para el conjunto de filas sin cadena, el segundo es para el primer conjunto de filas con capítulos (que es la agrupación de resultados en función de la primera categoría especificada en el campo CategorizationSet del mensaje CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4725">The cursor handles are returned in the following order: the first handle is to the unchaptered rowset, the second is to the first chaptered rowset (which is the grouping of results based on the first category specified in the CategorizationSet field of the CPMCreateQueryIn message.)</span></span>

<span data-ttu-id="d07fb-4726">Con fines informativos, se espera que las capas superiores puedan realizar las siguientes acciones, pero el cliente CISP no las aplica:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4726">For informative purposes, it is expected that higher layers can do the following actions, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="d07fb-4727">Use CPMSetBindingsIn para establecer enlaces para columnas individuales y realizar las acciones posteriores en la ruta de acceso de consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4727">Use CPMSetBindingsIn, to set bindings for individual columns and do any subsequent actions on query path</span></span>
-   <span data-ttu-id="d07fb-4728">Use CPMGetQueryStatusIn para comprobar el progreso de ejecución de una consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4728">Use CPMGetQueryStatusIn, to check on the execution progress of a query.</span></span>
-   <span data-ttu-id="d07fb-4729">Use CPMRatioFinishedIn para solicitar el porcentaje de finalización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4729">Use CPMRatioFinishedIn, to request the completion percentage of the query.</span></span>

### <a name="3252-receiving-a-cpmgetrowsout-response"></a><span data-ttu-id="d07fb-4730">3.2.5.2 Recepción de una respuesta CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-4730">3.2.5.2 Receiving a CPMGetRowsOut Response</span></span>

<span data-ttu-id="d07fb-4731">Cuando el cliente recibe una respuesta de mensaje CPMGetRowsOut del servidor, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4731">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4732">Compruebe si el \_ campo de estado del encabezado indica que se ha hecho correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4732">Check if the \_status field in the header indicates success or failure.</span></span>
-   <span data-ttu-id="d07fb-4733">Si el \_ valor de estado es BÚFER DE ESTADO DEMASIADO PEQUEÑO (0xC0000023), el cliente \_ DEBE comprobar el estado Último mensaje \_ \_ enviado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4733">If the \_status value is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), the client MUST check the Last Message Sent state.</span></span> <span data-ttu-id="d07fb-4734">Si no contiene un mensaje CPMGetRowsIn, el mensaje recibido DEBE omitirse en modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4734">If it does not contain a CPMGetRowsIn message, the received message MUST be silently ignored.</span></span> <span data-ttu-id="d07fb-4735">De lo contrario, el cliente DEBE enviar al servidor un nuevo mensaje CPMGetRowsIn con todos los campos idénticos al almacenado, excepto que cbReadBuffer DEBE aumentar en \_ 512 (pero no mayor que 0x4000).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4735">Otherwise, the client MUST send to the server a new CPMGetRowsIn message with all fields identical to the stored one, except that the \_cbReadBuffer MUST be increased by 512 (but not greater than 0x4000).</span></span> <span data-ttu-id="d07fb-4736">Si el estado es STATUS BUFFER TOO SMALL (0xC0000023) y El último mensaje enviado ya tiene \_ \_ cbReadBuffer igual 0x4000 el cliente DEBE notificar el error hasta el \_ \_ nivel \_ superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4736">If \_status is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), and Last Message Sent already has \_cbReadBuffer equal to 0x4000 client MUST report the error up to the higher level.</span></span>
-   <span data-ttu-id="d07fb-4737">Si el \_ valor de estado es cualquier otro valor de error, el cliente DEBE indicar el error hasta la capa superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4737">If the \_status value is any other error value, the client MUST indicate the failure up to the higher layer.</span></span>
-   <span data-ttu-id="d07fb-4738">Si el valor de estado indica correcto, los resultados DEBEN indicarse hasta la capa superior que solicita la información y las acciones adicionales están hasta \_ la capa superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4738">If the \_status value indicates success, the results MUST be indicated up to the higher layer requesting the information, and further actions are up to the higher layer.</span></span>

<span data-ttu-id="d07fb-4739">Para fines informativos, se espera que las capas superiores realicen normalmente las siguientes acciones, pero el cliente del Protocolo de servicio de indexación de contenido no las aplica:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4739">For informative purposes, it is expected that higher layers will typically do the following actions, but these are not enforced by the Content Indexing Service Protocol client:</span></span>

-   <span data-ttu-id="d07fb-4740">Si los valores de las filas representan los identificadores de documento, los identificadores de capítulo o marcador de la capa superior normalmente los almacenarán para su uso en operaciones posteriores que implican identificadores de documento válidos, identificadores de capítulos o marcadores.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4740">If the values in rows represent the document IDs, chapter or bookmark handles the higher layer will typically store them for use in subsequent operations which involve valid document IDs, chapter or bookmark handles.</span></span>
-   <span data-ttu-id="d07fb-4741">La capa superior normalmente almacenará o mostrará o usará los datos de los valores de fila.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4741">The higher layer will typically store or display or otherwise use the data from row values.</span></span>
-   <span data-ttu-id="d07fb-4742">Para los valores que se marcaron como capas superiores diferidas, se capturará el valor mediante mensajes CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4742">For the values which were marked as deferred higher layer will fetch the value using CPMFetchValueIn messages.</span></span>
-   <span data-ttu-id="d07fb-4743">La descripción de la búsqueda también se devuelve a una capa superior y la capa superior puede reutilizarla o examinarla.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4743">The seek description is returned back to higher layer as well, and can be reused or examined by the higher layer.</span></span>

<span data-ttu-id="d07fb-4744">Con fines informativos, si la capa superior solicitó identificadores a capítulos y marcadores que se recibieron en las filas, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4744">For informative purposes, if the higher layer requested handles to chapters and bookmarks which were received in the rows, it may do the following:</span></span>

-   <span data-ttu-id="d07fb-4745">Use CPMGetQueryStatusExIn para comprobar el progreso de ejecución de una consulta, así como información de estado adicional, como el número de documentos filtrados, los documentos que quedan por filtrar, la proporción de documentos procesados por la consulta, el número total de filas de la consulta y la posición del marcador en el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4745">Use CPMGetQueryStatusExIn, to check on the execution progress of a query, as well as additional status information, such as the number of filtered documents, documents remaining to be filtered, the ratio of documents processed by the query, the total number of rows in the query, and the position of the bookmark in the rowset.</span></span>
-   <span data-ttu-id="d07fb-4746">Use CPMGetNotify para solicitar que el servidor notifique al cliente los cambios del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4746">Use CPMGetNotify, to request that the server notify the client of rowset changes.</span></span>
-   <span data-ttu-id="d07fb-4747">Use CPMGetApproximatePositionIn para solicitar la posición aproximada de un marcador en un capítulo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4747">Use CPMGetApproximatePositionIn, to request the approximate position of a bookmark in a chapter.</span></span>
-   <span data-ttu-id="d07fb-4748">Use CPMCompareBmkIn para solicitar una comparación de dos marcadores en un capítulo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4748">Use CPMCompareBmkIn, to request a comparison of two bookmarks in a chapter.</span></span>
-   <span data-ttu-id="d07fb-4749">Use CPMRestartPositionIn en el servidor para cambiar la ubicación del cursor al inicio del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4749">Use CPMRestartPositionIn, to the server to change the location of the cursor to the start of rowset.</span></span>

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a><span data-ttu-id="d07fb-4750">3.2.5.3 Recepción de una respuesta CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-4750">3.2.5.3 Receiving a CPMFetchValueOut Response</span></span>

<span data-ttu-id="d07fb-4751">Cuando el cliente recibe una respuesta de mensaje CPMGetRowsOut del servidor, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4751">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="d07fb-4752">Compruebe si el \_ campo de estado del encabezado indica que se ha hecho correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4752">Check if the \_status field in the header indicates success or failure.</span></span> <span data-ttu-id="d07fb-4753">En caso de error, notifique a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4753">In a case of failure notify the higher layer.</span></span> <span data-ttu-id="d07fb-4754">De lo contrario, continúe a continuación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4754">Otherwise, continue below.</span></span>
-   <span data-ttu-id="d07fb-4755">Active fValueExist y, si se establece en 0x00000000 informe a la capa \_ superior de que no se encontró el valor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4755">Check \_fValueExist, and if set to 0x00000000 notify the higher layer that the value was not found.</span></span>
-   <span data-ttu-id="d07fb-4756">De lo contrario, \_ anexe los bytes cbValue de vValue al valor de propiedad actual.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4756">Otherwise append \_ cbValue bytes from vValue to Current Property Value.</span></span>
-   <span data-ttu-id="d07fb-4757">Si fMoreExists se establece en 0x00000001, incremente los bytes actuales recibidos por cbValue y envíe un mensaje \_ \_ \_ \_ CPMFetchValueIn al servidor, estableciendo cbSoFar en el valor de \_ Bytes actuales recibidos, cbPropSpec en cero y \_ \_ cbChunk en el tamaño de búfer deseado por la capa superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4757">If \_\_fMoreExists is set to 0x00000001 then increment \_Current Bytes Received by \_cbValue and send a CPMFetchValueIn message to the server, setting \_cbSoFar to the value of Current Bytes Received, \_cbPropSpec to zero and \_cbChunk to the buffer size desired by the higher layer.</span></span>
-   <span data-ttu-id="d07fb-4758">Si fMoreExists se establece en 0x00000000, indique el valor de propiedad de Valor de propiedad \_ actual a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4758">If \_fMoreExists is set to 0x00000000 then indicate the property value from Current Property Value to the higher layer.</span></span>

### <a name="3254-receiving-a-cpmfreecursorout-response"></a><span data-ttu-id="d07fb-4759">3.2.5.4 Recibir una respuesta CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="d07fb-4759">3.2.5.4 Receiving a CPMFreeCursorOut Response</span></span>

<span data-ttu-id="d07fb-4760">Cuando el cliente recibe una respuesta de mensaje CPMFreeCursorOut correcta del servidor, el cliente DEBE devolver el valor \_ cCursorsRemaining a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4760">When the client receives a successful CPMFreeCursorOut message response from the server, the client MUST return the \_cCursorsRemaining value to the higher layer.</span></span>

<span data-ttu-id="d07fb-4761">La siguiente información se proporciona solo con fines informativos y no la aplica el cliente CISP.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4761">The following information is given for informative purposes only and is not enforced by the CISP client.</span></span> <span data-ttu-id="d07fb-4762">Se espera que la capa superior realice un seguimiento de los identificadores de cursor y no use los que ya se han liberado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4762">The higher layer is expected to keep track of cursor handles and not to use ones which have already been freed.</span></span> <span data-ttu-id="d07fb-4763">Una vez que el número de cCursorsRemaining es igual a 0x00000000, la capa superior puede usar la conexión para especificar otra consulta (mediante un mensaje \_ CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4763">Once the number of \_cCursorsRemaining is equal to 0x00000000, the higher layer can use the connection to specify another query (using a CPMCreateQueryIn message).</span></span>

### <a name="326-timer-events"></a><span data-ttu-id="d07fb-4764">3.2.6 Eventos de temporizador</span><span class="sxs-lookup"><span data-stu-id="d07fb-4764">3.2.6 Timer Events</span></span>

<span data-ttu-id="d07fb-4765">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4765">None.</span></span>

### <a name="327-other-local-events"></a><span data-ttu-id="d07fb-4766">3.2.7 Otros eventos locales</span><span class="sxs-lookup"><span data-stu-id="d07fb-4766">3.2.7 Other Local Events</span></span>

<span data-ttu-id="d07fb-4767">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4767">None.</span></span>

## <a name="4-protocol-examples"></a><span data-ttu-id="d07fb-4768">4 Ejemplos de protocolo</span><span class="sxs-lookup"><span data-stu-id="d07fb-4768">4 Protocol Examples</span></span>

-   [<span data-ttu-id="d07fb-4769">4.1 Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4769">4.1 Example 1</span></span>](#41-example-1)
-   [<span data-ttu-id="d07fb-4770">4.2 Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4770">4.2 Example 2</span></span>](#42-example-2)

### <a name="41-example-1"></a><span data-ttu-id="d07fb-4771">4.1 Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="d07fb-4771">4.1 Example 1</span></span>

<span data-ttu-id="d07fb-4772">En el ejemplo siguiente, se considera un escenario en el que el usuario JOHN de la máquina A quiere obtener los tamaños de los archivos que contienen la palabra "Microsoft" del conjunto de documentos almacenados en el servidor X en el catálogo SYSTEM.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4772">In the following example, we consider a scenario in which the user JOHN on machine A wants to obtain the sizes of files that contain the word "Microsoft" from the set of documents stored on server X in catalog SYSTEM.</span></span> <span data-ttu-id="d07fb-4773">Supongamos que la máquina A ejecuta un sistema operativo Windows XP de 32 bits y la máquina X ejecuta un sistema operativo Windows Server 2003 de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4773">Let us assume that machine A is running a 32-bit Windows XP operating system and machine X is running a 32-bit Windows Server 2003 operating system.</span></span>

1.  <span data-ttu-id="d07fb-4774">El usuario inicia una aplicación de búsqueda y escribe la consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4774">The user launches a search application and enters the search query.</span></span> <span data-ttu-id="d07fb-4775">A su vez, la aplicación pasa la consulta de búsqueda al cliente de protocolo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4775">The application in turn passes the search query to the protocol client.</span></span>
2.  <span data-ttu-id="d07fb-4776">El cliente de protocolo establece una conexión con el servidor de indexación X. El cliente de protocolo usa la canalización con nombre CI TFTPDS para conectarse al \\ servidor X a través de \\ \_ SMB.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4776">The protocol client establishes a connection with indexing server X. The protocol client uses the named pipe \\pipe\\CI\_SKADS to connect to the server X over SMB.</span></span>
3.  <span data-ttu-id="d07fb-4777">A continuación, el cliente de protocolo prepara un mensaje CPMConnectIn con los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4777">The protocol client then prepares a CPMConnectIn message with the following values:</span></span>

    <span data-ttu-id="d07fb-4778">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4778">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="d07fb-4779">**\_ msg** se establece en 0x000000C8, lo que indica que se trata de un mensaje CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4779">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectIn message.</span></span>
    -   <span data-ttu-id="d07fb-4780">**\_ status** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4780">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="d07fb-4781">**\_ ulChecksum** contiene la suma de comprobación, calculada como se especifica en la sección 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4781">**\_ulChecksum** contains the checksum, computed as specified in Section 3.2.4.</span></span>
    -   <span data-ttu-id="d07fb-4782">**\_ ulReserved2** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4782">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="d07fb-4783">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4783">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="d07fb-4784">**\_ iClientVersion** se establece en 0x00000008, lo que indica que el servidor va a validar el campo de suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4784">**\_iClientVersion** is set to 0x00000008, indicating that the server is to validate the checksum field.</span></span>
    -   <span data-ttu-id="d07fb-4785">**\_ fClientIsRemote** se establece en 0x00000001, lo que indica que el servidor es un servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4785">**\_fClientIsRemote** is set to 0x00000001, indicating that the server is a remote server.</span></span>
    -   <span data-ttu-id="d07fb-4786">**\_ cbBlob1 se** establece en el tamaño, en bytes, de los campos cPropSet, PropertySet1 y PropertySet2 combinados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4786">**\_cbBlob1** is set to the size, in bytes, of the cPropSet, PropertySet1 and PropertySet2 fields combined.</span></span>
    -   <span data-ttu-id="d07fb-4787">**\_ cbBlob2** se establece en 0x00000004 (lo que significa que no hay conjuntos de propiedades adicionales).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4787">**\_cbBlob2** is set to 0x00000004 (meaning no extra property sets).</span></span>
    -   <span data-ttu-id="d07fb-4788">**MachineName** se establece en A.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4788">**MachineName** is set to A.</span></span>
    -   <span data-ttu-id="d07fb-4789">**UserName** se establece en JOHN.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4789">**UserName** is set to JOHN.</span></span>
    -   <span data-ttu-id="d07fb-4790">**cPropSets** se establece en 0x00000002.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4790">**cPropSets** is set to 0x00000002.</span></span>
    -   <span data-ttu-id="d07fb-4791">**El campo PropertySet1** es de tipo CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4791">**PropertySet1** field is of type CDbPropSet.</span></span> <span data-ttu-id="d07fb-4792">La estructura CDbPropSet que contiene el campo PropertySet1 se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4792">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>
        -   <span data-ttu-id="d07fb-4793">**El campo GuidPropSet** se establece en A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ EXT).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4793">**GuidPropSet** field is set to A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET\_FSCIFRMWRK\_EXT).</span></span>
        -   <span data-ttu-id="d07fb-4794">**El campo cProperties** se establece en 0x00000004.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4794">**cProperties** field is set to 0x00000004.</span></span>
        -   <span data-ttu-id="d07fb-4795">**El campo aProps** es una matriz de estructuras CDbProp.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4795">**aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="d07fb-4796">Para el **elemento aProps \[ 0: \]**</span><span class="sxs-lookup"><span data-stu-id="d07fb-4796">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="d07fb-4797">**PropId** se establece en 0x00000002 (DBPROP \_ CI \_ CATALOG \_ NAME).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4797">**PropId** is set to 0x00000002 (DBPROP\_CI\_CATALOG\_NAME).</span></span>
            -   <span data-ttu-id="d07fb-4798">**DBPROPOPTIONS** se establece en 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4798">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="d07fb-4799">**DBPROPSTATUS se** establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4799">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="d07fb-4800">Para el **elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="d07fb-4800">For the **ColId** element:</span></span>
                -   <span data-ttu-id="d07fb-4801">**eKind** se establece en 0x00000001 (DBKIND \_ GUID \_ PROPID)</span><span class="sxs-lookup"><span data-stu-id="d07fb-4801">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID)</span></span>
                -   <span data-ttu-id="d07fb-4802">**GUID** es null (todos los ceros), lo que significa que el valor se aplica a la consulta, no solo a una sola columna.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4802">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="d07fb-4803">**ulID** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4803">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="d07fb-4804">Para el **elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="d07fb-4804">For the **vValue** element:</span></span>
                -   <span data-ttu-id="d07fb-4805">**vType** se establece en 0x001F (VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4805">**vType** is set to 0x001F (VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="d07fb-4806">**vValue** se establece en "SYSTEM", el nombre del catálogo deseado.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4806">**vValue** is set to "SYSTEM", the name of the desired catalog.</span></span>

            <span data-ttu-id="d07fb-4807">Para el **elemento aProps \[ 1: \]**</span><span class="sxs-lookup"><span data-stu-id="d07fb-4807">For the **aProps\[1\]** element:</span></span>

            -   <span data-ttu-id="d07fb-4808">**PropId** se establece en 0x00000007 (DBPROP \_ CI \_ QUERY \_ TYPE)</span><span class="sxs-lookup"><span data-stu-id="d07fb-4808">**PropId** is set to 0x00000007 (DBPROP\_CI\_QUERY\_TYPE)</span></span>
            -   <span data-ttu-id="d07fb-4809">**DBPROPOPTIONS** se establece en 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4809">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="d07fb-4810">**DBPROPSTATUS** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4810">**DBPROPSTATUS** is set to0x00000000.</span></span>
            -   <span data-ttu-id="d07fb-4811">Para el **elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="d07fb-4811">For the **ColId** element:</span></span>
                -   <span data-ttu-id="d07fb-4812">**eKind** se establece en 0x00000001 (DBKIND \_ GUID \_ PROPID).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4812">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="d07fb-4813">**GUID** es null (todos los ceros), lo que significa que el valor se aplica a la consulta, no solo a una sola columna.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4813">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="d07fb-4814">**ulID** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4814">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="d07fb-4815">Para el **elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="d07fb-4815">For the **vValue** element:</span></span>
                -   <span data-ttu-id="d07fb-4816">**vType** se establece en 0x0003 (VT \_ I4).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4816">**vType** is set to 0x0003 (VT\_I4).</span></span>
                -   <span data-ttu-id="d07fb-4817">**vValue** se establece en 0x00000000 (CiNormal), lo que significa que es una consulta normal.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4817">**vValue** is set to 0x00000000 (CiNormal), meaning it is a regular query.</span></span>

            <span data-ttu-id="d07fb-4818">Para el **elemento aProps \[ 2: \]**</span><span class="sxs-lookup"><span data-stu-id="d07fb-4818">For the **aProps\[2\]** element:</span></span>

            -   <span data-ttu-id="d07fb-4819">**PropId** se establece en 0x00000004 (MARCAS DE \_ ÁMBITO DE CI DE \_ \_ DBPROP).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4819">**PropId** is set to 0x00000004 (DBPROP\_CI\_SCOPE\_FLAGS).</span></span>
            -   <span data-ttu-id="d07fb-4820">**DBPROPOPTIONS** se establece en 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4820">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="d07fb-4821">**DBPROPSTATUS se** establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4821">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="d07fb-4822">Para el **elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="d07fb-4822">For the **ColId** element:</span></span>
                -   <span data-ttu-id="d07fb-4823">**eKind** se establece en 0x00000001 (DBKIND \_ GUID \_ PROPID).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4823">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="d07fb-4824">**GUID** es null (todos los ceros), lo que significa que el valor se aplica a la consulta, no solo a una sola columna.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4824">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="d07fb-4825">**ulID** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4825">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="d07fb-4826">Para el **elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="d07fb-4826">For the **vValue** element:</span></span>
                -   <span data-ttu-id="d07fb-4827">**vType**: 0x1003 (VT \_ VECTOR VT \| \_ I4)</span><span class="sxs-lookup"><span data-stu-id="d07fb-4827">**vType**: 0x1003 (VT\_VECTOR \| VT\_I4)</span></span>
                -   <span data-ttu-id="d07fb-4828">**vValue:** 0x00000001 /0x00000001 (un elemento con el valor 1), lo que significa subcarpetas de búsqueda</span><span class="sxs-lookup"><span data-stu-id="d07fb-4828">**vValue**: 0x00000001 / 0x00000001 (one element with value 1), meaning search sub-folders</span></span>

            <span data-ttu-id="d07fb-4829">Para el **elemento aProps \[ 3: \]**</span><span class="sxs-lookup"><span data-stu-id="d07fb-4829">For the **aProps\[3\]** element:</span></span>

            -   <span data-ttu-id="d07fb-4830">**PropId:** 0x00000003 (ÁMBITOS DE INCLUDE \_ DE DBPROP \_ \_ CI)</span><span class="sxs-lookup"><span data-stu-id="d07fb-4830">**PropId**: 0x00000003 (DBPROP\_CI\_INCLUDE\_SCOPES)</span></span>
            -   <span data-ttu-id="d07fb-4831">**DBPROPOPTIONS:** 0x0000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-4831">**DBPROPOPTIONS**: 0x0000000</span></span>
            -   <span data-ttu-id="d07fb-4832">**DBPROPSTATUS:** 0x00000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-4832">**DBPROPSTATUS**: 0x00000000</span></span>
            -   <span data-ttu-id="d07fb-4833">Para el **elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="d07fb-4833">For the **ColId** element:</span></span>
                -   <span data-ttu-id="d07fb-4834">**eKind** se establece en 0x00000001 (DBKIND \_ GUID \_ PROPID).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4834">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="d07fb-4835">**GUID** es null (todos los ceros), lo que significa que el valor se aplica a la consulta, no solo a una sola columna.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4835">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="d07fb-4836">**ulID** se establece en 0x00000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-4836">**ulID** is set to 0x00000000</span></span>
            -   <span data-ttu-id="d07fb-4837">Para el **elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="d07fb-4837">For the **vValue** element:</span></span>
                -   <span data-ttu-id="d07fb-4838">**vType** se establece en 0x101F (VT \_ VECTOR \| VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4838">**vType** is set to 0x101F (VT\_VECTOR \| VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="d07fb-4839">**vValue** se establece en 0x00000001 / 0x00000002 / " " (un elemento con una cadena terminada en NULL de 2 caracteres), lo que significa el \\ ámbito raíz.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4839">**vValue** is set to 0x00000001 / 0x00000002 / "\\" (one element with a 2 character null-terminated string), meaning the root scope.</span></span>

    -   <span data-ttu-id="d07fb-4840">El **campo PropertySet2** es de tipo CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4840">The **PropertySet2** field is of type CDbPropSet.</span></span>

        <span data-ttu-id="d07fb-4841">La estructura CDbPropSet que contiene el campo PropertySet1 se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4841">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>

        -   <span data-ttu-id="d07fb-4842">**GuidPropSet** se establece en AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ EXT).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4842">**GuidPropSet** is set to AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET\_CIFRMWRKCORE\_EXT).</span></span>
        -   <span data-ttu-id="d07fb-4843">**El campo cProperties** se establece en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4843">**cProperties** field is set to 0x00000001.</span></span>
        -   <span data-ttu-id="d07fb-4844">El **campo aProps** es una matriz de estructuras CDbProp.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4844">The **aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="d07fb-4845">Para el **elemento aProps \[ 0: \]**</span><span class="sxs-lookup"><span data-stu-id="d07fb-4845">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="d07fb-4846">**PropId** se establece en 0x00000002 (DBPROP \_ MACHINE).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4846">**PropId** is set to 0x00000002 (DBPROP\_MACHINE).</span></span>
            -   <span data-ttu-id="d07fb-4847">**DBPROPOPTIONS** se establece en 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4847">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="d07fb-4848">**DBPROPSTATUS se** establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4848">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="d07fb-4849">Para el **elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="d07fb-4849">For the **ColId** element:</span></span>
                -   <span data-ttu-id="d07fb-4850">**eKind** se establece en 0x00000001 (DBKIND \_ GUID \_ PROPID),</span><span class="sxs-lookup"><span data-stu-id="d07fb-4850">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID),</span></span>
                -   <span data-ttu-id="d07fb-4851">**GUID** es null (todos los ceros), lo que significa que el valor se aplica a la consulta, no solo a una sola columna.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4851">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="d07fb-4852">**ulID** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4852">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="d07fb-4853">Para **el elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="d07fb-4853">For **vValue** element:</span></span>
                -   <span data-ttu-id="d07fb-4854">**vType:** 0x0008 (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="d07fb-4854">**vType**: 0x0008 (VT\_BSTR)</span></span>
                -   <span data-ttu-id="d07fb-4855">**vValue:** 0x04 / "X" (4 bytes /cadena Unicode terminada en NULL), lo que significa "X" -name de un servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4855">**vValue**: 0x04 / "X" (4 bytes / null-terminated Unicode string), meaning "X" -name of a server.</span></span>

    -   <span data-ttu-id="d07fb-4856">**El campo cExtPropSet** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4856">**cExtPropSet** field is set to 0x00000000.</span></span>
    -   <span data-ttu-id="d07fb-4857">**la matriz aPropertySets** no existe.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4857">**aPropertySets** array does not exist.</span></span>
    -   <span data-ttu-id="d07fb-4858">Se rellenan varios campos de relleno según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4858">Various padding fields are filled in as needed.</span></span> <span data-ttu-id="d07fb-4859">El mensaje se envía al servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4859">The message is sent to the server.</span></span>

4.  <span data-ttu-id="d07fb-4860">El servidor comprueba que **\_ ulChecksum** es correcto, comprueba que el usuario está autorizado para realizar esta solicitud y responde con un mensaje CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4860">The server verifies that the **\_ulChecksum** is correct, verifies that the user is authorized to make this request, and responds with a CPMConnectOut message.</span></span>

    <span data-ttu-id="d07fb-4861">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4861">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="d07fb-4862">**\_ msg** se establece en 0x000000C8, lo que indica que se trata de un mensaje CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4862">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectOut message.</span></span>
    -   <span data-ttu-id="d07fb-4863">**\_ status** se establece en 0x0000000 que indica SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4863">**\_status** is set to 0x0000000 indicating SUCCESS.</span></span>
    -   <span data-ttu-id="d07fb-4864">**\_ ulChecksum** se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4864">**\_ulChecksum** is set to 0.</span></span>
    -   <span data-ttu-id="d07fb-4865">**\_ ulReserved2** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4865">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="d07fb-4866">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4866">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="d07fb-4867">**\_ El campo serverVersion** se establece 0x00000007 (Windows XP de 32 bits o Windows Server 2003 de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4867">**\_serverVersion** field is set to 0x00000007 (32-bit Windows XP or 32-bit Windows Server 2003).</span></span>
    -   <span data-ttu-id="d07fb-4868">**\_ Los** campos reservados se rellenan con datos arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4868">**\_reserved** fields are filled with arbitrary data.</span></span>

5.  <span data-ttu-id="d07fb-4869">El cliente prepara un mensaje CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4869">The client prepares a CPMCreateQueryIn message.</span></span>

    <span data-ttu-id="d07fb-4870">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4870">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="d07fb-4871">**\_ msg** se establece en 0x000000CA, lo que indica que se trata de un mensaje CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4871">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryIn message.</span></span>
    -   <span data-ttu-id="d07fb-4872">**\_ status** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4872">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="d07fb-4873">**\_ ulChecksum** contiene la suma de comprobación, calculada según la versión 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4873">**\_ulChecksum** contains the checksum, computed according to 3.2.5.</span></span>
    -   <span data-ttu-id="d07fb-4874">**\_ ulReserved2** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4874">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="d07fb-4875">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4875">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="d07fb-4876">**El** campo Tamaño se establece en el tamaño del resto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4876">**Size** field is set to the size of the rest of the message.</span></span>
    -   <span data-ttu-id="d07fb-4877">**El campo CColumnSetPresent** se establece en 0x01.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4877">**CColumnSetPresent** field is set to 0x01.</span></span>
    -   <span data-ttu-id="d07fb-4878">**El campo ColumnSet** es de tipo CColumnSet.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4878">**ColumnSet** field is of type CColumnSet.</span></span> <span data-ttu-id="d07fb-4879">La estructura CColumnSet que contiene este campo se establece de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4879">The CColumnSet structure comprising this field is set as follows:</span></span>
        -   <span data-ttu-id="d07fb-4880">**\_ count** field se establece en 0x00000001 que indica que se devuelve una columna.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4880">**\_count** field is set to 0x00000001 indicating one column is returned.</span></span>
        -   <span data-ttu-id="d07fb-4881">**La** matriz indexes 0x00000000 indica la primera entrada de \_ aPropSpec.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4881">**indexes** array is 0x00000000 indicating the first entry in \_aPropSpec.</span></span>
    -   <span data-ttu-id="d07fb-4882">**El campo CRestrictionPresent** se establece en 0x01 que indica que **el campo Restricción** está presente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4882">**CRestrictionPresent** field is set to 0x01 indicating the **Restriction** field is present.</span></span>
    -   <span data-ttu-id="d07fb-4883">**El** campo Restricción es de tipo CRestriction y se establece en:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4883">**Restriction** field is of type CRestriction and is set to:</span></span>
        -   <span data-ttu-id="d07fb-4884">**\_ ulType** se establece en 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4884">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
        -   <span data-ttu-id="d07fb-4885">**\_ weight** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4885">**\_weight** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="d07fb-4886">El resto del campo contiene una estructura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4886">The rest of the field contains a CContentRestriction structure:</span></span>
        -   <span data-ttu-id="d07fb-4887">**\_ La** propiedad se establece en GUID B725F130-47EF-101A-A5F1-02608c9eebac/0x00000001 (para PRSPEC PROPID) / 0x13 que representa el cuerpo \_ del documento.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4887">**\_Property** is set to GUID B725F130-47EF-101A-A5F1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13 which represents the document body.</span></span>
        -   <span data-ttu-id="d07fb-4888">**\_ Cc** se establece en 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4888">**\_Cc** is set to 0x00000009.</span></span>
        -   <span data-ttu-id="d07fb-4889">**\_ pwcsphrase** se establece en la cadena "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="d07fb-4889">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
        -   <span data-ttu-id="d07fb-4890">**\_ lcid** se establece en 0x409 (para inglés).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4890">**\_lcid** is set to 0x409 (for English).</span></span>
        -   <span data-ttu-id="d07fb-4891">**\_ ulGenerateMethod** se establece en 0x00000000 (coincidencia exacta).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4891">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>
    -   <span data-ttu-id="d07fb-4892">**CSortPresent** se establece en 0x00.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4892">**CSortPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="d07fb-4893">**CCategorizationSetPresent** se establece en 0x00.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4893">**CCategorizationSetPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="d07fb-4894">**RowSetProperties** se establece de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4894">**RowSetProperties** is set as follows:</span></span>
        -   <span data-ttu-id="d07fb-4895">**\_ uBooleanOptions** se establece en 0x00000001 (secuencial).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4895">**\_uBooleanOptions** is set to 0x00000001 (sequential).</span></span>
        -   <span data-ttu-id="d07fb-4896">**\_ ulMaxOpenRows** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4896">**\_ulMaxOpenRows** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="d07fb-4897">**\_ ulMemoryUsage** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4897">**\_ulMemoryUsage** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="d07fb-4898">\_**cMaxResults** se establece en 0x00000100 (devuelve como máximo 256 filas).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4898">\_**cMaxResults** is set to 0x00000100 (return at most 256 rows).</span></span>
        -   <span data-ttu-id="d07fb-4899">**\_ cCmdTimeOut se** establece en 0x00000000 (nunca tiempo de espera).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4899">**\_cCmdTimeOut** is set to 0x00000000 (never timeout).</span></span>
    -   <span data-ttu-id="d07fb-4900">**PidMapper** se establece en:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4900">**PidMapper** is set to:</span></span>
        -   <span data-ttu-id="d07fb-4901">**\_ count** se establece en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4901">**\_count** is set to 0x00000001.</span></span>
        -   <span data-ttu-id="d07fb-4902">**\_ aPropSpec** se establece en GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC/0x00000001 (para PRSPEC PROPID) / 0x0000000c que representa la propiedad de tamaño de archivo \_ de Windows.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4902">**\_aPropSpec** is set to GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>

6.  <span data-ttu-id="d07fb-4903">El servidor lo procesa y responde con un mensaje CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4903">The server processes it and responds with a CPMCreateQueryOut message.</span></span>

    <span data-ttu-id="d07fb-4904">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4904">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="d07fb-4905">**\_ msg** se establece en 0x000000CA, lo que indica que se trata de un mensaje CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4905">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryOut message.</span></span>
    -   <span data-ttu-id="d07fb-4906">**\_ status** se establece en SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4906">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="d07fb-4907">**\_ ulChecksum** se establece en 0x00000000 (o cualquier otro valor arbitrario).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4907">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="d07fb-4908">**\_ ulReserved2** se establece en 0x00000000 (o cualquier otro valor arbitrario).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4908">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="d07fb-4909">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4909">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="d07fb-4910">**\_ fTrueSeqeuntial** se establece en 0x00000000, lo que indica que la consulta puede usar un índice.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4910">**\_fTrueSeqeuntial** is set to 0x00000000, indicating that the query can use an index.</span></span>
    -   <span data-ttu-id="d07fb-4911">**\_ fWorkIdUnique** se establece en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4911">**\_fWorkIdUnique** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="d07fb-4912">La **matriz aCursors** contiene solo un elemento, que representa un identificador de cursor para esta consulta.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4912">The **aCursors** array contains only one element, representing a cursor handle to this query.</span></span> <span data-ttu-id="d07fb-4913">El valor depende del estado del servidor.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4913">The value depends on the state of the server.</span></span> <span data-ttu-id="d07fb-4914">Supongamos que el valor devuelto es 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4914">Let us assume that the returned value is 0xAAAAAAAA.</span></span>

7.  <span data-ttu-id="d07fb-4915">El cliente emite un mensaje de solicitud CPMSetBindingsIn para definir el formato de una fila.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4915">The client issues a CPMSetBindingsIn request message to define the format of a row.</span></span>

    <span data-ttu-id="d07fb-4916">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4916">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="d07fb-4917">**\_ msg** se establece en 0x000000D0, lo que indica que se trata de un mensaje CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4917">**\_msg** is set to 0x000000D0, indicating that this is a CPMSetBindingsIn message.</span></span>
    -   <span data-ttu-id="d07fb-4918">**\_ status** se establece en SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4918">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="d07fb-4919">**\_ ulChecksum** se establece en 0x00000000 (o cualquier otro valor arbitrario).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4919">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="d07fb-4920">**\_ ulReserved2** se establece en 0x00000000 (o cualquier otro valor arbitrario).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4920">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="d07fb-4921">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4921">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="d07fb-4922">**\_ hCursor** se establece en 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4922">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="d07fb-4923">**\_ cbRow** se establece en 0x10 (lo suficientemente grande como para caber columnas).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4923">**\_cbRow** is set to 0x10 (big enough to fit columns).</span></span>
    -   <span data-ttu-id="d07fb-4924">**\_ cbBindingDesc** se establece en el tamaño de los campos **\_ cColumns** y **\_ aColumns** combinados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4924">**\_cbBindingDesc** is set to the size of the **\_cColumns** and **\_aColumns** fields combined.</span></span>
    -   <span data-ttu-id="d07fb-4925">**\_ cColumns** se establece en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4925">**\_cColumns** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="d07fb-4926">**\_ la matriz aColumns** está establecida para contener una estructura CTableColumn que contiene:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4926">**\_aColumns** array is set to contain one CTableColumn structure containing:</span></span>
    -   -   <span data-ttu-id="d07fb-4927">**\_ PropSpec** se establece en GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (para PRSPEC PROPID) / 0x0000000c que representa la propiedad de tamaño de archivo \_ de Windows.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4927">**\_PropSpec** is set to GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>
        -   <span data-ttu-id="d07fb-4928">**\_ vType** se establece en 0x0015 (VT \_ UI8).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4928">**\_vType** is set to 0x0015 (VT\_UI8).</span></span>
        -   <span data-ttu-id="d07fb-4929">**\_ ValueUsed** se establece en 0x01 (columna transferida en fila).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4929">**\_ValueUsed** is set to 0x01 (column transferred in row).</span></span>
        -   <span data-ttu-id="d07fb-4930">**\_ ValueOffset** se establece en 0x0002 (al principio de la fila).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4930">**\_ValueOffset** is set to 0x0002 (at beginning of row).</span></span>
        -   <span data-ttu-id="d07fb-4931">**\_ ValueSize** se establece en 0x08 (tamaño de una VT \_ UI8).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4931">**\_ValueSize** is set to 0x08 (size of a VT\_UI8).</span></span>
        -   <span data-ttu-id="d07fb-4932">**\_ StatusUsed** se establece en 0x01.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4932">**\_StatusUsed** is set to 0x01.</span></span>
        -   <span data-ttu-id="d07fb-4933">**\_ StatusOffset** se establece en 0x0A.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4933">**\_StatusOffset** is set to 0x0A.</span></span>
        -   <span data-ttu-id="d07fb-4934">**\_ LengthUsed** se establece en 0x00.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4934">**\_LengthUsed** is set to 0x00.</span></span>

8.  <span data-ttu-id="d07fb-4935">El servidor lo procesa y responde con un mensaje CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4935">The server processes it and responds with a CPMSetBindingsIn message.</span></span>

    <span data-ttu-id="d07fb-4936">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4936">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="d07fb-4937">**\_ msg** se establece en 0x000000D0.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4937">**\_msg** is set to 0x000000D0.</span></span>
    -   <span data-ttu-id="d07fb-4938">**\_ status** se establece en SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4938">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="d07fb-4939">**\_ ulChecksum** se establece en 0x00000000 (o cualquier otro valor arbitrario).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4939">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="d07fb-4940">**\_ ulReserved2** se establece en 0x00000000 (o cualquier otro valor arbitrario).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4940">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

9.  <span data-ttu-id="d07fb-4941">El cliente emite un mensaje de solicitud CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4941">The client issues a CPMGetRowsIn request message.</span></span> <span data-ttu-id="d07fb-4942">Supongamos que el cliente está preparado para aceptar 100 filas en este momento y las quiere en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4942">Let us assume that the client is prepared to accept 100 rows at this point, and wants them in ascending order.</span></span>

    <span data-ttu-id="d07fb-4943">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4943">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="d07fb-4944">**\_ msg** se establece en 0x000000CC, lo que indica que se trata de un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4944">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsIn message.</span></span>
    -   <span data-ttu-id="d07fb-4945">**\_ status** se establece en 0x00000000</span><span class="sxs-lookup"><span data-stu-id="d07fb-4945">**\_status** is set to 0x00000000</span></span>
    -   <span data-ttu-id="d07fb-4946">**\_ ulChecksum contiene** la suma de comprobación, calculada según la sección 0.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4946">**\_ulChecksum** contains the checksum, computed according to Section 0.</span></span>
    -   <span data-ttu-id="d07fb-4947">**\_ ulReserved2** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4947">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="d07fb-4948">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4948">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="d07fb-4949">**\_ hCursor** se establece en 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4949">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="d07fb-4950">**\_ cRowsToTransfer** se establece en 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4950">**\_cRowsToTransfer** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="d07fb-4951">**\_ cRowWidth** se establece en 0x00000010 (desde enlaces).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4951">**\_cRowWidth** is set to 0x00000010 (from bindings).</span></span>
    -   <span data-ttu-id="d07fb-4952">**\_ cbSeek** se establece en 0x14 que es el tamaño de los campos eType, chapt y \_ CRowSeekNext combinados.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4952">**\_cbSeek** is set to 0x14 which is the size of the eType, \_chapt and CRowSeekNext fields combined.</span></span>
    -   <span data-ttu-id="d07fb-4953">**\_ cbReserved** se establece en 0x18 (0x14 más \_ cbSeek).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4953">**\_cbReserved** is set to 0x18 (0x14 plus \_cbSeek).</span></span>
    -   <span data-ttu-id="d07fb-4954">**\_ cbReadBuffer** se establece en 0x800 (0x64 0x10 redondeada al siguiente \* múltiplo de 0x200).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4954">**\_cbReadBuffer** is set to 0x800 (0x64\*0x10 rounded up to the next multiple of 0x200).</span></span>
    -   <span data-ttu-id="d07fb-4955">**\_ ulClientBase** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4955">**\_ulClientBase** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="d07fb-4956">**\_ fBwdfetch** se establece en 0x00000000 que indica que las filas se van a capturar en orden de avance.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4956">**\_fBwdfetch** is set to 0x00000000 indicating that the rows are to be fetched in forward order.</span></span>
    -   <span data-ttu-id="d07fb-4957">**eType** se establece en 0x0000001 que indica que el cliente quiere las siguientes filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4957">**eType** is set to 0x0000001 indicating that the client wants next rows.</span></span>
    -   <span data-ttu-id="d07fb-4958">**\_ chapt** se establece en 0 (no en un resultado con capítulos).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4958">**\_chapt** is set to 0 (not a chaptered result).</span></span>
    -   <span data-ttu-id="d07fb-4959">**SeekDescription** se establece en CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4959">**SeekDescription** is set to CRowSeekNext.</span></span> <span data-ttu-id="d07fb-4960">La estructura CRowSeekNext contiene los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4960">The CRowSeekNext structure contains the following values:</span></span>
        -   <span data-ttu-id="d07fb-4961">**CiTblChapt** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4961">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="d07fb-4962">**\_ hRegion** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4962">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="d07fb-4963">**\_ cSkip** se establece en 0, lo que indica que el cliente no quiere omitir filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4963">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>

10. <span data-ttu-id="d07fb-4964">El servidor lo procesa y responde con un mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4964">The server processes it and responds with a CPMGetRowsOut message.</span></span> <span data-ttu-id="d07fb-4965">Supongamos que el servidor encontró 100 documentos que contienen la palabra "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="d07fb-4965">Let us assume that the server found 100 documents that contain the word "Microsoft".</span></span>

    <span data-ttu-id="d07fb-4966">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4966">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="d07fb-4967">**\_ msg** se establece en 0x000000CC, lo que indica que se trata de un mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4967">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsOut message.</span></span>
    -   <span data-ttu-id="d07fb-4968">**\_ status** se establece en SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4968">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="d07fb-4969">**\_ ulChecksum** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4969">**\_ulChecksum** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="d07fb-4970">**\_ ulReserved2** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4970">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="d07fb-4971">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4971">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="d07fb-4972">**\_ CRowsReturned** se establece en 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4972">**\_CRowsReturned** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="d07fb-4973">**eType** se establece en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4973">**eType** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="d07fb-4974">**\_ chapt** se establece en 0x00000000 (no en un resultado con capítulos).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4974">**\_chapt** is set to 0x00000000 (not a chaptered result).</span></span>
    -   <span data-ttu-id="d07fb-4975">**SeekDescription** contiene una estructura CRowSeekNext, rellenada de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4975">**SeekDescription** contains a CRowSeekNext structure, populated as follows:</span></span>
        -   <span data-ttu-id="d07fb-4976">**CiTblChapt** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4976">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="d07fb-4977">**\_ hRegion** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4977">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="d07fb-4978">**\_ cSkip** se establece en 0, lo que indica que el cliente no quiere omitir filas.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4978">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>
    -   <span data-ttu-id="d07fb-4979">**Las** filas contienen el tamaño de los 100 documentos que contienen la palabra "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="d07fb-4979">**Rows** contains the size of the 100 documents that contain the word "Microsoft".</span></span> <span data-ttu-id="d07fb-4980">Puesto que se trata de datos de tamaño fijo, simplemente se estructuran como una lista de enteros de 100 y 8 bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4980">Since this is fixed-sized data, it is simply structured as a list of 100, 8-byte unsigned integers.</span></span>

11. <span data-ttu-id="d07fb-4981">El cliente envía un mensaje CPMDisconnect para finalizar la conexión.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4981">The client sends a CPMDisconnect message to end the connection.</span></span>

    <span data-ttu-id="d07fb-4982">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4982">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="d07fb-4983">**\_ msg** se establece en 0x000000C9, lo que indica que se trata de un mensaje CPMDisconnect.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4983">**\_msg** is set to 0x000000C9, indicating that this is a CPMDisconnect message.</span></span>
    -   <span data-ttu-id="d07fb-4984">**\_ status** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4984">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="d07fb-4985">**\_ ulChecksum** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4985">**\_ulChecksum** is set to 0x00000000.</span></span>

12. <span data-ttu-id="d07fb-4986">El servidor procesa el mensaje y quita todo el estado del cliente.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4986">The server processes the message and removes all client state.</span></span>

### <a name="42-example-2"></a><span data-ttu-id="d07fb-4987">4.2 Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="d07fb-4987">4.2 Example 2</span></span>

<span data-ttu-id="d07fb-4988">En el ejemplo anterior, la consulta era bastante sencilla.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4988">In the previous example, the query was quite simple.</span></span> <span data-ttu-id="d07fb-4989">Ahora vamos a considerar una consulta ligeramente más compleja.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4989">Let us now consider a slightly more complex query.</span></span> <span data-ttu-id="d07fb-4990">Supongamos que el usuario quiere recuperar el tamaño de los documentos que contienen las siguientes palabras: "Microsoft" y "Office".</span><span class="sxs-lookup"><span data-stu-id="d07fb-4990">Let us assume that the user wants to retrieve the size of the documents that contain both the following words: "Microsoft" and "Office".</span></span> <span data-ttu-id="d07fb-4991">Esto se especifica cambiando el campo Restricción contenido en el mensaje CPMCreateQueryIn enviado en el paso 5 como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4991">This is specified by changing the Restriction field contained in the CPMCreateQueryIn message sent in step 5 as follows:</span></span>

<span data-ttu-id="d07fb-4992">El **campo** Restricción es de tipo CRestriction y se establece en:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4992">The **Restriction** field is of type CRestriction and is set to:</span></span>

-   -   <span data-ttu-id="d07fb-4993">**\_ ulType** se establece en 0x00000004 (RTAnd).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4993">**\_ulType** is set to 0x00000004 (RTAnd).</span></span>
    -   <span data-ttu-id="d07fb-4994">**\_ weight** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4994">**\_weight** is set to 0x00000000.</span></span>

<span data-ttu-id="d07fb-4995">El resto del campo contiene una estructura CNodeRestriction:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4995">The rest of the field contains a CNodeRestriction structure:</span></span>

-   -   <span data-ttu-id="d07fb-4996">**\_ cNode** se establece en 0x00000002, lo que indica que hay dos nodos en la matriz paNode.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4996">**\_cNode** is set to 0x00000002, indicating that there are two nodes in the paNode array.</span></span>
    -   <span data-ttu-id="d07fb-4997">El **\_ campo paNode** es una matriz de dos estructuras de CRestriction.</span><span class="sxs-lookup"><span data-stu-id="d07fb-4997">The **\_paNode** field is an array of two CRestriction structures.</span></span>

        <span data-ttu-id="d07fb-4998">**\_ paNode \[ \] 0** contiene:</span><span class="sxs-lookup"><span data-stu-id="d07fb-4998">**\_paNode\[0\]** contains:</span></span>

        -   -   <span data-ttu-id="d07fb-4999">**\_ ulType** se establece en 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="d07fb-4999">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="d07fb-5000">**\_ weight** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-5000">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="d07fb-5001">El resto del campo contiene una estructura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="d07fb-5001">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="d07fb-5002">**\_ La** propiedad se establece en GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (para PRSPEC \_ PROPID) / 0x13.</span><span class="sxs-lookup"><span data-stu-id="d07fb-5002">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="d07fb-5003">**\_ Cc** se establece en 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="d07fb-5003">**\_Cc** is set to 0x00000009.</span></span>
                -   <span data-ttu-id="d07fb-5004">**\_ pwcsphrase** se establece en la cadena "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="d07fb-5004">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
                -   <span data-ttu-id="d07fb-5005">**\_ lcid** se establece en 0x409 (para inglés).</span><span class="sxs-lookup"><span data-stu-id="d07fb-5005">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="d07fb-5006">**\_ ulGenerateMethod** se establece en 0x00000000 (coincidencia exacta).</span><span class="sxs-lookup"><span data-stu-id="d07fb-5006">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

        <span data-ttu-id="d07fb-5007">**\_ paNode \[ \] 1** contiene:</span><span class="sxs-lookup"><span data-stu-id="d07fb-5007">**\_paNode\[1\]** contains:</span></span>

        -   -   <span data-ttu-id="d07fb-5008">**\_ ulType** se establece en 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="d07fb-5008">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="d07fb-5009">**\_ weight** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d07fb-5009">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="d07fb-5010">El resto del campo contiene una estructura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="d07fb-5010">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="d07fb-5011">**\_ La** propiedad se establece en GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (para PRSPEC \_ PROPID) / 0x13.</span><span class="sxs-lookup"><span data-stu-id="d07fb-5011">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="d07fb-5012">**\_ Cc** se establece en 0x00000006.</span><span class="sxs-lookup"><span data-stu-id="d07fb-5012">**\_Cc** is set to 0x00000006.</span></span>
                -   <span data-ttu-id="d07fb-5013">**\_ pwcsphrase** se establece en la cadena "Office".</span><span class="sxs-lookup"><span data-stu-id="d07fb-5013">**\_pwcsphrase** is set to the string "Office".</span></span>
                -   <span data-ttu-id="d07fb-5014">**\_ lcid** se establece en 0x409 (para inglés).</span><span class="sxs-lookup"><span data-stu-id="d07fb-5014">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="d07fb-5015">**\_ ulGenerateMethod** se establece en 0x00000000 (coincidencia exacta).</span><span class="sxs-lookup"><span data-stu-id="d07fb-5015">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

## <a name="5-security"></a><span data-ttu-id="d07fb-5016">5 Seguridad</span><span class="sxs-lookup"><span data-stu-id="d07fb-5016">5 Security</span></span>

### <a name="51-security-considerations-for-implementers"></a><span data-ttu-id="d07fb-5017">5.1 Consideraciones de seguridad para los implementadores</span><span class="sxs-lookup"><span data-stu-id="d07fb-5017">5.1 Security Considerations for Implementers</span></span>

<span data-ttu-id="d07fb-5018">Las implementaciones de indexación que indexa el contenido seguro deben considerar la posibilidad de usar el contexto de usuario proporcionado por SMB MS-SMB para recortar los resultados de la búsqueda y devolver solo los accesibles para \[ el autor de la \] llamada.</span><span class="sxs-lookup"><span data-stu-id="d07fb-5018">Indexing implementations which index secure content should consider using the user context provided by SMB \[MS-SMB\] to trim search results and return only those accessible to the caller.</span></span>

### <a name="52-index-of-security-parameters"></a><span data-ttu-id="d07fb-5019">5.2 Índice de parámetros de seguridad</span><span class="sxs-lookup"><span data-stu-id="d07fb-5019">5.2 Index of Security Parameters</span></span>



| <span data-ttu-id="d07fb-5020">Parámetro de seguridad</span><span class="sxs-lookup"><span data-stu-id="d07fb-5020">Security Parameter</span></span>  | <span data-ttu-id="d07fb-5021">Sección</span><span class="sxs-lookup"><span data-stu-id="d07fb-5021">Section</span></span> |
|---------------------|---------|
| <span data-ttu-id="d07fb-5022">Nivel de suplantación</span><span class="sxs-lookup"><span data-stu-id="d07fb-5022">Impersonation level</span></span> | <span data-ttu-id="d07fb-5023">2.1</span><span class="sxs-lookup"><span data-stu-id="d07fb-5023">2.1</span></span>     |



 

## <a name="6-index-of-version-specific-behavior"></a><span data-ttu-id="d07fb-5024">6 Índice del comportamiento específico de la versión</span><span class="sxs-lookup"><span data-stu-id="d07fb-5024">6 Index of Version Specific Behavior</span></span>



| <span data-ttu-id="d07fb-5025">Comportamiento específico de la versión</span><span class="sxs-lookup"><span data-stu-id="d07fb-5025">Version Specific Behavior</span></span>                                                                         | <span data-ttu-id="d07fb-5026">Sección</span><span class="sxs-lookup"><span data-stu-id="d07fb-5026">Section</span></span>   | <span data-ttu-id="d07fb-5027">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d07fb-5027">Windows 2000</span></span> | <span data-ttu-id="d07fb-5028">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d07fb-5028">Windows XP</span></span> | <span data-ttu-id="d07fb-5029">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d07fb-5029">Windows Server 2003</span></span> |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| <span data-ttu-id="d07fb-5030">Este protocolo se implementa en Windows 2000, Windows XP, Windows Server 2003 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d07fb-5030">This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span> | <span data-ttu-id="d07fb-5031">1.3.2</span><span class="sxs-lookup"><span data-stu-id="d07fb-5031">1.3.2</span></span>     | <span data-ttu-id="d07fb-5032">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5032">X</span></span>            | <span data-ttu-id="d07fb-5033">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5033">X</span></span>          | <span data-ttu-id="d07fb-5034">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5034">X</span></span>                   |
| <span data-ttu-id="d07fb-5035">Las aplicaciones normalmente interactúan con un contenedor OLE DB interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="d07fb-5035">Applications typically interact with an OLE DB interface wrapper</span></span>                                  | <span data-ttu-id="d07fb-5036">1.4</span><span class="sxs-lookup"><span data-stu-id="d07fb-5036">1.4</span></span>       | <span data-ttu-id="d07fb-5037">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5037">X</span></span>            | <span data-ttu-id="d07fb-5038">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5038">X</span></span>          | <span data-ttu-id="d07fb-5039">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5039">X</span></span>                   |
| <span data-ttu-id="d07fb-5040">Valores NTSTATUS</span><span class="sxs-lookup"><span data-stu-id="d07fb-5040">NTSTATUS values</span></span>                                                                                   | <span data-ttu-id="d07fb-5041">1.8</span><span class="sxs-lookup"><span data-stu-id="d07fb-5041">1.8</span></span>       | <span data-ttu-id="d07fb-5042">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5042">X</span></span>            | <span data-ttu-id="d07fb-5043">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5043">X</span></span>          | <span data-ttu-id="d07fb-5044">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5044">X</span></span>                   |
| <span data-ttu-id="d07fb-5045">El cliente establece el campo \_ de estado en cada encabezado de mensaje.</span><span class="sxs-lookup"><span data-stu-id="d07fb-5045">The client sets the \_status field in each Message Header.</span></span>                                        | <span data-ttu-id="d07fb-5046">2.2.2</span><span class="sxs-lookup"><span data-stu-id="d07fb-5046">2.2.2</span></span>     | <span data-ttu-id="d07fb-5047">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5047">X</span></span>            | <span data-ttu-id="d07fb-5048">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5048">X</span></span>          | <span data-ttu-id="d07fb-5049">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5049">X</span></span>                   |
| <span data-ttu-id="d07fb-5050">El valor de cPendingScans suele ser cero.</span><span class="sxs-lookup"><span data-stu-id="d07fb-5050">cPendingScans value is usually zero</span></span>                                                               | <span data-ttu-id="d07fb-5051">2.2.3.1</span><span class="sxs-lookup"><span data-stu-id="d07fb-5051">2.2.3.1</span></span>   | <span data-ttu-id="d07fb-5052">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5052">X</span></span>            | <span data-ttu-id="d07fb-5053">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5053">X</span></span>          | <span data-ttu-id="d07fb-5054">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5054">X</span></span>                   |
| <span data-ttu-id="d07fb-5055">Valor de iClientVersion</span><span class="sxs-lookup"><span data-stu-id="d07fb-5055">iClientVersion value</span></span>                                                                              | <span data-ttu-id="d07fb-5056">2.2.3.6</span><span class="sxs-lookup"><span data-stu-id="d07fb-5056">2.2.3.6</span></span>   | <span data-ttu-id="d07fb-5057">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5057">X</span></span>            | <span data-ttu-id="d07fb-5058">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5058">X</span></span>          | <span data-ttu-id="d07fb-5059">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5059">X</span></span>                   |
| <span data-ttu-id="d07fb-5060">\_cbChunk value</span><span class="sxs-lookup"><span data-stu-id="d07fb-5060">\_cbChunk value</span></span>                                                                                   | <span data-ttu-id="d07fb-5061">2.2.3.19</span><span class="sxs-lookup"><span data-stu-id="d07fb-5061">2.2.3.19</span></span>  | <span data-ttu-id="d07fb-5062">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5062">X</span></span>            | <span data-ttu-id="d07fb-5063">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5063">X</span></span>          | <span data-ttu-id="d07fb-5064">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5064">X</span></span>                   |
| <span data-ttu-id="d07fb-5065">Direcciones de memoria de 32 y 64 bits</span><span class="sxs-lookup"><span data-stu-id="d07fb-5065">32-bit and 64-bit memory addresses</span></span>                                                                | <span data-ttu-id="d07fb-5066">3.2.4.2.4</span><span class="sxs-lookup"><span data-stu-id="d07fb-5066">3.2.4.2.4</span></span> | <span data-ttu-id="d07fb-5067">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5067">X</span></span>            | <span data-ttu-id="d07fb-5068">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5068">X</span></span>          | <span data-ttu-id="d07fb-5069">X</span><span class="sxs-lookup"><span data-stu-id="d07fb-5069">X</span></span>                   |



 

 

 





