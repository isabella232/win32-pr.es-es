---
title: VER. timerInterval
description: El atributo timerInterval especifica o recupera el intervalo, en milisegundos, en el que el temporizador activa eventos al controlador de eventos de tiempo de actividad.
ms.assetid: 1a69890f-5ea4-493a-8a9e-04fe60a41804
keywords:
- VISTA de Windows Media Player. timerInterval
topic_type:
- apiref
api_name:
- VIEW.timerInterval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790c95fbb2cded134222271d04c4c37dae412b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718642"
---
# <a name="viewtimerinterval"></a><span data-ttu-id="27ac5-104">VER. timerInterval</span><span class="sxs-lookup"><span data-stu-id="27ac5-104">VIEW.timerInterval</span></span>

<span data-ttu-id="27ac5-105">El atributo **timerInterval** especifica o recupera el intervalo, en milisegundos, en el que el temporizador activa eventos al controlador de eventos de **tiempo de actividad** .</span><span class="sxs-lookup"><span data-stu-id="27ac5-105">The **timerInterval** attribute specifies or retrieves the interval, in milliseconds, at which the timer fires events to the **ontimer** event handler.</span></span>

``` syntax
        elementID.timerInterval
```

## <a name="possible-values"></a><span data-ttu-id="27ac5-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="27ac5-106">Possible Values</span></span>

<span data-ttu-id="27ac5-107">Este atributo es un **número** de lectura y escritura (**Long**) con un valor predeterminado de 1000.</span><span class="sxs-lookup"><span data-stu-id="27ac5-107">This attribute is a read/write **Number** (**long**) with a default value of 1000.</span></span>



| <span data-ttu-id="27ac5-108">Value</span><span class="sxs-lookup"><span data-stu-id="27ac5-108">Value</span></span>        | <span data-ttu-id="27ac5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="27ac5-109">Description</span></span>                    |
|--------------|--------------------------------|
| <span data-ttu-id="27ac5-110">0</span><span class="sxs-lookup"><span data-stu-id="27ac5-110">0</span></span>            | <span data-ttu-id="27ac5-111">El evento de temporizador no se activa.</span><span class="sxs-lookup"><span data-stu-id="27ac5-111">The timer event does not fire.</span></span> |
| <span data-ttu-id="27ac5-112">50 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="27ac5-112">50 and above</span></span> | <span data-ttu-id="27ac5-113">Intervalo en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="27ac5-113">The interval in milliseconds.</span></span>  |



 

<span data-ttu-id="27ac5-114">Cualquier valor por debajo de 50 (incluidos los números negativos, pero sin incluir cero) genera un error y se mantiene el valor anterior.</span><span class="sxs-lookup"><span data-stu-id="27ac5-114">Any value below 50 (including negative numbers, but not including zero) generates an error and the previous value is maintained.</span></span>

## <a name="remarks"></a><span data-ttu-id="27ac5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27ac5-115">Remarks</span></span>

<span data-ttu-id="27ac5-116">Esto no se activará automáticamente si no se implementa ningún controlador de eventos de **tiempo de ejecución** .</span><span class="sxs-lookup"><span data-stu-id="27ac5-116">This will not fire automatically if no **ontimer** event handler is implemented.</span></span> <span data-ttu-id="27ac5-117">Por lo tanto, no hay degradación del rendimiento, aunque el valor predeterminado sea distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="27ac5-117">Thus there is no performance degradation even though the default value is nonzero.</span></span>

## <a name="requirements"></a><span data-ttu-id="27ac5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27ac5-118">Requirements</span></span>



| <span data-ttu-id="27ac5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="27ac5-119">Requirement</span></span> | <span data-ttu-id="27ac5-120">Value</span><span class="sxs-lookup"><span data-stu-id="27ac5-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="27ac5-121">Versión</span><span class="sxs-lookup"><span data-stu-id="27ac5-121">Version</span></span><br/> | <span data-ttu-id="27ac5-122">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="27ac5-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="27ac5-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="27ac5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27ac5-124">**Elemento de vista**</span><span class="sxs-lookup"><span data-stu-id="27ac5-124">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="27ac5-125">**VER. tiempo de espera**</span><span class="sxs-lookup"><span data-stu-id="27ac5-125">**VIEW.ontimer**</span></span>](view-ontimer.md)
</dt> </dl>

 

 





