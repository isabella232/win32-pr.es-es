---
description: La propiedad CursorType establece o recupera el tipo de cursor actual.
ms.assetid: f362e790-a7c7-4fb6-86f3-7cd25f78fe0e
title: Propiedad CursorType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c17ae74c471bebe6da2bcef4d22d7c247f4eda1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906636"
---
# <a name="cursortype-property"></a><span data-ttu-id="f744c-103">Propiedad CursorType</span><span class="sxs-lookup"><span data-stu-id="f744c-103">CursorType Property</span></span>

> [!Note]  
> <span data-ttu-id="f744c-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f744c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f744c-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="f744c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f744c-106">La `CursorType` propiedad establece o recupera el tipo de cursor actual.</span><span class="sxs-lookup"><span data-stu-id="f744c-106">The `CursorType` property sets or retrieves the current cursor type.</span></span>

``` syntax
[ iCursorType = ] MSWebDVD.CursorType
```

## <a name="return-value"></a><span data-ttu-id="f744c-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f744c-107">Return Value</span></span>

<span data-ttu-id="f744c-108">Devuelve un valor entero que representa el tipo de cursor.</span><span class="sxs-lookup"><span data-stu-id="f744c-108">Returns an integer value representing the cursor type.</span></span>

## <a name="remarks"></a><span data-ttu-id="f744c-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f744c-109">Remarks</span></span>

<span data-ttu-id="f744c-110">Los posibles valores para esta propiedad son:</span><span class="sxs-lookup"><span data-stu-id="f744c-110">The possible values for this property are:</span></span>



| <span data-ttu-id="f744c-111">Value</span><span class="sxs-lookup"><span data-stu-id="f744c-111">Value</span></span> | <span data-ttu-id="f744c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f744c-112">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="f744c-113">0</span><span class="sxs-lookup"><span data-stu-id="f744c-113">0</span></span>     | <span data-ttu-id="f744c-114">Flecha</span><span class="sxs-lookup"><span data-stu-id="f744c-114">Arrow</span></span>       |
| <span data-ttu-id="f744c-115">1</span><span class="sxs-lookup"><span data-stu-id="f744c-115">1</span></span>     | <span data-ttu-id="f744c-116">Acercar</span><span class="sxs-lookup"><span data-stu-id="f744c-116">Zoom In</span></span>     |
| <span data-ttu-id="f744c-117">2</span><span class="sxs-lookup"><span data-stu-id="f744c-117">2</span></span>     | <span data-ttu-id="f744c-118">Alejar</span><span class="sxs-lookup"><span data-stu-id="f744c-118">Zoom Out</span></span>    |
| <span data-ttu-id="f744c-119">3</span><span class="sxs-lookup"><span data-stu-id="f744c-119">3</span></span>     | <span data-ttu-id="f744c-120">Casilla</span><span class="sxs-lookup"><span data-stu-id="f744c-120">Hand</span></span>        |
| <span data-ttu-id="f744c-121">-1</span><span class="sxs-lookup"><span data-stu-id="f744c-121">-1</span></span>    | <span data-ttu-id="f744c-122">None</span><span class="sxs-lookup"><span data-stu-id="f744c-122">None</span></span>        |



 

<span data-ttu-id="f744c-123">Esta propiedad es de lectura/escritura y su valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="f744c-123">This property is read/write with a default value of zero.</span></span> <span data-ttu-id="f744c-124">Cuando se amplía la imagen, si se establece `CursorType` en **Hand** (0X3), la aplicación se coloca en modo de arrastre, lo que permite al usuario desplace la imagen dentro del área de presentación del vídeo.</span><span class="sxs-lookup"><span data-stu-id="f744c-124">When the picture is zoomed in, setting `CursorType` to **Hand** (0x3) puts the application into drag mode, enabling the user to move the image inside the video display area.</span></span>

 

 



