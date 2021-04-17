---
description: El tipo de datos de fecha y hora tiene la hora y la fecha almacenadas individualmente, utilizando enteros sin signo como campos de bits, empaquetados como se indica a continuación.
ms.assetid: 02c6076e-7f81-489c-9997-1435dec81852
title: Time/Date (Fecha y hora)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b973143c2043419e4a54348917aa5d38fa97ff67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652733"
---
# <a name="timedate"></a><span data-ttu-id="f4633-103">Time/Date (Fecha y hora)</span><span class="sxs-lookup"><span data-stu-id="f4633-103">Time/Date</span></span>

<span data-ttu-id="f4633-104">El tipo de datos de fecha y hora tiene la hora y la fecha almacenadas individualmente, utilizando enteros sin signo como campos de bits, empaquetados como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="f4633-104">The Time/Date data type has the time and the date stored individually, using unsigned integers as bit fields, packed as follows.</span></span>

## <a name="time"></a><span data-ttu-id="f4633-105">Hora</span><span class="sxs-lookup"><span data-stu-id="f4633-105">Time</span></span>

<span data-ttu-id="f4633-106">La hora se codifica en un entero de 2 bytes sin signo con los siguientes campos de bits.</span><span class="sxs-lookup"><span data-stu-id="f4633-106">Time is encoded in an unsigned 2-byte integer with the following bit fields.</span></span>



| <span data-ttu-id="f4633-107">Contenido</span><span class="sxs-lookup"><span data-stu-id="f4633-107">Contents</span></span>           | <span data-ttu-id="f4633-108">Bits</span><span class="sxs-lookup"><span data-stu-id="f4633-108">Bits</span></span>        | <span data-ttu-id="f4633-109">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="f4633-109">Value range</span></span> |
|--------------------|-------------|-------------|
| <span data-ttu-id="f4633-110">horas</span><span class="sxs-lookup"><span data-stu-id="f4633-110">hours</span></span>              | <span data-ttu-id="f4633-111">0 1 2 3 4</span><span class="sxs-lookup"><span data-stu-id="f4633-111">0 1 2 3 4</span></span>   | <span data-ttu-id="f4633-112">0–23</span><span class="sxs-lookup"><span data-stu-id="f4633-112">0–23</span></span>        |
| <span data-ttu-id="f4633-113">minutes</span><span class="sxs-lookup"><span data-stu-id="f4633-113">minutes</span></span>            | <span data-ttu-id="f4633-114">5 6 7 8 9 A</span><span class="sxs-lookup"><span data-stu-id="f4633-114">5 6 7 8 9 A</span></span> | <span data-ttu-id="f4633-115">0–59</span><span class="sxs-lookup"><span data-stu-id="f4633-115">0–59</span></span>        |
| <span data-ttu-id="f4633-116">intervalos de 2 segundos</span><span class="sxs-lookup"><span data-stu-id="f4633-116">2-second intervals</span></span> | <span data-ttu-id="f4633-117">B C D E F</span><span class="sxs-lookup"><span data-stu-id="f4633-117">B C D E F</span></span>   | <span data-ttu-id="f4633-118">de 0 a 29</span><span class="sxs-lookup"><span data-stu-id="f4633-118">0–29</span></span>        |



 

## <a name="date"></a><span data-ttu-id="f4633-119">Fecha</span><span class="sxs-lookup"><span data-stu-id="f4633-119">Date</span></span>

<span data-ttu-id="f4633-120">La fecha se codifica en un entero de 2 bytes sin signo con los siguientes campos de bits.</span><span class="sxs-lookup"><span data-stu-id="f4633-120">Date is encoded in an unsigned 2-byte integer with the following bit fields.</span></span>



| <span data-ttu-id="f4633-121">Contenido</span><span class="sxs-lookup"><span data-stu-id="f4633-121">Contents</span></span> | <span data-ttu-id="f4633-122">Bits</span><span class="sxs-lookup"><span data-stu-id="f4633-122">Bits</span></span>          | <span data-ttu-id="f4633-123">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="f4633-123">Value range</span></span>              |
|----------|---------------|--------------------------|
| <span data-ttu-id="f4633-124">year</span><span class="sxs-lookup"><span data-stu-id="f4633-124">year</span></span>     | <span data-ttu-id="f4633-125">0 1 2 3 4 5 6</span><span class="sxs-lookup"><span data-stu-id="f4633-125">0 1 2 3 4 5 6</span></span> | <span data-ttu-id="f4633-126">0 – 119 (con respecto a 1980)</span><span class="sxs-lookup"><span data-stu-id="f4633-126">0–119 (relative to 1980)</span></span> |
| <span data-ttu-id="f4633-127">month</span><span class="sxs-lookup"><span data-stu-id="f4633-127">month</span></span>    | <span data-ttu-id="f4633-128">7 8 9 A</span><span class="sxs-lookup"><span data-stu-id="f4633-128">7 8 9 A</span></span>       | <span data-ttu-id="f4633-129">1–12</span><span class="sxs-lookup"><span data-stu-id="f4633-129">1–12</span></span>                     |
| <span data-ttu-id="f4633-130">day</span><span class="sxs-lookup"><span data-stu-id="f4633-130">day</span></span>      | <span data-ttu-id="f4633-131">B C D E F</span><span class="sxs-lookup"><span data-stu-id="f4633-131">B C D E F</span></span>     | <span data-ttu-id="f4633-132">1–31</span><span class="sxs-lookup"><span data-stu-id="f4633-132">1–31</span></span>                     |



 

 

 



