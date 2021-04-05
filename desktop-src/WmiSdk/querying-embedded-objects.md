---
description: Tiene varias opciones para el formulario que realiza una consulta al consultar una clase de eventos que contiene objetos incrustados. Los resultados devueltos por la consulta varían en función del formulario de la consulta que use.
ms.assetid: b959a695-be15-4aa7-9368-b840962ae0da
ms.tgt_platform: multiple
title: Consultar objetos incrustados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed2e13bd9d9dc798891a723a6fed1b1734e1735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812440"
---
# <a name="querying-embedded-objects"></a><span data-ttu-id="61c2f-104">Consultar objetos incrustados</span><span class="sxs-lookup"><span data-stu-id="61c2f-104">Querying Embedded Objects</span></span>

<span data-ttu-id="61c2f-105">Tiene varias opciones para el formulario que realiza una consulta al consultar una clase de eventos que contiene objetos incrustados.</span><span class="sxs-lookup"><span data-stu-id="61c2f-105">You have several options as to the form a query takes when querying an event class that contains embedded objects.</span></span> <span data-ttu-id="61c2f-106">Los resultados devueltos por la consulta varían en función del formulario de la consulta que use.</span><span class="sxs-lookup"><span data-stu-id="61c2f-106">The results returned by the query vary, depending on the form of the query you use.</span></span>

## <a name="class-definitions"></a><span data-ttu-id="61c2f-107">Definiciones de clase</span><span class="sxs-lookup"><span data-stu-id="61c2f-107">Class Definitions</span></span>

<span data-ttu-id="61c2f-108">En el siguiente ejemplo se muestran las definiciones de clase que se utilizan para las consultas WQL de este tema.</span><span class="sxs-lookup"><span data-stu-id="61c2f-108">The following example shows the class definitions that are used for the WQL queries in this topic.</span></span>

``` syntax
class MyClass
{
   string Prop1;
   string Prop2;
};

class MyEvent : __ExtrinsicEvent
{
   MyClass E1;
   MyClass E2;
};
```

## <a name="examples"></a><span data-ttu-id="61c2f-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="61c2f-109">Examples</span></span>

<span data-ttu-id="61c2f-110">La consulta siguiente devuelve las clases incrustadas, **E1** y **E2**, cada una con **Prop1** y **Prop2** rellenados con datos.</span><span class="sxs-lookup"><span data-stu-id="61c2f-110">The following query returns both embedded classes, **E1** and **E2**, each having **Prop1** and **Prop2** populated with data.</span></span>

`SELECT * FROM MyEvent`

<span data-ttu-id="61c2f-111">La siguiente consulta devuelve el objeto de **E1** incrustado, pero no se ha rellenado con datos ni con **Prop1** ni **Prop2** .</span><span class="sxs-lookup"><span data-stu-id="61c2f-111">The following query returns the **E1** embedded object, but with neither **Prop1** nor **Prop2** populated with data.</span></span>

`SELECT E1 FROM MyEvent`

<span data-ttu-id="61c2f-112">La consulta siguiente devuelve la clase incrustada **E1** con solo **Prop1** rellenado con datos.</span><span class="sxs-lookup"><span data-stu-id="61c2f-112">The following query returns the embedded class **E1** with only **Prop1** populated with data.</span></span>

`SELECT E1.Prop1 FROM MyEvent`

<span data-ttu-id="61c2f-113">La consulta siguiente devuelve las clases incrustadas, **E1** y **E2**, cada una con **Prop1** y **Prop2** rellenados con datos.</span><span class="sxs-lookup"><span data-stu-id="61c2f-113">The following query returns both embedded classes, **E1** and **E2**, each having **Prop1** and **Prop2** populated with data.</span></span>

`ELECT E1.Prop1, E1.Prop2, E2.Prop1, E2.Prop2 FROM MyEvent`

<span data-ttu-id="61c2f-114">Esto es equivalente a la primera consulta que usa el asterisco ( \* ) en lugar de especificar cada objeto y propiedad.</span><span class="sxs-lookup"><span data-stu-id="61c2f-114">This is equivalent to the first query using the asterisk (\*) instead of specifying each object and property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61c2f-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="61c2f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61c2f-116">Realizar consultas con WQL</span><span class="sxs-lookup"><span data-stu-id="61c2f-116">Querying with WQL</span></span>](querying-with-wql.md)
</dt> </dl>

 

 



