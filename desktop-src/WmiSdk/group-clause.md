---
description: La cláusula GROUP hace que WMI genere una notificación única para representar un grupo de eventos.
ms.assetid: 811e72f8-2e50-4696-ad58-50bb5e211afb
ms.tgt_platform: multiple
title: GROUP (cláusula)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 032a8e86c84c0b317b3739c0e203a249b432b0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707216"
---
# <a name="group-clause"></a><span data-ttu-id="c2913-103">GROUP (cláusula)</span><span class="sxs-lookup"><span data-stu-id="c2913-103">GROUP Clause</span></span>

<span data-ttu-id="c2913-104">La cláusula GROUP hace que WMI genere una notificación única para representar un grupo de eventos.</span><span class="sxs-lookup"><span data-stu-id="c2913-104">The GROUP clause causes WMI to generate a single notification to represent a group of events.</span></span> <span data-ttu-id="c2913-105">La notificación representativa es una instancia de la clase del sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) .</span><span class="sxs-lookup"><span data-stu-id="c2913-105">The representative notification is an instance of the [**\_\_AggregateEvent**](--aggregateevent.md) system class.</span></span> <span data-ttu-id="c2913-106">La clase del sistema **\_ \_ AggregateEvent** contiene dos propiedades: **representator** y **NumberOfEvents**.</span><span class="sxs-lookup"><span data-stu-id="c2913-106">The **\_\_AggregateEvent** system class contains two properties: **Representative** and **NumberOfEvents**.</span></span> <span data-ttu-id="c2913-107">La propiedad **representativa** es un objeto incrustado que contiene una de las instancias recibidas durante el intervalo de agrupación especificado en la [cláusula Within](within-clause.md).</span><span class="sxs-lookup"><span data-stu-id="c2913-107">The **Representative** property is an embedded object that contains one of the instances received during the grouping interval specified in the [WITHIN clause](within-clause.md).</span></span> <span data-ttu-id="c2913-108">Por ejemplo, si se genera un evento agregado para notificar los eventos de modificación de instancia, el **representador** contiene una instancia de la clase [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) .</span><span class="sxs-lookup"><span data-stu-id="c2913-108">For example, if an aggregate event is generated to notify of instance modification events, **Representative** contains one instance of the [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) class.</span></span> <span data-ttu-id="c2913-109">La propiedad **NumberOfEvents** contiene el número de eventos recibidos durante el intervalo de agrupación.</span><span class="sxs-lookup"><span data-stu-id="c2913-109">The **NumberOfEvents** property contains the number of events received during the grouping interval.</span></span> <span data-ttu-id="c2913-110">El intervalo de agrupación especifica el período de tiempo, después de recibir un evento inicial, durante el cual WMI debe recopilar eventos similares.</span><span class="sxs-lookup"><span data-stu-id="c2913-110">The grouping interval specifies the time period, after receiving an initial event, during which WMI should collect similar events.</span></span>

<span data-ttu-id="c2913-111">La cláusula GROUP debe contener una cláusula WITHIN para especificar el intervalo de agrupación y puede contener la palabra clave BY o HAVING, o ambas.</span><span class="sxs-lookup"><span data-stu-id="c2913-111">The GROUP clause must contain a WITHIN clause to specify the grouping interval and can contain the BY or HAVING keyword, or both.</span></span> <span data-ttu-id="c2913-112">La cláusula GROUP se coloca después de la cláusula WHERE, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="c2913-112">The GROUP clause is placed after the WHERE clause, as shown following:</span></span>

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
    GROUP WITHIN interval [BY property_list]
    [HAVING NumberOfEvents operator integer]
