---
description: Windows Search proporciona características de búsqueda y rastreo de contenido que admiten la búsqueda de texto completo. El lenguaje de consulta que usa Windows Search amplía la sintaxis de consulta de base de datos SQL-92 y SQL-99 para mejorar su utilidad con las búsquedas basadas en texto.
ms.assetid: a2eb550a-bb55-4dbd-9ca1-60b776eb9339
title: Consultar el índice con la sintaxis SQL de Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5696891b14340e8d8fe97f0c0cfbdc75db08e464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497062"
---
# <a name="querying-the-index-with-windows-search-sql-syntax"></a><span data-ttu-id="a33a6-104">Consultar el índice con la sintaxis SQL de Windows Search</span><span class="sxs-lookup"><span data-stu-id="a33a6-104">Querying the Index with Windows Search SQL Syntax</span></span>

<span data-ttu-id="a33a6-105">Windows Search proporciona características de búsqueda y rastreo de contenido que admiten la búsqueda de texto completo.</span><span class="sxs-lookup"><span data-stu-id="a33a6-105">Windows Search provides content crawling and search features that support full-text searching.</span></span> <span data-ttu-id="a33a6-106">El lenguaje de consulta que usa Windows Search amplía la sintaxis de consulta de base de datos SQL-92 y SQL-99 para mejorar su utilidad con las búsquedas basadas en texto.</span><span class="sxs-lookup"><span data-stu-id="a33a6-106">The query language used by Windows Search extends the standard SQL-92 and SQL-99 database query syntax to enhance its usefulness with text-based searches.</span></span>

<span data-ttu-id="a33a6-107">Todas las características de Windows Search Lenguaje de consulta estructurado (SQL) son compatibles con Windows Search en Windows Vista y versiones posteriores, incluidas todas las versiones de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a33a6-107">All features of Windows Search Structured Query Language (SQL) are compatible with Windows Search on Windows Vista, and later, including all versions of Windows 10.</span></span>

<span data-ttu-id="a33a6-108">En esta sección se proporciona información general sobre la sintaxis de SQL en Windows Search e incluye los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="a33a6-108">This section provides an overview of SQL syntax in Windows Search, and includes the following topics:</span></span>

- [<span data-ttu-id="a33a6-109">Información general sobre la sintaxis SQL de búsqueda de Windows</span><span class="sxs-lookup"><span data-stu-id="a33a6-109">Overview of Windows Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
- [<span data-ttu-id="a33a6-110">Información general del lenguaje de consulta</span><span class="sxs-lookup"><span data-stu-id="a33a6-110">General Query Language Information</span></span>](-search-sql-generalqueryinfo.md)
- [<span data-ttu-id="a33a6-111">AGRUPAR POR... MÁS de... Privacidad</span><span class="sxs-lookup"><span data-stu-id="a33a6-111">GROUP ON ... OVER... Statement</span></span>](-search-sql-group-on-over.md)
- [<span data-ttu-id="a33a6-112">Instrucción SELECT</span><span class="sxs-lookup"><span data-stu-id="a33a6-112">SELECT Statement</span></span>](-search-sql-select.md)
- [<span data-ttu-id="a33a6-113">Cláusula FROM</span><span class="sxs-lookup"><span data-stu-id="a33a6-113">FROM Clause</span></span>](-search-sql-from.md)
- [<span data-ttu-id="a33a6-114">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="a33a6-114">WHERE Clause</span></span>](-search-sql-where.md)
- [<span data-ttu-id="a33a6-115">Cláusula ORDER BY</span><span class="sxs-lookup"><span data-stu-id="a33a6-115">ORDER BY Clause</span></span>](-search-sql-orderby.md)
- [<span data-ttu-id="a33a6-116">RANK BY (cláusula)</span><span class="sxs-lookup"><span data-stu-id="a33a6-116">RANK BY Clause</span></span>](-search-sql-rankby.md)
- [<span data-ttu-id="a33a6-117">SET (instrucción)</span><span class="sxs-lookup"><span data-stu-id="a33a6-117">SET Statement</span></span>](-search-sql-set.md)
- [<span data-ttu-id="a33a6-118">Propiedades del conjunto de filas</span><span class="sxs-lookup"><span data-stu-id="a33a6-118">Rowset Properties</span></span>](-search-sql-rowset-properties.md)

<span data-ttu-id="a33a6-119">En esta documentación se supone que está familiarizado con la vinculación de objetos y la incrustación de base de datos (OLE DB) y SQL.</span><span class="sxs-lookup"><span data-stu-id="a33a6-119">This documentation assumes familiarity with Object Linking and Embedding Database (OLE DB), and SQL.</span></span>

## <a name="code-samples"></a><span data-ttu-id="a33a6-120">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="a33a6-120">Code samples</span></span>

<span data-ttu-id="a33a6-121">En el ejemplo de código WSSQL se muestra cómo comunicarse entre Microsoft OLE DB y Windows Search a través de SQL.</span><span class="sxs-lookup"><span data-stu-id="a33a6-121">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through SQL.</span></span> <span data-ttu-id="a33a6-122">En el ejemplo de código WSOleDB se muestra Active Template Library (ATL) OLE DB el acceso a las aplicaciones de Windows Search y dos métodos adicionales para recuperar los resultados de la búsqueda de Windows.</span><span class="sxs-lookup"><span data-stu-id="a33a6-122">The WSOleDB code sample illustrates Active Template Library (ATL) OLE DB access to Windows Search applications, and two additional methods for retrieving results from Windows Search.</span></span> <span data-ttu-id="a33a6-123">Ambos ejemplos están disponibles en los [ejemplos de Windows Search](-search-samples-ovw.md) y en el [SDK de Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span><span class="sxs-lookup"><span data-stu-id="a33a6-123">Both samples are available in the [Windows Search Samples](-search-samples-ovw.md) and the [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span></span>

## <a name="related-topics"></a><span data-ttu-id="a33a6-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a33a6-124">Related topics</span></span>

[<span data-ttu-id="a33a6-125">Consulta del índice mediante programación</span><span class="sxs-lookup"><span data-stu-id="a33a6-125">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)

[<span data-ttu-id="a33a6-126">Uso de enfoques de SQL y AQS para consultar el índice</span><span class="sxs-lookup"><span data-stu-id="a33a6-126">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)

[<span data-ttu-id="a33a6-127">Consultar el índice con ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="a33a6-127">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)

[<span data-ttu-id="a33a6-128">Consultar el índice con el protocolo Search-MS</span><span class="sxs-lookup"><span data-stu-id="a33a6-128">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)

[<span data-ttu-id="a33a6-129">Consultar el índice con la sintaxis SQL de Windows Search</span><span class="sxs-lookup"><span data-stu-id="a33a6-129">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)

[<span data-ttu-id="a33a6-130">Usar la sintaxis de consulta avanzada mediante programación</span><span class="sxs-lookup"><span data-stu-id="a33a6-130">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
