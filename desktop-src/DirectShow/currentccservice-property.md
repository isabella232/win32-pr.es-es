---
description: La propiedad CurrentCCService establece o recupera el servicio de subtítulos (CC) actual.
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: Propiedad CurrentCCService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5c1ddf243b0ec943be1f22930a8802d28d1bda
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906696"
---
# <a name="currentccservice-property"></a><span data-ttu-id="4b708-103">Propiedad CurrentCCService</span><span class="sxs-lookup"><span data-stu-id="4b708-103">CurrentCCService Property</span></span>

> [!Note]  
> <span data-ttu-id="4b708-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4b708-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4b708-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="4b708-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4b708-106">La `CurrentCCService` propiedad establece o recupera el servicio de subtítulos (CC) actual.</span><span class="sxs-lookup"><span data-stu-id="4b708-106">The `CurrentCCService` property sets or retrieves the current closed captioning service.</span></span>

``` syntax
[ iService = ] MSWebDVD.CurrentCCService
```

## <a name="return-value"></a><span data-ttu-id="4b708-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b708-107">Return Value</span></span>

<span data-ttu-id="4b708-108">Devuelve un valor entero que indica el tipo de servicio de subtítulos (CC) habilitado.</span><span class="sxs-lookup"><span data-stu-id="4b708-108">Returns an integer value indicating the type of closed captioning service enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b708-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b708-109">Remarks</span></span>

<span data-ttu-id="4b708-110">Los valores posibles de esta propiedad son:</span><span class="sxs-lookup"><span data-stu-id="4b708-110">The possible values of this property are:</span></span>



| <span data-ttu-id="4b708-111">Value</span><span class="sxs-lookup"><span data-stu-id="4b708-111">Value</span></span> | <span data-ttu-id="4b708-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b708-112">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="4b708-113">0x0</span><span class="sxs-lookup"><span data-stu-id="4b708-113">0x0</span></span>   | <span data-ttu-id="4b708-114">No hay ningún servicio actual.</span><span class="sxs-lookup"><span data-stu-id="4b708-114">No current service.</span></span> <span data-ttu-id="4b708-115">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4b708-115">This is the default value.</span></span>                       |
| <span data-ttu-id="4b708-116">0x1</span><span class="sxs-lookup"><span data-stu-id="4b708-116">0x1</span></span>   | <span data-ttu-id="4b708-117">Título real, primer campo.</span><span class="sxs-lookup"><span data-stu-id="4b708-117">True captioning, first field.</span></span> <span data-ttu-id="4b708-118">Servicio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4b708-118">Default service.</span></span>                       |
| <span data-ttu-id="4b708-119">0x2</span><span class="sxs-lookup"><span data-stu-id="4b708-119">0x2</span></span>   | <span data-ttu-id="4b708-120">Subtítulos para el segundo campo del idioma secundario.</span><span class="sxs-lookup"><span data-stu-id="4b708-120">Captioning for secondary language, second field.</span></span> <span data-ttu-id="4b708-121">Por lo general, no se usa.</span><span class="sxs-lookup"><span data-stu-id="4b708-121">Generally not used.</span></span> |



 

<span data-ttu-id="4b708-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4b708-122">This property is read/write.</span></span>

## <a name="see-also"></a><span data-ttu-id="4b708-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b708-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b708-124">**CCActive**</span><span class="sxs-lookup"><span data-stu-id="4b708-124">**CCActive**</span></span>](ccactive-property.md)
</dt> </dl>

 

 



