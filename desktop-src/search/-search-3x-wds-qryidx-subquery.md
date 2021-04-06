---
description: Una subconsulta es un archivo de búsqueda guardado ( \* . Search-MS) que puede usar como filtro para una nueva consulta.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Argumento de subconsulta (búsqueda de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f673cf9c2a9867593fd6c8fdac83b5901f531257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000999"
---
# <a name="subquery-argument-windows-search"></a><span data-ttu-id="54216-103">Argumento de subconsulta (búsqueda de Windows)</span><span class="sxs-lookup"><span data-stu-id="54216-103">SUBQUERY Argument (Windows Search)</span></span>

<span data-ttu-id="54216-104">Una subconsulta es un archivo de búsqueda guardado ( \* . Search-MS) que puede usar como filtro para una nueva consulta.</span><span class="sxs-lookup"><span data-stu-id="54216-104">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="54216-105">Los resultados de la subconsulta se usan como origen de la nueva consulta.</span><span class="sxs-lookup"><span data-stu-id="54216-105">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="54216-106">Por ejemplo, supongamos que tiene varios archivos de búsqueda guardados que restringen una consulta por lista de distribución de correo electrónico: Departamento. Search-MS, teamproject. Search-MS y corporatewide. Search-ms.</span><span class="sxs-lookup"><span data-stu-id="54216-106">For example, let's say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="54216-107">El uso del `subquery` argumento le permite limitar las búsquedas de correo electrónico a cualquiera de estas búsquedas guardadas.</span><span class="sxs-lookup"><span data-stu-id="54216-107">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

<span data-ttu-id="54216-108">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="54216-108">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="54216-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="54216-109">Example</span></span>](#example)
-   [<span data-ttu-id="54216-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="54216-110">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="54216-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="54216-111">Example</span></span>


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a><span data-ttu-id="54216-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="54216-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54216-113">Introducción con argumentos de Parameter-Value</span><span class="sxs-lookup"><span data-stu-id="54216-113">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="54216-114">Argumentos de identificador de configuración regional</span><span class="sxs-lookup"><span data-stu-id="54216-114">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="54216-115">Argumento de MIGAs de</span><span class="sxs-lookup"><span data-stu-id="54216-115">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="54216-116">Argumento de sintaxis</span><span class="sxs-lookup"><span data-stu-id="54216-116">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="54216-117">Argumento STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="54216-117">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 



