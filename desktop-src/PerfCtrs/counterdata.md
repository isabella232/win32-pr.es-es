---
description: La tabla de contradatos contiene una fila por cada contador que se recopila en un momento determinado. Habrá un gran número de estas filas.
ms.assetid: 1253a9c7-b440-4ff2-b68c-c52b9b42a58b
title: Datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4604ce9886a6c4e3caa847dcf41a2d50b46d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909745"
---
# <a name="counterdata"></a><span data-ttu-id="5c403-104">Datos</span><span class="sxs-lookup"><span data-stu-id="5c403-104">CounterData</span></span>

<span data-ttu-id="5c403-105">La tabla de **contradatos** contiene una fila por cada contador que se recopila en un momento determinado.</span><span class="sxs-lookup"><span data-stu-id="5c403-105">The **CounterData** table contains a row for each counter that is collected at a particular time.</span></span> <span data-ttu-id="5c403-106">Habrá un gran número de estas filas.</span><span class="sxs-lookup"><span data-stu-id="5c403-106">There will be a large number of these rows.</span></span>

<span data-ttu-id="5c403-107">La tabla de **contradatos** define los campos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5c403-107">The **CounterData** table defines the following fields:</span></span>

-   <span data-ttu-id="5c403-108">**GUID:** GUID para este conjunto de datos.</span><span class="sxs-lookup"><span data-stu-id="5c403-108">**GUID:** GUID for this data set.</span></span> <span data-ttu-id="5c403-109">Use esta clave para combinar con la tabla [**DisplayToID**](displaytoid.md) .</span><span class="sxs-lookup"><span data-stu-id="5c403-109">Use this key to join with the [**DisplayToID**](displaytoid.md) table.</span></span>
-   <span data-ttu-id="5c403-110">**CounterID:** Identifica el contador.</span><span class="sxs-lookup"><span data-stu-id="5c403-110">**CounterID:** Identifies the counter.</span></span> <span data-ttu-id="5c403-111">Use esta clave para combinar con la tabla de [**detalles**](counterdetails.md) .</span><span class="sxs-lookup"><span data-stu-id="5c403-111">Use this key to join with the [**CounterDetails**](counterdetails.md) table.</span></span>
-   <span data-ttu-id="5c403-112">**RecordIndex:** Índice de ejemplo de un identificador de contador específico y un GUID de colección.</span><span class="sxs-lookup"><span data-stu-id="5c403-112">**RecordIndex:** The sample index for a specific counter identifier and collection GUID.</span></span> <span data-ttu-id="5c403-113">El valor aumenta para cada ejemplo sucesivo de este archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="5c403-113">The value increases for each successive sample in this log file.</span></span>
-   <span data-ttu-id="5c403-114">**Contradatetime:** La hora en que se inició la colección, en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="5c403-114">**CounterDateTime:** The time the collection was started, in UTC time.</span></span>
-   <span data-ttu-id="5c403-115">**Contravalor:** Valor con formato del contador.</span><span class="sxs-lookup"><span data-stu-id="5c403-115">**CounterValue:** The formatted value of the counter.</span></span> <span data-ttu-id="5c403-116">Este valor puede ser cero para el primer registro si el contador requiere dos muestras para calcular un valor que se puede mostrar.</span><span class="sxs-lookup"><span data-stu-id="5c403-116">This value may be zero for the first record if the counter requires two sample to compute a displayable value.</span></span>
-   <span data-ttu-id="5c403-117">**FirstValueA:** Combine este valor de 32 bits con el valor de **FirstValueB** para crear el miembro **FirstValue** del [**\_ \_ contador sin formato de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="5c403-117">**FirstValueA:** Combine this 32-bit value with the value of **FirstValueB** to create the **FirstValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="5c403-118">**FirstValueA** contiene los bits de orden inferior.</span><span class="sxs-lookup"><span data-stu-id="5c403-118">**FirstValueA** contains the low order bits.</span></span>
-   <span data-ttu-id="5c403-119">**FirstValueB:** Combine este valor de 32 bits con el valor de **FirstValueA** para crear el miembro **FirstValue** del [**\_ \_ contador sin formato de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="5c403-119">**FirstValueB:** Combine this 32-bit value with the value of **FirstValueA** to create the **FirstValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="5c403-120">**FirstValueB** contiene los bits de orden superior.</span><span class="sxs-lookup"><span data-stu-id="5c403-120">**FirstValueB** contains the high order bits.</span></span>
-   <span data-ttu-id="5c403-121">**SecondValueA:** Combine este valor de 32 bits con el valor de **SecondValueB** para crear el miembro **SecondValue** del [**\_ \_ contador sin formato de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="5c403-121">**SecondValueA:** Combine this 32-bit value with the value of **SecondValueB** to create the **SecondValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="5c403-122">**SecondValueA** contiene los bits de orden inferior.</span><span class="sxs-lookup"><span data-stu-id="5c403-122">**SecondValueA** contains the low order bits.</span></span>
-   <span data-ttu-id="5c403-123">**SecondValueB:** Combine este valor de 32 bits con el valor de **SecondValueA** para crear el miembro **SecondValue** del [**\_ \_ contador sin formato de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="5c403-123">**SecondValueB:** Combine this 32-bit value with the value of **SecondValueA** to create the **SecondValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="5c403-124">**SecondValueB** contiene los bits de orden superior.</span><span class="sxs-lookup"><span data-stu-id="5c403-124">**SecondValueB** contains the high order bits.</span></span>

<span data-ttu-id="5c403-125">Los campos **GUID**, **CounterID** y **RecordIndex** forman la clave principal de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="5c403-125">The **GUID**, **CounterID**, and **RecordIndex** fields make up the primary key for this table.</span></span>

 

 



