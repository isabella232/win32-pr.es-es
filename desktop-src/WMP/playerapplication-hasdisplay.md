---
title: PlayerApplication.hasDisplay
description: La propiedad hasDisplay recupera un valor que indica si el vídeo puede mostrarse a través del control de reproductor remoto.
ms.assetid: f90c5470-f985-4b98-823f-7395f89b238b
keywords:
- PlayerApplication. hasDisplay Windows Media Player
topic_type:
- apiref
api_name:
- PlayerApplication.hasDisplay
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef77cb42109decef6ab435aa031240f89b6cb98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708752"
---
# <a name="playerapplicationhasdisplay"></a><span data-ttu-id="d0c57-104">PlayerApplication.hasDisplay</span><span class="sxs-lookup"><span data-stu-id="d0c57-104">PlayerApplication.hasDisplay</span></span>

<span data-ttu-id="d0c57-105">La propiedad **hasDisplay** recupera un valor que indica si el vídeo puede mostrarse a través del control de reproductor remoto.</span><span class="sxs-lookup"><span data-stu-id="d0c57-105">The **hasDisplay** property retrieves a value indicating whether video can display through the remoted Player control.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0c57-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0c57-106">Syntax</span></span>

<span data-ttu-id="d0c57-107">*playerApplication*. **hasDisplay**</span><span class="sxs-lookup"><span data-stu-id="d0c57-107">*playerApplication*.**hasDisplay**</span></span>

## <a name="possible-values"></a><span data-ttu-id="d0c57-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="d0c57-108">Possible Values</span></span>

<span data-ttu-id="d0c57-109">Esta propiedad es un **valor booleano** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d0c57-109">This property is a read-only **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0c57-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0c57-110">Remarks</span></span>

<span data-ttu-id="d0c57-111">Esta propiedad solo se usa cuando la comunicación remota del control de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="d0c57-111">This property is used only when remoting the Windows Media Player control.</span></span>

<span data-ttu-id="d0c57-112">Varios controles de Windows Media Player se pueden ejecutar de forma remota al mismo tiempo, pero el vídeo solo puede mostrarse en una ubicación a la vez, ya sea en el modo completo del reproductor o en uno de los controles de Windows Media Player remotos.</span><span class="sxs-lookup"><span data-stu-id="d0c57-112">Several Windows Media Player controls can be running remotely at the same time, but video can only display in one location at a time, either in the full mode of the Player or in one of the remoted Windows Media Player controls.</span></span> <span data-ttu-id="d0c57-113">Utilice esta propiedad para determinar si el control actual es el que se puede mostrar en el vídeo.</span><span class="sxs-lookup"><span data-stu-id="d0c57-113">Use this property to determine whether the current control is the one through which video can be displayed.</span></span>

<span data-ttu-id="d0c57-114">**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="d0c57-114">**Windows Media Player 10 Mobile:** This property always returns **true**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0c57-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0c57-115">Requirements</span></span>



| <span data-ttu-id="d0c57-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0c57-116">Requirement</span></span> | <span data-ttu-id="d0c57-117">Value</span><span class="sxs-lookup"><span data-stu-id="d0c57-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c57-118">Versión</span><span class="sxs-lookup"><span data-stu-id="d0c57-118">Version</span></span><br/> | <span data-ttu-id="d0c57-119">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="d0c57-119">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="d0c57-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d0c57-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="d0c57-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0c57-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0c57-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0c57-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c57-123">**Objeto PlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="d0c57-123">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> <dt>

[<span data-ttu-id="d0c57-124">**Control remoto del Reproductor de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d0c57-124">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





