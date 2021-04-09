---
description: Las consultas de esquema son instrucciones WQL que solicitan definiciones de clase e información sobre las asociaciones de esquema.
ms.assetid: cb65e99f-9046-4c63-ab56-60dedc45bcef
ms.tgt_platform: multiple
title: Recuperar definiciones de clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d865b1a85eefa7e67b12ed4c0acc16ea9e19f9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155857"
---
# <a name="retrieving-class-definitions"></a><span data-ttu-id="a250c-103">Recuperar definiciones de clase</span><span class="sxs-lookup"><span data-stu-id="a250c-103">Retrieving Class Definitions</span></span>

<span data-ttu-id="a250c-104">Las consultas de esquema son instrucciones WQL que solicitan definiciones de clase e información sobre las [asociaciones de esquema](schema-associations.md).</span><span class="sxs-lookup"><span data-stu-id="a250c-104">Schema queries are WQL statements that request class definitions and information about [schema associations](schema-associations.md).</span></span> <span data-ttu-id="a250c-105">Los proveedores de clases utilizan consultas de esquema en sus instancias de la clase [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) para especificar las clases que admiten cuando se registran en WMI.</span><span class="sxs-lookup"><span data-stu-id="a250c-105">Class providers use schema queries in their instances of the [**\_\_ClassProviderRegistration**](--classproviderregistration.md) class to specify the classes that they support when they register with WMI.</span></span> <span data-ttu-id="a250c-106">Las consultas de esquema se colocan en las propiedades **ResultSetQueries**, **ReferencedSetQueries** y **UnsupportedQueries** de la instancia de **\_ \_ ClassProviderRegistration** .</span><span class="sxs-lookup"><span data-stu-id="a250c-106">Schema queries are placed in the **ResultSetQueries**, **ReferencedSetQueries**, and **UnsupportedQueries** properties of the **\_\_ClassProviderRegistration** instance.</span></span>

<span data-ttu-id="a250c-107">Las consultas de esquema son similares a las consultas de datos, ya que admiten las siguientes instrucciones WQL:</span><span class="sxs-lookup"><span data-stu-id="a250c-107">Schema queries are similar to data queries in that they support the following WQL statements:</span></span>

-   [<span data-ttu-id="a250c-108">SELECT</span><span class="sxs-lookup"><span data-stu-id="a250c-108">SELECT</span></span>](select-statement-for-schema-queries.md)
-   [<span data-ttu-id="a250c-109">ASSOCIATORS OF</span><span class="sxs-lookup"><span data-stu-id="a250c-109">ASSOCIATORS OF</span></span>](schema-associations.md)
-   [<span data-ttu-id="a250c-110">REFERENCIAS DE</span><span class="sxs-lookup"><span data-stu-id="a250c-110">REFERENCES OF</span></span>](schema-associations.md)
-   [<span data-ttu-id="a250c-111">ISA</span><span class="sxs-lookup"><span data-stu-id="a250c-111">ISA</span></span>](isa-operator-for-schema-queries.md)

<span data-ttu-id="a250c-112">Una consulta de esquema es similar a una [referencia de consulta de](references-of-statement.md) datos que especifica la palabra clave **ClassDefsOnly** . en otras palabras, que devuelve un conjunto de resultados de objetos de definición de clase en lugar de instancias reales de clases de asociación.</span><span class="sxs-lookup"><span data-stu-id="a250c-112">A schema query is similar to a [REFERENCES OF](references-of-statement.md) data query that specifies the **ClassDefsOnly** keyword; in other words, that returns a result set of class definition objects rather than actual instances of association classes.</span></span> <span data-ttu-id="a250c-113">Sin embargo, las referencias de solo devuelven definiciones de clase si hay instancias presentes.</span><span class="sxs-lookup"><span data-stu-id="a250c-113">However, REFERENCES OF returns class definitions only if there are instances present.</span></span> <span data-ttu-id="a250c-114">Una consulta de esquema devuelve definiciones de clase tanto si las instancias están presentes como si no.</span><span class="sxs-lookup"><span data-stu-id="a250c-114">A schema query returns class definitions whether or not instances are present.</span></span>

 

 



