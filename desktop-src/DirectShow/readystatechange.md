---
description: El evento ReadyStateChange se envía cuando cambia la propiedad ReadyState del control MSWebDVD.
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: ReadyStateChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46cc8d7ffdee650aac48839d49ed8162e10bb955
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537689"
---
# <a name="readystatechange"></a><span data-ttu-id="1cc77-103">ReadyStateChange</span><span class="sxs-lookup"><span data-stu-id="1cc77-103">ReadyStateChange</span></span>

> [!Note]  
> <span data-ttu-id="1cc77-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1cc77-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="1cc77-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="1cc77-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="1cc77-106">El `ReadyStateChange` evento se envía cuando cambia la propiedad **ReadyState** del control MSWebDVD.</span><span class="sxs-lookup"><span data-stu-id="1cc77-106">The `ReadyStateChange` event is sent when the **ReadyState** property of the MSWebDVD control has changed.</span></span>

``` syntax
ReadyStateChange(ReadyState)
```

## <a name="parameters"></a><span data-ttu-id="1cc77-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cc77-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cc77-108"><span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*ReadyState*</span><span class="sxs-lookup"><span data-stu-id="1cc77-108"><span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*ReadyState*</span></span>
</dt> <dd>

<span data-ttu-id="1cc77-109">Especifica el nuevo valor de la propiedad [**ReadyState**](readystate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="1cc77-109">Specifies the new value of the [**ReadyState**](readystate-property.md) property.</span></span>



| <span data-ttu-id="1cc77-110">Value</span><span class="sxs-lookup"><span data-stu-id="1cc77-110">Value</span></span> | <span data-ttu-id="1cc77-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cc77-111">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="1cc77-112">0</span><span class="sxs-lookup"><span data-stu-id="1cc77-112">0</span></span>     | <span data-ttu-id="1cc77-113">READYSTATE no \_ inicializado</span><span class="sxs-lookup"><span data-stu-id="1cc77-113">READYSTATE\_UNINITIALIZED</span></span> |
| <span data-ttu-id="1cc77-114">1</span><span class="sxs-lookup"><span data-stu-id="1cc77-114">1</span></span>     | <span data-ttu-id="1cc77-115">carga de READYSTATE \_</span><span class="sxs-lookup"><span data-stu-id="1cc77-115">READYSTATE\_LOADING</span></span>       |
| <span data-ttu-id="1cc77-116">2</span><span class="sxs-lookup"><span data-stu-id="1cc77-116">2</span></span>     | <span data-ttu-id="1cc77-117">se \_ cargó READYSTATE</span><span class="sxs-lookup"><span data-stu-id="1cc77-117">READYSTATE\_LOADED</span></span>        |
| <span data-ttu-id="1cc77-118">3</span><span class="sxs-lookup"><span data-stu-id="1cc77-118">3</span></span>     | <span data-ttu-id="1cc77-119">READYSTATE \_ interactivo</span><span class="sxs-lookup"><span data-stu-id="1cc77-119">READYSTATE\_INTERACTIVE</span></span>   |
| <span data-ttu-id="1cc77-120">4</span><span class="sxs-lookup"><span data-stu-id="1cc77-120">4</span></span>     | <span data-ttu-id="1cc77-121">se \_ completó READYSTATE</span><span class="sxs-lookup"><span data-stu-id="1cc77-121">READYSTATE\_COMPLETE</span></span>      |



 

</dd> </dl>

 

 



