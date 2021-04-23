---
description: El elemento at define el valor de un elemento param en un momento determinado, en relación con el inicio de la transición o el efecto que contiene el parámetro .
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: at (Elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5822f82a349f31f0d4c8de3f522f7f4f3346a08
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909833"
---
# <a name="at-element"></a><span data-ttu-id="15494-103">at (Elemento)</span><span class="sxs-lookup"><span data-stu-id="15494-103">at Element</span></span>

> [!Note]  
> <span data-ttu-id="15494-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="15494-104">\[Deprecated.</span></span> <span data-ttu-id="15494-105">Esta API puede quitarse de futuras versiones de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="15494-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="15494-106">El `at` elemento define el valor de un elemento [**param**](param-element.md) en un momento determinado, en relación con el inicio de la transición o el efecto que contiene el parámetro .</span><span class="sxs-lookup"><span data-stu-id="15494-106">The `at` element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the parameter.</span></span> <span data-ttu-id="15494-107">El `at` elemento hace que el parámetro salte repentinamente al nuevo valor en el momento dado.</span><span class="sxs-lookup"><span data-stu-id="15494-107">The `at` element causes the parameter to jump abruptly to the new value at the given time.</span></span> <span data-ttu-id="15494-108">Para una progresión suave a un nuevo valor, use el [**elemento**](linear-element.md) lineal.</span><span class="sxs-lookup"><span data-stu-id="15494-108">For a smooth progression to a new value, use the [**linear**](linear-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="15494-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="15494-109">Attributes</span></span>

<span data-ttu-id="15494-110">[**time**](time-attribute.md), [ **value**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="15494-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="15494-111">Información de elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="15494-111">Parent/Child Information</span></span>



| <span data-ttu-id="15494-112">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="15494-112">Label</span></span> | <span data-ttu-id="15494-113">Value</span><span class="sxs-lookup"><span data-stu-id="15494-113">Value</span></span> |
|----------|--------------------------------|
| <span data-ttu-id="15494-114">Parent</span><span class="sxs-lookup"><span data-stu-id="15494-114">Parent</span></span>   | [<span data-ttu-id="15494-115">**param**</span><span class="sxs-lookup"><span data-stu-id="15494-115">**param**</span></span>](param-element.md) |
| <span data-ttu-id="15494-116">Children</span><span class="sxs-lookup"><span data-stu-id="15494-116">Children</span></span> | <span data-ttu-id="15494-117">None</span><span class="sxs-lookup"><span data-stu-id="15494-117">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="15494-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="15494-118">Examples</span></span>


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a><span data-ttu-id="15494-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="15494-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15494-120">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="15494-120">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



