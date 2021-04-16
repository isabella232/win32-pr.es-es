---
description: La clase CSystemClock implementa un reloj que devuelve la hora del sistema.
ms.assetid: 22f8b641-6472-433f-bff4-4e62eae25c9b
title: Clase CSystemClock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock
api_type:
- COM
api_location: ''
ms.openlocfilehash: e9cc5e0bde8983cfd8c544d3898d4af628e10f87
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104562294"
---
# <a name="csystemclock-class"></a><span data-ttu-id="2983a-103">Clase CSystemClock</span><span class="sxs-lookup"><span data-stu-id="2983a-103">CSystemClock class</span></span>

![jerarquía de clases csystemclock](images/sclock01.png)

<span data-ttu-id="2983a-105">La `CSystemClock` clase implementa un reloj que devuelve la hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="2983a-105">The `CSystemClock` class implements a clock that returns the system time.</span></span>

<span data-ttu-id="2983a-106">Esta clase se deriva de la clase [**CBaseReferenceClock**](cbasereferenceclock.md) y agrega compatibilidad con las interfaces **IPersist** y [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) .</span><span class="sxs-lookup"><span data-stu-id="2983a-106">This class derives from the [**CBaseReferenceClock**](cbasereferenceclock.md) class, and adds support for the **IPersist** and [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) interfaces.</span></span>



| <span data-ttu-id="2983a-107">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="2983a-107">Public Methods</span></span>                                        | <span data-ttu-id="2983a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="2983a-108">Description</span></span>                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="2983a-109">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="2983a-109">**CreateInstance**</span></span>](csystemclock-createinstance.md) | <span data-ttu-id="2983a-110">Crea una nueva instancia de este objeto.</span><span class="sxs-lookup"><span data-stu-id="2983a-110">Creates a new instance of this object.</span></span>              |
| [<span data-ttu-id="2983a-111">**CSystemClock**</span><span class="sxs-lookup"><span data-stu-id="2983a-111">**CSystemClock**</span></span>](csystemclock-csystemclock.md)     | <span data-ttu-id="2983a-112">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="2983a-112">Constructor method.</span></span>                                 |
| <span data-ttu-id="2983a-113">Métodos IAMClockAdjust</span><span class="sxs-lookup"><span data-stu-id="2983a-113">IAMClockAdjust Methods</span></span>                                | <span data-ttu-id="2983a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2983a-114">Description</span></span>                                         |
| [<span data-ttu-id="2983a-115">**SetClockDelta**</span><span class="sxs-lookup"><span data-stu-id="2983a-115">**SetClockDelta**</span></span>](csystemclock-setclockdelta.md)   | <span data-ttu-id="2983a-116">Ajusta la hora de reloj.</span><span class="sxs-lookup"><span data-stu-id="2983a-116">Adjusts the clock time.</span></span>                             |
| <span data-ttu-id="2983a-117">Métodos IPersist</span><span class="sxs-lookup"><span data-stu-id="2983a-117">IPersist Methods</span></span>                                      | <span data-ttu-id="2983a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="2983a-118">Description</span></span>                                         |
| [<span data-ttu-id="2983a-119">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="2983a-119">**GetClassID**</span></span>](csystemclock-getclassid.md)         | <span data-ttu-id="2983a-120">Devuelve el identificador de clase (CLSID) del objeto.</span><span class="sxs-lookup"><span data-stu-id="2983a-120">Returns the class identifier (CLSID) of the object.</span></span> |



 

 

 



