---
description: El lenguaje de consulta de WMI (WQL) es un subconjunto de Lenguaje de consulta estructurado estándar de American National Standards Institute (ANSI SQL) con cambios semánticos menores para admitir WMI.
ms.assetid: 7e04ba37-c0e0-4304-b162-8b911f233f38
ms.tgt_platform: multiple
title: Realizar consultas con WQL
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8e2d3f68f4d7384781110958070b33b67a78405f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696806"
---
# <a name="querying-with-wql"></a><span data-ttu-id="e43ef-103">Realizar consultas con WQL</span><span class="sxs-lookup"><span data-stu-id="e43ef-103">Querying with WQL</span></span>

<span data-ttu-id="e43ef-104">El lenguaje de consulta de WMI (WQL) es un subconjunto de Lenguaje de consulta estructurado estándar de American National Standards Institute (ANSI SQL) con cambios semánticos menores para admitir WMI.</span><span class="sxs-lookup"><span data-stu-id="e43ef-104">The WMI Query Language (WQL) is a subset of standard American National Standards Institute Structured Query Language (ANSI SQL) with minor semantic changes to support WMI.</span></span>

<span data-ttu-id="e43ef-105">Para obtener una lista completa de las palabras clave WQL admitidas, consulte [WQL (SQL para WMI)](wql-sql-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="e43ef-105">For a complete list of supported WQL keywords, see [WQL (SQL for WMI)](wql-sql-for-wmi.md).</span></span> <span data-ttu-id="e43ef-106">El uso de palabras clave SQL para nombres de objeto o propiedad puede impedir que se analice una consulta.</span><span class="sxs-lookup"><span data-stu-id="e43ef-106">Using SQL keywords for object or property names may restrict a query from being parsed.</span></span> <span data-ttu-id="e43ef-107">Las siguientes palabras clave de SQL están restringidas: **null**, **true** y **false**.</span><span class="sxs-lookup"><span data-stu-id="e43ef-107">The following SQL keywords are restricted: **NULL**, **TRUE**, and **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="e43ef-108">Hay límites en el número de palabras clave AND y OR que se pueden usar en las consultas WQL.</span><span class="sxs-lookup"><span data-stu-id="e43ef-108">There are limits to the number of AND and OR keywords that can be used in WQL queries.</span></span> <span data-ttu-id="e43ef-109">Un gran número de palabras clave WQL usadas en una consulta compleja puede hacer que WMI devuelva el código de error de **\_ \_ \_ infracción de la cuota de WBEM E** como un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e43ef-109">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="e43ef-110">El límite de palabras clave de WQL depende de la complejidad de la consulta.</span><span class="sxs-lookup"><span data-stu-id="e43ef-110">The limit of WQL keywords depends on how complex the query is.</span></span>

 

<span data-ttu-id="e43ef-111">Las consultas pueden usar la cláusula **Where** para la extensión y la personalización, aunque no es necesario.</span><span class="sxs-lookup"><span data-stu-id="e43ef-111">Queries can use the **WHERE** clause for extension and customization, although it is not required.</span></span> <span data-ttu-id="e43ef-112">La cláusula **Where** se compone de una propiedad o una palabra clave, un operador y una constante.</span><span class="sxs-lookup"><span data-stu-id="e43ef-112">The **WHERE** clause is made up of a property or keyword, an operator, and a constant.</span></span> <span data-ttu-id="e43ef-113">Todas las cláusulas **Where** deben especificar uno de los operadores predefinidos que se incluyen en WQL.</span><span class="sxs-lookup"><span data-stu-id="e43ef-113">All **WHERE** clauses must specify one of the predefined operators that are included in WQL.</span></span> <span data-ttu-id="e43ef-114">Para obtener más información sobre la sintaxis, vea [cláusula WHERE](where-clause.md).</span><span class="sxs-lookup"><span data-stu-id="e43ef-114">For more information about syntax, see [WHERE Clause](where-clause.md).</span></span> <span data-ttu-id="e43ef-115">Para obtener más información sobre los operadores WQL válidos, vea [operadores WQL](wql-operators.md).</span><span class="sxs-lookup"><span data-stu-id="e43ef-115">For more information about valid WQL operators, see [WQL Operators](wql-operators.md).</span></span>

<span data-ttu-id="e43ef-116">Como con otras cadenas de consulta de SQL, puede hacer que las consultas escapen.</span><span class="sxs-lookup"><span data-stu-id="e43ef-116">As with other SQL query strings, you can escape your queries.</span></span>

> [!Note]  
> <span data-ttu-id="e43ef-117">WQL no admite consultas ni asociaciones entre espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="e43ef-117">WQL does not support cross-namespace queries or associations.</span></span> <span data-ttu-id="e43ef-118">No se puede consultar todas las instancias de una clase especificada que residan en todos los espacios de nombres del equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="e43ef-118">You cannot query for all instances of a specified class residing in all of the namespaces on the target computer.</span></span>

 

<span data-ttu-id="e43ef-119">WQL admite los siguientes tipos de consultas:</span><span class="sxs-lookup"><span data-stu-id="e43ef-119">WQL supports the following types of queries:</span></span>

-   <span data-ttu-id="e43ef-120">Consultas de datos</span><span class="sxs-lookup"><span data-stu-id="e43ef-120">Data queries</span></span>

    <span data-ttu-id="e43ef-121">Las consultas de datos se usan para recuperar instancias de clase y asociaciones de datos.</span><span class="sxs-lookup"><span data-stu-id="e43ef-121">Data queries are used to retrieve class instances and data associations.</span></span> <span data-ttu-id="e43ef-122">Son el tipo de consulta que se usa con más frecuencia en scripts y aplicaciones de WMI.</span><span class="sxs-lookup"><span data-stu-id="e43ef-122">They are the most commonly used type of query in WMI scripts and applications.</span></span> <span data-ttu-id="e43ef-123">Para obtener más información sobre la sintaxis de las consultas de datos, vea [solicitar datos de instancia de clase](requesting-class-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="e43ef-123">For more information about the syntax of data queries, see [Requesting Class Instance Data](requesting-class-instance-data.md).</span></span> <span data-ttu-id="e43ef-124">Para obtener más información sobre las asociaciones, vea [declarar una clase de asociación](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="e43ef-124">For more information about associations, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="e43ef-125">WQL no es compatible con las consultas de tipos de tipo de los tipos de tabla.</span><span class="sxs-lookup"><span data-stu-id="e43ef-125">WQL does not support queries of array datatypes.</span></span>

     

    <span data-ttu-id="e43ef-126">El siguiente ejemplo de consulta de datos solicita el archivo de registro de eventos denominado "Application" de todas las instancias de [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span><span class="sxs-lookup"><span data-stu-id="e43ef-126">The following data query example requests the event log file named "Application" from all instances of [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span>

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_NTLogEvent " _
        & "WHERE Logfile = 'Application'",,48)
    ```

    

-   <span data-ttu-id="e43ef-127">Consultas de eventos</span><span class="sxs-lookup"><span data-stu-id="e43ef-127">Event queries</span></span>

    <span data-ttu-id="e43ef-128">Los consumidores usan consultas de eventos para registrarse para recibir notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="e43ef-128">Consumers use event queries to register to receive notification of events.</span></span> <span data-ttu-id="e43ef-129">Los proveedores de eventos usan consultas de eventos para registrarse y admitir uno o varios eventos.</span><span class="sxs-lookup"><span data-stu-id="e43ef-129">Event providers use event queries to register to support one or more events.</span></span> <span data-ttu-id="e43ef-130">Para obtener más información acerca de las consultas de eventos, consulte [recibir notificaciones de eventos](receiving-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="e43ef-130">For more information about event queries, see [Receiving Event Notifications](receiving-event-notifications.md).</span></span>

    <span data-ttu-id="e43ef-131">La siguiente consulta de eventos de ejemplo de un consumidor de eventos temporal solicita una notificación cuando se crea una nueva instancia de una clase derivada de [**\_ NTLogEvent de Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) .</span><span class="sxs-lookup"><span data-stu-id="e43ef-131">The following example event query by a temporary event consumer requests notification when a new instance of a class derived from [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) is created.</span></span>

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM __InstanceModificationEvent WITHIN 10 WHERE " & _
        "TargetInstance ISA 'Win32_Service'" & _
        " AND TargetInstance._Class = 'win32_TerminalService'")

    i = TRUE
    Do While i = TRUE
        Set strReceivedEvent = objEvents.NextEvent

        'report an event
        Wscript.Echo "An event has occurred."
    Loop
    ```

    

-   <span data-ttu-id="e43ef-132">Consultas de esquema</span><span class="sxs-lookup"><span data-stu-id="e43ef-132">Schema queries</span></span>

    <span data-ttu-id="e43ef-133">Las consultas de esquema se utilizan para recuperar definiciones de clase (en lugar de instancias de clase) y asociaciones de esquema.</span><span class="sxs-lookup"><span data-stu-id="e43ef-133">Schema queries are used to retrieve class definitions (rather than class instances) and schema associations.</span></span> <span data-ttu-id="e43ef-134">Los proveedores de clases utilizan consultas de esquema para especificar las clases que admiten cuando se registran.</span><span class="sxs-lookup"><span data-stu-id="e43ef-134">Class providers use schema queries to specify the classes that they support when they register.</span></span> <span data-ttu-id="e43ef-135">Para obtener más información sobre las consultas de esquema, vea [recuperar definiciones de clase](retrieving-class-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="e43ef-135">For more information about schema queries, see [Retrieving Class Definitions](retrieving-class-definitions.md).</span></span>

    <span data-ttu-id="e43ef-136">En la consulta de esquema de ejemplo siguiente se muestra la sintaxis especial.</span><span class="sxs-lookup"><span data-stu-id="e43ef-136">The following example schema query shows the special syntax.</span></span>

    ```sql
    SELECT * FROM meta_class WHERE __this ISA "Win32_BaseService"
    ```

    

## <a name="related-topics"></a><span data-ttu-id="e43ef-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e43ef-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e43ef-138">Formato de fecha y hora de WMI</span><span class="sxs-lookup"><span data-stu-id="e43ef-138">WMI Date and Time Format</span></span>](date-and-time-format.md)
</dt> </dl>

 

 