```

<span data-ttu-id="c2913-113">El valor de *EventClass* es la clase de eventos de la que el evento es un miembro y *Value* es el valor de la propiedad en la que se requiere la notificación.</span><span class="sxs-lookup"><span data-stu-id="c2913-113">The *EventClass* value is the event class of which the event is a member, and *value* is the value for the property on which notification is required.</span></span> <span data-ttu-id="c2913-114">El intervalo es un entero sin signo que representa el intervalo de agrupación después de recibir el primer evento.</span><span class="sxs-lookup"><span data-stu-id="c2913-114">The interval is an unsigned integer that represents the grouping interval after receiving the first event.</span></span> <span data-ttu-id="c2913-115">El entero sin signo es un número de segundos.</span><span class="sxs-lookup"><span data-stu-id="c2913-115">The unsigned integer is a number of seconds.</span></span> <span data-ttu-id="c2913-116">La lista de propiedades es una lista delimitada por comas de una o varias propiedades que se incluyen en la clase de eventos; *Operator* es cualquier operador relacional; y *entero* es un entero de 32 bits sin signo que indica un número de eventos.</span><span class="sxs-lookup"><span data-stu-id="c2913-116">The property list is a comma-delimited list of one or more properties that are included in the event class; *operator* is any relational operator; and *integer* is an unsigned 32-bit integer indicating a number of events.</span></span>

<span data-ttu-id="c2913-117">Cuando se usa la cláusula GROUP, las cláusulas WHERE, BY y HAVING son opcionales.</span><span class="sxs-lookup"><span data-stu-id="c2913-117">When using the GROUP clause, the WHERE, BY, and HAVING clauses are optional.</span></span>

<span data-ttu-id="c2913-118">Un uso básico de la cláusula GROUP podría solicitar una agrupación de eventos dentro de un intervalo de tiempo que se inicia cuando se recibe el primer evento.</span><span class="sxs-lookup"><span data-stu-id="c2913-118">A basic use of the GROUP clause might request a grouping of events within a time interval that starts when the first event is received.</span></span> <span data-ttu-id="c2913-119">Por ejemplo, la consulta siguiente agrupa todos los eventos de correo electrónico enviados en 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="c2913-119">For example, the following query groups all of the email events sent within 5 minutes.</span></span> <span data-ttu-id="c2913-120">En lugar de paginar a un usuario cada vez que se recibe un mensaje de correo electrónico nuevo, el consumidor permanente podría usar esta consulta para informar al usuario solo si se ha recibido un nuevo correo electrónico en los últimos 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="c2913-120">Instead of paging a user every time a piece of new email is received, the permanent consumer might use this query to inform the user only if new email has been received within the last 5 minutes.</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300
```



<span data-ttu-id="c2913-121">Si se requiere información más detallada, los eventos se pueden agrupar por una o más propiedades de la clase de evento.</span><span class="sxs-lookup"><span data-stu-id="c2913-121">If more detailed information is required, events can be grouped by one or more properties of the event class.</span></span> <span data-ttu-id="c2913-122">La consulta siguiente solicita que los eventos de correo electrónico se combinen con otros eventos que tienen el mismo valor en la propiedad **Sender** :</span><span class="sxs-lookup"><span data-stu-id="c2913-122">The following query requests that email events be combined with other events that have the same value in the **Sender** property:</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 BY Sender
```



<span data-ttu-id="c2913-123">Se puede lograr un nivel de detalle todavía mayor agregando una cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="c2913-123">A still greater level of detail can be achieved by adding a WHERE clause.</span></span> <span data-ttu-id="c2913-124">Por ejemplo, la siguiente consulta notifica a un usuario de un mensaje de correo electrónico nuevo de un remitente determinado que ha llegado en los últimos 10 minutos, junto con otros eventos que tienen el mismo valor en la propiedad **importance** :</span><span class="sxs-lookup"><span data-stu-id="c2913-124">For example, the following query notifies a user of new email from a particular sender that has arrived within the last 10 minutes, combined with other events that have the same value in the **Importance** property:</span></span>


```sql
SELECT * FROM EventClass WHERE Sender = "MyBoss" 
  GROUP WITHIN 300 BY Importance
```



 

 



