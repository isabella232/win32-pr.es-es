---
title: Ensamblar cadenas de consulta
description: En Active Directory, el uso de criterios de filtrado específicos puede mejorar el rendimiento de la búsqueda. Esto se debe a que Active Directory evalúa todos los predicados, identifica los índices y, a continuación, selecciona un índice que probablemente produzca el conjunto más pequeño de valores devueltos.
ms.assetid: 4139eedb-1383-4654-9b40-5e294a71be24
ms.tgt_platform: multiple
keywords:
- Ensamblar las cadenas de consulta ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e56dec34f63a4a3e12385a36ad5fe5339a0f3d9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656195"
---
# <a name="assembling-query-strings"></a><span data-ttu-id="666ba-105">Ensamblar cadenas de consulta</span><span class="sxs-lookup"><span data-stu-id="666ba-105">Assembling Query Strings</span></span>

<span data-ttu-id="666ba-106">En Active Directory, el uso de criterios de filtrado específicos puede mejorar el rendimiento de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="666ba-106">In Active Directory, using specific filtering criteria can boost search performance.</span></span> <span data-ttu-id="666ba-107">Esto se debe a que Active Directory evalúa todos los predicados, identifica los índices y, a continuación, selecciona un índice que probablemente produzca el conjunto más pequeño de valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="666ba-107">This is because Active Directory evaluates all predicates, identifies the indices, and then selects one index likely to yield the smallest set of returned values.</span></span>

<span data-ttu-id="666ba-108">Evite buscar texto en el centro o el final de una cadena, por ejemplo, "CN = \* Hille \* " o "CN = \* Larouse".</span><span class="sxs-lookup"><span data-stu-id="666ba-108">Avoid searching for text in the middle or the end of a string, for example, "cn=\*hille\*" or "cn=\*larouse".</span></span>

<span data-ttu-id="666ba-109">Cuando sea posible, busque atributos indexados.</span><span class="sxs-lookup"><span data-stu-id="666ba-109">When possible, search for indexed attributes.</span></span> <span data-ttu-id="666ba-110">Los atributos indizados se almacenan en todos los controladores de dominio, por lo que es más probable que la consulta sea más rápida que la búsqueda de un atributo no indexado.</span><span class="sxs-lookup"><span data-stu-id="666ba-110">Indexed attributes are stored on all domain controllers, so the query will most likely be faster than searching for a non-indexed attribute.</span></span>

 

 




