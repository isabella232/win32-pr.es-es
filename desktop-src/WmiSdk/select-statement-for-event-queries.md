---
description: Describe la sintaxis básica de una instrucción SELECT para las consultas de eventos.
ms.assetid: 8882fdcb-3768-41e3-82ab-3006d903f3a0
ms.tgt_platform: multiple
title: Instrucción SELECT para consultas de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab840072269d04987bf42939f1f566ee6b99afab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278762"
---
# <a name="select-statement-for-event-queries"></a><span data-ttu-id="a2572-103">Instrucción SELECT para consultas de eventos</span><span class="sxs-lookup"><span data-stu-id="a2572-103">SELECT Statement for Event Queries</span></span>

<span data-ttu-id="a2572-104">Puede utilizar una serie de instrucciones SELECT para consultar información de eventos.</span><span class="sxs-lookup"><span data-stu-id="a2572-104">You can use a variety of SELECT statements to query for event information.</span></span> <span data-ttu-id="a2572-105">Las instrucciones pueden ser instrucciones básicas o pueden ser más restrictivas para restringir el conjunto de resultados que se devuelve de la consulta.</span><span class="sxs-lookup"><span data-stu-id="a2572-105">The statements can be basic statements or they can be more restrictive to narrow the result set that is returned from the query.</span></span>

<span data-ttu-id="a2572-106">El ejemplo siguiente es una instrucción SELECT básica que se utiliza para consultar la información de eventos.</span><span class="sxs-lookup"><span data-stu-id="a2572-106">The following example is a basic SELECT statement that is used to query for event information.</span></span>


```sql
SELECT * FROM EventClass
```



<span data-ttu-id="a2572-107">Cuando un consumidor envía una consulta, se trata de una solicitud para recibir notificaciones de todas las repeticiones del evento representado por **EventClass**.</span><span class="sxs-lookup"><span data-stu-id="a2572-107">When a consumer submits a query, it is a request to be notified of all occurrences of the event represented by **EventClass**.</span></span> <span data-ttu-id="a2572-108">Esta solicitud incluye una solicitud de notificación sobre todas las propiedades del sistema de eventos y las que no son del sistema.</span><span class="sxs-lookup"><span data-stu-id="a2572-108">This request includes a request for notification about all of the event system and nonsystem properties.</span></span> <span data-ttu-id="a2572-109">Cuando un proveedor de eventos envía una consulta, registra la compatibilidad para generar notificaciones cuando se produce un evento representado por **EventClass** .</span><span class="sxs-lookup"><span data-stu-id="a2572-109">When an event provider submits a query, it registers support for generating notifications when an event represented by **EventClass** occurs.</span></span>

<span data-ttu-id="a2572-110">Los consumidores pueden especificar propiedades individuales en lugar del asterisco ( \* ) en la instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="a2572-110">Consumers can specify individual properties instead of the asterisk (\*) in the SELECT statement.</span></span>

<span data-ttu-id="a2572-111">En el ejemplo siguiente se muestra cómo consultar propiedades específicas.</span><span class="sxs-lookup"><span data-stu-id="a2572-111">The following example shows how to query for specific properties.</span></span>


```sql
SELECT property_1, property_2, property_3 FROM MyEventClass
```



<span data-ttu-id="a2572-112">Sin embargo, se devuelven todas las propiedades de un objeto incrustado, aunque la consulta especifique las propiedades del objeto incrustado.</span><span class="sxs-lookup"><span data-stu-id="a2572-112">However, all of the properties of an embedded object are returned, even if the query specifies embedded object properties.</span></span>

<span data-ttu-id="a2572-113">En el ejemplo siguiente se muestran dos consultas que devuelven los mismos datos.</span><span class="sxs-lookup"><span data-stu-id="a2572-113">The following example shows two queries that return the same data.</span></span>


```sql
SELECT targetInstance FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```




```sql
SELECT targetInstance.Name FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```



<span data-ttu-id="a2572-114">Si una propiedad del sistema no es relevante para una consulta específica, contiene **null**.</span><span class="sxs-lookup"><span data-stu-id="a2572-114">If a system property is not relevant for a specific query, it contains **NULL**.</span></span> <span data-ttu-id="a2572-115">Por ejemplo, el valor de la propiedad del sistema **\_ \_ RELPATH** es **null** para todas las consultas de eventos.</span><span class="sxs-lookup"><span data-stu-id="a2572-115">For example, the value of the **\_\_RELPATH** system property is **NULL** for all event queries.</span></span>

<span data-ttu-id="a2572-116">Las siguientes propiedades del sistema contienen **valores NULL** para las consultas de eventos:</span><span class="sxs-lookup"><span data-stu-id="a2572-116">The following system properties contain **NULL** for event queries:</span></span>

<dl> <span data-ttu-id="a2572-117">\_\_System.IO</span><span class="sxs-lookup"><span data-stu-id="a2572-117">\_\_Namespace</span></span>  
<span data-ttu-id="a2572-118">\_\_Camino</span><span class="sxs-lookup"><span data-stu-id="a2572-118">\_\_Path</span></span>  
<span data-ttu-id="a2572-119">\_\_RelPath</span><span class="sxs-lookup"><span data-stu-id="a2572-119">\_\_RelPath</span></span>  
<span data-ttu-id="a2572-120">\_\_Servidor</span><span class="sxs-lookup"><span data-stu-id="a2572-120">\_\_Server</span></span>  
</dl>

