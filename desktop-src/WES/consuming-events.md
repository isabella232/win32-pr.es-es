---
title: Consumir eventos (registro de eventos de Windows)
description: Puede consumir eventos de los canales o de los archivos de registro.
ms.assetid: 17204d3f-0875-42c5-9af4-caca6349a67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb3fb1b36a0cd4ecf836a8893bc1abc14e46451
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105695832"
---
# <a name="consuming-events-windows-event-log"></a><span data-ttu-id="2c92f-103">Consumir eventos (registro de eventos de Windows)</span><span class="sxs-lookup"><span data-stu-id="2c92f-103">Consuming Events (Windows Event Log)</span></span>

<span data-ttu-id="2c92f-104">Puede consumir eventos de los canales o de los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="2c92f-104">You can consume events from channels or from log files.</span></span> <span data-ttu-id="2c92f-105">Para consumir eventos, puede consumir todos los eventos o especificar una expresión XPath que identifique los eventos que desea consumir.</span><span class="sxs-lookup"><span data-stu-id="2c92f-105">To consume events, you can consume all events or you can specify an XPath expression that identifies the events that you want to consume.</span></span> <span data-ttu-id="2c92f-106">Para determinar los elementos y atributos de un evento que puede utilizar en la expresión XPath, vea [esquema de eventos](eventschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="2c92f-106">To determine the elements and attributes of an event that you can use in your XPath expression, see [Event Schema](eventschema-schema.md).</span></span>

<span data-ttu-id="2c92f-107">El registro de eventos de Windows admite un subconjunto de XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="2c92f-107">Windows Event Log supports a subset of XPath 1.0.</span></span> <span data-ttu-id="2c92f-108">Para obtener más información sobre las limitaciones, consulte [restricciones de XPath 1,0](#xpath-10-limitations).</span><span class="sxs-lookup"><span data-stu-id="2c92f-108">For details on the limitations, see [XPath 1.0 limitations](#xpath-10-limitations).</span></span>

<span data-ttu-id="2c92f-109">En los ejemplos siguientes se muestran expresiones XPath simples.</span><span class="sxs-lookup"><span data-stu-id="2c92f-109">The following examples show simple XPath expressions.</span></span>


```XML
// The following query selects all events from the channel or log file
XPath Query: *

// The following query selects all the LowOnMemory events from the channel or log file
XPath Query: *[UserData/LowOnMemory]

// The following query selects all events with a severity level of 1 (Critical) from the channel or log file
XPath Query: *[System/Level=1]

// The following query shows a compound expression that selects all events from the channel or log file
// where the printer's name is MyPrinter and severity level is 1.
XPath Query: *[UserData/*/PrinterName="MyPrinter" and System/Level=1]

// The following query selects all events from the channel or log file where the severity level is
// less than or equal to 3 and the event occurred in the last 24 hour period.
XPath Query: *[System[(Level <= 3) and TimeCreated[timediff(@SystemTime) <= 86400000]]]
```



<span data-ttu-id="2c92f-110">Puede utilizar directamente las expresiones XPath al llamar a las funciones [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) o [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) , o puede usar una consulta XML estructurada que contenga la expresión XPath.</span><span class="sxs-lookup"><span data-stu-id="2c92f-110">You can use the XPath expressions directly when calling the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) functions or you can use a structured XML query that contains the XPath expression.</span></span> <span data-ttu-id="2c92f-111">En el caso de consultas simples que consultan eventos de un solo origen, el uso de una expresión XPath es correcto.</span><span class="sxs-lookup"><span data-stu-id="2c92f-111">For simple queries that query events from a single source, using an XPath expression is fine.</span></span> <span data-ttu-id="2c92f-112">Si la expresión XPath es una expresión compuesta que contiene más de 20 expresiones o está consultando eventos de varios orígenes, debe utilizar una consulta XML estructurada.</span><span class="sxs-lookup"><span data-stu-id="2c92f-112">If the XPath expression is a compound expression that contains more than 20 expressions or you are querying for events from multiple sources, then you must use a structured XML query.</span></span> <span data-ttu-id="2c92f-113">Para obtener más información sobre los elementos de una consulta XML estructurada, vea [esquema de consulta](queryschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="2c92f-113">For details on the elements of a structured XML query, see [Query Schema](queryschema-schema.md).</span></span>

<span data-ttu-id="2c92f-114">Una consulta estructurada identifica el origen de los eventos y uno o más selectores o suprimidores.</span><span class="sxs-lookup"><span data-stu-id="2c92f-114">A structured query identifies the source of the events and one or more selectors or suppressors.</span></span> <span data-ttu-id="2c92f-115">Un selector contiene una expresión XPath que selecciona los eventos del origen y un supresor contiene una expresión XPath que impide que se seleccionen los eventos.</span><span class="sxs-lookup"><span data-stu-id="2c92f-115">A selector contains an XPath expressions that selects events from the source and a suppressor contains an XPath expression that prevents events from being selected.</span></span> <span data-ttu-id="2c92f-116">Puede seleccionar eventos de más de un origen.</span><span class="sxs-lookup"><span data-stu-id="2c92f-116">You can select events from more than one source.</span></span> <span data-ttu-id="2c92f-117">Si un selector e supresor identifican el mismo evento, el evento no se incluye en el resultado.</span><span class="sxs-lookup"><span data-stu-id="2c92f-117">If a selector and suppressor identify the same event, the event is not included in the result.</span></span>

<span data-ttu-id="2c92f-118">A continuación se muestra una consulta XML estructurada que especifica un conjunto de selectores y suprimidores.</span><span class="sxs-lookup"><span data-stu-id="2c92f-118">The following shows a structured XML query that specifies a set of selectors and suppressors.</span></span>


```XML
<QueryList>
  <Query Id="0">
    <Select Path="Application">
        *[System[(Level <= 3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
    <Suppress Path="Application">
        *[System[(Level = 2)]]
    </Suppress>
    <Select Path="System">
        *[System[(Level=1  or Level=2 or Level=3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
  </Query>
</QueryList>
```



<span data-ttu-id="2c92f-119">El conjunto de resultados de la consulta no contiene una instantánea de los eventos en el momento de la consulta.</span><span class="sxs-lookup"><span data-stu-id="2c92f-119">The result set from the query does not contain a snapshot of the events at the time of the query.</span></span> <span data-ttu-id="2c92f-120">En su lugar, el conjunto de resultados incluye los eventos en el momento de la consulta y también contendrá todos los eventos nuevos que se generan que coinciden con los criterios de consulta mientras se enumeran los resultados.</span><span class="sxs-lookup"><span data-stu-id="2c92f-120">Instead, the result set includes the events at the time of the query and will also contain all new events that are raised that match the query criteria while you are enumerating the results.</span></span>

> [!Note]  
> <span data-ttu-id="2c92f-121">El orden de los eventos se conserva para los eventos que se escriben en el mismo subproceso.</span><span class="sxs-lookup"><span data-stu-id="2c92f-121">The order of the events is preserved for events that are written by the same thread.</span></span> <span data-ttu-id="2c92f-122">Sin embargo, es posible que los eventos escritos por subprocesos independientes en diferentes procesadores de un equipo con varios procesadores parezcan desordenados.</span><span class="sxs-lookup"><span data-stu-id="2c92f-122">However, it is possible for events written by separate threads on different processors of a multiple processor computer to appear out of order.</span></span>

 

<span data-ttu-id="2c92f-123">Para obtener información detallada sobre el consumo de eventos, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="2c92f-123">For details on consuming events, see the following topics:</span></span>

-   [<span data-ttu-id="2c92f-124">Consultar eventos</span><span class="sxs-lookup"><span data-stu-id="2c92f-124">Querying for Events</span></span>](querying-for-events.md)
-   [<span data-ttu-id="2c92f-125">Suscripción a eventos</span><span class="sxs-lookup"><span data-stu-id="2c92f-125">Subscribing to Events</span></span>](subscribing-to-events.md)
-   [<span data-ttu-id="2c92f-126">Representar eventos</span><span class="sxs-lookup"><span data-stu-id="2c92f-126">Rendering Events</span></span>](rendering-events.md)
-   [<span data-ttu-id="2c92f-127">Dar formato a mensajes de eventos</span><span class="sxs-lookup"><span data-stu-id="2c92f-127">Formatting Event Messages</span></span>](formatting-event-messages.md)
-   [<span data-ttu-id="2c92f-128">Marcar eventos</span><span class="sxs-lookup"><span data-stu-id="2c92f-128">Bookmarking Events</span></span>](bookmarking-events.md)

<span data-ttu-id="2c92f-129">Las herramientas estándar de usuario final para el evento de consumo son:</span><span class="sxs-lookup"><span data-stu-id="2c92f-129">The standard end user tools for consuming event are:</span></span>

-   <span data-ttu-id="2c92f-130">[Visor de eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="2c92f-130">[Event Viewer](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))</span></span>
-   <span data-ttu-id="2c92f-131">El cmdlet [Get-WinEvent](/previous-versions//dd367894(v=technet.10)) de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2c92f-131">The Windows PowerShell [Get-WinEvent](/previous-versions//dd367894(v=technet.10)) cmdlet</span></span>
-   [<span data-ttu-id="2c92f-132">**WevtUtil**</span><span class="sxs-lookup"><span data-stu-id="2c92f-132">**WevtUtil**</span></span>](windows-event-log-tools.md)

## <a name="xpath-10-limitations"></a><span data-ttu-id="2c92f-133">Limitaciones de XPath 1,0</span><span class="sxs-lookup"><span data-stu-id="2c92f-133">XPath 1.0 limitations</span></span>

<span data-ttu-id="2c92f-134">El registro de eventos de Windows admite un subconjunto de XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="2c92f-134">Windows Event Log supports a subset of XPath 1.0.</span></span> <span data-ttu-id="2c92f-135">La restricción principal es que solo los elementos XML que representan eventos se pueden seleccionar mediante un selector de eventos.</span><span class="sxs-lookup"><span data-stu-id="2c92f-135">The primary restriction is that only XML elements that represent events can be selected by an event selector.</span></span> <span data-ttu-id="2c92f-136">Una consulta XPath que no selecciona un evento no es válida.</span><span class="sxs-lookup"><span data-stu-id="2c92f-136">An XPath query that does not select an event is not valid.</span></span> <span data-ttu-id="2c92f-137">Todas las rutas de acceso de selector válidas empiezan por \* o "Event".</span><span class="sxs-lookup"><span data-stu-id="2c92f-137">All valid selector paths start with \* or "Event".</span></span> <span data-ttu-id="2c92f-138">Todas las rutas de acceso de ubicación operan en los nodos de eventos y se componen de una serie de pasos.</span><span class="sxs-lookup"><span data-stu-id="2c92f-138">All location paths operate on the event nodes and are composed of a series of steps.</span></span> <span data-ttu-id="2c92f-139">Cada paso es una estructura de tres partes: el eje, la prueba de nodo y el predicado.</span><span class="sxs-lookup"><span data-stu-id="2c92f-139">Each step is a structure of three parts: the axis, node test, and predicate.</span></span> <span data-ttu-id="2c92f-140">Para obtener más información acerca de estas partes y sobre XPath 1,0, consulte [lenguaje de rutas XML (XPath)](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="2c92f-140">For more information about these parts and about XPath 1.0, see [XML Path Language (XPath)](https://www.w3.org/TR/xpath).</span></span> <span data-ttu-id="2c92f-141">El registro de eventos de Windows impone las siguientes restricciones en la expresión:</span><span class="sxs-lookup"><span data-stu-id="2c92f-141">Windows Event Log places the following restrictions on the expression:</span></span>

-   <span data-ttu-id="2c92f-142">AXIS: solo se admiten los valores secundarios (default) y Attribute (y su eje abreviado "@").</span><span class="sxs-lookup"><span data-stu-id="2c92f-142">Axis: Only the Child (default) and Attribute (and its shorthand "@") axis are supported.</span></span>
-   <span data-ttu-id="2c92f-143">Pruebas de nodo: solo se admiten nombres de nodo y pruebas de NCName.</span><span class="sxs-lookup"><span data-stu-id="2c92f-143">Node Tests: Only node names and NCName tests are supported.</span></span> <span data-ttu-id="2c92f-144">\*Se admite el carácter "", que selecciona cualquier carácter.</span><span class="sxs-lookup"><span data-stu-id="2c92f-144">The "\*" character, which selects any character, is supported.</span></span>
-   <span data-ttu-id="2c92f-145">Predicados: cualquier expresión XPath válida es aceptable si las rutas de acceso de ubicación cumplen las restricciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="2c92f-145">Predicates: Any valid XPath expression is acceptable if the location paths conform to the following restrictions:</span></span>
    -   <span data-ttu-id="2c92f-146">Se admiten los operadores estándar **o**, **y**, =,! =, <=, <, >=, > y paréntesis.</span><span class="sxs-lookup"><span data-stu-id="2c92f-146">Standard operators **OR**, **AND**, =, !=, <=, <, >=, >, and parentheses are supported.</span></span>
    -   <span data-ttu-id="2c92f-147">No se admite la generación de un valor de cadena para un nombre de nodo.</span><span class="sxs-lookup"><span data-stu-id="2c92f-147">Generating a string value for a node name is not supported.</span></span>
    -   <span data-ttu-id="2c92f-148">No se admite la evaluación en orden inverso.</span><span class="sxs-lookup"><span data-stu-id="2c92f-148">Evaluation in reverse order is not supported.</span></span>
    -   <span data-ttu-id="2c92f-149">No se admiten conjuntos de nodos.</span><span class="sxs-lookup"><span data-stu-id="2c92f-149">Node sets are not supported.</span></span>
    -   <span data-ttu-id="2c92f-150">No se admite el ámbito de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="2c92f-150">Namespace scoping is not supported.</span></span>
    -   <span data-ttu-id="2c92f-151">No se admiten los nodos de espacio de nombres, procesamiento y comentario.</span><span class="sxs-lookup"><span data-stu-id="2c92f-151">Namespace, processing, and comment nodes are not supported.</span></span>
    -   <span data-ttu-id="2c92f-152">No se admite el tamaño del contexto.</span><span class="sxs-lookup"><span data-stu-id="2c92f-152">Context size is not supported.</span></span>
    -   <span data-ttu-id="2c92f-153">No se admiten los enlaces de variables.</span><span class="sxs-lookup"><span data-stu-id="2c92f-153">Variable bindings are not supported.</span></span>
    -   <span data-ttu-id="2c92f-154">Se admite la función Position y su referencia de matriz abreviada (solo en los nodos hoja).</span><span class="sxs-lookup"><span data-stu-id="2c92f-154">The position function, and its shorthand array reference, is supported (on leaf nodes only).</span></span>
    -   <span data-ttu-id="2c92f-155">Se admite la función de banda.</span><span class="sxs-lookup"><span data-stu-id="2c92f-155">The Band function is supported.</span></span> <span data-ttu-id="2c92f-156">La función realiza una operación and bit a bit para dos argumentos de número entero.</span><span class="sxs-lookup"><span data-stu-id="2c92f-156">The function performs a bitwise AND for two integer number arguments.</span></span> <span data-ttu-id="2c92f-157">Si el resultado de la operación and bit a bit es distinto de cero, la función se evalúa como true; de lo contrario, la función se evalúa como false.</span><span class="sxs-lookup"><span data-stu-id="2c92f-157">If the result of the bitwise AND is nonzero, the function evaluates to true; otherwise, the function evaluates to false.</span></span>
    -   <span data-ttu-id="2c92f-158">Se admite la función timediff.</span><span class="sxs-lookup"><span data-stu-id="2c92f-158">The timediff function is supported.</span></span> <span data-ttu-id="2c92f-159">La función calcula la diferencia entre el segundo argumento y el primer argumento.</span><span class="sxs-lookup"><span data-stu-id="2c92f-159">The function computes the difference between the second argument and the first argument.</span></span> <span data-ttu-id="2c92f-160">Uno de los argumentos debe ser un número literal.</span><span class="sxs-lookup"><span data-stu-id="2c92f-160">One of the arguments must be a literal number.</span></span> <span data-ttu-id="2c92f-161">Los argumentos deben usar la representación de FILETIME.</span><span class="sxs-lookup"><span data-stu-id="2c92f-161">The arguments must use FILETIME representation.</span></span> <span data-ttu-id="2c92f-162">El resultado es el número de milisegundos entre las dos horas.</span><span class="sxs-lookup"><span data-stu-id="2c92f-162">The result is the number of milliseconds between the two times.</span></span> <span data-ttu-id="2c92f-163">El resultado es positivo si el segundo argumento representa una hora posterior; de lo contrario, es negativo.</span><span class="sxs-lookup"><span data-stu-id="2c92f-163">The result is positive if the second argument represents a later time; otherwise, it is negative.</span></span> <span data-ttu-id="2c92f-164">Cuando no se proporciona el segundo argumento, se usa la hora actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="2c92f-164">When the second argument is not provided, the current system time is used.</span></span>

 

 
