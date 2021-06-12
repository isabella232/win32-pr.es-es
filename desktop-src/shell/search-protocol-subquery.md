---
description: Obtenga información sobre el argumento SUBQUERY en el Shell de Windows. Una subconsulta es un archivo de búsqueda guardado que puede usar como filtro para una nueva consulta.
title: Argumento SUBQUERY (Shell de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ef0b37c0f473f2b86c85c18a99124be3b366f447
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010668"
---
# <a name="subquery-argument-the-windows-shell"></a><span data-ttu-id="7a7f2-104">Argumento SUBQUERY (Shell de Windows)</span><span class="sxs-lookup"><span data-stu-id="7a7f2-104">SUBQUERY Argument (The Windows Shell)</span></span>

<span data-ttu-id="7a7f2-105">Una subconsulta es un archivo de búsqueda guardado (.search-ms) que puede usar como \* filtro para una nueva consulta.</span><span class="sxs-lookup"><span data-stu-id="7a7f2-105">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="7a7f2-106">Los resultados de la subconsulta se usan como origen de la nueva consulta.</span><span class="sxs-lookup"><span data-stu-id="7a7f2-106">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="7a7f2-107">Por ejemplo, digamos que tiene varios archivos de búsqueda guardados que restringen una consulta por lista de distribución de correo electrónico: mydepartment.search-ms, teamproject.search-ms y corporatewide.search-ms.</span><span class="sxs-lookup"><span data-stu-id="7a7f2-107">For example, say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="7a7f2-108">El uso del `subquery` argumento permite limitar las búsquedas de correo electrónico a cualquiera de estas búsquedas guardadas o a todas ellas.</span><span class="sxs-lookup"><span data-stu-id="7a7f2-108">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

## <a name="example"></a><span data-ttu-id="7a7f2-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7a7f2-109">Example</span></span>


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a><span data-ttu-id="7a7f2-110">Información de argumentos</span><span class="sxs-lookup"><span data-stu-id="7a7f2-110">Argument Information</span></span>



|                          |                                         |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="7a7f2-111">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="7a7f2-111">Minimum Operating System</span></span> | <span data-ttu-id="7a7f2-112">Windows Vista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="7a7f2-112">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



