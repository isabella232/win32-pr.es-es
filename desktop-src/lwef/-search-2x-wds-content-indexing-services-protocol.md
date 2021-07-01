---
title: Protocolo de servicios de indexación de contenido
description: Este documento es una especificación del protocolo content indexing Service.
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14573dac5a7a6818234c086d05b52e5b81c2a1c1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119740"
---
# <a name="content-indexing-services-protocol"></a><span data-ttu-id="cbf24-103">Protocolo de servicios de indexación de contenido</span><span class="sxs-lookup"><span data-stu-id="cbf24-103">Content Indexing Services Protocol</span></span>

> [!NOTE]
> <span data-ttu-id="cbf24-104">Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cbf24-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="cbf24-105">En versiones posteriores, use [Windows Search](../search/-search-3x-wds-overview.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="cbf24-106">Especificación de protocolo, versión 0.12</span><span class="sxs-lookup"><span data-stu-id="cbf24-106">Protocol Specification, Version 0.12</span></span>

-   [<span data-ttu-id="cbf24-107">1 Introducción</span><span class="sxs-lookup"><span data-stu-id="cbf24-107">1 Introduction</span></span>](#1-introduction)
    -   [<span data-ttu-id="cbf24-108">1.1 Glosario</span><span class="sxs-lookup"><span data-stu-id="cbf24-108">1.1 Glossary</span></span>](#11-glossary)
    -   [<span data-ttu-id="cbf24-109">1.2 Referencias</span><span class="sxs-lookup"><span data-stu-id="cbf24-109">1.2 References</span></span>](#12-references)
    -   [<span data-ttu-id="cbf24-110">Introducción al protocolo 1.3 (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="cbf24-110">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
    -   [<span data-ttu-id="cbf24-111">1.4 Relación con otros protocolos</span><span class="sxs-lookup"><span data-stu-id="cbf24-111">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
    -   [<span data-ttu-id="cbf24-112">1.5 Requisitos previos y condiciones previas</span><span class="sxs-lookup"><span data-stu-id="cbf24-112">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
    -   [<span data-ttu-id="cbf24-113">1.6 Declaración de aplicabilidad</span><span class="sxs-lookup"><span data-stu-id="cbf24-113">1.6 Applicability Statement</span></span>](#16-applicability-statement)
    -   [<span data-ttu-id="cbf24-114">1.7 Control de versiones y negociación de funcionalidad</span><span class="sxs-lookup"><span data-stu-id="cbf24-114">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
    -   [<span data-ttu-id="cbf24-115">1.8 Campos extensibles por el proveedor</span><span class="sxs-lookup"><span data-stu-id="cbf24-115">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
    -   [<span data-ttu-id="cbf24-116">1.9 Asignaciones de estándares</span><span class="sxs-lookup"><span data-stu-id="cbf24-116">1.9 Standards Assignments</span></span>](#19-standards-assignments)
-   [<span data-ttu-id="cbf24-117">2 Mensajes</span><span class="sxs-lookup"><span data-stu-id="cbf24-117">2 Messages</span></span>](#2-messages)
    -   [<span data-ttu-id="cbf24-118">2.1 Transporte</span><span class="sxs-lookup"><span data-stu-id="cbf24-118">2.1 Transport</span></span>](#21-transport)
    -   [<span data-ttu-id="cbf24-119">2.2 Sintaxis de mensajes</span><span class="sxs-lookup"><span data-stu-id="cbf24-119">2.2 Message Syntax</span></span>](#22-message-syntax)
-   [<span data-ttu-id="cbf24-120">3 Detalles del protocolo</span><span class="sxs-lookup"><span data-stu-id="cbf24-120">3 Protocol Details</span></span>](#3-protocol-details)
    -   [<span data-ttu-id="cbf24-121">3.1 Detalles del servidor</span><span class="sxs-lookup"><span data-stu-id="cbf24-121">3.1 Server Details</span></span>](#31-server-details)
    -   [<span data-ttu-id="cbf24-122">3.2 Detalles del cliente</span><span class="sxs-lookup"><span data-stu-id="cbf24-122">3.2 Client Details</span></span>](#32-client-details)
-   [<span data-ttu-id="cbf24-123">4 Ejemplos de protocolo</span><span class="sxs-lookup"><span data-stu-id="cbf24-123">4 Protocol Examples</span></span>](#4-protocol-examples)
    -   [<span data-ttu-id="cbf24-124">4.1 Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="cbf24-124">4.1 Example 1</span></span>](#41-example-1)
    -   [<span data-ttu-id="cbf24-125">4.2 Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="cbf24-125">4.2 Example 2</span></span>](#42-example-2)
-   [<span data-ttu-id="cbf24-126">5 Seguridad</span><span class="sxs-lookup"><span data-stu-id="cbf24-126">5 Security</span></span>](#5-security)
    -   [<span data-ttu-id="cbf24-127">5.1 Consideraciones de seguridad para los implementadores</span><span class="sxs-lookup"><span data-stu-id="cbf24-127">5.1 Security Considerations for Implementers</span></span>](#51-security-considerations-for-implementers)
    -   [<span data-ttu-id="cbf24-128">5.2 Índice de parámetros de seguridad</span><span class="sxs-lookup"><span data-stu-id="cbf24-128">5.2 Index of Security Parameters</span></span>](#52-index-of-security-parameters)
-   [<span data-ttu-id="cbf24-129">6 Índice del comportamiento específico de la versión</span><span class="sxs-lookup"><span data-stu-id="cbf24-129">6 Index of Version Specific Behavior</span></span>](#6-index-of-version-specific-behavior)

<span data-ttu-id="cbf24-130">Este documento es una especificación del protocolo content indexing Service.</span><span class="sxs-lookup"><span data-stu-id="cbf24-130">This document is a specification of the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="cbf24-131">La documentación del Programa de protocolo de servidor de grupo de trabajo (WSPP) está pensada para usarse junto con la documentación de estándares públicos, el arte de programación de red y los conceptos de sistemas distribuidos del grupo de trabajo de Windows, y supone que el lector está familiarizado con el material mencionado anteriormente o tiene acceso inmediato a él.</span><span class="sxs-lookup"><span data-stu-id="cbf24-131">The Workgroup Server Protocol Program (WSPP) documentation is intended for use in conjunction with public standards documentation, network programming art, and Windows workgroup distributed systems concepts, and assumes that the reader either is familiar with the aforementioned material or has immediate access to it.</span></span>

<span data-ttu-id="cbf24-132">Una especificación del protocolo WSPP no requiere el uso de herramientas de programación o entornos de programación de Microsoft para que un licenciado desarrolle una implementación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-132">A WSPP protocol specification does not require the use of Microsoft programming tools or programming environments in order for a Licensee to develop an implementation.</span></span> <span data-ttu-id="cbf24-133">Los licencias que tienen acceso a entornos y herramientas de programación de Microsoft son libres de aprovecharlas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-133">Licensees who have access to Microsoft programming tools and environments are free to take advantage of them.</span></span>

## <a name="1-introduction"></a><span data-ttu-id="cbf24-134">1 Introducción</span><span class="sxs-lookup"><span data-stu-id="cbf24-134">1 Introduction</span></span>

-   [<span data-ttu-id="cbf24-135">1.1 Glosario</span><span class="sxs-lookup"><span data-stu-id="cbf24-135">1.1 Glossary</span></span>](#11-glossary)
-   [<span data-ttu-id="cbf24-136">1.2 Referencias</span><span class="sxs-lookup"><span data-stu-id="cbf24-136">1.2 References</span></span>](#12-references)
-   [<span data-ttu-id="cbf24-137">Introducción al protocolo 1.3 (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="cbf24-137">1.3 Protocol Overview (Synopsis)</span></span>](#13-protocol-overview-synopsis)
-   [<span data-ttu-id="cbf24-138">1.4 Relación con otros protocolos</span><span class="sxs-lookup"><span data-stu-id="cbf24-138">1.4 Relationship to Other Protocols</span></span>](#14-relationship-to-other-protocols)
-   [<span data-ttu-id="cbf24-139">1.5 Requisitos previos y condiciones previas</span><span class="sxs-lookup"><span data-stu-id="cbf24-139">1.5 Prerequisites and Preconditions</span></span>](#15-prerequisites-and-preconditions)
-   [<span data-ttu-id="cbf24-140">1.6 Declaración de aplicabilidad</span><span class="sxs-lookup"><span data-stu-id="cbf24-140">1.6 Applicability Statement</span></span>](#16-applicability-statement)
-   [<span data-ttu-id="cbf24-141">1.7 Control de versiones y negociación de funcionalidad</span><span class="sxs-lookup"><span data-stu-id="cbf24-141">1.7 Versioning and Capability Negotiation</span></span>](#17-versioning-and-capability-negotiation)
-   [<span data-ttu-id="cbf24-142">1.8 Campos extensibles por el proveedor</span><span class="sxs-lookup"><span data-stu-id="cbf24-142">1.8 Vendor-Extensible Fields</span></span>](#18-vendor-extensible-fields)
-   [<span data-ttu-id="cbf24-143">1.9 Asignaciones de estándares</span><span class="sxs-lookup"><span data-stu-id="cbf24-143">1.9 Standards Assignments</span></span>](#19-standards-assignments)

### <a name="11-glossary"></a><span data-ttu-id="cbf24-144">1.1 Glosario</span><span class="sxs-lookup"><span data-stu-id="cbf24-144">1.1 Glossary</span></span>

> [!Note]  
> <span data-ttu-id="cbf24-145">Los términos siguientes se definen en la sección Glosario de \[ MS-SYS \] :</span><span class="sxs-lookup"><span data-stu-id="cbf24-145">The following terms are defined in the Glossary section of \[MS-SYS\]:</span></span>
>
> -   <span data-ttu-id="cbf24-146">GUID</span><span class="sxs-lookup"><span data-stu-id="cbf24-146">GUID</span></span>
> -   <span data-ttu-id="cbf24-147">Little Endian</span><span class="sxs-lookup"><span data-stu-id="cbf24-147">Little Endian</span></span>
> -   <span data-ttu-id="cbf24-148">Canalización con nombre</span><span class="sxs-lookup"><span data-stu-id="cbf24-148">Named Pipe</span></span>
> -   <span data-ttu-id="cbf24-149">Path</span><span class="sxs-lookup"><span data-stu-id="cbf24-149">Path</span></span>

 

<span data-ttu-id="cbf24-150">**Enlace:** solicitud para incluir una columna determinada **en** un conjunto de **filas devuelto.**</span><span class="sxs-lookup"><span data-stu-id="cbf24-150">**Binding**: A request to include a particular **column** in a returned **rowset** .</span></span> <span data-ttu-id="cbf24-151">El **enlace** especifica una propiedad que se va a incluir en los resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cbf24-151">The **binding** specifies a property to be included in the search results.</span></span>

<span data-ttu-id="cbf24-152">**Marcador:** marcador que identifica de forma única una fila dentro de un conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-152">**Bookmark**: A marker that uniquely identifies a row within a set of rows.</span></span>

<span data-ttu-id="cbf24-153">**Catálogo:** unidad de nivel superior de la organización en el servicio de indexación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-153">**Catalog**: The highest-level unit of organization in the indexing service.</span></span> <span data-ttu-id="cbf24-154">Representa un conjunto de documentos indexados en los que se pueden ejecutar consultas mediante el protocolo content indexing Service.</span><span class="sxs-lookup"><span data-stu-id="cbf24-154">It represents a set of indexed documents against which queries can be executed using the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="cbf24-155">**Categoría:** una agrupación jerárquica de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-155">**Category**: A hierarchical grouping of rows.</span></span> <span data-ttu-id="cbf24-156">Por ejemplo, un resultado de consulta que contiene columnas de autor y título se puede clasificar en función del autor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-156">For example, a query result containing author and title columns can be categorized based on author.</span></span> <span data-ttu-id="cbf24-157">Cada grupo de filas que contiene el mismo valor para author constituiría una categoría.</span><span class="sxs-lookup"><span data-stu-id="cbf24-157">Each group of rows containing the same value for author would constitute a category.</span></span>

<span data-ttu-id="cbf24-158">**Capítulo:** intervalo de **filas dentro** de un conjunto de **filas** .</span><span class="sxs-lookup"><span data-stu-id="cbf24-158">**Chapter** : A range of **rows** within a set of **rows** .</span></span>

<span data-ttu-id="cbf24-159">**Columna**: contenedor de un único tipo de información de una **fila.**</span><span class="sxs-lookup"><span data-stu-id="cbf24-159">**Column**: The container for a single type of information in a **row** .</span></span> <span data-ttu-id="cbf24-160">Las columnas se asignan a nombres de propiedad y especifican qué propiedades se usan para los elementos del árbol **de** comandos de la consulta **de** búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cbf24-160">Columns map to property names, and specify which properties are used for the search query's **command** **tree** elements.</span></span>

<span data-ttu-id="cbf24-161">**Árbol de comandos:** combinación de **restricciones,** **categorías** **y** criterios de ordenación especificados para la consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cbf24-161">**Command Tree**: A combination of **restrictions** , **categories** , and **sort orders** specified for the search query.</span></span>

<span data-ttu-id="cbf24-162">**Cursor:** entidad que se usa como mecanismo  para trabajar con  una fila o un pequeño bloque de filas a la vez en un conjunto de datos devuelto en un conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-162">**Cursor**: An entity that is used as a mechanism to work with one **row** or a small block of **rows** at a time in a set of data returned in a result set.</span></span> <span data-ttu-id="cbf24-163">Un **cursor** se coloca en una sola **fila dentro** del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-163">A **cursor** is positioned on a single **row** within the result set.</span></span> <span data-ttu-id="cbf24-164">Una vez **que el cursor** se coloca en una fila, se pueden realizar operaciones en esa fila o en un bloque de filas a partir de esa posición.  </span><span class="sxs-lookup"><span data-stu-id="cbf24-164">After the **cursor** is positioned on a row, operations can be performed on that **row** , or on a block of **rows** starting at that position.</span></span>

<span data-ttu-id="cbf24-165">**Identificador:** token que se puede usar para identificar y acceder a **cursores,** **capítulos** y **marcadores.**</span><span class="sxs-lookup"><span data-stu-id="cbf24-165">**Handle**: A token that can be used to identify and access **cursors** , **chapters** , and **bookmarks** .</span></span>

<span data-ttu-id="cbf24-166">**Índice:** estructura persistente que contiene el contenido de texto que un servicio de indexación extrayó de **los archivos.**</span><span class="sxs-lookup"><span data-stu-id="cbf24-166">**Index**: A persistent structure that contains the text content pulled out of files by an **indexing service** .</span></span> <span data-ttu-id="cbf24-167">Esto incluye la lista de palabras, que se almacenan junto con el nombre de archivo que contiene, la ubicación de la palabra y **la configuración regional.**</span><span class="sxs-lookup"><span data-stu-id="cbf24-167">This includes the list of words, which are stored along with the containing file name, word location, and **locale** .</span></span>

<span data-ttu-id="cbf24-168">**Indexación:** proceso de extracción de texto y propiedades de archivos y almacenamiento de los valores extraídos en los índices **(para** texto) y la caché de propiedades **(para** propiedades).</span><span class="sxs-lookup"><span data-stu-id="cbf24-168">**Indexing**: The process of extracting text and properties from files and storing the extracted values into the **indexes** (for text), and the **property cache** (for properties).</span></span>

<span data-ttu-id="cbf24-169">**Servicio de indexación:** servicio que crea **catálogos indexados** para el contenido y las propiedades de los sistemas de archivos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-169">**Indexing Service**: A service that creates indexed **catalogs** for the contents and properties of file systems.</span></span> <span data-ttu-id="cbf24-170">Las aplicaciones pueden buscar en los catálogos información de los archivos del sistema de archivos indexados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-170">Applications can search the catalogs for information from the files on the indexed file system.</span></span>

<span data-ttu-id="cbf24-171">**Configuración regional:** identificador, como se especifica en el Apéndice A de \[ MS-GPSI, que especifica \] las preferencias relacionadas con el idioma.</span><span class="sxs-lookup"><span data-stu-id="cbf24-171">**Locale**: An identifier, as specified in \[MS-GPSI\] Appendix A, that specifies preferences related to language.</span></span> <span data-ttu-id="cbf24-172">Estas preferencias indican cómo se va a dar formato a las fechas y horas, los elementos se ordenan alfabéticamente, las cadenas se van a comparar, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-172">These preferences indicate how dates and times are to be formatted, items are to be sorted alphabetically, strings are to be compared, and so on.</span></span>

<span data-ttu-id="cbf24-173">**Consulta de lenguaje natural:** consulta construida con lenguaje humano en lugar de sintaxis de consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-173">**Natural Language Query**: A query constructed using human language instead of query syntax.</span></span>

<span data-ttu-id="cbf24-174">**Palabra ruido:** palabra que el servicio de indexación omite cuando está presente en las **restricciones especificadas** para la consulta de búsqueda porque tiene poco valor discriminatorio.</span><span class="sxs-lookup"><span data-stu-id="cbf24-174">**Noise word**: A word that is ignored by the indexing service when present in the **restrictions** specified for the search query because it has little discriminatory value.</span></span> <span data-ttu-id="cbf24-175">Entre los ejemplos en inglés se incluyen "a", "and" y "the".</span><span class="sxs-lookup"><span data-stu-id="cbf24-175">English examples include "a", "and" and "the".</span></span>

<span data-ttu-id="cbf24-176">**Caché de propiedades:** caché de propiedades de archivo extraídas por un **servicio de indexación.**</span><span class="sxs-lookup"><span data-stu-id="cbf24-176">**Property Cache**: A cache of file properties extracted by an **indexing service** .</span></span>

<span data-ttu-id="cbf24-177">**Indexación de** propiedades: proceso  de  creación de un índice de propiedades de tipo de valor de un documento, incluidos el autor, el asunto, el tipo, el recuento de palabras, el recuento de páginas impresas y cualquier otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-177">**Property Indexing**: The process of creating an **index** of **value-type properties** of a document, including author, subject, type, word count, printed page count, and any other properties.</span></span>

<span data-ttu-id="cbf24-178">**Restricción:** conjunto de condiciones que un archivo debe cumplir para incluirse en los resultados de búsqueda devueltos por el servicio **de indexación** en respuesta a una consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cbf24-178">**Restriction**: A set of conditions that a file must meet to be included in the search results returned by the **indexing service** in response to a search query.</span></span> <span data-ttu-id="cbf24-179">Una **restricción** limita el foco de una consulta de búsqueda, limitando los archivos que el servicio de **indexación** incluirá en los resultados de la búsqueda a solo aquellos que coincidan con las condiciones.</span><span class="sxs-lookup"><span data-stu-id="cbf24-179">A **restriction** narrows the focus of a search query, limiting the files that the **indexing service** will include in the search results to only those that match the conditions.</span></span>

<span data-ttu-id="cbf24-180">**Fila:** colección de columnas **que** contiene los valores de propiedad que describen un único archivo del conjunto de archivos que coincidieron con las **restricciones especificadas** en la consulta de búsqueda enviada al servicio **de indexación.**</span><span class="sxs-lookup"><span data-stu-id="cbf24-180">**Row**: The collection of **columns** , containing the property values that describe a single file from the set of files that matched the **restrictions** specified in the search query submitted to the **indexing service** .</span></span>

<span data-ttu-id="cbf24-181">**Conjunto de filas:** conjunto de **filas devuelto en** los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cbf24-181">**Rowset**: A set of **rows** returned in the search results.</span></span>

<span data-ttu-id="cbf24-182">**Criterio de** ordenación: conjunto de reglas de una consulta de búsqueda que definen el orden de las filas en el resultado de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cbf24-182">**Sort Order**: The set of rules in a search query that define the ordering of rows in the search result.</span></span> <span data-ttu-id="cbf24-183">Cada regla consta de una propiedad (nombre, tamaño, etc.) y una dirección para la ordenación (ascendente o descendente).</span><span class="sxs-lookup"><span data-stu-id="cbf24-183">Each rule consists of a property (name, size, etc.) and a direction for the ordering (ascending or descending).</span></span> <span data-ttu-id="cbf24-184">Varias reglas se aplican secuencialmente</span><span class="sxs-lookup"><span data-stu-id="cbf24-184">Multiple rules are applied sequentially</span></span>

<span data-ttu-id="cbf24-185">**Propiedad de tipo de texto:** propiedad que describe el contenido de un documento y solo tiene texto sin formato asociado a su nombre.</span><span class="sxs-lookup"><span data-stu-id="cbf24-185">**Text-type Property**: A property that describes the content of a document and has only unformatted text associated with its name.</span></span>

<span data-ttu-id="cbf24-186">**Propiedad de tipo de valor:** propiedad que describe un único atributo de un documento completo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-186">**Value-type Property**: A property that describes a single attribute of an entire document.</span></span> <span data-ttu-id="cbf24-187">Una propiedad de tipo de valor tiene un identificador de tipo de datos y un valor de ese tipo de datos asociado a su nombre.</span><span class="sxs-lookup"><span data-stu-id="cbf24-187">A value-type property has a data type ID and a value of that data type associated with its name.</span></span>

<span data-ttu-id="cbf24-188">**Raíz virtual:** ruta de acceso alternativa a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-188">**Virtual Root**: An alternate path to a folder.</span></span> <span data-ttu-id="cbf24-189">Una carpeta física puede tener cero o más raíces virtuales.</span><span class="sxs-lookup"><span data-stu-id="cbf24-189">A physical folder can have zero or more virtual roots.</span></span> <span data-ttu-id="cbf24-190">Las rutas de acceso que comienzan con una raíz virtual se denominan rutas de acceso virtuales.</span><span class="sxs-lookup"><span data-stu-id="cbf24-190">Paths beginning with a virtual root are called virtual paths.</span></span> <span data-ttu-id="cbf24-191">Por ejemplo, /server/vanityroot podría ser una raíz virtual de C: \\ carpeta \\ web de \\ IIS1.</span><span class="sxs-lookup"><span data-stu-id="cbf24-191">For example, /server/vanityroot might be a virtual root of C:\\IIS\\web\\folder1.</span></span> <span data-ttu-id="cbf24-192">A continuación, el archivo C: carpeta web de IIS1default.htm una ruta de acceso \\ \\ virtual de \\ \\ /server/vanityroot/default.htm.</span><span class="sxs-lookup"><span data-stu-id="cbf24-192">Then the file C:\\IIS\\web\\folder1\\default.htm would have a virtual path of /server/vanityroot/default.htm.</span></span>

<span data-ttu-id="cbf24-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT:** estos términos (en todos los límites) se usan como se describe en \[ RFC2119 \] .</span><span class="sxs-lookup"><span data-stu-id="cbf24-193">**MAY, SHOULD, MUST, SHOULD NOT, MUST NOT**: These terms (in all caps) are used as described in \[RFC2119\].</span></span> <span data-ttu-id="cbf24-194">Todas las instrucciones de comportamiento opcional utilizan MAY, SHOULD o SHOULD NOT.</span><span class="sxs-lookup"><span data-stu-id="cbf24-194">All statements of optional behavior use either MAY, SHOULD, or SHOULD NOT.</span></span>

### <a name="12-references"></a><span data-ttu-id="cbf24-195">1.2 Referencias</span><span class="sxs-lookup"><span data-stu-id="cbf24-195">1.2 References</span></span>

### <a name="121-normative-references"></a><span data-ttu-id="cbf24-196">1.2.1 Referencias de normativa</span><span class="sxs-lookup"><span data-stu-id="cbf24-196">1.2.1 Normative References</span></span>

<span data-ttu-id="cbf24-197">\[IEEE754 \] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, octubre de 1985, https://standards.ieee.org/standard/754-1985.html</span><span class="sxs-lookup"><span data-stu-id="cbf24-197">\[IEEE754\] Institute of Electrical and Electronics Engineers, "Standard for Binary Floating-Point Arithmetic", IEEE 754-1985, October 1985, https://standards.ieee.org/standard/754-1985.html</span></span>

<span data-ttu-id="cbf24-198">\[MS-DCOM \] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", junio de 2006.</span><span class="sxs-lookup"><span data-stu-id="cbf24-198">\[MS-DCOM\] Microsoft Corporation, "Distributed Component Object Model Remote Protocols", June 2006.</span></span>

<span data-ttu-id="cbf24-199">\[MS-GPSI \] Microsoft Corporation, "Directiva de grupo de Instalación de software Extension", junio de 2006.</span><span class="sxs-lookup"><span data-stu-id="cbf24-199">\[MS-GPSI\] Microsoft Corporation, "Group Policy Software Installation Extension", June 2006.</span></span>

<span data-ttu-id="cbf24-200">\[MS-SMB \] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions", mayo de 2006.</span><span class="sxs-lookup"><span data-stu-id="cbf24-200">\[MS-SMB\] Microsoft Corporation, "Microsoft Server Message Block (SMB) Protocol and Extensions," May 2006.</span></span>

<span data-ttu-id="cbf24-201">\[MS-SYS \] Microsoft Corporation, "System Overview v4", julio de 2006.</span><span class="sxs-lookup"><span data-stu-id="cbf24-201">\[MS-SYS\] Microsoft Corporation, "System Overview v4", July 2006.</span></span>

<span data-ttu-id="cbf24-202">\[SALTON \] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span><span class="sxs-lookup"><span data-stu-id="cbf24-202">\[SALTON\] Salton, G., "Automatic Text Processing: The Transformation Analysis and Retrieval of Information by Computer", 1988, ISBN 0-201-2227-8.</span></span>

<span data-ttu-id="cbf24-203">\[UNICODE \] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span><span class="sxs-lookup"><span data-stu-id="cbf24-203">\[UNICODE\] The Unicode Consortium, "The Unicode Standard, Version 2.0", 1996, https://www.unicode.org</span></span>

### <a name="122-informative-references"></a><span data-ttu-id="cbf24-204">1.2.2 Referencias informativas</span><span class="sxs-lookup"><span data-stu-id="cbf24-204">1.2.2 Informative References</span></span>

<span data-ttu-id="cbf24-205">\[MSDN-OLEDB \] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp .</span><span class="sxs-lookup"><span data-stu-id="cbf24-205">\[MSDN-OLEDB\] Microsoft Corporation, OLE DB, https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp.</span></span>

<span data-ttu-id="cbf24-206">\[MSDN-QUERYERR \] Microsoft Corporation, Query-Execution, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span><span class="sxs-lookup"><span data-stu-id="cbf24-206">\[MSDN-QUERYERR\] Microsoft Corporation, Query-Execution Values, https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp</span></span>

### <a name="13-protocol-overview-synopsis"></a><span data-ttu-id="cbf24-207">Introducción al protocolo 1.3 (Synopsis)</span><span class="sxs-lookup"><span data-stu-id="cbf24-207">1.3 Protocol Overview (Synopsis)</span></span>

<span data-ttu-id="cbf24-208">Un servicio **de indexación de contenido** ayuda a organizar de forma eficaz las características extraídas de una colección de documentos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-208">A content **indexing service** helps efficiently organize the extracted features of a collection of documents.</span></span> <span data-ttu-id="cbf24-209">El Protocolo de servicio de indexación de contenido (CISP) permite a un cliente comunicarse con un servidor que hospeda un servicio de indexación para emitir consultas y permitir que un administrador administre el servidor de indexación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-209">The Content Indexing Service Protocol (CISP) allows a client to communicate with a server hosting an indexing service to issue queries and to allow an administrator to manage the indexing server.</span></span>

<span data-ttu-id="cbf24-210">Al procesar archivos, un servicio de indexación analiza un conjunto de documentos  y reorganiza su contenido de forma que las propiedades de esos documentos se puedan devolver de forma eficaz en respuesta a las consultas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-210">When processing files, an indexing service analyzes a set of documents and reorganizes their content in such a way that **properties** of those documents can be efficiently returned in response to queries.</span></span> <span data-ttu-id="cbf24-211">Una colección de documentos que se pueden consultar consta de un **catálogo .**</span><span class="sxs-lookup"><span data-stu-id="cbf24-211">A collection of documents that can be queried comprises a **catalog** .</span></span> <span data-ttu-id="cbf24-212">Un catálogo puede contener un **índice (para** referencia rápida al texto) y una caché de **propiedades** (para la recuperación rápida de valores de propiedad).</span><span class="sxs-lookup"><span data-stu-id="cbf24-212">A catalog may contain an **index** (for quick reference to text) and a **property cache** (for quick retrieval of property values).</span></span>

<span data-ttu-id="cbf24-213">Conceptualmente, un catálogo consta de una "tabla" lógica de propiedades con el texto o valor y la configuración regional correspondiente almacenada en **columnas** de la tabla.</span><span class="sxs-lookup"><span data-stu-id="cbf24-213">Conceptually, a catalog consists of a logical "table" of properties with the text or value and corresponding locale stored in **columns** of the table.</span></span> <span data-ttu-id="cbf24-214">Cada "fila" de la tabla corresponde a un documento independiente en el ámbito del catálogo y cada "columna" de la tabla corresponde a una propiedad .</span><span class="sxs-lookup"><span data-stu-id="cbf24-214">Each "row" of the table corresponds to a separate document in the scope of the catalog and each "column" of the table corresponds to a property.</span></span>

<span data-ttu-id="cbf24-215">Las tareas específicas realizadas por CISP se agrupan en dos áreas funcionales:</span><span class="sxs-lookup"><span data-stu-id="cbf24-215">The specific tasks performed by CISP are grouped into two functional areas:</span></span>

-   <span data-ttu-id="cbf24-216">Administración remota de catálogos de servicios de indexación,</span><span class="sxs-lookup"><span data-stu-id="cbf24-216">Remote administration of indexing service catalogs,</span></span>
-   <span data-ttu-id="cbf24-217">Consulta remota de catálogos de servicios de indexación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-217">Remote querying of indexing service catalogs.</span></span>

### <a name="131-remote-administration-tasks"></a><span data-ttu-id="cbf24-218">1.3.1 Tareas de administración remota</span><span class="sxs-lookup"><span data-stu-id="cbf24-218">1.3.1 Remote Administration Tasks</span></span>

<span data-ttu-id="cbf24-219">CISP habilita las siguientes tareas de administración del catálogo de servicios de indexación desde un cliente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-219">CISP enables the following indexing service catalog management tasks from a client:</span></span>

-   <span data-ttu-id="cbf24-220">Consulte el estado actual de un catálogo de servicios de indexación en el servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-220">Query the current state of an indexing service catalog on the server.</span></span>
-   <span data-ttu-id="cbf24-221">Actualice el estado de un catálogo de servicios de indexación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-221">Update the state of an indexing service catalog.</span></span>
-   <span data-ttu-id="cbf24-222">Inicie el proceso de indexación para un conjunto determinado de archivos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-222">Launch the indexing process for a particular set of files.</span></span>
-   <span data-ttu-id="cbf24-223">Inicie la optimización de un índice para mejorar el rendimiento de las consultas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-223">Initiate optimization of an index in order to improve query performance.</span></span>

<span data-ttu-id="cbf24-224">Todas las tareas de administración remota siguen un modelo sencillo de solicitud/respuesta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-224">All remote administration tasks follow a simple request/response model.</span></span> <span data-ttu-id="cbf24-225">No se mantiene ningún estado en el cliente para ninguna llamada de administración y las llamadas administrativas se pueden realizar en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="cbf24-225">No state is maintained on the client for any administration call and administrative calls can be made in any order.</span></span>

### <a name="132-remote-querying"></a><span data-ttu-id="cbf24-226">1.3.2 Consulta remota</span><span class="sxs-lookup"><span data-stu-id="cbf24-226">1.3.2 Remote Querying</span></span>

<span data-ttu-id="cbf24-227">CISP permite a los clientes realizar consultas de búsqueda en un servidor remoto que hospeda un servicio de indexación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-227">CISP enables clients to perform search queries against a remote server hosting an indexing service.</span></span>

<span data-ttu-id="cbf24-228">El envío de una consulta de búsqueda es un proceso de varios pasos iniciado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-228">Sending a search query is a multi-step process initiated by the client.</span></span> <span data-ttu-id="cbf24-229">Los pasos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="cbf24-229">The steps are as follows:</span></span>

1.  <span data-ttu-id="cbf24-230">El cliente solicita una conexión a un servidor que hospeda un servicio de indexación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-230">The client requests a connection to a server hosting an indexing service.</span></span>
2.  <span data-ttu-id="cbf24-231">El cliente envía los parámetros para la consulta de búsqueda, que incluyen:</span><span class="sxs-lookup"><span data-stu-id="cbf24-231">The client sends the parameters for the search query, which include:</span></span>
    -   <span data-ttu-id="cbf24-232">Restricciones para especificar qué documentos se van a incluir o excluir de los **resultados** de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cbf24-232">The **restrictions** to specify which documents are to be included and/or excluded from the search results.</span></span>
    -   <span data-ttu-id="cbf24-233">Orden en el que se van a devolver los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cbf24-233">The order in which the search results are to be returned.</span></span>
    -   <span data-ttu-id="cbf24-234">Columnas que se devolverán en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-234">The columns to be returned in the result set.</span></span>
    -   <span data-ttu-id="cbf24-235">Número máximo de **filas que** se deben devolver para la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-235">The maximum number of **rows** that should be returned for the query.</span></span>
    -   <span data-ttu-id="cbf24-236">Tiempo máximo para la ejecución de consultas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-236">The maximum time for query execution.</span></span>

        <span data-ttu-id="cbf24-237">Una vez que el servidor ha reconocido la solicitud del cliente para iniciar la consulta, el cliente puede solicitar información de estado sobre la consulta, pero este no es un paso necesario.</span><span class="sxs-lookup"><span data-stu-id="cbf24-237">Once the server has acknowledged the client's request to initiate the query, the client can request status information about the query, but this is not a required step.</span></span>

3.  <span data-ttu-id="cbf24-238">A continuación, el cliente especifica qué propiedades debe incluir el servidor en los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cbf24-238">The client then specifies which properties the server should include in the search results.</span></span>
4.  <span data-ttu-id="cbf24-239">El cliente solicita un conjunto de resultados del servidor y el servidor responde enviando al cliente los valores de propiedad de los archivos que se incluyeron en los resultados de la consulta de búsqueda del cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-239">The client requests a result set from the server, and the server responds by sending the client the property values for files that were included in the results for the client's search query.</span></span> <span data-ttu-id="cbf24-240">Si el valor de una propiedad es demasiado grande para caber en un búfer de respuesta único, el servidor no enviará la propiedad, sino que establecerá el estado de la propiedad en diferido.</span><span class="sxs-lookup"><span data-stu-id="cbf24-240">If the value of a property is too large to fit in a single response buffer the server will not send the property but instead will set the property status to deferred.</span></span> <span data-ttu-id="cbf24-241">A continuación, el cliente solicita el valor de propiedad por separado mediante una serie de solicitudes para fragmentos sucesivos del valor y, a continuación, reanuda la solicitud de otros valores.</span><span class="sxs-lookup"><span data-stu-id="cbf24-241">The client then requests the property value separately using a series of requests for successive chunks of the value, and then resumes requesting other values.</span></span>
5.  <span data-ttu-id="cbf24-242">Una vez que el cliente ha terminado con la consulta de búsqueda y ya no requiere resultados adicionales, el cliente se pone en contacto con el servidor para liberar la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-242">Once the client is finished with the search query and no longer requires additional results, the client contacts the server to release the query.</span></span>
6.  <span data-ttu-id="cbf24-243">Una vez que el servidor ha publicado la consulta, el cliente puede enviar una solicitud para desconectarse del servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-243">Once the server has released the query, the client may send a request to disconnect from the server.</span></span> <span data-ttu-id="cbf24-244">A continuación, se cierra la conexión.</span><span class="sxs-lookup"><span data-stu-id="cbf24-244">The connection is then closed.</span></span> <span data-ttu-id="cbf24-245">Como alternativa, el cliente puede emitir otra consulta y repetir la secuencia del paso 2.</span><span class="sxs-lookup"><span data-stu-id="cbf24-245">Alternatively, the client may issue another query and repeat the sequence from the step 2.</span></span>

<span data-ttu-id="cbf24-246">Comportamiento de Windows: este protocolo se implementa en Windows 2000, Windows XP, Windows Server 2003 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cbf24-246">Windows Behavior: This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span>

### <a name="14-relationship-to-other-protocols"></a><span data-ttu-id="cbf24-247">1.4 Relación con otros protocolos</span><span class="sxs-lookup"><span data-stu-id="cbf24-247">1.4 Relationship to Other Protocols</span></span>

<span data-ttu-id="cbf24-248">CISP se basa en el protocolo \[ SMB MS-SMB \] para el transporte de mensajes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-248">The CISP relies on the SMB \[MS-SMB\] protocol for message transport.</span></span> <span data-ttu-id="cbf24-249">Ningún otro protocolo depende directamente del protocolo del servicio de indexación de contenido.</span><span class="sxs-lookup"><span data-stu-id="cbf24-249">No other protocol depends directly on the Content Indexing Service Protocol.</span></span>

<span data-ttu-id="cbf24-250">*Comportamiento de Windows: las aplicaciones suelen interactuar con un contenedor de interfaz OLE DB \[ MSDN-OLEDB (por ejemplo, un cliente de protocolo) y no \] directamente con el protocolo.*</span><span class="sxs-lookup"><span data-stu-id="cbf24-250">*Windows Behavior: Applications typically interact with an OLE DB interface wrapper \[MSDN-OLEDB\] (e.g., a protocol client) and not directly with the protocol.*</span></span>

### <a name="15-prerequisites-and-preconditions"></a><span data-ttu-id="cbf24-251">1.5 Requisitos previos y condiciones previas</span><span class="sxs-lookup"><span data-stu-id="cbf24-251">1.5 Prerequisites and Preconditions</span></span>

<span data-ttu-id="cbf24-252">Se supone que el cliente ha obtenido el nombre del servidor y un nombre de catálogo antes de invocar este protocolo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-252">It is assumed that the client has obtained the name of the server and a catalog name before this protocol is invoked.</span></span> <span data-ttu-id="cbf24-253">La forma en que un cliente lo hace está fuera del ámbito de esta especificación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-253">How a client does this is outside of the scope of this specification.</span></span>

<span data-ttu-id="cbf24-254">También se supone que el cliente y el servidor tienen una asociación de seguridad que se puede usar con canalizaciones \[ con nombre MS-SMB. \]</span><span class="sxs-lookup"><span data-stu-id="cbf24-254">It is also assumed that the client and server have a security association usable with named pipes \[MS-SMB\].</span></span>

### <a name="16-applicability-statement"></a><span data-ttu-id="cbf24-255">1.6 Declaración de aplicabilidad</span><span class="sxs-lookup"><span data-stu-id="cbf24-255">1.6 Applicability Statement</span></span>

<span data-ttu-id="cbf24-256">CISP está diseñado para consultar y administrar catálogos en un servidor remoto desde un cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-256">CISP is designed for querying and managing catalogs on a remote server from a client.</span></span> <span data-ttu-id="cbf24-257">CISP está en desuso en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cbf24-257">CISP is deprecated on Windows Vista.</span></span>

### <a name="17-versioning-and-capability-negotiation"></a><span data-ttu-id="cbf24-258">1.7 Control de versiones y negociación de funcionalidad</span><span class="sxs-lookup"><span data-stu-id="cbf24-258">1.7 Versioning and Capability Negotiation</span></span>

<span data-ttu-id="cbf24-259">Este protocolo no tiene mecanismos de control de versiones ni de negociación de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="cbf24-259">This protocol has no versioning or capability negotiation mechanisms.</span></span>

### <a name="18-vendor-extensible-fields"></a><span data-ttu-id="cbf24-260">1.8 Campos extensibles por el proveedor</span><span class="sxs-lookup"><span data-stu-id="cbf24-260">1.8 Vendor-Extensible Fields</span></span>

<span data-ttu-id="cbf24-261">Este protocolo usa HULT que son extensibles por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-261">This protocol uses HRESULTs which are vendor-extensible.</span></span> <span data-ttu-id="cbf24-262">Los proveedores pueden elegir sus propios valores para este campo, siempre que el bit C (0x20000000) se establezca como se especifica en la sección 4.1.1 de MS-SYS, lo que indica que es un código de \[ \] cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-262">Vendors are free to choose their own values for this field, as long as the C bit (0x20000000) is set as specified in Section 4.1.1 of \[MS-SYS\], indicating it is a customer code.</span></span>

<span data-ttu-id="cbf24-263">Este protocolo también usa valores NTSTATUS tomados del espacio numérico NTSTATUS definido en \[ MS-SYS \] .</span><span class="sxs-lookup"><span data-stu-id="cbf24-263">This protocol also uses NTSTATUS values taken from the NTSTATUS number space defined in \[MS-SYS\].</span></span> <span data-ttu-id="cbf24-264">Los proveedores DEBEN reutilizar esos valores con su significado indicado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-264">Vendors SHOULD reuse those values with their indicated meaning.</span></span> <span data-ttu-id="cbf24-265">La elección de cualquier otro valor corre el riesgo de colisión en el futuro.</span><span class="sxs-lookup"><span data-stu-id="cbf24-265">Choosing any other value runs the risk of a collision in the future.</span></span>

<span data-ttu-id="cbf24-266">*Comportamiento de Windows: Windows solo usa los valores especificados en la sección 4.1.3 \[ de MS-SYS. \]*</span><span class="sxs-lookup"><span data-stu-id="cbf24-266">*Windows Behavior: Windows only uses the values specified in Section 4.1.3 of \[MS-SYS\].*</span></span>

### <a name="181-property-ids"></a><span data-ttu-id="cbf24-267">1.8.1 IDs de propiedad</span><span class="sxs-lookup"><span data-stu-id="cbf24-267">1.8.1 Property IDs</span></span>

<span data-ttu-id="cbf24-268">Las propiedades se representan mediante los iDs conocidos como los de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-268">Properties are represented by IDs known as Property IDs.</span></span> <span data-ttu-id="cbf24-269">Cada propiedad debe tener un identificador único global.</span><span class="sxs-lookup"><span data-stu-id="cbf24-269">Each property must have a globally unique identifier.</span></span> <span data-ttu-id="cbf24-270">Este identificador consta de un **GUID** que representa una colección de propiedades denominada conjunto de propiedades más una cadena o un entero de 32 bits para identificar la propiedad dentro del conjunto.</span><span class="sxs-lookup"><span data-stu-id="cbf24-270">This identifier consists of a **GUID** representing a collection of properties called a property set plus either a string or 32-bit integer to identify the property within the set.</span></span> <span data-ttu-id="cbf24-271">Si se usa la forma de entero de id., los valores 0x00000000, 0xFFFFFFFF y 0xFFFFFFFE se consideran no válidos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-271">If the integer form of ID is used, then the values 0x00000000, 0xFFFFFFFF and 0xFFFFFFFE are considered invalid.</span></span>

<span data-ttu-id="cbf24-272">Los proveedores pueden garantizar que sus propiedades se definen de forma única colocándolas en un conjunto de propiedades definido por su propio GUID.</span><span class="sxs-lookup"><span data-stu-id="cbf24-272">Vendors can guarantee their properties are uniquely defined by placing them in a property set defined by their own GUID.</span></span>

### <a name="19-standards-assignments"></a><span data-ttu-id="cbf24-273">1.9 Asignaciones de estándares</span><span class="sxs-lookup"><span data-stu-id="cbf24-273">1.9 Standards Assignments</span></span>

<span data-ttu-id="cbf24-274">Este protocolo no tiene asignaciones de estándares, solo asignaciones privadas realizadas por Microsoft mediante procedimientos de asignación especificados en otros protocolos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-274">This protocol has no standards assignments, only private assignments made by Microsoft using allocation procedures specified in other protocols.</span></span>

<span data-ttu-id="cbf24-275">Microsoft ha asignado a este protocolo una canalización con nombre como se especifica en \[ MS-SMB. \]</span><span class="sxs-lookup"><span data-stu-id="cbf24-275">Microsoft has allocated this protocol a named pipe as specified in \[MS-SMB\].</span></span> <span data-ttu-id="cbf24-276">La asignación es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-276">The assignment is:</span></span>



| <span data-ttu-id="cbf24-277">Parámetro</span><span class="sxs-lookup"><span data-stu-id="cbf24-277">Parameter</span></span> | <span data-ttu-id="cbf24-278">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-278">Value</span></span>             | <span data-ttu-id="cbf24-279">Referencia</span><span class="sxs-lookup"><span data-stu-id="cbf24-279">Reference</span></span>  |
|-----------|-------------------|------------|
| <span data-ttu-id="cbf24-280">Nombre de canalización</span><span class="sxs-lookup"><span data-stu-id="cbf24-280">Pipe name</span></span> | <span data-ttu-id="cbf24-281">\\pipe \\ CI \_ PIPEDS</span><span class="sxs-lookup"><span data-stu-id="cbf24-281">\\pipe\\CI\_SKADS</span></span> | <span data-ttu-id="cbf24-282">\[MS-SMB\]</span><span class="sxs-lookup"><span data-stu-id="cbf24-282">\[MS-SMB\]</span></span> |



 

## <a name="2-messages"></a><span data-ttu-id="cbf24-283">2 Mensajes</span><span class="sxs-lookup"><span data-stu-id="cbf24-283">2 Messages</span></span>

-   [<span data-ttu-id="cbf24-284">2.1 Transporte</span><span class="sxs-lookup"><span data-stu-id="cbf24-284">2.1 Transport</span></span>](#21-transport)
-   [<span data-ttu-id="cbf24-285">2.2 Sintaxis de mensajes</span><span class="sxs-lookup"><span data-stu-id="cbf24-285">2.2 Message Syntax</span></span>](#22-message-syntax)

### <a name="21-transport"></a><span data-ttu-id="cbf24-286">2.1 Transporte</span><span class="sxs-lookup"><span data-stu-id="cbf24-286">2.1 Transport</span></span>

<span data-ttu-id="cbf24-287">Todos los mensajes DEBEN transportarse mediante una canalización con nombre, como se especifica en \[ MS-SMB. \]</span><span class="sxs-lookup"><span data-stu-id="cbf24-287">All messages MUST be transported using a named pipe, as specified in \[MS-SMB\].</span></span> <span data-ttu-id="cbf24-288">Se usa el siguiente nombre de canalización:</span><span class="sxs-lookup"><span data-stu-id="cbf24-288">The following pipe name is used:</span></span>

-   <span data-ttu-id="cbf24-289">\\pipe \\ CI \_ PIPEDS</span><span class="sxs-lookup"><span data-stu-id="cbf24-289">\\pipe\\CI\_SKADS</span></span>

<span data-ttu-id="cbf24-290">Este protocolo usa el protocolo de canalización con nombre SMB subyacente para recuperar la identidad del autor de la llamada que realizó la conexión como se especifica en la sección 2.2.8 de MS-SMB; el cliente DEBE establecer SECURITY IDENTIFICATION como \[ \] ImpersonationLevel en la solicitud para abrir la canalización con \_ nombre.</span><span class="sxs-lookup"><span data-stu-id="cbf24-290">This protocol uses the underlying SMB named pipe protocol to retrieve the identity of the caller that made the connection as specified in Section 2.2.8 of \[MS-SMB\]; the client MUST set SECURITY\_IDENTIFICATION as the ImpersonationLevel in the request to open the named pipe.</span></span>

### <a name="22-message-syntax"></a><span data-ttu-id="cbf24-291">2.2 Sintaxis de mensajes</span><span class="sxs-lookup"><span data-stu-id="cbf24-291">2.2 Message Syntax</span></span>

<span data-ttu-id="cbf24-292">Varias estructuras y mensajes de las secciones siguientes hacen referencia a los identificadores de capítulos o marcadores.</span><span class="sxs-lookup"><span data-stu-id="cbf24-292">Several structures and messages in the following sections refer to chapter or bookmark handles.</span></span> <span data-ttu-id="cbf24-293">Un identificador es una estructura opaca de 32 bits de longitud que identifica de forma única un capítulo o marcador.</span><span class="sxs-lookup"><span data-stu-id="cbf24-293">A handle is a 32-bit long opaque structure which uniquely identifies a chapter or bookmark.</span></span> <span data-ttu-id="cbf24-294">Normalmente, las aplicaciones cliente reciben valores de identificador a través de llamadas a métodos. sin embargo, hay varios valores conocidos que no es necesario obtener de un servidor, cuyo significado se especifica en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-294">Typically, client applications receive handle values via method calls; however there are several well known values which need not be obtained from a server, the meaning of which is specified in the following table:</span></span>



| <span data-ttu-id="cbf24-295">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-295">Value</span></span>                         | <span data-ttu-id="cbf24-296">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-296">Meaning</span></span>                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-297">Db \_ NULL \_ HCHAPTER 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-297">DB\_NULL\_HCHAPTER 0x00000000</span></span> | <span data-ttu-id="cbf24-298">Identificador de capítulo para el conjunto de filas sin cadena que contiene todos los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-298">A chapter handle to the unchaptered rowset, containing all query results.</span></span>    |
| <span data-ttu-id="cbf24-299">DBBMK \_ FIRST 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-299">DBBMK\_FIRST 0x00000001</span></span>       | <span data-ttu-id="cbf24-300">Identificador de marcador de un marcador que identifica la primera fila del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-300">A bookmark handle to a bookmark that identifies the first row in the rowset.</span></span> |
| <span data-ttu-id="cbf24-301">ÚLTIMO 0x00000002 DBBMK \_</span><span class="sxs-lookup"><span data-stu-id="cbf24-301">DBBMK\_LAST 0x00000002</span></span>        | <span data-ttu-id="cbf24-302">Identificador de marcador para un marcador que identifica la última fila del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-302">A bookmark handle to a bookmark that identifies the last row in the rowset.</span></span>  |



 

### <a name="221-structures"></a><span data-ttu-id="cbf24-303">2.2.1 Estructuras</span><span class="sxs-lookup"><span data-stu-id="cbf24-303">2.2.1 Structures</span></span>

<span data-ttu-id="cbf24-304">En esta sección se detallan las estructuras de datos definidas y usadas por CISP.</span><span class="sxs-lookup"><span data-stu-id="cbf24-304">This section details data structures that are defined and used by CISP.</span></span>

<span data-ttu-id="cbf24-305">Todos los enteros de 2, 4 y 8 bytes con signo y sin signo de las estructuras siguientes DEBEN transferirse en orden de bytes little-endian.</span><span class="sxs-lookup"><span data-stu-id="cbf24-305">All 2-, 4- and 8-byte signed and unsigned integers in the following structures MUST be transferred in little-endian byte order.</span></span>

<span data-ttu-id="cbf24-306">En la tabla siguiente se resumen las estructuras de datos definidas en esta sección.</span><span class="sxs-lookup"><span data-stu-id="cbf24-306">The following table summarizes the data structures defined in this section.</span></span>



| <span data-ttu-id="cbf24-307">Estructura</span><span class="sxs-lookup"><span data-stu-id="cbf24-307">Structure</span></span>                    | <span data-ttu-id="cbf24-308">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbf24-308">Description</span></span>                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-309">CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="cbf24-309">CBaseStorageVariant</span></span>          | <span data-ttu-id="cbf24-310">Contiene el valor en el que se va a realizar una operación de coincidencia para una propiedad especificada en una estructura CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="cbf24-310">Contains the value on which to perform a match operation for a property specified in a CPropertyRestriction structure.</span></span> |
| <span data-ttu-id="cbf24-311">SAFEARRAY, SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="cbf24-311">SAFEARRAY, SAFEARRAY2</span></span>        | <span data-ttu-id="cbf24-312">Contiene una matriz multidimensional.</span><span class="sxs-lookup"><span data-stu-id="cbf24-312">Contains a multidimensional array.</span></span>                                                                                     |
| <span data-ttu-id="cbf24-313">SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="cbf24-313">SAFEARRAYBOUND</span></span>               | <span data-ttu-id="cbf24-314">Representa los límites de una dimensión de una matriz especificada en una estructura SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="cbf24-314">Represents the bounds for a dimension of an array specified in a SAFEARRAY structure.</span></span>                                  |
| <span data-ttu-id="cbf24-315">CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="cbf24-315">CFullPropSpec</span></span>                | <span data-ttu-id="cbf24-316">Contiene una especificación de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-316">Contains a property specification.</span></span>                                                                                     |
| <span data-ttu-id="cbf24-317">CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-317">CContentRestriction</span></span>          | <span data-ttu-id="cbf24-318">Contiene una cadena que debe coincidir con un valor de propiedad en la caché de propiedades.</span><span class="sxs-lookup"><span data-stu-id="cbf24-318">Contains a string to match for a property value in the property cache.</span></span>                                                 |
| <span data-ttu-id="cbf24-319">CKey</span><span class="sxs-lookup"><span data-stu-id="cbf24-319">CKey</span></span>                         | <span data-ttu-id="cbf24-320">Contiene un valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-320">Contains a property value.</span></span>                                                                                             |
| <span data-ttu-id="cbf24-321">CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-321">CInternalPropertyRestriction</span></span> | <span data-ttu-id="cbf24-322">Contiene un valor de propiedad que debe coincidir con una operación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-322">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="cbf24-323">CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-323">CNatLanguageRestriction</span></span>      | <span data-ttu-id="cbf24-324">Contiene una coincidencia de consulta de lenguaje natural para una propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-324">Contains a natural language query match for a property.</span></span>                                                                |
| <span data-ttu-id="cbf24-325">CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-325">CNodeRestriction</span></span>             | <span data-ttu-id="cbf24-326">Contiene una matriz de nodos de árbol de comandos que especifican las restricciones de una consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-326">Contains an array of command tree nodes specifying the restrictions for a query.</span></span>                                       |
| <span data-ttu-id="cbf24-327">COccRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-327">COccRestriction</span></span>              | <span data-ttu-id="cbf24-328">Contiene la ubicación de una palabra en una frase.</span><span class="sxs-lookup"><span data-stu-id="cbf24-328">Contains the location of a word in a phrase.</span></span>                                                                           |
| <span data-ttu-id="cbf24-329">CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-329">CPropertyRestriction</span></span>         | <span data-ttu-id="cbf24-330">Contiene un valor de propiedad que debe coincidir con una operación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-330">Contains a property value to match with an operation.</span></span>                                                                  |
| <span data-ttu-id="cbf24-331">CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-331">CRangeRestriction</span></span>            | <span data-ttu-id="cbf24-332">Contiene una restricción sobre un intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="cbf24-332">Contains a restriction on a range of values.</span></span>                                                                           |
| <span data-ttu-id="cbf24-333">CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-333">CScopeRestriction</span></span>            | <span data-ttu-id="cbf24-334">Contiene una restricción en los archivos en los que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-334">Contains a restriction on the files to be searched.</span></span>                                                                    |
| <span data-ttu-id="cbf24-335">CSort</span><span class="sxs-lookup"><span data-stu-id="cbf24-335">CSort</span></span>                        | <span data-ttu-id="cbf24-336">Identifica una columna que se ordenará.</span><span class="sxs-lookup"><span data-stu-id="cbf24-336">Identifies a column to sort.</span></span>                                                                                           |
| <span data-ttu-id="cbf24-337">CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-337">CSynRestriction</span></span>              | <span data-ttu-id="cbf24-338">Contiene una palabra o sus sinónimos para una frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-338">Contains a word or its synonyms for a query phrase.</span></span>                                                                    |
| <span data-ttu-id="cbf24-339">CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-339">CVectorRestriction</span></span>           | <span data-ttu-id="cbf24-340">Contiene una operación OR ponderada en un nodo de árbol de comandos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-340">Contains a weighted OR operation on a command tree node.</span></span>                                                               |
| <span data-ttu-id="cbf24-341">CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-341">CWordRestriction</span></span>             | <span data-ttu-id="cbf24-342">Contiene una palabra para una frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-342">Contains a word for a query phrase.</span></span>                                                                                    |
| <span data-ttu-id="cbf24-343">CRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-343">CRestriction</span></span>                 | <span data-ttu-id="cbf24-344">Contiene un nodo de un árbol de comandos de consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-344">Contains a node of a query command tree.</span></span>                                                                               |
| <span data-ttu-id="cbf24-345">CColumnSet</span><span class="sxs-lookup"><span data-stu-id="cbf24-345">CColumnSet</span></span>                   | <span data-ttu-id="cbf24-346">Indica el número de columnas que se devolverán.</span><span class="sxs-lookup"><span data-stu-id="cbf24-346">Indicates the number of columns to return.</span></span>                                                                             |
| <span data-ttu-id="cbf24-347">CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="cbf24-347">CCategorizationSet</span></span>           | <span data-ttu-id="cbf24-348">Contiene información sobre la agrupación de un conjunto de resultados de consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-348">Contains information about the grouping of a set of query results.</span></span>                                                     |
| <span data-ttu-id="cbf24-349">CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="cbf24-349">CCategorizationSpec</span></span>          | <span data-ttu-id="cbf24-350">Contiene una definición de categorías en las que se clasificarán los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-350">Contains a definition of categories into which query results will be categorized.</span></span>                                      |
| <span data-ttu-id="cbf24-351">CDbColId</span><span class="sxs-lookup"><span data-stu-id="cbf24-351">CDbColId</span></span>                     | <span data-ttu-id="cbf24-352">Contiene una columna.</span><span class="sxs-lookup"><span data-stu-id="cbf24-352">Contains a column.</span></span>                                                                                                     |
| <span data-ttu-id="cbf24-353">CDbProp</span><span class="sxs-lookup"><span data-stu-id="cbf24-353">CDbProp</span></span>                      | <span data-ttu-id="cbf24-354">Contiene una propiedad .</span><span class="sxs-lookup"><span data-stu-id="cbf24-354">Contains a property.</span></span>                                                                                                   |
| <span data-ttu-id="cbf24-355">CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="cbf24-355">CDbPropSet</span></span>                   | <span data-ttu-id="cbf24-356">Contiene un conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="cbf24-356">Contains a set of properties.</span></span>                                                                                          |
| <span data-ttu-id="cbf24-357">CPidMapper</span><span class="sxs-lookup"><span data-stu-id="cbf24-357">CPidMapper</span></span>                   | <span data-ttu-id="cbf24-358">Contiene una matriz de los IDs de propiedad que especifican las propiedades que se devolverán en un conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-358">Contains an array of property IDs specifying the properties to return in a rowset.</span></span>                                     |
| <span data-ttu-id="cbf24-359">CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="cbf24-359">CRowSeekAt</span></span>                   | <span data-ttu-id="cbf24-360">Contiene el desplazamiento en el que se van a recuperar las filas de un mensaje CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-360">Contains the offset at which to retrieve rows in a CPMGetRowsIn message</span></span>                                                |
| <span data-ttu-id="cbf24-361">CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="cbf24-361">CRowSeekAtRatio</span></span>              | <span data-ttu-id="cbf24-362">Identifica el punto en el que se va a iniciar la recuperación de un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-362">Identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>                                           |
| <span data-ttu-id="cbf24-363">CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="cbf24-363">CRowSeekByBookmark</span></span>           | <span data-ttu-id="cbf24-364">Identifica los marcadores de los que se van a recuperar las filas de un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-364">Identifies the bookmarks from which to retrieve rows for a CPMGetRowsIn message.</span></span>                                       |
| <span data-ttu-id="cbf24-365">CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="cbf24-365">CRowSeekNext</span></span>                 | <span data-ttu-id="cbf24-366">Contiene el número de filas que se omitirán en un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-366">Contains the number of rows to skip in a CPMGetRowsIn message.</span></span>                                                         |
| <span data-ttu-id="cbf24-367">CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="cbf24-367">CRowsetProperties</span></span>            | <span data-ttu-id="cbf24-368">Contiene la información de configuración de una consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-368">Contains the configuration information for a query.</span></span>                                                                    |
| <span data-ttu-id="cbf24-369">CSortSet</span><span class="sxs-lookup"><span data-stu-id="cbf24-369">CSortSet</span></span>                     | <span data-ttu-id="cbf24-370">Contiene el criterio de ordenación de una consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-370">Contains the sort order for a query.</span></span>                                                                                   |
| <span data-ttu-id="cbf24-371">CTableColumn</span><span class="sxs-lookup"><span data-stu-id="cbf24-371">CTableColumn</span></span>                 | <span data-ttu-id="cbf24-372">Contiene una columna para el mensaje CPMSetBindings.</span><span class="sxs-lookup"><span data-stu-id="cbf24-372">Contains a column for the CPMSetBindings message.</span></span>                                                                      |
| <span data-ttu-id="cbf24-373">SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="cbf24-373">SERIALIZEDPROPERTYVALUE</span></span>      | <span data-ttu-id="cbf24-374">Contiene un valor serializado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-374">Contains a serialized value.</span></span>                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a><span data-ttu-id="cbf24-375">2.2.1.1 CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="cbf24-375">2.2.1.1 CBaseStorageVariant</span></span>

<span data-ttu-id="cbf24-376">La estructura CBaseStorageVariant contiene el valor en el que se va a realizar una operación de coincidencia para una propiedad especificada en la estructura CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="cbf24-376">The CBaseStorageVariant structure contains the value on which to perform a match operation for a property specified in the CPropertyRestriction structure.</span></span>



<span data-ttu-id="cbf24-377">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-377">0</span></span>

<span data-ttu-id="cbf24-378">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-378">1</span></span>

<span data-ttu-id="cbf24-379">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-379">2</span></span>

<span data-ttu-id="cbf24-380">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-380">3</span></span>

<span data-ttu-id="cbf24-381">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-381">4</span></span>

<span data-ttu-id="cbf24-382">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-382">5</span></span>

<span data-ttu-id="cbf24-383">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-383">6</span></span>

<span data-ttu-id="cbf24-384">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-384">7</span></span>

<span data-ttu-id="cbf24-385">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-385">8</span></span>

<span data-ttu-id="cbf24-386">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-386">9</span></span>

<span data-ttu-id="cbf24-387">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-387">1</span></span><br/> <span data-ttu-id="cbf24-388">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-388">0</span></span><br/>

<span data-ttu-id="cbf24-389">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-389">1</span></span>

<span data-ttu-id="cbf24-390">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-390">2</span></span>

<span data-ttu-id="cbf24-391">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-391">3</span></span>

<span data-ttu-id="cbf24-392">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-392">4</span></span>

<span data-ttu-id="cbf24-393">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-393">5</span></span>

<span data-ttu-id="cbf24-394">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-394">6</span></span>

<span data-ttu-id="cbf24-395">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-395">7</span></span>

<span data-ttu-id="cbf24-396">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-396">8</span></span>

<span data-ttu-id="cbf24-397">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-397">9</span></span>

<span data-ttu-id="cbf24-398">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-398">2</span></span><br/> <span data-ttu-id="cbf24-399">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-399">0</span></span><br/>

<span data-ttu-id="cbf24-400">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-400">1</span></span>

<span data-ttu-id="cbf24-401">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-401">2</span></span>

<span data-ttu-id="cbf24-402">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-402">3</span></span>

<span data-ttu-id="cbf24-403">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-403">4</span></span>

<span data-ttu-id="cbf24-404">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-404">5</span></span>

<span data-ttu-id="cbf24-405">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-405">6</span></span>

<span data-ttu-id="cbf24-406">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-406">7</span></span>

<span data-ttu-id="cbf24-407">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-407">8</span></span>

<span data-ttu-id="cbf24-408">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-408">9</span></span>

<span data-ttu-id="cbf24-409">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-409">3</span></span><br/> <span data-ttu-id="cbf24-410">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-410">0</span></span><br/>

<span data-ttu-id="cbf24-411">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-411">1</span></span>

<span data-ttu-id="cbf24-412">vType</span><span class="sxs-lookup"><span data-stu-id="cbf24-412">vType</span></span>

<span data-ttu-id="cbf24-413">vData1</span><span class="sxs-lookup"><span data-stu-id="cbf24-413">vData1</span></span>

<span data-ttu-id="cbf24-414">vData2</span><span class="sxs-lookup"><span data-stu-id="cbf24-414">vData2</span></span>

<span data-ttu-id="cbf24-415">vValue (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-415">vValue (variable)</span></span>



 

<span data-ttu-id="cbf24-416">**vType:** un indicador de tipo que indica el tipo de vValue.</span><span class="sxs-lookup"><span data-stu-id="cbf24-416">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="cbf24-417">DEBE ser uno de los valores VARENUM especificados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-417">It MUST be one of the VARENUM values specified in the following table.</span></span>



| <span data-ttu-id="cbf24-418">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-418">Value</span></span>                 | <span data-ttu-id="cbf24-419">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-419">Meaning</span></span>                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-420">VT \_ EMPTY (0x0000)</span><span class="sxs-lookup"><span data-stu-id="cbf24-420">VT\_EMPTY (0x0000)</span></span>    | <span data-ttu-id="cbf24-421">vValue no está presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-421">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="cbf24-422">VT \_ NULL (0x0001)</span><span class="sxs-lookup"><span data-stu-id="cbf24-422">VT\_NULL (0x0001)</span></span>     | <span data-ttu-id="cbf24-423">vValue no está presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-423">vValue is not present.</span></span>                                                                                                               |
| <span data-ttu-id="cbf24-424">VT \_ I1 (0x0010)</span><span class="sxs-lookup"><span data-stu-id="cbf24-424">VT\_I1 (0x0010)</span></span>       | <span data-ttu-id="cbf24-425">Entero de 1 byte con signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-425">A 1-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="cbf24-426">VT \_ UI1 (0x0011)</span><span class="sxs-lookup"><span data-stu-id="cbf24-426">VT\_UI1 (0x0011)</span></span>      | <span data-ttu-id="cbf24-427">Entero de 1 byte sin signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-427">A 1-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="cbf24-428">VT \_ I2 (0x0002)</span><span class="sxs-lookup"><span data-stu-id="cbf24-428">VT\_I2 (0x0002)</span></span>       | <span data-ttu-id="cbf24-429">Entero de 2 bytes con signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-429">A 2-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="cbf24-430">VT \_ UI2 (0x0012)</span><span class="sxs-lookup"><span data-stu-id="cbf24-430">VT\_UI2 (0x0012)</span></span>      | <span data-ttu-id="cbf24-431">Entero de 2 bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-431">A 2-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="cbf24-432">VT \_ BOOL (0x000B)</span><span class="sxs-lookup"><span data-stu-id="cbf24-432">VT\_BOOL (0x000B)</span></span>     | <span data-ttu-id="cbf24-433">Valor booleano; entero de 2 bytes que contiene 0x0000 (FALSE) o 0xFFFF (TRUE).</span><span class="sxs-lookup"><span data-stu-id="cbf24-433">A boolean value; a 2-byte integer containing 0x0000 (FALSE) or 0xFFFF (TRUE).</span></span>                                                        |
| <span data-ttu-id="cbf24-434">VT \_ I4 (0x0003)</span><span class="sxs-lookup"><span data-stu-id="cbf24-434">VT\_I4 (0x0003)</span></span>       | <span data-ttu-id="cbf24-435">Entero de 4 bytes con signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-435">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="cbf24-436">VT \_ UI4 (0x0013)</span><span class="sxs-lookup"><span data-stu-id="cbf24-436">VT\_UI4 (0x0013)</span></span>      | <span data-ttu-id="cbf24-437">Entero de 4 bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-437">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="cbf24-438">VT \_ R4 (0x0004)</span><span class="sxs-lookup"><span data-stu-id="cbf24-438">VT\_R4 (0x0004)</span></span>       | <span data-ttu-id="cbf24-439">Número de punto flotante ieee de 32 bits, tal como se define en \[ IEEE754. \]</span><span class="sxs-lookup"><span data-stu-id="cbf24-439">An IEEE 32-bit floating-point number, as defined in \[IEEE754\].</span></span>                                                                     |
| <span data-ttu-id="cbf24-440">VT \_ INT (0x0016)</span><span class="sxs-lookup"><span data-stu-id="cbf24-440">VT\_INT (0x0016)</span></span>      | <span data-ttu-id="cbf24-441">Entero de 4 bytes con signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-441">A 4-byte signed integer.</span></span>                                                                                                             |
| <span data-ttu-id="cbf24-442">VT \_ UINT (0x0017)</span><span class="sxs-lookup"><span data-stu-id="cbf24-442">VT\_UINT (0x0017)</span></span>     | <span data-ttu-id="cbf24-443">Entero de 4 bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-443">A 4-byte unsigned integer.</span></span>                                                                                                           |
| <span data-ttu-id="cbf24-444">\_ERROR DE VT (0x000A)</span><span class="sxs-lookup"><span data-stu-id="cbf24-444">VT\_ERROR (0x000A)</span></span>    | <span data-ttu-id="cbf24-445">Entero de 4 bytes sin signo que contiene un valor HRESULT, tal y como se especifica en \[ MS-SYS \] .</span><span class="sxs-lookup"><span data-stu-id="cbf24-445">A 4-byte unsigned integer containing an HRESULT, as specified in \[MS-SYS\].</span></span>                                                         |
| <span data-ttu-id="cbf24-446">VT \_ I8 (0x0014)</span><span class="sxs-lookup"><span data-stu-id="cbf24-446">VT\_I8 (0x0014)</span></span>       | <span data-ttu-id="cbf24-447">Entero de 8 bytes con signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-447">An 8 byte signed integer.</span></span>                                                                                                            |
| <span data-ttu-id="cbf24-448">VT \_ UI8 (0x0015)</span><span class="sxs-lookup"><span data-stu-id="cbf24-448">VT\_UI8 (0x0015)</span></span>      | <span data-ttu-id="cbf24-449">Entero de 8 bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-449">An 8-byte unsigned integer.</span></span>                                                                                                          |
| <span data-ttu-id="cbf24-450">VT \_ R8 (0x0005)</span><span class="sxs-lookup"><span data-stu-id="cbf24-450">VT\_R8 (0x0005)</span></span>       | <span data-ttu-id="cbf24-451">Número de punto flotante ieee de 64 bits definido en \[ IEEE754. \]</span><span class="sxs-lookup"><span data-stu-id="cbf24-451">An IEEE 64-bit floating-point number as defined in \[IEEE754\].</span></span>                                                                      |
| <span data-ttu-id="cbf24-452">VT \_ CY (0x0006)</span><span class="sxs-lookup"><span data-stu-id="cbf24-452">VT\_CY (0x0006)</span></span>       | <span data-ttu-id="cbf24-453">Entero de complemento de dos de 8 bytes (escalado en 10 000).</span><span class="sxs-lookup"><span data-stu-id="cbf24-453">An 8-byte two's complement integer (scaled by 10,000).</span></span>                                                                               |
| <span data-ttu-id="cbf24-454">VT \_ DATE (0x0007)</span><span class="sxs-lookup"><span data-stu-id="cbf24-454">VT\_DATE (0x0007)</span></span>     | <span data-ttu-id="cbf24-455">Número de punto flotante de 64 bits que representa el número de días desde las 00:00:00 del 31 de diciembre de 1899 (hora universal coordinada).</span><span class="sxs-lookup"><span data-stu-id="cbf24-455">A 64-bit floating-point number representing the number of days since 00:00:00 on December 31, 1899 (Coordinated Universal Time).</span></span>     |
| <span data-ttu-id="cbf24-456">VT \_ FILETIME (0x0040)</span><span class="sxs-lookup"><span data-stu-id="cbf24-456">VT\_FILETIME (0x0040)</span></span> | <span data-ttu-id="cbf24-457">Entero de 64 bits que representa el número de intervalos de 100 nanosegundos desde las 00:00:00 del 1 de enero de 1601 (hora universal coordinada).</span><span class="sxs-lookup"><span data-stu-id="cbf24-457">A 64-bit integer representing the number of 100-nanosecond intervals since 00:00:00 on January 1, 1601 (Coordinated Universal Time).</span></span> |
| <span data-ttu-id="cbf24-458">\_VT DECIMAL (0x000E)</span><span class="sxs-lookup"><span data-stu-id="cbf24-458">VT\_DECIMAL (0x000E)</span></span>  | <span data-ttu-id="cbf24-459">Estructura DECIMAL especificada en la sección 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="cbf24-459">A DECIMAL structure as specified in section 2.2.1.1.1.1.</span></span>                                                                             |
| <span data-ttu-id="cbf24-460">VT \_ CLSID (0x0048)</span><span class="sxs-lookup"><span data-stu-id="cbf24-460">VT\_CLSID (0x0048)</span></span>    | <span data-ttu-id="cbf24-461">Valor binario de 16 bytes que contiene un GUID.</span><span class="sxs-lookup"><span data-stu-id="cbf24-461">A 16-byte binary value containing a GUID.</span></span>                                                                                            |
| <span data-ttu-id="cbf24-462">\_VT BLOB (0x0041)</span><span class="sxs-lookup"><span data-stu-id="cbf24-462">VT\_BLOB (0x0041)</span></span>     | <span data-ttu-id="cbf24-463">Un recuento entero de 4 bytes sin signo de bytes en el blob, seguido de tantos bytes de datos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-463">A 4-byte unsigned integer count of bytes in the blob, followed by that many bytes of data.</span></span>                                           |
| <span data-ttu-id="cbf24-464">VT \_ BSTR (0x0008)</span><span class="sxs-lookup"><span data-stu-id="cbf24-464">VT\_BSTR (0x0008)</span></span>     | <span data-ttu-id="cbf24-465">Un número entero de 4 bytes sin signo de bytes en la cadena, seguido de una cadena, como se especifica a continuación en vValue.</span><span class="sxs-lookup"><span data-stu-id="cbf24-465">A 4-byte unsigned integer count of bytes in the string, followed by a string, as specified below under vValue.</span></span>                       |
| <span data-ttu-id="cbf24-466">VT \_ LPSTR (0x001E)</span><span class="sxs-lookup"><span data-stu-id="cbf24-466">VT\_LPSTR (0x001E)</span></span>    | <span data-ttu-id="cbf24-467">Cadena ANSI terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="cbf24-467">A null-terminated ANSI string.</span></span>                                                                                                       |
| <span data-ttu-id="cbf24-468">VT \_ LPWSTR (0x001F)</span><span class="sxs-lookup"><span data-stu-id="cbf24-468">VT\_LPWSTR (0x001F)</span></span>   | <span data-ttu-id="cbf24-469">Cadena Unicode terminada en \[ \] NULL.</span><span class="sxs-lookup"><span data-stu-id="cbf24-469">A null-terminated Unicode \[UNICODE\] string.</span></span>                                                                                        |
| <span data-ttu-id="cbf24-470">VT \_ VARIANT (0x000C)</span><span class="sxs-lookup"><span data-stu-id="cbf24-470">VT\_VARIANT (0x000C)</span></span>  | <span data-ttu-id="cbf24-471">CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="cbf24-471">CBaseStorageVariant.</span></span> <span data-ttu-id="cbf24-472">DEBE combinarse con un modificador de tipo de VT \_ ARRAY o VT \_ VECTOR.</span><span class="sxs-lookup"><span data-stu-id="cbf24-472">MUST be combined with a type modifier of VT\_ARRAY or VT\_VECTOR.</span></span>                                               |



 

<span data-ttu-id="cbf24-473">En la tabla siguiente se especifican los modificadores de tipo para vType.</span><span class="sxs-lookup"><span data-stu-id="cbf24-473">The following table specifies the type modifiers for vType.</span></span> <span data-ttu-id="cbf24-474">Los modificadores de tipo pueden ser binarios ORed con vType, para cambiar el significado de vValue para indicar que es uno de los dos tipos de matriz posibles.</span><span class="sxs-lookup"><span data-stu-id="cbf24-474">Type modifiers can be binary ORed with vType, to change the meaning of vValue to indicate it is one of two possible array types.</span></span>



| <span data-ttu-id="cbf24-475">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-475">Value</span></span>               | <span data-ttu-id="cbf24-476">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-476">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-477">VT \_ VECTOR (0x1000)</span><span class="sxs-lookup"><span data-stu-id="cbf24-477">VT\_VECTOR (0x1000)</span></span> | <span data-ttu-id="cbf24-478">Si el indicador de tipo se combina con VT VECTOR mediante un operador OR, vValue es una matriz de valores con recuento \_ del tipo indicado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-478">If the type indicator is combined with VT\_VECTOR by using an OR operator, vValue is a counted array of values of the indicated type.</span></span> <span data-ttu-id="cbf24-479">Consulte la sección 2.2.1.1.1.2 para más información.</span><span class="sxs-lookup"><span data-stu-id="cbf24-479">See section 2.2.1.1.1.2 for details.</span></span> <br/> <span data-ttu-id="cbf24-480">Este modificador de tipo NO DEBE combinarse con los siguientes tipos: VT \_ INT, VT \_ UINT, VT \_ DECIMAL, VT \_ BLOB, VT \_ BLOB \_ OBJECT.</span><span class="sxs-lookup"><span data-stu-id="cbf24-480">This type modifier MUST NOT be combined with the following types: VT\_INT, VT\_UINT, VT\_DECIMAL, VT\_BLOB, VT\_BLOB\_OBJECT.</span></span><br/>                                    |
| <span data-ttu-id="cbf24-481">VT \_ ARRAY (0x2000)</span><span class="sxs-lookup"><span data-stu-id="cbf24-481">VT\_ARRAY (0x2000)</span></span>  | <span data-ttu-id="cbf24-482">Si un operador OR combina el indicador de tipo con VT ARRAY, el valor es SAFEARRAY (como se especifica en la sección \_ 2.2.1.1.1.3) que contiene valores del tipo indicado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-482">If the type indicator is combined with VT\_ARRAY by an OR operator, the value is a SAFEARRAY (as specified in section 2.2.1.1.1.3) containing values of the indicated type.</span></span> <br/> <span data-ttu-id="cbf24-483">Este modificador de tipo NO DEBE combinarse con los siguientes tipos: VT \_ I8, VT \_ UI8, VT \_ FILETIME, VT \_ CLSID, VT \_ BLOB, VT \_ BLOB \_ OBJECT, VT \_ LPSTR, VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="cbf24-483">This type modifier MUST NOT be combined with the following types: VT\_I8, VT\_UI8, VT\_FILETIME, VT\_CLSID, VT\_BLOB, VT\_BLOB\_OBJECT, VT\_LPSTR, VT\_LPWSTR.</span></span> <br/> |



 

<span data-ttu-id="cbf24-484">**vData1:** cuando vType es VT DECIMAL, el valor de este campo se especifica como el campo Escala de la sección \_ 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="cbf24-484">**vData1**: When vType is VT\_DECIMAL, the value of this field is specified as the Scale field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="cbf24-485">Para todos los demás vTypes, el valor DEBE establecerse en 0x00.</span><span class="sxs-lookup"><span data-stu-id="cbf24-485">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="cbf24-486">**vData2:** cuando vType es VT DECIMAL, el valor de este campo se especifica como el campo Sign de la sección \_ 2.2.1.1.1.1.</span><span class="sxs-lookup"><span data-stu-id="cbf24-486">**vData2**: When vType is VT\_DECIMAL, the value of this field is specified as the Sign field in section 2.2.1.1.1.1.</span></span> <span data-ttu-id="cbf24-487">Para todos los demás vTypes, el valor DEBE establecerse en 0x00.</span><span class="sxs-lookup"><span data-stu-id="cbf24-487">For all other vTypes, the value MUST be set to 0x00.</span></span>

<span data-ttu-id="cbf24-488">**vValue:** el valor de la operación de coincidencia.</span><span class="sxs-lookup"><span data-stu-id="cbf24-488">**vValue**: The value for the match operation.</span></span> <span data-ttu-id="cbf24-489">La sintaxis DEBE ser como se indica en el campo vType.</span><span class="sxs-lookup"><span data-stu-id="cbf24-489">The syntax MUST be as indicated in the vType field.</span></span>

<span data-ttu-id="cbf24-490">En la tabla siguiente se resumen los tamaños del campo vValue, que depende del campo vType para los tipos de datos de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="cbf24-490">The following table summarizes sizes for the vValue field, dependent upon the vType field for fixed-length data types.</span></span> <span data-ttu-id="cbf24-491">El tamaño es en bytes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-491">The size is in bytes.</span></span>



| <span data-ttu-id="cbf24-492">vType</span><span class="sxs-lookup"><span data-stu-id="cbf24-492">vType</span></span>                                                   | <span data-ttu-id="cbf24-493">Tamaño</span><span class="sxs-lookup"><span data-stu-id="cbf24-493">Size</span></span> |
|---------------------------------------------------------|------|
| <span data-ttu-id="cbf24-494">VT \_ I1, VT, \_ UI1</span><span class="sxs-lookup"><span data-stu-id="cbf24-494">VT\_I1, VT,\_UI1</span></span>                                        | <span data-ttu-id="cbf24-495">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-495">1</span></span>    |
| <span data-ttu-id="cbf24-496">VT \_ I2, VT \_ UI2, VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="cbf24-496">VT\_I2, VT\_UI2, VT\_BOOL</span></span>                               | <span data-ttu-id="cbf24-497">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-497">2</span></span>    |
| <span data-ttu-id="cbf24-498">VT \_ I4, VT \_ UI4, VT \_ R4, VT \_ INT, VT \_ UINT, VT \_ ERROR</span><span class="sxs-lookup"><span data-stu-id="cbf24-498">VT\_I4, VT\_UI4, VT\_R4, VT\_INT, VT\_UINT, VT\_ERROR</span></span>   | <span data-ttu-id="cbf24-499">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-499">4</span></span>    |
| <span data-ttu-id="cbf24-500">VT \_ I8, VT \_ UI8, VT \_ R8, VT \_ CY, VT \_ DATE, VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="cbf24-500">VT\_I8, VT\_UI8, VT\_R8, VT\_CY, VT\_DATE, VT\_FILETIME</span></span> | <span data-ttu-id="cbf24-501">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-501">8</span></span>    |
| <span data-ttu-id="cbf24-502">VT \_ DECIMAL, VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="cbf24-502">VT\_DECIMAL, VT\_CLSID</span></span>                                  | <span data-ttu-id="cbf24-503">16</span><span class="sxs-lookup"><span data-stu-id="cbf24-503">16</span></span>   |



 

<span data-ttu-id="cbf24-504">Si vType se establece en \_ VT BLOB, VT BSTR o VT LPSTR, la estructura de vValue se \_ especifica en el diagrama \_ siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-504">If vType is set to VT\_BLOB, VT\_BSTR or VT\_LPSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="cbf24-505">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-505">0</span></span>

<span data-ttu-id="cbf24-506">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-506">1</span></span>

<span data-ttu-id="cbf24-507">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-507">2</span></span>

<span data-ttu-id="cbf24-508">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-508">3</span></span>

<span data-ttu-id="cbf24-509">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-509">4</span></span>

<span data-ttu-id="cbf24-510">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-510">5</span></span>

<span data-ttu-id="cbf24-511">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-511">6</span></span>

<span data-ttu-id="cbf24-512">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-512">7</span></span>

<span data-ttu-id="cbf24-513">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-513">8</span></span>

<span data-ttu-id="cbf24-514">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-514">9</span></span>

<span data-ttu-id="cbf24-515">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-515">1</span></span><br/> <span data-ttu-id="cbf24-516">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-516">0</span></span><br/>

<span data-ttu-id="cbf24-517">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-517">1</span></span>

<span data-ttu-id="cbf24-518">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-518">2</span></span>

<span data-ttu-id="cbf24-519">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-519">3</span></span>

<span data-ttu-id="cbf24-520">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-520">4</span></span>

<span data-ttu-id="cbf24-521">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-521">5</span></span>

<span data-ttu-id="cbf24-522">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-522">6</span></span>

<span data-ttu-id="cbf24-523">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-523">7</span></span>

<span data-ttu-id="cbf24-524">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-524">8</span></span>

<span data-ttu-id="cbf24-525">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-525">9</span></span>

<span data-ttu-id="cbf24-526">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-526">2</span></span><br/> <span data-ttu-id="cbf24-527">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-527">0</span></span><br/>

<span data-ttu-id="cbf24-528">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-528">1</span></span>

<span data-ttu-id="cbf24-529">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-529">2</span></span>

<span data-ttu-id="cbf24-530">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-530">3</span></span>

<span data-ttu-id="cbf24-531">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-531">4</span></span>

<span data-ttu-id="cbf24-532">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-532">5</span></span>

<span data-ttu-id="cbf24-533">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-533">6</span></span>

<span data-ttu-id="cbf24-534">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-534">7</span></span>

<span data-ttu-id="cbf24-535">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-535">8</span></span>

<span data-ttu-id="cbf24-536">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-536">9</span></span>

<span data-ttu-id="cbf24-537">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-537">3</span></span><br/> <span data-ttu-id="cbf24-538">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-538">0</span></span><br/>

<span data-ttu-id="cbf24-539">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-539">1</span></span>

<span data-ttu-id="cbf24-540">cbSize</span><span class="sxs-lookup"><span data-stu-id="cbf24-540">cbSize</span></span>

<span data-ttu-id="cbf24-541">blobData (variable, opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-541">blobData (variable, optional)</span></span>



 

<span data-ttu-id="cbf24-542">**cbSize:** entero de 32 bits sin signo, que indica el tamaño del campo blobData en bytes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-542">**cbSize**: Unsigned 32-bit integer, indicating the size of the blobData field in bytes.</span></span> <span data-ttu-id="cbf24-543">Si vType se establece en VT BSTR o \_ VT LPSTR, cbSize DEBE establecerse en 0x00000000 cuando la cadena representada \_ es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="cbf24-543">If vType is set to VT\_BSTR or VT\_LPSTR, cbSize MUST be set to 0x00000000 when the string represented is an empty string.</span></span>

<span data-ttu-id="cbf24-544">**blobData:** DEBE tener la longitud cbSize en bytes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-544">**blobData**: MUST be of length cbSize in bytes.</span></span>

<span data-ttu-id="cbf24-545">Para vType establecido en VT \_ BLOB, este campo son datos de blob binario opacos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-545">For vType set to VT\_BLOB, this field is opaque binary blob data.</span></span>

<span data-ttu-id="cbf24-546">Para vType establecido en VT BSTR, este campo es un conjunto de caracteres en un \_ juego de caracteres seleccionado por OEM.</span><span class="sxs-lookup"><span data-stu-id="cbf24-546">For vType set to VT\_BSTR, this field is a set of characters in an OEM selected character set.</span></span> <span data-ttu-id="cbf24-547">El cliente y el servidor DEBEN configurarse para tener conjuntos de caracteres interoperables (fuera de banda del protocolo).</span><span class="sxs-lookup"><span data-stu-id="cbf24-547">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span> <span data-ttu-id="cbf24-548">No es necesario que se termine en null.</span><span class="sxs-lookup"><span data-stu-id="cbf24-548">There is no requirement that it be null-terminated.</span></span>

<span data-ttu-id="cbf24-549">Para vType establecido en VT LPSTR, este campo es una cadena de caracteres terminada en NULL en un juego de caracteres \_ seleccionado por OEM.</span><span class="sxs-lookup"><span data-stu-id="cbf24-549">For vType set to VT\_LPSTR this field is a null-terminated character string in an OEM selected character set.</span></span> <span data-ttu-id="cbf24-550">El cliente y el servidor DEBEN configurarse para tener conjuntos de caracteres interoperables (fuera de banda del protocolo).</span><span class="sxs-lookup"><span data-stu-id="cbf24-550">The client and server MUST be configured to have interoperable character sets (out of band of the protocol).</span></span>

<span data-ttu-id="cbf24-551">Si vType se establece en VT \_ LPWSTR, la estructura de vValue se especifica en el diagrama siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-551">If vType is set to VT\_LPWSTR then the structure of vValue is specified in the following diagram:</span></span>



<span data-ttu-id="cbf24-552">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-552">0</span></span>

<span data-ttu-id="cbf24-553">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-553">1</span></span>

<span data-ttu-id="cbf24-554">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-554">2</span></span>

<span data-ttu-id="cbf24-555">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-555">3</span></span>

<span data-ttu-id="cbf24-556">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-556">4</span></span>

<span data-ttu-id="cbf24-557">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-557">5</span></span>

<span data-ttu-id="cbf24-558">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-558">6</span></span>

<span data-ttu-id="cbf24-559">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-559">7</span></span>

<span data-ttu-id="cbf24-560">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-560">8</span></span>

<span data-ttu-id="cbf24-561">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-561">9</span></span>

<span data-ttu-id="cbf24-562">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-562">1</span></span><br/> <span data-ttu-id="cbf24-563">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-563">0</span></span><br/>

<span data-ttu-id="cbf24-564">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-564">1</span></span>

<span data-ttu-id="cbf24-565">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-565">2</span></span>

<span data-ttu-id="cbf24-566">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-566">3</span></span>

<span data-ttu-id="cbf24-567">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-567">4</span></span>

<span data-ttu-id="cbf24-568">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-568">5</span></span>

<span data-ttu-id="cbf24-569">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-569">6</span></span>

<span data-ttu-id="cbf24-570">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-570">7</span></span>

<span data-ttu-id="cbf24-571">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-571">8</span></span>

<span data-ttu-id="cbf24-572">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-572">9</span></span>

<span data-ttu-id="cbf24-573">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-573">2</span></span><br/> <span data-ttu-id="cbf24-574">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-574">0</span></span><br/>

<span data-ttu-id="cbf24-575">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-575">1</span></span>

<span data-ttu-id="cbf24-576">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-576">2</span></span>

<span data-ttu-id="cbf24-577">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-577">3</span></span>

<span data-ttu-id="cbf24-578">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-578">4</span></span>

<span data-ttu-id="cbf24-579">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-579">5</span></span>

<span data-ttu-id="cbf24-580">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-580">6</span></span>

<span data-ttu-id="cbf24-581">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-581">7</span></span>

<span data-ttu-id="cbf24-582">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-582">8</span></span>

<span data-ttu-id="cbf24-583">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-583">9</span></span>

<span data-ttu-id="cbf24-584">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-584">3</span></span><br/> <span data-ttu-id="cbf24-585">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-585">0</span></span><br/>

<span data-ttu-id="cbf24-586">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-586">1</span></span>

<span data-ttu-id="cbf24-587">ccLen</span><span class="sxs-lookup"><span data-stu-id="cbf24-587">ccLen</span></span>

<span data-ttu-id="cbf24-588">string (variable, opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-588">string (variable, optional)</span></span>



 

<span data-ttu-id="cbf24-589">**ccLen:** entero de 32 bits sin signo, que indica el tamaño del campo de cadena en caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="cbf24-589">**ccLen**: Unsigned 32-bit integer, indicating the size of the string field in Unicode characters.</span></span> <span data-ttu-id="cbf24-590">DEBE establecerse en 0x00000000 para una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="cbf24-590">MUST be set to 0x00000000 for an empty string.</span></span>

<span data-ttu-id="cbf24-591">**string**: cadena Unicode terminada en null.</span><span class="sxs-lookup"><span data-stu-id="cbf24-591">**string**: Null-terminated Unicode string.</span></span>

### <a name="22111-cbasestoragevariant-structures"></a><span data-ttu-id="cbf24-592">2.2.1.1.1 Estructuras CBaseStorageVariant</span><span class="sxs-lookup"><span data-stu-id="cbf24-592">2.2.1.1.1 CBaseStorageVariant Structures</span></span>

<span data-ttu-id="cbf24-593">Las estructuras siguientes se usan en la estructura CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="cbf24-593">The following structures are used in the CBaseStorageVariant structure.</span></span>

### <a name="221111-decimal"></a><span data-ttu-id="cbf24-594">2.2.1.1.1.1 DECIMAL</span><span class="sxs-lookup"><span data-stu-id="cbf24-594">2.2.1.1.1.1 DECIMAL</span></span>

<span data-ttu-id="cbf24-595">DECIMAL se usa para representar un valor numérico exacto con una precisión fija y una escala fija.</span><span class="sxs-lookup"><span data-stu-id="cbf24-595">DECIMAL is used to represent an exact numeric value with a fixed precision and fixed scale.</span></span>

<span data-ttu-id="cbf24-596">Cuando vType se establece en VT DECIMAL (0x0000E), los campos \_ vData1 y vData2 de CBaseStorageVariant DEBEN interpretarse de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-596">When vType is set to VT\_DECIMAL (0x0000E), the vData1 and vData2 fields of CBaseStorageVariant MUST be interpreted as follows:</span></span>

<span data-ttu-id="cbf24-597">**vData1:** número de dígitos a la derecha del separador decimal.</span><span class="sxs-lookup"><span data-stu-id="cbf24-597">**vData1**: The number of digits to the right of the decimal point.</span></span> <span data-ttu-id="cbf24-598">DEBE estar en el intervalo de 0 a 28.</span><span class="sxs-lookup"><span data-stu-id="cbf24-598">MUST be in the range 0 to 28.</span></span>

<span data-ttu-id="cbf24-599">**vData2:** signo del valor numérico.</span><span class="sxs-lookup"><span data-stu-id="cbf24-599">**vData2**: The sign of the numeric value.</span></span> <span data-ttu-id="cbf24-600">Establezca en 0x00 si es positivo, 0x80 si es negativo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-600">Set to 0x00 if positive, 0x80 if negative.</span></span>

<span data-ttu-id="cbf24-601">El formato del campo vValue es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-601">The format of the vValue field is:</span></span>



<span data-ttu-id="cbf24-602">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-602">0</span></span>

<span data-ttu-id="cbf24-603">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-603">1</span></span>

<span data-ttu-id="cbf24-604">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-604">2</span></span>

<span data-ttu-id="cbf24-605">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-605">3</span></span>

<span data-ttu-id="cbf24-606">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-606">4</span></span>

<span data-ttu-id="cbf24-607">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-607">5</span></span>

<span data-ttu-id="cbf24-608">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-608">6</span></span>

<span data-ttu-id="cbf24-609">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-609">7</span></span>

<span data-ttu-id="cbf24-610">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-610">8</span></span>

<span data-ttu-id="cbf24-611">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-611">9</span></span>

<span data-ttu-id="cbf24-612">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-612">1</span></span><br/> <span data-ttu-id="cbf24-613">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-613">0</span></span><br/>

<span data-ttu-id="cbf24-614">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-614">1</span></span>

<span data-ttu-id="cbf24-615">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-615">2</span></span>

<span data-ttu-id="cbf24-616">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-616">3</span></span>

<span data-ttu-id="cbf24-617">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-617">4</span></span>

<span data-ttu-id="cbf24-618">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-618">5</span></span>

<span data-ttu-id="cbf24-619">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-619">6</span></span>

<span data-ttu-id="cbf24-620">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-620">7</span></span>

<span data-ttu-id="cbf24-621">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-621">8</span></span>

<span data-ttu-id="cbf24-622">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-622">9</span></span>

<span data-ttu-id="cbf24-623">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-623">2</span></span><br/> <span data-ttu-id="cbf24-624">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-624">0</span></span><br/>

<span data-ttu-id="cbf24-625">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-625">1</span></span>

<span data-ttu-id="cbf24-626">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-626">2</span></span>

<span data-ttu-id="cbf24-627">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-627">3</span></span>

<span data-ttu-id="cbf24-628">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-628">4</span></span>

<span data-ttu-id="cbf24-629">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-629">5</span></span>

<span data-ttu-id="cbf24-630">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-630">6</span></span>

<span data-ttu-id="cbf24-631">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-631">7</span></span>

<span data-ttu-id="cbf24-632">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-632">8</span></span>

<span data-ttu-id="cbf24-633">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-633">9</span></span>

<span data-ttu-id="cbf24-634">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-634">3</span></span><br/> <span data-ttu-id="cbf24-635">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-635">0</span></span><br/>

<span data-ttu-id="cbf24-636">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-636">1</span></span>

<span data-ttu-id="cbf24-637">Hi32</span><span class="sxs-lookup"><span data-stu-id="cbf24-637">Hi32</span></span>

<span data-ttu-id="cbf24-638">Lo32</span><span class="sxs-lookup"><span data-stu-id="cbf24-638">Lo32</span></span>

<span data-ttu-id="cbf24-639">Mid32</span><span class="sxs-lookup"><span data-stu-id="cbf24-639">Mid32</span></span>



 

<span data-ttu-id="cbf24-640">**Hi32:** los 32 bits más altos del entero de 96 bits.</span><span class="sxs-lookup"><span data-stu-id="cbf24-640">**Hi32**: The highest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="cbf24-641">**Lo32:** los 32 bits más bajos del entero de 96 bits.</span><span class="sxs-lookup"><span data-stu-id="cbf24-641">**Lo32**: The lowest 32 bits of the 96 bit integer.</span></span>

<span data-ttu-id="cbf24-642">**Mid32:** los 32 bits centrales del entero de 96 bits.</span><span class="sxs-lookup"><span data-stu-id="cbf24-642">**Mid32**: The middle 32 bits of the 96 bit integer.</span></span>

### <a name="221112-vt_vector"></a><span data-ttu-id="cbf24-643">2.2.1.1.1.2 VT \_ VECTOR</span><span class="sxs-lookup"><span data-stu-id="cbf24-643">2.2.1.1.1.2 VT\_VECTOR</span></span>

<span data-ttu-id="cbf24-644">Vt \_ Vector se usa para pasar matrices unidimensionales.</span><span class="sxs-lookup"><span data-stu-id="cbf24-644">VT\_Vector is used to pass one-dimensional arrays.</span></span>



<span data-ttu-id="cbf24-645">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-645">0</span></span>

<span data-ttu-id="cbf24-646">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-646">1</span></span>

<span data-ttu-id="cbf24-647">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-647">2</span></span>

<span data-ttu-id="cbf24-648">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-648">3</span></span>

<span data-ttu-id="cbf24-649">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-649">4</span></span>

<span data-ttu-id="cbf24-650">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-650">5</span></span>

<span data-ttu-id="cbf24-651">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-651">6</span></span>

<span data-ttu-id="cbf24-652">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-652">7</span></span>

<span data-ttu-id="cbf24-653">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-653">8</span></span>

<span data-ttu-id="cbf24-654">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-654">9</span></span>

<span data-ttu-id="cbf24-655">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-655">1</span></span><br/> <span data-ttu-id="cbf24-656">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-656">0</span></span><br/>

<span data-ttu-id="cbf24-657">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-657">1</span></span>

<span data-ttu-id="cbf24-658">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-658">2</span></span>

<span data-ttu-id="cbf24-659">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-659">3</span></span>

<span data-ttu-id="cbf24-660">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-660">4</span></span>

<span data-ttu-id="cbf24-661">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-661">5</span></span>

<span data-ttu-id="cbf24-662">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-662">6</span></span>

<span data-ttu-id="cbf24-663">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-663">7</span></span>

<span data-ttu-id="cbf24-664">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-664">8</span></span>

<span data-ttu-id="cbf24-665">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-665">9</span></span>

<span data-ttu-id="cbf24-666">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-666">2</span></span><br/> <span data-ttu-id="cbf24-667">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-667">0</span></span><br/>

<span data-ttu-id="cbf24-668">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-668">1</span></span>

<span data-ttu-id="cbf24-669">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-669">2</span></span>

<span data-ttu-id="cbf24-670">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-670">3</span></span>

<span data-ttu-id="cbf24-671">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-671">4</span></span>

<span data-ttu-id="cbf24-672">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-672">5</span></span>

<span data-ttu-id="cbf24-673">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-673">6</span></span>

<span data-ttu-id="cbf24-674">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-674">7</span></span>

<span data-ttu-id="cbf24-675">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-675">8</span></span>

<span data-ttu-id="cbf24-676">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-676">9</span></span>

<span data-ttu-id="cbf24-677">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-677">3</span></span><br/> <span data-ttu-id="cbf24-678">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-678">0</span></span><br/>

<span data-ttu-id="cbf24-679">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-679">1</span></span>

<span data-ttu-id="cbf24-680">vVectorElements</span><span class="sxs-lookup"><span data-stu-id="cbf24-680">vVectorElements</span></span>

<span data-ttu-id="cbf24-681">vVectorData</span><span class="sxs-lookup"><span data-stu-id="cbf24-681">vVectorData</span></span>



 

<span data-ttu-id="cbf24-682">**vVectorElements:** entero de 32 bits sin signo, que indica el número de elementos del campo vVectorData.</span><span class="sxs-lookup"><span data-stu-id="cbf24-682">**vVectorElements**: Unsigned 32-bit integer, indicating the number of elements in the vVectorData field.</span></span>

<span data-ttu-id="cbf24-683">**vVectorData:** matriz de elementos que tienen un tipo indicado por vType con el 0x1000 de bits desactivado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-683">**vVectorData**: An array of items which have a type indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="cbf24-684">El tamaño de un elemento de longitud fija individual se puede obtener de la tabla de tipo de datos de longitud fija, como se especifica en la sección 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="cbf24-684">The size of an individual fixed-length item can be obtained from the fixed-length data type table, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="cbf24-685">La longitud de este campo, en bytes, se puede calcular multiplicando vVectorElements por el tamaño de un elemento individual.</span><span class="sxs-lookup"><span data-stu-id="cbf24-685">The length of this field, in bytes, can be calculated by multiplying vVectorElements by the size of individual item.</span></span>

<span data-ttu-id="cbf24-686">En el caso de los tipos de datos de longitud variable, vVectorData contiene una secuencia de tipos simples serializados consecutivamente donde el tipo se indica mediante vType con el 0x1000 bits desactivado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-686">For variable-length data types vVectorData contains a sequence of consecutively marshaled simple types where the type is indicated by vType with the 0x1000 bit cleared.</span></span> <span data-ttu-id="cbf24-687">Esto incluye un caso especial indicado por vType VT \_ ARRAY \| VT VARIANT \_ (es decir, 0x100C).</span><span class="sxs-lookup"><span data-stu-id="cbf24-687">This includes a special case indicated by vType VT\_ARRAY \| VT\_VARIANT (i.e., 0x100C).</span></span>

<span data-ttu-id="cbf24-688">Los elementos del campo vVectorData DEBEN estar separados por 0 a 3 bytes de relleno, de forma que cada elemento comience en un desplazamiento que sea un múltiplo de 4 bytes desde el principio del mensaje que contiene esta matriz.</span><span class="sxs-lookup"><span data-stu-id="cbf24-688">The elements in the vVectorData field MUST be separated by 0 to 3 padding bytes such that each element begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="cbf24-689">Si hay bytes de relleno, el valor que contienen es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cbf24-689">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="cbf24-690">El receptor DEBE omitir el contenido de los bytes de relleno.</span><span class="sxs-lookup"><span data-stu-id="cbf24-690">The content of the padding bytes MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cbf24-691">Para un vType establecido en VT ARRAY VT VARIANT, el tipo de los elementos de \_ \| esta secuencia es \_ CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="cbf24-691">For a vType set to VT\_ARRAY \| VT\_VARIANT, the type for items in this sequence is CBaseStorageVariant.</span></span>

### <a name="221113-safearray"></a><span data-ttu-id="cbf24-692">2.2.1.1.1.3 SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="cbf24-692">2.2.1.1.1.3 SAFEARRAY</span></span>

<span data-ttu-id="cbf24-693">SAFEARRAY se usa para pasar matrices multidimensionales.</span><span class="sxs-lookup"><span data-stu-id="cbf24-693">SAFEARRAY is used to pass multidimensional arrays.</span></span> <span data-ttu-id="cbf24-694">La estructura contiene información de tamaño de matriz, así como los datos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="cbf24-694">The structure contains array size information as well as the data in the array.</span></span>



<span data-ttu-id="cbf24-695">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-695">0</span></span>

<span data-ttu-id="cbf24-696">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-696">1</span></span>

<span data-ttu-id="cbf24-697">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-697">2</span></span>

<span data-ttu-id="cbf24-698">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-698">3</span></span>

<span data-ttu-id="cbf24-699">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-699">4</span></span>

<span data-ttu-id="cbf24-700">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-700">5</span></span>

<span data-ttu-id="cbf24-701">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-701">6</span></span>

<span data-ttu-id="cbf24-702">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-702">7</span></span>

<span data-ttu-id="cbf24-703">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-703">8</span></span>

<span data-ttu-id="cbf24-704">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-704">9</span></span>

<span data-ttu-id="cbf24-705">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-705">1</span></span><br/> <span data-ttu-id="cbf24-706">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-706">0</span></span><br/>

<span data-ttu-id="cbf24-707">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-707">1</span></span>

<span data-ttu-id="cbf24-708">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-708">2</span></span>

<span data-ttu-id="cbf24-709">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-709">3</span></span>

<span data-ttu-id="cbf24-710">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-710">4</span></span>

<span data-ttu-id="cbf24-711">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-711">5</span></span>

<span data-ttu-id="cbf24-712">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-712">6</span></span>

<span data-ttu-id="cbf24-713">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-713">7</span></span>

<span data-ttu-id="cbf24-714">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-714">8</span></span>

<span data-ttu-id="cbf24-715">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-715">9</span></span>

<span data-ttu-id="cbf24-716">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-716">2</span></span><br/> <span data-ttu-id="cbf24-717">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-717">0</span></span><br/>

<span data-ttu-id="cbf24-718">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-718">1</span></span>

<span data-ttu-id="cbf24-719">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-719">2</span></span>

<span data-ttu-id="cbf24-720">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-720">3</span></span>

<span data-ttu-id="cbf24-721">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-721">4</span></span>

<span data-ttu-id="cbf24-722">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-722">5</span></span>

<span data-ttu-id="cbf24-723">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-723">6</span></span>

<span data-ttu-id="cbf24-724">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-724">7</span></span>

<span data-ttu-id="cbf24-725">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-725">8</span></span>

<span data-ttu-id="cbf24-726">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-726">9</span></span>

<span data-ttu-id="cbf24-727">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-727">3</span></span><br/> <span data-ttu-id="cbf24-728">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-728">0</span></span><br/>

<span data-ttu-id="cbf24-729">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-729">1</span></span>

<span data-ttu-id="cbf24-730">cDims</span><span class="sxs-lookup"><span data-stu-id="cbf24-730">cDims</span></span>

<span data-ttu-id="cbf24-731">fFeatures</span><span class="sxs-lookup"><span data-stu-id="cbf24-731">fFeatures</span></span>

<span data-ttu-id="cbf24-732">cbElements</span><span class="sxs-lookup"><span data-stu-id="cbf24-732">cbElements</span></span>

<span data-ttu-id="cbf24-733">Rgsabound (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-733">Rgsabound (variable)</span></span>

<span data-ttu-id="cbf24-734">vData (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-734">vData (variable)</span></span>



 

<span data-ttu-id="cbf24-735">**cDims:** entero de 16 bits sin signo, que indica el número de dimensiones de la matriz multidimensional.</span><span class="sxs-lookup"><span data-stu-id="cbf24-735">**cDims**: Unsigned 16-bit integer, indicating the number of dimensions of the multidimensional array.</span></span>

<span data-ttu-id="cbf24-736">**fFeatures:** campo de bits de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="cbf24-736">**fFeatures**: A 16-bit bitfield.</span></span> <span data-ttu-id="cbf24-737">Los valores representan características, definidas por aplicaciones de capa superior y DEBEN omitirse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-737">The values represent features, defined by upper layer applications and MUST be ignored.</span></span>

<span data-ttu-id="cbf24-738">**cbElements:** entero de 32 bits sin signo que especifica el tamaño de cada elemento de la matriz.</span><span class="sxs-lookup"><span data-stu-id="cbf24-738">**cbElements**: A 32-bit unsigned integer specifying the size of each element of the array.</span></span>

<span data-ttu-id="cbf24-739">**Rgsabound:** matriz que contiene una estructura SAFEARRAYBOUND, como se especifica en la sección 2.2.1.1.1.4, por dimensión en SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="cbf24-739">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4, per dimension in the SAFEARRAY.</span></span> <span data-ttu-id="cbf24-740">Esta matriz tiene la dimensión más a la izquierda en primer lugar y la dimensión más a la derecha en último lugar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-740">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="cbf24-741">**vData:** vector de elementos serializados de un tipo determinado, indicado por el vType del elemento que contiene CBaseStorageVariant, con el bit 0x2000 borrado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-741">**vData**: A vector of marshaled items of a particular type, indicated by the vType of the containing CBaseStorageVariant, with the bit 0x2000 cleared.</span></span>

<span data-ttu-id="cbf24-742">vData se serializa de forma similar a VT VECTOR, como se especifica en la sección 2.2.1.1.1.2, con la diferencia de que el número de elementos no se almacena delante del \_ vector.</span><span class="sxs-lookup"><span data-stu-id="cbf24-742">vData is marshaled similarly to VT\_VECTOR, as specified in Section 2.2.1.1.1.2, with the difference that the number of items is not stored in front of the vector.</span></span> <span data-ttu-id="cbf24-743">En su lugar, el número de elementos se calcula multiplicando el valor cElements por todos los límites de matriz seguros especificados en el campo Rgsabound.</span><span class="sxs-lookup"><span data-stu-id="cbf24-743">Rather the number of items is calculated by multiplying the cElements value with all safe array bounds given in the Rgsabound field.</span></span> <span data-ttu-id="cbf24-744">Los elementos se almacenan en un vector en orden de dimensiones, iterando a partir de la dimensión más a la derecha.</span><span class="sxs-lookup"><span data-stu-id="cbf24-744">Elements are stored in a vector in order of dimensions, iterating beginning with the right-most dimension.</span></span>

<span data-ttu-id="cbf24-745">El diagrama siguiente representa visualmente una matriz bidimensional de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-745">The following diagram visually represents a sample two-dimensional array.</span></span> <span data-ttu-id="cbf24-746">La primera dimensión tiene cElements igual a 4 (representado horizontalmente) y lLbound igual a 0, y la segunda dimensión tiene cElements igual a 2 (representado verticalmente) y lLbound igual a 0.</span><span class="sxs-lookup"><span data-stu-id="cbf24-746">The first dimension has cElements equal to 4 (represented horizontally) and lLbound equal to 0, and the second dimension has cElements equal to 2 (represented vertically) and lLbound equal to 0.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="cbf24-747">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-747">0x00000001</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="cbf24-748">0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbf24-748">0x00000002</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="cbf24-749">0x00000003</span><span class="sxs-lookup"><span data-stu-id="cbf24-749">0x00000003</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="cbf24-750">0x00000005</span><span class="sxs-lookup"><span data-stu-id="cbf24-750">0x00000005</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="cbf24-751">::row:::</span><span class="sxs-lookup"><span data-stu-id="cbf24-751">::row:::</span></span>
    :::column:::
        0x00000007
    :::column-end:::
    :::column:::
        0x00000011
    :::column-end:::
    :::column:::
        0x00000013
    :::column-end:::
    :::column:::
        0x00000017
    :::column-end:::
:::row-end:::

<span data-ttu-id="cbf24-752">Con el diagrama anterior, vData contendrá la siguiente secuencia: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterando primero por la dimensión situada más a la derecha y, a continuación, incrementando la dimensión siguiente).</span><span class="sxs-lookup"><span data-stu-id="cbf24-752">Using the diagram above, vData will contain the following sequence: 0x00000001, 0x00000007, 0x00000002, 0x00000011, 0x00000003, 0x00000013, 0x00000005, 0x00000017 (iterating through the rightmost dimension first, then incrementing the next dimension).</span></span> <span data-ttu-id="cbf24-753">El Rgsabound anterior (que registra cElements y Lbound) sería: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-753">The preceding Rgsabound (which records cElements and Lbound) would be: 0x00000004, 0x00000000, 0x00000002, 0x00000000.</span></span>

### <a name="221114-safearraybound"></a><span data-ttu-id="cbf24-754">2.2.1.1.1.4 SAFEARRAYBOUND</span><span class="sxs-lookup"><span data-stu-id="cbf24-754">2.2.1.1.1.4 SAFEARRAYBOUND</span></span>

<span data-ttu-id="cbf24-755">La estructura SAFEARRAYBOUND representa los límites de una dimensión de SAFEARRAY o SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="cbf24-755">The SAFEARRAYBOUND structure represents the bounds of one dimension of a SAFEARRAY or SAFEARRAY2.</span></span> <span data-ttu-id="cbf24-756">Su formato es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-756">Its format is:</span></span>



<span data-ttu-id="cbf24-757">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-757">0</span></span>

<span data-ttu-id="cbf24-758">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-758">1</span></span>

<span data-ttu-id="cbf24-759">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-759">2</span></span>

<span data-ttu-id="cbf24-760">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-760">3</span></span>

<span data-ttu-id="cbf24-761">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-761">4</span></span>

<span data-ttu-id="cbf24-762">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-762">5</span></span>

<span data-ttu-id="cbf24-763">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-763">6</span></span>

<span data-ttu-id="cbf24-764">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-764">7</span></span>

<span data-ttu-id="cbf24-765">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-765">8</span></span>

<span data-ttu-id="cbf24-766">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-766">9</span></span>

<span data-ttu-id="cbf24-767">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-767">1</span></span><br/> <span data-ttu-id="cbf24-768">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-768">0</span></span><br/>

<span data-ttu-id="cbf24-769">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-769">1</span></span>

<span data-ttu-id="cbf24-770">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-770">2</span></span>

<span data-ttu-id="cbf24-771">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-771">3</span></span>

<span data-ttu-id="cbf24-772">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-772">4</span></span>

<span data-ttu-id="cbf24-773">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-773">5</span></span>

<span data-ttu-id="cbf24-774">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-774">6</span></span>

<span data-ttu-id="cbf24-775">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-775">7</span></span>

<span data-ttu-id="cbf24-776">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-776">8</span></span>

<span data-ttu-id="cbf24-777">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-777">9</span></span>

<span data-ttu-id="cbf24-778">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-778">2</span></span><br/> <span data-ttu-id="cbf24-779">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-779">0</span></span><br/>

<span data-ttu-id="cbf24-780">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-780">1</span></span>

<span data-ttu-id="cbf24-781">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-781">2</span></span>

<span data-ttu-id="cbf24-782">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-782">3</span></span>

<span data-ttu-id="cbf24-783">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-783">4</span></span>

<span data-ttu-id="cbf24-784">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-784">5</span></span>

<span data-ttu-id="cbf24-785">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-785">6</span></span>

<span data-ttu-id="cbf24-786">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-786">7</span></span>

<span data-ttu-id="cbf24-787">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-787">8</span></span>

<span data-ttu-id="cbf24-788">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-788">9</span></span>

<span data-ttu-id="cbf24-789">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-789">3</span></span><br/> <span data-ttu-id="cbf24-790">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-790">0</span></span><br/>

<span data-ttu-id="cbf24-791">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-791">1</span></span>

<span data-ttu-id="cbf24-792">cElements</span><span class="sxs-lookup"><span data-stu-id="cbf24-792">cElements</span></span>

<span data-ttu-id="cbf24-793">lLbound</span><span class="sxs-lookup"><span data-stu-id="cbf24-793">lLbound</span></span>



 

<span data-ttu-id="cbf24-794">**cElements:** entero de 32 bits sin signo que especifica el número de elementos de la dimensión.</span><span class="sxs-lookup"><span data-stu-id="cbf24-794">**cElements**: A 32-bit unsigned integer, specifying the number of elements in the dimension.</span></span>

<span data-ttu-id="cbf24-795">**lLbound:** entero de 32 bits sin signo que especifica el límite inferior de la dimensión.</span><span class="sxs-lookup"><span data-stu-id="cbf24-795">**lLbound**: A 32-bit unsigned integer, specifying the lower bound of the dimension.</span></span>

### <a name="221115-safearray2"></a><span data-ttu-id="cbf24-796">2.2.1.1.1.5 SAFEARRAY2</span><span class="sxs-lookup"><span data-stu-id="cbf24-796">2.2.1.1.1.5 SAFEARRAY2</span></span>

<span data-ttu-id="cbf24-797">SAFEARRAY2 se usa para pasar matrices multidimensionales en SERIALIZEDPROPERTYVALUE.</span><span class="sxs-lookup"><span data-stu-id="cbf24-797">SAFEARRAY2 is used to pass multidimensional arrays in SERIALIZEDPROPERTYVALUE.</span></span> <span data-ttu-id="cbf24-798">La estructura contiene información de límites, así como los datos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-798">The structure contains boundary information as well as the data.</span></span>



<span data-ttu-id="cbf24-799">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-799">0</span></span>

<span data-ttu-id="cbf24-800">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-800">1</span></span>

<span data-ttu-id="cbf24-801">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-801">2</span></span>

<span data-ttu-id="cbf24-802">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-802">3</span></span>

<span data-ttu-id="cbf24-803">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-803">4</span></span>

<span data-ttu-id="cbf24-804">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-804">5</span></span>

<span data-ttu-id="cbf24-805">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-805">6</span></span>

<span data-ttu-id="cbf24-806">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-806">7</span></span>

<span data-ttu-id="cbf24-807">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-807">8</span></span>

<span data-ttu-id="cbf24-808">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-808">9</span></span>

<span data-ttu-id="cbf24-809">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-809">1</span></span><br/> <span data-ttu-id="cbf24-810">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-810">0</span></span><br/>

<span data-ttu-id="cbf24-811">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-811">1</span></span>

<span data-ttu-id="cbf24-812">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-812">2</span></span>

<span data-ttu-id="cbf24-813">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-813">3</span></span>

<span data-ttu-id="cbf24-814">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-814">4</span></span>

<span data-ttu-id="cbf24-815">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-815">5</span></span>

<span data-ttu-id="cbf24-816">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-816">6</span></span>

<span data-ttu-id="cbf24-817">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-817">7</span></span>

<span data-ttu-id="cbf24-818">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-818">8</span></span>

<span data-ttu-id="cbf24-819">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-819">9</span></span>

<span data-ttu-id="cbf24-820">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-820">2</span></span><br/> <span data-ttu-id="cbf24-821">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-821">0</span></span><br/>

<span data-ttu-id="cbf24-822">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-822">1</span></span>

<span data-ttu-id="cbf24-823">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-823">2</span></span>

<span data-ttu-id="cbf24-824">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-824">3</span></span>

<span data-ttu-id="cbf24-825">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-825">4</span></span>

<span data-ttu-id="cbf24-826">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-826">5</span></span>

<span data-ttu-id="cbf24-827">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-827">6</span></span>

<span data-ttu-id="cbf24-828">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-828">7</span></span>

<span data-ttu-id="cbf24-829">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-829">8</span></span>

<span data-ttu-id="cbf24-830">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-830">9</span></span>

<span data-ttu-id="cbf24-831">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-831">3</span></span><br/> <span data-ttu-id="cbf24-832">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-832">0</span></span><br/>

<span data-ttu-id="cbf24-833">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-833">1</span></span>

<span data-ttu-id="cbf24-834">cDims</span><span class="sxs-lookup"><span data-stu-id="cbf24-834">cDims</span></span>

<span data-ttu-id="cbf24-835">Rgsabound (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-835">Rgsabound (variable)</span></span>

<span data-ttu-id="cbf24-836">vData (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-836">vData (variable)</span></span>



 

<span data-ttu-id="cbf24-837">**cDims:** entero de 32 bits sin signo, que indica el número de dimensiones de SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="cbf24-837">**cDims**: Unsigned 32-bit integer, indicating the number of dimensions of the SAFEARRAY2.</span></span>

<span data-ttu-id="cbf24-838">**Rgsabound:** matriz que contiene una estructura SAFEARRAYBOUND, como se especifica en la sección 2.2.1.1.1.4 por dimensión de SAFEARRAY2.</span><span class="sxs-lookup"><span data-stu-id="cbf24-838">**Rgsabound**: An array that contains one SAFEARRAYBOUND structure, as specified in section 2.2.1.1.1.4 per dimension in the SAFEARRAY2.</span></span> <span data-ttu-id="cbf24-839">Esta matriz tiene la dimensión más a la izquierda en primer lugar y la última dimensión más a la derecha.</span><span class="sxs-lookup"><span data-stu-id="cbf24-839">This array has left-most dimension first, and right-most dimension last.</span></span>

<span data-ttu-id="cbf24-840">**vData:** vector de elementos serializados de un tipo determinado, indicados por dwType de la clase SERIALIZEDPROPERTYVALUE que contiene, con valores de 0x2000 borrados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-840">**vData**: A vector of marshaled items of a particular type, indicated by the dwType of the containing SERIALIZEDPROPERTYVALUE, with bit 0x2000 cleared.</span></span> <span data-ttu-id="cbf24-841">El formato de vData es el mismo que el especificado para el campo vData de SAFEARRAY en la sección 2.2.1.1.1.3.</span><span class="sxs-lookup"><span data-stu-id="cbf24-841">The format of vData the same as that specified for the vData field of SAFEARRAY in Section 2.2.1.1.1.3.</span></span>

### <a name="2212-cfullpropspec"></a><span data-ttu-id="cbf24-842">2.2.1.2 CFullPropSpec</span><span class="sxs-lookup"><span data-stu-id="cbf24-842">2.2.1.2 CFullPropSpec</span></span>

<span data-ttu-id="cbf24-843">La estructura CFullPropSpec contiene un GUID del conjunto de propiedades y un identificador de propiedad para identificar de forma única la propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-843">The CFullPropSpec structure contains a property set GUID and a property identifier to uniquely identify property.</span></span>



<span data-ttu-id="cbf24-844">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-844">0</span></span>

<span data-ttu-id="cbf24-845">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-845">1</span></span>

<span data-ttu-id="cbf24-846">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-846">2</span></span>

<span data-ttu-id="cbf24-847">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-847">3</span></span>

<span data-ttu-id="cbf24-848">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-848">4</span></span>

<span data-ttu-id="cbf24-849">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-849">5</span></span>

<span data-ttu-id="cbf24-850">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-850">6</span></span>

<span data-ttu-id="cbf24-851">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-851">7</span></span>

<span data-ttu-id="cbf24-852">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-852">8</span></span>

<span data-ttu-id="cbf24-853">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-853">9</span></span>

<span data-ttu-id="cbf24-854">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-854">1</span></span><br/> <span data-ttu-id="cbf24-855">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-855">0</span></span><br/>

<span data-ttu-id="cbf24-856">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-856">1</span></span>

<span data-ttu-id="cbf24-857">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-857">2</span></span>

<span data-ttu-id="cbf24-858">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-858">3</span></span>

<span data-ttu-id="cbf24-859">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-859">4</span></span>

<span data-ttu-id="cbf24-860">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-860">5</span></span>

<span data-ttu-id="cbf24-861">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-861">6</span></span>

<span data-ttu-id="cbf24-862">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-862">7</span></span>

<span data-ttu-id="cbf24-863">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-863">8</span></span>

<span data-ttu-id="cbf24-864">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-864">9</span></span>

<span data-ttu-id="cbf24-865">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-865">2</span></span><br/> <span data-ttu-id="cbf24-866">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-866">0</span></span><br/>

<span data-ttu-id="cbf24-867">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-867">1</span></span>

<span data-ttu-id="cbf24-868">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-868">2</span></span>

<span data-ttu-id="cbf24-869">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-869">3</span></span>

<span data-ttu-id="cbf24-870">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-870">4</span></span>

<span data-ttu-id="cbf24-871">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-871">5</span></span>

<span data-ttu-id="cbf24-872">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-872">6</span></span>

<span data-ttu-id="cbf24-873">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-873">7</span></span>

<span data-ttu-id="cbf24-874">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-874">8</span></span>

<span data-ttu-id="cbf24-875">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-875">9</span></span>

<span data-ttu-id="cbf24-876">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-876">3</span></span><br/> <span data-ttu-id="cbf24-877">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-877">0</span></span><br/>

<span data-ttu-id="cbf24-878">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-878">1</span></span>

<span data-ttu-id="cbf24-879">\_guidPropSet</span><span class="sxs-lookup"><span data-stu-id="cbf24-879">\_guidPropSet</span></span>

<span data-ttu-id="cbf24-880">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-880">...</span></span>

<span data-ttu-id="cbf24-881">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-881">...</span></span>

<span data-ttu-id="cbf24-882">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-882">...</span></span>

<span data-ttu-id="cbf24-883">ulKind</span><span class="sxs-lookup"><span data-stu-id="cbf24-883">ulKind</span></span>

<span data-ttu-id="cbf24-884">PrSpec</span><span class="sxs-lookup"><span data-stu-id="cbf24-884">PrSpec</span></span>

<span data-ttu-id="cbf24-885">Nombre de propiedad (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-885">Property name (variable)</span></span>



 

<span data-ttu-id="cbf24-886">**\_ guidPropSet:** GUID del conjunto de propiedades al que pertenece la propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-886">**\_guidPropSet**: The GUID of the property set to which the property belongs.</span></span>

<span data-ttu-id="cbf24-887">**ulKind:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-887">**ulKind**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cbf24-888">Uno de los valores siguientes, que indica el contenido de PrSpec.</span><span class="sxs-lookup"><span data-stu-id="cbf24-888">One of the following values below, that indicates the contents of PrSpec.</span></span>



| <span data-ttu-id="cbf24-889">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-889">Value</span></span>                                            | <span data-ttu-id="cbf24-890">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-890">Meaning</span></span>                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-891">PRSPEC \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="cbf24-891">PRSPEC\_ LPWSTR</span></span><br/> <span data-ttu-id="cbf24-892">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-892">0x00000000</span></span><br/> | <span data-ttu-id="cbf24-893">El campo PrSpec especifica el número de caracteres que no son NULL en el campo Nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-893">The PrSpec field specifies the number of non-NULL characters in the Property name field.</span></span> |
| <span data-ttu-id="cbf24-894">PRSPEC \_ PROPID</span><span class="sxs-lookup"><span data-stu-id="cbf24-894">PRSPEC\_PROPID</span></span><br/> <span data-ttu-id="cbf24-895">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-895">0x00000001</span></span><br/>  | <span data-ttu-id="cbf24-896">El campo PrSpec especifica el identificador de propiedad (PROPID).</span><span class="sxs-lookup"><span data-stu-id="cbf24-896">The PrSpec field specifies the property ID (PROPID).</span></span>                                     |



 

<span data-ttu-id="cbf24-897">**PrSpec:** entero de 32 bits sin signo con un significado indicado por el campo ulKind.</span><span class="sxs-lookup"><span data-stu-id="cbf24-897">**PrSpec**: A 32-bit unsigned integer with a meaning as indicated by the ulKind field.</span></span>

<span data-ttu-id="cbf24-898">**Nombre de** propiedad: si ulKind se establece en PRSPEC \_ PROPID, este campo NO DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-898">**Property name**: If ulKind is set to PRSPEC\_PROPID, this field MUST NOT be present.</span></span> <span data-ttu-id="cbf24-899">Si ulKind se establece en PRSPEC LPWSTR, este campo DEBE contener una matriz sin mayúsculas y minúsculas de caracteres Unicode que no son NULL de PrSpec, que contiene el nombre de la \_ propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-899">If ulKind is set to PRSPEC\_LPWSTR, then this field MUST contain a case-insensitive array of PrSpec non-null Unicode characters, containing the name of the property.</span></span>

### <a name="2213-ccontentrestriction"></a><span data-ttu-id="cbf24-900">2.2.1.3 CContentRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-900">2.2.1.3 CContentRestriction</span></span>

<span data-ttu-id="cbf24-901">La estructura CContentRestriction contiene una cadena que debe coincidir con una propiedad de la caché de propiedades.</span><span class="sxs-lookup"><span data-stu-id="cbf24-901">The CContentRestriction structure contains a string to match for a property in the property cache.</span></span>



<span data-ttu-id="cbf24-902">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-902">0</span></span>

<span data-ttu-id="cbf24-903">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-903">1</span></span>

<span data-ttu-id="cbf24-904">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-904">2</span></span>

<span data-ttu-id="cbf24-905">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-905">3</span></span>

<span data-ttu-id="cbf24-906">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-906">4</span></span>

<span data-ttu-id="cbf24-907">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-907">5</span></span>

<span data-ttu-id="cbf24-908">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-908">6</span></span>

<span data-ttu-id="cbf24-909">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-909">7</span></span>

<span data-ttu-id="cbf24-910">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-910">8</span></span>

<span data-ttu-id="cbf24-911">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-911">9</span></span>

<span data-ttu-id="cbf24-912">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-912">1</span></span><br/> <span data-ttu-id="cbf24-913">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-913">0</span></span><br/>

<span data-ttu-id="cbf24-914">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-914">1</span></span>

<span data-ttu-id="cbf24-915">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-915">2</span></span>

<span data-ttu-id="cbf24-916">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-916">3</span></span>

<span data-ttu-id="cbf24-917">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-917">4</span></span>

<span data-ttu-id="cbf24-918">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-918">5</span></span>

<span data-ttu-id="cbf24-919">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-919">6</span></span>

<span data-ttu-id="cbf24-920">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-920">7</span></span>

<span data-ttu-id="cbf24-921">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-921">8</span></span>

<span data-ttu-id="cbf24-922">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-922">9</span></span>

<span data-ttu-id="cbf24-923">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-923">2</span></span><br/> <span data-ttu-id="cbf24-924">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-924">0</span></span><br/>

<span data-ttu-id="cbf24-925">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-925">1</span></span>

<span data-ttu-id="cbf24-926">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-926">2</span></span>

<span data-ttu-id="cbf24-927">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-927">3</span></span>

<span data-ttu-id="cbf24-928">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-928">4</span></span>

<span data-ttu-id="cbf24-929">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-929">5</span></span>

<span data-ttu-id="cbf24-930">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-930">6</span></span>

<span data-ttu-id="cbf24-931">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-931">7</span></span>

<span data-ttu-id="cbf24-932">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-932">8</span></span>

<span data-ttu-id="cbf24-933">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-933">9</span></span>

<span data-ttu-id="cbf24-934">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-934">3</span></span><br/> <span data-ttu-id="cbf24-935">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-935">0</span></span><br/>

<span data-ttu-id="cbf24-936">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-936">1</span></span>

<span data-ttu-id="cbf24-937">\_Propiedad (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-937">\_Property (variable)</span></span>

<span data-ttu-id="cbf24-938">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-938">...</span></span>

<span data-ttu-id="cbf24-939">Padding1 (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-939">Padding1 (variable)</span></span>

<span data-ttu-id="cbf24-940">CC</span><span class="sxs-lookup"><span data-stu-id="cbf24-940">Cc</span></span>

<span data-ttu-id="cbf24-941">\_pwcsPhrase (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-941">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="cbf24-942">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-942">...</span></span>

<span data-ttu-id="cbf24-943">Padding2 (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-943">Padding2 (variable)</span></span>

<span data-ttu-id="cbf24-944">lcid</span><span class="sxs-lookup"><span data-stu-id="cbf24-944">lcid</span></span>

<span data-ttu-id="cbf24-945">\_ulGenerateMethod</span><span class="sxs-lookup"><span data-stu-id="cbf24-945">\_ulGenerateMethod</span></span>



 

<span data-ttu-id="cbf24-946">**\_ Propiedad**: estructura CFullPropSpec, como se especifica en la sección 2.2.1.2.</span><span class="sxs-lookup"><span data-stu-id="cbf24-946">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2.</span></span> <span data-ttu-id="cbf24-947">Este campo indica la propiedad en la que se va a realizar una operación de coincidencia.</span><span class="sxs-lookup"><span data-stu-id="cbf24-947">This field indicates the property on which to perform a match operation.</span></span>

<span data-ttu-id="cbf24-948">**Padding1:** este campo DEBE tener una longitud de 0 a 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-948">**Padding1**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cbf24-949">La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="cbf24-949">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cbf24-950">Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cbf24-950">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cbf24-951">El receptor DEBE omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-951">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cbf24-952">**Cc:** entero de 32 bits sin signo que especifica el número de caracteres en el \_ campo pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="cbf24-952">**Cc**: A 32-bit unsigned integer, specifying the number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="cbf24-953">**\_ pwcsPhrase:** cadena Unicode no terminada en NULL que representa la palabra o frase que se debe coincidir con la propiedad .</span><span class="sxs-lookup"><span data-stu-id="cbf24-953">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="cbf24-954">Este campo NO DEBE estar vacío.</span><span class="sxs-lookup"><span data-stu-id="cbf24-954">This field MUST NOT be empty.</span></span> <span data-ttu-id="cbf24-955">El campo Cc contiene la longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="cbf24-955">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="cbf24-956">**Padding2:** este campo DEBE tener una longitud de 0 a 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-956">**Padding2**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cbf24-957">La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="cbf24-957">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cbf24-958">Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cbf24-958">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cbf24-959">El receptor DEBE omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-959">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cbf24-960">**Lcid:** entero de 32 bits sin signo, que indica la configuración regional de pwcsPhrase, como se especifica en el Apéndice A de \_ \[ MS-GPSI. \]</span><span class="sxs-lookup"><span data-stu-id="cbf24-960">**Lcid**: A 32-bit unsigned integer, indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

<span data-ttu-id="cbf24-961">**\_ ulGenerateMethod:** entero de 32 bits sin signo que especifica el método que se usará al generar formularios de palabras alternativos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-961">**\_ulGenerateMethod**: A 32-bit unsigned integer, specifying the method to use when generating alternate word forms</span></span>



| <span data-ttu-id="cbf24-962">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-962">Value</span></span>                                                       | <span data-ttu-id="cbf24-963">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-963">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-964">GENERATE \_ METHOD \_ EXACT</span><span class="sxs-lookup"><span data-stu-id="cbf24-964">GENERATE\_METHOD\_EXACT</span></span><br/> <span data-ttu-id="cbf24-965">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-965">0x00000000</span></span><br/>    | <span data-ttu-id="cbf24-966">Coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-966">Exact match.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="cbf24-967">GENERAR \_ PREFIJO DE \_ MÉTODO</span><span class="sxs-lookup"><span data-stu-id="cbf24-967">GENERATE\_METHOD\_PREFIX</span></span><br/> <span data-ttu-id="cbf24-968">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-968">0x00000001</span></span> <br/>  | <span data-ttu-id="cbf24-969">Coincidencia de prefijo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-969">Prefix match.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="cbf24-970">GENERATE \_ METHOD \_ INFLECT</span><span class="sxs-lookup"><span data-stu-id="cbf24-970">GENERATE\_METHOD\_INFLECT</span></span> <br/> <span data-ttu-id="cbf24-971">0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbf24-971">0x00000002</span></span><br/> | <span data-ttu-id="cbf24-972">Coincide con las inflexiones de una palabra.</span><span class="sxs-lookup"><span data-stu-id="cbf24-972">Matches inflections of a word.</span></span> <span data-ttu-id="cbf24-973">Una inflexión de una palabra es una variante de la palabra raíz en la misma parte de la voz que se ha modificado según las reglas lingüísticas de un idioma determinado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-973">An inflection of a word is a variant of the root word in the same part of speech that has been modified according to linguistic rules of a given language.</span></span> <span data-ttu-id="cbf24-974">Por ejemplo, las inflexiones del verbo "nado" en inglés incluyen "nada", "nada", "nada" y "nada".</span><span class="sxs-lookup"><span data-stu-id="cbf24-974">For example, inflections of the verb "swim" in English include "swim", "swims", "swimming", and "swam".</span></span> |



 

### <a name="2214-ckey"></a><span data-ttu-id="cbf24-975">2.2.1.4 CKey</span><span class="sxs-lookup"><span data-stu-id="cbf24-975">2.2.1.4 CKey</span></span>

<span data-ttu-id="cbf24-976">La estructura CKey contiene un valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-976">The CKey structure contains a property value.</span></span>



<span data-ttu-id="cbf24-977">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-977">0</span></span>

<span data-ttu-id="cbf24-978">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-978">1</span></span>

<span data-ttu-id="cbf24-979">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-979">2</span></span>

<span data-ttu-id="cbf24-980">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-980">3</span></span>

<span data-ttu-id="cbf24-981">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-981">4</span></span>

<span data-ttu-id="cbf24-982">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-982">5</span></span>

<span data-ttu-id="cbf24-983">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-983">6</span></span>

<span data-ttu-id="cbf24-984">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-984">7</span></span>

<span data-ttu-id="cbf24-985">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-985">8</span></span>

<span data-ttu-id="cbf24-986">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-986">9</span></span>

<span data-ttu-id="cbf24-987">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-987">1</span></span><br/> <span data-ttu-id="cbf24-988">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-988">0</span></span><br/>

<span data-ttu-id="cbf24-989">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-989">1</span></span>

<span data-ttu-id="cbf24-990">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-990">2</span></span>

<span data-ttu-id="cbf24-991">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-991">3</span></span>

<span data-ttu-id="cbf24-992">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-992">4</span></span>

<span data-ttu-id="cbf24-993">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-993">5</span></span>

<span data-ttu-id="cbf24-994">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-994">6</span></span>

<span data-ttu-id="cbf24-995">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-995">7</span></span>

<span data-ttu-id="cbf24-996">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-996">8</span></span>

<span data-ttu-id="cbf24-997">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-997">9</span></span>

<span data-ttu-id="cbf24-998">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-998">2</span></span><br/> <span data-ttu-id="cbf24-999">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-999">0</span></span><br/>

<span data-ttu-id="cbf24-1000">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1000">1</span></span>

<span data-ttu-id="cbf24-1001">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1001">2</span></span>

<span data-ttu-id="cbf24-1002">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1002">3</span></span>

<span data-ttu-id="cbf24-1003">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1003">4</span></span>

<span data-ttu-id="cbf24-1004">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1004">5</span></span>

<span data-ttu-id="cbf24-1005">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1005">6</span></span>

<span data-ttu-id="cbf24-1006">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1006">7</span></span>

<span data-ttu-id="cbf24-1007">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1007">8</span></span>

<span data-ttu-id="cbf24-1008">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1008">9</span></span>

<span data-ttu-id="cbf24-1009">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1009">3</span></span><br/> <span data-ttu-id="cbf24-1010">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1010">0</span></span><br/>

<span data-ttu-id="cbf24-1011">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1011">1</span></span>

<span data-ttu-id="cbf24-1012">PROPID</span><span class="sxs-lookup"><span data-stu-id="cbf24-1012">PROPID</span></span>

<span data-ttu-id="cbf24-1013">Cb</span><span class="sxs-lookup"><span data-stu-id="cbf24-1013">Cb</span></span>

<span data-ttu-id="cbf24-1014">buf (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1014">buf (variable)</span></span>



 

<span data-ttu-id="cbf24-1015">**PROPID:** entero de 32 bits sin signo que representa el identificador de propiedad como se describe en la sección 1.8.1.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1015">**PROPID**: A 32-bit unsigned integer, representing the property ID as discussed in section 1.8.1.</span></span> <span data-ttu-id="cbf24-1016">Los valores conocidos son:</span><span class="sxs-lookup"><span data-stu-id="cbf24-1016">Well-known values are:</span></span>



| <span data-ttu-id="cbf24-1017">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-1017">Value</span></span>      | <span data-ttu-id="cbf24-1018">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-1018">Meaning</span></span>                                                 |
|------------|---------------------------------------------------------|
| <span data-ttu-id="cbf24-1019">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="cbf24-1019">0xFFFFFFFF</span></span> | <span data-ttu-id="cbf24-1020">Representa un identificador de propiedad no válido y NO SE DEBE usar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1020">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="cbf24-1021">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="cbf24-1021">0xFFFFFFFE</span></span> | <span data-ttu-id="cbf24-1022">Representa un identificador de propiedad no válido y NO SE DEBE usar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1022">Represents an invalid property ID and MUST NOT be used.</span></span> |
| <span data-ttu-id="cbf24-1023">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-1023">0x00000000</span></span> | <span data-ttu-id="cbf24-1024">Representa cualquier identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1024">Represents any property ID.</span></span>                             |



 

<span data-ttu-id="cbf24-1025">**Cb:** entero de 32 bits sin signo que contiene la longitud de buf, en bytes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1025">**Cb**: A 32-bit unsigned integer containing the length of buf, in bytes.</span></span>

<span data-ttu-id="cbf24-1026">**buf:** secuencia de bytes que representa el valor de la propiedad .</span><span class="sxs-lookup"><span data-stu-id="cbf24-1026">**buf**: A sequence of bytes representing the value of the property.</span></span>

### <a name="2215-cinternalpropertyrestriction"></a><span data-ttu-id="cbf24-1027">2.2.1.5 CInternalPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-1027">2.2.1.5 CInternalPropertyRestriction</span></span>

<span data-ttu-id="cbf24-1028">La estructura CInternalPropertyRestriction contiene un valor de propiedad que debe coincidir con una operación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1028">The CInternalPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="cbf24-1029">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1029">0</span></span>

<span data-ttu-id="cbf24-1030">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1030">1</span></span>

<span data-ttu-id="cbf24-1031">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1031">2</span></span>

<span data-ttu-id="cbf24-1032">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1032">3</span></span>

<span data-ttu-id="cbf24-1033">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1033">4</span></span>

<span data-ttu-id="cbf24-1034">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1034">5</span></span>

<span data-ttu-id="cbf24-1035">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1035">6</span></span>

<span data-ttu-id="cbf24-1036">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1036">7</span></span>

<span data-ttu-id="cbf24-1037">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1037">8</span></span>

<span data-ttu-id="cbf24-1038">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1038">9</span></span>

<span data-ttu-id="cbf24-1039">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1039">1</span></span><br/> <span data-ttu-id="cbf24-1040">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1040">0</span></span><br/>

<span data-ttu-id="cbf24-1041">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1041">1</span></span>

<span data-ttu-id="cbf24-1042">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1042">2</span></span>

<span data-ttu-id="cbf24-1043">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1043">3</span></span>

<span data-ttu-id="cbf24-1044">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1044">4</span></span>

<span data-ttu-id="cbf24-1045">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1045">5</span></span>

<span data-ttu-id="cbf24-1046">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1046">6</span></span>

<span data-ttu-id="cbf24-1047">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1047">7</span></span>

<span data-ttu-id="cbf24-1048">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1048">8</span></span>

<span data-ttu-id="cbf24-1049">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1049">9</span></span>

<span data-ttu-id="cbf24-1050">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1050">2</span></span><br/> <span data-ttu-id="cbf24-1051">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1051">0</span></span><br/>

<span data-ttu-id="cbf24-1052">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1052">1</span></span>

<span data-ttu-id="cbf24-1053">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1053">2</span></span>

<span data-ttu-id="cbf24-1054">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1054">3</span></span>

<span data-ttu-id="cbf24-1055">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1055">4</span></span>

<span data-ttu-id="cbf24-1056">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1056">5</span></span>

<span data-ttu-id="cbf24-1057">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1057">6</span></span>

<span data-ttu-id="cbf24-1058">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1058">7</span></span>

<span data-ttu-id="cbf24-1059">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1059">8</span></span>

<span data-ttu-id="cbf24-1060">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1060">9</span></span>

<span data-ttu-id="cbf24-1061">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1061">3</span></span><br/> <span data-ttu-id="cbf24-1062">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1062">0</span></span><br/>

<span data-ttu-id="cbf24-1063">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1063">1</span></span>

<span data-ttu-id="cbf24-1064">\_volver a reestechar</span><span class="sxs-lookup"><span data-stu-id="cbf24-1064">\_relop</span></span>

<span data-ttu-id="cbf24-1065">\_Pid</span><span class="sxs-lookup"><span data-stu-id="cbf24-1065">\_pid</span></span>

<span data-ttu-id="cbf24-1066">\_prval (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1066">\_prval (variable)</span></span>

<span data-ttu-id="cbf24-1067">restrictionPresent</span><span class="sxs-lookup"><span data-stu-id="cbf24-1067">restrictionPresent</span></span>

<span data-ttu-id="cbf24-1068">nextRestriction (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1068">nextRestriction (variable)</span></span>



 

<span data-ttu-id="cbf24-1069">**\_ rehard:** entero de 32 bits que especifica la relación que se va a realizar en la propiedad .</span><span class="sxs-lookup"><span data-stu-id="cbf24-1069">**\_relop**: A 32-bit integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="cbf24-1070">DEBE ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="cbf24-1070">MUST be one of the following values:</span></span>



| <span data-ttu-id="cbf24-1071">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-1071">Value</span></span>                 | <span data-ttu-id="cbf24-1072">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-1072">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-1073">PrLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-1073">PRLT 0x00000000</span></span>       | <span data-ttu-id="cbf24-1074">Una comparación menor que.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1074">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="cbf24-1075">PrLE 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-1075">PRLE 0x00000001</span></span>       | <span data-ttu-id="cbf24-1076">Comparación menor o igual que.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1076">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="cbf24-1077">PrGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbf24-1077">PRGT 0x00000002</span></span>       | <span data-ttu-id="cbf24-1078">Una comparación mayor que.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1078">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="cbf24-1079">PRGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cbf24-1079">PRGE 0x00000003</span></span>       | <span data-ttu-id="cbf24-1080">Una comparación mayor o igual que.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1080">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="cbf24-1081">Requisitos previos 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cbf24-1081">PREQ 0x00000004</span></span>       | <span data-ttu-id="cbf24-1082">Comparación de igualdad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1082">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="cbf24-1083">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="cbf24-1083">PRNE 0x00000005</span></span>       | <span data-ttu-id="cbf24-1084">Comparación no igual.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1084">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="cbf24-1085">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="cbf24-1085">PRRE 0x00000006</span></span>       | <span data-ttu-id="cbf24-1086">Comparación de expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1086">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="cbf24-1087">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="cbf24-1087">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="cbf24-1088">AND bit a bit que devuelve el operando derecho.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1088">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="cbf24-1089">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cbf24-1089">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="cbf24-1090">AND bit a bit que devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1090">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="cbf24-1091">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="cbf24-1091">PRAll 0x00000100</span></span>      | <span data-ttu-id="cbf24-1092">La operación se va a realizar en una columna de un conjunto de filas y solo es true si la operación es verdadera para todas las filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1092">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="cbf24-1093">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="cbf24-1093">PRAny 0x00000200</span></span>      | <span data-ttu-id="cbf24-1094">La operación se va a realizar en una columna de un conjunto de filas y es true si la operación es verdadera para cualquier fila.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1094">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="cbf24-1095">**\_ pid:** entero de 32 bits sin signo que representa el identificador de propiedad (vea PROPID en la sección 2.2.1.4).</span><span class="sxs-lookup"><span data-stu-id="cbf24-1095">**\_pid**: A 32-bit unsigned integer, representing the property ID (see PROPID in section 2.2.1.4).</span></span>

<span data-ttu-id="cbf24-1096">**\_ prval:** CBaseStorageVariant que contiene el valor que se relaciona con la propiedad .</span><span class="sxs-lookup"><span data-stu-id="cbf24-1096">**\_prval**: A CBaseStorageVariant containing the value to relate to the property.</span></span>

<span data-ttu-id="cbf24-1097">**restrictionPresent:** valor de byte que indica si el campo nextRestriction está presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1097">**restrictionPresent**: A byte value indicating if the nextRestriction field is present.</span></span> <span data-ttu-id="cbf24-1098">DEBE establecerse en 0x00 o 0x01.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1098">MUST be set to either 0x00 or 0x01.</span></span> <span data-ttu-id="cbf24-1099">Si se establece en 0x01, restrictionPresent indica que el campo nextRestriction está presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1099">If set to 0x01, restrictionPresent indicates that the nextRestriction field is present.</span></span> <span data-ttu-id="cbf24-1100">Si se establece en 0x00, restrictionPresent indica que el campo nextRestriction no está presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1100">If set to 0x00, restrictionPresent indicates that the nextRestriction field is not present.</span></span>

<span data-ttu-id="cbf24-1101">**nextRestriction:** una estructura CRestriction, como se especifica en la sección 2.2.1.16, especificando una restricción adicional.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1101">**nextRestriction**: A CRestriction structure, as specified in section 2.2.1.16, specifying a further restriction.</span></span>

### <a name="2216-cnatlanguagerestriction"></a><span data-ttu-id="cbf24-1102">2.2.1.6 CNatLanguageRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-1102">2.2.1.6 CNatLanguageRestriction</span></span>

<span data-ttu-id="cbf24-1103">La estructura CNatLanguageRestriction contiene una coincidencia de consulta **en lenguaje natural** para una propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1103">The CNatLanguageRestriction structure contains a **natural language query** match for a property.</span></span>



<span data-ttu-id="cbf24-1104">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1104">0</span></span>

<span data-ttu-id="cbf24-1105">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1105">1</span></span>

<span data-ttu-id="cbf24-1106">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1106">2</span></span>

<span data-ttu-id="cbf24-1107">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1107">3</span></span>

<span data-ttu-id="cbf24-1108">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1108">4</span></span>

<span data-ttu-id="cbf24-1109">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1109">5</span></span>

<span data-ttu-id="cbf24-1110">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1110">6</span></span>

<span data-ttu-id="cbf24-1111">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1111">7</span></span>

<span data-ttu-id="cbf24-1112">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1112">8</span></span>

<span data-ttu-id="cbf24-1113">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1113">9</span></span>

<span data-ttu-id="cbf24-1114">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1114">1</span></span><br/> <span data-ttu-id="cbf24-1115">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1115">0</span></span><br/>

<span data-ttu-id="cbf24-1116">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1116">1</span></span>

<span data-ttu-id="cbf24-1117">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1117">2</span></span>

<span data-ttu-id="cbf24-1118">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1118">3</span></span>

<span data-ttu-id="cbf24-1119">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1119">4</span></span>

<span data-ttu-id="cbf24-1120">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1120">5</span></span>

<span data-ttu-id="cbf24-1121">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1121">6</span></span>

<span data-ttu-id="cbf24-1122">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1122">7</span></span>

<span data-ttu-id="cbf24-1123">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1123">8</span></span>

<span data-ttu-id="cbf24-1124">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1124">9</span></span>

<span data-ttu-id="cbf24-1125">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1125">2</span></span><br/> <span data-ttu-id="cbf24-1126">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1126">0</span></span><br/>

<span data-ttu-id="cbf24-1127">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1127">1</span></span>

<span data-ttu-id="cbf24-1128">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1128">2</span></span>

<span data-ttu-id="cbf24-1129">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1129">3</span></span>

<span data-ttu-id="cbf24-1130">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1130">4</span></span>

<span data-ttu-id="cbf24-1131">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1131">5</span></span>

<span data-ttu-id="cbf24-1132">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1132">6</span></span>

<span data-ttu-id="cbf24-1133">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1133">7</span></span>

<span data-ttu-id="cbf24-1134">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1134">8</span></span>

<span data-ttu-id="cbf24-1135">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1135">9</span></span>

<span data-ttu-id="cbf24-1136">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1136">3</span></span><br/> <span data-ttu-id="cbf24-1137">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1137">0</span></span><br/>

<span data-ttu-id="cbf24-1138">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1138">1</span></span>

<span data-ttu-id="cbf24-1139">\_Propiedad (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1139">\_Property (variable)</span></span>

<span data-ttu-id="cbf24-1140">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-1140">...</span></span>

<span data-ttu-id="cbf24-1141">\_padding \_ cc (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1141">\_padding\_cc (variable)</span></span>

<span data-ttu-id="cbf24-1142">CC</span><span class="sxs-lookup"><span data-stu-id="cbf24-1142">Cc</span></span>

<span data-ttu-id="cbf24-1143">\_pwcsPhrase (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1143">\_pwcsPhrase (variable)</span></span>

<span data-ttu-id="cbf24-1144">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-1144">...</span></span>

<span data-ttu-id="cbf24-1145">\_padding \_ lcid (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1145">\_padding\_lcid (variable)</span></span>

<span data-ttu-id="cbf24-1146">Lcid</span><span class="sxs-lookup"><span data-stu-id="cbf24-1146">Lcid</span></span>



 

<span data-ttu-id="cbf24-1147">**\_ Propiedad**: una estructura CFullPropSpec, como se especifica en la sección 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1147">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.3.</span></span> <span data-ttu-id="cbf24-1148">Este campo indica la propiedad en la que se va a realizar la operación de coincidencia.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1148">This field indicates the property on which to perform the match operation.</span></span>

<span data-ttu-id="cbf24-1149">**\_ padding \_ cc:** este campo DEBE tener una longitud de 0 a 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1149">**\_padding\_cc**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cbf24-1150">La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1150">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cbf24-1151">Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1151">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cbf24-1152">El receptor DEBE omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1152">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cbf24-1153">**Cc:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1153">**Cc**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cbf24-1154">Número de caracteres del campo \_ pwcsPhrase.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1154">The number of characters in the \_pwcsPhrase field.</span></span>

<span data-ttu-id="cbf24-1155">**\_ pwcsPhrase:** una cadena Unicode terminada en null que representa la palabra o frase que se debe coincidir con la propiedad .</span><span class="sxs-lookup"><span data-stu-id="cbf24-1155">**\_pwcsPhrase**: A non null-terminated Unicode string representing the word or phrase to match for the property.</span></span> <span data-ttu-id="cbf24-1156">NO DEBE estar vacío.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1156">MUST NOT be empty.</span></span> <span data-ttu-id="cbf24-1157">El campo Cc contiene la longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1157">The Cc field contains the length of the string.</span></span>

<span data-ttu-id="cbf24-1158">**\_ padding \_ lcid:** este campo DEBE tener entre 0 y 3 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1158">**\_padding\_lcid**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cbf24-1159">La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1159">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cbf24-1160">Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1160">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cbf24-1161">El receptor DEBE omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1161">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cbf24-1162">**Lcid:** entero de 32 bits sin signo que indica la configuración regional de pwcsPhrase, como se especifica en el apéndice A de \_ \[ MS-GPSI. \]</span><span class="sxs-lookup"><span data-stu-id="cbf24-1162">**Lcid**: A 32-bit unsigned integer indicating the locale of \_pwcsPhrase, as specified in \[MS-GPSI\] Appendix A.</span></span>

### <a name="2217-cnoderestriction"></a><span data-ttu-id="cbf24-1163">2.2.1.7 CNodeRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-1163">2.2.1.7 CNodeRestriction</span></span>

<span data-ttu-id="cbf24-1164">La estructura CNodeRestriction contiene una matriz de **nodos de árbol** de comandos que especifican las restricciones para la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1164">The CNodeRestriction structure contains an array of **command tree** nodes that specify the restrictions for the query.</span></span>



<span data-ttu-id="cbf24-1165">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1165">0</span></span>

<span data-ttu-id="cbf24-1166">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1166">1</span></span>

<span data-ttu-id="cbf24-1167">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1167">2</span></span>

<span data-ttu-id="cbf24-1168">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1168">3</span></span>

<span data-ttu-id="cbf24-1169">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1169">4</span></span>

<span data-ttu-id="cbf24-1170">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1170">5</span></span>

<span data-ttu-id="cbf24-1171">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1171">6</span></span>

<span data-ttu-id="cbf24-1172">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1172">7</span></span>

<span data-ttu-id="cbf24-1173">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1173">8</span></span>

<span data-ttu-id="cbf24-1174">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1174">9</span></span>

<span data-ttu-id="cbf24-1175">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1175">1</span></span><br/> <span data-ttu-id="cbf24-1176">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1176">0</span></span><br/>

<span data-ttu-id="cbf24-1177">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1177">1</span></span>

<span data-ttu-id="cbf24-1178">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1178">2</span></span>

<span data-ttu-id="cbf24-1179">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1179">3</span></span>

<span data-ttu-id="cbf24-1180">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1180">4</span></span>

<span data-ttu-id="cbf24-1181">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1181">5</span></span>

<span data-ttu-id="cbf24-1182">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1182">6</span></span>

<span data-ttu-id="cbf24-1183">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1183">7</span></span>

<span data-ttu-id="cbf24-1184">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1184">8</span></span>

<span data-ttu-id="cbf24-1185">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1185">9</span></span>

<span data-ttu-id="cbf24-1186">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1186">2</span></span><br/> <span data-ttu-id="cbf24-1187">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1187">0</span></span><br/>

<span data-ttu-id="cbf24-1188">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1188">1</span></span>

<span data-ttu-id="cbf24-1189">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1189">2</span></span>

<span data-ttu-id="cbf24-1190">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1190">3</span></span>

<span data-ttu-id="cbf24-1191">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1191">4</span></span>

<span data-ttu-id="cbf24-1192">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1192">5</span></span>

<span data-ttu-id="cbf24-1193">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1193">6</span></span>

<span data-ttu-id="cbf24-1194">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1194">7</span></span>

<span data-ttu-id="cbf24-1195">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1195">8</span></span>

<span data-ttu-id="cbf24-1196">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1196">9</span></span>

<span data-ttu-id="cbf24-1197">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1197">3</span></span><br/> <span data-ttu-id="cbf24-1198">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1198">0</span></span><br/>

<span data-ttu-id="cbf24-1199">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1199">1</span></span>

<span data-ttu-id="cbf24-1200">\_cNode</span><span class="sxs-lookup"><span data-stu-id="cbf24-1200">\_cNode</span></span>

<span data-ttu-id="cbf24-1201">\_paNode (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1201">\_paNode (variable)</span></span>



 

<span data-ttu-id="cbf24-1202">**\_ cNode:** entero de 32 bits sin signo que especifica el número de estructuras de CRestriction contenidas en el \_ campo paNode.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1202">**\_cNode**: A 32-bit unsigned integer specifying the number of CRestriction structures contained in the \_paNode field.</span></span>

<span data-ttu-id="cbf24-1203">**\_ paNode:** matriz de estructuras CRestriction.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1203">**\_paNode**: An array of CRestriction structures.</span></span> <span data-ttu-id="cbf24-1204">Las estructuras de la matriz DEBEN estar separadas por 0 a 3 bytes de relleno, de forma que cada estructura comience en un desplazamiento que sea un múltiplo de 4 bytes desde el principio del mensaje que contiene esta matriz.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1204">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="cbf24-1205">Si hay bytes de relleno, el valor que contienen es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1205">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="cbf24-1206">El receptor DEBE omitir el contenido de los bytes de relleno.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1206">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="2218-coccrestriction"></a><span data-ttu-id="cbf24-1207">2.2.1.8 COccRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-1207">2.2.1.8 COccRestriction</span></span>

<span data-ttu-id="cbf24-1208">La estructura COccRestriction contiene la ubicación de una palabra en una frase.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1208">The COccRestriction structure contains the location of a word in a phrase.</span></span>



<span data-ttu-id="cbf24-1209">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1209">0</span></span>

<span data-ttu-id="cbf24-1210">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1210">1</span></span>

<span data-ttu-id="cbf24-1211">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1211">2</span></span>

<span data-ttu-id="cbf24-1212">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1212">3</span></span>

<span data-ttu-id="cbf24-1213">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1213">4</span></span>

<span data-ttu-id="cbf24-1214">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1214">5</span></span>

<span data-ttu-id="cbf24-1215">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1215">6</span></span>

<span data-ttu-id="cbf24-1216">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1216">7</span></span>

<span data-ttu-id="cbf24-1217">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1217">8</span></span>

<span data-ttu-id="cbf24-1218">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1218">9</span></span>

<span data-ttu-id="cbf24-1219">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1219">1</span></span><br/> <span data-ttu-id="cbf24-1220">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1220">0</span></span><br/>

<span data-ttu-id="cbf24-1221">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1221">1</span></span>

<span data-ttu-id="cbf24-1222">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1222">2</span></span>

<span data-ttu-id="cbf24-1223">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1223">3</span></span>

<span data-ttu-id="cbf24-1224">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1224">4</span></span>

<span data-ttu-id="cbf24-1225">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1225">5</span></span>

<span data-ttu-id="cbf24-1226">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1226">6</span></span>

<span data-ttu-id="cbf24-1227">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1227">7</span></span>

<span data-ttu-id="cbf24-1228">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1228">8</span></span>

<span data-ttu-id="cbf24-1229">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1229">9</span></span>

<span data-ttu-id="cbf24-1230">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1230">2</span></span><br/> <span data-ttu-id="cbf24-1231">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1231">0</span></span><br/>

<span data-ttu-id="cbf24-1232">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1232">1</span></span>

<span data-ttu-id="cbf24-1233">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1233">2</span></span>

<span data-ttu-id="cbf24-1234">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1234">3</span></span>

<span data-ttu-id="cbf24-1235">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1235">4</span></span>

<span data-ttu-id="cbf24-1236">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1236">5</span></span>

<span data-ttu-id="cbf24-1237">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1237">6</span></span>

<span data-ttu-id="cbf24-1238">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1238">7</span></span>

<span data-ttu-id="cbf24-1239">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1239">8</span></span>

<span data-ttu-id="cbf24-1240">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1240">9</span></span>

<span data-ttu-id="cbf24-1241">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1241">3</span></span><br/> <span data-ttu-id="cbf24-1242">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1242">0</span></span><br/>

<span data-ttu-id="cbf24-1243">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1243">1</span></span>

<span data-ttu-id="cbf24-1244">\_Occ</span><span class="sxs-lookup"><span data-stu-id="cbf24-1244">\_occ</span></span>

<span data-ttu-id="cbf24-1245">\_cPrevNoiseWords</span><span class="sxs-lookup"><span data-stu-id="cbf24-1245">\_cPrevNoiseWords</span></span>

<span data-ttu-id="cbf24-1246">\_cNextNoiseWords</span><span class="sxs-lookup"><span data-stu-id="cbf24-1246">\_cNextNoiseWords</span></span>



 

<span data-ttu-id="cbf24-1247">**\_ occ:** entero de 32 bits sin signo que especifica el desplazamiento de la palabra en una cadena de consulta, en unidades de palabras.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1247">**\_occ**: A 32-bit unsigned integer specifying the offset of the word in a query string, in units of words.</span></span> <span data-ttu-id="cbf24-1248">Una palabra, como se usa en esta especificación, es una unidad de idioma en cualquier configuración regional que lleva significado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1248">A word, as used in this specification, is a unit of language in any locale that carries meaning.</span></span>

<span data-ttu-id="cbf24-1249">**\_ cPrevNoiseWords:** entero de 32 bits sin signo  que contiene el número de palabras de ruido que se producen entre esta palabra y la palabra anterior de la frase.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1249">**\_cPrevNoiseWords**: A 32-bit unsigned integer containing the number of **noise words** that occur between this word and the previous word in the phrase.</span></span>

<span data-ttu-id="cbf24-1250">**\_ cNextNoiseWords:** entero de 32 bits sin signo que contiene el número de palabras de ruido que se producen entre esta palabra y la siguiente palabra de la frase.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1250">**\_cNextNoiseWords**: A 32-bit unsigned integer containing the number of noise words that occur between this word and the next word in the phrase.</span></span>

### <a name="2219-cpropertyrestriction"></a><span data-ttu-id="cbf24-1251">2.2.1.9 CPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-1251">2.2.1.9 CPropertyRestriction</span></span>

<span data-ttu-id="cbf24-1252">La estructura CPropertyRestriction contiene un valor de propiedad que debe coincidir con una operación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1252">The CPropertyRestriction structure contains a property value to match with an operation.</span></span>



<span data-ttu-id="cbf24-1253">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1253">0</span></span>

<span data-ttu-id="cbf24-1254">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1254">1</span></span>

<span data-ttu-id="cbf24-1255">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1255">2</span></span>

<span data-ttu-id="cbf24-1256">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1256">3</span></span>

<span data-ttu-id="cbf24-1257">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1257">4</span></span>

<span data-ttu-id="cbf24-1258">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1258">5</span></span>

<span data-ttu-id="cbf24-1259">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1259">6</span></span>

<span data-ttu-id="cbf24-1260">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1260">7</span></span>

<span data-ttu-id="cbf24-1261">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1261">8</span></span>

<span data-ttu-id="cbf24-1262">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1262">9</span></span>

<span data-ttu-id="cbf24-1263">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1263">1</span></span><br/> <span data-ttu-id="cbf24-1264">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1264">0</span></span><br/>

<span data-ttu-id="cbf24-1265">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1265">1</span></span>

<span data-ttu-id="cbf24-1266">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1266">2</span></span>

<span data-ttu-id="cbf24-1267">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1267">3</span></span>

<span data-ttu-id="cbf24-1268">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1268">4</span></span>

<span data-ttu-id="cbf24-1269">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1269">5</span></span>

<span data-ttu-id="cbf24-1270">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1270">6</span></span>

<span data-ttu-id="cbf24-1271">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1271">7</span></span>

<span data-ttu-id="cbf24-1272">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1272">8</span></span>

<span data-ttu-id="cbf24-1273">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1273">9</span></span>

<span data-ttu-id="cbf24-1274">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1274">2</span></span><br/> <span data-ttu-id="cbf24-1275">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1275">0</span></span><br/>

<span data-ttu-id="cbf24-1276">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1276">1</span></span>

<span data-ttu-id="cbf24-1277">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1277">2</span></span>

<span data-ttu-id="cbf24-1278">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1278">3</span></span>

<span data-ttu-id="cbf24-1279">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1279">4</span></span>

<span data-ttu-id="cbf24-1280">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1280">5</span></span>

<span data-ttu-id="cbf24-1281">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1281">6</span></span>

<span data-ttu-id="cbf24-1282">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1282">7</span></span>

<span data-ttu-id="cbf24-1283">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1283">8</span></span>

<span data-ttu-id="cbf24-1284">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1284">9</span></span>

<span data-ttu-id="cbf24-1285">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1285">3</span></span><br/> <span data-ttu-id="cbf24-1286">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1286">0</span></span><br/>

<span data-ttu-id="cbf24-1287">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1287">1</span></span>

<span data-ttu-id="cbf24-1288">\_reeste</span><span class="sxs-lookup"><span data-stu-id="cbf24-1288">\_relop</span></span>

<span data-ttu-id="cbf24-1289">\_Propiedad (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1289">\_Property (variable)</span></span>

<span data-ttu-id="cbf24-1290">\_prval (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1290">\_prval (variable)</span></span>



 

<span data-ttu-id="cbf24-1291">**\_ reed:** entero de 32 bits sin signo que especifica la relación que se va a realizar en la propiedad .</span><span class="sxs-lookup"><span data-stu-id="cbf24-1291">**\_relop**: A 32-bit unsigned integer specifying the relation to perform on the property.</span></span> <span data-ttu-id="cbf24-1292">DEBE ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1292">MUST be one of the following values.</span></span>



| <span data-ttu-id="cbf24-1293">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-1293">Value</span></span>                 | <span data-ttu-id="cbf24-1294">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-1294">Meaning</span></span>                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-1295">PRLT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-1295">PRLT 0x00000000</span></span>       | <span data-ttu-id="cbf24-1296">Una comparación menor que.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1296">A less-than comparison.</span></span>                                                                                           |
| <span data-ttu-id="cbf24-1297">Prle 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-1297">PRLE 0x00000001</span></span>       | <span data-ttu-id="cbf24-1298">Una comparación menor o igual que.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1298">A less-than or equal-to comparison.</span></span>                                                                               |
| <span data-ttu-id="cbf24-1299">PrGT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbf24-1299">PRGT 0x00000002</span></span>       | <span data-ttu-id="cbf24-1300">Una comparación mayor que.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1300">A greater-than comparison.</span></span>                                                                                        |
| <span data-ttu-id="cbf24-1301">PRGE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cbf24-1301">PRGE 0x00000003</span></span>       | <span data-ttu-id="cbf24-1302">Una comparación mayor o igual que.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1302">A greater-than or equal-to comparison.</span></span>                                                                            |
| <span data-ttu-id="cbf24-1303">Preq 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cbf24-1303">PREQ 0x00000004</span></span>       | <span data-ttu-id="cbf24-1304">Comparación de igualdad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1304">An equality comparison.</span></span>                                                                                           |
| <span data-ttu-id="cbf24-1305">PRNE 0x00000005</span><span class="sxs-lookup"><span data-stu-id="cbf24-1305">PRNE 0x00000005</span></span>       | <span data-ttu-id="cbf24-1306">Comparación no igual.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1306">A not-equal comparison.</span></span>                                                                                           |
| <span data-ttu-id="cbf24-1307">PRRE 0x00000006</span><span class="sxs-lookup"><span data-stu-id="cbf24-1307">PRRE 0x00000006</span></span>       | <span data-ttu-id="cbf24-1308">Comparación de expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1308">A regular expression comparison.</span></span>                                                                                  |
| <span data-ttu-id="cbf24-1309">PRAllBits 0x00000007</span><span class="sxs-lookup"><span data-stu-id="cbf24-1309">PRAllBits 0x00000007</span></span>  | <span data-ttu-id="cbf24-1310">AND bit a bit que devuelve el operando derecho.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1310">A bitwise AND that returns the right operand.</span></span>                                                                     |
| <span data-ttu-id="cbf24-1311">PRSomeBits 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cbf24-1311">PRSomeBits 0x00000008</span></span> | <span data-ttu-id="cbf24-1312">AND bit a bit que devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1312">A bitwise AND that returns a nonzero value.</span></span>                                                                       |
| <span data-ttu-id="cbf24-1313">PRAll 0x00000100</span><span class="sxs-lookup"><span data-stu-id="cbf24-1313">PRAll 0x00000100</span></span>      | <span data-ttu-id="cbf24-1314">La operación se va a realizar en una columna de un conjunto de filas y solo es true si la operación es verdadera para todas las filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1314">The operation is to be performed on a column of a rowset, and is only true if the operation is true for all rows.</span></span> |
| <span data-ttu-id="cbf24-1315">PRAny 0x00000200</span><span class="sxs-lookup"><span data-stu-id="cbf24-1315">PRAny 0x00000200</span></span>      | <span data-ttu-id="cbf24-1316">La operación se va a realizar en una columna de un conjunto de filas y es true si la operación es verdadera para cualquier fila.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1316">The operation is to be performed on a column of a rowset, and is true if the operation is true for any row.</span></span>       |



 

<span data-ttu-id="cbf24-1317">**\_ Propiedad**: estructura CFullPropSpec, tal como se especifica en la sección 2.2.1.2, que indica la propiedad en la que se va a realizar una operación de coincidencia.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1317">**\_Property**: A CFullPropSpec structure, as specified in Section 2.2.1.2, indicating the property on which to perform a match operation.</span></span>

<span data-ttu-id="cbf24-1318">**\_ prval:** una estructura CBaseStorageVariant, como se especifica en la sección 2.2.1.1, que contiene el valor que se relaciona con la propiedad .</span><span class="sxs-lookup"><span data-stu-id="cbf24-1318">**\_prval**: A CBaseStorageVariant structure, as specified in Section 2.2.1.1, containing the value to relate to the property.</span></span>

### <a name="22110-crangerestriction"></a><span data-ttu-id="cbf24-1319">2.2.1.10 CRangeRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-1319">2.2.1.10 CRangeRestriction</span></span>

<span data-ttu-id="cbf24-1320">La estructura CRangeRestriction contiene una restricción en un intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1320">The CRangeRestriction structure contains a restriction on a range of values.</span></span>



<span data-ttu-id="cbf24-1321">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1321">0</span></span>

<span data-ttu-id="cbf24-1322">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1322">1</span></span>

<span data-ttu-id="cbf24-1323">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1323">2</span></span>

<span data-ttu-id="cbf24-1324">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1324">3</span></span>

<span data-ttu-id="cbf24-1325">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1325">4</span></span>

<span data-ttu-id="cbf24-1326">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1326">5</span></span>

<span data-ttu-id="cbf24-1327">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1327">6</span></span>

<span data-ttu-id="cbf24-1328">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1328">7</span></span>

<span data-ttu-id="cbf24-1329">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1329">8</span></span>

<span data-ttu-id="cbf24-1330">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1330">9</span></span>

<span data-ttu-id="cbf24-1331">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1331">1</span></span><br/> <span data-ttu-id="cbf24-1332">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1332">0</span></span><br/>

<span data-ttu-id="cbf24-1333">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1333">1</span></span>

<span data-ttu-id="cbf24-1334">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1334">2</span></span>

<span data-ttu-id="cbf24-1335">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1335">3</span></span>

<span data-ttu-id="cbf24-1336">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1336">4</span></span>

<span data-ttu-id="cbf24-1337">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1337">5</span></span>

<span data-ttu-id="cbf24-1338">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1338">6</span></span>

<span data-ttu-id="cbf24-1339">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1339">7</span></span>

<span data-ttu-id="cbf24-1340">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1340">8</span></span>

<span data-ttu-id="cbf24-1341">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1341">9</span></span>

<span data-ttu-id="cbf24-1342">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1342">2</span></span><br/> <span data-ttu-id="cbf24-1343">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1343">0</span></span><br/>

<span data-ttu-id="cbf24-1344">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1344">1</span></span>

<span data-ttu-id="cbf24-1345">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1345">2</span></span>

<span data-ttu-id="cbf24-1346">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1346">3</span></span>

<span data-ttu-id="cbf24-1347">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1347">4</span></span>

<span data-ttu-id="cbf24-1348">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1348">5</span></span>

<span data-ttu-id="cbf24-1349">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1349">6</span></span>

<span data-ttu-id="cbf24-1350">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1350">7</span></span>

<span data-ttu-id="cbf24-1351">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1351">8</span></span>

<span data-ttu-id="cbf24-1352">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1352">9</span></span>

<span data-ttu-id="cbf24-1353">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1353">3</span></span><br/> <span data-ttu-id="cbf24-1354">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1354">0</span></span><br/>

<span data-ttu-id="cbf24-1355">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1355">1</span></span>

<span data-ttu-id="cbf24-1356">\_keyStart (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1356">\_keyStart (variable)</span></span>

<span data-ttu-id="cbf24-1357">\_keyEnd (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1357">\_keyEnd (variable)</span></span>



 

<span data-ttu-id="cbf24-1358">**\_ keyStart:** estructura CKey, como se especifica en la sección 2.2.1.4, que contiene el principio del intervalo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1358">**\_keyStart**: A CKey structure, as specified in section 2.2.1.4, containing the beginning of the range.</span></span>

<span data-ttu-id="cbf24-1359">**\_ keyEnd:** estructura CKey que contiene el final del intervalo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1359">**\_keyEnd**: A CKey structure containing the end of the range.</span></span>

### <a name="22111-cscoperestriction"></a><span data-ttu-id="cbf24-1360">2.2.1.11 CScopeRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-1360">2.2.1.11 CScopeRestriction</span></span>

<span data-ttu-id="cbf24-1361">La estructura CScopeRestriction contiene una restricción en los archivos que se buscarán.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1361">The CScopeRestriction structure contains a restriction on the files to be searched</span></span>



<span data-ttu-id="cbf24-1362">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1362">0</span></span>

<span data-ttu-id="cbf24-1363">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1363">1</span></span>

<span data-ttu-id="cbf24-1364">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1364">2</span></span>

<span data-ttu-id="cbf24-1365">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1365">3</span></span>

<span data-ttu-id="cbf24-1366">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1366">4</span></span>

<span data-ttu-id="cbf24-1367">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1367">5</span></span>

<span data-ttu-id="cbf24-1368">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1368">6</span></span>

<span data-ttu-id="cbf24-1369">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1369">7</span></span>

<span data-ttu-id="cbf24-1370">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1370">8</span></span>

<span data-ttu-id="cbf24-1371">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1371">9</span></span>

<span data-ttu-id="cbf24-1372">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1372">1</span></span><br/> <span data-ttu-id="cbf24-1373">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1373">0</span></span><br/>

<span data-ttu-id="cbf24-1374">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1374">1</span></span>

<span data-ttu-id="cbf24-1375">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1375">2</span></span>

<span data-ttu-id="cbf24-1376">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1376">3</span></span>

<span data-ttu-id="cbf24-1377">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1377">4</span></span>

<span data-ttu-id="cbf24-1378">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1378">5</span></span>

<span data-ttu-id="cbf24-1379">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1379">6</span></span>

<span data-ttu-id="cbf24-1380">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1380">7</span></span>

<span data-ttu-id="cbf24-1381">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1381">8</span></span>

<span data-ttu-id="cbf24-1382">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1382">9</span></span>

<span data-ttu-id="cbf24-1383">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1383">2</span></span><br/> <span data-ttu-id="cbf24-1384">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1384">0</span></span><br/>

<span data-ttu-id="cbf24-1385">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1385">1</span></span>

<span data-ttu-id="cbf24-1386">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1386">2</span></span>

<span data-ttu-id="cbf24-1387">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1387">3</span></span>

<span data-ttu-id="cbf24-1388">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1388">4</span></span>

<span data-ttu-id="cbf24-1389">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1389">5</span></span>

<span data-ttu-id="cbf24-1390">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1390">6</span></span>

<span data-ttu-id="cbf24-1391">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1391">7</span></span>

<span data-ttu-id="cbf24-1392">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1392">8</span></span>

<span data-ttu-id="cbf24-1393">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1393">9</span></span>

<span data-ttu-id="cbf24-1394">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1394">3</span></span><br/> <span data-ttu-id="cbf24-1395">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1395">0</span></span><br/>

<span data-ttu-id="cbf24-1396">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1396">1</span></span>

<span data-ttu-id="cbf24-1397">CcLowerPath</span><span class="sxs-lookup"><span data-stu-id="cbf24-1397">CcLowerPath</span></span>

<span data-ttu-id="cbf24-1398">\_lowerPath (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1398">\_lowerPath (variable)</span></span>

<span data-ttu-id="cbf24-1399">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-1399">...</span></span>

<span data-ttu-id="cbf24-1400">\_padding (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1400">\_padding ( variable)</span></span>

<span data-ttu-id="cbf24-1401">\_Longitud</span><span class="sxs-lookup"><span data-stu-id="cbf24-1401">\_length</span></span>

<span data-ttu-id="cbf24-1402">\_fRecursive</span><span class="sxs-lookup"><span data-stu-id="cbf24-1402">\_fRecursive</span></span>

<span data-ttu-id="cbf24-1403">\_fVirtual</span><span class="sxs-lookup"><span data-stu-id="cbf24-1403">\_fVirtual</span></span>



 

<span data-ttu-id="cbf24-1404">**CcLowerPath:** entero de 32 bits sin signo que contiene el número de caracteres Unicode en el \_ campo lowerPath.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1404">**CcLowerPath**: A 32-bit unsigned integer containing the number of Unicode characters in the \_lowerPath field.</span></span>

<span data-ttu-id="cbf24-1405">**\_ lowerPath:** cadena Unicode no terminada en NULL que **representa** la ruta de acceso a la que se debe restringir la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1405">**\_lowerPath**: A non null-terminated Unicode string representing the **path** to which the query should be restricted.</span></span> <span data-ttu-id="cbf24-1406">El campo CcLowerPath contiene la longitud de la cadena.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1406">The CcLowerPath field contains the length of the string.</span></span>

<span data-ttu-id="cbf24-1407">**\_ padding:** este campo DEBE tener entre 0 y 3 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1407">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cbf24-1408">La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1408">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cbf24-1409">Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1409">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cbf24-1410">El receptor DEBE omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1410">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cbf24-1411">**\_ length:** entero de 32 bits sin signo que contiene la longitud de \_ lowerPath, en caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1411">**\_length**: A 32-bit unsigned integer containing the length of \_lowerPath, in Unicode characters.</span></span> <span data-ttu-id="cbf24-1412">DEBE ser el mismo valor que CcLowerPath.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1412">This MUST be the same value as CcLowerPath.</span></span>

<span data-ttu-id="cbf24-1413">**\_ fRecursive:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1413">**\_fRecursive**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cbf24-1414">DEBE establecerse en 0x00000001 o 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1414">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="cbf24-1415">Si se establece 0x00000001, el servidor examinará de forma recursiva todos los subdirectorios de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1415">If set to 0x00000001, the server is to recursively examine all subdirectories of the path.</span></span> <span data-ttu-id="cbf24-1416">Si se establece 0x00000000, el servidor no examinará ningún subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1416">If set to 0x00000000, the server is to not examine any subdirectories.</span></span>

<span data-ttu-id="cbf24-1417">**\_ fVirtual:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1417">**\_fVirtual**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cbf24-1418">DEBE establecerse en 0x00000001 o 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1418">MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="cbf24-1419">Si se establece en 0x00000001, lowerPath es una ruta de acceso virtual (el localizador uniforme de recursos (URL) asociado a un directorio físico en el sistema de \_ archivos) para un sitio web.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1419">If set to 0x00000001, \_lowerPath is a virtual path (the Uniform Resource Locator (URL) associated with a physical directory on the file system) for a web site.</span></span> <span data-ttu-id="cbf24-1420">Si se establece en 0x00000000, \_ lowerPath es una ruta de acceso del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1420">If set to 0x00000000, \_lowerPath is a file system path.</span></span>

### <a name="22112-csort"></a><span data-ttu-id="cbf24-1421">2.2.1.12 CSort</span><span class="sxs-lookup"><span data-stu-id="cbf24-1421">2.2.1.12 CSort</span></span>

<span data-ttu-id="cbf24-1422">La estructura CSort identifica una columna para ordenar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1422">The CSort structure identifies a column to sort.</span></span>



<span data-ttu-id="cbf24-1423">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1423">0</span></span>

<span data-ttu-id="cbf24-1424">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1424">1</span></span>

<span data-ttu-id="cbf24-1425">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1425">2</span></span>

<span data-ttu-id="cbf24-1426">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1426">3</span></span>

<span data-ttu-id="cbf24-1427">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1427">4</span></span>

<span data-ttu-id="cbf24-1428">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1428">5</span></span>

<span data-ttu-id="cbf24-1429">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1429">6</span></span>

<span data-ttu-id="cbf24-1430">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1430">7</span></span>

<span data-ttu-id="cbf24-1431">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1431">8</span></span>

<span data-ttu-id="cbf24-1432">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1432">9</span></span>

<span data-ttu-id="cbf24-1433">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1433">1</span></span><br/> <span data-ttu-id="cbf24-1434">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1434">0</span></span><br/>

<span data-ttu-id="cbf24-1435">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1435">1</span></span>

<span data-ttu-id="cbf24-1436">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1436">2</span></span>

<span data-ttu-id="cbf24-1437">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1437">3</span></span>

<span data-ttu-id="cbf24-1438">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1438">4</span></span>

<span data-ttu-id="cbf24-1439">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1439">5</span></span>

<span data-ttu-id="cbf24-1440">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1440">6</span></span>

<span data-ttu-id="cbf24-1441">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1441">7</span></span>

<span data-ttu-id="cbf24-1442">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1442">8</span></span>

<span data-ttu-id="cbf24-1443">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1443">9</span></span>

<span data-ttu-id="cbf24-1444">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1444">2</span></span><br/> <span data-ttu-id="cbf24-1445">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1445">0</span></span><br/>

<span data-ttu-id="cbf24-1446">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1446">1</span></span>

<span data-ttu-id="cbf24-1447">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1447">2</span></span>

<span data-ttu-id="cbf24-1448">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1448">3</span></span>

<span data-ttu-id="cbf24-1449">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1449">4</span></span>

<span data-ttu-id="cbf24-1450">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1450">5</span></span>

<span data-ttu-id="cbf24-1451">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1451">6</span></span>

<span data-ttu-id="cbf24-1452">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1452">7</span></span>

<span data-ttu-id="cbf24-1453">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1453">8</span></span>

<span data-ttu-id="cbf24-1454">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1454">9</span></span>

<span data-ttu-id="cbf24-1455">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1455">3</span></span><br/> <span data-ttu-id="cbf24-1456">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1456">0</span></span><br/>

<span data-ttu-id="cbf24-1457">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1457">1</span></span>

<span data-ttu-id="cbf24-1458">pidColumn</span><span class="sxs-lookup"><span data-stu-id="cbf24-1458">pidColumn</span></span>

<span data-ttu-id="cbf24-1459">dwOrder</span><span class="sxs-lookup"><span data-stu-id="cbf24-1459">dwOrder</span></span>

<span data-ttu-id="cbf24-1460">locale</span><span class="sxs-lookup"><span data-stu-id="cbf24-1460">locale</span></span>



 

<span data-ttu-id="cbf24-1461">**pidColumn:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1461">**pidColumn**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cbf24-1462">Número de la columna por la que se ordenará.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1462">The number of the column to sort by.</span></span>

<span data-ttu-id="cbf24-1463">**dwOrder:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1463">**dwOrder**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cbf24-1464">DEBE ser uno de los siguientes valores, especificando cómo ordenar en función de la columna.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1464">MUST be one of the following values, specifying how to sort based on the column.</span></span>



| <span data-ttu-id="cbf24-1465">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-1465">Value</span></span>                        | <span data-ttu-id="cbf24-1466">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-1466">Meaning</span></span>                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-1467">Query \_ SORTASCEND 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-1467">QUERY\_SORTASCEND 0x00000000</span></span> | <span data-ttu-id="cbf24-1468">Las filas deben ordenarse en orden ascendente en función de los valores de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1468">The rows are to be sorted in ascending order based on the values in the column specified.</span></span>  |
| <span data-ttu-id="cbf24-1469">Query \_ DESCEND 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-1469">QUERY\_DESCEND 0x00000001</span></span>    | <span data-ttu-id="cbf24-1470">Las filas deben ordenarse en orden descendente en función de los valores de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1470">The rows are to be sorted in descending order based on the values in the column specified.</span></span> |



 

<span data-ttu-id="cbf24-1471">**configuración regional:** entero de 32 bits sin signo que indica la configuración regional, como se especifica en el Apéndice A de \[ MS-GPSI, \] de la columna.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1471">**locale**: A 32-bit unsigned integer indicating the locale, as specified in \[MS-GPSI\] Appendix A, of the column.</span></span>

### <a name="22113-csynrestriction"></a><span data-ttu-id="cbf24-1472">2.2.1.13 CSynRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-1472">2.2.1.13 CSynRestriction</span></span>

<span data-ttu-id="cbf24-1473">La estructura CSynRestriction contiene una palabra o sus sinónimos para una frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1473">The CSynRestriction structure contains a word or its synonyms for a query phrase.</span></span>



<span data-ttu-id="cbf24-1474">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1474">0</span></span>

<span data-ttu-id="cbf24-1475">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1475">1</span></span>

<span data-ttu-id="cbf24-1476">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1476">2</span></span>

<span data-ttu-id="cbf24-1477">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1477">3</span></span>

<span data-ttu-id="cbf24-1478">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1478">4</span></span>

<span data-ttu-id="cbf24-1479">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1479">5</span></span>

<span data-ttu-id="cbf24-1480">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1480">6</span></span>

<span data-ttu-id="cbf24-1481">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1481">7</span></span>

<span data-ttu-id="cbf24-1482">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1482">8</span></span>

<span data-ttu-id="cbf24-1483">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1483">9</span></span>

<span data-ttu-id="cbf24-1484">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1484">1</span></span><br/> <span data-ttu-id="cbf24-1485">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1485">0</span></span><br/>

<span data-ttu-id="cbf24-1486">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1486">1</span></span>

<span data-ttu-id="cbf24-1487">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1487">2</span></span>

<span data-ttu-id="cbf24-1488">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1488">3</span></span>

<span data-ttu-id="cbf24-1489">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1489">4</span></span>

<span data-ttu-id="cbf24-1490">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1490">5</span></span>

<span data-ttu-id="cbf24-1491">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1491">6</span></span>

<span data-ttu-id="cbf24-1492">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1492">7</span></span>

<span data-ttu-id="cbf24-1493">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1493">8</span></span>

<span data-ttu-id="cbf24-1494">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1494">9</span></span>

<span data-ttu-id="cbf24-1495">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1495">2</span></span><br/> <span data-ttu-id="cbf24-1496">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1496">0</span></span><br/>

<span data-ttu-id="cbf24-1497">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1497">1</span></span>

<span data-ttu-id="cbf24-1498">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1498">2</span></span>

<span data-ttu-id="cbf24-1499">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1499">3</span></span>

<span data-ttu-id="cbf24-1500">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1500">4</span></span>

<span data-ttu-id="cbf24-1501">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1501">5</span></span>

<span data-ttu-id="cbf24-1502">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1502">6</span></span>

<span data-ttu-id="cbf24-1503">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1503">7</span></span>

<span data-ttu-id="cbf24-1504">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1504">8</span></span>

<span data-ttu-id="cbf24-1505">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1505">9</span></span>

<span data-ttu-id="cbf24-1506">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1506">3</span></span><br/> <span data-ttu-id="cbf24-1507">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1507">0</span></span><br/>

<span data-ttu-id="cbf24-1508">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1508">1</span></span>

<span data-ttu-id="cbf24-1509">Restricción</span><span class="sxs-lookup"><span data-stu-id="cbf24-1509">Restriction</span></span>

<span data-ttu-id="cbf24-1510">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-1510">...</span></span>

<span data-ttu-id="cbf24-1511">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-1511">...</span></span>

<span data-ttu-id="cbf24-1512">cKey</span><span class="sxs-lookup"><span data-stu-id="cbf24-1512">cKey</span></span>

<span data-ttu-id="cbf24-1513">\_keyArray (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1513">\_keyArray (variable)</span></span>

<span data-ttu-id="cbf24-1514">\_isRange</span><span class="sxs-lookup"><span data-stu-id="cbf24-1514">\_isRange</span></span>



 

<span data-ttu-id="cbf24-1515">**Restricción:** estructura COccRestriction que especifica la ubicación de la palabra.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1515">**Restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="cbf24-1516">**cKey:** entero de 32 bits sin signo que especifica el número de elementos de la \_ matriz keyArray.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1516">**cKey**: A 32-bit unsigned integer specifying the number of elements in the \_keyArray array.</span></span>

<span data-ttu-id="cbf24-1517">**\_ keyArray:** matriz de estructuras CKey que especifican una palabra y sus sinónimos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1517">**\_keyArray**: An array of CKey structures specifying a word and its synonyms.</span></span>

<span data-ttu-id="cbf24-1518">**\_ isRange:** si se establece en 0x01, las claves son prefijos para coincidir.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1518">**\_isRange**: If set to 0x01, the keys are prefixes to match.</span></span> <span data-ttu-id="cbf24-1519">Si se establece en 0x00, las claves son valores exactos que se van a coincidir.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1519">If set to 0x00, the keys are exact values to match.</span></span> <span data-ttu-id="cbf24-1520">\_isRange NO DEBE establecerse en ningún otro valor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1520">\_isRange MUST NOT be set to any other values.</span></span>

### <a name="22114-cvectorrestriction"></a><span data-ttu-id="cbf24-1521">2.2.1.14 CVectorRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-1521">2.2.1.14 CVectorRestriction</span></span>

<span data-ttu-id="cbf24-1522">La estructura CVectorRestriction contiene una operación OR ponderada en un nodo de árbol de comandos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1522">The CVectorRestriction structure contains a weighted OR operation on a command tree node.</span></span>



<span data-ttu-id="cbf24-1523">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1523">0</span></span>

<span data-ttu-id="cbf24-1524">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1524">1</span></span>

<span data-ttu-id="cbf24-1525">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1525">2</span></span>

<span data-ttu-id="cbf24-1526">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1526">3</span></span>

<span data-ttu-id="cbf24-1527">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1527">4</span></span>

<span data-ttu-id="cbf24-1528">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1528">5</span></span>

<span data-ttu-id="cbf24-1529">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1529">6</span></span>

<span data-ttu-id="cbf24-1530">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1530">7</span></span>

<span data-ttu-id="cbf24-1531">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1531">8</span></span>

<span data-ttu-id="cbf24-1532">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1532">9</span></span>

<span data-ttu-id="cbf24-1533">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1533">1</span></span><br/> <span data-ttu-id="cbf24-1534">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1534">0</span></span><br/>

<span data-ttu-id="cbf24-1535">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1535">1</span></span>

<span data-ttu-id="cbf24-1536">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1536">2</span></span>

<span data-ttu-id="cbf24-1537">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1537">3</span></span>

<span data-ttu-id="cbf24-1538">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1538">4</span></span>

<span data-ttu-id="cbf24-1539">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1539">5</span></span>

<span data-ttu-id="cbf24-1540">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1540">6</span></span>

<span data-ttu-id="cbf24-1541">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1541">7</span></span>

<span data-ttu-id="cbf24-1542">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1542">8</span></span>

<span data-ttu-id="cbf24-1543">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1543">9</span></span>

<span data-ttu-id="cbf24-1544">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1544">2</span></span><br/> <span data-ttu-id="cbf24-1545">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1545">0</span></span><br/>

<span data-ttu-id="cbf24-1546">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1546">1</span></span>

<span data-ttu-id="cbf24-1547">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1547">2</span></span>

<span data-ttu-id="cbf24-1548">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1548">3</span></span>

<span data-ttu-id="cbf24-1549">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1549">4</span></span>

<span data-ttu-id="cbf24-1550">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1550">5</span></span>

<span data-ttu-id="cbf24-1551">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1551">6</span></span>

<span data-ttu-id="cbf24-1552">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1552">7</span></span>

<span data-ttu-id="cbf24-1553">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1553">8</span></span>

<span data-ttu-id="cbf24-1554">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1554">9</span></span>

<span data-ttu-id="cbf24-1555">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1555">3</span></span><br/> <span data-ttu-id="cbf24-1556">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1556">0</span></span><br/>

<span data-ttu-id="cbf24-1557">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1557">1</span></span>

<span data-ttu-id="cbf24-1558">\_pres (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1558">\_pres (variable)</span></span>

<span data-ttu-id="cbf24-1559">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-1559">...</span></span>

<span data-ttu-id="cbf24-1560">\_padding (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1560">\_padding (variable)</span></span>

<span data-ttu-id="cbf24-1561">\_ulRankMethod</span><span class="sxs-lookup"><span data-stu-id="cbf24-1561">\_ulRankMethod</span></span>



 

<span data-ttu-id="cbf24-1562">**\_ pres:** árbol de comandos CNodeRestriction en el que se va a realizar una operación OR clasificada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1562">**\_pres**: A CNodeRestriction command tree upon which a ranked OR operation is to be performed.</span></span>

<span data-ttu-id="cbf24-1563">**\_ padding:** este campo DEBE tener una longitud de 0 a 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1563">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cbf24-1564">La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1564">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cbf24-1565">Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1565">If this field is present (i.e. length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cbf24-1566">El receptor DEBE omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1566">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cbf24-1567">**\_ ulRankMethod:** entero de 32 bits sin signo que especifica un algoritmo de clasificación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1567">**\_ulRankMethod**: A 32-bit unsigned integer specifying a ranking algorithm.</span></span> <span data-ttu-id="cbf24-1568">DEBE establecerse en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1568">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="cbf24-1569">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-1569">Value</span></span>                            | <span data-ttu-id="cbf24-1570">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-1570">Meaning</span></span>                                       |
|----------------------------------|-----------------------------------------------|
| <span data-ttu-id="cbf24-1571">VECTOR \_ RANK \_ MIN 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-1571">VECTOR\_RANK\_MIN 0x00000000</span></span>     | <span data-ttu-id="cbf24-1572">Use el algoritmo \[ mínimo SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="cbf24-1572">Use minimum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="cbf24-1573">VECTOR \_ RANK \_ MAX 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-1573">VECTOR\_RANK\_MAX 0x00000001</span></span>     | <span data-ttu-id="cbf24-1574">Use el algoritmo \[ máximo SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="cbf24-1574">Use maximum algorithm \[SALTON\].</span></span>             |
| <span data-ttu-id="cbf24-1575">VECTOR \_ RANK \_ INNER 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbf24-1575">VECTOR\_RANK\_INNER 0x00000002</span></span>   | <span data-ttu-id="cbf24-1576">Use el algoritmo de producto \[ interno SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="cbf24-1576">Use inner product algorithm \[SALTON\].</span></span>       |
| <span data-ttu-id="cbf24-1577">Vector \_ RANK \_ DICE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cbf24-1577">VECTOR\_RANK\_DICE 0x00000003</span></span>    | <span data-ttu-id="cbf24-1578">Use el algoritmo de coeficiente de \[ dados SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="cbf24-1578">Use Dice coefficient algorithm \[SALTON\].</span></span>    |
| <span data-ttu-id="cbf24-1579">Vector \_ RANK \_ 0X00000004</span><span class="sxs-lookup"><span data-stu-id="cbf24-1579">VECTOR\_RANK\_JACCARD 0x00000004</span></span> | <span data-ttu-id="cbf24-1580">Use el algoritmo de coeficiente de Rsacard \[ SALTON \] .</span><span class="sxs-lookup"><span data-stu-id="cbf24-1580">Use Jaccard coefficient algorithm \[SALTON\].</span></span> |



 

### <a name="22115-cwordrestriction"></a><span data-ttu-id="cbf24-1581">2.2.1.15 CWordRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-1581">2.2.1.15 CWordRestriction</span></span>

<span data-ttu-id="cbf24-1582">La estructura CWordRestriction contiene una palabra para una frase de consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1582">The CWordRestriction structure contains a word for a query phrase.</span></span>



<span data-ttu-id="cbf24-1583">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1583">0</span></span>

<span data-ttu-id="cbf24-1584">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1584">1</span></span>

<span data-ttu-id="cbf24-1585">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1585">2</span></span>

<span data-ttu-id="cbf24-1586">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1586">3</span></span>

<span data-ttu-id="cbf24-1587">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1587">4</span></span>

<span data-ttu-id="cbf24-1588">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1588">5</span></span>

<span data-ttu-id="cbf24-1589">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1589">6</span></span>

<span data-ttu-id="cbf24-1590">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1590">7</span></span>

<span data-ttu-id="cbf24-1591">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1591">8</span></span>

<span data-ttu-id="cbf24-1592">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1592">9</span></span>

<span data-ttu-id="cbf24-1593">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1593">1</span></span><br/> <span data-ttu-id="cbf24-1594">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1594">0</span></span><br/>

<span data-ttu-id="cbf24-1595">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1595">1</span></span>

<span data-ttu-id="cbf24-1596">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1596">2</span></span>

<span data-ttu-id="cbf24-1597">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1597">3</span></span>

<span data-ttu-id="cbf24-1598">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1598">4</span></span>

<span data-ttu-id="cbf24-1599">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1599">5</span></span>

<span data-ttu-id="cbf24-1600">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1600">6</span></span>

<span data-ttu-id="cbf24-1601">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1601">7</span></span>

<span data-ttu-id="cbf24-1602">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1602">8</span></span>

<span data-ttu-id="cbf24-1603">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1603">9</span></span>

<span data-ttu-id="cbf24-1604">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1604">2</span></span><br/> <span data-ttu-id="cbf24-1605">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1605">0</span></span><br/>

<span data-ttu-id="cbf24-1606">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1606">1</span></span>

<span data-ttu-id="cbf24-1607">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1607">2</span></span>

<span data-ttu-id="cbf24-1608">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1608">3</span></span>

<span data-ttu-id="cbf24-1609">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1609">4</span></span>

<span data-ttu-id="cbf24-1610">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1610">5</span></span>

<span data-ttu-id="cbf24-1611">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1611">6</span></span>

<span data-ttu-id="cbf24-1612">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1612">7</span></span>

<span data-ttu-id="cbf24-1613">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1613">8</span></span>

<span data-ttu-id="cbf24-1614">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1614">9</span></span>

<span data-ttu-id="cbf24-1615">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1615">3</span></span><br/> <span data-ttu-id="cbf24-1616">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1616">0</span></span><br/>

<span data-ttu-id="cbf24-1617">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1617">1</span></span>

<span data-ttu-id="cbf24-1618">restricción</span><span class="sxs-lookup"><span data-stu-id="cbf24-1618">restriction</span></span>

<span data-ttu-id="cbf24-1619">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-1619">...</span></span>

<span data-ttu-id="cbf24-1620">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-1620">...</span></span>

<span data-ttu-id="cbf24-1621">\_key (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1621">\_key (variable)</span></span>

<span data-ttu-id="cbf24-1622">\_isRange</span><span class="sxs-lookup"><span data-stu-id="cbf24-1622">\_isRange</span></span>



 

<span data-ttu-id="cbf24-1623">**restriction:** estructura COccRestriction que especifica la ubicación de la palabra.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1623">**restriction**: A COccRestriction structure specifying the location of the word.</span></span>

<span data-ttu-id="cbf24-1624">**\_ key:** estructura CKey que especifica una palabra.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1624">**\_key**: A CKey structure specifying a word.</span></span>

<span data-ttu-id="cbf24-1625">**\_ isRange:** si se establece en 0x01, la clave es un prefijo que debe coincidir.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1625">**\_isRange**: If set to 0x01, the key is a prefix to match.</span></span> <span data-ttu-id="cbf24-1626">Si se establece en 0x00, la clave es un valor exacto que debe coincidir.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1626">If set to 0x00, the key is an exact value to match.</span></span> <span data-ttu-id="cbf24-1627">\_isRange NO DEBE establecerse en ningún otro valor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1627">\_isRange MUST NOT be set to any other value.</span></span>

### <a name="22116-crestriction"></a><span data-ttu-id="cbf24-1628">2.2.1.16 CRestriction</span><span class="sxs-lookup"><span data-stu-id="cbf24-1628">2.2.1.16 CRestriction</span></span>

<span data-ttu-id="cbf24-1629">La estructura CRestriction contiene un nodo de un árbol de comandos de consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1629">The CRestriction structure contains a node of a query command tree.</span></span>



<span data-ttu-id="cbf24-1630">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1630">0</span></span>

<span data-ttu-id="cbf24-1631">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1631">1</span></span>

<span data-ttu-id="cbf24-1632">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1632">2</span></span>

<span data-ttu-id="cbf24-1633">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1633">3</span></span>

<span data-ttu-id="cbf24-1634">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1634">4</span></span>

<span data-ttu-id="cbf24-1635">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1635">5</span></span>

<span data-ttu-id="cbf24-1636">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1636">6</span></span>

<span data-ttu-id="cbf24-1637">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1637">7</span></span>

<span data-ttu-id="cbf24-1638">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1638">8</span></span>

<span data-ttu-id="cbf24-1639">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1639">9</span></span>

<span data-ttu-id="cbf24-1640">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1640">1</span></span><br/> <span data-ttu-id="cbf24-1641">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1641">0</span></span><br/>

<span data-ttu-id="cbf24-1642">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1642">1</span></span>

<span data-ttu-id="cbf24-1643">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1643">2</span></span>

<span data-ttu-id="cbf24-1644">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1644">3</span></span>

<span data-ttu-id="cbf24-1645">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1645">4</span></span>

<span data-ttu-id="cbf24-1646">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1646">5</span></span>

<span data-ttu-id="cbf24-1647">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1647">6</span></span>

<span data-ttu-id="cbf24-1648">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1648">7</span></span>

<span data-ttu-id="cbf24-1649">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1649">8</span></span>

<span data-ttu-id="cbf24-1650">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1650">9</span></span>

<span data-ttu-id="cbf24-1651">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1651">2</span></span><br/> <span data-ttu-id="cbf24-1652">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1652">0</span></span><br/>

<span data-ttu-id="cbf24-1653">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1653">1</span></span>

<span data-ttu-id="cbf24-1654">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1654">2</span></span>

<span data-ttu-id="cbf24-1655">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1655">3</span></span>

<span data-ttu-id="cbf24-1656">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1656">4</span></span>

<span data-ttu-id="cbf24-1657">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1657">5</span></span>

<span data-ttu-id="cbf24-1658">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1658">6</span></span>

<span data-ttu-id="cbf24-1659">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1659">7</span></span>

<span data-ttu-id="cbf24-1660">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1660">8</span></span>

<span data-ttu-id="cbf24-1661">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1661">9</span></span>

<span data-ttu-id="cbf24-1662">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1662">3</span></span><br/> <span data-ttu-id="cbf24-1663">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1663">0</span></span><br/>

<span data-ttu-id="cbf24-1664">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1664">1</span></span>

<span data-ttu-id="cbf24-1665">\_ulType</span><span class="sxs-lookup"><span data-stu-id="cbf24-1665">\_ulType</span></span>

<span data-ttu-id="cbf24-1666">Peso</span><span class="sxs-lookup"><span data-stu-id="cbf24-1666">Weight</span></span>

<span data-ttu-id="cbf24-1667">Restricción</span><span class="sxs-lookup"><span data-stu-id="cbf24-1667">Restriction</span></span>



 

<span data-ttu-id="cbf24-1668">**\_ ulType:** entero de 32 bits sin signo que indica el tipo de restricción utilizado para el nodo de árbol de comandos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1668">**\_ulType**: A 32-bit unsigned integer indicating the restriction type used for the command tree node.</span></span> <span data-ttu-id="cbf24-1669">DEBE establecerse en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1669">MUST be set to one of the following values.</span></span>



| <span data-ttu-id="cbf24-1670">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-1670">Value</span></span>                    | <span data-ttu-id="cbf24-1671">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-1671">Meaning</span></span>                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-1672">RTNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-1672">RTNone 0x00000000</span></span>        | <span data-ttu-id="cbf24-1673">El nodo representa una palabra ruidosa en una consulta vectorial.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1673">The node represents a noise word in a vector query.</span></span>                                         |
| <span data-ttu-id="cbf24-1674">RTAnd 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-1674">RTAnd 0x00000001</span></span>         | <span data-ttu-id="cbf24-1675">El nodo contiene una CNodeRestriction en la que se va a realizar una operación AND lógica.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1675">The node contains a CNodeRestriction upon which a logical AND operation it to be performed.</span></span> |
| <span data-ttu-id="cbf24-1676">RTOr 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbf24-1676">RTOr 0x00000002</span></span>          | <span data-ttu-id="cbf24-1677">El nodo contiene una CNodeRestriction en la que se va a realizar una operación OR lógica.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1677">The node contains a CNodeRestriction upon which a logical OR operation is to be performed.</span></span>  |
| <span data-ttu-id="cbf24-1678">RTNot 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cbf24-1678">RTNot 0x00000003</span></span>         | <span data-ttu-id="cbf24-1679">El nodo contiene una CRestriction en la que se va a realizar una operación NOT.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1679">The node contains a CRestriction upon which a NOT operation is to be performed.</span></span>             |
| <span data-ttu-id="cbf24-1680">RTContent 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cbf24-1680">RTContent 0x00000004</span></span>     | <span data-ttu-id="cbf24-1681">El nodo contiene un CContentRestriction.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1681">The node contains a CContentRestriction.</span></span>                                                    |
| <span data-ttu-id="cbf24-1682">RtProperty 0x00000005</span><span class="sxs-lookup"><span data-stu-id="cbf24-1682">RTProperty 0x00000005</span></span>    | <span data-ttu-id="cbf24-1683">El nodo contiene una CPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1683">The node contains a CPropertyRestriction.</span></span>                                                   |
| <span data-ttu-id="cbf24-1684">RtProximity 0x00000006</span><span class="sxs-lookup"><span data-stu-id="cbf24-1684">RTProximity 0x00000006</span></span>   | <span data-ttu-id="cbf24-1685">El nodo contiene una CNodeRestriction en la que se va a realizar una clasificación de proximidad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1685">The node contains a CNodeRestriction upon which a proximity ranking is to be performed,</span></span>     |
| <span data-ttu-id="cbf24-1686">RTVector 0x00000007</span><span class="sxs-lookup"><span data-stu-id="cbf24-1686">RTVector 0x00000007</span></span>      | <span data-ttu-id="cbf24-1687">El nodo contiene un CVectorRestriction.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1687">The node contains a CVectorRestriction.</span></span>                                                     |
| <span data-ttu-id="cbf24-1688">RTNatLanguage 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cbf24-1688">RTNatLanguage 0x00000008</span></span> | <span data-ttu-id="cbf24-1689">El nodo contiene un CNatLanguageRestriction.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1689">The node contains a CNatLanguageRestriction.</span></span>                                                |
| <span data-ttu-id="cbf24-1690">RtScope 0x00000009</span><span class="sxs-lookup"><span data-stu-id="cbf24-1690">RTScope 0x00000009</span></span>       | <span data-ttu-id="cbf24-1691">El nodo contiene una CScopeRestriction.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1691">The node contains a CScopeRestriction.</span></span>                                                      |
| <span data-ttu-id="cbf24-1692">PRAny 0xFFFFFFFA</span><span class="sxs-lookup"><span data-stu-id="cbf24-1692">PRAny 0xFFFFFFFA</span></span>         | <span data-ttu-id="cbf24-1693">El nodo contiene una CInternalPropertyRestriction.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1693">The node contains a CInternalPropertyRestriction.</span></span>                                           |
| <span data-ttu-id="cbf24-1694">RtRange 0xFFFFFFFC</span><span class="sxs-lookup"><span data-stu-id="cbf24-1694">RTRange 0xFFFFFFFC</span></span>       | <span data-ttu-id="cbf24-1695">El nodo contiene una CRangeRestriction.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1695">The node contains a CRangeRestriction.</span></span>                                                      |
| <span data-ttu-id="cbf24-1696">RTPhrase 0xFFFFFFFD</span><span class="sxs-lookup"><span data-stu-id="cbf24-1696">RTPhrase 0xFFFFFFFD</span></span>      | <span data-ttu-id="cbf24-1697">El nodo contiene una CNodeRestriction en la que se va a realizar una coincidencia de frases.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1697">The node contains a CNodeRestriction upon which a phrase match is to be performed.</span></span>          |
| <span data-ttu-id="cbf24-1698">RTSynonym 0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="cbf24-1698">RTSynonym 0xFFFFFFFE</span></span>     | <span data-ttu-id="cbf24-1699">El nodo contiene una CSynRestriction.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1699">The node contains a CSynRestriction.</span></span>                                                        |
| <span data-ttu-id="cbf24-1700">RtWord 0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="cbf24-1700">RTWord 0xFFFFFFFF</span></span>        | <span data-ttu-id="cbf24-1701">El nodo contiene una CWordRestriction.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1701">The node contains a CWordRestriction.</span></span>                                                       |



 

<span data-ttu-id="cbf24-1702">**Peso:** entero de 32 bits sin signo que representa el peso del nodo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1702">**Weight**: A 32-bit unsigned integer representing the weight of the node.</span></span> <span data-ttu-id="cbf24-1703">Peso indica la importancia del nodo con respecto a otros nodos del árbol de comandos de consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1703">Weight indicates the node's importance relative to other nodes in the query command tree.</span></span> <span data-ttu-id="cbf24-1704">Los valores de peso más altos son más importantes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1704">Higher weight values are more important.</span></span>

<span data-ttu-id="cbf24-1705">**Restricción:** tipo de restricción para el nodo de árbol de comandos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1705">**Restriction**: The restriction type for the command tree node.</span></span> <span data-ttu-id="cbf24-1706">La sintaxis DEBE ser tal como se indica en el \_ campo ulType.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1706">The syntax MUST be as indicated by the \_ulType field.</span></span>

### <a name="22117-ccolumnset"></a><span data-ttu-id="cbf24-1707">2.2.1.17 CColumnSet</span><span class="sxs-lookup"><span data-stu-id="cbf24-1707">2.2.1.17 CColumnSet</span></span>

<span data-ttu-id="cbf24-1708">La estructura CColumnSet especifica los números de columna que se devolverán.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1708">The CColumnSet structure specifies the column numbers to be returned.</span></span> <span data-ttu-id="cbf24-1709">Esta estructura siempre se usa en referencia a una estructura CPidMapper específica (sección 2.2.1.23).</span><span class="sxs-lookup"><span data-stu-id="cbf24-1709">This structure is always used in reference to a specific CPidMapper structure (section 2.2.1.23).</span></span>



<span data-ttu-id="cbf24-1710">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1710">0</span></span>

<span data-ttu-id="cbf24-1711">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1711">1</span></span>

<span data-ttu-id="cbf24-1712">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1712">2</span></span>

<span data-ttu-id="cbf24-1713">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1713">3</span></span>

<span data-ttu-id="cbf24-1714">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1714">4</span></span>

<span data-ttu-id="cbf24-1715">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1715">5</span></span>

<span data-ttu-id="cbf24-1716">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1716">6</span></span>

<span data-ttu-id="cbf24-1717">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1717">7</span></span>

<span data-ttu-id="cbf24-1718">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1718">8</span></span>

<span data-ttu-id="cbf24-1719">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1719">9</span></span>

<span data-ttu-id="cbf24-1720">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1720">1</span></span><br/> <span data-ttu-id="cbf24-1721">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1721">0</span></span><br/>

<span data-ttu-id="cbf24-1722">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1722">1</span></span>

<span data-ttu-id="cbf24-1723">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1723">2</span></span>

<span data-ttu-id="cbf24-1724">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1724">3</span></span>

<span data-ttu-id="cbf24-1725">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1725">4</span></span>

<span data-ttu-id="cbf24-1726">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1726">5</span></span>

<span data-ttu-id="cbf24-1727">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1727">6</span></span>

<span data-ttu-id="cbf24-1728">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1728">7</span></span>

<span data-ttu-id="cbf24-1729">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1729">8</span></span>

<span data-ttu-id="cbf24-1730">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1730">9</span></span>

<span data-ttu-id="cbf24-1731">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1731">2</span></span><br/> <span data-ttu-id="cbf24-1732">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1732">0</span></span><br/>

<span data-ttu-id="cbf24-1733">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1733">1</span></span>

<span data-ttu-id="cbf24-1734">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1734">2</span></span>

<span data-ttu-id="cbf24-1735">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1735">3</span></span>

<span data-ttu-id="cbf24-1736">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1736">4</span></span>

<span data-ttu-id="cbf24-1737">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1737">5</span></span>

<span data-ttu-id="cbf24-1738">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1738">6</span></span>

<span data-ttu-id="cbf24-1739">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1739">7</span></span>

<span data-ttu-id="cbf24-1740">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1740">8</span></span>

<span data-ttu-id="cbf24-1741">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1741">9</span></span>

<span data-ttu-id="cbf24-1742">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1742">3</span></span><br/> <span data-ttu-id="cbf24-1743">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1743">0</span></span><br/>

<span data-ttu-id="cbf24-1744">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1744">1</span></span>

<span data-ttu-id="cbf24-1745">count</span><span class="sxs-lookup"><span data-stu-id="cbf24-1745">count</span></span>

<span data-ttu-id="cbf24-1746">índices (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1746">indexes (variable)</span></span>



 

<span data-ttu-id="cbf24-1747">**count:** entero de 32 bits sin signo que especifica el número de elementos de la matriz de índices.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1747">**count**: A 32-bit unsigned integer specifying the number of elements in the indexes array.</span></span>

<span data-ttu-id="cbf24-1748">**indexes:** matriz de enteros sin signo de 4 bytes que representan índices de base cero en la matriz aPropSpec de la estructura CPidMapper correspondiente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1748">**indexes**: Array of 4-byte unsigned integers representing zero-based indexes into the aPropSpec array in the corresponding CPidMapper structure.</span></span>

### <a name="22118-ccategorizationset"></a><span data-ttu-id="cbf24-1749">2.2.1.18 CCategorizationSet</span><span class="sxs-lookup"><span data-stu-id="cbf24-1749">2.2.1.18 CCategorizationSet</span></span>

<span data-ttu-id="cbf24-1750">La estructura CCategorizationSet contiene información sobre la agrupación de un conjunto de resultados de consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1750">The CCategorizationSet structure contains information about the grouping of a query result set.</span></span>



<span data-ttu-id="cbf24-1751">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1751">0</span></span>

<span data-ttu-id="cbf24-1752">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1752">1</span></span>

<span data-ttu-id="cbf24-1753">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1753">2</span></span>

<span data-ttu-id="cbf24-1754">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1754">3</span></span>

<span data-ttu-id="cbf24-1755">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1755">4</span></span>

<span data-ttu-id="cbf24-1756">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1756">5</span></span>

<span data-ttu-id="cbf24-1757">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1757">6</span></span>

<span data-ttu-id="cbf24-1758">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1758">7</span></span>

<span data-ttu-id="cbf24-1759">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1759">8</span></span>

<span data-ttu-id="cbf24-1760">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1760">9</span></span>

<span data-ttu-id="cbf24-1761">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1761">1</span></span><br/> <span data-ttu-id="cbf24-1762">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1762">0</span></span><br/>

<span data-ttu-id="cbf24-1763">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1763">1</span></span>

<span data-ttu-id="cbf24-1764">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1764">2</span></span>

<span data-ttu-id="cbf24-1765">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1765">3</span></span>

<span data-ttu-id="cbf24-1766">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1766">4</span></span>

<span data-ttu-id="cbf24-1767">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1767">5</span></span>

<span data-ttu-id="cbf24-1768">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1768">6</span></span>

<span data-ttu-id="cbf24-1769">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1769">7</span></span>

<span data-ttu-id="cbf24-1770">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1770">8</span></span>

<span data-ttu-id="cbf24-1771">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1771">9</span></span>

<span data-ttu-id="cbf24-1772">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1772">2</span></span><br/> <span data-ttu-id="cbf24-1773">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1773">0</span></span><br/>

<span data-ttu-id="cbf24-1774">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1774">1</span></span>

<span data-ttu-id="cbf24-1775">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1775">2</span></span>

<span data-ttu-id="cbf24-1776">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1776">3</span></span>

<span data-ttu-id="cbf24-1777">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1777">4</span></span>

<span data-ttu-id="cbf24-1778">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1778">5</span></span>

<span data-ttu-id="cbf24-1779">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1779">6</span></span>

<span data-ttu-id="cbf24-1780">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1780">7</span></span>

<span data-ttu-id="cbf24-1781">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1781">8</span></span>

<span data-ttu-id="cbf24-1782">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1782">9</span></span>

<span data-ttu-id="cbf24-1783">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1783">3</span></span><br/> <span data-ttu-id="cbf24-1784">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1784">0</span></span><br/>

<span data-ttu-id="cbf24-1785">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1785">1</span></span>

<span data-ttu-id="cbf24-1786">count</span><span class="sxs-lookup"><span data-stu-id="cbf24-1786">count</span></span>

<span data-ttu-id="cbf24-1787">categorías (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1787">categories (variable)</span></span>



 

<span data-ttu-id="cbf24-1788">**count:** entero de 32 bits sin signo que contiene el número de elementos de la matriz categories.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1788">**count**: A 32-bit unsigned integer containing the number of elements in the categories array.</span></span>

<span data-ttu-id="cbf24-1789">**categories**: matriz de estructuras CCategorizationSpec que especifican la agrupación de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1789">**categories**: Array of CCategorizationSpec structures specifying the grouping of the query.</span></span>

### <a name="22119-ccategorizationspec"></a><span data-ttu-id="cbf24-1790">2.2.1.19 CCategorizationSpec</span><span class="sxs-lookup"><span data-stu-id="cbf24-1790">2.2.1.19 CCategorizationSpec</span></span>

<span data-ttu-id="cbf24-1791">La estructura CCategorizationSpec contiene una agrupación para un conjunto de resultados de consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1791">The CCategorizationSpec structure contains a grouping for a query result set.</span></span>



<span data-ttu-id="cbf24-1792">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1792">0</span></span>

<span data-ttu-id="cbf24-1793">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1793">1</span></span>

<span data-ttu-id="cbf24-1794">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1794">2</span></span>

<span data-ttu-id="cbf24-1795">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1795">3</span></span>

<span data-ttu-id="cbf24-1796">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1796">4</span></span>

<span data-ttu-id="cbf24-1797">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1797">5</span></span>

<span data-ttu-id="cbf24-1798">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1798">6</span></span>

<span data-ttu-id="cbf24-1799">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1799">7</span></span>

<span data-ttu-id="cbf24-1800">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1800">8</span></span>

<span data-ttu-id="cbf24-1801">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1801">9</span></span>

<span data-ttu-id="cbf24-1802">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1802">1</span></span><br/> <span data-ttu-id="cbf24-1803">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1803">0</span></span><br/>

<span data-ttu-id="cbf24-1804">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1804">1</span></span>

<span data-ttu-id="cbf24-1805">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1805">2</span></span>

<span data-ttu-id="cbf24-1806">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1806">3</span></span>

<span data-ttu-id="cbf24-1807">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1807">4</span></span>

<span data-ttu-id="cbf24-1808">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1808">5</span></span>

<span data-ttu-id="cbf24-1809">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1809">6</span></span>

<span data-ttu-id="cbf24-1810">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1810">7</span></span>

<span data-ttu-id="cbf24-1811">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1811">8</span></span>

<span data-ttu-id="cbf24-1812">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1812">9</span></span>

<span data-ttu-id="cbf24-1813">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1813">2</span></span><br/> <span data-ttu-id="cbf24-1814">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1814">0</span></span><br/>

<span data-ttu-id="cbf24-1815">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1815">1</span></span>

<span data-ttu-id="cbf24-1816">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1816">2</span></span>

<span data-ttu-id="cbf24-1817">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1817">3</span></span>

<span data-ttu-id="cbf24-1818">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1818">4</span></span>

<span data-ttu-id="cbf24-1819">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1819">5</span></span>

<span data-ttu-id="cbf24-1820">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1820">6</span></span>

<span data-ttu-id="cbf24-1821">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1821">7</span></span>

<span data-ttu-id="cbf24-1822">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1822">8</span></span>

<span data-ttu-id="cbf24-1823">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1823">9</span></span>

<span data-ttu-id="cbf24-1824">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1824">3</span></span><br/> <span data-ttu-id="cbf24-1825">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1825">0</span></span><br/>

<span data-ttu-id="cbf24-1826">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1826">1</span></span>

<span data-ttu-id="cbf24-1827">\_csColumns (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1827">\_csColumns (variable)</span></span>

<span data-ttu-id="cbf24-1828">\_ulCategType</span><span class="sxs-lookup"><span data-stu-id="cbf24-1828">\_ulCategType</span></span>



 

<span data-ttu-id="cbf24-1829">**\_ csColumns:** estructura CColumnSet que indica las columnas por las que se va a agrupar la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1829">**\_csColumns**: A CColumnSet structure indicating the columns by which to group the query.</span></span>

<span data-ttu-id="cbf24-1830">**\_ ulCategType:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1830">**\_ulCategType**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cbf24-1831">DEBE establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1831">MUST be set to 0x00000000.</span></span>

### <a name="22120-cdbcolid"></a><span data-ttu-id="cbf24-1832">2.2.1.20 CDbColId</span><span class="sxs-lookup"><span data-stu-id="cbf24-1832">2.2.1.20 CDbColId</span></span>

<span data-ttu-id="cbf24-1833">La estructura CDbColId contiene una columna.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1833">The CDbColId structure contains a column.</span></span>



<span data-ttu-id="cbf24-1834">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1834">0</span></span>

<span data-ttu-id="cbf24-1835">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1835">1</span></span>

<span data-ttu-id="cbf24-1836">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1836">2</span></span>

<span data-ttu-id="cbf24-1837">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1837">3</span></span>

<span data-ttu-id="cbf24-1838">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1838">4</span></span>

<span data-ttu-id="cbf24-1839">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1839">5</span></span>

<span data-ttu-id="cbf24-1840">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1840">6</span></span>

<span data-ttu-id="cbf24-1841">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1841">7</span></span>

<span data-ttu-id="cbf24-1842">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1842">8</span></span>

<span data-ttu-id="cbf24-1843">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1843">9</span></span>

<span data-ttu-id="cbf24-1844">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1844">1</span></span><br/> <span data-ttu-id="cbf24-1845">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1845">0</span></span><br/>

<span data-ttu-id="cbf24-1846">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1846">1</span></span>

<span data-ttu-id="cbf24-1847">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1847">2</span></span>

<span data-ttu-id="cbf24-1848">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1848">3</span></span>

<span data-ttu-id="cbf24-1849">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1849">4</span></span>

<span data-ttu-id="cbf24-1850">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1850">5</span></span>

<span data-ttu-id="cbf24-1851">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1851">6</span></span>

<span data-ttu-id="cbf24-1852">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1852">7</span></span>

<span data-ttu-id="cbf24-1853">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1853">8</span></span>

<span data-ttu-id="cbf24-1854">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1854">9</span></span>

<span data-ttu-id="cbf24-1855">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1855">2</span></span><br/> <span data-ttu-id="cbf24-1856">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1856">0</span></span><br/>

<span data-ttu-id="cbf24-1857">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1857">1</span></span>

<span data-ttu-id="cbf24-1858">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1858">2</span></span>

<span data-ttu-id="cbf24-1859">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1859">3</span></span>

<span data-ttu-id="cbf24-1860">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1860">4</span></span>

<span data-ttu-id="cbf24-1861">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1861">5</span></span>

<span data-ttu-id="cbf24-1862">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1862">6</span></span>

<span data-ttu-id="cbf24-1863">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1863">7</span></span>

<span data-ttu-id="cbf24-1864">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1864">8</span></span>

<span data-ttu-id="cbf24-1865">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1865">9</span></span>

<span data-ttu-id="cbf24-1866">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1866">3</span></span><br/> <span data-ttu-id="cbf24-1867">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1867">0</span></span><br/>

<span data-ttu-id="cbf24-1868">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1868">1</span></span>

<span data-ttu-id="cbf24-1869">eKind</span><span class="sxs-lookup"><span data-stu-id="cbf24-1869">eKind</span></span>

<span data-ttu-id="cbf24-1870">GUID</span><span class="sxs-lookup"><span data-stu-id="cbf24-1870">GUID</span></span>

<span data-ttu-id="cbf24-1871">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-1871">...</span></span>

<span data-ttu-id="cbf24-1872">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-1872">...</span></span>

<span data-ttu-id="cbf24-1873">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-1873">...</span></span>

<span data-ttu-id="cbf24-1874">ulId</span><span class="sxs-lookup"><span data-stu-id="cbf24-1874">ulId</span></span>

<span data-ttu-id="cbf24-1875">vString (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1875">vString (variable)</span></span>



 

<span data-ttu-id="cbf24-1876">**eKind:** debe establecerse en uno de los valores siguientes que indica el contenido de GUID y vValue.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1876">**eKind**: MUST be set to one of the values below that indicates the contents of GUID and vValue.</span></span>



| <span data-ttu-id="cbf24-1877">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-1877">Value</span></span>                            | <span data-ttu-id="cbf24-1878">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-1878">Meaning</span></span>                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-1879">Nombre del GUID de DBKIND \_ \_ 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-1879">DBKIND\_GUID\_NAME 0x00000000</span></span>    | <span data-ttu-id="cbf24-1880">vString contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1880">vString contains a property name.</span></span>                                                                               |
| <span data-ttu-id="cbf24-1881">DBKIND \_ GUID \_ PROPID 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-1881">DBKIND\_GUID\_PROPID 0x00000001</span></span>  | <span data-ttu-id="cbf24-1882">ulId contiene un entero de 4 bytes que indica el identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1882">ulId contains a 4-byte integer indicating the property ID.</span></span>                                                      |
| <span data-ttu-id="cbf24-1883">Nombre \_ de PGUID de DBKIND \_ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cbf24-1883">DBKIND\_PGUID\_NAME 0x00000003</span></span>   | <span data-ttu-id="cbf24-1884">vString contiene un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1884">vString contains a property name.</span></span> <span data-ttu-id="cbf24-1885">Este valor DEBE tratarse igual que DBKIND \_ GUID \_ NAME.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1885">This value MUST be treated the same as DBKIND\_GUID\_NAME.</span></span>                    |
| <span data-ttu-id="cbf24-1886">DBKIND \_ PGUID \_ PROPID 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cbf24-1886">DBKIND\_PGUID\_PROPID 0x00000004</span></span> | <span data-ttu-id="cbf24-1887">ulId contiene un entero de 4 bytes que indica el identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1887">ulId contains a 4-byte integer indicating the property ID.</span></span> <span data-ttu-id="cbf24-1888">Este valor DEBE ser el mismo que DBKIND \_ GUID \_ PROPID.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1888">This value MUST be the same as DBKIND\_GUID\_PROPID.</span></span> |



 

<span data-ttu-id="cbf24-1889">**GUID: GUID** de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1889">**GUID**: The property GUID.</span></span>

<span data-ttu-id="cbf24-1890">**ulId:** si eKind es DBKIND GUID PROPID o \_ \_ DBKIND \_ PGUID PROPID, este campo contiene un entero sin signo, especificando el \_ identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1890">**ulId**: If eKind is DBKIND\_GUID\_PROPID or DBKIND\_PGUID\_PROPID, this field contains an unsigned integer, specifying the property ID.</span></span> <span data-ttu-id="cbf24-1891">Si eKind es DBKIND GUID NAME o \_ \_ DBKIND PGUID NAME, este campo contiene un entero sin signo que especifica el número de caracteres Unicode contenidos en el \_ \_ campo vString.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1891">If eKind is DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME, this field contains an unsigned integer specifying the number of Unicode characters contained in the vString field.</span></span>

<span data-ttu-id="cbf24-1892">**vString:** cadena Unicode no terminada en NULL que representa el nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1892">**vString**: A non null-terminated Unicode string representing the property name.</span></span> <span data-ttu-id="cbf24-1893">Debe omitirse a menos que el campo eKind esté establecido en DBKIND \_ GUID \_ NAME o DBKIND \_ PGUID \_ NAME.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1893">It MUST be omitted unless the eKind field is set to DBKIND\_GUID\_NAME or DBKIND\_PGUID\_NAME.</span></span>

### <a name="22121-cdbprop"></a><span data-ttu-id="cbf24-1894">2.2.1.21 CDbProp</span><span class="sxs-lookup"><span data-stu-id="cbf24-1894">2.2.1.21 CDbProp</span></span>

<span data-ttu-id="cbf24-1895">La estructura CDbProp contiene una propiedad .</span><span class="sxs-lookup"><span data-stu-id="cbf24-1895">The CDbProp structure contains a property.</span></span>



<span data-ttu-id="cbf24-1896">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1896">0</span></span>

<span data-ttu-id="cbf24-1897">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1897">1</span></span>

<span data-ttu-id="cbf24-1898">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1898">2</span></span>

<span data-ttu-id="cbf24-1899">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1899">3</span></span>

<span data-ttu-id="cbf24-1900">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1900">4</span></span>

<span data-ttu-id="cbf24-1901">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1901">5</span></span>

<span data-ttu-id="cbf24-1902">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1902">6</span></span>

<span data-ttu-id="cbf24-1903">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1903">7</span></span>

<span data-ttu-id="cbf24-1904">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1904">8</span></span>

<span data-ttu-id="cbf24-1905">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1905">9</span></span>

<span data-ttu-id="cbf24-1906">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1906">1</span></span><br/> <span data-ttu-id="cbf24-1907">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1907">0</span></span><br/>

<span data-ttu-id="cbf24-1908">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1908">1</span></span>

<span data-ttu-id="cbf24-1909">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1909">2</span></span>

<span data-ttu-id="cbf24-1910">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1910">3</span></span>

<span data-ttu-id="cbf24-1911">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1911">4</span></span>

<span data-ttu-id="cbf24-1912">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1912">5</span></span>

<span data-ttu-id="cbf24-1913">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1913">6</span></span>

<span data-ttu-id="cbf24-1914">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1914">7</span></span>

<span data-ttu-id="cbf24-1915">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1915">8</span></span>

<span data-ttu-id="cbf24-1916">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1916">9</span></span>

<span data-ttu-id="cbf24-1917">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1917">2</span></span><br/> <span data-ttu-id="cbf24-1918">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1918">0</span></span><br/>

<span data-ttu-id="cbf24-1919">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1919">1</span></span>

<span data-ttu-id="cbf24-1920">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-1920">2</span></span>

<span data-ttu-id="cbf24-1921">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1921">3</span></span>

<span data-ttu-id="cbf24-1922">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-1922">4</span></span>

<span data-ttu-id="cbf24-1923">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-1923">5</span></span>

<span data-ttu-id="cbf24-1924">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-1924">6</span></span>

<span data-ttu-id="cbf24-1925">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-1925">7</span></span>

<span data-ttu-id="cbf24-1926">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-1926">8</span></span>

<span data-ttu-id="cbf24-1927">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-1927">9</span></span>

<span data-ttu-id="cbf24-1928">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-1928">3</span></span><br/> <span data-ttu-id="cbf24-1929">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-1929">0</span></span><br/>

<span data-ttu-id="cbf24-1930">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-1930">1</span></span>

<span data-ttu-id="cbf24-1931">DBPROPID</span><span class="sxs-lookup"><span data-stu-id="cbf24-1931">DBPROPID</span></span>

<span data-ttu-id="cbf24-1932">DBPROPOPTIONS</span><span class="sxs-lookup"><span data-stu-id="cbf24-1932">DBPROPOPTIONS</span></span>

<span data-ttu-id="cbf24-1933">DBPROPSTATUS</span><span class="sxs-lookup"><span data-stu-id="cbf24-1933">DBPROPSTATUS</span></span>

<span data-ttu-id="cbf24-1934">yd (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1934">colid (variable)</span></span>

<span data-ttu-id="cbf24-1935">vValue (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-1935">vValue (variable)</span></span>



 

<span data-ttu-id="cbf24-1936">**DBPROPID:** entero de 32 bits sin signo que indica el identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1936">**DBPROPID**: A 32-bit unsigned integer, indicating the property ID.</span></span>

<span data-ttu-id="cbf24-1937">**DBPROPOPTIONS:** DEBE establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1937">**DBPROPOPTIONS** : MUST be set to 0x00000000.</span></span>

<span data-ttu-id="cbf24-1938">**DBPROPSTATUS:** DEBE establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1938">**DBPROPSTATUS**: MUST be set to 0x00000000.</span></span>

<span data-ttu-id="cbf24-1939">**: estructura** CDbColId, como se especifica en la sección 2.2.1.20, que indica la columna a la que se aplica la propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1939">**colid**: A CDbColId structure, as specified in section 2.2.1.20, indicating the column to which the property applies.</span></span>

<span data-ttu-id="cbf24-1940">**vValue:** CBaseStorageVariant que contiene el valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1940">**vValue**: A CBaseStorageVariant containing the property value.</span></span>

### <a name="221211-properties"></a><span data-ttu-id="cbf24-1941">2.2.1.21.1 Propiedades</span><span class="sxs-lookup"><span data-stu-id="cbf24-1941">2.2.1.21.1 Properties</span></span>

<span data-ttu-id="cbf24-1942">En esta sección se detallan las propiedades que usa CISP.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1942">This section details the properties that are used by CISP.</span></span> <span data-ttu-id="cbf24-1943">Estas propiedades se agrupan en tres conjuntos de propiedades, ident2.2.1.21.1, en el campo guidPropertySet de la estructura CDbPropSet (sección 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="cbf24-1943">These properties are grouped into three property sets, ident2.2.1.21.1 ified in the guidPropertySet field of the CDbPropSet structure (Section 2.2.1.22).</span></span>

<span data-ttu-id="cbf24-1944">En la tabla siguiente se enumeran las propiedades que forman parte del conjunto de propiedades DBPROPSET \_ FSCIFRMWRK \_ EXT.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1944">The following table lists the properties that are part of the DBPROPSET\_FSCIFRMWRK\_EXT property set.</span></span>



| <span data-ttu-id="cbf24-1945">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-1945">Value</span></span>                                  | <span data-ttu-id="cbf24-1946">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-1946">Meaning</span></span>                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-1947">Nombre del CATÁLOGO DE CI de DBPROP \_ \_ \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbf24-1947">DBPROP\_CI\_CATALOG\_NAME 0x00000002</span></span>   | <span data-ttu-id="cbf24-1948">Especifica el nombre del catálogo o catálogos que se consultan.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1948">Specifies the name of the catalog or catalogs to query.</span></span> <span data-ttu-id="cbf24-1949">El valor DEBE ser VT \_ LPWSTR o VT \_ VECTOR \| VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1949">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR</span></span>                                   |
| <span data-ttu-id="cbf24-1950">ÁMBITOS \_ DE INCLUIR \_ ÁMBITOS DE CI DE DBPROP \_ 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cbf24-1950">DBPROP\_CI\_INCLUDE\_SCOPES 0x00000003</span></span> | <span data-ttu-id="cbf24-1951">Especifica una o varias rutas de acceso que se incluirán en la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1951">Specifies one or more paths to be included in the query.</span></span> <span data-ttu-id="cbf24-1952">El valor DEBE ser VT \_ LPWSTR o VT \_ VECTOR \| VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1952">Value MUST be a VT\_LPWSTR or a VT\_VECTOR \| VT\_LPWSTR.</span></span>                                 |
| <span data-ttu-id="cbf24-1953">MARCAS DE ÁMBITO DE CI DE DBPROP \_ \_ \_ 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cbf24-1953">DBPROP\_CI\_SCOPE\_FLAGS 0x00000004</span></span>    | <span data-ttu-id="cbf24-1954">Especifica cómo se van a tratar las rutas de acceso especificadas por la propiedad DBPROP \_ CI \_ INCLUDE \_ SCOPES.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1954">Specifies how the paths specified by the DBPROP\_CI\_INCLUDE\_SCOPES property are to be treated.</span></span> <span data-ttu-id="cbf24-1955">El valor DEBE ser VT \_ I4 o VT \_ VECTOR VT \| \_ I4.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1955">Value MUST be a VT\_I4 or a VT\_VECTOR \| VT\_I4.</span></span> |
| <span data-ttu-id="cbf24-1956">TIPO DE \_ CONSULTA DE CI \_ \_ DBPROP 0x00000007</span><span class="sxs-lookup"><span data-stu-id="cbf24-1956">DBPROP\_CI\_QUERY\_TYPE 0x00000007</span></span>     | <span data-ttu-id="cbf24-1957">Especifica el tipo de consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1957">Specifies the type of query.</span></span> <span data-ttu-id="cbf24-1958">CDbColId DEBE establecerse en \_ NULLID de base de datos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1958">The CDbColId MUST be set to DB\_NULLID.</span></span>                                                                               |



 

<span data-ttu-id="cbf24-1959">En la tabla siguiente se enumeran las marcas de la propiedad DBPROP \_ CI \_ SCOPE \_ FLAGS:</span><span class="sxs-lookup"><span data-stu-id="cbf24-1959">The following table lists the flags for the DBPROP\_CI\_SCOPE\_FLAGS property:</span></span>



| <span data-ttu-id="cbf24-1960">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-1960">Value</span></span>                     | <span data-ttu-id="cbf24-1961">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-1961">Meaning</span></span>                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-1962">CONSULTA \_ DE DATOS 0X01</span><span class="sxs-lookup"><span data-stu-id="cbf24-1962">QUERY\_DEEP 0x01</span></span>          | <span data-ttu-id="cbf24-1963">Si se establece, indica que los archivos del directorio de ámbito y todos los subdirectorios se incluyen en los resultados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1963">If set, indicates that files in the scope directory and all subdirectories are included in the results.</span></span> <span data-ttu-id="cbf24-1964">Si está claro, solo los archivos del directorio de ámbito se incluyen en los resultados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1964">If clear, only files in the scope directory are included in the results.</span></span> <span data-ttu-id="cbf24-1965">NO SE DEBE combinar con QUERY \_ DEEP.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1965">MUST NOT be combined with QUERY\_DEEP.</span></span> |
| <span data-ttu-id="cbf24-1966">RUTA \_ DE ACCESO VIRTUAL DE CONSULTA \_ 0x02</span><span class="sxs-lookup"><span data-stu-id="cbf24-1966">QUERY\_VIRTUAL\_PATH 0x02</span></span> | <span data-ttu-id="cbf24-1967">Si se establece, indica que el ámbito es una ruta de acceso virtual.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1967">If set, indicates that the scope is a virtual path.</span></span> <span data-ttu-id="cbf24-1968">Si está claro, indica que el ámbito es un directorio físico.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1968">If clear, indicates that the scope is a physical directory.</span></span>                                                                                                         |



 

<span data-ttu-id="cbf24-1969">En la tabla siguiente se enumeran los tipos de consulta para la propiedad DBPROP \_ CI \_ QUERY \_ TYPE:</span><span class="sxs-lookup"><span data-stu-id="cbf24-1969">The following table lists the query types for the DBPROP\_CI\_QUERY\_TYPE property:</span></span>



| <span data-ttu-id="cbf24-1970">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-1970">Value</span></span>                     | <span data-ttu-id="cbf24-1971">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-1971">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-1972">CiNormal 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-1972">CiNormal 0x00000000</span></span>       | <span data-ttu-id="cbf24-1973">Una consulta normal.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1973">A regular query.</span></span>                                                                                                   |
| <span data-ttu-id="cbf24-1974">CiVirtualRoots 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-1974">CiVirtualRoots 0x00000001</span></span> | <span data-ttu-id="cbf24-1975">La consulta solicita una lista de las raíces virtuales del catálogo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1975">The query is requesting a list of the virtual roots of the catalog.</span></span> <span data-ttu-id="cbf24-1976">Este valor requiere privilegios administrativos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1976">This value requires administrative privileges.</span></span> |
| <span data-ttu-id="cbf24-1977">CiProperties 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cbf24-1977">CiProperties 0x00000003</span></span>   | <span data-ttu-id="cbf24-1978">La consulta solicita una lista de todas las propiedades admitidas por el servicio de indexación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1978">The query is requesting a list of all the properties supported by the indexing service.</span></span>                            |
| <span data-ttu-id="cbf24-1979">CiAdminOp 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cbf24-1979">CiAdminOp 0x00000004</span></span>      | <span data-ttu-id="cbf24-1980">La consulta es una operación administrativa.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1980">The query is an administrative operation.</span></span> <span data-ttu-id="cbf24-1981">Este valor requiere privilegios administrativos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1981">This value requires administrative privileges.</span></span>                           |



 

<span data-ttu-id="cbf24-1982">En la tabla siguiente se enumeran las propiedades que forman parte del conjunto de propiedades DBPROPSET \_ QUERYEXT.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1982">The following table lists the properties that are part of the DBPROPSET\_QUERYEXT property set.</span></span>



| <span data-ttu-id="cbf24-1983">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-1983">Value</span></span>                                      | <span data-ttu-id="cbf24-1984">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-1984">Meaning</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-1985">DBPROP \_ USECONTENTINDEX 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbf24-1985">DBPROP\_USECONTENTINDEX 0x00000002</span></span>         | <span data-ttu-id="cbf24-1986">Especifica cómo el servicio de indexación debe controlar consultas lentas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1986">Specifies how the indexing service is to handle slow queries.</span></span> <span data-ttu-id="cbf24-1987">El valor DEBE ser un \_ VT BOOL.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1987">Value MUST be a VT\_BOOL.</span></span> <span data-ttu-id="cbf24-1988">Si es TRUE, el servidor puede producir un error en estas consultas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1988">If TRUE, the server is allowed to fail these queries.</span></span>                                                                                    |
| <span data-ttu-id="cbf24-1989">DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cbf24-1989">DBPROP\_DEFERNONINDEXEDTRIMMING 0x00000003</span></span> | <span data-ttu-id="cbf24-1990">Indica si el servicio de indexación va a realizar el recorte de resultados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1990">Indicates whether the indexing service is to perform results trimming.</span></span> <span data-ttu-id="cbf24-1991">Si es TRUE, el servidor debe considerar la posibilidad de realizar el recorte de resultados de forma que optimice el tiempo de respuesta al cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1991">If TRUE, the server is to consider performing results trimming in a way that optimizes response time to the client.</span></span> <span data-ttu-id="cbf24-1992">El valor DEBE ser un \_ VT BOOL.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1992">Value MUST be a VT\_BOOL.</span></span>             |
| <span data-ttu-id="cbf24-1993">DBPROP \_ USEEXTENDEDDBTYPES 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cbf24-1993">DBPROP\_USEEXTENDEDDBTYPES 0x00000004</span></span>      | <span data-ttu-id="cbf24-1994">Indica si el cliente admite tipos de datos VT \_ VECTOR.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1994">Indicates whether the client supports VT\_VECTOR data types.</span></span> <span data-ttu-id="cbf24-1995">Si es TRUE, el cliente admite VT VECTOR; si es FALSE, el servidor va a convertir tipos de datos VT VECTOR en tipos de datos \_ \_ VT \_ ARRAY.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1995">If TRUE, then the client supports VT\_VECTOR; if FALSE, then the server is to convert VT\_VECTOR data types to VT\_ARRAY data types.</span></span>  <span data-ttu-id="cbf24-1996">El valor DEBE ser VT \_ BOOL.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1996">The value MUST be a VT\_BOOL.</span></span> |
| <span data-ttu-id="cbf24-1997">DBPROP \_ FIRSTROWS 0x00000007</span><span class="sxs-lookup"><span data-stu-id="cbf24-1997">DBPROP\_FIRSTROWS 0x00000007</span></span>               | <span data-ttu-id="cbf24-1998">Indica las coincidencias de fila que se devolverán.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1998">Indicates the row matches to return.</span></span> <span data-ttu-id="cbf24-1999">Si es TRUE, el servidor devolverá el primer conjunto de filas coincidentes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-1999">If TRUE, the server is to return the first set of matching rows.</span></span> <span data-ttu-id="cbf24-2000">Si es FALSE, se deben devolver las mejores filas coincidentes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2000">If FALSE, the best matching rows should be returned.</span></span> <span data-ttu-id="cbf24-2001">El valor DEBE ser un \_ VT BOOL.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2001">Value MUST be a VT\_BOOL.</span></span>                                             |



 

<span data-ttu-id="cbf24-2002">En la tabla siguiente se enumeran las propiedades que forman parte del conjunto de propiedades DBPROPSET \_ CIFRMWRKCORE \_ EXT.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2002">The following table lists the properties that are part of the DBPROPSET\_CIFRMWRKCORE\_EXT property set.</span></span>



| <span data-ttu-id="cbf24-2003">Valor/DBPROPID</span><span class="sxs-lookup"><span data-stu-id="cbf24-2003">Value / DBPROPID</span></span>                 | <span data-ttu-id="cbf24-2004">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-2004">Meaning</span></span>                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-2005">DbPROP \_ MACHINE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbf24-2005">DBPROP\_MACHINE 0x00000002</span></span>       | <span data-ttu-id="cbf24-2006">Especifica los nombres de los equipos en los que se va a procesar una consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2006">Specifies the names of the computer(s) on which a query is to be processed.</span></span> <span data-ttu-id="cbf24-2007">El valor DEBE ser VT \_ BSTR o VT \_ ARRAY VT \| \_ BSTR.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2007">The value MUST be either VT\_BSTR or VT\_ARRAY \| VT\_BSTR.</span></span> |
| <span data-ttu-id="cbf24-2008">DBPROP \_ CLIENT \_ CLSID 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cbf24-2008">DBPROP\_CLIENT\_CLSID 0x00000003</span></span> | <span data-ttu-id="cbf24-2009">Especifica una constante de conexión para el servicio de indexación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2009">Specifies a connection constant for the indexing service.</span></span> <span data-ttu-id="cbf24-2010">El valor DEBE ser un \_ CLSID VT que contenga 0x2A4880706FD911D0A80800A0C906241A.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2010">The value MUST be a VT\_CLSID containing 0x2A4880706FD911D0A80800A0C906241A.</span></span>  |



 

### <a name="22122-cdbpropset"></a><span data-ttu-id="cbf24-2011">2.2.1.22 CDbPropSet</span><span class="sxs-lookup"><span data-stu-id="cbf24-2011">2.2.1.22 CDbPropSet</span></span>

<span data-ttu-id="cbf24-2012">La estructura CDbPropSet contiene un conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2012">The CDbPropSet structure contains a set of properties.</span></span> <span data-ttu-id="cbf24-2013">Tenga en cuenta que el primer campo es de tamaño fijo, pero puede que no esté alineado en un desplazamiento que sea un múltiplo de 4 bytes desde el inicio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2013">Note that the first field is fixed-size, but may not be aligned at an offset that is a 4-byte multiple from the start of the message containing this structure.</span></span> <span data-ttu-id="cbf24-2014">Sin embargo, el campo cProperties está alineado como tal y, por lo tanto, el formato se representa de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-2014">However, the cProperties field is aligned as such, and hence the format is depicted as follows:</span></span>



<span data-ttu-id="cbf24-2015">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2015">0</span></span>

<span data-ttu-id="cbf24-2016">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2016">1</span></span>

<span data-ttu-id="cbf24-2017">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2017">2</span></span>

<span data-ttu-id="cbf24-2018">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2018">3</span></span>

<span data-ttu-id="cbf24-2019">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2019">4</span></span>

<span data-ttu-id="cbf24-2020">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2020">5</span></span>

<span data-ttu-id="cbf24-2021">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2021">6</span></span>

<span data-ttu-id="cbf24-2022">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2022">7</span></span>

<span data-ttu-id="cbf24-2023">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2023">8</span></span>

<span data-ttu-id="cbf24-2024">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2024">9</span></span>

<span data-ttu-id="cbf24-2025">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2025">1</span></span><br/> <span data-ttu-id="cbf24-2026">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2026">0</span></span><br/>

<span data-ttu-id="cbf24-2027">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2027">1</span></span>

<span data-ttu-id="cbf24-2028">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2028">2</span></span>

<span data-ttu-id="cbf24-2029">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2029">3</span></span>

<span data-ttu-id="cbf24-2030">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2030">4</span></span>

<span data-ttu-id="cbf24-2031">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2031">5</span></span>

<span data-ttu-id="cbf24-2032">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2032">6</span></span>

<span data-ttu-id="cbf24-2033">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2033">7</span></span>

<span data-ttu-id="cbf24-2034">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2034">8</span></span>

<span data-ttu-id="cbf24-2035">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2035">9</span></span>

<span data-ttu-id="cbf24-2036">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2036">2</span></span><br/> <span data-ttu-id="cbf24-2037">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2037">0</span></span><br/>

<span data-ttu-id="cbf24-2038">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2038">1</span></span>

<span data-ttu-id="cbf24-2039">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2039">2</span></span>

<span data-ttu-id="cbf24-2040">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2040">3</span></span>

<span data-ttu-id="cbf24-2041">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2041">4</span></span>

<span data-ttu-id="cbf24-2042">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2042">5</span></span>

<span data-ttu-id="cbf24-2043">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2043">6</span></span>

<span data-ttu-id="cbf24-2044">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2044">7</span></span>

<span data-ttu-id="cbf24-2045">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2045">8</span></span>

<span data-ttu-id="cbf24-2046">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2046">9</span></span>

<span data-ttu-id="cbf24-2047">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2047">3</span></span><br/> <span data-ttu-id="cbf24-2048">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2048">0</span></span><br/>

<span data-ttu-id="cbf24-2049">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2049">1</span></span>

<span data-ttu-id="cbf24-2050">guidPropertySet</span><span class="sxs-lookup"><span data-stu-id="cbf24-2050">guidPropertySet</span></span>

<span data-ttu-id="cbf24-2051">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-2051">...</span></span>

<span data-ttu-id="cbf24-2052">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-2052">...</span></span>

<span data-ttu-id="cbf24-2053">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-2053">...</span></span>

<span data-ttu-id="cbf24-2054">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-2054">...</span></span>

<span data-ttu-id="cbf24-2055">\_padding (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2055">\_padding (variable)</span></span>

<span data-ttu-id="cbf24-2056">cProperties</span><span class="sxs-lookup"><span data-stu-id="cbf24-2056">cProperties</span></span>

<span data-ttu-id="cbf24-2057">aProps (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2057">aProps (variable)</span></span>



 

<span data-ttu-id="cbf24-2058">**guidPropertySet:** GUID que identifica el conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2058">**guidPropertySet**: A GUID identifying the property set.</span></span> <span data-ttu-id="cbf24-2059">DEBE establecerse en el formulario binario correspondiente a uno de los siguientes valores (que se muestra en el formulario de representación de cadena), identificando el conjunto de propiedades de las propiedades contenidas en el campo aProps.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2059">MUST be set to the binary form corresponding to one of the following values (shown in string representation form), identifying the property set of the properties contained in the aProps field.</span></span>



| <span data-ttu-id="cbf24-2060">Valor/GUID</span><span class="sxs-lookup"><span data-stu-id="cbf24-2060">Value / GUID</span></span>                                                                              | <span data-ttu-id="cbf24-2061">Nombre</span><span class="sxs-lookup"><span data-stu-id="cbf24-2061">Name</span></span>                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="cbf24-2062">DBPROPSET \_ FSCIFRMWRK \_ EXT</span><span class="sxs-lookup"><span data-stu-id="cbf24-2062">DBPROPSET\_FSCIFRMWRK\_EXT</span></span><br/> <span data-ttu-id="cbf24-2063">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span><span class="sxs-lookup"><span data-stu-id="cbf24-2063">{A9BD1526-6A80-11D0-8C9D-0020AF1D740E}</span></span><br/>   | <span data-ttu-id="cbf24-2064">Conjunto de propiedades del marco de índice de contenido del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="cbf24-2064">File System Content Index Framework Property Set</span></span> |
| <span data-ttu-id="cbf24-2065">DBPROPSET \_ QUERYEXT</span><span class="sxs-lookup"><span data-stu-id="cbf24-2065">DBPROPSET\_QUERYEXT</span></span><br/> <span data-ttu-id="cbf24-2066">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span><span class="sxs-lookup"><span data-stu-id="cbf24-2066">{A7AC77ED-F8D7-11CE-A798-0020F8008025}</span></span><br/>          | <span data-ttu-id="cbf24-2067">Conjunto de propiedades de extensión de consulta</span><span class="sxs-lookup"><span data-stu-id="cbf24-2067">Query Extension Property Set</span></span>                     |
| <span data-ttu-id="cbf24-2068">DBPROPSET \_ CIFRMWRKCORE \_ EXT</span><span class="sxs-lookup"><span data-stu-id="cbf24-2068">DBPROPSET\_CIFRMWRKCORE\_EXT</span></span><br/> <span data-ttu-id="cbf24-2069">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span><span class="sxs-lookup"><span data-stu-id="cbf24-2069">{AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}</span></span><br/> | <span data-ttu-id="cbf24-2070">Conjunto de propiedades de Content Index Framework Core</span><span class="sxs-lookup"><span data-stu-id="cbf24-2070">Content Index Framework Core Property Set</span></span>        |



 

<span data-ttu-id="cbf24-2071">**\_ padding:** este campo DEBE tener entre 0 y 3 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2071">**\_padding**: This field MUST be 0 to 3 bytes in length.</span></span> <span data-ttu-id="cbf24-2072">La longitud de este campo DEBE ser tal que el siguiente campo comienza en un desplazamiento que es un múltiplo de 4 bytes desde el principio del mensaje que contiene esta estructura.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2072">The length of this field MUST be such that the following field begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this structure.</span></span> <span data-ttu-id="cbf24-2073">Si este campo está presente (es decir, longitud distinta de cero), el valor que contiene es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2073">If this field is present (i.e., length nonzero), the value it contains is arbitrary.</span></span> <span data-ttu-id="cbf24-2074">El receptor DEBE omitir el contenido de este campo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2074">The content of this field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cbf24-2075">**cProperties:** entero de 32 bits sin signo que contiene el número de elementos de la matriz aProps.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2075">**cProperties**: A 32-bit unsigned integer containing the number of elements in the aProps array.</span></span>

<span data-ttu-id="cbf24-2076">**aProps:** matriz de estructuras CDbProp, como se especifica en la sección 0, que contiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2076">**aProps**: An array of CDbProp structures, as specified in section 0, containing properties.</span></span> <span data-ttu-id="cbf24-2077">Las estructuras de la matriz DEBEN estar separadas por 0 a 3 bytes de relleno, de forma que cada estructura comience en un desplazamiento que sea un múltiplo de 4 bytes desde el principio del mensaje que contiene esta matriz.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2077">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure begins at an offset that is a multiple of 4 bytes from the beginning of the message that contains this array.</span></span> <span data-ttu-id="cbf24-2078">Si hay bytes de relleno, el valor que contienen es arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2078">If padding bytes are present, the value they contain is arbitrary.</span></span> <span data-ttu-id="cbf24-2079">El receptor DEBE omitir el contenido de los bytes de relleno.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2079">The content of the padding bytes MUST be ignored by the receiver.</span></span>

### <a name="22123-cpidmapper"></a><span data-ttu-id="cbf24-2080">2.2.1.23 CPidMapper</span><span class="sxs-lookup"><span data-stu-id="cbf24-2080">2.2.1.23 CPidMapper</span></span>

<span data-ttu-id="cbf24-2081">La estructura CPidMapper contiene una matriz de los nombres de propiedad que especifican las propiedades que se devolverán en un conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2081">The CPidMapper structure contains an array of property IDs specifying the properties to return in a rowset.</span></span>



<span data-ttu-id="cbf24-2082">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2082">0</span></span>

<span data-ttu-id="cbf24-2083">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2083">1</span></span>

<span data-ttu-id="cbf24-2084">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2084">2</span></span>

<span data-ttu-id="cbf24-2085">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2085">3</span></span>

<span data-ttu-id="cbf24-2086">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2086">4</span></span>

<span data-ttu-id="cbf24-2087">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2087">5</span></span>

<span data-ttu-id="cbf24-2088">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2088">6</span></span>

<span data-ttu-id="cbf24-2089">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2089">7</span></span>

<span data-ttu-id="cbf24-2090">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2090">8</span></span>

<span data-ttu-id="cbf24-2091">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2091">9</span></span>

<span data-ttu-id="cbf24-2092">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2092">1</span></span><br/> <span data-ttu-id="cbf24-2093">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2093">0</span></span><br/>

<span data-ttu-id="cbf24-2094">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2094">1</span></span>

<span data-ttu-id="cbf24-2095">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2095">2</span></span>

<span data-ttu-id="cbf24-2096">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2096">3</span></span>

<span data-ttu-id="cbf24-2097">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2097">4</span></span>

<span data-ttu-id="cbf24-2098">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2098">5</span></span>

<span data-ttu-id="cbf24-2099">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2099">6</span></span>

<span data-ttu-id="cbf24-2100">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2100">7</span></span>

<span data-ttu-id="cbf24-2101">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2101">8</span></span>

<span data-ttu-id="cbf24-2102">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2102">9</span></span>

<span data-ttu-id="cbf24-2103">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2103">2</span></span><br/> <span data-ttu-id="cbf24-2104">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2104">0</span></span><br/>

<span data-ttu-id="cbf24-2105">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2105">1</span></span>

<span data-ttu-id="cbf24-2106">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2106">2</span></span>

<span data-ttu-id="cbf24-2107">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2107">3</span></span>

<span data-ttu-id="cbf24-2108">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2108">4</span></span>

<span data-ttu-id="cbf24-2109">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2109">5</span></span>

<span data-ttu-id="cbf24-2110">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2110">6</span></span>

<span data-ttu-id="cbf24-2111">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2111">7</span></span>

<span data-ttu-id="cbf24-2112">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2112">8</span></span>

<span data-ttu-id="cbf24-2113">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2113">9</span></span>

<span data-ttu-id="cbf24-2114">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2114">3</span></span><br/> <span data-ttu-id="cbf24-2115">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2115">0</span></span><br/>

<span data-ttu-id="cbf24-2116">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2116">1</span></span>

<span data-ttu-id="cbf24-2117">count</span><span class="sxs-lookup"><span data-stu-id="cbf24-2117">count</span></span>

<span data-ttu-id="cbf24-2118">aPropSpec</span><span class="sxs-lookup"><span data-stu-id="cbf24-2118">aPropSpec</span></span>

<span data-ttu-id="cbf24-2119">... (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2119">... (variable)</span></span>



 

<span data-ttu-id="cbf24-2120">**count:** entero de 32 bits sin signo que contiene el número de elementos de la matriz aPropSpec.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2120">**count**: A 32-bit unsigned integer containing the number of elements in the aPropSpec array.</span></span>

<span data-ttu-id="cbf24-2121">**aPropSpec:** matriz de estructuras CFullPropSpec que indican las propiedades que se devolverán.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2121">**aPropSpec**: Array of CFullPropSpec structures indicating the properties to return.</span></span> <span data-ttu-id="cbf24-2122">Las estructuras de la matriz DEBEN estar separadas por 0 a 3 bytes de relleno, de forma que cada estructura tenga una alineación de 4 bytes desde el principio de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2122">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="cbf24-2123">Estos bytes de relleno pueden ser cualquier valor arbitrario y DEBEN omitirse al recibirse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2123">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22124-crowseekat"></a><span data-ttu-id="cbf24-2124">2.2.1.24 CRowSeekAt</span><span class="sxs-lookup"><span data-stu-id="cbf24-2124">2.2.1.24 CRowSeekAt</span></span>

<span data-ttu-id="cbf24-2125">La estructura CRowSeekAt contiene el desplazamiento en el que se van a recuperar las filas de un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2125">The CRowSeekAt structure contains the offset at which to retrieve rows in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="cbf24-2126">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2126">0</span></span>

<span data-ttu-id="cbf24-2127">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2127">1</span></span>

<span data-ttu-id="cbf24-2128">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2128">2</span></span>

<span data-ttu-id="cbf24-2129">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2129">3</span></span>

<span data-ttu-id="cbf24-2130">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2130">4</span></span>

<span data-ttu-id="cbf24-2131">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2131">5</span></span>

<span data-ttu-id="cbf24-2132">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2132">6</span></span>

<span data-ttu-id="cbf24-2133">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2133">7</span></span>

<span data-ttu-id="cbf24-2134">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2134">8</span></span>

<span data-ttu-id="cbf24-2135">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2135">9</span></span>

<span data-ttu-id="cbf24-2136">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2136">1</span></span><br/> <span data-ttu-id="cbf24-2137">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2137">0</span></span><br/>

<span data-ttu-id="cbf24-2138">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2138">1</span></span>

<span data-ttu-id="cbf24-2139">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2139">2</span></span>

<span data-ttu-id="cbf24-2140">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2140">3</span></span>

<span data-ttu-id="cbf24-2141">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2141">4</span></span>

<span data-ttu-id="cbf24-2142">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2142">5</span></span>

<span data-ttu-id="cbf24-2143">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2143">6</span></span>

<span data-ttu-id="cbf24-2144">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2144">7</span></span>

<span data-ttu-id="cbf24-2145">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2145">8</span></span>

<span data-ttu-id="cbf24-2146">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2146">9</span></span>

<span data-ttu-id="cbf24-2147">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2147">2</span></span><br/> <span data-ttu-id="cbf24-2148">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2148">0</span></span><br/>

<span data-ttu-id="cbf24-2149">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2149">1</span></span>

<span data-ttu-id="cbf24-2150">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2150">2</span></span>

<span data-ttu-id="cbf24-2151">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2151">3</span></span>

<span data-ttu-id="cbf24-2152">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2152">4</span></span>

<span data-ttu-id="cbf24-2153">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2153">5</span></span>

<span data-ttu-id="cbf24-2154">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2154">6</span></span>

<span data-ttu-id="cbf24-2155">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2155">7</span></span>

<span data-ttu-id="cbf24-2156">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2156">8</span></span>

<span data-ttu-id="cbf24-2157">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2157">9</span></span>

<span data-ttu-id="cbf24-2158">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2158">3</span></span><br/> <span data-ttu-id="cbf24-2159">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2159">0</span></span><br/>

<span data-ttu-id="cbf24-2160">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2160">1</span></span>

<span data-ttu-id="cbf24-2161">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="cbf24-2161">\_hRegion</span></span>

<span data-ttu-id="cbf24-2162">\_cskip</span><span class="sxs-lookup"><span data-stu-id="cbf24-2162">\_cskip</span></span>

<span data-ttu-id="cbf24-2163">\_bmkOffset</span><span class="sxs-lookup"><span data-stu-id="cbf24-2163">\_bmkOffset</span></span>



 

<span data-ttu-id="cbf24-2164">**\_ hRegion**: DEBE establecerse en 0x00000000 y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2164">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="cbf24-2165">**\_ cskip:** entero de 32 bits sin signo que contiene el número de filas que se omitirán en el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2165">**\_cskip**: A 32-bit unsigned integer containing the number of rows to skip in the rowset.</span></span>

<span data-ttu-id="cbf24-2166">**\_ bmkOffset:** valor de 32 bits que  representa el identificador del marcador que indica la posición inicial desde la que se omite el número de filas especificadas en cskip, antes de comenzar la \_ recuperación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2166">**\_bmkOffset**: A 32-bit value representing the handle of the **bookmark** indicating the starting position from which to skip the number of rows specified in \_cskip, before beginning retrieval.</span></span>

### <a name="22125-crowseekatratio"></a><span data-ttu-id="cbf24-2167">2.2.1.25 CRowSeekAtRatio</span><span class="sxs-lookup"><span data-stu-id="cbf24-2167">2.2.1.25 CRowSeekAtRatio</span></span>

<span data-ttu-id="cbf24-2168">La estructura CRowSeekAtRatio identifica el punto en el que se va a iniciar la recuperación de un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2168">The CRowSeekAtRatio structure identifies the point at which to begin retrieval for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="cbf24-2169">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2169">0</span></span>

<span data-ttu-id="cbf24-2170">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2170">1</span></span>

<span data-ttu-id="cbf24-2171">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2171">2</span></span>

<span data-ttu-id="cbf24-2172">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2172">3</span></span>

<span data-ttu-id="cbf24-2173">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2173">4</span></span>

<span data-ttu-id="cbf24-2174">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2174">5</span></span>

<span data-ttu-id="cbf24-2175">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2175">6</span></span>

<span data-ttu-id="cbf24-2176">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2176">7</span></span>

<span data-ttu-id="cbf24-2177">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2177">8</span></span>

<span data-ttu-id="cbf24-2178">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2178">9</span></span>

<span data-ttu-id="cbf24-2179">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2179">1</span></span><br/> <span data-ttu-id="cbf24-2180">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2180">0</span></span><br/>

<span data-ttu-id="cbf24-2181">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2181">1</span></span>

<span data-ttu-id="cbf24-2182">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2182">2</span></span>

<span data-ttu-id="cbf24-2183">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2183">3</span></span>

<span data-ttu-id="cbf24-2184">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2184">4</span></span>

<span data-ttu-id="cbf24-2185">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2185">5</span></span>

<span data-ttu-id="cbf24-2186">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2186">6</span></span>

<span data-ttu-id="cbf24-2187">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2187">7</span></span>

<span data-ttu-id="cbf24-2188">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2188">8</span></span>

<span data-ttu-id="cbf24-2189">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2189">9</span></span>

<span data-ttu-id="cbf24-2190">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2190">2</span></span><br/> <span data-ttu-id="cbf24-2191">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2191">0</span></span><br/>

<span data-ttu-id="cbf24-2192">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2192">1</span></span>

<span data-ttu-id="cbf24-2193">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2193">2</span></span>

<span data-ttu-id="cbf24-2194">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2194">3</span></span>

<span data-ttu-id="cbf24-2195">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2195">4</span></span>

<span data-ttu-id="cbf24-2196">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2196">5</span></span>

<span data-ttu-id="cbf24-2197">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2197">6</span></span>

<span data-ttu-id="cbf24-2198">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2198">7</span></span>

<span data-ttu-id="cbf24-2199">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2199">8</span></span>

<span data-ttu-id="cbf24-2200">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2200">9</span></span>

<span data-ttu-id="cbf24-2201">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2201">3</span></span><br/> <span data-ttu-id="cbf24-2202">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2202">0</span></span><br/>

<span data-ttu-id="cbf24-2203">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2203">1</span></span>

<span data-ttu-id="cbf24-2204">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="cbf24-2204">CiTblChapt</span></span>

<span data-ttu-id="cbf24-2205">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="cbf24-2205">\_hRegion</span></span>

<span data-ttu-id="cbf24-2206">\_ulNumerator</span><span class="sxs-lookup"><span data-stu-id="cbf24-2206">\_ulNumerator</span></span>

<span data-ttu-id="cbf24-2207">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="cbf24-2207">\_ulDenominator</span></span>



 

<span data-ttu-id="cbf24-2208">**CiTblChapt:** entero de 32 bits sin signo que indica el capítulo del conjunto de filas del que se recuperan las filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2208">**CiTblChapt**: A 32-bit unsigned integer indicating the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="cbf24-2209">**\_ hRegion**: DEBE establecerse en 0x00000000 y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2209">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="cbf24-2210">**\_ ulNumerator:** entero de 32 bits sin signo que representa el numerador de la proporción de filas del capítulo en el que se va a iniciar la recuperación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2210">**\_ulNumerator**: Unsigned 32-bit integer representing the numerator of the ratio of rows in the chapter at which to begin retrieval.</span></span>

<span data-ttu-id="cbf24-2211">**\_ ulDenominator:** entero de 32 bits sin signo que representa el denominador de la proporción de filas del capítulo en el que se va a iniciar la recuperación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2211">**\_ulDenominator**: Unsigned 32-bit integer representing the denominator of the ratio of rows in the chapter at which to begin retrieval.</span></span> <span data-ttu-id="cbf24-2212">DEBE ser mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2212">MUST be greater than zero.</span></span>

### <a name="22126-crowseekbybookmark"></a><span data-ttu-id="cbf24-2213">2.2.1.26 CRowSeekByBookmark</span><span class="sxs-lookup"><span data-stu-id="cbf24-2213">2.2.1.26 CRowSeekByBookmark</span></span>

<span data-ttu-id="cbf24-2214">La estructura CRowSeekByBookmark identifica los marcadores desde los que empezar a recuperar filas para un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2214">The CRowSeekByBookmark structure identifies the bookmarks from which to begin retrieving rows for a CPMGetRowsIn message.</span></span>



<span data-ttu-id="cbf24-2215">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2215">0</span></span>

<span data-ttu-id="cbf24-2216">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2216">1</span></span>

<span data-ttu-id="cbf24-2217">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2217">2</span></span>

<span data-ttu-id="cbf24-2218">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2218">3</span></span>

<span data-ttu-id="cbf24-2219">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2219">4</span></span>

<span data-ttu-id="cbf24-2220">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2220">5</span></span>

<span data-ttu-id="cbf24-2221">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2221">6</span></span>

<span data-ttu-id="cbf24-2222">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2222">7</span></span>

<span data-ttu-id="cbf24-2223">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2223">8</span></span>

<span data-ttu-id="cbf24-2224">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2224">9</span></span>

<span data-ttu-id="cbf24-2225">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2225">1</span></span><br/> <span data-ttu-id="cbf24-2226">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2226">0</span></span><br/>

<span data-ttu-id="cbf24-2227">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2227">1</span></span>

<span data-ttu-id="cbf24-2228">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2228">2</span></span>

<span data-ttu-id="cbf24-2229">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2229">3</span></span>

<span data-ttu-id="cbf24-2230">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2230">4</span></span>

<span data-ttu-id="cbf24-2231">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2231">5</span></span>

<span data-ttu-id="cbf24-2232">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2232">6</span></span>

<span data-ttu-id="cbf24-2233">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2233">7</span></span>

<span data-ttu-id="cbf24-2234">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2234">8</span></span>

<span data-ttu-id="cbf24-2235">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2235">9</span></span>

<span data-ttu-id="cbf24-2236">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2236">2</span></span><br/> <span data-ttu-id="cbf24-2237">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2237">0</span></span><br/>

<span data-ttu-id="cbf24-2238">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2238">1</span></span>

<span data-ttu-id="cbf24-2239">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2239">2</span></span>

<span data-ttu-id="cbf24-2240">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2240">3</span></span>

<span data-ttu-id="cbf24-2241">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2241">4</span></span>

<span data-ttu-id="cbf24-2242">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2242">5</span></span>

<span data-ttu-id="cbf24-2243">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2243">6</span></span>

<span data-ttu-id="cbf24-2244">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2244">7</span></span>

<span data-ttu-id="cbf24-2245">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2245">8</span></span>

<span data-ttu-id="cbf24-2246">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2246">9</span></span>

<span data-ttu-id="cbf24-2247">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2247">3</span></span><br/> <span data-ttu-id="cbf24-2248">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2248">0</span></span><br/>

<span data-ttu-id="cbf24-2249">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2249">1</span></span>

<span data-ttu-id="cbf24-2250">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="cbf24-2250">\_hRegion</span></span>

<span data-ttu-id="cbf24-2251">\_cBookmarks</span><span class="sxs-lookup"><span data-stu-id="cbf24-2251">\_cBookmarks</span></span>

<span data-ttu-id="cbf24-2252">\_maxRet</span><span class="sxs-lookup"><span data-stu-id="cbf24-2252">\_maxRet</span></span>

<span data-ttu-id="cbf24-2253">\_cValidRet</span><span class="sxs-lookup"><span data-stu-id="cbf24-2253">\_cValidRet</span></span>

<span data-ttu-id="cbf24-2254">\_aBookmarks (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2254">\_aBookmarks (variable)</span></span>

<span data-ttu-id="cbf24-2255">\_ascRet (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2255">\_ascRet (variable)</span></span>



 

<span data-ttu-id="cbf24-2256">**\_ hRegion**: DEBE establecerse en 0x00000000 y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2256">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="cbf24-2257">**\_ cBookmarks:** entero de 32 bits sin signo que representa el número de elementos de \_ una matriz de aBookmarks.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2257">**\_cBookmarks**: Unsigned 32-bit integer representing the number of elements in \_aBookmarks array.</span></span>

<span data-ttu-id="cbf24-2258">**\_ maxRet:** entero de 32 bits sin signo que representa el número de elementos de la matriz \_ ascRet.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2258">**\_maxRet**: Unsigned 32-bit integer representing the number of elements in \_ascRet array.</span></span>

<span data-ttu-id="cbf24-2259">**\_ cValidRet:** entero de 32 bits sin signo que representa el número de elementos de la matriz \_ ascRet que son válidos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2259">**\_cValidRet**: Unsigned 32-bit integer representing the number of elements in the \_ascRet array which are valid.</span></span> <span data-ttu-id="cbf24-2260">Se han definido elementos válidos en la matriz, mientras que los elementos no válidos no están definidos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2260">Valid elements have been defined in the array, while invalid elements are undefined.</span></span>

<span data-ttu-id="cbf24-2261">**\_ aBookmarks:** matriz de identificadores de marcador (cada uno representado por 4 bytes), como se obtiene de un mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2261">**\_aBookmarks**: An array of bookmark handles (each represented by 4 bytes), as obtained from a CPMGetRowsOut message.</span></span>

<span data-ttu-id="cbf24-2262">**\_ ascRet:** matriz de valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2262">**\_ascRet**: An array of HRESULT values.</span></span> <span data-ttu-id="cbf24-2263">Cuando se envía CRowSeekByBookMark como parte de la solicitud CPMGetRowsIn, el número de entradas de la matriz DEBE ser igual a \_ cBookMarks.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2263">When the CRowSeekByBookMark is sent as part of the CPMGetRowsIn request, the number of entries in the array MUST be equal to \_cBookMarks.</span></span> <span data-ttu-id="cbf24-2264">Cuando el cliente los envía, los valores DEBEN establecerse en cero y el servidor DEBE omitir el contenido de la matriz.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2264">When sent by the client, the values MUST be set zero, and the server MUST ignore the contents of the array.</span></span> <span data-ttu-id="cbf24-2265">Cuando el servidor lo envía (como parte del mensaje CPMGetRowsOut), los valores de la matriz indican el estado del resultado de cada recuperación de fila.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2265">When sent by the server (as part of the CPMGetRowsOut message), the values in the array indicate the result status for each row retrieval.</span></span>

### <a name="22127-crowseeknext"></a><span data-ttu-id="cbf24-2266">2.2.1.27 CRowSeekNext</span><span class="sxs-lookup"><span data-stu-id="cbf24-2266">2.2.1.27 CRowSeekNext</span></span>

<span data-ttu-id="cbf24-2267">La estructura CRowSeekNext contiene el número de filas que se omitirán en un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2267">The CRowSeekNext structure contains the number of rows to skip in a CPMGetRowsIn message.</span></span>



<span data-ttu-id="cbf24-2268">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2268">0</span></span>

<span data-ttu-id="cbf24-2269">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2269">1</span></span>

<span data-ttu-id="cbf24-2270">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2270">2</span></span>

<span data-ttu-id="cbf24-2271">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2271">3</span></span>

<span data-ttu-id="cbf24-2272">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2272">4</span></span>

<span data-ttu-id="cbf24-2273">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2273">5</span></span>

<span data-ttu-id="cbf24-2274">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2274">6</span></span>

<span data-ttu-id="cbf24-2275">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2275">7</span></span>

<span data-ttu-id="cbf24-2276">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2276">8</span></span>

<span data-ttu-id="cbf24-2277">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2277">9</span></span>

<span data-ttu-id="cbf24-2278">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2278">1</span></span><br/> <span data-ttu-id="cbf24-2279">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2279">0</span></span><br/>

<span data-ttu-id="cbf24-2280">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2280">1</span></span>

<span data-ttu-id="cbf24-2281">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2281">2</span></span>

<span data-ttu-id="cbf24-2282">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2282">3</span></span>

<span data-ttu-id="cbf24-2283">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2283">4</span></span>

<span data-ttu-id="cbf24-2284">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2284">5</span></span>

<span data-ttu-id="cbf24-2285">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2285">6</span></span>

<span data-ttu-id="cbf24-2286">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2286">7</span></span>

<span data-ttu-id="cbf24-2287">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2287">8</span></span>

<span data-ttu-id="cbf24-2288">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2288">9</span></span>

<span data-ttu-id="cbf24-2289">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2289">2</span></span><br/> <span data-ttu-id="cbf24-2290">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2290">0</span></span><br/>

<span data-ttu-id="cbf24-2291">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2291">1</span></span>

<span data-ttu-id="cbf24-2292">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2292">2</span></span>

<span data-ttu-id="cbf24-2293">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2293">3</span></span>

<span data-ttu-id="cbf24-2294">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2294">4</span></span>

<span data-ttu-id="cbf24-2295">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2295">5</span></span>

<span data-ttu-id="cbf24-2296">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2296">6</span></span>

<span data-ttu-id="cbf24-2297">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2297">7</span></span>

<span data-ttu-id="cbf24-2298">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2298">8</span></span>

<span data-ttu-id="cbf24-2299">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2299">9</span></span>

<span data-ttu-id="cbf24-2300">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2300">3</span></span><br/> <span data-ttu-id="cbf24-2301">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2301">0</span></span><br/>

<span data-ttu-id="cbf24-2302">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2302">1</span></span>

<span data-ttu-id="cbf24-2303">CiTblChapt</span><span class="sxs-lookup"><span data-stu-id="cbf24-2303">CiTblChapt</span></span>

<span data-ttu-id="cbf24-2304">\_hRegion</span><span class="sxs-lookup"><span data-stu-id="cbf24-2304">\_hRegion</span></span>

<span data-ttu-id="cbf24-2305">\_cskip</span><span class="sxs-lookup"><span data-stu-id="cbf24-2305">\_cskip</span></span>



 

<span data-ttu-id="cbf24-2306">**CiTblChapt:** entero de 32 bits sin signo que especifica el capítulo del conjunto de filas del que se recuperarán las filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2306">**CiTblChapt**: Unsigned 32-bit integer specifying the rowset chapter from which to retrieve rows.</span></span>

<span data-ttu-id="cbf24-2307">**\_ hRegion**: DEBE establecerse en 0x00000000 y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2307">**\_hRegion**: MUST be set to 0x00000000, and MUST be ignored.</span></span>

<span data-ttu-id="cbf24-2308">**\_ cskip:** entero de 32 bits sin signo que representa el número de filas que se omitirán en el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2308">**\_cskip**: Unsigned 32-bit integer representing the number of rows to skip in the rowset.</span></span>

### <a name="22128-crowsetproperties"></a><span data-ttu-id="cbf24-2309">2.2.1.28 CRowsetProperties</span><span class="sxs-lookup"><span data-stu-id="cbf24-2309">2.2.1.28 CRowsetProperties</span></span>

<span data-ttu-id="cbf24-2310">La estructura CRowsetProperties contiene información de configuración para una consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2310">The CRowsetProperties structure contains configuration information for a query.</span></span>



<span data-ttu-id="cbf24-2311">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2311">0</span></span>

<span data-ttu-id="cbf24-2312">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2312">1</span></span>

<span data-ttu-id="cbf24-2313">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2313">2</span></span>

<span data-ttu-id="cbf24-2314">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2314">3</span></span>

<span data-ttu-id="cbf24-2315">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2315">4</span></span>

<span data-ttu-id="cbf24-2316">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2316">5</span></span>

<span data-ttu-id="cbf24-2317">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2317">6</span></span>

<span data-ttu-id="cbf24-2318">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2318">7</span></span>

<span data-ttu-id="cbf24-2319">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2319">8</span></span>

<span data-ttu-id="cbf24-2320">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2320">9</span></span>

<span data-ttu-id="cbf24-2321">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2321">1</span></span><br/> <span data-ttu-id="cbf24-2322">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2322">0</span></span><br/>

<span data-ttu-id="cbf24-2323">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2323">1</span></span>

<span data-ttu-id="cbf24-2324">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2324">2</span></span>

<span data-ttu-id="cbf24-2325">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2325">3</span></span>

<span data-ttu-id="cbf24-2326">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2326">4</span></span>

<span data-ttu-id="cbf24-2327">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2327">5</span></span>

<span data-ttu-id="cbf24-2328">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2328">6</span></span>

<span data-ttu-id="cbf24-2329">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2329">7</span></span>

<span data-ttu-id="cbf24-2330">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2330">8</span></span>

<span data-ttu-id="cbf24-2331">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2331">9</span></span>

<span data-ttu-id="cbf24-2332">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2332">2</span></span><br/> <span data-ttu-id="cbf24-2333">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2333">0</span></span><br/>

<span data-ttu-id="cbf24-2334">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2334">1</span></span>

<span data-ttu-id="cbf24-2335">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2335">2</span></span>

<span data-ttu-id="cbf24-2336">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2336">3</span></span>

<span data-ttu-id="cbf24-2337">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2337">4</span></span>

<span data-ttu-id="cbf24-2338">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2338">5</span></span>

<span data-ttu-id="cbf24-2339">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2339">6</span></span>

<span data-ttu-id="cbf24-2340">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2340">7</span></span>

<span data-ttu-id="cbf24-2341">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2341">8</span></span>

<span data-ttu-id="cbf24-2342">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2342">9</span></span>

<span data-ttu-id="cbf24-2343">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2343">3</span></span><br/> <span data-ttu-id="cbf24-2344">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2344">0</span></span><br/>

<span data-ttu-id="cbf24-2345">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2345">1</span></span>

<span data-ttu-id="cbf24-2346">\_uBooleanOptions</span><span class="sxs-lookup"><span data-stu-id="cbf24-2346">\_uBooleanOptions</span></span>

<span data-ttu-id="cbf24-2347">\_ulMaxOpenRows</span><span class="sxs-lookup"><span data-stu-id="cbf24-2347">\_ulMaxOpenRows</span></span>

<span data-ttu-id="cbf24-2348">\_ulMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="cbf24-2348">\_ulMemoryUsage</span></span>

<span data-ttu-id="cbf24-2349">\_cMaxResults</span><span class="sxs-lookup"><span data-stu-id="cbf24-2349">\_cMaxResults</span></span>

<span data-ttu-id="cbf24-2350">\_cCmdTimeout</span><span class="sxs-lookup"><span data-stu-id="cbf24-2350">\_cCmdTimeout</span></span>



 

<span data-ttu-id="cbf24-2351">**\_ uBooleanOptions:** los 3 bits menos significativos de este campo DEBEN contener uno de los tres valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="cbf24-2351">**\_uBooleanOptions**: The least significant 3 bits of this field MUST contain one of the following three values:</span></span>



| <span data-ttu-id="cbf24-2352">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-2352">Value</span></span>                  | <span data-ttu-id="cbf24-2353">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-2353">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cbf24-2354">eSequential 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-2354">eSequential 0x00000001</span></span> | <span data-ttu-id="cbf24-2355">El cursor solo se puede mover hacia delante.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2355">The cursor can only be moved forwards.</span></span>                              |
| <span data-ttu-id="cbf24-2356">eLocatable 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cbf24-2356">eLocatable 0x00000003</span></span>  | <span data-ttu-id="cbf24-2357">El cursor se puede mover a cualquier posición.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2357">The cursor can be moved to any position.</span></span>                            |
| <span data-ttu-id="cbf24-2358">eScrollable 0x00000007</span><span class="sxs-lookup"><span data-stu-id="cbf24-2358">eScrollable 0x00000007</span></span> | <span data-ttu-id="cbf24-2359">El cursor se puede mover a cualquier posición y capturar en cualquier dirección.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2359">The cursor can be moved to any position and fetch in any direction.</span></span> |



 

<span data-ttu-id="cbf24-2360">Los bits restantes pueden ser claros o establecerse en cualquier combinación de los siguientes valores de forma lógica o conjunta:</span><span class="sxs-lookup"><span data-stu-id="cbf24-2360">The remaining bits may either be clear, or set to any combination of the following values logically OR'd together:</span></span>



| <span data-ttu-id="cbf24-2361">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-2361">Value</span></span>                     | <span data-ttu-id="cbf24-2362">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-2362">Meaning</span></span>                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-2363">eAsynchronous 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cbf24-2363">eAsynchronous 0x00000008</span></span>  | <span data-ttu-id="cbf24-2364">El cliente no esperará a que finalice la ejecución.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2364">The client will not wait for execution completion.</span></span>                                                          |
| <span data-ttu-id="cbf24-2365">eFirstRows 0x00000080</span><span class="sxs-lookup"><span data-stu-id="cbf24-2365">eFirstRows 0x00000080</span></span>     | <span data-ttu-id="cbf24-2366">Devuelve las primeras filas encontradas, no las mejores coincidencias.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2366">Return the first rows encountered, not the best matches.</span></span>                                                    |
| <span data-ttu-id="cbf24-2367">eHoldRows 0x00000200</span><span class="sxs-lookup"><span data-stu-id="cbf24-2367">eHoldRows 0x00000200</span></span>      | <span data-ttu-id="cbf24-2368">El servidor NO DEBE descartar filas hasta que el cliente se realiza con una consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2368">The server MUST NOT discard rows until the client is done with a query.</span></span>                                     |
| <span data-ttu-id="cbf24-2369">eChaptered 0x00000800</span><span class="sxs-lookup"><span data-stu-id="cbf24-2369">eChaptered 0x00000800</span></span>     | <span data-ttu-id="cbf24-2370">El conjunto de filas admite capítulos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2370">The rowset supports chapters.</span></span>                                                                               |
| <span data-ttu-id="cbf24-2371">eUseCI 0x00001000</span><span class="sxs-lookup"><span data-stu-id="cbf24-2371">eUseCI 0x00001000</span></span>         | <span data-ttu-id="cbf24-2372">Responda solo a la consulta desde el índice, no desde el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2372">Only answer the query from the index, not the file system.</span></span>                                                  |
| <span data-ttu-id="cbf24-2373">eDeferTrimming 0x00002000</span><span class="sxs-lookup"><span data-stu-id="cbf24-2373">eDeferTrimming 0x00002000</span></span> | <span data-ttu-id="cbf24-2374">El servicio de indexación debe considerar la posibilidad de optimizar el tiempo de respuesta al cliente al realizar la eliminación de resultados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2374">The indexing service is to consider optimizing response time to the client when performing results removal.</span></span> |



 

<span data-ttu-id="cbf24-2375">**\_ ulMaxOpenRows:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2375">**\_ulMaxOpenRows**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="cbf24-2376">Debe establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2376">Must be set to 0x00000000.</span></span> <span data-ttu-id="cbf24-2377">No se usa y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2377">Not used and MUST be ignored.</span></span>

<span data-ttu-id="cbf24-2378">**\_ ulMemoryUsage:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2378">**\_ulMemoryUsage**: Unsigned 32-bit integer.</span></span> <span data-ttu-id="cbf24-2379">Debe establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2379">Must be set to 0x00000000.</span></span> <span data-ttu-id="cbf24-2380">No se usa y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2380">Not used and MUST be ignored.</span></span>

<span data-ttu-id="cbf24-2381">**\_ cMaxResults:** entero de 32 bits sin signo que especifica el número máximo de filas que se van a devolver para la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2381">**\_cMaxResults**: A 32-bit unsigned integer specifying the maximum number of rows that are to be returned for the query.</span></span>

<span data-ttu-id="cbf24-2382">**\_ cCmdTimeout:** entero de 32 bits sin signo, que especifica el número de segundos en los que se va a finalizar una consulta y finalizar automáticamente, contando desde el momento en que la consulta comienza a ejecutarse en el servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2382">**\_cCmdTimeout**: A 32-bit unsigned integer, specifying the number of seconds at which a query is to time out and automatically terminate, counting from the time the query starts executing on the server.</span></span> <span data-ttu-id="cbf24-2383">Un valor de 0x00000000 significa que la consulta no debe hacer tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2383">A value of 0x00000000 means that the query is not to time out.</span></span>

### <a name="22129-crowvariant"></a><span data-ttu-id="cbf24-2384">2.2.1.29 CRowVariant</span><span class="sxs-lookup"><span data-stu-id="cbf24-2384">2.2.1.29 CRowVariant</span></span>

<span data-ttu-id="cbf24-2385">La estructura CRowVariant contiene la parte de tamaño fijo de un tipo de datos de longitud variable almacenado en el mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2385">The CRowVariant structure contains the fixed-size portion of a variable length data type stored in the CPMGetRowsOut message.</span></span>



<span data-ttu-id="cbf24-2386">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2386">0</span></span>

<span data-ttu-id="cbf24-2387">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2387">1</span></span>

<span data-ttu-id="cbf24-2388">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2388">2</span></span>

<span data-ttu-id="cbf24-2389">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2389">3</span></span>

<span data-ttu-id="cbf24-2390">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2390">4</span></span>

<span data-ttu-id="cbf24-2391">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2391">5</span></span>

<span data-ttu-id="cbf24-2392">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2392">6</span></span>

<span data-ttu-id="cbf24-2393">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2393">7</span></span>

<span data-ttu-id="cbf24-2394">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2394">8</span></span>

<span data-ttu-id="cbf24-2395">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2395">9</span></span>

<span data-ttu-id="cbf24-2396">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2396">1</span></span><br/> <span data-ttu-id="cbf24-2397">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2397">0</span></span><br/>

<span data-ttu-id="cbf24-2398">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2398">1</span></span>

<span data-ttu-id="cbf24-2399">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2399">2</span></span>

<span data-ttu-id="cbf24-2400">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2400">3</span></span>

<span data-ttu-id="cbf24-2401">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2401">4</span></span>

<span data-ttu-id="cbf24-2402">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2402">5</span></span>

<span data-ttu-id="cbf24-2403">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2403">6</span></span>

<span data-ttu-id="cbf24-2404">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2404">7</span></span>

<span data-ttu-id="cbf24-2405">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2405">8</span></span>

<span data-ttu-id="cbf24-2406">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2406">9</span></span>

<span data-ttu-id="cbf24-2407">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2407">2</span></span><br/> <span data-ttu-id="cbf24-2408">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2408">0</span></span><br/>

<span data-ttu-id="cbf24-2409">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2409">1</span></span>

<span data-ttu-id="cbf24-2410">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2410">2</span></span>

<span data-ttu-id="cbf24-2411">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2411">3</span></span>

<span data-ttu-id="cbf24-2412">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2412">4</span></span>

<span data-ttu-id="cbf24-2413">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2413">5</span></span>

<span data-ttu-id="cbf24-2414">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2414">6</span></span>

<span data-ttu-id="cbf24-2415">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2415">7</span></span>

<span data-ttu-id="cbf24-2416">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2416">8</span></span>

<span data-ttu-id="cbf24-2417">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2417">9</span></span>

<span data-ttu-id="cbf24-2418">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2418">3</span></span><br/> <span data-ttu-id="cbf24-2419">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2419">0</span></span><br/>

<span data-ttu-id="cbf24-2420">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2420">1</span></span>

<span data-ttu-id="cbf24-2421">vType</span><span class="sxs-lookup"><span data-stu-id="cbf24-2421">vType</span></span>

<span data-ttu-id="cbf24-2422">reserved1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2422">reserved1</span></span>

<span data-ttu-id="cbf24-2423">reserved2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2423">reserved2</span></span>

<span data-ttu-id="cbf24-2424">Desplazamiento (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2424">Offset (optional)</span></span>



 

<span data-ttu-id="cbf24-2425">**vType:** un indicador de tipo que indica el tipo de vValue.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2425">**vType**: A type indicator, indicating the type of vValue.</span></span> <span data-ttu-id="cbf24-2426">DEBE ser uno de los valores VARENUM especificados en la sección 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2426">It MUST be one of the VARENUM values specified in section 2.2.1.1.</span></span>

<span data-ttu-id="cbf24-2427">**reserved1:** no se usa.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2427">**reserved1**: Not used.</span></span> <span data-ttu-id="cbf24-2428">El valor se puede establecer en cualquier valor arbitrario y DEBE omitirse al recibirse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2428">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="cbf24-2429">**reserved2:** no se usa.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2429">**reserved2**: Not used.</span></span> <span data-ttu-id="cbf24-2430">El valor se puede establecer en cualquier valor arbitrario y DEBE omitirse al recibirse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2430">The value can be set to any arbitrary value and it MUST be ignored on receipt.</span></span>

<span data-ttu-id="cbf24-2431">**Offset:** desplazamiento a datos de longitud variable (por ejemplo, una cadena).</span><span class="sxs-lookup"><span data-stu-id="cbf24-2431">**Offset**: An offset to variable length data (e.g. a string).</span></span>  <span data-ttu-id="cbf24-2432">Debe ser un valor de 32 bits (4 bytes de longitud) si se usan desplazamientos de 32 bits (según las reglas de la sección 2.2.3.16) o un valor de 64 bytes (8 bytes de longitud) si se usan desplazamientos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2432">This MUST be a 32-bit value (4 bytes long) if 32-bit offsets are being used (per the rules in section 2.2.3.16), or a 64-byte value (8 bytes long) if 64-bit offsets are being used.</span></span>

### <a name="22130-csortset"></a><span data-ttu-id="cbf24-2433">2.2.1.30 CSortSet</span><span class="sxs-lookup"><span data-stu-id="cbf24-2433">2.2.1.30 CSortSet</span></span>

<span data-ttu-id="cbf24-2434">La estructura CSortSet contiene el criterio de ordenación de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2434">The CSortSet structure contains the sort order of the query.</span></span>



<span data-ttu-id="cbf24-2435">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2435">0</span></span>

<span data-ttu-id="cbf24-2436">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2436">1</span></span>

<span data-ttu-id="cbf24-2437">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2437">2</span></span>

<span data-ttu-id="cbf24-2438">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2438">3</span></span>

<span data-ttu-id="cbf24-2439">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2439">4</span></span>

<span data-ttu-id="cbf24-2440">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2440">5</span></span>

<span data-ttu-id="cbf24-2441">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2441">6</span></span>

<span data-ttu-id="cbf24-2442">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2442">7</span></span>

<span data-ttu-id="cbf24-2443">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2443">8</span></span>

<span data-ttu-id="cbf24-2444">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2444">9</span></span>

<span data-ttu-id="cbf24-2445">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2445">1</span></span><br/> <span data-ttu-id="cbf24-2446">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2446">0</span></span><br/>

<span data-ttu-id="cbf24-2447">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2447">1</span></span>

<span data-ttu-id="cbf24-2448">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2448">2</span></span>

<span data-ttu-id="cbf24-2449">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2449">3</span></span>

<span data-ttu-id="cbf24-2450">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2450">4</span></span>

<span data-ttu-id="cbf24-2451">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2451">5</span></span>

<span data-ttu-id="cbf24-2452">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2452">6</span></span>

<span data-ttu-id="cbf24-2453">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2453">7</span></span>

<span data-ttu-id="cbf24-2454">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2454">8</span></span>

<span data-ttu-id="cbf24-2455">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2455">9</span></span>

<span data-ttu-id="cbf24-2456">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2456">2</span></span><br/> <span data-ttu-id="cbf24-2457">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2457">0</span></span><br/>

<span data-ttu-id="cbf24-2458">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2458">1</span></span>

<span data-ttu-id="cbf24-2459">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2459">2</span></span>

<span data-ttu-id="cbf24-2460">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2460">3</span></span>

<span data-ttu-id="cbf24-2461">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2461">4</span></span>

<span data-ttu-id="cbf24-2462">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2462">5</span></span>

<span data-ttu-id="cbf24-2463">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2463">6</span></span>

<span data-ttu-id="cbf24-2464">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2464">7</span></span>

<span data-ttu-id="cbf24-2465">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2465">8</span></span>

<span data-ttu-id="cbf24-2466">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2466">9</span></span>

<span data-ttu-id="cbf24-2467">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2467">3</span></span><br/> <span data-ttu-id="cbf24-2468">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2468">0</span></span><br/>

<span data-ttu-id="cbf24-2469">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2469">1</span></span>

<span data-ttu-id="cbf24-2470">Count</span><span class="sxs-lookup"><span data-stu-id="cbf24-2470">Count</span></span>

<span data-ttu-id="cbf24-2471">sortArray (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2471">sortArray (variable)</span></span>



 

<span data-ttu-id="cbf24-2472">**count:** entero de 32 bits sin signo que especifica el número de elementos en sortArray.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2472">**count**: A 32-bit unsigned integer specifying number of elements in sortArray.</span></span>

<span data-ttu-id="cbf24-2473">**sortArray:** matriz de estructuras de CSort que describen el orden en el que se ordenan los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2473">**sortArray**: An array of CSort structures describing the order in which to sort the results of the query.</span></span> <span data-ttu-id="cbf24-2474">Las estructuras de la matriz DEBEN estar separadas por 0 a 3 bytes de relleno, de forma que cada estructura tenga una alineación de 4 bytes desde el principio de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2474">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="cbf24-2475">Estos bytes de relleno pueden ser cualquier valor arbitrario y DEBEN omitirse al recibirse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2475">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22131-ctablecolumn"></a><span data-ttu-id="cbf24-2476">2.2.1.31 CTableColumn</span><span class="sxs-lookup"><span data-stu-id="cbf24-2476">2.2.1.31 CTableColumn</span></span>

<span data-ttu-id="cbf24-2477">La estructura CTableColumn contiene una columna de un mensaje CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-2477">The CTableColumn structure contains a column of a CPMSetBindingsIn message</span></span>



<span data-ttu-id="cbf24-2478">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2478">0</span></span>

<span data-ttu-id="cbf24-2479">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2479">1</span></span>

<span data-ttu-id="cbf24-2480">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2480">2</span></span>

<span data-ttu-id="cbf24-2481">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2481">3</span></span>

<span data-ttu-id="cbf24-2482">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2482">4</span></span>

<span data-ttu-id="cbf24-2483">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2483">5</span></span>

<span data-ttu-id="cbf24-2484">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2484">6</span></span>

<span data-ttu-id="cbf24-2485">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2485">7</span></span>

<span data-ttu-id="cbf24-2486">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2486">8</span></span>

<span data-ttu-id="cbf24-2487">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2487">9</span></span>

<span data-ttu-id="cbf24-2488">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2488">1</span></span><br/> <span data-ttu-id="cbf24-2489">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2489">0</span></span><br/>

<span data-ttu-id="cbf24-2490">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2490">1</span></span>

<span data-ttu-id="cbf24-2491">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2491">2</span></span>

<span data-ttu-id="cbf24-2492">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2492">3</span></span>

<span data-ttu-id="cbf24-2493">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2493">4</span></span>

<span data-ttu-id="cbf24-2494">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2494">5</span></span>

<span data-ttu-id="cbf24-2495">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2495">6</span></span>

<span data-ttu-id="cbf24-2496">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2496">7</span></span>

<span data-ttu-id="cbf24-2497">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2497">8</span></span>

<span data-ttu-id="cbf24-2498">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2498">9</span></span>

<span data-ttu-id="cbf24-2499">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2499">2</span></span><br/> <span data-ttu-id="cbf24-2500">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2500">0</span></span><br/>

<span data-ttu-id="cbf24-2501">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2501">1</span></span>

<span data-ttu-id="cbf24-2502">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2502">2</span></span>

<span data-ttu-id="cbf24-2503">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2503">3</span></span>

<span data-ttu-id="cbf24-2504">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2504">4</span></span>

<span data-ttu-id="cbf24-2505">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2505">5</span></span>

<span data-ttu-id="cbf24-2506">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2506">6</span></span>

<span data-ttu-id="cbf24-2507">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2507">7</span></span>

<span data-ttu-id="cbf24-2508">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2508">8</span></span>

<span data-ttu-id="cbf24-2509">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2509">9</span></span>

<span data-ttu-id="cbf24-2510">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2510">3</span></span><br/> <span data-ttu-id="cbf24-2511">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2511">0</span></span><br/>

<span data-ttu-id="cbf24-2512">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2512">1</span></span>

<span data-ttu-id="cbf24-2513">PropSpec</span><span class="sxs-lookup"><span data-stu-id="cbf24-2513">PropSpec</span></span>

<span data-ttu-id="cbf24-2514">... (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2514">...(variable)</span></span>

<span data-ttu-id="cbf24-2515">vType</span><span class="sxs-lookup"><span data-stu-id="cbf24-2515">vType</span></span>

<span data-ttu-id="cbf24-2516">ValueUsed</span><span class="sxs-lookup"><span data-stu-id="cbf24-2516">ValueUsed</span></span>

<span data-ttu-id="cbf24-2517">\_padding1 (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2517">\_padding1 (optional)</span></span>

<span data-ttu-id="cbf24-2518">ValueOffset (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2518">ValueOffset (optional)</span></span>

<span data-ttu-id="cbf24-2519">ValueSize (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2519">ValueSize (optional)</span></span>

<span data-ttu-id="cbf24-2520">StatusUsed</span><span class="sxs-lookup"><span data-stu-id="cbf24-2520">StatusUsed</span></span>

<span data-ttu-id="cbf24-2521">\_padding2 (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2521">\_padding2 (optional)</span></span>

<span data-ttu-id="cbf24-2522">StatusOffset (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2522">StatusOffset (optional)</span></span>

<span data-ttu-id="cbf24-2523">LengthUsed</span><span class="sxs-lookup"><span data-stu-id="cbf24-2523">LengthUsed</span></span>

<span data-ttu-id="cbf24-2524">\_padding3 (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2524">\_padding3 (optional)</span></span>

<span data-ttu-id="cbf24-2525">LengthOffset (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2525">LengthOffset (optional)</span></span>



 

<span data-ttu-id="cbf24-2526">**PropSpec:** una estructura CFullPropSpec tal como se especifica en la sección 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2526">**PropSpec**: A CFullPropSpec structure as specified in Section 2.2.1.3.</span></span>

<span data-ttu-id="cbf24-2527">**vType:** especifica el tipo de valor de datos contenido en la columna.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2527">**vType**: Specifies the type of data value contained in the column.</span></span> <span data-ttu-id="cbf24-2528">Consulte el campo vType de la sección 2.2.1.1 para obtener la lista de valores de este campo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2528">See the vType field in Section 2.2.1.1 for the list of values for this field.</span></span>

<span data-ttu-id="cbf24-2529">**ValueUsed:** campo de un byte que DEBE establecerse en 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2529">**ValueUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="cbf24-2530">Si se establece en 0x01, la columna se transfiere dentro de la fila de tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2530">If set to 0x01, the column is transferred within the fixed size row.</span></span> <span data-ttu-id="cbf24-2531">Si se establece en 0x00, el valor de la columna se transfiere en la sección de longitud variable al final del búfer.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2531">If set to 0x00, the value of the column is transferred in the variable-length section at the end of the buffer.</span></span>

<span data-ttu-id="cbf24-2532">**\_ padding1:** campo de un byte que SE DEBE insertar antes de ValueOffset si, sin él, ValueOffset no comenzaría con un desplazamiento par desde el principio del mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2532">**\_padding1**: A one byte field that MUST be inserted before ValueOffset if, without it, ValueOffset would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="cbf24-2533">El valor de este byte es arbitrario y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2533">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="cbf24-2534">Si ValueUsed está establecido en 0x00, este campo NO DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2534">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="cbf24-2535">**ValueOffset:** entero de 2 bytes sin signo que especifica el desplazamiento del valor de columna de la fila.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2535">**ValueOffset**: An unsigned 2-byte integer specifying the offset of the column value in the row.</span></span> <span data-ttu-id="cbf24-2536">Si ValueUsed está establecido en 0x00, este campo NO DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2536">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="cbf24-2537">**ValueSize:** entero de 2 bytes sin signo que especifica el tamaño del valor de columna en bytes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2537">**ValueSize**: An unsigned 2-byte integer specifying the size of the column value in bytes.</span></span> <span data-ttu-id="cbf24-2538">Si ValueUsed está establecido en 0x00, este campo NO DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2538">If ValueUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="cbf24-2539">**StatusUsed:** campo de un byte que DEBE establecerse en 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2539">**StatusUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="cbf24-2540">Si se establece en 0x01, el estado de la columna se transfiere dentro de la fila.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2540">If set to 0x01, the status of the column is transferred within the row.</span></span> <span data-ttu-id="cbf24-2541">Si 0x00, el estado de la columna no se transfiere dentro de la fila.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2541">If 0x00, the status of the column is not transferred within the row.</span></span>

<span data-ttu-id="cbf24-2542">**\_ padding2:** campo de un byte que SE DEBE insertar antes de StatusOffset si, sin él, el campo StatusOffset no comenzaría con un desplazamiento par desde el principio del mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2542">**\_padding2**: A one byte field that MUST be inserted before StatusOffset if, without it,the StatusOffset field would not begin at an even offset from the beginning of the message.</span></span> <span data-ttu-id="cbf24-2543">El valor de este byte es arbitrario y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2543">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="cbf24-2544">Si StatusUsed está establecido en 0x00, este campo NO DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2544">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="cbf24-2545">**StatusOffset:** entero de 2 bytes sin signo que especifica el desplazamiento del estado de la columna en la fila.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2545">**StatusOffset**: An unsigned 2-byte integer specifying the offset of the column status in the row.</span></span> <span data-ttu-id="cbf24-2546">Si StatusUsed está establecido en 0x00, este campo NO DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2546">If StatusUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="cbf24-2547">**LengthUsed:** campo de un byte que DEBE establecerse en 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2547">**LengthUsed**: A one byte field that MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="cbf24-2548">Si se establece en 0x01, la longitud de la columna se transfiere dentro de la fila.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2548">If set to 0x01, the length of the column is transferred within the row.</span></span> <span data-ttu-id="cbf24-2549">Si 0x00, la longitud de la columna NO SE DEBE transferir dentro de la fila.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2549">If 0x00, the length of the column MUST NOT be transferred within the row.</span></span>

<span data-ttu-id="cbf24-2550">**\_ padding3:** campo de un byte que SE DEBE insertar antes de LengthOffset si, sin él, LengthOffset no comenzaría con un desplazamiento par desde el principio de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2550">**\_padding3**: A one byte field which MUST be inserted before LengthOffset if, without it, LengthOffset would not begin at an even offset from the beginning of a message.</span></span> <span data-ttu-id="cbf24-2551">El valor de este byte es arbitrario y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2551">The value of this byte is arbitrary and MUST be ignored.</span></span> <span data-ttu-id="cbf24-2552">Si LengthUsed está establecido en 0x00, este campo NO DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2552">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

<span data-ttu-id="cbf24-2553">**LengthOffset:** entero de 2 bytes sin signo que especifica el desplazamiento de la longitud de columna de la fila.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2553">**LengthOffset**: An unsigned 2-byte integer specifying the offset of the column length in the row.</span></span> <span data-ttu-id="cbf24-2554">Si LengthUsed está establecido en 0x00, este campo NO DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2554">If LengthUsed is set to 0x00, this field MUST NOT be present.</span></span>

### <a name="22132-serializedpropertyvalue"></a><span data-ttu-id="cbf24-2555">2.2.1.32 SERIALIZEDPROPERTYVALUE</span><span class="sxs-lookup"><span data-stu-id="cbf24-2555">2.2.1.32 SERIALIZEDPROPERTYVALUE</span></span>

<span data-ttu-id="cbf24-2556">La estructura SERIALIZEDPROPERTYVALUE contiene un valor serializado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2556">The SERIALIZEDPROPERTYVALUE structure contains a serialized value.</span></span>



<span data-ttu-id="cbf24-2557">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2557">0</span></span>

<span data-ttu-id="cbf24-2558">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2558">1</span></span>

<span data-ttu-id="cbf24-2559">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2559">2</span></span>

<span data-ttu-id="cbf24-2560">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2560">3</span></span>

<span data-ttu-id="cbf24-2561">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2561">4</span></span>

<span data-ttu-id="cbf24-2562">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2562">5</span></span>

<span data-ttu-id="cbf24-2563">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2563">6</span></span>

<span data-ttu-id="cbf24-2564">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2564">7</span></span>

<span data-ttu-id="cbf24-2565">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2565">8</span></span>

<span data-ttu-id="cbf24-2566">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2566">9</span></span>

<span data-ttu-id="cbf24-2567">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2567">1</span></span><br/> <span data-ttu-id="cbf24-2568">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2568">0</span></span><br/>

<span data-ttu-id="cbf24-2569">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2569">1</span></span>

<span data-ttu-id="cbf24-2570">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2570">2</span></span>

<span data-ttu-id="cbf24-2571">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2571">3</span></span>

<span data-ttu-id="cbf24-2572">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2572">4</span></span>

<span data-ttu-id="cbf24-2573">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2573">5</span></span>

<span data-ttu-id="cbf24-2574">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2574">6</span></span>

<span data-ttu-id="cbf24-2575">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2575">7</span></span>

<span data-ttu-id="cbf24-2576">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2576">8</span></span>

<span data-ttu-id="cbf24-2577">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2577">9</span></span>

<span data-ttu-id="cbf24-2578">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2578">2</span></span><br/> <span data-ttu-id="cbf24-2579">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2579">0</span></span><br/>

<span data-ttu-id="cbf24-2580">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2580">1</span></span>

<span data-ttu-id="cbf24-2581">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2581">2</span></span>

<span data-ttu-id="cbf24-2582">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2582">3</span></span>

<span data-ttu-id="cbf24-2583">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2583">4</span></span>

<span data-ttu-id="cbf24-2584">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2584">5</span></span>

<span data-ttu-id="cbf24-2585">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2585">6</span></span>

<span data-ttu-id="cbf24-2586">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2586">7</span></span>

<span data-ttu-id="cbf24-2587">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2587">8</span></span>

<span data-ttu-id="cbf24-2588">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2588">9</span></span>

<span data-ttu-id="cbf24-2589">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2589">3</span></span><br/> <span data-ttu-id="cbf24-2590">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2590">0</span></span><br/>

<span data-ttu-id="cbf24-2591">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2591">1</span></span>

<span data-ttu-id="cbf24-2592">dwType</span><span class="sxs-lookup"><span data-stu-id="cbf24-2592">dwType</span></span>

<span data-ttu-id="cbf24-2593">rgb (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2593">rgb (variable)</span></span>



 

<span data-ttu-id="cbf24-2594">**dwType:** uno de los tipos de variante, definidos en la sección 2.2.1.1, que se puede combinar con modificadores de tipo variant.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2594">**dwType**: One of the variant types, defined in section 2.2.1.1, which can be combined with variant type modifiers.</span></span> <span data-ttu-id="cbf24-2595">Para todos los tipos de variante, excepto los combinados con VT ARRAY, SERIALIZEDPROPERTYVALUE tiene el mismo diseño que CBaseStorageVariant, tal como se especifica en la sección \_ 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2595">For all variant types, except those combined with VT\_ARRAY, SERIALIZEDPROPERTYVALUE has the same layout as CBaseStorageVariant, as specified in Section 2.2.1.1.</span></span> <span data-ttu-id="cbf24-2596">Si el tipo de variante se combina con el modificador de tipo VT ARRAY, se usa SAFEARRAY2, especificado en la sección \_ 2.2.1.2.1.1, en lugar de SAFEARRAY en el campo vValue de CBaseStorageVariant.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2596">If the variant type is combined with the VT\_ARRAY type modifier, then SAFEARRAY2, specified in Section 2.2.1.2.1.1, is used instead of SAFEARRAY in CBaseStorageVariant's vValue field.</span></span>

<span data-ttu-id="cbf24-2597">**rgb:** valor serializado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2597">**rgb**: Serialized value.</span></span> <span data-ttu-id="cbf24-2598">Vea los detalles de serialización de vValue en 2.2.1.1.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2598">See details of serialization for vValue in 2.2.1.1.</span></span>

### <a name="222-message-headers"></a><span data-ttu-id="cbf24-2599">2.2.2 Encabezados de mensaje</span><span class="sxs-lookup"><span data-stu-id="cbf24-2599">2.2.2 Message Headers</span></span>

<span data-ttu-id="cbf24-2600">Todos los mensajes de Content Indexing Service Protocol tienen un encabezado de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2600">All Content Indexing Service Protocol messages have a 16 byte header.</span></span>

<span data-ttu-id="cbf24-2601">A continuación se muestra un diagrama que muestra el formato de encabezado de mensaje del Protocolo de indexación de contenido.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2601">Below is a diagram showing the Content Indexing Service Protocol message header format.</span></span>



<span data-ttu-id="cbf24-2602">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2602">0</span></span>

<span data-ttu-id="cbf24-2603">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2603">1</span></span>

<span data-ttu-id="cbf24-2604">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2604">2</span></span>

<span data-ttu-id="cbf24-2605">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2605">3</span></span>

<span data-ttu-id="cbf24-2606">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2606">4</span></span>

<span data-ttu-id="cbf24-2607">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2607">5</span></span>

<span data-ttu-id="cbf24-2608">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2608">6</span></span>

<span data-ttu-id="cbf24-2609">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2609">7</span></span>

<span data-ttu-id="cbf24-2610">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2610">8</span></span>

<span data-ttu-id="cbf24-2611">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2611">9</span></span>

<span data-ttu-id="cbf24-2612">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2612">1</span></span><br/> <span data-ttu-id="cbf24-2613">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2613">0</span></span><br/>

<span data-ttu-id="cbf24-2614">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2614">1</span></span>

<span data-ttu-id="cbf24-2615">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2615">2</span></span>

<span data-ttu-id="cbf24-2616">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2616">3</span></span>

<span data-ttu-id="cbf24-2617">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2617">4</span></span>

<span data-ttu-id="cbf24-2618">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2618">5</span></span>

<span data-ttu-id="cbf24-2619">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2619">6</span></span>

<span data-ttu-id="cbf24-2620">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2620">7</span></span>

<span data-ttu-id="cbf24-2621">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2621">8</span></span>

<span data-ttu-id="cbf24-2622">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2622">9</span></span>

<span data-ttu-id="cbf24-2623">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2623">2</span></span><br/> <span data-ttu-id="cbf24-2624">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2624">0</span></span><br/>

<span data-ttu-id="cbf24-2625">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2625">1</span></span>

<span data-ttu-id="cbf24-2626">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2626">2</span></span>

<span data-ttu-id="cbf24-2627">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2627">3</span></span>

<span data-ttu-id="cbf24-2628">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2628">4</span></span>

<span data-ttu-id="cbf24-2629">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2629">5</span></span>

<span data-ttu-id="cbf24-2630">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2630">6</span></span>

<span data-ttu-id="cbf24-2631">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2631">7</span></span>

<span data-ttu-id="cbf24-2632">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2632">8</span></span>

<span data-ttu-id="cbf24-2633">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2633">9</span></span>

<span data-ttu-id="cbf24-2634">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2634">3</span></span><br/> <span data-ttu-id="cbf24-2635">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2635">0</span></span><br/>

<span data-ttu-id="cbf24-2636">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2636">1</span></span>

<span data-ttu-id="cbf24-2637">\_msg</span><span class="sxs-lookup"><span data-stu-id="cbf24-2637">\_msg</span></span>

<span data-ttu-id="cbf24-2638">\_Estado</span><span class="sxs-lookup"><span data-stu-id="cbf24-2638">\_status</span></span>

<span data-ttu-id="cbf24-2639">\_ulChecksum</span><span class="sxs-lookup"><span data-stu-id="cbf24-2639">\_ulChecksum</span></span>

<span data-ttu-id="cbf24-2640">\_ulReserved2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2640">\_ulReserved2</span></span>



 

<span data-ttu-id="cbf24-2641">\_**msg:** entero de 32 bits que identifica el tipo de mensaje que sigue al encabezado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2641">\_**msg**: A 32 bit integer that identifies the type of message following the header.</span></span> <span data-ttu-id="cbf24-2642">En la tabla siguiente se enumeran los mensajes del Protocolo de servicio de indexación de contenido y los valores enteros especificados para cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2642">The following table lists the Content Indexing Service Protocol messages and the integer values specified for each message.</span></span> <span data-ttu-id="cbf24-2643">Como se muestra en la tabla, algunos valores identifican dos mensajes en la tabla.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2643">As shown in the table, some values identify 2 messages in the table.</span></span> <span data-ttu-id="cbf24-2644">En esos casos, el mensaje que sigue al encabezado se puede identificar por la dirección del flujo de mensajes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2644">In those instances the message following the header can be identified by the direction of the message flow.</span></span> <span data-ttu-id="cbf24-2645">Si la dirección es cliente a servidor, se indica el mensaje con "In" anexado al nombre del mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2645">If the direction is client to server, the message with "In" appended to the message name is indicated.</span></span> <span data-ttu-id="cbf24-2646">Si la dirección es de servidor a cliente, se indica el mensaje con "Out" anexado al nombre del mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2646">If the direction is server to client, the message with "Out" appended to the message name is indicated.</span></span>



| <span data-ttu-id="cbf24-2647">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-2647">Value</span></span>      | <span data-ttu-id="cbf24-2648">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-2648">Meaning</span></span>                                                     |
|------------|-------------------------------------------------------------|
| <span data-ttu-id="cbf24-2649">0x000000C8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2649">0x000000C8</span></span> | <span data-ttu-id="cbf24-2650">CPMConnectIn o CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-2650">CPMConnectIn or CPMConnectOut</span></span>                               |
| <span data-ttu-id="cbf24-2651">0x000000C9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2651">0x000000C9</span></span> | <span data-ttu-id="cbf24-2652">CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="cbf24-2652">CPMDisconnect</span></span>                                               |
| <span data-ttu-id="cbf24-2653">0x000000CA</span><span class="sxs-lookup"><span data-stu-id="cbf24-2653">0x000000CA</span></span> | <span data-ttu-id="cbf24-2654">CPMCreateQueryIn o CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-2654">CPMCreateQueryIn or CPMCreateQueryOut</span></span>                       |
| <span data-ttu-id="cbf24-2655">0x000000CB</span><span class="sxs-lookup"><span data-stu-id="cbf24-2655">0x000000CB</span></span> | <span data-ttu-id="cbf24-2656">CPMFreeCursorIn o CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-2656">CPMFreeCursorIn or CPMFreeCursorOut</span></span>                         |
| <span data-ttu-id="cbf24-2657">0x000000CC</span><span class="sxs-lookup"><span data-stu-id="cbf24-2657">0x000000CC</span></span> | <span data-ttu-id="cbf24-2658">CPMGetRowsIn o CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-2658">CPMGetRowsIn or CPMGetRowsOut</span></span>                               |
| <span data-ttu-id="cbf24-2659">0x000000CD</span><span class="sxs-lookup"><span data-stu-id="cbf24-2659">0x000000CD</span></span> | <span data-ttu-id="cbf24-2660">CPMRatioFinishedIn o CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-2660">CPMRatioFinishedIn or CPMRatioFinishedOut</span></span>                   |
| <span data-ttu-id="cbf24-2661">0x000000CE</span><span class="sxs-lookup"><span data-stu-id="cbf24-2661">0x000000CE</span></span> | <span data-ttu-id="cbf24-2662">CPMCompareBmkIn o CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-2662">CPMCompareBmkIn or CPMCompareBmkOut</span></span>                         |
| <span data-ttu-id="cbf24-2663">0x000000CF</span><span class="sxs-lookup"><span data-stu-id="cbf24-2663">0x000000CF</span></span> | <span data-ttu-id="cbf24-2664">CPMGetApproximatePositionIn o CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-2664">CPMGetApproximatePositionIn or CPMGetApproximatePositionOut</span></span> |
| <span data-ttu-id="cbf24-2665">0x000000D0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2665">0x000000D0</span></span> | <span data-ttu-id="cbf24-2666">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-2666">CPMSetBindingsIn</span></span>                                            |
| <span data-ttu-id="cbf24-2667">0x000000D1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2667">0x000000D1</span></span> | <span data-ttu-id="cbf24-2668">CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="cbf24-2668">CPMGetNotify</span></span>                                                |
| <span data-ttu-id="cbf24-2669">0x000000D2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2669">0x000000D2</span></span> | <span data-ttu-id="cbf24-2670">CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-2670">CPMSendNotifyOut</span></span>                                            |
| <span data-ttu-id="cbf24-2671">0x000000D7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2671">0x000000D7</span></span> | <span data-ttu-id="cbf24-2672">CPMGetQueryStatusIn o CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-2672">CPMGetQueryStatusIn or CPMGetQueryStatusOut</span></span>                 |
| <span data-ttu-id="cbf24-2673">0x000000D9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2673">0x000000D9</span></span> | <span data-ttu-id="cbf24-2674">CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-2674">CPMCiStateInOut</span></span>                                             |
| <span data-ttu-id="cbf24-2675">0x000000E1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2675">0x000000E1</span></span> | <span data-ttu-id="cbf24-2676">CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-2676">CPMForceMergeIn</span></span>                                             |
| <span data-ttu-id="cbf24-2677">0x000000E4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2677">0x000000E4</span></span> | <span data-ttu-id="cbf24-2678">CPMFetchValueIn o CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-2678">CPMFetchValueIn or CPMFetchValueOut</span></span>                         |
| <span data-ttu-id="cbf24-2679">0x000000E6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2679">0x000000E6</span></span> | <span data-ttu-id="cbf24-2680">CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-2680">CPMUpdateDocumentsIn</span></span>                                        |
| <span data-ttu-id="cbf24-2681">0x000000E7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2681">0x000000E7</span></span> | <span data-ttu-id="cbf24-2682">CPMGetQueryStatusExIn o PMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-2682">CPMGetQueryStatusExIn or PMGetQueryStatusExOut</span></span>              |
| <span data-ttu-id="cbf24-2683">0x000000E8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2683">0x000000E8</span></span> | <span data-ttu-id="cbf24-2684">CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-2684">CPMRestartPositionIn</span></span>                                        |
| <span data-ttu-id="cbf24-2685">0x000000E9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2685">0x000000E9</span></span> | <span data-ttu-id="cbf24-2686">CPMStopAsynchIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-2686">CPMStopAsynchIn</span></span>                                             |
| <span data-ttu-id="cbf24-2687">0x000000EC</span><span class="sxs-lookup"><span data-stu-id="cbf24-2687">0x000000EC</span></span> | <span data-ttu-id="cbf24-2688">CPMSetCatStateIn o CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-2688">CPMSetCatStateIn or CPMSetCatStateOut</span></span>                       |



 

<span data-ttu-id="cbf24-2689">\_**status:** HRESULT \[ MS-SYS \] , que indica el estado de la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2689">\_**status**: An HRESULT \[MS-SYS\], indicating the status of the requested operation.</span></span>

\* *

<span data-ttu-id="cbf24-2690">*Comportamiento de Windows: el cliente siempre establece el \_ campo de estado en 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="cbf24-2690">*Windows Behavior: The client always sets the \_status field to 0x00000000.*</span></span>

<span data-ttu-id="cbf24-2691">**\_ ulChecksum:** ulChecksum DEBE calcularse según lo especificado en la sección \_ 3.2.4 para los mensajes siguientes:</span><span class="sxs-lookup"><span data-stu-id="cbf24-2691">**\_ulChecksum**: The \_ulChecksum MUST be calculated as specified in Section 3.2.4 for the following messages:</span></span>

-   <span data-ttu-id="cbf24-2692">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-2692">CPMConnectIn</span></span>
-   <span data-ttu-id="cbf24-2693">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-2693">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="cbf24-2694">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-2694">CPMSetBindingsIn</span></span>
-   <span data-ttu-id="cbf24-2695">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-2695">CPMGetRowsIn</span></span>
-   <span data-ttu-id="cbf24-2696">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-2696">CPMFetchValueIn</span></span>

<span data-ttu-id="cbf24-2697">Para todos los demás mensajes, \_ ulChecksum DEBE establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2697">For all other messages, \_ulChecksum MUST be set to 0x00000000.</span></span> <span data-ttu-id="cbf24-2698">Un cliente DEBE omitir el \_ campo ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2698">A client MUST ignore the\_ulChecksum field.</span></span>

<span data-ttu-id="cbf24-2699">**\_ ulReserved2:** DEBE establecerse en 0 y el receptor debe omitirlo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2699">**\_ulReserved2**: MUST be set to 0, and ignored by the receiver.</span></span>

### <a name="223-messages"></a><span data-ttu-id="cbf24-2700">2.2.3 Mensajes</span><span class="sxs-lookup"><span data-stu-id="cbf24-2700">2.2.3 Messages</span></span>

### <a name="2231-cpmcistateinout"></a><span data-ttu-id="cbf24-2701">2.2.3.1 CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-2701">2.2.3.1 CPMCiStateInOut</span></span>

<span data-ttu-id="cbf24-2702">El mensaje CPMCiStateInOut contiene información sobre el estado del servicio de indexación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2702">The CPMCiStateInOut message contains information about the state of the indexing service.</span></span> <span data-ttu-id="cbf24-2703">El formato del mensaje CPMCiStateInOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-2703">The format of the CPMCiStateInOut message that follows the header is:</span></span>



<span data-ttu-id="cbf24-2704">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2704">0</span></span>

<span data-ttu-id="cbf24-2705">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2705">1</span></span>

<span data-ttu-id="cbf24-2706">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2706">2</span></span>

<span data-ttu-id="cbf24-2707">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2707">3</span></span>

<span data-ttu-id="cbf24-2708">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2708">4</span></span>

<span data-ttu-id="cbf24-2709">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2709">5</span></span>

<span data-ttu-id="cbf24-2710">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2710">6</span></span>

<span data-ttu-id="cbf24-2711">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2711">7</span></span>

<span data-ttu-id="cbf24-2712">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2712">8</span></span>

<span data-ttu-id="cbf24-2713">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2713">9</span></span>

<span data-ttu-id="cbf24-2714">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2714">1</span></span><br/> <span data-ttu-id="cbf24-2715">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2715">0</span></span><br/>

<span data-ttu-id="cbf24-2716">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2716">1</span></span>

<span data-ttu-id="cbf24-2717">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2717">2</span></span>

<span data-ttu-id="cbf24-2718">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2718">3</span></span>

<span data-ttu-id="cbf24-2719">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2719">4</span></span>

<span data-ttu-id="cbf24-2720">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2720">5</span></span>

<span data-ttu-id="cbf24-2721">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2721">6</span></span>

<span data-ttu-id="cbf24-2722">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2722">7</span></span>

<span data-ttu-id="cbf24-2723">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2723">8</span></span>

<span data-ttu-id="cbf24-2724">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2724">9</span></span>

<span data-ttu-id="cbf24-2725">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2725">2</span></span><br/> <span data-ttu-id="cbf24-2726">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2726">0</span></span><br/>

<span data-ttu-id="cbf24-2727">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2727">1</span></span>

<span data-ttu-id="cbf24-2728">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2728">2</span></span>

<span data-ttu-id="cbf24-2729">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2729">3</span></span>

<span data-ttu-id="cbf24-2730">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2730">4</span></span>

<span data-ttu-id="cbf24-2731">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2731">5</span></span>

<span data-ttu-id="cbf24-2732">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2732">6</span></span>

<span data-ttu-id="cbf24-2733">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2733">7</span></span>

<span data-ttu-id="cbf24-2734">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2734">8</span></span>

<span data-ttu-id="cbf24-2735">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2735">9</span></span>

<span data-ttu-id="cbf24-2736">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2736">3</span></span><br/> <span data-ttu-id="cbf24-2737">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2737">0</span></span><br/>

<span data-ttu-id="cbf24-2738">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2738">1</span></span>

<span data-ttu-id="cbf24-2739">cbStruct</span><span class="sxs-lookup"><span data-stu-id="cbf24-2739">cbStruct</span></span>

<span data-ttu-id="cbf24-2740">cWordList</span><span class="sxs-lookup"><span data-stu-id="cbf24-2740">cWordList</span></span>

<span data-ttu-id="cbf24-2741">cPersistentIndex</span><span class="sxs-lookup"><span data-stu-id="cbf24-2741">cPersistentIndex</span></span>

<span data-ttu-id="cbf24-2742">cQueries</span><span class="sxs-lookup"><span data-stu-id="cbf24-2742">cQueries</span></span>

<span data-ttu-id="cbf24-2743">cDocuments</span><span class="sxs-lookup"><span data-stu-id="cbf24-2743">cDocuments</span></span>

<span data-ttu-id="cbf24-2744">cFreshTest</span><span class="sxs-lookup"><span data-stu-id="cbf24-2744">cFreshTest</span></span>

<span data-ttu-id="cbf24-2745">dwMergeProgress</span><span class="sxs-lookup"><span data-stu-id="cbf24-2745">dwMergeProgress</span></span>

<span data-ttu-id="cbf24-2746">eState</span><span class="sxs-lookup"><span data-stu-id="cbf24-2746">eState</span></span>

<span data-ttu-id="cbf24-2747">cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="cbf24-2747">cFilteredDocuments</span></span>

<span data-ttu-id="cbf24-2748">cTotalDocuments</span><span class="sxs-lookup"><span data-stu-id="cbf24-2748">cTotalDocuments</span></span>

<span data-ttu-id="cbf24-2749">cPendingScans</span><span class="sxs-lookup"><span data-stu-id="cbf24-2749">cPendingScans</span></span>

<span data-ttu-id="cbf24-2750">dwIndexSize</span><span class="sxs-lookup"><span data-stu-id="cbf24-2750">dwIndexSize</span></span>

<span data-ttu-id="cbf24-2751">cUniqueKeys</span><span class="sxs-lookup"><span data-stu-id="cbf24-2751">cUniqueKeys</span></span>

<span data-ttu-id="cbf24-2752">cSecQDocuments</span><span class="sxs-lookup"><span data-stu-id="cbf24-2752">cSecQDocuments</span></span>

<span data-ttu-id="cbf24-2753">dwPropCacheSize</span><span class="sxs-lookup"><span data-stu-id="cbf24-2753">dwPropCacheSize</span></span>



 

<span data-ttu-id="cbf24-2754">**cbStruct:** entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2754">**cbStruct**: A 32-bit unsigned integer.</span></span> <span data-ttu-id="cbf24-2755">Tamaño en bytes de este mensaje (excepto el encabezado común).</span><span class="sxs-lookup"><span data-stu-id="cbf24-2755">The size in bytes of this message (excluding the common header).</span></span> <span data-ttu-id="cbf24-2756">DEBE establecerse en 0x0000003C.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2756">MUST be set to 0x0000003C.</span></span>

<span data-ttu-id="cbf24-2757">**cWordList:** entero de 32 bits sin signo que indica el recuento de índices iniciales creados para documentos indexados recientemente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2757">**cWordList**: A 32-bit unsigned integer indicating the count of initial indexes created for recently indexed documents.</span></span>

<span data-ttu-id="cbf24-2758">**cPersistentIndex:** entero de 32 bits sin signo que indica el recuento de índices persistentes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2758">**cPersistentIndex**: A 32-bit unsigned integer indicating the count of persistent indexes.</span></span>

<span data-ttu-id="cbf24-2759">**cQueries:** entero de 32 bits sin signo que indica un número de consultas que se ejecutan activamente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2759">**cQueries**: A 32-bit unsigned integer indicating a number of actively running queries.</span></span>

<span data-ttu-id="cbf24-2760">**cDocuments:** entero de 32 bits sin signo que indica el número total de documentos que esperan ser indexados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2760">**cDocuments**: A 32-bit unsigned integer indicating the total number of documents waiting to be indexed.</span></span>

<span data-ttu-id="cbf24-2761">**cFreshTest:** entero de 32 bits sin signo que indica el número de documentos únicos con información en índices que no están totalmente optimizados para el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2761">**cFreshTest**: A 32-bit unsigned integer indicating the number of unique documents with information in indexes that are not fully optimized for performance.</span></span>

<span data-ttu-id="cbf24-2762">**dwMergeProgress:** entero de 32 bits sin signo que especifica el porcentaje de finalización de la optimización completa actual de índices, si la optimización está actualmente en curso.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2762">**dwMergeProgress**: Unsigned 32-bit integer specifying the completion percentage of current full optimization of indexes, if optimization is currently in progress.</span></span> <span data-ttu-id="cbf24-2763">DEBE ser menor o igual que 100.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2763">MUST be less than or equal to 100.</span></span>

<span data-ttu-id="cbf24-2764">**eState:** estado de la indexación de contenido según lo especificado por una o varias de las constantes DE ESTADO DE \_ \_ \* CI, definidas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2764">**eState**: State of content indexing as given by one or more of the CI\_STATE\_\* constants, defined in the table below.</span></span>



| <span data-ttu-id="cbf24-2765">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-2765">Value</span></span>                                         | <span data-ttu-id="cbf24-2766">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-2766">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-2767">COMBINACIÓN \_ DE \_ \_ SOMBRAS DE ESTADO DE CI 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-2767">CI\_STATE\_SHADOW\_MERGE 0x00000001</span></span>           | <span data-ttu-id="cbf24-2768">El servicio de indexación está en proceso de optimizar algunos de los índices para reducir el uso de memoria y mejorar el rendimiento de las consultas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2768">The indexing service is in the process of optimizing some of the indexes to reduce memory usage and improve query performance.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="cbf24-2769">Ci \_ STATE MASTER MERGE \_ \_ 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbf24-2769">CI\_STATE\_MASTER\_MERGE 0x00000002</span></span>           | <span data-ttu-id="cbf24-2770">El servicio de indexación está en proceso de optimización completa para todos los índices.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2770">The indexing service is in the process of full optimization for all indexes.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cbf24-2771">EXAMEN \_ DE CONTENIDO DE ESTADO DE CI \_ \_ \_ 0X00000004</span><span class="sxs-lookup"><span data-stu-id="cbf24-2771">CI\_STATE\_CONTENT\_SCAN\_REQUIRED 0x00000004</span></span> | <span data-ttu-id="cbf24-2772">Algunos documentos del índice han cambiado y el servicio de indexación debe determinar cuáles se han agregado, modificado o eliminado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2772">Some documents in the index have changed and the indexing service needs to determine which have been added, changed, or deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="cbf24-2773">Ci \_ STATE \_ \_ RECOCIDO MERGE 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cbf24-2773">CI\_STATE\_ANNEALING\_MERGE 0x00000008</span></span>        | <span data-ttu-id="cbf24-2774">El servicio de indexación está en proceso de optimizar los índices para reducir el uso de memoria y mejorar el rendimiento de las consultas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2774">The indexing service is in the process of optimizing indexes to reduce memory usage and improve query performance.</span></span> <span data-ttu-id="cbf24-2775">Este proceso es más completo que el identificado por el valor CI STATE SHADOW MERGE, pero no es tan completo como se especifica en el valor \_ DE CI STATE MASTER \_ \_ \_ \_ \_ MERGE.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2775">This process is more comprehensive than the one identified by the CI\_STATE\_SHADOW\_MERGE value, but it is not as comprehensive as specified by the CI\_STATE\_MASTER\_MERGE value.</span></span> <span data-ttu-id="cbf24-2776">Estas optimizaciones son específicas de la implementación, ya que dependen de la forma en que los datos se almacenan internamente. las optimizaciones no afectan al protocolo de ninguna manera que no sea el tiempo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2776">Such optimizations are implementation-specific as they depend on the way data is stored internally; the optimizations do not affect the protocol in any way other than response time.</span></span> |
| <span data-ttu-id="cbf24-2777">Análisis \_ de ESTADO DE CI \_ 0x00000010</span><span class="sxs-lookup"><span data-stu-id="cbf24-2777">CI\_STATE\_SCANNING 0x00000010</span></span>                | <span data-ttu-id="cbf24-2778">El servicio de indexación está examinando un directorio o un conjunto de directorios para ver si se ha agregado, eliminado o actualizado algún archivo desde la última vez que se indexó el directorio.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2778">The indexing service is examining a directory or a set of directories to see if any files have been added, deleted, or updated since the last time the directory was indexed.</span></span>                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="cbf24-2779">RECUPERACIÓN \_ DE ESTADO DE CI \_ 0x00000020</span><span class="sxs-lookup"><span data-stu-id="cbf24-2779">CI\_STATE\_RECOVERING 0x00000020</span></span>              | <span data-ttu-id="cbf24-2780">El servicio se inicia desde el último estado guardado y está en proceso de recuperación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2780">The service is starting from the last saved state and is in the process of recovering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="cbf24-2781">ESTADO DE CI \_ \_ MEMORIA BAJA \_ 0x00000080</span><span class="sxs-lookup"><span data-stu-id="cbf24-2781">CI\_STATE\_LOW\_MEMORY 0x00000080</span></span>             | <span data-ttu-id="cbf24-2782">La mayor parte de la memoria virtual del servidor está en uso.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2782">Most of the virtual memory of the server is in use.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="cbf24-2783">Ci \_ STATE HIGH IO \_ \_ 0x00000100</span><span class="sxs-lookup"><span data-stu-id="cbf24-2783">CI\_STATE\_HIGH\_IO 0x00000100</span></span>                | <span data-ttu-id="cbf24-2784">El nivel de actividad de entrada/salida (E/S) en el servidor es relativamente alto.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2784">The level of input/output (I/O) activity on the server is relatively high.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="cbf24-2785">CI \_ STATE MASTER MERGE \_ \_ \_ PAUSED 0x00000200</span><span class="sxs-lookup"><span data-stu-id="cbf24-2785">CI\_STATE\_MASTER\_MERGE\_PAUSED 0x00000200</span></span>   | <span data-ttu-id="cbf24-2786">Se ha pausado el proceso de optimización completa para todos los índices que se encontraban en curso.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2786">The process of full optimization for all indexes that was in progress has been paused.</span></span> <span data-ttu-id="cbf24-2787">Esto se proporciona solo con fines informativos y no afecta a CISP.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2787">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cbf24-2788">Estado de CI \_ \_ solo lectura \_ 0x00000400</span><span class="sxs-lookup"><span data-stu-id="cbf24-2788">CI\_STATE\_READ\_ONLY 0x00000400</span></span>              | <span data-ttu-id="cbf24-2789">Se ha pausado la parte del servicio de indexación que recoge nuevos documentos para indexar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2789">The portion of the indexing service that picks up new documents to index has been paused.</span></span> <span data-ttu-id="cbf24-2790">Esto se proporciona solo con fines informativos y no afecta a CISP.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2790">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="cbf24-2791">Ci \_ STATE BATTERY POWER \_ \_ 0x00000800</span><span class="sxs-lookup"><span data-stu-id="cbf24-2791">CI\_STATE\_BATTERY\_POWER 0x00000800</span></span>          | <span data-ttu-id="cbf24-2792">La parte del servicio de indexación que recoge nuevos documentos para indexar se ha pausado para conservar la duración de la batería, pero sigue respondiendo a las consultas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2792">The portion of the indexing service that picks up new documents to index has been paused to conserve battery lifetime but still replies to the queries.</span></span> <span data-ttu-id="cbf24-2793">Esto se proporciona solo con fines informativos y no afecta a CISP.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2793">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="cbf24-2794">USUARIO \_ ACTIVO DE ESTADO DE CI \_ \_ 0x00001000</span><span class="sxs-lookup"><span data-stu-id="cbf24-2794">CI\_STATE\_USER\_ACTIVE 0x00001000</span></span>            | <span data-ttu-id="cbf24-2795">La parte del servicio de indexación que recoge nuevos documentos para indexar se ha pausado debido a la alta actividad del usuario (teclado o mouse), pero sigue respondiendo a las consultas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2795">The portion of the indexing service that picks up new documents to index has been paused due to high activity by the user (keyboard or mouse) but still replies to the queries.</span></span> <span data-ttu-id="cbf24-2796">Esto se proporciona solo con fines informativos y no afecta a CISP.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2796">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="cbf24-2797">CI \_ STATE \_ STARTING 0x00002000</span><span class="sxs-lookup"><span data-stu-id="cbf24-2797">CI\_STATE\_STARTING 0x00002000</span></span>                | <span data-ttu-id="cbf24-2798">El servicio está iniciándose.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2798">The service is starting.</span></span> <span data-ttu-id="cbf24-2799">Las consultas se pueden ejecutar, pero el examen y la notificación aún no se han habilitado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2799">Queries can be run, but scanning and notification have not been enabled yet.</span></span> <span data-ttu-id="cbf24-2800">Esto se proporciona solo con fines informativos y no afecta a CISP.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2800">This is given for informative purposes only and does not affect CISP.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="cbf24-2801">ESTADO \_ DE CI QUE LEE \_ \_ USNS 0x00004000</span><span class="sxs-lookup"><span data-stu-id="cbf24-2801">CI\_STATE\_READING\_USNS 0x00004000</span></span>           | <span data-ttu-id="cbf24-2802">El servicio no ha leído el registro que mantiene el sistema de archivos para realizar un seguimiento de los cambios en los archivos o directorios de un volumen, por lo que es posible que el índice no esté actualizado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2802">The service has not read the log kept by the file system to keep track of changes to files or directories in a volume, so the index might not be up to date.</span></span>                                                                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="cbf24-2803">**cFilteredDocuments:** entero de 32 bits sin signo que indica el número de documentos indexados desde que se inició la indexación de contenido.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2803">**cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents indexed since content indexing was begun.</span></span>

<span data-ttu-id="cbf24-2804">**cTotalDocuments:** entero de 32 bits sin signo que indica el número total de documentos del sistema.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2804">**cTotalDocuments**: A 32-bit unsigned integer indicating the total number of documents in the system.</span></span>

<span data-ttu-id="cbf24-2805">**cPendingScans:** entero de 32 bits sin signo que indica el número de operaciones de indexación de alto nivel pendientes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2805">**cPendingScans**: A 32-bit unsigned integer indicating the number of pending high level indexing operations.</span></span> <span data-ttu-id="cbf24-2806">El significado de este valor es específico del proveedor, pero se espera que números mayores indiquen que queda más indexación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2806">The meaning of this value is provider-specific but larger numbers are expected to indicate more indexing remains.</span></span>

<span data-ttu-id="cbf24-2807">*Comportamiento de Windows:* este valor suele ser cero, excepto inmediatamente después de que se haya iniciado la indexación o después de que se desborda una cola de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2807">*Windows Behavior*: This value is usually zero, except immediately after indexing has been started or after a notification queue overflows.</span></span>

<span data-ttu-id="cbf24-2808">**dwIndexSize:** entero de 32 bits sin signo que indica el tamaño, en megabytes, del índice (excepto la caché de propiedades).</span><span class="sxs-lookup"><span data-stu-id="cbf24-2808">**dwIndexSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the index (excluding the property cache).</span></span>

<span data-ttu-id="cbf24-2809">**cUniqueKeys:** entero de 32 bits sin signo que indica el número aproximado de claves únicas del catálogo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2809">**cUniqueKeys**: A 32-bit unsigned integer indicating the approximate number of unique keys in the catalog.</span></span>

<span data-ttu-id="cbf24-2810">**cSecQDocuments:** entero de 32 bits sin signo que indica el número de documentos que el servicio de indexación volverá a intentar indexar debido a un error durante el intento de indexación inicial.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2810">**cSecQDocuments**: A 32-bit unsigned integer indicating the number of documents that the indexing service will re-attempt to index because of a failure during the initial indexing attempt.</span></span>

<span data-ttu-id="cbf24-2811">**dwPropCacheSize:** entero de 32 bits sin signo que indica el tamaño, en megabytes, de la caché de propiedades.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2811">**dwPropCacheSize**: A 32-bit unsigned integer indicating the size, in megabytes, of the property cache.</span></span>

### <a name="2232-cpmsetcatstatein"></a><span data-ttu-id="cbf24-2812">2.2.3.2 CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-2812">2.2.3.2 CPMSetCatStateIn</span></span>

<span data-ttu-id="cbf24-2813">El mensaje CPMSetCatStateIn establece el estado de un catálogo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2813">The CPMSetCatStateIn message sets the state of a catalog.</span></span> <span data-ttu-id="cbf24-2814">El formato del mensaje CPMSetCatStateIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-2814">The format of the CPMSetCatStateIn message that follows the header is:</span></span>



<span data-ttu-id="cbf24-2815">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2815">0</span></span>

<span data-ttu-id="cbf24-2816">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2816">1</span></span>

<span data-ttu-id="cbf24-2817">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2817">2</span></span>

<span data-ttu-id="cbf24-2818">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2818">3</span></span>

<span data-ttu-id="cbf24-2819">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2819">4</span></span>

<span data-ttu-id="cbf24-2820">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2820">5</span></span>

<span data-ttu-id="cbf24-2821">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2821">6</span></span>

<span data-ttu-id="cbf24-2822">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2822">7</span></span>

<span data-ttu-id="cbf24-2823">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2823">8</span></span>

<span data-ttu-id="cbf24-2824">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2824">9</span></span>

<span data-ttu-id="cbf24-2825">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2825">1</span></span><br/> <span data-ttu-id="cbf24-2826">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2826">0</span></span><br/>

<span data-ttu-id="cbf24-2827">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2827">1</span></span>

<span data-ttu-id="cbf24-2828">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2828">2</span></span>

<span data-ttu-id="cbf24-2829">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2829">3</span></span>

<span data-ttu-id="cbf24-2830">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2830">4</span></span>

<span data-ttu-id="cbf24-2831">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2831">5</span></span>

<span data-ttu-id="cbf24-2832">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2832">6</span></span>

<span data-ttu-id="cbf24-2833">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2833">7</span></span>

<span data-ttu-id="cbf24-2834">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2834">8</span></span>

<span data-ttu-id="cbf24-2835">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2835">9</span></span>

<span data-ttu-id="cbf24-2836">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2836">2</span></span><br/> <span data-ttu-id="cbf24-2837">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2837">0</span></span><br/>

<span data-ttu-id="cbf24-2838">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2838">1</span></span>

<span data-ttu-id="cbf24-2839">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2839">2</span></span>

<span data-ttu-id="cbf24-2840">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2840">3</span></span>

<span data-ttu-id="cbf24-2841">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2841">4</span></span>

<span data-ttu-id="cbf24-2842">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2842">5</span></span>

<span data-ttu-id="cbf24-2843">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2843">6</span></span>

<span data-ttu-id="cbf24-2844">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2844">7</span></span>

<span data-ttu-id="cbf24-2845">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2845">8</span></span>

<span data-ttu-id="cbf24-2846">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2846">9</span></span>

<span data-ttu-id="cbf24-2847">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2847">3</span></span><br/> <span data-ttu-id="cbf24-2848">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2848">0</span></span><br/>

<span data-ttu-id="cbf24-2849">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2849">1</span></span>

<span data-ttu-id="cbf24-2850">\_partID</span><span class="sxs-lookup"><span data-stu-id="cbf24-2850">\_partID</span></span>

<span data-ttu-id="cbf24-2851">\_dwNewState</span><span class="sxs-lookup"><span data-stu-id="cbf24-2851">\_dwNewState</span></span>

<span data-ttu-id="cbf24-2852">\_CatName (variable, opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2852">\_CatName (variable, optional)</span></span>



 

<span data-ttu-id="cbf24-2853">**\_ partID:** DEBE establecerse en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2853">**\_partID**: MUST be set to 0x00000001.</span></span>

<span data-ttu-id="cbf24-2854">**\_ dwNewState**: debe establecerse en uno de los valores siguientes, lo que indica el nuevo estado del catálogo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2854">**\_dwNewState**: MUST be set to one of the following values, indicating the new state of the catalog.</span></span>



| <span data-ttu-id="cbf24-2855">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-2855">Value</span></span>                         | <span data-ttu-id="cbf24-2856">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-2856">Meaning</span></span>                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-2857">CICAT \_ STOPPED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-2857">CICAT\_STOPPED 0x00000001</span></span>     | <span data-ttu-id="cbf24-2858">El catálogo se detiene.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2858">The catalog is stopped.</span></span> <span data-ttu-id="cbf24-2859">Este estado significa que no se van a indexar nuevos archivos y que no se van a procesar consultas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2859">This state means no new files are to be indexed, and no search queries are to be processed.</span></span>                                                     |
| <span data-ttu-id="cbf24-2860">CICAT \_ READONLY 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbf24-2860">CICAT\_READONLY 0x00000002</span></span>    | <span data-ttu-id="cbf24-2861">El catálogo es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2861">The catalog is read-only.</span></span> <span data-ttu-id="cbf24-2862">No se van a indexar nuevos archivos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2862">No new files are to be indexed.</span></span>                                                                                                               |
| <span data-ttu-id="cbf24-2863">CICAT \_ WRITABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cbf24-2863">CICAT\_WRITABLE 0x00000004</span></span>    | <span data-ttu-id="cbf24-2864">El catálogo se puede escribir.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2864">The catalog is writable.</span></span> <span data-ttu-id="cbf24-2865">Se pueden indexar nuevos archivos y se van a procesar las consultas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2865">New files can be indexed, and search queries are to be processed.</span></span>                                                                              |
| <span data-ttu-id="cbf24-2866">CICAT \_ NO \_ QUERY 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cbf24-2866">CICAT\_NO\_QUERY 0x00000008</span></span>   | <span data-ttu-id="cbf24-2867">El catálogo no está disponible para realizar consultas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2867">The catalog is not available for querying.</span></span>                                                                                                                              |
| <span data-ttu-id="cbf24-2868">CICAT \_ GET \_ STATE 0x00000010</span><span class="sxs-lookup"><span data-stu-id="cbf24-2868">CICAT\_GET\_STATE 0x00000010</span></span>  | <span data-ttu-id="cbf24-2869">El estado del catálogo no se va a cambiar, solo se recupera.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2869">The state of the catalog is not to be changed, only retrieved.</span></span>                                                                                                          |
| <span data-ttu-id="cbf24-2870">CICAT \_ ALL \_ OPENED 0x00000020</span><span class="sxs-lookup"><span data-stu-id="cbf24-2870">CICAT\_ALL\_OPENED 0x00000020</span></span> | <span data-ttu-id="cbf24-2871">Una comprobación para ver si se han iniciado todos los catálogos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2871">A check to see if all of the catalogs have been started.</span></span> <span data-ttu-id="cbf24-2872">Si es así, el campo dwOldState enviado en la respuesta CPMSetCatStateOut a este mensaje se notifica \_ como distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2872">If so, the \_dwOldState field sent in the CPMSetCatStateOut reply to this message will be reported as nonzero.</span></span> |



 

<span data-ttu-id="cbf24-2873">**\_ CatName:** el nombre del catálogo que debe modificar su estado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2873">**\_CatName**: The name of the catalog which is to have its state modified.</span></span> <span data-ttu-id="cbf24-2874">El nombre DEBE ser una cadena Unicode terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2874">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="cbf24-2875">Este campo DEBE omitirse si \_ dwNewState está establecido en CICAT \_ ALL \_ OPENED.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2875">This field MUST be omitted if \_dwNewState is set to CICAT\_ALL\_OPENED.</span></span>

### <a name="2233-cpmsetcatstateout"></a><span data-ttu-id="cbf24-2876">2.2.3.3 CPMSetCatStateOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-2876">2.2.3.3 CPMSetCatStateOut</span></span>

<span data-ttu-id="cbf24-2877">El mensaje CPMSetCatStateOut es una respuesta a un mensaje CPMSetCatStateIn con el estado anterior del catálogo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2877">The CPMSetCatStateOut message is a reply to a CPMSetCatStateIn message with the old state of the catalog.</span></span> <span data-ttu-id="cbf24-2878">El formato del mensaje CPMSetCatStateOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-2878">The format of the CPMSetCatStateOut message that follows the header is:</span></span>



<span data-ttu-id="cbf24-2879">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2879">0</span></span>

<span data-ttu-id="cbf24-2880">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2880">1</span></span>

<span data-ttu-id="cbf24-2881">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2881">2</span></span>

<span data-ttu-id="cbf24-2882">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2882">3</span></span>

<span data-ttu-id="cbf24-2883">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2883">4</span></span>

<span data-ttu-id="cbf24-2884">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2884">5</span></span>

<span data-ttu-id="cbf24-2885">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2885">6</span></span>

<span data-ttu-id="cbf24-2886">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2886">7</span></span>

<span data-ttu-id="cbf24-2887">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2887">8</span></span>

<span data-ttu-id="cbf24-2888">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2888">9</span></span>

<span data-ttu-id="cbf24-2889">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2889">1</span></span><br/> <span data-ttu-id="cbf24-2890">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2890">0</span></span><br/>

<span data-ttu-id="cbf24-2891">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2891">1</span></span>

<span data-ttu-id="cbf24-2892">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2892">2</span></span>

<span data-ttu-id="cbf24-2893">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2893">3</span></span>

<span data-ttu-id="cbf24-2894">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2894">4</span></span>

<span data-ttu-id="cbf24-2895">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2895">5</span></span>

<span data-ttu-id="cbf24-2896">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2896">6</span></span>

<span data-ttu-id="cbf24-2897">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2897">7</span></span>

<span data-ttu-id="cbf24-2898">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2898">8</span></span>

<span data-ttu-id="cbf24-2899">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2899">9</span></span>

<span data-ttu-id="cbf24-2900">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2900">2</span></span><br/> <span data-ttu-id="cbf24-2901">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2901">0</span></span><br/>

<span data-ttu-id="cbf24-2902">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2902">1</span></span>

<span data-ttu-id="cbf24-2903">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2903">2</span></span>

<span data-ttu-id="cbf24-2904">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2904">3</span></span>

<span data-ttu-id="cbf24-2905">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2905">4</span></span>

<span data-ttu-id="cbf24-2906">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2906">5</span></span>

<span data-ttu-id="cbf24-2907">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2907">6</span></span>

<span data-ttu-id="cbf24-2908">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2908">7</span></span>

<span data-ttu-id="cbf24-2909">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2909">8</span></span>

<span data-ttu-id="cbf24-2910">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2910">9</span></span>

<span data-ttu-id="cbf24-2911">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2911">3</span></span><br/> <span data-ttu-id="cbf24-2912">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2912">0</span></span><br/>

<span data-ttu-id="cbf24-2913">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2913">1</span></span>

<span data-ttu-id="cbf24-2914">\_dwOldState</span><span class="sxs-lookup"><span data-stu-id="cbf24-2914">\_dwOldState</span></span>



 

<span data-ttu-id="cbf24-2915">**\_ dwOldState:** uno de los valores siguientes, que indica el estado anterior del catálogo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2915">**\_dwOldState**: One of the following values, indicating the old state of the catalog.</span></span>



| <span data-ttu-id="cbf24-2916">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-2916">Value</span></span>                       | <span data-ttu-id="cbf24-2917">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-2917">Meaning</span></span>                                    |
|-----------------------------|--------------------------------------------|
| <span data-ttu-id="cbf24-2918">CICAT \_ STOPPED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-2918">CICAT\_STOPPED 0x00000001</span></span>   | <span data-ttu-id="cbf24-2919">El catálogo se detiene.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2919">The catalog is stopped.</span></span>                    |
| <span data-ttu-id="cbf24-2920">CICAT \_ READONLY 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbf24-2920">CICAT\_READONLY 0x00000002</span></span>  | <span data-ttu-id="cbf24-2921">El catálogo es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2921">The catalog is read-only.</span></span>                  |
| <span data-ttu-id="cbf24-2922">CICAT \_ WRITABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cbf24-2922">CICAT\_WRITABLE 0x00000004</span></span>  | <span data-ttu-id="cbf24-2923">El catálogo se puede escribir.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2923">The catalog is writable.</span></span>                   |
| <span data-ttu-id="cbf24-2924">CICAT \_ NO \_ QUERY 0x00000008</span><span class="sxs-lookup"><span data-stu-id="cbf24-2924">CICAT\_NO\_QUERY 0x00000008</span></span> | <span data-ttu-id="cbf24-2925">El catálogo no está disponible para realizar consultas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2925">The catalog is not available for querying.</span></span> |



 

### <a name="2234-cpmupdatedocumentsin"></a><span data-ttu-id="cbf24-2926">2.2.3.4 CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-2926">2.2.3.4 CPMUpdateDocumentsIn</span></span>

<span data-ttu-id="cbf24-2927">El mensaje CPMUpdateDocumentsIn indica al servidor que indexe la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2927">The CPMUpdateDocumentsIn message directs the server to index the specified path.</span></span>

<span data-ttu-id="cbf24-2928">El servidor responderá con el encabezado del mensaje CPMUpdateDocumentsOut, con los resultados de la solicitud contenida en el campo de estado del \_ encabezado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2928">The server will reply with the message header of the CPMUpdateDocumentsOut message, with the results of the request contained in the \_status field of the message header.</span></span>

<span data-ttu-id="cbf24-2929">El formato del mensaje CPMUpdateDocumentsIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-2929">The format of the CPMUpdateDocumentsIn message that follows the header is:</span></span>



<span data-ttu-id="cbf24-2930">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2930">0</span></span>

<span data-ttu-id="cbf24-2931">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2931">1</span></span>

<span data-ttu-id="cbf24-2932">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2932">2</span></span>

<span data-ttu-id="cbf24-2933">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2933">3</span></span>

<span data-ttu-id="cbf24-2934">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2934">4</span></span>

<span data-ttu-id="cbf24-2935">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2935">5</span></span>

<span data-ttu-id="cbf24-2936">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2936">6</span></span>

<span data-ttu-id="cbf24-2937">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2937">7</span></span>

<span data-ttu-id="cbf24-2938">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2938">8</span></span>

<span data-ttu-id="cbf24-2939">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2939">9</span></span>

<span data-ttu-id="cbf24-2940">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2940">1</span></span><br/> <span data-ttu-id="cbf24-2941">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2941">0</span></span><br/>

<span data-ttu-id="cbf24-2942">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2942">1</span></span>

<span data-ttu-id="cbf24-2943">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2943">2</span></span>

<span data-ttu-id="cbf24-2944">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2944">3</span></span>

<span data-ttu-id="cbf24-2945">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2945">4</span></span>

<span data-ttu-id="cbf24-2946">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2946">5</span></span>

<span data-ttu-id="cbf24-2947">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2947">6</span></span>

<span data-ttu-id="cbf24-2948">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2948">7</span></span>

<span data-ttu-id="cbf24-2949">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2949">8</span></span>

<span data-ttu-id="cbf24-2950">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2950">9</span></span>

<span data-ttu-id="cbf24-2951">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2951">2</span></span><br/> <span data-ttu-id="cbf24-2952">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2952">0</span></span><br/>

<span data-ttu-id="cbf24-2953">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2953">1</span></span>

<span data-ttu-id="cbf24-2954">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2954">2</span></span>

<span data-ttu-id="cbf24-2955">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2955">3</span></span>

<span data-ttu-id="cbf24-2956">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2956">4</span></span>

<span data-ttu-id="cbf24-2957">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2957">5</span></span>

<span data-ttu-id="cbf24-2958">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2958">6</span></span>

<span data-ttu-id="cbf24-2959">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2959">7</span></span>

<span data-ttu-id="cbf24-2960">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-2960">8</span></span>

<span data-ttu-id="cbf24-2961">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-2961">9</span></span>

<span data-ttu-id="cbf24-2962">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2962">3</span></span><br/> <span data-ttu-id="cbf24-2963">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2963">0</span></span><br/>

<span data-ttu-id="cbf24-2964">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2964">1</span></span>

<span data-ttu-id="cbf24-2965">\_flag (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2965">\_flag (optional)</span></span>

<span data-ttu-id="cbf24-2966">\_fRootPath (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2966">\_fRootPath (optional)</span></span>

<span data-ttu-id="cbf24-2967">RootPath (variable, opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-2967">RootPath (variable, optional)</span></span>



 

<span data-ttu-id="cbf24-2968">**\_ flag**: tipo de actualización que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2968">**\_flag**: The type of update to be performed.</span></span> <span data-ttu-id="cbf24-2969">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2969">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="cbf24-2970">Este campo DEBE establecerse en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="cbf24-2970">This field MUST be set to one of the following values:</span></span>



| <span data-ttu-id="cbf24-2971">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-2971">Value</span></span>                  | <span data-ttu-id="cbf24-2972">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-2972">Meaning</span></span>                                   |
|------------------------|-------------------------------------------|
| <span data-ttu-id="cbf24-2973">UPD \_ INCREM 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-2973">UPD\_INCREM 0x00000000</span></span> | <span data-ttu-id="cbf24-2974">Se va a realizar una actualización incremental.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2974">An incremental update is to be performed.</span></span> |
| <span data-ttu-id="cbf24-2975">UPD \_ FULL 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-2975">UPD\_FULL 0x00000001</span></span>   | <span data-ttu-id="cbf24-2976">Se va a realizar una actualización completa.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2976">A full update is to be performed.</span></span>         |
| <span data-ttu-id="cbf24-2977">Upd \_ INIT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbf24-2977">UPD\_INIT 0x00000002</span></span>   | <span data-ttu-id="cbf24-2978">Se va a realizar una nueva inicialización.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2978">A new initialization is to be performed.</span></span>  |



 

<span data-ttu-id="cbf24-2979">**\_ fRootPath:** valor booleano que indica si el campo RootPath especifica una ruta de acceso en la que se va a realizar la actualización.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2979">**\_fRootPath**: A boolean value indicating if the RootPath field specifies a path on which to perform the update.</span></span> <span data-ttu-id="cbf24-2980">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2980">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="cbf24-2981">Este campo DEBE establecerse en 0x00000001 o 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2981">This field MUST be set to 0x00000001 or 0x00000000.</span></span> <span data-ttu-id="cbf24-2982">Si se establece en 0x00000001, se incluye una ruta de acceso en la que realizar la actualización en RootPath.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2982">If set to 0x00000001, then a path on which to perform the update is included in RootPath.</span></span> <span data-ttu-id="cbf24-2983">Si se establece en 0x00000000, la actualización se realizará en todas las rutas de acceso indizadas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2983">If set to 0x00000000, then the update is to be performed on all indexed paths.</span></span>

<span data-ttu-id="cbf24-2984">**RootPath:** nombre de la ruta de acceso que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2984">**RootPath**: The name of the path to be updated.</span></span> <span data-ttu-id="cbf24-2985">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2985">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="cbf24-2986">El nombre DEBE ser una cadena Unicode terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2986">The name MUST be a null-terminated Unicode string.</span></span> <span data-ttu-id="cbf24-2987">Este campo DEBE omitirse si \_ fRootPath está establecido en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2987">This field MUST be omitted if \_fRootPath is set to 0x00000000.</span></span>

### <a name="2235-cpmforcemergein"></a><span data-ttu-id="cbf24-2988">2.2.3.5 CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-2988">2.2.3.5 CPMForceMergeIn</span></span>

<span data-ttu-id="cbf24-2989">El mensaje CPMForceMergeIn solicita a un servidor que realice el mantenimiento necesario para mejorar el rendimiento de las consultas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2989">The CPMForceMergeIn message requests a server to perform any maintenance necessary to improve query performance.</span></span> <span data-ttu-id="cbf24-2990">El servidor responderá con el encabezado del mensaje CPMForceMergeIn, con los resultados de la solicitud contenida en el \_ campo de estado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-2990">The server will reply with the message header of the CPMForceMergeIn message, with the results of the request contained in the \_status field.</span></span>

<span data-ttu-id="cbf24-2991">El formato del mensaje CPMForceMergeIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-2991">The format of the CPMForceMergeIn message that follows the header is:</span></span>



<span data-ttu-id="cbf24-2992">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-2992">0</span></span>

<span data-ttu-id="cbf24-2993">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-2993">1</span></span>

<span data-ttu-id="cbf24-2994">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-2994">2</span></span>

<span data-ttu-id="cbf24-2995">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-2995">3</span></span>

<span data-ttu-id="cbf24-2996">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-2996">4</span></span>

<span data-ttu-id="cbf24-2997">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-2997">5</span></span>

<span data-ttu-id="cbf24-2998">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-2998">6</span></span>

<span data-ttu-id="cbf24-2999">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-2999">7</span></span>

<span data-ttu-id="cbf24-3000">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3000">8</span></span>

<span data-ttu-id="cbf24-3001">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3001">9</span></span>

<span data-ttu-id="cbf24-3002">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3002">1</span></span><br/> <span data-ttu-id="cbf24-3003">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3003">0</span></span><br/>

<span data-ttu-id="cbf24-3004">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3004">1</span></span>

<span data-ttu-id="cbf24-3005">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3005">2</span></span>

<span data-ttu-id="cbf24-3006">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3006">3</span></span>

<span data-ttu-id="cbf24-3007">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3007">4</span></span>

<span data-ttu-id="cbf24-3008">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3008">5</span></span>

<span data-ttu-id="cbf24-3009">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3009">6</span></span>

<span data-ttu-id="cbf24-3010">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3010">7</span></span>

<span data-ttu-id="cbf24-3011">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3011">8</span></span>

<span data-ttu-id="cbf24-3012">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3012">9</span></span>

<span data-ttu-id="cbf24-3013">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3013">2</span></span><br/> <span data-ttu-id="cbf24-3014">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3014">0</span></span><br/>

<span data-ttu-id="cbf24-3015">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3015">1</span></span>

<span data-ttu-id="cbf24-3016">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3016">2</span></span>

<span data-ttu-id="cbf24-3017">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3017">3</span></span>

<span data-ttu-id="cbf24-3018">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3018">4</span></span>

<span data-ttu-id="cbf24-3019">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3019">5</span></span>

<span data-ttu-id="cbf24-3020">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3020">6</span></span>

<span data-ttu-id="cbf24-3021">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3021">7</span></span>

<span data-ttu-id="cbf24-3022">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3022">8</span></span>

<span data-ttu-id="cbf24-3023">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3023">9</span></span>

<span data-ttu-id="cbf24-3024">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3024">3</span></span><br/> <span data-ttu-id="cbf24-3025">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3025">0</span></span><br/>

<span data-ttu-id="cbf24-3026">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3026">1</span></span>

<span data-ttu-id="cbf24-3027">\_partID (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3027">\_partID (optional)</span></span>



 

<span data-ttu-id="cbf24-3028">**\_ partID:** este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3028">**\_partID**: This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="cbf24-3029">Cuando este campo está presente, debe establecerse en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3029">When this field is present, it MUST be set to 0x00000001.</span></span>

### <a name="2236-cpmconnectin"></a><span data-ttu-id="cbf24-3030">2.2.3.6 CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-3030">2.2.3.6 CPMConnectIn</span></span>

<span data-ttu-id="cbf24-3031">El mensaje CPMConnectIn inicia una sesión entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3031">The CPMConnectIn message begins a session between the client and server.</span></span>

<span data-ttu-id="cbf24-3032">El formato del mensaje CPMConnectIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3032">The format of the CPMConnectIn message that follows the header is:</span></span>



<span data-ttu-id="cbf24-3033">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3033">0</span></span>

<span data-ttu-id="cbf24-3034">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3034">1</span></span>

<span data-ttu-id="cbf24-3035">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3035">2</span></span>

<span data-ttu-id="cbf24-3036">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3036">3</span></span>

<span data-ttu-id="cbf24-3037">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3037">4</span></span>

<span data-ttu-id="cbf24-3038">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3038">5</span></span>

<span data-ttu-id="cbf24-3039">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3039">6</span></span>

<span data-ttu-id="cbf24-3040">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3040">7</span></span>

<span data-ttu-id="cbf24-3041">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3041">8</span></span>

<span data-ttu-id="cbf24-3042">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3042">9</span></span>

<span data-ttu-id="cbf24-3043">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3043">1</span></span><br/> <span data-ttu-id="cbf24-3044">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3044">0</span></span><br/>

<span data-ttu-id="cbf24-3045">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3045">1</span></span>

<span data-ttu-id="cbf24-3046">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3046">2</span></span>

<span data-ttu-id="cbf24-3047">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3047">3</span></span>

<span data-ttu-id="cbf24-3048">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3048">4</span></span>

<span data-ttu-id="cbf24-3049">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3049">5</span></span>

<span data-ttu-id="cbf24-3050">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3050">6</span></span>

<span data-ttu-id="cbf24-3051">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3051">7</span></span>

<span data-ttu-id="cbf24-3052">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3052">8</span></span>

<span data-ttu-id="cbf24-3053">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3053">9</span></span>

<span data-ttu-id="cbf24-3054">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3054">2</span></span><br/> <span data-ttu-id="cbf24-3055">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3055">0</span></span><br/>

<span data-ttu-id="cbf24-3056">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3056">1</span></span>

<span data-ttu-id="cbf24-3057">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3057">2</span></span>

<span data-ttu-id="cbf24-3058">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3058">3</span></span>

<span data-ttu-id="cbf24-3059">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3059">4</span></span>

<span data-ttu-id="cbf24-3060">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3060">5</span></span>

<span data-ttu-id="cbf24-3061">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3061">6</span></span>

<span data-ttu-id="cbf24-3062">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3062">7</span></span>

<span data-ttu-id="cbf24-3063">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3063">8</span></span>

<span data-ttu-id="cbf24-3064">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3064">9</span></span>

<span data-ttu-id="cbf24-3065">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3065">3</span></span><br/> <span data-ttu-id="cbf24-3066">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3066">0</span></span><br/>

<span data-ttu-id="cbf24-3067">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3067">1</span></span>

<span data-ttu-id="cbf24-3068">\_iClientVersion</span><span class="sxs-lookup"><span data-stu-id="cbf24-3068">\_iClientVersion</span></span>

<span data-ttu-id="cbf24-3069">\_fClientIsRemote</span><span class="sxs-lookup"><span data-stu-id="cbf24-3069">\_fClientIsRemote</span></span>

<span data-ttu-id="cbf24-3070">\_cbBlob1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3070">\_cbBlob1</span></span>

<span data-ttu-id="cbf24-3071">\_cbBlob2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3071">\_cbBlob2</span></span>

<span data-ttu-id="cbf24-3072">\_Acolchado</span><span class="sxs-lookup"><span data-stu-id="cbf24-3072">\_padding</span></span>

<span data-ttu-id="cbf24-3073">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-3073">...</span></span>

<span data-ttu-id="cbf24-3074">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-3074">...</span></span>

<span data-ttu-id="cbf24-3075">MachineName</span><span class="sxs-lookup"><span data-stu-id="cbf24-3075">MachineName</span></span>

<span data-ttu-id="cbf24-3076">... (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3076">... (variable)</span></span>

<span data-ttu-id="cbf24-3077">UserName</span><span class="sxs-lookup"><span data-stu-id="cbf24-3077">UserName</span></span>

<span data-ttu-id="cbf24-3078">... (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3078">... (variable)</span></span>

<span data-ttu-id="cbf24-3079">\_paddingcPropSets (opcional, variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3079">\_paddingcPropSets (optional, variable)</span></span>

<span data-ttu-id="cbf24-3080">cPropSets</span><span class="sxs-lookup"><span data-stu-id="cbf24-3080">cPropSets</span></span>

<span data-ttu-id="cbf24-3081">PropertySet1 (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3081">PropertySet1 (variable)</span></span>

<span data-ttu-id="cbf24-3082">PropertySet2 (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3082">PropertySet2 (variable)</span></span>

<span data-ttu-id="cbf24-3083">\_paddingExtPropset (opcional, variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3083">\_paddingExtPropset (optional, variable)</span></span>

<span data-ttu-id="cbf24-3084">cExtPropSet</span><span class="sxs-lookup"><span data-stu-id="cbf24-3084">cExtPropSet</span></span>

<span data-ttu-id="cbf24-3085">aPropertySets (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3085">aPropertySets (variable)</span></span>



 

<span data-ttu-id="cbf24-3086">**\_ iClientVersion:** entero de 32 bits que indica si el servidor va a validar el valor de suma de comprobación especificado en el campo ulChecksum de los encabezados de mensaje para los mensajes enviados por \_ el cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3086">**\_iClientVersion**: A 32-bit integer indicating whether the server is to validate the checksum value specified in the \_ulChecksum field of the message headers for messages sent by the client.</span></span> <span data-ttu-id="cbf24-3087">Si el campo iClientVersion está establecido en 0x00000008 o superior, el servidor DEBE validar el valor del campo \_ \_ ulChecksum para los mensajes siguientes:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3087">If the \_iClientVersion field is set to 0x00000008 or greater, the server MUST validate the \_ulChecksum field value for the following messages:</span></span>

-   <span data-ttu-id="cbf24-3088">CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-3088">CPMConnectIn</span></span>
-   <span data-ttu-id="cbf24-3089">CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-3089">CPMCreateQueryIn</span></span>
-   <span data-ttu-id="cbf24-3090">CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-3090">CPMFetchValueIn</span></span>
-   <span data-ttu-id="cbf24-3091">CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-3091">CPMGetRowsIn</span></span>
-   <span data-ttu-id="cbf24-3092">CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-3092">CPMSetBindingsIn</span></span>

<span data-ttu-id="cbf24-3093">Para obtener más información sobre cómo el servidor valida el valor especificado por el cliente en el campo ulChecksum para los mensajes enumerados anteriormente, consulte la sección 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3093">For details about how the server validates the value specified by the client in the ulChecksum field for the messages listed above, see Section 3.2.5.</span></span>

<span data-ttu-id="cbf24-3094">Si el valor es mayor que 0x00000008, se supone que el cliente es capaz de controlar desplazamientos de 64 bits en mensajes CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3094">If the value is greater than 0x00000008 then the client is assumed capable of handling 64-bit offsets in CPMGetRowsOut messages.</span></span> <span data-ttu-id="cbf24-3095">Consulte la sección 2.2.3.16 para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3095">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="cbf24-3096">*Comportamiento de Windows: en los clientes windows, iClientVersion se establece de la siguiente manera:*</span><span class="sxs-lookup"><span data-stu-id="cbf24-3096">*Windows Behavior: On Windows clients, the iClientVersion is set as follows*:</span></span>



| <span data-ttu-id="cbf24-3097">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-3097">Value</span></span>      | <span data-ttu-id="cbf24-3098">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-3098">Meaning</span></span>                                                              |
|------------|----------------------------------------------------------------------|
| <span data-ttu-id="cbf24-3099">0x00000005</span><span class="sxs-lookup"><span data-stu-id="cbf24-3099">0x00000005</span></span> | <span data-ttu-id="cbf24-3100">El sistema operativo cliente es Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3100">Client OS is Windows 2000.</span></span>                                           |
| <span data-ttu-id="cbf24-3101">0x00000008</span><span class="sxs-lookup"><span data-stu-id="cbf24-3101">0x00000008</span></span> | <span data-ttu-id="cbf24-3102">El sistema operativo cliente es Windows XP de 32 bits o Windows Server 2003 de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3102">Client OS is either 32-bit Windows XP or 32-bit Windows Server 2003.</span></span> |
| <span data-ttu-id="cbf24-3103">0x00010008</span><span class="sxs-lookup"><span data-stu-id="cbf24-3103">0x00010008</span></span> | <span data-ttu-id="cbf24-3104">El sistema operativo cliente es Windows XP de 64 bits o Windows Server 2003 de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3104">Client OS is either 64-bit Windows XP or 64-bit Windows Server 2003.</span></span> |



 

<span data-ttu-id="cbf24-3105">\_**fClientIsRemote:** valor booleano que indica si el cliente se ejecuta en un equipo diferente al servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3105">\_**fClientIsRemote**: A boolean value indicating whether the client is running on a different machine than the server.</span></span> <span data-ttu-id="cbf24-3106">DEBE establecerse en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3106">MUST be set to 0x00000001.</span></span>

<span data-ttu-id="cbf24-3107">\_**cbBlob1:** entero de 32 bits sin signo que indica el tamaño en bytes de los campos cPropSet, PropertySet1 y PropertySet2, combinados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3107">\_**cbBlob1**: A 32-bit unsigned integer indicating the size in bytes of cPropSet, PropertySet1, and PropertySet2 fields, combined.</span></span>

<span data-ttu-id="cbf24-3108">\_**cbBlob2:** entero de 32 bits sin signo que indica el tamaño en bytes de los campos cExPropSet y aPropertySet, combinados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3108">\_**cbBlob2**: A 32-bit unsigned integer indicating the size in bytes of cExPropSet and aPropertySet fields, combined.</span></span>

<span data-ttu-id="cbf24-3109">\_**padding:** 12 bytes de relleno que puede contener valores arbitrarios y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3109">\_**padding**: 12 bytes of padding which can contain arbitrary values and MUST be ignored.</span></span>

<span data-ttu-id="cbf24-3110">**MachineName:** el nombre del equipo del cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3110">**MachineName**: The machine name of the client.</span></span> <span data-ttu-id="cbf24-3111">La cadena de nombre DEBE ser una matriz terminada en NULL de menos de 512 caracteres Unicode, incluido el terminador NULL.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3111">The name string MUST be a null-terminated array of less than 512 Unicode characters, including the NULL terminator.</span></span>

<span data-ttu-id="cbf24-3112">**UserName:** cadena que representa el nombre de usuario de la persona que ejecuta la aplicación que invocó este protocolo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3112">**UserName**: A string that represents the user name of the person who is running the application that invoked this protocol.</span></span> <span data-ttu-id="cbf24-3113">La cadena de nombre DEBE ser una matriz terminada en NULL de menos de 512 caracteres Unicode cuando se concatena con MachineName.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3113">The name string MUST be a null-terminated array of less than 512 Unicode characters when concatenated with MachineName.</span></span>

<span data-ttu-id="cbf24-3114">**\_ paddingcPropSets:** este campo DEBE tener entre 0 y 7 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3114">**\_paddingcPropSets**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="cbf24-3115">El número de bytes DEBE ser el número necesario para realizar el desplazamiento de bytes del campo cPropSets desde el principio del mensaje que contiene esta estructura, que es un múltiplo de 8.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3115">The number of bytes MUST be the number required to make the byte offset of the cPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="cbf24-3116">El valor de los bytes puede ser cualquier valor arbitrario y EL receptor DEBE omitirlo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3116">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cbf24-3117">**cPropSets:** entero de 32 bits sin signo que indica el número de estructuras CDbPropSet que sigue a este campo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3117">**cPropSets**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span> <span data-ttu-id="cbf24-3118">Este valor DEBE establecerse en 0x0000002.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3118">This value MUST be set to 0x0000002.</span></span>

<span data-ttu-id="cbf24-3119">**PropertySet1:** una estructura CDbPropSet con guidPropertySet que contiene DBPROPSET \_ FSCIFRMWRK EXT (consulte la sección \_ 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="cbf24-3119">**PropertySet1**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_FSCIFRMWRK\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="cbf24-3120">**PropertySet2:** una estructura CDbPropSet con guidPropertySet que contiene DBPROPSET \_ CIFRMWRKCORE EXT (consulte la sección \_ 2.2.1.22).</span><span class="sxs-lookup"><span data-stu-id="cbf24-3120">**PropertySet2**: A CDbPropSet structure with guidPropertySet containing DBPROPSET\_CIFRMWRKCORE\_EXT (see section 2.2.1.22).</span></span>

<span data-ttu-id="cbf24-3121">\_**PaddingExtPropset:** este campo DEBE tener entre 0 y 7 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3121">\_**PaddingExtPropset**: This field MUST be 0 to 7 bytes in length.</span></span> <span data-ttu-id="cbf24-3122">El número de bytes DEBE ser el número necesario para que el desplazamiento de bytes del campo cExtPropSets desde el principio del mensaje que contiene esta estructura sea un múltiplo de 8.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3122">The number of bytes MUST be the number required to make the byte offset of the cExtPropSets field from the beginning of the message which contains this structure be a multiple of 8.</span></span> <span data-ttu-id="cbf24-3123">El valor de los bytes puede ser cualquier valor arbitrario y el receptor debe omitirlo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3123">The value of the bytes can be any arbitrary value, and MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cbf24-3124">**cExtPropSet:** entero de 32 bits sin signo que indica el número de estructuras CDbPropSet que sigue a este campo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3124">**cExtPropSet**: A 32-bit unsigned integer indicating the number of CDbPropSet structures following this field.</span></span>

<span data-ttu-id="cbf24-3125">**aPropertySets:** matriz de estructuras CDbPropSet que especifican otras propiedades.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3125">**aPropertySets**: An array of CDbPropSet structures specifying other properties.</span></span> <span data-ttu-id="cbf24-3126">El número de elementos de esta matriz DEBE ser igual a cExtPropSet.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3126">The number of elements in this array MUST be equal to cExtPropSet.</span></span>

### <a name="2237-cpmconnectout"></a><span data-ttu-id="cbf24-3127">2.2.3.7 CPMConnectOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-3127">2.2.3.7 CPMConnectOut</span></span>

<span data-ttu-id="cbf24-3128">El mensaje CPMConnectOut contiene una respuesta a un mensaje CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3128">The CPMConnectOut message contains a response to a CPMConnectIn message.</span></span>

<span data-ttu-id="cbf24-3129">El formato del mensaje CPMConnectOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3129">The format of the CPMConnectOut message that follows the header is:</span></span>



<span data-ttu-id="cbf24-3130">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3130">0</span></span>

<span data-ttu-id="cbf24-3131">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3131">1</span></span>

<span data-ttu-id="cbf24-3132">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3132">2</span></span>

<span data-ttu-id="cbf24-3133">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3133">3</span></span>

<span data-ttu-id="cbf24-3134">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3134">4</span></span>

<span data-ttu-id="cbf24-3135">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3135">5</span></span>

<span data-ttu-id="cbf24-3136">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3136">6</span></span>

<span data-ttu-id="cbf24-3137">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3137">7</span></span>

<span data-ttu-id="cbf24-3138">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3138">8</span></span>

<span data-ttu-id="cbf24-3139">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3139">9</span></span>

<span data-ttu-id="cbf24-3140">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3140">1</span></span><br/> <span data-ttu-id="cbf24-3141">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3141">0</span></span><br/>

<span data-ttu-id="cbf24-3142">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3142">1</span></span>

<span data-ttu-id="cbf24-3143">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3143">2</span></span>

<span data-ttu-id="cbf24-3144">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3144">3</span></span>

<span data-ttu-id="cbf24-3145">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3145">4</span></span>

<span data-ttu-id="cbf24-3146">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3146">5</span></span>

<span data-ttu-id="cbf24-3147">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3147">6</span></span>

<span data-ttu-id="cbf24-3148">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3148">7</span></span>

<span data-ttu-id="cbf24-3149">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3149">8</span></span>

<span data-ttu-id="cbf24-3150">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3150">9</span></span>

<span data-ttu-id="cbf24-3151">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3151">2</span></span><br/> <span data-ttu-id="cbf24-3152">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3152">0</span></span><br/>

<span data-ttu-id="cbf24-3153">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3153">1</span></span>

<span data-ttu-id="cbf24-3154">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3154">2</span></span>

<span data-ttu-id="cbf24-3155">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3155">3</span></span>

<span data-ttu-id="cbf24-3156">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3156">4</span></span>

<span data-ttu-id="cbf24-3157">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3157">5</span></span>

<span data-ttu-id="cbf24-3158">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3158">6</span></span>

<span data-ttu-id="cbf24-3159">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3159">7</span></span>

<span data-ttu-id="cbf24-3160">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3160">8</span></span>

<span data-ttu-id="cbf24-3161">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3161">9</span></span>

<span data-ttu-id="cbf24-3162">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3162">3</span></span><br/> <span data-ttu-id="cbf24-3163">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3163">0</span></span><br/>

<span data-ttu-id="cbf24-3164">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3164">1</span></span>

<span data-ttu-id="cbf24-3165">\_serverVersion</span><span class="sxs-lookup"><span data-stu-id="cbf24-3165">\_serverVersion</span></span>

<span data-ttu-id="cbf24-3166">\_reserved (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3166">\_reserved (variable)</span></span>



 

<span data-ttu-id="cbf24-3167">**\_ serverVersion**:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3167">**\_serverVersion**:</span></span>

<span data-ttu-id="cbf24-3168">Entero de 32 bits que indica si el servidor puede admitir desplazamientos de 64 *bits.*</span><span class="sxs-lookup"><span data-stu-id="cbf24-3168">A 32-bit integer, indicating whether the server can support 64-bit offsets *.*</span></span> <span data-ttu-id="cbf24-3169">Consulte la sección 2.2.3.16 para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3169">See section 2.2.3.16 for details.</span></span>



| <span data-ttu-id="cbf24-3170">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-3170">Value</span></span>      | <span data-ttu-id="cbf24-3171">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-3171">Meaning</span></span>                                 |
|------------|-----------------------------------------|
| <span data-ttu-id="cbf24-3172">0x00000007</span><span class="sxs-lookup"><span data-stu-id="cbf24-3172">0x00000007</span></span> | <span data-ttu-id="cbf24-3173">El servidor solo puede enviar desplazamientos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3173">Server is can only send 32-bit offsets.</span></span> |
| <span data-ttu-id="cbf24-3174">0x00010007</span><span class="sxs-lookup"><span data-stu-id="cbf24-3174">0x00010007</span></span> | <span data-ttu-id="cbf24-3175">El servidor puede enviar desplazamientos de 32 o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3175">Server can send 32 or 64-bit offsets.</span></span>   |



 

<span data-ttu-id="cbf24-3176">**\_ reserved:** reservado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3176">**\_reserved**: Reserved.</span></span> <span data-ttu-id="cbf24-3177">El servidor PUEDE enviar un número arbitrario de valores arbitrarios y el cliente DEBE omitir estos valores si están presentes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3177">The server MAY send an arbitrary number of arbitrary values and the client MUST ignore these values if present.</span></span>

### <a name="2238-cpmcreatequeryin"></a><span data-ttu-id="cbf24-3178">2.2.3.8 CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-3178">2.2.3.8 CPMCreateQueryIn</span></span>

<span data-ttu-id="cbf24-3179">El mensaje CPMCreateQueryIn crea una nueva consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3179">The CPMCreateQueryIn message creates a new query.</span></span> <span data-ttu-id="cbf24-3180">El formato del mensaje CPMCreateQueryIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3180">The format of the CPMCreateQueryIn message that follows the header is:</span></span>



<span data-ttu-id="cbf24-3181">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3181">0</span></span>

<span data-ttu-id="cbf24-3182">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3182">1</span></span>

<span data-ttu-id="cbf24-3183">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3183">2</span></span>

<span data-ttu-id="cbf24-3184">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3184">3</span></span>

<span data-ttu-id="cbf24-3185">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3185">4</span></span>

<span data-ttu-id="cbf24-3186">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3186">5</span></span>

<span data-ttu-id="cbf24-3187">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3187">6</span></span>

<span data-ttu-id="cbf24-3188">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3188">7</span></span>

<span data-ttu-id="cbf24-3189">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3189">8</span></span>

<span data-ttu-id="cbf24-3190">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3190">9</span></span>

<span data-ttu-id="cbf24-3191">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3191">1</span></span><br/> <span data-ttu-id="cbf24-3192">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3192">0</span></span><br/>

<span data-ttu-id="cbf24-3193">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3193">1</span></span>

<span data-ttu-id="cbf24-3194">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3194">2</span></span>

<span data-ttu-id="cbf24-3195">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3195">3</span></span>

<span data-ttu-id="cbf24-3196">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3196">4</span></span>

<span data-ttu-id="cbf24-3197">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3197">5</span></span>

<span data-ttu-id="cbf24-3198">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3198">6</span></span>

<span data-ttu-id="cbf24-3199">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3199">7</span></span>

<span data-ttu-id="cbf24-3200">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3200">8</span></span>

<span data-ttu-id="cbf24-3201">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3201">9</span></span>

<span data-ttu-id="cbf24-3202">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3202">2</span></span><br/> <span data-ttu-id="cbf24-3203">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3203">0</span></span><br/>

<span data-ttu-id="cbf24-3204">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3204">1</span></span>

<span data-ttu-id="cbf24-3205">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3205">2</span></span>

<span data-ttu-id="cbf24-3206">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3206">3</span></span>

<span data-ttu-id="cbf24-3207">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3207">4</span></span>

<span data-ttu-id="cbf24-3208">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3208">5</span></span>

<span data-ttu-id="cbf24-3209">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3209">6</span></span>

<span data-ttu-id="cbf24-3210">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3210">7</span></span>

<span data-ttu-id="cbf24-3211">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3211">8</span></span>

<span data-ttu-id="cbf24-3212">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3212">9</span></span>

<span data-ttu-id="cbf24-3213">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3213">3</span></span><br/> <span data-ttu-id="cbf24-3214">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3214">0</span></span><br/>

<span data-ttu-id="cbf24-3215">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3215">1</span></span>

<span data-ttu-id="cbf24-3216">Tamaño</span><span class="sxs-lookup"><span data-stu-id="cbf24-3216">Size</span></span>

<span data-ttu-id="cbf24-3217">CColumnSetPresent</span><span class="sxs-lookup"><span data-stu-id="cbf24-3217">CColumnSetPresent</span></span>

<span data-ttu-id="cbf24-3218">ColumnSet (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3218">ColumnSet (optional)</span></span>

<span data-ttu-id="cbf24-3219">... (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3219">... (variable)</span></span>

<span data-ttu-id="cbf24-3220">CRestrictionPresent.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3220">CRestrictionPresent.</span></span>

<span data-ttu-id="cbf24-3221">Restricción (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3221">Restriction (optional)</span></span>

<span data-ttu-id="cbf24-3222">... (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3222">... (variable)</span></span>

<span data-ttu-id="cbf24-3223">CSortSetPresent</span><span class="sxs-lookup"><span data-stu-id="cbf24-3223">CSortSetPresent</span></span>

<span data-ttu-id="cbf24-3224">SortSet (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3224">SortSet (optional)</span></span>

<span data-ttu-id="cbf24-3225">... (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3225">... (variable)</span></span>

<span data-ttu-id="cbf24-3226">CCategorizationSetPresent</span><span class="sxs-lookup"><span data-stu-id="cbf24-3226">CCategorizationSetPresent</span></span>

<span data-ttu-id="cbf24-3227">CategorizationSet (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3227">CategorizationSet (optional)</span></span>

<span data-ttu-id="cbf24-3228">... (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3228">... (variable)</span></span>

<span data-ttu-id="cbf24-3229">RowSetProperties</span><span class="sxs-lookup"><span data-stu-id="cbf24-3229">RowSetProperties</span></span>

<span data-ttu-id="cbf24-3230">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-3230">...</span></span>

<span data-ttu-id="cbf24-3231">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-3231">...</span></span>

<span data-ttu-id="cbf24-3232">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-3232">...</span></span>

<span data-ttu-id="cbf24-3233">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-3233">...</span></span>

<span data-ttu-id="cbf24-3234">PidMapper (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3234">PidMapper (variable)</span></span>



 

<span data-ttu-id="cbf24-3235">**Tamaño:** entero de 32 bits sin signo que indica el número de bytes desde el principio de este campo hasta el final del mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3235">**Size**: A 32-bit unsigned integer indicating the number of bytes from the beginning of this field to the end of the message.</span></span>

<span data-ttu-id="cbf24-3236">**CColumnSetPresent:** campo de bytes que indica si el campo ColumnSet está presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3236">**CColumnSetPresent**: A byte field indicating if the ColumnSet field is present.</span></span> <span data-ttu-id="cbf24-3237">Este campo DEBE establecerse en 0x01 o 0x00.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3237">This field MUST be set to 0x01 or 0x00.</span></span> <span data-ttu-id="cbf24-3238">Si se establece 0x01 el campo CColumnSet DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3238">If set to 0x01 the CColumnSet field MUST be present.</span></span> <span data-ttu-id="cbf24-3239">Si se establece 0x00, DEBE estar ausente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3239">If set to 0x00, it MUST be absent.</span></span>

<span data-ttu-id="cbf24-3240">**ColumnSet:** estructura CColumnSet que contiene los números de columna en los que se devolverán las propiedades de CPidMapper.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3240">**ColumnSet**: A CColumnSet structure containing the column numbers in which the properties of CPidMapper is to be returned.</span></span>

<span data-ttu-id="cbf24-3241">**CRestrictionPresent:** campo de bytes que indica si el campo Restricción está presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3241">**CRestrictionPresent**: A byte field indicating if the Restriction field is present.</span></span> <span data-ttu-id="cbf24-3242">Si se establece en cualquier valor distinto de cero, el campo Restricción DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3242">If set to any nonzero value, the Restriction field MUST be present.</span></span> <span data-ttu-id="cbf24-3243">Si se establece en 0x00, la restricción DEBE estar ausente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3243">If set to 0x00, Restriction MUST be absent.</span></span>

<span data-ttu-id="cbf24-3244">**Restricción:** estructura CRestriction que contiene el árbol de comandos de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3244">**Restriction**: A CRestriction structure containing the command tree of the query.</span></span>

<span data-ttu-id="cbf24-3245">**CSortSetPresent:** campo de bytes que indica si el campo SortSet está presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3245">**CSortSetPresent**: A byte field indicating if the SortSet field is present.</span></span> <span data-ttu-id="cbf24-3246">Si se establece en cualquier valor distinto de cero, el campo SortSet DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3246">If set to any nonzero value, the SortSet field MUST be present.</span></span> <span data-ttu-id="cbf24-3247">Si se establece en 0x00, SortSet DEBE estar ausente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3247">If set to 0x00, SortSet MUST be absent.</span></span>

<span data-ttu-id="cbf24-3248">**SortSet:** una estructura CSortSet que indica el criterio de ordenación de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3248">**SortSet**: A CSortSet structure indicating the sort order of the query.</span></span>

<span data-ttu-id="cbf24-3249">**CCategorizationSetPresent:** campo de bytes que indica si el campo CCategorizationSet está presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3249">**CCategorizationSetPresent**: A byte field indicating if the CCategorizationSet field is present.</span></span> <span data-ttu-id="cbf24-3250">Si se establece en cualquier valor distinto de cero, el campo CCategorizationSet DEBE estar presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3250">If set to any nonzero value, the CCategorizationSet field MUST be present.</span></span> <span data-ttu-id="cbf24-3251">Si se establece en 0x00, CCategorizationSet DEBE estar ausente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3251">If set to 0x00, CCategorizationSet MUST be absent.</span></span>

<span data-ttu-id="cbf24-3252">**CCategorizationSet:** estructura CCategorizationSet que contiene los grupos de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3252">**CCategorizationSet**: A CCategorizationSet structure that contains the groups for the query.</span></span>

<span data-ttu-id="cbf24-3253">**RowSetProperties:** estructura CRowsetProperties que proporciona información de configuración para la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3253">**RowSetProperties**: A CRowsetProperties structure providing configuration information for the query.</span></span>

<span data-ttu-id="cbf24-3254">**PidMapper:** una estructura CPidMapper que contiene las propiedades que se devuelven en un conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3254">**PidMapper**: A CPidMapper structure containing properties to return in a rowset.</span></span>

### <a name="2239-cpmcreatequeryout"></a><span data-ttu-id="cbf24-3255">2.2.3.9 CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-3255">2.2.3.9 CPMCreateQueryOut</span></span>

<span data-ttu-id="cbf24-3256">El mensaje CPMCreateQueryOut contiene una respuesta a un mensaje CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3256">The CPMCreateQueryOut message contains a response to a CPMCreateQueryIn message.</span></span>

<span data-ttu-id="cbf24-3257">El formato del mensaje CPMCreateQueryOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3257">The format of the CPMCreateQueryOut message that follows the header is:</span></span>



<span data-ttu-id="cbf24-3258">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3258">0</span></span>

<span data-ttu-id="cbf24-3259">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3259">1</span></span>

<span data-ttu-id="cbf24-3260">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3260">2</span></span>

<span data-ttu-id="cbf24-3261">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3261">3</span></span>

<span data-ttu-id="cbf24-3262">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3262">4</span></span>

<span data-ttu-id="cbf24-3263">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3263">5</span></span>

<span data-ttu-id="cbf24-3264">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3264">6</span></span>

<span data-ttu-id="cbf24-3265">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3265">7</span></span>

<span data-ttu-id="cbf24-3266">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3266">8</span></span>

<span data-ttu-id="cbf24-3267">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3267">9</span></span>

<span data-ttu-id="cbf24-3268">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3268">1</span></span><br/> <span data-ttu-id="cbf24-3269">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3269">0</span></span><br/>

<span data-ttu-id="cbf24-3270">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3270">1</span></span>

<span data-ttu-id="cbf24-3271">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3271">2</span></span>

<span data-ttu-id="cbf24-3272">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3272">3</span></span>

<span data-ttu-id="cbf24-3273">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3273">4</span></span>

<span data-ttu-id="cbf24-3274">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3274">5</span></span>

<span data-ttu-id="cbf24-3275">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3275">6</span></span>

<span data-ttu-id="cbf24-3276">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3276">7</span></span>

<span data-ttu-id="cbf24-3277">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3277">8</span></span>

<span data-ttu-id="cbf24-3278">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3278">9</span></span>

<span data-ttu-id="cbf24-3279">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3279">2</span></span><br/> <span data-ttu-id="cbf24-3280">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3280">0</span></span><br/>

<span data-ttu-id="cbf24-3281">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3281">1</span></span>

<span data-ttu-id="cbf24-3282">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3282">2</span></span>

<span data-ttu-id="cbf24-3283">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3283">3</span></span>

<span data-ttu-id="cbf24-3284">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3284">4</span></span>

<span data-ttu-id="cbf24-3285">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3285">5</span></span>

<span data-ttu-id="cbf24-3286">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3286">6</span></span>

<span data-ttu-id="cbf24-3287">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3287">7</span></span>

<span data-ttu-id="cbf24-3288">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3288">8</span></span>

<span data-ttu-id="cbf24-3289">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3289">9</span></span>

<span data-ttu-id="cbf24-3290">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3290">3</span></span><br/> <span data-ttu-id="cbf24-3291">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3291">0</span></span><br/>

<span data-ttu-id="cbf24-3292">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3292">1</span></span>

<span data-ttu-id="cbf24-3293">\_fTrueSequential</span><span class="sxs-lookup"><span data-stu-id="cbf24-3293">\_fTrueSequential</span></span>

<span data-ttu-id="cbf24-3294">\_fWorkIdUnique</span><span class="sxs-lookup"><span data-stu-id="cbf24-3294">\_fWorkIdUnique</span></span>

<span data-ttu-id="cbf24-3295">aCursors</span><span class="sxs-lookup"><span data-stu-id="cbf24-3295">aCursors</span></span>



 

<span data-ttu-id="cbf24-3296">**\_ fTrueSequential:** un valor booleano informativo que indica si se puede esperar que la consulta proporcione resultados más rápido.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3296">**\_fTrueSequential**: An informative boolean value indicating if the query can be expected to provide results faster.</span></span> <span data-ttu-id="cbf24-3297">Cuando se establece en 0x00000001 para la consulta proporcionada en CPMCreateQueryIn, el servidor puede usar el índice de forma que los resultados de la consulta probablemente se entreguen más rápido.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3297">When set to 0x00000001 for the query provided in CPMCreateQueryIn, the server can use the index in such a way that query results will likely be delivered faster.</span></span> <span data-ttu-id="cbf24-3298">Cuando se establece en 0x00000000, habría una latencia mayor en la entrega de los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3298">When set to 0x00000000, there would be a bigger latency in delivering query results.</span></span> <span data-ttu-id="cbf24-3299">NO DEBE establecerse en ningún otro valor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3299">MUST not be set to any other value.</span></span>

<span data-ttu-id="cbf24-3300">**\_ fWorkIdUnique:** valor booleano que indica si los identificadores de documento a los que apuntan los cursores son únicos en los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3300">**\_fWorkIdUnique**: A boolean value indicating if the document identifiers pointed by the cursors are unique throughout query results.</span></span> <span data-ttu-id="cbf24-3301">Si se establece en 0x00000001, los identificadores son únicos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3301">If set to 0x00000001, the identifiers are unique.</span></span> <span data-ttu-id="cbf24-3302">Si se establece en 0x00000000, son únicos solo en todo el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3302">If set to 0x00000000, they are unique only throughout the rowset.</span></span>

<span data-ttu-id="cbf24-3303">**aCursors:** matriz de enteros sin signo de 32 bits que representan los identificadores de los cursores, con el número de elementos igual al número de categorías del campo CategorizationSet del mensaje CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3303">**aCursors**: An array of 32-bit unsigned integers representing the handles to cursors, with the number of elements equal to the number of categories in the CategorizationSet field of CPMCreateQueryIn message.</span></span>

### <a name="22310-cpmgetquerystatusin"></a><span data-ttu-id="cbf24-3304">2.2.3.10 CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-3304">2.2.3.10 CPMGetQueryStatusIn</span></span>

<span data-ttu-id="cbf24-3305">El mensaje CPMGetQueryStatusIn solicita el estado de una consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3305">The CPMGetQueryStatusIn message requests the status of a query.</span></span> <span data-ttu-id="cbf24-3306">El formato del mensaje CPMGetQueryStatusIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3306">The format of the CPMGetQueryStatusIn message that follows the header is:</span></span>



<span data-ttu-id="cbf24-3307">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3307">0</span></span>

<span data-ttu-id="cbf24-3308">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3308">1</span></span>

<span data-ttu-id="cbf24-3309">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3309">2</span></span>

<span data-ttu-id="cbf24-3310">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3310">3</span></span>

<span data-ttu-id="cbf24-3311">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3311">4</span></span>

<span data-ttu-id="cbf24-3312">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3312">5</span></span>

<span data-ttu-id="cbf24-3313">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3313">6</span></span>

<span data-ttu-id="cbf24-3314">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3314">7</span></span>

<span data-ttu-id="cbf24-3315">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3315">8</span></span>

<span data-ttu-id="cbf24-3316">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3316">9</span></span>

<span data-ttu-id="cbf24-3317">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3317">1</span></span><br/> <span data-ttu-id="cbf24-3318">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3318">0</span></span><br/>

<span data-ttu-id="cbf24-3319">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3319">1</span></span>

<span data-ttu-id="cbf24-3320">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3320">2</span></span>

<span data-ttu-id="cbf24-3321">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3321">3</span></span>

<span data-ttu-id="cbf24-3322">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3322">4</span></span>

<span data-ttu-id="cbf24-3323">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3323">5</span></span>

<span data-ttu-id="cbf24-3324">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3324">6</span></span>

<span data-ttu-id="cbf24-3325">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3325">7</span></span>

<span data-ttu-id="cbf24-3326">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3326">8</span></span>

<span data-ttu-id="cbf24-3327">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3327">9</span></span>

<span data-ttu-id="cbf24-3328">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3328">2</span></span><br/> <span data-ttu-id="cbf24-3329">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3329">0</span></span><br/>

<span data-ttu-id="cbf24-3330">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3330">1</span></span>

<span data-ttu-id="cbf24-3331">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3331">2</span></span>

<span data-ttu-id="cbf24-3332">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3332">3</span></span>

<span data-ttu-id="cbf24-3333">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3333">4</span></span>

<span data-ttu-id="cbf24-3334">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3334">5</span></span>

<span data-ttu-id="cbf24-3335">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3335">6</span></span>

<span data-ttu-id="cbf24-3336">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3336">7</span></span>

<span data-ttu-id="cbf24-3337">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3337">8</span></span>

<span data-ttu-id="cbf24-3338">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3338">9</span></span>

<span data-ttu-id="cbf24-3339">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3339">3</span></span><br/> <span data-ttu-id="cbf24-3340">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3340">0</span></span><br/>

<span data-ttu-id="cbf24-3341">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3341">1</span></span>

<span data-ttu-id="cbf24-3342">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cbf24-3342">\_hCursor</span></span>



 

<span data-ttu-id="cbf24-3343">**\_ hCursor:** entero de 32 bits sin signo que representa el identificador del mensaje CPMCreateQueryOut que identifica la consulta para la que se va a recuperar información de estado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3343">**\_hCursor**: A 32-bit unsigned integer representing the handle from CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

### <a name="22311-cpmgetquerystatusout"></a><span data-ttu-id="cbf24-3344">2.2.3.11 CPMGetQueryStatusOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-3344">2.2.3.11 CPMGetQueryStatusOut</span></span>

<span data-ttu-id="cbf24-3345">El mensaje CPMGetQueryStatusOut responde a un mensaje CPMGetQueryStatusIn con el estado de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3345">The CPMGetQueryStatusOut message replies to a CPMGetQueryStatusIn message with the status of the query.</span></span> <span data-ttu-id="cbf24-3346">El formato del mensaje CPMGetQueryStatusOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3346">The format of the CPMGetQueryStatusOut message that follows the header is:</span></span>



<span data-ttu-id="cbf24-3347">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3347">0</span></span>

<span data-ttu-id="cbf24-3348">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3348">1</span></span>

<span data-ttu-id="cbf24-3349">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3349">2</span></span>

<span data-ttu-id="cbf24-3350">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3350">3</span></span>

<span data-ttu-id="cbf24-3351">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3351">4</span></span>

<span data-ttu-id="cbf24-3352">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3352">5</span></span>

<span data-ttu-id="cbf24-3353">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3353">6</span></span>

<span data-ttu-id="cbf24-3354">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3354">7</span></span>

<span data-ttu-id="cbf24-3355">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3355">8</span></span>

<span data-ttu-id="cbf24-3356">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3356">9</span></span>

<span data-ttu-id="cbf24-3357">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3357">1</span></span><br/> <span data-ttu-id="cbf24-3358">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3358">0</span></span><br/>

<span data-ttu-id="cbf24-3359">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3359">1</span></span>

<span data-ttu-id="cbf24-3360">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3360">2</span></span>

<span data-ttu-id="cbf24-3361">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3361">3</span></span>

<span data-ttu-id="cbf24-3362">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3362">4</span></span>

<span data-ttu-id="cbf24-3363">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3363">5</span></span>

<span data-ttu-id="cbf24-3364">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3364">6</span></span>

<span data-ttu-id="cbf24-3365">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3365">7</span></span>

<span data-ttu-id="cbf24-3366">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3366">8</span></span>

<span data-ttu-id="cbf24-3367">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3367">9</span></span>

<span data-ttu-id="cbf24-3368">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3368">2</span></span><br/> <span data-ttu-id="cbf24-3369">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3369">0</span></span><br/>

<span data-ttu-id="cbf24-3370">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3370">1</span></span>

<span data-ttu-id="cbf24-3371">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3371">2</span></span>

<span data-ttu-id="cbf24-3372">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3372">3</span></span>

<span data-ttu-id="cbf24-3373">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3373">4</span></span>

<span data-ttu-id="cbf24-3374">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3374">5</span></span>

<span data-ttu-id="cbf24-3375">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3375">6</span></span>

<span data-ttu-id="cbf24-3376">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3376">7</span></span>

<span data-ttu-id="cbf24-3377">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3377">8</span></span>

<span data-ttu-id="cbf24-3378">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3378">9</span></span>

<span data-ttu-id="cbf24-3379">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3379">3</span></span><br/> <span data-ttu-id="cbf24-3380">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3380">0</span></span><br/>

<span data-ttu-id="cbf24-3381">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3381">1</span></span>

<span data-ttu-id="cbf24-3382">\_Estado</span><span class="sxs-lookup"><span data-stu-id="cbf24-3382">\_Status</span></span>



 

<span data-ttu-id="cbf24-3383">**\_ Estado:** máscara de bits de valores definidos en las tablas siguientes, que describe la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3383">**\_Status**: A bitmask of values defined in the tables below, that describes the query.</span></span>

<span data-ttu-id="cbf24-3384">En la tabla siguiente se enumeran los valores STAT obtenidos mediante la realización de una operación AND bit a bit \_ \* en Status con \_ 0x00000007.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3384">The following table lists STAT\_\* values obtained by performing a bitwise AND operation on \_Status with 0x00000007.</span></span> <span data-ttu-id="cbf24-3385">El resultado DEBE ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3385">The result MUST be one of the following:</span></span>



| <span data-ttu-id="cbf24-3386">Constante</span><span class="sxs-lookup"><span data-stu-id="cbf24-3386">Constant</span></span>                 | <span data-ttu-id="cbf24-3387">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-3387">Meaning</span></span>                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-3388">Stat \_ BUSY 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-3388">STAT\_BUSY 0x00000000</span></span>    | <span data-ttu-id="cbf24-3389">La consulta asincrónica todavía se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3389">The asynchronous query is still running.</span></span>                                          |
| <span data-ttu-id="cbf24-3390">ERROR \_ DE STAT 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-3390">STAT\_ERROR 0x00000001</span></span>   | <span data-ttu-id="cbf24-3391">La consulta está en estado de error.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3391">The query is in an error state.</span></span>                                                   |
| <span data-ttu-id="cbf24-3392">STAT \_ DONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbf24-3392">STAT\_DONE 0x00000002</span></span>    | <span data-ttu-id="cbf24-3393">La consulta se ha completado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3393">The query is complete.</span></span>                                                            |
| <span data-ttu-id="cbf24-3394">Actualización \_ de STAT 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cbf24-3394">STAT\_REFRESH 0x00000003</span></span> | <span data-ttu-id="cbf24-3395">La consulta está completa, pero las actualizaciones están generando cálculos de consulta adicionales.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3395">The query is complete, but updates are resulting in additional query computation.</span></span> |



 

<span data-ttu-id="cbf24-3396">En la tabla siguiente se enumeran los bits stat \_ \* adicionales que se pueden establecer de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3396">The following table lists additional STAT\_\* bits that can be set independently.</span></span>



| <span data-ttu-id="cbf24-3397">Constante</span><span class="sxs-lookup"><span data-stu-id="cbf24-3397">Constant</span></span>                                    | <span data-ttu-id="cbf24-3398">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-3398">Meaning</span></span>                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf24-3399">STAT \_ NOISE \_ WORDS 0x00000010</span><span class="sxs-lookup"><span data-stu-id="cbf24-3399">STAT\_NOISE\_WORDS 0x00000010</span></span>               | <span data-ttu-id="cbf24-3400">Las palabras ruidosas se reemplazaron por caracteres comodín en la consulta de contenido.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3400">Noise words were replaced by wildcard characters in the content query.</span></span>                                                              |
| <span data-ttu-id="cbf24-3401">CONTENIDO \_ DE STAT NO ACTUALIZADO \_ \_ \_ 0x00000020</span><span class="sxs-lookup"><span data-stu-id="cbf24-3401">STAT\_CONTENT\_OUT\_OF\_DATE 0x00000020</span></span>     | <span data-ttu-id="cbf24-3402">Los resultados de la consulta podrían ser incorrectos porque la consulta implicaba archivos modificados, pero sin indexar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3402">The results of the query might be incorrect because the query involved modified, but un-indexed, files.</span></span>                             |
| <span data-ttu-id="cbf24-3403">ACTUALIZACIÓN \_ DE \_ ESTADÍSTICAS INCOMPLETA 0x00000040</span><span class="sxs-lookup"><span data-stu-id="cbf24-3403">STAT\_REFRESH\_INCOMPLETE 0x00000040</span></span>        | <span data-ttu-id="cbf24-3404">Los resultados de la consulta podrían ser incorrectos porque la consulta implicaba archivos modificados y indexados cuyo contenido no se incluyó.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3404">The results of the query might be incorrect because the query involved modified and re-indexed files whose content wasn't included.</span></span> |
| <span data-ttu-id="cbf24-3405">CONSULTA \_ DE CONTENIDO DE STAT INCOMPLETA \_ \_ 0x00000080</span><span class="sxs-lookup"><span data-stu-id="cbf24-3405">STAT\_CONTENT\_QUERY\_INCOMPLETE 0x00000080</span></span> | <span data-ttu-id="cbf24-3406">La consulta de contenido era demasiado compleja para completar o enumeración necesaria en lugar de usar el índice de contenido.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3406">The content query was too complex to complete or required enumeration instead of use of the content index.</span></span>                          |
| <span data-ttu-id="cbf24-3407">SE \_ HA SUPERADO EL LÍMITE DE TIEMPO DE \_ \_ 0X00000100</span><span class="sxs-lookup"><span data-stu-id="cbf24-3407">STAT\_TIME\_LIMIT\_EXCEEDED 0x00000100</span></span>      | <span data-ttu-id="cbf24-3408">Los resultados de la consulta pueden ser incorrectos porque el tiempo de ejecución de la consulta alcanzó el tiempo máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3408">The results of the query might be incorrect because the query execution time reached the maximum allowable time.</span></span>                    |



 

### <a name="22312-cpmgetquerystatusexin"></a><span data-ttu-id="cbf24-3409">2.2.3.12 CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-3409">2.2.3.12 CPMGetQueryStatusExIn</span></span>

<span data-ttu-id="cbf24-3410">El mensaje CPMGetQueryStatusExIn solicita el estado de una consulta e información adicional, como el número de documentos que se han indexado, el número de documentos que quedan por indexar, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3410">The CPMGetQueryStatusExIn message requests the status of a query and additional information, such as the number of documents that have been indexed, the number of documents remaining to be indexed, and so on.</span></span> <span data-ttu-id="cbf24-3411">El formato del mensaje CPMGetQueryStatusExIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3411">The format of the CPMGetQueryStatusExIn message that follows the header is:</span></span>



<span data-ttu-id="cbf24-3412">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3412">0</span></span>

<span data-ttu-id="cbf24-3413">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3413">1</span></span>

<span data-ttu-id="cbf24-3414">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3414">2</span></span>

<span data-ttu-id="cbf24-3415">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3415">3</span></span>

<span data-ttu-id="cbf24-3416">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3416">4</span></span>

<span data-ttu-id="cbf24-3417">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3417">5</span></span>

<span data-ttu-id="cbf24-3418">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3418">6</span></span>

<span data-ttu-id="cbf24-3419">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3419">7</span></span>

<span data-ttu-id="cbf24-3420">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3420">8</span></span>

<span data-ttu-id="cbf24-3421">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3421">9</span></span>

<span data-ttu-id="cbf24-3422">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3422">1</span></span><br/> <span data-ttu-id="cbf24-3423">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3423">0</span></span><br/>

<span data-ttu-id="cbf24-3424">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3424">1</span></span>

<span data-ttu-id="cbf24-3425">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3425">2</span></span>

<span data-ttu-id="cbf24-3426">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3426">3</span></span>

<span data-ttu-id="cbf24-3427">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3427">4</span></span>

<span data-ttu-id="cbf24-3428">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3428">5</span></span>

<span data-ttu-id="cbf24-3429">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3429">6</span></span>

<span data-ttu-id="cbf24-3430">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3430">7</span></span>

<span data-ttu-id="cbf24-3431">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3431">8</span></span>

<span data-ttu-id="cbf24-3432">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3432">9</span></span>

<span data-ttu-id="cbf24-3433">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3433">2</span></span><br/> <span data-ttu-id="cbf24-3434">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3434">0</span></span><br/>

<span data-ttu-id="cbf24-3435">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3435">1</span></span>

<span data-ttu-id="cbf24-3436">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3436">2</span></span>

<span data-ttu-id="cbf24-3437">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3437">3</span></span>

<span data-ttu-id="cbf24-3438">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3438">4</span></span>

<span data-ttu-id="cbf24-3439">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3439">5</span></span>

<span data-ttu-id="cbf24-3440">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3440">6</span></span>

<span data-ttu-id="cbf24-3441">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3441">7</span></span>

<span data-ttu-id="cbf24-3442">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3442">8</span></span>

<span data-ttu-id="cbf24-3443">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3443">9</span></span>

<span data-ttu-id="cbf24-3444">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3444">3</span></span><br/> <span data-ttu-id="cbf24-3445">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3445">0</span></span><br/>

<span data-ttu-id="cbf24-3446">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3446">1</span></span>

<span data-ttu-id="cbf24-3447">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cbf24-3447">\_hCursor</span></span>

<span data-ttu-id="cbf24-3448">\_Bmk</span><span class="sxs-lookup"><span data-stu-id="cbf24-3448">\_bmk</span></span>



 

<span data-ttu-id="cbf24-3449">**\_ hCursor:** valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut que identifica la consulta para la que se va a recuperar información de estado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3449">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve status information.</span></span>

<span data-ttu-id="cbf24-3450">**\_ bmk:** valor de 32 bits que indica el identificador de un marcador cuya posición se debe recuperar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3450">**\_bmk**: A 32-bit value indicating the handle of a bookmark whose position should be retrieved.</span></span>

### <a name="22313-cpmgetquerystatusexout"></a><span data-ttu-id="cbf24-3451">2.2.3.13 CPMGetQueryStatusExOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-3451">2.2.3.13 CPMGetQueryStatusExOut</span></span>

<span data-ttu-id="cbf24-3452">El mensaje CPMGetQueryStatusExOut responde a un mensaje CPMGetQueryStatusExIn con el estado de la consulta y otra información de estado, como se describe en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3452">The CPMGetQueryStatusExOut message replies to a CPMGetQueryStatusExIn message with both the status of the query and other status information, as outlined in the diagram below.</span></span> <span data-ttu-id="cbf24-3453">El formato del mensaje CPMGetQueryStatusExOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3453">The format of the CPMGetQueryStatusExOut message that follows the header is:</span></span>



<span data-ttu-id="cbf24-3454">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3454">0</span></span>

<span data-ttu-id="cbf24-3455">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3455">1</span></span>

<span data-ttu-id="cbf24-3456">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3456">2</span></span>

<span data-ttu-id="cbf24-3457">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3457">3</span></span>

<span data-ttu-id="cbf24-3458">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3458">4</span></span>

<span data-ttu-id="cbf24-3459">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3459">5</span></span>

<span data-ttu-id="cbf24-3460">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3460">6</span></span>

<span data-ttu-id="cbf24-3461">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3461">7</span></span>

<span data-ttu-id="cbf24-3462">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3462">8</span></span>

<span data-ttu-id="cbf24-3463">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3463">9</span></span>

<span data-ttu-id="cbf24-3464">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3464">1</span></span><br/> <span data-ttu-id="cbf24-3465">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3465">0</span></span><br/>

<span data-ttu-id="cbf24-3466">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3466">1</span></span>

<span data-ttu-id="cbf24-3467">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3467">2</span></span>

<span data-ttu-id="cbf24-3468">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3468">3</span></span>

<span data-ttu-id="cbf24-3469">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3469">4</span></span>

<span data-ttu-id="cbf24-3470">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3470">5</span></span>

<span data-ttu-id="cbf24-3471">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3471">6</span></span>

<span data-ttu-id="cbf24-3472">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3472">7</span></span>

<span data-ttu-id="cbf24-3473">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3473">8</span></span>

<span data-ttu-id="cbf24-3474">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3474">9</span></span>

<span data-ttu-id="cbf24-3475">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3475">2</span></span><br/> <span data-ttu-id="cbf24-3476">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3476">0</span></span><br/>

<span data-ttu-id="cbf24-3477">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3477">1</span></span>

<span data-ttu-id="cbf24-3478">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3478">2</span></span>

<span data-ttu-id="cbf24-3479">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3479">3</span></span>

<span data-ttu-id="cbf24-3480">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3480">4</span></span>

<span data-ttu-id="cbf24-3481">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3481">5</span></span>

<span data-ttu-id="cbf24-3482">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3482">6</span></span>

<span data-ttu-id="cbf24-3483">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3483">7</span></span>

<span data-ttu-id="cbf24-3484">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3484">8</span></span>

<span data-ttu-id="cbf24-3485">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3485">9</span></span>

<span data-ttu-id="cbf24-3486">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3486">3</span></span><br/> <span data-ttu-id="cbf24-3487">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3487">0</span></span><br/>

<span data-ttu-id="cbf24-3488">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3488">1</span></span>

<span data-ttu-id="cbf24-3489">\_Estado</span><span class="sxs-lookup"><span data-stu-id="cbf24-3489">\_Status</span></span>

<span data-ttu-id="cbf24-3490">\_cFilteredDocuments</span><span class="sxs-lookup"><span data-stu-id="cbf24-3490">\_cFilteredDocuments</span></span>

<span data-ttu-id="cbf24-3491">\_cDocumentsToFilter</span><span class="sxs-lookup"><span data-stu-id="cbf24-3491">\_cDocumentsToFilter</span></span>

<span data-ttu-id="cbf24-3492">\_dwRatioFinishedDenominator</span><span class="sxs-lookup"><span data-stu-id="cbf24-3492">\_dwRatioFinishedDenominator</span></span>

<span data-ttu-id="cbf24-3493">\_dwRatioFinishedNumerator</span><span class="sxs-lookup"><span data-stu-id="cbf24-3493">\_dwRatioFinishedNumerator</span></span>

<span data-ttu-id="cbf24-3494">\_iRowBmk</span><span class="sxs-lookup"><span data-stu-id="cbf24-3494">\_iRowBmk</span></span>

<span data-ttu-id="cbf24-3495">\_cRowsTotal</span><span class="sxs-lookup"><span data-stu-id="cbf24-3495">\_cRowsTotal</span></span>



 

<span data-ttu-id="cbf24-3496">**\_ Estado:** una de las estadísticas \_ \* valores especificados en la sección 2.2.3.11.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3496">**\_Status**: One of the STAT\_\* values specified in Section 2.2.3.11.</span></span>

<span data-ttu-id="cbf24-3497">**\_ cFilteredDocuments:** entero de 32 bits sin signo que indica el número de documentos que se han indexado</span><span class="sxs-lookup"><span data-stu-id="cbf24-3497">**\_cFilteredDocuments**: A 32-bit unsigned integer indicating the number of documents that have been indexed</span></span>

<span data-ttu-id="cbf24-3498">**\_ cDocumentsToFilter:** entero de 32 bits sin signo que indica el número de documentos que quedan por indexar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3498">**\_cDocumentsToFilter**: A 32-bit unsigned integer indicating the number of documents that still remain to be indexed.</span></span>

<span data-ttu-id="cbf24-3499">**\_ dwRatioFinishedDenominator:** entero de 32 bits sin signo que indica el denominador de la proporción de documentos que la consulta ha terminado de procesar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3499">**\_dwRatioFinishedDenominator**: A 32-bit unsigned integer indicating the denominator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="cbf24-3500">**\_ dwRatioFinishedNumerator:** entero de 32 bits sin signo que indica el numerador de la proporción de documentos que la consulta ha terminado de procesar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3500">**\_dwRatioFinishedNumerator**: A 32-bit unsigned integer indicating the numerator of the ratio of documents the query has finished processing.</span></span>

<span data-ttu-id="cbf24-3501">**\_ iRowBmk:** entero de 32 bits sin signo que indica la posición aproximada del marcador en el conjunto de filas en términos de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3501">**\_iRowBmk**: A 32-bit unsigned integer indicating the approximate position of the bookmark in the rowset in terms of rows.</span></span>

<span data-ttu-id="cbf24-3502">**\_ cRowsTotal:** entero de 32 bits sin signo que especifica el número total de filas del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3502">**\_cRowsTotal**: A 32-bit unsigned integer specifying the total number of rows in the rowset.</span></span>

### <a name="22314-cpmsetbindingsin"></a><span data-ttu-id="cbf24-3503">2.2.3.14 CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-3503">2.2.3.14 CPMSetBindingsIn</span></span>

<span data-ttu-id="cbf24-3504">El mensaje CPMSetBindingsIn solicita el enlace de columnas a un conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3504">The CPMSetBindingsIn message requests the binding of columns to a rowset.</span></span> <span data-ttu-id="cbf24-3505">El servidor responderá al mensaje de solicitud CPMSetBindingsIn mediante la sección de encabezado del mensaje CPMBindingsIn con los resultados de la solicitud contenida en el campo \_ de estado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3505">The server will reply to the CPMSetBindingsIn request message using the header section of the CPMBindingsIn message with the results of the request contained in the \_status field.</span></span> <span data-ttu-id="cbf24-3506">El formato del mensaje CPMSetBindingsIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3506">The format of the CPMSetBindingsIn message that follows the header is:</span></span>



<span data-ttu-id="cbf24-3507">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3507">0</span></span>

<span data-ttu-id="cbf24-3508">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3508">1</span></span>

<span data-ttu-id="cbf24-3509">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3509">2</span></span>

<span data-ttu-id="cbf24-3510">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3510">3</span></span>

<span data-ttu-id="cbf24-3511">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3511">4</span></span>

<span data-ttu-id="cbf24-3512">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3512">5</span></span>

<span data-ttu-id="cbf24-3513">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3513">6</span></span>

<span data-ttu-id="cbf24-3514">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3514">7</span></span>

<span data-ttu-id="cbf24-3515">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3515">8</span></span>

<span data-ttu-id="cbf24-3516">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3516">9</span></span>

<span data-ttu-id="cbf24-3517">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3517">1</span></span><br/> <span data-ttu-id="cbf24-3518">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3518">0</span></span><br/>

<span data-ttu-id="cbf24-3519">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3519">1</span></span>

<span data-ttu-id="cbf24-3520">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3520">2</span></span>

<span data-ttu-id="cbf24-3521">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3521">3</span></span>

<span data-ttu-id="cbf24-3522">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3522">4</span></span>

<span data-ttu-id="cbf24-3523">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3523">5</span></span>

<span data-ttu-id="cbf24-3524">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3524">6</span></span>

<span data-ttu-id="cbf24-3525">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3525">7</span></span>

<span data-ttu-id="cbf24-3526">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3526">8</span></span>

<span data-ttu-id="cbf24-3527">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3527">9</span></span>

<span data-ttu-id="cbf24-3528">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3528">2</span></span><br/> <span data-ttu-id="cbf24-3529">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3529">0</span></span><br/>

<span data-ttu-id="cbf24-3530">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3530">1</span></span>

<span data-ttu-id="cbf24-3531">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3531">2</span></span>

<span data-ttu-id="cbf24-3532">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3532">3</span></span>

<span data-ttu-id="cbf24-3533">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3533">4</span></span>

<span data-ttu-id="cbf24-3534">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3534">5</span></span>

<span data-ttu-id="cbf24-3535">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3535">6</span></span>

<span data-ttu-id="cbf24-3536">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3536">7</span></span>

<span data-ttu-id="cbf24-3537">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3537">8</span></span>

<span data-ttu-id="cbf24-3538">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3538">9</span></span>

<span data-ttu-id="cbf24-3539">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3539">3</span></span><br/> <span data-ttu-id="cbf24-3540">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3540">0</span></span><br/>

<span data-ttu-id="cbf24-3541">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3541">1</span></span>

<span data-ttu-id="cbf24-3542">\_hCursor (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3542">\_hCursor (optional)</span></span>

<span data-ttu-id="cbf24-3543">\_cbRow (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3543">\_cbRow (optional)</span></span>

<span data-ttu-id="cbf24-3544">\_cbBindingDesc (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3544">\_cbBindingDesc (optional)</span></span>

<span data-ttu-id="cbf24-3545">\_dummy (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3545">\_dummy (optional)</span></span>

<span data-ttu-id="cbf24-3546">cColumns (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3546">cColumns (optional)</span></span>

<span data-ttu-id="cbf24-3547">aColumns (variable, opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3547">aColumns (variable, optional)</span></span>



 

<span data-ttu-id="cbf24-3548">**\_ hCursor:** valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut que identifica la fila para la que se establecen los enlaces.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3548">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message that identifies the row for which to set bindings.</span></span> <span data-ttu-id="cbf24-3549">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3549">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="cbf24-3550">**\_ cbRow:** entero de 32 bits sin signo que indica el tamaño, en bytes, de una fila.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3550">**\_cbRow**: A 32-bit unsigned integer indicating the size, in bytes, of a row.</span></span> <span data-ttu-id="cbf24-3551">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3551">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="cbf24-3552">**\_ cbBindingDesc:** entero de 32 bits sin signo que indica la longitud, en bytes, de los campos siguientes al \_ campo ficticio.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3552">**\_cbBindingDesc**: A 32-bit unsigned integer indicating the length, in bytes, of the fields following the \_dummy field.</span></span> <span data-ttu-id="cbf24-3553">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3553">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="cbf24-3554">**\_ dummy:** este campo no se usa y DEBE omitirse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3554">**\_dummy**: This field is unused and MUST be ignored.</span></span> <span data-ttu-id="cbf24-3555">Se puede establecer en cualquier valor arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3555">It can be set to any arbitrary value.</span></span> <span data-ttu-id="cbf24-3556">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3556">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="cbf24-3557">**cColumns:** entero de 32 bits sin signo que indica el número de elementos de la matriz aColumns.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3557">**cColumns**: A 32-bit unsigned integer indicating the number of elements in the aColumns array.</span></span> <span data-ttu-id="cbf24-3558">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3558">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="cbf24-3559">**aColumns:** matriz de las estructuras CTableColumn que describen las columnas de una fila del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3559">**aColumns**: An array of the CTableColumn structures describing the columns of a row in the rowset.</span></span> <span data-ttu-id="cbf24-3560">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3560">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span> <span data-ttu-id="cbf24-3561">Las estructuras de la matriz DEBEN estar separadas por 0 a 3 bytes de relleno, de forma que cada estructura tenga una alineación de 4 bytes desde el principio de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3561">Structures in the array MUST be separated by 0 to 3 padding bytes such that each structure has a 4-byte alignment from the beginning of a message.</span></span> <span data-ttu-id="cbf24-3562">Estos bytes de relleno pueden ser cualquier valor arbitrario y DEBEN omitirse al recibirse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3562">Such padding bytes can be any arbitrary value, and MUST be ignored on receipt.</span></span>

### <a name="22315-cpmgetrowsin"></a><span data-ttu-id="cbf24-3563">2.2.3.15 CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-3563">2.2.3.15 CPMGetRowsIn</span></span>

<span data-ttu-id="cbf24-3564">El mensaje CPMGetRowsIn solicita filas de una consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3564">The CPMGetRowsIn message requests rows from a query.</span></span> <span data-ttu-id="cbf24-3565">El formato del mensaje CPMGetRowsIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3565">The format of the CPMGetRowsIn message that follows the header is:</span></span>



<span data-ttu-id="cbf24-3566">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3566">0</span></span>

<span data-ttu-id="cbf24-3567">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3567">1</span></span>

<span data-ttu-id="cbf24-3568">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3568">2</span></span>

<span data-ttu-id="cbf24-3569">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3569">3</span></span>

<span data-ttu-id="cbf24-3570">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3570">4</span></span>

<span data-ttu-id="cbf24-3571">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3571">5</span></span>

<span data-ttu-id="cbf24-3572">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3572">6</span></span>

<span data-ttu-id="cbf24-3573">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3573">7</span></span>

<span data-ttu-id="cbf24-3574">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3574">8</span></span>

<span data-ttu-id="cbf24-3575">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3575">9</span></span>

<span data-ttu-id="cbf24-3576">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3576">1</span></span><br/> <span data-ttu-id="cbf24-3577">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3577">0</span></span><br/>

<span data-ttu-id="cbf24-3578">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3578">1</span></span>

<span data-ttu-id="cbf24-3579">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3579">2</span></span>

<span data-ttu-id="cbf24-3580">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3580">3</span></span>

<span data-ttu-id="cbf24-3581">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3581">4</span></span>

<span data-ttu-id="cbf24-3582">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3582">5</span></span>

<span data-ttu-id="cbf24-3583">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3583">6</span></span>

<span data-ttu-id="cbf24-3584">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3584">7</span></span>

<span data-ttu-id="cbf24-3585">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3585">8</span></span>

<span data-ttu-id="cbf24-3586">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3586">9</span></span>

<span data-ttu-id="cbf24-3587">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3587">2</span></span><br/> <span data-ttu-id="cbf24-3588">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3588">0</span></span><br/>

<span data-ttu-id="cbf24-3589">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3589">1</span></span>

<span data-ttu-id="cbf24-3590">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3590">2</span></span>

<span data-ttu-id="cbf24-3591">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3591">3</span></span>

<span data-ttu-id="cbf24-3592">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3592">4</span></span>

<span data-ttu-id="cbf24-3593">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3593">5</span></span>

<span data-ttu-id="cbf24-3594">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3594">6</span></span>

<span data-ttu-id="cbf24-3595">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3595">7</span></span>

<span data-ttu-id="cbf24-3596">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3596">8</span></span>

<span data-ttu-id="cbf24-3597">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3597">9</span></span>

<span data-ttu-id="cbf24-3598">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3598">3</span></span><br/> <span data-ttu-id="cbf24-3599">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3599">0</span></span><br/>

<span data-ttu-id="cbf24-3600">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3600">1</span></span>

<span data-ttu-id="cbf24-3601">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cbf24-3601">\_hCursor</span></span>

<span data-ttu-id="cbf24-3602">\_cRowsToTransfer</span><span class="sxs-lookup"><span data-stu-id="cbf24-3602">\_cRowsToTransfer</span></span>

<span data-ttu-id="cbf24-3603">\_cbRowWidth</span><span class="sxs-lookup"><span data-stu-id="cbf24-3603">\_cbRowWidth</span></span>

<span data-ttu-id="cbf24-3604">\_cbSeek</span><span class="sxs-lookup"><span data-stu-id="cbf24-3604">\_cbSeek</span></span>

<span data-ttu-id="cbf24-3605">\_cbReserved</span><span class="sxs-lookup"><span data-stu-id="cbf24-3605">\_cbReserved</span></span>

<span data-ttu-id="cbf24-3606">\_cbReadBuffer</span><span class="sxs-lookup"><span data-stu-id="cbf24-3606">\_cbReadBuffer</span></span>

<span data-ttu-id="cbf24-3607">\_ulClientBase</span><span class="sxs-lookup"><span data-stu-id="cbf24-3607">\_ulClientBase</span></span>

<span data-ttu-id="cbf24-3608">\_fBwdFetch</span><span class="sxs-lookup"><span data-stu-id="cbf24-3608">\_fBwdFetch</span></span>

<span data-ttu-id="cbf24-3609">eType</span><span class="sxs-lookup"><span data-stu-id="cbf24-3609">eType</span></span>

<span data-ttu-id="cbf24-3610">\_chapt</span><span class="sxs-lookup"><span data-stu-id="cbf24-3610">\_chapt</span></span>

<span data-ttu-id="cbf24-3611">SeekDescription</span><span class="sxs-lookup"><span data-stu-id="cbf24-3611">SeekDescription</span></span>

<span data-ttu-id="cbf24-3612">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-3612">...</span></span>

<span data-ttu-id="cbf24-3613">... (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3613">... (variable)</span></span>



 

<span data-ttu-id="cbf24-3614">**\_ hCursor:** valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut que identifica la consulta para la que se recuperan las filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3614">**\_hCursor**: A 32-bit value representing the handle from the CPMCreateQueryOut message identifying the query for which to retrieve rows.</span></span>

<span data-ttu-id="cbf24-3615">**\_ cRowsToTransfer:** entero de 32 bits sin signo que indica el número máximo de filas que el cliente desea recibir en respuesta a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3615">**\_cRowsToTransfer**: A 32-bit unsigned integer indicating the maximum number of rows the client wishes to receive in response to this message.</span></span>

<span data-ttu-id="cbf24-3616">**\_ cbRowWidth:** entero de 32 bits sin signo que indica la longitud de una fila, en bytes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3616">**\_cbRowWidth**: A 32-bit unsigned integer indicating the length of a row, in bytes.</span></span>

<span data-ttu-id="cbf24-3617">**\_ cbSeek:** entero de 32 bits sin signo que indica el tamaño del mensaje que comienza por eType.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3617">**\_cbSeek**: A 32-bit unsigned integer indicating the size of the message beginning with eType.</span></span>

<span data-ttu-id="cbf24-3618">**\_ cbReserved:** entero de 32 bits sin signo que indica el tamaño, en bytes, de un mensaje CPMGetRowsOut (sin los campos Rows y SeekDescriptions).</span><span class="sxs-lookup"><span data-stu-id="cbf24-3618">**\_cbReserved**: A 32-bit unsigned integer indicating the size, in bytes, of a CPMGetRowsOut message (without the Rows and SeekDescriptions fields).</span></span> <span data-ttu-id="cbf24-3619">Este valor de este campo se agrega al valor del campo cbSeek y, a continuación, se usará para calcular el desplazamiento del campo Rows en el mensaje \_ CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3619">This value in this field is added to the value of the \_cbSeek field, and then is to be used to calculate the offset of Rows field in CPMGetRowsOut message.</span></span>

<span data-ttu-id="cbf24-3620">**\_ cbReadBuffer:** entero de 32 bits sin signo que DEBE establecerse en el máximo del valor de cbRowWidth o 1000 veces el valor de \_ cRowsToTransfer, redondeado al múltiplo de \_ 512 bytes más cercano.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3620">**\_cbReadBuffer**: A 32-bit unsigned integer which MUST be set to the maximum of the value of \_cbRowWidth or 1000 times the value of \_cRowsToTransfer, rounded up to the nearest 512 byte multiple.</span></span> <span data-ttu-id="cbf24-3621">El valor NO DEBE superar 0x00004000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3621">The value MUST NOT exceed 0x00004000.</span></span>

<span data-ttu-id="cbf24-3622">**\_ ulClientBase:** entero de 32 bits sin signo que indica el valor base que se usará para los cálculos de puntero en el búfer de fila.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3622">**\_ulClientBase**: A 32-bit unsigned integer indicating the base value to use for pointer calculations in the row buffer.</span></span> <span data-ttu-id="cbf24-3623">Si se usan desplazamientos de 64 bits, el campo reserved2 del encabezado del mensaje se usa como los 32 bits superiores y ulClientBase como los 32 bits inferiores de un valor de \_ 64 bits.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3623">If 64-bit offsets are being used, then the reserved2 field of the message header is used as the upper 32-bits and \_ulClientBase as the lower 32-bits of a 64-bit value.</span></span> <span data-ttu-id="cbf24-3624">Consulte la sección 2.2.3.16 para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3624">See section 2.2.3.16 for details.</span></span>

<span data-ttu-id="cbf24-3625">**\_ fBwdFetch:** entero de 32 bits sin signo que indica el orden en el que se capturan las filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3625">**\_fBwdFetch**: A 32-bit unsigned integer indicating the order in which to fetch the rows.</span></span> <span data-ttu-id="cbf24-3626">Si se establece 0x00000001, las filas se capturarán en orden inverso.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3626">If set to 0x00000001, the rows are to be fetched in reverse order.</span></span> <span data-ttu-id="cbf24-3627">Si se establece en 0x00000000, las filas se capturarán en orden de avance.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3627">If set to 0x00000000, the rows are to be fetched in forward order.</span></span> <span data-ttu-id="cbf24-3628">NO DEBE establecerse en ningún otro valor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3628">MUST NOT be set to any other values.</span></span>

<span data-ttu-id="cbf24-3629">**eType:** entero de 32 bits sin signo que contiene uno de los valores siguientes para indicar el tipo de operación que se debe realizar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3629">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of operation to perform.</span></span>



| <span data-ttu-id="cbf24-3630">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-3630">Value</span></span>                         | <span data-ttu-id="cbf24-3631">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-3631">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="cbf24-3632">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-3632">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="cbf24-3633">SeekDescription contiene una estructura CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3633">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="cbf24-3634">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbf24-3634">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="cbf24-3635">SeekDescription contiene una estructura CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3635">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="cbf24-3636">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cbf24-3636">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="cbf24-3637">SeekDescription contiene una estructura CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3637">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="cbf24-3638">ERowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cbf24-3638">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="cbf24-3639">SeekDescription contiene una estructura CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3639">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="cbf24-3640">**\_ chapt:** valor de 32 bits que representa el identificador del capítulo del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3640">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="cbf24-3641">**SeekDescription:** este campo DEBE contener una estructura del tipo indicado por el valor eType.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3641">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType value.</span></span>

### <a name="22316-cpmgetrowsout"></a><span data-ttu-id="cbf24-3642">2.2.3.16 CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-3642">2.2.3.16 CPMGetRowsOut</span></span>

<span data-ttu-id="cbf24-3643">El mensaje CPMGetRowsOut responde a un mensaje CPMGetRowsIn con las filas de una consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3643">The CPMGetRowsOut message replies to a CPMGetRowsIn message with the rows of a query.</span></span> <span data-ttu-id="cbf24-3644">Los servidores DEBEN dar formato a los desplazamientos a los tipos de datos de longitud variable en el campo Filas de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3644">Servers MUST format offsets to variable length data types in the Rows field as follows:</span></span>

-   <span data-ttu-id="cbf24-3645">El cliente indicó que era un sistema de 32 bits (0x00000008 o menos en el campo iClientVersion de CPMConnectIn): los desplazamientos son enteros de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3645">Client indicated it was a 32-bit system (0x00000008 or less in the iClientVersion field of CPMConnectIn): Offsets are 32-bit integers.</span></span>
-   <span data-ttu-id="cbf24-3646">El cliente indicó que era un sistema de 64 bits (iClientVersion > 0x00000008 en CPMConnectIn) y Server indicó que era un sistema de 32 bits (serverVersion establecido en \_ \_ 0x00000007 en CPMConnectOut): los desplazamientos son enteros de 32 bits</span><span class="sxs-lookup"><span data-stu-id="cbf24-3646">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 32-bit system (\_serverVersion set to 0x00000007 in CPMConnectOut): Offsets are 32-bit integers</span></span>
-   <span data-ttu-id="cbf24-3647">El cliente indicó que era un sistema de 64 bits (iClientVersion > 0x00000008 en CPMConnectIn) y Server indicó que era un sistema de 64 bits (serverVersion establecido en \_ \_ 0x00010007 en CPMConnectOut): los desplazamientos son enteros de 64 bits</span><span class="sxs-lookup"><span data-stu-id="cbf24-3647">Client indicated it was a 64-bit system (\_iClientVersion > 0x00000008 in CPMConnectIn) and Server indicated it was a 64-bit system (\_serverVersion set to 0x00010007 in CPMConnectOut): Offsets are 64-bit integers</span></span>

<span data-ttu-id="cbf24-3648">El formato del mensaje CPMGetRowsOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3648">The format of the CPMGetRowsOut message that follows the header is:</span></span>



<span data-ttu-id="cbf24-3649">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3649">0</span></span>

<span data-ttu-id="cbf24-3650">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3650">1</span></span>

<span data-ttu-id="cbf24-3651">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3651">2</span></span>

<span data-ttu-id="cbf24-3652">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3652">3</span></span>

<span data-ttu-id="cbf24-3653">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3653">4</span></span>

<span data-ttu-id="cbf24-3654">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3654">5</span></span>

<span data-ttu-id="cbf24-3655">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3655">6</span></span>

<span data-ttu-id="cbf24-3656">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3656">7</span></span>

<span data-ttu-id="cbf24-3657">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3657">8</span></span>

<span data-ttu-id="cbf24-3658">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3658">9</span></span>

<span data-ttu-id="cbf24-3659">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3659">1</span></span><br/> <span data-ttu-id="cbf24-3660">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3660">0</span></span><br/>

<span data-ttu-id="cbf24-3661">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3661">1</span></span>

<span data-ttu-id="cbf24-3662">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3662">2</span></span>

<span data-ttu-id="cbf24-3663">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3663">3</span></span>

<span data-ttu-id="cbf24-3664">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3664">4</span></span>

<span data-ttu-id="cbf24-3665">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3665">5</span></span>

<span data-ttu-id="cbf24-3666">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3666">6</span></span>

<span data-ttu-id="cbf24-3667">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3667">7</span></span>

<span data-ttu-id="cbf24-3668">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3668">8</span></span>

<span data-ttu-id="cbf24-3669">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3669">9</span></span>

<span data-ttu-id="cbf24-3670">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3670">2</span></span><br/> <span data-ttu-id="cbf24-3671">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3671">0</span></span><br/>

<span data-ttu-id="cbf24-3672">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3672">1</span></span>

<span data-ttu-id="cbf24-3673">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3673">2</span></span>

<span data-ttu-id="cbf24-3674">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3674">3</span></span>

<span data-ttu-id="cbf24-3675">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3675">4</span></span>

<span data-ttu-id="cbf24-3676">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3676">5</span></span>

<span data-ttu-id="cbf24-3677">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3677">6</span></span>

<span data-ttu-id="cbf24-3678">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3678">7</span></span>

<span data-ttu-id="cbf24-3679">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3679">8</span></span>

<span data-ttu-id="cbf24-3680">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3680">9</span></span>

<span data-ttu-id="cbf24-3681">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3681">3</span></span><br/> <span data-ttu-id="cbf24-3682">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3682">0</span></span><br/>

<span data-ttu-id="cbf24-3683">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3683">1</span></span>

<span data-ttu-id="cbf24-3684">\_cRowsReturned</span><span class="sxs-lookup"><span data-stu-id="cbf24-3684">\_cRowsReturned</span></span>

<span data-ttu-id="cbf24-3685">eType</span><span class="sxs-lookup"><span data-stu-id="cbf24-3685">eType</span></span>

<span data-ttu-id="cbf24-3686">\_chapt</span><span class="sxs-lookup"><span data-stu-id="cbf24-3686">\_chapt</span></span>

<span data-ttu-id="cbf24-3687">SeekDescription (opcional, variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3687">SeekDescription (optional, variable)</span></span>

<span data-ttu-id="cbf24-3688">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-3688">...</span></span>

<span data-ttu-id="cbf24-3689">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-3689">...</span></span>

<span data-ttu-id="cbf24-3690">paddingRows (opcional, variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3690">paddingRows (optional, variable)</span></span>

<span data-ttu-id="cbf24-3691">Filas</span><span class="sxs-lookup"><span data-stu-id="cbf24-3691">Rows</span></span>



 

<span data-ttu-id="cbf24-3692">**\_ cRowsReturned:** entero de 32 bits sin signo que indica el número de filas devueltas en Filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3692">**\_cRowsReturned**: A 32-bit unsigned integer indicating the number of rows returned in Rows.</span></span>

<span data-ttu-id="cbf24-3693">**eType:** entero de 32 bits sin signo que contiene uno de los valores siguientes para indicar el tipo de operación rowseek que se debe realizar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3693">**eType**: A 32-bit unsigned integer containing one of the following values to indicate the type of rowseek operation to perform</span></span>



| <span data-ttu-id="cbf24-3694">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-3694">Value</span></span>                         | <span data-ttu-id="cbf24-3695">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-3695">Meaning</span></span>                                                  |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="cbf24-3696">eRowsSeekNone 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-3696">eRowsSeekNone 0x00000000</span></span>      | <span data-ttu-id="cbf24-3697">Sin SeekDescription, ignore el campo SeekDescription.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3697">No SeekDescription, ignore SeekDescription field.</span></span>        |
| <span data-ttu-id="cbf24-3698">eRowSeekNext 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-3698">eRowSeekNext 0x00000001</span></span>       | <span data-ttu-id="cbf24-3699">SeekDescription contiene una estructura CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3699">SeekDescription contains a CRowSeekNext structure.</span></span>       |
| <span data-ttu-id="cbf24-3700">eRowSeekAt 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbf24-3700">eRowSeekAt 0x00000002</span></span>         | <span data-ttu-id="cbf24-3701">SeekDescription contiene una estructura CRowSeekAt.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3701">SeekDescription contains a CRowSeekAt structure.</span></span>         |
| <span data-ttu-id="cbf24-3702">eRowSeekAtRatio 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cbf24-3702">eRowSeekAtRatio 0x00000003</span></span>    | <span data-ttu-id="cbf24-3703">SeekDescription contiene una estructura CRowSeekAtRatio.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3703">SeekDescription contains a CRowSeekAtRatio structure.</span></span>    |
| <span data-ttu-id="cbf24-3704">ERowSeekByBookmark 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cbf24-3704">eRowSeekByBookmark 0x00000004</span></span> | <span data-ttu-id="cbf24-3705">SeekDescription contiene una estructura CRowSeekByBookmark.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3705">SeekDescription contains a CRowSeekByBookmark structure.</span></span> |



 

<span data-ttu-id="cbf24-3706">**\_ chapt:** valor de 32 bits que representa el identificador del capítulo del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3706">**\_chapt**: A 32-bit value representing the handle of the rowset chapter.</span></span>

<span data-ttu-id="cbf24-3707">**SeekDescription:** este campo DEBE contener una estructura del tipo indicado por el campo eType.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3707">**SeekDescription**: This field MUST contain a structure of the type indicated by the eType field.</span></span>

<span data-ttu-id="cbf24-3708">**paddingRows:** este campo DEBE tener una longitud suficiente (de 0 a cbReserved-1 bytes) para rellenar el campo Rows hasta el desplazamiento cbReserved desde el principio de un mensaje, donde cbReserved es el valor del mensaje \_ \_ \_ CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3708">**paddingRows**: This field MUST be of sufficient length (0 to \_cbReserved-1 bytes) to pad the Rows field to \_cbReserved offset from the beginning of a message, where \_cbReserved is the value in the CPMGetRowsIn message.</span></span> <span data-ttu-id="cbf24-3709">Los bytes de relleno utilizados en este campo pueden ser cualquier valor arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3709">Padding bytes used in this field can be any arbitrary value.</span></span> <span data-ttu-id="cbf24-3710">El receptor DEBE omitir este campo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3710">This field MUST be ignored by the receiver.</span></span>

<span data-ttu-id="cbf24-3711">**Filas:** los datos de fila tienen el formato indicado por la información de columna en el mensaje CPMSetBindingsIn más reciente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3711">**Rows**: Row data, is formatted as prescribed by column information in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="cbf24-3712">Las filas DEBEN almacenarse en orden de reenvío (por ejemplo, la fila 1 antes de la fila 2).</span><span class="sxs-lookup"><span data-stu-id="cbf24-3712">Rows MUST be stored in forward order (e.g. row 1 before row 2).</span></span>

<span data-ttu-id="cbf24-3713">Las columnas de tamaño fijo DEBEN almacenarse en los desplazamientos especificados por el mensaje CPMSetBindingsIn más reciente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3713">Fixed-sized columns MUST be stored at the offsets specified by the most recent CPMSetBindingsIn message.</span></span>

<span data-ttu-id="cbf24-3714">Las columnas de tamaño variable (por ejemplo, cadenas) DEBEN almacenarse de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3714">Variable-sized columns (e.g., strings) MUST be stored as follows:</span></span>

-   <span data-ttu-id="cbf24-3715">Los propios datos de la variable (por ejemplo, la cadena) se almacenan cerca del final del búfer en orden descendente (por ejemplo, la colección de todos los datos de variables para la fila 1 está al final, la fila 2 siguiente más cercana, etc.).</span><span class="sxs-lookup"><span data-stu-id="cbf24-3715">The variable data itself (e.g. the string) is stored near the end of the buffer in descending order (e.g. the collection of all variable data for row 1 is at the end, row 2 next closest, etc.).</span></span>
-   <span data-ttu-id="cbf24-3716">El área de tamaño fijo (al principio del búfer de fila) DEBE contener un CRowVariant para cada columna, almacenado en el desplazamiento especificado en el mensaje CPMSetBindingsIn más reciente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3716">The fixed sized area (at the beginning of the row buffer) MUST contain a CRowVariant for each column, stored at the offset specified in the most recent CPMSetBindingsIn message.</span></span> <span data-ttu-id="cbf24-3717">vType DEBE contener el tipo de datos (por ejemplo, VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="cbf24-3717">vType MUST contain the data type (ex: VT\_LPWSTR).</span></span> <span data-ttu-id="cbf24-3718">Si, según lo determinado por las reglas al principio de la sección de esta sección, se usan desplazamientos de 32 bits, el campo Offset de CRowVariant DEBE contener un valor de 32 bits que sea el desplazamiento de los datos de variable desde el principio del mensaje CPMGetRowsOut, más el valor de ulClientBase especificado en el mensaje \_ CPMGetRowsIn más reciente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3718">If, as determined by the rules at the beginning of section this section, 32-bit offsets are being used then the Offset field in CRowVariant MUST contain a 32-bit value that is the offset of the variable data from the beginning of the CPMGetRowsOut message, plus the value of \_ulClientBase specified in the most recent CPMGetRowsIn message.</span></span> <span data-ttu-id="cbf24-3719">Si se usan desplazamientos de 64 bits, el campo Offset de CRowVariant DEBE contener un valor de 64 bits que sea el desplazamiento desde el principio del mensaje CPMGetRowsOut, agregado a un valor de 64 bits compuesto por el uso de ulClientBase como los 32 bits inferiores y \_ \_ ulReserved2 como los 32 bits altos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3719">If 64-bit offsets are being used then the Offset field in CRowVariant MUST contain a 64-bit value that is the offset from the beginning of the CPMGetRowsOut message, added to a 64-bit value composed by using \_ulClientBase as the low 32-bits and \_ulReserved2 as the high 32-bits.</span></span>

<span data-ttu-id="cbf24-3720">Por ejemplo, si el mensaje CPMSetBindingsIn especificaba dos columnas -Size (VT \_ I4) y Title \_ (VT LPWSTR)-y ulClientBase de CPMGetRowsIn era 0x10000 dos filas aparecerán como \_ sigue.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3720">For example, if the CPMSetBindingsIn message specified two columns-Size (VT\_I4) and Title (VT\_LPWSTR)-and \_ulClientBase from CPMGetRowsIn was 0x10000 then two rows would appear as follows.</span></span> <span data-ttu-id="cbf24-3721">La sección marcada en gris es la parte de longitud fija del búfer.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3721">The section marked in grey is the fixed-length part of the buffer.</span></span>

![Ejemplo de mensaje cpmsetbindingsin](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a><span data-ttu-id="cbf24-3723">2.2.3.17 CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-3723">2.2.3.17 CPMRatioFinishedIn</span></span>

<span data-ttu-id="cbf24-3724">El mensaje CPMRatioFinishedIn solicita el porcentaje de finalización de una consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3724">The CPMRatioFinishedIn message requests the completion percentage of a query.</span></span> <span data-ttu-id="cbf24-3725">El formato del mensaje CPMRatioFinishedIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3725">The format of the CPMRatioFinishedIn message that follows the header is:</span></span>



<span data-ttu-id="cbf24-3726">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3726">0</span></span>

<span data-ttu-id="cbf24-3727">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3727">1</span></span>

<span data-ttu-id="cbf24-3728">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3728">2</span></span>

<span data-ttu-id="cbf24-3729">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3729">3</span></span>

<span data-ttu-id="cbf24-3730">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3730">4</span></span>

<span data-ttu-id="cbf24-3731">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3731">5</span></span>

<span data-ttu-id="cbf24-3732">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3732">6</span></span>

<span data-ttu-id="cbf24-3733">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3733">7</span></span>

<span data-ttu-id="cbf24-3734">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3734">8</span></span>

<span data-ttu-id="cbf24-3735">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3735">9</span></span>

<span data-ttu-id="cbf24-3736">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3736">1</span></span><br/> <span data-ttu-id="cbf24-3737">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3737">0</span></span><br/>

<span data-ttu-id="cbf24-3738">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3738">1</span></span>

<span data-ttu-id="cbf24-3739">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3739">2</span></span>

<span data-ttu-id="cbf24-3740">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3740">3</span></span>

<span data-ttu-id="cbf24-3741">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3741">4</span></span>

<span data-ttu-id="cbf24-3742">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3742">5</span></span>

<span data-ttu-id="cbf24-3743">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3743">6</span></span>

<span data-ttu-id="cbf24-3744">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3744">7</span></span>

<span data-ttu-id="cbf24-3745">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3745">8</span></span>

<span data-ttu-id="cbf24-3746">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3746">9</span></span>

<span data-ttu-id="cbf24-3747">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3747">2</span></span><br/> <span data-ttu-id="cbf24-3748">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3748">0</span></span><br/>

<span data-ttu-id="cbf24-3749">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3749">1</span></span>

<span data-ttu-id="cbf24-3750">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3750">2</span></span>

<span data-ttu-id="cbf24-3751">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3751">3</span></span>

<span data-ttu-id="cbf24-3752">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3752">4</span></span>

<span data-ttu-id="cbf24-3753">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3753">5</span></span>

<span data-ttu-id="cbf24-3754">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3754">6</span></span>

<span data-ttu-id="cbf24-3755">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3755">7</span></span>

<span data-ttu-id="cbf24-3756">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3756">8</span></span>

<span data-ttu-id="cbf24-3757">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3757">9</span></span>

<span data-ttu-id="cbf24-3758">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3758">3</span></span><br/> <span data-ttu-id="cbf24-3759">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3759">0</span></span><br/>

<span data-ttu-id="cbf24-3760">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3760">1</span></span>

<span data-ttu-id="cbf24-3761">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cbf24-3761">\_hCursor</span></span>

<span data-ttu-id="cbf24-3762">\_fQuick</span><span class="sxs-lookup"><span data-stu-id="cbf24-3762">\_fQuick</span></span>



 

<span data-ttu-id="cbf24-3763">**\_ hCursor:** identificador del mensaje CPMCreateQueryOut que identifica la consulta para la que se va a solicitar información de finalización.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3763">**\_hCursor**: The handle from CPMCreateQueryOut message identifying the query for which to request completion information.</span></span>

<span data-ttu-id="cbf24-3764">**\_ fQuick:** DEBE establecerse en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3764">**\_fQuick**: MUST be set to 0x00000001.</span></span> <span data-ttu-id="cbf24-3765">El servidor no usa y DEBE omitirlo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3765">Unused and MUST be ignored by the server.</span></span>

### <a name="22318-cpmratiofinishedout"></a><span data-ttu-id="cbf24-3766">2.2.3.18 CPMRatioFinishedOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-3766">2.2.3.18 CPMRatioFinishedOut</span></span>

<span data-ttu-id="cbf24-3767">El mensaje CPMRatioFinishedOut responde a un mensaje CPMRatioFinishedIn con la proporción de finalización de una consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3767">The CPMRatioFinishedOut message replies to a CPMRatioFinishedIn message with the completion ratio of a query.</span></span> <span data-ttu-id="cbf24-3768">El formato del mensaje CPMRatioFinishedOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3768">The format of the CPMRatioFinishedOut message that follows the header is:</span></span>



<span data-ttu-id="cbf24-3769">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3769">0</span></span>

<span data-ttu-id="cbf24-3770">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3770">1</span></span>

<span data-ttu-id="cbf24-3771">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3771">2</span></span>

<span data-ttu-id="cbf24-3772">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3772">3</span></span>

<span data-ttu-id="cbf24-3773">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3773">4</span></span>

<span data-ttu-id="cbf24-3774">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3774">5</span></span>

<span data-ttu-id="cbf24-3775">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3775">6</span></span>

<span data-ttu-id="cbf24-3776">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3776">7</span></span>

<span data-ttu-id="cbf24-3777">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3777">8</span></span>

<span data-ttu-id="cbf24-3778">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3778">9</span></span>

<span data-ttu-id="cbf24-3779">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3779">1</span></span><br/> <span data-ttu-id="cbf24-3780">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3780">0</span></span><br/>

<span data-ttu-id="cbf24-3781">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3781">1</span></span>

<span data-ttu-id="cbf24-3782">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3782">2</span></span>

<span data-ttu-id="cbf24-3783">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3783">3</span></span>

<span data-ttu-id="cbf24-3784">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3784">4</span></span>

<span data-ttu-id="cbf24-3785">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3785">5</span></span>

<span data-ttu-id="cbf24-3786">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3786">6</span></span>

<span data-ttu-id="cbf24-3787">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3787">7</span></span>

<span data-ttu-id="cbf24-3788">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3788">8</span></span>

<span data-ttu-id="cbf24-3789">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3789">9</span></span>

<span data-ttu-id="cbf24-3790">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3790">2</span></span><br/> <span data-ttu-id="cbf24-3791">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3791">0</span></span><br/>

<span data-ttu-id="cbf24-3792">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3792">1</span></span>

<span data-ttu-id="cbf24-3793">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3793">2</span></span>

<span data-ttu-id="cbf24-3794">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3794">3</span></span>

<span data-ttu-id="cbf24-3795">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3795">4</span></span>

<span data-ttu-id="cbf24-3796">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3796">5</span></span>

<span data-ttu-id="cbf24-3797">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3797">6</span></span>

<span data-ttu-id="cbf24-3798">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3798">7</span></span>

<span data-ttu-id="cbf24-3799">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3799">8</span></span>

<span data-ttu-id="cbf24-3800">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3800">9</span></span>

<span data-ttu-id="cbf24-3801">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3801">3</span></span><br/> <span data-ttu-id="cbf24-3802">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3802">0</span></span><br/>

<span data-ttu-id="cbf24-3803">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3803">1</span></span>

<span data-ttu-id="cbf24-3804">\_ ulNumerator</span><span class="sxs-lookup"><span data-stu-id="cbf24-3804">\_ ulNumerator</span></span>

<span data-ttu-id="cbf24-3805">\_ulDenominator</span><span class="sxs-lookup"><span data-stu-id="cbf24-3805">\_ulDenominator</span></span>

<span data-ttu-id="cbf24-3806">\_Cuervos</span><span class="sxs-lookup"><span data-stu-id="cbf24-3806">\_cRows</span></span>

<span data-ttu-id="cbf24-3807">\_fNewRows</span><span class="sxs-lookup"><span data-stu-id="cbf24-3807">\_fNewRows</span></span>



 

<span data-ttu-id="cbf24-3808">**\_ ulNumerator:** entero de 32 bits sin signo que indica el numerador de la proporción de finalización en términos de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3808">**\_ulNumerator**: A 32-bit unsigned integer indicating the numerator of the completion ratio in terms of rows.</span></span>

<span data-ttu-id="cbf24-3809">**\_ ulDenominator:** entero de 32 bits sin signo que indica el denominador de la proporción de finalización en términos de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3809">**\_ulDenominator**: A 32-bit unsigned integer indicating the denominator of the completion ratio in terms of rows.</span></span> <span data-ttu-id="cbf24-3810">DEBE ser mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3810">MUST be greater than zero.</span></span>

<span data-ttu-id="cbf24-3811">**\_ cRows:** entero de 32 bits sin signo que indica el número total de filas de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3811">**\_cRows**: A 32-bit unsigned integer indicating the total number of rows for the query.</span></span>

<span data-ttu-id="cbf24-3812">**\_ fNewRows:** valor booleano que indica si hay nuevas filas disponibles.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3812">**\_fNewRows**: A boolean value indicating if there are new rows available.</span></span> <span data-ttu-id="cbf24-3813">Un valor de 0x00000001 indica que hay nuevas filas disponibles en el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3813">A value of 0x00000001 indicates that new rows are available in the rowset.</span></span> <span data-ttu-id="cbf24-3814">Un valor de 0x00000000 indica que el conjunto de filas no contiene ninguna fila nueva.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3814">A value of 0x00000000 indicates that the rowset does not contain any new rows.</span></span> <span data-ttu-id="cbf24-3815">Este campo NO DEBE establecerse en ningún otro valor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3815">This field MUST NOT be set to any other values.</span></span>

### <a name="22319-cpmfetchvaluein"></a><span data-ttu-id="cbf24-3816">2.2.3.19 CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-3816">2.2.3.19 CPMFetchValueIn</span></span>

<span data-ttu-id="cbf24-3817">El mensaje CPMFetchValueIn solicita un valor de propiedad demasiado grande para devolverlo en un conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3817">The CPMFetchValueIn message requests a property value that was too large to return in a rowset.</span></span> <span data-ttu-id="cbf24-3818">Como se especifica en la sección 3.2.4.2.5, este mensaje se envía repetidamente para recuperar todos los bytes de la propiedad, actualizando cbSoFar para cada uno, hasta que el campo fMoreExists del mensaje \_ \_ CPMFetchValueOut se establece en **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="cbf24-3818">As specified in section 3.2.4.2.5, this message is sent repeatedly to retrieve all bytes of the property, updating \_cbSoFar for each, until the \_fMoreExists field of CPMFetchValueOut message is set to **FALSE**.</span></span>

<span data-ttu-id="cbf24-3819">El formato del mensaje CPMFetchValueIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3819">The format of the CPMFetchValueIn message that follows the header is:</span></span>



<span data-ttu-id="cbf24-3820">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3820">0</span></span>

<span data-ttu-id="cbf24-3821">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3821">1</span></span>

<span data-ttu-id="cbf24-3822">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3822">2</span></span>

<span data-ttu-id="cbf24-3823">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3823">3</span></span>

<span data-ttu-id="cbf24-3824">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3824">4</span></span>

<span data-ttu-id="cbf24-3825">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3825">5</span></span>

<span data-ttu-id="cbf24-3826">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3826">6</span></span>

<span data-ttu-id="cbf24-3827">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3827">7</span></span>

<span data-ttu-id="cbf24-3828">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3828">8</span></span>

<span data-ttu-id="cbf24-3829">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3829">9</span></span>

<span data-ttu-id="cbf24-3830">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3830">1</span></span><br/> <span data-ttu-id="cbf24-3831">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3831">0</span></span><br/>

<span data-ttu-id="cbf24-3832">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3832">1</span></span>

<span data-ttu-id="cbf24-3833">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3833">2</span></span>

<span data-ttu-id="cbf24-3834">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3834">3</span></span>

<span data-ttu-id="cbf24-3835">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3835">4</span></span>

<span data-ttu-id="cbf24-3836">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3836">5</span></span>

<span data-ttu-id="cbf24-3837">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3837">6</span></span>

<span data-ttu-id="cbf24-3838">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3838">7</span></span>

<span data-ttu-id="cbf24-3839">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3839">8</span></span>

<span data-ttu-id="cbf24-3840">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3840">9</span></span>

<span data-ttu-id="cbf24-3841">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3841">2</span></span><br/> <span data-ttu-id="cbf24-3842">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3842">0</span></span><br/>

<span data-ttu-id="cbf24-3843">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3843">1</span></span>

<span data-ttu-id="cbf24-3844">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3844">2</span></span>

<span data-ttu-id="cbf24-3845">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3845">3</span></span>

<span data-ttu-id="cbf24-3846">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3846">4</span></span>

<span data-ttu-id="cbf24-3847">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3847">5</span></span>

<span data-ttu-id="cbf24-3848">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3848">6</span></span>

<span data-ttu-id="cbf24-3849">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3849">7</span></span>

<span data-ttu-id="cbf24-3850">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3850">8</span></span>

<span data-ttu-id="cbf24-3851">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3851">9</span></span>

<span data-ttu-id="cbf24-3852">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3852">3</span></span><br/> <span data-ttu-id="cbf24-3853">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3853">0</span></span><br/>

<span data-ttu-id="cbf24-3854">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3854">1</span></span>

<span data-ttu-id="cbf24-3855">\_Wid</span><span class="sxs-lookup"><span data-stu-id="cbf24-3855">\_wid</span></span>

<span data-ttu-id="cbf24-3856">\_cbSoFar</span><span class="sxs-lookup"><span data-stu-id="cbf24-3856">\_cbSoFar</span></span>

<span data-ttu-id="cbf24-3857">\_cbPropSpec</span><span class="sxs-lookup"><span data-stu-id="cbf24-3857">\_cbPropSpec</span></span>

<span data-ttu-id="cbf24-3858">\_cbChunk</span><span class="sxs-lookup"><span data-stu-id="cbf24-3858">\_cbChunk</span></span>

<span data-ttu-id="cbf24-3859">PropSpec (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3859">PropSpec (variable)</span></span>

<span data-ttu-id="cbf24-3860">...</span><span class="sxs-lookup"><span data-stu-id="cbf24-3860">...</span></span>

<span data-ttu-id="cbf24-3861">\_padding (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3861">\_padding (variable)</span></span>



 

<span data-ttu-id="cbf24-3862">**\_ wid:** entero de 32 bits sin signo que contiene información sobre el identificador de documento que identifica el documento para el que se debe capturar una propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3862">**\_wid**: A 32-bit unsigned integer containing information about the document ID identifying the document for which a property should be fetched.</span></span>

<span data-ttu-id="cbf24-3863">**\_ cbSoFar:** entero de 32 bits sin signo que contiene el número de bytes transferidos previamente para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3863">**\_cbSoFar**: A 32-bit unsigned integer containing the number of bytes previously transferred for this property.</span></span> <span data-ttu-id="cbf24-3864">DEBE establecerse en 0x00000000 en el primer mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3864">MUST be set to 0x00000000 in the first message.</span></span>

<span data-ttu-id="cbf24-3865">**\_ cbPropSpec:** entero de 32 bits sin signo que contiene el tamaño del campo PropSpec, en bytes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3865">**\_cbPropSpec**: A 32-bit unsigned integer containing the size of the PropSpec field, in bytes.</span></span>

<span data-ttu-id="cbf24-3866">**\_ cbChunk:** entero de 32 bits sin signo que contiene el número máximo de bytes que el remitente puede aceptar en un mensaje CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3866">**\_cbChunk**: A 32-bit unsigned integer containing the maximum number of bytes that the sender can accept in a CPMFetchValueOut message.</span></span>

<span data-ttu-id="cbf24-3867">*Comportamiento de Windows: este campo se establece en 0x00004000 para todas las versiones de Windows.*</span><span class="sxs-lookup"><span data-stu-id="cbf24-3867">*Windows Behavior: This field is set to 0x00004000 for all versions of Windows.*</span></span>

<span data-ttu-id="cbf24-3868">**PropSpec:** estructura CFullPropSpec que especifica la propiedad que se recuperará.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3868">**PropSpec**: A CFullPropSpec structure specifying the property to retrieve.</span></span>

<span data-ttu-id="cbf24-3869">**\_ padding:** este campo DEBE tener la longitud necesaria (de 0 a 3 bytes) para rellenar el mensaje hasta un múltiplo de 4 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3869">**\_padding**: This field MUST be of the length necessary (0 to 3 bytes) to pad the message out to a multiple of 4 bytes in length.</span></span> <span data-ttu-id="cbf24-3870">El valor de los bytes de relleno puede ser cualquier valor arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3870">The value of the padding bytes can be any arbitrary value.</span></span> <span data-ttu-id="cbf24-3871">El receptor DEBE omitir este campo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3871">This field MUST be ignored by the receiver.</span></span>

### <a name="22320-cpmfetchvalueout"></a><span data-ttu-id="cbf24-3872">2.2.3.20 CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-3872">2.2.3.20 CPMFetchValueOut</span></span>

<span data-ttu-id="cbf24-3873">El mensaje CPMFetchValueOut responde a un mensaje CPMFetchValueIn con un valor de propiedad de una consulta anterior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3873">The CPMFetchValueOut message replies to a CPMFetchValueIn message with a property value from a previous query.</span></span> <span data-ttu-id="cbf24-3874">Como se especifica en la sección 3.1.5.2.8, este mensaje se envía después de cada mensaje CPMFetchValueIn hasta que se transfieren todos los bytes de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3874">As specified in section 3.1.5.2.8, this message is sent after each CPMFetchValueIn message until all bytes of the property are transferred.</span></span>

<span data-ttu-id="cbf24-3875">El formato del mensaje CPMFetchValueOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3875">The format of the CPMFetchValueOut message that follows the header is:</span></span>



<span data-ttu-id="cbf24-3876">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3876">0</span></span>

<span data-ttu-id="cbf24-3877">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3877">1</span></span>

<span data-ttu-id="cbf24-3878">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3878">2</span></span>

<span data-ttu-id="cbf24-3879">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3879">3</span></span>

<span data-ttu-id="cbf24-3880">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3880">4</span></span>

<span data-ttu-id="cbf24-3881">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3881">5</span></span>

<span data-ttu-id="cbf24-3882">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3882">6</span></span>

<span data-ttu-id="cbf24-3883">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3883">7</span></span>

<span data-ttu-id="cbf24-3884">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3884">8</span></span>

<span data-ttu-id="cbf24-3885">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3885">9</span></span>

<span data-ttu-id="cbf24-3886">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3886">1</span></span><br/> <span data-ttu-id="cbf24-3887">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3887">0</span></span><br/>

<span data-ttu-id="cbf24-3888">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3888">1</span></span>

<span data-ttu-id="cbf24-3889">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3889">2</span></span>

<span data-ttu-id="cbf24-3890">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3890">3</span></span>

<span data-ttu-id="cbf24-3891">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3891">4</span></span>

<span data-ttu-id="cbf24-3892">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3892">5</span></span>

<span data-ttu-id="cbf24-3893">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3893">6</span></span>

<span data-ttu-id="cbf24-3894">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3894">7</span></span>

<span data-ttu-id="cbf24-3895">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3895">8</span></span>

<span data-ttu-id="cbf24-3896">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3896">9</span></span>

<span data-ttu-id="cbf24-3897">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3897">2</span></span><br/> <span data-ttu-id="cbf24-3898">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3898">0</span></span><br/>

<span data-ttu-id="cbf24-3899">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3899">1</span></span>

<span data-ttu-id="cbf24-3900">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3900">2</span></span>

<span data-ttu-id="cbf24-3901">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3901">3</span></span>

<span data-ttu-id="cbf24-3902">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3902">4</span></span>

<span data-ttu-id="cbf24-3903">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3903">5</span></span>

<span data-ttu-id="cbf24-3904">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3904">6</span></span>

<span data-ttu-id="cbf24-3905">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3905">7</span></span>

<span data-ttu-id="cbf24-3906">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3906">8</span></span>

<span data-ttu-id="cbf24-3907">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3907">9</span></span>

<span data-ttu-id="cbf24-3908">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3908">3</span></span><br/> <span data-ttu-id="cbf24-3909">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3909">0</span></span><br/>

<span data-ttu-id="cbf24-3910">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3910">1</span></span>

<span data-ttu-id="cbf24-3911">\_cbValue</span><span class="sxs-lookup"><span data-stu-id="cbf24-3911">\_cbValue</span></span>

<span data-ttu-id="cbf24-3912">\_fMoreExists</span><span class="sxs-lookup"><span data-stu-id="cbf24-3912">\_fMoreExists</span></span>

<span data-ttu-id="cbf24-3913">\_fValueExists</span><span class="sxs-lookup"><span data-stu-id="cbf24-3913">\_fValueExists</span></span>

<span data-ttu-id="cbf24-3914">vType</span><span class="sxs-lookup"><span data-stu-id="cbf24-3914">vType</span></span>

<span data-ttu-id="cbf24-3915">vValue (variable)</span><span class="sxs-lookup"><span data-stu-id="cbf24-3915">vValue (variable)</span></span>



 

<span data-ttu-id="cbf24-3916">**\_ cbValue:** entero de 32 bits sin signo que contiene el tamaño total, en bytes en vValue.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3916">**\_cbValue**: A 32-bit unsigned integer containing the total size, in bytes in vValue.</span></span>

<span data-ttu-id="cbf24-3917">**\_ fMoreExists:** valor booleano que indica si hay mensajes CPMFetchValueOut adicionales disponibles.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3917">**\_fMoreExists**: A boolean value indicating whether there are additional CPMFetchValueOut messages available.</span></span> <span data-ttu-id="cbf24-3918">Si se establece en 0x00000001, hay mensajes CPMFetchValueOut adicionales.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3918">If set to 0x00000001, then there are additional CPMFetchValueOut messages.</span></span> <span data-ttu-id="cbf24-3919">Si se establece en 0x00000000, no hay mensajes CPMFetchValueOut adicionales disponibles.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3919">If set to 0x00000000, then there are no additional CPMFetchValueOut messages available.</span></span>

<span data-ttu-id="cbf24-3920">**\_ fValueExists:** valor booleano que indica si hay un valor para la propiedad .</span><span class="sxs-lookup"><span data-stu-id="cbf24-3920">**\_fValueExists**: A boolean value indicating whether there is a value for the property.</span></span> <span data-ttu-id="cbf24-3921">Si se establece en 0x00000001, existe un valor para la propiedad .</span><span class="sxs-lookup"><span data-stu-id="cbf24-3921">If set to 0x00000001, a value for the property exists.</span></span> <span data-ttu-id="cbf24-3922">Si se establece 0x00000000, no existe ningún valor para la propiedad .</span><span class="sxs-lookup"><span data-stu-id="cbf24-3922">If set to 0x00000000, a value for the property does not exist.</span></span>

<span data-ttu-id="cbf24-3923">**vType:** un valor de la enumeración VARENUM, vea la sección 2.2.1.1 para obtener más información y describir el tipo de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3923">**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.</span></span>

<span data-ttu-id="cbf24-3924">**vValue:** parte de una matriz de bytes que contiene una estructura SERIALIZEDPROPERTYVALUE como se especifica en la sección 2.2.1.32, donde el desplazamiento del principio de la parte es el valor \_ de cbSoFar en CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3924">**vValue**: A portion of a byte array containing a SERIALIZEDPROPERTYVALUE structure as specified in section 2.2.1.32, where the offset of the beginning of the portion is the value of\_cbSoFar in CPMFetchValueIn.</span></span> <span data-ttu-id="cbf24-3925">La longitud de la parte, indicada por el campo cbValue, DEBE ser igual al valor de \_ \_ cbChunk en CPMFetchValueIn si \_ fMoreExists está establecido en 0x00000001 y DEBE ser menor o igual que el valor de cbChunk en caso \_ contrario.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3925">The length of the portion, indicated by the \_cbValue field, MUST be equal to the value of \_cbChunk in CPMFetchValueIn if \_fMoreExists is set to 0x00000001, and MUST be less than or equal to the value of \_cbChunk otherwise.</span></span>

### <a name="22321-cpmgetnotify"></a><span data-ttu-id="cbf24-3926">2.2.3.21 CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="cbf24-3926">2.2.3.21 CPMGetNotify</span></span>

<span data-ttu-id="cbf24-3927">El mensaje CPMGetNotify solicita que se notifique al cliente de los cambios del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3927">The CPMGetNotify message requests that the client wants to be notified of rowset changes.</span></span>

<span data-ttu-id="cbf24-3928">El mensaje NO DEBE incluir un cuerpo; solo se enviará el encabezado del mensaje, tal como se especifica en la sección 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3928">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2, is to be sent.</span></span>

### <a name="22322-cpmsendnotifyout"></a><span data-ttu-id="cbf24-3929">2.2.3.22 CPMSendNotifyOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-3929">2.2.3.22 CPMSendNotifyOut</span></span>

<span data-ttu-id="cbf24-3930">El mensaje CPMSendNotifyOut notifica al cliente un cambio en los resultados de una consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3930">The CPMSendNotifyOut message notifies the client of a change to the results of a query.</span></span>

<span data-ttu-id="cbf24-3931">Este mensaje solo se envía cuando se produce un cambio.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3931">This message is only sent when a change occurs.</span></span> <span data-ttu-id="cbf24-3932">El formato del mensaje CPMSendNotifyOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3932">The format of the CPMSendNotifyOut message that follows the header is:</span></span>



<span data-ttu-id="cbf24-3933">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3933">0</span></span>

<span data-ttu-id="cbf24-3934">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3934">1</span></span>

<span data-ttu-id="cbf24-3935">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3935">2</span></span>

<span data-ttu-id="cbf24-3936">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3936">3</span></span>

<span data-ttu-id="cbf24-3937">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3937">4</span></span>

<span data-ttu-id="cbf24-3938">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3938">5</span></span>

<span data-ttu-id="cbf24-3939">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3939">6</span></span>

<span data-ttu-id="cbf24-3940">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3940">7</span></span>

<span data-ttu-id="cbf24-3941">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3941">8</span></span>

<span data-ttu-id="cbf24-3942">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3942">9</span></span>

<span data-ttu-id="cbf24-3943">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3943">1</span></span><br/> <span data-ttu-id="cbf24-3944">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3944">0</span></span><br/>

<span data-ttu-id="cbf24-3945">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3945">1</span></span>

<span data-ttu-id="cbf24-3946">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3946">2</span></span>

<span data-ttu-id="cbf24-3947">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3947">3</span></span>

<span data-ttu-id="cbf24-3948">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3948">4</span></span>

<span data-ttu-id="cbf24-3949">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3949">5</span></span>

<span data-ttu-id="cbf24-3950">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3950">6</span></span>

<span data-ttu-id="cbf24-3951">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3951">7</span></span>

<span data-ttu-id="cbf24-3952">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3952">8</span></span>

<span data-ttu-id="cbf24-3953">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3953">9</span></span>

<span data-ttu-id="cbf24-3954">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3954">2</span></span><br/> <span data-ttu-id="cbf24-3955">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3955">0</span></span><br/>

<span data-ttu-id="cbf24-3956">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3956">1</span></span>

<span data-ttu-id="cbf24-3957">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3957">2</span></span>

<span data-ttu-id="cbf24-3958">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3958">3</span></span>

<span data-ttu-id="cbf24-3959">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3959">4</span></span>

<span data-ttu-id="cbf24-3960">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3960">5</span></span>

<span data-ttu-id="cbf24-3961">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3961">6</span></span>

<span data-ttu-id="cbf24-3962">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3962">7</span></span>

<span data-ttu-id="cbf24-3963">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3963">8</span></span>

<span data-ttu-id="cbf24-3964">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3964">9</span></span>

<span data-ttu-id="cbf24-3965">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3965">3</span></span><br/> <span data-ttu-id="cbf24-3966">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3966">0</span></span><br/>

<span data-ttu-id="cbf24-3967">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3967">1</span></span>

<span data-ttu-id="cbf24-3968">\_watchNotify</span><span class="sxs-lookup"><span data-stu-id="cbf24-3968">\_watchNotify</span></span>



 

<span data-ttu-id="cbf24-3969">**\_ watchNotify:** el cambio en la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3969">**\_watchNotify**: The change to the query.</span></span> <span data-ttu-id="cbf24-3970">DEBE ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3970">It MUST be one of the following values:</span></span>



| <span data-ttu-id="cbf24-3971">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-3971">Value</span></span>                                     | <span data-ttu-id="cbf24-3972">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-3972">Meaning</span></span>                                             |
|-------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="cbf24-3973">DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-3973">DBWATCHNOTIFY\_ROWSCHANGED 0x00000001</span></span>     | <span data-ttu-id="cbf24-3974">El número de filas del conjunto de filas de consulta ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3974">The number of rows in the query rowset has changed.</span></span> |
| <span data-ttu-id="cbf24-3975">DBWATCHNOTIFY \_ QUERYDONE 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbf24-3975">DBWATCHNOTIFY\_QUERYDONE 0x00000002</span></span>       | <span data-ttu-id="cbf24-3976">La consulta se ha completado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3976">The query has completed.</span></span>                            |
| <span data-ttu-id="cbf24-3977">DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cbf24-3977">DBWATCHNOTIFY\_QUERYREEXECUTED 0x00000003</span></span> | <span data-ttu-id="cbf24-3978">La consulta se ha re-ejecutado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3978">The query has been re-executed.</span></span>                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a><span data-ttu-id="cbf24-3979">2.2.3.23 CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-3979">2.2.3.23 CPMGetApproximatePositionIn</span></span>

<span data-ttu-id="cbf24-3980">El mensaje CPMGetApproximatePositionIn solicita la posición aproximada de un marcador en un capítulo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-3980">The CPMGetApproximatePositionIn message requests the approximate position of a bookmark in a chapter.</span></span> <span data-ttu-id="cbf24-3981">El formato del mensaje CPMGetApproximatePositionIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-3981">The format of the CPMGetApproximatePositionIn message that follows the header is:</span></span>



<span data-ttu-id="cbf24-3982">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3982">0</span></span>

<span data-ttu-id="cbf24-3983">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3983">1</span></span>

<span data-ttu-id="cbf24-3984">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3984">2</span></span>

<span data-ttu-id="cbf24-3985">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3985">3</span></span>

<span data-ttu-id="cbf24-3986">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3986">4</span></span>

<span data-ttu-id="cbf24-3987">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3987">5</span></span>

<span data-ttu-id="cbf24-3988">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3988">6</span></span>

<span data-ttu-id="cbf24-3989">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-3989">7</span></span>

<span data-ttu-id="cbf24-3990">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-3990">8</span></span>

<span data-ttu-id="cbf24-3991">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-3991">9</span></span>

<span data-ttu-id="cbf24-3992">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3992">1</span></span><br/> <span data-ttu-id="cbf24-3993">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-3993">0</span></span><br/>

<span data-ttu-id="cbf24-3994">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-3994">1</span></span>

<span data-ttu-id="cbf24-3995">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-3995">2</span></span>

<span data-ttu-id="cbf24-3996">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-3996">3</span></span>

<span data-ttu-id="cbf24-3997">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-3997">4</span></span>

<span data-ttu-id="cbf24-3998">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-3998">5</span></span>

<span data-ttu-id="cbf24-3999">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-3999">6</span></span>

<span data-ttu-id="cbf24-4000">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4000">7</span></span>

<span data-ttu-id="cbf24-4001">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4001">8</span></span>

<span data-ttu-id="cbf24-4002">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4002">9</span></span>

<span data-ttu-id="cbf24-4003">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4003">2</span></span><br/> <span data-ttu-id="cbf24-4004">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4004">0</span></span><br/>

<span data-ttu-id="cbf24-4005">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4005">1</span></span>

<span data-ttu-id="cbf24-4006">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4006">2</span></span>

<span data-ttu-id="cbf24-4007">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4007">3</span></span>

<span data-ttu-id="cbf24-4008">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4008">4</span></span>

<span data-ttu-id="cbf24-4009">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4009">5</span></span>

<span data-ttu-id="cbf24-4010">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4010">6</span></span>

<span data-ttu-id="cbf24-4011">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4011">7</span></span>

<span data-ttu-id="cbf24-4012">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4012">8</span></span>

<span data-ttu-id="cbf24-4013">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4013">9</span></span>

<span data-ttu-id="cbf24-4014">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4014">3</span></span><br/> <span data-ttu-id="cbf24-4015">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4015">0</span></span><br/>

<span data-ttu-id="cbf24-4016">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4016">1</span></span>

<span data-ttu-id="cbf24-4017">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cbf24-4017">\_hCursor</span></span>

<span data-ttu-id="cbf24-4018">\_chapt</span><span class="sxs-lookup"><span data-stu-id="cbf24-4018">\_chapt</span></span>

<span data-ttu-id="cbf24-4019">\_Bmk</span><span class="sxs-lookup"><span data-stu-id="cbf24-4019">\_bmk</span></span>



 

<span data-ttu-id="cbf24-4020">**\_ hCursor:** valor de 32 bits que representa el cursor de consulta obtenido de CPMCreateQueryOut para el conjunto de filas que contiene el marcador.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4020">**\_hCursor**: A 32-bit value representing the query cursor obtained from CPMCreateQueryOut for the rowset containing the bookmark.</span></span>

<span data-ttu-id="cbf24-4021">**\_ chapt:** valor de 32 bits que representa el identificador del capítulo que contiene el marcador.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4021">**\_chapt**: A 32-bit value representing the handle to the chapter containing the bookmark.</span></span>

<span data-ttu-id="cbf24-4022">**\_ bmk:** valor de 32 bits que representa el identificador del marcador para el que se va a recuperar la posición aproximada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4022">**\_bmk**: A 32-bit value representing the handle to the bookmark for which to retrieve the approximate position.</span></span>

### <a name="22324-cpmgetapproximatepositionout"></a><span data-ttu-id="cbf24-4023">2.2.3.24 CPMGetApproximatePositionOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-4023">2.2.3.24 CPMGetApproximatePositionOut</span></span>

<span data-ttu-id="cbf24-4024">El mensaje CPMGetApproximatePositionOut responde a un mensaje CPMGetApproximatePositionIn que describe la posición aproximada del marcador en el capítulo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4024">The CPMGetApproximatePositionOut message replies to a CPMGetApproximatePositionIn message describing the approximate position of the bookmark in the chapter.</span></span> <span data-ttu-id="cbf24-4025">El formato del mensaje CPMGetApproximatePositionOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4025">The format of the CPMGetApproximatePositionOut message that follows the header is:</span></span>



<span data-ttu-id="cbf24-4026">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4026">0</span></span>

<span data-ttu-id="cbf24-4027">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4027">1</span></span>

<span data-ttu-id="cbf24-4028">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4028">2</span></span>

<span data-ttu-id="cbf24-4029">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4029">3</span></span>

<span data-ttu-id="cbf24-4030">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4030">4</span></span>

<span data-ttu-id="cbf24-4031">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4031">5</span></span>

<span data-ttu-id="cbf24-4032">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4032">6</span></span>

<span data-ttu-id="cbf24-4033">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4033">7</span></span>

<span data-ttu-id="cbf24-4034">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4034">8</span></span>

<span data-ttu-id="cbf24-4035">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4035">9</span></span>

<span data-ttu-id="cbf24-4036">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4036">1</span></span><br/> <span data-ttu-id="cbf24-4037">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4037">0</span></span><br/>

<span data-ttu-id="cbf24-4038">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4038">1</span></span>

<span data-ttu-id="cbf24-4039">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4039">2</span></span>

<span data-ttu-id="cbf24-4040">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4040">3</span></span>

<span data-ttu-id="cbf24-4041">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4041">4</span></span>

<span data-ttu-id="cbf24-4042">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4042">5</span></span>

<span data-ttu-id="cbf24-4043">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4043">6</span></span>

<span data-ttu-id="cbf24-4044">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4044">7</span></span>

<span data-ttu-id="cbf24-4045">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4045">8</span></span>

<span data-ttu-id="cbf24-4046">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4046">9</span></span>

<span data-ttu-id="cbf24-4047">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4047">2</span></span><br/> <span data-ttu-id="cbf24-4048">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4048">0</span></span><br/>

<span data-ttu-id="cbf24-4049">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4049">1</span></span>

<span data-ttu-id="cbf24-4050">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4050">2</span></span>

<span data-ttu-id="cbf24-4051">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4051">3</span></span>

<span data-ttu-id="cbf24-4052">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4052">4</span></span>

<span data-ttu-id="cbf24-4053">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4053">5</span></span>

<span data-ttu-id="cbf24-4054">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4054">6</span></span>

<span data-ttu-id="cbf24-4055">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4055">7</span></span>

<span data-ttu-id="cbf24-4056">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4056">8</span></span>

<span data-ttu-id="cbf24-4057">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4057">9</span></span>

<span data-ttu-id="cbf24-4058">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4058">3</span></span><br/> <span data-ttu-id="cbf24-4059">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4059">0</span></span><br/>

<span data-ttu-id="cbf24-4060">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4060">1</span></span>

<span data-ttu-id="cbf24-4061">\_numerator</span><span class="sxs-lookup"><span data-stu-id="cbf24-4061">\_numerator</span></span>

<span data-ttu-id="cbf24-4062">\_denominator</span><span class="sxs-lookup"><span data-stu-id="cbf24-4062">\_denominator</span></span>



 

<span data-ttu-id="cbf24-4063">**\_ numerator:** entero de 32 bits sin signo que contiene el número de fila del marcador en el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4063">**\_numerator**: A 32-bit unsigned integer containing the row number of the bookmark in the rowset.</span></span> <span data-ttu-id="cbf24-4064">Si no hay filas, este campo DEBE establecerse en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4064">If there are no rows, this field MUST be set to 0x00000000.</span></span>

<span data-ttu-id="cbf24-4065">**\_ denominador:** entero de 32 bits sin signo que contiene el número de filas del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4065">**\_denominator**: A 32-bit unsigned integer containing the number of rows in the rowset.</span></span>

### <a name="22325-cpmcomparebmkin"></a><span data-ttu-id="cbf24-4066">2.2.3.25 CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4066">2.2.3.25 CPMCompareBmkIn</span></span>

<span data-ttu-id="cbf24-4067">El mensaje CPMCompareBmkIn solicita una comparación de dos marcadores en un capítulo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4067">The CPMCompareBmkIn message requests a comparison of two bookmarks in a chapter.</span></span>

<span data-ttu-id="cbf24-4068">El formato del mensaje CPMCompareBmkIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4068">The format of the CPMCompareBmkIn message that follows the header is:</span></span>



<span data-ttu-id="cbf24-4069">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4069">0</span></span>

<span data-ttu-id="cbf24-4070">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4070">1</span></span>

<span data-ttu-id="cbf24-4071">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4071">2</span></span>

<span data-ttu-id="cbf24-4072">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4072">3</span></span>

<span data-ttu-id="cbf24-4073">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4073">4</span></span>

<span data-ttu-id="cbf24-4074">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4074">5</span></span>

<span data-ttu-id="cbf24-4075">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4075">6</span></span>

<span data-ttu-id="cbf24-4076">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4076">7</span></span>

<span data-ttu-id="cbf24-4077">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4077">8</span></span>

<span data-ttu-id="cbf24-4078">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4078">9</span></span>

<span data-ttu-id="cbf24-4079">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4079">1</span></span><br/> <span data-ttu-id="cbf24-4080">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4080">0</span></span><br/>

<span data-ttu-id="cbf24-4081">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4081">1</span></span>

<span data-ttu-id="cbf24-4082">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4082">2</span></span>

<span data-ttu-id="cbf24-4083">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4083">3</span></span>

<span data-ttu-id="cbf24-4084">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4084">4</span></span>

<span data-ttu-id="cbf24-4085">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4085">5</span></span>

<span data-ttu-id="cbf24-4086">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4086">6</span></span>

<span data-ttu-id="cbf24-4087">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4087">7</span></span>

<span data-ttu-id="cbf24-4088">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4088">8</span></span>

<span data-ttu-id="cbf24-4089">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4089">9</span></span>

<span data-ttu-id="cbf24-4090">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4090">2</span></span><br/> <span data-ttu-id="cbf24-4091">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4091">0</span></span><br/>

<span data-ttu-id="cbf24-4092">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4092">1</span></span>

<span data-ttu-id="cbf24-4093">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4093">2</span></span>

<span data-ttu-id="cbf24-4094">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4094">3</span></span>

<span data-ttu-id="cbf24-4095">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4095">4</span></span>

<span data-ttu-id="cbf24-4096">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4096">5</span></span>

<span data-ttu-id="cbf24-4097">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4097">6</span></span>

<span data-ttu-id="cbf24-4098">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4098">7</span></span>

<span data-ttu-id="cbf24-4099">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4099">8</span></span>

<span data-ttu-id="cbf24-4100">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4100">9</span></span>

<span data-ttu-id="cbf24-4101">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4101">3</span></span><br/> <span data-ttu-id="cbf24-4102">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4102">0</span></span><br/>

<span data-ttu-id="cbf24-4103">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4103">1</span></span>

<span data-ttu-id="cbf24-4104">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cbf24-4104">\_hCursor</span></span>

<span data-ttu-id="cbf24-4105">\_chapt</span><span class="sxs-lookup"><span data-stu-id="cbf24-4105">\_chapt</span></span>

<span data-ttu-id="cbf24-4106">\_bmkFirst</span><span class="sxs-lookup"><span data-stu-id="cbf24-4106">\_bmkFirst</span></span>

<span data-ttu-id="cbf24-4107">\_bmkSecond</span><span class="sxs-lookup"><span data-stu-id="cbf24-4107">\_bmkSecond</span></span>



 

<span data-ttu-id="cbf24-4108">\_**hCursor:** valor de 32 bits que representa el identificador del mensaje CPMCreateQueryOut para el conjunto de filas que contiene los marcadores.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4108">\_**hCursor**: A 32-bit value representing the handle from CPMCreateQueryOut message for the rowset containing the bookmarks.</span></span>

<span data-ttu-id="cbf24-4109">\_**chapt:** valor de 32 bits que representa el identificador del capítulo que contiene los marcadores que se compararán.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4109">\_**chapt**: A 32-bit value representing the handle of the chapter containing the bookmarks to compare.</span></span>

<span data-ttu-id="cbf24-4110">\_**bmkFirst:** valor de 32 bits que representa el identificador del primer marcador que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4110">\_**bmkFirst**: A 32-bit value representing the handle to the first bookmark to compare.</span></span>

<span data-ttu-id="cbf24-4111">\_**bmkSecond:** valor de 32 bits que representa el identificador del segundo marcador que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4111">\_**bmkSecond**: A 32-bit value representing the handle to the second bookmark to compare.</span></span>

### <a name="22326-cpmcomparebmkout"></a><span data-ttu-id="cbf24-4112">2.2.3.26 CPMCompareBmkOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-4112">2.2.3.26 CPMCompareBmkOut</span></span>

<span data-ttu-id="cbf24-4113">El mensaje CPMCompareBmkOut responde a un mensaje CPMCompareBmkIn con la comparación de los dos marcadores del capítulo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4113">The CPMCompareBmkOut message replies to a CPMCompareBmkIn message with the comparison of the two bookmarks in the chapter.</span></span> <span data-ttu-id="cbf24-4114">El formato del mensaje CPMCompareBmkOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4114">The format of the CPMCompareBmkOut message that follows the header is:</span></span>



<span data-ttu-id="cbf24-4115">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4115">0</span></span>

<span data-ttu-id="cbf24-4116">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4116">1</span></span>

<span data-ttu-id="cbf24-4117">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4117">2</span></span>

<span data-ttu-id="cbf24-4118">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4118">3</span></span>

<span data-ttu-id="cbf24-4119">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4119">4</span></span>

<span data-ttu-id="cbf24-4120">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4120">5</span></span>

<span data-ttu-id="cbf24-4121">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4121">6</span></span>

<span data-ttu-id="cbf24-4122">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4122">7</span></span>

<span data-ttu-id="cbf24-4123">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4123">8</span></span>

<span data-ttu-id="cbf24-4124">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4124">9</span></span>

<span data-ttu-id="cbf24-4125">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4125">1</span></span><br/> <span data-ttu-id="cbf24-4126">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4126">0</span></span><br/>

<span data-ttu-id="cbf24-4127">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4127">1</span></span>

<span data-ttu-id="cbf24-4128">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4128">2</span></span>

<span data-ttu-id="cbf24-4129">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4129">3</span></span>

<span data-ttu-id="cbf24-4130">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4130">4</span></span>

<span data-ttu-id="cbf24-4131">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4131">5</span></span>

<span data-ttu-id="cbf24-4132">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4132">6</span></span>

<span data-ttu-id="cbf24-4133">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4133">7</span></span>

<span data-ttu-id="cbf24-4134">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4134">8</span></span>

<span data-ttu-id="cbf24-4135">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4135">9</span></span>

<span data-ttu-id="cbf24-4136">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4136">2</span></span><br/> <span data-ttu-id="cbf24-4137">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4137">0</span></span><br/>

<span data-ttu-id="cbf24-4138">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4138">1</span></span>

<span data-ttu-id="cbf24-4139">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4139">2</span></span>

<span data-ttu-id="cbf24-4140">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4140">3</span></span>

<span data-ttu-id="cbf24-4141">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4141">4</span></span>

<span data-ttu-id="cbf24-4142">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4142">5</span></span>

<span data-ttu-id="cbf24-4143">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4143">6</span></span>

<span data-ttu-id="cbf24-4144">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4144">7</span></span>

<span data-ttu-id="cbf24-4145">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4145">8</span></span>

<span data-ttu-id="cbf24-4146">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4146">9</span></span>

<span data-ttu-id="cbf24-4147">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4147">3</span></span><br/> <span data-ttu-id="cbf24-4148">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4148">0</span></span><br/>

<span data-ttu-id="cbf24-4149">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4149">1</span></span>

<span data-ttu-id="cbf24-4150">\_dwComparison</span><span class="sxs-lookup"><span data-stu-id="cbf24-4150">\_dwComparison</span></span>



 

<span data-ttu-id="cbf24-4151">\_**dwComparison:** uno de los valores siguientes, que indica las posiciones relativas de los dos marcadores del capítulo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4151">\_**dwComparison**: One of the following values, indicating the relative positions of the two bookmarks in the chapter.</span></span>



| <span data-ttu-id="cbf24-4152">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-4152">Value</span></span>                               | <span data-ttu-id="cbf24-4153">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-4153">Meaning</span></span>                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="cbf24-4154">DBCOMPARE \_ LT 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-4154">DBCOMPARE\_LT 0x00000000</span></span>            | <span data-ttu-id="cbf24-4155">El primer marcador se coloca delante del segundo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4155">The first bookmark is positioned before the second.</span></span>               |
| <span data-ttu-id="cbf24-4156">DBCOMPARE \_ EQ 0x00000001</span><span class="sxs-lookup"><span data-stu-id="cbf24-4156">DBCOMPARE\_EQ 0x00000001</span></span>            | <span data-ttu-id="cbf24-4157">El primer marcador tiene la misma posición que el segundo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4157">The first bookmark has the same position as the second.</span></span>           |
| <span data-ttu-id="cbf24-4158">DBCOMPARE \_ GT 0x00000002</span><span class="sxs-lookup"><span data-stu-id="cbf24-4158">DBCOMPARE\_GT 0x00000002</span></span>            | <span data-ttu-id="cbf24-4159">El primer marcador se coloca después del segundo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4159">The first bookmark is positioned after the second.</span></span>                |
| <span data-ttu-id="cbf24-4160">DBCOMPARE \_ NE 0x00000003</span><span class="sxs-lookup"><span data-stu-id="cbf24-4160">DBCOMPARE\_NE 0x00000003</span></span>            | <span data-ttu-id="cbf24-4161">El primer marcador no tiene la misma posición que el segundo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4161">The first bookmark does not have the same position as the second.</span></span> |
| <span data-ttu-id="cbf24-4162">DBCOMPARE \_ NOTCOMPARABLE 0x00000004</span><span class="sxs-lookup"><span data-stu-id="cbf24-4162">DBCOMPARE\_NOTCOMPARABLE 0x00000004</span></span> | <span data-ttu-id="cbf24-4163">El primer marcador no es comparable al segundo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4163">The first bookmark is not comparable to the second.</span></span>               |



 

### <a name="22327-cpmrestartpositionin"></a><span data-ttu-id="cbf24-4164">2.2.3.27 CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4164">2.2.3.27 CPMRestartPositionIn</span></span>

<span data-ttu-id="cbf24-4165">El mensaje CPMRestartPositionIn mueve la posición de captura de un cursor al principio del capítulo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4165">The CPMRestartPositionIn message moves the fetch position for a cursor to the beginning of the chapter.</span></span> <span data-ttu-id="cbf24-4166">Como se especifica en la sección 3.1.5.2.12, el servidor responderá con el mismo mensaje, con los resultados de la solicitud contenida en el campo de estado del \_ encabezado CISP.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4166">As specified in section 3.1.5.2.12, the server will reply using the same message, with the results of the request contained in the \_status field of the CISP header.</span></span>

<span data-ttu-id="cbf24-4167">El formato del mensaje CPMRestartPositionIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4167">The format of the CPMRestartPositionIn message that follows the header is:</span></span>



<span data-ttu-id="cbf24-4168">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4168">0</span></span>

<span data-ttu-id="cbf24-4169">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4169">1</span></span>

<span data-ttu-id="cbf24-4170">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4170">2</span></span>

<span data-ttu-id="cbf24-4171">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4171">3</span></span>

<span data-ttu-id="cbf24-4172">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4172">4</span></span>

<span data-ttu-id="cbf24-4173">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4173">5</span></span>

<span data-ttu-id="cbf24-4174">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4174">6</span></span>

<span data-ttu-id="cbf24-4175">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4175">7</span></span>

<span data-ttu-id="cbf24-4176">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4176">8</span></span>

<span data-ttu-id="cbf24-4177">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4177">9</span></span>

<span data-ttu-id="cbf24-4178">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4178">1</span></span><br/> <span data-ttu-id="cbf24-4179">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4179">0</span></span><br/>

<span data-ttu-id="cbf24-4180">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4180">1</span></span>

<span data-ttu-id="cbf24-4181">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4181">2</span></span>

<span data-ttu-id="cbf24-4182">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4182">3</span></span>

<span data-ttu-id="cbf24-4183">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4183">4</span></span>

<span data-ttu-id="cbf24-4184">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4184">5</span></span>

<span data-ttu-id="cbf24-4185">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4185">6</span></span>

<span data-ttu-id="cbf24-4186">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4186">7</span></span>

<span data-ttu-id="cbf24-4187">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4187">8</span></span>

<span data-ttu-id="cbf24-4188">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4188">9</span></span>

<span data-ttu-id="cbf24-4189">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4189">2</span></span><br/> <span data-ttu-id="cbf24-4190">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4190">0</span></span><br/>

<span data-ttu-id="cbf24-4191">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4191">1</span></span>

<span data-ttu-id="cbf24-4192">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4192">2</span></span>

<span data-ttu-id="cbf24-4193">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4193">3</span></span>

<span data-ttu-id="cbf24-4194">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4194">4</span></span>

<span data-ttu-id="cbf24-4195">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4195">5</span></span>

<span data-ttu-id="cbf24-4196">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4196">6</span></span>

<span data-ttu-id="cbf24-4197">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4197">7</span></span>

<span data-ttu-id="cbf24-4198">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4198">8</span></span>

<span data-ttu-id="cbf24-4199">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4199">9</span></span>

<span data-ttu-id="cbf24-4200">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4200">3</span></span><br/> <span data-ttu-id="cbf24-4201">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4201">0</span></span><br/>

<span data-ttu-id="cbf24-4202">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4202">1</span></span>

<span data-ttu-id="cbf24-4203">\_hCursor (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-4203">\_hCursor (optional)</span></span>

<span data-ttu-id="cbf24-4204">\_chapt (opcional)</span><span class="sxs-lookup"><span data-stu-id="cbf24-4204">\_chapt (optional)</span></span>



 

<span data-ttu-id="cbf24-4205">**\_ hCursor:** valor de 32 bits que representa el identificador, obtenido de un mensaje CPMCreateQueryOut, que identifica la consulta para la que se debe reiniciar la posición.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4205">**\_hCursor**: A 32-bit value representing the handle, obtained from a CPMCreateQueryOut message, which identifies the query for which to restart the position.</span></span> <span data-ttu-id="cbf24-4206">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4206">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

<span data-ttu-id="cbf24-4207">**\_ chapt:** valor de 32 bits que representa el identificador de un capítulo del que se recuperan filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4207">**\_chapt**: A 32-bit value representing the handle of a chapter from which to retrieve rows.</span></span> <span data-ttu-id="cbf24-4208">Este campo DEBE estar presente cuando el cliente envía el mensaje y DEBE estar ausente cuando el servidor envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4208">This field MUST be present when the message is sent by the client, and MUST be absent when the message is sent by the server.</span></span>

### <a name="22328-cpmfreecursorin"></a><span data-ttu-id="cbf24-4209">2.2.3.28 CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4209">2.2.3.28 CPMFreeCursorIn</span></span>

<span data-ttu-id="cbf24-4210">El mensaje CPMFreeCursorIn solicita la liberación de un cursor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4210">The CPMFreeCursorIn message requests the release of a cursor.</span></span> <span data-ttu-id="cbf24-4211">El formato del mensaje CPMFreeCursorIn que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4211">The format of the CPMFreeCursorIn message that follows the header is:</span></span>



<span data-ttu-id="cbf24-4212">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4212">0</span></span>

<span data-ttu-id="cbf24-4213">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4213">1</span></span>

<span data-ttu-id="cbf24-4214">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4214">2</span></span>

<span data-ttu-id="cbf24-4215">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4215">3</span></span>

<span data-ttu-id="cbf24-4216">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4216">4</span></span>

<span data-ttu-id="cbf24-4217">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4217">5</span></span>

<span data-ttu-id="cbf24-4218">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4218">6</span></span>

<span data-ttu-id="cbf24-4219">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4219">7</span></span>

<span data-ttu-id="cbf24-4220">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4220">8</span></span>

<span data-ttu-id="cbf24-4221">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4221">9</span></span>

<span data-ttu-id="cbf24-4222">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4222">1</span></span><br/> <span data-ttu-id="cbf24-4223">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4223">0</span></span><br/>

<span data-ttu-id="cbf24-4224">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4224">1</span></span>

<span data-ttu-id="cbf24-4225">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4225">2</span></span>

<span data-ttu-id="cbf24-4226">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4226">3</span></span>

<span data-ttu-id="cbf24-4227">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4227">4</span></span>

<span data-ttu-id="cbf24-4228">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4228">5</span></span>

<span data-ttu-id="cbf24-4229">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4229">6</span></span>

<span data-ttu-id="cbf24-4230">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4230">7</span></span>

<span data-ttu-id="cbf24-4231">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4231">8</span></span>

<span data-ttu-id="cbf24-4232">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4232">9</span></span>

<span data-ttu-id="cbf24-4233">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4233">2</span></span><br/> <span data-ttu-id="cbf24-4234">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4234">0</span></span><br/>

<span data-ttu-id="cbf24-4235">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4235">1</span></span>

<span data-ttu-id="cbf24-4236">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4236">2</span></span>

<span data-ttu-id="cbf24-4237">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4237">3</span></span>

<span data-ttu-id="cbf24-4238">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4238">4</span></span>

<span data-ttu-id="cbf24-4239">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4239">5</span></span>

<span data-ttu-id="cbf24-4240">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4240">6</span></span>

<span data-ttu-id="cbf24-4241">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4241">7</span></span>

<span data-ttu-id="cbf24-4242">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4242">8</span></span>

<span data-ttu-id="cbf24-4243">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4243">9</span></span>

<span data-ttu-id="cbf24-4244">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4244">3</span></span><br/> <span data-ttu-id="cbf24-4245">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4245">0</span></span><br/>

<span data-ttu-id="cbf24-4246">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4246">1</span></span>

<span data-ttu-id="cbf24-4247">\_hCursor</span><span class="sxs-lookup"><span data-stu-id="cbf24-4247">\_hCursor</span></span>



 

<span data-ttu-id="cbf24-4248">**\_ hCursor:** valor de 32 bits que representa el identificador del cursor del mensaje CPMCreateQueryOut que se liberará.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4248">**\_hCursor**: A 32-bit value representing the handle of the cursor from the CPMCreateQueryOut message to release.</span></span>

### <a name="22329-cpmfreecursorout"></a><span data-ttu-id="cbf24-4249">2.2.3.29 CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-4249">2.2.3.29 CPMFreeCursorOut</span></span>

<span data-ttu-id="cbf24-4250">El mensaje CPMFreeCursorOut responde a un mensaje CPMFreeCursorIn con los resultados de liberar un cursor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4250">The CPMFreeCursorOut message replies to a CPMFreeCursorIn message with the results of freeing a cursor.</span></span> <span data-ttu-id="cbf24-4251">El formato del mensaje CPMFreeCursorOut que sigue al encabezado es:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4251">The format of the CPMFreeCursorOut message that follows the header is:</span></span>



<span data-ttu-id="cbf24-4252">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4252">0</span></span>

<span data-ttu-id="cbf24-4253">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4253">1</span></span>

<span data-ttu-id="cbf24-4254">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4254">2</span></span>

<span data-ttu-id="cbf24-4255">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4255">3</span></span>

<span data-ttu-id="cbf24-4256">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4256">4</span></span>

<span data-ttu-id="cbf24-4257">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4257">5</span></span>

<span data-ttu-id="cbf24-4258">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4258">6</span></span>

<span data-ttu-id="cbf24-4259">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4259">7</span></span>

<span data-ttu-id="cbf24-4260">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4260">8</span></span>

<span data-ttu-id="cbf24-4261">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4261">9</span></span>

<span data-ttu-id="cbf24-4262">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4262">1</span></span><br/> <span data-ttu-id="cbf24-4263">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4263">0</span></span><br/>

<span data-ttu-id="cbf24-4264">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4264">1</span></span>

<span data-ttu-id="cbf24-4265">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4265">2</span></span>

<span data-ttu-id="cbf24-4266">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4266">3</span></span>

<span data-ttu-id="cbf24-4267">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4267">4</span></span>

<span data-ttu-id="cbf24-4268">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4268">5</span></span>

<span data-ttu-id="cbf24-4269">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4269">6</span></span>

<span data-ttu-id="cbf24-4270">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4270">7</span></span>

<span data-ttu-id="cbf24-4271">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4271">8</span></span>

<span data-ttu-id="cbf24-4272">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4272">9</span></span>

<span data-ttu-id="cbf24-4273">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4273">2</span></span><br/> <span data-ttu-id="cbf24-4274">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4274">0</span></span><br/>

<span data-ttu-id="cbf24-4275">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4275">1</span></span>

<span data-ttu-id="cbf24-4276">2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4276">2</span></span>

<span data-ttu-id="cbf24-4277">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4277">3</span></span>

<span data-ttu-id="cbf24-4278">4</span><span class="sxs-lookup"><span data-stu-id="cbf24-4278">4</span></span>

<span data-ttu-id="cbf24-4279">5</span><span class="sxs-lookup"><span data-stu-id="cbf24-4279">5</span></span>

<span data-ttu-id="cbf24-4280">6</span><span class="sxs-lookup"><span data-stu-id="cbf24-4280">6</span></span>

<span data-ttu-id="cbf24-4281">7</span><span class="sxs-lookup"><span data-stu-id="cbf24-4281">7</span></span>

<span data-ttu-id="cbf24-4282">8</span><span class="sxs-lookup"><span data-stu-id="cbf24-4282">8</span></span>

<span data-ttu-id="cbf24-4283">9</span><span class="sxs-lookup"><span data-stu-id="cbf24-4283">9</span></span>

<span data-ttu-id="cbf24-4284">3</span><span class="sxs-lookup"><span data-stu-id="cbf24-4284">3</span></span><br/> <span data-ttu-id="cbf24-4285">0</span><span class="sxs-lookup"><span data-stu-id="cbf24-4285">0</span></span><br/>

<span data-ttu-id="cbf24-4286">1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4286">1</span></span>

<span data-ttu-id="cbf24-4287">\_cCursorsRemaining</span><span class="sxs-lookup"><span data-stu-id="cbf24-4287">\_cCursorsRemaining</span></span>



 

<span data-ttu-id="cbf24-4288">**\_ cCursorsRemaining:** entero de 32 bits sin signo que indica el número de cursores que siguen en uso para la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4288">**\_cCursorsRemaining**: A 32-bit unsigned integer indicating the number of cursors still in use for the query.</span></span>

### <a name="22330-cpmdisconnect"></a><span data-ttu-id="cbf24-4289">2.2.3.30 CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="cbf24-4289">2.2.3.30 CPMDisconnect</span></span>

<span data-ttu-id="cbf24-4290">El mensaje CPMDisconnect finaliza la conexión con el servidor</span><span class="sxs-lookup"><span data-stu-id="cbf24-4290">The CPMDisconnect message ends the connection with the server</span></span>

<span data-ttu-id="cbf24-4291">El mensaje NO DEBE incluir un cuerpo; solo se enviará el encabezado del mensaje, tal como se especifica en la sección 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4291">The message MUST NOT include a body; only the message header, as specified in Section 2.2.2 is to be sent.</span></span>

### <a name="224-errors"></a><span data-ttu-id="cbf24-4292">2.2.4 Errores</span><span class="sxs-lookup"><span data-stu-id="cbf24-4292">2.2.4 Errors</span></span>

<span data-ttu-id="cbf24-4293">Todos los mensajes de Content Indexing Service Protocol DEBEN devolver 0x00000000 correcto; De lo contrario, devuelven un código de error distinto de cero de 32 bits que puede ser un valor HRESULT o NTSTATUS (consulte la sección 1.8).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4293">All Content Indexing Service Protocol messages MUST return 0x00000000 on success; otherwise, they return a 32-bit nonzero error code which can be either an HRESULT or an NTSTATUS value (see section 1.8).</span></span> <span data-ttu-id="cbf24-4294">Si un búfer es demasiado pequeño para ajustarse a un resultado, se debe devolver un código de estado de STATUS \_ INSUFFICIENT RESOURCES (0xC0000009A) y la operación con errores debe reinterse con un búfer \_ mayor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4294">If a buffer is too small to fit a result, a status code of STATUS\_INSUFFICIENT\_RESOURCES (0xC0000009A) MUST be returned and the failing operation should be retried with a larger buffer.</span></span>

<span data-ttu-id="cbf24-4295">Todos los demás valores de error DEBEN tratarse igual.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4295">All other error values MUST be treated the same.</span></span>

<span data-ttu-id="cbf24-4296">(Tenga en cuenta que actualmente los espacios de numeración HRESULT y NTSTATUS no se superponen excepto con valores de significado idéntico, pero incluso si estuvieran en conflicto en el futuro, no produciría ningún problema de protocolo siempre que el valor de STATUS \_ INSUFFICIENT \_ RESOURCES sigue siendo único, ya que todos los demás valores de error se tratan igual).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4296">(Note that currently the HRESULT and NTSTATUS numbering spaces do not overlap except with values of identical meaning, but even if they were to be conflicts in the future, it would not cause any protocol issues as long as the value for STATUS\_INSUFFICIENT\_RESOURCES remains unique, since all other error values are treated the same.)</span></span>

## <a name="3-protocol-details"></a><span data-ttu-id="cbf24-4297">3 Detalles del protocolo</span><span class="sxs-lookup"><span data-stu-id="cbf24-4297">3 Protocol Details</span></span>

-   [<span data-ttu-id="cbf24-4298">3.1 Detalles del servidor</span><span class="sxs-lookup"><span data-stu-id="cbf24-4298">3.1 Server Details</span></span>](#31-server-details)
-   [<span data-ttu-id="cbf24-4299">3.2 Detalles del cliente</span><span class="sxs-lookup"><span data-stu-id="cbf24-4299">3.2 Client Details</span></span>](#32-client-details)

<span data-ttu-id="cbf24-4300">Las solicitudes de mensajes CISP para consultar de forma remota los catálogos del servicio de indexación no requieren ninguna secuencia determinada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4300">CISP message requests for remotely querying the indexing service catalogs do not require any particular sequence.</span></span> <span data-ttu-id="cbf24-4301">Sin embargo, se recomienda que la capa superior se ajuste a una secuencia de mensajes significativa, como en el caso de los mensajes que se reciben fuera de esta secuencia o con datos no válidos, el servidor responderá con un error.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4301">It is advised that the higher layer adhere to a meaningful message sequence though, as for messages that are received out of this sequence or with invalid data, the server will respond with an error.</span></span> <span data-ttu-id="cbf24-4302">Algunos mensajes también dependen de la capa superior que proporciona datos válidos que se recibieron en los mensajes anteriores de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4302">Some messages are also dependent on the higher layer providing valid data that was received in messages earlier in the sequence.</span></span>

<span data-ttu-id="cbf24-4303">En el diagrama siguiente se muestra una secuencia de mensajes típica para una consulta simple desde un cliente a un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4303">A typical message sequence for a simple query from a client to a remote computer is illustrated in the following diagram.</span></span>

![secuencia de mensajes para una consulta simple](images/protocoldetails.jpg)

<span data-ttu-id="cbf24-4305">Los mensajes representados en el diagrama anterior representan un subconjunto de todos los mensajes CISP usados para consultar un catálogo de servicios de indexación remota.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4305">The messages represented in the preceding diagram represent a subset of all of the CISP messages used for querying a remote indexing service catalog.</span></span>

### <a name="31-server-details"></a><span data-ttu-id="cbf24-4306">3.1 Detalles del servidor</span><span class="sxs-lookup"><span data-stu-id="cbf24-4306">3.1 Server Details</span></span>

### <a name="311-abstract-data-model"></a><span data-ttu-id="cbf24-4307">3.1.1 Modelo de datos abstracto</span><span class="sxs-lookup"><span data-stu-id="cbf24-4307">3.1.1 Abstract Data Model</span></span>

<span data-ttu-id="cbf24-4308">En la sección siguiente se especifican los datos y el estado que mantiene el servidor CISP.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4308">The following section specifies data and state maintained by the CISP server.</span></span> <span data-ttu-id="cbf24-4309">Los datos que se proporcionan aquí son para facilitar la explicación de cómo se comporta el protocolo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4309">The data provided here is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="cbf24-4310">Esta sección no exige que las implementaciones se adhieran a este modelo, siempre que su comportamiento externo sea coherente con el descrito en este documento.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4310">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="cbf24-4311">Un servicio de indexación que implementa CISP DEBE mantener los siguientes elementos de datos abstractos:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4311">An indexing service implementing the CISP MUST maintain the following abstract data elements:</span></span>

-   <span data-ttu-id="cbf24-4312">Lista de clientes conectados al servidor</span><span class="sxs-lookup"><span data-stu-id="cbf24-4312">The list of clients connected to the server</span></span>
-   <span data-ttu-id="cbf24-4313">Información sobre cada cliente, que incluye:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4313">Information about each client, which includes:</span></span>
-   -   <span data-ttu-id="cbf24-4314">Versión del cliente (como se indica en el mensaje CPMConnectIn especificado en la sección 2.2.3.6)</span><span class="sxs-lookup"><span data-stu-id="cbf24-4314">Client's version (as indicated in the CPMConnectIn message specified in section 2.2.3.6)</span></span>
    -   <span data-ttu-id="cbf24-4315">Catálogo asociado al cliente (por un mensaje CPMConnectIn)</span><span class="sxs-lookup"><span data-stu-id="cbf24-4315">Catalog associated with the client (by a CPMConnectIn message)</span></span>
    -   <span data-ttu-id="cbf24-4316">Propiedades de cliente adicionales como se especifica en la sección 2.2.1.21.1.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4316">Additional client properties as specified in section 2.2.1.21.1.</span></span>
    -   <span data-ttu-id="cbf24-4317">Consulta de búsqueda del cliente</span><span class="sxs-lookup"><span data-stu-id="cbf24-4317">Client's search query</span></span>
    -   <span data-ttu-id="cbf24-4318">Lista de identificadores de cursor para la consulta y la posición en el conjunto de resultados para cada identificador.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4318">List of cursor handles for the query and position in result set for each handle.</span></span>
    -   <span data-ttu-id="cbf24-4319">Conjunto actual de enlaces</span><span class="sxs-lookup"><span data-stu-id="cbf24-4319">Current set of bindings</span></span>
    -   <span data-ttu-id="cbf24-4320">Estado actual de la consulta que incluye (para cada cursor):</span><span class="sxs-lookup"><span data-stu-id="cbf24-4320">Current status of the query which includes (for each cursor):</span></span>
    -   -   <span data-ttu-id="cbf24-4321">Número de filas en el resultado de la consulta</span><span class="sxs-lookup"><span data-stu-id="cbf24-4321">Number of rows in query result</span></span>
        -   <span data-ttu-id="cbf24-4322">Numerador y denominador de la finalización de consultas</span><span class="sxs-lookup"><span data-stu-id="cbf24-4322">Numerator and denominator of query completion</span></span>
        -   <span data-ttu-id="cbf24-4323">Último número de filas, notificado por el mensaje CPMRatioFinishedOut más reciente para este cursor</span><span class="sxs-lookup"><span data-stu-id="cbf24-4323">Last number of rows, reported by most recent CPMRatioFinishedOut message for this cursor</span></span>
        -   <span data-ttu-id="cbf24-4324">Si el servidor supervisa la consulta en busca de cambios en los resultados de la consulta y si se supervisa, qué ha cambiado en los resultados de la consulta desde que CPMSendNotifyOut la informó por última vez al cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4324">Whether the query is monitored by the server for changes in query results and if it is monitored, what changed in the query results since it was last reported to client by CPMSendNotifyOut</span></span>
        -   <span data-ttu-id="cbf24-4325">Lista de identificadores de capítulos que sirve esta consulta a un cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4325">List of chapters handles, served by this query to a client.</span></span>
        -   <span data-ttu-id="cbf24-4326">Lista de identificadores de marcador para cada cursor, que sirve esta consulta a un cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4326">List of bookmark handles for each cursor, served by this query to a client.</span></span>

-   <span data-ttu-id="cbf24-4327">Estado actual del servicio de indexación, que puede ser "no inicializado", "en ejecución" o "apagado".</span><span class="sxs-lookup"><span data-stu-id="cbf24-4327">The current state of the indexing service, which may be "not initialized", "running", or "shutting down".</span></span> <span data-ttu-id="cbf24-4328">Tenga en cuenta que la mayoría de las veces el servidor está en estado "en ejecución".</span><span class="sxs-lookup"><span data-stu-id="cbf24-4328">Note that most of the time server is in "running" state.</span></span> <span data-ttu-id="cbf24-4329">A continuación se muestra el diagrama de la máquina de estado para el servidor:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4329">Following is the state machine diagram for the server:</span></span>

    ![diagrama de máquina de estado del servidor de servicio de indexación](images/abstractdatamodel.jpg)

-   <span data-ttu-id="cbf24-4331">Información por catálogo: número de documentos indexados, tamaño del índice, número de claves únicas, etc. (consulte la sección 2.2.3.1 para obtener una lista completa), estado (que corresponde a los valores de dwNewState en la sección 2.2.3.2).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4331">Per-catalog information: number of documents indexed, size of index, number of unique keys, etc (see section 2.2.3.1 for complete list), state (which corresponds to the values of dwNewState in section 2.2.3.2).</span></span>
-   <span data-ttu-id="cbf24-4332">Para cada idioma admitido, una base de datos de variaciones de palabras como se describe en la sección 2.2.1.3.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4332">For each language supported, a database of word variations as discussed in section 2.2.1.3.</span></span>

### <a name="312-timers"></a><span data-ttu-id="cbf24-4333">3.1.2 Temporizadores</span><span class="sxs-lookup"><span data-stu-id="cbf24-4333">3.1.2 Timers</span></span>

<span data-ttu-id="cbf24-4334">No se requiere ningún temporizador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4334">No protocol timers are required.</span></span>

### <a name="313-initialization"></a><span data-ttu-id="cbf24-4335">3.1.3 Inicialización</span><span class="sxs-lookup"><span data-stu-id="cbf24-4335">3.1.3 Initialization</span></span>

<span data-ttu-id="cbf24-4336">Tras la inicialización, el servidor DEBE establecer su estado en "no inicializado" y empezar a escuchar mensajes en la canalización con nombre especificada en la sección 1.9.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4336">Upon initialization, the server MUST set its state to "not initialized" and start listening for messages on the named pipe specified in section 1.9.</span></span> <span data-ttu-id="cbf24-4337">Después de realizar cualquier otra inicialización interna, DEBE pasar al estado "en ejecución".</span><span class="sxs-lookup"><span data-stu-id="cbf24-4337">After doing any other internal initialization, it MUST transition to the "running" state.</span></span>

### <a name="314-higher-layer-triggered-events"></a><span data-ttu-id="cbf24-4338">3.1.4 Eventos desencadenados al más alto nivel</span><span class="sxs-lookup"><span data-stu-id="cbf24-4338">3.1.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="cbf24-4339">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4339">None.</span></span>

### <a name="315-message-processing-and-sequencing-rules"></a><span data-ttu-id="cbf24-4340">3.1.5 Reglas de procesamiento y secuenciación de mensajes</span><span class="sxs-lookup"><span data-stu-id="cbf24-4340">3.1.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="cbf24-4341">Cada vez que se produce un error durante el procesamiento de un mensaje enviado por un cliente, el servidor DEBE notificar un error al cliente como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4341">Whenever there is an error occurs during processing of a message sent by a client the server MUST report an error back to the client as follows:</span></span>

-   <span data-ttu-id="cbf24-4342">Detener el procesamiento del mensaje enviado por el cliente</span><span class="sxs-lookup"><span data-stu-id="cbf24-4342">Stop processing the message sent by the client</span></span>
-   <span data-ttu-id="cbf24-4343">Responda con el encabezado del mensaje (solo) del mensaje enviado por el cliente, manteniendo \_ intacto el campo msg.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4343">Respond with the message header (only) of the message sent by the client, keeping \_msg field intact.</span></span>
-   <span data-ttu-id="cbf24-4344">Establezca el \_ campo de estado en el valor del código de error.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4344">Set the \_status field to the error code value.</span></span>

<span data-ttu-id="cbf24-4345">Cuando llega un mensaje, el servidor DEBE comprobar el valor del campo msg para ver si es un tipo conocido (consulte la \_ sección 2.2.2).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4345">When a message arrives, the server MUST check the \_msg field value to see if it is a known type (see section 2.2.2).</span></span> <span data-ttu-id="cbf24-4346">Si no se conoce el tipo, DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4346">If the type is not known, it MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="cbf24-4347">A continuación, el servidor DEBE validar el valor del campo \_ ulChecksum si el tipo de mensaje es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4347">The server MUST then validate the \_ulChecksum field value if the message type is one of the following:</span></span>

-   <span data-ttu-id="cbf24-4348">CPMConnectIn (0x000000C8)</span><span class="sxs-lookup"><span data-stu-id="cbf24-4348">CPMConnectIn (0x000000C8)</span></span>
-   <span data-ttu-id="cbf24-4349">CPMCreateQueryIn (0x000000CA)</span><span class="sxs-lookup"><span data-stu-id="cbf24-4349">CPMCreateQueryIn (0x000000CA)</span></span>
-   <span data-ttu-id="cbf24-4350">CPMSetBindingsIn (0x000000D0)</span><span class="sxs-lookup"><span data-stu-id="cbf24-4350">CPMSetBindingsIn (0x000000D0)</span></span>
-   <span data-ttu-id="cbf24-4351">CPMGetRowsIn (0x000000CC)</span><span class="sxs-lookup"><span data-stu-id="cbf24-4351">CPMGetRowsIn (0x000000CC)</span></span>
-   <span data-ttu-id="cbf24-4352">CPMFetchValueIn (0x000000E4)</span><span class="sxs-lookup"><span data-stu-id="cbf24-4352">CPMFetchValueIn (0x000000E4)</span></span>

<span data-ttu-id="cbf24-4353">Para validar el valor del campo ulChecksum, el servidor DEBE comprobar el valor que el cliente especificó en el campo iClientVersion en el \_ \_ mensaje CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4353">To validate the \_ulChecksum field value, the server MUST check the value the client specified in the \_iClientVersion field in the CPMConnectIn message.</span></span>

<span data-ttu-id="cbf24-4354">Si el campo iClientVersion no está establecido en 0x00000008 y el campo ulChecksum no está establecido en 0x00000000, el servidor DEBE notificar un \_ error STATUS INVALID PARAMETER \_ \_ \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4354">If the \_iClientVersion field is not set to 0x00000008 and the \_ulChecksum field is not set to 0x00000000, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="cbf24-4355">El servidor NO DEBE validar el campo ulChecksum para los clientes y establecer el campo iClientVersion en un \_ \_ valor menor que 0x00000008.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4355">Server MUST NOT validate the \_ulChecksum field for clients the set the \_iClientVersion field to a value less than 0x00000008.</span></span>

<span data-ttu-id="cbf24-4356">Si el valor del campo iClientVersionfield es 0x00000008 o superior, el servidor DEBE validar que el campo ulChecksum se calculó como se especifica en la sección \_ \_ 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4356">If the \_iClientVersionfield field value is 0x00000008 or greater, the server MUST validate that the \_ulChecksum field was calculated as specified in section 3.2.4.</span></span> <span data-ttu-id="cbf24-4357">Si el \_ valor ulChecksum no es válido, el servidor DEBE notificar un error STATUS \_ INVALID PARAMETER \_ (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4357">If the \_ulChecksum value is invalid, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>

<span data-ttu-id="cbf24-4358">A continuación, el servidor comprueba en qué estado se encuentra.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4358">Next, the server checks which state is it in.</span></span> <span data-ttu-id="cbf24-4359">Si su estado es "no inicializado", el servidor DEBE notificar un error CI \_ E \_ NOT \_ INITIALIZED (0x8004180B).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4359">If its state is "not initialized" the server MUST report a CI\_E\_NOT\_INITIALIZED (0x8004180B) error.</span></span> <span data-ttu-id="cbf24-4360">Si el estado es "apagar", el servidor DEBE notificar un error CI \_ E \_ SHUTDOWN (0x80041812).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4360">If the state is "shutting down" the server MUST report a CI\_E\_SHUTDOWN (0x80041812) error.</span></span>

<span data-ttu-id="cbf24-4361">Una vez que se ha determinado que un encabezado es válido y que el servidor está en estado "en ejecución", se DEBE realizar un procesamiento más específico del mensaje tal como se especifica en las subsecciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4361">Once a header has been determined to be valid and the server to be in "running" state, further message-specific processing MUST be done as specified in the subsections below.</span></span>

### <a name="3151-remote-indexing-service-catalog-management"></a><span data-ttu-id="cbf24-4362">3.1.5.1 Remote Indexing Service Catalog Management</span><span class="sxs-lookup"><span data-stu-id="cbf24-4362">3.1.5.1 Remote Indexing Service Catalog Management</span></span>

### <a name="31511-receiving-a-cpmcistateinout-request"></a><span data-ttu-id="cbf24-4363">3.1.5.1.1 Recepción de una solicitud CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-4363">3.1.5.1.1 Receiving a CPMCiStateInOut Request</span></span>

<span data-ttu-id="cbf24-4364">Cuando el servidor recibe una solicitud de mensaje CPMCIStateInOut del cliente, el servidor debe comprobar primero si el cliente está en una lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4364">When the server receives a CPMCIStateInOut message request from the client, the server MUST first check if the client is in a list of connected clients.</span></span> <span data-ttu-id="cbf24-4365">Si el cliente no está en la lista, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4365">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span> <span data-ttu-id="cbf24-4366">De lo contrario, DEBE responder al cliente con un mensaje CPMCIStateInOut, rellenando con información sobre el catálogo asociado del cliente, tal como se especifica en la sección 2.2.3.1.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4366">Otherwise, it MUST respond to the client with a CPMCIStateInOut message, filling it in with information about the client's associated catalog as specified in Section 2.2.3.1.</span></span>

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a><span data-ttu-id="cbf24-4367">3.1.5.1.2 Recepción de una solicitud CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4367">3.1.5.1.2 Receiving a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="cbf24-4368">Cuando el servidor recibe una solicitud de mensaje CPMSetCatStateIn del cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4368">When the server receives a CPMSetCatStateIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4369">Compruebe que el cliente tiene acceso administrativo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4369">Check that client has administrative access.</span></span> <span data-ttu-id="cbf24-4370">Si el cliente no tiene acceso administrativo, el servidor DEBE notificar un error STATUS \_ ACCESS \_ DENIED (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4370">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="cbf24-4371">Si dwNewState no es igual a CICAT ALL OPENED, cambie el estado del catálogo especificado en el campo CatName según lo especificado por el \_ \_ campo \_ \_ dwNewState.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4371">If \_dwNewState is not equal to CICAT\_ALL\_OPENED then change the state of the catalog specified in the CatName field as specified by the \_dwNewState field.</span></span> <span data-ttu-id="cbf24-4372">Consulte la sección 2.2.3.2 para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4372">See Section 2.2.3.2 for more details.</span></span> <span data-ttu-id="cbf24-4373">Si el servidor no encuentra un catálogo con el nombre especificado en el campo CatName, el servidor DEBE devolver un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4373">If the server does not locate a catalog with the name specified in the CatName field, the server MUST return a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cbf24-4374">Responda al cliente con un mensaje CPMSetCatStateOut, donde dwOldState DEBE establecerse en \_ el estado anterior del catálogo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4374">Respond to the client with a CPMSetCatStateOut message, where \_dwOldState MUST be set to the previous state of the catalog.</span></span> <span data-ttu-id="cbf24-4375">Si dwNewState es igual a CICAT ALL OPENED, el servidor DEBE comprobar el estado de todos los catálogos y, si todos ellos se inician, debe establecer dwOldState en 0x00000001 y, de lo \_ \_ \_ \_ contrario, \_ establecer dwOldState en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4375">If \_dwNewState is equal to CICAT\_ALL\_OPENED the server MUST check the status of all catalogs and if all of them are started it MUST set \_dwOldState to 0x00000001, and otherwise set \_dwOldState to 0x00000000.</span></span>

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="cbf24-4376">3.1.5.1.3 Recepción de una solicitud CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4376">3.1.5.1.3 Receiving a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="cbf24-4377">Cuando el servidor recibe una solicitud de mensaje CPMUpdateDocumentsIn, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4377">When the server receives a CPMUpdateDocumentsIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4378">Compruebe si el cliente está en una lista de clientes conectados (que tienen un catálogo asociado).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4378">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="cbf24-4379">Si el cliente no está en la lista, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4379">If client is not in the list, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cbf24-4380">Compruebe que el cliente tiene acceso administrativo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4380">Check that client has administrative access.</span></span> <span data-ttu-id="cbf24-4381">Si el cliente no tiene acceso administrativo al servidor, el servidor DEBE notificar un error DE ACCESO DE ESTADO DENEGADO \_ \_ (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4381">If the client does not have administrative access to the server, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="cbf24-4382">Comience el proceso de indexación de la ruta de acceso especificada por el cliente, realizando un examen completo o incremental, en función del valor del campo de marca en el mensaje \_ CPMUpdateDocumentsIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4382">Begin the process of indexing the path specified by the client, doing a full or incremental scan, depending on value of \_flag field in CPMUpdateDocumentsIn message.</span></span> <span data-ttu-id="cbf24-4383">Si la ruta de acceso no se indexó previamente, DEBE agregarse a la colección de ubicaciones indizadas y realizar un examen completo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4383">If the path was not previously indexed, it MUST be added to the collection of indexed locations and a full scan performed.</span></span> <span data-ttu-id="cbf24-4384">Si se especifica un valor no válido del campo de marca, el servidor DEBE actuar como si la marca se hubiera establecido en UPD INIT y realizar \_ \_ un examen \_ completo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4384">If an illegal value of the \_flag field is specified, the server MUST act as if \_flag was set to UPD\_INIT and perform a full scan.</span></span> <span data-ttu-id="cbf24-4385">Esta operación DEBE realizarse en el catálogo asociado al cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4385">This operation MUST be performed in the catalog associated with the client.</span></span>
-   <span data-ttu-id="cbf24-4386">Responda al cliente con el encabezado de mensaje para CPMUpdateDocumentsIn y establezca el campo de estado \_ en los resultados de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4386">Respond to the client with the message header for the CPMUpdateDocumentsIn, and set the \_status field to the results of the request.</span></span>

### <a name="31514-receiving-a-cpmforcemergein-request"></a><span data-ttu-id="cbf24-4387">3.1.5.1.4 Recepción de una solicitud CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4387">3.1.5.1.4 Receiving a CPMForceMergeIn Request</span></span>

<span data-ttu-id="cbf24-4388">Cuando el servidor recibe una solicitud de mensaje CPMForceMergeIn, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4388">When the server receives a CPMForceMergeIn message request, the server MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4389">Compruebe si el cliente está en una lista de clientes conectados (que tienen un catálogo asociado).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4389">Check if the client is in a list of connected clients (which have a catalog associated).</span></span> <span data-ttu-id="cbf24-4390">Si el cliente no está en la lista, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4390">If client is not in the list the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cbf24-4391">Compruebe que el cliente tiene acceso administrativo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4391">Check that client has administrative access.</span></span> <span data-ttu-id="cbf24-4392">Si el cliente no tiene acceso administrativo, el servidor DEBE notificar un error STATUS \_ ACCESS \_ DENIED (0xC0000022).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4392">If the client does not have administrative access, the server MUST report a STATUS\_ACCESS\_DENIED (0xC0000022) error.</span></span>
-   <span data-ttu-id="cbf24-4393">Inicie cualquier proceso de mantenimiento necesario para mejorar el rendimiento de las consultas en un catálogo, asociado al cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4393">Begin any process of maintenance necessary to improve query performance on a catalog, associated with the client.</span></span>
-   <span data-ttu-id="cbf24-4394">Responda al cliente con un encabezado de mensaje para CPMForceMergeIn y establezca el campo de estado \_ en los resultados de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4394">Respond to the client with a message header for the CPMForceMergeIn, and set the \_status field to the results of the request.</span></span>

<span data-ttu-id="cbf24-4395">Tenga en cuenta que el proceso de mantenimiento es asincrónico y puede continuar después de que el cliente reciba el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4395">Note that process of maintenance is asynchronous and can continue after client receives the response message.</span></span> <span data-ttu-id="cbf24-4396">Este proceso no afecta directamente al protocolo de ninguna manera (aparte del tiempo de respuesta).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4396">This process does not directly impact the protocol in any way (other than response time).</span></span>

### <a name="3152-remote-indexing-service-querying"></a><span data-ttu-id="cbf24-4397">3.1.5.2 Consultas remotas del servicio de indexación</span><span class="sxs-lookup"><span data-stu-id="cbf24-4397">3.1.5.2 Remote Indexing Service Querying</span></span>

### <a name="31521-receiving-a-cpmconnectin-request"></a><span data-ttu-id="cbf24-4398">3.1.5.2.1 Recepción de una solicitud CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4398">3.1.5.2.1 Receiving a CPMConnectIn Request</span></span>

<span data-ttu-id="cbf24-4399">Cuando el servidor recibe una solicitud CPMConnectIn de un cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4399">When the server receives a CPMConnectIn request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4400">Compruebe si el cliente está en la lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4400">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="cbf24-4401">Si este es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4401">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cbf24-4402">Comprueba si el catálogo especificado existe y no está en estado detenido.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4402">Checks if the specified catalog exists and not in the stopped state.</span></span> <span data-ttu-id="cbf24-4403">Si este no es el caso, el servidor DEBE notificar un error CI \_ E \_ NO CATALOG \_ (0x8004181D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4403">If this is not the case then the server MUST a report CI\_E\_NO\_CATALOG (0x8004181D) error.</span></span>
-   <span data-ttu-id="cbf24-4404">Agregue el cliente a la lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4404">Add the client to the list of connected clients.</span></span>
-   <span data-ttu-id="cbf24-4405">Asocie el catálogo al cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4405">Associate the catalog with the client.</span></span>
-   <span data-ttu-id="cbf24-4406">Almacene la información pasada en el mensaje CPMConnectIn (como el nombre del catálogo, la versión del cliente, etc.) en el estado de cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4406">Store the information passed in the CPMConnectIn message (such as catalog name, client version, etc.) in the client state.</span></span>
-   <span data-ttu-id="cbf24-4407">Responda al cliente con un mensaje CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4407">Respond to the client with a CPMConnectOut message.</span></span>

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a><span data-ttu-id="cbf24-4408">3.1.5.2.2 Recepción de una solicitud CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4408">3.1.5.2.2 Receiving a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="cbf24-4409">Cuando el servidor recibe una solicitud de mensaje CPMCreateQueryIn de un cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4409">When the server receives a CPMCreateQueryIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4410">Compruebe si el cliente está en la lista de clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4410">Check if the client is in the list of connected clients.</span></span> <span data-ttu-id="cbf24-4411">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4411">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cbf24-4412">Compruebe si el cliente ya tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4412">Check if the client already has a query associated with it.</span></span> <span data-ttu-id="cbf24-4413">Si este es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4413">If this is the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cbf24-4414">Compruebe si el catálogo asociado al cliente está en estado que permite procesar la consulta (CICAT \_ READONLY o CICAT \_ WRITABLE).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4414">Check if the catalog associated with the client is in state which allows query to be processed (CICAT\_READONLY or CICAT\_WRITABLE).</span></span> <span data-ttu-id="cbf24-4415">Si este no es el caso, el servidor DEBE notificar un error QUERY \_ S \_ NO QUERY \_ (0x8004160C).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4415">If this is not the case, the server MUST report a QUERY\_S\_NO\_QUERY (0x8004160C) error.</span></span>
-   <span data-ttu-id="cbf24-4416">Analice el conjunto de restricciones, los criterios de ordenación y las agrupaciones especificados en la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4416">Parse the restriction set, sort orders, and groupings specified in the query.</span></span> <span data-ttu-id="cbf24-4417">Si el servidor encuentra un error, DEBE notificar un error adecuado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4417">If the server encounters an error, it MUST report an appropriate error.</span></span> <span data-ttu-id="cbf24-4418">Si se produce un error en este paso por cualquier otro motivo, el servidor DEBE notificar el error encontrado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4418">If this step fails for any other reason, the server MUST report the error encountered.</span></span> <span data-ttu-id="cbf24-4419">Para obtener información sobre los errores de consulta del servicio de indexación, \[ vea MSDN-QUERYERR \] .</span><span class="sxs-lookup"><span data-stu-id="cbf24-4419">For information about indexing service query errors, see \[MSDN-QUERYERR\].</span></span>
-   <span data-ttu-id="cbf24-4420">Guarde la consulta de búsqueda en el estado del cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4420">Save the search query in the state for the client.</span></span>
-   <span data-ttu-id="cbf24-4421">Realice los preparativos necesarios para atender filas a un cliente y asocie la consulta con los identificadores de cursor adecuados (en función de la información que se pase en el mensaje CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4421">Make any preparations needed to serve rows to a client and associate the query with appropriate cursor handles (depending on information passed in CPMCreateQueryIn message).</span></span>
-   <span data-ttu-id="cbf24-4422">Agregue esos identificadores a la lista de identificadores de cursor del cliente e inicialice listas de identificadores de capítulos y marcadores.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4422">Add those handles to client's list of cursor handles, and initialize lists of chapter handles and bookmarks.</span></span>
-   <span data-ttu-id="cbf24-4423">Inicializar una lista de identificadores de capítulos para cada cursor de esta consulta en DB \_ NULL \_ HCHAPTER</span><span class="sxs-lookup"><span data-stu-id="cbf24-4423">Initialize list of chapter handles for every cursor in this query to DB\_NULL\_HCHAPTER</span></span>
-   <span data-ttu-id="cbf24-4424">Inicialice la lista de identificadores de marcador para cada cursor de esta consulta en un conjunto de DBBMK \_ FIRST y DBBMK \_ LAST.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4424">Initialize list of bookmark handles for every cursor in this query to a set of DBBMK\_FIRST and DBBMK\_LAST.</span></span>
-   <span data-ttu-id="cbf24-4425">Marque la consulta como no supervisada para los cambios.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4425">Mark the query as not monitored for changes.</span></span>
-   <span data-ttu-id="cbf24-4426">Inicialice el número de filas en el número calculado actualmente de filas (que puede ser 0 si la consulta no comenzó a ejecutarse o algún número si la consulta está en un proceso de ejecución) e inicialice el numerador y el denominador de finalización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4426">Initialize the number of rows to the currently calculated number of rows (which can be 0 if query did not start to execute or some number if query is in a process of execution), and initialize the numerator and denominator of query completion.</span></span>
-   <span data-ttu-id="cbf24-4427">Responda al cliente con un mensaje CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4427">Respond to the client with a CPMCreateQueryOut message.</span></span>

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a><span data-ttu-id="cbf24-4428">3.1.5.2.3 Recepción de una solicitud CPMGetQueryStatusIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4428">3.1.5.2.3 Receiving a CPMGetQueryStatusIn Request</span></span>

<span data-ttu-id="cbf24-4429">Cuando el servidor recibe una solicitud de mensaje CPMGetQueryStatusIn de un cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4429">When the server receives a CPMGetQueryStatusIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4430">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4430">Check if the client has query associated with it.</span></span> <span data-ttu-id="cbf24-4431">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4431">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cbf24-4432">Compruebe si el identificador del cursor está en una lista de identificadores de cursor del cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4432">Check if the cursor handle is in a list of client's cursor handles.</span></span> <span data-ttu-id="cbf24-4433">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4433">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cbf24-4434">Prepare un mensaje CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4434">Prepare a CPMGetQueryStatusOut message.</span></span> <span data-ttu-id="cbf24-4435">El servidor DEBE recuperar el estado de consulta actual y establecerlo en el \_ campo QStatus (vea 2.2.3.11 para ver los valores posibles).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4435">The server MUST retrieve the current query status and set it in the \_QStatus field (see 2.2.3.11 for possible values).</span></span> <span data-ttu-id="cbf24-4436">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar un error.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4436">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="cbf24-4437">Responda al cliente con el mensaje CPMGetQueryStatusOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4437">Respond to the client with the CPMGetQueryStatusOut message.</span></span>

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a><span data-ttu-id="cbf24-4438">3.1.5.2.4 Recepción de una solicitud CPMGetQueryStatusExIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4438">3.1.5.2.4 Receiving a CPMGetQueryStatusExIn Request</span></span>

<span data-ttu-id="cbf24-4439">Cuando el servidor recibe una solicitud de mensaje CPMGetQueryStatusExIn de un cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4439">When the server receives a CPMGetQueryStatusExIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4440">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4440">Check if the client has a query associated with it.</span></span> <span data-ttu-id="cbf24-4441">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4441">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cbf24-4442">Compruebe si el identificador de cursor pasado está en una lista de identificadores de cursor del cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4442">Check if the cursor handle passed is in a list of client's cursor handles.</span></span> <span data-ttu-id="cbf24-4443">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4443">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cbf24-4444">Prepare un mensaje CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4444">Prepare a CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="cbf24-4445">El servidor DEBE recuperar el estado de consulta actual y el progreso de la consulta y establecer QStatus (vea 2.2.3.11 para ver los valores posibles), \_ dwRatioFinishedDenominator y \_ dwRatioFinishedNumerator, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4445">The server MUST retrieve the current query status and query progress and set QStatus (see 2.2.3.11 for possible values), \_dwRatioFinishedDenominator and \_dwRatioFinishedNumerator respectively.</span></span> <span data-ttu-id="cbf24-4446">A continuación, DEBE establecer el número de filas de los resultados de la consulta \_ en cRowsTotal.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4446">It MUST then set the number of rows in the query results to \_cRowsTotal.</span></span> <span data-ttu-id="cbf24-4447">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar que se ha encontrado un error.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4447">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cbf24-4448">Recupere información sobre el catálogo del cliente y rellene \_ cFilteredDocuments y \_ cDocumentsToFilter.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4448">Retrieve information about client's catalog and fill in \_cFilteredDocuments and \_cDocumentsToFilter.</span></span> <span data-ttu-id="cbf24-4449">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar que se ha encontrado un error.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4449">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cbf24-4450">Recupere la posición del marcador indicado por el identificador en el campo bmk y rellene el campo iRowBmk restante en el mensaje \_ \_ CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4450">Retrieve the position of the bookmark indicated by the handle in the \_bmk field, and fill the remaining \_iRowBmk field in the CPMGetQueryStatusExOut message.</span></span> <span data-ttu-id="cbf24-4451">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar que se ha encontrado un error.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4451">If this step fails for any reason server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cbf24-4452">Responda al cliente con el mensaje CPMGetQueryStatusExOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4452">Respond to the client with the CPMGetQueryStatusExOut message.</span></span>

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a><span data-ttu-id="cbf24-4453">3.1.5.2.5 Recepción de una solicitud CPMRatioFinishedIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4453">3.1.5.2.5 Receiving a CPMRatioFinishedIn Request</span></span>

<span data-ttu-id="cbf24-4454">Cuando el servidor recibe una solicitud de mensaje CPMRatioFinishedIn de un cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4454">When the server receives a CPMRatioFinishedIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4455">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4455">Check if the client has query associated with it.</span></span> <span data-ttu-id="cbf24-4456">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4456">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cbf24-4457">Compruebe si el identificador de cursor pasado está en la lista de identificadores de cursor del cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4457">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="cbf24-4458">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4458">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cbf24-4459">Prepare un mensaje CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4459">Prepare a CPMRatioFinishedOut message.</span></span> <span data-ttu-id="cbf24-4460">El servidor DEBE recuperar el estado de consulta del cliente y rellenar los campos \_ ulNumerator, \_ ulDenominator \_ y cRows.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4460">The server MUST retrieve the client's query status and fill in \_ulNumerator, \_ulDenominator and \_cRows fields.</span></span> <span data-ttu-id="cbf24-4461">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar que se ha encontrado un error.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4461">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cbf24-4462">Si cRows es igual al último número notificado de filas para esta consulta, establezca \_ \_ fNewRows en 0x00000000; de lo contrario, estafórelo en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4462">If \_cRows is equal to the last reported number of rows for this query, then set \_fNewRows to 0x00000000, otherwise set it to 0x00000001.</span></span>
-   <span data-ttu-id="cbf24-4463">Actualice el último número notificado de filas de esta consulta al valor \_ de cRows.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4463">Update the last reported number of rows for this query to the value of \_cRows.</span></span>
-   <span data-ttu-id="cbf24-4464">Responda al cliente con el mensaje CPMRatioFinishedOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4464">Respond to the client with the CPMRatioFinishedOut message.</span></span>

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a><span data-ttu-id="cbf24-4465">3.1.5.2.6 Recepción de una solicitud CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4465">3.1.5.2.6 Receiving a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="cbf24-4466">Cuando el servidor recibe una solicitud de mensaje CPMSetBindingsIn de un cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4466">When the server receives a CPMSetBindingsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4467">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4467">Check if the client has a query associated with it.</span></span> <span data-ttu-id="cbf24-4468">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4468">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cbf24-4469">Compruebe si el identificador de cursor pasado está en la lista de identificadores de cursor del cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4469">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="cbf24-4470">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4470">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cbf24-4471">Compruebe que la información de enlaces es válida (es decir, la columna especifica al menos el valor, la longitud o el estado que se va a devolver; no se superpone en los enlaces para el valor, la longitud o el estado; y el valor, la longitud y el estado se ajustan al tamaño de fila especificado) y, si no se informa de un \_ error BADBINDINFO (0x80040E08) de base de \_ datos.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4471">Verify that bindings information is valid (i.e., column at least specifies value, length or status to be returned; no overlap in bindings for value, length or status; and value, length and status fit in the row size specified) and if not report a DB\_E\_BADBINDINFO (0x80040E08) error.</span></span>
-   <span data-ttu-id="cbf24-4472">Guarde la información de enlace asociada a las columnas especificadas en el campo aColumns.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4472">Save the binding information associated with the columns specified in the aColumns field.</span></span> <span data-ttu-id="cbf24-4473">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar que se ha encontrado un error.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4473">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cbf24-4474">Responda al cliente con un encabezado de mensaje (solo) con msg establecido en CPMSetBindingsIn y el estado establecido en los resultados \_ \_ del enlace especificado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4474">Respond to the client with a message header (only) with \_msg set to CPMSetBindingsIn, and \_status set to the results of the specified binding.</span></span>

### <a name="31527-receiving-a-cpmgetrowsin-request"></a><span data-ttu-id="cbf24-4475">3.1.5.2.7 Recepción de una solicitud CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4475">3.1.5.2.7 Receiving a CPMGetRowsIn Request</span></span>

<span data-ttu-id="cbf24-4476">Cuando el servidor recibe una solicitud de mensaje CPMGetRowsIn de un cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4476">When the server receives a CPMGetRowsIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4477">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4477">Check if the client has query associated with it.</span></span> <span data-ttu-id="cbf24-4478">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4478">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cbf24-4479">Compruebe si el identificador de cursor pasado está en la lista de identificadores de cursor del cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4479">Check if the cursor handle passed is in athelist of the client's cursor handles.</span></span> <span data-ttu-id="cbf24-4480">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4480">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cbf24-4481">Compruebe si el cliente tiene un conjunto actual de enlaces.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4481">Check if the client has a current set of bindings.</span></span> <span data-ttu-id="cbf24-4482">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4482">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cbf24-4483">Prepare un mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4483">Prepare a CPMGetRowsOut message.</span></span> <span data-ttu-id="cbf24-4484">El servidor DEBE colocar el cursor en los resultados de la consulta como se indica en la descripción de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4484">The server MUST position the cursor in query results as indicated by the seek description.</span></span> <span data-ttu-id="cbf24-4485">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar que se ha encontrado un error.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4485">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cbf24-4486">Capture tantas filas como quepa en un búfer, cuyo tamaño se indica mediante cbReadBuffer, pero no más de lo indicado \_ por \_ cRowsToTransfer.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4486">Fetch as many rows as fits in a buffer, the size of which is indicated by \_cbReadBuffer, but not more than indicated by \_cRowsToTransfer.</span></span> <span data-ttu-id="cbf24-4487">Al capturar filas, el servidor DEBE comparar el tipo de valor de propiedad de cada columna seleccionada con el tipo especificado en el conjunto actual de enlaces del cliente (sección 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4487">When fetching rows, the server MUST compare each selected column's property value type to the type specified in the Client's current set of bindings (section 3.1.1).</span></span> <span data-ttu-id="cbf24-4488">Si el tipo del enlace no es VT VARIANT, el servidor DEBE intentar convertir el valor de propiedad de la columna \_ en ese tipo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4488">If the type in the binding is not VT\_VARIANT, the server MUST attempt to convert the column's property value to that type.</span></span> <span data-ttu-id="cbf24-4489">De lo contrario, si la marca DBPROP USEEXTENDEDDBTYPES está establecida en el conjunto de propiedades \_ DBPROPSET QUERYEXT del cliente, o si el valor de propiedad de la columna no es un tipo VT VECTOR, el valor de propiedad DEBE devolverse en su \_ \_ tipo normal.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4489">Otherwise, if the DBPROP\_USEEXTENDEDDBTYPES flag is set in the client's DBPROPSET\_QUERYEXT property set, or if the column's property value is not a VT\_VECTOR type, then the property value MUST be returned in its normal type.</span></span> <span data-ttu-id="cbf24-4490">Si ninguno de estos casos es el caso (es decir, el servidor tiene un tipo VT VECTOR y el cliente no admite VT VECTOR), el servidor DEBE intentar convertirlo a un tipo VT ARRAY como se muestra a continuación: los elementos de la matriz VT \_ \_ \_ \_ I8, VT \_ UI8, VT FILETIME y \_ VT \_ CLSID no se pueden convertir y, en su lugar, producir un error; Los elementos de la matriz VT LPSTR y VT LPWSTR DEBEN convertirse en \_ VT BSTR; los elementos de matriz de todos los demás tipos \_ DEBEN permanecer sin \_ cambios.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4490">If none of these are the case (i.e., the server has a VT\_VECTOR type, and the client does not support VT\_VECTOR), then the server MUST attempt to convert it to a VT\_ARRAY type as follows: VT\_I8, VT\_UI8, VT\_FILETIME, and VT\_CLSID array elements cannot be converted and instead fail; VT\_LPSTR and VT\_LPWSTR array elements MUST be converted to VT\_BSTR; array elements of all other types MUST remain unchanged.</span></span> <span data-ttu-id="cbf24-4491">Por último, si las columnas de fila contienen identificadores de capítulo o identificadores de marcador, el servidor DEBE actualizar las listas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4491">Finally, if row columns contain chapter handles or bookmark handles, the server MUST update the corresponding lists.</span></span> <span data-ttu-id="cbf24-4492">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar que se ha encontrado un error.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4492">If this step fails for any reason, the server MUST report that an error was encountered.</span></span>
-   <span data-ttu-id="cbf24-4493">Almacene el número real de filas capturadas en \_ cRowsReturned.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4493">Store the actual number of rows fetched in \_cRowsReturned.</span></span>
-   <span data-ttu-id="cbf24-4494">Copie la descripción de la búsqueda y el campo de capítulo de CPMGetRowsIn en un mensaje CPMGetRowsOut que se va a enviar.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4494">Copy the seek description and chapter field from CPMGetRowsIn to a CPMGetRowsOut message to be sent.</span></span>
-   <span data-ttu-id="cbf24-4495">Almacene las filas capturadas en el campo Filas (vea la nota sobre el byte de estado siguiente y la sección 2.2.3.16 en la estructura del campo Filas).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4495">Store fetched rows in the Rows field (see note on status byte below and section 2.2.3.16 on the structure of the Rows field).</span></span>
-   <span data-ttu-id="cbf24-4496">Responda al cliente con el mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4496">Respond to the client with the CPMGetRowsOut message.</span></span>

<span data-ttu-id="cbf24-4497">Nota sobre el campo de bytes de estado:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4497">Note on status byte field:</span></span>

<span data-ttu-id="cbf24-4498">Si StatusUsed está establecido en 0x01 en la CTableColumn del mensaje CPMSetBindingIn de la columna, el servidor DEBE establecer el byte de estado (que se encuentra en StatusOffset desde el principio de la fila) para esta columna en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4498">If StatusUsed is set to 0x01 in the CTableColumn of the CPMSetBindingIn message for the column, then the server MUST set the status byte (which is located at StatusOffset from the start of the row) for this column to one of the following values:</span></span>



| <span data-ttu-id="cbf24-4499">Valor</span><span class="sxs-lookup"><span data-stu-id="cbf24-4499">Value</span></span> | <span data-ttu-id="cbf24-4500">Significado</span><span class="sxs-lookup"><span data-stu-id="cbf24-4500">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="cbf24-4501">0x00</span><span class="sxs-lookup"><span data-stu-id="cbf24-4501">0x00</span></span>  | <span data-ttu-id="cbf24-4502">StatusOK</span><span class="sxs-lookup"><span data-stu-id="cbf24-4502">StatusOK</span></span>       |
| <span data-ttu-id="cbf24-4503">0x01</span><span class="sxs-lookup"><span data-stu-id="cbf24-4503">0x01</span></span>  | <span data-ttu-id="cbf24-4504">StatusDeferred</span><span class="sxs-lookup"><span data-stu-id="cbf24-4504">StatusDeferred</span></span> |
| <span data-ttu-id="cbf24-4505">0x02</span><span class="sxs-lookup"><span data-stu-id="cbf24-4505">0x02</span></span>  | <span data-ttu-id="cbf24-4506">StatusNull</span><span class="sxs-lookup"><span data-stu-id="cbf24-4506">StatusNull</span></span>     |



 

<span data-ttu-id="cbf24-4507">Si el valor de propiedad no está presente para esta fila, el servidor DEBE establecer el byte de estado en StatusNull.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4507">If the property value is absent for this row, the server MUST set the status byte to StatusNull.</span></span> <span data-ttu-id="cbf24-4508">Si el valor es demasiado grande para transferirse en el mensaje CPMGetRowsOut, el servidor DEBE establecer el byte de estado en StatusDeferred.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4508">If the value is too big to be transferred in the CPMGetRowsOut message, the server MUST set the status byte to StatusDeferred.</span></span> <span data-ttu-id="cbf24-4509">De lo contrario, el servidor DEBE establecer el byte de estado en StatusOK.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4509">Otherwise the server MUST set the status byte to StatusOK.</span></span>

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a><span data-ttu-id="cbf24-4510">3.1.5.2.8 Recepción de una solicitud CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4510">3.1.5.2.8 Receiving a CPMFetchValueIn Request</span></span>

<span data-ttu-id="cbf24-4511">Cuando el servidor recibe una solicitud de mensaje CPMFetchValueIn de un cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4511">When the server receives a CPMFetchValueIn message request from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4512">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4512">Check if the client has query associated with it.</span></span> <span data-ttu-id="cbf24-4513">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4513">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cbf24-4514">Prepare un mensaje CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4514">Prepare a CPMFetchValueOut message.</span></span> <span data-ttu-id="cbf24-4515">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar un error.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4515">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="cbf24-4516">Busque el documento indicado por el campo wid y compruebe si el identificador de propiedad de este documento (más adelante denominado "valor de propiedad") indicado por la estructura PropSpec está disponible para este \_ cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4516">Find the document indicated by the\_wid field and check if the property ID for this document (later referred to as 'property value') indicated by the PropSpec structure is available for this client.</span></span> <span data-ttu-id="cbf24-4517">Si este valor no está disponible, el servidor DEBE establecer fValueExists en 0x00000000 y, de lo \_ contrario, \_ establecer fValueExists en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4517">If this value is not available the server MUST set \_fValueExists to 0x00000000, and otherwise set \_fValueExists to 0x00000001.</span></span> <span data-ttu-id="cbf24-4518">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar un error.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4518">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="cbf24-4519">Si \_ fValueExists es igual a 0x00000001 el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4519">If \_fValueExists is equal to 0x00000001 the server MUST do the following:</span></span>
-   -   <span data-ttu-id="cbf24-4520">Serialice el valor de propiedad en una estructura SERIALIZEDPROPERTYVALUE y copie, a partir del desplazamiento \_ cbSoFar, como máximo los bytes cbChunk (pero no más allá del final de la propiedad serializada) en el \_ campo vValue.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4520">Serialize the property value to a SERIALIZEDPROPERTYVALUE structure and copy, starting from the \_cbSoFar offset, at most \_cbChunk bytes (but not past the end of the serialized property) to vValue field.</span></span> <span data-ttu-id="cbf24-4521">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar un error.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4521">If this step fails for any reason server MUST report an error.</span></span>
    -   <span data-ttu-id="cbf24-4522">Establezca \_ cbValue en el número de bytes copiados en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4522">Set \_cbValue to the number of bytes copied in previous step.</span></span>
    -   <span data-ttu-id="cbf24-4523">Establezca vType en el tipo de propiedad del valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4523">Set vType to the property type of the property value.</span></span>
    -   <span data-ttu-id="cbf24-4524">Si la longitud de la propiedad serializada es mayor que cbSoFar agregada a \_ \_ cbValue, establezca fMoreExists en 0x00000001; de lo contrario, estafrála \_ en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4524">If the length of serialized property is greater than \_cbSoFar added to \_cbValue, then set \_fMoreExists to 0x00000001, otherwise set it to 0x00000000.</span></span>

-   <span data-ttu-id="cbf24-4525">Respuesta al cliente con el mensaje CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-4525">Respond to the client with the CPMFetchValueOut message</span></span>

### <a name="31529-receiving-a-cpmgetnotify-request"></a><span data-ttu-id="cbf24-4526">3.1.5.2.9 Recibir una solicitud CPMGetNotify</span><span class="sxs-lookup"><span data-stu-id="cbf24-4526">3.1.5.2.9 Receiving a CPMGetNotify Request</span></span>

<span data-ttu-id="cbf24-4527">Cuando el servidor recibe un mensaje CPMGetNotify de un cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4527">When the server receives a CPMGetNotify message from a client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4528">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4528">Check if the client has query associated with it.</span></span> <span data-ttu-id="cbf24-4529">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4529">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cbf24-4530">Si no se ha realizado ningún cambio en el conjunto de resultados de la consulta desde el último mensaje CPMSendNotifyOut para este cliente, o si la consulta no está supervisada actualmente para los cambios en el conjunto de resultados, el servidor DEBE responder con el mensaje CPMGetNotify y empezar a supervisar la consulta en busca de cambios en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4530">If there were no changes in the query result set since the last CPMSendNotifyOut message for this client, or if the query is not currently monitored for changes in the results set, then the server MUST respond with CPMGetNotify message and start to monitor the query for changes in results set.</span></span> <span data-ttu-id="cbf24-4531">Si más adelante se produce un cambio en el conjunto de resultados de la consulta, el servidor DEBE enviar exactamente un mensaje CPMSendNotifyOut al cliente y DEBE especificar el cambio en el \_ campo watchNotify.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4531">If at a later time there is a change in the query results set then the server MUST send exactly one CPMSendNotifyOut message to the client and MUST specify the change in the \_watchNotify field.</span></span>
-   <span data-ttu-id="cbf24-4532">Si se han realizado cambios en el conjunto de resultados de la consulta desde el último mensaje CPMSendNotifyOut, el servidor DEBE responder con CPMSendNotifyOut y DEBE especificar el cambio en el \_ campo watchNotify.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4532">If there were changes to the query result set since the last CPMSendNotifyOut message, the server MUST reply with CPMSendNotifyOut and MUST specify the change in the \_watchNotify field.</span></span> <span data-ttu-id="cbf24-4533">Tenga en cuenta que, en el caso de muchos cambios en los resultados de la consulta, DBWATCHNOTIFY ROWSCHANGED tiene prioridad (es decir, si la consulta se ha realizado, se vuelve a ejecutar y, a continuación, el número de filas cambia y la consulta se ha realizado de nuevo, el evento notificado sería \_ DBWATCHNOTIFY \_ ROWSCHANGED).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4533">Note, that in the case of many changes to query results, DBWATCHNOTIFY\_ROWSCHANGED takes priority (i.e., if the query was done, re-executed and then the number of rows changed and the query was done again then the event reported would be DBWATCHNOTIFY\_ROWSCHANGED).</span></span>

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a><span data-ttu-id="cbf24-4534">3.1.5.2.10 Recepción de una solicitud CPMGetApproximatePositionIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4534">3.1.5.2.10 Receiving a CPMGetApproximatePositionIn Request</span></span>

<span data-ttu-id="cbf24-4535">Cuando el servidor recibe una solicitud de mensaje CPMGetApproximatePositionIn del cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4535">When the server receives a CPMGetApproximatePositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4536">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4536">Check if the client has a query associated with it.</span></span> <span data-ttu-id="cbf24-4537">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4537">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cbf24-4538">Compruebe si el identificador del cursor, el identificador de capítulo y el identificador de marcador pasados están en las listas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4538">Check if the cursor handle, chapter handle and bookmark handle passed are in corresponding lists.</span></span> <span data-ttu-id="cbf24-4539">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4539">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cbf24-4540">Busque una fila asociada al identificador de marcador en los resultados de la consulta y aproxime la posición de la fila en el conjunto de filas, a la que hace referencia el identificador de capítulo, y determine el numerador y el denominador de la posición.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4540">Find a row which is associated with the bookmark handle in the query results and approximate the position of the row in the rowset, referred to by the chapter handle, and determine the numerator and denominator for the position.</span></span> <span data-ttu-id="cbf24-4541">Tenga en cuenta que cuando el identificador del capítulo es DB \_ NULL HCHAPTER, el capítulo correspondiente es el conjunto de filas \_ principal de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4541">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="cbf24-4542">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar un error.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4542">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="cbf24-4543">Responda al cliente con un mensaje CPMFetchValueOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4543">Respond to the client with a CPMFetchValueOut message.</span></span>

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a><span data-ttu-id="cbf24-4544">3.1.5.2.11 Recibir una solicitud CPMCompareBmkIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4544">3.1.5.2.11 Receiving a CPMCompareBmkIn Request</span></span>

<span data-ttu-id="cbf24-4545">Cuando el servidor recibe una solicitud de mensaje CPMCompareBmkIn del cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4545">When the server receives a CPMCompareBmkIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4546">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4546">Check if the client has a query associated with it.</span></span> <span data-ttu-id="cbf24-4547">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4547">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cbf24-4548">Compruebe si el identificador del cursor, el identificador de capítulo y los identificadores de marcador pasados están en las listas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4548">Check if the cursor handle, chapter handle and bookmark handles passed are in corresponding lists.</span></span> <span data-ttu-id="cbf24-4549">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4549">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cbf24-4550">Prepare un mensaje CPMCompareBmkOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4550">Prepare a CPMCompareBmkOut message.</span></span>
-   <span data-ttu-id="cbf24-4551">Si los identificadores de marcador son iguales, \_ dwComparison DEBE estar establecido en DBCOMPARE \_ EQ.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4551">If bookmark handles are equal, then \_dwComparison MUST be is set to DBCOMPARE\_EQ.</span></span>
-   <span data-ttu-id="cbf24-4552">De lo contrario, si uno de los identificadores de marcador es DBBMK FIRST o \_ DBBMK \_ LAST, \_ dwComparison DEBE establecerse en DBCOMPARE \_ NE.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4552">Otherwise, if one of bookmarks handles is DBBMK\_FIRST or DBBMK\_LAST then \_dwComparison MUST be set to DBCOMPARE\_NE.</span></span>
-   <span data-ttu-id="cbf24-4553">De lo contrario, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4553">Otherwise the server MUST do the following:</span></span>
-   -   <span data-ttu-id="cbf24-4554">Buscar filas a las que hace referencia cada identificador de marcador en los resultados de la consulta</span><span class="sxs-lookup"><span data-stu-id="cbf24-4554">Find rows which are referred to by each bookmark handle in the query results</span></span>
    -   <span data-ttu-id="cbf24-4555">Si alguna de las filas no está en el capítulo indicado por el identificador de capítulo en CPMCompareBmkIn, dwComparison DEBE establecerse en \_ DBCOMPARE \_ NOTCOMPARABLE.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4555">If any one of the rows is not in the chapter indicated by the chapter handle in CPMCompareBmkIn, then \_dwComparison MUST be set to DBCOMPARE\_NOTCOMPARABLE.</span></span>
    -   <span data-ttu-id="cbf24-4556">De lo contrario, cuando ambas filas están en el mismo capítulo, el servidor DEBE aproximarse a una posición de esas filas en el conjunto de filas al que hace referencia el identificador de este capítulo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4556">Otherwise, when both rows are in the same chapter, then the server MUST approximate a position of those rows in the rowset referred to by this chapter's handle.</span></span> <span data-ttu-id="cbf24-4557">A continuación, DEBE comparar los valores de posición y establecer dwComparison en DBCOMPARE LT si la posición de la primera fila es menor que la posición de la segunda fila; de lo contrario, dwComparison DEBE establecerse en \_ \_ \_ DBCOMPARE \_ GT.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4557">It MUST then compare position values and set\_dwComparison to DBCOMPARE\_LT if position of first row is smaller than position of the second row; otherwise \_dwComparison MUST be set to DBCOMPARE\_GT.</span></span>

-   <span data-ttu-id="cbf24-4558">Responda al cliente con el mensaje CPMCompareBmkOut rellenado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4558">Respond to the client with filled CPMCompareBmkOut message.</span></span>

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a><span data-ttu-id="cbf24-4559">3.1.5.2.12 Recepción de una solicitud CPMRestartPositionIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4559">3.1.5.2.12 Receiving a CPMRestartPositionIn Request</span></span>

<span data-ttu-id="cbf24-4560">Cuando el servidor recibe la solicitud de mensaje CPMRestartPositionIn del cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4560">When the server receives the CPMRestartPositionIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4561">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4561">Check if the client has a query associated with it.</span></span> <span data-ttu-id="cbf24-4562">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4562">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cbf24-4563">Compruebe si el identificador de cursor y el identificador de capítulo pasados están en las listas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4563">Check if the cursor handle and chapter handle passed are in corresponding lists.</span></span> <span data-ttu-id="cbf24-4564">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4564">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cbf24-4565">Mueva el cursor al principio del capítulo, identificado por el identificador del capítulo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4565">Move the cursor to the beginning of the chapter, identified by the chapter handle.</span></span> <span data-ttu-id="cbf24-4566">Tenga en cuenta que cuando el identificador del capítulo es DB \_ NULL HCHAPTER, el capítulo correspondiente es el conjunto de filas \_ principal de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4566">Note that when the chapter handle is DB\_NULL\_HCHAPTER, the corresponding chapter is the main rowset of the query.</span></span> <span data-ttu-id="cbf24-4567">Si se produce un error en este paso por cualquier motivo, el servidor DEBE notificar un error.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4567">If this step fails for any reason, the server MUST report an error.</span></span>
-   <span data-ttu-id="cbf24-4568">Responda al cliente con un mensaje CPMRestartPositionIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4568">Respond to the client with a CPMRestartPositionIn message.</span></span>

### <a name="315213-receiving-a-cpmfreecursorin-request"></a><span data-ttu-id="cbf24-4569">3.1.5.2.13 Recepción de una solicitud CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4569">3.1.5.2.13 Receiving a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="cbf24-4570">Cuando el servidor recibe una solicitud de mensaje CPMFreeCursorIn del cliente, el servidor DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4570">When the server receives a CPMFreeCursorIn message request from the client, the server MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4571">Compruebe si el cliente tiene una consulta asociada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4571">Check if the client has a query associated with it.</span></span> <span data-ttu-id="cbf24-4572">Si este no es el caso, el servidor DEBE notificar un error STATUS \_ INVALID \_ PARAMETER (0xC000000D).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4572">If this is not the case, the server MUST report a STATUS\_INVALID\_PARAMETER (0xC000000D) error.</span></span>
-   <span data-ttu-id="cbf24-4573">Compruebe si el identificador de cursor pasado está en la lista de identificadores de cursor del cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4573">Check if the cursor handle passed is in the list of the client's cursor handles.</span></span> <span data-ttu-id="cbf24-4574">Si este no es el caso, el servidor DEBE notificar un error E \_ FAIL (0x80004005).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4574">If this is not the case, the server MUST report an E\_FAIL (0x80004005) error.</span></span>
-   <span data-ttu-id="cbf24-4575">Libere el cursor y los recursos asociados (consulte la sección 3.1.1 para obtener una lista completa) para este identificador de cursor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4575">Release the cursor and associated resources (see section 3.1.1 for complete list) for this cursor handle.</span></span>
-   <span data-ttu-id="cbf24-4576">Quite el cursor de la lista de cursores para ese cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4576">Remove the cursor from the list of cursors for that client.</span></span>
-   <span data-ttu-id="cbf24-4577">Responda con un mensaje CPMFreeCursorOut, estableciendo el campo \_ cCursorsRemaining con el número de cursores restantes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4577">Respond with a CPMFreeCursorOut message, setting the \_cCursorsRemaining field with the number of cursors remaining.</span></span> <span data-ttu-id="cbf24-4578">en la lista de este cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4578">in this client's list.</span></span>
-   <span data-ttu-id="cbf24-4579">Si no hay más cursores para este cliente, el servidor DEBE liberar la consulta y los recursos asociados (consulte la sección 3.1.1).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4579">If there are no more cursors for this client, the server MUST release the query and associated resources (see section 3.1.1).</span></span>

### <a name="315214-receiving-a-cpmdisconnect-request"></a><span data-ttu-id="cbf24-4580">3.1.5.2.14 Recepción de una solicitud CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="cbf24-4580">3.1.5.2.14 Receiving a CPMDisconnect Request</span></span>

<span data-ttu-id="cbf24-4581">Cuando el servidor recibe una solicitud de mensaje CPMDisconnect del cliente, el servidor DEBE quitar el cliente de la lista de clientes conectados y liberar todos los recursos asociados al cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4581">When the server receives a CPMDisconnect message request from the client, the server MUST remove the client from the list of connected clients and release all resources associated with the client.</span></span>

### <a name="316-timer-events"></a><span data-ttu-id="cbf24-4582">3.1.6 Eventos de temporizador</span><span class="sxs-lookup"><span data-stu-id="cbf24-4582">3.1.6 Timer Events</span></span>

<span data-ttu-id="cbf24-4583">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4583">None.</span></span>

### <a name="317-other-local-events"></a><span data-ttu-id="cbf24-4584">3.1.7 Otros eventos locales</span><span class="sxs-lookup"><span data-stu-id="cbf24-4584">3.1.7 Other Local Events</span></span>

<span data-ttu-id="cbf24-4585">Cuando se detiene el servidor, debe pasar primero al estado de "apagado".</span><span class="sxs-lookup"><span data-stu-id="cbf24-4585">When the server is stopped, it MUST first transition to the "shutting down" state.</span></span> <span data-ttu-id="cbf24-4586">A continuación, DEBE dejar de escuchar la canalización, realizar cualquier otra tarea de apagado específica de la implementación y, a continuación, realizar la transición al estado "detenido".</span><span class="sxs-lookup"><span data-stu-id="cbf24-4586">It MUST then stop listening to the pipe, perform any other implementation-specific shutdown tasks, and then transition into the "stopped" state.</span></span>

### <a name="32-client-details"></a><span data-ttu-id="cbf24-4587">3.2 Detalles del cliente</span><span class="sxs-lookup"><span data-stu-id="cbf24-4587">3.2 Client Details</span></span>

### <a name="321-abstract-data-model"></a><span data-ttu-id="cbf24-4588">3.2.1 Modelo de datos abstractos</span><span class="sxs-lookup"><span data-stu-id="cbf24-4588">3.2.1 Abstract Data Model</span></span>

<span data-ttu-id="cbf24-4589">En la sección siguiente se especifican los datos y el estado que mantiene el cliente del Protocolo de servicio de indexación de contenido.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4589">The following section specifies data and state maintained by the Content Indexing Service Protocol client.</span></span> <span data-ttu-id="cbf24-4590">Los datos proporcionados son para facilitar la explicación de cómo se comporta el protocolo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4590">The provided data is to facilitate the explanation of how the protocol behaves.</span></span> <span data-ttu-id="cbf24-4591">Esta sección no exige que las implementaciones cumplan este modelo siempre y cuando su comportamiento externo sea coherente con el descrito en este documento.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4591">This section does not mandate that implementations adhere to this model as long as their external behavior is consistent with that described in this document.</span></span>

<span data-ttu-id="cbf24-4592">Un cliente tiene el siguiente estado abstracto:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4592">A client has the following abstract state:</span></span>

-   <span data-ttu-id="cbf24-4593">**Último mensaje enviado:** copia del último mensaje enviado al servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4593">**Last Message Sent**: A copy of the last message sent to the server.</span></span>
-   <span data-ttu-id="cbf24-4594">**Valor de propiedad actual:** valor parcial de una propiedad "diferida", que está en proceso de recuperación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4594">**Current Property Value**: A partial value of a "deferred" property, which is in the process of being retrieved.</span></span>
-   <span data-ttu-id="cbf24-4595">**Bytes actuales recibidos:** el número de bytes recibidos para el valor de propiedad actual hasta ahora.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4595">**Current Bytes Received**: The number of bytes received for Current Property Value so far.</span></span>
-   <span data-ttu-id="cbf24-4596">**Estado de conexión de canalización con nombre:** una conexión al servidor</span><span class="sxs-lookup"><span data-stu-id="cbf24-4596">**Named pipe connection state**: A connection to the server</span></span>

### <a name="322-timers"></a><span data-ttu-id="cbf24-4597">3.2.2 Temporizadores</span><span class="sxs-lookup"><span data-stu-id="cbf24-4597">3.2.2 Timers</span></span>

<span data-ttu-id="cbf24-4598">No se requiere ningún temporizador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4598">No protocol timers are required.</span></span>

### <a name="323-initialization"></a><span data-ttu-id="cbf24-4599">3.2.3 Inicialización</span><span class="sxs-lookup"><span data-stu-id="cbf24-4599">3.2.3 Initialization</span></span>

<span data-ttu-id="cbf24-4600">No se realizarán acciones hasta que se reciba una solicitud de capa superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4600">No actions are taken until a higher layer request is received.</span></span>

### <a name="324-higher-layer-triggered-events"></a><span data-ttu-id="cbf24-4601">3.2.4 Eventos Higher-Layer desencadenados</span><span class="sxs-lookup"><span data-stu-id="cbf24-4601">3.2.4 Higher-Layer Triggered Events</span></span>

<span data-ttu-id="cbf24-4602">Cuando se recibe una solicitud de una capa superior, el cliente DEBE crear una conexión de canalización con nombre al servidor, utilizando los detalles especificados en la sección 2.1.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4602">When a request is received from a higher layer, the client MUST create a named pipe connection to the server, using the details specified in Section 2.1.</span></span> <span data-ttu-id="cbf24-4603">Si no puede hacerlo, se DEBE dar error a la solicitud de capa superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4603">If it is unable to do so, the higher layer request MUST be failed.</span></span> <span data-ttu-id="cbf24-4604">Es decir, en caso de que no se pueda conectar, es responsabilidad del nivel superior reintentar si lo desea.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4604">That is, in case of a failure to connect, it is the responsibility of the higher level to retry if desired.</span></span>

<span data-ttu-id="cbf24-4605">Un encabezado DEBE incluirse previamente con campos establecidos como se especifica en la sección 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4605">A header MUST be pre-pended with fields set as specified in section 2.2.2.</span></span>

<span data-ttu-id="cbf24-4606">Para los mensajes que se especifican como que requieren una suma de comprobación distinta de cero, el \_ valor ulChecksum DEBE calcularse de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4606">For messages that are specified as requiring a nonzero checksum, the \_ulChecksum value MUST be calculated as follows:</span></span>

1.  <span data-ttu-id="cbf24-4607">El contenido del mensaje después del campo ulReserved2 en el encabezado del mensaje DEBE interpretarse como una secuencia de enteros de \_ 32 bits.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4607">The contents of the message after the \_ulReserved2 field in the message header MUST be interpreted as a sequence of 32 bit integers.</span></span> <span data-ttu-id="cbf24-4608">El cliente DEBE calcular la suma de los valores numéricos especificados por estos enteros.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4608">The client MUST calculate the sum of the numeric values given by these integers.</span></span>
2.  <span data-ttu-id="cbf24-4609">Calcule el XOR bit a bit de este valor con 0x59533959.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4609">Calculate the bitwise XOR of this value with 0x59533959.</span></span>
3.  <span data-ttu-id="cbf24-4610">Resta el valor especificado por \_ msg del valor que resulta del XOR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4610">Subtract the value given by \_msg from the value that results from the bitwise XOR.</span></span>

### <a name="3241-remote-indexing-service-catalog-management"></a><span data-ttu-id="cbf24-4611">3.2.4.1 Remote Indexing Service Catalog Management</span><span class="sxs-lookup"><span data-stu-id="cbf24-4611">3.2.4.1 Remote Indexing Service Catalog Management</span></span>

<span data-ttu-id="cbf24-4612">Cada mensaje se desencadena mediante una solicitud de la capa superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4612">Each message is triggered by a request from the higher layer.</span></span> <span data-ttu-id="cbf24-4613">El cliente no aplica ninguna secuencia de mensajes para las solicitudes de mensajes CISP para administrar catálogos de forma remota, pero (a excepción de un mensaje CPMSetCatStateIn), el servidor solo responderá correctamente si el cliente se conectó previamente por medio de un mensaje CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4613">There is no message sequence enforced by the client for CISP message requests for remotely managing catalogs, but (with the exception of a CPMSetCatStateIn message) the server will only reply with success if the client previously connected by means of a CPMConnectIn message.</span></span>

### <a name="32411-sending-a-cpmcistateinout-request"></a><span data-ttu-id="cbf24-4614">3.2.4.1.1 Envío de una solicitud CPMCiStateInOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-4614">3.2.4.1.1 Sending a CPMCiStateInOut Request</span></span>

<span data-ttu-id="cbf24-4615">Normalmente, la capa superior solicita al cliente de protocolo que envíe un mensaje CPMCiStateInOut cuando requiera información sobre la indexación de servicios en el servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4615">Typically, the higher layer asks the protocol client to send a CPMCiStateInOut message when it requires information about indexing services on the server.</span></span>

<span data-ttu-id="cbf24-4616">Cuando se le solicite que envíe este mensaje, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4616">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4617">Envíe un mensaje CPMCiStateInOut como se especifica en la sección 2.2.3.1 al servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4617">Send a CPMCiStateInOut message as specified in section 2.2.3.1 to the server.</span></span>
-   <span data-ttu-id="cbf24-4618">Espere a recibir el mensaje CPMCiStateInOut del servidor, descartando silenciosamente todos los demás mensajes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4618">Wait to receive CPMCiStateInOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="cbf24-4619">Informe del valor del campo de estado de la respuesta y, si se ha realizado correctamente, la estructura de información vuelve \_ a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4619">Report the value of the \_status field of the response and, if it was successful, the informational structure back to the higher layer.</span></span>

### <a name="32412-sending-a-cpmsetcatstatein-request"></a><span data-ttu-id="cbf24-4620">3.2.4.1.2 Envío de una solicitud CPMSetCatStateIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4620">3.2.4.1.2 Sending a CPMSetCatStateIn Request</span></span>

<span data-ttu-id="cbf24-4621">Normalmente, la capa superior solicita al cliente de protocolo que envíe un mensaje CPMSetCatStateIn cuando requiera información sobre un catálogo o todo el catálogo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4621">Typically, the higher layer asks the protocol client to send a CPMSetCatStateIn message when it requires information about a catalog or all catalog.</span></span> <span data-ttu-id="cbf24-4622">Para este mensaje, la capa superior debe proporcionar al cliente de protocolo un valor para dwNewState y, si es necesario, el \_ nombre del catálogo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4622">For this message the higher layer needs to provide the protocol client with a value for \_dwNewState and, if required, the name of the catalog.</span></span>

<span data-ttu-id="cbf24-4623">Cuando se le solicite que envíe este mensaje, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4623">When requested to send this message, the client MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4624">Envíe un mensaje CPMSetCatStateIn como se especifica en 2.2.3.2 al servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4624">Send a CPMSetCatStateIn message as specified in 2.2.3.2 to the server.</span></span>
-   <span data-ttu-id="cbf24-4625">Espere a recibir un mensaje CPMSetCatStateOut del servidor, descartando silenciosamente todos los demás mensajes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4625">Wait to receive a CPMSetCatStateOut message from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="cbf24-4626">Informe del valor del campo de estado de la respuesta y, si se ha realizado \_ correctamente, dwOldState de nuevo \_ a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4626">Report the value of the \_status field of the response and, if it was successful, the \_dwOldState back to the higher layer.</span></span>

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a><span data-ttu-id="cbf24-4627">3.2.4.1.3 Envío de una solicitud CPMUpdateDocumentsIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4627">3.2.4.1.3 Sending a CPMUpdateDocumentsIn Request</span></span>

<span data-ttu-id="cbf24-4628">La capa superior normalmente solicita que envíe este mensaje cuando necesite actualizar documentos en la ruta de acceso existente o agregar una nueva ruta de acceso de archivo al índice.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4628">The higher layer typically asks to send this message when it needs to either update documents in existing path or add a new file path to the index.</span></span> <span data-ttu-id="cbf24-4629">Por lo tanto, la capa superior es proporcionar la ruta de acceso y el tipo de un examen, que se especifica como en la sección 2.2.3.4, donde una actualización incremental o completa está pensada para las rutas de acceso existentes, y la inicialización nueva está pensada para nuevas rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4629">Thus the higher layer is to provide the path and type of a scan, which is specified as in section 2.2.3.4 where an incremental or full update is meant for existing paths, and new initialization is meant for new paths.</span></span>

<span data-ttu-id="cbf24-4630">Para atender la solicitud de capa superior, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4630">In order to serve the higher layer request, the client MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4631">Envíe un mensaje CPMUpdateDocumentsIn como se especifica en la sección 2.2.3.4 al servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4631">Send a CPMUpdateDocumentsIn message as specified in section 2.2.3.4 to the server.</span></span>
-   <span data-ttu-id="cbf24-4632">Espere a recibir el mensaje CPMUpdateDocumentsIn del servidor, descartando de forma silenciosa todos los demás mensajes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4632">Wait to receive CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="cbf24-4633">Informe el valor del campo \_ de estado de la respuesta a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4633">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="32414-sending-a-cpmforcemergein-request"></a><span data-ttu-id="cbf24-4634">3.2.4.1.4 Envío de una solicitud CPMForceMergeIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4634">3.2.4.1.4 Sending a CPMForceMergeIn Request</span></span>

<span data-ttu-id="cbf24-4635">Normalmente, la capa superior solicita enviar este mensaje cuando es necesario mejorar el rendimiento de las consultas o forma parte del mantenimiento programado del servicio de indexación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4635">Typically, the higher layer requests to send this message when there is a need to improve query performance, or it's a part of scheduled indexing service maintenance.</span></span>

<span data-ttu-id="cbf24-4636">Para atender la capa superior, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4636">In order to serve the higher layer the client MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4637">Envíe el mensaje CPMForceMergeIn tal como se especifica en la sección 2.2.3.5 al servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4637">Send CPMForceMergeIn message as specified by section 2.2.3.5 to the server.</span></span>
-   <span data-ttu-id="cbf24-4638">Espere a recibir un mensaje CPMUpdateDocumentsIn del servidor, descartando de forma silenciosa todos los demás mensajes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4638">Wait to receive a CPMUpdateDocumentsIn message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="cbf24-4639">Informe el valor del campo \_ de estado de la respuesta a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4639">Report the value of the \_status field of the response back to the higher layer.</span></span>

### <a name="3242-remote-indexing-service-catalog-query-messages"></a><span data-ttu-id="cbf24-4640">3.2.4.2 Mensajes de consulta del catálogo del servicio de indexación remota</span><span class="sxs-lookup"><span data-stu-id="cbf24-4640">3.2.4.2 Remote Indexing Service Catalog Query Messages</span></span>

<span data-ttu-id="cbf24-4641">A excepción de CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, hay una relación uno a uno entre los mensajes CISP y las solicitudes de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4641">With the exception of CPMGetRowsIn/CPMGetRowsOut, CPMFetchValueIn/CPMFetchValueOut, there is a one-to-one relationship between CISP messages and higher layer requests.</span></span> <span data-ttu-id="cbf24-4642">Para las dos excepciones mencionadas anteriormente, puede haber varios mensajes generados por el cliente para satisfacer los requisitos de tamaño o para recuperar una propiedad completa.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4642">For the two exceptions mentioned above, there can be multiple messages generated by the client to either satisfy size requirements, or to retrieve a complete property.</span></span> <span data-ttu-id="cbf24-4643">La capa superior suele realizar un seguimiento de toda la información específica de la consulta (como los identificadores de cursor abiertos, los valores legales para los identificadores de marcador y capítulo, los valores de wid para los valores de propiedad diferida, etc.) y también realiza un seguimiento de si el cliente está en un estado conectado, pero el cliente no lo aplica de ninguna manera.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4643">The higher layer typically keeps track of all query-specific information (such as cursor handles opened, legal values for bookmark and chapter handles, wid values for deferred property values, etc.) and also tracks if the client is in a connected state, but this is not enforced in any way by the client.</span></span>

<span data-ttu-id="cbf24-4644">Con fines ilustrativos, la parte del cliente del diagrama de la sección 3 ilustra esta secuencia para una consulta sencilla de Indexing Service.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4644">For illustrative purposes the client portion of the diagram in Section 3 illustrates this sequence for a simple Indexing Service query.</span></span>

### <a name="32421-sending-a-cpmconnectin-request"></a><span data-ttu-id="cbf24-4645">3.2.4.2.1 Envío de una solicitud CPMConnectIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4645">3.2.4.2.1 Sending a CPMConnectIn Request</span></span>

<span data-ttu-id="cbf24-4646">Este mensaje suele ser la primera solicitud de la capa superior (como si el cliente no está conectado, el servidor producirá un error en la mayoría de los mensajes con la excepción de CPMSetCatStateIn).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4646">This message is typically the very first request from the higher layer (as if the client is not connected, the server will fail most of the messages with exception of CPMSetCatStateIn).</span></span> <span data-ttu-id="cbf24-4647">El nivel superior proporciona al cliente de protocolo la información necesaria para conectarse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4647">The higher level provides the protocol client with information necessary to connect.</span></span>

<span data-ttu-id="cbf24-4648">Para atender la capa superior, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4648">In order to serve the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4649">Rellene el mensaje con la información proporcionada por el cliente de capa superior (consulte la sección 2.2.3.6) en \_ iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 y aPropertySet.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4649">Fill in the message, using information which the higher layer client provided (see section 2.2.3.6) in \_iClientVersion, MachineName, UserName, PropertySet1, PropertySet2 and aPropertySet.</span></span>
-   <span data-ttu-id="cbf24-4650">Establezca \_ fClientIsRemote, \_ cbBlob, \_ cbBlob2, cPropSet y cExtPropSet como se especifica en 2.2.3.6.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4650">Set \_fClientIsRemote, \_cbBlob, \_cbBlob2, cPropSet and cExtPropSet as specified in 2.2.3.6.</span></span>
-   <span data-ttu-id="cbf24-4651">Establezca la suma de comprobación en \_ el campo ulChecksum.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4651">Set the checksum in the \_ulChecksum field.</span></span>
-   <span data-ttu-id="cbf24-4652">Envíe el mensaje CPMConnectIn al servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4652">Send the CPMConnectIn message to the server.</span></span>
-   <span data-ttu-id="cbf24-4653">Espere a recibir un mensaje CPMConnectOut del servidor, descartando de forma silenciosa todos los demás mensajes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4653">Wait to receive a CPMConnectOut message back from the server, silently discarding all other messages.</span></span>
-   <span data-ttu-id="cbf24-4654">Informe del valor del campo de estado de la respuesta y, si se ha realizado correctamente, serverVersion de \_ nuevo a la capa \_ superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4654">Report the value of the \_status field of the response and, if it was successful, the \_serverVersion back to the higher layer.</span></span>

<span data-ttu-id="cbf24-4655">Para fines informativos, se espera que las capas superiores realicen normalmente las siguientes acciones tras una conexión correcta, pero el cliente CISP no las aplica:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4655">For informative purposes, it is expected that higher layers will typically do the following actions upon successful connection, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="cbf24-4656">Uso de mensajes de administración remota del catálogo de servicios de indexación para tareas administrativas</span><span class="sxs-lookup"><span data-stu-id="cbf24-4656">Use remote indexing service catalog management messages for administrative tasks</span></span>
-   <span data-ttu-id="cbf24-4657">Use una solicitud CPMCreateQueryIn para crear una consulta de búsqueda con el fin de recuperar los resultados del catálogo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4657">Use a CPMCreateQueryIn request to create a search query with a purpose of retrieving results from the catalog.</span></span>

### <a name="32422-sending-a-cpmcreatequeryin-request"></a><span data-ttu-id="cbf24-4658">3.2.4.2.2 Envío de una solicitud CPMCreateQueryIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4658">3.2.4.2.2 Sending a CPMCreateQueryIn Request</span></span>

<span data-ttu-id="cbf24-4659">La capa superior normalmente proporcionará información para la creación de consultas una vez conectado el cliente de protocolo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4659">The higher layer will typically provide information for the query creation once the protocol client is connected.</span></span> <span data-ttu-id="cbf24-4660">La capa superior proporciona al cliente un conjunto de restricciones, un conjunto de columnas, reglas de criterio de ordenación y un conjunto de categorización (cada uno de ellos se puede omitir), propiedades de conjunto de filas y estructura del asignador de identificadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4660">The higher layer provides the client with a restrictions set, columns set, sort order rules and categorization set (each of them can be omitted), rowset properties and property ID mapper structure.</span></span>

<span data-ttu-id="cbf24-4661">Cuando esta solicitud se recibe de una capa superior, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4661">When this request is received from a higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4662">Prepare CPMCreateQueryOut como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4662">Prepare a CPMCreateQueryOut as follows.</span></span>
-   -   <span data-ttu-id="cbf24-4663">Si hay un conjunto de columnas, establezca CColumnsSetPreset en 0x01 y rellene el campo ColumnsSet.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4663">If a columns set is present then set CColumnsSetPreset to 0x01 and fill the ColumnsSet field.</span></span>
    -   <span data-ttu-id="cbf24-4664">Si existen restricciones, establezca CRestrictionPresent en 0x01 y rellene el campo Restricción.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4664">If restrictions are present, set CRestrictionPresent to 0x01 and fill the Restriction field.</span></span>
    -   <span data-ttu-id="cbf24-4665">Si hay un conjunto de ordenación, rellene el campo SortSet.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4665">If a sort set is present, fill the SortSet field.</span></span>
    -   <span data-ttu-id="cbf24-4666">Si hay un conjunto de categorización, establezca CSortSetPresent en 0x01 y rellene el campo CategorizationSet.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4666">If a categorization set is present, set CSortSetPresent to 0x01 and fill the CategorizationSet field.</span></span>
    -   <span data-ttu-id="cbf24-4667">Establezca el resto de campos como se especifica en 2.2.3.8.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4667">Set the rest of fields as specified in 2.2.3.8</span></span>

-   <span data-ttu-id="cbf24-4668">Calcule \_ el campo ulCheckSum en el encabezado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4668">Calculate \_ulCheckSum field in the header.</span></span>
-   <span data-ttu-id="cbf24-4669">Envíe el mensaje CPMCreateQueryIn al servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4669">Send the CPMCreateQueryIn message to the server.</span></span>
-   <span data-ttu-id="cbf24-4670">Espere a recibir el mensaje CPMCreateQueryOut (consulte los detalles de la sección 3.2.5.1.1), descartando silenciosamente todos los demás mensajes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4670">Wait to receive CPMCreateQueryOut message (see details in section 3.2.5.1.1), silently discarding all other messages.</span></span>
-   <span data-ttu-id="cbf24-4671">Informe del valor del campo de estado de la respuesta y, si se ha realizado correctamente, la matriz de identificadores de cursor y los valores booleanos informativos (como se especifica en \_ 2.2.3.9) de vuelta a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4671">Report the value of the \_status field of the response and, if it was successful, the array of cursor handles, and informative Boolean values (as specified in 2.2.3.9) back to the higher layer.</span></span>

### <a name="32423-sending-a-cpmsetbindingsin-request"></a><span data-ttu-id="cbf24-4672">3.2.4.2.3 Envío de una solicitud CPMSetBindingsIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4672">3.2.4.2.3 Sending a CPMSetBindingsIn Request</span></span>

<span data-ttu-id="cbf24-4673">Normalmente, la capa superior establecerá enlaces para cada columna que se devolverá en las filas cuando ya tenga un identificador de cursor válido (después de recibir correctamente CPMCreateQueryOut, vea la sección 3.2.5.1.1).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4673">Typically, the higher layer will set bindings for each column to be returned in the rows when it already has valid cursor handle (after successfully receiving CPMCreateQueryOut, see section 3.2.5.1.1).</span></span> <span data-ttu-id="cbf24-4674">Se espera que el valor superior proporcione una matriz de estructuras CTableColumn, como se especifica en la sección 2.2.4.31, para el campo aColumns y un identificador de cursor válido.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4674">The higher is expected to provide an array of CTableColumn structures, as specified in Section 2.2.4.31, for the aColumns field and a valid cursor handle.</span></span>

<span data-ttu-id="cbf24-4675">Cuando esta solicitud se recibe de la capa superior, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4675">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4676">Calcule el número de estructuras CTableColumn de la matriz aColumns y establezca el campo cColumns en este valor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4676">Calculate the number of CTableColumn structures in the aColumns array, and set the cColumns field to this value.</span></span>
-   <span data-ttu-id="cbf24-4677">Calcule el tamaño total en bytes de los campos cColumns y aColumns y establezca el \_ campo cbBindingDesc en este valor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4677">Calculate the total size in bytes of the cColumns and aColumns fields, and set the \_cbBindingDesc field to this value.</span></span>
-   <span data-ttu-id="cbf24-4678">Establezca los campos especificados en el mensaje CPMSetBindingsIn en los valores proporcionados por la capa de aplicación superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4678">Set specified fields in CPMSetBindingsIn message to the values provided by the higher application layer.</span></span> <span data-ttu-id="cbf24-4679">Establezca el \_ campo ulChecksum en el valor calculado según se especifica en la sección 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4679">Set the \_ulChecksum field to the value calculated as specified in Section 3.2.5.</span></span>
-   <span data-ttu-id="cbf24-4680">Envíe el mensaje CPMSetBindignsIn completado al servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4680">Send the completed CPMSetBindignsIn message to the server.</span></span>
-   <span data-ttu-id="cbf24-4681">Espere a recibir un mensaje CPMSetBindingsIn del servidor, descartando otros mensajes.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4681">Wait to receive a CPMSetBindingsIn message from server, discarding other messages.</span></span>
-   <span data-ttu-id="cbf24-4682">Indique el estado del \_ campo de estado de la respuesta a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4682">Indicate the status from \_status field of the response to the higher layer.</span></span>

<span data-ttu-id="cbf24-4683">Para fines informativos, se espera que las capas superiores soliciten normalmente a un cliente que envíe un mensaje CPMGetRowsIn, pero esto no lo exige el Protocolo de servicio de indexación de contenido.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4683">For informative purposes, it is expected that higher layers will typically request a client to send a CPMGetRowsIn message, but this is not enforced by the Content Indexing Service Protocol.</span></span>

### <a name="32424-sending-a-cpmgetrowsin-request"></a><span data-ttu-id="cbf24-4684">3.2.4.2.4 Envío de una solicitud CPMGetRowsIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4684">3.2.4.2.4 Sending a CPMGetRowsIn Request</span></span>

<span data-ttu-id="cbf24-4685">Cuando la capa superior está a punto de recibir información de filas, proporcionará al cliente de protocolo un identificador válido de cursor y capítulo, y proporcionará la descripción de la búsqueda adecuada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4685">When the higher layer is about to receive rows information it will provide protocol client with valid cursor and chapter handle and give appropriate seek description.</span></span> <span data-ttu-id="cbf24-4686">Normalmente, se espera que una capa superior lo haga cuando tenga un identificador de cursor o capítulo válido y los enlaces se hayan establecido con el mensaje CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4686">Typically, a higher layer is expected to do so when it has a valid cursor and/or chapter handle, and the bindings had been set with CPMSetBindingsIn message.</span></span> <span data-ttu-id="cbf24-4687">Para acceder al conjunto de filas de un capítulo, la capa superior es usar el identificador de capítulo recibido del servidor en un mensaje CPMGetRowsOut anterior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4687">To access the rowset in a chapter, the higher layer is to use chapter handle received from the server in a previous CPMGetRowsOut message.</span></span>

<span data-ttu-id="cbf24-4688">Cuando esta solicitud se recibe de la capa superior, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4688">When this request is received from the higher layer, the client MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4689">Determine qué valor entero sin signo se va a especificar para el \_ campo cbReadBuffer.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4689">Determine what unsigned integer value to specify for the \_cbReadBuffer field.</span></span> <span data-ttu-id="cbf24-4690">Para determinar este valor, el cliente DEBE tomar el valor máximo de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4690">To determine this value, the client MUST take the maximum value from the following:</span></span>
-   -   <span data-ttu-id="cbf24-4691">Mil veces el valor del campo \_ RowsToTransfer de c.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4691">One thousand times the value of the c\_RowsToTransfer field.</span></span>
    -   <span data-ttu-id="cbf24-4692">Valor de \_ cbRowWidth, redondeado al múltiplo de 512 bytes más cercano.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4692">Value of \_cbRowWidth, rounded up to the nearest 512 byte multiple.</span></span>
    -   <span data-ttu-id="cbf24-4693">Tome el valor más alto de estos dos valores, hasta el límite de 16 000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4693">Take the higher of these two values, up to the 16K limit.</span></span>
    -   <span data-ttu-id="cbf24-4694">En los casos en los que una sola fila es mayor que 16 000, el servidor no puede devolver resultados a esta consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4694">In cases where a single row is larger than 16K, the server cannot return results to this query.</span></span>

<span data-ttu-id="cbf24-4695">Especifique una base de cliente para los datos de fila de tamaño variable en el espacio de direcciones del cliente \_ en el campo ulClientBase.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4695">Specify a client base for variable-sized row data in client address space in \_ulClientBase field.</span></span>

<span data-ttu-id="cbf24-4696">*Comportamiento de Windows: para un cliente de 32 bits que habla con un servidor de 32 bits o un cliente de 64 bits que habla con un servidor de 64 bits, este valor se establece en una dirección de memoria del búfer receptor en el proceso de aplicación. Esto permite que los punteros recibidos en el campo Filas de CPMGetRowsOut sean punteros de memoria correctos en un proceso de aplicación cliente. De lo contrario, se establece en 0x00000000.*</span><span class="sxs-lookup"><span data-stu-id="cbf24-4696">*Windows Behavior: For a 32-bit client talking to a 32-bit server, or a 64 bit client talking to a 64-bit server this value is set to a memory address of the receiving buffer in application process. This allows for pointers, received in Rows field of CPMGetRowsOut to be correct memory pointers in a client application process. Otherwise it is set to 0x00000000.*</span></span>

-   <span data-ttu-id="cbf24-4697">Calcule el tamaño de la descripción de la búsqueda y estapóla en el \_ campo cbSeek.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4697">Calculate the size of seek description and set it in the \_cbSeek field.</span></span>
-   <span data-ttu-id="cbf24-4698">Establezca el valor de cbReserved (que actuaría como desplazamiento para El inicio de filas) en el valor \_ de cbSeek más 0x14.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4698">Set the value of cbReserved (which would act as an offset for Rows start) to the value of \_cbSeek plus 0x14.</span></span>
-   <span data-ttu-id="cbf24-4699">Envíe un mensaje de CPMConnectIn como se especifica en 2.2.3.15 al servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4699">Send a CPMConnectIn message as specified in 2.2.3.15 to the server.</span></span>

### <a name="32425-sending-a-cpmfetchvaluein-request"></a><span data-ttu-id="cbf24-4700">3.2.4.2.5 Envío de una solicitud CPMFetchValueIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4700">3.2.4.2.5 Sending a CPMFetchValueIn Request</span></span>

<span data-ttu-id="cbf24-4701">Si el cliente recibe una respuesta CPMGetRowsOut del servidor con el campo Status de la columna establecido en StatusDeferred (0x01), significa que el valor de propiedad no se incluyó en el campo Rows del mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4701">If the client receives a CPMGetRowsOut response from the server with the column's Status field set to StatusDeferred (0x01) it means that the property value was not included in the Rows field of the CPMGetRowsOut message.</span></span> <span data-ttu-id="cbf24-4702">En este caso, la capa superior normalmente solicita al cliente de protocolo que recupere el valor por medio del mensaje CPMFetchValueIn y proporciona el valor PropSpec y wid para una propiedad diferida, que el cliente de protocolo DEBE usar en el primer mensaje \_ CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4702">In this case the higher layer typically asks the protocol client to retrieve the value by means of CPMFetchValueIn message, and provides the PropSpec and \_wid value for a deferred property, which the protocol client MUST use in the first CPMFetchValueIn message.</span></span>

<span data-ttu-id="cbf24-4703">Si este es el primer mensaje CPMFetchValueIn que el cliente ha enviado para solicitar la propiedad especificada, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4703">If this is the first CPMFetchValueIn message the client has sent to request the specified property, the client MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4704">Establezca todos los campos de un mensaje como se especifica en la sección 2.2.3.19.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4704">Set all the fields in a message as specified in section 2.2.3.19.</span></span>
-   <span data-ttu-id="cbf24-4705">Establezca \_ cbSoFar en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4705">Set \_cbSoFar to 0x00000000.</span></span>
-   <span data-ttu-id="cbf24-4706">Establezca Bytes actuales recibidos en 0.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4706">Set Current Bytes Received to 0.</span></span>
-   <span data-ttu-id="cbf24-4707">Envíe el mensaje CPMFetchValueIn al servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4707">Send the CPMFetchValueIn message to the server.</span></span>

### <a name="32426-sending-a-cpmfreecursorin-request"></a><span data-ttu-id="cbf24-4708">3.2.4.2.6 Envío de una solicitud CPMFreeCursorIn</span><span class="sxs-lookup"><span data-stu-id="cbf24-4708">3.2.4.2.6 Sending a CPMFreeCursorIn Request</span></span>

<span data-ttu-id="cbf24-4709">Una vez que el nivel superior ya no usa la consulta de búsqueda, puede liberar los recursos en el servidor solicitando al cliente que envíe un mensaje CPMFreeCursorIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4709">Once the higher level is no longer using the search query, it can release the resources on the server by asking the client to send a CPMFreeCursorIn message.</span></span>

<span data-ttu-id="cbf24-4710">Cuando se recibe esta solicitud, el cliente DEBE enviar un mensaje CPMFreeCursorIn tal como se especifica en 2.2.3.28 al servidor, que contiene el identificador especificado por la capa superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4710">When this request is received, the client MUST send a CPMFreeCursorIn message as specified in 2.2.3.28 to the server, containing the handle specified by the upper layer.</span></span>

### <a name="32427-sending-a-cpmdisconnect-message"></a><span data-ttu-id="cbf24-4711">3.2.4.2.7 Envío de un mensaje CPMDisconnect</span><span class="sxs-lookup"><span data-stu-id="cbf24-4711">3.2.4.2.7 Sending a CPMDisconnect Message</span></span>

<span data-ttu-id="cbf24-4712">Si la capa superior no tiene más consultas para el servicio de indexación, para liberar más recursos de servidor, la aplicación puede solicitar que el cliente envíe un mensaje CPMDisconnect al servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4712">If the higher layer has no more queries for the indexing service, to free up more server resources, the application may request that the client send a CPMDisconnect message to the server.</span></span> <span data-ttu-id="cbf24-4713">Cuando se recibe esta consulta, el cliente DEBE enviar simplemente el mensaje como se solicitó.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4713">When this query is received, the client MUST simply send the message as requested.</span></span> <span data-ttu-id="cbf24-4714">No hay ninguna respuesta a este mensaje desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4714">There is no response to this message from the server.</span></span>

### <a name="325-message-processing-and-sequencing-rules"></a><span data-ttu-id="cbf24-4715">3.2.5 Reglas de procesamiento y secuenciación de mensajes</span><span class="sxs-lookup"><span data-stu-id="cbf24-4715">3.2.5 Message Processing and Sequencing Rules</span></span>

<span data-ttu-id="cbf24-4716">Cuando el cliente recibe una respuesta de mensaje del servidor, el cliente DEBE usar el último mensaje enviado para determinar si el mensaje recibido del servidor es el esperado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4716">When the client receives a message response from the server, the client MUST use the Last Sent Message to determine if the message received from the server is the one expected by the client.</span></span> <span data-ttu-id="cbf24-4717">Todos los mensajes \_ con el campo msg distinto del de Last Send Message (Último mensaje de envío) DEBEN omitirse.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4717">All messages with \_msg field different from the one in Last Send Message MUST be ignored.</span></span>

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a><span data-ttu-id="cbf24-4718">3.2.5.1 Recepción de una respuesta CPMCreateQueryOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-4718">3.2.5.1 Receiving a CPMCreateQueryOut Response</span></span>

<span data-ttu-id="cbf24-4719">Cuando el cliente recibe una respuesta de mensaje CPMCreateQueryOut del servidor, el cliente DEBE devolver el estado y (si el estado es correcto) controlar los valores del cursor de vuelta a una \_ capa superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4719">When the client receives a CPMCreateQueryOut message response from the server, the client MUST return \_status and (if the status is successful) cursor handle values back to higher layer.</span></span> <span data-ttu-id="cbf24-4720">Las acciones adicionales están hasta la capa superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4720">Any further actions are up to the higher layer.</span></span>

<span data-ttu-id="cbf24-4721">Como la capa superior es consciente de la estructura de consulta, siempre esperará que se devuelva el número correcto de identificadores de cursor en el mensaje CPMCreateOueryOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4721">As the higher layer is aware of query structure it will always expect correct number of cursor handles to be returned in the CPMCreateOueryOut message.</span></span> <span data-ttu-id="cbf24-4722">Los identificadores de cursor se devuelven en el orden siguiente: el primer identificador es para el conjunto de filas sin cadena, el segundo es para el primer conjunto de filas con capítulos (que es la agrupación de resultados según la primera categoría especificada en el campo CategorizationSet del mensaje CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4722">The cursor handles are returned in the following order: the first handle is to the unchaptered rowset, the second is to the first chaptered rowset (which is the grouping of results based on the first category specified in the CategorizationSet field of the CPMCreateQueryIn message.)</span></span>

<span data-ttu-id="cbf24-4723">Con fines informativos, se espera que las capas superiores puedan realizar las siguientes acciones, pero el cliente CISP no las aplica:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4723">For informative purposes, it is expected that higher layers can do the following actions, but these are not enforced by the CISP client:</span></span>

-   <span data-ttu-id="cbf24-4724">Use CPMSetBindingsIn para establecer enlaces para columnas individuales y realizar las acciones posteriores en la ruta de acceso de consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4724">Use CPMSetBindingsIn, to set bindings for individual columns and do any subsequent actions on query path</span></span>
-   <span data-ttu-id="cbf24-4725">Use CPMGetQueryStatusIn para comprobar el progreso de ejecución de una consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4725">Use CPMGetQueryStatusIn, to check on the execution progress of a query.</span></span>
-   <span data-ttu-id="cbf24-4726">Use CPMRatioFinishedIn para solicitar el porcentaje de finalización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4726">Use CPMRatioFinishedIn, to request the completion percentage of the query.</span></span>

### <a name="3252-receiving-a-cpmgetrowsout-response"></a><span data-ttu-id="cbf24-4727">3.2.5.2 Recepción de una respuesta CPMGetRowsOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-4727">3.2.5.2 Receiving a CPMGetRowsOut Response</span></span>

<span data-ttu-id="cbf24-4728">Cuando el cliente recibe una respuesta de mensaje CPMGetRowsOut del servidor, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4728">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4729">Compruebe si el \_ campo de estado del encabezado indica que se ha hecho correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4729">Check if the \_status field in the header indicates success or failure.</span></span>
-   <span data-ttu-id="cbf24-4730">Si el \_ valor de estado es BÚFER DE ESTADO DEMASIADO PEQUEÑO (0xC0000023), el cliente \_ DEBE comprobar el estado Último mensaje \_ \_ enviado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4730">If the \_status value is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), the client MUST check the Last Message Sent state.</span></span> <span data-ttu-id="cbf24-4731">Si no contiene un mensaje CPMGetRowsIn, el mensaje recibido DEBE omitirse en modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4731">If it does not contain a CPMGetRowsIn message, the received message MUST be silently ignored.</span></span> <span data-ttu-id="cbf24-4732">De lo contrario, el cliente DEBE enviar al servidor un nuevo mensaje CPMGetRowsIn con todos los campos idénticos al almacenado, excepto que cbReadBuffer DEBE aumentarse en \_ 512 (pero no mayor que 0x4000).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4732">Otherwise, the client MUST send to the server a new CPMGetRowsIn message with all fields identical to the stored one, except that the \_cbReadBuffer MUST be increased by 512 (but not greater than 0x4000).</span></span> <span data-ttu-id="cbf24-4733">Si el estado es STATUS BUFFER TOO SMALL (0xC0000023) y El último mensaje enviado ya tiene \_ \_ cbReadBuffer igual 0x4000 el cliente DEBE notificar el error hasta el \_ \_ nivel \_ superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4733">If \_status is STATUS\_BUFFER\_TOO\_SMALL (0xC0000023), and Last Message Sent already has \_cbReadBuffer equal to 0x4000 client MUST report the error up to the higher level.</span></span>
-   <span data-ttu-id="cbf24-4734">Si el \_ valor de estado es cualquier otro valor de error, el cliente DEBE indicar el error hasta la capa superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4734">If the \_status value is any other error value, the client MUST indicate the failure up to the higher layer.</span></span>
-   <span data-ttu-id="cbf24-4735">Si el valor de estado indica correcto, los resultados DEBEN indicarse hasta la capa superior que solicita la información y las acciones adicionales están hasta \_ la capa superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4735">If the \_status value indicates success, the results MUST be indicated up to the higher layer requesting the information, and further actions are up to the higher layer.</span></span>

<span data-ttu-id="cbf24-4736">Con fines informativos, se espera que las capas superiores realicen normalmente las siguientes acciones, pero el cliente del Protocolo de servicio de indexación de contenido no las aplica:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4736">For informative purposes, it is expected that higher layers will typically do the following actions, but these are not enforced by the Content Indexing Service Protocol client:</span></span>

-   <span data-ttu-id="cbf24-4737">Si los valores de las filas representan los identificadores de documento, los identificadores de capítulo o marcador de la capa superior normalmente los almacenarán para su uso en operaciones posteriores que implican identificadores de documento válidos, identificadores de capítulos o marcadores.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4737">If the values in rows represent the document IDs, chapter or bookmark handles the higher layer will typically store them for use in subsequent operations which involve valid document IDs, chapter or bookmark handles.</span></span>
-   <span data-ttu-id="cbf24-4738">La capa superior normalmente almacenará o mostrará o usará los datos de los valores de fila.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4738">The higher layer will typically store or display or otherwise use the data from row values.</span></span>
-   <span data-ttu-id="cbf24-4739">Para los valores que se marcaron como capas más altas diferidas, se capturará el valor mediante mensajes CPMFetchValueIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4739">For the values which were marked as deferred higher layer will fetch the value using CPMFetchValueIn messages.</span></span>
-   <span data-ttu-id="cbf24-4740">La descripción de la búsqueda también se devuelve a una capa superior y la capa superior puede reutilizarla o examinarla.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4740">The seek description is returned back to higher layer as well, and can be reused or examined by the higher layer.</span></span>

<span data-ttu-id="cbf24-4741">Con fines informativos, si la capa superior solicitó identificadores a capítulos y marcadores que se recibieron en las filas, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4741">For informative purposes, if the higher layer requested handles to chapters and bookmarks which were received in the rows, it may do the following:</span></span>

-   <span data-ttu-id="cbf24-4742">Use CPMGetQueryStatusExIn para comprobar el progreso de ejecución de una consulta, así como información de estado adicional, como el número de documentos filtrados, los documentos que quedan por filtrar, la proporción de documentos procesados por la consulta, el número total de filas de la consulta y la posición del marcador en el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4742">Use CPMGetQueryStatusExIn, to check on the execution progress of a query, as well as additional status information, such as the number of filtered documents, documents remaining to be filtered, the ratio of documents processed by the query, the total number of rows in the query, and the position of the bookmark in the rowset.</span></span>
-   <span data-ttu-id="cbf24-4743">Use CPMGetNotify para solicitar que el servidor notifique al cliente los cambios del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4743">Use CPMGetNotify, to request that the server notify the client of rowset changes.</span></span>
-   <span data-ttu-id="cbf24-4744">Use CPMGetApproximatePositionIn para solicitar la posición aproximada de un marcador en un capítulo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4744">Use CPMGetApproximatePositionIn, to request the approximate position of a bookmark in a chapter.</span></span>
-   <span data-ttu-id="cbf24-4745">Use CPMCompareBmkIn para solicitar una comparación de dos marcadores en un capítulo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4745">Use CPMCompareBmkIn, to request a comparison of two bookmarks in a chapter.</span></span>
-   <span data-ttu-id="cbf24-4746">Use CPMRestartPositionIn en el servidor para cambiar la ubicación del cursor al inicio del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4746">Use CPMRestartPositionIn, to the server to change the location of the cursor to the start of rowset.</span></span>

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a><span data-ttu-id="cbf24-4747">3.2.5.3 Recepción de una respuesta CPMFetchValueOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-4747">3.2.5.3 Receiving a CPMFetchValueOut Response</span></span>

<span data-ttu-id="cbf24-4748">Cuando el cliente recibe una respuesta de mensaje CPMGetRowsOut del servidor, el cliente DEBE hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4748">When the client receives a CPMGetRowsOut message response from the server, the client MUST do the following:</span></span>

-   <span data-ttu-id="cbf24-4749">Compruebe si el \_ campo de estado del encabezado indica que se ha hecho correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4749">Check if the \_status field in the header indicates success or failure.</span></span> <span data-ttu-id="cbf24-4750">En caso de error, notifíquelo a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4750">In a case of failure notify the higher layer.</span></span> <span data-ttu-id="cbf24-4751">De lo contrario, continúe a continuación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4751">Otherwise, continue below.</span></span>
-   <span data-ttu-id="cbf24-4752">Active fValueExist y, si se establece en 0x00000000 notificar a la capa \_ superior que no se encontró el valor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4752">Check \_fValueExist, and if set to 0x00000000 notify the higher layer that the value was not found.</span></span>
-   <span data-ttu-id="cbf24-4753">En caso contrario, \_ anexe los bytes cbValue de vValue al valor de propiedad actual.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4753">Otherwise append \_ cbValue bytes from vValue to Current Property Value.</span></span>
-   <span data-ttu-id="cbf24-4754">Si fMoreExists se establece en 0x00000001 incremente los bytes actuales recibidos por cbValue y envíe un mensaje \_ \_ \_ \_ CPMFetchValueIn al servidor, estableciendo cbSoFar en el valor de \_ Bytes actuales recibidos, cbPropSpec en cero y \_ \_ cbChunk en el tamaño de búfer deseado por la capa superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4754">If \_\_fMoreExists is set to 0x00000001 then increment \_Current Bytes Received by \_cbValue and send a CPMFetchValueIn message to the server, setting \_cbSoFar to the value of Current Bytes Received, \_cbPropSpec to zero and \_cbChunk to the buffer size desired by the higher layer.</span></span>
-   <span data-ttu-id="cbf24-4755">Si fMoreExists se establece en 0x00000000, indique el valor de propiedad de Valor de propiedad \_ actual a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4755">If \_fMoreExists is set to 0x00000000 then indicate the property value from Current Property Value to the higher layer.</span></span>

### <a name="3254-receiving-a-cpmfreecursorout-response"></a><span data-ttu-id="cbf24-4756">3.2.5.4 Recepción de una respuesta CPMFreeCursorOut</span><span class="sxs-lookup"><span data-stu-id="cbf24-4756">3.2.5.4 Receiving a CPMFreeCursorOut Response</span></span>

<span data-ttu-id="cbf24-4757">Cuando el cliente recibe una respuesta de mensaje CPMFreeCursorOut correcta del servidor, el cliente DEBE devolver el valor \_ cCursorsRemaining a la capa superior.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4757">When the client receives a successful CPMFreeCursorOut message response from the server, the client MUST return the \_cCursorsRemaining value to the higher layer.</span></span>

<span data-ttu-id="cbf24-4758">La siguiente información se proporciona solo con fines informativos y no la aplica el cliente CISP.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4758">The following information is given for informative purposes only and is not enforced by the CISP client.</span></span> <span data-ttu-id="cbf24-4759">Se espera que la capa superior realice un seguimiento de los identificadores de cursor y no use los que ya se han liberado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4759">The higher layer is expected to keep track of cursor handles and not to use ones which have already been freed.</span></span> <span data-ttu-id="cbf24-4760">Una vez que el número de cCursorsRemaining es igual a 0x00000000, la capa superior puede usar la conexión para especificar otra consulta (mediante un mensaje \_ CPMCreateQueryIn).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4760">Once the number of \_cCursorsRemaining is equal to 0x00000000, the higher layer can use the connection to specify another query (using a CPMCreateQueryIn message).</span></span>

### <a name="326-timer-events"></a><span data-ttu-id="cbf24-4761">3.2.6 Eventos de temporizador</span><span class="sxs-lookup"><span data-stu-id="cbf24-4761">3.2.6 Timer Events</span></span>

<span data-ttu-id="cbf24-4762">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4762">None.</span></span>

### <a name="327-other-local-events"></a><span data-ttu-id="cbf24-4763">3.2.7 Otros eventos locales</span><span class="sxs-lookup"><span data-stu-id="cbf24-4763">3.2.7 Other Local Events</span></span>

<span data-ttu-id="cbf24-4764">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4764">None.</span></span>

## <a name="4-protocol-examples"></a><span data-ttu-id="cbf24-4765">4 Ejemplos de protocolo</span><span class="sxs-lookup"><span data-stu-id="cbf24-4765">4 Protocol Examples</span></span>

-   [<span data-ttu-id="cbf24-4766">4.1 Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4766">4.1 Example 1</span></span>](#41-example-1)
-   [<span data-ttu-id="cbf24-4767">4.2 Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4767">4.2 Example 2</span></span>](#42-example-2)

### <a name="41-example-1"></a><span data-ttu-id="cbf24-4768">4.1 Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="cbf24-4768">4.1 Example 1</span></span>

<span data-ttu-id="cbf24-4769">En el ejemplo siguiente, se considera un escenario en el que el usuario JOHN de la máquina A quiere obtener los tamaños de los archivos que contienen la palabra "Microsoft" del conjunto de documentos almacenados en el servidor X en el catálogo SYSTEM.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4769">In the following example, we consider a scenario in which the user JOHN on machine A wants to obtain the sizes of files that contain the word "Microsoft" from the set of documents stored on server X in catalog SYSTEM.</span></span> <span data-ttu-id="cbf24-4770">Supongamos que la máquina A ejecuta un sistema operativo Windows XP de 32 bits y la máquina X ejecuta un sistema operativo Windows Server 2003 de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4770">Let us assume that machine A is running a 32-bit Windows XP operating system and machine X is running a 32-bit Windows Server 2003 operating system.</span></span>

1.  <span data-ttu-id="cbf24-4771">El usuario inicia una aplicación de búsqueda y escribe la consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4771">The user launches a search application and enters the search query.</span></span> <span data-ttu-id="cbf24-4772">A su vez, la aplicación pasa la consulta de búsqueda al cliente de protocolo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4772">The application in turn passes the search query to the protocol client.</span></span>
2.  <span data-ttu-id="cbf24-4773">El cliente de protocolo establece una conexión con el servidor de indexación X. El cliente de protocolo usa la canalización con nombre CI TFTPDS para conectarse al \\ servidor X a través de \\ \_ SMB.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4773">The protocol client establishes a connection with indexing server X. The protocol client uses the named pipe \\pipe\\CI\_SKADS to connect to the server X over SMB.</span></span>
3.  <span data-ttu-id="cbf24-4774">A continuación, el cliente de protocolo prepara un mensaje CPMConnectIn con los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4774">The protocol client then prepares a CPMConnectIn message with the following values:</span></span>

    <span data-ttu-id="cbf24-4775">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4775">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cbf24-4776">**\_ msg** se establece en 0x000000C8, lo que indica que se trata de un mensaje CPMConnectIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4776">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectIn message.</span></span>
    -   <span data-ttu-id="cbf24-4777">**\_ status** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4777">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cbf24-4778">**\_ ulChecksum** contiene la suma de comprobación, calculada como se especifica en la sección 3.2.4.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4778">**\_ulChecksum** contains the checksum, computed as specified in Section 3.2.4.</span></span>
    -   <span data-ttu-id="cbf24-4779">**\_ ulReserved2** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4779">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="cbf24-4780">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4780">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cbf24-4781">**\_ iClientVersion** se establece en 0x00000008, lo que indica que el servidor va a validar el campo de suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4781">**\_iClientVersion** is set to 0x00000008, indicating that the server is to validate the checksum field.</span></span>
    -   <span data-ttu-id="cbf24-4782">**\_ fClientIsRemote** se establece en 0x00000001, lo que indica que el servidor es un servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4782">**\_fClientIsRemote** is set to 0x00000001, indicating that the server is a remote server.</span></span>
    -   <span data-ttu-id="cbf24-4783">**\_ cbBlob1 se** establece en el tamaño, en bytes, de los campos cPropSet, PropertySet1 y PropertySet2 combinados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4783">**\_cbBlob1** is set to the size, in bytes, of the cPropSet, PropertySet1 and PropertySet2 fields combined.</span></span>
    -   <span data-ttu-id="cbf24-4784">**\_ cbBlob2** se establece en 0x00000004 (lo que significa que no hay conjuntos de propiedades adicionales).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4784">**\_cbBlob2** is set to 0x00000004 (meaning no extra property sets).</span></span>
    -   <span data-ttu-id="cbf24-4785">**MachineName** se establece en A.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4785">**MachineName** is set to A.</span></span>
    -   <span data-ttu-id="cbf24-4786">**UserName** se establece en JOHN.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4786">**UserName** is set to JOHN.</span></span>
    -   <span data-ttu-id="cbf24-4787">**cPropSets** se establece en 0x00000002.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4787">**cPropSets** is set to 0x00000002.</span></span>
    -   <span data-ttu-id="cbf24-4788">**El campo PropertySet1** es de tipo CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4788">**PropertySet1** field is of type CDbPropSet.</span></span> <span data-ttu-id="cbf24-4789">La estructura CDbPropSet que comprende el campo PropertySet1 se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4789">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>
        -   <span data-ttu-id="cbf24-4790">**El campo GuidPropSet** se establece en A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ EXT).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4790">**GuidPropSet** field is set to A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET\_FSCIFRMWRK\_EXT).</span></span>
        -   <span data-ttu-id="cbf24-4791">**El campo cProperties** se establece en 0x00000004.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4791">**cProperties** field is set to 0x00000004.</span></span>
        -   <span data-ttu-id="cbf24-4792">**El campo aProps** es una matriz de estructuras CDbProp.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4792">**aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="cbf24-4793">Para el **elemento aProps \[ 0: \]**</span><span class="sxs-lookup"><span data-stu-id="cbf24-4793">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="cbf24-4794">**PropId** se establece en 0x00000002 (DBPROP \_ CI \_ CATALOG \_ NAME).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4794">**PropId** is set to 0x00000002 (DBPROP\_CI\_CATALOG\_NAME).</span></span>
            -   <span data-ttu-id="cbf24-4795">**DBPROPOPTIONS** se establece en 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4795">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="cbf24-4796">**DBPROPSTATUS se** establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4796">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cbf24-4797">Para el **elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="cbf24-4797">For the **ColId** element:</span></span>
                -   <span data-ttu-id="cbf24-4798">**eKind** se establece en 0x00000001 (DBKIND \_ GUID \_ PROPID)</span><span class="sxs-lookup"><span data-stu-id="cbf24-4798">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID)</span></span>
                -   <span data-ttu-id="cbf24-4799">**GUID** es null (todos los ceros), lo que significa que el valor se aplica a la consulta, no solo a una sola columna.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4799">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="cbf24-4800">**ulID** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4800">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cbf24-4801">Para el **elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="cbf24-4801">For the **vValue** element:</span></span>
                -   <span data-ttu-id="cbf24-4802">**vType** se establece en 0x001F (VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4802">**vType** is set to 0x001F (VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="cbf24-4803">**vValue** se establece en "SYSTEM", el nombre del catálogo deseado.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4803">**vValue** is set to "SYSTEM", the name of the desired catalog.</span></span>

            <span data-ttu-id="cbf24-4804">Para el **elemento aProps \[ 1: \]**</span><span class="sxs-lookup"><span data-stu-id="cbf24-4804">For the **aProps\[1\]** element:</span></span>

            -   <span data-ttu-id="cbf24-4805">**PropId** se establece en 0x00000007 (DBPROP \_ CI \_ QUERY \_ TYPE)</span><span class="sxs-lookup"><span data-stu-id="cbf24-4805">**PropId** is set to 0x00000007 (DBPROP\_CI\_QUERY\_TYPE)</span></span>
            -   <span data-ttu-id="cbf24-4806">**DBPROPOPTIONS** se establece en 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4806">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="cbf24-4807">**DBPROPSTATUS** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4807">**DBPROPSTATUS** is set to0x00000000.</span></span>
            -   <span data-ttu-id="cbf24-4808">Para el **elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="cbf24-4808">For the **ColId** element:</span></span>
                -   <span data-ttu-id="cbf24-4809">**eKind** se establece en 0x00000001 (DBKIND \_ GUID \_ PROPID).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4809">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="cbf24-4810">**GUID** es null (todos los ceros), lo que significa que el valor se aplica a la consulta, no solo a una sola columna.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4810">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="cbf24-4811">**ulID** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4811">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cbf24-4812">Para el **elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="cbf24-4812">For the **vValue** element:</span></span>
                -   <span data-ttu-id="cbf24-4813">**vType** se establece en 0x0003 (VT \_ I4).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4813">**vType** is set to 0x0003 (VT\_I4).</span></span>
                -   <span data-ttu-id="cbf24-4814">**vValue** se establece en 0x00000000 (CiNormal), lo que significa que es una consulta normal.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4814">**vValue** is set to 0x00000000 (CiNormal), meaning it is a regular query.</span></span>

            <span data-ttu-id="cbf24-4815">Para el **elemento aProps \[ 2: \]**</span><span class="sxs-lookup"><span data-stu-id="cbf24-4815">For the **aProps\[2\]** element:</span></span>

            -   <span data-ttu-id="cbf24-4816">**PropId** se establece en 0x00000004 (MARCAS DE \_ ÁMBITO DE CI DE \_ \_ DBPROP).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4816">**PropId** is set to 0x00000004 (DBPROP\_CI\_SCOPE\_FLAGS).</span></span>
            -   <span data-ttu-id="cbf24-4817">**DBPROPOPTIONS** se establece en 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4817">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="cbf24-4818">**DBPROPSTATUS se** establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4818">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cbf24-4819">Para el **elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="cbf24-4819">For the **ColId** element:</span></span>
                -   <span data-ttu-id="cbf24-4820">**eKind** se establece en 0x00000001 (DBKIND \_ GUID \_ PROPID).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4820">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="cbf24-4821">**GUID** es null (todos los ceros), lo que significa que el valor se aplica a la consulta, no solo a una sola columna.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4821">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="cbf24-4822">**ulID** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4822">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cbf24-4823">Para el **elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="cbf24-4823">For the **vValue** element:</span></span>
                -   <span data-ttu-id="cbf24-4824">**vType:** 0x1003 (VT \_ VECTOR \| VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="cbf24-4824">**vType**: 0x1003 (VT\_VECTOR \| VT\_I4)</span></span>
                -   <span data-ttu-id="cbf24-4825">**vValue:** 0x00000001 /0x00000001 (un elemento con el valor 1), lo que significa subcarpetas de búsqueda</span><span class="sxs-lookup"><span data-stu-id="cbf24-4825">**vValue**: 0x00000001 / 0x00000001 (one element with value 1), meaning search sub-folders</span></span>

            <span data-ttu-id="cbf24-4826">Para el **elemento aProps \[ 3: \]**</span><span class="sxs-lookup"><span data-stu-id="cbf24-4826">For the **aProps\[3\]** element:</span></span>

            -   <span data-ttu-id="cbf24-4827">**PropId:** 0x00000003 (ÁMBITOS DE INCLUDE \_ DE DBPROP \_ \_ CI)</span><span class="sxs-lookup"><span data-stu-id="cbf24-4827">**PropId**: 0x00000003 (DBPROP\_CI\_INCLUDE\_SCOPES)</span></span>
            -   <span data-ttu-id="cbf24-4828">**DBPROPOPTIONS:** 0x0000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-4828">**DBPROPOPTIONS**: 0x0000000</span></span>
            -   <span data-ttu-id="cbf24-4829">**DBPROPSTATUS:** 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-4829">**DBPROPSTATUS**: 0x00000000</span></span>
            -   <span data-ttu-id="cbf24-4830">Para el **elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="cbf24-4830">For the **ColId** element:</span></span>
                -   <span data-ttu-id="cbf24-4831">**eKind** se establece en 0x00000001 (DBKIND \_ GUID \_ PROPID).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4831">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID).</span></span>
                -   <span data-ttu-id="cbf24-4832">**GUID** es null (todos los ceros), lo que significa que el valor se aplica a la consulta, no solo a una sola columna.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4832">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="cbf24-4833">**ulID** se establece en 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-4833">**ulID** is set to 0x00000000</span></span>
            -   <span data-ttu-id="cbf24-4834">Para el **elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="cbf24-4834">For the **vValue** element:</span></span>
                -   <span data-ttu-id="cbf24-4835">**vType** se establece en 0x101F (VT \_ VECTOR \| VT \_ LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4835">**vType** is set to 0x101F (VT\_VECTOR \| VT\_LPWSTR).</span></span>
                -   <span data-ttu-id="cbf24-4836">**vValue** se establece en 0x00000001 / 0x00000002 / " " " (un elemento con una cadena terminada en null de 2 caracteres), lo que significa el \\ ámbito raíz.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4836">**vValue** is set to 0x00000001 / 0x00000002 / "\\" (one element with a 2 character null-terminated string), meaning the root scope.</span></span>

    -   <span data-ttu-id="cbf24-4837">El **campo PropertySet2** es de tipo CDbPropSet.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4837">The **PropertySet2** field is of type CDbPropSet.</span></span>

        <span data-ttu-id="cbf24-4838">La estructura CDbPropSet que comprende el campo PropertySet1 se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4838">The CDbPropSet structure comprising the PropertySet1 field is populated as follows:</span></span>

        -   <span data-ttu-id="cbf24-4839">**GuidPropSet** se establece en AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ EXT).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4839">**GuidPropSet** is set to AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET\_CIFRMWRKCORE\_EXT).</span></span>
        -   <span data-ttu-id="cbf24-4840">**El campo cProperties** se establece en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4840">**cProperties** field is set to 0x00000001.</span></span>
        -   <span data-ttu-id="cbf24-4841">El **campo aProps** es una matriz de estructuras CDbProp.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4841">The **aProps** field is an array of CDbProp structures.</span></span>

            <span data-ttu-id="cbf24-4842">Para el **elemento aProps \[ 0: \]**</span><span class="sxs-lookup"><span data-stu-id="cbf24-4842">For the **aProps\[0\]** element:</span></span>

            -   <span data-ttu-id="cbf24-4843">**PropId** se establece en 0x00000002 (DBPROP \_ MACHINE).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4843">**PropId** is set to 0x00000002 (DBPROP\_MACHINE).</span></span>
            -   <span data-ttu-id="cbf24-4844">**DBPROPOPTIONS** se establece en 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4844">**DBPROPOPTIONS** is set to 0x0000000.</span></span>
            -   <span data-ttu-id="cbf24-4845">**DBPROPSTATUS se** establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4845">**DBPROPSTATUS** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cbf24-4846">Para el **elemento ColId:**</span><span class="sxs-lookup"><span data-stu-id="cbf24-4846">For the **ColId** element:</span></span>
                -   <span data-ttu-id="cbf24-4847">**eKind** se establece en 0x00000001 (DBKIND \_ GUID \_ PROPID),</span><span class="sxs-lookup"><span data-stu-id="cbf24-4847">**eKind** is set to 0x00000001 (DBKIND\_GUID\_PROPID),</span></span>
                -   <span data-ttu-id="cbf24-4848">**GUID** es null (todos los ceros), lo que significa que el valor se aplica a la consulta, no solo a una sola columna.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4848">**GUID** is null (all zeros), meaning the value applies to the query, not just a single column.</span></span>
                -   <span data-ttu-id="cbf24-4849">**ulID** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4849">**ulID** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cbf24-4850">Para **el elemento vValue:**</span><span class="sxs-lookup"><span data-stu-id="cbf24-4850">For **vValue** element:</span></span>
                -   <span data-ttu-id="cbf24-4851">**vType:** 0x0008 (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="cbf24-4851">**vType**: 0x0008 (VT\_BSTR)</span></span>
                -   <span data-ttu-id="cbf24-4852">**vValue:** 0x04 / "X" (4 bytes /cadena Unicode terminada en NULL), lo que significa "X" -name de un servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4852">**vValue**: 0x04 / "X" (4 bytes / null-terminated Unicode string), meaning "X" -name of a server.</span></span>

    -   <span data-ttu-id="cbf24-4853">**El campo cExtPropSet** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4853">**cExtPropSet** field is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cbf24-4854">**la matriz aPropertySets** no existe.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4854">**aPropertySets** array does not exist.</span></span>
    -   <span data-ttu-id="cbf24-4855">Se rellenan varios campos de relleno según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4855">Various padding fields are filled in as needed.</span></span> <span data-ttu-id="cbf24-4856">El mensaje se envía al servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4856">The message is sent to the server.</span></span>

4.  <span data-ttu-id="cbf24-4857">El servidor comprueba que **\_ ulChecksum** es correcto, comprueba que el usuario está autorizado para realizar esta solicitud y responde con un mensaje CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4857">The server verifies that the **\_ulChecksum** is correct, verifies that the user is authorized to make this request, and responds with a CPMConnectOut message.</span></span>

    <span data-ttu-id="cbf24-4858">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4858">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cbf24-4859">**\_ msg** se establece en 0x000000C8, lo que indica que se trata de un mensaje CPMConnectOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4859">**\_msg** is set to 0x000000C8, indicating that this is a CPMConnectOut message.</span></span>
    -   <span data-ttu-id="cbf24-4860">**\_ status** se establece en 0x0000000 que indica SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4860">**\_status** is set to 0x0000000 indicating SUCCESS.</span></span>
    -   <span data-ttu-id="cbf24-4861">**\_ ulChecksum** se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4861">**\_ulChecksum** is set to 0.</span></span>
    -   <span data-ttu-id="cbf24-4862">**\_ ulReserved2** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4862">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="cbf24-4863">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4863">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cbf24-4864">**\_ El campo serverVersion** se establece en 0x00000007 (Windows XP de 32 bits o Windows Server 2003 de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4864">**\_serverVersion** field is set to 0x00000007 (32-bit Windows XP or 32-bit Windows Server 2003).</span></span>
    -   <span data-ttu-id="cbf24-4865">**\_ los** campos reservados se rellenan con datos arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4865">**\_reserved** fields are filled with arbitrary data.</span></span>

5.  <span data-ttu-id="cbf24-4866">El cliente prepara un mensaje CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4866">The client prepares a CPMCreateQueryIn message.</span></span>

    <span data-ttu-id="cbf24-4867">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4867">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cbf24-4868">**\_ msg** se establece en 0x000000CA, lo que indica que se trata de un mensaje CPMCreateQueryIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4868">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryIn message.</span></span>
    -   <span data-ttu-id="cbf24-4869">**\_ status** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4869">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cbf24-4870">**\_ ulChecksum** contiene la suma de comprobación, calculada según 3.2.5.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4870">**\_ulChecksum** contains the checksum, computed according to 3.2.5.</span></span>
    -   <span data-ttu-id="cbf24-4871">**\_ ulReserved2** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4871">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="cbf24-4872">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4872">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cbf24-4873">**El** campo Tamaño se establece en el tamaño del resto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4873">**Size** field is set to the size of the rest of the message.</span></span>
    -   <span data-ttu-id="cbf24-4874">**El campo CColumnSetPresent** se establece en 0x01.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4874">**CColumnSetPresent** field is set to 0x01.</span></span>
    -   <span data-ttu-id="cbf24-4875">**El campo ColumnSet** es de tipo CColumnSet.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4875">**ColumnSet** field is of type CColumnSet.</span></span> <span data-ttu-id="cbf24-4876">La estructura CColumnSet que comprende este campo se establece de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4876">The CColumnSet structure comprising this field is set as follows:</span></span>
        -   <span data-ttu-id="cbf24-4877">**\_ count** field se establece en 0x00000001 indica que se devuelve una columna.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4877">**\_count** field is set to 0x00000001 indicating one column is returned.</span></span>
        -   <span data-ttu-id="cbf24-4878">**la** matriz indexes 0x00000000 indica la primera entrada \_ en aPropSpec.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4878">**indexes** array is 0x00000000 indicating the first entry in \_aPropSpec.</span></span>
    -   <span data-ttu-id="cbf24-4879">**El campo CRestrictionPresent** se establece en 0x01 indica que **el campo Restricción** está presente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4879">**CRestrictionPresent** field is set to 0x01 indicating the **Restriction** field is present.</span></span>
    -   <span data-ttu-id="cbf24-4880">**El** campo de restricción es de tipo CRestriction y se establece en:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4880">**Restriction** field is of type CRestriction and is set to:</span></span>
        -   <span data-ttu-id="cbf24-4881">**\_ ulType** se establece en 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4881">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
        -   <span data-ttu-id="cbf24-4882">**\_ weight** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4882">**\_weight** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cbf24-4883">El resto del campo contiene una estructura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4883">The rest of the field contains a CContentRestriction structure:</span></span>
        -   <span data-ttu-id="cbf24-4884">**\_ La** propiedad se establece en GUID B725F130-47EF-101A-A5F1-02608c9eebac/0x00000001 (para PRSPEC PROPID) / 0x13 que representa el cuerpo \_ del documento.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4884">**\_Property** is set to GUID B725F130-47EF-101A-A5F1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13 which represents the document body.</span></span>
        -   <span data-ttu-id="cbf24-4885">**\_ Cc** se establece en 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4885">**\_Cc** is set to 0x00000009.</span></span>
        -   <span data-ttu-id="cbf24-4886">**\_ pwcsphrase** se establece en la cadena "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="cbf24-4886">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
        -   <span data-ttu-id="cbf24-4887">**\_ lcid** se establece en 0x409 (para inglés).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4887">**\_lcid** is set to 0x409 (for English).</span></span>
        -   <span data-ttu-id="cbf24-4888">**\_ ulGenerateMethod** se establece en 0x00000000 (coincidencia exacta).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4888">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>
    -   <span data-ttu-id="cbf24-4889">**CSortPresent** se establece en 0x00.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4889">**CSortPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="cbf24-4890">**CCategorizationSetPresent** se establece en 0x00.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4890">**CCategorizationSetPresent** is set to 0x00.</span></span>
    -   <span data-ttu-id="cbf24-4891">**RowSetProperties** se establece de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4891">**RowSetProperties** is set as follows:</span></span>
        -   <span data-ttu-id="cbf24-4892">**\_ uBooleanOptions** se establece en 0x00000001 (secuencial).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4892">**\_uBooleanOptions** is set to 0x00000001 (sequential).</span></span>
        -   <span data-ttu-id="cbf24-4893">**\_ ulMaxOpenRows** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4893">**\_ulMaxOpenRows** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="cbf24-4894">**\_ ulMemoryUsage** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4894">**\_ulMemoryUsage** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="cbf24-4895">\_**cMaxResults** se establece en 0x00000100 (devuelve como máximo 256 filas).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4895">\_**cMaxResults** is set to 0x00000100 (return at most 256 rows).</span></span>
        -   <span data-ttu-id="cbf24-4896">**\_ cCmdTimeOut se** establece en 0x00000000 (nunca tiempo de espera).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4896">**\_cCmdTimeOut** is set to 0x00000000 (never timeout).</span></span>
    -   <span data-ttu-id="cbf24-4897">**PidMapper** se establece en:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4897">**PidMapper** is set to:</span></span>
        -   <span data-ttu-id="cbf24-4898">**\_ count** se establece en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4898">**\_count** is set to 0x00000001.</span></span>
        -   <span data-ttu-id="cbf24-4899">**\_ aPropSpec** se establece en GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC/0x00000001 (para PRSPEC PROPID) / 0x0000000c que representa la propiedad de tamaño de archivo \_ de Windows.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4899">**\_aPropSpec** is set to GUID B725F130-47EF-101A-A5-F1-02608C9EEBAC / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>

6.  <span data-ttu-id="cbf24-4900">El servidor lo procesa y responde con un mensaje CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4900">The server processes it and responds with a CPMCreateQueryOut message.</span></span>

    <span data-ttu-id="cbf24-4901">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4901">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cbf24-4902">**\_ msg** se establece en 0x000000CA, lo que indica que se trata de un mensaje CPMCreateQueryOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4902">**\_msg** is set to 0x000000CA, indicating that this is a CPMCreateQueryOut message.</span></span>
    -   <span data-ttu-id="cbf24-4903">**\_ status** se establece en SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4903">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="cbf24-4904">**\_ ulChecksum** se establece en 0x00000000 (o cualquier otro valor arbitrario).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4904">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="cbf24-4905">**\_ ulReserved2** se establece en 0x00000000 (o cualquier otro valor arbitrario).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4905">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="cbf24-4906">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4906">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cbf24-4907">**\_ fTrueSeqeuntial** se establece en 0x00000000, lo que indica que la consulta puede usar un índice.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4907">**\_fTrueSeqeuntial** is set to 0x00000000, indicating that the query can use an index.</span></span>
    -   <span data-ttu-id="cbf24-4908">**\_ fWorkIdUnique** se establece en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4908">**\_fWorkIdUnique** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="cbf24-4909">La **matriz aCursors** contiene solo un elemento, que representa un identificador de cursor para esta consulta.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4909">The **aCursors** array contains only one element, representing a cursor handle to this query.</span></span> <span data-ttu-id="cbf24-4910">El valor depende del estado del servidor.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4910">The value depends on the state of the server.</span></span> <span data-ttu-id="cbf24-4911">Supongamos que el valor devuelto es 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4911">Let us assume that the returned value is 0xAAAAAAAA.</span></span>

7.  <span data-ttu-id="cbf24-4912">El cliente emite un mensaje de solicitud CPMSetBindingsIn para definir el formato de una fila.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4912">The client issues a CPMSetBindingsIn request message to define the format of a row.</span></span>

    <span data-ttu-id="cbf24-4913">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4913">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cbf24-4914">**\_ msg** se establece en 0x000000D0, lo que indica que se trata de un mensaje CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4914">**\_msg** is set to 0x000000D0, indicating that this is a CPMSetBindingsIn message.</span></span>
    -   <span data-ttu-id="cbf24-4915">**\_ status** se establece en SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4915">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="cbf24-4916">**\_ ulChecksum** se establece en 0x00000000 (o cualquier otro valor arbitrario).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4916">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="cbf24-4917">**\_ ulReserved2** se establece en 0x00000000 (o cualquier otro valor arbitrario).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4917">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

    <span data-ttu-id="cbf24-4918">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4918">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cbf24-4919">**\_ hCursor** se establece en 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4919">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="cbf24-4920">**\_ cbRow** se establece en 0x10 (lo suficientemente grande como para caber columnas).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4920">**\_cbRow** is set to 0x10 (big enough to fit columns).</span></span>
    -   <span data-ttu-id="cbf24-4921">**\_ cbBindingDesc** se establece en el tamaño de los campos **\_ cColumns** y **\_ aColumns** combinados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4921">**\_cbBindingDesc** is set to the size of the **\_cColumns** and **\_aColumns** fields combined.</span></span>
    -   <span data-ttu-id="cbf24-4922">**\_ cColumns** se establece en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4922">**\_cColumns** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="cbf24-4923">**\_ la matriz aColumns** está establecida para contener una estructura CTableColumn que contiene:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4923">**\_aColumns** array is set to contain one CTableColumn structure containing:</span></span>
    -   -   <span data-ttu-id="cbf24-4924">**\_ PropSpec** se establece en GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (para PRSPEC PROPID) / 0x0000000c que representa la propiedad de tamaño de archivo \_ de Windows.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4924">**\_PropSpec** is set to GUID b725f130-47ef-101a-a5-f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x0000000c which represents the Windows file size property.</span></span>
        -   <span data-ttu-id="cbf24-4925">**\_ vType** se establece en 0x0015 (VT \_ UI8).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4925">**\_vType** is set to 0x0015 (VT\_UI8).</span></span>
        -   <span data-ttu-id="cbf24-4926">**\_ ValueUsed** se establece en 0x01 (columna transferida en fila).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4926">**\_ValueUsed** is set to 0x01 (column transferred in row).</span></span>
        -   <span data-ttu-id="cbf24-4927">**\_ ValueOffset** se establece en 0x0002 (al principio de la fila).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4927">**\_ValueOffset** is set to 0x0002 (at beginning of row).</span></span>
        -   <span data-ttu-id="cbf24-4928">**\_ ValueSize** se establece en 0x08 (tamaño de una VT \_ UI8).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4928">**\_ValueSize** is set to 0x08 (size of a VT\_UI8).</span></span>
        -   <span data-ttu-id="cbf24-4929">**\_ StatusUsed** se establece en 0x01.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4929">**\_StatusUsed** is set to 0x01.</span></span>
        -   <span data-ttu-id="cbf24-4930">**\_ StatusOffset** se establece en 0x0A.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4930">**\_StatusOffset** is set to 0x0A.</span></span>
        -   <span data-ttu-id="cbf24-4931">**\_ LengthUsed** se establece en 0x00.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4931">**\_LengthUsed** is set to 0x00.</span></span>

8.  <span data-ttu-id="cbf24-4932">El servidor lo procesa y responde con un mensaje CPMSetBindingsIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4932">The server processes it and responds with a CPMSetBindingsIn message.</span></span>

    <span data-ttu-id="cbf24-4933">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4933">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cbf24-4934">**\_ msg** se establece en 0x000000D0.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4934">**\_msg** is set to 0x000000D0.</span></span>
    -   <span data-ttu-id="cbf24-4935">**\_ status** se establece en SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4935">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="cbf24-4936">**\_ ulChecksum** se establece en 0x00000000 (o cualquier otro valor arbitrario).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4936">**\_ulChecksum** is set to 0x00000000 (or any other arbitrary value).</span></span>
    -   <span data-ttu-id="cbf24-4937">**\_ ulReserved2** se establece en 0x00000000 (o cualquier otro valor arbitrario).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4937">**\_ulReserved2** is set to 0x00000000 (or any other arbitrary value).</span></span>

9.  <span data-ttu-id="cbf24-4938">El cliente emite un mensaje de solicitud CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4938">The client issues a CPMGetRowsIn request message.</span></span> <span data-ttu-id="cbf24-4939">Supongamos que el cliente está preparado para aceptar 100 filas en este momento y las quiere en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4939">Let us assume that the client is prepared to accept 100 rows at this point, and wants them in ascending order.</span></span>

    <span data-ttu-id="cbf24-4940">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4940">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cbf24-4941">**\_ msg** se establece en 0x000000CC, lo que indica que se trata de un mensaje CPMGetRowsIn.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4941">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsIn message.</span></span>
    -   <span data-ttu-id="cbf24-4942">**\_ status** se establece en 0x00000000</span><span class="sxs-lookup"><span data-stu-id="cbf24-4942">**\_status** is set to 0x00000000</span></span>
    -   <span data-ttu-id="cbf24-4943">**\_ ulChecksum contiene** la suma de comprobación, calculada según la sección 0.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4943">**\_ulChecksum** contains the checksum, computed according to Section 0.</span></span>
    -   <span data-ttu-id="cbf24-4944">**\_ ulReserved2** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4944">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="cbf24-4945">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4945">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cbf24-4946">**\_ hCursor** se establece en 0xAAAAAAAA.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4946">**\_hCursor** is set to 0xAAAAAAAA.</span></span>
    -   <span data-ttu-id="cbf24-4947">**\_ cRowsToTransfer** se establece en 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4947">**\_cRowsToTransfer** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="cbf24-4948">**\_ cRowWidth** se establece en 0x00000010 (desde enlaces).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4948">**\_cRowWidth** is set to 0x00000010 (from bindings).</span></span>
    -   <span data-ttu-id="cbf24-4949">**\_ cbSeek** se establece en 0x14 tamaño de los campos eType, chapt y \_ CRowSeekNext combinados.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4949">**\_cbSeek** is set to 0x14 which is the size of the eType, \_chapt and CRowSeekNext fields combined.</span></span>
    -   <span data-ttu-id="cbf24-4950">**\_ cbReserved** se establece en 0x18 (0x14 más \_ cbSeek).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4950">**\_cbReserved** is set to 0x18 (0x14 plus \_cbSeek).</span></span>
    -   <span data-ttu-id="cbf24-4951">**\_ cbReadBuffer** se establece en 0x800 (0x64 0x10 redondeada al siguiente \* múltiplo de 0x200).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4951">**\_cbReadBuffer** is set to 0x800 (0x64\*0x10 rounded up to the next multiple of 0x200).</span></span>
    -   <span data-ttu-id="cbf24-4952">**\_ ulClientBase** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4952">**\_ulClientBase** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cbf24-4953">**\_ fBwdfetch** se establece en 0x00000000 que indica que las filas se van a capturar en orden de avance.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4953">**\_fBwdfetch** is set to 0x00000000 indicating that the rows are to be fetched in forward order.</span></span>
    -   <span data-ttu-id="cbf24-4954">**eType** se establece en 0x0000001 que indica que el cliente quiere las siguientes filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4954">**eType** is set to 0x0000001 indicating that the client wants next rows.</span></span>
    -   <span data-ttu-id="cbf24-4955">**\_ chapt** se establece en 0 (no en un resultado con capítulos).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4955">**\_chapt** is set to 0 (not a chaptered result).</span></span>
    -   <span data-ttu-id="cbf24-4956">**SeekDescription** se establece en CRowSeekNext.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4956">**SeekDescription** is set to CRowSeekNext.</span></span> <span data-ttu-id="cbf24-4957">La estructura CRowSeekNext contiene los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4957">The CRowSeekNext structure contains the following values:</span></span>
        -   <span data-ttu-id="cbf24-4958">**CiTblChapt** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4958">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="cbf24-4959">**\_ hRegion** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4959">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="cbf24-4960">**\_ cSkip** se establece en 0, lo que indica que el cliente no quiere omitir filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4960">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>

10. <span data-ttu-id="cbf24-4961">El servidor lo procesa y responde con un mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4961">The server processes it and responds with a CPMGetRowsOut message.</span></span> <span data-ttu-id="cbf24-4962">Supongamos que el servidor encontró 100 documentos que contienen la palabra "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="cbf24-4962">Let us assume that the server found 100 documents that contain the word "Microsoft".</span></span>

    <span data-ttu-id="cbf24-4963">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4963">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cbf24-4964">**\_ msg** se establece en 0x000000CC, lo que indica que se trata de un mensaje CPMGetRowsOut.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4964">**\_msg** is set to 0x000000CC, indicating that this is a CPMGetRowsOut message.</span></span>
    -   <span data-ttu-id="cbf24-4965">**\_ status** se establece en SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4965">**\_status** is set to SUCCESS.</span></span>
    -   <span data-ttu-id="cbf24-4966">**\_ ulChecksum** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4966">**\_ulChecksum** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cbf24-4967">**\_ ulReserved2** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4967">**\_ulReserved2** is set to 0x00000000.</span></span>

    <span data-ttu-id="cbf24-4968">El cuerpo del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4968">The body of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cbf24-4969">**\_ CRowsReturned** se establece en 0x00000064.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4969">**\_CRowsReturned** is set to 0x00000064.</span></span>
    -   <span data-ttu-id="cbf24-4970">**eType** se establece en 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4970">**eType** is set to 0x00000001.</span></span>
    -   <span data-ttu-id="cbf24-4971">**\_ chapt** se establece en 0x00000000 (no en un resultado con capítulos).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4971">**\_chapt** is set to 0x00000000 (not a chaptered result).</span></span>
    -   <span data-ttu-id="cbf24-4972">**SeekDescription** contiene una estructura CRowSeekNext, rellenada de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4972">**SeekDescription** contains a CRowSeekNext structure, populated as follows:</span></span>
        -   <span data-ttu-id="cbf24-4973">**CiTblChapt** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4973">**CiTblChapt** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="cbf24-4974">**\_ hRegion** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4974">**\_hRegion** is set to 0x00000000.</span></span>
        -   <span data-ttu-id="cbf24-4975">**\_ cSkip** se establece en 0, lo que indica que el cliente no quiere omitir filas.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4975">**\_cSkip** is set to 0 indicating that the client does not want to skip rows.</span></span>
    -   <span data-ttu-id="cbf24-4976">**Las** filas contienen el tamaño de los 100 documentos que contienen la palabra "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="cbf24-4976">**Rows** contains the size of the 100 documents that contain the word "Microsoft".</span></span> <span data-ttu-id="cbf24-4977">Dado que se trata de datos de tamaño fijo, simplemente se estructura como una lista de 100 enteros de 8 bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4977">Since this is fixed-sized data, it is simply structured as a list of 100, 8-byte unsigned integers.</span></span>

11. <span data-ttu-id="cbf24-4978">El cliente envía un mensaje CPMDisconnect para finalizar la conexión.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4978">The client sends a CPMDisconnect message to end the connection.</span></span>

    <span data-ttu-id="cbf24-4979">El encabezado del mensaje se rellena de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4979">The header of the message is populated as follows:</span></span>

    -   <span data-ttu-id="cbf24-4980">**\_ msg** se establece en 0x000000C9, lo que indica que se trata de un mensaje CPMDisconnect.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4980">**\_msg** is set to 0x000000C9, indicating that this is a CPMDisconnect message.</span></span>
    -   <span data-ttu-id="cbf24-4981">**\_ status** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4981">**\_status** is set to 0x00000000.</span></span>
    -   <span data-ttu-id="cbf24-4982">**\_ ulChecksum** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4982">**\_ulChecksum** is set to 0x00000000.</span></span>

12. <span data-ttu-id="cbf24-4983">El servidor procesa el mensaje y quita todo el estado del cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4983">The server processes the message and removes all client state.</span></span>

### <a name="42-example-2"></a><span data-ttu-id="cbf24-4984">4.2 Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="cbf24-4984">4.2 Example 2</span></span>

<span data-ttu-id="cbf24-4985">En el ejemplo anterior, la consulta era bastante sencilla.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4985">In the previous example, the query was quite simple.</span></span> <span data-ttu-id="cbf24-4986">Ahora vamos a considerar una consulta ligeramente más compleja.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4986">Let us now consider a slightly more complex query.</span></span> <span data-ttu-id="cbf24-4987">Supongamos que el usuario quiere recuperar el tamaño de los documentos que contienen las siguientes palabras: "Microsoft" y "Office".</span><span class="sxs-lookup"><span data-stu-id="cbf24-4987">Let us assume that the user wants to retrieve the size of the documents that contain both the following words: "Microsoft" and "Office".</span></span> <span data-ttu-id="cbf24-4988">Esto se especifica cambiando el campo Restricción contenido en el mensaje CPMCreateQueryIn enviado en el paso 5 como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4988">This is specified by changing the Restriction field contained in the CPMCreateQueryIn message sent in step 5 as follows:</span></span>

<span data-ttu-id="cbf24-4989">El **campo** Restricción es de tipo CRestriction y se establece en:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4989">The **Restriction** field is of type CRestriction and is set to:</span></span>

-   -   <span data-ttu-id="cbf24-4990">**\_ ulType** se establece en 0x00000004 (RTAnd).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4990">**\_ulType** is set to 0x00000004 (RTAnd).</span></span>
    -   <span data-ttu-id="cbf24-4991">**\_ weight** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4991">**\_weight** is set to 0x00000000.</span></span>

<span data-ttu-id="cbf24-4992">El resto del campo contiene una estructura CNodeRestriction:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4992">The rest of the field contains a CNodeRestriction structure:</span></span>

-   -   <span data-ttu-id="cbf24-4993">**\_ cNode** se establece en 0x00000002, lo que indica que hay dos nodos en la matriz paNode.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4993">**\_cNode** is set to 0x00000002, indicating that there are two nodes in the paNode array.</span></span>
    -   <span data-ttu-id="cbf24-4994">El **\_ campo paNode** es una matriz de dos estructuras de CRestriction.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4994">The **\_paNode** field is an array of two CRestriction structures.</span></span>

        <span data-ttu-id="cbf24-4995">**\_ paNode \[ \] 0** contiene:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4995">**\_paNode\[0\]** contains:</span></span>

        -   -   <span data-ttu-id="cbf24-4996">**\_ ulType** se establece en 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="cbf24-4996">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="cbf24-4997">**\_ weight** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4997">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cbf24-4998">El resto del campo contiene una estructura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="cbf24-4998">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="cbf24-4999">**\_ La** propiedad se establece en GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (para PRSPEC \_ PROPID) / 0x13.</span><span class="sxs-lookup"><span data-stu-id="cbf24-4999">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="cbf24-5000">**\_ Cc** se establece en 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="cbf24-5000">**\_Cc** is set to 0x00000009.</span></span>
                -   <span data-ttu-id="cbf24-5001">**\_ pwcsphrase** se establece en la cadena "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="cbf24-5001">**\_pwcsphrase** is set to the string "Microsoft".</span></span>
                -   <span data-ttu-id="cbf24-5002">**\_ lcid** se establece en 0x409 (para inglés).</span><span class="sxs-lookup"><span data-stu-id="cbf24-5002">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="cbf24-5003">**\_ ulGenerateMethod** se establece en 0x00000000 (coincidencia exacta).</span><span class="sxs-lookup"><span data-stu-id="cbf24-5003">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

        <span data-ttu-id="cbf24-5004">**\_ paNode \[ \] 1** contiene:</span><span class="sxs-lookup"><span data-stu-id="cbf24-5004">**\_paNode\[1\]** contains:</span></span>

        -   -   <span data-ttu-id="cbf24-5005">**\_ ulType** se establece en 0x00000004 (RTContent).</span><span class="sxs-lookup"><span data-stu-id="cbf24-5005">**\_ulType** is set to 0x00000004 (RTContent).</span></span>
            -   <span data-ttu-id="cbf24-5006">**\_ weight** se establece en 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cbf24-5006">**\_weight** is set to 0x00000000.</span></span>
            -   <span data-ttu-id="cbf24-5007">El resto del campo contiene una estructura CContentRestriction:</span><span class="sxs-lookup"><span data-stu-id="cbf24-5007">The rest of the field contains a CContentRestriction structure:</span></span>
                -   <span data-ttu-id="cbf24-5008">**\_ La** propiedad se establece en GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (para PRSPEC \_ PROPID) / 0x13.</span><span class="sxs-lookup"><span data-stu-id="cbf24-5008">**\_Property** is set to GUID b725f130-47ef-101a-a5f1-02608c9eebac / 0x00000001 (for PRSPEC\_PROPID) / 0x13.</span></span>
                -   <span data-ttu-id="cbf24-5009">**\_ Cc** se establece en 0x00000006.</span><span class="sxs-lookup"><span data-stu-id="cbf24-5009">**\_Cc** is set to 0x00000006.</span></span>
                -   <span data-ttu-id="cbf24-5010">**\_ pwcsphrase** se establece en la cadena "Office".</span><span class="sxs-lookup"><span data-stu-id="cbf24-5010">**\_pwcsphrase** is set to the string "Office".</span></span>
                -   <span data-ttu-id="cbf24-5011">**\_ lcid** se establece en 0x409 (para inglés).</span><span class="sxs-lookup"><span data-stu-id="cbf24-5011">**\_lcid** is set to 0x409 (for English).</span></span>
                -   <span data-ttu-id="cbf24-5012">**\_ ulGenerateMethod** se establece en 0x00000000 (coincidencia exacta).</span><span class="sxs-lookup"><span data-stu-id="cbf24-5012">**\_ulGenerateMethod** is set to 0x00000000 (exact match).</span></span>

## <a name="5-security"></a><span data-ttu-id="cbf24-5013">5 Seguridad</span><span class="sxs-lookup"><span data-stu-id="cbf24-5013">5 Security</span></span>

### <a name="51-security-considerations-for-implementers"></a><span data-ttu-id="cbf24-5014">5.1 Consideraciones de seguridad para los implementadores</span><span class="sxs-lookup"><span data-stu-id="cbf24-5014">5.1 Security Considerations for Implementers</span></span>

<span data-ttu-id="cbf24-5015">Las implementaciones de indexación que indexa el contenido seguro deben considerar la posibilidad de usar el contexto de usuario proporcionado por SMB MS-SMB para recortar los resultados de la búsqueda y devolver solo los accesibles para \[ el autor de la \] llamada.</span><span class="sxs-lookup"><span data-stu-id="cbf24-5015">Indexing implementations which index secure content should consider using the user context provided by SMB \[MS-SMB\] to trim search results and return only those accessible to the caller.</span></span>

### <a name="52-index-of-security-parameters"></a><span data-ttu-id="cbf24-5016">5.2 Índice de parámetros de seguridad</span><span class="sxs-lookup"><span data-stu-id="cbf24-5016">5.2 Index of Security Parameters</span></span>



| <span data-ttu-id="cbf24-5017">Parámetro de seguridad</span><span class="sxs-lookup"><span data-stu-id="cbf24-5017">Security Parameter</span></span>  | <span data-ttu-id="cbf24-5018">Sección</span><span class="sxs-lookup"><span data-stu-id="cbf24-5018">Section</span></span> |
|---------------------|---------|
| <span data-ttu-id="cbf24-5019">Nivel de suplantación</span><span class="sxs-lookup"><span data-stu-id="cbf24-5019">Impersonation level</span></span> | <span data-ttu-id="cbf24-5020">2.1</span><span class="sxs-lookup"><span data-stu-id="cbf24-5020">2.1</span></span>     |



 

## <a name="6-index-of-version-specific-behavior"></a><span data-ttu-id="cbf24-5021">6 Índice del comportamiento específico de la versión</span><span class="sxs-lookup"><span data-stu-id="cbf24-5021">6 Index of Version Specific Behavior</span></span>



| <span data-ttu-id="cbf24-5022">Comportamiento específico de la versión</span><span class="sxs-lookup"><span data-stu-id="cbf24-5022">Version Specific Behavior</span></span>                                                                         | <span data-ttu-id="cbf24-5023">Sección</span><span class="sxs-lookup"><span data-stu-id="cbf24-5023">Section</span></span>   | <span data-ttu-id="cbf24-5024">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cbf24-5024">Windows 2000</span></span> | <span data-ttu-id="cbf24-5025">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cbf24-5025">Windows XP</span></span> | <span data-ttu-id="cbf24-5026">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cbf24-5026">Windows Server 2003</span></span> |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| <span data-ttu-id="cbf24-5027">Este protocolo se implementa en Windows 2000, Windows XP, Windows Server 2003 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cbf24-5027">This protocol is implemented on Windows 2000, Windows XP, Windows Server 2003, and Windows Vista.</span></span> | <span data-ttu-id="cbf24-5028">1.3.2</span><span class="sxs-lookup"><span data-stu-id="cbf24-5028">1.3.2</span></span>     | <span data-ttu-id="cbf24-5029">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5029">X</span></span>            | <span data-ttu-id="cbf24-5030">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5030">X</span></span>          | <span data-ttu-id="cbf24-5031">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5031">X</span></span>                   |
| <span data-ttu-id="cbf24-5032">Las aplicaciones normalmente interactúan con un contenedor OLE DB interfaz</span><span class="sxs-lookup"><span data-stu-id="cbf24-5032">Applications typically interact with an OLE DB interface wrapper</span></span>                                  | <span data-ttu-id="cbf24-5033">1.4</span><span class="sxs-lookup"><span data-stu-id="cbf24-5033">1.4</span></span>       | <span data-ttu-id="cbf24-5034">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5034">X</span></span>            | <span data-ttu-id="cbf24-5035">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5035">X</span></span>          | <span data-ttu-id="cbf24-5036">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5036">X</span></span>                   |
| <span data-ttu-id="cbf24-5037">Valores NTSTATUS</span><span class="sxs-lookup"><span data-stu-id="cbf24-5037">NTSTATUS values</span></span>                                                                                   | <span data-ttu-id="cbf24-5038">1.8</span><span class="sxs-lookup"><span data-stu-id="cbf24-5038">1.8</span></span>       | <span data-ttu-id="cbf24-5039">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5039">X</span></span>            | <span data-ttu-id="cbf24-5040">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5040">X</span></span>          | <span data-ttu-id="cbf24-5041">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5041">X</span></span>                   |
| <span data-ttu-id="cbf24-5042">El cliente establece el campo \_ de estado en cada encabezado de mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbf24-5042">The client sets the \_status field in each Message Header.</span></span>                                        | <span data-ttu-id="cbf24-5043">2.2.2</span><span class="sxs-lookup"><span data-stu-id="cbf24-5043">2.2.2</span></span>     | <span data-ttu-id="cbf24-5044">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5044">X</span></span>            | <span data-ttu-id="cbf24-5045">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5045">X</span></span>          | <span data-ttu-id="cbf24-5046">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5046">X</span></span>                   |
| <span data-ttu-id="cbf24-5047">El valor de cPendingScans suele ser cero.</span><span class="sxs-lookup"><span data-stu-id="cbf24-5047">cPendingScans value is usually zero</span></span>                                                               | <span data-ttu-id="cbf24-5048">2.2.3.1</span><span class="sxs-lookup"><span data-stu-id="cbf24-5048">2.2.3.1</span></span>   | <span data-ttu-id="cbf24-5049">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5049">X</span></span>            | <span data-ttu-id="cbf24-5050">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5050">X</span></span>          | <span data-ttu-id="cbf24-5051">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5051">X</span></span>                   |
| <span data-ttu-id="cbf24-5052">Valor de iClientVersion</span><span class="sxs-lookup"><span data-stu-id="cbf24-5052">iClientVersion value</span></span>                                                                              | <span data-ttu-id="cbf24-5053">2.2.3.6</span><span class="sxs-lookup"><span data-stu-id="cbf24-5053">2.2.3.6</span></span>   | <span data-ttu-id="cbf24-5054">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5054">X</span></span>            | <span data-ttu-id="cbf24-5055">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5055">X</span></span>          | <span data-ttu-id="cbf24-5056">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5056">X</span></span>                   |
| <span data-ttu-id="cbf24-5057">\_cbChunk value</span><span class="sxs-lookup"><span data-stu-id="cbf24-5057">\_cbChunk value</span></span>                                                                                   | <span data-ttu-id="cbf24-5058">2.2.3.19</span><span class="sxs-lookup"><span data-stu-id="cbf24-5058">2.2.3.19</span></span>  | <span data-ttu-id="cbf24-5059">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5059">X</span></span>            | <span data-ttu-id="cbf24-5060">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5060">X</span></span>          | <span data-ttu-id="cbf24-5061">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5061">X</span></span>                   |
| <span data-ttu-id="cbf24-5062">Direcciones de memoria de 32 y 64 bits</span><span class="sxs-lookup"><span data-stu-id="cbf24-5062">32-bit and 64-bit memory addresses</span></span>                                                                | <span data-ttu-id="cbf24-5063">3.2.4.2.4</span><span class="sxs-lookup"><span data-stu-id="cbf24-5063">3.2.4.2.4</span></span> | <span data-ttu-id="cbf24-5064">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5064">X</span></span>            | <span data-ttu-id="cbf24-5065">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5065">X</span></span>          | <span data-ttu-id="cbf24-5066">X</span><span class="sxs-lookup"><span data-stu-id="cbf24-5066">X</span></span>                   |



 

 

 





