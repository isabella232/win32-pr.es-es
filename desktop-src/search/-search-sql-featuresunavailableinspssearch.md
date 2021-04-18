---
description: El lenguaje de consulta de Microsoft Windows Search se basa en Lenguaje de consulta estructurado (SQL); sin embargo, no busca en una base de datos relacional con tablas o índices definidos por el usuario.
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: Características de SQL no disponibles en Microsoft Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cf0e082a10a7775ca2d880be6153b7d99b6bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715003"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a><span data-ttu-id="e3930-103">Características de SQL no disponibles en Microsoft Search</span><span class="sxs-lookup"><span data-stu-id="e3930-103">SQL Features Unavailable in Microsoft Windows Search</span></span>

<span data-ttu-id="e3930-104">El lenguaje de consulta de Microsoft Windows Search se basa en Lenguaje de consulta estructurado (SQL); sin embargo, no busca en una base de datos relacional con tablas o índices definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="e3930-104">Microsoft Windows Search query language is based on Structured Query Language (SQL); however, it does not search in a relational database with user-defined tables or indexes.</span></span> <span data-ttu-id="e3930-105">Por este motivo, no se aplican muchas de las instrucciones SQL estándar y las características de sintaxis.</span><span class="sxs-lookup"><span data-stu-id="e3930-105">Because of this, many standard SQL statements and syntax features do not apply.</span></span> <span data-ttu-id="e3930-106">A continuación se muestra una lista de las características de SQL más importantes que no se admiten en Windows Search.</span><span class="sxs-lookup"><span data-stu-id="e3930-106">The following is a list of the more significant SQL features that are not supported in Windows Search.</span></span>


-   <span data-ttu-id="e3930-107">Instrucciones por lotes</span><span class="sxs-lookup"><span data-stu-id="e3930-107">BATCH statements</span></span>
-   <span data-ttu-id="e3930-108">Coalesce ( \_ función de tabla)</span><span class="sxs-lookup"><span data-stu-id="e3930-108">COALESCE\_TABLE function</span></span>
-   <span data-ttu-id="e3930-109">CONVERT (función) (usar en su lugar las funciones de conversión)</span><span class="sxs-lookup"><span data-stu-id="e3930-109">CONVERT function (use the CAST functions instead)</span></span>
-   <span data-ttu-id="e3930-110">CREATE VIEW, instrucción</span><span class="sxs-lookup"><span data-stu-id="e3930-110">CREATE VIEW statement</span></span>
-   <span data-ttu-id="e3930-111">Lenguaje de definición de datos</span><span class="sxs-lookup"><span data-stu-id="e3930-111">Data definition language</span></span>
-   <span data-ttu-id="e3930-112">DATASOURCE (instrucción)</span><span class="sxs-lookup"><span data-stu-id="e3930-112">DATASOURCE statement</span></span>
-   <span data-ttu-id="e3930-113">Formatos de fecha y hora distintos de la marca de fecha y hora ISO</span><span class="sxs-lookup"><span data-stu-id="e3930-113">Date and Time formats other than ISO date and time stamp</span></span>
-   <span data-ttu-id="e3930-114">Instrucción DELETE</span><span class="sxs-lookup"><span data-stu-id="e3930-114">DELETE statement</span></span>
-   <span data-ttu-id="e3930-115">GRANT, instrucción</span><span class="sxs-lookup"><span data-stu-id="e3930-115">GRANT statement</span></span>
-   <span data-ttu-id="e3930-116">Esquema de información</span><span class="sxs-lookup"><span data-stu-id="e3930-116">Information schema</span></span>
-   <span data-ttu-id="e3930-117">Instrucción INSERT</span><span class="sxs-lookup"><span data-stu-id="e3930-117">INSERT statement</span></span>
-   <span data-ttu-id="e3930-118">OLE DB tipos de datos</span><span class="sxs-lookup"><span data-stu-id="e3930-118">OLE DB data types</span></span>
-   <span data-ttu-id="e3930-119">Expresiones regulares de SQL estándar (use Contains o LIKE en su lugar)</span><span class="sxs-lookup"><span data-stu-id="e3930-119">SQL-standard regular expressions (use CONTAINS or LIKE instead)</span></span>
-   <span data-ttu-id="e3930-120">Parámetros para consultas SQL</span><span class="sxs-lookup"><span data-stu-id="e3930-120">Parameters to SQL queries</span></span>
-   <span data-ttu-id="e3930-121">Comparación de columnas relacionales</span><span class="sxs-lookup"><span data-stu-id="e3930-121">Relational column comparison</span></span>
-   <span data-ttu-id="e3930-122">Encabezado de ID. de revisión</span><span class="sxs-lookup"><span data-stu-id="e3930-122">Revision ID header</span></span>
-   <span data-ttu-id="e3930-123">REVOKE, instrucción</span><span class="sxs-lookup"><span data-stu-id="e3930-123">REVOKE statement</span></span>
-   <span data-ttu-id="e3930-124">Alias de ámbito o números de revisión</span><span class="sxs-lookup"><span data-stu-id="e3930-124">SCOPE aliases or revision numbers</span></span>
-   <span data-ttu-id="e3930-125">SELECCIONAR todo (quita los duplicados automáticamente)</span><span class="sxs-lookup"><span data-stu-id="e3930-125">SELECT ALL (removes duplicates automatically)</span></span>
-   <span data-ttu-id="e3930-126">Procedimientos almacenados</span><span class="sxs-lookup"><span data-stu-id="e3930-126">Stored procedures</span></span>
-   <span data-ttu-id="e3930-127">Expansión de documentos estructurados</span><span class="sxs-lookup"><span data-stu-id="e3930-127">Structured document expansion</span></span>
-   <span data-ttu-id="e3930-128">UNION ALL</span><span class="sxs-lookup"><span data-stu-id="e3930-128">UNION ALL</span></span>
-   <span data-ttu-id="e3930-129">Palabra clave UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="e3930-129">UNKNOWN keyword</span></span>
-   <span data-ttu-id="e3930-130">Instrucción UPDATE</span><span class="sxs-lookup"><span data-stu-id="e3930-130">UPDATE statement</span></span>

<span data-ttu-id="e3930-131">Windows Search no admite palabras irrelevantes y de sinónimos.</span><span class="sxs-lookup"><span data-stu-id="e3930-131">Windows Search does not support Thesaurus and Noise Words.</span></span>

 

 



