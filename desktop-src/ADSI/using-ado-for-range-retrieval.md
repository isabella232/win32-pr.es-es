---
title: Usar ADO para la recuperación por intervalos
description: Si se utiliza un lenguaje de automatización, los objetos de directorio ActiveX (ADO) deben usarse para recuperar un intervalo de valores de propiedad. Cuando se usa ADO para la recuperación por intervalos, hay un problema que se debe solucionar de forma específica.
ms.assetid: ca06169d-7de7-4552-aa7d-e9427353e49e
ms.tgt_platform: multiple
keywords:
- Usar ADO para la recuperación de intervalos ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb8950a71708bd9c824c90842f043808c897554
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772901"
---
# <a name="using-ado-for-range-retrieval"></a><span data-ttu-id="45644-104">Usar ADO para la recuperación por intervalos</span><span class="sxs-lookup"><span data-stu-id="45644-104">Using ADO for Range Retrieval</span></span>

<span data-ttu-id="45644-105">Si se utiliza un lenguaje de automatización, los objetos de directorio ActiveX (ADO) deben usarse para recuperar un intervalo de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="45644-105">If an automation language is used, the ActiveX Directory Objects (ADO) should be used to retrieve a range of property values.</span></span>

<span data-ttu-id="45644-106">Cuando se usa ADO para la recuperación por intervalos, hay un problema que se debe solucionar de forma específica.</span><span class="sxs-lookup"><span data-stu-id="45644-106">When using ADO for range retrieval, there is one problem that must be specifically addressed.</span></span> <span data-ttu-id="45644-107">Al consultar el grupo final de valores de propiedad, el objeto ADO recuperará cero objetos, aunque se mantenga más.</span><span class="sxs-lookup"><span data-stu-id="45644-107">When querying for the final group of property values, the ADO object will retrieve zero objects, even though more remain.</span></span> <span data-ttu-id="45644-108">Para recuperar los valores restantes, use el carácter comodín de intervalo ' \* '.</span><span class="sxs-lookup"><span data-stu-id="45644-108">To retrieve the remaining values, use the range wildcard '\*'.</span></span> <span data-ttu-id="45644-109">Por ejemplo, si un grupo contiene 150 miembros, los valores de miembro 0-100 se pueden recuperar normalmente mediante la recuperación por intervalos.</span><span class="sxs-lookup"><span data-stu-id="45644-109">For example, if a group contains 150 members, member values 0-100 can be retrieved normally using ranged retrieval.</span></span> <span data-ttu-id="45644-110">Si se solicita el intervalo 101-200, el objeto ADO devolverá cero objetos.</span><span class="sxs-lookup"><span data-stu-id="45644-110">If range 101-200 is then requested, the ADO object will return zero objects.</span></span> <span data-ttu-id="45644-111">En este punto, es necesario modificar la consulta para que el intervalo de solicitud sea 101- \* .</span><span class="sxs-lookup"><span data-stu-id="45644-111">At this point, it is necessary to modify the query to request range 101-\*.</span></span> <span data-ttu-id="45644-112">Se recuperarán los valores de 101 a 150.</span><span class="sxs-lookup"><span data-stu-id="45644-112">This will retrieve values from 101 to 150.</span></span> <span data-ttu-id="45644-113">Para obtener más información y un ejemplo de código, vea [ejemplo de código para usar el intervalo para recuperar miembros de un grupo](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).</span><span class="sxs-lookup"><span data-stu-id="45644-113">For more information and a code example, see [Example Code for Using Ranging to Retrieve Members of a Group](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).</span></span>

<span data-ttu-id="45644-114">Para obtener más información sobre el uso de ADO para la recuperación de intervalos, vea:</span><span class="sxs-lookup"><span data-stu-id="45644-114">For more information about using ADO for range retrieval, see:</span></span>

-   [<span data-ttu-id="45644-115">Lenguaje de dialecto de ADO LDAP</span><span class="sxs-lookup"><span data-stu-id="45644-115">ADO LDAP Ranging Dialect</span></span>](ado-ldap-ranging-dialect.md)
-   [<span data-ttu-id="45644-116">Dialecto SQL de ADO</span><span class="sxs-lookup"><span data-stu-id="45644-116">ADO SQL Ranging Dialect</span></span>](ado-sql-ranging-dialect.md)
-   [<span data-ttu-id="45644-117">Código de ejemplo para utilizar el intervalo para recuperar miembros de un grupo</span><span class="sxs-lookup"><span data-stu-id="45644-117">Example Code for Using Ranging to Retrieve Members of a Group</span></span>](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

 

 




