---
description: Una subconsulta es un archivo de búsqueda guardado ( \* . Search-MS) que puede usar como filtro para una nueva consulta.
title: Argumento de subconsulta (Shell de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 43e4a5b904d5e769eb43acad05aa5d8ce37ebde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997885"
---
# <a name="subquery-argument-the-windows-shell"></a><span data-ttu-id="552fc-103">Argumento de subconsulta (Shell de Windows)</span><span class="sxs-lookup"><span data-stu-id="552fc-103">SUBQUERY Argument (The Windows Shell)</span></span>

<span data-ttu-id="552fc-104">Una subconsulta es un archivo de búsqueda guardado ( \* . Search-MS) que puede usar como filtro para una nueva consulta.</span><span class="sxs-lookup"><span data-stu-id="552fc-104">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="552fc-105">Los resultados de la subconsulta se usan como origen de la nueva consulta.</span><span class="sxs-lookup"><span data-stu-id="552fc-105">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="552fc-106">Por ejemplo, supongamos que tiene varios archivos de búsqueda guardados que restringen una consulta por lista de distribución de correo electrónico: Departamento. Search-MS, teamproject. Search-MS y corporatewide. Search-ms.</span><span class="sxs-lookup"><span data-stu-id="552fc-106">For example, say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="552fc-107">El uso del `subquery` argumento le permite limitar las búsquedas de correo electrónico a cualquiera de estas búsquedas guardadas.</span><span class="sxs-lookup"><span data-stu-id="552fc-107">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

## <a name="example"></a><span data-ttu-id="552fc-108">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="552fc-108">Example</span></span>


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a><span data-ttu-id="552fc-109">Información de argumentos</span><span class="sxs-lookup"><span data-stu-id="552fc-109">Argument Information</span></span>



|                          |                                         |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="552fc-110">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="552fc-110">Minimum Operating System</span></span> | <span data-ttu-id="552fc-111">Windows Vista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="552fc-111">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



