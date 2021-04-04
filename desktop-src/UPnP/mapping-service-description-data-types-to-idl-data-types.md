---
title: Asignar tipos de datos de descripción de servicio a tipos de datos IDL
description: En la tabla siguiente se muestra la asignación de los tipos de datos XML especificados en una descripción del servicio a los tipos de datos correspondientes utilizados en IDL.
ms.assetid: eeb86177-8c3b-47f1-bbe1-f9aabd2dde76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b5fac697c41f54279ecde7436900434895ff23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076185"
---
# <a name="mapping-service-description-data-types-to-idl-data-types"></a><span data-ttu-id="af315-103">Asignar tipos de datos de descripción de servicio a tipos de datos IDL</span><span class="sxs-lookup"><span data-stu-id="af315-103">Mapping Service Description Data Types to IDL Data Types</span></span>

<span data-ttu-id="af315-104">En la tabla siguiente se muestra la asignación de los tipos de datos XML especificados en una descripción del servicio a los tipos de datos correspondientes utilizados en IDL.</span><span class="sxs-lookup"><span data-stu-id="af315-104">The following table shows the mapping of XML data types specified in a service description to the corresponding data types used in IDL.</span></span>



| <span data-ttu-id="af315-105">Tipos de datos XML</span><span class="sxs-lookup"><span data-stu-id="af315-105">XML Data Type</span></span> | <span data-ttu-id="af315-106">IDL (tipo de datos)</span><span class="sxs-lookup"><span data-stu-id="af315-106">IDL Data Type</span></span>  |
|---------------|----------------|
| <span data-ttu-id="af315-107">bin.base64</span><span class="sxs-lookup"><span data-stu-id="af315-107">bin.base64</span></span>    | <span data-ttu-id="af315-108">SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="af315-108">SAFEARRAY</span></span>      |
| <span data-ttu-id="af315-109">bin.hex</span><span class="sxs-lookup"><span data-stu-id="af315-109">bin.hex</span></span>       | <span data-ttu-id="af315-110">SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="af315-110">SAFEARRAY</span></span>      |
| <span data-ttu-id="af315-111">boolean</span><span class="sxs-lookup"><span data-stu-id="af315-111">boolean</span></span>       | <span data-ttu-id="af315-112">VARIANTE \_ bool</span><span class="sxs-lookup"><span data-stu-id="af315-112">VARIANT\_BOOL</span></span>  |
| <span data-ttu-id="af315-113">char</span><span class="sxs-lookup"><span data-stu-id="af315-113">char</span></span>          | <span data-ttu-id="af315-114">WCHAR \_ t</span><span class="sxs-lookup"><span data-stu-id="af315-114">wchar\_t</span></span>       |
| <span data-ttu-id="af315-115">date</span><span class="sxs-lookup"><span data-stu-id="af315-115">date</span></span>          | <span data-ttu-id="af315-116">DATE</span><span class="sxs-lookup"><span data-stu-id="af315-116">DATE</span></span>           |
| <span data-ttu-id="af315-117">dateTime</span><span class="sxs-lookup"><span data-stu-id="af315-117">dateTime</span></span>      | <span data-ttu-id="af315-118">DATE</span><span class="sxs-lookup"><span data-stu-id="af315-118">DATE</span></span>           |
| <span data-ttu-id="af315-119">dateTime.tz</span><span class="sxs-lookup"><span data-stu-id="af315-119">dateTime.tz</span></span>   | <span data-ttu-id="af315-120">DATE</span><span class="sxs-lookup"><span data-stu-id="af315-120">DATE</span></span>           |
| <span data-ttu-id="af315-121">fixed.14.4</span><span class="sxs-lookup"><span data-stu-id="af315-121">fixed.14.4</span></span>    | <span data-ttu-id="af315-122">CY</span><span class="sxs-lookup"><span data-stu-id="af315-122">CY</span></span>             |
| <span data-ttu-id="af315-123">FLOAT</span><span class="sxs-lookup"><span data-stu-id="af315-123">float</span></span>         | <span data-ttu-id="af315-124">FLOAT</span><span class="sxs-lookup"><span data-stu-id="af315-124">float</span></span>          |
| <span data-ttu-id="af315-125">i1</span><span class="sxs-lookup"><span data-stu-id="af315-125">i1</span></span>            | <span data-ttu-id="af315-126">char</span><span class="sxs-lookup"><span data-stu-id="af315-126">char</span></span>           |
| <span data-ttu-id="af315-127">i2</span><span class="sxs-lookup"><span data-stu-id="af315-127">i2</span></span>            | <span data-ttu-id="af315-128">short</span><span class="sxs-lookup"><span data-stu-id="af315-128">short</span></span>          |
| <span data-ttu-id="af315-129">i4</span><span class="sxs-lookup"><span data-stu-id="af315-129">i4</span></span>            | <span data-ttu-id="af315-130">long</span><span class="sxs-lookup"><span data-stu-id="af315-130">long</span></span>           |
| <span data-ttu-id="af315-131">int</span><span class="sxs-lookup"><span data-stu-id="af315-131">int</span></span>           | <span data-ttu-id="af315-132">long</span><span class="sxs-lookup"><span data-stu-id="af315-132">long</span></span>           |
| <span data-ttu-id="af315-133">number</span><span class="sxs-lookup"><span data-stu-id="af315-133">number</span></span>        | <span data-ttu-id="af315-134">BSTR</span><span class="sxs-lookup"><span data-stu-id="af315-134">BSTR</span></span>           |
| <span data-ttu-id="af315-135">r4</span><span class="sxs-lookup"><span data-stu-id="af315-135">r4</span></span>            | <span data-ttu-id="af315-136">FLOAT</span><span class="sxs-lookup"><span data-stu-id="af315-136">float</span></span>          |
| <span data-ttu-id="af315-137">r8</span><span class="sxs-lookup"><span data-stu-id="af315-137">r8</span></span>            | <span data-ttu-id="af315-138">double</span><span class="sxs-lookup"><span data-stu-id="af315-138">double</span></span>         |
| <span data-ttu-id="af315-139">string</span><span class="sxs-lookup"><span data-stu-id="af315-139">string</span></span>        | <span data-ttu-id="af315-140">BSTR</span><span class="sxs-lookup"><span data-stu-id="af315-140">BSTR</span></span>           |
| <span data-ttu-id="af315-141">time</span><span class="sxs-lookup"><span data-stu-id="af315-141">time</span></span>          | <span data-ttu-id="af315-142">DATE</span><span class="sxs-lookup"><span data-stu-id="af315-142">DATE</span></span>           |
| <span data-ttu-id="af315-143">time.tz</span><span class="sxs-lookup"><span data-stu-id="af315-143">time.tz</span></span>       | <span data-ttu-id="af315-144">DATE</span><span class="sxs-lookup"><span data-stu-id="af315-144">DATE</span></span>           |
| <span data-ttu-id="af315-145">ui1</span><span class="sxs-lookup"><span data-stu-id="af315-145">ui1</span></span>           | <span data-ttu-id="af315-146">unsigned char</span><span class="sxs-lookup"><span data-stu-id="af315-146">unsigned char</span></span>  |
| <span data-ttu-id="af315-147">ui2</span><span class="sxs-lookup"><span data-stu-id="af315-147">ui2</span></span>           | <span data-ttu-id="af315-148">unsigned short</span><span class="sxs-lookup"><span data-stu-id="af315-148">unsigned short</span></span> |
| <span data-ttu-id="af315-149">ui4</span><span class="sxs-lookup"><span data-stu-id="af315-149">ui4</span></span>           | <span data-ttu-id="af315-150">unsigned long</span><span class="sxs-lookup"><span data-stu-id="af315-150">unsigned long</span></span>  |
| <span data-ttu-id="af315-151">uri</span><span class="sxs-lookup"><span data-stu-id="af315-151">uri</span></span>           | <span data-ttu-id="af315-152">BSTR</span><span class="sxs-lookup"><span data-stu-id="af315-152">BSTR</span></span>           |
| <span data-ttu-id="af315-153">uuid</span><span class="sxs-lookup"><span data-stu-id="af315-153">uuid</span></span>          | <span data-ttu-id="af315-154">BSTR</span><span class="sxs-lookup"><span data-stu-id="af315-154">BSTR</span></span>           |



 

 

 




