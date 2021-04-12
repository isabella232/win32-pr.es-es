---
description: Las enumeraciones tienden a usar una cantidad significativa de recursos del sistema.
ms.assetid: 4163e6c2-4ee3-4906-b297-618509666c90
ms.tgt_platform: multiple
title: Mejorar el rendimiento de la enumeración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2554e9e1df2f2ece58f5703d6099d84acbe01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277929"
---
# <a name="improving-enumeration-performance"></a><span data-ttu-id="6ddad-103">Mejorar el rendimiento de la enumeración</span><span class="sxs-lookup"><span data-stu-id="6ddad-103">Improving Enumeration Performance</span></span>

<span data-ttu-id="6ddad-104">Las enumeraciones tienden a usar una cantidad significativa de recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="6ddad-104">Enumerations tend to use a significant amount of system resources.</span></span> <span data-ttu-id="6ddad-105">Por lo tanto, debe intentar optimizar el proceso de enumeración de WMI si planea realizar enumeraciones en un grupo de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="6ddad-105">Therefore, you should try to optimize the WMI enumeration process if you plan on performing enumerations on a large group.</span></span> <span data-ttu-id="6ddad-106">Los scripts también pueden usar una consulta para evitar la degradación del rendimiento en las operaciones "for each.... Next" con un conjunto grande.</span><span class="sxs-lookup"><span data-stu-id="6ddad-106">Scripts can also use a query to avoid performance degradation in "For each….Next" operations with a large set.</span></span> <span data-ttu-id="6ddad-107">Para obtener más información, consulte [consultar WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6ddad-107">For more information, see [Querying WMI](querying-wmi.md).</span></span>

<span data-ttu-id="6ddad-108">En el procedimiento siguiente se describe cómo mejorar el rendimiento de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="6ddad-108">The following procedure describes how to improve enumeration performance.</span></span>

<span data-ttu-id="6ddad-109">**Para mejorar el rendimiento de la enumeración**</span><span class="sxs-lookup"><span data-stu-id="6ddad-109">**To improve enumeration performance**</span></span>

1.  <span data-ttu-id="6ddad-110">Establezca el parámetro *lFlags* para permitir la devolución semisincrónica de los datos con un enumerador que descarte cada elemento de WMI cuando se entregue.</span><span class="sxs-lookup"><span data-stu-id="6ddad-110">Set the *lFlags* parameter to allow semisynchronous return of the data with an enumerator that discards each item from WMI as it is delivered.</span></span> <span data-ttu-id="6ddad-111">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="6ddad-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

    <span data-ttu-id="6ddad-112">En el ejemplo de código de C++ siguiente se muestra cómo utilizar la **marca de WBEM devolver las marcas \_ \_ \_ inmediato** y de **WBEM marca de \_ \_ \_ solo avance** .</span><span class="sxs-lookup"><span data-stu-id="6ddad-112">The following C++ code example shows how to use the **WBEM\_FLAG\_RETURN\_IMMEDIATE** and **WBEM\_FLAG\_FORWARD\_ONLY** flags.</span></span>

    `WBEM_FLAG_RETURN_IMMEDIATE | WBEM_FLAG_FORWARD_ONLY`

    <span data-ttu-id="6ddad-113">En VBScript o Visual Basic, use las marcas de scripting **WbemFlagReturnImmediately** y **WbemFlagForwardOnly** de [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span><span class="sxs-lookup"><span data-stu-id="6ddad-113">In VBScript or Visual Basic, use the scripting flags **WbemFlagReturnImmediately** and **WbemFlagForwardOnly** from [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span> <span data-ttu-id="6ddad-114">El valor combinado de estas marcas es decimal 48.</span><span class="sxs-lookup"><span data-stu-id="6ddad-114">The combined value of these flags is decimal 48.</span></span>

    <span data-ttu-id="6ddad-115">Las marcas de scripting y de parámetros producen el siguiente comportamiento:</span><span class="sxs-lookup"><span data-stu-id="6ddad-115">The scripting and parameter flags cause the following behavior:</span></span>

    -   <span data-ttu-id="6ddad-116">La **\_ marca WBEM \_ devuelve \_** el comportamiento semisincrónico de las solicitudes de marca **wbemFlagReturnImmediately** o inmediata.</span><span class="sxs-lookup"><span data-stu-id="6ddad-116">The **WBEM\_FLAG\_RETURN\_IMMEDIATE** or **wbemFlagReturnImmediately** flag requests semisynchronous behavior.</span></span> <span data-ttu-id="6ddad-117">La llamada para crear el enumerador se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="6ddad-117">The call to create the enumerator returns immediately.</span></span> <span data-ttu-id="6ddad-118">A continuación, puede empezar a recorrer el conjunto de objetos que recibe.</span><span class="sxs-lookup"><span data-stu-id="6ddad-118">You can then begin to traverse the object set that you receive.</span></span>
    -   <span data-ttu-id="6ddad-119">La marca **WBEM \_ marca de \_ \_ solo avance** o la marca **wbemFlagForwardOnly** solicita un enumerador que no se puede rebobinar.</span><span class="sxs-lookup"><span data-stu-id="6ddad-119">The **WBEM\_FLAG\_FORWARD\_ONLY** flag or **wbemFlagForwardOnly** flag requests an enumerator that you cannot rewind.</span></span> <span data-ttu-id="6ddad-120">Es decir, WMI puede liberar un objeto después de ver el objeto.</span><span class="sxs-lookup"><span data-stu-id="6ddad-120">That is, WMI can release an object after you view the object.</span></span>

    <span data-ttu-id="6ddad-121">En situaciones en las que la enumeración es grande y la aplicación es muy rápida, el uso de enumeradores de solo avance con procesamiento semisincrónico permite a WMI conservar muchos menos objetos, lo que aumenta significativamente el tiempo de respuesta y el rendimiento de la memoria.</span><span class="sxs-lookup"><span data-stu-id="6ddad-121">In situations where the enumeration is large and the application is very fast, using forward-only enumerators with semisynchronous processing allows WMI to hold on to far fewer objects, thereby increasing response time and memory performance significantly.</span></span>

    <span data-ttu-id="6ddad-122">En el ejemplo de código de VBScript siguiente se muestra cómo hacer una llamada mediante las marcas combinadas **wbemFlagReturnImmediately** y **wbemFlagForwardOnly** para obtener una colección de eventos de un registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="6ddad-122">The following VBScript code example shows how to make a call using the combined **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** flags to obtain a collection of events from an event log.</span></span>

    ```VB
    Set Events = GetObject("winmgmts:").ExecQuery _
         ("SELECT * FROM Win32_NTLogEvent " _
          & "WHERE Logfile = 'System'",,48)
    ```

    

2.  <span data-ttu-id="6ddad-123">Siempre que sea posible, evite usar [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) en C++ o [**SWbemServices. instances**](swbemservices-instancesof.md)y, en su lugar, use **ExecQuery**.</span><span class="sxs-lookup"><span data-stu-id="6ddad-123">Whenever possible, avoid using [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) in C++ or [**SWbemServices.InstancesOf**](swbemservices-instancesof.md), and instead use **ExecQuery**.</span></span>

    <span data-ttu-id="6ddad-124">El método **ExecQuery** consulta a WMI mediante tecnologías de base de datos, mientras que [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) o [**SWbemServices. instances**](swbemservices-instancesof.md) enumera los objetos WMI.</span><span class="sxs-lookup"><span data-stu-id="6ddad-124">The **ExecQuery** method queries WMI using database technologies, while [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) or [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) enumerates WMI objects.</span></span> <span data-ttu-id="6ddad-125">En concreto, **ExecQuery** puede solicitar subconjuntos específicos de datos que los métodos de enumeración no pueden.</span><span class="sxs-lookup"><span data-stu-id="6ddad-125">Specifically, **ExecQuery** can request specific subsets of data that the enumerating methods cannot.</span></span>

    <span data-ttu-id="6ddad-126">Dado que algunos proveedores no tienen capacidades de consulta, WMI proporciona una característica de "filtro posterior" que permite a WMI descartar las instancias que no cumplen las especificaciones de una consulta.</span><span class="sxs-lookup"><span data-stu-id="6ddad-126">Because some providers do not have querying capabilities, WMI provides a "post filter" feature that allows WMI to discard instances that do not fulfill a query's specifications.</span></span> <span data-ttu-id="6ddad-127">Si un determinado proveedor aprovecha esta característica, es el autor del proveedor.</span><span class="sxs-lookup"><span data-stu-id="6ddad-127">Whether a particular provider takes advantage of this feature is up to the provider author.</span></span>

3.  <span data-ttu-id="6ddad-128">Experimente con diferentes consultas para determinar lo que le da el mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="6ddad-128">Experiment with different queries to determine what gives you the best performance.</span></span>

    <span data-ttu-id="6ddad-129">Por ejemplo, WMI raramente procesa las consultas con las cláusulas **Where** con el formato Prop1 < "x".</span><span class="sxs-lookup"><span data-stu-id="6ddad-129">For example, WMI seldom efficiently processes queries with **WHERE** clauses of the form Prop1 < "x".</span></span> <span data-ttu-id="6ddad-130">Por el contrario, WMI normalmente procesa las consultas con el formato KeyProp1 = "x" de manera eficaz.</span><span class="sxs-lookup"><span data-stu-id="6ddad-130">In contrast, WMI normally processes queries of the form KeyProp1 = "x" efficiently.</span></span>

<span data-ttu-id="6ddad-131">Para obtener más información, consulte [enumeración de WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6ddad-131">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

 

 



