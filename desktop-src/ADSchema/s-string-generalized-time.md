---
title: Sintaxis de String (tiempo generalizado)
description: Formato de cadena de hora definido por los estándares ASN. 1. | Sintaxis de String (tiempo generalizado)
ms.assetid: c69ab29b-5877-47d4-b58d-4f103758dfac
ms.tgt_platform: multiple
keywords:
- Esquema de AD de sintaxis de cadena (en tiempo generalizado)
topic_type:
- apiref
api_name:
- String(Generalized-Time)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e754fe622d3ff6f010521b7bc9b9e4ff7a5f34
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280007"
---
# <a name="stringgeneralized-time-syntax"></a><span data-ttu-id="fb05a-105">Sintaxis de String (tiempo generalizado)</span><span class="sxs-lookup"><span data-stu-id="fb05a-105">String(Generalized-Time) syntax</span></span>

<span data-ttu-id="fb05a-106">Formato de cadena de hora definido por los estándares ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="fb05a-106">A time string format defined by ASN.1 standards.</span></span> <span data-ttu-id="fb05a-107">Use esta sintaxis para almacenar valores de hora en Generalized-Time formato.</span><span class="sxs-lookup"><span data-stu-id="fb05a-107">Use this syntax for storing time values in Generalized-Time format.</span></span>

<span data-ttu-id="fb05a-108">El formato de la sintaxis de Generalized-Time es "AAAAMMDDHHMMSS. 0Z".</span><span class="sxs-lookup"><span data-stu-id="fb05a-108">The format for the Generalized-Time syntax is "YYYYMMDDHHMMSS.0Z".</span></span> <span data-ttu-id="fb05a-109">Un ejemplo de un valor aceptable es "20010928060000.0 Z".</span><span class="sxs-lookup"><span data-stu-id="fb05a-109">An example of an acceptable value is "20010928060000.0Z".</span></span> <span data-ttu-id="fb05a-110">La "Z" no indica ninguna diferencia horaria.</span><span class="sxs-lookup"><span data-stu-id="fb05a-110">The "Z" indicates no time differential.</span></span> <span data-ttu-id="fb05a-111">Active Directory almacena la fecha y hora como hora del meridiano de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="fb05a-111">Active Directory stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="fb05a-112">Si no se especifica ninguna diferencia horaria, GMT es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fb05a-112">If no time differential is specified, GMT is the default.</span></span>

<span data-ttu-id="fb05a-113">Si se especifica la hora en una zona horaria distinta de GMT, la diferencia entre la zona horaria y GMT se anexa a la cadena en lugar de a "Z" en la forma "aaaammddhhmmss. 0 \[ +/- \] hhmm".</span><span class="sxs-lookup"><span data-stu-id="fb05a-113">If the time is specified in a time zone other than GMT, the differential between the time zone and GMT is appended to the string instead of "Z" in the form "YYYYMMDDHHMMSS.0\[+/-\]HHMM".</span></span> <span data-ttu-id="fb05a-114">Un ejemplo de un valor aceptable es "20010928060000.0 + 0200".</span><span class="sxs-lookup"><span data-stu-id="fb05a-114">An example of an acceptable value is "20010928060000.0+0200".</span></span> <span data-ttu-id="fb05a-115">La diferencia se basa en la fórmula: GMT = local + diferencial.</span><span class="sxs-lookup"><span data-stu-id="fb05a-115">The differential is based on the formula: GMT=Local+differential.</span></span>

<span data-ttu-id="fb05a-116">Para obtener más información, vea ISO 8601 y X680.</span><span class="sxs-lookup"><span data-stu-id="fb05a-116">For more information, see ISO 8601 and X680.</span></span>



| <span data-ttu-id="fb05a-117">Entrada</span><span class="sxs-lookup"><span data-stu-id="fb05a-117">Entry</span></span> | <span data-ttu-id="fb05a-118">Value</span><span class="sxs-lookup"><span data-stu-id="fb05a-118">Value</span></span> |
|--------------|----------------------------------------------------------------------------|
| <span data-ttu-id="fb05a-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="fb05a-119">Name</span></span>         | <span data-ttu-id="fb05a-120">String(Generalized-Time)</span><span class="sxs-lookup"><span data-stu-id="fb05a-120">String(Generalized-Time)</span></span>                                                   |
| <span data-ttu-id="fb05a-121">IDENTIFICADOR de sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb05a-121">Syntax ID</span></span>    | <span data-ttu-id="fb05a-122">2.5.5.11</span><span class="sxs-lookup"><span data-stu-id="fb05a-122">2.5.5.11</span></span>                                                                   |
| <span data-ttu-id="fb05a-123">IDENTIFICADOR DE OM</span><span class="sxs-lookup"><span data-stu-id="fb05a-123">OM ID</span></span>        | <span data-ttu-id="fb05a-124">24</span><span class="sxs-lookup"><span data-stu-id="fb05a-124">24</span></span>                                                                         |
| <span data-ttu-id="fb05a-125">Tipo MAPI</span><span class="sxs-lookup"><span data-stu-id="fb05a-125">MAPI Type</span></span>    | <span data-ttu-id="fb05a-126">SYSTIME</span><span class="sxs-lookup"><span data-stu-id="fb05a-126">SYSTIME</span></span>                                                                    |
| <span data-ttu-id="fb05a-127">Tipo ADS</span><span class="sxs-lookup"><span data-stu-id="fb05a-127">ADS Type</span></span>     | <span data-ttu-id="fb05a-128">\_hora UTC de ADSTYPE \_</span><span class="sxs-lookup"><span data-stu-id="fb05a-128">ADSTYPE\_UTC\_TIME</span></span>                                                         |
| <span data-ttu-id="fb05a-129">Tipo Variant</span><span class="sxs-lookup"><span data-stu-id="fb05a-129">Variant Type</span></span> | <span data-ttu-id="fb05a-130">fecha de VT \_</span><span class="sxs-lookup"><span data-stu-id="fb05a-130">VT\_DATE</span></span>                                                                   |
| <span data-ttu-id="fb05a-131">Tipo de SDS</span><span class="sxs-lookup"><span data-stu-id="fb05a-131">SDS Type</span></span>     | [<span data-ttu-id="fb05a-132">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="fb05a-132">System.DateTime</span></span>](/dotnet/api/system.datetime) |



## <a name="see-also"></a><span data-ttu-id="fb05a-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb05a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb05a-134">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="fb05a-134">System.DateTime</span></span>](/dotnet/api/system.datetime)
</dt> </dl>

 

 
