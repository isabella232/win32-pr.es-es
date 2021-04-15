---
title: Atributo PLAYERAPPLICATION. playerDocked
description: El atributo playerDocked recupera un valor que indica si el Media Player de Windows está en un estado acoplado.
ms.assetid: 8b95da72-037b-4179-a564-fc9bc63368ac
keywords:
- PLAYERAPPLICATION. playerDocked Windows Media Player
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.playerDocked
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21abe3dd5cb14906db39e8eb50a1d18302a92ff6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708870"
---
# <a name="playerapplicationplayerdocked"></a><span data-ttu-id="46287-104">PLAYERAPPLICATION.playerDocked</span><span class="sxs-lookup"><span data-stu-id="46287-104">PLAYERAPPLICATION.playerDocked</span></span>

<span data-ttu-id="46287-105">El atributo **playerDocked** recupera un valor que indica si el Media Player de Windows está en un estado acoplado.</span><span class="sxs-lookup"><span data-stu-id="46287-105">The **playerDocked** attribute retrieves a value indicating whether Windows Media Player is in a docked state.</span></span>

``` syntax
        elementID.playerDocked
```

## <a name="possible-values"></a><span data-ttu-id="46287-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="46287-106">Possible Values</span></span>

<span data-ttu-id="46287-107">Este atributo es un **valor booleano** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="46287-107">This attribute is a read-only **Boolean**.</span></span>



| <span data-ttu-id="46287-108">Value</span><span class="sxs-lookup"><span data-stu-id="46287-108">Value</span></span> | <span data-ttu-id="46287-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="46287-109">Description</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="46287-110">True</span><span class="sxs-lookup"><span data-stu-id="46287-110">True</span></span>  | <span data-ttu-id="46287-111">Windows Media Player está acoplado.</span><span class="sxs-lookup"><span data-stu-id="46287-111">Windows Media Player is docked.</span></span>   |
| <span data-ttu-id="46287-112">False</span><span class="sxs-lookup"><span data-stu-id="46287-112">False</span></span> | <span data-ttu-id="46287-113">Windows Media Player está desacoplado.</span><span class="sxs-lookup"><span data-stu-id="46287-113">Windows Media Player is undocked.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="46287-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46287-114">Remarks</span></span>

<span data-ttu-id="46287-115">Este atributo solo se usa cuando la comunicación remota del control de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="46287-115">This attribute is used only when remoting the Windows Media Player control.</span></span>

## <a name="requirements"></a><span data-ttu-id="46287-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46287-116">Requirements</span></span>



| <span data-ttu-id="46287-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="46287-117">Requirement</span></span> | <span data-ttu-id="46287-118">Value</span><span class="sxs-lookup"><span data-stu-id="46287-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="46287-119">Versión</span><span class="sxs-lookup"><span data-stu-id="46287-119">Version</span></span><br/> | <span data-ttu-id="46287-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="46287-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46287-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="46287-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46287-122">**Elemento PLAYERAPPLICATION**</span><span class="sxs-lookup"><span data-stu-id="46287-122">**PLAYERAPPLICATION Element**</span></span>](playerapplication-element.md)
</dt> <dt>

[<span data-ttu-id="46287-123">**Control remoto del Reproductor de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="46287-123">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





