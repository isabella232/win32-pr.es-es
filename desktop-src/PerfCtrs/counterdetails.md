---
description: En la tabla de detalles se describe un contador específico de un equipo determinado.
ms.assetid: e2a16a6e-8cd4-4fd3-adeb-461faed948e4
title: Detalles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 751073cdc2f2646ad1f2351bff0bdc02c498d428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001984"
---
# <a name="counterdetails"></a><span data-ttu-id="1d728-103">Detalles</span><span class="sxs-lookup"><span data-stu-id="1d728-103">CounterDetails</span></span>

<span data-ttu-id="1d728-104">En la tabla de **detalles** se describe un contador específico de un equipo determinado.</span><span class="sxs-lookup"><span data-stu-id="1d728-104">The **CounterDetails** table describes a specific counter on a particular computer.</span></span>

<span data-ttu-id="1d728-105">En la tabla de **detalles** se definen los campos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1d728-105">The **CounterDetails** table defines the following fields:</span></span>

-   <span data-ttu-id="1d728-106">**CounterID:** Un identificador único en la base de datos que se asigna a una cadena de texto de nombre de contador específico.</span><span class="sxs-lookup"><span data-stu-id="1d728-106">**CounterID:** A unique identifier in the database that maps to a specific counter name text string.</span></span> <span data-ttu-id="1d728-107">Este campo es la clave principal de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="1d728-107">This field is the primary key of this table.</span></span>
-   <span data-ttu-id="1d728-108">**MachineName:** Nombre del equipo que registró este conjunto de datos.</span><span class="sxs-lookup"><span data-stu-id="1d728-108">**MachineName:** The name of the computer that logged this data set.</span></span>
-   <span data-ttu-id="1d728-109">**Objectname:** Nombre del objeto de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="1d728-109">**ObjectName:** The name of the performance object.</span></span>
-   <span data-ttu-id="1d728-110">**Nombre:** Nombre del contador.</span><span class="sxs-lookup"><span data-stu-id="1d728-110">**CounterName:** The name of the counter.</span></span>
-   <span data-ttu-id="1d728-111">**Contratipo:** El tipo de contador.</span><span class="sxs-lookup"><span data-stu-id="1d728-111">**CounterType:** The counter type.</span></span> <span data-ttu-id="1d728-112">Para obtener una lista de los tipos de contador y sus fórmulas, vea la sección tipos de contador del [Kit de implementación de Windows Server 2003](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="1d728-112">For a list of counter types and their formulas, see the Counter Types section of the [Windows Server 2003 Deployment Kit](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).</span></span>
-   <span data-ttu-id="1d728-113">**DefaultScale:** Escalado predeterminado que se va a aplicar a los datos de contador de rendimiento sin procesar.</span><span class="sxs-lookup"><span data-stu-id="1d728-113">**DefaultScale:** The default scaling to be applied to the raw performance counter data.</span></span>
-   <span data-ttu-id="1d728-114">**NombreDeInstancia:** Nombre de la instancia de contador.</span><span class="sxs-lookup"><span data-stu-id="1d728-114">**InstanceName:** The name of the counter instance.</span></span>
-   <span data-ttu-id="1d728-115">**InstanceIndex:** Número de índice de la instancia de contador.</span><span class="sxs-lookup"><span data-stu-id="1d728-115">**InstanceIndex:** The index number of the counter instance.</span></span>
-   <span data-ttu-id="1d728-116">**ParentName:** Algunos contadores están asociados lógicamente a otros y se conocen como elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1d728-116">**ParentName:** Some counters are logically associated with others, and are referred to as parents.</span></span> <span data-ttu-id="1d728-117">Por ejemplo, el elemento primario de un subproceso es un proceso y el primario de un controlador de disco lógico es una unidad física.</span><span class="sxs-lookup"><span data-stu-id="1d728-117">For example, the parent of a thread is a process and the parent of a logical disk driver is a physical drive.</span></span> <span data-ttu-id="1d728-118">Este campo contiene el nombre del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="1d728-118">This field contains the name of the parent.</span></span> <span data-ttu-id="1d728-119">El valor de este campo o el campo **iddeobjetoprincipal** identifica una instancia primaria específica.</span><span class="sxs-lookup"><span data-stu-id="1d728-119">Either the value in this field or the **ParentObjectID** field identifies a specific parent instance.</span></span> <span data-ttu-id="1d728-120">Si el valor de este campo es **null**, se debe comprobar el valor del campo **iddeobjetoprincipal** para identificar el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="1d728-120">If the value in this field is **NULL**, the value in the **ParentObjectID** field must be checked to identify the parent.</span></span> <span data-ttu-id="1d728-121">Si los valores de los dos campos son **null**, el contador no tiene un elemento primario.</span><span class="sxs-lookup"><span data-stu-id="1d728-121">If the values in both fields are **NULL**, the counter does not have a parent.</span></span>
-   <span data-ttu-id="1d728-122">**Iddeobjetoprincipal:** Identificador único del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="1d728-122">**ParentObjectID:** The unique identifier of the parent.</span></span> <span data-ttu-id="1d728-123">El valor de este campo o del campo **ParentName** identifica una instancia primaria específica.</span><span class="sxs-lookup"><span data-stu-id="1d728-123">The value in either this field or the **ParentName** field identifies a specific parent instance.</span></span> <span data-ttu-id="1d728-124">Si el valor de este campo es **null**, se debe comprobar el valor del campo **ParentName** para identificar el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="1d728-124">If the value in this field is **NULL**, the value in the **ParentName** field must be checked to identify the parent.</span></span>

 

 
