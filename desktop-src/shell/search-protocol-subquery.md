---
description: Obtenga información sobre el argumento SUBQUERY en The Windows Shell. Una subconsulta es un archivo de búsqueda guardado que puede usar como filtro para una nueva consulta.
title: Argumento SUBQUERY (El shell Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c27ce11d4d2e6ac36792f3ce47c053e9646d9903
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581603"
---
# <a name="subquery-argument-the-windows-shell"></a><span data-ttu-id="48421-104">Argumento SUBQUERY (El shell Windows)</span><span class="sxs-lookup"><span data-stu-id="48421-104">SUBQUERY Argument (The Windows Shell)</span></span>

<span data-ttu-id="48421-105">Una subconsulta es un archivo de búsqueda guardado (.search-ms) que puede usar como \* filtro para una nueva consulta.</span><span class="sxs-lookup"><span data-stu-id="48421-105">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="48421-106">Los resultados de la subconsulta se usan como origen de la nueva consulta.</span><span class="sxs-lookup"><span data-stu-id="48421-106">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="48421-107">Por ejemplo, digamos que tiene varios archivos de búsqueda guardados que restringen una consulta por lista de distribución de correo electrónico: mydepartment.search-ms, teamproject.search-ms y corporatewide.search-ms.</span><span class="sxs-lookup"><span data-stu-id="48421-107">For example, say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="48421-108">El uso del `subquery` argumento permite limitar las búsquedas de correo electrónico a cualquiera de estas búsquedas guardadas o a todas ellas.</span><span class="sxs-lookup"><span data-stu-id="48421-108">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

## <a name="example"></a><span data-ttu-id="48421-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="48421-109">Example</span></span>


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a><span data-ttu-id="48421-110">Información de argumentos</span><span class="sxs-lookup"><span data-stu-id="48421-110">Argument Information</span></span>



|                              | <span data-ttu-id="48421-111">Value</span><span class="sxs-lookup"><span data-stu-id="48421-111">Value</span></span>                                   |
|------------------------------|-----------------------------------------|
| <span data-ttu-id="48421-112">**Sistema operativo mínimo**</span><span class="sxs-lookup"><span data-stu-id="48421-112">**Minimum Operating System**</span></span> | <span data-ttu-id="48421-113">Windows Vista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="48421-113">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



