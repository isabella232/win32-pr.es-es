---
description: La cláusula HAVING se utiliza para filtrar los eventos que se reciben durante el intervalo de agrupación especificado en la cláusula WITHIN.
ms.assetid: 787e31df-df6a-4fb0-a1c0-18bd60867e2f
ms.tgt_platform: multiple
title: Cláusula HAVING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f93fbe082fb2f655dfad59d7642e1d0ff9a33e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707213"
---
# <a name="having-clause"></a><span data-ttu-id="ccdb3-103">Cláusula HAVING</span><span class="sxs-lookup"><span data-stu-id="ccdb3-103">HAVING Clause</span></span>

<span data-ttu-id="ccdb3-104">La cláusula HAVING se utiliza para filtrar los eventos que se reciben durante el intervalo de agrupación especificado en la [cláusula Within](within-clause.md).</span><span class="sxs-lookup"><span data-stu-id="ccdb3-104">The HAVING clause is used to filter the events that are received during the grouping interval specified in the [WITHIN clause](within-clause.md).</span></span> <span data-ttu-id="ccdb3-105">Por ejemplo, una instrucción SELECT podría construirse para que no devuelva nada a menos que haya al menos 5 eventos en el intervalo de los últimos 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="ccdb3-105">For example, a SELECT statement could be constructed so that it returns nothing unless there HAVE been at least 5 events within the past 30 second INTERVAL.</span></span>

<span data-ttu-id="ccdb3-106">La cláusula WITHIN sigue inmediatamente en la [instrucción SELECT](select-statement-for-event-queries.md) después de la cláusula [Group](group-clause.md) .</span><span class="sxs-lookup"><span data-stu-id="ccdb3-106">The WITHIN clause follows immediately in the [SELECT statement](select-statement-for-event-queries.md) after the [GROUP](group-clause.md) clause.</span></span> <span data-ttu-id="ccdb3-107">La cláusula HAVING funciona en la propiedad **NumberOfEvents** de la clase del sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) , de la que el grupo creado por la cláusula Group es un miembro.</span><span class="sxs-lookup"><span data-stu-id="ccdb3-107">The HAVING clause operates on the **NumberOfEvents** property of the [**\_\_AggregateEvent**](--aggregateevent.md) system class, of which the group created by the GROUP clause is a member.</span></span> <span data-ttu-id="ccdb3-108">La cláusula HAVING puede utilizar todos los operadores relacionales estándar.</span><span class="sxs-lookup"><span data-stu-id="ccdb3-108">The HAVING clause can use all of the standard relational operators.</span></span>

<span data-ttu-id="ccdb3-109">La sintaxis es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="ccdb3-109">The syntax is as follows:</span></span>

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
  GROUP WITHIN interval [BY property_list]
  HAVING NumberOfEvents operator constant
```

<span data-ttu-id="ccdb3-110">El valor de *EventClass* es la clase de eventos de la que el evento es un miembro y *Value* es el valor de la propiedad en la que se requiere la notificación.</span><span class="sxs-lookup"><span data-stu-id="ccdb3-110">The *EventClass* value is the event class of which the event is a member, and *value* is the value for the property on which notification is required.</span></span> <span data-ttu-id="ccdb3-111">El intervalo es un entero sin signo que representa el intervalo de agrupación (en segundos) después de recibir el primer evento.</span><span class="sxs-lookup"><span data-stu-id="ccdb3-111">The interval is an unsigned integer that represents the grouping interval (in seconds) after receiving the first event.</span></span> <span data-ttu-id="ccdb3-112">La lista de propiedades es una lista delimitada por comas de una o varias propiedades que se incluyen en la clase de eventos.</span><span class="sxs-lookup"><span data-stu-id="ccdb3-112">The property list is a comma-delimited list of one or more properties that are included in the event class.</span></span> <span data-ttu-id="ccdb3-113">El operador es cualquier operador relacional.</span><span class="sxs-lookup"><span data-stu-id="ccdb3-113">The operator is any relational operator.</span></span> <span data-ttu-id="ccdb3-114">El valor constante es cualquier entero de 32 bits sin signo que indique el número de eventos utilizados para filtrar.</span><span class="sxs-lookup"><span data-stu-id="ccdb3-114">The constant value is any unsigned 32-bit integer indicating the number of events used for filtering.</span></span>

<span data-ttu-id="ccdb3-115">Cuando se usa la cláusula HAVING, las cláusulas WHERE y BY son opcionales.</span><span class="sxs-lookup"><span data-stu-id="ccdb3-115">When using the HAVING clause, the WHERE and BY clauses are optional.</span></span>

<span data-ttu-id="ccdb3-116">La siguiente consulta de eventos solicita que las notificaciones de la clase **EmailEvent** se agrupen en un evento 300 segundos después del primer evento que recibe WMI.</span><span class="sxs-lookup"><span data-stu-id="ccdb3-116">The following event query requests that notifications of the **EmailEvent** class be grouped into one event 300 seconds after the first event that WMI receives.</span></span> <span data-ttu-id="ccdb3-117">Además, la consulta solicita que la instancia de [**\_ \_ AggregateEvent**](--aggregateevent.md) se entregue solo si WMI recibe más de cinco eventos de correo electrónico en los 300 segundos.</span><span class="sxs-lookup"><span data-stu-id="ccdb3-117">Also, the query requests the [**\_\_AggregateEvent**](--aggregateevent.md) instance should be delivered only if WMI receives more than five email events in that 300 seconds.</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 HAVING NumberOfEvents > 5
```



<span data-ttu-id="ccdb3-118">En el ejemplo siguiente se agrupan todos los eventos recibidos en 600 segundos (es decir, 10 minutos) por **TargetInstance**. Propiedad **SourceName** .</span><span class="sxs-lookup"><span data-stu-id="ccdb3-118">The following example groups all events received in 600 seconds (that is, 10 minutes) by the **TargetInstance**.**SourceName** property.</span></span> <span data-ttu-id="ccdb3-119">En este ejemplo, los eventos de agregado solo se entregan si el número de eventos [**\_ NTLogEvent de Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) recibidos del mismo origen es superior a 25.</span><span class="sxs-lookup"><span data-stu-id="ccdb3-119">In this example, aggregate events are delivered only if the number of [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) events received from the same source exceeds 25.</span></span> <span data-ttu-id="ccdb3-120">Tenga en cuenta que el operador ISA hace que la propiedad **TargetInstance** de la clase del sistema [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) represente una instancia de la clase **\_ NTLogEvent de Win32** .</span><span class="sxs-lookup"><span data-stu-id="ccdb3-120">Keep in mind that the ISA operator causes the **TargetInstance** property of the [**\_\_InstanceCreationEvent**](--instancecreationevent.md) system class to represent an instance of the **Win32\_NTLogEvent** class.</span></span>


```sql
SELECT * FROM __InstanceCreationEvent 
  WHERE TargetInstance ISA "Win32_NTLogEvent" 
  GROUP WITHIN 600 BY TargetInstance.SourceName
  HAVING NumberOfEvents > 25
```



 

 
