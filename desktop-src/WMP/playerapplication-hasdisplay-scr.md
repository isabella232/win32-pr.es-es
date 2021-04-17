---
title: Atributo PLAYERAPPLICATION. hasDisplay
description: El atributo hasDisplay recupera un valor que indica si el vídeo puede mostrarse a través del control remoto de Windows Media Player.
ms.assetid: c6a735a4-29ae-401c-9381-d8aad2c456eb
keywords:
- PLAYERAPPLICATION. hasDisplay Windows Media Player
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.hasDisplay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7579c724496ee2f36ce12adb01c2f13a0962e7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708753"
---
# <a name="playerapplicationhasdisplay"></a><span data-ttu-id="d921d-104">PLAYERAPPLICATION.hasDisplay</span><span class="sxs-lookup"><span data-stu-id="d921d-104">PLAYERAPPLICATION.hasDisplay</span></span>

<span data-ttu-id="d921d-105">El atributo **hasDisplay** recupera un valor que indica si el vídeo puede mostrarse a través del control remoto de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d921d-105">The **hasDisplay** attribute retrieves a value indicating whether video can display through the remoted Windows Media Player control.</span></span>

``` syntax
        elementID.hasDisplay
```

## <a name="possible-values"></a><span data-ttu-id="d921d-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="d921d-106">Possible Values</span></span>

<span data-ttu-id="d921d-107">Este atributo es un **valor booleano** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d921d-107">This attribute is a read-only **Boolean**.</span></span>



| <span data-ttu-id="d921d-108">Value</span><span class="sxs-lookup"><span data-stu-id="d921d-108">Value</span></span> | <span data-ttu-id="d921d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d921d-109">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="d921d-110">True</span><span class="sxs-lookup"><span data-stu-id="d921d-110">True</span></span>  | <span data-ttu-id="d921d-111">El vídeo se puede mostrar.</span><span class="sxs-lookup"><span data-stu-id="d921d-111">The video can display.</span></span>    |
| <span data-ttu-id="d921d-112">False</span><span class="sxs-lookup"><span data-stu-id="d921d-112">False</span></span> | <span data-ttu-id="d921d-113">No se puede mostrar el vídeo.</span><span class="sxs-lookup"><span data-stu-id="d921d-113">The video cannot display.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d921d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d921d-114">Remarks</span></span>

<span data-ttu-id="d921d-115">Este atributo solo se usa cuando la comunicación remota del control de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="d921d-115">This attribute is used only when remoting the Windows Media Player control.</span></span>

<span data-ttu-id="d921d-116">Varios controles de Windows Media Player se pueden ejecutar de forma remota al mismo tiempo, pero el vídeo solo puede mostrarse en una ubicación a la vez, ya sea en el modo completo del reproductor o en uno de los controles remotos.</span><span class="sxs-lookup"><span data-stu-id="d921d-116">Several Windows Media Player controls can be running remotely at the same time, but video can only display in one location at a time, either in the full mode of the Player or in one of the remoted controls.</span></span> <span data-ttu-id="d921d-117">Utilice esta propiedad para determinar si el control actual es el que se puede mostrar en el vídeo.</span><span class="sxs-lookup"><span data-stu-id="d921d-117">Use this property to determine whether the current control is the one through which video can be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d921d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d921d-118">Requirements</span></span>



| <span data-ttu-id="d921d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d921d-119">Requirement</span></span> | <span data-ttu-id="d921d-120">Value</span><span class="sxs-lookup"><span data-stu-id="d921d-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="d921d-121">Versión</span><span class="sxs-lookup"><span data-stu-id="d921d-121">Version</span></span><br/> | <span data-ttu-id="d921d-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="d921d-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d921d-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d921d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d921d-124">**Elemento PLAYERAPPLICATION**</span><span class="sxs-lookup"><span data-stu-id="d921d-124">**PLAYERAPPLICATION Element**</span></span>](playerapplication-element.md)
</dt> <dt>

[<span data-ttu-id="d921d-125">**Control remoto del Reproductor de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d921d-125">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