<span data-ttu-id="a2572-121">Para obtener más información, vea [referencia de propiedades del sistema WMI](wmi-system-properties.md).</span><span class="sxs-lookup"><span data-stu-id="a2572-121">For more information, see [WMI System Property Reference](wmi-system-properties.md).</span></span>

<span data-ttu-id="a2572-122">Todas las consultas de eventos pueden incluir una [cláusula WHERE](where-clause.md)opcional, pero los consumidores usan principalmente las cláusulas WHERE para especificar filtros adicionales.</span><span class="sxs-lookup"><span data-stu-id="a2572-122">All event queries can include an optional [WHERE clause](where-clause.md), but WHERE clauses are primarily used by consumers to specify additional filtering.</span></span> <span data-ttu-id="a2572-123">Se recomienda encarecidamente que los consumidores especifiquen siempre una cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="a2572-123">It is strongly recommended that consumers always specify a WHERE clause.</span></span> <span data-ttu-id="a2572-124">El costo de una consulta compleja es mínimo en comparación con el costo de entrega y procesamiento de notificaciones innecesarias.</span><span class="sxs-lookup"><span data-stu-id="a2572-124">The cost of a complex query is minimal compared to the cost of delivering and processing unneeded notifications.</span></span>

<span data-ttu-id="a2572-125">En el ejemplo siguiente se muestra una consulta que solicita notificaciones de todos los eventos de modificación de instancia que afectan a la clase hipotética **EmailEvent**.</span><span class="sxs-lookup"><span data-stu-id="a2572-125">The following example shows a query that requests notifications of all instance modification events that affect the hypothetical class **EmailEvent**.</span></span>


```sql
SELECT * FROM EmailEvent
```



<span data-ttu-id="a2572-126">Si los eventos asociados a **EmailEvent** se producen con frecuencia, el consumidor se inunda con eventos.</span><span class="sxs-lookup"><span data-stu-id="a2572-126">If events associated with **EmailEvent** occur frequently, the consumer is flooded with events.</span></span> <span data-ttu-id="a2572-127">Una consulta mejor solicita eventos solo cuando las condiciones específicas usan propiedades de la clase especificada, como cuando el nivel de importancia es alto.</span><span class="sxs-lookup"><span data-stu-id="a2572-127">A better query requests events only when specific conditions use properties of the class specified, such as when the importance level is high.</span></span>

<span data-ttu-id="a2572-128">En el ejemplo siguiente se muestra la consulta que se puede usar si **EmailImportance** es una propiedad de la clase **EmailEvent**.</span><span class="sxs-lookup"><span data-stu-id="a2572-128">The following example shows the query you can use if **EmailImportance** is a property of the class **EmailEvent**.</span></span>


```sql
SELECT * FROM EmailEvent WHERE EmailImportance > 3
```



<span data-ttu-id="a2572-129">Tenga en cuenta que WMI puede rechazar una consulta por una serie de motivos.</span><span class="sxs-lookup"><span data-stu-id="a2572-129">Note that WMI can reject a query for a number of reasons.</span></span> <span data-ttu-id="a2572-130">Por ejemplo, la consulta puede ser demasiado compleja o consumir muchos recursos para su evaluación.</span><span class="sxs-lookup"><span data-stu-id="a2572-130">For example, the query can be too complex or resource-intensive for evaluation.</span></span> <span data-ttu-id="a2572-131">Cuando esto ocurre, WMI devuelve códigos de error específicos, como **la \_ \_ \_ consulta no válida WBEM E**.</span><span class="sxs-lookup"><span data-stu-id="a2572-131">When this occurs, WMI returns specific error codes, such as **WBEM\_E\_INVALID\_QUERY**.</span></span>

<span data-ttu-id="a2572-132">Las propiedades de los objetos incrustados se pueden usar en la cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="a2572-132">Properties of embedded objects can be used in the WHERE clause.</span></span>

<span data-ttu-id="a2572-133">En el ejemplo siguiente se muestra cómo consultar objetos en los que la propiedad **TargetInstance** de la clase del sistema [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) es un objeto [**\_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) incrustado y **FreeSpace** es una propiedad de **Win32 \_ LogicalDisk**.</span><span class="sxs-lookup"><span data-stu-id="a2572-133">The following example shows how to query for objects where the **TargetInstance** property of the [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) system class is an embedded [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) object and **FreeSpace** is a property of **Win32\_LogicalDisk**.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
    WHERE TargetInstance ISA "Win32_LogicalDisk" 
    AND   TargetInstance.FreeSpace < 1000000
```



## <a name="examples"></a><span data-ttu-id="a2572-134">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a2572-134">Examples</span></span>

<span data-ttu-id="a2572-135">El [evento de creación de monitor para el nombre de proceso específico](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) ejemplo de VBScript en TechNet usa la instrucción SELECT para supervisar los eventos de creación de instancia de WMI para \_ el proceso de Win32, filtrando por un nombre de proceso específico.</span><span class="sxs-lookup"><span data-stu-id="a2572-135">The [Monitor creation event for specific process name](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) VBScript sample on TechNet uses the SELECT statement to monitor WMI instance creation events for Win32\_Process, filtering for a specific process name.</span></span>

 

 
