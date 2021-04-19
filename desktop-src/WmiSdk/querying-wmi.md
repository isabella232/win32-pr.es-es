---
description: Una de las principales herramientas de Instrumental de administración de Windows (WMI) es la capacidad de consultar el repositorio WMI para obtener información sobre la clase y la instancia.
ms.assetid: 0cceda42-fba0-4a08-90dd-43f022d0be41
ms.tgt_platform: multiple
title: Consultando WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdae44d4c40e1127bfc4d3436d6230eafd52146a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696804"
---
# <a name="querying-wmi"></a><span data-ttu-id="68fca-103">Consultando WMI</span><span class="sxs-lookup"><span data-stu-id="68fca-103">Querying WMI</span></span>

<span data-ttu-id="68fca-104">Una de las principales herramientas de Instrumental de administración de Windows (WMI) es la capacidad de consultar el repositorio WMI para obtener información sobre la clase y la instancia.</span><span class="sxs-lookup"><span data-stu-id="68fca-104">One of the main tools of Windows Management Instrumentation (WMI) is the ability to query the WMI repository for class and instance information.</span></span> <span data-ttu-id="68fca-105">Por ejemplo, puede solicitar que WMI devuelva todos los objetos que representan los eventos de cierre del sistema de escritorio.</span><span class="sxs-lookup"><span data-stu-id="68fca-105">For example, you can request that WMI return all the objects representing shut-down events from your desktop system.</span></span> <span data-ttu-id="68fca-106">También puede recuperar los datos de la clase, la instancia o el esquema.</span><span class="sxs-lookup"><span data-stu-id="68fca-106">You can also retrieve class, instance, or schema data.</span></span> <span data-ttu-id="68fca-107">En la tabla siguiente se enumeran los diferentes tipos de consultas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="68fca-107">The following table lists the different types of queries you can make.</span></span>



| <span data-ttu-id="68fca-108">Tema</span><span class="sxs-lookup"><span data-stu-id="68fca-108">Topic</span></span>                                                                | <span data-ttu-id="68fca-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="68fca-109">Description</span></span>                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68fca-110">Invocar una consulta sincrónica</span><span class="sxs-lookup"><span data-stu-id="68fca-110">Invoking a Synchronous Query</span></span>](invoking-a-synchronous-query.md)     | <span data-ttu-id="68fca-111">Describe cómo mantener un vínculo con WMI a lo largo del proceso de consulta.</span><span class="sxs-lookup"><span data-stu-id="68fca-111">Describes how to maintain a link with WMI throughout the query process.</span></span> <span data-ttu-id="68fca-112">Las consultas sincrónicas son adecuadas para consultas pequeñas o consultas en un sistema local.</span><span class="sxs-lookup"><span data-stu-id="68fca-112">Synchronous queries are good for small queries or queries to a local system.</span></span><br/>                                  |
| [<span data-ttu-id="68fca-113">Invocar una consulta asincrónica</span><span class="sxs-lookup"><span data-stu-id="68fca-113">Invoking an Asynchronous Query</span></span>](invoking-an-asynchronous-query.md) | <span data-ttu-id="68fca-114">Describe cómo configurar un proceso independiente para recibir consultas.</span><span class="sxs-lookup"><span data-stu-id="68fca-114">Describes how to set up a separate process to receive queries.</span></span> <span data-ttu-id="68fca-115">Las consultas asincrónicas son más complejas y proporcionan un nivel inferior de seguridad, pero, por lo general, mejoran el rendimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="68fca-115">Asynchronous queries are more complex and provide a lower level of security, but generally improve system performance.</span></span><br/> |



 

<span data-ttu-id="68fca-116">Además de consultar el repositorio WMI, también puede usar el [*lenguaje de consulta de WMI (WQL)*](gloss-w.md) para enrutar los eventos de notificación a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="68fca-116">In addition to querying the WMI repository, you can also use the [*WMI Query Language (WQL)*](gloss-w.md) to route notification events to your application.</span></span> <span data-ttu-id="68fca-117">Para obtener más información, consulte [recibir un evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="68fca-117">For more information, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

> [!Note]
>
> <span data-ttu-id="68fca-118">Para consultar correctamente WMI, debe tener una buena comprensión de WQL.</span><span class="sxs-lookup"><span data-stu-id="68fca-118">To properly query WMI, you must have a good understanding of WQL.</span></span> <span data-ttu-id="68fca-119">Una consulta incorrecta, demasiado compleja o inapropiada puede hacer que el procesador de consultas devuelva un error o resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="68fca-119">A query that is incorrect, too complex, or inappropriate can cause the query processor to return an error or unexpected results.</span></span> <span data-ttu-id="68fca-120">Para obtener una guía completa de WQL, vea [consultas con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="68fca-120">For a comprehensive guide to WQL, see [Querying with WQL](querying-with-wql.md).</span></span>
>
> <span data-ttu-id="68fca-121">Hay límites en el número de palabras clave **and** y **or** que se pueden usar en las consultas WQL.</span><span class="sxs-lookup"><span data-stu-id="68fca-121">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="68fca-122">Un gran número de palabras clave WQL usadas en una consulta compleja puede hacer que WMI devuelva el código de error de **\_ \_ \_ infracción de la cuota de WBEM E** como un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="68fca-122">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="68fca-123">El límite de palabras clave de WQL depende de la complejidad de la consulta.</span><span class="sxs-lookup"><span data-stu-id="68fca-123">The limit of WQL keywords depends on how complex the query is.</span></span>
>
> <span data-ttu-id="68fca-124">Al consultar los valores de propiedad con un tipo de datos **UInt64** o **sint64** en un lenguaje de scripting como VBScript, WMI devuelve valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="68fca-124">When querying for property values with a **uint64** or **sint64** data type in a scripting language like VBScript, WMI returns string values.</span></span> <span data-ttu-id="68fca-125">Pueden producirse resultados inesperados al comparar estos valores, ya que la comparación de cadenas devuelve resultados diferentes a los de la comparación de números.</span><span class="sxs-lookup"><span data-stu-id="68fca-125">Unexpected results can occur when comparing these values, because comparing strings returns different results than comparing numbers.</span></span> <span data-ttu-id="68fca-126">Por ejemplo, "10 mil millones" es menor que "9" al comparar cadenas y 9 es inferior a 10 mil millones al comparar números.</span><span class="sxs-lookup"><span data-stu-id="68fca-126">For example, "10000000000" is less than "9" when comparing strings, and 9 is less than 10000000000 when comparing numbers.</span></span> <span data-ttu-id="68fca-127">Para evitar confusiones, debe utilizar el método [CDbl](/previous-versions//ftekwwt0(v=vs.85)) en VBScript cuando las propiedades de tipo **UInt64** o **SINT64** se recuperan de WMI.</span><span class="sxs-lookup"><span data-stu-id="68fca-127">To avoid confusion you should use the [CDbl](/previous-versions//ftekwwt0(v=vs.85)) method in VBScript when properties of type **uint64** or **sint64** are retrieved from WMI.</span></span>

 

> [!Note]  

 

<span data-ttu-id="68fca-128">Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="68fca-128">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

