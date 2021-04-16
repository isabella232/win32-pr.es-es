---
description: Después de la instrucción SELECT, use la cláusula FROM para especificar dónde buscar documentos coincidentes.
ms.assetid: 437d36d1-dd6d-4405-8f35-c37fd04fa0f6
title: Cláusula FROM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37100a614ca7cc08cdf510f27e42b045acc1ec23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686622"
---
# <a name="from-clause"></a><span data-ttu-id="ad23f-103">Cláusula FROM</span><span class="sxs-lookup"><span data-stu-id="ad23f-103">FROM Clause</span></span>

<span data-ttu-id="ad23f-104">Después de la instrucción SELECT, use la cláusula FROM para especificar dónde buscar documentos coincidentes.</span><span class="sxs-lookup"><span data-stu-id="ad23f-104">Following the SELECT statement, you use the FROM clause to specify where to search for matching documents.</span></span> <span data-ttu-id="ad23f-105">La siguiente es la sintaxis de la cláusula FROM para una consulta local:</span><span class="sxs-lookup"><span data-stu-id="ad23f-105">The following is the syntax of the FROM clause for a local query:</span></span>


```
FROM [<ComputerName>.]SystemIndex
```



<span data-ttu-id="ad23f-106">Actualmente, Windows Search solo admite un catálogo, SystemIndex.</span><span class="sxs-lookup"><span data-stu-id="ad23f-106">Currently, Windows Search supports only one catalog, SystemIndex.</span></span> <span data-ttu-id="ad23f-107">Para consultar el catálogo local de un equipo remoto, incluya el nombre del equipo delante del catálogo y una ruta de acceso UNC (Convención de nomenclatura universal) en el equipo remoto en la cláusula SCOPE o DIRECTORY.</span><span class="sxs-lookup"><span data-stu-id="ad23f-107">To query the local catalog of a remote computer, include the computer name before the catalog and a Universal Naming Convention (UNC) path on the remote computer in the SCOPE or DIRECTORY clause.</span></span>

<span data-ttu-id="ad23f-108">Especifique un ámbito como restricción en la cláusula WHERE, tal como se describe en el tema [ámbito y predicados de directorio](-search-sql-folderdepth.md) .</span><span class="sxs-lookup"><span data-stu-id="ad23f-108">You specify a scope as a restriction in the WHERE clause, as described in the [SCOPE and DIRECTORY Predicates](-search-sql-folderdepth.md) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="ad23f-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ad23f-109">Examples</span></span>


```
SELECT System.ItemName,System.ItemUrl
FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM zarascomputer.SystemIndex WHERE SCOPE='file://zarascomputer/SomeFolder' AND CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM server.SystemIndex WHERE SCOPE='file://server/users' AND CONTAINS('Microsoft')
```



<span data-ttu-id="ad23f-110">En el segundo de los ejemplos anteriores, la consulta se dirige a un equipo remoto llamado "zarascomputer".</span><span class="sxs-lookup"><span data-stu-id="ad23f-110">In the second of the preceding examples, the query targets a remote computer called "zarascomputer".</span></span> <span data-ttu-id="ad23f-111">Tenga en cuenta que este nombre de equipo aparece en las cláusulas FROM y SCOPE.</span><span class="sxs-lookup"><span data-stu-id="ad23f-111">Notice that this computer name appears in both the FROM and SCOPE clauses.</span></span> <span data-ttu-id="ad23f-112">En el tercer ejemplo, la consulta tiene como destino un nombre de recurso compartido "usuarios" en un servidor denominado "Server" (donde la ruta de acceso UNC sería \\ \\ usuarios del servidor \\ ).</span><span class="sxs-lookup"><span data-stu-id="ad23f-112">In the third example, the query targets a share name "users" on a server named "server" (where the UNC path would be \\\\server\\users).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad23f-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad23f-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ad23f-114">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ad23f-114">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ad23f-115">Información general de la sintaxis de búsqueda de SQL</span><span class="sxs-lookup"><span data-stu-id="ad23f-115">Overview of the Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[<span data-ttu-id="ad23f-116">Instrucción SELECT</span><span class="sxs-lookup"><span data-stu-id="ad23f-116">SELECT Statement</span></span>](-search-sql-select.md)
</dt> <dt>

[<span data-ttu-id="ad23f-117">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="ad23f-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

[<span data-ttu-id="ad23f-118">Predicados de ámbito y directorio</span><span class="sxs-lookup"><span data-stu-id="ad23f-118">SCOPE and DIRECTORY Predicates</span></span>](-search-sql-folderdepth.md)
</dt> </dl>

 

 



