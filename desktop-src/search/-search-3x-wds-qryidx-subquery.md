---
description: Obtenga información sobre el argumento SUBQUERY en Windows Search. Una subconsulta es un archivo de búsqueda guardado que puede usar como filtro para una nueva consulta.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Argumento SUBQUERY (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b23028d0bddcc674714f51f8b31883052431bd
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011038"
---
# <a name="subquery-argument-windows-search"></a><span data-ttu-id="74015-104">Argumento SUBQUERY (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="74015-104">SUBQUERY Argument (Windows Search)</span></span>

<span data-ttu-id="74015-105">Una subconsulta es un archivo de búsqueda guardado (.search-ms) que puede usar como \* filtro para una nueva consulta.</span><span class="sxs-lookup"><span data-stu-id="74015-105">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="74015-106">Los resultados de la subconsulta se usan como origen de la nueva consulta.</span><span class="sxs-lookup"><span data-stu-id="74015-106">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="74015-107">Por ejemplo, supongamos que tiene varios archivos de búsqueda guardados que restringen una consulta por lista de distribución de correo electrónico: mydepartment.search-ms, teamproject.search-ms y corporatewide.search-ms.</span><span class="sxs-lookup"><span data-stu-id="74015-107">For example, let's say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="74015-108">El uso `subquery` del argumento permite limitar las búsquedas de correo electrónico a cualquiera de estas búsquedas guardadas o a todas ellas.</span><span class="sxs-lookup"><span data-stu-id="74015-108">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

<span data-ttu-id="74015-109">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="74015-109">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="74015-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="74015-110">Example</span></span>](#example)
-   [<span data-ttu-id="74015-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74015-111">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="74015-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="74015-112">Example</span></span>


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a><span data-ttu-id="74015-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74015-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74015-114">Tareas iniciales con Parameter-Value argumentos</span><span class="sxs-lookup"><span data-stu-id="74015-114">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="74015-115">Argumentos del identificador de configuración regional</span><span class="sxs-lookup"><span data-stu-id="74015-115">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="74015-116">Argumento CRUMB</span><span class="sxs-lookup"><span data-stu-id="74015-116">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="74015-117">Argumento SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74015-117">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="74015-118">Argumento STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="74015-118">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 



