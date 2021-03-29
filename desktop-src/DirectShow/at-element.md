---
description: El elemento at define el valor de un elemento Param en un momento determinado, en relación con el inicio de la transición o efecto que contiene el parámetro.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: Elemento at
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb539331519fb23b6b8aa45b374457229f807a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806596"
---
# <a name="at-element"></a><span data-ttu-id="e96fa-103">Elemento at</span><span class="sxs-lookup"><span data-stu-id="e96fa-103">at Element</span></span>

> [!Note]  
> <span data-ttu-id="e96fa-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="e96fa-104">\[Deprecated.</span></span> <span data-ttu-id="e96fa-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e96fa-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e96fa-106">El `at` elemento define el valor de un elemento [**param**](param-element.md) en un momento determinado, en relación con el inicio de la transición o efecto que contiene el parámetro.</span><span class="sxs-lookup"><span data-stu-id="e96fa-106">The `at` element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the parameter.</span></span> <span data-ttu-id="e96fa-107">El `at` elemento hace que el parámetro salte repentinamente al nuevo valor en el momento dado.</span><span class="sxs-lookup"><span data-stu-id="e96fa-107">The `at` element causes the parameter to jump abruptly to the new value at the given time.</span></span> <span data-ttu-id="e96fa-108">Para una progresión fluida a un nuevo valor, use el elemento [**lineal**](linear-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e96fa-108">For a smooth progression to a new value, use the [**linear**](linear-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="e96fa-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="e96fa-109">Attributes</span></span>

<span data-ttu-id="e96fa-110">[**hora**](time-attribute.md), [ **valor**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="e96fa-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="e96fa-111">Información de elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="e96fa-111">Parent/Child Information</span></span>



|          |                                |
|----------|--------------------------------|
| <span data-ttu-id="e96fa-112">Parent</span><span class="sxs-lookup"><span data-stu-id="e96fa-112">Parent</span></span>   | [<span data-ttu-id="e96fa-113">**param**</span><span class="sxs-lookup"><span data-stu-id="e96fa-113">**param**</span></span>](param-element.md) |
| <span data-ttu-id="e96fa-114">Children</span><span class="sxs-lookup"><span data-stu-id="e96fa-114">Children</span></span> | <span data-ttu-id="e96fa-115">None</span><span class="sxs-lookup"><span data-stu-id="e96fa-115">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="e96fa-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e96fa-116">Examples</span></span>


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a><span data-ttu-id="e96fa-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="e96fa-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e96fa-118">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="e96fa-118">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



