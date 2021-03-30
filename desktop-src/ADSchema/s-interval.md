---
title: Sintaxis de Interval
description: Representa un valor de intervalo de tiempo.
ms.assetid: e41b71da-cd05-4a4a-8b97-9210dbe314de
ms.tgt_platform: multiple
keywords:
- Esquema de AD de sintaxis de intervalo
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b92961deecde7faa879dbbda6bfd24560ad705
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104422643"
---
# <a name="interval-syntax"></a><span data-ttu-id="93175-104">Sintaxis de Interval</span><span class="sxs-lookup"><span data-stu-id="93175-104">Interval syntax</span></span>

<span data-ttu-id="93175-105">Representa un valor de intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="93175-105">Represents a time interval value.</span></span> <span data-ttu-id="93175-106">Las unidades de tiempo reales dependen del atributo que usa esta sintaxis.</span><span class="sxs-lookup"><span data-stu-id="93175-106">The actual time units depend on which attribute is using this syntax.</span></span> <span data-ttu-id="93175-107">Esta sintaxis es idéntica a la sintaxis de [**LargeInteger**](s-largeinteger.md) , excepto que los valores altos y bajos son enteros sin signo.</span><span class="sxs-lookup"><span data-stu-id="93175-107">This syntax is identical to the [**LargeInteger**](s-largeinteger.md) syntax, except the high and low values are unsigned integers.</span></span>



| <span data-ttu-id="93175-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="93175-108">Entry</span></span> | <span data-ttu-id="93175-109">Value</span><span class="sxs-lookup"><span data-stu-id="93175-109">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="93175-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="93175-110">Name</span></span>         | <span data-ttu-id="93175-111">Intervalo</span><span class="sxs-lookup"><span data-stu-id="93175-111">Interval</span></span>                                                                           |
| <span data-ttu-id="93175-112">IDENTIFICADOR de sintaxis</span><span class="sxs-lookup"><span data-stu-id="93175-112">Syntax ID</span></span>    | <span data-ttu-id="93175-113">2.5.5.16</span><span class="sxs-lookup"><span data-stu-id="93175-113">2.5.5.16</span></span>                                                                           |
| <span data-ttu-id="93175-114">IDENTIFICADOR DE OM</span><span class="sxs-lookup"><span data-stu-id="93175-114">OM ID</span></span>        | <span data-ttu-id="93175-115">65</span><span class="sxs-lookup"><span data-stu-id="93175-115">65</span></span>                                                                                 |
| <span data-ttu-id="93175-116">Tipo MAPI</span><span class="sxs-lookup"><span data-stu-id="93175-116">MAPI Type</span></span>    | \-                                                                                 |
| <span data-ttu-id="93175-117">Tipo ADS</span><span class="sxs-lookup"><span data-stu-id="93175-117">ADS Type</span></span>     | <span data-ttu-id="93175-118">\_entero grande de ADSTYPE \_</span><span class="sxs-lookup"><span data-stu-id="93175-118">ADSTYPE\_LARGE\_INTEGER</span></span>                                                            |
| <span data-ttu-id="93175-119">Tipo Variant</span><span class="sxs-lookup"><span data-stu-id="93175-119">Variant Type</span></span> | <span data-ttu-id="93175-120">distribución de VT \_</span><span class="sxs-lookup"><span data-stu-id="93175-120">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="93175-121">Tipo de SDS</span><span class="sxs-lookup"><span data-stu-id="93175-121">SDS Type</span></span>     | <span data-ttu-id="93175-122">Objeto COM que se puede convertir en un [**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger).</span><span class="sxs-lookup"><span data-stu-id="93175-122">A COM object that can be cast to an [**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger).</span></span> |



## <a name="see-also"></a><span data-ttu-id="93175-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="93175-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93175-124">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="93175-124">**IADsLargeInteger**</span></span>](/windows/desktop/api/iads/nn-iads-iadslargeinteger)
</dt> <dt>

[<span data-ttu-id="93175-125">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="93175-125">**LargeInteger**</span></span>](s-largeinteger.md)
</dt> </dl>

 

 
